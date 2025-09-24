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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-09-24<br>IPv6: 2025-09-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.280MiB (6.585MB) – 314,443 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a52aeb0b6a81d7e84ffa98e4a0a93b24<br>SHA1: 53aafa1ce197a477fe160710062a990e10f1128a<br>SHA256: d15a17925c8ebd2ee5dea988bcef92e1c0448a1e2f692ee7cee8acd9992c863d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.764MiB (7.093MB) – 102,791 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07a11fef6252e0a7eafd6ff2018b9192<br>SHA1: ea8e188e7a7b097fd9e48bb8d8298bd09e2cbdef<br>SHA256: 51e468840cf5f78c4c3d89ce3ac1e491b5f6bbd1c3b654929ad65618397a3fe2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-09-24<br>IPv6: 2025-09-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.648MiB (9.068MB) – 433,049 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eda4d1f4697613bd58fac5adf413d88c<br>SHA1: 0d24735d5a9890e41f64738588fa88e1fda895f5<br>SHA256: 2f45fb8a4a46d500ba3f1286c1e84167cdb2a1b8af767b8f5d09acbbc2f7b1d6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.295MiB (7.650MB) – 110,983 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78368133e3b6760b746bdd5a64ed2b57<br>SHA1: 18b9bcbd46df906cdf765e7e5286ac5f3222c204<br>SHA256: 74041468d6e3c22f7b2460ea45a1b4345db147caad3b2ad8d89f332d0e975b4f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-09-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.12MiB (12.71MB) – 606,957 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1efe91fbb7e80b591b8e48e3ae0ad13c<br>SHA1: 86687021d2b158eba8626a036d8a6481abc8a8a4<br>SHA256: 66b9fb137effa80d72ca287686398db3c908e6729e149a6e7d87607e779c7dc4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>62.50MiB (65.54MB) – 949,859 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55f2de6a151849364e6db0a7a65cfd71<br>SHA1: 1c18b858a4f783dd99388898c8e47a97861661b5<br>SHA256: 7e46340be70da03ef32887e559989cd7448d3dcf1f26d07c4b292e12c208d73a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.825MiB (7.157MB) – 341,824 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dae1f431e9d10a462dae84888365884<br>SHA1: c0cc78c9aa347b8d712850c57537fc0dc50f1dfd<br>SHA256: 3f57c286e145770c2ac0d5d3c14088a919db312a222bfef2cb85941399367b2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.93MB) – 245,375 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f7e3a8bff7f09ee7cfd621ef044564b<br>SHA1: feacd88a985ae6ef5d668ffcf375eefeed7948b4<br>SHA256: f554d05a841ea0162859a713eecebb3fb0dc814ea2d39b91150dd45627c31fed</pre></details></small> |
| | | Full Location | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (217.0MB) – 3,624,799 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7154efa553f5c77576cadbc5c42ec9c<br>SHA1: b63ba0a183e94bf6cd1aa8a15db942b52d55841e<br>SHA256: 00286d8f1fc1f8f801a25f123213615fc637aa494c49fb2537047bdab4b1aaed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>448.8MiB (470.6MB) – 4,362,462 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7375867bcf97ba785ec1fa3d092fb0ae<br>SHA1: 37a209470da0930c2308178d77c0c1cac376d849<br>SHA256: df10547da1aed72a27d58d5fbd860b66dc9bfc40df34c5dcca2b7da7fdf24ca0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.185MiB (5.437MB) – 259,491 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50d719d1853e86e8da56334658c35eba<br>SHA1: f811bb310275e7b7653fa90e869cf112fe526acc<br>SHA256: bcbf902929f7d249538703a8dbbcc64d8fae4900531479cf0e3063367391f946</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.57MiB (23.67MB) – 343,010 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff677ddad3772ab36197d2ef84bf42e7<br>SHA1: 8be3a4e0ee14af3d087f70294904f7aa883b6743<br>SHA256: 0f288add4994bc16d4d6387a5818de57f3def88cb259fb8fe4a8f6b507e4c820</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.4MB) – 2,949,463 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ec6ef92605faf0c8ed3176f371a4f89<br>SHA1: cd21e0629e442168ad794701d10639489e2d7e3c<br>SHA256: 3470fc0e8a3432aae0bb7caf8d995d20c8043b2486e3fbc23fd209fe4a11d530</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.9MiB (308.1MB) – 2,846,052 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8446667c1feaa357c25104ee40c7db47<br>SHA1: 1631c4d82f37dbaa7ece00c99dde97aa5483e6ea<br>SHA256: a265bc2be67ada5c65a6d3631fcbea01cc1272b1b51f27002bc5f3bffbf061ed</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-09-23<br>IPv6: 2025-09-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.70MiB (13.31MB) – 635,444 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad5cb1c724eb3f5f8c77730e609a4927<br>SHA1: 34fd8526e0f8f665260edfb813ac422822921633<br>SHA256: e8bf47d2df1c8befc8c0b217a49f6b546e56803578795e489f0b7750c5fae502</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.05MiB (45.14MB) – 654,255 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e87704ad688165adf8d34951d6af5f7c<br>SHA1: 795be4fc5bdeaab6ab649657c0d3cc313d2acd80<br>SHA256: d4b140ffbc29821c68876b3a1755cf213b40bcc23cab2be6b7296948bf1cdc98</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-09-23<br>IPv6: 2025-09-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>176.0MiB (184.6MB) – 3,468,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3157aef9463495701003ba791e49707<br>SHA1: f99ea23a5538b8859b1183606387c7ef380a141e<br>SHA256: 7b9ab32df721688225a56bbf325bcfd3e4906b7d3f8d999593a99aadb3e2f1f3</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>187.1MiB (196.2MB) – 3,468,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e70310a4b616eedd9105b38c5c83c9e<br>SHA1: 155860848962bd5c59a593b80b3dd31f508d1c0e<br>SHA256: 77ce5167361ad0612bea41f0ea432368815e7e5c7ddf71efcdaff4e81a3163a8</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>175.0MiB (183.5MB) – 3,468,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 593ad1d6f934edb4d8db465128c70d38<br>SHA1: 3e74de567b37d4da52083c40c863baae6f0f060b<br>SHA256: 3ebcd80ecd3caa7bbb81bebbaa0f2eddbd9650c448625860a7d694cc435c64ce</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>177.8MiB (186.4MB) – 3,468,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 652d7961c96def44e387e384ac998d37<br>SHA1: ae659908574ab75d06ba2fa9e4840a35d77b92df<br>SHA256: d119c7082b6334a1df06683b46e9b22017e4497dbb05d1abd407a1e97aa670df</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>223.0MiB (233.8MB) – 3,468,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d34c366a0ebcc096a935dfd1c735b8ee<br>SHA1: f8f9488036a5861990079f49f71a883394071866<br>SHA256: cb5a61758c58359c474d373142d5a31baa590f26a3cf7b6fd5b51ba14999fbd9</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>174.7MiB (183.2MB) – 3,468,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6f7d0eee7c471aa6f1fa41b4d09649c<br>SHA1: 889b2cff8f812158cc2b891651a2d95e1ff8f9c1<br>SHA256: 8e733687950a5cf9a9c82f799c716827a614293b56d05e665200d86861eebeec</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>216.7MiB (227.2MB) – 3,468,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17262e47362de8fa9f98cd81181b54f7<br>SHA1: ada9126647468c27e1b9e2fac23f73c8d18d66e2<br>SHA256: fb21633152ccf571b9abda7b783bdb8b122a2faa75bc6aa4ead33e9a2598316a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>182.1MiB (190.9MB) – 3,468,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8abd637215a8172e58b7d6abcd2b93f<br>SHA1: 44aaac5d4b4d5f6f68680fbcff0ec0bcfc1be576<br>SHA256: c8f489d855d6ef0f23a2eaf099dc6d94ed5ccb4cbe88fb2803197d7da2109064</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>178.0MiB (186.7MB) – 1,887,680 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f2b413d5f10a7785848fcde9b3ee314<br>SHA1: 4a6be6f03ae535a17c6f223560bfb8c8557cd8cd<br>SHA256: 247c8a5db11022cbbca07af1b1aabaac685c1c90c6d1095f97a4ccac353a6ae9</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.2MiB (191.1MB) – 1,887,680 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61d38e98e0576d7053a4b9947c5016b4<br>SHA1: 632a320cc13aa22ab9f241c47420ec3930493cc6<br>SHA256: 402acbcdf288f87b135c23b20d42ad5e85ec4c304334b8de2c7ad959f78aeafd</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.1MiB (184.7MB) – 1,887,680 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 644e0cf8c88f8a4aceaf5cf7b5e0664d<br>SHA1: 2191d636908d0890b63eef00703453c9765cd209<br>SHA256: e1f7851387f4c8b269c3222041a1877658c55f55f3ba29a170394f7cd915b6bd</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>176.4MiB (185.0MB) – 1,887,680 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 464ac45a0c17548d8ee6ca32371f21e9<br>SHA1: c2a1aae7d5d781b21dab2fdaffdbbbe919f6e242<br>SHA256: 80528d9a309c6c2f0a7050a6d2b2e282fc845e169482f4ed1f6ecc979d46ac5c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.5MiB (205.0MB) – 1,887,680 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99446c862f61e01f0224e9e027e56a96<br>SHA1: ba319c03a1320bd3717ca627d68d2dc8d6bd6a88<br>SHA256: c62c789e7581ee98bed5a7f21a3d759cf128a7967bbb568008f2f3f58f767b8c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>175.9MiB (184.4MB) – 1,887,680 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4bdf221c58a01977f6cfadf1c39d982c<br>SHA1: c99ca8b68dc19103c73b186a2d7a71bf479214c8<br>SHA256: e7285308a34e7097566376eeb2db655ef94c338611192ce59932423d27b1ea1d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.3MiB (205.8MB) – 1,887,680 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c369c5d0826a7a350ec43ddc319051ea<br>SHA1: af635d767294f3346a81855d7df29c08cb782a0f<br>SHA256: 56adc2bb49e237fced9e279d068eae0b5d1ff65b9b444c861fef2555d000f80a</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>180.0MiB (188.8MB) – 1,887,680 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8da9e5de4b67f26d9e5087be21cc6e02<br>SHA1: 5a9492448cd97c254fc8c65f0835d147a635cb7e<br>SHA256: 127923c5160f2ade15a83f20ecf9c05e2c793cdff56a93420052947c18521d42</pre></details></small> |


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
