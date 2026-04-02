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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-04-02<br>IPv6: 2026-04-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.517MiB (6.834MB) – 326,428 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73c44678bed7e3babf310b3d1b188dbd<br>SHA1: c6fbd1ce01b5bdeec38345d22396ea518ebe1096<br>SHA256: f00e8d312648cc51d29df384dac2d02bb449059fa887723766933eb8c1b5f96d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.54MiB (16.29MB) – 236,090 rows – 258 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d06952f8f4462a45594c9ddcc53b14a2<br>SHA1: 6c1e29d590f18d77050b83df7c2e907dfa6f1312<br>SHA256: 1f27e1e80294d2357d18eefaf1fbb485923ff428e9439817432e3f9b80d1d9c3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-04-02<br>IPv6: 2026-04-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.827MiB (9.256MB) – 442,009 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8878a321bba337e89ee350d8e4add56a<br>SHA1: 906a7991b11d280d235f3e835b4194196bdccdae<br>SHA256: 5decae022c20c9ff60e0fca4d6631c295c1075924dfa9902dcf267e543466ef3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.703MiB (8.077MB) – 117,168 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf8a53ff2c39c2537e4dcbfaa21284f2<br>SHA1: 016413061e9085ed97923742c7bee276f4e1dcbd<br>SHA256: a9b4893012d8d96b439f3ff93737ee81b65403d1bf789cb2464c450d2bc67410</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-04-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.67MiB (13.29MB) – 634,533 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d73d085858b162f8ea7ccf57bfb8a637<br>SHA1: 7e0646d89de0f9536c2342a53822a2a5bd969d95<br>SHA256: bc92ad8228508fbdb042203e972feafb122c7d8b6b0d250a627c7f5fdd306a00</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>82.13MiB (86.12MB) – 1,248,045 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c9025012348cdbff8d74d8e3526bbbe<br>SHA1: e565ca8b21a20bbd6903c54736814ef48b370c3e<br>SHA256: a0440b3ebd31f0b2bbd542b4f004cf4202571df394fdcb0c7ce1e2a827290842</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.025MiB (7.366MB) – 351,952 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42fee322e3d50e46ba0b80eea81e4cbf<br>SHA1: c92420984bf626b44e3e67d758d69445fb143ffb<br>SHA256: e146504776921dc692c63f60d2370bf79fb07292660469d770fa106e4631207a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.64MiB (24.79MB) – 359,308 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33ee0b03816b02204291c82b23bb2198<br>SHA1: 33e35a7659da8340230685dd9ccb2c9c6589fe0d<br>SHA256: 7b71bc7b8fa243eafaa0756dac58003d65456d19aaf08c1f2f37d5f5b9ee996d</pre></details></small> |
| | | Full Location | Monthly<br>2026-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.6MiB (220.8MB) – 3,695,080 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bdaeedeecb09baae48fc74bf2e9e66ba<br>SHA1: 3e714e02782357dff78e09d95e5418409fba591e<br>SHA256: 2ca1d6e1fe3ca8b62e5ac300d3b78e9b466888442d00539706490057a1729934</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>453.1MiB (475.1MB) – 4,404,475 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5521d7ab94f632b0a2c554ad74dbf65c<br>SHA1: 74f50e2d2befb3c668a9339dc9038b31c82b54cb<br>SHA256: 3e49779045e3221a1ebaf9babc696dfdcf541b95d4da27bef8d0a1ef06874c5c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-03-31<br>IPv6: 2026-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.462MiB (5.727MB) – 273,350 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b173b6a7b8672083b10526c4796d4f9b<br>SHA1: 0e6f9963d4be9ee56a49e049763bd02f205d3a85<br>SHA256: ebe5ef8a85349b7035cb097711e046af6cb85da6e55e75db4c86fcde26693184</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.55MiB (20.50MB) – 297,090 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccd416bd2a6eb3354a2f0bd2c14e2e95<br>SHA1: 999fc6189bdbfd9fabfa26cb33d6459328a9d3df<br>SHA256: d6bc811052a30726e83d58e2ce20a497d664e995f75c3ac2e67f59d02f53ebe5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-03-31<br>IPv6: 2026-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>165.2MiB (173.2MB) – 2,861,537 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af0030c49cdd21d319a270940b2f23d4<br>SHA1: 54cb1ca880bc94036c7b2d5087b3a50232f02bcb<br>SHA256: 9fca85ebd3cd11fb4f7e2162eabe558238743487e9b6da288ad98cad73b60553</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>280.0MiB (293.6MB) – 2,713,153 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08e913f1ced14f2ca98aee2b12eed0c8<br>SHA1: 6a690dd5c18501daf66681173ed29afd4c44c178<br>SHA256: c2501fe0c75d957b6f27a198c035b841c73c6f52da1352ef12f100da228b6e2d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-03-31<br>IPv6: 2026-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.97MiB (12.56MB) – 599,507 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46c638355161128fbb4853f3f807b2ab<br>SHA1: 8b518bbd77c9aed1a8abae28eaa127eb3dee2737<br>SHA256: d66400494325165f301426122205b75dbcf8476f09b3b9f8e83e7c0a078eb97a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.61MiB (43.63MB) – 632,312 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb34e850741cd61df3c9a5a19062d004<br>SHA1: 85aee61a94d29fd55e86ea494d6426b26dbcbfd4<br>SHA256: a56bc2e494bdaec2f17f43c66b38eb3f0ff88b6d63f0716eda333d26ecf2de22</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-03-31<br>IPv6: 2026-03-31 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>188.1MiB (197.3MB) – 3,704,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96364795d8b54fdc304d12375ec857b2<br>SHA1: 9aafe09edb8ecef978aebf6bf025383ea8a00487<br>SHA256: 230d5bcdbf2146031b29172b1469b348150a0b093caf9f5f9a85414addeec47b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>199.7MiB (209.4MB) – 3,704,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f98486f803c02149fe082fa2f1de545<br>SHA1: d7c5325781c624ff7d80a3fc410b2dad3e3bb521<br>SHA256: c841b5b986deae4a452876184a41b584b1b010a67bfcb2df20ab767e75332de9</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>187.4MiB (196.5MB) – 3,704,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c54c155e1843a16394fc3f51923e774<br>SHA1: 6cc076b61829ac8ccb3397e941147b2afdb7bac5<br>SHA256: 624001c27fb36ff8bb64f44cd524bb5512d565869eb69a944302496630a70a9a</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>190.4MiB (199.6MB) – 3,704,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b893587e32154fbb4432b3a2b1e20d4<br>SHA1: dad54a5f5205e9eeb2ad8d5247c84602a4f9f224<br>SHA256: fe9c7c94a487edc8c8e97bd98a880230dd95bdfdb7cdd17755d6d40cf516004a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>238.7MiB (250.3MB) – 3,704,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d62396d3f9a766298ef0bb6c6f5b9974<br>SHA1: 2fcbf67cd4f73fbeab644ac67d780aff572ce662<br>SHA256: 47e88832d8abecb827f54b5903e8c66f051cd9e3bd43b8dac465a058ffc9352e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.9MiB (196.0MB) – 3,704,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 426e7c6f81afef2d6f7f609e3236f910<br>SHA1: 5abecddd4c865be51d40b553ae168d8ef02662a2<br>SHA256: 64047108ff94dba8d0eda9c379279018a06c492e9099d1cf4240eec1b47c1f29</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>232.3MiB (243.6MB) – 3,704,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb2022f5171974c8ebd6509dd6d5a8d0<br>SHA1: b8eb03d60b7d39af8c951bc91f2de366b75c7ab1<br>SHA256: 47a46d44c7c11fdfe81f741a6935dae940f4ab0edf0f4d709f00700e55a852b8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>195.3MiB (204.8MB) – 3,704,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21995afad1e4d5a0c7d41687e17da44f<br>SHA1: d14d3c9b39ab69fb9f4d9155a3658466f555b1f7<br>SHA256: 1a70b8dd304c239e3562c2eebca2e614cd3f38929671ab3fef350e08d1a94146</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>190.5MiB (199.8MB) – 2,009,306 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93b5d1bb6c63919477b2f768fbce2598<br>SHA1: bd56a378c15cc51d2a70354b64dc5e9d8e952c8c<br>SHA256: 77ae43c446e748ab17dc7b3d3188c6b0a23823be36f11458b55daed5dc180c86</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>194.8MiB (204.3MB) – 2,009,306 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e05b8cd73eeb4c71b273521e31676902<br>SHA1: e3c9ead2d20142340f59d285c1ad11ed606208ee<br>SHA256: 9172d1a3ff6c3f6278823c055eea0aca3e23d6a8804b4944a6be8c99c4fc8774</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>188.2MiB (197.4MB) – 2,009,306 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1edf8f35b50a73e7ca0d903785c11a66<br>SHA1: f4b820c5162ffefd2eb922fe1415c361b32e2c51<br>SHA256: 6959c20f250e6e5a098aaf3f5c451d2fade6abae4f4d8acb4094d7f2a387cba5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>189.0MiB (198.2MB) – 2,009,306 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8582da40b82a02e0be6b8ad84722c691<br>SHA1: 9466732051d38ef90022a4b568537ff083ccd0a1<br>SHA256: 0ccfe903b40c26103b9960b24e0c89d3d30b25e068e3d55e3492d8dfd467735d</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>209.5MiB (219.6MB) – 2,009,306 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4421bef15a22f313e21d2be4bbc55b3f<br>SHA1: 2b5879806ef8accd1d8eead9472ab8c504f756c0<br>SHA256: 3a381cc586af4966ba2ff42cf0bb23fd12ad7004fcb140d5ba934ac863053df5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>188.0MiB (197.2MB) – 2,009,306 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7dc4d56eddb9979c608d4317e276971d<br>SHA1: c3efd1ff92338a8e646f033b074bb4c14fda555b<br>SHA256: 5c1291995234bb23ecdc2c6eb8faf74f32d45696ead4aa2603f7453b6a3f7b1b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>209.2MiB (219.4MB) – 2,009,306 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7104d209233322af4aa806bf86f1230<br>SHA1: 615933059eaec68a5cade86ab6d889ed73558959<br>SHA256: 2f4f5c6671b8704610eb06c0a46a66ffb968e1261f0cddf547cb0bb7d27102da</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>191.7MiB (201.0MB) – 2,009,306 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5b2a3c56afb159c0187a003a0a6d556<br>SHA1: c94921c80e3d25e17c9e6cbdd3620c380387cd27<br>SHA256: f1e5c86cdc7453b1eacef1750f6ddb017f37c9a0bc003a1a2da66b154422ab10</pre></details></small> |


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
