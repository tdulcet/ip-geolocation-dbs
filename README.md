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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-09-02<br>IPv6: 2026-09-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.495 MiB (5.762 MB) – 275,022 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22883301d33cc229aff5c3d344c42156<br>SHA1: b15e6be741e8ac9066c7f5586f0630d901ec9f5e<br>SHA256: 7c1360f9f6c4eafe8b48e4ca0dba1fac67fdcfa8a0554c9198896191232674ac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.63 MiB (17.44 MB) – 252,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e6baa595339c65b3fad1e6ae3d093ee<br>SHA1: d5a9c6c1761c551f8dcccada932f2c4e871d5729<br>SHA256: 1cb19a867fa5a23cccf9c9e619022953f4f3fdb0dbee6d371a37edec3b856961</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-09-03<br>IPv6: 2026-09-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.114 MiB (9.557 MB) – 456,378 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7bfa0567d8b5743426072a2dd15812f<br>SHA1: fc105b1b250962ce9c5bd4227aec904ec4964929<br>SHA256: 7eb0ac3f53db538a330d6d7525b73dd5905a01c0accb0a9e259c68f9d7b711af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.000 MiB (8.389 MB) – 121,689 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e8bc6bd41f0ca2f037b32a6fe2633e4<br>SHA1: ba3d43598e4ff6c1e77d4152872a7a15d62a2372<br>SHA256: 944457a43b6097737ae56d14d5fc81a60fea3c57d509df217bef25a0beabe143</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-09-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.40 MiB (13.00 MB) – 620,859 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7ef6387f97a4d616e5296f015b03eeb<br>SHA1: db86c1c15d014de6a7890f69c7050ae6848b91f2<br>SHA256: a1ac6ce0747001cc101f634bad0aff5c6e0c959c6c6e08b1260140bfd86b9385</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>48.75 MiB (51.12 MB) – 740,883 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcc80a651c251cc77138974ac5b0d9f6<br>SHA1: 46ccac24f644bb8046ec943bd51b3548981c216a<br>SHA256: ae7e5b88c47efd91978397db0c46bff353d5670e95b064b343f49e0f3eb128e6</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.133 MiB (7.479 MB) – 357,311 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c47fd01af8b18cc1d5cf2004691771<br>SHA1: 6b08ac2e1f8b48e55e72f8ba6ea0079e50a1af12<br>SHA256: 63aa3454aeef9769e4f0d68b4b93b23a7d195199a50487f4db5d258d90f8b08e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.68 MiB (24.83 MB) – 359,841 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ed7b2550b03a35e3bcceffa4ff9516e<br>SHA1: 2f8880592eb4dfde0c92576fbc78417988b521fc<br>SHA256: ecd35f269cfec0024d6ea639910b54c657f3f1dc08ab339c3d0b0384ed3cb607</pre></details></small> |
| | | Full Location | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>204.7 MiB (214.7 MB) – 3,588,539 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343b463b14a760e04ccbd188e88baa4d<br>SHA1: b7e446f674922e349cb17f01c859bc3bd62fd5e3<br>SHA256: ba1847bf8c90ff7f1ab0a19c20aae3512e9bf7a3f144673fad5d87dafbf7780a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.2 MiB (449.0 MB) – 4,160,441 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2542313832b0583d31e84cd0f9afbfe8<br>SHA1: f2d167034376bc0d28d3f5a38fe3c15945c4ba61<br>SHA256: 9c2aa7d6132f5be8f547273ac5e8f21c074f3d7a26b3f7795c642f4a3b6a9693</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.693 MiB (5.970 MB) – 284,967 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97d1441c258db85b80d0e10e763efc3a<br>SHA1: bba017e67350bbb91f08c10880ea6bbf6075ce56<br>SHA256: 9f5f3b2e3fc347c2c22172f226a573570d8ea695da978d00eff31b6ec4c0bcb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.63 MiB (23.73 MB) – 343,947 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b535c7a01e55c212ad6026f97094c92<br>SHA1: 48d55f71ae24b9f77ed2ef0926558ff6cf80dc3d<br>SHA256: 864a57987908eceeceecd3527d4e34630a58ff489bc5b2f73ef46eeaaf2f0e90</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.2 MiB (177.4 MB) – 2,928,511 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ccbf72a4307bf248403aef0a149708c<br>SHA1: d217e8012b6f3ce376e14989cd982f9ac5ce09e7<br>SHA256: b13b48ae2e8f41dc7d68a5dc01260dad043b4d119d3facdfbdb8af15a20226be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>302.1 MiB (316.7 MB) – 2,928,220 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c526d9a3e207b31b76b3907454601b0<br>SHA1: fcd803fede475e876008bbda8d9640e03c187231<br>SHA256: 1f6a62357734817fd3ced380fd7dcae8e1b8636e8143e3169f12b64ad522d539</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-09-01<br>IPv6: 2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.20 MiB (11.75 MB) – 560,879 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a96e3e9be6b4dda1b02081511a03ccc0<br>SHA1: 2c60071846bf74bc6e4b8792e0736a0f0a459d98<br>SHA256: c12eb5f84cfa36d0778ef6314af541f2b98b7c88387f4fa08024db4de6af949e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>34.61 MiB (36.29 MB) – 525,959 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8671980fb76208afe995cbefeb51f254<br>SHA1: ae68c107bb7037335f497d1dbaa37e9febb958ce<br>SHA256: 0d0c58a75cbe54031ed6b09a3b5980c5fb9c9474cacee12e00d92708152f564d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-09-01<br>IPv6: 2026-09-01 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>190.4 MiB (199.7 MB) – 3,712,023 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8b671987b89faa768d0053cd2f75c0b<br>SHA1: bb82f49024c33384131a610061668ac964ab7345<br>SHA256: 214a97e57fdf977cd6d42585803719367c5fb97afc3599aff662f5af80802a41</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>199.4 MiB (209.1 MB) – 3,712,023 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5d6161b461a82a4ce2af8d90060aae6<br>SHA1: 5803d8d87b92e940fa38627b84ef650770738f98<br>SHA256: 493e6356ecd12f815f63d1d2ff26e5fcfcfa31bac1c29081c1ca018a686912e6</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>189.7 MiB (198.9 MB) – 3,712,023 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc9f7d121e809f03d222336b14d4db06<br>SHA1: ca293e8f72e6f5f9690bdb729edeaa5a4685f273<br>SHA256: 0bbbceea48b234d0b38f61a05c34f01764127a7f25feee6bd7fd6b36601f3968</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>191.3 MiB (200.6 MB) – 3,712,023 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34f712643d3069acda7c9fe6e996468e<br>SHA1: 7953ab63d067e5ece4ba8518d977e77182a5a486<br>SHA256: 3b01726e62b2262947f257ba89899a7effb5fb552182e7c66159a944fbd10a95</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>241.1 MiB (252.9 MB) – 3,712,023 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cacf84b3d4f02ab7da34800ddfd612f8<br>SHA1: 1f2469763364c14329bcd6844912dcb94bec2038<br>SHA256: d8d700e7dfda5f3ca370142fcdf8891942cc21992c811626f2235cb701e957bd</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>189.0 MiB (198.1 MB) – 3,712,023 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b81ea611da88fdf7c4a444c50dc466b<br>SHA1: 421a5dacbfdc7b8383c7c082efeb3a9d02870750<br>SHA256: 24beafa85fef5a9873f2e8c4593cd8dcb80917d7d730ae9b4b62e4146a7ed16e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>231.3 MiB (242.5 MB) – 3,712,023 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01a0c474121c52ad4f4ca9b6bbe91ebe<br>SHA1: ab5ca3579046819988e840601c399b502247880d<br>SHA256: 2dec7d7c878045cf5e92a0614e365dd6c582095beb81864b194c3f91b6a02127</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>194.6 MiB (204.1 MB) – 3,712,023 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a387989b603abf6c91e4a78b70f986d<br>SHA1: 5b1dfe4a5635b731f3d7b972554ccc43a0362e38<br>SHA256: bc4ce46ba61f5b0c48ec11fc582bc7029c21686680d2ca36cc5337da1cd0f82a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.0 MiB (208.6 MB) – 2,084,053 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc1d586f6819e4adc78452790fdb693d<br>SHA1: a08c8d2e15b2eccc1658bb22419f31eb5a90b82c<br>SHA256: 028f757e90d5bea0b27b9244d10379e2b43b7f37fffe5890b6b7a7f8b9e69fdb</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.4 MiB (212.2 MB) – 2,084,053 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd2c0aa4e1d03532e857d80744898bc4<br>SHA1: 0352359de6c85c190da76322a2e19c7efce9d302<br>SHA256: 84f93c1b149d9fc5fd875e695451f310f2a4dfae8a9707835d0a95d97d76bac3</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.5 MiB (206.0 MB) – 2,084,053 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38199c1efb7177b655a21925dcf20bb4<br>SHA1: 26c2de36e8a059d34f8d111e258c2c1a457dcc7d<br>SHA256: 80aead3e1fbd4dd7df7080528558e245bb6db6ebea1dd6501fd4ee650f8a470f</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 2,084,053 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e8e324394913cd29c0544d36edc8e63<br>SHA1: 2547512009c78beb8930b6a77c6fda73550fbc64<br>SHA256: 603414555b4b1e4a791eea004a5f93621ff600c0aaae3e00b7f9492dca24f322</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.2 MiB (229.8 MB) – 2,084,053 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43bdfe825f14158ad3ffa0a237d327d5<br>SHA1: ea934f04227054a6547d512e135cef1868b7e015<br>SHA256: beca551b5d474756d5c0360ed335a933de89de2e4938fccae9202154cd664197</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.3 MiB (205.9 MB) – 2,084,053 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2938659bd88f1b350308abf9b83fe891<br>SHA1: 128f18161d950ca9b4694a3623079b710584a2cb<br>SHA256: 512fd8295f103e40afca1af0e27fa92002fc6cf7516819c5cf730e052ba2afee</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>217.6 MiB (228.2 MB) – 2,084,053 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 631e2d520a32a32464e78871607e20f4<br>SHA1: 8883cecf4b4ec29e9c59e14f9431d72086b6bb81<br>SHA256: fa655d9e9f87c81dc0554f62823065166569716523d2288b94ee6ed9086cd61a</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.1 MiB (208.7 MB) – 2,084,053 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a210139d91039f362a6b6d53572ad6a8<br>SHA1: b48b63ecf82ff2f88ab84528a87c9132c1539d6e<br>SHA256: 83dd9e21841cefe5bb55d36fe337a4eba1e5b5eb56cf8fbc8bcbb0f578138095</pre></details></small> |


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
