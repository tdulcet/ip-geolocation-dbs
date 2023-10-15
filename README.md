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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-10-15<br>IPv6: 2023-10-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.619MiB (5.892MB) – 239,357 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e09d06252442fd3b2da22f3bd6b779c3<br>SHA1: b02f12489ab8fed430a97bed2cc722935aab64a6<br>SHA256: 3f859e6f41f064744c890832bc9d5d89d732abf4366b67286c26b1c4782092a2</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.321MiB (6.628MB) – 81,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd025af9c05876610312f354e9ca5abb<br>SHA1: a18f58ac5a198250c58f70c1a55aeb9b47bfe5cd<br>SHA256: 1d5cf3b990e7dc0c6c4e26dfb57842fdc33ad17bd71bbbedda9871bb7a837db5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-10-15<br>IPv6: 2023-10-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.600MiB (10.07MB) – 407,732 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2311390cbe4a5f2e0494e930824294a8<br>SHA1: 3d01ea668d28cc13f2b4892121ba7bf7a81bdf38<br>SHA256: 92d37fa09642c86cc4c19fcd9994fae27e5e1e8b8403baaa68cdddf1069f5334</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.084MiB (8.477MB) – 104,747 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d3bee8488e3cf5e2794b8c765923b70<br>SHA1: 45e6496b2b60e28db43b570975ea9c10499d09b0<br>SHA256: c32c7d436cf4598903c12f6a4b657b5ee9b1a660aa82fb99dcddecdabfc3352f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-10-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>16.30MiB (17.09MB) – 694,853 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe6d313a1784a124d4f89afa1320a153<br>SHA1: 2d0330d5ff277e33639c78065787c846d312d6b5<br>SHA256: aed744f18795ac70fd24c0785448f392c819eea2580f94610d585bae05ee8113</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>42.63MiB (44.70MB) – 551,842 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d60ca064237c6b4f0f51b25b1c17f0a<br>SHA1: c461ddcf57f0c4a985d571e81bba02287c1ea63b<br>SHA256: 0459a854039aa003c2c55898903278eb1c30d8408521cd6526103c9db875e3ca</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.207MiB (7.557MB) – 307,820 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ff8d81d8ce4efd3476359318175af0<br>SHA1: d105d1c4490b536a83d0461759256799109a17cc<br>SHA256: 4cb45f08b0bbd6d6c4fb204e776835b939ac663761aea652d12ae2ab20494228</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.54MiB (27.83MB) – 343,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3256ab7e4df24ca9917bf92c70b9ce1<br>SHA1: 832b96b707911579f91d2a42cc84b0766c5db738<br>SHA256: fdb03997e4b7c1a6bdffa274673b7756d8dbfb2ede55f1186b3957ade7042544</pre></details></small> |
| | | Full Location | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>184.9MiB (193.9MB) – 3,048,591 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed65f47a5f866d476bde81f05015d0ad<br>SHA1: b0ef2e2cdf8875da35c99816df76f9fa88d3de9e<br>SHA256: 5bca8efa9618ae69c9fe4228342c0ec4bfb4d581ca0766a3a8e45978d1fe7875</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>269.4MiB (282.5MB) – 2,345,213 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f854d9364b9ab55744dfdc557c9f9f6<br>SHA1: f419e9a0b9db7b3c78b5c98927c74c8427f3fcd0<br>SHA256: 3d1595b762a094dfd2f9ac1525dcc77a67ac87dec747f420b0fa63ac4fe51cbb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-10-15<br>IPv6: 2023-10-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.547MiB (5.816MB) – 236,500 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4857bb88f1e540efdbadfb3e56c208c8<br>SHA1: 0190e03fc0543a58ca868f0f36a92556049db942<br>SHA256: 44b7a5f1e09f7ad797ea8511ecfc8ddada844067bdff82f4255273d85906d172</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.24MiB (20.18MB) – 249,120 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5105fe9bbe5d0ddc9bf8995e1cd8fdca<br>SHA1: 48b9366c0983f8d70d79ad112999057d17d64829<br>SHA256: c10da1d1999f1867044c9753957966c4989400bf25df0e7fb02c524b43dc90fb</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-10-15<br>IPv6: 2023-10-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>171.6MiB (179.9MB) – 2,803,356 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4abca24edbdd7d97ffaa621ecb9327a9<br>SHA1: 97c24a0d18b54cd8d2692e708765b79162107242<br>SHA256: 903407a226a3eb479f2165ba004762c64c3a41dd5a9c0d515be1353f99e5796a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>166.3MiB (174.4MB) – 1,448,721 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d928761a3b79f2ef6c55ec6d4dd813e<br>SHA1: e7de15f34cace41d4332e3d59c8ffe729fc2f8ec<br>SHA256: 613e34be98c76eab733c9982022bfa16a5d1ab57fd73444f0d6e8a2ef59ae567</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-10-12<br>IPv6: 2023-10-12 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.20MiB (10.70MB) – 435,410 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 754026a10835ae7b2fe281b91fcdd82e<br>SHA1: b91c2a42da10904e107465dee0086aa9a62ace53<br>SHA256: 0ba797df847590e614e229cdcacdc672c7bb0866aa6fe6b8bcd73be08b7b1948</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>18.39MiB (19.28MB) – 238,017 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9eaf984ea892548eae9222a6dd616edc<br>SHA1: 804a5715bfa6c102483047b365acd54b09ac9e1e<br>SHA256: ba46cfa3725490fc95f7e6ab9d62cb69c8ca99760a9077ed6472e4ccad1e26dc</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-10-12<br>IPv6: 2023-10-12 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>192.2MiB (201.5MB) – 3,825,453 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b22730fefcc2dd160e25ca15f30adae8<br>SHA1: eae3416eb1325638f22ee020f3bf773244bf644c<br>SHA256: de074a36e2f3b267652c399912b4ede4c6a7fdebe09ba97b3c62bcaafad6b370</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>224.3MiB (235.1MB) – 3,825,453 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8f0d94bf572ca72e83fa1d7a62fc547<br>SHA1: e1ffaeef072de01191f9bdd751829e2753e572d9<br>SHA256: 4d6039867738dbf7d1c98e379072fbc089a10e9ae28c2f1114ae4fb1be5a2103</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>198.8MiB (208.5MB) – 3,825,453 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5de41f015daf8e108b9bff58211a7de<br>SHA1: 0cbf2aaa8b0c746c700c32a028dae6f69151c597<br>SHA256: 11c79d389e66ad8199c3723a2b4c2ec721344997f6a75cbdccf3ac15d8cae9ee</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>205.3MiB (215.2MB) – 3,825,453 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 727a94708da578920277fcad3e5e5d5d<br>SHA1: d43e0735b1dca31143189b5cde86dc283d771336<br>SHA256: b054ce576b62faf5b577632348e7dd2a3c6f7d3a7022d459cf57b75b90e5fbab</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>241.3MiB (253.0MB) – 3,825,453 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40453861bbaf5d91473ebd467acd4d83<br>SHA1: 201b8f734970e06ddf8aeaaff662c515030df299<br>SHA256: a949af577d2e0a1a27e5c0607fc0b884eb9e77fd4723f03df079ddcc78ff2d2f</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>193.2MiB (202.6MB) – 3,825,453 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e1eb9867e954e71da17a623e5136a80<br>SHA1: 8e90ae3bbcd5510cb5c6212c1ac06d67936a1ce8<br>SHA256: 90526a4dc8496be49bd4969088ff4f78fccc1da3d9591afb0cb241148f99bcfa</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>241.0MiB (252.7MB) – 3,825,453 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ae116bf03c4065fe76ec6dec8e63d98<br>SHA1: cb81f3b0bead23933e4b6861ed86a32fb45a7f31<br>SHA256: 175370d39d6028c2b232097d54782937e67faff85c86d3e3992be9d371a00308</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>205.5MiB (215.4MB) – 3,825,453 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10f21351d6f527040fad8f7bd8f38505<br>SHA1: da23ffdb5e2fe0fe2b5f095312fc12b64c6e46f0<br>SHA256: db81f0221c6f0144209564defd9554a0bf1c16c132903f28b97b22f211d652d4</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>120.2MiB (126.1MB) – 1,195,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 926cc84b8a4e7a1f0cb962a0cdd7e66e<br>SHA1: 0f7068e7956c0947ddae0759d376374bab2a3bc6<br>SHA256: afcf385d8834379d50e22ef9684a58c46c4243a6a228d431c8381270cc8ec4d8</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>127.6MiB (133.8MB) – 1,195,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87b8200f741bc7f78ed523f547fa71f7<br>SHA1: 4ea0db5f06f62968459e7dfc643fecb4b6b4cf59<br>SHA256: e57567c9346b26dd97a036b3be09ad49ab92d36857e509a96803f6529a8eaaa7</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>122.1MiB (128.1MB) – 1,195,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2cd6349498cd3d61e84ccb5658029c52<br>SHA1: 36e409f9fdecdcf49d188023a2e4105cb582c6d4<br>SHA256: 5750a5e828f5ba0acc558ac21334b69e762ef55413d58334e3290148e13212c1</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>123.8MiB (129.8MB) – 1,195,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1dfdffae3ffea86b791ac21b2162987d<br>SHA1: 8f518c39789db2b743320aa008e544eebbffc7d7<br>SHA256: 9c2ebdf6c11b62971756562ce3eece4f4130b1ac0c234d8ae32b4dd8e5203e55</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>131.2MiB (137.5MB) – 1,195,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ce7d85dc193708e959c5721bc9b9f34<br>SHA1: abc30555bcc8305237b06b0f91464759db38e316<br>SHA256: 91f2bcf418c0d79c1d89eed1de27fab31b25b2dfa2a66d7324cb937673f7d26a</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>121.1MiB (126.9MB) – 1,195,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44b6939da6dff254500c99eb4a311bf7<br>SHA1: 48ab833e0188914c17a25ea8efcb321ef52c9487<br>SHA256: db6ff915ca91e2264fec2d808949b8d6865766d3b482c135c1e9670c9fdc6a24</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>131.5MiB (137.9MB) – 1,195,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e72981af6f1afcd0812912a9e5c59be6<br>SHA1: 2162851f601bc1aa8b01e0686634765b99a790ad<br>SHA256: 600546f94c6b7cfb179f74e5b40abba1bb990eb876061891e894c7f7bc837fb8</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>124.1MiB (130.1MB) – 1,195,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2336c21c5e3e7147e7f6fc7ae5f1ba48<br>SHA1: 0614ab89eac89f2a50b99ac807d71fa4c7927a9c<br>SHA256: ea5fbaa2a0bab82304a6fc90ee0ec9a08ebe840ee68abe14e3d17bb2a4d861a1</pre></details></small> |


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
