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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-08-26<br>IPv6: 2026-08-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.470 MiB (5.736 MB) – 273,761 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7d3202c42e03b8422bf171efd41ece5<br>SHA1: d6854626b51981acb76184ee1561d4a4e42cf866<br>SHA256: 2d815beab4b2210480842cba198dcdf1b793aade98c2d39fb906bd0bd3128265</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.61 MiB (17.41 MB) – 252,380 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba19c989b4946cab3ea2398d0bd24af4<br>SHA1: 1576a5481c830978922dbf97005df7160aa5d06a<br>SHA256: 92ab39339eca694c236305bec8b942032f3d54be457cd5ec125ff4bc822223ab</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-08-27<br>IPv6: 2026-08-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.104 MiB (9.546 MB) – 455,869 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 076c3fba22837f6e69357ba02907f082<br>SHA1: 19a43ab4647aad751e9529c1cb9fb9a253840874<br>SHA256: 72283ca7b7b73bbd3dd078b3d5356539fb37a7050503cb8683d33296e91b55d5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.087 MiB (8.479 MB) – 123,005 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: faa3abeb5e257585f46e22b5c7604cbe<br>SHA1: 97219d0b439d7227d05b316bd60644ccb20de83a<br>SHA256: e6a39463f4b5996fbbb5218245ae75a6a997051f55a84a5bf31e10eb2f5847f8</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-08-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.17 MiB (12.77 MB) – 609,491 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb5e40475e22a1a132f7e639b90f4af9<br>SHA1: ab11031982c59731c2356d7c6c8e052667f6054c<br>SHA256: ea3f539ea32882a3d5f1683ed51fd49f6a17d35528b9596ab92887e17433fc16</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>47.07 MiB (49.35 MB) – 715,259 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e434337bcd59a9b7e2a838b6c7f76406<br>SHA1: 77a1064c310cd8ee5359ecbeaf1955a6b2267364<br>SHA256: 0e48196d69c41f1a2293e36b811b7bac382fcee0636b7b9c1f43f0e799460877</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.149 MiB (7.496 MB) – 358,140 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d3e21d2da14fe2fa0da1db2f6424311<br>SHA1: f274f58aadcfa3311603218b88e8b24a01671e36<br>SHA256: f62294be209c966f38eb82e27717bc64116462241210756e85c31429048d1f96</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.92 MiB (24.03 MB) – 348,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60cc96dd0eef36fef003b9981e7aa19c<br>SHA1: 077fc11bdf3b1a16ed5a8e22cb9889e86b007cf5<br>SHA256: da4f32fc9e285ea393eb3d4fec4fb4a153874623b14fc77373e8f448758ac135</pre></details></small> |
| | | Full Location | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>208.4 MiB (218.6 MB) – 3,652,137 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68a79460a812a271884a0a50858ee1f8<br>SHA1: e1cb26165f0fc2b394c3f08d99642d1e5a3e653e<br>SHA256: f40963b044ff4637dff7dd3608244f6e065cc97e9bb7262d5fea4abeed6cf026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>440.2 MiB (461.6 MB) – 4,274,498 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e9801b97694446ef740a7093d24488<br>SHA1: c8e28d1130d3667d5b313b6e468c5d9d69ffb027<br>SHA256: 88971b264e462d0a2d37d85f793d5e488192b4d883a1ad0142a7c28d9a60af96</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.716 MiB (5.994 MB) – 286,131 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d282e141eb5464b8254973895dd4a19f<br>SHA1: 43ed365a77bcc1acf8efbfc3769c01a237bf775f<br>SHA256: 436d012d7deb50897534e496aeb1616f14ea008640929405f2664f5122ffbbe2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.50 MiB (23.60 MB) – 341,989 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51aa8116a79265830a4cc7cd4ef86053<br>SHA1: c18af12e87abaf09ccf88a3c0de5227c764e8a1e<br>SHA256: 374157270162797a62dd05862b45a4be9f350bd4c2e81ca0a48534910fb28817</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9 MiB (179.2 MB) – 2,958,317 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a7499b08d50db46b5cf9fb15cd346d<br>SHA1: c27a4fdfd31298e65e03fed44f2b36b4aba8504e<br>SHA256: 7e2727a2650e2ae9c6e50b6fbae1b77db0938c91593e6e1e1de5d7e195393e70</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>299.6 MiB (314.2 MB) – 2,903,507 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a92797de8e315b9794c5a75c021c7b8<br>SHA1: 3bad371e9bab711cade7d5e88cc542a34819152a<br>SHA256: 4479ccaf1ffb1b9388ae015e24ea8e3e1780c412777f1ee2b0a30bda83f5d0e9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-08-25<br>IPv6: 2026-08-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.22 MiB (11.77 MB) – 561,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40b5f62358c1f1cd734aef577c4e1b0a<br>SHA1: 19efbb41f1ad1fd335e11761ad8b4ab09f89fb3b<br>SHA256: e9b2aac357ccdda1526c086a53580bed5c39a56c805665f123870ab632cac016</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>34.89 MiB (36.59 MB) – 530,244 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71eb3856712fe77de8100262d8206249<br>SHA1: 515eafbf05d72ab002aabadb12616fb4cb9091b7<br>SHA256: 02564f71e270fd2547248e8dacc9cd5f20e105d595bf67a759418ff91086956f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-08-25<br>IPv6: 2026-08-25 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>190.2 MiB (199.5 MB) – 3,708,771 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6323ee26fbc7169dbf6b376ba00795e<br>SHA1: 38d1da53eb913f75e4c9b64e659040d2211c9d8e<br>SHA256: 91334f59c10f0aab24984e4c1700e5ad3d11d78221b918611a734e6df2e0d09f</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>199.2 MiB (208.9 MB) – 3,708,771 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60e7cba1419a7712dcfb022c2550c400<br>SHA1: a97ce14147ffa9569183eeb1bb4c68787e06ba63<br>SHA256: 5b3998011d8d1b0fcfd4c1a1149ed8746f4eb3f0d15560dbb4887482c3f3e429</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>189.4 MiB (198.6 MB) – 3,708,771 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bad8243cbdeb773f45baf98b2ac038c6<br>SHA1: 7eace891b0c83191c83059594729a858192defc5<br>SHA256: 77312b78839004766ef0f69ea5fd38de1ff004397c191ae742172e9bab5a157e</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>191.1 MiB (200.4 MB) – 3,708,771 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c08ec8ec37bba6def8cd1d46518e694<br>SHA1: dc37d184f84858315255c43a977632abc0a91747<br>SHA256: 929184d8ccfdcb53e67bd76b62e61e3a0343b6f6f586d469e8ce72bdf2fe0b31</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>240.9 MiB (252.6 MB) – 3,708,771 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65e1cfa48d556f3f0647a8b4309706d2<br>SHA1: d9d10d819e75f493152d08739a738dcb448d5332<br>SHA256: 1a0732d27105801d27c2f85f5ad895ae7eae338919b72aad7420a69c500b2276</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>188.7 MiB (197.9 MB) – 3,708,771 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7783e1029109bea5436f18bd0f8edaa0<br>SHA1: cedb6860361d0183c0f04397b66cb4f883d94fc4<br>SHA256: ee65647848f3cd69cd70190b153c74b7f84f21e081e89443ea561320fad2abe1</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>231.0 MiB (242.3 MB) – 3,708,771 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 769a7c13c91deb31fd9832f01dc03dd4<br>SHA1: f690730b369e4c4a07deda3e4c05152729f172dc<br>SHA256: 8bbca97f4e2a0326be76b56e7a7a80cc0a96f06d41747a9b93cc2d937abd0c21</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>194.4 MiB (203.8 MB) – 3,708,771 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eda960ec782a1cd0245a5c87439ab1e8<br>SHA1: 2ca290c0984849ea3ea18815cf901ada9e555488<br>SHA256: 6e5f51b6f7c4843436959f347a298f9e9a477e8a30dd31d460e0ddadec5d5b54</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.4 MiB (209.1 MB) – 2,086,467 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9c5c0f5e150bba2408a446447e58f67<br>SHA1: 79319a76ae8fe5f699c102caaa51c53ec6bc16be<br>SHA256: 7a15d6cfd3bdfc5144f06abbbbdb9e9ea77022b26db8f75db2b55ffdd26df120</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.7 MiB (212.5 MB) – 2,086,467 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b36e984aec949c9519a5d8a3fc21f5bc<br>SHA1: f6cb6da472fe333715d6e304f1ed9698c94f049b<br>SHA256: 9cc123a6e77ee9b6ec3af0ad9ccae94debd30bf053f2c16f6f474a5b33c9280d</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.7 MiB (206.3 MB) – 2,086,467 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b808c6fabda8039cd4c4dd1be6291c3<br>SHA1: a830eb2c8ed959c2ef20a47a040d6750a6f4976c<br>SHA256: d54d8b3a4682ce200930a9b80c36bb328b995ce9acded93e24f95faf1ae25a4a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.2 MiB (206.7 MB) – 2,086,467 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f222dee98e1b456b28cbd07ff582021e<br>SHA1: d52dca7caf338ff1da97b93f0284813752d39c9d<br>SHA256: ae93d718d83ebf8fbaeb2e81d07455acbca49fafbb80cbe082564d97ea7c3ee4</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.5 MiB (230.2 MB) – 2,086,467 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04d5c66fc5ae4d30bbd553f656c740a0<br>SHA1: fb9a4d237df6c40224e58f109b9861d2ef7653c4<br>SHA256: 9b29c3bb697a30e2b86a13a3a7b70d476190a0825f20e6011394cd794fb1886a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.6 MiB (206.2 MB) – 2,086,467 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2193fd79e4f60fb1a00b4b6ca0fc0b08<br>SHA1: de3e9abebb7f2be624293860df796964f8b93414<br>SHA256: 302101061173a2ef9d0758600482f14e27966c284e1345818174757e82d642ba</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>218.1 MiB (228.7 MB) – 2,086,467 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 755a8564cac746949fc06de7f9027fac<br>SHA1: 74c20974319d24197c54eaea7f38cae28b646e70<br>SHA256: d5c24e16a19141f5f4b1d96b8cc3e25eacc7cea430efc9efb29484bce07b4f92</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.4 MiB (209.1 MB) – 2,086,467 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 547410484de1569ec9e61f21de8de022<br>SHA1: bf3cd01c09ab00ad63be279306785ac26ac66806<br>SHA256: 122294cba312afda929ee7b54fbdac3218fff6e999d60f2b9fe6c1fc57948c9e</pre></details></small> |


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
