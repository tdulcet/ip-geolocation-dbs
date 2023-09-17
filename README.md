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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-09-17<br>IPv6: 2023-09-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.615MiB (5.888MB) – 239,203 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b903ae19374cb4bc5529da648150b2a9<br>SHA1: 9ff0eafb0196fe577a6d2b8f3b4fd22f2cc9c6c5<br>SHA256: 706336c1ee4d3d02c061968a961600055764e36f59944f6f11bd8b883430c647</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.165MiB (6.464MB) – 79,805 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c8b16f15f40e2be596f1ddad3b67385<br>SHA1: 8a4c01e56c80dc9809cd73ac81e98aed33f9c600<br>SHA256: 3d43bb2a964ea0731617b094334ffd45beabb16e23e7ddc37db7ee4cd4ed345f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-09-17<br>IPv6: 2023-09-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.575MiB (10.04MB) – 406,700 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afd8c53bed6418a0ba2e8f5cbda3aec8<br>SHA1: ad9ffaccdc11679a7334a47016653eb5605c75fa<br>SHA256: 16a3bc5b71887daa430f4ab92b6da40e860628486c613085941bddaba60de2bf</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.838MiB (8.219MB) – 101,562 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76bc9260a57e348deeab95cca5a0d2f2<br>SHA1: aabb051354a90fcf3691c3a4a25cfc5a401b3dfe<br>SHA256: 954b8698928d9a9e7baba7819eb467167763bf450f89db6ed0064374142f61fb</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-09-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.98MiB (15.71MB) – 638,702 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f0591b328273401669cad0b2d33b35f<br>SHA1: 7c6b1f9c5ac1bec13220cea5d2e22ca5cf6b54dc<br>SHA256: 6fbd3d5bbe45bbc6a458855aec7dd20e4bfc8ba0cac4e25516ae2abd4d336c89</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>46.99MiB (49.27MB) – 608,303 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44c67657301952fefead541aea2b05e3<br>SHA1: a9d1da8311e4bb5114ec8fd0479b5701817a745d<br>SHA256: fca70b6db17719b4e0d7cac355c85b81a2d7001effb08105d34e2090f3751c5e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.416MiB (7.776MB) – 317,712 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8af33754952bca633e2643d56b9b3556<br>SHA1: 635e2f9c397074c2d69ffb9220affbfd86ec55f6<br>SHA256: 3ebea563a71e9352b6b395144accf2da57a57d06e4f59e570f279b0f7dd0b26d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.32MiB (27.60MB) – 340,762 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eabb53c9e90baf81be978b9f452f9fcf<br>SHA1: 926f5a148ab14f14ab51042d5e540547e30fdc1f<br>SHA256: 1fc208ccb6c914cdec8d9914c6bbc9c49c7d9cc9dfb2403391c007a74eb2b066</pre></details></small> |
| | | Full Location | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>190.1MiB (199.4MB) – 3,137,207 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2af38dd10686ebd6a86c594c3c4a2080<br>SHA1: 65277ab4aa4e2343a37d4407ef75cd7b9577ce09<br>SHA256: 30a72428cfaf99539c901922da1a549a4e9635f9cd813dc24c43dff6412dd165</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>281.2MiB (294.8MB) – 2,444,157 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03a9ee13cf7bef9c5c8c0f0940f7d68d<br>SHA1: 76dd4832de692a91cac900713620ea3132b3d208<br>SHA256: f8c720b6ce16ea0971582e27752eb16eb5bb69ed472ed8330ee45a84bc6666c0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-09-17<br>IPv6: 2023-09-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.512MiB (5.780MB) – 235,008 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f5b6633d21428ca1b77b02bd93ccf8b<br>SHA1: 52d80d0117cb022e501c545e2ce94f0292f49302<br>SHA256: b7ec29dd99ff8c1b7df35a0e90a87fb1ac93c22dfd85334670687358c1b14288</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.53MiB (19.43MB) – 239,903 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0828735b19358ff575bc94aeb9fd5e5d<br>SHA1: 89731a1b44a22cddc2b7f5cd9cee902f9ea0134b<br>SHA256: 32050d76fcd8c0b1edb50d74e670dcdd6ec2c415a0c478c78b5b036bbb262e48</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-09-17<br>IPv6: 2023-09-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,035,503 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25939bb2ee9379027c7ed8b48c581ef9<br>SHA1: 0cc26f98398ad29837f913a430a0614477064fba<br>SHA256: a228f642ae927e8d72503c3daf7971e53068c745a86162a71f7c0ee85e3fcacc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 1,407,049 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9148267828dd02b4a07b8d71be61e05<br>SHA1: 3385387c9e1e91d9a4fefb58750dbd3ecf5b473f<br>SHA256: 84af78d046b164d3df6de0dbc9ec0d4555678bffc281df97f9793acfc4c09d03</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-09-14<br>IPv6: 2023-09-14 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.52MiB (11.03MB) – 449,053 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a763404de3dd17a5ed85aa0448e90cf<br>SHA1: 1cdc9fb467f3226b4a5338a939f91ca8e0d2406d<br>SHA256: 1a41877af7b92e87dbc1fcd7e96fec1b4d08b07b781455a636c2f48f8cb6aeb9</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>23.19MiB (24.31MB) – 300,152 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 096c19b7e0ed71c31e414864de9120bb<br>SHA1: 5f914b866ee3e823104b4dd65d5a0484bdb0535b<br>SHA256: 716af495f8b049420060f1458f75de856f646de4f7fcbf15282cbb4e6beed7ff</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-09-14<br>IPv6: 2023-09-14 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>191.5MiB (200.8MB) – 3,818,864 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06e48411bb06b84319fc8eafaf0a1e2f<br>SHA1: bad681beff1ac2247038c357b1be819908ef09d4<br>SHA256: 2dabaab5026f5f7787d1a015a3d6e0566393bf283a9e1bf50eac641015ff0992</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>224.0MiB (234.8MB) – 3,818,864 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5728df715044391666b83394de986f9b<br>SHA1: 6f44ae645e69e1dde6d816fde31a1403fc7099b6<br>SHA256: ac2eed7c73890ec23fb144995e4614cc7c422a1a882234b88c79a8ccdf42060c</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>198.6MiB (208.2MB) – 3,818,864 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1051bf37f4de0729cbf7664c5af4baa<br>SHA1: 0ef6d1a96ecbda6d6cddc20dbab79d29608a7486<br>SHA256: cc72262df0983802ffb1ec9cb820c2834cc6cac693fd04a8c4bba5104eb36e1d</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>205.0MiB (214.9MB) – 3,818,864 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b9915355572674c928edbb2d15c282e<br>SHA1: eeca2367a27eb0b6a82e2d0ee795f393fe4beb4f<br>SHA256: 9f25161277047a57234a07b86e6469b558115ebc8ecb25d87f1491d67667f2c3</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>241.1MiB (252.8MB) – 3,818,864 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71a500616fcb3db1066cbc90b0350823<br>SHA1: 2edab40c9ae9912f1e3e1aa509bbf3aa2c13a51d<br>SHA256: 1bfe03dbe4d62281c09158a407feff3fa3b90ae0b4208d717621dbf87ea928c3</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>192.9MiB (202.3MB) – 3,818,864 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31d11865ce8f23e854c61bdbbf17e89d<br>SHA1: f6607495e956d4c76c84a1f291c7f3131405a721<br>SHA256: 5a7f163adc3ffefc64db5cf4ab2bb930b7f54a67467fd98a8229736700520eb4</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.7MiB (252.4MB) – 3,818,864 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8aa2ca9eb1326d4296ae3acb03b2398<br>SHA1: 53f26cf758978390391f77ee7a626aaae1c2f495<br>SHA256: b077ab544602660ad61bcbe3010a2ab427c9978386f65a59001e8af989d0c8b8</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>205.2MiB (215.1MB) – 3,818,864 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c3ca9a13dfb2f89037cb04d9062a0e5<br>SHA1: bf1f342d4842604c4a98af26a764fca129ecbe90<br>SHA256: 995483a44a0860a27e04150887f0aae1d224dfc14e29aa81eb23c55454acaa42</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>132.6MiB (139.0MB) – 1,322,454 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7c54c4c1d5467ebddd0d71ceb27be75<br>SHA1: 0aef0a27f8d74649fe251148964f0e4bb3a4d1c2<br>SHA256: dbd588f7839495838102867070573e76c259e308456dac4f8ea3de52f4139d8c</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>141.1MiB (147.9MB) – 1,322,454 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74592a55a4157a4452d1bebb860ddfce<br>SHA1: f148726cf52f2980acbd28f26bf57425d56e51bd<br>SHA256: dff4fc29ed4690155c17ec5ea592bedbb38a956e9348cae3af038c2f31457072</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>135.1MiB (141.6MB) – 1,322,454 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be930781ec82be4570be27b68cf6859a<br>SHA1: b9bca3086c792b68ae89ef33381ac130ec7279c7<br>SHA256: e6b9263ae9892376c4796d734acc212f52a4dba0ff7b62e669160933cfca7d81</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>137.0MiB (143.6MB) – 1,322,454 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e3bb18365c550fa1a50ef92b6b98f64<br>SHA1: 42be0f584795939239716d673617f64402307e7a<br>SHA256: 80b0f8c9e0db7f7c2b0611b71a2a5a421889aac9ff44330ba42028c58abfc68f</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>145.0MiB (152.0MB) – 1,322,454 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c12884442e134a3d7078e57fab719231<br>SHA1: be61da8a67fd9da3982c2942f62e68f1035033d8<br>SHA256: 57dd26e405c688001f1779bedf9382d65976e9b868285bdca865d861382d30f4</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>134.0MiB (140.5MB) – 1,322,454 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c56f149caedd9b2bf8dfa1ae3f499f04<br>SHA1: ea162521952a98d281171129f3688bb4dcafbeb0<br>SHA256: ea4d4407061fe0009dcb89a04f19445e28d31ddfbb8b9ca1aca85a9eb348c997</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>145.5MiB (152.6MB) – 1,322,454 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e6b6a16ec7d112095bed49853daa588<br>SHA1: 30eac5eda839a430e7d0b9e3f4e13ac796006133<br>SHA256: bb5cb073cbd4ff6652a6ead0b2bacc0d1643d59bb18217dc688e9d862b0895d3</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>137.3MiB (144.0MB) – 1,322,454 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c882be3ca9013a693325ded921044e2a<br>SHA1: 2fb9b8b19de18bd11997aaa0390f2a4399d39ad7<br>SHA256: 20bf43b16e27bf9f72288544b4a9092a80f42c18002e4fb541d55e785e585367</pre></details></small> |


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
