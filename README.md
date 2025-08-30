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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-08-30<br>IPv6: 2025-08-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.226MiB (6.528MB) – 311,742 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3a61aaf0a26ffbbe961597b8315e167<br>SHA1: 74d19980e7cf8d9c9132d5a3f779e67ea20f0458<br>SHA256: 6647deb2f9542c16f6178122383cd0d979e8b1743e686f28bc445a5f0fcf54b8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.81MiB (11.34MB) – 164,353 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2cc529b91384453b6fe88768e1bf2e5e<br>SHA1: 4d699678d6d9d1ac6436662aa79799abd39ba3f3<br>SHA256: 68a6f5f0f5c4a169ce637244441e67d6b5be74ac9eb7a431dbc389e9df93ac44</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-08-30<br>IPv6: 2025-08-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.612MiB (9.031MB) – 431,254 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 365f4917a9a7af3501e550a46f8f7731<br>SHA1: a1b80be694e5d73fe9299546b19a96440f51567b<br>SHA256: 938c06431a5acd4ff6407a08cfb2246db8eccd17b8edfd18364bab65d0673540</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.176MiB (7.525MB) – 109,174 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44ec0aec18e56db38a147a8611652621<br>SHA1: 08e2d2c173766ceba71411306e6ac1203d0fba1a<br>SHA256: 134b21a767e502db4041237a9f7d194a774567d2c4b11db266e2df16d1b4f3aa</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-08-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.89MiB (12.47MB) – 595,223 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a264124d4091b7275e0adf4e20c863ca<br>SHA1: eae31902bb9de392e97f82183dcbda556ee842ab<br>SHA256: fae80f6774cfd3b56edb46dea60d00c64968cc310f653e12a52fbec194392f5d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>93.08MiB (97.60MB) – 1,414,510 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72c3d2a580cdb091beb69b0a2a0c8503<br>SHA1: de59d1c117dbeb62460d2c791c4509c8edeeaf55<br>SHA256: 8beedc52b03c69540f28d07ed37c9aec56ff84c42fb789dcb307a1074ad8073f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.840MiB (7.173MB) – 342,618 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fced5df941addb9056b94a0f6f68597<br>SHA1: de47b1f9ba9f0ffbb556398c71c34fbf530591e4<br>SHA256: db6544ac94d1d22426f86a2b1b3d5b70f2d1b38ecd54fa536f817c5e106d4055</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.11MiB (16.89MB) – 244,855 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f879c057a5e3c7efdb9494722cfb973e<br>SHA1: 2a0586c6bd247669bc87d96e3dab86aee5e3a9ec<br>SHA256: 648aa19d3202320593d396fb44d416960c2d602a521000ac2510160c5d272d14</pre></details></small> |
| | | Full Location | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (216.9MB) – 3,615,295 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84dbaf75b3817fac2d522b918bcc3861<br>SHA1: 9b4ee36fa0923a2f68da4704164feac99f7551ba<br>SHA256: 43bd2f31f3e4f69856dfa6208d46d73b0063c028474adf986db93aef2740a7da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>447.1MiB (468.8MB) – 4,343,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4cfa7e8b0505f21943fa43a915ea9be<br>SHA1: dcb876a3bb589b77672f628a8ae019d6011d447b<br>SHA256: d3f883acce4ef8ed03ae21f30d09b7ca51f895f0830643368c5767a3642faf6c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.152MiB (5.402MB) – 257,838 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07e653090dfd5d1c13121b162af09fab<br>SHA1: a808596024eb433213c8e90bc6277f5bb0611ced<br>SHA256: 6da92c7dd70266c69657400e1252ef514fc1e7028aa8a0e6bb3bb9294c78588f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.38MiB (23.46MB) – 340,069 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a95a5ab506163fb86cd3197ca9610e1<br>SHA1: a7fba9b72e8a271807218c6b426e547f46226c54<br>SHA256: d86789dca5ee5d16277ae57abc33199b0ea4a3b3fbd358a820c9a2d761c4edd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,023 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec0f30e04446d83c414d7ba54cd9da6<br>SHA1: 4440d7254688eef8397b92e3f583e9b9240fe63b<br>SHA256: 3eb81d283d8a85d9a1e21e2d775d4bef02c37fd3fddf7b3981fe5aef17ec27be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>287.6MiB (301.5MB) – 2,785,870 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b12d395e9581ae946a39d0335c84cd65<br>SHA1: 66a2ff83b2e1cedccb7704236a41162bb2e963ac<br>SHA256: 8a594aae021dd354a93a799eaf42efd4fab365f15f15ca3401e4ee230579599b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-08-29<br>IPv6: 2025-08-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.49MiB (13.10MB) – 625,117 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27bad77d75bdf71413a71d84eae85af5<br>SHA1: 1320464aa48175e68a2316bfb2750bbbf3e1a811<br>SHA256: b094d315415121fd67af6fb05495206d1009f903c9c36193b7e4e50cf7cfe077</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.13MiB (44.17MB) – 640,208 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98fa867c67532626316c06abb7074d2a<br>SHA1: ae0f65a8ac1f993e005bd77f920ab950c7cf7267<br>SHA256: 90a124e4630c3f6ea39ca47d71a4c61c7e8552a2640c60817e177f7e7027e541</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-08-29<br>IPv6: 2025-08-29 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.6MiB (182.0MB) – 3,421,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6aa6f1b9cb640c9898d7dc6dd9802e48<br>SHA1: 924b74f67201bb01a4cbe5011a5abe5cefb9ebe3<br>SHA256: 7cfb46f3fdbf1f2e855ddf9d951bc60faa8192f368dd86c573cb839131515f4b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.3MiB (193.3MB) – 3,421,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16045e8fe056d506c464149875177671<br>SHA1: ebdab64898fc422e33839e2ad89b8dda86ff079e<br>SHA256: b5c1123355d3f60d4cd36ce21d62d04d19f6999232d8da4d062a408dc3d6379a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.6MiB (181.0MB) – 3,421,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5011ae07ab5941c288c35323cbe851f<br>SHA1: b133491b188738b8edc33b4cfc0dd4448967104d<br>SHA256: 1af070c05f011ab43c9ce20eba9c8b3fc7b14799bfd35279cb2af22f6b6bb4ed</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.3MiB (183.8MB) – 3,421,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52aadeb4f68ddd9d5f45fdfc26c4abc9<br>SHA1: 49e67f092f0fbe64b921dc4d40d3ecc06622ff8f<br>SHA256: 82328dc694e79a6bb0ddfc59ae5f3b44ad66ba1a1d0f90d11bdadd0e6d81810f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.7MiB (230.4MB) – 3,421,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d941e1eaf170bed2c01226584e71a075<br>SHA1: 839517f926dedc8cf92792778fecd85737daa401<br>SHA256: 57183c067047b85fbb66f5e81e01a806b4e4685563090ad626329d9745a8c7d0</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.2MiB (180.6MB) – 3,421,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d423959bf66db81f8f8bb49e9789488c<br>SHA1: b259080ab1738c416672ec2a70453432532df001<br>SHA256: 560ca72b5ab9747581c3feb3b4761afca7b522a5a10a6bb1699fb4dbaf1dde42</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.5MiB (223.8MB) – 3,421,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c02d05746f231f07c2e1390c1e88fd72<br>SHA1: 91743751eb934ed836f7f52f46a9fe3e806dd356<br>SHA256: 0f9094c0c7616a6681ec5703ec8eda19d5c0a31973c0245585461eca064fdcee</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.4MiB (188.2MB) – 3,421,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e149418591cd0e240cdeebcc66b2cb1<br>SHA1: 5f955493046e8eb327d07eeb3cc1f1585aa7219f<br>SHA256: 6e9852bb91a93cdb0e92e95348edb1044bd0a5f950eb9777802bb91f33de4884</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>174.0MiB (182.5MB) – 1,845,478 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fe6f6dd81c80e0a36eb7611d424f333<br>SHA1: 709277f5bb0aef4c09bc37d7d839621d99756ca2<br>SHA256: 17fb0ad1d317fe2d5b8a549a141db40e6ec262a394d357b85e8a6a45be3e1bfe</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>177.8MiB (186.4MB) – 1,845,478 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7dfb2c33b21aa6e08e17ba40472cf5db<br>SHA1: 9b3a276392d4af370af55189504dd82daa9174b9<br>SHA256: 6e954cfba185ad9cb4727a73196d188c563a387820fc72a77817e3e748ad179e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>172.2MiB (180.5MB) – 1,845,478 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0bca49dea3204be2f68508b68e45a0b<br>SHA1: 41f80c59b6a5ddb6b0a571dafcd1670f614be0f9<br>SHA256: 7ce36a09353e473fc583a7b61091f651e14f6b0cfa6ff6340984e4fdcfd7ca2e</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>172.3MiB (180.7MB) – 1,845,478 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e78947c34a989d84fdd07b0ffd44d4c<br>SHA1: cb62a2cc684da96bf42674052cc814aacc52b959<br>SHA256: 79d3eeed7d7a0a33e4097c712bd7c889525282e8d82569388da31b281d8c4f91</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>190.6MiB (199.8MB) – 1,845,478 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f8439e4f3269b7321a797b90a04eddb<br>SHA1: fafa949733d7aad9259cdb651ad4c6f9062f3c7f<br>SHA256: 0eb87d79cde338cdda21c0d60edc0994273e43b4529ccc3b2fbc771b1092078d</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>172.1MiB (180.4MB) – 1,845,478 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c0764bb348210faa2566104d107d8c5<br>SHA1: 69a536cc12b03ea058340edf1637293924525a92<br>SHA256: 82b2727ded40e7eb29d16e3a173ca7c3f005cdeaf61f25275d1c0ba114bf15ab</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>191.5MiB (200.8MB) – 1,845,478 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64216407e99e448dab3c34a9515f4f20<br>SHA1: edbfbbdabe6dc4dee83d9058fe9be0ed1e57fe7a<br>SHA256: ac73e80a25aa1a77f39daa316b6258d8d17b5c95b9f869e94f3e79551294ee06</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>176.0MiB (184.5MB) – 1,845,478 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3bbcbf2e5878dd57dc9e6044a7f7ec1c<br>SHA1: 2e78307cc4a0b61f5bc2a0ddd5259d9f247c07cc<br>SHA256: a79255c5a554ed82c2723aa94113e3d5681ca83a3c5c28b35d35d889bc76ce1c</pre></details></small> |


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
