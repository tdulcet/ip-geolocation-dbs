[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-08-11<br>IPv6: 2023-08-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.675MiB (5.950MB) – 241,737 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f26b1dc938b051b224a3ad76be625ee5<br>SHA1: b2bae9f50c6768178e3e43286536d30e170a4278<br>SHA256: 5b25d476948d4be42d7cf3eb6391681d09666840bf453130976eda0c4cc5e954</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.583MiB (6.902MB) – 85,215 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43ccb065e4d3bfbacba82b91c7465a2e<br>SHA1: ab53869367a805cfacecf85340856da00fb9f41a<br>SHA256: 9119029094faade7a82c860efc1dc70aca6bfaecdca7905ecf0257c8e52279f5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-08-11<br>IPv6: 2023-08-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.540MiB (10.00MB) – 405,245 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5617a5c7d9ee8dac83a15c33c333bc2a<br>SHA1: c59a37975f9be06caf37e711e667fe2c348a2779<br>SHA256: 97f92bd53a4198afcb297213a5cdb411bf4f49b52328d82acfa4c289db101df7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.704MiB (8.078MB) – 99,829 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e1f64b2e3e188fa860ac29ea4096c10<br>SHA1: 168c7650f961dbf3e720885efeee05a8053ea637<br>SHA256: 0d5ff9d3d688a603570b1e49da8daf137a6a8b31ac2c9af3d68d85506fb70abe</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-08-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>17.72MiB (18.58MB) – 758,640 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f61e2af75e5b4e99cf38cb8b151bb9<br>SHA1: 7c2cad874100a93d2bcf4630140adcdb76b26342<br>SHA256: ee1dace122079c7380e42c8db4f17dc4cadd23348ec8fe7559da60f38fc4b8b8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>37.75MiB (39.59MB) – 488,702 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89c8dc4fe09623c54eec147417af88f4<br>SHA1: 2864b02ff132bf76cb0d1c662af104d215809113<br>SHA256: 10a19e7e7d4a4d1b04d6e6046fc9f285e6691482c83040e9e73055580f077a40</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.354MiB (7.711MB) – 314,876 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca76b98b742610e14368fd012848c6e<br>SHA1: 5a246f7aa51c885d4dc479284c99db5643e6770f<br>SHA256: e98c856388c6a61108e688ede0fd4bb7b818be019a620f09abfa12f09f9d4af0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.39MiB (27.67MB) – 341,571 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956b52205bafb278c0610cfec5e8e6f3<br>SHA1: 6e3ecda1bff92e53f23bf2ef3885149bc6312eff<br>SHA256: 0edd51b1478170d678f6905901a1c6a3ac7486a66f8672ee06079354a8c40436</pre></details></small> |
| | | Full Location | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.0MiB (201.3MB) – 3,170,913 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e50f1d7e16995e4854b0f105bd6c8b2b<br>SHA1: 1dcbe021497af64af841ae21163751821541e06e<br>SHA256: fa28f36a198a238e8f503e858e7561b54fb9c909d90276f58d195afea9f75250</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.8MiB (311.2MB) – 2,579,615 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bac2a6b630483711e47113caedf6461c<br>SHA1: 234b956c8061d27a07de03503b53aafee1dae740<br>SHA256: 67b384e2ddde5241f818748e689acf0bf9c436ed15bc23bd12c76eb991bd4fa3</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-08-11<br>IPv6: 2023-08-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-08-11<br>IPv6: 2023-08-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-08-10<br>IPv6: 2023-08-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.16MiB (10.66MB) – 433,550 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5a1934e1f8f6e676240c10d3e7e8288<br>SHA1: 1430795057150c0a024a55d1d59e07822ef0e9b0<br>SHA256: d5171d2acb39f4d0f86c070d7b248b145d26c2aaf228f3c5fe881efc553acbb0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.92MiB (22.98MB) – 283,714 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4dda828e9d710ff88e1abac6bb2d5225<br>SHA1: 520fcbe1e96eaebb4038d1231aec26799c0e885a<br>SHA256: 41814dfa3da01fff05301e3510979ef5d8a4629f64151dacc418c480f8f6f800</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-08-10<br>IPv6: 2023-08-10 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.5MiB (198.8MB) – 3,782,840 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e82e24958e1b7b0967ec96c0fe983b5<br>SHA1: c18ad1e3792b073077f7ed812fcd4e33b203c7ea<br>SHA256: 0be0ef729f04c125478cbc1fe1a2a23df6d6aacdb20851895a42452fb15ac20e</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.8MiB (232.6MB) – 3,782,840 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8125988d732a89ec52d0d3818dbd7cd6<br>SHA1: 24953fa615cbcae89d392e2abec4c9d302390213<br>SHA256: 75e16ac5e14075dba6d17ed186193f201a2631b5793c06454a8fcb8953165cef</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.4MiB (206.0MB) – 3,782,840 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f858f97b7c32b420a75885df1f81a53<br>SHA1: 3a7026f8284a7e0ec6bcb4a67bd97b13dfe3dee6<br>SHA256: ecb4185e63b1063b11fecdb19f00d052dff199f0edb830c6b39c62350c8a0451</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.1MiB (212.9MB) – 3,782,840 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 135b3ac2904f9a0618158944969e2796<br>SHA1: 7a2fc0a81002078be821579ce3c079888174a398<br>SHA256: 8c4c12ee5021a0a93256b6f69d3c994bad6368fbd6f93301abf78447fb37e68c</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.7MiB (250.3MB) – 3,782,840 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92a3afebd82709c858bfd7a4f67ff33a<br>SHA1: 02b253e61429e1f34f25813dae567557fa59e7f9<br>SHA256: c29a2416e147b86fcc24dcd67dae3b74eb5e59c3a988585518dbcc6a4f0cd30e</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.0MiB (200.3MB) – 3,782,840 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0a568e6711bdc55806f408f89c9dc0e<br>SHA1: ee23fb26271de9968989f04067f47aaf99d5c5aa<br>SHA256: 5b2d956fda73204b3f9543b1d0d42f51be9119012c2d44ab11feda498bc612e8</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.7MiB (250.3MB) – 3,782,840 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eff4ffa34a03f3f9726ef543381e9b27<br>SHA1: 6181eb7880e003e89c94833387cd928b6e836543<br>SHA256: 79e6fee56c7a95cf237f5370c7fec2d5f7b145c526324acb3268e5377b0c74c8</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.3MiB (213.2MB) – 3,782,840 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc55254174957f95e3dc31abd7ed2b30<br>SHA1: 7029febb17c269421027e8f2e031fc3905291575<br>SHA256: 70c3437fe5f5e44fc1d5d8dad1f7d3827a0b7968e65e0b90e0d8aba339c5de15</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.6MiB (134.8MB) – 1,282,078 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c76f8fe19d5ccd21b9f36af2c5d01103<br>SHA1: 345a6d0f340fb83e10799d6366d90afc6f807ccd<br>SHA256: 6db7df82c61820ad4c18594a1e410e639edb67ac7a1ef91ef796cb1e1ac69c0c</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.8MiB (143.5MB) – 1,282,078 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 542b360fdb26098f29021f22d835ecd2<br>SHA1: bced746cd05ca923619b4dc55f80e1a821f8dfc9<br>SHA256: a538598d80231d6d6c3ccec9aa609d35fc896e1defb17b36dcc60d1764cd6622</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.0MiB (137.4MB) – 1,282,078 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf82dd1ba8558214e26d66f6aa689410<br>SHA1: 7d077d5ed19f92d374638b810382bfb5a4ad7118<br>SHA256: 62ab2aee2c464817f47eca9e7f000804a8eaa68def661b35b50af512e20324e9</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.8MiB (139.3MB) – 1,282,078 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 063355e5517c200ae54bbd344ce0f626<br>SHA1: f8acc73573accbbb44dcb322999c0e38d58dd0ad<br>SHA256: c5d5ae5e3e84c794a1c82a9e20538804f6a9c765ea44f892af59a927270404bc</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>140.7MiB (147.5MB) – 1,282,078 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f52baf8e9feb9670a4996e5b74aea481<br>SHA1: da0c582e0bb38ea353d752a268082dc287d41443<br>SHA256: 940633612c1a77455f94145f61f1d55fad8aa990fb77e620e01c869fca0287a5</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.8MiB (136.2MB) – 1,282,078 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c2165d6e2c0d9dc476eb0fcea1a840b<br>SHA1: 9036c36ee5df3fb70c0192bdc5e9ba29ab724e64<br>SHA256: 164e8a225b5c388d79fc41dbc4951ca1d38424039be48ade81a5ecd39c0a091b</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>141.1MiB (148.0MB) – 1,282,078 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c975a4517a3706862555015b9fd1e5a6<br>SHA1: ef762f998e7469996452bd781b1270070d8be1ff<br>SHA256: c664f3b605172746b3b0f5d354698edcad8199b7dbecae318c8199fdd5cd8092</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>133.2MiB (139.7MB) – 1,282,078 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4195643d67ef048f44cb21a06323fc0a<br>SHA1: ef5c81c7bf5d492cf5502e6bff800f3eb316e9f7<br>SHA256: 27b19c1c223e280286f5c76b8f2e77132a55c58dff8b9c3dd3f181d201424b41</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hex format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
