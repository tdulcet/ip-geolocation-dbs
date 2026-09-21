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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-09-20<br>IPv6: 2026-09-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.550 MiB (5.819 MB) – 277,755 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d01a51d177aeda38277669a6a460b18<br>SHA1: 0e859728f1fcc3edb25b03e198422beb66d45287<br>SHA256: 4dfd481f84c98cd78bddf626884d325f80741d1d3e44b7c04d1b728538ae615d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.74 MiB (17.55 MB) – 254,320 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e852e73a59e181a6848745deba41568<br>SHA1: 97dd9c7110fbbae428a84662890be423e1d39b6e<br>SHA256: 167082b675f9ee3d9c720afb3e0c19f425a2c0609f05a09390c7f29f2d696340</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-09-21<br>IPv6: 2026-09-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.143 MiB (9.588 MB) – 457,839 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ef4d225172f28c4696cf7d11b05d1f8<br>SHA1: c4646c28a1c85c6b65e7fa04f24368786490fddf<br>SHA256: 5f860a6e8e2e1d1ce7ed007666fc16607b2759ed82a399e0ca0a1e67b4563c0f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.048 MiB (8.439 MB) – 122,420 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3b41beaf43b4daac88532e67e4473ed<br>SHA1: f3c0b1f60525f031524cea1b24313570ebecf49b<br>SHA256: 39eaa618cada30a3986db5a40312a66202ba293c6601d1c721903761a1d553d1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-09-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.46 MiB (13.07 MB) – 624,094 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47c6f33e6eba12151f13d44a4a8215cf<br>SHA1: bb952cd575294f030f57023029a2d2d592f5a711<br>SHA256: 54ae31c2299780d845cf27114333b86eddfd0c17fd7d2a4b2465375cfdf5d4d8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>55.76 MiB (58.47 MB) – 847,436 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7b697961fcd4b9e33f4b33b4d21f49a<br>SHA1: b55453df1cbda18f7d372e63281106dc74b31629<br>SHA256: f4c4636bb7f2df29a6d833a1e4fd4268b45ad94e3be12527a7ff2f67c487fe6a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.133 MiB (7.479 MB) – 357,311 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c47fd01af8b18cc1d5cf2004691771<br>SHA1: 6b08ac2e1f8b48e55e72f8ba6ea0079e50a1af12<br>SHA256: 63aa3454aeef9769e4f0d68b4b93b23a7d195199a50487f4db5d258d90f8b08e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.68 MiB (24.83 MB) – 359,841 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ed7b2550b03a35e3bcceffa4ff9516e<br>SHA1: 2f8880592eb4dfde0c92576fbc78417988b521fc<br>SHA256: ecd35f269cfec0024d6ea639910b54c657f3f1dc08ab339c3d0b0384ed3cb607</pre></details></small> |
| | | Full Location | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>204.7 MiB (214.7 MB) – 3,588,539 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343b463b14a760e04ccbd188e88baa4d<br>SHA1: b7e446f674922e349cb17f01c859bc3bd62fd5e3<br>SHA256: ba1847bf8c90ff7f1ab0a19c20aae3512e9bf7a3f144673fad5d87dafbf7780a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.2 MiB (449.0 MB) – 4,160,441 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2542313832b0583d31e84cd0f9afbfe8<br>SHA1: f2d167034376bc0d28d3f5a38fe3c15945c4ba61<br>SHA256: 9c2aa7d6132f5be8f547273ac5e8f21c074f3d7a26b3f7795c642f4a3b6a9693</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-09-14<br>IPv6: 2026-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.761 MiB (6.040 MB) – 288,365 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6747ad281e6d203df87a7283739262e3<br>SHA1: 90c532db8f1cce14645149b8f5cc394de42a2c96<br>SHA256: 6a9d95b18e972f327a0f7a32b7b4d33f0e33eef14e127439bb12b976b30249fa</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.80 MiB (23.91 MB) – 346,477 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1bfa9fbed82c09b5db9b5982e8b6d9a<br>SHA1: 8ce51aafdc54a7b6766d611cfafb10502b38fca4<br>SHA256: 9bc47e288cb9732ba16dbdd489323efcc7ac2a64bf0d684bc731464539bd785e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-09-14<br>IPv6: 2026-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0 MiB (179.3 MB) – 2,957,517 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dab7122ae812dd44dc6c14b6519b1f5f<br>SHA1: 10115286d4268e45b97d687718e7f7a5030498c3<br>SHA256: 9fcf166e7c6b2ce4064e5878e3c5094a10efd8718e9f3a05b0ce3206d68189e2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>304.4 MiB (319.2 MB) – 2,948,617 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 802cd20efc7238eaddac6e73d1914581<br>SHA1: a16e3bf85f8d17952c77749f9a5547179a3e0bef<br>SHA256: 3bb02a5d77da37fb74e8ab2d2e8e28be7e39f3e0486c0af2178bdaa6b3ff86a6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-09-18<br>IPv6: 2026-09-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.20 MiB (11.75 MB) – 561,050 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa3b8538215c65bd9cb308249f80c3fc<br>SHA1: 8445a8f964cd3b190e84458869c7b804122939e9<br>SHA256: 81f0aef5f78b603c9ff7460d95299277e1ee9a7903102056f290670db7a724c7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>33.76 MiB (35.40 MB) – 513,056 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdae93c419e111314d80d9730571eb76<br>SHA1: 24dd233fe660d6a5573baca0f584e1094420bb82<br>SHA256: fc799c95e430650f1bffcb278c45f9187555ee40e96a40e72c6d45a3daffc626</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-09-18<br>IPv6: 2026-09-18 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>190.8 MiB (200.1 MB) – 3,717,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c996f349c6c5bcb210825be2062cd28<br>SHA1: a79fce5ab917b73e442b3ea1cf9d5698dc372e9f<br>SHA256: 06d6d13fae274e91b15d916a9267953c6e3a746e714b526d5a8a287fa5cb2382</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>199.8 MiB (209.5 MB) – 3,717,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68104bdc14ea4dd89e3282c382361e54<br>SHA1: 69faebfa5755caa32ce63febd7752c3b3f7e7cec<br>SHA256: d773af66c815e5e3ce0914f55573d35cc47f90f3f4550ebf355747ecf77889e0</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>189.8 MiB (199.0 MB) – 3,717,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f59b463c18e2651cc210bece8baabdbe<br>SHA1: 477b0671f34cdeacd60e40ec89c809689b95dbf0<br>SHA256: 5a1ad4c8b1b2d0adf776d297a0ac9e2624b041f3bb27cf5899d7a168c5846fd4</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>191.5 MiB (200.8 MB) – 3,717,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 255df96771c13c257b44900e32ae6d4f<br>SHA1: 4c718e8400fbbb4931f5ed8ce485ee3ad0a75abe<br>SHA256: 744bc863630678cddbcc059e8151f0ea4ac4fede2a0c1d4bb1594f0ca4202fbd</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>241.4 MiB (253.1 MB) – 3,717,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66e560a977c4200ef425742d57a4db35<br>SHA1: ddb179ae3b5a3148cda0db295d55dd62dbd26f0d<br>SHA256: 4a41536f8ad721671b2a189e08e90a56b7253e84ef7e8af9fa39b104fea8cc80</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>189.3 MiB (198.5 MB) – 3,717,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc0ca35e66ce1166e5f457cec67d05c7<br>SHA1: 4ee783edac85f829e2c4ac43e874653b23bdac7d<br>SHA256: 95444e434a444b4e979b8853fa578a90044bdaae7613bfae16b8c2a196889f6c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.0 MiB (245.3 MB) – 3,717,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e60005dc5805dd37cf79403024e38c6b<br>SHA1: fbefb10cd00ecc6c1643ee72bca5ecb2d2a27608<br>SHA256: 13473c534aa6078761793b9b9f39b03c3535c34a49ae5ef9bb8848a9be9d71b7</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>195.0 MiB (204.4 MB) – 3,717,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c2d7b3bd3d6de0b08243bb4ba4f3d00<br>SHA1: 4d8421cdaa019addbde07417d6a43809be347fc0<br>SHA256: 4527677e814a0dc13b2ec383bfed4ee2d1c3b266c1abf0ba3e0362a49d0511bf</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>201.1 MiB (210.9 MB) – 2,104,838 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07df306dd903705390e8f5195a2dfdff<br>SHA1: 9cbe7822045a3d097db066bca4a3eb7d458a1b0d<br>SHA256: 5739fb606caf59edd99021da1c5b7d403ac528549fc33467d3ca321895667675</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>204.4 MiB (214.4 MB) – 2,104,838 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccd86ded317e8c62140288987adf8fc1<br>SHA1: c61fefb03c33bbbda1e2ca9c2448101bfc349713<br>SHA256: 264f64fa48cdc37354544fa1d46e13e1681c8473e0675f5da5907812decb09c7</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>198.4 MiB (208.1 MB) – 2,104,838 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43833a3c3cc074725ce62793d08d36b8<br>SHA1: 15bbfb63495b2842db794b55ae4bc3fe0f8a0291<br>SHA256: f4d9ea75974a3eb2d54f6c62cf9cf4c681fbbb6c425d15bf559a1c0a28088d09</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>199.0 MiB (208.7 MB) – 2,104,838 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08557c9cf5d77f0103162c383218cec6<br>SHA1: 8c372ee0018246e832fd950188981572134be664<br>SHA256: 471290e9750050ea15e3cfb85452182c464521bce890c350c22890633ced0b5f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>221.8 MiB (232.6 MB) – 2,104,838 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7bb836a9e5a6fecac0e2056f97b850e<br>SHA1: 7d797127d804280205db7d8aaa8aebe974602439<br>SHA256: 30bac516ea121bb1f94e1fc22778d036184a4b79d8cadf5da424e239991d2d6a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>198.5 MiB (208.1 MB) – 2,104,838 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e256c4060e07233a434399597392dde<br>SHA1: b8a71c840747b4acfc8ab5ba8a7af1bb5aeb3d8d<br>SHA256: a4960d07ed70e26ce45a4ae1da759f0f79ba3dc4b558973a8534dc5c8884746c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.1 MiB (231.9 MB) – 2,104,838 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62c06e803f7d5ea36386495d9acfd9ca<br>SHA1: 5fc530ab0cd6c0e4ebfb521b4c8919e22724e377<br>SHA256: c31f77737116fda28f6c39a6e118f377611700a5ec2bebb0ce31778bd81cb3c9</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>201.4 MiB (211.2 MB) – 2,104,838 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9e443e5acfeb912a3db2f65e00473b0<br>SHA1: 9112f27671d09b6266527d81ea8288abd94235ca<br>SHA256: 2baa4f075276c620bb8b68159ba55a2b657c59c0dfd5f56a6fe5f56ccd3658bc</pre></details></small> |


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
