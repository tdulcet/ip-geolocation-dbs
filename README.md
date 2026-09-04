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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-09-03<br>IPv6: 2026-09-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.488 MiB (5.755 MB) – 274,663 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06d918bf808ad675ec9e942058c9001f<br>SHA1: 400335bf081b18324a56adbac636b33125ee14f1<br>SHA256: 009124054821acd9cddd091520358724888004514cfeea7a0a4514d3451baca1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.63 MiB (17.44 MB) – 252,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f93bac36693f9177808e883fc06f1a25<br>SHA1: e6d8fc4a9b67be2428a6f5955bf039c8605d43a4<br>SHA256: b22c70ca3378524134922dbabf7ae00f6fe67e0ebdbb1fc79ac45cb824968be8</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-09-04<br>IPv6: 2026-09-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.119 MiB (9.562 MB) – 456,604 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a721ae88aac7f0e6e688eaa2ab507db<br>SHA1: 194ccd2b89cd2998b82c5cbc6b8efba92e2655da<br>SHA256: fa7b01cc220887b908c9dd762161f55aa4e03b20501650f94fb839af739bedfd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.002 MiB (8.391 MB) – 121,716 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec868f1a3a5a5f8e9a23e0c98064c273<br>SHA1: f3a85a11717f0fa18d16d28fb835148b65cd1faa<br>SHA256: 14d1ef1cf81f026a94ce8f92c9fe71165e327a355141ca980946451bdce472e1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-09-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.40 MiB (13.00 MB) – 620,859 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7ef6387f97a4d616e5296f015b03eeb<br>SHA1: db86c1c15d014de6a7890f69c7050ae6848b91f2<br>SHA256: a1ac6ce0747001cc101f634bad0aff5c6e0c959c6c6e08b1260140bfd86b9385</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>48.75 MiB (51.12 MB) – 740,883 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcc80a651c251cc77138974ac5b0d9f6<br>SHA1: 46ccac24f644bb8046ec943bd51b3548981c216a<br>SHA256: ae7e5b88c47efd91978397db0c46bff353d5670e95b064b343f49e0f3eb128e6</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.133 MiB (7.479 MB) – 357,311 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c47fd01af8b18cc1d5cf2004691771<br>SHA1: 6b08ac2e1f8b48e55e72f8ba6ea0079e50a1af12<br>SHA256: 63aa3454aeef9769e4f0d68b4b93b23a7d195199a50487f4db5d258d90f8b08e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.68 MiB (24.83 MB) – 359,841 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ed7b2550b03a35e3bcceffa4ff9516e<br>SHA1: 2f8880592eb4dfde0c92576fbc78417988b521fc<br>SHA256: ecd35f269cfec0024d6ea639910b54c657f3f1dc08ab339c3d0b0384ed3cb607</pre></details></small> |
| | | Full Location | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>204.7 MiB (214.7 MB) – 3,588,539 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343b463b14a760e04ccbd188e88baa4d<br>SHA1: b7e446f674922e349cb17f01c859bc3bd62fd5e3<br>SHA256: ba1847bf8c90ff7f1ab0a19c20aae3512e9bf7a3f144673fad5d87dafbf7780a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.2 MiB (449.0 MB) – 4,160,441 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2542313832b0583d31e84cd0f9afbfe8<br>SHA1: f2d167034376bc0d28d3f5a38fe3c15945c4ba61<br>SHA256: 9c2aa7d6132f5be8f547273ac5e8f21c074f3d7a26b3f7795c642f4a3b6a9693</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.693 MiB (5.970 MB) – 284,967 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97d1441c258db85b80d0e10e763efc3a<br>SHA1: bba017e67350bbb91f08c10880ea6bbf6075ce56<br>SHA256: 9f5f3b2e3fc347c2c22172f226a573570d8ea695da978d00eff31b6ec4c0bcb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.63 MiB (23.73 MB) – 343,947 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b535c7a01e55c212ad6026f97094c92<br>SHA1: 48d55f71ae24b9f77ed2ef0926558ff6cf80dc3d<br>SHA256: 864a57987908eceeceecd3527d4e34630a58ff489bc5b2f73ef46eeaaf2f0e90</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.2 MiB (177.4 MB) – 2,928,511 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ccbf72a4307bf248403aef0a149708c<br>SHA1: d217e8012b6f3ce376e14989cd982f9ac5ce09e7<br>SHA256: b13b48ae2e8f41dc7d68a5dc01260dad043b4d119d3facdfbdb8af15a20226be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>302.1 MiB (316.7 MB) – 2,928,220 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c526d9a3e207b31b76b3907454601b0<br>SHA1: fcd803fede475e876008bbda8d9640e03c187231<br>SHA256: 1f6a62357734817fd3ced380fd7dcae8e1b8636e8143e3169f12b64ad522d539</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-09-04<br>IPv6: 2026-09-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.23 MiB (11.77 MB) – 562,238 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 925617c67ce41a138c13a9c737693ae0<br>SHA1: c1bd3a1af908390ecadb72330c94510180d91684<br>SHA256: adc736e74d050255412d1cd5c447d6b1555717ad3a3c3834c2f49d9a863a81bf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>34.63 MiB (36.31 MB) – 526,253 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 255f3eae83a99ee80a03876e26db30b6<br>SHA1: 8ff855785efd89e4084c37593e52302330be43ad<br>SHA256: 8276b0b779b811be4c2825e19c3d59872b238ef8231aff785d437a6c88a2fc98</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-09-04<br>IPv6: 2026-09-04 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>190.4 MiB (199.7 MB) – 3,712,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae607cbef1026a7d3b579d63cd28e905<br>SHA1: 1aea262df2643ca621abd36d382c563cbbe0dcc0<br>SHA256: c42ed5ec393d4c21b741e07c5997d0c8f60a139777f5bfe74aaab6edde823621</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>199.5 MiB (209.1 MB) – 3,712,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58501c65ce8092549d2517eb4bf8bdc<br>SHA1: 5bda6ace3da98430f310c809e02539b0c0fd0dbb<br>SHA256: 567fac97d88377a71998b8d54babc216a5e597b0b38650803adc8d74ec9de84d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>189.7 MiB (198.9 MB) – 3,712,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c9186b54e2c084ef3c71809491baebd<br>SHA1: da2795f1d790892c6428a4aa45de818b4e4a1ac4<br>SHA256: 47cbb541c5b3863d3c437a0d65815a1a520fbaf1bdfc07140de1f626a3066c2e</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>191.3 MiB (200.6 MB) – 3,712,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beaf0f15c12474befb0e4186f61f5ee7<br>SHA1: 1d287dfdc40b202b6203115d9932391c45c312ac<br>SHA256: 3ffb26829f1bfabffdf2894582f8f81a3428d3484aeb0df65c8985975211655f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>241.1 MiB (252.9 MB) – 3,712,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 900fd2527c3bbe89bf1ea05025e84fff<br>SHA1: 646db86ba5482efc3ee5ab3191c06b097eadf200<br>SHA256: e012b5e323a67257cf84cd7f9c47b3b1f0a815ad8eb5797fd85729a1f3fe55ca</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>189.0 MiB (198.1 MB) – 3,712,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03c33282afbbb8db899fbcaf342af873<br>SHA1: 3c957101116fb5d70f7f9667b059e5f36666d967<br>SHA256: 5f310e25b4bd3a455ba90eb83ba997637ba88019f5d15587fddfc05df08960df</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>231.3 MiB (242.5 MB) – 3,712,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01f2226e721b5713bbe9d990ca07896b<br>SHA1: 5ecae3f3627584a44be348142d26950fd0de42e4<br>SHA256: ab9aa5d0da9b6151ab91797a3e8ace76c0f95f20ab42888fb1d92b7a9bb83958</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>194.6 MiB (204.1 MB) – 3,712,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b17b1cd6df0745196133c48245f9d5f<br>SHA1: 9b9565ef5d8d54f42f3886d860aceeb243d53984<br>SHA256: 086284ea57892450d0c5a93a3856b89b7077cf7128c79968711f15ec89c1ca75</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.2 MiB (208.9 MB) – 2,083,665 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0204f92e168f4360b4396e9753897fe2<br>SHA1: 0e24ab3d1c8f4e441985e9063af02a1243d4d016<br>SHA256: dabf2807dd6382e9f11bf253b238975ce7cdf219e3ab1e32dc82904baa3ddc54</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.5 MiB (212.3 MB) – 2,083,665 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fbbc03792f199c74650e7376570ce21<br>SHA1: 160a43f148928d3bf69aec90f08b270649eaa790<br>SHA256: 024b2ee5742dd37c353c99228db61de15aa64a01c67df37a97d3e0591c8aa594</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.5 MiB (206.1 MB) – 2,083,665 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f69a7e5b3bb0f6f7406d403e7bd82fa3<br>SHA1: e2f9fac37df5b08f234a02b3d2aec3f1228d7814<br>SHA256: 8f411a1eca22af1747ef4f38ffc24604b74d268f13df3d21a901d4cba80d4efa</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.0 MiB (206.6 MB) – 2,083,665 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0342a2fefc0788715c4fd4f36335d185<br>SHA1: 47806cfca4c501c8c6d3b07ea02da5da28cefc01<br>SHA256: 2eb7d3e643638f4ef490e353048e46c1e4cc4adaf8492e4153bb30eff8941296</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.3 MiB (230.0 MB) – 2,083,665 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb7f15c58004c6102ba126376228b674<br>SHA1: 74c68cae97e029d42bf8809d09930531a1970f09<br>SHA256: 67464889d7804d9b7e8cf75cd8115ae46e1695634dca3fe361ec5f766893e204</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.4 MiB (206.0 MB) – 2,083,665 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 171a90ac8151f90fba777688cae94a45<br>SHA1: 98b0f0cd86bce3610d2ab4330958a5f79827896b<br>SHA256: ef3590faa06bc9167e039ccbe60672d0acc15c781f50e9995c928f4527eeb15d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>218.0 MiB (228.6 MB) – 2,083,665 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08b106197758fce58b5635cad36ae9ec<br>SHA1: a3eb224cc5a98e5060aa4a126982ec78b4a1b47c<br>SHA256: 1939b910777b58b5bbbdf531b5243e5a44f92167a0269c692d359c566888d8a5</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.2 MiB (208.9 MB) – 2,083,665 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b002ca5f8520f1e541144a84dc7489af<br>SHA1: d4929eaf9e03a37b878dbdb11c8e50921e5cc244<br>SHA256: 7384e23d0dc265ac472cde2307d1af5e22724d1801e3bf7d9b3361f934201fcc</pre></details></small> |


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
