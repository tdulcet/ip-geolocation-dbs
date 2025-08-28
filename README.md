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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-08-28<br>IPv6: 2025-08-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.218MiB (6.520MB) – 311,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e812d6169545ff1d890bd63cb155685<br>SHA1: 234f894a1dc19a45910e2d40a5d39ef610e08a6f<br>SHA256: d887ed8a09a0e90ec0776548f0c9ea3501acbff7981051e94a3e8cf7ee07705d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>7.103MiB (7.448MB) – 107,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d5c02ad31f0988851e33a0b8113dc11<br>SHA1: b9d6e8c3728a7a6ab1df3d1fc2f01a278f725926<br>SHA256: c6831a52a35df9c7c73907c49832e512c1101049935d393565517fbced83bd39</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-08-28<br>IPv6: 2025-08-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.613MiB (9.032MB) – 431,296 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4bf639650088256d964490d3815ece6b<br>SHA1: 9bbc2983ddfba38552ef9be78c92422c73cbe6ab<br>SHA256: afa9987c4e3ab80aa7ca3cfdaec18d8e45fac60e7b49794211ab8dbb555ed476</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.165MiB (7.513MB) – 109,004 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50b87126638cf9a8d2ad34d574a818b3<br>SHA1: a43647d312ebdfdd46e1946255ed548821379541<br>SHA256: 2bcc322f3277aa0c5d4f94592345d31dc85a0d7907b8472b25f142d8296a97ad</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-08-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.99MiB (12.57MB) – 600,314 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f07bcae85035a6bf0062d50fcaf27424<br>SHA1: 749d9360b58d01f2aa0e0139addcc8b3d2c68787<br>SHA256: e4c06d8abb29f2cf9e06ee93ffd4c66029e162a17c9e811c68c7acff5c1f904a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>96.17MiB (100.8MB) – 1,461,472 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 260d26a16f1853fc34413b4a6c99c97b<br>SHA1: 8a9bcca8778164de3d7660ee0c589a6f2b4dff23<br>SHA256: 137b263d7add8879a7dbbee86ef9c18c445067f8df6126014060cdf95fc55b59</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.840MiB (7.173MB) – 342,618 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fced5df941addb9056b94a0f6f68597<br>SHA1: de47b1f9ba9f0ffbb556398c71c34fbf530591e4<br>SHA256: db6544ac94d1d22426f86a2b1b3d5b70f2d1b38ecd54fa536f817c5e106d4055</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.11MiB (16.89MB) – 244,855 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f879c057a5e3c7efdb9494722cfb973e<br>SHA1: 2a0586c6bd247669bc87d96e3dab86aee5e3a9ec<br>SHA256: 648aa19d3202320593d396fb44d416960c2d602a521000ac2510160c5d272d14</pre></details></small> |
| | | Full Location | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (216.9MB) – 3,615,295 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84dbaf75b3817fac2d522b918bcc3861<br>SHA1: 9b4ee36fa0923a2f68da4704164feac99f7551ba<br>SHA256: 43bd2f31f3e4f69856dfa6208d46d73b0063c028474adf986db93aef2740a7da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>447.1MiB (468.8MB) – 4,343,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4cfa7e8b0505f21943fa43a915ea9be<br>SHA1: dcb876a3bb589b77672f628a8ae019d6011d447b<br>SHA256: d3f883acce4ef8ed03ae21f30d09b7ca51f895f0830643368c5767a3642faf6c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.152MiB (5.402MB) – 257,838 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07e653090dfd5d1c13121b162af09fab<br>SHA1: a808596024eb433213c8e90bc6277f5bb0611ced<br>SHA256: 6da92c7dd70266c69657400e1252ef514fc1e7028aa8a0e6bb3bb9294c78588f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.38MiB (23.46MB) – 340,069 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a95a5ab506163fb86cd3197ca9610e1<br>SHA1: a7fba9b72e8a271807218c6b426e547f46226c54<br>SHA256: d86789dca5ee5d16277ae57abc33199b0ea4a3b3fbd358a820c9a2d761c4edd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-14<br>IPv6: 2025-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,023 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec0f30e04446d83c414d7ba54cd9da6<br>SHA1: 4440d7254688eef8397b92e3f583e9b9240fe63b<br>SHA256: 3eb81d283d8a85d9a1e21e2d775d4bef02c37fd3fddf7b3981fe5aef17ec27be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>287.6MiB (301.5MB) – 2,785,870 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b12d395e9581ae946a39d0335c84cd65<br>SHA1: 66a2ff83b2e1cedccb7704236a41162bb2e963ac<br>SHA256: 8a594aae021dd354a93a799eaf42efd4fab365f15f15ca3401e4ee230579599b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-08-26<br>IPv6: 2025-08-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.46MiB (13.06MB) – 623,576 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 509b6be5b17574410aa53056dcceddf6<br>SHA1: 98433386882dc38a2f919ada51ac7bf05965aecd<br>SHA256: 214c0e2eefae205bee9bd19fea7d3ae2621d645db07b17865405817d850c7455</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.95MiB (43.99MB) – 637,473 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 548de502b525f15010d071906c8c970b<br>SHA1: 4616f2c12e94d110afc46e229270f87715f81239<br>SHA256: 0eb4f46586e56e815737f10e4f221e8bcacd654511acfc793316e2d11469c253</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-08-26<br>IPv6: 2025-08-26 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.5MiB (181.9MB) – 3,420,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 489bf91aefee498aae5d87bd5e293a49<br>SHA1: 12cadfa5f7fd0b3df939b8a69fe1ad60ed0f93c7<br>SHA256: 0e7e293bceff4d4ffeb04f7b13a8ecaea4353cfa6a33df116e6ee4220b3b73d0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.3MiB (193.2MB) – 3,420,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4cc59d269324358261128a3a132c1721<br>SHA1: 8a7a41e9fac0169f08b8a50224a90c77ebaf789d<br>SHA256: d57de3642d369ff29456bc771195dc4952cfa9337971a25f90eeeea231bda6a5</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.5MiB (180.9MB) – 3,420,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ddea9e8e42b4b1dd062be52ef528648<br>SHA1: 581fe8d70035684ef5a41627056bb03dcd147a4b<br>SHA256: 2b02a6491a45b8e8bf1178e525ad793566fffebcb2f28b8e18c1e84278ff57bd</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.2MiB (183.7MB) – 3,420,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdcb5d3c1ff52e42fea71aa361a42087<br>SHA1: beeb2349df2808f8511280e08f58057955dc3677<br>SHA256: f89fcc95284bb7063a6de9e368cfeb7c6e4aefe85ec9610966f355c38d1b402b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.6MiB (230.3MB) – 3,420,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d733751f6e21bb50ec6d739591ae7a7<br>SHA1: 0937a91518e7b2f3ac7ff78fd8ccaef0400e917d<br>SHA256: d0ddfed722baf4c9da88e9660481d550580815c16eb7bd02eea0b75bbaf71e97</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.2MiB (180.5MB) – 3,420,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50b3f8b22f653741b6ff4d2180cd5294<br>SHA1: ba3ff05a44917815867db0db54db4cfe6e71daf7<br>SHA256: c4e0e1e90b91b1b567aa4920949d048c836cb474f43a8f6659803e6b3b45e796</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.4MiB (223.8MB) – 3,420,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eca8f1b8f49472f77506637d260d1d6c<br>SHA1: 6655b0e0776ea37ca18a5f39a84810c712b43f50<br>SHA256: 8174ee30c226696d7d984ecc316d47160c4ec16801dfdffc842db451df78c290</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.4MiB (188.1MB) – 3,420,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57abefc36107b7d6d7cfe1a7488e0e06<br>SHA1: 9459877469a0b56cc3be76476d3ec6978994ba81<br>SHA256: 09f8be7c13c71256daf91fcc1b7f5761893fcf87f2f2638dec9f95e713158777</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>173.7MiB (182.1MB) – 1,841,377 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6aa835667cea60f69ce28bf782a0e8b4<br>SHA1: b98d66b719a5ecc105bd27355dc36ce0314ba72d<br>SHA256: 449205ceece8732b9b68c37dbfe6674ab1b46e955878ae9260f65021b037a29b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>177.4MiB (186.0MB) – 1,841,377 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7bfda871032f5003cab576913b9fc825<br>SHA1: 1e12786d8797027901b0f3c937b0fb00eff76a89<br>SHA256: 7f5f3d6bc21a0c8d47225c88f5a18cd43e24cdb2ce4126d9acafbc4cb790d56e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>171.8MiB (180.1MB) – 1,841,377 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6bc0ce7211d6b1054637911e0acfd31<br>SHA1: 6770e4d608078db12228cea7b435be47324f3e60<br>SHA256: 7418250558d31880d3fb993cd013cbe277ffb8b681a9b4911f09746347a62138</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>171.9MiB (180.3MB) – 1,841,377 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1be5e0b4b9802a1bab801b7ccfbae7dd<br>SHA1: b8f8c8f223cfa8de7c8625de1d2ffbde486b0731<br>SHA256: 097075738e5aa7edfbdbefa0e819e7a4d76c4cec4c9eca7961c612b0cbd19718</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>190.1MiB (199.4MB) – 1,841,377 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 828b252844d284034069097e82b098cd<br>SHA1: e485d12c4fa6bcb6bc3f7c923081bc425738810e<br>SHA256: 043576c6ed32a3ad1357d3839bb56316727bfd4cd5d573404ad5c4cb80760b84</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>171.7MiB (180.0MB) – 1,841,377 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7df14d594b32a1c6d96bbc0dace4c8b3<br>SHA1: 7ca98cc524640b385ce13a12e7f30051f2e03249<br>SHA256: d1bee7f81b9c0efd002a3f6aec61a1bb0a9d6be227f9aa423799d80b6ff7a1b6</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>191.1MiB (200.4MB) – 1,841,377 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dac6c9a3276840664408e5df1837bc54<br>SHA1: b1bb346974f6b02e72b4afd02879a3db8175a288<br>SHA256: 2500761e66cfc05dbb9e4b9911fa6637e6c4f6930ed38f6cac51c76125dda331</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>175.6MiB (184.1MB) – 1,841,377 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00b92973fea12b76bd348b690916b414<br>SHA1: 7239d3515704d314f3fb3981bfe712d85a229c9c<br>SHA256: d9d6d00886be85574ae9b14f06d385937e53d8f85edc13f270f983ce9f67572b</pre></details></small> |


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
