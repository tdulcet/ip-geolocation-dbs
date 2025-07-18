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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-18<br>IPv6: 2025-07-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.317MiB (6.624MB) – 316,366 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90afe4c5382f3186abb95349623870ee<br>SHA1: 2a9e04fc7a70e5ae26f8ca091ed49a33d411f87f<br>SHA256: 16976a1c12d7edd00f92fc0fa7c21dd022dfa6dd1470efbaec9dfa069d58f617</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.37MiB (12.97MB) – 187,946 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 444be2d9e7f86e2f23d5fabe4df7d291<br>SHA1: 833dfdbb0f8710b5bd2f85ca9f7f77b2cd8db93d<br>SHA256: 215fcee261d4278c0f9fdb14ec5763e9074aaa4450c1fcf1f3fbc8e50764340b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.82MiB (12.39MB) – 591,511 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ade7189babd648cec996147e71c55b5b<br>SHA1: 6a0c17b025999d05079fc56817ec92b681156301<br>SHA256: a4b51f8ae5f166975026043214f789c0967732154a84632c06454ade019039ce</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>84.39MiB (88.49MB) – 1,282,457 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 239d46bebe147b35f9a18a3b2a78e5dc<br>SHA1: f6c131b0714f6e3c1ccf55d24369e19ca4f34a5f<br>SHA256: 4d2c75f6e30d09a319ef9de88bf0a41d93351b4a1c4d0436db7ed709bf5fc495</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-18<br>IPv6: 2025-07-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.068MiB (5.314MB) – 253,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ddf95be39b948ff8a1f5f72a989f3db<br>SHA1: 53e521e70cdc7bf139a71019e836b80590d710b8<br>SHA256: 50c6f2769387e3ee7cedf43b469b7ba544e29e43852d8c3fccd14dbf39e376a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.78MiB (22.84MB) – 330,989 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43bd9e1f0cc46c204def11cc25411429<br>SHA1: bb110aabf0613079fa6821963cb9072ee8a672f5<br>SHA256: ef3129675278c4750cafd639f31a9a899cbc6468108504cf55d1a6439f90199f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-18<br>IPv6: 2025-07-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.2MiB (176.3MB) – 2,916,495 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec46eb0d6770f3a4934f80b9ba8b43ce<br>SHA1: f00f5138d48a37c35fcf9f170e21939324735351<br>SHA256: 16a49d4f2d09a24369e498fa18c855ad30e4610d4fb1424acea4ea9ccec6048c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>279.1MiB (292.7MB) – 2,704,923 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dac800448bd3a785c553531ef23da1b6<br>SHA1: aaef79ba06d4297b621a7688cc2224cb694528a0<br>SHA256: 6c59b673d7391b858e46d6527a0bce731c26713b44246050076e424d61a9f656</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-17<br>IPv6: 2025-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.56MiB (13.18MB) – 628,993 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6d17ae5e502c70617e05f152d098c7c<br>SHA1: 2290f205f1923ee6b5512ec415542f781565b85a<br>SHA256: 005824dbbf55cad7c6c3a7c397106083c074dd42cd6e2b83c438979d1648e76d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.46MiB (44.52MB) – 645,223 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37dd99a7ad7e37c192d1478332cd9cda<br>SHA1: 01e93683397ce9ee854c8bc16e1dd9adc561e85c<br>SHA256: b1bb0c48f477f35472bd2fbc79f3b65a170d23146bd7db127b1dfdf1df8945c2</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-17<br>IPv6: 2025-07-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.1MiB (182.6MB) – 3,434,747 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e43627cfc58fc238054323249caa2ddd<br>SHA1: b652440b224cca230a3ab9a75e36c8db723d7ac7<br>SHA256: 923b4be7cd5ba39b1ab05fbc5b825bef42b01d33d42ab708acd9b108b423cd7b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.0MiB (194.0MB) – 3,434,747 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52f8a3c04821b09281a853d793f7c142<br>SHA1: c523534edafa647321889948bbd3db8115e92754<br>SHA256: a9635698858f49475a936759b3169e7cee9c93a7fce1d7122332a003b616a6ed</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>173.3MiB (181.8MB) – 3,434,747 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6dab3f6471326d9adc5c48246d71b3aa<br>SHA1: e30dafd0657055331e377a09ba551d51651a7522<br>SHA256: c0fcf587b9c6f5e776561a477d6685bceb1e268e6f02a14bf6c9562df575c8f1</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.8MiB (184.4MB) – 3,434,747 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a055f7b1a8c4316790a25a8d5d0b92d<br>SHA1: f573b9614df5d0db5e92a57dfe8634d6f03a5c77<br>SHA256: 9f11bfed66fa24fe8b96871c2c02b62498be3be06af7e1dbd4cb840b44a14599</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.5MiB (231.2MB) – 3,434,747 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccda07a98c3635f48944a06be4655a48<br>SHA1: 1ed241ceb7777281d095d74de6054b7246b66941<br>SHA256: 094117da9f1c2d59d41a3897da6808cbf9f15baaef8a10ccceb23aada1f92d31</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,434,747 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cf76e9d578064e1c2dd3dd350308ed1<br>SHA1: 91cfbd9654b411f155981ade08dabc48f023c6e7<br>SHA256: 4683221cc9e24e1c17d7365dabc8a81a83e136decfee725ef521ed84d60592a1</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>214.3MiB (224.7MB) – 3,434,747 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70483c03552e3af7163b6179c4f41704<br>SHA1: 56b07ac82cede18194a84ced6fe4e1d0ecb08807<br>SHA256: bb676fabfdc9290463d234e7b4920991de221e4042ba7e0c7e64bf464278cec8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>180.2MiB (188.9MB) – 3,434,747 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 755e612126d6f44fcab212239c7486c0<br>SHA1: a4f32da2ac3ffee2acb9077f97395aadee41da23<br>SHA256: 0038d4c70371e686e81504d155058c2b35b5f3f23f6fa0b9e841c475e1f6f8b6</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>178.5MiB (187.2MB) – 1,895,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a0ad31f0cf1e2276e5b2f9489a1ee1<br>SHA1: d0c8aeb717794ec2ccc0439080c49728cf30a940<br>SHA256: 47d4fc7f29d8488c33751894e287cf1f5d807eb9ad9da1a928529a5c5d64553a</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.5MiB (191.4MB) – 1,895,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 733da002eee94c59e7d1f814e0d75f92<br>SHA1: 3cf6a2eb8f337841dabfa5ea619a55990cb87027<br>SHA256: a5b19ba1092f93f33a5c84553451278eb81415aa8d200187ed3a378ae815983c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.7MiB (185.3MB) – 1,895,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b4cdec96be3a8e88d896db68b10ddca<br>SHA1: bedd2449d5af2092712833b305510ed872a630a3<br>SHA256: 7c5f3d4b931af6fb6df02aca69881fef060c7ac55a0079cc78bb9d998deeac22</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,895,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0e58d1353bc9b1d78e41d8b48b39ff5<br>SHA1: 1f80ef12e8b7b1553ad099e69a24ad4799b61169<br>SHA256: f1d5bf333da50b70d6899cb0daada1b116ebd491a5eaf615759498a08664778f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.8MiB (205.3MB) – 1,895,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90ffd34ff7da0c90c90d6f3025eaf6d0<br>SHA1: 6d9519db7be6027bfd2c283ce9ed59aa743cd3d0<br>SHA256: 35f0f57a8988a4e7aa23e2bbd42a31b58b4eaeffdc489195758c13c4e880d18a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>176.4MiB (185.0MB) – 1,895,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 676e82e9e1c2665ce94d47de0caa1cfa<br>SHA1: 3f75105ec36e1c1b9067c9752debfd9454f53d87<br>SHA256: e3bcb8452a6fc58155ceebd737b0627caff5cae4a5f020c22082a107fa41a20d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.5MiB (206.1MB) – 1,895,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55958e0b68c8fb092b1d91155c345516<br>SHA1: 20f5606580fff515cc7b2c1fb4e1efeab835acba<br>SHA256: 195dca4cda69e04ef06f7f5430538cf315330484bc02b9406b7152aa609702f4</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>180.5MiB (189.3MB) – 1,895,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d89210d094d68179d71a41b01f5347c<br>SHA1: 985a0871659e0c3ff4b623fc907ad15e839bec04<br>SHA256: ea8050641696f4d996909003dcc6abc1dda46efe60a9c32ad905238e9b87754a</pre></details></small> |


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
