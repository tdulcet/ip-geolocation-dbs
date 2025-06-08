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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-06-08<br>IPv6: 2025-06-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.265MiB (6.570MB) – 313,761 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2280c1737fbe9ed9adc88a7e8e50e794<br>SHA1: fea4d7ef89c742b26ed68ffdc5d16933443cc05f<br>SHA256: 20615d3c14a09402f4b6d19700fab27dc1d46446bcbdb4b41feaa52c51ba8b4d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.30MiB (12.90MB) – 186,993 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d163003756ad0ea797f969ae76f863dc<br>SHA1: 791cbe94682044918f4720431fd46035aac31ce2<br>SHA256: 72619f2e83dca722a07e01a880e00c4f1c3e3dee3e0097572be461ef69849087</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-06-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.46MiB (13.07MB) – 623,759 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3174fd1b8e35b313075bb4d1e5ef3b7<br>SHA1: 5f7a83e342f2aba36b7084c6ed3f9f05411b33e1<br>SHA256: 156b47b8c8f027433a9e73bc7c13f07db13ab465590cfb7adfd809a304c9dc18</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>71.31MiB (74.77MB) – 1,083,658 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4a74ab8821dda501c0a9eed8e71d64a<br>SHA1: 03aca4ea1799326c76ecd7676044a7c05777b1bb<br>SHA256: 2341275d308195c424bd0eff1505491577a00492fcf15056b06b5926fa74f9fc</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.020MiB (7.361MB) – 352,022 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5d6ce30939ecacab9e5fbbde143dd7a<br>SHA1: dbe45e91ef39b1de3ae5caecefe6dce72faff5e1<br>SHA256: 843f29bd3db6468809b0042da7a6b44aa5aa0f7b3378bce2344b427d7b8b2458</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.50MiB (17.30MB) – 250,746 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86b9bc39132e2d99653445ab24f13e89<br>SHA1: 04cafe97346c96dfaa2a0c192e271c1aa18bb99e<br>SHA256: d337bc1e4ec66010e25e0e0279f489bc7bb3f2218829c1b952e7b21620faf6b0</pre></details></small> |
| | | Full Location | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>189.6MiB (198.8MB) – 3,310,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1255823f4fa6d96cb2339938032ec17<br>SHA1: 7bcb7165d5248f918857090fad507b3b62aff99f<br>SHA256: f33143e90c472ffeaf3431c1f790ca9297c4fcb75c4f9b48690bbe6cb9d79c80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>401.5MiB (421.0MB) – 3,898,653 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50981857bc3865133c307de9e8f457db<br>SHA1: 915f84f9ac8ac491a0dc82f8e1c8a8b51e82b9eb<br>SHA256: af893c4ae1cfc50fe6b043a92e1ececd960d30f00aa8a0067646fda960aa8ddc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-06-08<br>IPv6: 2025-06-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.060MiB (6.354MB) – 306,250 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66813478af08592fdfc48fd31bff150b<br>SHA1: 811a9109b04c7e248ec3039089a3534799a0b45e<br>SHA256: 7438026d984ce77dc6a3c83ea0623314e8e04ce52f031ecb819c2211c10dda60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.18MiB (22.21MB) – 321,882 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dc7e513e52e0755f6fdadbaacc17b5a<br>SHA1: c9ee76ff47638d91e8db56f68fe6b0d1ca2f6cef<br>SHA256: 35bfcec7d2598e67771e9d918023c4280f9109650acfb7bc6d7776c000fa7505</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-06-08<br>IPv6: 2025-06-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,073,788 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5842c1e89d9e6a7ace62a726c41126ac<br>SHA1: e3950375fff9f4e7a1b551e841a320f17e1763f3<br>SHA256: 136c0e48f44d563e0a01829656f7c14024757ccb342856959d0a6797ee9afb85</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>243.8MiB (255.7MB) – 2,366,384 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e93be5d64be521626b8e98eb9c04690<br>SHA1: 8491599042ab2c0661a6d9968a86b0de5322e2e2<br>SHA256: 699e1f5782b93d7acd864659595c72dc1e8bf20e3457b3d9fbe5503103a35841</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-06-06<br>IPv6: 2025-06-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.97MiB (12.55MB) – 599,062 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1a48390743533826c52508030c2b42f<br>SHA1: a7d1307d4d786273dead7c2157559f4b9df1d3c8<br>SHA256: d3e29eb119ee227e2dc59dfefabcc07f18b0f4d2c034e7e3127722bdea5ca887</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.05MiB (43.05MB) – 623,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e23f3a607ba64e26d5b63f169df066e<br>SHA1: 498ab6f2c1713f831ec7fe3d9c0ba0f9a5ce2be8<br>SHA256: 5ba823572139faa10cb28fdc18aab0a0a1cbf66d3605b30d58f5fc65dddbcdc9</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-06-06<br>IPv6: 2025-06-06 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.5MiB (179.8MB) – 3,385,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0d6652beb448f90a2706d5134c751e4<br>SHA1: 2711aaf504f03b7bd4ed4570601a36037be0f9b6<br>SHA256: 38174d7914c74f2807f602c4ad599561824a1b992c1fc8bd0538b850e9b1817e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.2MiB (191.1MB) – 3,385,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26088944529598e2995f33fae39b21f8<br>SHA1: b03096f978e544a3a5cc62565044a95309f06656<br>SHA256: 6b20f6adff85e292a07ac81e2a75b7e56b17d962c641e11d3bf64dfc142bc666</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.7MiB (179.0MB) – 3,385,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad9580b181b2ac472551108a43b8bc11<br>SHA1: 397e5677e5fd68c8abb0cb1634bd75cca6b5d9d2<br>SHA256: 4f5a181dd64ed1f9016e3e4f24e0b6a858a059d757cd1525f0ea704db3b10b91</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.1MiB (181.5MB) – 3,385,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0619930f4d985ef803530c6b9c141bf1<br>SHA1: 08be3bbde9da3da4262eeec562176abb3bf3a71d<br>SHA256: db420ee6c76783d66f9fba603d6207a856c70f84e7c314ff2eb28f3721b0de99</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.0MiB (227.6MB) – 3,385,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72e975054897fda007730d6d3d7a9818<br>SHA1: 11dd38c40bc2958c900963e31660cfdda8688952<br>SHA256: a95d088f081d65c5d2cdf9b9f6312adf93d0b4b652e17e50119e57d3ce07adc4</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.3MiB (178.6MB) – 3,385,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f341c46ac24e95311eacbfd034107e7<br>SHA1: c4d6ffce256df0877ad372c98b24002728a67e3a<br>SHA256: 72adf98574d57442ed2291dbba3e77a854363f47438c467daab1ebd68628199b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>210.9MiB (221.1MB) – 3,385,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eae0a5fbfebaca4c2698f9c1f2a9d072<br>SHA1: 0223479d9e60d10d3dd9d42f89fac58ac0e103f9<br>SHA256: a8f487e6c7a5d955a9a96ecfd2608e69a8f3532ddc4f1a7b074a5cb12247c5d3</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.5MiB (186.1MB) – 3,385,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b3ab401246d468d25850d4d2e917698<br>SHA1: 9ae59a3c352aeb0d4bc1d6164be527a20a9532a2<br>SHA256: 9921223b6ded50f1c3c0dd3fe190b7670ad4fcf7b7c664e37ae8a5e7010926fd</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>171.9MiB (180.3MB) – 1,829,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17d07d8f1beb06aee6640a67d585c135<br>SHA1: 2334ee7b70d966ba37f4c998432701cc6de56060<br>SHA256: 9441fa8817f6270da301b37d1c91145a187f6f0c8f0f31a94b2203de7ea8daff</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>175.7MiB (184.3MB) – 1,829,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16745d1b0457e501f25665f4cb572616<br>SHA1: 279384482dc04e2d5e718a7fedff8513b473f6d0<br>SHA256: 7ac37186bdda3e7470cbbff23da932d1a802677977aae92c0533c139ef15a3a6</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>170.1MiB (178.4MB) – 1,829,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9855a27754ef0efcfd8f7c9dbfa81fdf<br>SHA1: fbfdb673a56b9132b451bb1268bb24a21fe57cc7<br>SHA256: 0579d75a88e3e25a975b6dc32783ee8cf62f3543f7cc9dd57fdb89da49f3794e</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>170.3MiB (178.6MB) – 1,829,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f83a7b328db64fa136ad3aa0ad3ffe8<br>SHA1: c9c2b4b12f6763c4c78518b884eeadd5481115a9<br>SHA256: f7735c59c02c7abae92639ef52e5385cf4fa6a61bbeb8eb94340bf19cf21fa5e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>188.1MiB (197.2MB) – 1,829,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ef4b88578696c6be583791dc670bca6<br>SHA1: 06902fd4878d8d39478f2d5a8697b497d160dbc0<br>SHA256: 53bb66a556bfb5fe37e90afa761b574f5686d1623b3b1e0d0aac4b799b26256e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>169.9MiB (178.1MB) – 1,829,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50f29ab2e219eace4af9d3aa0a885fc2<br>SHA1: bfead4c3209ab1f8c022bb47a332715a8d216c7f<br>SHA256: bd1d5552c8ac41cc5af99f1957d01dd6dffff5e35fe5e90b8ebaf0fc1d0f0a75</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>189.0MiB (198.2MB) – 1,829,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee89d9bae68947e7367461823c284891<br>SHA1: 7b85cd1b35e5266e16fb70928e784d161be21b79<br>SHA256: 2f7b6484aa92c991fb8d2d84063541e772df808af5438c415ee18b2be93f5c3d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>173.7MiB (182.2MB) – 1,829,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21f4fcea0005d9f79df7ee29224900ad<br>SHA1: ed722c3791e23ddf0c3fe9bf69e1c27c9703a7d9<br>SHA256: e03a44b891ddbb1ddce3ae4bd3b332245cdee9f6dce5a4be1514c480f82586dd</pre></details></small> |


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
