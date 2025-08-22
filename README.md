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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-08-22<br>IPv6: 2025-08-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.204MiB (6.505MB) – 310,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edb1f62a160bed9c84f334dc5f3aac9b<br>SHA1: dcfd47c3a88ff565acdb915f5649e21cbc303b86<br>SHA256: 7689b1a9166fe4a6fdc557587868213abf2a51450fa71b009274e766e94b133a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.74MiB (11.26MB) – 163,144 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c887138ef89f7f59f2b17761ee8e49c5<br>SHA1: b32864f43c0ffcc42bd668292f2400ed68a93b2b<br>SHA256: 5539671a459a608c4813bba1b63d4d7e1d58eb7ce2ef088d7b3f547b96d7382a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-08-22<br>IPv6: 2025-08-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.598MiB (9.015MB) – 430,528 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14390d1dd88f220d1621476da6cbce36<br>SHA1: a7a16d2ceb68d6e6e3519df2d283fbb5dafb42a5<br>SHA256: b8cb00bc87463ac1161ee2f02101b23d2f54bc101da8b39eb63d7e086ce8da06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.130MiB (7.477MB) – 108,476 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b47e326d2adf5b68fa2f3bb5cf71cdb<br>SHA1: 8202c7aa0801515c8f037a8c6379bb92e325517d<br>SHA256: c2251669797f0c1827700c7aee6f3b33c5603a2f1f710be78db634cf114d7fd4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-08-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.83MiB (12.41MB) – 592,342 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36f12ae813989fdb241905fae9170d64<br>SHA1: 5aa4babeda896f5f9300b1816a8db1bd233943b9<br>SHA256: e0356e645fecadfa4ad9e49c4d4b7ddc28344472fdb04c2d1a396b174a6f94d2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>65.70MiB (68.90MB) – 998,497 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 321c4e996eb57e8c843f4a1a7c086b86<br>SHA1: d6e62f7315238ac4e6835164f379db12c9baa71a<br>SHA256: 205f2245f9cddffe0092ebc578e51180381224049abf9e44a11fa8815f384ede</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.840MiB (7.173MB) – 342,618 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fced5df941addb9056b94a0f6f68597<br>SHA1: de47b1f9ba9f0ffbb556398c71c34fbf530591e4<br>SHA256: db6544ac94d1d22426f86a2b1b3d5b70f2d1b38ecd54fa536f817c5e106d4055</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.11MiB (16.89MB) – 244,855 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f879c057a5e3c7efdb9494722cfb973e<br>SHA1: 2a0586c6bd247669bc87d96e3dab86aee5e3a9ec<br>SHA256: 648aa19d3202320593d396fb44d416960c2d602a521000ac2510160c5d272d14</pre></details></small> |
| | | Full Location | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (216.9MB) – 3,615,295 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84dbaf75b3817fac2d522b918bcc3861<br>SHA1: 9b4ee36fa0923a2f68da4704164feac99f7551ba<br>SHA256: 43bd2f31f3e4f69856dfa6208d46d73b0063c028474adf986db93aef2740a7da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>447.1MiB (468.8MB) – 4,343,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4cfa7e8b0505f21943fa43a915ea9be<br>SHA1: dcb876a3bb589b77672f628a8ae019d6011d447b<br>SHA256: d3f883acce4ef8ed03ae21f30d09b7ca51f895f0830643368c5767a3642faf6c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.152MiB (5.402MB) – 257,838 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07e653090dfd5d1c13121b162af09fab<br>SHA1: a808596024eb433213c8e90bc6277f5bb0611ced<br>SHA256: 6da92c7dd70266c69657400e1252ef514fc1e7028aa8a0e6bb3bb9294c78588f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.38MiB (23.46MB) – 340,069 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a95a5ab506163fb86cd3197ca9610e1<br>SHA1: a7fba9b72e8a271807218c6b426e547f46226c54<br>SHA256: d86789dca5ee5d16277ae57abc33199b0ea4a3b3fbd358a820c9a2d761c4edd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,023 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec0f30e04446d83c414d7ba54cd9da6<br>SHA1: 4440d7254688eef8397b92e3f583e9b9240fe63b<br>SHA256: 3eb81d283d8a85d9a1e21e2d775d4bef02c37fd3fddf7b3981fe5aef17ec27be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>287.6MiB (301.5MB) – 2,785,870 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b12d395e9581ae946a39d0335c84cd65<br>SHA1: 66a2ff83b2e1cedccb7704236a41162bb2e963ac<br>SHA256: 8a594aae021dd354a93a799eaf42efd4fab365f15f15ca3401e4ee230579599b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-08-19<br>IPv6: 2025-08-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.40MiB (13.00MB) – 620,782 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b60b2056afbe94b5ba933acc8d6f7fd1<br>SHA1: d121afba06910b3a5e452761473878168b8db80a<br>SHA256: 428539ebf205e79367462aa123b1083856da2a094aa41bf653217ccce67673a3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.85MiB (43.89MB) – 636,054 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd3c720531e5758d33c787939fe41604<br>SHA1: bfbb1383476f2fd4af3cc652f9e14706b075efe0<br>SHA256: aaa5205696ae61fabfed59d013712f6e75cc774fd9487c167fe4edcecececd9c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-08-19<br>IPv6: 2025-08-19 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.7MiB (182.1MB) – 3,423,141 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab01b1f791472d8d6e1f58c915d7826c<br>SHA1: ae28c4a3b9229f97e328317c9ffda8bfe1d58092<br>SHA256: 6bc6e12a6d5570fd18183b8d03b6ff2c40b71551a76dc919bc0207733017a958</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.5MiB (193.4MB) – 3,423,141 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d34051e516fafcba304f40bfe1c94bce<br>SHA1: 877400ac2efde2dfd73b7af314decf5f0bd6c0c2<br>SHA256: e14b36412237c4f94714d99fc0c6ce35bba764d64278b3496d9f1ffc0e6211cc</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.7MiB (181.1MB) – 3,423,141 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce9ecb77bb1aeba83b77866801416772<br>SHA1: 1746e46294c0edb7d8be4c0d9541c1c8328aeeee<br>SHA256: dc4db1d75a535c2eca62a89c3dc62d641322634ced6b6db855a6e7bfde387dcb</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.5MiB (184.0MB) – 3,423,141 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d0e5968cdbf9257661da2583b7f58ad<br>SHA1: a4fd0e7862f64fda4d7e9db07eb4330f1afc8565<br>SHA256: 6e18d2f19e538b7b1dd90ba33cc995f7be215cb8f708a6de62122a41af503855</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.0MiB (230.7MB) – 3,423,141 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3506c85d9fb834d48876a7cace2e2728<br>SHA1: 58b66a104573aa32b13824bac06dffd43e9e61fb<br>SHA256: f7c847cf549b3a17c2c31255f3c4c7a7914689a444f4f3311b3b7dc27807d465</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.4MiB (180.8MB) – 3,423,141 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89f79eae865459adb0decf37e26956c1<br>SHA1: fa85a162926cc5695d76491d356ed30c4a8b374a<br>SHA256: 151b4d649e62ec2d674ced82acc5f85fa57dfc04dfe1bc72941d2ab283f768c3</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,423,141 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46e25e6e4a08f341bc00a542207dd187<br>SHA1: 8d4a06d4d8b8c7fc6f18becf146ddc5f59acf26f<br>SHA256: 5b18083feabafea22508dc12ac7a3b28ebc6a146cb5aa4c026e6980c24a40b6a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.7MiB (188.4MB) – 3,423,141 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 560dfaa2a7b61e8c400a89188ced060d<br>SHA1: eacc8313e98dedb8cb9036fd7ceeaa007b3347b9<br>SHA256: 0c29a56cf84f7aec9c0e669c2fe7ff9836029f4462682d78265af74c9bb5280b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>173.4MiB (181.9MB) – 1,838,016 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17f5ba330b350ce1d98f9f560ad449d0<br>SHA1: 03ce28995b75b2b3a64a53db058e84b33825ca11<br>SHA256: 128ae2003a0582b814d7f6d2d8662af23dd69116db4621b2ee46cc4160d36f8b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>177.2MiB (185.8MB) – 1,838,016 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a231994f3a7bcc5182fa33286f92e065<br>SHA1: 7a7f6d8c2aff6f1ef449bb730a63f70b517f80c6<br>SHA256: 39819689d7c636f9dd12b800c64362040f80be74e082b21641155384a7b697fa</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>171.6MiB (179.9MB) – 1,838,016 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4951e83482a0fc2094b8488c49cb4601<br>SHA1: 8c980e6bd5a40598c35a5b3d54e36b61d0be4839<br>SHA256: c49b5e005c8dd72fd62a0f04c87dd794420b4484dc878c0c994e1ac1b2b67243</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>171.7MiB (180.0MB) – 1,838,016 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 556fe92db99a5468ee382eeedb196645<br>SHA1: cbdd03ef3d7a700f1cac23d350ccbf5edaefd041<br>SHA256: 81d970767583e2d7bd848c6c9cc34de893a85f1f23cc9597b2902c67e2418ddd</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>190.0MiB (199.2MB) – 1,838,016 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5db5afbad3fd11fbbc04b36f71f729e4<br>SHA1: f5dae98397917620b38c379bce7cde205a367197<br>SHA256: 655683c76bde9edbe4a17423c26f6e6e8f7c66afaf2ddca876591ccd04585fac</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>171.5MiB (179.8MB) – 1,838,016 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec415bfca4916bed237badaf1e1907a2<br>SHA1: ed0a6852beff5ee7858e0b6323a4abbea837daca<br>SHA256: 136b5bcd6301c0a3ae3e70652cfcdf6c7a2d01a36b97d5e6596dd10b9941e20e</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>190.9MiB (200.2MB) – 1,838,016 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76871bf44bc729f450df4355aebe7e44<br>SHA1: 784af40c6bba4bb95b6faf1d6d99c95f5e7e57f2<br>SHA256: 6f718189f3dc7ac9b8d67f19ce246639ccbea2d7dee9a6c0be5f952a1768299b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>175.4MiB (183.9MB) – 1,838,016 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3222df3add6bd98881ee8bc185c8e06a<br>SHA1: 147606934db04c1a59559e95f0fcf31bfbdd7031<br>SHA256: 6199892efa6c5fe8b32a2d95f3feb03d145f1cb97e922b5ff5dade251ab08e6b</pre></details></small> |


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
