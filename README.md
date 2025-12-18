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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-18<br>IPv6: 2025-12-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.416MiB (6.727MB) – 321,269 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3847b2f019ba7ab5ffb99e0696cf0a68<br>SHA1: c7bb934d7ab286d6fae7010c1515e00cc36c6ab2<br>SHA256: ffccc7e93b3eb59ac295997f869dba3d3424d53065ff79d084a1fc55067f4e07</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.17MiB (15.90MB) – 230,466 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03ca914093958e9992c88db2de1520b0<br>SHA1: f86641071c133048c0eb4e8c0c6cf7c5516ea736<br>SHA256: 9668964140abdd93e6cd0dead15fd95cab2f316f32b8ad0a4ff58f0e2aee2895</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-18<br>IPv6: 2025-12-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.754MiB (9.179MB) – 438,333 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a3754bf03c6dc7680efbd1d2d7f5f8c<br>SHA1: 814de672bcc7ccae78981d470f6ffa03b621f985<br>SHA256: e6ce5d543f70d7bbb40d0ca7843c964665279afb0219df57dfa69b1b5ab4d4eb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.585MiB (7.954MB) – 115,388 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec351498b7e416d6ad8a58036c226c01<br>SHA1: 2370948f691479815e6139e323f12533ec058f5d<br>SHA256: 7ef00a470a74c8c121c27eb352991af7711c93ed465cc98954f7ef3102cf142e</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.18MiB (12.77MB) – 609,768 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aab615076ab6e8c79ef9bf0839b23132<br>SHA1: 5ec85482ba06131b3197510d13ea47f5677ef079<br>SHA256: f972703dde7c5a53428e85f510ba87413ef0baf042e66c2043a37f7143eba8ae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>82.05MiB (86.04MB) – 1,246,922 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b630e40c4118de1d3f423825abc95c4<br>SHA1: 7dc492673c44b64f14a17548c2d5165cd1791377<br>SHA256: 286e9ae5b92a893d57c62d3027718fe4289557d1c7c538eca4218141a2569afc</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.196MiB (5.448MB) – 260,054 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd1da47eecbcb1371255bdc50c718d77<br>SHA1: 750933e1de8cb3d548ac391160af871b871bed93<br>SHA256: 057d957bff860585d56f46ecfe886d386bfef914406c23dbc1816ac00ba37c62</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.00MiB (24.11MB) – 349,485 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78fac9141a055ba1200b9e4197d17a6d<br>SHA1: 2dad5e9fe9e6680a486b8de86a165bcc1d75629c<br>SHA256: 2f85601d58de0e24dd53e1f990a048c34f01bcf4433e39e78d3d87d89d39ae02</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.5MB) – 2,947,207 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd8aac3eeb88b310fa305cd0935ecfd9<br>SHA1: c74492fae9ff6ac08a5c5dbc08bed733d3da06ea<br>SHA256: 1dcc9f177867a631fe4c98c83a10cdb7d7578efba05eb4d13a9d34ff00ead1c9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.3MiB (305.4MB) – 2,823,618 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf7686fea78936ceeebd798c0594060a<br>SHA1: 3bf18b3cb9ecb79d04eff383fce69df36bae3d51<br>SHA256: a5bbe43965014f4f35c9262bd8e7ae3e3dceb030619ee951589b718687fc8ec6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-16<br>IPv6: 2025-12-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.29MiB (12.89MB) – 615,201 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76f5589a8a7898208f02730cdb75e6f0<br>SHA1: 60e2cd5b79b62e7a731d8c7421aaf867b49d5927<br>SHA256: 29ed8f5844783b938cc51e88521eb1f90a2bbb9a2bf105fbfbc5514e7c90bcff</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.81MiB (44.89MB) – 650,620 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49b132361edc8909bf28f445e5653c4e<br>SHA1: 621784661470db1e95156c7ec8ad4ef0c55fd773<br>SHA256: adeef9cfd41c86122791861640a2483ca9568bf19864a614a3416e2318994d1e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-17<br>IPv6: 2025-12-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.6MiB (187.2MB) – 3,524,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c7f6f7ac369fdd5f71f3e1d73031625<br>SHA1: 204e640ce312ab77c049e73d453c6279f8244356<br>SHA256: 048ad8be4c8ed4a31cf763561aa94d620a5d74e4acef33ad91bc9365efd5d398</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.7MiB (198.9MB) – 3,524,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97a0a59831d9a4884110af6b7452419c<br>SHA1: 46424d585e5c0a02e7c40f232522c2f22a1fc72b<br>SHA256: 67b55829942ecd2d2cc9679f47891682f79a8560f054e0ed754d125fb0b6b70b</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.6MiB (186.2MB) – 3,524,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed5bb40e7827355f58185c0bf09f147<br>SHA1: e102b373b98ad4834713fb7e71941a41b604f2d7<br>SHA256: d51d651a41194b168ce03bc8d2b246a3bae4115de75a9b84163b5b9d52f823de</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.5MiB (189.3MB) – 3,524,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0668200712db5f8b0a23ab11b3fe4b6<br>SHA1: e0f03332965260c8d159d00704413ee265a1fa7f<br>SHA256: dd6391d2ce1aea47759512256566b906d5c17bb86dd2a9a5461f7ed33d8f15e8</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.6MiB (236.6MB) – 3,524,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4790542189821813e43a46bf567c514e<br>SHA1: f0cc9dc028f03dec6ee98d313897881c083ef437<br>SHA256: bd15be2ba03a690edd8b44eb71878f657dcbabd087e18bdac53faa6743622e9f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,524,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f040bfaf319b187e0b72c04b367a697e<br>SHA1: 4707ef9fe0379b77ae6d85ea1fc633f97a2e9b54<br>SHA256: 815299ac0aa4cd5fe3caa9f159f649f6c838e127eb6a1262e63771ccd7b1be93</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.5MiB (230.2MB) – 3,524,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af1bfb91b01a9ed000502c651441062b<br>SHA1: f77b87894771c9aab45c05e35cb3367b88eb86b4<br>SHA256: 2a0452c234342a13a8424de6f498d92e047be278e792fcc2a853d4c983c11b41</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.3MiB (193.3MB) – 3,524,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0909ee7c2902082f346c5906fea7d5cb<br>SHA1: c13b1e7393e35e00f4032304e583984fd9f76192<br>SHA256: 074a23cc0daa39143cf83ab64572d6acb31727fadfbd8c578505c0a231353196</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>185.9MiB (194.9MB) – 1,959,392 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5fcd65684a97acceff7235cc152d98df<br>SHA1: 1848d433dddfb441ee7b8bf00d266af8a630342b<br>SHA256: 0adaeaf56e730ec175c26da262c59c93dadba698e6ad305af0ca8db146d87e21</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>190.2MiB (199.5MB) – 1,959,392 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e5781c8b8eb742960398246c85841ed<br>SHA1: 13843157e12db2126a1926036bfeb8d58b6cfc27<br>SHA256: 10d97fc6ca812e773b61fe01a129d10dc35f65137abfc9ac50b8a04ae9c77f46</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>183.6MiB (192.5MB) – 1,959,392 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15caef5aace4bf86db3e7097f7969925<br>SHA1: c050b83491a8c1a653a2a437f10f13219b7e7099<br>SHA256: 0c7ec5a42f66d47f755b786e81086bdb7347ee7257babde9b923d102e236c680</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>184.4MiB (193.4MB) – 1,959,392 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f950dde14f3ed4fc7262f1ff65df56e<br>SHA1: 85519e881d52f1718e733046f18854c70e69039b<br>SHA256: 8f5eeed8099afcf831c816e3e5dfadb95e32aed53502e1c3a924b8c66ce13699</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>204.2MiB (214.1MB) – 1,959,392 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7feb6900f196632e2ba1e4eaddf4bf67<br>SHA1: bbd1699680be3f8401e2407d26637b4b15a4f316<br>SHA256: 08b75148fc4b201b8f230107e533e1281f8df16cb6b009319d495bcf83fe5e6a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>183.3MiB (192.2MB) – 1,959,392 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5df3ba68d18ba2ad88f6d03837c0624c<br>SHA1: 557b50a1d57ee31cafa47404ae4341b05dd9d38b<br>SHA256: 5684030c1bf94cc5e79bf6b48d2db131671f8021ccbd6863a33654814ad10a0a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>204.2MiB (214.1MB) – 1,959,392 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba38d76e77fc386e2ece62f8af12ceac<br>SHA1: 29e44cc5a06cc22844715c3ff763f77abe6f28c8<br>SHA256: b08218872be547eebb28541069fc6a1734d6adbd7f8c21111524e9283e68639b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>186.9MiB (196.0MB) – 1,959,392 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a4ea312db5e9492a18e96d7e5db55a0<br>SHA1: 27d4b964f8c22c1b01193bd0dfca1c23df07e0c3<br>SHA256: 2022aa2f5280517f8341a4e0d8640196ff8ff513c025a8fb5dfd17d78d87b26d</pre></details></small> |


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
