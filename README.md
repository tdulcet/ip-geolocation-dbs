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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-23<br>IPv6: 2025-07-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.123MiB (6.420MB) – 306,588 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd97835c511f9092fde23370a94207c3<br>SHA1: 8f4bfd9f8b2ba1201049813725a14d1817614bd7<br>SHA256: 5858fe2c73a6c00d86f93db301c0c6ae8c1cd52c2d9971a3d6d15c03c2ccd931</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.14MiB (10.63MB) – 154,080 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c9e843c7a2f771a7c46e93b8814cf4b<br>SHA1: a34d557331ae48950d403b2443b6f990cea41f4f<br>SHA256: a587ba418bd0d7747b6510471a066611ef8fc741eb6a9839c58eaa15d5e09c0e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.84MiB (12.42MB) – 592,847 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 798aba39026507a78902dbf4c8d9ebdd<br>SHA1: 679c3f41c48a45b9443021172a52a0444392006d<br>SHA256: a4db1437461d87764b4ef29520559d7e9bb864b5245ff46e33a8ced95d1311cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>126.3MiB (132.4MB) – 1,919,042 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2691118726969fc163492d3bd7046a36<br>SHA1: 4f6904731e7bec45535b0235545913e9b624a25a<br>SHA256: f9969f5eb1f31500d83f1768195a189e379a51a3df222e5fea9c3a2a5dc8ef8c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-23<br>IPv6: 2025-07-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.068MiB (5.314MB) – 253,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ddf95be39b948ff8a1f5f72a989f3db<br>SHA1: 53e521e70cdc7bf139a71019e836b80590d710b8<br>SHA256: 50c6f2769387e3ee7cedf43b469b7ba544e29e43852d8c3fccd14dbf39e376a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.78MiB (22.84MB) – 330,989 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43bd9e1f0cc46c204def11cc25411429<br>SHA1: bb110aabf0613079fa6821963cb9072ee8a672f5<br>SHA256: ef3129675278c4750cafd639f31a9a899cbc6468108504cf55d1a6439f90199f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-23<br>IPv6: 2025-07-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.2MiB (176.3MB) – 2,916,495 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec46eb0d6770f3a4934f80b9ba8b43ce<br>SHA1: f00f5138d48a37c35fcf9f170e21939324735351<br>SHA256: 16a49d4f2d09a24369e498fa18c855ad30e4610d4fb1424acea4ea9ccec6048c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>279.1MiB (292.7MB) – 2,704,923 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dac800448bd3a785c553531ef23da1b6<br>SHA1: aaef79ba06d4297b621a7688cc2224cb694528a0<br>SHA256: 6c59b673d7391b858e46d6527a0bce731c26713b44246050076e424d61a9f656</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-22<br>IPv6: 2025-07-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.58MiB (13.19MB) – 629,875 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d15f5ae9dfca6bc47afde475c18908d<br>SHA1: c6dc97091516b055f2fe310c2cabb754f36c813f<br>SHA256: dc12720fa1b824b12b80c6425362b96ef03a1e9c1c719147b77a8a5d3a83aa04</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.53MiB (44.59MB) – 646,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2993c30775e2bd2b5805b90205655d42<br>SHA1: a53533e0bf3c376f9952fb28c683afdc615e6c24<br>SHA256: 4f42b83839113b5beb1008548a83732beca3d25f19e5f42e0453a59edce58859</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-22<br>IPv6: 2025-07-22 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.6MiB (182.0MB) – 3,424,830 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a500a1fc6cbcc73ffa314d372d7e466f<br>SHA1: 3247173f2f01ffac506cfe8df4f1e5e47c68f1e1<br>SHA256: d9a8575e260df9b0bd2c68b1fabc073342104c3fc2d55a1a4d147e889472c372</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.4MiB (193.4MB) – 3,424,830 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b28eb9acad88b093b018bb91039188<br>SHA1: 5756b73dcbbec0dcf05c6f1fac8c06ef06311783<br>SHA256: 63cebf8f34219d3e27d30cc81a7223bc49fb5e09522ddc2323bfcc014fc2b884</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.8MiB (181.2MB) – 3,424,830 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 340f3f663c913809f4d74039c8051804<br>SHA1: 5a501377199a2bd8cc111d9a6eebfd3ecc3e296d<br>SHA256: 2057cea44b0cc900b7e6afa729aee021a2ea2187c12c1604b1a4895a7895065b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.3MiB (183.8MB) – 3,424,830 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5d3e67fc1203702ccb320ec574bee47<br>SHA1: 70676fe071626161dd73ed9d80efd9f60d8edcf6<br>SHA256: b6c512b228c97fd6f942ffbe10123ba6e132ff0d69e9c76f7f62c38af7784ad9</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.7MiB (230.4MB) – 3,424,830 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db2258717226a9a37b621211792e5386<br>SHA1: a2226354a682fec4e8068765d1412cce27da9287<br>SHA256: f725ade63104da339259fb507891b2dd43f4b714dc884e2d8a390ce22451c1d7</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.3MiB (180.7MB) – 3,424,830 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d47513e3640fcd7dc18a4f70aba8168<br>SHA1: 0e4f077fb30daacbecc841ddd05771534323f4fb<br>SHA256: d67566afc05ba11d1ea53e39452ebf5bc76b2a693cd3638093317c6356065d2e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.5MiB (223.9MB) – 3,424,830 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 608fc48e49ab6efb3050e96797551d53<br>SHA1: 9cbed52ca90d07a571f0ab78e4e59a40479b58b9<br>SHA256: 599fd458d64bd59cc92fee2eb91066ee54fe1a1b70a51be34eba5203726e6552</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.6MiB (188.3MB) – 3,424,830 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d490cf4e6d005b7e7b45cbed8acd047<br>SHA1: 8aa9a09c12f5da1d9e97731c40542236cf7b5e70<br>SHA256: 9d16e25cede63d0b49685c7d7921c48d12c6140e9525239b5453b28bd4b7e788</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>178.7MiB (187.3MB) – 1,896,345 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61df2c387952317872f68e9b4dfb3b8a<br>SHA1: 4ee90a20e127452a4437b5954b18d0064032984c<br>SHA256: 68719ad553ef18aa03bf6b8149792e04262d49a32f0c1ba76e28915470179fa1</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.6MiB (191.5MB) – 1,896,345 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b9301a5aa575d9158b915c0be4f91c6<br>SHA1: 8cb50b4661ae1dc91d62f561684862ca83791cf2<br>SHA256: 62edb7440fa10f98cacd8692df09b6f57bb958f43030e80ef2b4936be8fd7b3e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.8MiB (185.4MB) – 1,896,345 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7aad4baab496aba14a16814f679e5411<br>SHA1: fcbd530831881b55c831757413af8e4fa71d0991<br>SHA256: 43cc687bbe12a8182fde9eff6c49246e64d79977f65c92992bf036b430518cc1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>177.1MiB (185.7MB) – 1,896,345 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0216e9bfa4218c01472152fce9f84fe2<br>SHA1: 1614b48ab3eba229d492975e30ac1260b228059d<br>SHA256: 8605eb65e3544fee4fcbdb751fa6e1cd19d4aa4236a4878972321e47892ac0b6</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.9MiB (205.5MB) – 1,896,345 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6535292ef1f7273327fe0dc154a12100<br>SHA1: d02f3626861718b84b25925e6cc84f446dfb6531<br>SHA256: 327014502108afee0fd03a98719b78342969503f3f36495a9b613cced180f4df</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>176.6MiB (185.1MB) – 1,896,345 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53f5faa1c7e619e0c88457630c4676ee<br>SHA1: 172b551dcd45257cf1a5e5d77f5cc2615f9dc7b0<br>SHA256: d49ec46c897b90170e9b99c5ea894e251c06d9836104b456361b8771c2327639</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.7MiB (206.2MB) – 1,896,345 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88d9b8bf35c44456f6e9c1823463d235<br>SHA1: d20f9129db65005013ef9be1294265f49d14e10a<br>SHA256: 9329bfb110a6cd1a4939a4cc9bbd83da8a0c822d9c78a5c04c37dfe5b6785cf0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>180.7MiB (189.4MB) – 1,896,345 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5990ed37721e8bc8618cb3dae24dc6a9<br>SHA1: aa25569e376079e90125269eaf4ba52fcf7eb606<br>SHA256: 6d537d963ba421cd46c589af13ba3a8f99444420e71c5e1f7f1ce2855ca7bdf1</pre></details></small> |


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
