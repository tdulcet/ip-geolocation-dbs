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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-02-12<br>IPv6: 2024-02-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.799MiB (5.033MB) – 240,270 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8607f40fe8d08a1f017acf92080c892c<br>SHA1: 7a28ae9e1a39f2f2673e0f96f6e06a6bc6f0a099<br>SHA256: 2396e5a7b5a77f3e6971b5ee22cb690c6eb51705d0aa5f4d76646d931ec8c335</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.633MiB (5.906MB) – 85,596 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e23462b86400956510d1a0fe0b62049<br>SHA1: 534659d04df2f9043fd75eccc7879b123b56306a<br>SHA256: 726699d99cfd9026edd1fd9d6184f52c9b8bf3f02781de906d8f75bb92215dbe</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-02-12<br>IPv6: 2024-02-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.184MiB (8.582MB) – 409,848 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b07645e135616728904868cf5cac7895<br>SHA1: 2f9514f168ff9686a9bc4207038d6c88cdaa96af<br>SHA256: e8d64fb4ec50ec565e8b7839c35fbabf36a5b34a8960cee5643977b2dc588b45</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.963MiB (7.302MB) – 105,935 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19e0c980aca989650f5de9258d6f744d<br>SHA1: 3a8f411bc99ca31791fffa36250cbf6bde417370<br>SHA256: 3dba170f23d6a4c545996ebb572b96597028cf5c3e49f2dffc2bfd2c1e608cb5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-02-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.95MiB (17.77MB) – 848,667 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 623c949a5181e5fc68caa29a909eb48a<br>SHA1: 53eb4de87cbe9f49555d9e4fe7faaca6eb48deba<br>SHA256: 836a02f766c9b9fc0d062fdf0ff117bd2b76ff51e81f93ce0d50beb8a8d8863a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>50.71MiB (53.17MB) – 770,638 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42bfaeca4f79a465be1f89ed0a9d15b4<br>SHA1: 5138647c589d719e1e0101cc06a6d6e75528a985<br>SHA256: 080ebfbfeceb5a3a8f4b33649004ccf5915fc03a1a5a230aaa66a83ec7849e71</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 322,238 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58dc67267f460ea3cf5cad59cd04fb2<br>SHA1: d7cd4a637354f5a5c457e96633e1f5c9cc5c059c<br>SHA256: 55313849f9b0eeefb503ca58aa485ebe95d325c7771a4b2e5e9def19ee8aa2f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.67MiB (19.57MB) – 283,667 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b73dc10990e7bef8c444f1cde6991f<br>SHA1: 07ae49b41bae3e257ad578c4bf31ee8040ccf1fa<br>SHA256: 7ea6211e834aaf328302ede30e6777fc4f71afb40ab1238cf0af2be151b5b248</pre></details></small> |
| | | Full Location | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>179.7MiB (188.5MB) – 3,143,531 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4796f68669fd62ff1776c3d247e13dff<br>SHA1: 8d63c70c0bd62e8829cfbd2dfba8d6b8e6c77fd0<br>SHA256: 04e5000cfd1d52386cf975f825886bb214085c10b75c2568efa51ce70fb6c3df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>291.6MiB (305.8MB) – 2,831,720 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 657b58a340f82d12479e96ce7f695a45<br>SHA1: 1b9c4719ee91d1e9da68e6f0dd1529e893bf9777<br>SHA256: fbe98efa467387f6ceb69603459abde1562d03903aa05b063edc68d9aa4e87d0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-02-12<br>IPv6: 2024-02-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.640MiB (4.865MB) – 232,256 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fec6f73486236c8d0d94598e079d6f<br>SHA1: 7f19645a2e7ae1f5579b6769363477a0ec58e5f6<br>SHA256: 7f7145aa700bc6d9b86d8e430377fb6751efd3a786e0455999aabe3401d275c5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-02-12<br>IPv6: 2024-02-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.9MiB (177.1MB) – 2,925,251 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434c9a2a5a5c869e663a7e206ad5962c<br>SHA1: f2e0c48f3ecc7d10f4697a8c5c698e1979b08714<br>SHA256: 8d5321147896799a07280f735aae4be97a74bdd31110778527dc8f4b77485f61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-02-09<br>IPv6: 2024-02-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.349MiB (9.803MB) – 468,312 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cbffb70b3fcb5b12cf41e68a0678be1<br>SHA1: 7ad2c96057df31baa6aa5b695bf6a6e96981ea94<br>SHA256: dbd390beba89649fe780743183a13427d3cf741bdac3e12929171cfe31ac1f6c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.41MiB (19.30MB) – 279,728 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4562f7b749df7b56ee297f0ba5dfa552<br>SHA1: bc8b03c8976f2e80d9fded82e09a86b7b5ad21e8<br>SHA256: 4e1d1f07abc3110d57c59fbc3f7abf942e986bd1dd0bffd89a22a3a803ce52c0</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-02-09<br>IPv6: 2024-02-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>158.9MiB (166.6MB) – 3,376,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df4faef21ca9d7831e4b4244aa3e5ce<br>SHA1: 002866726f573304f3dfae0a3409db992239bcad<br>SHA256: a80854d469a19696efa2ca8c36e6f849d556922dc5ddbfec90d9f6b0e65e97e6</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.0MiB (194.0MB) – 3,376,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d85032919856eb3cccbf489b8734f82<br>SHA1: c7e2ca62a8dc2640576cdaf1ed633700db46dc10<br>SHA256: 500e84f0ec01b838fb3303784811e7311f038346fa004070f342b3b2e7f71537</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.0MiB (171.0MB) – 3,376,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2efc37a100d1aad8f0141ec4d4a68256<br>SHA1: 598b5445970b8231e59970561ecbd7dc715ec349<br>SHA256: 69fbfa6912ada4ae2e2a975a4995913e3d58cc0de3300436dd885dc9193cac58</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.4MiB (177.6MB) – 3,376,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04cae55a7f46f50554be51cc86066f69<br>SHA1: 2bb8efc164ca7a92f6d46128758d263d883738fc<br>SHA256: 0fc9e21ab65d773e70c0f77e6136c319281836ac64a17198702fcdec5223ba71</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>197.9MiB (207.5MB) – 3,376,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e7943fc93c5495013308dac2da16bcf<br>SHA1: 8a1f60f290ddcb0160114c939d8924794ad79f35<br>SHA256: e8acbb68d18a115724ca805023dd88c58c6b2cbe2a2079f1bdde0a823d8f1d0e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>157.6MiB (165.3MB) – 3,376,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b83db911d91c8df89dc217c946282a9d<br>SHA1: 220217fed497475383ebdfdeda548dc946231470<br>SHA256: 7cef9b1833ff29264a74193908ea4faee20c33ff5d28fc44a7f901faf994a7c1</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>197.3MiB (206.9MB) – 3,376,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1752d59ed0726ce64c00e931c7e9af2b<br>SHA1: 833a10b38e95ba90c45db62445ab270c5df189a0<br>SHA256: 9a1d392273d6a6709d10c2b5739274db43639c6368886ddfeeb84536f599c8d3</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>166.7MiB (174.8MB) – 3,376,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d51d86f1b6ec90756b6289bad44446be<br>SHA1: 113afb79e4bbce08508b86174d552a21d16a674b<br>SHA256: 26f5ccabbdfd5bdb56a323457f2412974c58d946590282456d7f52af3b0501dd</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>105.2MiB (110.3MB) – 1,176,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d4772f993958c1f88c7fef360934c71<br>SHA1: 86b81e26ae9a458bbf8c4590129ab9edd7e569e5<br>SHA256: cd7bd5fe051d80d611b94211a0e5584d7b82437786d4b05418e4a3b60eddd825</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>112.9MiB (118.4MB) – 1,176,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 270d49da991d800b9a127b755c0f8c25<br>SHA1: c2c04364b3b757697032529d167381adf2cef676<br>SHA256: 2e76c8decd645aab5de03cf79db61497745bfdfbda96b59083f7ccbfafb20ec8</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>107.5MiB (112.7MB) – 1,176,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 698e37b6fa0abb08adf42e2af365f904<br>SHA1: bd973ce91870eee966360d1bc1171ab7aa0833ef<br>SHA256: b8fb9e62f9d331a312c4656860f1fa6536248a56e2e4b3e6b0cd8997d012c51b</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>108.3MiB (113.6MB) – 1,176,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21d23985d067f7f3bdd786a287e10e5d<br>SHA1: 6890ff6670d0e1987168f2eb1cedceb3c741b7c8<br>SHA256: 2e6473a83704935de7e11e9dd9f9c3b7dd885533f73711382775dad9da7fe989</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>116.5MiB (122.1MB) – 1,176,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1fe8f0c0f8bed57816ffebeec94a04f<br>SHA1: d04972f5b56731041c64aafce704d537f5b59cb0<br>SHA256: b40fe1200b2eae73bda94bf0252bdcb352e3c7e172fe367cff133d2e7803ebe0</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>106.3MiB (111.4MB) – 1,176,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41f141be97d46cd0a93a29fe033e1690<br>SHA1: 6d98de599b13cbc4530bac7d7649cd425ec1bf52<br>SHA256: 630933dad4ce50380551caf93f674768297603ec250fe430463e09a1487e8192</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>116.8MiB (122.5MB) – 1,176,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 994ade6e4acc9d13891d2f5a17683a7b<br>SHA1: 30a79041504832b9bbca5416dc1351d7ff2bc253<br>SHA256: 31d7745625f48a0a7b808ec8a4cdd64b322a722d1879b9fa48cb40ec806f3af0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>109.3MiB (114.6MB) – 1,176,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfc0b31713869bbb2e0935f829d47342<br>SHA1: 7cb3eec2c4e99f73211c321bca3e15fa2f7068a0<br>SHA256: 78da8deeb53fd6f53c52d407db77adb12fbfff28a9aa9872ffe245ddb3dffd9a</pre></details></small> |


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
