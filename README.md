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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-07-09<br>IPv6: 2026-07-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.386 MiB (5.648 MB) – 269,540 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da2167e27a3961a426ea6f031db9d134<br>SHA1: 30d0799ad84c083f2e3a77da74e5317bae7a0e8a<br>SHA256: 12aad0729b61b40f68c8d171f58c85b4237b78f2eee546b9252194ce99176a9a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.75 MiB (17.56 MB) – 254,508 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4febd725624b5a213b3dcc3e336943ff<br>SHA1: cad0301d5fee0a63f12bb7b7e96ef295af5d7372<br>SHA256: a170544647f77d31b8e29359cbd8f43e8f2bc307cc85e886c9f569535b567bed</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-07-10<br>IPv6: 2026-07-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.007 MiB (9.445 MB) – 450,988 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02daf6b976ae86d392fbdc2703400026<br>SHA1: 35f33751b930e2d196850a04245538c9857ec76c<br>SHA256: 2b9771358ea5d36e82f2d08b9d03ff9d3082bf362154ec5b8d110ceb19109bc4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.936 MiB (8.322 MB) – 120,723 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51edf2ef04e1914ff34f738d20518f97<br>SHA1: 56b42a29acc7fe8bf92ca8fb0db7a300ff0f9953<br>SHA256: 6b06af4cde57bb975323d52e7f2613dc1edd5ba5c5eeb65fbbdafa6fea287b20</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-07-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.25 MiB (12.85 MB) – 613,553 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f9903d8e332d302d8feea780c908d7e<br>SHA1: 92b16b52967ae493dac6e584aa17464871f93bfe<br>SHA256: bab3a25716c2dde8e5169b46caef559d84aab838888e6bfb472ff42d7c23282c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>41.59 MiB (43.61 MB) – 631,973 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7a241834ac60e35284b6422d8a42a4d<br>SHA1: 6ff8576b57df55cf1be387292ac543f7d313ba06<br>SHA256: 865faaa46a2cbc6cd43d6b3e06a53c2dcfaf98b88a9d3c8404fa8741e59ced1a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.078 MiB (7.422 MB) – 354,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ec835290735187164b1f2f622ad9c0<br>SHA1: 10464ef5eb489f4745096b1c71046b06409244b5<br>SHA256: 6bc4af63c1e15b4d99d5b9dd9cddeb67bbf2eafc2529ba5d9ec4525e0fe7964c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.51 MiB (23.60 MB) – 342,046 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569d0c6b66a745289f0e152318090f38<br>SHA1: baf1ef75355d41d9bc4380f97ed3b085db479655<br>SHA256: 8940a06c7f9a27f129048c5a7a0b1579b368020d88f2d2efe0fc813b6d2f97e4</pre></details></small> |
| | | Full Location | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.3 MiB (219.4 MB) – 3,666,805 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b729ab459cc2b765b3b4ea035f481b<br>SHA1: 1496af12b72ee784e304cd84eb7335c826bc3906<br>SHA256: 69fc5ebf5414a7a939fc25a35f3128451cf340211ae51ab9f82d53a331d8ca03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.3 MiB (473.3 MB) – 4,386,528 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f197b2ebcfed77f9adc3310fc7b6020<br>SHA1: 24b1454a40fdda39f37fa9367a6a6a5a88d3be33<br>SHA256: 0160ad6b5bca3517eb65f79d6db1f9e373eeb34cfccbf189a588bb330d17af06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.663 MiB (5.938 MB) – 283,439 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5e0b2b6a8aeacf3ff5598adb8880765<br>SHA1: 8804233331909b27cede1b5b43c2f97e3e0fa7fb<br>SHA256: b76b958024d8951ae29a80cf988f69d1e662dcc0bea8d923f50bdc702ec7cf2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.09 MiB (23.16 MB) – 335,708 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a285d07eeae37dd9fc478666744fc01a<br>SHA1: 088c9efb11f726ab15157c87e8ea1f653a7ad960<br>SHA256: 276a36ba7f5863bec8cfdfc9f38541e0dfacd40d41312852daaca8be67b6585a</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4 MiB (176.6 MB) – 2,914,372 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77a6d0d39cccc6773bd841068fea21aa<br>SHA1: 2b573d6c293a367a2052b0737018f62a9b4b74c1<br>SHA256: 63c79df13cea9f7d90cb141a952a0ec792fe5f5c39e6a4cb98f1caae5055b951</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>295.0 MiB (309.3 MB) – 2,857,634 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78f9a0f50b954077a7222ec29768405c<br>SHA1: e7cf8076d18ce13f2ca1ddb68037263adaac2c3f<br>SHA256: 8eb07f6e7f6d570b63e6735ef434d9dbfc7a394946b35bb3ecbb67d2c31d9863</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-07-07<br>IPv6: 2026-07-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.33 MiB (11.88 MB) – 567,245 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bca1f8d4c7d5e56ea449b4b5aa286f30<br>SHA1: 7abf3a8322b29c407c138f23726350db8701d2a5<br>SHA256: a7b15028608994c398bdfc2e572cc25f77cdabb19d651b5c99b42b2f8c48291d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>36.88 MiB (38.67 MB) – 560,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80e489462cb26183fe6926c6a65f2b9e<br>SHA1: c5ff7b484792510376297eb13f28e1c517478e43<br>SHA256: 4b24c8e9bc26b7f02bf6f0b9cb7ca01ede39bd1d82a7cf790d04359bc883f766</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-07-07<br>IPv6: 2026-07-07 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>192.7 MiB (202.1 MB) – 3,752,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfebad95fd283c4b8d6c326f0735ddc4<br>SHA1: 6299e302d0c8dff9b7049249f71f44e67613b59f<br>SHA256: 8fab76f361fa16fcff23967ceab81ed1a9409200b84e518f37893d033dd9bbe3</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>201.7 MiB (211.5 MB) – 3,752,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d7214e4ece8875a4b4c551f5c99f134<br>SHA1: 8cf352945360b41653cc4bf8204a51c2f24490db<br>SHA256: af8844cd366b0395550c8699e3774c396365a40e1f83fb88ca8f9e98e71dc3b0</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>191.9 MiB (201.2 MB) – 3,752,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a338c1e7506df96fc1b3eee135efb953<br>SHA1: 86d8b23b47a9fa1b9a614af96fb6adf3f3857ce3<br>SHA256: 3a3f506ff34d02f5511d61509ed53f2883ac028acd5ec14011a1bc898fb3ba74</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>193.6 MiB (203.0 MB) – 3,752,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 228f78516b023995b1fc15bf381d2e20<br>SHA1: 5a78c8f7e97731db12eaa4844889fc3fe5e70849<br>SHA256: f8de9d95316016e817f6a4fd0a2b21d2f61e78b36e7502b848b2cf87434b8dda</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.1 MiB (255.9 MB) – 3,752,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8625eb350caa29f21515ff4f418c9c6<br>SHA1: a0412a44f6ad0c13e95e8bb1d44bdb32f3d11ae5<br>SHA256: 07364796536f451efb63548c2b7892e5cfa760240bde141b1b8d61182d1a968d</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.1 MiB (200.4 MB) – 3,752,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c233972087ab7c775fff0b8a82e3b123<br>SHA1: d991ab8562b6071441e8c1e90eb7a2308519d7a5<br>SHA256: 3ceba7b79fadae13a97f986c7a644edd0774dba9c81948e17591d08269c2fff8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.1 MiB (245.4 MB) – 3,752,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1fa9cf7861db02964df1e61d0a410ff0<br>SHA1: 61a67ef30e9c1bd53924559c093bf6ad58a3ec8b<br>SHA256: 957529a1b1200f485bd803dae19242ffbc95faadef6c314b2c0e657f6f036c26</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 3,752,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 517b5d706cc0a0f8d54e0c9e85e94842<br>SHA1: 55822f7346b3708ca9aeff6b300fbf2481971d1b<br>SHA256: df637ff1a8128f0bb44267371d3ad68c64799213b98e4a03fc6a0596e4ef459b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>196.7 MiB (206.3 MB) – 2,062,678 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bd775b089ebb953980c83dd7c1e8696<br>SHA1: e534a2b8ead6e8bb3a5596a6aef9eb219d2955a3<br>SHA256: 3ad9529583c4ae07686d168054507913978446a47fac48598c25dbfb007cc772</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>200.0 MiB (209.7 MB) – 2,062,678 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c82db309c76ceba2b3da2b399b60f55<br>SHA1: 55c6e80aeee82e22b83988da7a5b223f45ef95a0<br>SHA256: b25474a4447b2590a9b2bb2612fd450957ba99edca81a0edc537a4d046d886b0</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>194.1 MiB (203.6 MB) – 2,062,678 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd4b5f8b26e19b800de23285f64ef3ca<br>SHA1: dfd9babb58a02d8409c648023f92ee3b80a1ed9c<br>SHA256: c0ae5c5d8af43f6cd8da107356ca679645bdf423d2a64c9ddb0fe6e257b428f9</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>194.7 MiB (204.2 MB) – 2,062,678 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c92c0300d9111d74368938da93e68904<br>SHA1: 8330e577136f9fe906e4681e21a2266927236e40<br>SHA256: 313dc142fe6b69f4ea4cce949a1699cc6954e04f7f6fc0f68d3cbc2f01a16ad8</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>216.7 MiB (227.2 MB) – 2,062,678 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 160cc893d9dc3ec4572594c0c249d5c9<br>SHA1: 123fbb7afc453e02e105af479f7cc6e573e20d19<br>SHA256: 36d33f482a6a76be976c0c601af90ab73d92096f56a898b9566de5a455ccded6</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>193.9 MiB (203.4 MB) – 2,062,678 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c3b45a41ea543b822c9ad2c8c1dcca3<br>SHA1: d38bb8f60693d5aec6a8e90c4e6ef35a5cd7c799<br>SHA256: 17108a8efa1b7fb035435dfd8a175583b87a197c52e5830c1b6acc10f129c587</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>215.1 MiB (225.6 MB) – 2,062,678 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1c52226658c7a940e3bb3dc04ac679d<br>SHA1: 05c3d94b592f726122d3bf9d4c7aa88c7e546153<br>SHA256: 8c78763b5fb160e10633e21f618f0408732a83fc62c154a253c7f3c12aff6290</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 2,062,678 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd26e67deeb0904eae7efa1cd04386b0<br>SHA1: 6cae39060b7d2ce41d4d223924cc0c474d5cd478<br>SHA256: 01c0f0780e8f1b68c17b7cd56c1aa8d2072985041608002ef393f48b4418b532</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
