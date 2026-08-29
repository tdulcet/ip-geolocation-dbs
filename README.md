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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-08-29<br>IPv6: 2026-08-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.489 MiB (5.756 MB) – 274,704 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9851af2354af0031f2a68793ca9be2d9<br>SHA1: bccbe652f696f4800a5407d2b658d7c6380d3537<br>SHA256: 406b4dd44dc184a45f8b8b1726c3ae941b71cf4a93254a8b53307b2bd9565f58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.61 MiB (17.41 MB) – 252,370 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c522e3a9a5ec85326859589afcf40a02<br>SHA1: 24d703023d321f6227037b4424ba6ca8c337548a<br>SHA256: 56ccc6cdd631257856dd7cd33cd1784d8144f443e319fbe611f300d771365811</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-08-29<br>IPv6: 2026-08-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.098 MiB (9.540 MB) – 455,569 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d2fe32ec745bc04c372ae282ff3f772<br>SHA1: 9c229983e303168b5c1bcc71395e875c87870e53<br>SHA256: 3d90195c325ae8f9ed287bd7d2e7be1c0c80a428474f8dc87a79cb32a677dc19</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.029 MiB (8.419 MB) – 122,126 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5c9ed679c9a775e3311fe5c8330b6f4<br>SHA1: 2b78fdc6c4c0ad2dc44891bdabf6e65040a130da<br>SHA256: c006e8bc96db2d9fca30191de467cdba83aa9dba785c9675abf4707baed5a8f1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-08-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.19 MiB (12.78 MB) – 610,140 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a81c1953bd60ebfc65769399d1f7dc0c<br>SHA1: 67326f760cabc67aed70e632ee21996539f2b2e6<br>SHA256: 9e782b12664a7c1b55a35accc00056fdd274c9d30129d201f250392fe536bc6a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>47.05 MiB (49.33 MB) – 714,933 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d9e7f4152b4d2469d511b75e76ef7a0<br>SHA1: ca1ee62512b8d3389aada3b9f9b0f78aa0ea9bba<br>SHA256: bf5f57fde8be72794888c99409e891722656785f1464cb1ec40a5213d4a29ff3</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.149 MiB (7.496 MB) – 358,140 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d3e21d2da14fe2fa0da1db2f6424311<br>SHA1: f274f58aadcfa3311603218b88e8b24a01671e36<br>SHA256: f62294be209c966f38eb82e27717bc64116462241210756e85c31429048d1f96</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.92 MiB (24.03 MB) – 348,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60cc96dd0eef36fef003b9981e7aa19c<br>SHA1: 077fc11bdf3b1a16ed5a8e22cb9889e86b007cf5<br>SHA256: da4f32fc9e285ea393eb3d4fec4fb4a153874623b14fc77373e8f448758ac135</pre></details></small> |
| | | Full Location | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>208.4 MiB (218.6 MB) – 3,652,137 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68a79460a812a271884a0a50858ee1f8<br>SHA1: e1cb26165f0fc2b394c3f08d99642d1e5a3e653e<br>SHA256: f40963b044ff4637dff7dd3608244f6e065cc97e9bb7262d5fea4abeed6cf026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>440.2 MiB (461.6 MB) – 4,274,498 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e9801b97694446ef740a7093d24488<br>SHA1: c8e28d1130d3667d5b313b6e468c5d9d69ffb027<br>SHA256: 88971b264e462d0a2d37d85f793d5e488192b4d883a1ad0142a7c28d9a60af96</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.716 MiB (5.994 MB) – 286,131 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d282e141eb5464b8254973895dd4a19f<br>SHA1: 43ed365a77bcc1acf8efbfc3769c01a237bf775f<br>SHA256: 436d012d7deb50897534e496aeb1616f14ea008640929405f2664f5122ffbbe2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.50 MiB (23.60 MB) – 341,989 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51aa8116a79265830a4cc7cd4ef86053<br>SHA1: c18af12e87abaf09ccf88a3c0de5227c764e8a1e<br>SHA256: 374157270162797a62dd05862b45a4be9f350bd4c2e81ca0a48534910fb28817</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9 MiB (179.2 MB) – 2,958,317 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a7499b08d50db46b5cf9fb15cd346d<br>SHA1: c27a4fdfd31298e65e03fed44f2b36b4aba8504e<br>SHA256: 7e2727a2650e2ae9c6e50b6fbae1b77db0938c91593e6e1e1de5d7e195393e70</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>299.6 MiB (314.2 MB) – 2,903,507 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a92797de8e315b9794c5a75c021c7b8<br>SHA1: 3bad371e9bab711cade7d5e88cc542a34819152a<br>SHA256: 4479ccaf1ffb1b9388ae015e24ea8e3e1780c412777f1ee2b0a30bda83f5d0e9</pre></details></small> |
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
