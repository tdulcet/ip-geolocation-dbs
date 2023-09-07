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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-09-07<br>IPv6: 2023-09-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.637MiB (5.911MB) – 240,157 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8486d24c42ced41612514862a508df0<br>SHA1: d26a3bfd73b0b4228a734dedc3fd7587386eca02<br>SHA256: 2bc2f80917e1359a5c1a43ac3eb0596ebb102556e981430b40ec732204fbc086</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.090MiB (6.385MB) – 78,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ed655eed4121c1f928261c6c033f1b9<br>SHA1: aea2b3a3274b0ed1737213103d1bdf522d624db3<br>SHA256: 866de6c3f187bc9cc7958bea8063fe3ea13bb69b451a0b94caec6dba04d4367e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-09-07<br>IPv6: 2023-09-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.553MiB (10.02MB) – 405,767 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f4197432d39a567071ea48f920f3b8c<br>SHA1: 5e3f5600377f431d3361923d506d612d907b98a2<br>SHA256: 051fe28fc8313b66f58d4f3178407af4370e1d9b39a7c4e9b710429c8487cb30</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.801MiB (8.180MB) – 101,082 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b6b70a0a7471509827c7ed7dde24dfc<br>SHA1: fcae1bc0c6249d49cded94f22c0dc4ef7b6bba6d<br>SHA256: 0383d411c1576c133527280ca7f9031bd378de4bd8787c62bdf6b162bd4564b5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-09-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.27MiB (16.01MB) – 650,726 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1782f1648e0f31a996e14f4695670a8e<br>SHA1: 647c2aac203b6a27b2668919b310e8e79addbfa0<br>SHA256: 779e10cf82a2ad1f70646c2094f884c1839ab0d029e004780d4ddaa64fe2226e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>38.76MiB (40.65MB) – 501,800 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e9c2c381569d65bd25b69efcfd0ecca<br>SHA1: 71f4913534c570dadf7da93f2a3457bfff8b0366<br>SHA256: ebbc11b350b73f68c0146918ccc1a3e8bd6b4098d6eebbc33aa9423db10bdae2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.416MiB (7.776MB) – 317,712 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8af33754952bca633e2643d56b9b3556<br>SHA1: 635e2f9c397074c2d69ffb9220affbfd86ec55f6<br>SHA256: 3ebea563a71e9352b6b395144accf2da57a57d06e4f59e570f279b0f7dd0b26d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.32MiB (27.60MB) – 340,762 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eabb53c9e90baf81be978b9f452f9fcf<br>SHA1: 926f5a148ab14f14ab51042d5e540547e30fdc1f<br>SHA256: 1fc208ccb6c914cdec8d9914c6bbc9c49c7d9cc9dfb2403391c007a74eb2b066</pre></details></small> |
| | | Full Location | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>190.1MiB (199.4MB) – 3,137,207 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2af38dd10686ebd6a86c594c3c4a2080<br>SHA1: 65277ab4aa4e2343a37d4407ef75cd7b9577ce09<br>SHA256: 30a72428cfaf99539c901922da1a549a4e9635f9cd813dc24c43dff6412dd165</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>281.2MiB (294.8MB) – 2,444,157 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03a9ee13cf7bef9c5c8c0f0940f7d68d<br>SHA1: 76dd4832de692a91cac900713620ea3132b3d208<br>SHA256: f8c720b6ce16ea0971582e27752eb16eb5bb69ed472ed8330ee45a84bc6666c0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-09-07<br>IPv6: 2023-09-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.512MiB (5.780MB) – 235,008 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f5b6633d21428ca1b77b02bd93ccf8b<br>SHA1: 52d80d0117cb022e501c545e2ce94f0292f49302<br>SHA256: b7ec29dd99ff8c1b7df35a0e90a87fb1ac93c22dfd85334670687358c1b14288</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.53MiB (19.43MB) – 239,903 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0828735b19358ff575bc94aeb9fd5e5d<br>SHA1: 89731a1b44a22cddc2b7f5cd9cee902f9ea0134b<br>SHA256: 32050d76fcd8c0b1edb50d74e670dcdd6ec2c415a0c478c78b5b036bbb262e48</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-09-07<br>IPv6: 2023-09-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,035,503 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25939bb2ee9379027c7ed8b48c581ef9<br>SHA1: 0cc26f98398ad29837f913a430a0614477064fba<br>SHA256: a228f642ae927e8d72503c3daf7971e53068c745a86162a71f7c0ee85e3fcacc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 1,407,049 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9148267828dd02b4a07b8d71be61e05<br>SHA1: 3385387c9e1e91d9a4fefb58750dbd3ecf5b473f<br>SHA256: 84af78d046b164d3df6de0dbc9ec0d4555678bffc281df97f9793acfc4c09d03</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-09-05<br>IPv6: 2023-09-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.49MiB (11.00MB) – 447,697 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01ed2386d7a623e6d460659fb5162392<br>SHA1: 78f9822b13432d071b7a9f62ce5511be839f6773<br>SHA256: d3261702ff37bf5a7361e5b7a9c0d0ff94a115b94b7d32242a580e409377a2a0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>23.10MiB (24.22MB) – 299,075 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0f3e8f44ebd09fc2057cfde7a8b5166<br>SHA1: b334da3a0ba9fa844d6706703a14d8ee5c9026ef<br>SHA256: 5bc83d739976896dd57656e332e418df6af0fb95481e260e390df1e287ff86de</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-09-05<br>IPv6: 2023-09-05 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.9MiB (199.1MB) – 3,787,783 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac8ded412ffdc9380ff48aeac2f32c4e<br>SHA1: f799bca531336553f4485adefa602dfc44da03fd<br>SHA256: 5b76b27de2368455007faa37ec17cc6b3e044fd97649cbc3b1c1a92171fb0b2e</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.0MiB (232.8MB) – 3,787,783 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54910d87c53d8c4c2b36e2c324c05a7a<br>SHA1: db250a5c876dd03bcd49b300b30c9ac1ec807e27<br>SHA256: 53f3ee96236907b0ab5b858eb3c25576ac45c5aeff2ccb7e943a062dfc01b504</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.9MiB (206.5MB) – 3,787,783 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f51fae3815736feb21e3e49a6f85d8ff<br>SHA1: 2a7354607bd85077eec57f67101a77942356e44f<br>SHA256: 46cebd379c534f4b13ce138ab0698b0999606fd5089604b61b510640a25de2c5</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.2MiB (213.1MB) – 3,787,783 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fdb24101925ec756ae94ca1e7199f074<br>SHA1: 7c827326692b4bf91b031916b8c2e4722e609ab9<br>SHA256: 9b31148980a10b23bf1ee60d260dcf3b4f36b50812a538837c77087aec357085</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.1MiB (250.7MB) – 3,787,783 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96dc94a4775a8b5c90414ac0a978f6be<br>SHA1: b39a50e990c162f1e804c2b8e4213131f7859b64<br>SHA256: 9843cfe8ad36d1ef29451117262c3d14b1134eab68012b6bc7f923013759f411</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,787,783 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19e26549ba305465b643b37ec53cac08<br>SHA1: ab44775440b98394566feaa7b74fd2b76d77a31a<br>SHA256: d84c262279792bbd2baa986bdb637b4fdb17eede0d8e74c4e9b8ea33ed32d0ef</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.7MiB (250.3MB) – 3,787,783 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3118429c1d557b721969601d67146320<br>SHA1: 7c71f2c5e2216e227a461535197dc1bf3edd5296<br>SHA256: d407bba917084a88c1f2fb9aadea6b4797aa29f305fbb4c2f4c10927ebf65deb</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.5MiB (213.4MB) – 3,787,783 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69495f540cbe281923f229ab5802527f<br>SHA1: 0e9e50d6fdf447f73a3abb21e9fb68c2d00ed171<br>SHA256: cd2e0c29852b51775fc9c6a059ec12f44a5ccecc079edbfd7c2f3fd47bb316c7</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>130.9MiB (137.2MB) – 1,305,185 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8a0b1bfc2d72c5b24616c2e6a3d41ed<br>SHA1: 36e48cdd236eb1097449bb1299cf5aef02d47d95<br>SHA256: 0866ae38a9fcc7e61fe79a043901b77e29c56cca9a2e250125464a0690ccdbed</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>139.2MiB (146.0MB) – 1,305,185 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5c766107f3bc0b315413824b27f9335<br>SHA1: 35716f3a1ff7f74adb9bbe1036c9a7b00579971d<br>SHA256: 955bdc290a3d50be76d9d99141070a3258e2da931af45f651f9ef05d23ccb500</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>133.3MiB (139.8MB) – 1,305,185 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c9a451b95f02c33e500cca19929f807<br>SHA1: 6906f4077bf02b0b1806f86e2f7ac3c9e6255aa1<br>SHA256: f501231131ba9feef9950e8270f26c0ae314aa45c65d05c25dd5b165237265ef</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>135.2MiB (141.8MB) – 1,305,185 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 239e2d8a092af40980f5bf62403d670d<br>SHA1: 2668b8b4f2576fd453e0abc6a14cbc0ddd5f69c8<br>SHA256: df9835b9b854eb760839ff63fe45ac1a25914ea63317dbf5c6b6873d94c2426d</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>143.1MiB (150.1MB) – 1,305,185 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d7f098d85cb274fb11340d69377bea8<br>SHA1: bcf58efda50c2c02e96f47a96162d31a878bcafa<br>SHA256: 7ed494fd1723e1a222d4863f2e92e1e7e4b893eea4b30ba8846b51c16c3eb791</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>132.2MiB (138.6MB) – 1,305,185 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f468f2b1ea367db917cd09edd52d48c0<br>SHA1: f6e6714cd24879c425133ad7dacd29274da6e3b2<br>SHA256: 777e80bf060a3cff439e453b879940d8c5d2d30d16048fc9c9ce091895743fe2</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>143.7MiB (150.7MB) – 1,305,185 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4bab92bd9dbee54a5d22679980a2ac4<br>SHA1: 3b91d21fd3e6554e7cc27c57ad5ef37f8dd0691f<br>SHA256: 0c48da0a9540e44bdcb118c4fbc5172b18c1ffddafc1c0e869f48147b53c6cc9</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>135.6MiB (142.2MB) – 1,305,185 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6043a7683d091b9960add0a1af70bac5<br>SHA1: 20da849d3612673656fde116c5d30f5b957b5d2b<br>SHA256: e312ff08bea78ce9938a323d77cd8afe064c09d0c15d9f69e086d2aef36d90be</pre></details></small> |


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
