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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-03-09<br>IPv6: 2024-03-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.807MiB (5.040MB) – 240,640 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6269b4763716f5b9f501d65f546c619<br>SHA1: a120370a106582af6ba58242087c979dbb318261<br>SHA256: b904a2fedda489a351190200fe6f46249bb0952c87272416901ccd8de2280ee7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.993MiB (6.284MB) – 91,079 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d43b330a631cfecbae5caa9ecab3e1f<br>SHA1: bccd00bfa34da12d6e535053ecdc01cdb293427a<br>SHA256: 376b4cf636e12537c6e0ea3424a1e457cd9a9efc6500343a6e1fb24f01548cd2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-03-09<br>IPv6: 2024-03-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.200MiB (8.598MB) – 410,657 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98c0dd21a0d09948bf0ce2a592bb9f95<br>SHA1: 44761a95385e23751ee67c6bec61d994dcc28c64<br>SHA256: 0effd55a650fa5ccdd1e84c101db6996e5df20235908b9368bc62d68ccdd35e8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.046MiB (7.389MB) – 107,196 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 772479308f56bcb7f20d119d1549c7cd<br>SHA1: 706056e82b50067075923dda50adba440d9defe6<br>SHA256: 5e6d0a14d997250375b4b86cef5e1d124d53e624e018f9a108e149bfa559a14f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-03-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.59MiB (18.45MB) – 880,765 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de7fecdea8def75928ca05e653930462<br>SHA1: 6aa4c8f0361de451955efebc6e3fb01f0a5c5297<br>SHA256: 461502ba78a7da94dc974d284d9bade1fdae4e9f60b03dcc321a3aa97333c227</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>68.92MiB (72.27MB) – 1,047,364 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b172df0ebc3ab31511156a8773422b6a<br>SHA1: e91c33db92af3e777b8989b6448404d2e075ff8b<br>SHA256: a6882d6312dbe60ee958768c4f2b6234fc2322698d3dca514466970a4a10cf07</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 322,326 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b232d78e18dacf266bba37244688a18f<br>SHA1: 2ea0bf2a68630d5c12c6fa1d18f2f3eb0845f297<br>SHA256: b9f2935f135d22119e5db5d8d8666980b07ac2e36359fd6dbdc9c26a8b3be2f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.03MB) – 275,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49241985f6153f5f100b60421257f25<br>SHA1: 51e0348aaa544a9b75aa17c9431f3745175c5c5f<br>SHA256: 3420806d6067a2579fe3eef92e4cd09b9b792cce9c418a3ca7f3c820f4edb887</pre></details></small> |
| | | Full Location | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,158,494 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd92465491c42b3844af48593793b1d0<br>SHA1: 53a3bac0d03e0e4bef95ad11b21c1a1e92eed9f8<br>SHA256: 6157eb8d8b93b5da65533893b6b1af8682e371476cd754957d56f3cfd1179aad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>307.8MiB (322.7MB) – 2,989,351 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a432fad1dde6398b8b6ee222abf32676<br>SHA1: 78d2ec063fa05a95bb17703a5111864cd91a5446<br>SHA256: 5974cc41b3872ea8fe373def59322db31b678ff8585a6e529b9737d648343c0d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-03-09<br>IPv6: 2024-03-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.772MiB (5.004MB) – 238,843 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c15a8429d90e259b5d89e46f363cb94<br>SHA1: 11590e995ca6469691aed3ae703c69398c77a07d<br>SHA256: 36416d6d7e8c82177e05f1950529ec607ca389a020fb40fc49b45bdf0bcf638d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-03-09<br>IPv6: 2024-03-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.8MiB (178.1MB) – 2,942,325 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8bf036b2620260eba08c4b59f30ad2b5<br>SHA1: a99847ab6732f596cef7ddc2da1038c4ceb123c5<br>SHA256: a2351d207b79faebc18456f39c7c525677f4083269f536c4bf18267d2697cc0e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-03-08<br>IPv6: 2024-03-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.580MiB (10.05MB) – 479,941 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ce4e7158c86651561042c69aba2b7c4<br>SHA1: df112e8f2e1a951892adace58fdaf589a8ab04cc<br>SHA256: 4e09e21b540921b741d188c4c5af23158fc22182cea62f2e246a75c4132a07f2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.40MiB (19.29MB) – 279,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6298a313b21f02f0d2f78ec6825a71ca<br>SHA1: 4cfb61b89f364e8ca5906047f8baaf2d360e3701<br>SHA256: e466cc8177f1b4bce9424d7b3c6d3ed95404de7133f578cbce552eb1868e31f3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-03-08<br>IPv6: 2024-03-08 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>157.3MiB (165.0MB) – 3,342,318 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 151748b20e9ab40b1fc76c2b0f8037f5<br>SHA1: bb46b58dcf670e3fc0ec8713aa3d2b3e4f6f271b<br>SHA256: cb0583548a0009168e478aab3076062543412f2f6d079f106f7290e0853cb35b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.8MiB (191.7MB) – 3,342,318 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d1b0fb715c94d02983408a95a60fcaf<br>SHA1: 5be38c2bb38f5ccab94f828dacf9667144fc8f7f<br>SHA256: e49673d630adf68ede5651be98fc65ba9c3fddcee348ca85a981f85924b184db</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>161.6MiB (169.4MB) – 3,342,318 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f917d5f71bbb8a69a935b287740e4ee7<br>SHA1: 2f31d455c94162db1a9e0d6652fb31738a8c76f2<br>SHA256: 802c8f1e491330ce119c6da74302e25911cc9e8a344b3020b4e1ce5f288e785e</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>167.7MiB (175.8MB) – 3,342,318 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 150b13e6683bb0f23ab95cdb4315c936<br>SHA1: 676563cf83993d6540ad26c14e6be0dc5a7c45ce<br>SHA256: 0723d195f21066517098093d3c037a1d817a0ea1b881244b044b0e7dde7e599b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>195.9MiB (205.5MB) – 3,342,318 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4350ca061a054dd0e6298e38e2991e31<br>SHA1: 8c7fb750ed6f7481c1ec3968ec330740f1670e6c<br>SHA256: 794bf0d57ccb09914e3c79282d0f6233e5741a5a93466556fe9a26d0d5661907</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>156.3MiB (163.9MB) – 3,342,318 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50fefef97855cdc32dab9e8b2f97c268<br>SHA1: 82ae794a9e8b3a0f3895f267ae4562aee110f7c8<br>SHA256: 4551c44b4d913c4fdbe3c55c9d5cbdd5f4b5e82103b61ff23950bd1c534fd59e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>195.4MiB (204.9MB) – 3,342,318 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23e3ef76b8c15fed4ae4cd7a24b7d00e<br>SHA1: 97c070924ec193c871d5fefb7ee4a3ed1c3546f7<br>SHA256: 38b0fec397c40d92f9f3d48bd9388c8c41f316c7f8d022ffa8936c9cc0ef11a8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>165.0MiB (173.0MB) – 3,342,318 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59c49f345a46e930f1314f86b6f94c48<br>SHA1: aef90463136c0d1dded4f100c76596ca773773af<br>SHA256: dbff47881082790ec1dc881c57e2399d404382cd089d6fa24105e8e7c589590b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>104.0MiB (109.0MB) – 1,162,963 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5d513b1f1da504daae6a3de72bde3eb<br>SHA1: ca1a40441d52f8969ecc7e3e4b439b751e0c3b41<br>SHA256: c2a87523f45ac5d73dd90724e3851d6478ea70b251221caf568b8efd8d40b4f2</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>111.5MiB (116.9MB) – 1,162,963 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3cc1da1cc5896665ea72bc1cd1ec0e37<br>SHA1: fb43737a99e483111b94f96524beb8ebe3cd3ffe<br>SHA256: af0d82fdc5b206b2f7a12af88ff62acca89967922c1b8f5d2429149c297659c1</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>106.1MiB (111.2MB) – 1,162,963 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721920f1582b36fa62483f00698cc735<br>SHA1: 4983adb71df5f60db8a870211558c9f6c2cf0e19<br>SHA256: ffb2f780b0df81e2a06be7212ad4c588f44e4563a1c88d134fdc1fe777e0ea6d</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>107.1MiB (112.3MB) – 1,162,963 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f32ff299bb684a44b549c16f8f5d9530<br>SHA1: d77cd932c0e745790f95d8d4abce86c14a83c064<br>SHA256: ded6a29dbff1537bd25583c7b89cb80ea3963fa4588300e73bab459f4615ff18</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>114.9MiB (120.5MB) – 1,162,963 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aeb075eeb31e08a73f3b649e1e2b63f5<br>SHA1: 0cffed38a0f6588423c9a98ccbabdc439d3d0d44<br>SHA256: a64d44616f5aa59854a515afc7d04ac8391e444ecdc9f2b8b36710a4ec2708c4</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>105.1MiB (110.2MB) – 1,162,963 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956eb9be7486efbcc11978961642cc34<br>SHA1: 9113374ba4d1a8b718bba1b9c39d0f93f4f6358c<br>SHA256: d30334c3e42c523db79b6ccfc78a471c0de06d90e5186400dd955f0e76099094</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>115.2MiB (120.8MB) – 1,162,963 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9d260a8ec48481722d6080ee1d0d9b2<br>SHA1: e8b59bfa6c797c38b32c35c016b055a3f9ea0c10<br>SHA256: 7901d8ee48eff35cf2c67b0a6191885e246233190098e38ed04e22532a3cb571</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>108.0MiB (113.2MB) – 1,162,963 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cef852dbf5ecfcb7edfefd15253f2f85<br>SHA1: cea849bb9dde662e7c6b110952d6e2aec247cd68<br>SHA256: 35c90af1e501515d549ae42e0b6ce8923e12056702715f861632fe6c2eaae6ea</pre></details></small> |


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
