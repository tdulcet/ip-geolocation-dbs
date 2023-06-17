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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-06-17<br>IPv6: 2023-06-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.680MiB (5.956MB) – 241,998 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d31ace22bd7b2f68acdd4eaadeeffeff<br>SHA1: a0c8116fef035aa7b8a1903f108ef76a3393f377<br>SHA256: 42985e06fb2e9becf2d6a6dcbcfc655fb3b0c362c36b6ad3d0c50fcdfd5f626b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.506MiB (6.822MB) – 84,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe6bd6be9d272a4e96221960793dc9de<br>SHA1: 0c1f9c42ee772042b0422e1600e75c51f6082c5a<br>SHA256: 908d17ba5eb1ec978f1fc0eda2e2fe78ccd7732a8377790d1faf41b9c33a9933</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-06-17<br>IPv6: 2023-06-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.480MiB (9.941MB) – 402,653 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 673ff6c9bf92990edf55fb106aa582db<br>SHA1: 04a7a179c60017cb817c190df250547f4c83d6f1<br>SHA256: 19f4edd3f6591f0c3c4d9a72cd6a7fda937ba650a5194a247778be98e90e1c94</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.670MiB (8.042MB) – 99,387 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25bdd4b831253f54eed184a177c31e20<br>SHA1: f828fe07a5618d9b1ed2621c87ef8f136aa18883<br>SHA256: 3aead0f96e456b7542f4be3efe164673dd357192b2836f8cd1ff7b043013077b</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-06-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.00MiB (14.68MB) – 596,653 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7640ac87a40e8827d7f672b1a5f8af18<br>SHA1: 587c2b8ca3eebc2af022917f1c374fc727d6ca2c<br>SHA256: dcbdf7c8b92d9bdec39757ba7143f66fe41d8846c4614b71e8b1bc6ec9fcc209</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>23.04MiB (24.16MB) – 298,277 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c00afe3e0d5e5686afa4bd700c832d4<br>SHA1: d232e2bc3c0ab7a15ebaf9221cf2dbfbd3a0c043<br>SHA256: a10e77e9b88f8911f2c5de74bc18a21db789b05afa173af988ea9213c2b00abf</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.258MiB (7.611MB) – 310,670 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea16f2b91095213f9faf4261a5404be0<br>SHA1: c745544fc460b4fd9cb1ac68204736bcf9eabf79<br>SHA256: f0ea96ff5e89f5f267e07aa2f74df623e088bcb91f1df0d02845e1c412aeea46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.86MiB (27.12MB) – 334,770 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7634f17216ca6f115cf06e4df5e44bcb<br>SHA1: 60cbd088cb95f3f19ddbebb63ee62aa7d4d5943c<br>SHA256: c3c8f61cd5d80cb8dabda6b047d66bfd6d73c7d0d9eef7427890f9825a480636</pre></details></small> |
| | | Full Location | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,190,306 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f9e88d1ad989b6a665fbfd9d3b82b2<br>SHA1: e1ce63d9dae9f45709cd662cb78d5f323b9caca9<br>SHA256: ca5be0a45d234b5f3db9fd7993ca3b95fb26381d390a4e0d3e8111f2e7922199</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>351.1MiB (368.2MB) – 3,068,912 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4471e6e2accf2b2f3c070f5cb39ed63a<br>SHA1: 158105fcee685e8e94bbff314ca8be8e235b169b<br>SHA256: 82b7025d3a47fff4700bbb503d62d17692265f78fae12837a6995bed2c31d118</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-06-17<br>IPv6: 2023-06-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.582MiB (5.853MB) – 238,084 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1341c73b679015c1849651b02f8442<br>SHA1: 68ca29c935cf40cbfd663086deea4e61d8c8dc4f<br>SHA256: 4124a3662930f11954fa549834f6208912d91c3ddb53382a0c39cfaba1a71bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.40MiB (27.69MB) – 477,002 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2db255cf92eb5224035b1230f0efcc2b<br>SHA1: 4e4c6b67a3842bcdf119210a6676113f6543fa54<br>SHA256: c4335ed7e2c56df30bddbe55d518c81bb73286caae4ae123b4969eca63c72f25</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-06-17<br>IPv6: 2023-06-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,120,022 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1419e77505317334ccdf478ab7daef44<br>SHA1: 1d97a0ac2b0129e4e268083a3cbc23c627acabbe<br>SHA256: 35551439abd88f4346ee7c19bd2da4093eab3273897ca4f28e5cdb1e5d078ee1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.0MiB (399.5MB) – 4,504,439 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e04f9fe903ade529e55bb6b0d36ccdb<br>SHA1: 3f03d09739691bd6ada8c4ee23de98629caf20c3<br>SHA256: 5f023916ba65784e33d23b0934799adf20ae2b5448b40b7bd34e659f96864649</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-06-15<br>IPv6: 2023-06-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.780MiB (10.25MB) – 416,982 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0548cd28b136985d312f85b6a202c010<br>SHA1: 66f28aefa43a688f4f74a97635c5f4b58b66d6ce<br>SHA256: d5ae6e41915da356630ac86174b6d276b85519f706def17b6123fbe7c7611f51</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.93MiB (21.95MB) – 270,935 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 779e8d988a9a61319b9ac28858769a28<br>SHA1: b448feb57c32f901588f87e5304a72fde0f1f732<br>SHA256: a0e6f915c9345562a5e3ae32ef5c4781bc74d781448a74b491d4cc151df5b80a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-06-15<br>IPv6: 2023-06-15 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>188.7MiB (197.9MB) – 3,757,563 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46eef0a9a318eb9d3538628aeec5cb5e<br>SHA1: d1a7fa0e1495089a5f3cf203e1753ea196ef309c<br>SHA256: 992189b9fea7372edd747f0c5939f047347095f50c0a68c87f269f7b9caf6ef1</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>220.9MiB (231.7MB) – 3,757,563 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ec61029e04de362660222207ad7398b<br>SHA1: 5f55ebb7845aa2794f98b7ab15589c0d0e4c2c64<br>SHA256: 89a9f589bca06bd153a5b29e3eed8964252a2806e3f9a895584ff9dc6de8dfb1</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.5MiB (205.0MB) – 3,757,563 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de7e77803cf2c590edff07fa9be1ef25<br>SHA1: 16cd2987f1f1679983a84e12d46cd373e1a10717<br>SHA256: 9873f27ce4d3f06d34fc8ab60808ec73b39670bd80ce94386284cf5833ba8de9</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.4MiB (212.2MB) – 3,757,563 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a35661a31c304d29379049a74ef09b01<br>SHA1: d1663e169dac1f489cd086a7e81873774fdf98c4<br>SHA256: d4613528c38203c23072783adde066d904574352281216d6c1c370c314f72116</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.0MiB (249.6MB) – 3,757,563 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78e872bd22d9d46e281d1769c4c9d43d<br>SHA1: 38fa96cdddc57d39a857520ccc90f41efee31708<br>SHA256: 2240dbc61aff95d21f5ac4dd339944eb82054f5ea0faa5287685c190951ca2bd</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.4MiB (199.6MB) – 3,757,563 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a3865a4143e4c2928fb14d6a20a81f<br>SHA1: 9f7b037a8f5cd3eef6eb9bf10d85e57820036e8c<br>SHA256: 91590592c69d061d8c430b65b48f853d54b80bb70967ddd00eb89edb524e3f2c</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.5MiB (250.0MB) – 3,757,563 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4cf4a86b8bfef8485e0329932e71c1c<br>SHA1: 8295e5292c34a018787f6ebebc16eef34e8f07f8<br>SHA256: 513e7390aacf69fce486742a8f31270a1e18d4306b08cac2f6b8aca3e462d6c1</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.5MiB (212.3MB) – 3,757,563 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b48eb28d600fcc81defc617eebcf9fcd<br>SHA1: 5d08eed3e2219f4d43abe25cb525469b990e7117<br>SHA256: 81774f2f3c7a95068b0800d543878bbdefdfdf12e4cb7160581644c477976f76</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.7MiB (131.8MB) – 1,254,769 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38ce60e853c0b6400c09c9bdb7b26fe2<br>SHA1: e010bde4dd3f5a7adb009c704b9614cdfdbd4829<br>SHA256: 8edd300234f82e3fae52489ec1b0de7352c12a70e9172c76ba380d24541ed5b8</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>133.7MiB (140.2MB) – 1,254,769 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aadecbe0cc8831e28f5d414d0f3dd49f<br>SHA1: c9be828488407eda2e9bcfb59544bd1fdca0f6bb<br>SHA256: 074914d8a9875aa435d4832f34786635fc2455ec9aaa63ce4242d4a57f42a25a</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.9MiB (134.1MB) – 1,254,769 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 180e8c30726c574b993a407f88e2f419<br>SHA1: 221022498c3b54c22092e0d8ef1fabfbb5a52807<br>SHA256: c0848f24f9cf9990054d2da59906b0a9c0aa142767fe611346fe80ce51a92620</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>129.7MiB (136.0MB) – 1,254,769 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0456aec781618695470daa4a4253c03<br>SHA1: dd2692e2aa68c2528b50e3523f73848bb69b2a1b<br>SHA256: 44b3f3d3487e1c161886a7e24e740f8744b45fa595709156f886660fb3210d42</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>137.3MiB (143.9MB) – 1,254,769 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9ee8cd6d7a0df37927fb3e68c0dc5b7<br>SHA1: 4478e9e0cb9746c60b34320038a981f1b7ca29b7<br>SHA256: 4e5505c7bca961df0aea4ed1b5c00ab685e184908ba8c7ca8137ed413ddd420b</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>127.0MiB (133.2MB) – 1,254,769 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1771032189567fd4647dfb8af0017bc2<br>SHA1: bdc4bc5fe3a103cc541b49098e2eab29b22c1577<br>SHA256: d271eba72cd2a0f8665f818a4748f58ab5d48dd8c11311350295d1a29d2fba09</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>137.7MiB (144.4MB) – 1,254,769 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd651f79bdbffbb3734b7c33d26fd93d<br>SHA1: 9dd1913819acce450f6f2fd280db7f7e311b3b46<br>SHA256: 4aba4dc91cd079748683512e8a111da8b0a9c9849820516e4db1af0890643f97</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>129.9MiB (136.2MB) – 1,254,769 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82a08f0665db920154ee03c8623ccc12<br>SHA1: 5ca0f2cfba65d930845aa2d147e69472ebf8ff49<br>SHA256: 7217e0d289ccbb48affedb9f27dc6113b0701ea823949deec61697fc4125caaa</pre></details></small> |


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
