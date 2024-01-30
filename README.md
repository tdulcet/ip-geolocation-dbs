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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-01-30<br>IPv6: 2024-01-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.792MiB (5.025MB) – 239,922 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a91580d5831835e60f2ebfe2437cea8c<br>SHA1: 4438e556bde7f35ce02482badad87bc89b1f49f6<br>SHA256: e8ded08bd30c9d6b21c05c724b55cfe5cb7014550ba11fd9ff5d4bcb25b1d796</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.580MiB (5.851MB) – 84,801 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1abacabfa54f279177eaf47c9f9e8457<br>SHA1: a596a45df70e8661fc9b69f23881b4f0cf932d2b<br>SHA256: ccbcf414b1b7ca60d4abd47680f07b4f3485c72804c3824c69f53a1f4ce32950</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-01-30<br>IPv6: 2024-01-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.265MiB (8.666MB) – 413,874 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5d6e20f39885d5e1e514700c7f932d9<br>SHA1: d4f9d2da2c961bade55123e45911457e7d93b9d4<br>SHA256: 68396a7da45e2c897c44b9971c5f1de1cd7597e647b40b4ec02766175666d757</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.920MiB (7.256MB) – 105,273 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2461429d1cfe4aaab416ed8d72c71d8d<br>SHA1: 88b4e0420417ae1682284a698bec9fb19fe46a73<br>SHA256: ab7172b5099634adddf95a9626d132820afba49049b4976bea0bfbe5f345e181</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-01-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>18.73MiB (19.64MB) – 938,246 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e8964972f8ad60c07bdb70112b76ec4<br>SHA1: 51873e9a0db952e22b648c2c06ce42a27c81ed84<br>SHA256: 0dd11970a5076a871114d9504676b0261a1dfce8e68cf547ba7ec21d2264b5c4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>52.58MiB (55.14MB) – 799,090 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 717b9f7b22a6850f4416fd1cdf7d3c81<br>SHA1: 7ed78494c457736dc7f770225c19381e7d95cb78<br>SHA256: 66bedd3efeb05fb464d3a71873bf6043ad21975fa0df7f10899e05135334376f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.162MiB (6.461MB) – 308,408 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736158b820db1062b003cfce212076a4<br>SHA1: f3b03108eb0edf83c338abed05e010c2b0e9cde1<br>SHA256: 68e446a0380ab263a21743f68ab8aa6b249b213af0d6ffdac0780fe4912cb7c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>21.05MiB (22.08MB) – 319,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73819723f00de32c17c8aeca84d93383<br>SHA1: 71d954fffd9f9f5979ff89981fcfae6f73cadb05<br>SHA256: 1328a782f89b58d1f6fabcf3542ce4bb259d89c1f28a0cc70abfe70b5e573eea</pre></details></small> |
| | | Full Location | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,096,472 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b990a48af772fbc4cf7093aa51d35b4c<br>SHA1: 8ddfa8795c4c534c0bfd99b2472382b368d7fd5c<br>SHA256: 117938f84386f9ca627464e7c42856b6d9ff4f68bbcac12a393b73ea1ac0836f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>243.3MiB (255.2MB) – 2,358,639 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c61e48446e598bab5cfa16234f5f136<br>SHA1: c3373a6fe2e2f8e08a48274939c4b494fb99b5f1<br>SHA256: ff81c189923d299847f5b5e0e5c472fe10d836d11e24fa5379a2def67c998406</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-01-30<br>IPv6: 2024-01-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.626MiB (4.851MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24caac24a9c72bc3caa6451ceab08833<br>SHA1: aa114043e64d74ecd9e8ccd339b80c62d3fcbabb<br>SHA256: 6d48a0384e6e4d38820ac8d2936c12db7eb726dfe20c59600d4f14d173e3b15f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.10MiB (17.93MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fc970b50f7b01de0d0c6bd29224c13<br>SHA1: cb1fe32e67d0561cefef5f2908570ae3af446a24<br>SHA256: e0f36200f10f817a89b6cf80d8d459900c5428a669cc706af32d15b709a8b624</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-01-30<br>IPv6: 2024-01-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4MiB (176.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4104f39d8c379ec8967157286f495717<br>SHA1: 440c75c20491f104948897ce552c95510badba7d<br>SHA256: 6689c6e63153fcbdc00272e2ec6cf04f0c6877860b4a667b3972dfa08c898747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 142dfb0f4dc0ceb4f5a41b018ea53524<br>SHA1: 284b510184f46179e9e34f60dd0db14fc72f3e50<br>SHA256: c57159c9a8879702623a2ef4d0c2fad06d21e96f1836db2d3a09f9216aee1641</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-01-26<br>IPv6: 2024-01-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.322MiB (9.775MB) – 466,954 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c98e9ed1c50ae30e00d156be0f0b04d1<br>SHA1: 7ebaba2fc25d110b0343895ccb533af0bb2f332d<br>SHA256: f6d8abef4a3a4513768b728cd91f3b060d90a8615ee8170f6c388b661ba22ed8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.64MiB (19.54MB) – 283,242 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f21d8e8fe00088bf9473114d70d8ce7<br>SHA1: 5be8e77037ae12ec0c385b1fcb2bbc5eaad4c855<br>SHA256: a235224e316abf497b7f5255f1ace9d203d511c02ef142bede01039fd7b0e3e1</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-01-26<br>IPv6: 2024-01-26 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.2MiB (182.6MB) – 3,695,194 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32560772b6cbf9dfa0c186681dc4ba68<br>SHA1: cb446dde04d3a2543fc8de2bb571e53413e1771c<br>SHA256: 7fc41837f1899719f18ae0db2d40a1b73557100b7b46c49aaa252664886e44e9</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>203.5MiB (213.4MB) – 3,695,194 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92243d1e8e0cbb93fe02353777496d0b<br>SHA1: 4e1674813c290abae3e7f567aa64b7049d9c6e9c<br>SHA256: 498574b95ac78a11cb4ec519d4f20c3306de67bde4c1c5177fa4454e0409a389</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.9MiB (187.5MB) – 3,695,194 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b8499cbf4083b51cb51d0d2cf69b1b2<br>SHA1: e7111af1a68ba6552381516db1e293311ac3e921<br>SHA256: 622ba981880bbf4f6e71f16a1411fa9dc259329b4936b19c0352600ef5a99b94</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>186.1MiB (195.1MB) – 3,695,194 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bfec2a2fe07de3545c256b066f43d36d<br>SHA1: 0be5bd30df1c14b694b96380eecdfd07c0c5cd08<br>SHA256: 289baec2b947d70ee910d47922b7389fe4a1381c2719496eb09da69d815c55ec</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.2MiB (228.9MB) – 3,695,194 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1bd2f6ceefad534efa6cb93e2886b67b<br>SHA1: 577675bb9f23f0681173a98b7db789f3fa153416<br>SHA256: 96051a9790d99f47d047d892cde413ad237749834f470c765d54e3b84f463312</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>173.2MiB (181.6MB) – 3,695,194 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d303d819e9661fe0f9e53dea03858b0<br>SHA1: 170ad2486f4e4037b804ec67c6fd634031c767d0<br>SHA256: 5aa7c6218b1f5cee8ab5d3d64a173c3a82a215ba6c1c439ec0a950d78a1dd80e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>217.3MiB (227.9MB) – 3,695,194 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 070a34f910c99e737935825ff23bd478<br>SHA1: 0ee4cfb2522b0f2933b4ff137bdad7eaff878f73<br>SHA256: eeec2f257809b1eebd464eae5a50f58acf41b95d04fb81d53774fef7bc570a61</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.7MiB (192.6MB) – 3,695,194 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ee8c593feb021cf03df4c8d8d24f96a<br>SHA1: f8bf7af001e82bc10fb98496a7a9ad5e3f905d1e<br>SHA256: fa1899d76364ea6362d9b0e872d352ab049c8747f627b517b70910995a4757d2</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>107.4MiB (112.6MB) – 1,202,410 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 868c5e5073279279ff7226be0f3152cd<br>SHA1: acd15c9dbc8047f3dab713f6af237b5ab7b692c3<br>SHA256: dca777352508e8d95fda8cb87bdde6dff1c59d2d2bfd3599af843a5eae4a1651</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>115.3MiB (120.9MB) – 1,202,410 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d735add5649e571f9508827571d7999b<br>SHA1: 337d6416a944f5c4ab1472dcd5bae0803b2117be<br>SHA256: 9599fbe2c4b6f400468a44d19196f2d36e4fd4de3dd39b5d44c037d5227a288e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>109.8MiB (115.1MB) – 1,202,410 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17ad119f93574d3b22d2290db6cebd7c<br>SHA1: 5565103dbcc2e626c5a25a2c8c8b68f78b3c35c4<br>SHA256: 40fb937739139ea4d5fde2f5b3632f244cc4e3efce1a0c64ae4dd5c3220903d7</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>110.7MiB (116.1MB) – 1,202,410 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fae7d0ecae8de9acb0fad7b66dac78d3<br>SHA1: e86f7c5b79d024d87905fb46ad13f13cdb0e0198<br>SHA256: 97919ecf5f9b952f908500fc45e0254c81d2e962abd42d098708839f00ab773c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>118.7MiB (124.5MB) – 1,202,410 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 976d38325888865468edb7e50e181c0f<br>SHA1: 00a1c59f196047ad3cf246727d3511cb0f30a944<br>SHA256: c23b1b0f7149a0e975c6efb344c730efe36267b2a0c87792c7325a86755542cc</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>108.5MiB (113.8MB) – 1,202,410 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74f193b923b793c71d40214410804ce1<br>SHA1: d416c3a783c27110fb1ab9bacfb2df962b1b5d11<br>SHA256: 3b6c8bf36944dae4d03a0723b343a8791de5bf53d35d2aabda0a99c0932ad607</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>118.9MiB (124.7MB) – 1,202,410 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98af4851e653c95f72cdea87edaede19<br>SHA1: 536421add7f73cd99fe68a0c24b1f57db8677cf1<br>SHA256: 8469f857d01ccfde479c0ca991aaebeefe8ea9af4b3bfaccf3664dde650c04b9</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>111.6MiB (117.0MB) – 1,202,410 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a7e4bad523ab28af6e185462a9ce80b<br>SHA1: bee4e676c8ba301c3b517fc1ee8d09c3e186a9a4<br>SHA256: 4c52ed0b62020154b4ae0a7dba26b682718f80eb557b64b3694e90bd9797f092</pre></details></small> |


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
