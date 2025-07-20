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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-20<br>IPv6: 2025-07-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.323MiB (6.630MB) – 316,636 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eca3a0887f1d9f4fbe29e07ff741adf<br>SHA1: 1d744516363423c5bd0c40773c598f6d83af4827<br>SHA256: 1805971c6b4a25fbac4d930875a67e2f162df62039d14b7f2a51f8ce7da33036</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.37MiB (12.97MB) – 188,014 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ebc86e7773823c379635dff7b5f3a67c<br>SHA1: 141af97c237c992448b1333d53bf2530b464bf1b<br>SHA256: be0e766d13805ef22aa603b5b7654fb7c0191eaa9519269ab630184405246b89</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.82MiB (12.39MB) – 591,535 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56192d55ee032914301a6aac293af717<br>SHA1: d95ee14856b716585bf36de44162e68a1a39c60e<br>SHA256: 8d7aaa742dd0644dbee005c7943acec48cf6b4178a6ab4c50dd6c5f1d229f344</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>84.40MiB (88.50MB) – 1,282,585 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62b5f542127444fc1664108b0075c88c<br>SHA1: 291cfbc1461e81875cc1699369b2c87182023ca8<br>SHA256: 29e77a8ddee98c1d17b6e260854fd2c39f0d2aeab292336063b8a607ffb2d779</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-20<br>IPv6: 2025-07-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.068MiB (5.314MB) – 253,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ddf95be39b948ff8a1f5f72a989f3db<br>SHA1: 53e521e70cdc7bf139a71019e836b80590d710b8<br>SHA256: 50c6f2769387e3ee7cedf43b469b7ba544e29e43852d8c3fccd14dbf39e376a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.78MiB (22.84MB) – 330,989 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43bd9e1f0cc46c204def11cc25411429<br>SHA1: bb110aabf0613079fa6821963cb9072ee8a672f5<br>SHA256: ef3129675278c4750cafd639f31a9a899cbc6468108504cf55d1a6439f90199f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-20<br>IPv6: 2025-07-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.2MiB (176.3MB) – 2,916,495 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec46eb0d6770f3a4934f80b9ba8b43ce<br>SHA1: f00f5138d48a37c35fcf9f170e21939324735351<br>SHA256: 16a49d4f2d09a24369e498fa18c855ad30e4610d4fb1424acea4ea9ccec6048c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>279.1MiB (292.7MB) – 2,704,923 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dac800448bd3a785c553531ef23da1b6<br>SHA1: aaef79ba06d4297b621a7688cc2224cb694528a0<br>SHA256: 6c59b673d7391b858e46d6527a0bce731c26713b44246050076e424d61a9f656</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-18<br>IPv6: 2025-07-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.57MiB (13.18MB) – 629,329 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb444e67613c650e151c17c7400f7a27<br>SHA1: d095fbdfc6a09bdd582cd0b8f0f5eb36d59c3ef8<br>SHA256: 74655d6b0bbdd7f79c7114fda579fe6fb6b558688eea8e763472cc94970f2d10</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.49MiB (44.55MB) – 645,670 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f207f304d89f94ea8e492e907e1cfea<br>SHA1: d711b11ad2185f266877606ca643164e6032e3d2<br>SHA256: fcd30853ccebd5a231a30775780c640ec09b20a8641173f2346484261f687856</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-18<br>IPv6: 2025-07-18 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.2MiB (182.7MB) – 3,435,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec44b0896b097ef60d42bea08ce112e<br>SHA1: 681dc62526ecac51eea365ea89f4a13326418a19<br>SHA256: 8fd41f2f8d28999102c9d86eb9284d261095577e5de1e0b556ff541589a109cd</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.1MiB (194.1MB) – 3,435,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 094472e28f723a5a9c4a7d47f473f18c<br>SHA1: bd93ea03b22a80761b939f75735d1da09cf27879<br>SHA256: 7268c3cad610db4a1f44c844d308ba421337a2f23e10be349a3b9aca5c49d2ce</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>173.4MiB (181.8MB) – 3,435,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af88d817cb33c75a55260dffe474bbf1<br>SHA1: 2316a2fb3e064a53d578df25b6610977899ffc49<br>SHA256: 43cf088bddfe32e057b65b04e73783db52b364ef116ed82d3d136bc89a678282</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.9MiB (184.4MB) – 3,435,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a30116d10b19c67da2eb21028383011<br>SHA1: 12de7fd345b1051a484e3168b959a9ca92fb6fa8<br>SHA256: df8625cc3327105899f77a2fe9da836b0e1730a5a0de816656b020c24e10378b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.5MiB (231.3MB) – 3,435,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2c2049d4f5f160abd3654ec48b3a15b<br>SHA1: db1c70abea81388d93e1b9883d42e81f64c458f7<br>SHA256: b59e1046c992bbac8450205d535e3110637915ee0f0a65d7d6ab1a20fb3033c1</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,435,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2cacc299346c59112a549848c325260c<br>SHA1: c78002cfd19303570c9404b5285ad4bb479f834c<br>SHA256: 38c7e7b5d334f5837d67995e9f5f06ef4d1587d991b26c01b8d60dd2748e13e8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>214.3MiB (224.7MB) – 3,435,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 331553f670a68b22e2c59545c325e8a7<br>SHA1: 30af231e71f8ab660a17aa264c8e6a352274893d<br>SHA256: cca406182c61ff32a3122456401322afb97803d7a75a7260537da683afe05027</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>180.2MiB (189.0MB) – 3,435,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a15f1d5d5feac257319e34af87988daa<br>SHA1: 3b8ed7677194ea87213c811ec98a8734d4495b44<br>SHA256: 9748ad20ca42b1a7e0b03f09b453db34a24de7b6363ff422f7d267b03234eb6f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>178.6MiB (187.3MB) – 1,896,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 269f7a82978f226284b68ba168c524cf<br>SHA1: 58700ce505bf16e1a11f14e2636f06151c110fb6<br>SHA256: c2c0e853a374cc3a16fdd1223b637536d4b1966cc610290a9b1e21beae9abea3</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.6MiB (191.5MB) – 1,896,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b829763d03e0502450ef2a72bc493ca<br>SHA1: 589543551d2bd2e680e70fb5d161a4dc85f27f62<br>SHA256: 5997e91857d74b74e895b014c9afe9a7e13955fbd70077e0f7f53c8b4c67b929</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.8MiB (185.4MB) – 1,896,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f2d7a084adb05cd564d2578b94e0b7c<br>SHA1: ab546ee183829eeb10285dabbe40be1211ef2e61<br>SHA256: cf769db5ccbc0986eb6ac365e8d1355d7b92bb6dee3b6143e1e5a19e15370315</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>177.0MiB (185.6MB) – 1,896,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5367530d50685702f3c2eaed6f8622e3<br>SHA1: 44a01c8c0c77090b897ae0f8890347026d4c9b9f<br>SHA256: 7cd4980123e990eb729e8cd5555334a3272e9885712725a610836b66118d16e4</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.9MiB (205.4MB) – 1,896,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d41f8aaf32c86caffe7435c97f92d22<br>SHA1: 312bbac2d303e3af59c61444ecdfa81ea91b3aca<br>SHA256: fb9a5e39535a90e165f1125b392989e2df543f4e5744ed04b5689cdabcb80b8a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>176.5MiB (185.1MB) – 1,896,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25f94f0fca51f456d6b966e77219d978<br>SHA1: f09880fb4c1f265802ccdb3477f2664857a99b34<br>SHA256: 98950efa97223eb323d15c710ec348d1685c7d82a3c9144edb556bcb926947fd</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.6MiB (206.2MB) – 1,896,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 254988667ab401a49fe81796f471ebb3<br>SHA1: e6f855fd5365d8952a976694fed8405ecba7e51b<br>SHA256: 544cb21082d36e083ae390ea85be8edc7cfb4cc7ded83540ed29a294d4bf7ae9</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>180.6MiB (189.4MB) – 1,896,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc8999b0e2e8156f8c63d033edc3b429<br>SHA1: 40afdae49478e65ba48f2e5f6e00419e21a2b778<br>SHA256: d11d94b97c1e17232dc396b144c25ef7394fda340d0528785bd7c375772949be</pre></details></small> |


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
