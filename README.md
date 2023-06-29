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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-06-29<br>IPv6: 2023-06-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.652MiB (5.927MB) – 240,821 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e21a70a91c03a71fbdb1ed8fa87443f<br>SHA1: 1def4cb96324737b88af3b59948a2032ecd132de<br>SHA256: 8ab543fdc47114c2b3895e3e6fec35d7b6bbca27de409dc9a9b638acc8e2424c</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.542MiB (6.860MB) – 84,689 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5853bc2fcd03bd1594abdb36a52526ed<br>SHA1: 9575c0dad83de71e3416600451e969e3ba2953b9<br>SHA256: 322f4260eaa6747ca96cb7a06a3a997364304d4e9e205173256d927c79d1a0c6</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-06-29<br>IPv6: 2023-06-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.492MiB (9.953MB) – 403,142 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 817fe87ff14823fc04f142e22a61a579<br>SHA1: 8aad6d8d7c6fe6fa62fdb79fea29a42d7c308a2a<br>SHA256: 0bd42924c986a55a91e72a528d06044f91ae1095e535face8a7179e402a6736b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.698MiB (8.072MB) – 99,757 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc2f6cd23ec3c143010f3f205c9c3f01<br>SHA1: 33d0ff70500af904ddb40874bd46864f67faaf26<br>SHA256: 2604e62d99286f25f689a81537dad81a185b784850abac2bf48583dcc5ced928</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-06-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.53MiB (15.23MB) – 619,685 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7b378228f877fccea227cf5d8a379d8<br>SHA1: a084dd05533f9c1fa2b6a3164c8dcb9263309f6a<br>SHA256: 507a520b3da408fcbd58df07034dcf32cb07223e1c58a975796d45c4e80f349d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>25.41MiB (26.65MB) – 328,967 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 720fd7b3f641cd1ec5e4e5412e15edd3<br>SHA1: d321840064dd96091a7f40a9e3db8a4477e6ecd4<br>SHA256: dde194f1dbccb16c341f4da7cc39681d3f7b723f0908a1b68e319fa0b7c81d19</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.258MiB (7.611MB) – 310,670 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea16f2b91095213f9faf4261a5404be0<br>SHA1: c745544fc460b4fd9cb1ac68204736bcf9eabf79<br>SHA256: f0ea96ff5e89f5f267e07aa2f74df623e088bcb91f1df0d02845e1c412aeea46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.86MiB (27.12MB) – 334,770 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7634f17216ca6f115cf06e4df5e44bcb<br>SHA1: 60cbd088cb95f3f19ddbebb63ee62aa7d4d5943c<br>SHA256: c3c8f61cd5d80cb8dabda6b047d66bfd6d73c7d0d9eef7427890f9825a480636</pre></details></small> |
| | | Full Location | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,190,306 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f9e88d1ad989b6a665fbfd9d3b82b2<br>SHA1: e1ce63d9dae9f45709cd662cb78d5f323b9caca9<br>SHA256: ca5be0a45d234b5f3db9fd7993ca3b95fb26381d390a4e0d3e8111f2e7922199</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>351.1MiB (368.2MB) – 3,068,912 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4471e6e2accf2b2f3c070f5cb39ed63a<br>SHA1: 158105fcee685e8e94bbff314ca8be8e235b169b<br>SHA256: 82b7025d3a47fff4700bbb503d62d17692265f78fae12837a6995bed2c31d118</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-06-29<br>IPv6: 2023-06-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.582MiB (5.853MB) – 238,084 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1341c73b679015c1849651b02f8442<br>SHA1: 68ca29c935cf40cbfd663086deea4e61d8c8dc4f<br>SHA256: 4124a3662930f11954fa549834f6208912d91c3ddb53382a0c39cfaba1a71bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.40MiB (27.69MB) – 477,002 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2db255cf92eb5224035b1230f0efcc2b<br>SHA1: 4e4c6b67a3842bcdf119210a6676113f6543fa54<br>SHA256: c4335ed7e2c56df30bddbe55d518c81bb73286caae4ae123b4969eca63c72f25</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-06-29<br>IPv6: 2023-06-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,120,022 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1419e77505317334ccdf478ab7daef44<br>SHA1: 1d97a0ac2b0129e4e268083a3cbc23c627acabbe<br>SHA256: 35551439abd88f4346ee7c19bd2da4093eab3273897ca4f28e5cdb1e5d078ee1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.0MiB (399.5MB) – 4,504,439 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e04f9fe903ade529e55bb6b0d36ccdb<br>SHA1: 3f03d09739691bd6ada8c4ee23de98629caf20c3<br>SHA256: 5f023916ba65784e33d23b0934799adf20ae2b5448b40b7bd34e659f96864649</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-06-26<br>IPv6: 2023-06-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.844MiB (10.32MB) – 419,731 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8fde09a55f9b5007cba5614460488b6<br>SHA1: 40441a92a2c84a160e9899cc63781f14b8f3f83c<br>SHA256: ade9f7f0a9c2927470b71e5522d09ff799c621d224d96adc11e591d2885d9d28</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.63MiB (22.68MB) – 279,978 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e07de1fbb7ca89994c9e3579b722c28<br>SHA1: dc9b6c0f02fb2bd507275cf2447950fd852d72a7<br>SHA256: efd25442079378cbc4198249b09ec46b1a15ed64aac8b13de1ba5db28cc34f7b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-06-26<br>IPv6: 2023-06-26 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>188.8MiB (198.0MB) – 3,761,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 331bc731f2c0a114a01ae8172146fe28<br>SHA1: 0af0fcb6c9646bbf6ac9bd35b1eee07d7f459a08<br>SHA256: 33f0f0ed29fd0275f788b4a302b336ced932e0a1ac68ec5105585045b668f0b0</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.0MiB (231.7MB) – 3,761,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aca75ab2c85da0ccfc5b2ba3305bd4e5<br>SHA1: 23ceae819b4d1559668267ac79dbfa96fdf83f12<br>SHA256: 6a723a1973a910f3486b84e60777e0607294fe21e3e43b3efe95da281912666a</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.6MiB (205.1MB) – 3,761,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2db9633415d1c594d56247d12fdc194<br>SHA1: 6497eff4d5c8d592363091e1197ac1f593d5063c<br>SHA256: 1c308b28fdeeba210f77f128dc7f57b52e6fc141b14c2014a330cccc75cef211</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.5MiB (212.3MB) – 3,761,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ced53a49b96f7edb868bb6efcbd8360<br>SHA1: ec5f0899f126708d53163382e3d76dca0ca2b933<br>SHA256: e2d20c150d1bd8b8883b7b2e5cbc84ce2d54d66e9fa00ada4047380557573790</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>237.9MiB (249.5MB) – 3,761,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7b4393ee4916f186fd79568bba82d59<br>SHA1: acaafb7155f14a1db09d38b98b9b3c135eddfd82<br>SHA256: 197e316c2fa75a1f2e02030a59f8787a96326fca4b8f66d345f06eb56c999a8b</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.3MiB (199.6MB) – 3,761,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f73d6b51801a68cb2a776741db908a1<br>SHA1: b7265ab0d44781e9d4f06a6e033ebed3047f2532<br>SHA256: 03546671f2f06c8ff9bc94d00ebca06f0dd0534339685a95462900f44dde6d7e</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.3MiB (249.9MB) – 3,761,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78cf8afdc6c1dcc48b14466b90b0d376<br>SHA1: 08f3fe29239873c5621852d57d2e189a06097857<br>SHA256: f9fcf2cbdc455141b5418af47b7b2be65b680d5d3e61fc955914f8544b2eb08a</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.5MiB (212.3MB) – 3,761,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4e248f3f05457723fa6fadf92bbab9c<br>SHA1: 64a10b2441dd768d4fd9542413567f502c2663c2<br>SHA256: b62d8a355b6be141e323c3f9aea5ae3913df3f39d37806de5f46d03210b111eb</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.6MiB (131.7MB) – 1,254,801 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c5e50a04871237f813f2a107d92e298<br>SHA1: 74ee1cf0e64d8779d5c828bafe420972a0568c8d<br>SHA256: 60cbb1ce84af684036963bdb6e8934ea2decddb84110b3e2e79a27c5814e4981</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>133.7MiB (140.1MB) – 1,254,801 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc01aa01aa9133245ec7a86940843b0a<br>SHA1: 757fa58122991123f3251652892c4e79defa67f4<br>SHA256: 9e02e96e6c8b2339eca596819bd0df0e570447d431b544cb9c32e58158019685</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.8MiB (134.0MB) – 1,254,801 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e04ce0f6dda7345fe8acff71b7f37d4<br>SHA1: 0835152a2ae6d5c39607f63c9010797807aa492b<br>SHA256: 66858ddacc8bc200a11e6b9d1a06fef1ba7792297e95e05886f54086a8bf4798</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>129.6MiB (135.9MB) – 1,254,801 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87509289a86709a4c431437cf6c09ef8<br>SHA1: ccfa679a81c75b335ab0c7fcceff6214112b542b<br>SHA256: 9942cba9e00967580ea6b2984fdd51672f7fb0ff5485c71e99c172a5bff776dc</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>137.1MiB (143.8MB) – 1,254,801 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e32e81eac0f4cd608add60a87c862d13<br>SHA1: a72072e7e0a75917910bf0762c5cf7b0529d3e7d<br>SHA256: e0f9f8ee8868652f3c69e310ebb32e762221a470c6063f1e04d4f7dfda3dbfad</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>126.9MiB (133.1MB) – 1,254,801 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae0adc00bb1ab53d70407441572d0ed4<br>SHA1: d98e021042165ea453ead52e5c02934cf59dfd42<br>SHA256: 8779f3ee586635badd8660b5cd0bd285419ab08bd1a4abe2815c0edc7b10421f</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>137.6MiB (144.3MB) – 1,254,801 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42baa92ad40ec2c8953f20b441c390e7<br>SHA1: 36f46db4255af42660141ae245fc88cf7e2dcb08<br>SHA256: e3712488cb8813e96609636d3cbc9c32787fc39eeb26725cd1b32f1a88467fda</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>129.8MiB (136.2MB) – 1,254,801 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b624e1e5a9b8d3909d9ede98059c3470<br>SHA1: 2f67a37e123a904687d7b6b91fbc0e55383dc265<br>SHA256: bd564cba493c31dc4c210d89e503b43624f60ad0524c831db2c595d550487c2a</pre></details></small> |


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
