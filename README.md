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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-06-06<br>IPv6: 2025-06-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.266MiB (6.571MB) – 313,799 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07d85a5a441b91dfe3573b11b3b24bed<br>SHA1: 2e2a7ad050526d2170604209bcf3d8f1fcde9b6b<br>SHA256: f6a7353281a13343b2945674dbd3e089ea133ccf306a25116877256e45608604</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.28MiB (12.88MB) – 186,684 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e8ed1e8868b97f95db18bb5571b1036<br>SHA1: 9786d9fd190ff30c0ac628a7de5eac5e81454610<br>SHA256: 5932fd3525e94f4a0ab0e58fcd81de0f20771cdd16eee8105785cc6ce7d2c6d0</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-06-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.67MiB (13.28MB) – 634,117 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c167ff70db411cad18e936ed00b4aa09<br>SHA1: 289fc1253ad3121903bafc332722bac68b3e977d<br>SHA256: d6b79d9e022fc5f41d44f1e7e1a705fa264f40681d02aafb42237edc7943038c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>83.52MiB (87.58MB) – 1,269,243 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d147307e80f71a105275322b2e19da5<br>SHA1: c7975f2be16b2ba30d903e2c99d8e6d12e747884<br>SHA256: 36dd01760ee04826f7f55258a269a35167e46072ac8d8a5ed2606d3c85477593</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.020MiB (7.361MB) – 352,022 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5d6ce30939ecacab9e5fbbde143dd7a<br>SHA1: dbe45e91ef39b1de3ae5caecefe6dce72faff5e1<br>SHA256: 843f29bd3db6468809b0042da7a6b44aa5aa0f7b3378bce2344b427d7b8b2458</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.50MiB (17.30MB) – 250,746 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86b9bc39132e2d99653445ab24f13e89<br>SHA1: 04cafe97346c96dfaa2a0c192e271c1aa18bb99e<br>SHA256: d337bc1e4ec66010e25e0e0279f489bc7bb3f2218829c1b952e7b21620faf6b0</pre></details></small> |
| | | Full Location | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>189.6MiB (198.8MB) – 3,310,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1255823f4fa6d96cb2339938032ec17<br>SHA1: 7bcb7165d5248f918857090fad507b3b62aff99f<br>SHA256: f33143e90c472ffeaf3431c1f790ca9297c4fcb75c4f9b48690bbe6cb9d79c80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>401.5MiB (421.0MB) – 3,898,653 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50981857bc3865133c307de9e8f457db<br>SHA1: 915f84f9ac8ac491a0dc82f8e1c8a8b51e82b9eb<br>SHA256: af893c4ae1cfc50fe6b043a92e1ececd960d30f00aa8a0067646fda960aa8ddc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-06-06<br>IPv6: 2025-06-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.060MiB (6.354MB) – 306,250 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66813478af08592fdfc48fd31bff150b<br>SHA1: 811a9109b04c7e248ec3039089a3534799a0b45e<br>SHA256: 7438026d984ce77dc6a3c83ea0623314e8e04ce52f031ecb819c2211c10dda60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.18MiB (22.21MB) – 321,882 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dc7e513e52e0755f6fdadbaacc17b5a<br>SHA1: c9ee76ff47638d91e8db56f68fe6b0d1ca2f6cef<br>SHA256: 35bfcec7d2598e67771e9d918023c4280f9109650acfb7bc6d7776c000fa7505</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-06-06<br>IPv6: 2025-06-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,073,788 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5842c1e89d9e6a7ace62a726c41126ac<br>SHA1: e3950375fff9f4e7a1b551e841a320f17e1763f3<br>SHA256: 136c0e48f44d563e0a01829656f7c14024757ccb342856959d0a6797ee9afb85</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>243.8MiB (255.7MB) – 2,366,384 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e93be5d64be521626b8e98eb9c04690<br>SHA1: 8491599042ab2c0661a6d9968a86b0de5322e2e2<br>SHA256: 699e1f5782b93d7acd864659595c72dc1e8bf20e3457b3d9fbe5503103a35841</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-06-03<br>IPv6: 2025-06-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.94MiB (12.52MB) – 597,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58d37885eb9cba3e325161c5736f8571<br>SHA1: 8a7a37e058eb777dc8390e26798ee5ce2e272136<br>SHA256: f066700f815e0c191f46c3cbdaf1d30ab496a58c358c0c7b52309669229d1d5a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.96MiB (42.95MB) – 622,425 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a28641c6e1dcda6ffd3118c35639b50<br>SHA1: 96e99cfbc4782833358d50dea84330999513ef59<br>SHA256: 666a20af8b0fd95f2dcb99c0d8dcd8ab835b08b612eba9868b02d078c8766977</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-06-03<br>IPv6: 2025-06-03 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.4MiB (179.7MB) – 3,383,407 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ad7f4630e22856e3c3be15106fc420f<br>SHA1: cbb4e7c6067e08c2f76e9b44ab03a932ce28aac6<br>SHA256: 3df08495678d216c6d6e6446ee004d139ac0a11d273777809b7c9826f83ec0e6</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.1MiB (191.0MB) – 3,383,407 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5962f78842e276533871302388cc9fa2<br>SHA1: ffdde03107528764707d559d91081ffe50774c7b<br>SHA256: 6d63902c47508613b04c0ee5d5ad976a819746b52a7b4c5d2da0b782d00390ea</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.6MiB (178.9MB) – 3,383,407 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 562807cf22ebb50bed06770cd5f6a8e8<br>SHA1: 8b41ef93cec524da9917a65f0627e101fc85394a<br>SHA256: cfeb2b9af97d2ec55068179fc6dc7988250e5ab9bfe92b4d5ee24d26d91edb2a</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.0MiB (181.4MB) – 3,383,407 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba38e304347e7503aff61def72af16a6<br>SHA1: 6f26f9f629a3185dae5a85ec748eee39977d6c60<br>SHA256: 5f18f118a02d58b84dbcba98a2f36b21a6cd18d23479f27b2548ff08a9fc887c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>216.9MiB (227.4MB) – 3,383,407 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 919bd7661f4413b5e1636e95d837a3a3<br>SHA1: f17ca28b391649b243dcd117b244b5f049c812dc<br>SHA256: 3c9cf4fa43f40eb39615a7f1de11ece8ee53ff141dcfae37f8413441d3658991</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.2MiB (178.5MB) – 3,383,407 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 135141e17ddbd921570985e4a0f2cb01<br>SHA1: f1fd159f60c1627d7272769310b5aeb8be194dce<br>SHA256: 2e6e1c298956d4309eb1e8a9c82850d024a8162d545fe637046459ebbc122c4a</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>210.7MiB (221.0MB) – 3,383,407 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25289411dad29795633be57a2ee2f17e<br>SHA1: 6667ae672d07514e668dad96279c231e71931a69<br>SHA256: 95c0edf2d11046356187b8a4aa3cab934e688e4042f79136af40f4ba5c8f826d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.4MiB (186.0MB) – 3,383,407 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 12eb07f326b0787d2b380bd90799fac9<br>SHA1: 058c6d88bf5720ba41364d527da05abe130d77d0<br>SHA256: 58a07ca1380cfd86fd3f7c0ac745bb4a877dbf3f08f3097c226befeb81db06cc</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>171.7MiB (180.1MB) – 1,827,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54d5f5aafbf190fec53051c32d1d0e3b<br>SHA1: 0f03fbfef8cb0a276a734c2521704a629561e2f9<br>SHA256: 42645e6ea9b5c83da4e87b49568b945ee09e80a840699d9c1e5c18fe43e4eef3</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>175.5MiB (184.0MB) – 1,827,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c10add97c2886b2077e545e690fb3a99<br>SHA1: 7fe8b107a6e341e8e94b6af52d4bb8e9d6f9b655<br>SHA256: 9613584f812ce9858f6173e7bfb3ff5f2d04dd822f05cccdfcbcc177c26595f9</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>169.9MiB (178.2MB) – 1,827,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 772280152f119778e3e2d3de40d8741d<br>SHA1: 328762f41dfdade7a6049bae1ba56de58110140e<br>SHA256: b72af3da9d181057e08d768bacb9a25034cd40416871d53005b2a37f0e553825</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>170.1MiB (178.4MB) – 1,827,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1bb75538c7bbd3aff23b029112a4135f<br>SHA1: 5dc52232adb532eb93393d76e8780ca5c277af14<br>SHA256: 3facd2ab8e78177cd84ec55573b52e27a19ce38df03d4288a14eb5ff755faf6f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>187.8MiB (197.0MB) – 1,827,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cadce326823930e4915ddbf963aef580<br>SHA1: 97e9581c1a8547f7bf5f46947ad8d9e7a82bb599<br>SHA256: e27160b8342d9a1f172d20469f773ee06960b07ea67a235e902a46b60949cb1a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>169.7MiB (177.9MB) – 1,827,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d8b0d8bca4be014d7272b394662b65<br>SHA1: 6fa0b4c93a44d4d6abe2b1cb740bafeafed1b76e<br>SHA256: 0fdd20d9bfa6960149d92cee9e86dbb09f2b2520f2d74f4b7fd95f0fb8b74441</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>188.8MiB (197.9MB) – 1,827,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7782f4ba8e9c13533afbca8d28e72f93<br>SHA1: 4cd3ad43e8c52f96166c73794cf23261d68ec81c<br>SHA256: b33fb4c8aeabb07937d82d7019962485eac4d156b1e8400839b0262f2003f474</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>173.5MiB (182.0MB) – 1,827,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ba19ad4a08515c71d2b56c9792c650c<br>SHA1: c4daedf040e07d1f290316005d4ad0918a89128e<br>SHA256: 3513161fd290ce5fc331e65fea8d927a26f44faf36225896cf862325c427ae3d</pre></details></small> |


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
