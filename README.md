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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-02-25<br>IPv6: 2024-02-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.803MiB (5.036MB) – 240,449 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 268f6d04af864aae5d0cb7e0ef7c92af<br>SHA1: 032f427d7ab858c4a8574a920e8d743af802c0e7<br>SHA256: 2b65f725e85ab50a465f9d44c6eec8ea95ad4a589b6b07cac5b5e2b995c4a80a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.672MiB (5.948MB) – 86,201 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 997c870048cbfd5e1bc4e3e62463786e<br>SHA1: b0d9c53b3283dff1243cd050cfc62fc896490789<br>SHA256: 4ea92eae5b15053119d3fdfd27ffcab8e5e963c349ed47a6c976ebfb986b328d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-02-25<br>IPv6: 2024-02-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.186MiB (8.584MB) – 409,968 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ab9de492207e115402dab3d1a1a639c<br>SHA1: 387573b20f1c83cbc507741c2a6c52b62e8da505<br>SHA256: 5890733d281faf4c097e89b9f37334df0745481dcda4e5d5b6304c7d3844b4d8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.002MiB (7.343MB) – 106,531 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64c34b0603e8ad6cbe028b05ebf7272d<br>SHA1: 522b84359c00d69c33b33f401937731e51419efd<br>SHA256: fa9e0065a9ead662ac9a0d6cc2a47b259938f48ce46676b50134358cc1f9c97f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-02-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.49MiB (18.34MB) – 875,709 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62e2037e4e0becda72e2d44e5ba6d0b8<br>SHA1: aae9cb831f95b2e097f2f5459b07849ef147a5f6<br>SHA256: b168efe265c435e005b827b0f47b401fda46bf51312dc9b0ff5a8e82e799f471</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>58.09MiB (60.91MB) – 882,797 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8d3841d4d70fdb02780b65ea38d9c5e<br>SHA1: 5336f0d86a3ceac5ceb01da6efcaea4d8c30b818<br>SHA256: 18bc4b1cb437c20a0ec33974e13d51795375806567509174b2c131a18ece7db1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 322,238 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58dc67267f460ea3cf5cad59cd04fb2<br>SHA1: d7cd4a637354f5a5c457e96633e1f5c9cc5c059c<br>SHA256: 55313849f9b0eeefb503ca58aa485ebe95d325c7771a4b2e5e9def19ee8aa2f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.67MiB (19.57MB) – 283,667 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b73dc10990e7bef8c444f1cde6991f<br>SHA1: 07ae49b41bae3e257ad578c4bf31ee8040ccf1fa<br>SHA256: 7ea6211e834aaf328302ede30e6777fc4f71afb40ab1238cf0af2be151b5b248</pre></details></small> |
| | | Full Location | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>179.7MiB (188.5MB) – 3,143,531 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4796f68669fd62ff1776c3d247e13dff<br>SHA1: 8d63c70c0bd62e8829cfbd2dfba8d6b8e6c77fd0<br>SHA256: 04e5000cfd1d52386cf975f825886bb214085c10b75c2568efa51ce70fb6c3df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>291.6MiB (305.8MB) – 2,831,720 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 657b58a340f82d12479e96ce7f695a45<br>SHA1: 1b9c4719ee91d1e9da68e6f0dd1529e893bf9777<br>SHA256: fbe98efa467387f6ceb69603459abde1562d03903aa05b063edc68d9aa4e87d0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-02-25<br>IPv6: 2024-02-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.640MiB (4.865MB) – 232,256 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fec6f73486236c8d0d94598e079d6f<br>SHA1: 7f19645a2e7ae1f5579b6769363477a0ec58e5f6<br>SHA256: 7f7145aa700bc6d9b86d8e430377fb6751efd3a786e0455999aabe3401d275c5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-02-25<br>IPv6: 2024-02-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.9MiB (177.1MB) – 2,925,251 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434c9a2a5a5c869e663a7e206ad5962c<br>SHA1: f2e0c48f3ecc7d10f4697a8c5c698e1979b08714<br>SHA256: 8d5321147896799a07280f735aae4be97a74bdd31110778527dc8f4b77485f61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-02-23<br>IPv6: 2024-02-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.365MiB (9.820MB) – 469,108 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a9a592f3dfe87914a946ba853ce39bc<br>SHA1: f720f5ea4f185d57f4c703a76fabc7d15ea386ee<br>SHA256: aba8a7a9d9174a516acdfb4e4318f0a39ccc304e7c81086ee8c3eb8402ced66c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.48MiB (20.43MB) – 296,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a8386d896d176b5e8b6815fc59d968a<br>SHA1: f5636b1fdd17cb293eb0b6f85552614dd9f1b51d<br>SHA256: de218c6059c4d83770f9cf5829e4a613e131ba4ab1abdbcb45f48007a782e379</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-02-23<br>IPv6: 2024-02-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>148.1MiB (155.3MB) – 3,147,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf01b30afd42aeec9d4942deae44ec49<br>SHA1: df5c1e7f1d7bb72656ca2a541ef7b5c66ac7d8bb<br>SHA256: 6650adf7ddc14175a0e8a3b4ac148f3e0989589cb8b3d677ed969604c8f719c9</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>171.8MiB (180.2MB) – 3,147,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e555d747d8bc65752ec4bb5d0a182a14<br>SHA1: c623ea2158f2b81d032bc67c8f3458d8b2d04d1b<br>SHA256: 700cd2e95236196d3cc7855ec16f649685877273ea24854236bd7baad9fac790</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>152.0MiB (159.4MB) – 3,147,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dfb77c60a387905cd56399c3978ea49<br>SHA1: 7f75469b2e0c21441becd02840931d11db5d3149<br>SHA256: 63892b0ca21a7c1475b9295e553f18260f9eba94562da1b6e91a9fec7cdfd78b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>157.8MiB (165.4MB) – 3,147,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eef5e5bffa4996aa78ab69495e41d89<br>SHA1: 49747d029cb0a1767b4cd134c9b02eb8f0865610<br>SHA256: e2e54f4bd37e7849154369370080a2c9b735139ffcee3e11cbdebd1a2e6d1206</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>184.5MiB (193.5MB) – 3,147,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d8417b8376b9dbd28dd271bba944c29<br>SHA1: be857bbb2f517150f67bb5486bf66fb640df4582<br>SHA256: 7dcd03600ea526b454fc783223038ab8fe25ee6729e1f25876887071368cb9b6</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>147.1MiB (154.2MB) – 3,147,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 104232a02e720c5701810418882f7400<br>SHA1: d0affaf14852ffc51bbbeb0ba879c77cffd6ba6a<br>SHA256: 3026b7a864de0e426c7e3ad8e83f962dd98a521d2478a81b944b67418b0b133f</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>183.8MiB (192.7MB) – 3,147,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70b9c612ed47af7a181c55f2efedbf6e<br>SHA1: ae74a24c1e769b06d02fc9f1cbbe715994444188<br>SHA256: c58672ff4d727e8153ae36b9ea150cb9dde3205dfbfd25f49e17b63568707b13</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>155.3MiB (162.8MB) – 3,147,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57907dd22165cd1f483235b5400e6b84<br>SHA1: e6b1516720f765d4df2726c8d13244e0942b762f<br>SHA256: c324b9e749ee0d2bd110ba584d1d8f50e179c409daab8c699485ff657046af62</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>102.0MiB (107.0MB) – 1,134,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85279ff389425ce7cee46c4a18156425<br>SHA1: ceca8cdb995b59fb5883298aacd2b1bb29982320<br>SHA256: 285f93170e8a9048902a7a11714ef0e779f19b2a84b499ed68c487d7960b618e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>110.4MiB (115.7MB) – 1,134,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60014f0aa8a4acb2e1b6e0a6063330a4<br>SHA1: 190f3e30cfc60203bf5ffa1aeb8d29c344b42a83<br>SHA256: f39adb6dd2b07425dde3095a9f06b7b1a1854c290fc3d53e9470d8c13e365821</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>104.6MiB (109.7MB) – 1,134,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f5809ca040373b39595775efa6055d3<br>SHA1: d9efd80c5716373b2f94bebfb166064e72b56c11<br>SHA256: 34921b70ecee1641b90567f525b755e59bbbcc940158e8e08a5610feb6826ef8</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>105.3MiB (110.5MB) – 1,134,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: caa3f4ac39bad5b434b11259260fcecc<br>SHA1: bed992bbb61f6d7474758f24bd8bece4174e6eeb<br>SHA256: 23ea7c3ae0cb7ba7017904df1e3c72e9bfefa303875ee1d73ec021df14d2e004</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>114.2MiB (119.7MB) – 1,134,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed36152fc4d8721e4e33e30dd5b353ea<br>SHA1: 16ba18034cdd32625c2d1162699049847efd8daf<br>SHA256: 8cf229028dac3b3e7bcaf11aa651f446bccf86381b5cc9b8ea414bb33e79cc91</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>103.5MiB (108.6MB) – 1,134,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 032543df56903d0aa5cc27104838458b<br>SHA1: dd39ea0fb5dede82d250bc9657bc400408b0e8b4<br>SHA256: 82ce94fc4c96f809fc620aff8a9df664f710ece783d556ee959ea6617749a42d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>114.8MiB (120.4MB) – 1,134,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 678058279857e54c75bc9409fa4773e0<br>SHA1: 4fb7dfff44f3f1449c54a50deb05175c53a5fc60<br>SHA256: ff56f1739972a38111032b32b7a92cc158eb2934d22c52f797594f5689bc0521</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>106.8MiB (112.0MB) – 1,134,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2114e4422dfd7b79c9a761c6f4938e04<br>SHA1: 836e02f62835b93699167355ae7664d7797286ee<br>SHA256: c7f6c6546370bc56f7f603406d5c56e0bbb3fcf2aaa5659966da6ed807774a3c</pre></details></small> |


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
