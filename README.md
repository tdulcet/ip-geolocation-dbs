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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-17<br>IPv6: 2025-12-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.416MiB (6.727MB) – 321,260 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e9d73f9764e62244585a1ec15666e08<br>SHA1: eb4605f104ca75b380a209f0b5e87c36aa0f4ba9<br>SHA256: 57d8d005ea39a230d1e7d6abd936d20badea52b42a8615eb974dbd5ffdc2f946</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.13MiB (15.86MB) – 229,859 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35921a6b86d1867661c0c4e2d90e107d<br>SHA1: 4929822b650f315cb4463b8d2397d41a0396e793<br>SHA256: 740e9b895bbf8f3154c120ec53f7e01ad235c21b711cb4300134718ebe5580c1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-17<br>IPv6: 2025-12-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.769MiB (9.195MB) – 439,097 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a936ca8b7e0a2875721ed0c888f7ac2<br>SHA1: fd909fdffa3c4cba15ff057aa393de9d3f0e5f0d<br>SHA256: 1aa4c77c35cb83d57b20c23bf0964f8bc64ac7d0bbfc88a114cf962d735b0248</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.586MiB (7.955MB) – 115,403 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1b5f87573ca83f4c9fafbc86312c827<br>SHA1: 4dc98b9d3c22512c17bdbb6dd1dc8063dd9e8e21<br>SHA256: 8fe7f04275abc794778876dcc2e71eb4967f2a377d706b20c039413e69d6ae3a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.18MiB (12.77MB) – 609,768 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aab615076ab6e8c79ef9bf0839b23132<br>SHA1: 5ec85482ba06131b3197510d13ea47f5677ef079<br>SHA256: f972703dde7c5a53428e85f510ba87413ef0baf042e66c2043a37f7143eba8ae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>82.05MiB (86.04MB) – 1,246,922 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b630e40c4118de1d3f423825abc95c4<br>SHA1: 7dc492673c44b64f14a17548c2d5165cd1791377<br>SHA256: 286e9ae5b92a893d57c62d3027718fe4289557d1c7c538eca4218141a2569afc</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.196MiB (5.448MB) – 260,054 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd1da47eecbcb1371255bdc50c718d77<br>SHA1: 750933e1de8cb3d548ac391160af871b871bed93<br>SHA256: 057d957bff860585d56f46ecfe886d386bfef914406c23dbc1816ac00ba37c62</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.00MiB (24.11MB) – 349,485 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78fac9141a055ba1200b9e4197d17a6d<br>SHA1: 2dad5e9fe9e6680a486b8de86a165bcc1d75629c<br>SHA256: 2f85601d58de0e24dd53e1f990a048c34f01bcf4433e39e78d3d87d89d39ae02</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.5MB) – 2,947,207 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd8aac3eeb88b310fa305cd0935ecfd9<br>SHA1: c74492fae9ff6ac08a5c5dbc08bed733d3da06ea<br>SHA256: 1dcc9f177867a631fe4c98c83a10cdb7d7578efba05eb4d13a9d34ff00ead1c9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.3MiB (305.4MB) – 2,823,618 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf7686fea78936ceeebd798c0594060a<br>SHA1: 3bf18b3cb9ecb79d04eff383fce69df36bae3d51<br>SHA256: a5bbe43965014f4f35c9262bd8e7ae3e3dceb030619ee951589b718687fc8ec6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-16<br>IPv6: 2025-12-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.29MiB (12.89MB) – 615,201 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76f5589a8a7898208f02730cdb75e6f0<br>SHA1: 60e2cd5b79b62e7a731d8c7421aaf867b49d5927<br>SHA256: 29ed8f5844783b938cc51e88521eb1f90a2bbb9a2bf105fbfbc5514e7c90bcff</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.81MiB (44.89MB) – 650,620 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49b132361edc8909bf28f445e5653c4e<br>SHA1: 621784661470db1e95156c7ec8ad4ef0c55fd773<br>SHA256: adeef9cfd41c86122791861640a2483ca9568bf19864a614a3416e2318994d1e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-16<br>IPv6: 2025-12-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.5MiB (187.2MB) – 3,523,998 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9cb7ad9f1085a8bce7edf542eb073613<br>SHA1: 6f59d762e7d7894bba9e26cc88258d0a181bb1ec<br>SHA256: b4d35f8f762a54f431c1264d912627c95401a174402f44773405ca01bd6d8c75</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.6MiB (198.9MB) – 3,523,998 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe72037e96e1f03ccb980a0746bc2644<br>SHA1: 6be26d34f4ced0873f4869eca141235f7a8f6c27<br>SHA256: 9922923d5c14ee82608e87497a7738ae61c808d8a24de00f1aee78d192995b66</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.6MiB (186.2MB) – 3,523,998 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e9acb892f213dd417c1331213279083<br>SHA1: 4925722c70caf50067e8dbd98e16897400eefc84<br>SHA256: 82dd3eccfd25f0a0ce8f17b8a88f1d3bff9d6326b28a3656a8cced79c11bb63f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.5MiB (189.2MB) – 3,523,998 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec5450a7f4c61532e8e0f5c9dc894c31<br>SHA1: 9358d6fe40fe04889fd7bc53a6de1fd59f537200<br>SHA256: 9feb0ab8beb37592baac7d7acc52d4457cbf7be1f91acb2c6ef0fc121d214d5b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.6MiB (236.6MB) – 3,523,998 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d61b30b1520c3ce4ccd1d5f95c9d0912<br>SHA1: 650193989a8ef541dc69482ab7d58b9a888c7333<br>SHA256: e9a1e538f568da20a96a40813badaecbd65226f9ad14034b1c619034fdafd356</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,523,998 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6cee987ed4e302dfb89fbc5c65a6f41<br>SHA1: d57abb343400d069e4497198f8f7d696663ccac4<br>SHA256: b532c88f1564daeffb41351b3345dd3fa43204dd042fab1b64d203db05699286</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.5MiB (230.2MB) – 3,523,998 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e01f69ca9167fe2bbe7e198880675029<br>SHA1: dd41cba2a838756280f1683a648a8e52dc4372c5<br>SHA256: 1e392606acfe5c8d0712f7c604e707e86cdacbc942f6360193d5faebbd230ca8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.3MiB (193.3MB) – 3,523,998 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d3a35ee69b1d8d8e577577726114afe<br>SHA1: 9b2556344054b5473f4498e2d95a1998904cd8ab<br>SHA256: 2a63ec419ff4d781cd6cfbd6151be0936440879751460941586918af65902197</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>185.9MiB (194.9MB) – 1,959,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a46c0f06dcd72ea493891bed1f57645<br>SHA1: 34f84fc81f58b39bac6787b522e83f8b0a6af913<br>SHA256: 6a4b9f253fb279a2138c5b9c8c3abb0a90ed21e10d9c089e993ffe23467bf1d4</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>190.2MiB (199.5MB) – 1,959,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11ec05d0db590f4fc6a1c0173409dcf7<br>SHA1: 34272136a92d1808f587e1755a9683ddb7994f10<br>SHA256: f858f76378f8e81cae35520b17a387c430fa3d9d4bd0321022d60905b6125984</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>183.6MiB (192.5MB) – 1,959,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0730f948ec523deb971b43471da3cd2f<br>SHA1: b7a98239bdd16995d52655dfaa3a9ef57a843b90<br>SHA256: 67d1cb34e749fd0793ae4c9ce368b93b02b39c08b37e7073866928f6747a6047</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>184.4MiB (193.4MB) – 1,959,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6a71bf67fd6533ffdf3b41d22b34175<br>SHA1: 57cc9a92a3d56b2dc14c6754a3531007e8838bec<br>SHA256: b4b997131e566f362fa0ed6167e91323496ff05c6c655d9acff7df2f8dd7ef53</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>204.2MiB (214.1MB) – 1,959,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b49d324d2dc5a79dd02e71867026af95<br>SHA1: a5c20f6e562fe30e91ef581c063b8be74018a0c6<br>SHA256: 75a4f932f267caaa2e436964c5a56a5ea9f5474f18a76108dae3346ec964817c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>183.3MiB (192.2MB) – 1,959,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e4ae12ec44c8ff63d096bd793a860f9<br>SHA1: 30f9930418dfaad815e12275e9f4c1d0fcacae50<br>SHA256: d0fa37cd02570eef4f5a1d5cf9db00b70d37c752d857d471d69e23fdf9bddd6a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>204.2MiB (214.1MB) – 1,959,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd6b7df935f2b84e937d0e567bdf3fc2<br>SHA1: fd84f32b210f7525a99b83212850a26a5329ee21<br>SHA256: 6117ed47cbe259e4ac4ba92301d6e7a69336eaf4426b6e31591a22a493d55fd7</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>186.9MiB (196.0MB) – 1,959,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 445ab598203b76d0ec0bbb6f7b369a7b<br>SHA1: 1fe2ad2c6ff5dba407bf612924d7d21f113d032a<br>SHA256: 60f08857ee10b3b9943b8862d51545dfb52f043aa316ef9255ed07f588d1e107</pre></details></small> |


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
