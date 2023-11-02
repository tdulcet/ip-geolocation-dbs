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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-11-02<br>IPv6: 2023-11-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.589MiB (5.860MB) – 238,060 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3c095ad93879aa496a46e61ecfcbae2<br>SHA1: 80021b4fb58df4726a94a9f9612eb0723deee0e0<br>SHA256: 4e4a9e44d130989ddac60edf10e5c4cd3d57abb11efdfba9948a08b711e32a0e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.264MiB (6.569MB) – 81,093 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf5e41aaf7437d644cff0b6375380cd6<br>SHA1: 50b4a0a467b35b214fa52d0e332a0221d3d9c6cb<br>SHA256: 2542117ce00d047af47a98dfeeca67cee48e3951a95fa8597d02059e73ef30ed</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-11-02<br>IPv6: 2023-11-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.645MiB (10.11MB) – 409,675 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e194671a7b0e5c9deeb4d51918c3750<br>SHA1: b6ad544319ee3f2b9ff30661ea1f953fe2a66feb<br>SHA256: f2a824416ec9eae23203d36889d768df02de669046fd033090be938de6bfe352</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.032MiB (8.423MB) – 104,081 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf3ffbb8d04b1eb350b4cb367d0cc96c<br>SHA1: db2d158b5bc8dd59919fdb7375a91717dbd2ea13<br>SHA256: 6696015deea546cfbf0c9eb085adf85a3c75f16ca1c2ec12623f79814b6276cf</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-11-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>18.80MiB (19.71MB) – 799,133 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48d5f2ce7c028ff584dce786587ab9da<br>SHA1: be7a6977459984f728db1ad9ce3b18c8e5023af1<br>SHA256: df54e2860f71eab5503d1ef74de349dd7fb1f20af6475cd2d763f87ba63a6413</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>41.69MiB (43.71MB) – 539,687 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6eddeb230cd5f795c33487b10f944501<br>SHA1: 4c49ecf0a4e295c6e29950a9ef4bf93c417fcf92<br>SHA256: 4ebfef5170e0cc2d9dce68865745df8c2f094d7094e6f0d1ffb0081b222965c8</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.260MiB (7.613MB) – 309,964 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7fc3106cf6c65db7d44df8b4fb1d16<br>SHA1: 6ec97588db0af32a305835217289c32883d23f64<br>SHA256: 9bc7152bcf323316fc78e69cfa190cbddf22834208f48cee2e624c18150c9478</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.63MiB (26.88MB) – 331,798 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264a68f442d85aea134072d7bca0f4fe<br>SHA1: 65171ab00588cb7f2ae029d9345b44cccc888d24<br>SHA256: f76d40c34e6881d9cf3d98b34ced8105e9bd9efbb3f55e2bc224ece181569030</pre></details></small> |
| | | Full Location | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>186.8MiB (195.9MB) – 3,075,320 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96e5fc94ee00f3349281d3d79c8e3e83<br>SHA1: cf6b55598525f02890d9596fefd546190401adc9<br>SHA256: 5dfdabdba40afb770f6ff5afcc35db6136e9e28182bd6b3fd23b3c203dca5d1f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.3MiB (303.3MB) – 2,504,397 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bcf1dc4f4611d3e39906c6048aa8fc<br>SHA1: 2cd36733f3043bb3d9985d20fa8416a68b122e30<br>SHA256: e3d5ccb9e02dd929dc48ad40f82d484f9ffe60f9098c5a3ac296e33c5b9c2a9e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-11-02<br>IPv6: 2023-11-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.446MiB (5.711MB) – 232,323 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f7d79b6a3ef8bc35c3c8381e7c028<br>SHA1: cbc8e9cbd5c151f0cdb02a21e5e6fe9d8b662cc8<br>SHA256: 9f3976e09ec875d7e97185503221656e80f41f531e268da1bbf874127de2583e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.41MiB (20.36MB) – 251,316 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df2ea3be7027267ebb1947b4220cc4b<br>SHA1: e94b6a993297b5dff456113130c22e323534e39e<br>SHA256: 44458ed651d7b4bd99ad73459d500395c410da1b2fce9fbb2c4e5ce318c4bcf9</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-11-02<br>IPv6: 2023-11-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.3MiB (180.7MB) – 2,814,468 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25688ced507227d7990066c41a0d58d6<br>SHA1: 28da5022ff88d543bba4e15cc01b703781801bba<br>SHA256: cf219cb6d358d6e4df364a87f28817e4aaf8322370b86495ef74cc1941c73f5d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>171.4MiB (179.7MB) – 1,495,017 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d4ab0c657ede6538d2756cef356f5f<br>SHA1: c2865c0d416ae7143165db8aca21627725b4b45c<br>SHA256: 66022701ed347d75f4f400e76024ae545696e742e4c0fd30bedf981c262b318b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-10-31<br>IPv6: 2023-10-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.74MiB (11.26MB) – 458,587 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b42af979c727e681ecb6c304ebf0386<br>SHA1: d42ca7b45cb9a9d0acd820a3479283b5adc47acb<br>SHA256: 945b3c63b0f2e28e1b6cfb33b503c1c3fa7b41a2646e1b615040130a0e307967</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.80MiB (23.90MB) – 295,097 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd59e5fcd16a059e169c40f63b633530<br>SHA1: 5c09fea54113ca94b5d99d8d543625e9531149f8<br>SHA256: 8e4598b72b8079e167858fbf9510b38a62618356066cc0c4075d837c2847b7d0</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-10-31<br>IPv6: 2023-10-31 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>157.6MiB (165.3MB) – 3,127,292 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c960632ede62f255692a643a2be21a3<br>SHA1: b97e9ca75262afa29c653b5ece612bb59f7dc906<br>SHA256: eb9050ff91ec73a1bf7a25838f647baaaa93ad734c27712df483cbeaf3c62678</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>182.1MiB (191.0MB) – 3,127,292 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e907e13de7080105bd73cc89033c56f2<br>SHA1: 79aa08db91ccc6b1f06febc07182527f2f0a80ae<br>SHA256: 69d8fbff1a5f108a356aff85ce99249721b19d0ad915f9229612f1706c01924c</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>161.6MiB (169.4MB) – 3,127,292 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b0a05b99e483702c368f5def9a0813b<br>SHA1: 4d58137f7c7e146bca8e3680c458e2b736d6edec<br>SHA256: 46c3340217ef30640c814eb0620de1768117871c9858485c8cce19f271de2e16</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>167.5MiB (175.6MB) – 3,127,292 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bfe4b34094b6aeb401767c32f4a6e663<br>SHA1: 1b5078d0a7b9993a3bc79560f65487373b3ea9d0<br>SHA256: f77fdf5e1461aebef811fafb9e27f33062a41e09894be39a7ded4e1a717a81e0</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>190.9MiB (200.1MB) – 3,127,292 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b7ee2a1938ba8b193889045b6f33b88<br>SHA1: ef3e11161802ccab21d863614772dd6678b5d5e2<br>SHA256: ecb76320014cb03ed71be15a7bc56717df27826d3891c646b9076fc1acfc5d56</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>156.6MiB (164.2MB) – 3,127,292 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6af152e6fe6180495ad9e28f651d29d6<br>SHA1: 6a25a44553183890e4b9bb4f059adfb3192c3b65<br>SHA256: 6b79be6d4405b75ffb3a4f9b88aed31b662a4c1286a89e0ad0ce02a508b1e0cd</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>192.4MiB (201.7MB) – 3,127,292 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f77c25c58646ea5f2580ba93cae30d13<br>SHA1: fdbe034714101fa39e8c898cfefea883a897f551<br>SHA256: 8a6dae8c9eb1bc859442baa800a91f6d0e78c1656b6965d46fe1d3f6f67ceb8d</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>163.2MiB (171.1MB) – 3,127,292 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7830f4605a6da01acf0cb4e138ced558<br>SHA1: f85803205287ea90111bf709821392c98a376098<br>SHA256: d6c9f4a4beff296b44112e4c0ff2349097e2187459b5bba5b589404f7dfb76ab</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.0MiB (127.9MB) – 1,211,633 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 069b9784c447dfc8bc7da73d910aff66<br>SHA1: 296978afc1b3a14873dfd619becd781ffb34c113<br>SHA256: f61c55bf952978b63b46de43d6e61f67a7c09e3dbf8c7fc84cb6ff956de497eb</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>129.5MiB (135.8MB) – 1,211,633 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bef891924078b40c8f5ff55239b5080<br>SHA1: 08455539423853322499ee6d66479d0006a0e196<br>SHA256: 53394ef49eaa6f44d90dfc14293dd675f78f7a3f26fe143723ea10f80b95546e</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>123.9MiB (129.9MB) – 1,211,633 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e0033d0e7db0f2d522b2ccfd4ed8939<br>SHA1: a051e26bcf4e0792d2273e0350a708d35e9e9ceb<br>SHA256: 895e68b720c563e292d3ae387cb4e7e0150865214a468cca9f3f6e3d92fa1195</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>125.6MiB (131.7MB) – 1,211,633 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 707a9ee67b2a944f732c678a9933c7e4<br>SHA1: 46e17fe4b143084da99cd81d0d5e86a38c3f4727<br>SHA256: 387651326117e8e8cbe877bf0d8f4ab0e0070a58580f4140a608fd28b9924af1</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>133.1MiB (139.6MB) – 1,211,633 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 943066a99016cf5ccfe170f098147b49<br>SHA1: e7f23bfaaf83e8e6ad2e9100a481295ca6e7629e<br>SHA256: c59278576f70accc8fcccf4001d91e90d73065054149d6c8f1fa69422aa2d4d0</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>122.8MiB (128.8MB) – 1,211,633 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74f58c3dff3cbff2f3777ddab2a218d7<br>SHA1: ab08a829345e823f413badf0b4922c9150764ab8<br>SHA256: db20bc2f5912c182773abf148a33fc4c916131cf1d94c7c828e26bd9448701d1</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>133.5MiB (140.0MB) – 1,211,633 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4915af7d55543e563270530d0df48a60<br>SHA1: c1cb2e1f2537fc7574bd96d2ef8a303dc955a57b<br>SHA256: 35cfbcb295423e9e4b3c4b1ddd8c65848f34622d45415f78a3a182e4d3d125a4</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>125.9MiB (132.0MB) – 1,211,633 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3afb5166a011eda173ba75049dc62dca<br>SHA1: 4abfb9395bc360d08144dcb4137a623615adb1aa<br>SHA256: ad470fe8a63a1f8946130c87daad865b609b543e689eb1e9826e85cdad9e00b1</pre></details></small> |


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
