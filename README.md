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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-09-01<br>IPv6: 2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.491 MiB (5.758 MB) – 274,801 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77e637cce473b1917354767a7d755e39<br>SHA1: c50d438a4243ea231d6d059288aaa7813f72d364<br>SHA256: a5d7a3c32aa587097f162802baedc4466bdb7db0066d08eabfcdb17c4ea67656</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.61 MiB (17.42 MB) – 252,485 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d8f16e840d9b93b7865dcb26ed511ad<br>SHA1: 70d86314d40a9b9a8e83d854f8edc1d8e9a78fd0<br>SHA256: 48cc3a9ae5ce5e9f59b42224fad238449901336a74b54922671694bf789658cb</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-09-01<br>IPv6: 2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.107 MiB (9.549 MB) – 456,017 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9bd8b66d8885dcf3f673705181ffa3f<br>SHA1: 5092e9bdc85e051f65a21f238498f3f214f2bf98<br>SHA256: e91ff49e016b42b7461b928861f0d9813e28201255d52e19a05e1dddcbb78a20</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.004 MiB (8.393 MB) – 121,746 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2878b01845a692ca16cb45fa6891fff1<br>SHA1: 58f8ba22bde4afdb35485d2db2f4470ff1370b45<br>SHA256: 4206b8d4d4b386365a376bd1c6343fb2b2a6c3c7530941b51b9ec7850cb0f6b1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.19 MiB (12.78 MB) – 610,140 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a81c1953bd60ebfc65769399d1f7dc0c<br>SHA1: 67326f760cabc67aed70e632ee21996539f2b2e6<br>SHA256: 9e782b12664a7c1b55a35accc00056fdd274c9d30129d201f250392fe536bc6a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>47.05 MiB (49.33 MB) – 714,933 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d9e7f4152b4d2469d511b75e76ef7a0<br>SHA1: ca1ee62512b8d3389aada3b9f9b0f78aa0ea9bba<br>SHA256: bf5f57fde8be72794888c99409e891722656785f1464cb1ec40a5213d4a29ff3</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.133 MiB (7.479 MB) – 357,311 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c47fd01af8b18cc1d5cf2004691771<br>SHA1: 6b08ac2e1f8b48e55e72f8ba6ea0079e50a1af12<br>SHA256: 63aa3454aeef9769e4f0d68b4b93b23a7d195199a50487f4db5d258d90f8b08e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.68 MiB (24.83 MB) – 359,841 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ed7b2550b03a35e3bcceffa4ff9516e<br>SHA1: 2f8880592eb4dfde0c92576fbc78417988b521fc<br>SHA256: ecd35f269cfec0024d6ea639910b54c657f3f1dc08ab339c3d0b0384ed3cb607</pre></details></small> |
| | | Full Location | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>204.7 MiB (214.7 MB) – 3,588,539 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343b463b14a760e04ccbd188e88baa4d<br>SHA1: b7e446f674922e349cb17f01c859bc3bd62fd5e3<br>SHA256: ba1847bf8c90ff7f1ab0a19c20aae3512e9bf7a3f144673fad5d87dafbf7780a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.2 MiB (449.0 MB) – 4,160,441 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2542313832b0583d31e84cd0f9afbfe8<br>SHA1: f2d167034376bc0d28d3f5a38fe3c15945c4ba61<br>SHA256: 9c2aa7d6132f5be8f547273ac5e8f21c074f3d7a26b3f7795c642f4a3b6a9693</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.693 MiB (5.970 MB) – 284,967 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97d1441c258db85b80d0e10e763efc3a<br>SHA1: bba017e67350bbb91f08c10880ea6bbf6075ce56<br>SHA256: 9f5f3b2e3fc347c2c22172f226a573570d8ea695da978d00eff31b6ec4c0bcb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.63 MiB (23.73 MB) – 343,947 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b535c7a01e55c212ad6026f97094c92<br>SHA1: 48d55f71ae24b9f77ed2ef0926558ff6cf80dc3d<br>SHA256: 864a57987908eceeceecd3527d4e34630a58ff489bc5b2f73ef46eeaaf2f0e90</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.2 MiB (177.4 MB) – 2,928,511 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ccbf72a4307bf248403aef0a149708c<br>SHA1: d217e8012b6f3ce376e14989cd982f9ac5ce09e7<br>SHA256: b13b48ae2e8f41dc7d68a5dc01260dad043b4d119d3facdfbdb8af15a20226be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>302.1 MiB (316.7 MB) – 2,928,220 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c526d9a3e207b31b76b3907454601b0<br>SHA1: fcd803fede475e876008bbda8d9640e03c187231<br>SHA256: 1f6a62357734817fd3ced380fd7dcae8e1b8636e8143e3169f12b64ad522d539</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-08-28<br>IPv6: 2026-08-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.22 MiB (11.77 MB) – 561,897 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b20805d12511529085a5a922eee29fc<br>SHA1: 2a733555663adccaedf36895c5a44659aeda6169<br>SHA256: d999c479e8b4c32fadc43d8cf818b698691f65110ba60a5af0602962c4102ad2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>34.85 MiB (36.55 MB) – 529,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04ec853f748752a347565ccc3d4d9219<br>SHA1: 24691876d22af3e6876f5196989c32e3992cba07<br>SHA256: 4b4ae6a45054b7e7c8ae9f0441190a9e79c5de85319f9859d0f1003f97511fdf</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-08-28<br>IPv6: 2026-08-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>190.3 MiB (199.6 MB) – 3,710,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdd75229edb471307d30adf4b86cd9d5<br>SHA1: 7d8d4e0b3090cc3eca09826e0cef6360e420992f<br>SHA256: 6cb34270701edb79402e78e19bd8849bb12e70cfedaa0295e5ca88aaf3f496d2</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>199.3 MiB (209.0 MB) – 3,710,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff85214b325a5577d0e7ece6c1f24f30<br>SHA1: dc1879a9fdd9c33269e462b31fa69eae8162534b<br>SHA256: 34d9eb1929908388aabbc5823644d48381b526e1db71865b2296bf21050b4739</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>189.5 MiB (198.7 MB) – 3,710,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77f00d4a004cb36913e55d7b624bb983<br>SHA1: b4828817b06d40acc111d8f1847b3019e79a468c<br>SHA256: bb3eef9484de3aa20365f220e4271425e2a4b5c09d9ef412d070c2f31500c2ec</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>191.2 MiB (200.5 MB) – 3,710,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b57a6c7b345f0b9c5dd5ec5f4df14911<br>SHA1: 5e5903bbb757bd5ab152f120baf0b42a1daa44c2<br>SHA256: 86f887a7c7c01432c76164fbb5b994a0306079668b1e8a32be69bda8a076488c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>240.9 MiB (252.6 MB) – 3,710,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c50b264941f64cbddc09f5b0815e8e7<br>SHA1: 26286ef968bc96e51e406c7d88fa67f64d66a4e2<br>SHA256: 68436b16aaf455ef8ec040d6fa0c892e803f3aaa65eab79fe2738e49e3d0e5a3</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>188.8 MiB (198.0 MB) – 3,710,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55822039069acb4e700f7aa0d9966d1f<br>SHA1: 4022b9818281b04119908347ecc3e5ece47e6a22<br>SHA256: 598e38ba0d0242a78d4c2bf83ee2d7089bfa103791c8533c81f3380893cc3aa8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>231.1 MiB (242.4 MB) – 3,710,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e5b0a9d58aab08926b8dade7d44a2ba<br>SHA1: b80096779ed1867060ad42bb92ddd48f912722f7<br>SHA256: 549270d43847e954d36e39ac223a1c4ae1ff9f8b039ccaff8e931341de0c7a52</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>194.5 MiB (203.9 MB) – 3,710,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58f26ac99cf3d980e08b1513360645c5<br>SHA1: 206846f763678d7c20caba189e6ffc5eca637b74<br>SHA256: 722f760b71a401857c7f25279cc97ffe55bd8a5ebb2c1d61898893dc76bde97c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.5 MiB (209.2 MB) – 2,087,895 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4b607b810d6faeb11ada68a5164705d<br>SHA1: 449cab485cce18dce0361d61dbf6277443125fce<br>SHA256: 78d08f857b5f52a04ed43b5c6814c7ad5c3ecbf5a8b6db1651972c446d07fbc4</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.8 MiB (212.7 MB) – 2,087,895 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45d89f4685b33ce0b1db37e03d0820d8<br>SHA1: e189cc2e54907dd75c483bb963258df804a36f45<br>SHA256: cc49b288ded25713c132cd78c5ee73f213ed340263a1e927cda706670bc3ac41</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.8 MiB (206.4 MB) – 2,087,895 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c242b67e967f18ba9f91f96c486216f<br>SHA1: 2d881635e5930d2058dbfe10da9484f3e5effe98<br>SHA256: 712c70234982b0c09347b022247ef6b675bd373d06d5e2e375e1e5d180c1ea37</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.3 MiB (206.9 MB) – 2,087,895 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a551b332d3e2a91b2c4a88f005e6eb1e<br>SHA1: 7b77d70fc382132eb940c5b5cf42b5eb2156fd5c<br>SHA256: d4b77094b17e5bd85d485522038a13ffa96c93862772115e783c097f579dba46</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.7 MiB (230.4 MB) – 2,087,895 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e43be30fe87afe653d2f56a28783c55<br>SHA1: 40739350928d5f72d02e7aaef57b2b2b76a63c48<br>SHA256: e48244cc9ea5c66a78c7c86b077345ddbfde7ab258fd5070a726a8062c3a9ca6</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.8 MiB (206.3 MB) – 2,087,895 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6078f9676b6836a0a11568ac10919864<br>SHA1: 05745cc25864898167d4341eff63402579639fa1<br>SHA256: 90aa6d10a8f3a4ac7dc808b7388fcf061fd9e03771b94bc87949a71298e3ee98</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>218.3 MiB (228.9 MB) – 2,087,895 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10f8e7915553779a85145b56be1bed77<br>SHA1: 371cd65f23e142f9d340541fa8fdce5260aeeffd<br>SHA256: 79e3e320934113bd6d18cc46b416eea7ad3c2d2c72ec9160d75cbd67e0c35260</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.6 MiB (209.3 MB) – 2,087,895 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0bb59d39a922c4fd11f24faf76f073a5<br>SHA1: 906b8cd358148a922290d7b7c656a84118fdd95a<br>SHA256: 8bb8f86a20d354df4ea8a77f198c20a4f25e63a67cb769416ac16a52cfda06b8</pre></details></small> |


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
