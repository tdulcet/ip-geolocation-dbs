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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-17<br>IPv6: 2025-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.318MiB (6.625MB) – 316,424 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 511965c436fd2ab552ac4dcf1fee176f<br>SHA1: fb4465de4f2ac6dc4c5c10ec93ae6929c60af02c<br>SHA256: e5378bc9c225203ad3f569de33bc5ea44ebbf2ae7c9b596280fe25ade598f4a9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.35MiB (12.95MB) – 187,736 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37066a17d67e38edb3c0e1c8ece4e62d<br>SHA1: f6d98f65bd020a8e8af0488b9c9a58ec19769c81<br>SHA256: 3905b10c56eb54c32be90ed33ca4cd1eaf94cffcf598dc72539ce95b2b8f67e2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.82MiB (12.39MB) – 591,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bba85116626f7075c3be6d0cb1076fbb<br>SHA1: a0f3f6afa6a830117ca10f0c111cfe79fbc3ae67<br>SHA256: d57815ba742fbabddf358fe04a634eecfdf465b24a4a52cf4c18e7219c0cf8c7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>84.35MiB (88.45MB) – 1,281,906 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f12ea780c5d259a9cab8f0aabf620a6<br>SHA1: 1ad530a56f314f3c0fce0eff16fcafba43c57f14<br>SHA256: 011435949bfe3596339ab11d7424ee0f65696ce99ddac6748b818f765d38563d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-17<br>IPv6: 2025-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.068MiB (5.314MB) – 253,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ddf95be39b948ff8a1f5f72a989f3db<br>SHA1: 53e521e70cdc7bf139a71019e836b80590d710b8<br>SHA256: 50c6f2769387e3ee7cedf43b469b7ba544e29e43852d8c3fccd14dbf39e376a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.78MiB (22.84MB) – 330,989 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43bd9e1f0cc46c204def11cc25411429<br>SHA1: bb110aabf0613079fa6821963cb9072ee8a672f5<br>SHA256: ef3129675278c4750cafd639f31a9a899cbc6468108504cf55d1a6439f90199f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-17<br>IPv6: 2025-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.2MiB (176.3MB) – 2,916,495 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec46eb0d6770f3a4934f80b9ba8b43ce<br>SHA1: f00f5138d48a37c35fcf9f170e21939324735351<br>SHA256: 16a49d4f2d09a24369e498fa18c855ad30e4610d4fb1424acea4ea9ccec6048c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>279.1MiB (292.7MB) – 2,704,923 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dac800448bd3a785c553531ef23da1b6<br>SHA1: aaef79ba06d4297b621a7688cc2224cb694528a0<br>SHA256: 6c59b673d7391b858e46d6527a0bce731c26713b44246050076e424d61a9f656</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-16<br>IPv6: 2025-07-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.56MiB (13.17MB) – 628,734 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a15491427335e306d75917b8a77490d<br>SHA1: 002ba21a8623363fd0822a036e188989cb8bc18f<br>SHA256: 2f10480bc7fcb073886fdc0fad5cf861307e73865ec5ccf680e9f6b399a4586b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.44MiB (44.51MB) – 645,011 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f62d237f5541c0be4b3f0329d794ce3<br>SHA1: 54bbbd038b2d3906b44732706207f2ff1180c31f<br>SHA256: 35d2d80ec9a170c92a7ca6562548e2c4f550563e66c123eea410205ec3f4b9d3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-16<br>IPv6: 2025-07-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.1MiB (182.6MB) – 3,434,532 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ef3e706fe89810ead8f9b6400c98108<br>SHA1: 336a73fa7dfc236b44afe7cc397a99b56fdb9043<br>SHA256: 63b7e769dd496dbec6a97c7b3fc3b0a4d792af13ed1784f3ba5d4953f0a095eb</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.0MiB (194.0MB) – 3,434,532 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d806566d44b77d77fd40458c207d92c7<br>SHA1: ccdfa57f182232a287a1a582753c57d890a0ee98<br>SHA256: 31b9d116b3399f48a6135ae3d6b229905309ab1d4b3856c35c6c51a8d0ec6581</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>173.3MiB (181.7MB) – 3,434,532 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a897f729dce3e627de709acb0fa34286<br>SHA1: a0702c8fb2fab2dd53822fff69b3a8e88c09b18e<br>SHA256: e32016716255cd9f4c4480b877bfca1d4e0fc4e924140f79bf5d8282ca0cc478</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.8MiB (184.4MB) – 3,434,532 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fce7be3bb73996825785436e677cf65<br>SHA1: b9a50faea79e804314639c10bc983f52d91b22f5<br>SHA256: 5894854ffc689160ae9bd9e7d6e7dccf22aedde270dea900f35a7f697fd40740</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.5MiB (231.2MB) – 3,434,532 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 620cd11d5961fad4ff324e93b0b2809e<br>SHA1: 20e43164b941c4103e8fb1b94cc7428d5fbf654f<br>SHA256: 4f42c3b8c1e087cf66b555aa025577d7a2cbc739b34d30fc1e4376ee044020cc</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,434,532 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dcf5800933ca10dd7b0ecbca09daaae<br>SHA1: 3ded99bf8a7a0fb0ac11f3493d0b2b4bd6e85645<br>SHA256: d12869d5533d962e81ceea4bcf4156860f0abb69287485a3839a16943eaa1435</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>214.2MiB (224.7MB) – 3,434,532 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b86b351f80972617154ab3f97a115b8b<br>SHA1: 3c62f41dbf0e26072b683b8390d9f814e5abeb27<br>SHA256: d28188dea0407192d4196ac1fd9fbd216d516ed233c782d49e45c6e3d117f8c2</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>180.2MiB (188.9MB) – 3,434,532 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78e53a71fb3293282c6656e356842ad3<br>SHA1: 67f82fd02099fdd9f52aa04da70a233d7cf8fc79<br>SHA256: 5372aec9a4e92a737a77efb43e1d7d299017ddad48254144a0bd56f9f7f575bd</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>178.5MiB (187.2MB) – 1,895,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1625196896c1655d2eae08d73c397bff<br>SHA1: a9a6e1e4114f21475d04424667d346d9460a0b1f<br>SHA256: dc35c6688d2ed37e90d4490105d68e059f3cc4a18b584ccc8a681b8dfc304ac8</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.5MiB (191.3MB) – 1,895,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e653f8ca59905c4ceea6af504e380be<br>SHA1: 3c55dc54f511dd1dbd73ca706db74f5a5f49c91c<br>SHA256: 1c6f59005f5f5f12ee59e9431080901cf9f9e276b232d1b0d9e1d18729899040</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.7MiB (185.3MB) – 1,895,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fe23f6390431eee640c198db3781d4<br>SHA1: 133deeb614e345400039df41b862e6422230dde2<br>SHA256: 47eaaca0bd8f1ab508123dec84b07cb168096933dc0a20dd17911a91e7e960b2</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,895,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50168e0754a952a4ed6bfc42009fdcbf<br>SHA1: a66088f2e85d9ae7f5a23d28d3e24b1596aefb98<br>SHA256: 19904605d102e40148df30b26cc33cc17f0dd96b94646dba75b018e269eea72a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.8MiB (205.3MB) – 1,895,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63a8cd910c413692333374a011aae54a<br>SHA1: aec3fc9dfa59705bfbc1a4943a80c14441ae3a6a<br>SHA256: a8c92503fa851e7f5255d8152933cd5e3cdb10c73bc957f79a778cab9de85a37</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>176.4MiB (185.0MB) – 1,895,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ac25523ab22e560ecf58f84f74bcd35<br>SHA1: 06d65441c003cabf8cc89c2e605ffe09d242c5b5<br>SHA256: 0e8cf958924d73f73c40594c0690acb47e961a828833920166a494e41d856c4a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.5MiB (206.0MB) – 1,895,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74a4856e0be3187e5f1b66c0b724211b<br>SHA1: e44c07a8edde3669cd97b100711e9c560085767b<br>SHA256: 49a6ce1fdee649c25fa3e7d05a4159f65ce2fa5080b739daf22c2a0da68dbcb4</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>180.5MiB (189.3MB) – 1,895,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1243520b0556b2235d30ecb157c98485<br>SHA1: 31585aca4a938c52475f929db8be029cca86fc1b<br>SHA256: 55ba55c20f59aa68ca7bda53adf392ff9054ec24de38c02308d86a01721a8400</pre></details></small> |


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
