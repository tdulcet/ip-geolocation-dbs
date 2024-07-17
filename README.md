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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-07-17<br>IPv6: 2024-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.745MiB (4.976MB) – 237,558 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92aead33bc1a7fdea8313b8efac277eb<br>SHA1: beffa64939a47d8b2d35399c652a74bed96c0849<br>SHA256: da0e87644d2b0d848f5600475a60580ee2f001ee83b9537dc3929d2a52eaf6eb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.726MiB (6.004MB) – 87,017 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4917417eded57a266a1b539ce8564cf8<br>SHA1: 6aad505c484719b9ff9dd206a6b82c51bb70ab37<br>SHA256: abb6502de07a7c85c53043152a9d136a7e18667bba1c789eda527ab8c65f9576</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-07-17<br>IPv6: 2024-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.106MiB (8.499MB) – 405,914 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53fbebb5b8cd5bcdf9e50dcdcd0f40b0<br>SHA1: 405d25ad508a67cc77c3e98a27fb834048c7070f<br>SHA256: 1cf3619e6e33ae0965336f15c74965f9ce92ee4be6d8ad0a1ac1aeb0f27d7693</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.568MiB (6.887MB) – 99,924 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b1aa2f85d52fa38d7c00b6491919c27<br>SHA1: f4e4d6f48954c47dddc413a8bf46bb29d8f83a5d<br>SHA256: e034834148bde38bc5d2bd6122e67c9474d1091e68fe7173404132b914bdc8e4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>18.76MiB (19.67MB) – 938,606 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b10a6923b4425e957ed80902b1c89dcf<br>SHA1: 19b80dfdb5bb24a64cbdc964f998da40694a26c1<br>SHA256: fdd90b5a05d4a038a5490e546f0b944cc786e35849d2357ad899a738edf987f3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>77.72MiB (81.50MB) – 1,181,162 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f1b2ec344a9114ed53d342b8fd30b75<br>SHA1: bd6e39555c5665a6e98ea66cc5de4b04808d188a<br>SHA256: b64944aa05ff29825b1231f1be29c19f54a0b5d77ca7e606a7201050ea843fef</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.909MiB (7.244MB) – 347,080 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cc33d54c3bf6b9175e0b145f7c4118<br>SHA1: a3816e7df4ffb8f7c8a3e26e9ecc5b337da78413<br>SHA256: cacc1ada016c1e717e0b0224945498ec7c02f45e18e6ccc3f699cf925eb98541</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.77MiB (16.53MB) – 239,599 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d8002e2bd70b383a55c26aa6c39879<br>SHA1: 2e8b5538dfa991864d56253287cfea899c731ec6<br>SHA256: 417be26de93d6c5b8d2da113e60494952f0235ed696211cedbd93a8683cecbc7</pre></details></small> |
| | | Full Location | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,260,981 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1931ab257b12ab9982e2e837f7a344a<br>SHA1: 265a511f4b4152bd6a0cba4302e7e551263bf78e<br>SHA256: af747f9dd2423c564835352c37e87e14cf8cec475eff93b3c6b458b8ad3a8e43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>339.4MiB (355.9MB) – 3,295,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3cd81e94c6b15797cf1a60147cbd224<br>SHA1: f49f6c791890b20c1ca8c05135f5558493b09356<br>SHA256: b412df8ef796f81fa4522b3051247207cb9af864a32937188218b559f4a52daf</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-07-17<br>IPv6: 2024-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.882MiB (5.119MB) – 244,344 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f71b297b6d31124fb4d85a0573420148<br>SHA1: c19cd0e022cce41cdad248812b6ed96ce01f3d96<br>SHA256: 4f6fdac09cbc5c0e25e4305fde012ad03b4b27ba701095ec557f2c1ed1c594bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.18MiB (19.07MB) – 276,325 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 455753ce19833b0e8aa5a719617562cf<br>SHA1: b7cdef244498f6ea069a0523ddc0f9997aed06ad<br>SHA256: 7da4ff6463125871ea8fa12c1e2c0bb4c82cbd5eb13603b15bb06a6c12f21dbb</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-07-17<br>IPv6: 2024-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.9MiB (180.3MB) – 2,978,355 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec317919e654aaf26ba2956cba42987<br>SHA1: 5a1d6e846a17d001ab2649860d9e68064c6a788d<br>SHA256: 5099491c3b03773fa74caf9833a9dbb55e732c359aa505587dcd7b44b8c904e3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>200.7MiB (210.5MB) – 1,942,692 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 038ee21bebef5c2336a17368fd32209f<br>SHA1: a21d0b165419264ad815c5d369b16dde7b1ffe6c<br>SHA256: 7d3aaf19058abf9358cba535f4f8cc3c6475d21045808f084c2bc63c0857a3df</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-07-16<br>IPv6: 2024-07-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.843MiB (10.32MB) – 493,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 999f6d385b922c9ac35f76794878b907<br>SHA1: 91936f549659260b7bab4211b188f761787483d8<br>SHA256: 0f020219a9ee419b1f1bc4d4f202f67879fccc5bbdad0d3830b4de6d1c4cbb57</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.50MiB (20.45MB) – 296,403 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e5124d298105a2aed3b3e4dfaba2d88<br>SHA1: f47f85fc7de986da462e8274eeeabec07560ce9a<br>SHA256: f37ca3e702625b63db2af77735747a084501c5315ab56eaec45cd7c868cb36f7</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-07-16<br>IPv6: 2024-07-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.5MiB (126.4MB) – 2,414,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c27c17f56d933fb3afaadd8ad246150d<br>SHA1: 5ee0e0bc50c1786aa855d9b4bc180cacc0a17d15<br>SHA256: 4a12a5e79beb546028ac15c06315b40ba542fcc258a65e0c7a4bb0a4b9ab4a40</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.6MiB (135.9MB) – 2,414,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3907d8893c2906d061b626517deca871<br>SHA1: 0aaf69f8a0839104a8115a83848b7fa2a5925dbc<br>SHA256: 0f0d02521d5ff52a57770fd67c6840d66824947df0ec4ca26f917ac4317f58b3</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.3MiB (126.2MB) – 2,414,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b57d2f2bb5e806dca4c86132a314e159<br>SHA1: 8ac47b260f9a2c64467fba2720b5876f0b4a421d<br>SHA256: a30967b6175b4be696bd38fd20753f0271523481e87a78ee8ac0bdc0cb8ed003</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.8MiB (128.8MB) – 2,414,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49b37789f16c1064c01c56704207949<br>SHA1: a1e5b55fe414a62bd17233fd0ffa50b6726c1fa0<br>SHA256: 51522a5918c9971782b0ac38944b9ef47a9fd8c4c31259ef540841ba53a4d0ca</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.2MiB (157.5MB) – 2,414,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 937efde8db6e60f9d18d3a090e7137df<br>SHA1: ce718ab77b174365277ea33354ca0d08e9b4a007<br>SHA256: 752dfe5b6ae472b99efd72d613304493eb7cdc421456e94f893f8d0d640e437d</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.5MiB (125.3MB) – 2,414,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21d138537584b6545da8c89c2f4741c1<br>SHA1: f2b1f94f4968ab1364357518d5775e7b0a3813a1<br>SHA256: 13cb63feb2923a0ad008c4b398471f09eb00a142f8c03d5c6e4217253585ed4a</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.6MiB (153.7MB) – 2,414,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bfdab1f98b45167c09202e15eebb566a<br>SHA1: 7d42720542b883c529c7f3e9c4e272eedb1dd6fc<br>SHA256: e84121462d8b7e1a5a2fe88716dc1987d711589a09a6596ebbea5c6c8e3610d9</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.0MiB (129.0MB) – 2,414,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 623ffc8bf8094a66b7b8ab982a32f0ee<br>SHA1: 065f42bb8d089b76e52eb9c32f27f7b2cd1c9e94<br>SHA256: 3c8654a334c14b9ffd37ee2ce51a730ca86b3762fbe9171b200e986e31c8be29</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>117.3MiB (123.0MB) – 1,264,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a96b88be6c71a1bf92cd9d39f8736f38<br>SHA1: 823af17917cc2d8e2dffdd556c18cd272336cf4d<br>SHA256: 721b0fdec9f35f1a51a70e314ee3bb1b99eecc4f80a49039f2ce7c4b79087981</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>121.5MiB (127.4MB) – 1,264,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1eac0eacc9cdcbc366a78e0b52a5c844<br>SHA1: b7edde3b68abf29a4b1f9a503ac8312d125ccdfc<br>SHA256: caaca3e1aef9f59180654fc4beab929eb0dd62b8454bdb25c5409db1d2baa4bc</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>117.7MiB (123.5MB) – 1,264,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e2dd233d0029b4f40a98e2443446a99<br>SHA1: 08aa6ad8027864caa07920604943a527f9f9cc44<br>SHA256: dbb49009910dc5b1876675a1c535bcef9041a8263c013a9a31e8cc63439e68ed</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>118.2MiB (123.9MB) – 1,264,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 622f1707b194e564dc4199b56e6764f0<br>SHA1: e3c610ad43b43bd64f14e481ed4a174e114d8b77<br>SHA256: 192e5f96f40f560a52c9d2391e755b520b77796a36523954a2c8cec039914013</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>129.4MiB (135.7MB) – 1,264,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0df95df4022451d13341d7a22084bc12<br>SHA1: 1093a32b0a548a6431c7b9652621762abe7ab6e9<br>SHA256: 142358770b3dab00fb7d5c1688ec3c995ec7b533a45ef7859a9b1ee82ee356d5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>117.3MiB (123.0MB) – 1,264,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b559592c786a1e3d8f9b6e84ef001481<br>SHA1: 8e56d6a93aca523b45df01708ac6badd0878214d<br>SHA256: 8b7bc7adf528f2f38d3064094856d60f21039d365e827c64da8f2e9968566e27</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>128.6MiB (134.8MB) – 1,264,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14b7e8dea1b34ce27a15c8f6c49d25a3<br>SHA1: 5049b740bfac55c3505269ef7c2a1033b27f46f5<br>SHA256: 27ae626fa02f3b46309dc04dbba411dbc78afc495a7062ec5c910abc6102075e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>119.2MiB (125.0MB) – 1,264,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac23210eec8317e5c1faebcc425b0fb7<br>SHA1: 53fd3973b6ccd86e8ece7b91f9b6431dda5e558f<br>SHA256: 1b8e22968be19b2ac6e9741a9507cb2081125a858021246e0e55bf549b7bb224</pre></details></small> |


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
