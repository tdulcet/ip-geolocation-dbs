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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-06-15<br>IPv6: 2023-06-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.678MiB (5.954MB) – 241,943 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6155741626bdeeecb6810c40716c1352<br>SHA1: 9ab2b65dfc9f5faa014d0bdc926e37c1952b34f4<br>SHA256: 07795c56d8186663c8794f0f46cc54a5cff77143d2084f1df804ec0ea566f5e0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.500MiB (6.816MB) – 84,143 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6721e08fbf655d0257927cf1cae2267e<br>SHA1: 2e23e62cbfb0a0642467e0546be0bbec5b501230<br>SHA256: f1c153d1c7045e2850178f526412339a2124a52d1f432239ae44803e78d18f55</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-06-15<br>IPv6: 2023-06-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.480MiB (9.941MB) – 402,647 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d1d6edce95ffd17d1da70900e0ed696<br>SHA1: f19e9c5c6cb3a98ce7ae16f6dbef72d15cf89f2e<br>SHA256: d47f74794a112b9eeae33f32da49b734e3ecd0f6c2d3615c07a3926c0a3a1009</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.660MiB (8.032MB) – 99,254 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c3fb63b1b9a0ba27aa6573725c6aa17<br>SHA1: d8f73d28ce663f061bfa3fe151262967566985a1<br>SHA256: c97715e5195103460574ebc2e2dbbac854436d1399eb70cff35b8e60119a695f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-06-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.96MiB (14.64MB) – 595,120 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ca0b0e06524b1c2719ba0f8b4ac2389<br>SHA1: 4c534a43fae13561ea0955a396fefd79a1cd1df3<br>SHA256: bcae3f85f985b0e0f40a085606d7b2818c36b9101749a7da1e6c0da0093f5221</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>23.33MiB (24.46MB) – 301,955 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 511269d4f00f525cbd444adb5b0eeb6a<br>SHA1: 472efa2a72056888a9052c608af10d6ccb8315c6<br>SHA256: efda03c4839767f4f1dd5f6e8db88322aed0e13dd00a4181d07c2d6d7fc46d87</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.258MiB (7.611MB) – 310,670 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea16f2b91095213f9faf4261a5404be0<br>SHA1: c745544fc460b4fd9cb1ac68204736bcf9eabf79<br>SHA256: f0ea96ff5e89f5f267e07aa2f74df623e088bcb91f1df0d02845e1c412aeea46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.86MiB (27.12MB) – 334,770 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7634f17216ca6f115cf06e4df5e44bcb<br>SHA1: 60cbd088cb95f3f19ddbebb63ee62aa7d4d5943c<br>SHA256: c3c8f61cd5d80cb8dabda6b047d66bfd6d73c7d0d9eef7427890f9825a480636</pre></details></small> |
| | | Full Location | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,190,306 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f9e88d1ad989b6a665fbfd9d3b82b2<br>SHA1: e1ce63d9dae9f45709cd662cb78d5f323b9caca9<br>SHA256: ca5be0a45d234b5f3db9fd7993ca3b95fb26381d390a4e0d3e8111f2e7922199</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>351.1MiB (368.2MB) – 3,068,912 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4471e6e2accf2b2f3c070f5cb39ed63a<br>SHA1: 158105fcee685e8e94bbff314ca8be8e235b169b<br>SHA256: 82b7025d3a47fff4700bbb503d62d17692265f78fae12837a6995bed2c31d118</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-06-15<br>IPv6: 2023-06-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.582MiB (5.853MB) – 238,084 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1341c73b679015c1849651b02f8442<br>SHA1: 68ca29c935cf40cbfd663086deea4e61d8c8dc4f<br>SHA256: 4124a3662930f11954fa549834f6208912d91c3ddb53382a0c39cfaba1a71bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.40MiB (27.69MB) – 477,002 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2db255cf92eb5224035b1230f0efcc2b<br>SHA1: 4e4c6b67a3842bcdf119210a6676113f6543fa54<br>SHA256: c4335ed7e2c56df30bddbe55d518c81bb73286caae4ae123b4969eca63c72f25</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-06-15<br>IPv6: 2023-06-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,120,022 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1419e77505317334ccdf478ab7daef44<br>SHA1: 1d97a0ac2b0129e4e268083a3cbc23c627acabbe<br>SHA256: 35551439abd88f4346ee7c19bd2da4093eab3273897ca4f28e5cdb1e5d078ee1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.0MiB (399.5MB) – 4,504,439 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e04f9fe903ade529e55bb6b0d36ccdb<br>SHA1: 3f03d09739691bd6ada8c4ee23de98629caf20c3<br>SHA256: 5f023916ba65784e33d23b0934799adf20ae2b5448b40b7bd34e659f96864649</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-06-12<br>IPv6: 2023-06-12 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.760MiB (10.23MB) – 416,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b66684808124854c85e616141ad9fa25<br>SHA1: cdafaf3f04e581adc6bb0d58695fb56980d0b178<br>SHA256: 783ea328bc6084ce67e73bfb8676d48bbb5030bb419b9a68678e3a5f2de7528d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.90MiB (21.92MB) – 270,608 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6aaff78fbc55d64b9196abf41a760b3d<br>SHA1: 51cb56b5eb78addb80641fa2fa6cd1a25fbc20a6<br>SHA256: ddab895b97010df8427a5e1eafa4e4b7bbbbc8e5efbaedca9397160d6e965306</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-06-12<br>IPv6: 2023-06-12 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>188.5MiB (197.7MB) – 3,754,479 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f34d1e353c5295eaf4762d4dfb3819bc<br>SHA1: 1a49b798b1614886a3507a6ba3289a7bd120d028<br>SHA256: 4f7ac90a57c90124ed7a341d8df6e366ec858637f91b628745f0c87b0330ffbf</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>220.8MiB (231.5MB) – 3,754,479 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 751875204f2d081f7eeaafa75ba75440<br>SHA1: 5bbf355ee1ff69743ace321e655f6caca7caab8d<br>SHA256: 916eb02e858bd367dfebb8f1ce5fbffd2aea3915772d03f5e4d6de01e20d3b65</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.3MiB (204.8MB) – 3,754,479 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ce329aea483fb66f4d9a9790e3a2851<br>SHA1: 7d52a593127e90b1b3f0415005e675bce6168f1f<br>SHA256: bf5c2656c6688337af9cfe1f156d44139595351461466e82745002061d31b5aa</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.2MiB (212.1MB) – 3,754,479 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd97d2cf97cce28f35d2d7dda0dd6701<br>SHA1: 68ed21b21c41c6ae5d2a5b1cc4c5dd910331e50c<br>SHA256: eaf018c07ada1741726e7e00ec250a9ac021fb730b9c3e7342e8b0229822703f</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>237.8MiB (249.3MB) – 3,754,479 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ad7e174adca2f92251503f9023fa454<br>SHA1: a808e1237486947d28c953174b9feed5cece837d<br>SHA256: 739f2355fc708fafa304e5f20e6496f7c9e5575f93fbe3c36cb2e34fa3770b9f</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.2MiB (199.4MB) – 3,754,479 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eddf69d70d4914529ec9f4f9ca214e57<br>SHA1: 4cee6a9e5495264f53723ec337e7a463d8a0fc65<br>SHA256: 79fd6cb7e88f6d5185235b18a2bc34c9600c005bf7658ae3c3d07197222fcfc3</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.4MiB (249.9MB) – 3,754,479 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0bd816806431fbe3a619ea15f590245d<br>SHA1: 25de0affb22bb26b35835a0ef9aed895d9d58187<br>SHA256: 43c3601b04ccf8e8172f48451c2ac6d6e88dc7df0bd00d6c044d83e5254bad93</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.3MiB (212.1MB) – 3,754,479 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfceb7db6c90369add2c55d15c48229b<br>SHA1: fc97fe43d85297979f025b4ccf78ee2f78756ff6<br>SHA256: 787c43aa8324e8ba71053313960e0c9213d29fe3d74b83e4d44ee42ec4e0eee5</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.6MiB (131.7MB) – 1,253,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59beec41658e375c6eda7747b14ff0d8<br>SHA1: b9134773bb79ac529288797c2740538e943f507a<br>SHA256: 8573ded65b21709afbaee69f54c768df3332383acbd977cd49af318b78a93b7b</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>133.6MiB (140.1MB) – 1,253,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31d5e53851ecb51c6ca501c5c2eeb71e<br>SHA1: d1de1ef8a940e3f62364d9f479e74856ed02bd0b<br>SHA256: 87dadaab32f81e7a2e6509a7269c8c59044e1d3dfc410baa267f260293d22c8c</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.8MiB (134.0MB) – 1,253,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1c37393c60d55fdbfb26d64fe363236<br>SHA1: 60ba91c7c9177bd095778ece9faed9810b592520<br>SHA256: dd96eb70048e19b44fba7efe6c11f39c22943cfe76203fe7a475aed4a04dfbe0</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>129.6MiB (135.9MB) – 1,253,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb95c55b20b1a1c2349d3a981f2a50da<br>SHA1: cec01376c74ad6e8d563468f4b0d6561ea6fb71b<br>SHA256: 93f90a459816d6d8c1a99f84e93cafc4e45f3f17974d5fd94790f1e0e158777e</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>137.1MiB (143.7MB) – 1,253,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cebc4fddd36026e3011392186a25471<br>SHA1: 886cb6971ef6096a253a6c61398f5334d669c9d3<br>SHA256: a47ad94e7a3e8f3205163ef1f272c037b7335841609eefdcf3544c0d2e52b92e</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>126.9MiB (133.0MB) – 1,253,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5adf9f637847fa73a55c380c31414cb1<br>SHA1: f839614e2a60f637cbab77495053f30452c5d35a<br>SHA256: 2a1d7e34d52fd0f9c44ee9f6f2c1670df74c6ceb21141b57b53984b5b482f07e</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>137.5MiB (144.2MB) – 1,253,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00be299aafe15d68c6fae99e0c59ea6e<br>SHA1: 755be9ad8fcc0a05e1a71ef7019e0dd7ff5c7ae9<br>SHA256: f5b1189e69cc2167a7a5fb0d6682feaf61da212dfcf7db1d24a557f0c703d48d</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>129.8MiB (136.1MB) – 1,253,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 405abeec64567ee194eabc3de65a00e3<br>SHA1: 0883ba631395026e01a34546f86adaccd4d62934<br>SHA256: 7ec10a178c5d338f37344b8ef4cdaa91eb5eb505c221f5772adf308dc86e631f</pre></details></small> |


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
