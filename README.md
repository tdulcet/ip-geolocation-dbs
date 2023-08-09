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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-08-09<br>IPv6: 2023-08-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.673MiB (5.949MB) – 241,677 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 505d35d939999e845e7abd40ef78b1ce<br>SHA1: bdafc76996c19d25dc487b9ec5c331d4970e58d6<br>SHA256: 1e4ac1a1cae4401ba28ebf67f0bc5880dff27e03141a686476d4027f76cab5eb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.576MiB (6.896MB) – 85,133 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9f776082ba4bb7aa5858e4e72b66501<br>SHA1: e158698049710e0acca38ce0a59e8a82dfc3a8ba<br>SHA256: ecc0f183b442ddc5975c027f025e21b64392b1f8c31353c19543589e08f2a47b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-08-09<br>IPv6: 2023-08-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.540MiB (10.00MB) – 405,232 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50a282b76b132ac55d7e88ac0f1b9d4b<br>SHA1: 2990598f2f7a90e2a1ea32d9784951b0221b14bd<br>SHA256: 781cc1673af2b1d248a8d5efdf15e9cc3634e3a81a6981ab5d10145caeaa8303</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.687MiB (8.061MB) – 99,615 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18a7124f52c93c387ecca9f1a27a7496<br>SHA1: 5b350460d5ca23e1e82e18e6fe1fb823e9354cdd<br>SHA256: 89c91195ca2b81d6eb36df518a67909d871f66605d3cf156ba00bc496e8b1ccf</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-08-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>17.98MiB (18.85MB) – 769,902 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4352b99568b29851d4c7820875053b21<br>SHA1: 430452b6064180340bd55eb2a24f15fbea58b5a9<br>SHA256: 3819d6c1c9be7866af15a18b961e8ca536793b08c894fb674d94e4993044d69d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>37.47MiB (39.29MB) – 485,034 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1c8219c73e57f1bc968f923c85ab53f<br>SHA1: b91a01c3fc3c29be53dea0b3d4e56cf63f20d918<br>SHA256: 1dc41108789a388fbe1b76618648f131c75a72787b4c6e7e556116e5646b12e4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.354MiB (7.711MB) – 314,876 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca76b98b742610e14368fd012848c6e<br>SHA1: 5a246f7aa51c885d4dc479284c99db5643e6770f<br>SHA256: e98c856388c6a61108e688ede0fd4bb7b818be019a620f09abfa12f09f9d4af0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.39MiB (27.67MB) – 341,571 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956b52205bafb278c0610cfec5e8e6f3<br>SHA1: 6e3ecda1bff92e53f23bf2ef3885149bc6312eff<br>SHA256: 0edd51b1478170d678f6905901a1c6a3ac7486a66f8672ee06079354a8c40436</pre></details></small> |
| | | Full Location | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.0MiB (201.3MB) – 3,170,913 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e50f1d7e16995e4854b0f105bd6c8b2b<br>SHA1: 1dcbe021497af64af841ae21163751821541e06e<br>SHA256: fa28f36a198a238e8f503e858e7561b54fb9c909d90276f58d195afea9f75250</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.8MiB (311.2MB) – 2,579,615 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bac2a6b630483711e47113caedf6461c<br>SHA1: 234b956c8061d27a07de03503b53aafee1dae740<br>SHA256: 67b384e2ddde5241f818748e689acf0bf9c436ed15bc23bd12c76eb991bd4fa3</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-08-09<br>IPv6: 2023-08-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-08-09<br>IPv6: 2023-08-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-08-07<br>IPv6: 2023-08-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.44MiB (10.95MB) – 445,478 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c91610ce96b882e569bca278c1f22e8<br>SHA1: a9bbd7f51797e9184e9cc8ac8cffea6a86497301<br>SHA256: d5de12158c9502a7178097b96378ab203f8e84202d147a0081320b2c83e4a5fd</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.19MiB (23.27MB) – 287,228 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90cbaa7925c5524398a1941fa1f301bc<br>SHA1: ce35b4b13230d97701e802b160f70ed54a338db4<br>SHA256: 4b4623ccb3103fa981b8e67680f475ab9c16b87fa5f3272833c62e56dd6ea145</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-08-08<br>IPv6: 2023-08-08 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>147.3MiB (154.5MB) – 2,925,589 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f138847c672afbd4827375e77c847611<br>SHA1: 2c6a8aa1afd7602b5c47956511024ad3b5ed931c<br>SHA256: 0bdddb04535ec280f53b34b9e25a91986d65835285a0b094f33a9faa57b79383</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>171.5MiB (179.9MB) – 2,925,589 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69145c079ac0a5420a62ceddcb2bfe46<br>SHA1: 2f800a3de5cc533cb0c4b30620ec9103c9b35ef3<br>SHA256: 727b588fcf843c57de89442b3b02fd567c7ed98dfe957f9761fe6615f3ac27c7</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>151.1MiB (158.4MB) – 2,925,589 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d485d1d6531011eb3e8516f6de5bfda8<br>SHA1: 29b6de160ebebc5042581576d3fd1540853a6da4<br>SHA256: c3a99c14a043d84bc124336dbc24fe83392bc4d57dc89e6e88c382807bf6d0f6</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>157.1MiB (164.8MB) – 2,925,589 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfacec441ba87b834d3442b0ce616150<br>SHA1: d4c8934fde0fcad326152f10005c05b692a37a69<br>SHA256: d14798651958bd33eff9eadd7e67e45f81af7d299824dddbf530d99352c34e35</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>178.3MiB (187.0MB) – 2,925,589 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7ae2f28ba6f051dae9e49cfa22f07e1<br>SHA1: 4bd7947823c56a5c882a0eb4ccd06088a10fd752<br>SHA256: 476609e4bc58d94970b0d5ad8dc8bc0146381a79ebfd03cf42a4d1a4f899c7e8</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>146.4MiB (153.5MB) – 2,925,589 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be21b2fde2bce8395d007996df19c309<br>SHA1: 04a654ba19d6cd5c4ddb0801946324842b1b1352<br>SHA256: 53572d1641d43fab4984f46cd22b7de7ffc1c9ec11d8b4890467ae395b1eec9e</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>180.2MiB (189.0MB) – 2,925,589 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8d8992933d1abb1a504d9b1ae59aba2<br>SHA1: 49433bb6e03c3f0ba14bd6b7dd967e1af639867f<br>SHA256: 9193cfa179f8e150b0219b69dc4fe7315588f7df324eb5be300a54c99535a047</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>152.7MiB (160.1MB) – 2,925,589 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98a8e281d882364afed51e379525a4a6<br>SHA1: cc549fdfe3cbecdf8a5663c427731ba505ccc763<br>SHA256: a785444e1b682f4977ec7082429cd00182b7addb34d50f0fdd79eb03e685d395</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.8MiB (135.0MB) – 1,283,982 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bc489ecdca153a4d3ad869ebdc62405<br>SHA1: 4fd0df25a13a18f4aef5b8af138e01957890d620<br>SHA256: e04b63672f2fd7ddb0a49a0ec3f9da535eeeb8c2cdd0daac1d3e7a6208611ef5</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>137.0MiB (143.7MB) – 1,283,982 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c4b652b3d44becbab8bf925613c0162<br>SHA1: b2ccc752504307f3820f69216a595097e34dc928<br>SHA256: 82701c1e961952ce0986419fc49e4e8bf3aa238bcfa3446d8da48dfd770fcb9b</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.2MiB (137.6MB) – 1,283,982 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a789353e39032179a66855376ad2bc18<br>SHA1: 188d4089a65782e614850bde52668cb8c25caa88<br>SHA256: 6c4959e1db30f316b4ac9708c45371e7adc22ffd2fd5a0f7ec5d65124e52106b</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>133.0MiB (139.5MB) – 1,283,982 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 512850f09803938122d13da5d49bef28<br>SHA1: d6cb4da8d2022c69ab4e1d28e29a0c8e62fbe9db<br>SHA256: 6d0bbba7517da4adb4cf1f5979100e0145aeedbc592cca3e15abd9f0ab60fc92</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>140.9MiB (147.7MB) – 1,283,982 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e94c9fd68a9bffcc4be9f00aeaa8f01<br>SHA1: 91e69c785bb074724f9e26066938f0db69cf35f9<br>SHA256: c7a2591dc5df8d62149fbb8e415fd1be68be3102896ff31526c987f2f2210d73</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>130.0MiB (136.3MB) – 1,283,982 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1b85c770f33ba49a37718136f7169f5<br>SHA1: 42575cacbbe3c632d6d148b3366589994d45536a<br>SHA256: cfff643615bf927a63957714ddbba81b486f0954322e4943be343f102ec6df2b</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>141.3MiB (148.2MB) – 1,283,982 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1239b345c6e66e161f0f96929c976df8<br>SHA1: 65128ab627804cb573344cd02c525d41bb4355c3<br>SHA256: 2ac01a58a719e56263402203c910c7c8911147e6e05002b14b2ad520511dcd0c</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>133.4MiB (139.9MB) – 1,283,982 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c038cf117d87bb6b41a9af01361d7614<br>SHA1: de4a8494497375c10d11c82270cd2f81f4adde0c<br>SHA256: 329a7a75eae2ba4fe7146ae328dc87b023a8c51e8f95533946ab66496bfa5cc7</pre></details></small> |


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
