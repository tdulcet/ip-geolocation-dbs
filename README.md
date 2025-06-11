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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-06-11<br>IPv6: 2025-06-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.268MiB (6.573MB) – 313,908 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5f60bca16d177745978d529982d8bcc<br>SHA1: ef4c0a899e956bc9e66e6a9964f1154e5f465c33<br>SHA256: add0d20eec9155dcc9b1159e84573c528f2fdbd95f9b337d1017d39c8c1c66e0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.30MiB (12.90MB) – 186,966 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 171739cdfdae5857f3ec5741dad2eb90<br>SHA1: ff54f96c144a4170eaa14f7fe106d1307efb11d2<br>SHA256: b3e4e7c2e11f1122197e26607b268d84241d14b01299c5408e8da2e433b3a707</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-06-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.33MiB (12.93MB) – 617,132 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2105c8f5a5f0e35d5c98917f467c063<br>SHA1: 1f852acb2375a26f5b59f072de0de01ab6d096d2<br>SHA256: ca1d2409f805aafbcbfa1f435609865d2dcdf981e800f34e44889d575ba13539</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>75.92MiB (79.61MB) – 1,153,761 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 628f22005ac501851f7c2c022aba1ea3<br>SHA1: 3e5d6cfe3a3113573fbec12d37190f641f8ae4e6<br>SHA256: 94ef5acc09e476749daae177df9bdd7d5bb614f9c7fcd550f50b09ac79a08d4b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.020MiB (7.361MB) – 352,022 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5d6ce30939ecacab9e5fbbde143dd7a<br>SHA1: dbe45e91ef39b1de3ae5caecefe6dce72faff5e1<br>SHA256: 843f29bd3db6468809b0042da7a6b44aa5aa0f7b3378bce2344b427d7b8b2458</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.50MiB (17.30MB) – 250,746 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86b9bc39132e2d99653445ab24f13e89<br>SHA1: 04cafe97346c96dfaa2a0c192e271c1aa18bb99e<br>SHA256: d337bc1e4ec66010e25e0e0279f489bc7bb3f2218829c1b952e7b21620faf6b0</pre></details></small> |
| | | Full Location | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>189.6MiB (198.8MB) – 3,310,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1255823f4fa6d96cb2339938032ec17<br>SHA1: 7bcb7165d5248f918857090fad507b3b62aff99f<br>SHA256: f33143e90c472ffeaf3431c1f790ca9297c4fcb75c4f9b48690bbe6cb9d79c80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>401.5MiB (421.0MB) – 3,898,653 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50981857bc3865133c307de9e8f457db<br>SHA1: 915f84f9ac8ac491a0dc82f8e1c8a8b51e82b9eb<br>SHA256: af893c4ae1cfc50fe6b043a92e1ececd960d30f00aa8a0067646fda960aa8ddc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-06-11<br>IPv6: 2025-06-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.060MiB (6.354MB) – 306,250 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66813478af08592fdfc48fd31bff150b<br>SHA1: 811a9109b04c7e248ec3039089a3534799a0b45e<br>SHA256: 7438026d984ce77dc6a3c83ea0623314e8e04ce52f031ecb819c2211c10dda60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.18MiB (22.21MB) – 321,882 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dc7e513e52e0755f6fdadbaacc17b5a<br>SHA1: c9ee76ff47638d91e8db56f68fe6b0d1ca2f6cef<br>SHA256: 35bfcec7d2598e67771e9d918023c4280f9109650acfb7bc6d7776c000fa7505</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-06-11<br>IPv6: 2025-06-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,073,788 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5842c1e89d9e6a7ace62a726c41126ac<br>SHA1: e3950375fff9f4e7a1b551e841a320f17e1763f3<br>SHA256: 136c0e48f44d563e0a01829656f7c14024757ccb342856959d0a6797ee9afb85</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>243.8MiB (255.7MB) – 2,366,384 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e93be5d64be521626b8e98eb9c04690<br>SHA1: 8491599042ab2c0661a6d9968a86b0de5322e2e2<br>SHA256: 699e1f5782b93d7acd864659595c72dc1e8bf20e3457b3d9fbe5503103a35841</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-06-10<br>IPv6: 2025-06-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.05MiB (12.63MB) – 603,225 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56e06765ae6f42bfcee41c91e54e5f35<br>SHA1: 81cc5eff91ca85d7d8d511a7c6033b9394c398be<br>SHA256: 8fa369ea04298bfdd963c08656125ea381ff60f0ebe547fe49676d9bd858cfba</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.20MiB (43.20MB) – 626,051 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4213bd81a3df12cd06d95fb8e886658f<br>SHA1: 4bed52a3da10fae7e68e8b84a1b72328b08dcc39<br>SHA256: dadd966e679b4609185bd6c3f14dd227a7418865e0307d165ffffc32e3dfed17</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-06-10<br>IPv6: 2025-06-10 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.5MiB (180.9MB) – 3,403,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9eded3717e1fc414c598afcfe03e09c8<br>SHA1: 2c1106f0277e6f4a81facb8fa6937b98208ded5b<br>SHA256: a0161ee6c8676dd8d5b9c5bc75aee28862a88116ac201040364548e961de27ea</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.3MiB (192.2MB) – 3,403,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73d8056205f9a87150e7844ee0d02223<br>SHA1: 78ab9e3f04cfc27b262543fe18295d5278a4e223<br>SHA256: 376a6267a5a397f2b25c2420a2f37ee6fbcd87a08d98798733e063c5c44b5745</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>171.7MiB (180.0MB) – 3,403,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce5cd58a381040f5cd36bfe6439b576c<br>SHA1: bfee15f74bb1e0a4a810eb39a03bcf2d96ff25b2<br>SHA256: 53449661334ac682c0f825c8a411351b49396f731a5fbdc0206d8070bf932170</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>174.1MiB (182.6MB) – 3,403,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bb4bdc47ef59b54559301bb0667325a<br>SHA1: 83a5c7c861807c7986842ec262ecc2c374e5ee46<br>SHA256: 3340018becb9f7376eac46d0016fea48f721b24241534676e25bf7f131e542a2</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.5MiB (229.1MB) – 3,403,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5858742b0a5879607e8913e7f1aae75d<br>SHA1: 821eac2633ae9c21467b2c4acbda07536c43cc23<br>SHA256: a499b01758d8d42175797a7b369fcd000ea5321a17805abac172dd0fc63153fd</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.2MiB (179.6MB) – 3,403,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d1f6d3dd2341b31bf172b5998cf026e<br>SHA1: 7f60871e0344511d5a5f4f53d649a8036d995bd4<br>SHA256: a96db7e26605d9f0b6cea0387a5bc79a9e32e7a66ec4c4631825fb282ffd4276</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>212.2MiB (222.6MB) – 3,403,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a8063a1029c2e8ae2747a7551dcca24<br>SHA1: 78993114052343a75740024bb2c1234d85de370d<br>SHA256: 5f8db00106463a7211332e1602d74ca3811e39757ff87d8cdd75844edcbe725d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.5MiB (187.1MB) – 3,403,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2dc68c692c6c6e215c090099cb48a713<br>SHA1: 605d3fac1a550b9dd763b48c3875014f77e1dd87<br>SHA256: b2170a070849b4faaba5eb08ebb4381a41302f499279dabde26fd0c13715f6ab</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>178.1MiB (186.7MB) – 1,892,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0603e1ff5057f9c1f176c18436423f13<br>SHA1: 6c2294331d40f84afdc5be3cc49ccf0731b54924<br>SHA256: 3ce48d61485e447175f824f5e6d7ddae2f88f628b7d75450355558c43a5f4390</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.1MiB (190.9MB) – 1,892,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bfc6e6b38406b12a064bbe6d6da35495<br>SHA1: d068c0aab24f89fba8b26a361bd12a2225f9b840<br>SHA256: 002cc74bd19c734c78f625fb697212577578208739d7ae83b89a4b8fa2fb6e9b</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.3MiB (184.8MB) – 1,892,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0bd1103146dca0372f8e4188f68ea6ec<br>SHA1: 9dde2056ccff8567dad138d158ce6be0b592ac87<br>SHA256: 08af36e44a4f8050a05354dadd2a710613fe76b269e98b1e80973ca7d263c391</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>176.5MiB (185.1MB) – 1,892,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c3b14bf2cdbd14a6bd9b656552069eb<br>SHA1: 5ca140e8671f4a43ccd9e5a2fdf2066979dc608c<br>SHA256: 7718a6209db944901d6c8e913c0a2a359c80db6bb06d5781efcbdcd51ac13dd2</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.3MiB (204.7MB) – 1,892,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e39191a06fec4f5936e822cfc7ff2d2d<br>SHA1: 69d66831b41452b0f750515a0d3cbf0ddb3f91ce<br>SHA256: d920909a42004327a2a8a58581563179b7d30c53ce86766967f5e9f2d6376b07</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>176.0MiB (184.5MB) – 1,892,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e25f5c249adf23e5ca247762c2239fc7<br>SHA1: 6fff072299c6dfcded4136eed86d3aff2b123bd1<br>SHA256: 1deb9da9bb328e78456a42d8ae4b48580ed74820d05003f7f78a827e527e1b5b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.1MiB (205.6MB) – 1,892,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc27cedbbb08bd3785a3d798f23a51ec<br>SHA1: 0ac97d8682bc730fa5c04df358f95b2142288073<br>SHA256: 098688a634933778217d74030180a5762563210caa8386e0d7425357a3a2e597</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>180.0MiB (188.7MB) – 1,892,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9820f5ef434cc50bc5e1cf7912a48b94<br>SHA1: 96f3d28ab7abb7fc67b0d937c4574785b6b43af2<br>SHA256: 1448ef56d3d5af0b48ebc847620dc3af715088061e283cf200ee30c27f9d3414</pre></details></small> |


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
