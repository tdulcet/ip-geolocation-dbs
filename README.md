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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-07-08<br>IPv6: 2024-07-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.740MiB (4.970MB) – 237,299 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d0c13a9a5ed8104be38247d3dbdba58<br>SHA1: 284ddcfe8552d465fdada5041ea807ad5f8d111e<br>SHA256: 5a8329055c97608d5f84703d8d33724d07cb5b1e0fe4cf988ecd10a7cf6937df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.516MiB (6.832MB) – 99,018 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98044fcfdc56e8afa0f28510d4e14e1c<br>SHA1: 0f484d9a93f214613278d0ea45570b1c24b796a1<br>SHA256: 9c1bb17d935cb327d85ef546613836f82df49322a7ef921ecc3e5d350461dceb</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-07-08<br>IPv6: 2024-07-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.094MiB (8.487MB) – 405,327 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 592c5576ff7340a28a0632ec2302e57c<br>SHA1: 62ec239e5ff84ea890dcb7de0dd4fca31d4a0151<br>SHA256: 099607c6268136cec541b28bbdf6479cb59519a0f8c8d558ae7f516d93123df1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.490MiB (6.805MB) – 98,740 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc454adb378c58f1b1f776131f9d3a0a<br>SHA1: 4aac7768be68cf6e60b5914edf408a2fb52cdfbc<br>SHA256: 54161e10d266a9c41ecfd91ed9d56fc00481fc96ca9b9c8a2e530edfbfee65ea</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-07-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.17MiB (18.00MB) – 859,045 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ebbfe4c4c63c2f410dcf0d5eaf8a01f<br>SHA1: 3cfd2a38e8acc7b8ee3b2895806b2448a9b4dc93<br>SHA256: 7ada642478b24491bb7f7911e9f01701c10f921baa8143a522e6ee295e68d4b5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>73.79MiB (77.37MB) – 1,121,303 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7bae2740815fab95c3211e098011bae<br>SHA1: e1533c4cb6f577d8a4a911fb638de5e07e47643b<br>SHA256: 5ba6f659ff7961f6d3ebdc60762e75c08bdd13e46781610562baf82244b859cd</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.909MiB (7.244MB) – 347,080 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cc33d54c3bf6b9175e0b145f7c4118<br>SHA1: a3816e7df4ffb8f7c8a3e26e9ecc5b337da78413<br>SHA256: cacc1ada016c1e717e0b0224945498ec7c02f45e18e6ccc3f699cf925eb98541</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.77MiB (16.53MB) – 239,599 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d8002e2bd70b383a55c26aa6c39879<br>SHA1: 2e8b5538dfa991864d56253287cfea899c731ec6<br>SHA256: 417be26de93d6c5b8d2da113e60494952f0235ed696211cedbd93a8683cecbc7</pre></details></small> |
| | | Full Location | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,260,981 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1931ab257b12ab9982e2e837f7a344a<br>SHA1: 265a511f4b4152bd6a0cba4302e7e551263bf78e<br>SHA256: af747f9dd2423c564835352c37e87e14cf8cec475eff93b3c6b458b8ad3a8e43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>339.4MiB (355.9MB) – 3,295,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3cd81e94c6b15797cf1a60147cbd224<br>SHA1: f49f6c791890b20c1ca8c05135f5558493b09356<br>SHA256: b412df8ef796f81fa4522b3051247207cb9af864a32937188218b559f4a52daf</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-07-08<br>IPv6: 2024-07-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.882MiB (5.119MB) – 244,344 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f71b297b6d31124fb4d85a0573420148<br>SHA1: c19cd0e022cce41cdad248812b6ed96ce01f3d96<br>SHA256: 4f6fdac09cbc5c0e25e4305fde012ad03b4b27ba701095ec557f2c1ed1c594bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.18MiB (19.07MB) – 276,325 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 455753ce19833b0e8aa5a719617562cf<br>SHA1: b7cdef244498f6ea069a0523ddc0f9997aed06ad<br>SHA256: 7da4ff6463125871ea8fa12c1e2c0bb4c82cbd5eb13603b15bb06a6c12f21dbb</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-07-08<br>IPv6: 2024-07-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.9MiB (180.3MB) – 2,978,355 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec317919e654aaf26ba2956cba42987<br>SHA1: 5a1d6e846a17d001ab2649860d9e68064c6a788d<br>SHA256: 5099491c3b03773fa74caf9833a9dbb55e732c359aa505587dcd7b44b8c904e3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>200.7MiB (210.5MB) – 1,942,692 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 038ee21bebef5c2336a17368fd32209f<br>SHA1: a21d0b165419264ad815c5d369b16dde7b1ffe6c<br>SHA256: 7d3aaf19058abf9358cba535f4f8cc3c6475d21045808f084c2bc63c0857a3df</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-07-05<br>IPv6: 2024-07-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.862MiB (10.34MB) – 494,012 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c743f192810e1c7a830551708f05de8<br>SHA1: 79bffa41698819675c363085880bdabf2697fab7<br>SHA256: 8c49b004272ea990099d6f78ee375a16f0dd7e7909129a1d67830cf43bcdd5b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.70MiB (20.66MB) – 299,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a595ba8a0d2154b664de02ac74c08172<br>SHA1: 25c6eb7e731005b217808b325a75215f4da8e747<br>SHA256: 8f554ebe1eaedd763470b6e80d615037b5358fcc506cf38c0aed79f0efdf228f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-07-05<br>IPv6: 2024-07-05 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>119.3MiB (125.1MB) – 2,392,366 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aff5683dc8697265db37c7b56999c3c8<br>SHA1: 4b757ae40dd40af601b3d577936e1f39a5f72c89<br>SHA256: a143b34f48300e6ecb9f926f2a117e2772729847aaa9690821f1934c33544d24</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>128.2MiB (134.4MB) – 2,392,366 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ad855762570e47e79612f43ee84e091<br>SHA1: b20d1f88f51c75291567eaaa3cb5b854cc127b14<br>SHA256: 5a0134dd3162572614eafd81546d6a62f623aba346d70cdf25dc793bfe6222d3</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>119.1MiB (124.9MB) – 2,392,366 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7fb9c0ff9b2c65f5f84470ddf32aa78<br>SHA1: 7bf0d3bdecc714a376c49322e24975d27891d2e1<br>SHA256: ff7e869d2f69c519b2dfd45b37afe580927d8d96249c56db324440c3b366541a</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>121.6MiB (127.5MB) – 2,392,366 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32a6e52aabd06e3150dbc945d542c274<br>SHA1: f27bf66adef05f21e3dea80dc6d162334c7a8a61<br>SHA256: efa866f3d9a33aef68441e0f14046b1731187d0809c468ebe3db5e12ffbd7b2e</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>148.7MiB (155.9MB) – 2,392,366 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aca2d8fefe91c952074dbee14fcac32a<br>SHA1: 2ac01834f57816d80b8ceb9f0eca66c167ec71c4<br>SHA256: 588130bc20e6341b7ca3d271d04a4217b22ad8cd53f8e491ca4fe4c5572766fe</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>118.4MiB (124.1MB) – 2,392,366 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db03c9455c2fae8683382f33e3d335d6<br>SHA1: d7f1b3267d9fdd32a984006ad80c3a921abf33bf<br>SHA256: ec785fbc51330356de351484abdf2b94f986dae911519e518050d283071a5457</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>145.1MiB (152.1MB) – 2,392,366 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5b3580ce399b6e768feaa3e43b4c141<br>SHA1: cf56532259f4a29ed8e3f4d935ce040c1e642619<br>SHA256: fe97037c9a4c107f77590a9f62ddba66b783e1b21e1a16cf7dc6a3021a55e287</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>121.8MiB (127.7MB) – 2,392,366 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b3ec964ddf35d21520c7ce2644484df<br>SHA1: b678824106d83e896c11d7f669ef79e496716597<br>SHA256: 7eb10033ba3fb629f20a94c6fe27ce5f958e8f340b5825b1c22cb32e7baacd06</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>110.4MiB (115.7MB) – 1,189,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b35b29464c7fe30f7b7094e15ccf1785<br>SHA1: ead0b2870f919c772bc35e3c6295e572b47f9ff8<br>SHA256: 3b69f12c35ad66a2e1bdf7496b2937d0af5b1302052488855aa50dec9b68c170</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>114.2MiB (119.7MB) – 1,189,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18b55a10387d82e204ac60ed5d5dbf05<br>SHA1: 10f451abe22be9205f5cf1d010a7d5620bf11571<br>SHA256: 6df0429e6e84b2803ed55478b39d7a97fcecc486485e5209b9b7e8613cad7ab4</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>110.6MiB (116.0MB) – 1,189,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02d5bcd3307da6bd56253f59eb23dfd1<br>SHA1: aa492e43b7ebc5260f5ddfdc58838d2dd0cdff02<br>SHA256: a5d903b2995bc5a6aaf8ab38873112fc1b91eb9cc70fe38684ca9ebece77bd39</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>111.0MiB (116.4MB) – 1,189,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feceb68febb11ce6263ae6ba0432f22b<br>SHA1: fbcc57221a7a53e44059ed862649d52aa3008b6c<br>SHA256: fa2b91a450b8831c0f0542b6c6c8db1edb651ef6e649fe69a94e5160a3779765</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>121.6MiB (127.5MB) – 1,189,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf00cc14dde8d718b821609a742e5ffa<br>SHA1: e04039f4f329d81ecc7a9b92291c0a456bbeb572<br>SHA256: b553dd8d29372961cc533ea811269194e18f58e2ae3a126aa92653dfd9b185db</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>110.3MiB (115.6MB) – 1,189,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf1149a8f66f4e5e43bbd60b99a600d0<br>SHA1: 99e21d13f4b3252dcda0edc5cb717c0167bde535<br>SHA256: 08b390a2b763cdf04188361ad12d0b9312d679c9bad6372b6033d21a03c6a496</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>120.9MiB (126.8MB) – 1,189,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0550e683147a59c92ab8b6ef505c8411<br>SHA1: 547a85767b8c55e23f447e080fa2fb36f1a146db<br>SHA256: 54715761f1f72adcb24c8ac2344d3266218869f49c6542be28387cc3d2384048</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>112.2MiB (117.7MB) – 1,189,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 566dcbaf73c92fd3cb3bc487db5aa6ab<br>SHA1: c0256096f1b63ac0e51db97d4d22c7f09545b810<br>SHA256: b31539aea86cc2114558b6e5fb75307618cc9a4000c62f6dbec671c9ee4d90c7</pre></details></small> |


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
