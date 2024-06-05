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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-06-05<br>IPv6: 2024-06-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.847MiB (5.083MB) – 242,644 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5b7471500b8894897888969666fc9a7<br>SHA1: 74004328cb097d5486d4dd05885923ba5111a393<br>SHA256: 59d01050edb0ce2578b6f1cff1f28a93cbe201bcc073355a9782b0e98be57573</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.418MiB (6.730MB) – 97,533 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 466f7dfcbcad5d6f39d2dd43c030b368<br>SHA1: 12a8cbf030f7283a6be0af14cace9b9ebe1cb682<br>SHA256: eade48f8ce288a97a0d3541e035b2dc95a9847e57dba2139a9083f6d42a87359</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-06-05<br>IPv6: 2024-06-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.173MiB (8.570MB) – 409,278 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8bb5e9a0366e36e2407c16e8c11ec6c<br>SHA1: 16fd1a9905ca31a1e30204ed03c68dbb9b489c6f<br>SHA256: 98324857c1c3092742b2ff98b80083b08fe2e64f23aa2096f49d733cbb9d1b0a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.389MiB (6.700MB) – 97,212 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7fe159b6ef3ac2393cf6f92a70f6932<br>SHA1: b00e51714ec788bf1dee08e334202e0da77f7626<br>SHA256: b9fe01eb7277c47ad9316cad0d88e464d49c67196010c7ec36a1fdda6b326865</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-06-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.75MiB (18.61MB) – 888,025 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea5ef67bbdda611bfce5e877e483bb4d<br>SHA1: f643c36bef0087e92ad4aaadc9fe47dba04ec895<br>SHA256: 48f601de4c9a6bf0d736b73afc09893cc60f4627475aa87bdae09fbaffa9ebb2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>82.76MiB (86.78MB) – 1,257,706 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eac6336cbfd3aa1743feb1d12ba51d5b<br>SHA1: 35e0c7fa80b02c5703e552aafefb94ae3f4e4316<br>SHA256: ce0c923fa011a8ed77ca80577e40a10cd935c72c84b4108a0630325aae145b11</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.920MiB (7.257MB) – 347,790 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228d49dd4c10c1d4778473109614f06<br>SHA1: 84aeb9072586fe27e7a2fd0cdc62b4421b417010<br>SHA256: becc801a5b95a0c7e6dea789881460b3cce70a60f8b941077db5db9f24f332a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.87MiB (16.64MB) – 241,164 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77063c075f456a1e11f7a52af24ac9ce<br>SHA1: c787ab002266a3398026d5342c963fd1ea59f3b4<br>SHA256: 72503d5df7ba2b39c61d7f574dd167649fdff103e81019ba98b18c192a045f0b</pre></details></small> |
| | | Full Location | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.7MiB (195.7MB) – 3,261,621 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d700e342b096e0b5285fb98e7ea719e<br>SHA1: 95986a4433c4d6be7ba8f0d38d9ac62adeb2d962<br>SHA256: 48ea78edb396cd5b834f2a55d80909bfe196c2ba8756c47776a331bc1537686c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>341.2MiB (357.7MB) – 3,305,843 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8cd42e639e764b6915b74d34e29681e<br>SHA1: 59487357d7497ea585a66be963038da0bd3d8c79<br>SHA256: 093ad3c5b00a0620dd5ab55a96d31fdbde283e096d5d86611cf2e0af2cb6f688</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-06-05<br>IPv6: 2024-06-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.893MiB (5.131MB) – 244,932 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffde7736a4dce2d1dc8a9bbdbbed74a5<br>SHA1: b43b198dcef1ba6df65e58c1860df753727d07a0<br>SHA256: 8724d93cfde83ae2b1ecc823b3e74fd2991e6b70f24b1547c184c710023795dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.66MiB (18.52MB) – 268,413 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0affbc6694e8124ef8380a96f029473c<br>SHA1: ee3211b937aab5e966a663960fff6c4ebac1172f<br>SHA256: 1ab2b436fcbc1c46882e731a91c9c9ace7151e260ba27191c665827291450dad</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-06-05<br>IPv6: 2024-06-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.2MiB (179.5MB) – 2,966,969 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23fb370ce2d6e35cc080047ec96854e<br>SHA1: 6375dc2f3658701b80ddbbb07172e7979cfd3c60<br>SHA256: d5616074b0d3213fccda295fa79eab456cf538541040ad6d2b330f9b8e18e286</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>192.6MiB (201.9MB) – 1,864,338 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c773064f37ebb2a011fd7af63e5eb82<br>SHA1: 2b1c4e83df9f45b9539528f8dc4a01a661ce71e9<br>SHA256: a4a6a481f67fa24ccffea017ecff51d398b6046177a33e77ad479f97889e8457</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-06-04<br>IPv6: 2024-06-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.742MiB (10.22MB) – 488,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af3a5a5f9d3a403425eb90b2e97d3400<br>SHA1: 2d899b8bd9b366e1b6d5f93abd188a5b8ecdf658<br>SHA256: 2a08829255ab75f234239f405034322e2633631a7d7afc944491199b86988ed9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>20.22MiB (21.20MB) – 307,303 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc50bffc6ccb621fb69661f2de795f22<br>SHA1: a046f719afa486325ba82a5a55d0b485eab9a4dd<br>SHA256: cb8fb0177f8409c91a11787d83ed6e20b4a39ca85b5a693ed9bc348850910c2d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-06-04<br>IPv6: 2024-06-04 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>117.8MiB (123.5MB) – 2,358,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74a5031cd2cf35ab18df1e857ba36aa0<br>SHA1: 32cfc50ce1c8070e5a9bfabe4b50e7bce62ec1f9<br>SHA256: 56c964cb6cef089db6468235ae8d7360283b16932df3028e66cee3c3588bacb3</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>126.6MiB (132.8MB) – 2,358,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ad9034293ae5bce5b1d3124679aafb0<br>SHA1: a3645651e69220901dd826c60e8eee97f188d2f3<br>SHA256: 7c94369c180650014a4349e7b0018dcbaf6cbba7cb33b5a64850c000a8fe9ead</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>117.6MiB (123.3MB) – 2,358,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3872ce7a6650b1aaced63c36c659050<br>SHA1: bf096626b67bdbaa3077da55757812b23d666aab<br>SHA256: 49bf597209738afaf5843fe509039d5cf40cc0cca03f06055cc0f111d89f4b2e</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>120.0MiB (125.9MB) – 2,358,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d03f85fabd6c724b370375cdbb1cb1da<br>SHA1: 99ebf04ce008227b54884c5cdd2e0fa5f9bb18e2<br>SHA256: 96054e0b7d22acaba6b2255685b221015c54da3a9ddd9025d3ba8f588331925e</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>147.0MiB (154.2MB) – 2,358,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 023fc24d1954e4b6d89cd3af5506dedd<br>SHA1: abc2a2b78bf82021a5401d565bc4523fb288ff68<br>SHA256: cff86a93fd734f6b9149803333d54d07c8a3fee70393b37bc733c906fc7e7506</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>116.9MiB (122.5MB) – 2,358,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66aa5fb2087e340a1f88058356719891<br>SHA1: 48d25e95dbf65d390c04d769223722843600b97c<br>SHA256: bda0fde29ea43ac058f88eee894aa38ee4d31a54003a1a87bc9fd1377e6308d2</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>143.4MiB (150.4MB) – 2,358,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a30c80e1a841f4c27bed5cb3cceaba1<br>SHA1: 3ca4c5f101aaa41e951afe4ca310b9139d162a58<br>SHA256: 5f25bb853d9ea9eeee491e64397b54d31a750430d602115ecc994f95a5bc33eb</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>120.3MiB (126.2MB) – 2,358,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a289a6a4af0d0bfe23070c24e406bb17<br>SHA1: d499e0df142928237cb44582c806e2a84da7d584<br>SHA256: ca8c6b2919e3220df4f20aacd7336a2ed9dd5ded8549deeeec763ede69fed35e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>108.4MiB (113.7MB) – 1,158,785 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 475bd6f0ffdb15383615699d2726725c<br>SHA1: ba83be4bd8a2433543e3a3000d079002baf8549a<br>SHA256: 5a6622d45f0da4017fb57cf89c72bf0e0f2dae0d4bf0bb48fa9251bd7bce36e9</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>112.7MiB (118.1MB) – 1,158,785 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b05363bff6bd077b62dc9bceb5223941<br>SHA1: 6e54b3ac187e6bcc85319e942f6188c43da23216<br>SHA256: 656e9395661c3f4f6acd33043c56a4f9a5e746146e6546c874d8604e3734fbfc</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>108.7MiB (113.9MB) – 1,158,785 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45a48512a1cda154c954ce4f3ae16b7d<br>SHA1: e8f5a11178a027a3cadf7c13290b35a11e2b4280<br>SHA256: b9120b78d74277e6191334e8b1cf4abf833bea1696887a6c39c7d564bea9a186</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>109.1MiB (114.4MB) – 1,158,785 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d93e0d105ffd2e5fbf6b90e89592a3d6<br>SHA1: f2c745a7fcffd2a70d869c2b3f04be34ba851f06<br>SHA256: 7cfcaf15ac42a05172ec240b13531ca961ba673820f6d1b4d0f5cd4f02c9ac14</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>120.3MiB (126.1MB) – 1,158,785 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c39c15a0dcfef127b9b5ba7d9591bbe<br>SHA1: 6d455b94802273e0a9ab69311e60523147ab70ee<br>SHA256: eebf97fd11336bc42fdb633d2de48bd4d8d116f468e37d3841b7d61710465691</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>108.3MiB (113.6MB) – 1,158,785 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9411d47637ed32342fa03b2a31b7bad2<br>SHA1: ea8c3f45aafa89b5bc0614df9fd35fe2edc149b7<br>SHA256: 9df966ede175e426f2c6803a0166aa28ee0d6b184723681662ec0b0a54486d66</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>119.5MiB (125.3MB) – 1,158,785 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbde38c8800bc8fb468cc3e98098b5f5<br>SHA1: 5061547282fef2fc3ebfdfc99f43846765f351c0<br>SHA256: d155d9fd5f70616d52ea9e8bd602c52a6a4e749d175144e030d185a71ccb562b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>110.3MiB (115.7MB) – 1,158,785 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dad9b79f1eeb95892f8f9fc1c988ae2<br>SHA1: ab2373add3109b508db88c4941d66a1e0301a908<br>SHA256: e7e6bf58fe3184912202950fc65aef71f3157f812e7a0ad9e6de69898723e3f8</pre></details></small> |


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
