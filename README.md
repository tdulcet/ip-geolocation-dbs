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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-28<br>IPv6: 2026-10-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.685 MiB (5.961 MB) – 284,541 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e1ecd750cc8b433713d0a4c9ac5e3d0<br>SHA1: 711ea6a0ded75d182b5996088d5b7224e7817e68<br>SHA256: 6c1f91a9acb4352cdd020663f52d3dd9aa9d7b138d5abbf355939f40a95b486e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.55 MiB (18.40 MB) – 266,671 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3232af8afe8cd8ae295b1dc1ede52c11<br>SHA1: 77cfcadea226a604830c9162c8917c1e0df6192d<br>SHA256: aa2352e9f2f45f07d51b44814b913db9b29ad2fab4a8d895858eec70c61d08c4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-28<br>IPv6: 2026-10-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.184 MiB (9.630 MB) – 459,882 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95ed132ba4e55bb90104f739022d2a9c<br>SHA1: c799ef8be4b8c60fa770a8c2d5e637734aa85d90<br>SHA256: cbde37d0d5ec6df58fe40d0120a6e55162a1eff05ad2a9557a54501945d2db9f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.104 MiB (8.497 MB) – 123,264 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf0e0705e586e260b27f08194a72e95f<br>SHA1: f15a43b4d22c0bc969ce33aac18ad671b40b85fb<br>SHA256: 5cdd38c70b05b8b6370b7d12081ccd62512a3beb967c5b528fa139d906d2e518</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.44 MiB (13.04 MB) – 622,593 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6603cb257c2ffc09524e828e7b10d9d3<br>SHA1: 0442e53e13308e24eaf551f8ad4d1207b09f4aae<br>SHA256: 7ca0fcbd336c903598d4164b07220c86d42897c725b39abf2d763fe310e301a0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>85.46 MiB (89.61 MB) – 1,298,702 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 865caeb0ab311a2f075e248cb4edae23<br>SHA1: f6b052fed0f9f2940be898ce6ed7126473007b6a<br>SHA256: 1ba47e7b22446dcba4e5430653d77d9c730e8f4874d604f7ddad1808994a4f11</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.818 MiB (6.101 MB) – 291,264 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eac94e3e3ab719ab78593afa964f45da<br>SHA1: af19435e4e57c25937afe53d6fba292805882dbe<br>SHA256: 9f6a222c0122eb47e34ee42c495df4f17830c0ee40f4a9921b8535690d3270fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.44 MiB (24.57 MB) – 356,148 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ce580593be34cc4df87bfe5bc81e9b4<br>SHA1: 7a4ab5ae6144faf1b72fae6b2c3be92bb30697c0<br>SHA256: adebdde6726b52568b80d2b7d08b6598f6ecc66c089d6ef69e629573f008cb40</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.7 MiB (179.0 MB) – 2,951,725 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68b1b79e84df6b26076250d820ea0b18<br>SHA1: dda1c9fc8b5b7c2a62cf7a72bf999fc82e55255b<br>SHA256: e664ee3e96917e7ba878660728524375c22f39e4e3aee5f4eda024aeac6910dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,535 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fa4ebcfb46463ed745e92304c503838<br>SHA1: df8c366979b5a5c5a906cf825f26a8437c8d2081<br>SHA256: d04f2b9be41819f8c7cc2d6f4075f927287880b221d8d14a85195ba76acecbb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-27<br>IPv6: 2026-10-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.27 MiB (11.82 MB) – 564,227 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc44b683a5bb81fcbca91831bd3a049a<br>SHA1: afbd9131f8736d8b0065525202cf8a30028b551a<br>SHA256: d0f69b18da179ea3033d98fbf69a5484dc4543bed583936fa1cad4070a01df73</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.78 MiB (34.37 MB) – 498,101 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee45a914ea91c6644e6356cdd582237<br>SHA1: 1923f57cadd959e89a927c30fd09a3f0b1d7d484<br>SHA256: 0500f523b8f4c3adb314032b2ff75d98ce3f9c55d76bf0ce62ba0e0ea0b17d2d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-27<br>IPv6: 2026-10-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>188.1 MiB (197.2 MB) – 3,667,569 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9965effeb4b35a9a5e011765096a505d<br>SHA1: ccee812930c3e499176eec465cddacd101917eaf<br>SHA256: b1c11ff4efc23687721c41e1538b03c19d4dd2e68d753c48bdd66d7d74722413</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>196.8 MiB (206.3 MB) – 3,667,569 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51fcc18a201ea7a7d4205481a2a6674b<br>SHA1: 70c71165c67d6c7c4f3fae27ed65eedc7b79a77c<br>SHA256: ec582f48ca04565dbfe7cd214ecf20873d3ecf86d2f849799176e288eae0ea0a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>187.2 MiB (196.2 MB) – 3,667,569 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c8d9250ee2c129f1a96362143996a06<br>SHA1: e1898db23c410b158300f5e55ad125f6efb8e677<br>SHA256: 9064282e0c4dad985bb6c532260fbb8beb1d4922aef8c5a6db2d2c2b9993b646</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>188.7 MiB (197.9 MB) – 3,667,569 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b22c1393f25d39d10cb40e7959544a9<br>SHA1: 1e4fe8a0f716a443426e095ba32ef81fb5ed417a<br>SHA256: 420b0a75f021edd11e86af392b31fa77f48b080de7f7421464fca76b63a4bf3d</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>237.8 MiB (249.4 MB) – 3,667,569 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a2d0aa29829108754af56738a7b09e8<br>SHA1: 903a728b500d0278702ecf90d039b1d4b50c5d7d<br>SHA256: e6decd4f442b8aedd0f1ae799bb5a1526225f5261a96caea8be6d8f214afadb1</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.6 MiB (195.7 MB) – 3,667,569 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46915450e03c5afeb2105924bb2e1a46<br>SHA1: 3aeaf329e949354b644705f886f3779fd549c537<br>SHA256: 007fcb1695d4871d129b9d25707c2522a1535429c2428a6b4d5f68814f9b67c1</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.3 MiB (246.8 MB) – 3,667,569 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a672695cfe3b53c18f60253b5c6a956<br>SHA1: d8d28992cb9c23c23cedcaaf90760def178bf500<br>SHA256: 62f612ee54064ffc2595964a14ce372687ce023fa655abaf5576a6f5a65468da</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>192.4 MiB (201.7 MB) – 3,667,569 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e80794cb722095c21b7aa86b0ea2106c<br>SHA1: 003a65eba910b59e51b81c74b7c1740ed508a9e6<br>SHA256: e514791d135f2642ad81593c942b72654275ebbb2d957d787a6efa67553993b7</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.2 MiB (208.9 MB) – 2,088,358 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81defe1594ff4e5b50c3cf9a842a8686<br>SHA1: 177f787aebb185588f3984eef9f7e7cab39174b1<br>SHA256: e757f9092a96277bd259796ec62a8e47a2919a37349d047360bd0922070b2731</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.5 MiB (212.4 MB) – 2,088,358 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afdeaa95318521e9defb32918ca3f755<br>SHA1: 925680d824ad778bff4a9d93b220eedadc5e28b9<br>SHA256: 9372987e1525dc3533f09cd61cd4a26e7c697ec57875840719bda38d730d1998</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.6 MiB (206.2 MB) – 2,088,358 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 256e9b6a3aa69549757202875e86fa1c<br>SHA1: b9bff3b1159ac31856bdea062f170303491f3d91<br>SHA256: 63a60dce53c6ae9555e1e1000bdace6c11de91da0907a75c1553ae3a7ef68eb6</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.1 MiB (206.7 MB) – 2,088,358 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d38253bde0f5f7a7ab654002838a62c<br>SHA1: 53e359c15f78a8224c9cae000ecf7a82738fc69f<br>SHA256: 3e3299201a828c7ea6379c85968e1158a2c036e50a47e947c92eebf744fd128f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.2 MiB (229.8 MB) – 2,088,358 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9542e0026c4f9fcfee741b80b5e03260<br>SHA1: 10f7f690ace5b63afc9d1f216021c93a3b1822a6<br>SHA256: fe5d5aff1a80e89f4b945487fc83bfcf5cee9bc6b3d71f281d3068c7207f0687</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.6 MiB (206.1 MB) – 2,088,358 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b07720398da8a19b1ba4c0699a9c5f9<br>SHA1: a6b24fc3d4261cc11b5840f1ab050014b8147077<br>SHA256: b74a564bb7cc124e5e31816fde0154923ecc998e97a49678adb79baedd73cfe7</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.6 MiB (232.3 MB) – 2,088,358 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37df36d40e6cea364d93477b171bb568<br>SHA1: 3db366f787e6b4b60e9a5408c61cfd23020ef570<br>SHA256: 3008acd1e48870fb824e49a70e494faf47c6e6176624d8c75d49161b0f7c298a</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.6 MiB (209.3 MB) – 2,088,358 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 016920a5b5cc88c1c527a8ac90db06b2<br>SHA1: 55599db9e244017363a3d0335b55976b87e569ca<br>SHA256: ee86de68374abcb0568fcec8979c04b40c7924a22615c2f34d126b847ffdf7a0</pre></details></small> |


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
