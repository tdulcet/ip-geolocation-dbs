[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-06-22<br>IPv6: 2023-06-22 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.679MiB (5.955MB) – 241,996 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fac452b93d168e94d5b73ebab990823c<br>SHA1: 49d7df233fba9f1023dc6a0c41a26477d85ade2a<br>SHA256: 8b87a32dacb08264d78a3dea85be1026c67cf3e46fe30669e9eac4ce84bc9ad6</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.514MiB (6.831MB) – 84,329 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6fb54ea7f96a2cecac9a8c086e9ceae<br>SHA1: 77b6a3cf1ff9c5e9dd3b694107b209000f70e064<br>SHA256: e05533ae07d772ecd707bce278f033a716fcb5637d9f01c2c48bcf3503b6cee1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-06-22<br>IPv6: 2023-06-22 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.487MiB (9.948MB) – 402,937 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f71567aff723ccd1411e28036426676d<br>SHA1: f45d01745cbdb1a9c90ad2eb77c00ba809b964fe<br>SHA256: 56aab4589aa1e96447377acd48ba6d855a806039c31337c0354b0a7ba76d0d85</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.668MiB (8.041MB) – 99,365 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3820b05085ecb3f588c338e1420f953<br>SHA1: c2d832b8dc70881fa93599ed4cbb0560b6fed330<br>SHA256: ac8b1d460748c9138075a8921546543058e013e3416bdd4e85bf41996324e6a5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-06-22 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.08MiB (14.76MB) – 600,387 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d62528754c273e14118f7866fb346bd<br>SHA1: 7b91072a54b329d8ea93382e60a1e8bb00d4d477<br>SHA256: d7cbc8dbd6da153f7d7dabeac69cb0cdb9873a8dd696286e172f8615a60f8a4d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>23.36MiB (24.50MB) – 302,434 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f6944b704b620632774ba1ec2b82f45<br>SHA1: 9a93bcb21e8d21a437e80810304418ea154f04ce<br>SHA256: d5974b134dda15039ffe0ab72829d151e3dcb30db2c6aa18548ac791e3ea73fb</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.258MiB (7.611MB) – 310,670 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea16f2b91095213f9faf4261a5404be0<br>SHA1: c745544fc460b4fd9cb1ac68204736bcf9eabf79<br>SHA256: f0ea96ff5e89f5f267e07aa2f74df623e088bcb91f1df0d02845e1c412aeea46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.86MiB (27.12MB) – 334,770 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7634f17216ca6f115cf06e4df5e44bcb<br>SHA1: 60cbd088cb95f3f19ddbebb63ee62aa7d4d5943c<br>SHA256: c3c8f61cd5d80cb8dabda6b047d66bfd6d73c7d0d9eef7427890f9825a480636</pre></details></small> |
| | | Full Location | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,190,306 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f9e88d1ad989b6a665fbfd9d3b82b2<br>SHA1: e1ce63d9dae9f45709cd662cb78d5f323b9caca9<br>SHA256: ca5be0a45d234b5f3db9fd7993ca3b95fb26381d390a4e0d3e8111f2e7922199</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>351.1MiB (368.2MB) – 3,068,912 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4471e6e2accf2b2f3c070f5cb39ed63a<br>SHA1: 158105fcee685e8e94bbff314ca8be8e235b169b<br>SHA256: 82b7025d3a47fff4700bbb503d62d17692265f78fae12837a6995bed2c31d118</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-06-22<br>IPv6: 2023-06-22 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.582MiB (5.853MB) – 238,084 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1341c73b679015c1849651b02f8442<br>SHA1: 68ca29c935cf40cbfd663086deea4e61d8c8dc4f<br>SHA256: 4124a3662930f11954fa549834f6208912d91c3ddb53382a0c39cfaba1a71bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.40MiB (27.69MB) – 477,002 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2db255cf92eb5224035b1230f0efcc2b<br>SHA1: 4e4c6b67a3842bcdf119210a6676113f6543fa54<br>SHA256: c4335ed7e2c56df30bddbe55d518c81bb73286caae4ae123b4969eca63c72f25</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-06-22<br>IPv6: 2023-06-22 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,120,022 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1419e77505317334ccdf478ab7daef44<br>SHA1: 1d97a0ac2b0129e4e268083a3cbc23c627acabbe<br>SHA256: 35551439abd88f4346ee7c19bd2da4093eab3273897ca4f28e5cdb1e5d078ee1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.0MiB (399.5MB) – 4,504,439 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e04f9fe903ade529e55bb6b0d36ccdb<br>SHA1: 3f03d09739691bd6ada8c4ee23de98629caf20c3<br>SHA256: 5f023916ba65784e33d23b0934799adf20ae2b5448b40b7bd34e659f96864649</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-06-19<br>IPv6: 2023-06-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.828MiB (10.31MB) – 419,059 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0581ddfee02a3df76ba29bf77ffbdaa5<br>SHA1: 3fa057662353dcbe99159c17a52ebbfbc0d7deab<br>SHA256: db3519e74c323f1ea4309a9c1c31a520b3ad6728ceb13ad3d4be49112c2197c1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.93MiB (21.94MB) – 270,926 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2bc6406936d5944939a1fe29ef9549e<br>SHA1: e23949d0bcdc1109bf3b59e072af28ea67477f78<br>SHA256: 01ad3af751c4b4e57b5a3e31698da34f8e6fd78ec547518c24ecccbde50b01e0</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-06-19<br>IPv6: 2023-06-19 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>188.8MiB (198.0MB) – 3,760,957 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dea61d8d275d47b0681193f31f79d4d9<br>SHA1: a9a29dc29d774064f68f969eed1fd115871bd56a<br>SHA256: 4eefe319cab6d931723c2dd419ecb4b5061e82e13cd08a91eb6f8280904d0376</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.0MiB (231.7MB) – 3,760,957 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4350c41f2475ef247eb9072335cb8086<br>SHA1: baca3f1d392e14e982733ba93e5fc15730bcef83<br>SHA256: 08eb3f034e15be342726dca63284a0d25f0ae21ea14a6a06a0376235109404c9</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.5MiB (205.0MB) – 3,760,957 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82453a39a924b3acf6b632771f33f537<br>SHA1: 710c3030bec3a80f4b4925e32dcfc1cdce68cd43<br>SHA256: a1bb86de149d4085e4ed582ed45f7285ec9b50c229c8b6816d80b512d2a98028</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.5MiB (212.3MB) – 3,760,957 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78639d4d2202cb8e2cd811081606489b<br>SHA1: d05c518f55a4a993f075d0077746b41aa174840d<br>SHA256: 235470f6c2d9b8c3d40f912e7d7ff7f402f2cbf99d5813217ed8513acbfd63e0</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>237.9MiB (249.4MB) – 3,760,957 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd963442f089a2e494748f1e43153090<br>SHA1: e8f7cabbddfe1abab1b6304a5c1fb194c7f44e68<br>SHA256: 2f59b0cef0f479b5d90562b9ade5a030eb681739845f75b1ad1951eba737fa7c</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.3MiB (199.6MB) – 3,760,957 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b09f14e56bb58b0f04c681b0a700f006<br>SHA1: 8be4fdac6b697b04ab3c9019132195c1420bb1cb<br>SHA256: 1c78164f6dd1f19df5cb88f35b6446aa08e430e00f3cf81f6aec26c2663c0f4f</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.3MiB (249.8MB) – 3,760,957 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e485d2a014e3ed6a3ec5c6a6476b8c24<br>SHA1: 5824a585327e9634b3a5967933213d3db98d3695<br>SHA256: a84cb7cebcf5eeb93951cecd2bcd16a57ab7697b6e232a586ba78ada7340b1e8</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.4MiB (212.3MB) – 3,760,957 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e690ef615274c9170e2c2ccc25c194f<br>SHA1: 195e404fc63d8cf853f2255abd3c8a2c16ee0563<br>SHA256: 6add07cc2b65c037c33f04ae7a8a852fe544db671f645ad967a357e22b37a4e1</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>126.7MiB (132.9MB) – 1,263,822 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50c24d7fbd37dc33847923ea51a5f89c<br>SHA1: 67c28908dc4b0c91b9b58340bcb797ab36a71790<br>SHA256: d37a20e9bcf172804d5505e18d77ca6b7eb75efee6a3b6a40c7c4c989dc9c64c</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>134.8MiB (141.4MB) – 1,263,822 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19887a772713fdb331faf0f9e4a116f1<br>SHA1: adacaeb3fed5f782e14484cf3560695cc8a373b6<br>SHA256: 98d9e471828d7566c28a1504e30bac3fdbdf2999e4abb6b4ae096a020558964c</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>129.0MiB (135.2MB) – 1,263,822 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eebaddbad1eed9eccf34f51283b4e4de<br>SHA1: 8f3f897ac67627d57dc67383b3fc6ab547ed8f87<br>SHA256: 0d39934f5ed6a69d806b371014a1ab95adcddc3870da5565e0d1fcee0897ac78</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>130.8MiB (137.2MB) – 1,263,822 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91a5ee4476b1c5e3bf4de22b0028628e<br>SHA1: cceea384ce0117906a11c0edc1931c6ad329fca2<br>SHA256: 9e4a627b9edb350aad8a3e3cb32469de0723ff37103bc6ae00bdfc4392de74a5</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>138.5MiB (145.3MB) – 1,263,822 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17776cb3b72c27ede39381045db4cbc2<br>SHA1: 7d016dda3ca24be8b821ebab2a929e8a823b2410<br>SHA256: 27a4d6ea075d647fd4d0f588bd64eaf20234b85a070b9a1b5a5f3e8c4d8fae16</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>128.0MiB (134.2MB) – 1,263,822 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96f7cf4b3dd71ad03be24ad01372daa4<br>SHA1: ddcf8f17b46350982fbfbb1d13aa70471273bf33<br>SHA256: 6b9bec3379746b643391bc32762415cac3056791987d508c874bad02d91b7b96</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>139.0MiB (145.7MB) – 1,263,822 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b4f9695a0519ac72d1f1fb598735c66<br>SHA1: ebb6fa28e70844d6014c0e111a96fab5e36840e9<br>SHA256: bc79ea1604191ba7e71d307634a4092186962c4d3b2c33e27133bc67a1217223</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>131.0MiB (137.4MB) – 1,263,822 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 961f16c9454061a47408b543d2e0c4b8<br>SHA1: 494751bedce2d87c90cc67790c61420822613e45<br>SHA256: 2a549990dd670ef36e7d09d884e702d26bb4e0e1f45ff3a9941e4d169bf4328c</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hex format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
