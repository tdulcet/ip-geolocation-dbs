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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-08-19<br>IPv6: 2025-08-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.205MiB (6.506MB) – 310,703 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dab9843dc40bdb8197acf7c9f43185<br>SHA1: d5e3bf9fc6e8fcdb4ae1d45bc969ddbedce0a844<br>SHA256: d08f7551882db6725aaf2d311b547603151691a48137ffa797ddfa6faf297e82</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.71MiB (11.23MB) – 162,750 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d46d27b64687fab479ef9acf0892e5a4<br>SHA1: e2dcd0033b39f7b1f45302553a51d07a115d1937<br>SHA256: c9d26f1b75b4daa6745eef18c0019a2a0778e306105c21c5df6bd0c89c5a82cc</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-08-19<br>IPv6: 2025-08-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.597MiB (9.015MB) – 430,498 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a8a69149f240f203e4d180723ec9b50<br>SHA1: 4c2929663ce73385676c265b6e4118936bda91cb<br>SHA256: 69fa35719c7ec4d70d073d4b69581fbf818af290c5d4818ff0c9895a7aa4b2c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.103MiB (7.448MB) – 108,059 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68ab5aa51fb24f621497738ee2430970<br>SHA1: 267df95c5783668c8f06dc47a5cff880b22bff75<br>SHA256: 61c2d208cd9330e88e841bbff19e71992f6a11263cf6fc3b0ab9a9d13af9fd66</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-08-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.91MiB (12.49MB) – 596,237 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab565580566007c7269f8c40e3fa5b92<br>SHA1: 6a6abe49432ddd3adb6f11919383babcdbbed152<br>SHA256: 84e617bd7e9ce849eef19436f386b4ef1110b1d0150678e13953a03b4e07186d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>92.65MiB (97.15MB) – 1,407,982 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b494f5898d5147cc59c4f32ee43e94fa<br>SHA1: ee31b94c52df034b7461c17ba921739757035355<br>SHA256: 75663651e25e2ed4151dd50860677481940e35dd59ed89a78b68b429746b643a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.840MiB (7.173MB) – 342,618 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fced5df941addb9056b94a0f6f68597<br>SHA1: de47b1f9ba9f0ffbb556398c71c34fbf530591e4<br>SHA256: db6544ac94d1d22426f86a2b1b3d5b70f2d1b38ecd54fa536f817c5e106d4055</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.11MiB (16.89MB) – 244,855 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f879c057a5e3c7efdb9494722cfb973e<br>SHA1: 2a0586c6bd247669bc87d96e3dab86aee5e3a9ec<br>SHA256: 648aa19d3202320593d396fb44d416960c2d602a521000ac2510160c5d272d14</pre></details></small> |
| | | Full Location | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (216.9MB) – 3,615,295 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84dbaf75b3817fac2d522b918bcc3861<br>SHA1: 9b4ee36fa0923a2f68da4704164feac99f7551ba<br>SHA256: 43bd2f31f3e4f69856dfa6208d46d73b0063c028474adf986db93aef2740a7da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>447.1MiB (468.8MB) – 4,343,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4cfa7e8b0505f21943fa43a915ea9be<br>SHA1: dcb876a3bb589b77672f628a8ae019d6011d447b<br>SHA256: d3f883acce4ef8ed03ae21f30d09b7ca51f895f0830643368c5767a3642faf6c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.152MiB (5.402MB) – 257,838 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07e653090dfd5d1c13121b162af09fab<br>SHA1: a808596024eb433213c8e90bc6277f5bb0611ced<br>SHA256: 6da92c7dd70266c69657400e1252ef514fc1e7028aa8a0e6bb3bb9294c78588f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.38MiB (23.46MB) – 340,069 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a95a5ab506163fb86cd3197ca9610e1<br>SHA1: a7fba9b72e8a271807218c6b426e547f46226c54<br>SHA256: d86789dca5ee5d16277ae57abc33199b0ea4a3b3fbd358a820c9a2d761c4edd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,023 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec0f30e04446d83c414d7ba54cd9da6<br>SHA1: 4440d7254688eef8397b92e3f583e9b9240fe63b<br>SHA256: 3eb81d283d8a85d9a1e21e2d775d4bef02c37fd3fddf7b3981fe5aef17ec27be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>287.6MiB (301.5MB) – 2,785,870 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b12d395e9581ae946a39d0335c84cd65<br>SHA1: 66a2ff83b2e1cedccb7704236a41162bb2e963ac<br>SHA256: 8a594aae021dd354a93a799eaf42efd4fab365f15f15ca3401e4ee230579599b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-08-15<br>IPv6: 2025-08-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.40MiB (13.00MB) – 620,635 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63edf092a124c9d88fd8c44d9b362428<br>SHA1: 13a238062fa89087e1fcbd38b25364f4ef2a40b0<br>SHA256: bcd050f1e66c6d3cc662179282f47fcc313467b2330d0893c199b67230a0b0cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.75MiB (43.78MB) – 634,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7541f2104eda2eaafb99855af661cc67<br>SHA1: 48ebfab9763b81f2f73ce6717c4e4f46da078033<br>SHA256: d8d9227f3e50db8e46677d37ce8dd1701c7c934ebea683a9faa866b910d9ed6c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-08-15<br>IPv6: 2025-08-15 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,423,919 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 831a1206f5c22d03460ba6c8ec8c1065<br>SHA1: 5ae203a23deaf764d67f5b48800566476f407414<br>SHA256: 673b8c52fcce743eab252596b7665a5ec4898acd4ca70905e15f7c5e1ec7836e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.6MiB (193.5MB) – 3,423,919 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1108ce10beb722a8d333a46c6422465b<br>SHA1: e16fc3424ed925d10eafcd8adac29738b637aabf<br>SHA256: 73efffe6f83c7a76b109f7420350de4b6cfa8d9bfb68d3d8d6602f910c77757c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.8MiB (181.2MB) – 3,423,919 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08ce988a4123a36a8422dd1dc20c40ac<br>SHA1: 32c489b12fe9875e944232fb59bcf2f1c9f83f13<br>SHA256: 97d8465bd4d212d551247771259560e8abb9f139fbb3cd78ed633d6b9d1f9fbc</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.5MiB (184.1MB) – 3,423,919 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e86793783112fcccab26cffe201e158<br>SHA1: fa7b03fb1c972012cde7566d4271d90bd41b9b40<br>SHA256: 4ae72be5c399d8f2633dcb067278c5cdad3654ade19a4427e70d63dd69f3f770</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.1MiB (230.8MB) – 3,423,919 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b1a00c07ea21284d9e5cf09e3c20bb3<br>SHA1: 17b6f7c92b9b318df5936865554060f131cd4e8d<br>SHA256: 6015cf465b487f49eb96d885ef3fafc6868cc9bb49d27c0392289ee33e11fdff</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.5MiB (180.9MB) – 3,423,919 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 190a92c5bdab344439d973893dc37a53<br>SHA1: 4c845219418bd7aff013d40e60606635dd7b76c0<br>SHA256: cb8cb79fe9a4c827c0410d67919103dbaa0e8f13e7cfb97d6fe123df400cf158</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.8MiB (224.2MB) – 3,423,919 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ca5d08ce286d170eb48b43ba9d64bb5<br>SHA1: a8e1f9960118767b0dc91737122767c4f802bb5d<br>SHA256: 643fd02e6678503aa5d1320cfc236006056066629921f7a95b3618968b455808</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.7MiB (188.4MB) – 3,423,919 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e565fd9a4ce9945ec169f330eff6e5a<br>SHA1: 3042e237725bfac6bb603db5856a69d9a4ebda89<br>SHA256: f073fa5d1c6e3fd65b12569ba5a8beb46a09b0c981d8e7eb0f8d24d9c3f8bd6d</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>172.7MiB (181.1MB) – 1,834,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4b28a2a46139b8293cdafee9906f58c<br>SHA1: 5371eac76b835268ae20745cd58c5c6521a9b6ee<br>SHA256: cb9117605e5d81dee304616c3700e5579141fff38202476eaba4c124a5865dfb</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>176.5MiB (185.0MB) – 1,834,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 217a25eec3f0abbd8aa06af5c1daa8fd<br>SHA1: fbff2c0bf69a340f51a58d0ef4a36003f2eaaa78<br>SHA256: f4a072c545063556ccdd3ec9f87cf208d8c0f841fbe97cde5b14d6d3182f2fbb</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>170.9MiB (179.2MB) – 1,834,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 028c5c2a617d73888cc8186a25df50d9<br>SHA1: 647bd670fde5161dde92289e440a4920cde9056d<br>SHA256: 48e93ab4629b5001e69d45a60a0593759bebee926dbec97e2f42ed3dab6d1f42</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>171.1MiB (179.4MB) – 1,834,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58230583298bf36760e6642ecb9b4dce<br>SHA1: e814ef38577e81f57c0315a9014a174615eed1af<br>SHA256: 476b5c6e80fe87116276c9fc8f84fa705a1887f6976c8ec2d7f1187110407792</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>189.1MiB (198.3MB) – 1,834,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7eef097499c8b4a1009e488ddaa4d48<br>SHA1: 453d5360e18ed4c99f9e2fc4243fe9016bc3f2be<br>SHA256: e170c1c004a75a73fecb70143b857b71a5ffc1eefc098086d2d0489b944dcdbc</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>170.6MiB (178.9MB) – 1,834,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53012211549ab77e786e989a27d8e6e2<br>SHA1: d1338df81387c4d2c400408a616deea96fdc2d2f<br>SHA256: dcae09258694511bc2fa3dd332df09b321f11a03b3c6b24515ed784a62692399</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>190.1MiB (199.3MB) – 1,834,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 687091a156a867fae74590faa9be96a6<br>SHA1: 63a81a4414ad94307018ce43136dcda071e62b8a<br>SHA256: fca11967cb2d8a4045514bff6e0b22e5773a10035e263746a03fa295af1870a1</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>174.6MiB (183.1MB) – 1,834,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9021586a98b83ae6336e7c9a2cd45ab<br>SHA1: 8691713036098764e2103bf53d563a54474687fa<br>SHA256: 8c9b9e86242a0c42d55151d804b93cab0cba05099f55aa81e4ab6c4a0d36a591</pre></details></small> |


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
