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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-09-13<br>IPv6: 2023-09-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.640MiB (5.914MB) – 240,265 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f53aecdb742528c66c7d773eb9c42eb3<br>SHA1: 919a870b1c8ea7e55b8e5e84edba045c7ef8984b<br>SHA256: 9c2192f92a1ebd029da5d735df7d54bf8fe7819f220649b2c56764c0a38c0183</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.135MiB (6.433MB) – 79,415 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 419a83a0049ff4b868b254321d0cbbfb<br>SHA1: 72c88edd31ebe4b832fedb42f102f034b1c370ea<br>SHA256: dc05f7f783569bf79981ea1b8263dda5aa5dc402067546aea360881596c9aad4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-09-13<br>IPv6: 2023-09-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.572MiB (10.04MB) – 406,588 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0339947671d21dc9a017c8ca58ab5885<br>SHA1: 26114726578dc3f8331f06bf58dcee09f1094025<br>SHA256: f9da7fb5c456af9aaae8bcaa338858426104f65199cd266521dc8a40ba456f59</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.805MiB (8.184MB) – 101,131 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 384f380a84e80cc7b4a68b3fc7694199<br>SHA1: 19b49d00926c2a385f642287e19668d6f9d0c201<br>SHA256: 2dba404f60d0b348c22eceeec9617681232a5f957edcb512ca95591ec1795cd9</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-09-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.27MiB (16.01MB) – 650,726 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1782f1648e0f31a996e14f4695670a8e<br>SHA1: 647c2aac203b6a27b2668919b310e8e79addbfa0<br>SHA256: 779e10cf82a2ad1f70646c2094f884c1839ab0d029e004780d4ddaa64fe2226e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>38.76MiB (40.65MB) – 501,800 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e9c2c381569d65bd25b69efcfd0ecca<br>SHA1: 71f4913534c570dadf7da93f2a3457bfff8b0366<br>SHA256: ebbc11b350b73f68c0146918ccc1a3e8bd6b4098d6eebbc33aa9423db10bdae2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.416MiB (7.776MB) – 317,712 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8af33754952bca633e2643d56b9b3556<br>SHA1: 635e2f9c397074c2d69ffb9220affbfd86ec55f6<br>SHA256: 3ebea563a71e9352b6b395144accf2da57a57d06e4f59e570f279b0f7dd0b26d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.32MiB (27.60MB) – 340,762 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eabb53c9e90baf81be978b9f452f9fcf<br>SHA1: 926f5a148ab14f14ab51042d5e540547e30fdc1f<br>SHA256: 1fc208ccb6c914cdec8d9914c6bbc9c49c7d9cc9dfb2403391c007a74eb2b066</pre></details></small> |
| | | Full Location | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>190.1MiB (199.4MB) – 3,137,207 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2af38dd10686ebd6a86c594c3c4a2080<br>SHA1: 65277ab4aa4e2343a37d4407ef75cd7b9577ce09<br>SHA256: 30a72428cfaf99539c901922da1a549a4e9635f9cd813dc24c43dff6412dd165</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>281.2MiB (294.8MB) – 2,444,157 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03a9ee13cf7bef9c5c8c0f0940f7d68d<br>SHA1: 76dd4832de692a91cac900713620ea3132b3d208<br>SHA256: f8c720b6ce16ea0971582e27752eb16eb5bb69ed472ed8330ee45a84bc6666c0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-09-13<br>IPv6: 2023-09-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.512MiB (5.780MB) – 235,008 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f5b6633d21428ca1b77b02bd93ccf8b<br>SHA1: 52d80d0117cb022e501c545e2ce94f0292f49302<br>SHA256: b7ec29dd99ff8c1b7df35a0e90a87fb1ac93c22dfd85334670687358c1b14288</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.53MiB (19.43MB) – 239,903 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0828735b19358ff575bc94aeb9fd5e5d<br>SHA1: 89731a1b44a22cddc2b7f5cd9cee902f9ea0134b<br>SHA256: 32050d76fcd8c0b1edb50d74e670dcdd6ec2c415a0c478c78b5b036bbb262e48</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-09-13<br>IPv6: 2023-09-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,035,503 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25939bb2ee9379027c7ed8b48c581ef9<br>SHA1: 0cc26f98398ad29837f913a430a0614477064fba<br>SHA256: a228f642ae927e8d72503c3daf7971e53068c745a86162a71f7c0ee85e3fcacc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 1,407,049 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9148267828dd02b4a07b8d71be61e05<br>SHA1: 3385387c9e1e91d9a4fefb58750dbd3ecf5b473f<br>SHA256: 84af78d046b164d3df6de0dbc9ec0d4555678bffc281df97f9793acfc4c09d03</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-09-11<br>IPv6: 2023-09-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.49MiB (11.00MB) – 447,542 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb80fdf1f4b3d2207b46e8b43ecf4624<br>SHA1: 76de56d7dfc9961d415744dae2679165d546c80d<br>SHA256: f818ceff278fc561f38662e245b5ffd035972cf9a7de67b72874fe2db6176e90</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>23.07MiB (24.19MB) – 298,601 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 867bcad0e0ac323cd502eb2be9a0acd6<br>SHA1: 6c9eb3ed2775940933a11933082caa066daa08ae<br>SHA256: 49e15fa833b03540196c29ef2cf25d057e9c501b5ec727623aaeb2006508b45a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-09-11<br>IPv6: 2023-09-11 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>191.7MiB (201.0MB) – 3,823,607 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d085388587038b7fe29388b318273cde<br>SHA1: 352bf93b0aa7d4d485039e3d0d94afc919ea2189<br>SHA256: faf02462d8950e8e69bd66b130374b6cbf50e6065fa66513a548a972226241ac</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>224.2MiB (235.1MB) – 3,823,607 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dea2f8306e4b4c9e1727deb25c50e8e5<br>SHA1: 22e67dbe307f9c843ddf2bf8f3e7f776b1ab6978<br>SHA256: 4d251ed110e6ef2262caff0a0acf0d2ec48edddc2da25a14c7f8305be19edf70</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>198.8MiB (208.4MB) – 3,823,607 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b978a107a8cd72cafd25da5d6519f8a<br>SHA1: 1a405f628bdd5318ffb8bd5f77f56be79d940267<br>SHA256: a52cbf3e5a62bbafeb84c4392bebd43aee736e1ce62e426c1704d629716f97f3</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>205.2MiB (215.2MB) – 3,823,607 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 400d8905826fde844cdd226bf381a6e4<br>SHA1: 31f3ef06cb5da54f14d1240a7fb93233b5742d59<br>SHA256: 7ccc4692f0b8c4b842eb60afff8c98493b48d6562ad530f5b3918bcebc220aea</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>241.3MiB (253.0MB) – 3,823,607 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a74afbb647fa01c2ff4ebdf3f33b4db9<br>SHA1: 0c71b12b74c324ac56d7f29d9ddc6a2e970e6689<br>SHA256: daaf7e73576a6a839716a6e7ee8d1a01d6350b31d3fad9d2c2dc849aca0ab3e9</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>193.1MiB (202.5MB) – 3,823,607 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5e7bd11164c265a3b3f726fa717d90f<br>SHA1: d9d05437386fec532254f4013e93c5b2dfd65330<br>SHA256: 9f784a20d73824a4d30879464dd3577b5d0fc1bdecc54b4578e49f5741b68f2b</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.9MiB (252.6MB) – 3,823,607 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efaf2ac9ae1da0fba690033cfa42005c<br>SHA1: 156dbbe6c6b780217223f2338a2a6a4cc0522d5b<br>SHA256: 208f0758790e7e2fa009922d352bbd2958f03018acbc2bbf27631426551b6c47</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>205.4MiB (215.4MB) – 3,823,607 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4de30d79f0c78d5ecbc51148aeaeba81<br>SHA1: 88b297ba6ab474747d949c8195afc21775c8ebb8<br>SHA256: f6b81a545878e10bff3e8f817f6856054da0f0d57a04b8133658e9c6b3a4a089</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>132.9MiB (139.4MB) – 1,325,214 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a300d9be50d01e0a09d263b11e91a6f0<br>SHA1: 1c9041992a6aecb7d9dbd5454e0513f27e8aeb23<br>SHA256: 133daadf19e92f24dedc2fe24876d31eaa31490fd7690d1592424fadb30556c0</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>141.4MiB (148.2MB) – 1,325,214 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85f2fd5dcef60890c2f38a83aac75004<br>SHA1: 6629d01ea781d8226efeed8e43772cc236883707<br>SHA256: 8c40c711a66441d712972e9f9498cf9193618949240f7e31696666edb9e91ed5</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>135.4MiB (141.9MB) – 1,325,214 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b8f903bf6afda19d35c8df34416e0b9<br>SHA1: e8d2606377593f5e7705a4afa1763d6f4ab408d3<br>SHA256: 5da65b8bcdf1f1d367e17c6d36c103d4fddec611935353d209487a3a9b4c93da</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>137.3MiB (143.9MB) – 1,325,214 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f592f335900cd7d3c414043df1ee3f6a<br>SHA1: 9099e660f043e8c24d500773302b3175d32b6296<br>SHA256: d9c27ac110524ad749fb0502bc1eb14dccff96b9df8f8e4807bd2436e34af243</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>145.3MiB (152.3MB) – 1,325,214 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fbbef71338c2f026e2e18c9eb20c688<br>SHA1: 0770c6298d333a0659f0d90e7defc24ed15ec6ff<br>SHA256: b3e6256f36f38395eae45a74cfe93779c8882db2c05dbfe391d2d88c6f215fe3</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>134.2MiB (140.8MB) – 1,325,214 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6ea5c214cda6ce7e975ff2b31f4da1d<br>SHA1: 6267c616eafab21e2d6c9e0d4752ddc28696fd67<br>SHA256: a27ce3bea7401fc430015a40006c5ac4f2b02fd16aa1ef1b493c73cf886692c0</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>145.8MiB (152.9MB) – 1,325,214 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21e29441335487230a1419f104d48a1b<br>SHA1: 0e8f4ce98686422f7252fb6ef4a6371454d5de1e<br>SHA256: e70ab9a0e20861a5ee17e9103a68b922129603ef869740ae5974a31636828b04</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>137.6MiB (144.3MB) – 1,325,214 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4528e1875fb59461a2f6a4eb6ca78cae<br>SHA1: 27d8e55852bf3509f0723138fb91b5cc20173f82<br>SHA256: e957c380cb16b0905b76a0cf163b60a6aa2dca57bb9752e07696f4c3bf33452f</pre></details></small> |


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
