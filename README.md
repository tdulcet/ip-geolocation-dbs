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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-26<br>IPv6: 2025-12-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.427MiB (6.740MB) – 321,853 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b998f2002a091c15f4aaa980e3b498f5<br>SHA1: 5547e9b333b551e1da15d67475887484f39664c8<br>SHA256: f3932ad1a2a75c0074dd437fb7dde5b5fde5be4f0978d421a6d962e4f1c8db69</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.18MiB (15.91MB) – 230,652 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99b291e3e56497b1815fffe14728814e<br>SHA1: 237ff0a1fdd5be4097c83341916f46aa4eecc7ee<br>SHA256: 404cb8285461aa0f1e6864756092d3897a5fa3d3b14618da399c186e4550e3de</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-26<br>IPv6: 2025-12-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.181MiB (9.627MB) – 459,674 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03472ca990e124af84923831c056d19b<br>SHA1: 4b224c59998140b1fd9f46ee3fdbd7fcd1cd6ced<br>SHA256: f2fdb78b9eae9ba15f6f0e3f0310e4bf3fea8d29398bd59e75cc66b6e3e44d41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.495MiB (7.859MB) – 114,019 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c23cee1e890c25e1d1af89ea7942bc52<br>SHA1: d0a05658f82830a1826b6a8caffe5cb2023ec209<br>SHA256: eea45c3213c032c24828ed44cf6ca2b06618056e28099106b91279a75f3e3d1f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.41MiB (13.01MB) – 621,360 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6977c9fcfa76fee09f4d37623fcd90d1<br>SHA1: 2c52f4781686d0cf87d87f251e1b6f1142a33d49<br>SHA256: 77b5afd86d513a551ecb392bba120c1bb8a5529c90343a2b0c781791c70db319</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>76.42MiB (80.14MB) – 1,161,403 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5439f979d278d0c26be3ee1984607e00<br>SHA1: 13556bdc40af8da12ff068f82a817b1457ec3ec4<br>SHA256: 801447debc484a2c7bf7955f84fe3310bd0afb67a1a52414951b38458ca544dd</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.196MiB (5.448MB) – 260,054 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd1da47eecbcb1371255bdc50c718d77<br>SHA1: 750933e1de8cb3d548ac391160af871b871bed93<br>SHA256: 057d957bff860585d56f46ecfe886d386bfef914406c23dbc1816ac00ba37c62</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.00MiB (24.11MB) – 349,485 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78fac9141a055ba1200b9e4197d17a6d<br>SHA1: 2dad5e9fe9e6680a486b8de86a165bcc1d75629c<br>SHA256: 2f85601d58de0e24dd53e1f990a048c34f01bcf4433e39e78d3d87d89d39ae02</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.5MB) – 2,947,207 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd8aac3eeb88b310fa305cd0935ecfd9<br>SHA1: c74492fae9ff6ac08a5c5dbc08bed733d3da06ea<br>SHA256: 1dcc9f177867a631fe4c98c83a10cdb7d7578efba05eb4d13a9d34ff00ead1c9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.3MiB (305.4MB) – 2,823,618 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf7686fea78936ceeebd798c0594060a<br>SHA1: 3bf18b3cb9ecb79d04eff383fce69df36bae3d51<br>SHA256: a5bbe43965014f4f35c9262bd8e7ae3e3dceb030619ee951589b718687fc8ec6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-23<br>IPv6: 2025-12-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.27MiB (12.86MB) – 614,001 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 971567474d8930ee3110998e76d64a81<br>SHA1: ec5da6a0d7a7918655efea4177e000cfa1a930bd<br>SHA256: 7cfeb9d670c7dae1eed3b690ffee32eb718903d5b4f132a1bee0ccb5cf2cbb6c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.57MiB (44.64MB) – 646,900 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 983816fef0f0e3777e7f3261f327680f<br>SHA1: f2381db0e793b8d6161e6e48055fc588e513d612<br>SHA256: 454cd79783ddabfda80f8a2437e79807f18048e01e6c32288e5aa0378501ad6f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-23<br>IPv6: 2025-12-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.3MiB (187.0MB) – 3,520,147 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a15c752bd073b255f53865e011f1dc89<br>SHA1: 7c67b4aa15ae6bbb1930a669bdd41d36557ff519<br>SHA256: 1dc8db1b855ea2ec2a915cc8dc58cc29adc09f8cb380d6b94e30df44c8f0a338</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.4MiB (198.6MB) – 3,520,147 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 502b1df0da710c5157d2aa5b3b86d40b<br>SHA1: 45db4d4376a5ff126e5982c5ffa02b5966e97bb8<br>SHA256: c1fde3849778e89045008b406c3350ba398c31f58937df14b0227c1043873771</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.4MiB (186.0MB) – 3,520,147 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9606006407213538a9deaf1d98c1d621<br>SHA1: 92106610876adfa55395d2d6e4e08d45c9255fd8<br>SHA256: 330e0433824f171a36890291cbb261f1a3b0b138fb5cf3a1f3b18ce24acda035</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.3MiB (189.1MB) – 3,520,147 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6be4fd99d6c135d202176e53a4ce89cb<br>SHA1: feb75e7eefec632fd9ac88852634200e5ed1c0ed<br>SHA256: bf713e22f555cd37417a69b63de1c8ea92d5342418c446f0cc91fbfd3ab5b388</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.3MiB (236.2MB) – 3,520,147 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0352c06f59e0ca487fc72cdcf91da830<br>SHA1: ae76bfaa41c392967a06953c2db6359c3b1534c1<br>SHA256: 65de6b136400df7a8e72bebd898eb077c9dfc0f8318d4b82a454170eef7a80a2</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.0MiB (185.6MB) – 3,520,147 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2524414083c4c709a9b8aba3011cd5f5<br>SHA1: cf8b992bc88db4749533d7a2e050c192c05feb1f<br>SHA256: f44a4246e55a865efb9e7bc408e7fb29ce5175afd7d7e19f9939318b67e82e1c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.3MiB (229.9MB) – 3,520,147 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dbcdad75314c47a51008bc65db844501<br>SHA1: 956f6b18f8dc64fe95c2d294346562e6d111f0fb<br>SHA256: af8c7a783dc39765664e616084e187c73fda268f274d47efd3bba71f7cf78116</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.1MiB (193.1MB) – 3,520,147 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7db18671d82f50fa0757f5a1bcb18497<br>SHA1: a374b8119ee907e981020a7ec69b65e7370bd549<br>SHA256: 7c85ca3ebe16ff9240d7cf5b247209260f4a8797a816517bc61e7869644f269d</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>183.6MiB (192.5MB) – 1,936,716 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16f92641328525282b1abd1e7149a05b<br>SHA1: 2519a00b9d8cfd128d6567b7bb3e1a5053a9bd28<br>SHA256: 5b233dacb242341f8a90bcdcb6602ca4bd932049a29bab520dd6a834f4c06c75</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>187.8MiB (196.9MB) – 1,936,716 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5feb09d79d0cb74a3ba091bdcc4e667f<br>SHA1: 1c17031d4a8bc6eead551c9d41fd806327680185<br>SHA256: 06fe5c2add83a086c9be7c0386fd709cd59648f045a3dce8355637828bb59aab</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>181.3MiB (190.1MB) – 1,936,716 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d53b66ed30596e4056d5eb71efcc09a<br>SHA1: 470ad3bd18c33e8a4ab8895daaa8a214335df6cd<br>SHA256: 06b818b522834ea2bbc4af7ea48fa3ff86546478d45139b5ac0c5114df1c0e67</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>182.1MiB (190.9MB) – 1,936,716 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb3e351dd9767346c8296edb76e415d6<br>SHA1: 6cef71ed5f1e5e22fa83c4b18c0b7e9a58568aac<br>SHA256: 62cd2e8a34e0c1f0407577c3ff6e5b9103a20a2fd07185861e5451fa6fde9932</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>201.5MiB (211.3MB) – 1,936,716 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3eaf6fe05e189491d13694aa8a00b94<br>SHA1: 569b8e20a75b7e6d5245438a42438a89122eee62<br>SHA256: ed0149995ad668f8fb5a2f73e70caed48faa21413c9b147780dd838f34e03767</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>181.0MiB (189.8MB) – 1,936,716 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27d1802183900a0d214de62f839c79ec<br>SHA1: ac030210a3a0a1d99ddfcbd27de71782ffe8a668<br>SHA256: 763c722ff779bd1e9d392d25f556aba432df991b383f9d1a4b8e714cc727eea1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>201.6MiB (211.4MB) – 1,936,716 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f45099d89d0ef636376345bc10c25bc7<br>SHA1: 2c780a5cbce7ca6622a6b3dfc14a55517ac2aec2<br>SHA256: e738af2a49b0316c92a864a7e8167cfd4bec2bfa440e6a839f32248eb6dea7d5</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>184.6MiB (193.6MB) – 1,936,716 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 565e59d818a9f009b4201ede414fe141<br>SHA1: 9731d1b8ae60b8dc21467f9031e3774964482c7c<br>SHA256: 54e5df6f3647b98e281667befdb09dd4da51131de1a096782df86b3319f4c7ef</pre></details></small> |


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
