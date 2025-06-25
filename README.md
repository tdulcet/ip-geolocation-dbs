[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent TSV format with no quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases changed from [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) to TSV format and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than one day (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-06-25<br>IPv6: 2025-06-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.208MiB (6.509MB) – 310,891 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a6077050a1d6d9dd4c33c826690bd2a<br>SHA1: 1135d3f95658a92e1efd49dde92be40609b01040<br>SHA256: 086801633d4ae7a7bc6bdfa2880be5681f7d468b269bc7a1ec9cffb9e1f794d7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.21MiB (12.81MB) – 185,589 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d07115fc8ac14d54166d9ed313421632<br>SHA1: da77c320633535f3db5d35b590f216a5c607bae9<br>SHA256: e3b41b9ac8f4e8ee520c0c806367409c1608384d9f12548f35b4b9a44b9c8694</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-06-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.17MiB (12.76MB) – 609,304 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c36cbc12e4bc51dbd9270f2e14fc27ee<br>SHA1: 125f6038ef674449f8132a070697c390e2dbe87a<br>SHA256: 15b6ff89f47bc068474b18345eedbcf7e963427ffa68b76d465b619fbfa00be3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.17MiB (93.50MB) – 1,355,130 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09b130c4b16a5bec58da27bc077349aa<br>SHA1: 36eb32b2dcdbf0887fb9ccd308a307d4a92a2de4<br>SHA256: b1fc5ebf29a5b31876ae1b9243c85ce2c5c55f31e6e13d031ead1113083d2e09</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.020MiB (7.361MB) – 352,022 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5d6ce30939ecacab9e5fbbde143dd7a<br>SHA1: dbe45e91ef39b1de3ae5caecefe6dce72faff5e1<br>SHA256: 843f29bd3db6468809b0042da7a6b44aa5aa0f7b3378bce2344b427d7b8b2458</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.50MiB (17.30MB) – 250,746 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86b9bc39132e2d99653445ab24f13e89<br>SHA1: 04cafe97346c96dfaa2a0c192e271c1aa18bb99e<br>SHA256: d337bc1e4ec66010e25e0e0279f489bc7bb3f2218829c1b952e7b21620faf6b0</pre></details></small> |
| | | Full Location | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>189.6MiB (198.8MB) – 3,310,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1255823f4fa6d96cb2339938032ec17<br>SHA1: 7bcb7165d5248f918857090fad507b3b62aff99f<br>SHA256: f33143e90c472ffeaf3431c1f790ca9297c4fcb75c4f9b48690bbe6cb9d79c80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>401.5MiB (421.0MB) – 3,898,653 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50981857bc3865133c307de9e8f457db<br>SHA1: 915f84f9ac8ac491a0dc82f8e1c8a8b51e82b9eb<br>SHA256: af893c4ae1cfc50fe6b043a92e1ececd960d30f00aa8a0067646fda960aa8ddc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-06-25<br>IPv6: 2025-06-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.060MiB (6.354MB) – 306,250 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66813478af08592fdfc48fd31bff150b<br>SHA1: 811a9109b04c7e248ec3039089a3534799a0b45e<br>SHA256: 7438026d984ce77dc6a3c83ea0623314e8e04ce52f031ecb819c2211c10dda60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.18MiB (22.21MB) – 321,882 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dc7e513e52e0755f6fdadbaacc17b5a<br>SHA1: c9ee76ff47638d91e8db56f68fe6b0d1ca2f6cef<br>SHA256: 35bfcec7d2598e67771e9d918023c4280f9109650acfb7bc6d7776c000fa7505</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-06-24<br>IPv6: 2025-06-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.34MiB (12.94MB) – 618,006 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d352e79600c6c0182b3fa523164a857<br>SHA1: b98cc3ff2e271fa3b826fdc51ff3baab8e3b0d56<br>SHA256: 0da5c92a3bf3b87de35ad1975860b857e7e52b88499e73b624bdb632c7a08554</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.72MiB (44.80MB) – 649,267 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4a939649f1f923d734bda669f78cbdd<br>SHA1: 06acc60c469cd8f802f1ca78ed7aa6495088b0ea<br>SHA256: efe7dc5af7b80b72ac3696ce2762a78b5fedae2e900366d3a947bbe22bb6a418</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-06-24<br>IPv6: 2025-06-24 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.1MiB (181.5MB) – 3,416,279 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ef28df0904132d963c63308abad4001<br>SHA1: 088a40b9259397159381defe59dc5452796fc123<br>SHA256: 42395af888c15e9ac8c094de537e82ccac34909c0230b34cf59fbd81859bd794</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.0MiB (192.9MB) – 3,416,279 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbbc6f5c3475ef3d112568502645b294<br>SHA1: c41fa4825bf775d9e2c5aa5fa858d398fec5dbbc<br>SHA256: 8f0731208223a63257524ef0672c0723f9277a27a14357f79a22230a29b05e53</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.3MiB (180.7MB) – 3,416,279 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04c89fa3e7951e882dc03ef5ecb72a33<br>SHA1: e4ec3cb1f9be826c2dc0245b675e1c090303387e<br>SHA256: eff7b25312c47daa10286775ff9f20ddb4d5a807abf096f087d1ac62fbbc335c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>174.8MiB (183.3MB) – 3,416,279 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b6403416b97294efd18ac49212c1e6a<br>SHA1: cd8aca643174a0c1577c5a0d5b1c8d96840020e0<br>SHA256: d9e304791956af3afe4dc3b3a0d291dc221a45d156a9625eba7330dc4ef6d7be</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.3MiB (229.9MB) – 3,416,279 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3545cc538712bfa4040ead2743d98af<br>SHA1: 7cd67b86f21083c49d578b7a1bf13196f94d75d7<br>SHA256: 158b83bcbe138626dd3273b2c8569ad9062afff7582b03503eb8cc5c137198d8</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.9MiB (180.2MB) – 3,416,279 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 827093a1b1c4f303b74c7e71304745e2<br>SHA1: edc41c17940eab42c1c38fa78bd52ba777baf3dd<br>SHA256: a3cc2ca671efb81020b6a0b0bddff47c1360195b072ea32ec442d29cd6be0e31</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.0MiB (223.4MB) – 3,416,279 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44bb8245aaea3a6b7c8e651e9c7bb9c8<br>SHA1: e0cdff471bcc703ced211cfb7500ff49896f0340<br>SHA256: bfedf21fb4e7a4f18d8fc0b7e493124fadc8b6039de0c00c757177ad108e8fc4</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.1MiB (187.8MB) – 3,416,279 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e1e12bdde55a4337a3c30741e2d4be7<br>SHA1: 29dc4e0672afba1bbc2ef384be7ca097c8076bbd<br>SHA256: 5be71fd3c7515e080f9b04d3d6f1183d52c58d46a725e738426cf51f9d2fe2c2</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>180.2MiB (188.9MB) – 1,913,744 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53ffdd346045fb0831c4c2ac6551f223<br>SHA1: 6ad2fd6efed88441f6081b0181be1bae64a22bdc<br>SHA256: a304e1b65e7b28802ee16972096ff0889182efcfea72ced3e0066e23e8eb7f97</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>184.3MiB (193.2MB) – 1,913,744 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 864ce29622dfde4678ab446ea94c169a<br>SHA1: 17aa205e26bbc575ebc76fbf6bd28f1584a1f228<br>SHA256: 8383aa95ed190ff802b5c83979806756ad3642fc337fc8cd6a5814e02f4e61cf</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>178.3MiB (187.0MB) – 1,913,744 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac446c3cf0fd7abc90bc1d37215f3eb1<br>SHA1: a95b892351cbc1c50678f177e2681753ff5bbf38<br>SHA256: d8761f214f5112caa69a7799792a8ef54a539b4ed2420923ba1be9682ca3243e</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>178.6MiB (187.3MB) – 1,913,744 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b16870db6f69586565b582b8bdff7480<br>SHA1: ae2f605f643b33eda53b9354e1f5f0e947a1fc1e<br>SHA256: 0f470cf67fcc4b60e3718f3c60ce898703ec57c33b14026ba3603e6b3eabe020</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>197.7MiB (207.3MB) – 1,913,744 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c0e83f4b9463566ff60c81e47fccea4<br>SHA1: d08ab7a173d2f2433accdac09194da26fbbeaab6<br>SHA256: c3c7a16571e929faa342d837e21489509d60766792e653cfe40dfb3e2a0bd576</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>178.1MiB (186.7MB) – 1,913,744 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a57129f3b0b2638e050c99bf36729e9<br>SHA1: 7f41dab745cf595b45bb113c7541ebd19add15b2<br>SHA256: 20b2a2abcb7895e2418c34ecc2fbebdef1e43bf216ba6c21ca22aca22b8c530d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>198.4MiB (208.1MB) – 1,913,744 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b308e3c5dd2453656882e8bbadabdea2<br>SHA1: f56672c33f5ab06281d104fe4414918e13b05024<br>SHA256: df8f42b4afc5968be031a6795e217f22d52c07eb832583d2e0be0aecf807b617</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>182.1MiB (191.0MB) – 1,913,744 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e00b755708d2b84c98b8dce72f544c94<br>SHA1: c673e1070fe5697058287c88101d0f4fca2c7abd<br>SHA256: 5876803a2904c3417c5e0eead1802ababd6fe9da265ae43461939d655199e67c</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### TSV format
`ip_range_start	ip_range_end	country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in TSV format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### TSV format
`ip_range_start	ip_range_end	country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### TSV format
`ip_range_start	ip_range_end	country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country TSV format
`ip_range_start	ip_range_end	country_code`

##### Full location TSV format
`ip_range_start	ip_range_end	country_code	state/providence	city	latitude	longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country TSV format
`ip_range_start	ip_range_end	country_code`

##### Full location TSV format
`ip_range_start	ip_range_end	country_code	state/providence_2	state/providence_1	city	latitude	longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country TSV format
`ip_range_start	ip_range_end	country_code`

##### Full location TSV format
`ip_range_start	ip_range_end	country_code	state/providence	city	latitude	longitude`

Note that `state/providence` and `city` are blank for some rows.

## TSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `1000000	10000FF	AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `1000000` is the hexadecimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `20010200000000000000000000000000	20010200FFFFFFFFFFFFFFFFFFFFFFFF	JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `20010200000000000000000000000000` is the hexadecimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
