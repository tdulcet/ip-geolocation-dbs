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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-08-25<br>IPv6: 2025-08-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.193MiB (6.494MB) – 310,103 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0fc4bfa66befc28527dbe3c1fcdd85f<br>SHA1: 5ea1747444a2845a16ab32a1de005b6e4d623640<br>SHA256: 2fb210b6010baa9944336cfea935822c311d00dd9d869317c95ceb6307a56869</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.620MiB (6.941MB) – 100,601 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97e78be66429117a026b83937fbb1ee8<br>SHA1: f14f10646f000b38e27a0a8f5f0c8515d5dc94cf<br>SHA256: ea72df5d469f0a7cc2eddc8dc88a145410dfa72db62fc3b2d4aa16922db8754f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-08-25<br>IPv6: 2025-08-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.605MiB (9.023MB) – 430,918 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a261e83a29ef2cdc8dd99d0e7a6b849d<br>SHA1: 3d09accd06ecd626b1eeaecde98cdc891c66ce0f<br>SHA256: 31ccfa51c5f26b7c5c77eda32c9b3978d97991bc483d1d7685d987a0e22f2e57</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.140MiB (7.487MB) – 108,619 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab03ddd28388c4f19c210a33858bf907<br>SHA1: 609683812059d507439d4a5b4019aa3088a50833<br>SHA256: aadbc4e0173d38b93a28009dee3de067254c23ff98accb28cbb63b43822d883c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-08-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.88MiB (12.46MB) – 595,013 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 793b560fe1e95564661183a69aec1260<br>SHA1: 0056f861b20510932e7f827e9550e6e4f187d410<br>SHA256: 680da1353fc06cb7dce20d94e7b88ece47fffa1c93a1c7beaf86043b85c5dba7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>65.71MiB (68.91MB) – 998,653 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d025ce613332474b69a08cc18be23b2c<br>SHA1: c533d9fdd754fa16c4041a385fb293d6e07d1e23<br>SHA256: 1c674a6f1597382439e12af71f7abaa31e88add47570132789188702f50e083b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.840MiB (7.173MB) – 342,618 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fced5df941addb9056b94a0f6f68597<br>SHA1: de47b1f9ba9f0ffbb556398c71c34fbf530591e4<br>SHA256: db6544ac94d1d22426f86a2b1b3d5b70f2d1b38ecd54fa536f817c5e106d4055</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.11MiB (16.89MB) – 244,855 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f879c057a5e3c7efdb9494722cfb973e<br>SHA1: 2a0586c6bd247669bc87d96e3dab86aee5e3a9ec<br>SHA256: 648aa19d3202320593d396fb44d416960c2d602a521000ac2510160c5d272d14</pre></details></small> |
| | | Full Location | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (216.9MB) – 3,615,295 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84dbaf75b3817fac2d522b918bcc3861<br>SHA1: 9b4ee36fa0923a2f68da4704164feac99f7551ba<br>SHA256: 43bd2f31f3e4f69856dfa6208d46d73b0063c028474adf986db93aef2740a7da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>447.1MiB (468.8MB) – 4,343,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4cfa7e8b0505f21943fa43a915ea9be<br>SHA1: dcb876a3bb589b77672f628a8ae019d6011d447b<br>SHA256: d3f883acce4ef8ed03ae21f30d09b7ca51f895f0830643368c5767a3642faf6c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.152MiB (5.402MB) – 257,838 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07e653090dfd5d1c13121b162af09fab<br>SHA1: a808596024eb433213c8e90bc6277f5bb0611ced<br>SHA256: 6da92c7dd70266c69657400e1252ef514fc1e7028aa8a0e6bb3bb9294c78588f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.38MiB (23.46MB) – 340,069 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a95a5ab506163fb86cd3197ca9610e1<br>SHA1: a7fba9b72e8a271807218c6b426e547f46226c54<br>SHA256: d86789dca5ee5d16277ae57abc33199b0ea4a3b3fbd358a820c9a2d761c4edd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,023 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec0f30e04446d83c414d7ba54cd9da6<br>SHA1: 4440d7254688eef8397b92e3f583e9b9240fe63b<br>SHA256: 3eb81d283d8a85d9a1e21e2d775d4bef02c37fd3fddf7b3981fe5aef17ec27be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>287.6MiB (301.5MB) – 2,785,870 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b12d395e9581ae946a39d0335c84cd65<br>SHA1: 66a2ff83b2e1cedccb7704236a41162bb2e963ac<br>SHA256: 8a594aae021dd354a93a799eaf42efd4fab365f15f15ca3401e4ee230579599b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-08-22<br>IPv6: 2025-08-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.42MiB (13.03MB) – 621,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c968d7b8fd7c7e05e79684396bab35c9<br>SHA1: 1c8e7f4dd55efa31119fd32be66ef2c33c2ef67d<br>SHA256: a06002c2a9cfa14f76d74d07b461cc5018d4ddb78c32071978ec9b4f1885e846</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.91MiB (43.95MB) – 636,953 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 933bae97eeaad26cc686bd81b616d4c9<br>SHA1: 2c33cac684cc1f98ea5660699f34cd499719552e<br>SHA256: 31634c8b44bfb2fe71275ed9d9114b5857fa98230cb144f98012b9adada6dc1e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-08-22<br>IPv6: 2025-08-22 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.5MiB (181.9MB) – 3,420,330 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62078d31ec9a2f9171ab5327d23feaa2<br>SHA1: 58b408120db40443d813d7d77ea04e092270ba50<br>SHA256: 03d9f16c91f0af14c9b86fe0bc004f4922290646f117d74798b16c498635b924</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.2MiB (193.2MB) – 3,420,330 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc053b9cde135a32af9be792d5f4458d<br>SHA1: 4908ab2220f9e71422c5bddb6827d70b20dd1173<br>SHA256: 8162ffb5137b5b8caa9a3b9bab69305cb69ba7ee495d9f2687b1a724c393c50a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.6MiB (180.9MB) – 3,420,330 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 136403592f226147c028fdd09ddaaee5<br>SHA1: b835a4d29acc849f6a45b356853f5dfd57fb6816<br>SHA256: 2d886fdf8bf0f89cae84f4948388b809174e64790be5c6ca4cc27e6e9cb9d593</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.2MiB (183.7MB) – 3,420,330 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d983d026b543791ff7315a5449b5a00<br>SHA1: fbe88f2e1b3733b1c71c86382dd8a44ca4ee9cdd<br>SHA256: 7e182a55a7ef4f0dbef32c9eab277687075cf2760cc34144d0b42248b34c7b64</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.7MiB (230.3MB) – 3,420,330 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02fd80eeaaf46f2e731cb2e87e4fa30f<br>SHA1: d8f6b7f02bdcd4d38daf58a325f744574d2fc556<br>SHA256: 77f0d21e95b014dbc46169bd6b670bfb7c3668f9be2e8f9a66cd267bab0fff71</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.2MiB (180.5MB) – 3,420,330 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6dcd8303d4617a30d5e7c67a3a7addd<br>SHA1: a8b7ae39ad8cf8077f78b30bc28f8367692e071a<br>SHA256: 664c6b68e4a91198635492a6de6aefb2cea159afe49298b6563ef23ec951a5d9</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.4MiB (223.8MB) – 3,420,330 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b72ef263cc96b9c30486fcfa235fec0<br>SHA1: 363bf83b51b77d9b94550218a26001fb3c77f01a<br>SHA256: eaf145118dc446bf23b34d9e8e2438d7059301ca304d419bd22e96c1e35f9105</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.4MiB (188.1MB) – 3,420,330 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f984c1e43ab4bd022d8616572358703<br>SHA1: 75aa8edec2d5bd8d868381f69d426ed6caa22667<br>SHA256: 7a46371599dbf05151c1618c0bb4b32f1556230cf08b74b10defccc547413060</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>173.6MiB (182.1MB) – 1,840,078 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64c06777baed750658d0834910d014b8<br>SHA1: 4f6bc3ff43db3675f42b956a44c9f7c49ce7d82f<br>SHA256: 88ad8c4f44249730add20a60e28b48f5c7b2e14378869abfde1c5c2c67637539</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>177.3MiB (186.0MB) – 1,840,078 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70670813bb17b3966e35dec4f97175c5<br>SHA1: 2254d4b210caa1ba6c666858cd4faa409fe060cf<br>SHA256: 86a15d10017ace2dd5514a742572239f8b8857f41327b7efc6e7a106a61447b4</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>171.8MiB (180.1MB) – 1,840,078 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec29faf0cfe6cc455d0667d9094abe5d<br>SHA1: 92f0759ba2f784042af01f90805607d3cc64a35f<br>SHA256: 8cac07644070ac119bc341b461fb032457f226c598975ed5d25965872129d476</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>171.9MiB (180.2MB) – 1,840,078 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bc3f8ed560dea9a4389cab905c322ac<br>SHA1: 391596b170c3954ba3cd504e94f1a7e3dce8a2e3<br>SHA256: 24318e9e1fc6c1b13a36de8276c148e4497b03db678ae1ccababcfa19d81775b</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>190.2MiB (199.4MB) – 1,840,078 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf1111918fd32ebf24451ae999998899<br>SHA1: 10b726e470712dda8cfade8242344312fc804b33<br>SHA256: 354cb37a72464b8c6352789bf2bd79278d4cbf86aef417ddcdc8ca62e9a28f78</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>171.6MiB (180.0MB) – 1,840,078 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e687617fcb1fec19c8ad2edcb8b0b69<br>SHA1: 54d3fadddba32d99e5de8ec9e926b9ae8fbfb836<br>SHA256: 4c5708dbc004bca4a5a0e64053fb9cf2602a1fc5a82acdae0ff67162dbcf887f</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>191.1MiB (200.4MB) – 1,840,078 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a45d55634d14d67c65106fa76ed5bdb7<br>SHA1: 698c493102f63a4c8f0ec04e23570eacba28a887<br>SHA256: b69f42a36c4e0422ecd00a86923728242023c4de3d88b1db31b03de367aab484</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>175.6MiB (184.1MB) – 1,840,078 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da6e7e6fbe4671c2792e4b243bf2b492<br>SHA1: 1dfc6f4e8b5a5abb70bd51b17e5c8160f1f641db<br>SHA256: d3c7d45dcf273f174654d25433728d37f9d6763340fc481ec0a6efe96cc90a42</pre></details></small> |


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
