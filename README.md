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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-02-28<br>IPv6: 2024-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.804MiB (5.037MB) – 240,474 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eba6672fbd9e2d1008d7a4d5d5672b76<br>SHA1: 93112ba6b1e941f7b3ff0cfc4c5f7128afff3a12<br>SHA256: f853699307abdb5fd93c62c2d26fa9c1b543ff7f3e8f56729d825b40f5eed9b1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.690MiB (5.967MB) – 86,477 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b96ed0e99d5185573cccf0abd07cfaea<br>SHA1: 9a8037f57dfbac7389ddab3de6592411a43ed6e1<br>SHA256: 9d44010797a502b22db21d3f9756507ce0ccc89129e7f3e568a88d1c41980c41</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-02-28<br>IPv6: 2024-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.191MiB (8.589MB) – 410,213 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 226b52c8fad4ff4e7acbe5e971e589a4<br>SHA1: 0d85477f01bc5e19e33fd56155f6bc654f47f6a9<br>SHA256: e9441700f15fcfce89c098a075cd4de1787ec40d046113c6eb4e873521fedafe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.012MiB (7.352MB) – 106,669 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5bc1982f751bb965df94b9258cf33f8<br>SHA1: 20585534cd04de299fb4b178e064be5bb1f0d253<br>SHA256: f188cdabad1542feae8ffe4f61b400d1c637d16a490d6e34116c30085e15642f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.44MiB (18.29MB) – 873,350 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffdd939b50e2b6b3098adbe1af194253<br>SHA1: 6d2ac9d700193d38154385135b0a3333d1045164<br>SHA256: 8f35c62cacdad0b246c2eeedf023902e5df2718a0c8db8621e58d1ca5d6b8ee2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>58.04MiB (60.86MB) – 882,011 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d906f4b55d883779e7b6854742daaad9<br>SHA1: 4e3410d8f768fec45a3464fe5a217d248d4d26a9<br>SHA256: 7df791f73dc2fef4cd53e9c343171be5bd1116fa9a879622fc8c8c2aef55ce1f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 322,238 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58dc67267f460ea3cf5cad59cd04fb2<br>SHA1: d7cd4a637354f5a5c457e96633e1f5c9cc5c059c<br>SHA256: 55313849f9b0eeefb503ca58aa485ebe95d325c7771a4b2e5e9def19ee8aa2f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.67MiB (19.57MB) – 283,667 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b73dc10990e7bef8c444f1cde6991f<br>SHA1: 07ae49b41bae3e257ad578c4bf31ee8040ccf1fa<br>SHA256: 7ea6211e834aaf328302ede30e6777fc4f71afb40ab1238cf0af2be151b5b248</pre></details></small> |
| | | Full Location | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>179.7MiB (188.5MB) – 3,143,531 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4796f68669fd62ff1776c3d247e13dff<br>SHA1: 8d63c70c0bd62e8829cfbd2dfba8d6b8e6c77fd0<br>SHA256: 04e5000cfd1d52386cf975f825886bb214085c10b75c2568efa51ce70fb6c3df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>291.6MiB (305.8MB) – 2,831,720 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 657b58a340f82d12479e96ce7f695a45<br>SHA1: 1b9c4719ee91d1e9da68e6f0dd1529e893bf9777<br>SHA256: fbe98efa467387f6ceb69603459abde1562d03903aa05b063edc68d9aa4e87d0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-02-28<br>IPv6: 2024-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.640MiB (4.865MB) – 232,256 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fec6f73486236c8d0d94598e079d6f<br>SHA1: 7f19645a2e7ae1f5579b6769363477a0ec58e5f6<br>SHA256: 7f7145aa700bc6d9b86d8e430377fb6751efd3a786e0455999aabe3401d275c5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-02-28<br>IPv6: 2024-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.9MiB (177.1MB) – 2,925,251 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434c9a2a5a5c869e663a7e206ad5962c<br>SHA1: f2e0c48f3ecc7d10f4697a8c5c698e1979b08714<br>SHA256: 8d5321147896799a07280f735aae4be97a74bdd31110778527dc8f4b77485f61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-02-27<br>IPv6: 2024-02-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.520MiB (9.982MB) – 476,874 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b50ff6d5688fa91491e958e24090522d<br>SHA1: 5a402f397136f67a7f139302cbbaf9cc92f74bd5<br>SHA256: a72ad09c05d72a8f33c932adc2d8fc9887661f5fc387d3615638ead5d30dbad3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.68MiB (19.59MB) – 283,872 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80b933c77b8b8b959679f4d837a2f82f<br>SHA1: 130966739cf43861549495808917431375ec9b2a<br>SHA256: 11f77155d06358f4c7bd34bbb8227d2f0b54ba4ac7fcd15da34e9ed80200bc27</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-02-27<br>IPv6: 2024-02-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>148.5MiB (155.7MB) – 3,156,641 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73a886c0dbadf4b95105c9585a7ed537<br>SHA1: d0ada5fa37091d5d811b7867aa5b3b53979c59a2<br>SHA256: 11b8b66130af91dff44ac444efdd5762daeb8f30459c3e4117a8f48bbbdf9a48</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>172.3MiB (180.6MB) – 3,156,641 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c1c8da927d7916ddec8175a366d315c<br>SHA1: b34cea037a14612e788a5ab1b0c060861a8569ca<br>SHA256: 51a4c8113984d5bfa3cf562f5a42105197ae3ca1310a9c0bdeaf6994d8c8e7a5</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>152.4MiB (159.8MB) – 3,156,641 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b08620bf4fa727be99933c8d1ffb0d1<br>SHA1: 2027a9643411de45256329b965cc65861366d373<br>SHA256: 6f33ecd850037f6e513e38f5c01e81b40d27857d312ebc3994b1ebb1eb42fc0d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>158.2MiB (165.9MB) – 3,156,641 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1927cdc185aa51c8cd46f49a91d0efb3<br>SHA1: f47e0bc5f08f481facbb861d6b019ae082e15184<br>SHA256: e61454197bfc7a82ef272df2c1c61b983cdfae707a90901e5a02c3986619f93c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>185.0MiB (194.0MB) – 3,156,641 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 252485b020c59ad5f8072d04ce33a9a1<br>SHA1: e2137d99f620592275f2e6c4f52204dde6dd7da1<br>SHA256: 9fa3d66a0871e45932cd70c9bf785a1022a9a15f408edd8b7545e4f6455cfa99</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>147.4MiB (154.6MB) – 3,156,641 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5590aa698e4585b15fa50f75ff77d9fc<br>SHA1: f0b360c743a5d9e61c90cd3eddd0b4089c4071a8<br>SHA256: 75e2478caafc9871b1e1abedf00bc995e3b237ae5fcbe1472d0cc002242c27b8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>184.3MiB (193.2MB) – 3,156,641 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21b29b8f6e20805cd5412fc4cea43a8f<br>SHA1: d1f4124681c6e34936cc6bd7c50377bb54bce828<br>SHA256: 5f1a33d5719c5bf5a54376ec1c4f4c4a1975a2f7f06214b08acc3fcf393b5234</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>155.7MiB (163.2MB) – 3,156,641 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43b57767929d7e0ac4d3dac8370ea17c<br>SHA1: bbe785f372986a6398dfb2bc5cf478b0df018e76<br>SHA256: 497c72dfc80bc0f3d81f924b97af3ec9ef7b7c01d7f9d4bf311a5cd952528b7a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>103.5MiB (108.6MB) – 1,157,704 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70600504df789b553bf2a0321c39c531<br>SHA1: 639d82c2c826d6aeaa695367d4f10c7bf22a5287<br>SHA256: fc1625930f0dbf63cbfadf8facb42db429e40fe407719b96424482a697cf0534</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>111.0MiB (116.4MB) – 1,157,704 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6582c14619ec2f5c961c1f07560e6c1<br>SHA1: dd5b74af050e516d8ded895bcbe11d6eb1d0d539<br>SHA256: 9616fc20e7d475884cd628e7f472a46ed7628cbe66fbce598922686187535cb5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>105.8MiB (110.9MB) – 1,157,704 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f5189663f6a8aa77b851366082d56fb<br>SHA1: 0c89c8180f15362a5920563a6dc513e2746e2e0d<br>SHA256: 42b7c654933768979e8bee16ccefe53d3ff90f3b4a50de62d26472ed6962bf90</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>106.6MiB (111.8MB) – 1,157,704 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e3ee046c891390f43c75c0ba902d0a9<br>SHA1: 408aeb7c700568e4c6517b29b57f774271de3975<br>SHA256: 128b4da4642a491d51bee30eeb48c3c2b4e96dfaf2594dac601b469454753bd2</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>114.4MiB (120.0MB) – 1,157,704 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a82be2d2e6a16eedc70fba3dff39791f<br>SHA1: fe36b9f5dd0db377935a65984c359d27fd3b3f3d<br>SHA256: 6108b13ad346b8cc89cf4b65e3b519faa4af4e61c770531fe474a5906d410bf2</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>104.7MiB (109.8MB) – 1,157,704 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f86cf9b7e1ce664173721c8c622b752<br>SHA1: bae9b8e1b2a18f74fe34e66c54be33018bd3ebde<br>SHA256: 84fa91ceafaf4d501c722484fc4d2a4f8f270be8c49c2e4384b715300c2e4875</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>114.8MiB (120.4MB) – 1,157,704 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc3bb7fcbbdcb279a5f3795014f8a9f1<br>SHA1: ea0cb80477e0ef2133159358c912ed034ea9a28d<br>SHA256: abf131aa62c65bb5f24aa61ad4c5f947a3a9dc3e2bb979f94a791bdb52d59c95</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>107.5MiB (112.7MB) – 1,157,704 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c2c15062f878f6d649bffb4f4635b1d<br>SHA1: 21a01c902a4cbc1efdeaabe0a99524a079c75fef<br>SHA256: 00b2e663273aa45c48f336ecc30748b3d40139e3c54658b97d89d0e571a8ce8c</pre></details></small> |


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
