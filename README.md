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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-06-29<br>IPv6: 2024-06-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.738MiB (4.968MB) – 237,167 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a35c9afb1d4429ffa93de4fc7b38443<br>SHA1: 7080c67a0aaeb89ff670c8665ba711e3c053da6c<br>SHA256: 0eef9a9093b6476c317fb3889aecc7f441100f33faf89e4ce3ed92ff3d71e096</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.520MiB (6.837MB) – 99,080 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b23178aa4e459b4160df9f09f10ba73f<br>SHA1: bb4f0991a54bec42e411131ed4028eaa96dbab5d<br>SHA256: 59318a49e8c540037f99dad2bd240110281e1a96db3bc0516677491a23cdc1a2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-06-29<br>IPv6: 2024-06-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.098MiB (8.491MB) – 405,534 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92b3aaf2be28209bfa170bb162319ea3<br>SHA1: c54bbfcbcebd30cc9ec0bbab148d4c9c10a488df<br>SHA256: 914e8456316c3886c39ae989fb061de00e685b8f4420a9759cacef98f3eca51d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.470MiB (6.784MB) – 98,430 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e76bd96325cd608a6ec4a6750ea2375<br>SHA1: 3c0d8a43074f62303bca7163241cd9b3e9a16a22<br>SHA256: 86268efd40a8982eb3640817a86115a002d0b157cd43be7076a327d50ff5ff42</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-06-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.58MiB (18.44MB) – 879,899 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 872414f4420f10d5a7de1b9b80f65f4f<br>SHA1: 69d6642703f1c9d9639b3691be44ce315b3407c9<br>SHA256: c1be2fe28dc677b682b23f4c1103b54bdc309c33063fff324b1df0780fa62330</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>78.78MiB (82.61MB) – 1,197,253 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434456807bd78e5bf3009679138c09f2<br>SHA1: 0f8a4fc2d2cff2f533c7e8bc7fea6f3eb84de370<br>SHA256: 211da9e5526dac39c2c8e4774b5126a4335284b77e3120b280163aa9718db167</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.920MiB (7.257MB) – 347,790 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228d49dd4c10c1d4778473109614f06<br>SHA1: 84aeb9072586fe27e7a2fd0cdc62b4421b417010<br>SHA256: becc801a5b95a0c7e6dea789881460b3cce70a60f8b941077db5db9f24f332a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.87MiB (16.64MB) – 241,164 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77063c075f456a1e11f7a52af24ac9ce<br>SHA1: c787ab002266a3398026d5342c963fd1ea59f3b4<br>SHA256: 72503d5df7ba2b39c61d7f574dd167649fdff103e81019ba98b18c192a045f0b</pre></details></small> |
| | | Full Location | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.7MiB (195.7MB) – 3,261,621 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d700e342b096e0b5285fb98e7ea719e<br>SHA1: 95986a4433c4d6be7ba8f0d38d9ac62adeb2d962<br>SHA256: 48ea78edb396cd5b834f2a55d80909bfe196c2ba8756c47776a331bc1537686c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>341.2MiB (357.7MB) – 3,305,843 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8cd42e639e764b6915b74d34e29681e<br>SHA1: 59487357d7497ea585a66be963038da0bd3d8c79<br>SHA256: 093ad3c5b00a0620dd5ab55a96d31fdbde283e096d5d86611cf2e0af2cb6f688</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-06-29<br>IPv6: 2024-06-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.882MiB (5.119MB) – 244,344 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f71b297b6d31124fb4d85a0573420148<br>SHA1: c19cd0e022cce41cdad248812b6ed96ce01f3d96<br>SHA256: 4f6fdac09cbc5c0e25e4305fde012ad03b4b27ba701095ec557f2c1ed1c594bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.18MiB (19.07MB) – 276,325 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 455753ce19833b0e8aa5a719617562cf<br>SHA1: b7cdef244498f6ea069a0523ddc0f9997aed06ad<br>SHA256: 7da4ff6463125871ea8fa12c1e2c0bb4c82cbd5eb13603b15bb06a6c12f21dbb</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-06-29<br>IPv6: 2024-06-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.9MiB (180.3MB) – 2,978,355 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec317919e654aaf26ba2956cba42987<br>SHA1: 5a1d6e846a17d001ab2649860d9e68064c6a788d<br>SHA256: 5099491c3b03773fa74caf9833a9dbb55e732c359aa505587dcd7b44b8c904e3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>200.7MiB (210.5MB) – 1,942,692 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 038ee21bebef5c2336a17368fd32209f<br>SHA1: a21d0b165419264ad815c5d369b16dde7b1ffe6c<br>SHA256: 7d3aaf19058abf9358cba535f4f8cc3c6475d21045808f084c2bc63c0857a3df</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-06-28<br>IPv6: 2024-06-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.850MiB (10.33MB) – 493,408 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35c7f2b50d5e0f46a23ae5f866a28aeb<br>SHA1: 802bcb68cb07987d34f9a340028c68c1662d74f8<br>SHA256: 12f3a2f5d60ade69a4d1bf27cb072aabd0327f562f6de994e82489428bc84db1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.40MiB (20.34MB) – 294,810 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21eebf4a11513ef724559cc01f85536e<br>SHA1: e8d5c6daefcb1c99c0fc5b414f312d80454747af<br>SHA256: 9169095fbfab5ce68e27f79ba7ef8ca34f1de3a073ef38f469f7efc10d4acbe4</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-06-28<br>IPv6: 2024-06-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.5MiB (126.4MB) – 2,414,314 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 989195ff02ff709cea8c8dbd8bfc1413<br>SHA1: 7cb61ba7f397d9b54a7c631f5ffbebfa798eb16a<br>SHA256: 018ae9f94e731c94d338a112b6217c48643b5a0cece36ebcd4517648a84fd720</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.5MiB (135.8MB) – 2,414,314 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35c66bef70228ec43dc7a67536838a3f<br>SHA1: fa365fe60f3db6a9dfb72ba9baff78969c48e791<br>SHA256: 3ab0829b2954755ec13916382a21278c9362e9380832199ee44242ec56a31de8</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.3MiB (126.1MB) – 2,414,314 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9afa4b8b3179641961e2664bb008d710<br>SHA1: 08dfb40097fd259cbbd22f1a7dd58cbda51cf284<br>SHA256: 25bcd58d1bd54fec3bbff873e0e85807da5056f78cb79c2da336a57028263f46</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.8MiB (128.7MB) – 2,414,314 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d49bb232b6d8249f0b312ba85732326<br>SHA1: 824fcf26991d4c0fe7880ce856c604d98ba7fbf9<br>SHA256: 6c6835d17ffd2e97049bb4b0a085e50b392f12dd60b488958e101ad89a1528cf</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.2MiB (157.5MB) – 2,414,314 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99576af7e3dc4b5db8a0c2b542540171<br>SHA1: 1e3e9d130b7dff18570ca2d7641434b5abad327c<br>SHA256: e3cd0daac374a5a2870614ce4fbef84c17fc7e06a71294aaeb96f92ae3ac6960</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.5MiB (125.3MB) – 2,414,314 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd1c3c48735bf7ed97c878abd1a24d30<br>SHA1: 75d64b6dfa1f511361630a7b8ebb49b69645b934<br>SHA256: 61925bee910252666b92bc1757131b66fd287eadc1907b3a07818f942e90617e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.6MiB (153.7MB) – 2,414,314 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c87e0e34129b2f14ec587ede0eec4ca8<br>SHA1: 0a95db7972fc8b0baf1e5f7fc216497b853ae55c<br>SHA256: 191bb86da4dde45564ef0d3ae030b645b8f811ed6a16ccdbd91041f309cca974</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.0MiB (129.0MB) – 2,414,314 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44a78ddd68647c1c11490b90f7afca20<br>SHA1: f4391963120885226ba5275bed48303f143e1f3e<br>SHA256: bb6da3b42d22f9e433689685b83914993396eb072fb952f73a07743cd58707db</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>116.5MiB (122.2MB) – 1,253,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2582e4330424b518e9a9eaf5a2175ff<br>SHA1: 299beb4d792fc852d4159052cf49d5964930cc91<br>SHA256: 5f5d392eed558f205cc3df1f08721641d79b4cbd71d825c1ff77a44c675588f8</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>120.5MiB (126.4MB) – 1,253,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6355b6c9abc5ffe99b2d6c4568e4a7ec<br>SHA1: fc134ca99b5e206ec9b9089cac0c4a14dbc324f9<br>SHA256: da46fa7d51dcbb730f59062c084e22c46cc14f5d9571a586ce4e8753cd3e797c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>116.8MiB (122.5MB) – 1,253,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c75c86515a128626af77086c73cc728a<br>SHA1: dfdd88641fdfb7053c45742d8024dc2f70cf9159<br>SHA256: 4ea6cc116c9179d8ff7a0aa4f7dd9caaee487e573eb39f5e9db4276cf634b0dd</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>117.2MiB (122.9MB) – 1,253,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee859ae8d35478a29dee0b04a7666e8d<br>SHA1: 808366d9dff87de7332280f4a46b8d6c7f7609ec<br>SHA256: 3bdc76bdc8d293e1532747ebd544e33e1d2191b37f766a057855763af4ecd2e3</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>128.4MiB (134.7MB) – 1,253,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: def8770a54a785fc3ad3d6ec51115860<br>SHA1: 7671fac4397049c49d6b7b05ffb5cc9bfd2187a2<br>SHA256: 2601ec21edfe3ac75f61517e8ce97f5a043536a34b8521d2f236be588ad44af7</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>116.4MiB (122.0MB) – 1,253,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ace32f849c0f0a7d1bec0b17d76774ab<br>SHA1: 9d787bd5d9fdd32257aec7c0eb1be58a0867982b<br>SHA256: fdec2b9d96694c02794028ead4287c62524bea3543035243ed2fdfbf25d68daa</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>127.7MiB (133.9MB) – 1,253,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1787e4d176a114d51073af17efd31f2<br>SHA1: 59ce3413bcaaacaabfd0cd03df631f098706227c<br>SHA256: 6585af61b299a304667c857d86eaf127db0a714425601e5100ea5e4b132fbf6e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>118.3MiB (124.1MB) – 1,253,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b0ec36cac0577749e156a68c50af355<br>SHA1: 4beb0c2c47dd2b9ff39b358dd3e37d850bfcb44c<br>SHA256: dd09a84f283ed1afcb5c8f799553d20782af64011ad7b78154c2245592e242ff</pre></details></small> |


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
