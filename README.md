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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-10-17<br>IPv6: 2023-10-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.620MiB (5.893MB) – 239,370 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f290b6105c48470a0b6c708b365c6ba7<br>SHA1: e587f3264e4314a42d11dedc70b351365c09b779<br>SHA256: 8a462af6c9ee96b8303af8f66198744f5abc05272c7d158ccea053de10490620</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.327MiB (6.634MB) – 81,901 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 275ea0e27ae54c8a0e73f1f4033c50da<br>SHA1: abfbf875494955047933e060c0d131b0dc973123<br>SHA256: 2b9dfd8f518163a25728f7671189f31ca05c77e3d6f15d109420b2e65b95cd2e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-10-17<br>IPv6: 2023-10-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.611MiB (10.08MB) – 408,241 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53dad8c5618f5d15a1f8f442a46aef62<br>SHA1: bf05647f955a1922cbfc06d3b1851453f15c1dec<br>SHA256: a5c469011f9404033a42f78ad95317cbbe8edcaa0a703e77c440753e81254ed2</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.086MiB (8.479MB) – 104,774 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8548f327fef41ab759806a68dd3fe639<br>SHA1: 033e6950a1b5287be9785b670eabd06aa4fbfa39<br>SHA256: aefd8c9ff261b8da4eaf522fe187ffde7e4edcd1e2ca2d3acd51490096385041</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-10-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>16.29MiB (17.08MB) – 694,412 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5aeb5fb694ce3359fa5cdeea60fa6a28<br>SHA1: 0fc26ecbaab7626b23cf0f42fe55a979622b2ff8<br>SHA256: e89145f4df09e034564bb69710037322027a02a86d3606d4f4bc61c0c3912085</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>42.64MiB (44.71MB) – 551,971 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eaa4989cf0acdc04db305d7ee0b2d36d<br>SHA1: 7f674a7dad5cdb3f24b646ef6117e941586b6915<br>SHA256: d2b7bbade415ea69d62c3020c62fece9c5fec9c96cfc04dcc2dcaba883fb1e0f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.207MiB (7.557MB) – 307,820 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ff8d81d8ce4efd3476359318175af0<br>SHA1: d105d1c4490b536a83d0461759256799109a17cc<br>SHA256: 4cb45f08b0bbd6d6c4fb204e776835b939ac663761aea652d12ae2ab20494228</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.54MiB (27.83MB) – 343,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3256ab7e4df24ca9917bf92c70b9ce1<br>SHA1: 832b96b707911579f91d2a42cc84b0766c5db738<br>SHA256: fdb03997e4b7c1a6bdffa274673b7756d8dbfb2ede55f1186b3957ade7042544</pre></details></small> |
| | | Full Location | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>184.9MiB (193.9MB) – 3,048,591 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed65f47a5f866d476bde81f05015d0ad<br>SHA1: b0ef2e2cdf8875da35c99816df76f9fa88d3de9e<br>SHA256: 5bca8efa9618ae69c9fe4228342c0ec4bfb4d581ca0766a3a8e45978d1fe7875</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>269.4MiB (282.5MB) – 2,345,213 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f854d9364b9ab55744dfdc557c9f9f6<br>SHA1: f419e9a0b9db7b3c78b5c98927c74c8427f3fcd0<br>SHA256: 3d1595b762a094dfd2f9ac1525dcc77a67ac87dec747f420b0fa63ac4fe51cbb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-10-17<br>IPv6: 2023-10-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.547MiB (5.816MB) – 236,500 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4857bb88f1e540efdbadfb3e56c208c8<br>SHA1: 0190e03fc0543a58ca868f0f36a92556049db942<br>SHA256: 44b7a5f1e09f7ad797ea8511ecfc8ddada844067bdff82f4255273d85906d172</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.24MiB (20.18MB) – 249,120 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5105fe9bbe5d0ddc9bf8995e1cd8fdca<br>SHA1: 48b9366c0983f8d70d79ad112999057d17d64829<br>SHA256: c10da1d1999f1867044c9753957966c4989400bf25df0e7fb02c524b43dc90fb</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-10-17<br>IPv6: 2023-10-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>171.6MiB (179.9MB) – 2,803,356 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4abca24edbdd7d97ffaa621ecb9327a9<br>SHA1: 97c24a0d18b54cd8d2692e708765b79162107242<br>SHA256: 903407a226a3eb479f2165ba004762c64c3a41dd5a9c0d515be1353f99e5796a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>166.3MiB (174.4MB) – 1,448,721 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d928761a3b79f2ef6c55ec6d4dd813e<br>SHA1: e7de15f34cace41d4332e3d59c8ffe729fc2f8ec<br>SHA256: 613e34be98c76eab733c9982022bfa16a5d1ab57fd73444f0d6e8a2ef59ae567</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-10-16<br>IPv6: 2023-10-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.58MiB (11.10MB) – 451,686 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f814079dc59ac3164f23536f20c76f0c<br>SHA1: 6953593956832885d187d3d2e7d631a1c8b477a6<br>SHA256: 4e4f9f0c09410ab649acabe5e3b83300a5480a42d5e0e41469ee3905b5edda28</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>18.91MiB (19.83MB) – 244,777 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c113d7c106a20d2352822c32f9b9ec75<br>SHA1: 2b664cd7291ab8bd6724b95b6dbcc5d3435dba2f<br>SHA256: eaf502ad7118026ccac599dc56e1c7595e9e2f458d8f5ac02641be3f80173d23</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-10-16<br>IPv6: 2023-10-16 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>195.3MiB (204.8MB) – 3,883,227 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc8a024ccd489873f2661eebd46b469e<br>SHA1: ca2e091f3d1ed82c2305066ae608a60d05ab161b<br>SHA256: 5c3859244783ceb35934cd63280beaaf9a4c4c42c0be8e6b70f35d64fda3c75b</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>227.6MiB (238.6MB) – 3,883,227 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6360e8b854714d1e2595fa9ca17dc5f<br>SHA1: e6e8141cf4cfe28c43c918ee4a81fead4e79e6fa<br>SHA256: 94ab74a3b6058323719ce9771c5e15e3f175719ce9e7cb1e8ca03a51e6f9c55f</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>202.0MiB (211.8MB) – 3,883,227 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64962234de9e3cd8d0e32c3c9a8cc39d<br>SHA1: 3d603afabe4c17b361fb48bdcf907b4b7e8a7283<br>SHA256: 6f7dff769b1999bc1a520bc67dbe057c5a795bd13b8da46a79ae62b1a1cc33ad</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>208.5MiB (218.7MB) – 3,883,227 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7321393696f55d4b17771b0c7f677d0f<br>SHA1: 7ca3563189ebb4db186763ecdfdfdd8b282d7de3<br>SHA256: 7dd01b0e6e24cf378a897cd9f88d1b2fae36313620b0c35ac943c19bb381bc25</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>245.3MiB (257.2MB) – 3,883,227 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bafe5d354e1697ae01324227c759d389<br>SHA1: 3b752ca79c712a2c5492a976acf487e6090e8953<br>SHA256: caf91abefed42ff74e9414d9fd847fed42a925ad6de11825691f24c8f75e0fb2</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>196.3MiB (205.8MB) – 3,883,227 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78b521db7173229c984988e2c63ec246<br>SHA1: 6c334c835a209bf4ee7082d62545d672b607d7bb<br>SHA256: 586e6080cc8dea112667645d185a0b3e2b4121761376c613428078feb70d3c39</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>244.9MiB (256.8MB) – 3,883,227 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c2b3f77d69d694b437d30aa181dee54<br>SHA1: 5893d1754fb58cfaa526dc82cd35a1ebb5150036<br>SHA256: 2938e110c46beb46b08d5d4b1e47d005e4b2db61266cde900a112a7c7f8c8e8d</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>208.6MiB (218.7MB) – 3,883,227 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e91b2f2b5ec9ebc26be70c352a22703<br>SHA1: 50fc93a5c50f3b3ce2917b8ff9b0d17edd650eaa<br>SHA256: 3b24df3b54e1e8b7fe809a872b7cb4d43ba5a65b5c6dd88907446490cb4cb9ef</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>121.2MiB (127.0MB) – 1,204,096 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e66863287bb7e1d455e2d4a19e06c11<br>SHA1: 236fd92337a68f6bf9773561d670c608bca257f8<br>SHA256: 1f6f9ec0701643673df952b0910054283d7952f8c7d124115b074d65c234edd8</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>128.6MiB (134.8MB) – 1,204,096 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f28964dfd9183f39281f7455256fe0c<br>SHA1: f3906571d1f6a8bc3edacb080be6eae6a6899905<br>SHA256: 6751fbaf2c4e795e1d041d02f4b04a6d482db8b83b0a9564b8c63ad46b3d14b0</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>123.0MiB (129.0MB) – 1,204,096 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0599e48390d477c51956a35b8d5d1f3<br>SHA1: 0ddc39a9415fff6aa043d10c1e368f5ae6381f93<br>SHA256: 83e60a67871ad21698f340e677bf0a536e38ccc6124a111d3add85f73013157b</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>124.8MiB (130.8MB) – 1,204,096 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9bcf10283591f12904af613471ca9f62<br>SHA1: 279d4742185e4cae243f921bc1dce5776bd1572b<br>SHA256: a3aee8f9088974792d6c91db054b14942c2669dd8722b63a1eeaaa93baf5e249</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>132.1MiB (138.6MB) – 1,204,096 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 398631dd74b9f3ee3f72e17d6a05e8eb<br>SHA1: e29e4680dd8d2f7fe57ac88a2da15e589e65f7e8<br>SHA256: 82ea574a1557c03ebf68339d1f71be78a63825219e07408c5841e630f99fa16d</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>122.0MiB (127.9MB) – 1,204,096 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc439459f13754a6461ca271998d7bd3<br>SHA1: 6dbaf45d304ff32b7dd4fbc5de0e2a837a1fe847<br>SHA256: 21a1c737129f30f28908689b078ce25ac0bd0d5f688e1e9591212771980620e2</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>132.5MiB (139.0MB) – 1,204,096 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79cfac891eb8c76816258dcfc5fb74df<br>SHA1: ef7d822b3767b298f6c0a37dfe5149f53abc5105<br>SHA256: 61dace254bd2a79827376ab54e717c6674257514ead59c81506ce6e5de50668a</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>125.0MiB (131.1MB) – 1,204,096 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b8537e1e40ff9c7d6c4b438daa47d66<br>SHA1: 3764679bc190e517c43f4ca4239f0d34bfd05de5<br>SHA256: 9316a046097cc52fbc8d32c1b0206359d1312eb4d284a917152c8182c05f7438</pre></details></small> |


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
