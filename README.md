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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-08<br>IPv6: 2025-12-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.396MiB (6.707MB) – 320,279 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b3677874a5449fe58166dafbb9ed15d<br>SHA1: 8659b6df7d6b0f977ee9b370cb4c5b5c3effa2c5<br>SHA256: 3191f4c29516fcb4d5e13687161c829974851bb7960038846fc2fc1882698e33</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.16MiB (15.90MB) – 230,444 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b63c3be74fa92d209e2fb49e5dd3bf99<br>SHA1: 93f26ef79ee1b7c7f589e522658c7f5e5f8d558f<br>SHA256: 6234b19e500521ab5e96b4f5140594111af68b82a9399d5158771dad581d5d87</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-08<br>IPv6: 2025-12-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.789MiB (9.216MB) – 440,096 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d32ba958615b0530233916eec0163ce<br>SHA1: dda7cc9765fdb1ecf90ebdb23adb7e3e826c0693<br>SHA256: 00ef8bf427a8c2c58157dbc3d4f401d32cd7de588afbcb59080b35bd9d90c7c9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.538MiB (7.904MB) – 114,672 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e44f61b039a12c0e49690ed8d500788<br>SHA1: 30f74ef13a78542b985d487920d8ce2bc7133519<br>SHA256: 2e4670dc37cfb7828ace0aabe0c980003c1797ebe2644389ac0d77651211f388</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.16MiB (12.75MB) – 608,741 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4615cc5e7d95b6ceb6cf2106ea0a653d<br>SHA1: 01b479815cf17ee6f379f6f185a59b5b756ceb65<br>SHA256: 4affc9dc71fc167da688c284c473305132b8472e65e2c019a58a1b42734fd8fa</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>95.68MiB (100.3MB) – 1,454,046 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 326fb60355b8e194202c7f6569a8d0d6<br>SHA1: b336be84bcaa8740bb6fa16040f090c962bceb7f<br>SHA256: f7216131bba0a334594d24c138a7bbde31d0a8910ea27cb0948ddeaec5a3dd8d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.367MiB (5.628MB) – 269,273 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f62178d410cf3bce771f73d48e43faa<br>SHA1: f7860e76e84e2e025ff86a4e5640a5e924783fe0<br>SHA256: c1072a02c991020475c91925325c135d490b5d243b47ddaaf047c7cdef840cb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>20.32MiB (21.31MB) – 308,850 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 594439a3c0811d183bfe5550c4fa8326<br>SHA1: 2cdad07afa5d0806f1da62dff5def384ca6b52c2<br>SHA256: 86d5eca80b132381a0466a85510652d17f94597f2ba2f6e7a930843309468a04</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.3MiB (179.7MB) – 2,965,067 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a5854fc5ad699cdf214288eb10b070<br>SHA1: 02297fb66300226ae67a1dcf129bca4e4e77ed1b<br>SHA256: 2eafbe9230ee8d23f99e769b27da134fac2c62d6a74beda67c278e8823866eb7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>277.7MiB (291.2MB) – 2,688,825 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7579bd752fa4e59ed8578642ac57a02e<br>SHA1: dc5caed7e7217beea7fbec082ae0651c0f13d1b6<br>SHA256: 0d03be0ad75f92ed0fe8301ab4717341f744711cd9bce0dd880a1632aee11d8d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-05<br>IPv6: 2025-12-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.41MiB (13.02MB) – 621,341 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9511cfa782164ad8a5b4be82f55e3740<br>SHA1: 3d182e2d2ae33ec2b7215109bea7943d12718bc2<br>SHA256: 2fd5583cb316face3a51dcbd1e21fcdc20a44d0c316abe077f0a47ea8c1126ee</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.55MiB (44.61MB) – 646,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74b30fffc9d979ba4713ff698c658dfa<br>SHA1: 103e2fdf31bd9b70884caa5810775a0c44808fab<br>SHA256: 3447ee635ad7d2e60fac9393d9a72e7d557e462b1e6fe0475a8799ba3b9b092b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-05<br>IPv6: 2025-12-05 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.1MiB (187.8MB) – 3,538,362 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f85cb46aa33c7433652409eed0e0639<br>SHA1: ed9bd69e81b7e751f0ee865c3d35bc51fef1e4e9<br>SHA256: 35b48b0c2ce7fd4cd2dabf16888422b9dcad7abeff3eaef62805389511cd40b3</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.3MiB (199.6MB) – 3,538,362 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d572bef49a781bf664e8355d3b2dd299<br>SHA1: b838c809a076d6e22caa28f5d1126f2e27bb1030<br>SHA256: 3b3aa0bda4f8ccc2334aa9fe65d4657246e5a75a59f5b7db9be0fb95ea5d423c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.2MiB (186.9MB) – 3,538,362 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37f7a75261d0447dfaf0cb4f80c952da<br>SHA1: 391b6c1f5f75906d0b1be1e1ef3184e2930ad059<br>SHA256: 90e62961d91c941e7a82989fb83bac4de9e028a036b75d33a4876247481ce9dc</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.0MiB (189.8MB) – 3,538,362 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2eef86e2abe61f2a8ecc73501c256331<br>SHA1: 6cb5bf87797af22ea9fe75ec897a0efe9569e08e<br>SHA256: 14ba28cc6e6f087745163578357ceb7a1b118153dca37d3e90ae52a22c1e5632</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>226.4MiB (237.4MB) – 3,538,362 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 818d3cb2b8b27a5b58c32c686288431a<br>SHA1: 5e1b6dd6045322fa3c7384790f7a6ca04723e2fb<br>SHA256: 20b1dd479ba4c638d8a23cfe69a6c8a2773509ed82c22179a787e2ba1982074f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.9MiB (186.5MB) – 3,538,362 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b0f24e635c8af1bda1e2b38faa6b8ca<br>SHA1: 9ced3bfa0aebe454c06515a2868d02bc2f5a31a9<br>SHA256: bf10eafa20dcb4e3ee125c72578790b666618f92a947547c7bec177438368efd</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.1MiB (230.8MB) – 3,538,362 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3b95fb325415e85ae3ba121f3cb5fab<br>SHA1: 291dd92371bb46ee9236b23e76588a3bc705ce14<br>SHA256: b30ab07ee940da67c365f614cd759768e8b797c9b8eeadf54d4f8ebc6c45f79f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.0MiB (194.0MB) – 3,538,362 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21a021cdf6021520432503d384406cee<br>SHA1: 5d5896d7b1400974e8c2847c425073c60948a31a<br>SHA256: 755cd29011d8020b3a92e9f64c0d83729611271e61c4cff42525502fb819fe6e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>180.7MiB (189.5MB) – 1,905,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2a4e10d79768a4c1330ff26a5ce5ba4<br>SHA1: 1298b53908f056164e353e5fa694f6f902b96cdf<br>SHA256: 723c093027f499dad9a9595c99766b68d6234737662313b319042f3c3c3afe62</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>185.0MiB (194.0MB) – 1,905,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02e807b79a4e24719942baa8198d6cad<br>SHA1: df666061043a88928772ca81ebf3d2a8f5edf2d9<br>SHA256: bd8c06838ad88178b83d204bff6ca337662c9544db5017f16d0761d7880c4854</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>178.5MiB (187.2MB) – 1,905,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2abb91ff07ad3298a3268fd2e75cf00<br>SHA1: 4123817961f64eb02ac662c824b4ef592c84edbe<br>SHA256: 1cfac5b86f2824d9950fc021cf82654088d2f09d45dd546ea3ab8a79f646a343</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>179.3MiB (188.0MB) – 1,905,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f11ac3b19d29b566f2848b49d182fac9<br>SHA1: e80c356b5f7c0d23d329dcbf3559e790c6a443a9<br>SHA256: 6927eae2599b5ea0f37da04a6fce041901fd10ee920f2e565de789e09e70753c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>198.7MiB (208.3MB) – 1,905,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6ced21772cc288ad6449a78a5d5124d<br>SHA1: 696f343974df299d4146f3ecdbbdeadb5fb0ed9e<br>SHA256: 19150961167098a6cfa715a765acc97981712eabaa154e4bb2c513d835d1b862</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>178.2MiB (186.9MB) – 1,905,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 226a6497d2705275de1122bd298508e0<br>SHA1: 55fbcc9b49c53ba4bf652ca76ac1ab824711b696<br>SHA256: 567c515847ebf5a4146c68a1c2bb921fc615abb35b7327f84c59881f2ff51f65</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>198.7MiB (208.3MB) – 1,905,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74bf75dbab84b79c96fb0e5a1eaa355a<br>SHA1: 717dcfd932af9eeef350f1a95412af67535dc690<br>SHA256: be5a04928711a9646c99077d475f20f51c44adead4e276433d416121d54cbdfe</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>181.6MiB (190.4MB) – 1,905,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11cc341f5ef8ced5783e7bbc5d693817<br>SHA1: f38de1c135eaf8a805ec78b00471402a6041cf81<br>SHA256: 74b84442bd57574e88f305db0e34c77e6ff6dc91ca84959934ab8cddf2f03e17</pre></details></small> |


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
