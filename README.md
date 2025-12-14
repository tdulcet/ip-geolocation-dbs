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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.412MiB (6.723MB) – 321,060 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f15366481e75996c3f3fd38da621841<br>SHA1: 8f54011d6024a9ad6e3c5da90f5759e8382838ab<br>SHA256: dd8fbd158f328d974e191fb26d687831246e72682037624b0a71339df1095a44</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.21MiB (15.94MB) – 231,082 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c055face49a8194ae84c98d83c9dbbc1<br>SHA1: 8704bd68443961b7853e93b78c92a42860778bac<br>SHA256: 817330094fa0ce6487c7c38926ec83e1be8db4d8035c2fcbe3ef7fef3fb2a564</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.773MiB (9.199MB) – 439,279 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6226c260ca5241e4e1a94bc121bbe377<br>SHA1: bfc5a50bb89f8e9aabdbcf98a4888e4faad2f94b<br>SHA256: 30696d95cb56166a36011e7b05241f344bda32ccc2d286ffdf76077a513a641b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.572MiB (7.939MB) – 115,180 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf1eae17462055778c39a41819e8d665<br>SHA1: 0effeef27d629fa50895e5d42b95509eb8af22f4<br>SHA256: 6386993c5204f59f125992cae315456a64a63992d628e2d05788239fab2b54b9</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.15MiB (12.74MB) – 608,096 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bfa52cc294c63700b126d4958ef431ce<br>SHA1: 954caca67a57c89669f711f5904257b9aafaedbf<br>SHA256: 811f0432772a3b657f130cdbe35802df1bff972cedb5722ada83bd2f3c25a7f3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>83.01MiB (87.04MB) – 1,261,517 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7f1339356e48010212c09737aff6c2a<br>SHA1: b65b23a09ff9362a714f426628c20be4408f8f63<br>SHA256: 3b581d6fbd74f23e538e44eb21c7b8bb7d487572160e55f6d92ed858f25e3799</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.367MiB (5.628MB) – 269,273 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f62178d410cf3bce771f73d48e43faa<br>SHA1: f7860e76e84e2e025ff86a4e5640a5e924783fe0<br>SHA256: c1072a02c991020475c91925325c135d490b5d243b47ddaaf047c7cdef840cb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>20.32MiB (21.31MB) – 308,850 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 594439a3c0811d183bfe5550c4fa8326<br>SHA1: 2cdad07afa5d0806f1da62dff5def384ca6b52c2<br>SHA256: 86d5eca80b132381a0466a85510652d17f94597f2ba2f6e7a930843309468a04</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.3MiB (179.7MB) – 2,965,067 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a5854fc5ad699cdf214288eb10b070<br>SHA1: 02297fb66300226ae67a1dcf129bca4e4e77ed1b<br>SHA256: 2eafbe9230ee8d23f99e769b27da134fac2c62d6a74beda67c278e8823866eb7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>277.7MiB (291.2MB) – 2,688,825 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7579bd752fa4e59ed8578642ac57a02e<br>SHA1: dc5caed7e7217beea7fbec082ae0651c0f13d1b6<br>SHA256: 0d03be0ad75f92ed0fe8301ab4717341f744711cd9bce0dd880a1632aee11d8d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-12<br>IPv6: 2025-12-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.35MiB (12.95MB) – 618,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b9bc1caa436bc0db195e950df170515<br>SHA1: 2e3ec94a246dae447c0cdec728a8a5ad6cdb405e<br>SHA256: 606248823fafb6ec9ba5e1eaa05b8671d6147281b5404a444f38f37fc463282a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.79MiB (44.86MB) – 650,213 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d86bc822c8ec1741620e867b7555208c<br>SHA1: 3d7fdaa1b021bbe0cc5f5cb8463a992a10807d91<br>SHA256: 97d0d8d4eddb844dd93ffa568fd383fec4ccdcc80dc7e228f869937f942f90bb</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-12<br>IPv6: 2025-12-12 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>180.0MiB (188.7MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2307bda53abb7f05b05742098dc6eaeb<br>SHA1: 346c2d8052c4cb4e0b902b240cac97cc472102b0<br>SHA256: 1c1002a96836a068c727fda1446f0f70b79bc54a5c963f686e2761f5762e44ce</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>191.2MiB (200.5MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfb766895ecf6d98d9edf08f0f1392ba<br>SHA1: a973751dab8ab70db391a1e6cfd33159e497e229<br>SHA256: d96fac80e0649b5c452dd2fc007f56018488a83c60d2b2e753f4f20e98f32a1f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4158c4a779bd5d1c4620a4244ad3113<br>SHA1: 09fc64a8c6b629c9432b24f6eeebba30f9d0a402<br>SHA256: b922ff3b3af049ad3c5a3741f96b01022f4b5d4c915575785c689e0f005936a5</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.9MiB (190.7MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0f7dab87c19aff03722d05cfa00c86e<br>SHA1: a964076f52d73b6a1fdcdb5478b96186937404d9<br>SHA256: 1a6bee308ea7aeeee86af2168ccac56bb50a992fe6f24b51581f965c3dea05b6</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.5MiB (238.5MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d20b11014692e12b6e15734c85fe1082<br>SHA1: 4e944d0a49fcaa67139ba4e12133875df1de364a<br>SHA256: d586f20932b496512e8c9424041618cc887a9ec57ab53e0e50e3958b55dea27f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.6MiB (187.3MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a7bede5b2984f2b4ed053489f533314<br>SHA1: 0d91d0ba3c0066b8dbed6ac0ed33b5e157d81727<br>SHA256: 05e90e7031e3b875c01788d065eadab156aae1c22454ecfb37d606dd06d45307</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>221.3MiB (232.0MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d399b0afa2eafa1d394c1c6b5ff859d2<br>SHA1: d9693491145c2b858d3db49a324ff51275ce5160<br>SHA256: da63173e3b3a4374720188dd0f4d00a08d1be4d155ed8a7a13839c2c4d2a272c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.8MiB (194.8MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61ba5b9db0cd9ed10d3aee8ad5a992dc<br>SHA1: cb3eb43ad18cc4d65501e1a37217d276b11a8823<br>SHA256: 690df7c3c31570c8181761b528b30b476dda436b411676160c57898cede6bb9b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.2MiB (196.3MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c42b4bc3a35852569745f0aba4111855<br>SHA1: a9936db361ca6cb8f42ca98b49ab21197b28f72f<br>SHA256: d0af5a29ad9c6c36220da83a569d1cdb12ad67eae198fc822f0c061fa98e9ed2</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.6MiB (200.9MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee801492d9366e0fe046cb574693c5ec<br>SHA1: 656cdb592a80551166896cfd04e727ba0ecef0a1<br>SHA256: 47e407801d8b0a3170b94fdcd66284f43bbde766546333aee81bb597fe901636</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>185.0MiB (194.0MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed30f389de68a22ae925cfde2e4fec3e<br>SHA1: cf3b33d465da8ec1aa38dfa73baad0bd54782a28<br>SHA256: e5daea18225945f28644763b077e11a52706e4404d68c1e75d45b0a98da42cba</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.7MiB (194.7MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d522200734e9f2743e511af411a288a<br>SHA1: ba4f08abe740083d7df2e4856f44b388430047d3<br>SHA256: 6a4eb485e49d2653231db6cfeaa736764c8390a3de10857bdbc9e15db6558020</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.7MiB (215.7MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90be09edc9e23818eac38b9b2e4d024a<br>SHA1: d68f8e5d2a7e88f7c92fb2ce6e90ae8e982df975<br>SHA256: f06f47a83626ecaef191851520370ad971a26089594899f2293b7f0c878a1728</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.8MiB (193.8MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8457111895a3957246e25c50be309461<br>SHA1: 625a2eb8300862bc333ac571372bc81beec10738<br>SHA256: 12ad9c1ca8eac049b92aab2e1f98d433cb6a7fcfcf6c4966fd6cf0547deca91c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.7MiB (215.7MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a20c8be1ee7f8b2690e031f8f47da235<br>SHA1: 6c0465e33456741073d45b882b207cbb912e1711<br>SHA256: fae913b946ece3c524d4d608b6dadee9a36b6eb96cf64e0c008d26cbba4e5ffd</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.3MiB (197.4MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4aa73c1c203a2540321867b649ba210a<br>SHA1: 27a977080a7bee16342df3055227c7f65b1b59f5<br>SHA256: f52377662c4ef365cb01976d5f432402e2f041d9437d296f919736a987468550</pre></details></small> |


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
