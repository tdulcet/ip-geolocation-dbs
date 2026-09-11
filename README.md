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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-09-10<br>IPv6: 2026-09-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.528 MiB (5.796 MB) – 276,656 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d55ee93cea3e6503e44545e2a0a6d60<br>SHA1: bfcc69060d2a000f052f94b192849e4dec7e2b24<br>SHA256: 25c80e5f0f4b71f83960ba13870faf04c71205c690d0f4b58a1c32bdd8c98be0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.68 MiB (17.49 MB) – 253,406 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57902c92a97c074d2231ef26b89597fd<br>SHA1: 361259b8a66439b347fb7983dab0387df8bcd468<br>SHA256: 1ff844a75f2f98510a4dcea39576c5ccc4d82b879845af859c1296ceab4ca6c5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-09-11<br>IPv6: 2026-09-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.124 MiB (9.567 MB) – 456,847 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ddcdbfdee9d5012d7009980ac5b5131<br>SHA1: 837f78a436b85c773cf59b782ecb24a283c31dbe<br>SHA256: 527e55f34ae1adef09f8c53c6a7e902cf28396c64af0e98c1b851a6d7cbad396</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.016 MiB (8.406 MB) – 121,937 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2933db6464ecfdd858ee38c3d2ca8abc<br>SHA1: c8e4c3d4316b80b4534b8ca1fa36fdcddfff3aa3<br>SHA256: 95add39019bc1cda740c524132f92557ca5695b3efcab31e36ccc2ce663d1c34</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-09-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.30 MiB (12.89 MB) – 615,605 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 830d4662bad4dc66c838138fbbe23665<br>SHA1: 4d695b6602a3ecbbcae7cb48e3c577329a1149b1<br>SHA256: 41d8b7aa46f34286219de2e577589accaf6ceed62cf6e0935cc84ef666fca793</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>48.79 MiB (51.16 MB) – 741,402 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c55417285da09fec8da338f8d015bc2<br>SHA1: 621f576a23aa323cadf97f4bfbba3e87e13d69db<br>SHA256: 06ef3b0f497772e9a395b80db230b6ef6b1d4703dff5d6870eade5165e425e76</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.133 MiB (7.479 MB) – 357,311 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c47fd01af8b18cc1d5cf2004691771<br>SHA1: 6b08ac2e1f8b48e55e72f8ba6ea0079e50a1af12<br>SHA256: 63aa3454aeef9769e4f0d68b4b93b23a7d195199a50487f4db5d258d90f8b08e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.68 MiB (24.83 MB) – 359,841 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ed7b2550b03a35e3bcceffa4ff9516e<br>SHA1: 2f8880592eb4dfde0c92576fbc78417988b521fc<br>SHA256: ecd35f269cfec0024d6ea639910b54c657f3f1dc08ab339c3d0b0384ed3cb607</pre></details></small> |
| | | Full Location | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>204.7 MiB (214.7 MB) – 3,588,539 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343b463b14a760e04ccbd188e88baa4d<br>SHA1: b7e446f674922e349cb17f01c859bc3bd62fd5e3<br>SHA256: ba1847bf8c90ff7f1ab0a19c20aae3512e9bf7a3f144673fad5d87dafbf7780a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.2 MiB (449.0 MB) – 4,160,441 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2542313832b0583d31e84cd0f9afbfe8<br>SHA1: f2d167034376bc0d28d3f5a38fe3c15945c4ba61<br>SHA256: 9c2aa7d6132f5be8f547273ac5e8f21c074f3d7a26b3f7795c642f4a3b6a9693</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.693 MiB (5.970 MB) – 284,967 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97d1441c258db85b80d0e10e763efc3a<br>SHA1: bba017e67350bbb91f08c10880ea6bbf6075ce56<br>SHA256: 9f5f3b2e3fc347c2c22172f226a573570d8ea695da978d00eff31b6ec4c0bcb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.63 MiB (23.73 MB) – 343,947 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b535c7a01e55c212ad6026f97094c92<br>SHA1: 48d55f71ae24b9f77ed2ef0926558ff6cf80dc3d<br>SHA256: 864a57987908eceeceecd3527d4e34630a58ff489bc5b2f73ef46eeaaf2f0e90</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.2 MiB (177.4 MB) – 2,928,511 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ccbf72a4307bf248403aef0a149708c<br>SHA1: d217e8012b6f3ce376e14989cd982f9ac5ce09e7<br>SHA256: b13b48ae2e8f41dc7d68a5dc01260dad043b4d119d3facdfbdb8af15a20226be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>302.1 MiB (316.7 MB) – 2,928,220 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c526d9a3e207b31b76b3907454601b0<br>SHA1: fcd803fede475e876008bbda8d9640e03c187231<br>SHA256: 1f6a62357734817fd3ced380fd7dcae8e1b8636e8143e3169f12b64ad522d539</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-09-08<br>IPv6: 2026-09-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.23 MiB (11.78 MB) – 562,361 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 013f3f2b7c0e6de707161bbb1d70acb5<br>SHA1: 3cb318fb376d61df7ad59ba7f952acba6715f283<br>SHA256: 3a2f474bfe2e12ec2c01356d60c0fb2a7efe55c02719d25d1cb044ceb0a98420</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>34.39 MiB (36.06 MB) – 522,552 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3e8526eb5b945b8859bf8772f8f032e<br>SHA1: abb7661b7341233444be4a0210c82e9835e8de44<br>SHA256: 3473a28f080aa09eb6142faaa7e2bf61108db195ec8acbccbe770f8e4e13e012</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-09-08<br>IPv6: 2026-09-08 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>191.1 MiB (200.4 MB) – 3,724,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7214c5d810357688d853f716e8f47251<br>SHA1: 0b631b541f2db662130b86fbcfd121a6d060515d<br>SHA256: d749a29623146ee539ffc56373f0d05d55d581ae11261223d1e758c8fd89d4f7</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>200.2 MiB (209.9 MB) – 3,724,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d98472625ac199ff1ef5b45f5fd3dc46<br>SHA1: f61d0e64d69c1f330b9a8f32eac4576b633dd453<br>SHA256: be0f8cab8067a910fc31507eb2a57a01e17993e337281a9aabb89d13a7e041de</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>190.1 MiB (199.4 MB) – 3,724,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3d832295a5423d465d8486b97640bf0<br>SHA1: dbd23902e618bae3e32cee74d2c59ad39d9b317e<br>SHA256: 89b30a66c2e9dc89d40b53a5c889767a8ce49b82fbb1711fa187943a27e44948</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>191.8 MiB (201.1 MB) – 3,724,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 515fe9dadf08b02bad5e23c496962d99<br>SHA1: 3b1371605c5a567d40c2c63857c880fa2e9a207f<br>SHA256: 08503d425d5ab6d8ce2c809883592025deecaf509b6e46d178e6604d778d1952</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>241.8 MiB (253.6 MB) – 3,724,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60561c4e21fba9c46339d60bea908002<br>SHA1: fe1e412eb950f723c4efacac9606370f56c6ee34<br>SHA256: 483d28ccffd97e65cc3dc5bb3097ea610ea84cd253da8f9303f50b0496f6619a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>189.6 MiB (198.8 MB) – 3,724,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43fc7308ebd5c70a61b64503aeb5f4b2<br>SHA1: 3e9b2a3001dc16aa89af823fc0dad2ac52a8121b<br>SHA256: 0ff6bf70183772f4a65f3175851385ba58a52098240c0d7bc6fd2435386a82fc</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.4 MiB (245.8 MB) – 3,724,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5fd53b4649e165f9d63643475cb3caa0<br>SHA1: 70cc34b7795b29a8b6a35440a8058273089f3b22<br>SHA256: f3d8d6065cc6d6138f0a924adf57822669019a7db46d8ce59f2ca21e225c7d3d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>195.3 MiB (204.8 MB) – 3,724,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a11912c6ddda5d9b8aa882cadfcdb1c4<br>SHA1: 261e257ec8ea18e4381b840ea0cb584c7733d535<br>SHA256: c033b00a3a96225a258dbe2b5479a0330bfd4d70642fa384fc751d95865f2575</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>201.1 MiB (210.9 MB) – 2,104,802 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6346ea5236c8e22792bc03ca83585b74<br>SHA1: 6ce902bbdda31ddab1991a4a1f2d09bd6c0eff93<br>SHA256: f7ba4e0d34678d082154bfaa08416307d200d8a3ffb71eb7f41fa29e913e6915</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>204.4 MiB (214.4 MB) – 2,104,802 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5282abcf39336e9ac3e69927bd10fae<br>SHA1: fc070674fc7d0fab51c48fa56a64aea1b38e5004<br>SHA256: 4077cfec4ebefd2891d3e95250f4de38ee402e6b9cc2bd85b51662d6b54c8d18</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>198.4 MiB (208.1 MB) – 2,104,802 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f99f8ff0edddf0af2b2d9f678f1cbb6d<br>SHA1: dd1dd6876512c3a6c35550bc5681029be49b6607<br>SHA256: ab86f95f0a362db7c316bd6ff8256fd12cdf3bec4ba75a3c567832fe54a292cd</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>199.0 MiB (208.7 MB) – 2,104,802 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61e7388be96ebbb2847dc6925fc4ad8a<br>SHA1: ea617f3989b43e5bd0f421b6d4ef02429b7d810b<br>SHA256: d1780d9f6302ade62b6820068d16d13f77181425488c0ca0aea488cd4a493abe</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>221.8 MiB (232.6 MB) – 2,104,802 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4dad2a5b45e71142700592dd343e90a9<br>SHA1: 22d3aa0fd290636128b0938a853f6858ca77b8e6<br>SHA256: 79f650ba8af2586ae426905cd0746a49f5e277ba8bead4ac92e631c5e1ce8f20</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>198.5 MiB (208.1 MB) – 2,104,802 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b9fb1e94ecb452a74c5c48db5bcf798<br>SHA1: c6fc82502ea8c863084bc3183df4e2855e7fa308<br>SHA256: 63731a661ea39e7cd3ddd158f0e4f13d5c7c35fd4e37c934de1da5a1962a8acd</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.2 MiB (232.0 MB) – 2,104,802 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bfa031fd2e05470e92f1682cba8cc60<br>SHA1: ba086c4c842e0026aae02941c6f9242d39792b01<br>SHA256: 9259b00312b8d6334044399ecda27ffa0c45dd7557361a8f68f39d49cc64317d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>201.5 MiB (211.3 MB) – 2,104,802 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1252b2e47c5d7331ffe1d26a848948a5<br>SHA1: 6b04ed6a7d436a63fb3399f49418e670c5832d7f<br>SHA256: 3840f2a59a8d029c6976742987eef29646eca26e3db679b2d7fa21a8364b5d3c</pre></details></small> |


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
