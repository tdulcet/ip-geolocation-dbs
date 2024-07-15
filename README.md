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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-07-15<br>IPv6: 2024-07-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.744MiB (4.974MB) – 237,477 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9310ed57c23e31ba85597b532c2d668<br>SHA1: 31972a33a9003bdaba342ee99f6bf3107b1b89db<br>SHA256: c26f9500b98f8fd21584cb480e5068fd3afc6a32b9003c62b7e2dabe88e2c7db</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.545MiB (6.863MB) – 99,460 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: add9645a1d0a9e84a3b9565ece9ad816<br>SHA1: 035c3d5167116a2325f768d3b6240e2cea3748f9<br>SHA256: 47cab48fffe6ebf3482de5b4e5d4de94f3a5df88ed36e02a778b1e350fe9939a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-07-15<br>IPv6: 2024-07-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.098MiB (8.491MB) – 405,530 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acb7e8631cbb986c6b19e7ec61dec7d9<br>SHA1: 15aa33b56ec67b315a932034475e95c9886e8b3c<br>SHA256: 6a1115817bb15afd59d8a6045278f78ad674ec4aa5d3bb0400acae2ffce7a9ac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.573MiB (6.893MB) – 100,009 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b5b5e82c8f31f83bcbff23c707865ed<br>SHA1: 26f2d4c1374da92c00a2ecd92b56dab49b3e757a<br>SHA256: 2305df4449add703a55b3f4a0e6b999bfff8ebc59f4ab3d681d728608a99958a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-07-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>18.59MiB (19.50MB) – 930,529 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae328389cdbe6beab88540d8e89f0e42<br>SHA1: fec737009da71133485622e1cdd94cd5cf268324<br>SHA256: 9d37afe1a062b67f06d0d0a25a646ee568d5e41537b059ba6053de0115d8e0f1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>76.88MiB (80.61MB) – 1,168,269 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 837b99671702b295c4f4d7782f3a0afb<br>SHA1: 1021bcac682c1d73011e7ff580abb1dd014bf42a<br>SHA256: e6d2b2de880b63e1da26ad696cadc36609e56b1d98f2a34fc7a0fe56bc951fc4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.909MiB (7.244MB) – 347,080 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cc33d54c3bf6b9175e0b145f7c4118<br>SHA1: a3816e7df4ffb8f7c8a3e26e9ecc5b337da78413<br>SHA256: cacc1ada016c1e717e0b0224945498ec7c02f45e18e6ccc3f699cf925eb98541</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.77MiB (16.53MB) – 239,599 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d8002e2bd70b383a55c26aa6c39879<br>SHA1: 2e8b5538dfa991864d56253287cfea899c731ec6<br>SHA256: 417be26de93d6c5b8d2da113e60494952f0235ed696211cedbd93a8683cecbc7</pre></details></small> |
| | | Full Location | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,260,981 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1931ab257b12ab9982e2e837f7a344a<br>SHA1: 265a511f4b4152bd6a0cba4302e7e551263bf78e<br>SHA256: af747f9dd2423c564835352c37e87e14cf8cec475eff93b3c6b458b8ad3a8e43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>339.4MiB (355.9MB) – 3,295,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3cd81e94c6b15797cf1a60147cbd224<br>SHA1: f49f6c791890b20c1ca8c05135f5558493b09356<br>SHA256: b412df8ef796f81fa4522b3051247207cb9af864a32937188218b559f4a52daf</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-07-15<br>IPv6: 2024-07-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.882MiB (5.119MB) – 244,344 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f71b297b6d31124fb4d85a0573420148<br>SHA1: c19cd0e022cce41cdad248812b6ed96ce01f3d96<br>SHA256: 4f6fdac09cbc5c0e25e4305fde012ad03b4b27ba701095ec557f2c1ed1c594bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.18MiB (19.07MB) – 276,325 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 455753ce19833b0e8aa5a719617562cf<br>SHA1: b7cdef244498f6ea069a0523ddc0f9997aed06ad<br>SHA256: 7da4ff6463125871ea8fa12c1e2c0bb4c82cbd5eb13603b15bb06a6c12f21dbb</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-07-15<br>IPv6: 2024-07-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.9MiB (180.3MB) – 2,978,355 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec317919e654aaf26ba2956cba42987<br>SHA1: 5a1d6e846a17d001ab2649860d9e68064c6a788d<br>SHA256: 5099491c3b03773fa74caf9833a9dbb55e732c359aa505587dcd7b44b8c904e3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>200.7MiB (210.5MB) – 1,942,692 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 038ee21bebef5c2336a17368fd32209f<br>SHA1: a21d0b165419264ad815c5d369b16dde7b1ffe6c<br>SHA256: 7d3aaf19058abf9358cba535f4f8cc3c6475d21045808f084c2bc63c0857a3df</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-07-12<br>IPv6: 2024-07-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.865MiB (10.34MB) – 494,176 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3b4d69af3f82da58222ead444d9d9ed<br>SHA1: a57ec0e925c60a9b08845d4892e9178b40d33125<br>SHA256: 07b60fc353794c3c68683ad5e2c83120e86a2d3d8d2c794bb577f14351b5d846</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.48MiB (20.42MB) – 296,006 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01429ea541336de7afbdf7a41fc4290b<br>SHA1: c80ab631d4171c05cad7cf90256ca5b47ff64472<br>SHA256: 391544f0c3145dc7621feee93820efd94dfaf10ab8b70f045ef3663fb1423cbf</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-07-12<br>IPv6: 2024-07-12 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.7MiB (126.6MB) – 2,418,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fd6910b6b986046b62e1f198b30c7fe<br>SHA1: 06bd5327732e41ca37e12fa787bc0de416ce30c3<br>SHA256: eac0f69367fda179626e704d4fd9bf82f4664dfc309491b703d956b1d8756fff</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.8MiB (136.1MB) – 2,418,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a0fc000c801da190d9586fd2e7e227a<br>SHA1: d4d4987bb2a182d3ff0d366b5cc81d7118595327<br>SHA256: 90c979e291131e5790c8872409aeb898736dc58e07f264465e0658d571ba32b9</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.5MiB (126.4MB) – 2,418,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5705a9010dc871814df8634a88c3de4f<br>SHA1: 24604b3835972d3028107f44e1531663c7c4092d<br>SHA256: 04ede0af557dfc9ba472e86d5e29d21726cd84ff473fffdd777abb876d2963a4</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>123.0MiB (128.9MB) – 2,418,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27eed3b6a700a4ed50b2a03a4d1caa9c<br>SHA1: d9c82b47ca6b5d22ecf1279fac7517f55bac66f5<br>SHA256: 283cf26dc1dd166ea301071c1145b22781b42b9fdc5e7bcf99d1d2534f96eafc</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.4MiB (157.7MB) – 2,418,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d4ebfcad1e1345a8da7e788f342917b<br>SHA1: f2ff787577aebf644da17f4eea77603f1bae82a0<br>SHA256: be9a91d02a76640b2ffa71c2713bf0a2d5ef7390e5261a72b6451cd6d43a1a35</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.7MiB (125.5MB) – 2,418,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02edfb29a3fc78e963981c14b7db79dd<br>SHA1: 811bce2184c75b43dcfbd09924f23630a6f0380d<br>SHA256: 8769e240767be7281d3134c92af7203a9070ba2e7a7a29120b0e57e9f8797280</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.8MiB (153.9MB) – 2,418,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a3208c17ae85a00ce51ecadd931013d<br>SHA1: 7a40d552f9035caab1f56b8eaae9c0c7678f7ea8<br>SHA256: b7afeff093b58cca0f415260c55fd43f0b242000ff1702ff26e9e09004ffc5b9</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.2MiB (129.2MB) – 2,418,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8323d99eeb2a391e5f28f28f7eb94c7<br>SHA1: b641ab654f199b0b7b5f460120bd534772f471e5<br>SHA256: cdae0b9f6ed03fd43275debf1a089f142a47f8e40fb93381dc3aa50a24ee6134</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>117.3MiB (123.0MB) – 1,263,760 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 739d95d91774f88f1dd856e84ed9349d<br>SHA1: 80f73032449b1a60aafe94331a1aaa88b48f33ae<br>SHA256: 2400fa43ed6aaa5bffd2af8ee3fdffbf44c6a8a2f8e4e46487bbbce69360c163</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>121.4MiB (127.3MB) – 1,263,760 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4eb7dd0623f5dde06705f44862dfd347<br>SHA1: c962352cbc3af60d50257cb0f62e7ccbe3850d34<br>SHA256: abf7b0dab38be0b3816d6ebb681a94723fc9331452c65aa6af2c20a2df4e54a6</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>117.7MiB (123.4MB) – 1,263,760 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e242e606f294745cf15baa7c78133a8<br>SHA1: 42fc443e27e7b659b1b4efe69c9a75f78b054964<br>SHA256: e41d190cbf335c9bd5c4b1c5187cbbb91e7af5a6a6634ea3fd774c378b76becf</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>118.1MiB (123.9MB) – 1,263,760 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 152e27813087ac86358a1654474d4510<br>SHA1: 39ade204826e504d669001f0bc2efeea4a7bc1f1<br>SHA256: 3c9f098f244ed52190304642793a20b4889740915c1abed7a2815a6ce3c0234c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>129.4MiB (135.6MB) – 1,263,760 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2d5c3c98864c52c41eb5399a3b543e8<br>SHA1: 0d24a26494062f9e1a570fee76047f6e12555e28<br>SHA256: b351d35325d0e0727dcae94c1b983184d5984cbefaecd1f28b7770f8e30dff30</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>117.2MiB (122.9MB) – 1,263,760 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1aeab91f0caa8752e7f25f5bdf49f9f6<br>SHA1: 6c5ae5167ae62ffa2714d73bf627b652b6f11f6d<br>SHA256: e255557718a300c59e2f0762802ddf83baf90847a9d6e8f5b266b36ce54b8625</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>128.5MiB (134.7MB) – 1,263,760 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50d01277f80d8cb06b0e278ea7c9d678<br>SHA1: e50eeb0b732cf343b14ca23bca4c83850afad75c<br>SHA256: 877e1088d5f0a72bb9e90bea5e4316f571d9f7e34ca424f9056b6aa2b11f8835</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>119.2MiB (125.0MB) – 1,263,760 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8765a6497d10be547096d631aecaca5<br>SHA1: 6cdaa5e0eabbf1b6a16f6c3f00c81e5f2bbe9e7d<br>SHA256: 4cd72eed0b602aad53d729987ab7b61f647fe7636d769d9b492d0cee51de42f8</pre></details></small> |


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
