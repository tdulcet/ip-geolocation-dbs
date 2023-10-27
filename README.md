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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-10-27<br>IPv6: 2023-10-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.615MiB (5.888MB) – 239,165 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2001587c13abfda73a0432ad6182df37<br>SHA1: cc7467d74ec25e55696f668f70a10ae225b925eb<br>SHA256: 3fa243c21466745d926d33385624425ff46c12f02caa95a8204e6cff2d94a55d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.394MiB (6.705MB) – 82,778 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 239e53c28766056be412cb792a2c72df<br>SHA1: b318d2748977649f8fb690bf00ca61744bd699e2<br>SHA256: e768ef53f39b05ff3d00ff1d5bb338aa9894019d0721ca94ccb4caa764e32d7c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-10-27<br>IPv6: 2023-10-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.637MiB (10.10MB) – 409,314 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1fb6f840aebb38aacbe956cf46688b1<br>SHA1: e6904dee0f674704836c19f68a314ae34d31004c<br>SHA256: 9b20896863aea44a23401a77511d45cf227d3b7728f5c228ca097201717a8e48</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.134MiB (8.530MB) – 105,402 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38dd8c0d5422180fe6c2a5bde6af740f<br>SHA1: d1b77e13a28b7506566c15f6f0ac8d7b2f834e48<br>SHA256: 3d20423420918f1e9af24ed12209177da92965a412cd88c3c1df0adfb3d5e65a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-10-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>18.12MiB (19.00MB) – 771,334 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bce7cee1786cbbaaf8b87de39be6a00e<br>SHA1: cb883716e079fbabf3bc5b554a2a8a028a181360<br>SHA256: ac845163254935fdb7eec7b7eeeb0f318af1bdfb45db5daac2535ea686223708</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>41.66MiB (43.69MB) – 539,342 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9391eb9e26adcbf7a8fcfe97dcb51df3<br>SHA1: 98ce3aaa48dd311a5b05d82f26f971fa7313a98c<br>SHA256: f4768ccc30518e9f3949f666f3823001bb9030f84abf8077839767e5161f297e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.207MiB (7.557MB) – 307,820 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ff8d81d8ce4efd3476359318175af0<br>SHA1: d105d1c4490b536a83d0461759256799109a17cc<br>SHA256: 4cb45f08b0bbd6d6c4fb204e776835b939ac663761aea652d12ae2ab20494228</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.54MiB (27.83MB) – 343,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3256ab7e4df24ca9917bf92c70b9ce1<br>SHA1: 832b96b707911579f91d2a42cc84b0766c5db738<br>SHA256: fdb03997e4b7c1a6bdffa274673b7756d8dbfb2ede55f1186b3957ade7042544</pre></details></small> |
| | | Full Location | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>184.9MiB (193.9MB) – 3,048,591 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed65f47a5f866d476bde81f05015d0ad<br>SHA1: b0ef2e2cdf8875da35c99816df76f9fa88d3de9e<br>SHA256: 5bca8efa9618ae69c9fe4228342c0ec4bfb4d581ca0766a3a8e45978d1fe7875</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>269.4MiB (282.5MB) – 2,345,213 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f854d9364b9ab55744dfdc557c9f9f6<br>SHA1: f419e9a0b9db7b3c78b5c98927c74c8427f3fcd0<br>SHA256: 3d1595b762a094dfd2f9ac1525dcc77a67ac87dec747f420b0fa63ac4fe51cbb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-10-27<br>IPv6: 2023-10-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.547MiB (5.816MB) – 236,500 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4857bb88f1e540efdbadfb3e56c208c8<br>SHA1: 0190e03fc0543a58ca868f0f36a92556049db942<br>SHA256: 44b7a5f1e09f7ad797ea8511ecfc8ddada844067bdff82f4255273d85906d172</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.24MiB (20.18MB) – 249,120 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5105fe9bbe5d0ddc9bf8995e1cd8fdca<br>SHA1: 48b9366c0983f8d70d79ad112999057d17d64829<br>SHA256: c10da1d1999f1867044c9753957966c4989400bf25df0e7fb02c524b43dc90fb</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-10-27<br>IPv6: 2023-10-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>171.6MiB (179.9MB) – 2,803,356 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4abca24edbdd7d97ffaa621ecb9327a9<br>SHA1: 97c24a0d18b54cd8d2692e708765b79162107242<br>SHA256: 903407a226a3eb479f2165ba004762c64c3a41dd5a9c0d515be1353f99e5796a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>166.3MiB (174.4MB) – 1,448,721 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d928761a3b79f2ef6c55ec6d4dd813e<br>SHA1: e7de15f34cace41d4332e3d59c8ffe729fc2f8ec<br>SHA256: 613e34be98c76eab733c9982022bfa16a5d1ab57fd73444f0d6e8a2ef59ae567</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-10-24<br>IPv6: 2023-10-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.70MiB (11.22MB) – 456,957 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18bc30169d86970a077015f8d7cf0286<br>SHA1: ce6b21415419fb3526df521653b472a299993517<br>SHA256: 406fad48df67fb32dd23beecf7dbe796131639fe4f5dd68cf33c14229e320ef0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>19.00MiB (19.92MB) – 245,973 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbfd4b6063fb95083fe2d52919afc851<br>SHA1: 50b95303daad04ff4c772841e2638d9f475f1ec7<br>SHA256: 6242a68581e79946f94b5c09d07c516b1c8a789b099444b0ee2a3bade2c7c3a6</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-10-24<br>IPv6: 2023-10-24 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>158.2MiB (165.9MB) – 3,138,805 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90efd103ab42fb21d3be4b5e08262007<br>SHA1: d51da25bc7c965e87daf08665dfccfd53b13552b<br>SHA256: 616ad540d0846d6c95c854868c0e38a31b26b0dd1259ace7196d25f97d25c054</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>182.9MiB (191.8MB) – 3,138,805 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 868292cee666c6f39d80cfb92c02472e<br>SHA1: dcbdccd27bb564422df22bb34edbae528b708050<br>SHA256: d3dfa58d463f557aa28553e321b4b66d1f3f044b6782366b12fed60bdd749176</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>162.2MiB (170.1MB) – 3,138,805 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 804ea81440f7c83ccb3fac2eb6dbcaad<br>SHA1: 40ebf4c78ef61493645058767eb8974e4c9d4d33<br>SHA256: 8e241b4a3904fe1fbe31c2e385f5121ede8bb25915d9fc34dda2169b7235661d</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>168.2MiB (176.4MB) – 3,138,805 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd0ef64d4fa08b61bf5705862abd2191<br>SHA1: 99212e09a226dd64d3412130a6736a722ab72482<br>SHA256: 8488442e46534df74e91fa33da1b3f0a9909c79d659fba72533ce8bf35519a70</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>191.6MiB (200.9MB) – 3,138,805 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5ead23b84b4d0216d1e8202fe7c12df<br>SHA1: 07ddf04d47f4a82277b420f1d826a3d66c49977e<br>SHA256: ccc4434ddb336f649d804d2ac3bf858571aec90d3752533c24f761113f7cfb77</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>157.2MiB (164.8MB) – 3,138,805 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26d5f7ae511bf33957088d7f8e611705<br>SHA1: 54aac1c82c1911854ae06050eb5e2beafdbd4061<br>SHA256: 3d13941bcdd336b735da6376fb1d2a3de3f18cc1956223ba1b33f89393bc90c4</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>193.1MiB (202.5MB) – 3,138,805 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9cc498c399a0f113950bf3f74377544<br>SHA1: a2486bffd0de42800da329af0fa6d9f2a6e27667<br>SHA256: ac7b9c90be14bc806dde4ea00e20473f780845e053650a888077c6726b33646b</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>163.9MiB (171.8MB) – 3,138,805 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6bf28dbf83f1bbe8e099d753651d2e1<br>SHA1: b1bef57aad52bd013e2c97ea4508d00e65ea0a2d<br>SHA256: ef360d026cc0d862ad080180aacec7b9935c285be8cd88ae62890a6b8701236a</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.0MiB (127.9MB) – 1,212,485 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2610a96a1557a2d012bc0664c26b1b3<br>SHA1: 6a2a02f06ae8fd932023878d08db312cbbc63687<br>SHA256: a34fec1d6e905c44f17db92a759bfa468123306194e702b6ed24dd187668c200</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>129.6MiB (135.8MB) – 1,212,485 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5cf4c206e8bdcf7fc8ab7909888916bf<br>SHA1: 5eb118097b7c36915269cd5c44186eba0758af97<br>SHA256: 82b8cc6018b07adfda5009edd67e46ef9cd3ac98091ea11216d09189d4998f3c</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>124.0MiB (130.0MB) – 1,212,485 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55d4c366e8480569a2903496f8023dfa<br>SHA1: 95741e6b52df9aa0fe25ccde2910876e12593163<br>SHA256: a7c5451f762cae30fb1dc44120ccd3a317d3d84a38f6c46ee7587f0a826a5edc</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>125.7MiB (131.8MB) – 1,212,485 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49ec73579bfd3562ccbc06c205ca1067<br>SHA1: 3924781e100b2a3d9cd826c617436c73d9a07e1f<br>SHA256: f3d57ec640ac195f328307831cfc72fb7976810f693dca4f1f9f7451c684cac1</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>133.2MiB (139.7MB) – 1,212,485 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 899716c8fdd3731c0969f0b6f6b4c697<br>SHA1: 787c1df111252c7bdde8b34eb7b81451c1bd2f5b<br>SHA256: 72dfa44b386b7fb45e017a61229a3569b3802a978af32de0bc3a0faeb304f634</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>122.9MiB (128.8MB) – 1,212,485 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e3f262104be28149dd5bca2d961649f<br>SHA1: e12944dc6495c62af90e435a2511536de5bc2166<br>SHA256: 64e2fb4be736d52d7de6d6b7045ed2565f2c557b9baa7e8253156ef7b6c81b43</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>133.6MiB (140.1MB) – 1,212,485 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e4b0de865a1c955597ffaf44614c63c<br>SHA1: cd6e3e39505d12847ec048c828b9c92114282d85<br>SHA256: bc021dda256e3847cbd8e8cfb2ef2d2e7a32e2d1724ebe9162f6ca2ffae09e86</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.0MiB (132.1MB) – 1,212,485 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22b4532cb9d1683cc10870281f69ac57<br>SHA1: 40f5107468e69cbcf3bb30d93681c288db4de4cb<br>SHA256: 2fb466b710286d7fd3dbb453edc6573e43bc5b64ec963b9a467763f514fb9905</pre></details></small> |


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
