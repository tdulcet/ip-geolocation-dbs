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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-07-22<br>IPv6: 2024-07-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.751MiB (4.982MB) – 237,835 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27c48f2b534c01832d73aaada753c48b<br>SHA1: 034eff4ef9535ff067aa7694752d9a651f765e80<br>SHA256: 84d33475bcdd673a251460f417fcdc585bf0b0658d3f1eccab4f3797f5416323</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.733MiB (6.012MB) – 87,130 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d00c39da2f75d441a43ed48b9b5a564b<br>SHA1: bbeac1973108f84a3387e6d28e2eb395d4106370<br>SHA256: fedadb9b6cb63aa80ffbc55bb46e5b07453a22237ef2f67b71652ef9ac83ce2f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-07-22<br>IPv6: 2024-07-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.058MiB (8.449MB) – 403,541 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c9169ef451aa67f91765976b87e036b<br>SHA1: 4d6abb212676fe90f710f2c29942e341afa14298<br>SHA256: 07b1bd1a172b282100152056f3c017e813178623d66892ac46b297c8e184f90f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.540MiB (6.858MB) – 99,506 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69323a48e52d279d750793804814f504<br>SHA1: 611082fc06c5138dd41d2e7535f0616f42125833<br>SHA256: e07fd2ddb5685fa08c1ea614cb053e890739ea2109220fd51d926c53a91f3982</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-07-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>18.16MiB (19.04MB) – 908,324 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21454dee87df003fd259d5733da1e7ec<br>SHA1: 9fe96172abd057d94794113a7544794b9d0d82de<br>SHA256: 767153c347ed6b91297af5d052124945b64aa2bc2aa3799eac769a19780b67a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>64.69MiB (67.83MB) – 983,073 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfcf404e448f94bc98de2540e0d51cbf<br>SHA1: 096754ba4d7406ea94c4b97be695f9826b0cb253<br>SHA256: 0b6c4f75f959c3590d1b0bdc70ac8910553cc29dcde69c67a1a42b59a3470d71</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.909MiB (7.244MB) – 347,080 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cc33d54c3bf6b9175e0b145f7c4118<br>SHA1: a3816e7df4ffb8f7c8a3e26e9ecc5b337da78413<br>SHA256: cacc1ada016c1e717e0b0224945498ec7c02f45e18e6ccc3f699cf925eb98541</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.77MiB (16.53MB) – 239,599 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d8002e2bd70b383a55c26aa6c39879<br>SHA1: 2e8b5538dfa991864d56253287cfea899c731ec6<br>SHA256: 417be26de93d6c5b8d2da113e60494952f0235ed696211cedbd93a8683cecbc7</pre></details></small> |
| | | Full Location | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,260,981 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1931ab257b12ab9982e2e837f7a344a<br>SHA1: 265a511f4b4152bd6a0cba4302e7e551263bf78e<br>SHA256: af747f9dd2423c564835352c37e87e14cf8cec475eff93b3c6b458b8ad3a8e43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>339.4MiB (355.9MB) – 3,295,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3cd81e94c6b15797cf1a60147cbd224<br>SHA1: f49f6c791890b20c1ca8c05135f5558493b09356<br>SHA256: b412df8ef796f81fa4522b3051247207cb9af864a32937188218b559f4a52daf</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-07-22<br>IPv6: 2024-07-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.882MiB (5.119MB) – 244,344 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f71b297b6d31124fb4d85a0573420148<br>SHA1: c19cd0e022cce41cdad248812b6ed96ce01f3d96<br>SHA256: 4f6fdac09cbc5c0e25e4305fde012ad03b4b27ba701095ec557f2c1ed1c594bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.18MiB (19.07MB) – 276,325 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 455753ce19833b0e8aa5a719617562cf<br>SHA1: b7cdef244498f6ea069a0523ddc0f9997aed06ad<br>SHA256: 7da4ff6463125871ea8fa12c1e2c0bb4c82cbd5eb13603b15bb06a6c12f21dbb</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-07-22<br>IPv6: 2024-07-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.9MiB (180.3MB) – 2,978,355 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec317919e654aaf26ba2956cba42987<br>SHA1: 5a1d6e846a17d001ab2649860d9e68064c6a788d<br>SHA256: 5099491c3b03773fa74caf9833a9dbb55e732c359aa505587dcd7b44b8c904e3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>200.7MiB (210.5MB) – 1,942,692 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 038ee21bebef5c2336a17368fd32209f<br>SHA1: a21d0b165419264ad815c5d369b16dde7b1ffe6c<br>SHA256: 7d3aaf19058abf9358cba535f4f8cc3c6475d21045808f084c2bc63c0857a3df</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-07-19<br>IPv6: 2024-07-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.870MiB (10.35MB) – 494,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7bbdec4b6ce94a17c1484166976b8c5<br>SHA1: 33490c0c3c8e78d8b7c5b9431e06a115cae578e2<br>SHA256: abbcea671cf67bc19b6f7a3749f7502b4addd989e9ebdcf73c2a227f6feedf31</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.55MiB (20.50MB) – 297,132 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1de85b06e5bffba9e6b2331e9c9a2397<br>SHA1: b04f3f417f6f9ea790f4c39ec11a87dfa4fe723d<br>SHA256: 5b2413351b8146115c634d8225787362820cc7c668ae324ec11acd85751a8316</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-07-19<br>IPv6: 2024-07-19 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.6MiB (126.5MB) – 2,416,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a23b394263db28080421068aa616a68<br>SHA1: 686f0946303fe4e8b60eadd76fee9b80baebf2e5<br>SHA256: 40c364c282f2bbe058d21fd24d002987dcb7a4a04b7cd7ef762acc49678fe66f</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.7MiB (136.0MB) – 2,416,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce3e5b997f3247b0d888416c1f06b726<br>SHA1: 23cd2e39e07ed6feddeb9d27f1ac9b7249d8d04e<br>SHA256: c090142bfc577fb5046192a51f5c407e49fe9b630aa62f7d86756a2efe53bd28</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.4MiB (126.3MB) – 2,416,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 102ad171b5b3f3385ca2c52dc93d2baa<br>SHA1: 19ae2dec0b63b26de2186e2d3b90bab36654b3f1<br>SHA256: 510d278fb8f894d26269de7925d748b035db7a5db39089ee2e98a5735646c25b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.9MiB (128.9MB) – 2,416,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1062fbf1a006dfc11d40b6ed157ca44<br>SHA1: 03e1feb4e6edb446a15070d0c55fff5777039c2d<br>SHA256: 4ec695717b0a9de1adcac7d230aea904fb79db564e65c748b07a886c1374fdcb</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.4MiB (157.7MB) – 2,416,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b237e85abe3657ea3478717d154b0868<br>SHA1: 4c95ab406b88009609331be9839e72c6ed59da87<br>SHA256: 6e9a00d778b569d8801d3e539da5d1b67745524bb98bcc86ba468d1bf9257ede</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.7MiB (125.5MB) – 2,416,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51ac4fc950097b9f0cc585a57978c58a<br>SHA1: 12512ecf5a4dbf1f076c974112935b7bb9ab9725<br>SHA256: fd81088751600f61b9c8ea92a3685263ea4b1e21da57890a5d94c140020a3714</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.7MiB (153.8MB) – 2,416,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93f635aa3d383dfdf02fa6a56e92c07f<br>SHA1: 9f83f1081dce6ff01d31674a68b6d68c7c9d56f8<br>SHA256: ff15f3ece32b315a1be48e7c2401c09e29f033ba8c2d81308e256ab4871c9b40</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.1MiB (129.1MB) – 2,416,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afb726eda9bc78d02156aac5ec32db11<br>SHA1: 7b4374cb65012cd83815a448b6212452ed83825b<br>SHA256: 863a612d2f7da2b61182a0021aacee73ea384b5b3f8bfb8a50e35d5a7dbfa36f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>117.6MiB (123.3MB) – 1,266,395 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c19564087c262413f296fd79556d597<br>SHA1: b5ba4546d559cd1c72758db701cb466b8a8bd301<br>SHA256: 6608bc4af94870709317af91d61496184d28f17db78701c7c922479b96ec58bf</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>121.7MiB (127.6MB) – 1,266,395 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbefcd50cdc7a8dc90cb24f25cff9659<br>SHA1: eab8e61ef4ec5c81bf117b5ca7280e5bd403c402<br>SHA256: 0749a1cd7cd35c690efdc6976585573ba3a2953452ecbdbf9d8c1edcea7e364f</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>118.0MiB (123.7MB) – 1,266,395 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54157c7a02a4534a7d430aa355187e35<br>SHA1: 43adbb885de77f9c6a4796a13d19d13ccc633139<br>SHA256: 43885d56bf7b656d1f69557ee6240ae557bde223ee0f3bf9d39e50206dab2bd6</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>118.4MiB (124.2MB) – 1,266,395 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 839f53ce723f81d018e330bde31d08bb<br>SHA1: 1d164d4cdedbc8aa27ff7b4850ef8fccada7c1e5<br>SHA256: e7f1eae6f9263fa8d83fdbc5f8dac936bd94a449f4c8beea1ebc85b7eb74ce09</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>129.7MiB (136.0MB) – 1,266,395 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0892c1ccb24cc1d172443e6ac9362a37<br>SHA1: d2ccb5e5c63efede43efea270c73ada05751e030<br>SHA256: a30603bc76ea0778c5400213d9d2054049bb7732ece69a612ca3f58aa036c079</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>117.5MiB (123.2MB) – 1,266,395 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a66a52d81cb0bad7603c308566ebbee<br>SHA1: 679b8160125f95049ad3a07622f05689a45ebc51<br>SHA256: 92a473473ecbd23714e907e8c2fdddf41c37f73a9509e871d43a424d53f7dfc6</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>128.8MiB (135.1MB) – 1,266,395 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9d71e983ee5c1ac4366816c9c747485<br>SHA1: 3380f828f6cc3532a63ccfd76a73b648bd91471d<br>SHA256: 10f98bb47876c719a052032da17c1e34766a104620d7cb055ac2102abff826b5</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>119.5MiB (125.3MB) – 1,266,395 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e7f191c70b739235f94a320a29e38c<br>SHA1: 9ded0365183c17162d5adf897762a9880be9e0d8<br>SHA256: 60f2a94959c7fc02a59c1b5051f2e12c6c8fbce0535d0f9d98efc308d51a57e6</pre></details></small> |


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
