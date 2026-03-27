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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-03-27<br>IPv6: 2026-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.501MiB (6.817MB) – 325,622 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4a1cb893664a0653fdb14221f8e77f4<br>SHA1: 9b01b08c4045977a85d20fb8dd70cc84b35ad221<br>SHA256: 0f7143f9d8d78b6b479e80ce2448d0a9a7e199d1e6b8b0a389e5fedb584eb710</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.49MiB (16.25MB) – 235,466 rows – 258 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 466b11df1dbd449e6400e64008397242<br>SHA1: cd5648f4162c26883d21584b7584f2b41f4188d4<br>SHA256: 4a93b6f3ffaf00e4dcb1d8f90c1a019d2bf43d6fe6a649ba6f5bc059734e4a3e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-03-27<br>IPv6: 2026-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.807MiB (9.235MB) – 441,003 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4e81fefd729a8c9a38bf60b22003b39<br>SHA1: d2b523ecf1bbcc99b3659b4bb6edeaefbd0e73d6<br>SHA256: 01f223b9eb7c2cc9ea1456a4341ded5f7dea3967afc6c000aea668a720b8de2f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.688MiB (8.062MB) – 116,953 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d27d378eac57e73ac3d9b9c93016495d<br>SHA1: 618e02688027a6df792d5888dc26bbaa9a7d29af<br>SHA256: e4c192b904ccce291e39ed1e0895e0f949b84a4297d0b31e334853c3e8d84620</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.39MiB (12.99MB) – 620,157 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94aea2d1d7336fa87ffe05e244358deb<br>SHA1: f07dd9f1a508dd0eca0591937b44cd80ac88571a<br>SHA256: d6c9852e31b870a2352ab100be94594bfee03f64baf5916b4acfe61927297e99</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>107.8MiB (113.0MB) – 1,637,865 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0a67d8e543811945bd8cf9c24611ace<br>SHA1: 55b0ff79cf869b03447920823bc5c0b7f9366eb0<br>SHA256: 70e20a37886b7c193f3403f81ad03a87b4fa98b97219159bff4f7d7b41bf3f8a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.906MiB (7.241MB) – 345,970 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be67480ebe04792eaa1e993732e26bbc<br>SHA1: b9c086649cbd7a697ce8b1a6f1200cf343683838<br>SHA256: 97e3ba0306a918694a1abd35fb0fbe18e3275c023a00d3f378bb52d0381e6ca4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.48MiB (17.29MB) – 250,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614f4ebb16bfdb3cd44828a77fb774d9<br>SHA1: be56f3e3114c6c18c1b7e097bb867772c72bf90a<br>SHA256: babfcc027ee9656b7ebe280a391c73174b4990721bda2e7c584c23450f4c5452</pre></details></small> |
| | | Full Location | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.5MiB (222.8MB) – 3,723,444 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d34e3013a398743fdc3bdbd816dba48<br>SHA1: 4f4868afd37a86dcd98f0ff21e863db08c4c69b8<br>SHA256: d805d064a2ceaeb75e8ee847780d1dcf8f54852ffa98bc007b0894fd1c1d24d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>446.9MiB (468.6MB) – 4,345,257 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b0322dcdc11f95be5a5b01f4221151<br>SHA1: 5bcecfc1d1a51db165a9a209bc8f4b9a5e7e1bda<br>SHA256: 9a67a943e4fadd058173607911c45bce627c5fbebc2abef2f229894d2e8fc57d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.419MiB (5.682MB) – 271,203 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c176ca445d23383a4c5e1e2ebd9e541<br>SHA1: d9049c5c5fbb465dca6e199246fc0f4419435e17<br>SHA256: c56f984490695ab20d84eadbfd37f601c78de75f4958c1d1ee5927482ffa66cd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.22MiB (23.30MB) – 337,655 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c07180576fcf598a4054e35c7eca4e61<br>SHA1: fa9ee16f19dba3851f20083872d13d4acbc065ca<br>SHA256: 8e65ba7778f59ef63c1a8df94112a447927b3896dbadb00d080914b5ea37167f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.6MiB (174.7MB) – 2,881,763 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1614bd25a28d2b44922c3116279f804<br>SHA1: d2cd1e423c13e941548d01a453978c165e423b8b<br>SHA256: 8486e52f22f5c609925e25d4d0d4e74ae714d31b8ee7067d87a99f951d8352c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>298.4MiB (312.9MB) – 2,892,579 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85c1923ae57109129fbe714df2b92c0c<br>SHA1: 846479cc0828f79ca640a39a279ddc2fc7b8aa2b<br>SHA256: 1759b2d35ec83b135771dbe6a08ae383efaa2981f42a80b1dcd3ee4ffa98633a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-03-24<br>IPv6: 2026-03-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.93MiB (12.51MB) – 597,188 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1c48bfebde95e6e59bacda1f1678d06<br>SHA1: cbc7b4048f3c0a7c3f93430c300895bdd17bf5ab<br>SHA256: 892ea135b8ad18955bcb78bef0cc450bbbdd128cb3369fafe0f84c9397e74901</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.66MiB (43.69MB) – 633,155 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24d01f1513d4b8c8dc0ab7e158784c6c<br>SHA1: 1f68baf1739d1fc09dd73010341b271b6c334405<br>SHA256: aed122324d49c30a48868f110b764ff5d94387bf0451c56500f548f9c6df613a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-03-24<br>IPv6: 2026-03-24 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.9MiB (187.5MB) – 3,534,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c41acc705d1f67005e045ab1dd089a38<br>SHA1: 56080c098d640324775432ebf89c38a48009f1bd<br>SHA256: 235be6d9aae05ab8ed8765e77079592915a5d421d89d9e6de8a38711d8ea1a5c</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.8MiB (199.0MB) – 3,534,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79b72c4079ff38035123c5516256451a<br>SHA1: 39854bc7f1a2bbed8bb7da1cd8499ccb647a98c0<br>SHA256: 0bbd3a0d9d2d198f1a316c6dee24ce9ca96fb7de5dd7590d9ca4427850e30ea7</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.0MiB (186.6MB) – 3,534,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90f761bf137fe1755b5930447573b144<br>SHA1: 2f63a63ad247d6bb81c6747d6479d273b1f1b538<br>SHA256: 9ec2cccca17200b6a91a9c10a70a29d2bee4dfae63b84fc63eb704316a0bdf96</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.8MiB (189.6MB) – 3,534,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0d963cb45085764c0b00b2475c5be83<br>SHA1: ceba611779736d6307771a6a5010982df312e32b<br>SHA256: c7f0ff7bfd25d8c2959aa992f0ebeb644551eded5f1004db40c2e3f080d4cb39</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.4MiB (236.4MB) – 3,534,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42a9f072648fa551e417d232ae109d46<br>SHA1: 86f2341f7d12f91c91f61fad0d1f711ee0f8f77f<br>SHA256: 1419d8dfcc903ad3d6ace353cf411e74918b4319c4abe478ddc64f09c0fdf8f3</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.5MiB (186.1MB) – 3,534,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73a072107066b2a6368634bf9845d8e2<br>SHA1: 7070d34a9cb452fd117f6c1100dde3182bb17b8b<br>SHA256: 8ae18483053c253f2fd99348ecf8fc3ceecc524a38d33ad49bf5be6b22d85542</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.5MiB (230.2MB) – 3,534,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7291379d0f2c9a9e1e1306aa8d0841bf<br>SHA1: 131189ffa755856e5df6bad0e40ba45c8fcf069e<br>SHA256: cb7d3ebdf31ae73e4f7bea0ee59b7ca561edadb8e97313c7a5c360c57777d76f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.8MiB (193.8MB) – 3,534,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76e4c6cf03acdc9cf43c26ccd5213b5a<br>SHA1: a81ba711c6804833cd5dccf7a1fef5c5b8b9db0b<br>SHA256: 21114718f818e81cb28f71bf7e83de8a7275622e014a890df4a16da68f8469fa</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.5MiB (196.6MB) – 1,976,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a6e60361ac70cf87f08a412241816df<br>SHA1: 8c11068bb583f1f236da49791921b702996f2ad2<br>SHA256: bdceb31a8209b5a7ef595f929b081cef6d7442c951ac6fa482a4a9ea9441f787</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.8MiB (201.1MB) – 1,976,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b0265054cc4f712da9b92034d5114f0<br>SHA1: 6faca86112d3e01a08c7fea25675f1d852d7b6fd<br>SHA256: 7cbb7c9761a1c36be919e972c08646b6af576f32b98bdd7f3c80a23fbaea9247</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>185.2MiB (194.2MB) – 1,976,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3345ec947d3c15aaded98a69c9f672a9<br>SHA1: 9ec601409e081ae38b1a5c812b08446e510aee11<br>SHA256: 2276a314f66a5c290ac2b1b34ed955d255abd4334e0ed86667e7126e4c8fce3c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.9MiB (195.0MB) – 1,976,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a046a118b8d1e6ffd854bee846e82a5<br>SHA1: 300b2f1e6b0a6eb23d05c80a33eb8475ac1173bf<br>SHA256: 1668376b725271681a87cb6e5ca8b7fe05d4486a15a37c9bf39a059f54769533</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>206.0MiB (216.0MB) – 1,976,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbb8faf1c4ffa010f85683f5e6813734<br>SHA1: d841a2619649c55fdef3db7b88521ab9f6fcf062<br>SHA256: 321876c29b9eafc47af25d61b041954dd2b8cf841f7730197525dd0f6a0272a4</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>185.0MiB (194.0MB) – 1,976,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0adc5519fe937a00610902581ccdda61<br>SHA1: 1a3659e3a5a4847ed842f89fd209f9b9c9065e48<br>SHA256: aa14a895a88ff3800afd35432b742e7ddd05b97a83a87d3c87ad301072e0f0ce</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.9MiB (215.9MB) – 1,976,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6e5a3ce4c522e852b148f1ff927c1bf<br>SHA1: 548b79619baa6eda3ad8b8c5b6e6f563ac9f230e<br>SHA256: f0894b5bd02b9ad47ad746c2c73a1b497350a9c5c9b2e411a9d97fcef0c5b05e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.6MiB (197.7MB) – 1,976,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79dbd957817330c7779ab57aea584bbd<br>SHA1: 9795326cd4114ba763b7622344960c59b97b8318<br>SHA256: a62b738fbc5e6c3acfcd2d2153a89282d4262a1ae2aa6f3d0d2c19a6a10035e4</pre></details></small> |


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
