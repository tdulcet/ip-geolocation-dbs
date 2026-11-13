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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-11-13<br>IPv6: 2026-11-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.736 MiB (6.015 MB) – 287,108 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d566d46fde906755c7309a9d46253083<br>SHA1: e0f067e2946731bc2d480add1536519de4a249ec<br>SHA256: 27139ec1c643b00cd29dd335db59adb37c3335b90961a8f9df310392ebb3acf6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.63 MiB (18.48 MB) – 267,855 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c767081d739f5a0b6d06c67b28debbe<br>SHA1: d044d6431ff1e1df5aa582402385237398e36a52<br>SHA256: 00a229c1a59ada84ac81f8ee8f6366f8873d32d7dd330a36664d437859a08dc9</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-11-01<br>IPv6: 2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.186 MiB (9.632 MB) – 459,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84167ee008949c7e879c18eaa6df481d<br>SHA1: e998f760da828517741b8a57f76ceac532d2afea<br>SHA256: 03cc8544ec1d65aa3d43c09d4f8db8b5471fb5a48eb435c2e8626cb2c202790e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.883 MiB (8.266 MB) – 119,798 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93720f717969024f48fd382cad72f274<br>SHA1: 5173d179b24a928fce65b1c5c1194626035a37ab<br>SHA256: 645dfd169109e1cda747277411d71f68ca9d428d01b715756c1925f6ae7473f0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-11-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.05 MiB (13.68 MB) – 653,292 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98155cc759d1fa6b975067ae290efea9<br>SHA1: a6fc4df925486aeeac4e1546f7073996d28353b0<br>SHA256: 54625c97525ace79c1faf376304f57e6c9f37bbfc1a4b9d9041b145f6ed4f6cd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>91.73 MiB (96.19 MB) – 1,394,010 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb41f879bc8964b311263feaae7561b0<br>SHA1: 65be88340297142a3695014a9963cd02d3e1ddfe<br>SHA256: 87f77251a4129e3a8f468e5e55a9ad52eeb67feeb850a21cb9a00dce5ffd4b4d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.244 MiB (7.596 MB) – 362,984 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1896a3d70d9c776ebbbc51174d2dff7a<br>SHA1: 6b153e2b071d13e45ab9795a9d41e7fcbf0b910a<br>SHA256: fb52bd209b940b70d4fa6772242238a7238e3fdf267f7232a326a283a172da63</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>24.33 MiB (25.52 MB) – 369,794 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90147b4da0ef46e810078a3ca7e5aa0b<br>SHA1: 9df64ba895edf447da29fd2c604e9ff223a49471<br>SHA256: d30738d906d231b000d8994f7a07aee2550e5ba72a4d6ed8b60712ef87862557</pre></details></small> |
| | | Full Location | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>205.3 MiB (215.2 MB) – 3,598,802 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a48535424fbcaaabbc7dfc056e39f5a3<br>SHA1: 4394336d775415fe1a653bacbda7921ede4fd2c4<br>SHA256: a320a6ae6f82cb61d2d9b36a2baf9ed6a69c127627aabc98a1c598893700a202</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>430.4 MiB (451.3 MB) – 4,178,996 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b774537c14ceaf921dbde58aa6fb3f09<br>SHA1: 7695b1a6e7b8783b8331d8935d87fb6691eb8b0f<br>SHA256: cee773355d5c7bcb515c4efd0abc0daeb0b545de5e714601f54daa4c6c03e77c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.813 MiB (6.095 MB) – 290,990 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c7072a914951e8601c9ceeada7a3d6d<br>SHA1: cf54f7394145aaf4cad9d5806cf033c5d2e05129<br>SHA256: ae75289541009f5e4e55f485a547f5969d05bf27e77319236873e0cbe6042b95</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.34 MiB (24.47 MB) – 354,673 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e0dc2b8d91b7ba4229624281d2e16c2<br>SHA1: 0b3d99b5bb726900a6a60d2a140865a09f6c202e<br>SHA256: 8c00dd52b8cad30ef157bea8292f275ce2427479b23834b052923df53c5ab3e0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.4 MiB (177.7 MB) – 2,928,935 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c7dfce82c76c40935365010e208451b<br>SHA1: ceefe3f4d1597102c1e20a15432939082505547c<br>SHA256: 25dd83a6bf875037466f23e735227da25d97c795213017cef409de7778c8671f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,928 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75980237a60e580bcf5a6bb2276cefaf<br>SHA1: 87785f70ceb15fdf9f19a474ecb10f6d04550358<br>SHA256: 63657dda83bd39e0d502cc12ad78bb16eb3be91705bad6374d45345f41c7c24d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-11-10<br>IPv6: 2026-11-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.28 MiB (11.83 MB) – 564,812 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a8dcd04b1a238799376cb4fb8f30236<br>SHA1: dea8ea92e2e81940d74d6769a19e5581fd0f76ad<br>SHA256: ba3d7d0b9ed53e44827db3783786be8515f7e3eff85394737160d7ad5cbb6f15</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.54 MiB (34.13 MB) – 494,577 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31369861f7b54237a6d3da21eb47d74b<br>SHA1: fa43ae550953a766e82460c745feb47967784f7a<br>SHA256: a9d5aca15de733741543f76510420054e65ffaadee712342a1b547979cb6b85f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-11-10<br>IPv6: 2026-11-10 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>187.1 MiB (196.1 MB) – 3,646,041 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d300bdc3f8e9db283f1f47cf64b78e91<br>SHA1: d989349321c532d351366d34bddd48e8ccd1ceaa<br>SHA256: b9d0ba00a6269c3b7922ba29deb5c7bd16d6b8a288bc65201bf12fc1eb89691a</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>195.6 MiB (205.1 MB) – 3,646,041 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 921efa90bec963a9dfb2005b3285cc8f<br>SHA1: 29b1b9388483e6fb8eae46ce351cb37621337a27<br>SHA256: 8ec3b46adce5201a98ca5c204ed90bf55c246dc290c2183c7e2a06c910640ca6</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>186.1 MiB (195.2 MB) – 3,646,041 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfa561899390c6b3738a4e948eefdacb<br>SHA1: 6c638fb1afb99514f9b23bf4ad20fc41c111fb02<br>SHA256: 0aeb7d9acd9f073e8e269a9b2fbff574a15937524afd8ecdd3d3571e183f8ddf</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>187.6 MiB (196.8 MB) – 3,646,041 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ed4db012444b35a73c49ccb4a2127a5<br>SHA1: 9f6eb6bf99395b025b5d41f13f5733d50b851d4f<br>SHA256: c2bff073489cef2ea141ab6685c9e9ab0ebf532fe67694932d5c8e7766010f67</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>236.3 MiB (247.8 MB) – 3,646,041 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30d0dfafb27411e912256d2bd51d4f2c<br>SHA1: f7f3049beeeab66280f432cb2befbeb96f0385ef<br>SHA256: 3961dce7dd1ae132ec59b54a3af96d54a692bae998bde339a475b06a03575228</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>185.5 MiB (194.5 MB) – 3,646,041 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 623e4bbbe83ab3a2b591f1c189bd84a0<br>SHA1: 0690217d63e9104d5c4b85cd65d2ed2a8c96927f<br>SHA256: df459686a06fdabb39b9ba8fae9c0796b2cd8969a5fec2beca781b0c6512acb0</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.0 MiB (246.4 MB) – 3,646,041 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffabccf5e9d5cf6411d1f0e1ed66e7c8<br>SHA1: 36f16b415fdf902db8af1ff2d9f44a7e67eb86ba<br>SHA256: 9dd5f9d29ddf9a3f10dcf78a3dc57235dd45343c4c4a04cf595a8defdc249c28</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>200.2 MiB (209.9 MB) – 3,646,041 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a90a6b2a422e0ad4658be0b784974c7b<br>SHA1: 1cb067d2c0664e6b669458555a9ebd97dc864485<br>SHA256: de10abee5497d05ce10883ffeecae03bd11b22c8c0d1fd66a3f9b3f5f8f08391</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>201.0 MiB (210.7 MB) – 2,110,150 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4d5e6ddd112adb1928222376c845140<br>SHA1: 7641ebb3e87e3ef77a62064bd4cd5b50301d8f79<br>SHA256: 977b898070de54521c4a1578a2b5fa483e86a46dca69faae1128c0561b10a6bf</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>204.3 MiB (214.2 MB) – 2,110,150 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d330c1224ad2828bcb6bcaba042cc0<br>SHA1: 0a6eb00e8c15eea2a26d26e2842956e910481962<br>SHA256: e874e05f8e9ee2957cda45e62229081576e2fa117070c167abf2ef7d15bf31c4</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>198.4 MiB (208.0 MB) – 2,110,150 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bdeba5a9229738bb9d0ed3e64f0f8a8<br>SHA1: b6d66b38decaef329ccde84fa66b50e659be8df5<br>SHA256: 99bfadb3a132c59bd07d7a9ff13822bc304ea99aa0386ea1bd51cfc91a2345bb</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>198.8 MiB (208.5 MB) – 2,110,150 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a27e9fc001084e960abbf4ab45711db<br>SHA1: e4e47c30054c0382e850ea51003fd230ff24f775<br>SHA256: c32b2b884f0bef39e99c17b883edf891e8929bda70f094d2cbd09aa3b7b50beb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>220.9 MiB (231.6 MB) – 2,110,150 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65bb285761c08eead788d583d70af960<br>SHA1: adebb64f80e738f62b72c2c60a71666b0a59e9f9<br>SHA256: b69af692718ab7ba32e7845a2b4d06c981328d783611a3d3028e848498a1eecc</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>198.4 MiB (208.0 MB) – 2,110,150 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e65bce352c80106fafbfb92e71469fa6<br>SHA1: 3f7ce7ad3dc2d514f704699aed0342d20b5edbee<br>SHA256: e69b6a89c125d09f1e8d10e69cb783bad9e6696efa07fb30d4d1c55033ae2476</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>223.7 MiB (234.6 MB) – 2,110,150 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4c35af0cf05582e1b0aca906dd324eb<br>SHA1: 235d3f3cd50b751334474bbd6c038171ee51c209<br>SHA256: 6383c1c9580378f0faee9fa55277c3b0cb631a672a6e75c552b69b08d28a8e79</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>205.8 MiB (215.8 MB) – 2,110,150 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9794988186e66a7f652719587be00825<br>SHA1: d89c56fd348538e6e94005719c4029a14f87336a<br>SHA256: 6c611f3078c65bb20e31308360a3e064e2e05243219381e9719bd80d5269ab9e</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
