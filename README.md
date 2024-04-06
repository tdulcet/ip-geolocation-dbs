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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-04-06<br>IPv6: 2024-04-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.816MiB (5.050MB) – 241,122 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fea9fb577e3e67f700cf0ee9726ce90a<br>SHA1: 7711432e235a402a9ab1abdaad7f34731baa1115<br>SHA256: 467536b451ef01e61175ef3db92d9f63b145389993f1b1cffda9ce8efdaa0715</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.104MiB (6.401MB) – 92,762 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d566c414a125a47b4775d3c60d27b81<br>SHA1: fdc55dfd71e000098bb4bc2ed24c3e28a72d4382<br>SHA256: 0e7ccfac2d17fa05b74a71d32de9fa57ea609733f00ab689cfc3fc6d1bb36e13</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-04-06<br>IPv6: 2024-04-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.225MiB (8.625MB) – 411,908 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27675eaba6ac689444304bfad95e5269<br>SHA1: fc083d9db12ce736812bad9b988cacc0fbd7bca3<br>SHA256: 1136a65f363a8638ae10be13fa5cef0fd72cade78d70ea14b476718a33e20ce9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.569MiB (7.937MB) – 115,139 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc3cc08c4db0f93efabd9dbb72dddb14<br>SHA1: b34f1cc0907080a30a739fdf2c278a96740a066c<br>SHA256: 1a861a489790362a58f83cad98c59d0c7e13f52a6a8f04a5fafdb6b07cad6cd0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-04-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.60MiB (18.45MB) – 880,946 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19dcc3e074f4e389d1b1de578737395c<br>SHA1: 0a6089b704e7a1ac5eb47a94e6f3f088b376b074<br>SHA256: 91677858e459807b3334512151fb113d08b55fbc4f100531874812954d1de0c6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>95.34MiB (99.97MB) – 1,448,868 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8f5327267cba79cf1fcec8729733028<br>SHA1: d6f6b5cc4cb1c8dd397d81480f349daccc75a7cd<br>SHA256: 4e6df561350ea8d132e19e91a2b35b8781b2addc763964e5efdedc3cf3738428</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.603MiB (6.924MB) – 331,502 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed612f6829372d96d1503867a952099<br>SHA1: d545a9307049b4d56f79cfc1544864fa920d1b6b<br>SHA256: 91dde8f7a7970c4c1b8054b947e0cca9ae1b8735bdd19fe420e6e491a7427366</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.03MiB (18.91MB) – 274,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b254c68dde265fc8d6412499c6db3dd7<br>SHA1: 2cbecfceb25b68f5f0f9889993e2f4931f5e18dd<br>SHA256: e4727e6d32df38a7582a7b9172ee67820f196bd746046a5050cd654393436920</pre></details></small> |
| | | Full Location | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.8MiB (189.6MB) – 3,159,870 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e335ee8885a5e6286297a9c06a48db0a<br>SHA1: 9b10ee274410a884c26ab662fbabb41f315616a5<br>SHA256: fc15b0d16ccdb65b6da2de506405d685d02531ce5571558ba78ed3e9110dcbbe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>322.9MiB (338.6MB) – 3,132,412 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eb566a7a93d1e35f303a2978c1da77b<br>SHA1: 78d75aa920c86cb0b75dff47ca09bb4f55bb6fd9<br>SHA256: f95d154f7a461a32269f564496c943eb8cb5e61df0269c831e76ea2f52896979</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-04-06<br>IPv6: 2024-04-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.897MiB (5.134MB) – 245,145 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86953d84c1cd0d89d0994ab1cd100b39<br>SHA1: d3303729b5fdd4e92be0090d728786a641d6bdf4<br>SHA256: 9503103e96fef9a268f0d6e3e3e189c3c227ba6a962256a4be433fec98dd6295</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.43MiB (18.28MB) – 264,858 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dee1827a7716642179bea6a3edb75c4<br>SHA1: 6d32a09ab10cd650c38bb65962cded09532e32f0<br>SHA256: d1b625011cb76995dc6c5895dea53ec54db80bd372c0878631cf89b1e7957469</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-04-06<br>IPv6: 2024-04-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.5MiB (178.8MB) – 2,955,821 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 100c457dda8054191dec8cb248ef7116<br>SHA1: 5997f43cfa17dfe7406c1480e1305b0ee4d7d2b8<br>SHA256: 2e80f7bb769fbecd8a09c918b55397ec9abeb21f176c73e5c23ca937d52e974b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,714,136 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09506237fd701236f9a08be9c399f75a<br>SHA1: 012fc8437c33186fadb2add162e68a946c843774<br>SHA256: b25eb4c33c6657facc2a0eab8012f99200c9aa7dcbc9eb0f151bcbda5e02cae0</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-04-05<br>IPv6: 2024-04-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.671MiB (10.14MB) – 484,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c19e5c583916415289c342e0cfe66f78<br>SHA1: a3a232bc99a78bf51c5fbc9f63335919cc5d638d<br>SHA256: 66e12c2c50c8515c5024f8b98282bdead8742dec0ba8890de4c7a7a14cfa56d8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.60MiB (20.55MB) – 297,872 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 555124f111723491ab84827b9abfcc40<br>SHA1: b8708ba8ee2af065c753f1de661c9eaca7882186<br>SHA256: a27d8012c78330f095d40afca9174db58dd3d3b552e2c1a6b2e1f1a4bc9b05e2</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-04-05<br>IPv6: 2024-04-05 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>128.5MiB (134.7MB) – 2,569,149 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccccef3de170bbd5364312ff1f6e9939<br>SHA1: 85c1dd9859c744b18626bbbd4b3412249424f793<br>SHA256: e3850505868ce85d1aa2248e47cd906f91ce1acec0f36d749a662a4210d1add0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>138.4MiB (145.1MB) – 2,569,149 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2d6f38c0ef75e329ce47b9221230fb5<br>SHA1: f0356eb095fac54b7e8076e19f1b7f8ed725bda5<br>SHA256: fb9a8b67acf64237a37d02c92a2f00d8e738d5c9da08f2da9b96ea8cd5b4e7cd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>128.2MiB (134.5MB) – 2,569,149 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a619e2ba56538f4f34448c85fd10830a<br>SHA1: 3044e65f2cff3e4a90216c28b770197536767c80<br>SHA256: b8dc3258f77d3bd534a6de222bb46b3674f2df6ed4b255dd38166c137ee6f43f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>130.9MiB (137.3MB) – 2,569,149 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb98ca49a79bbb79dbeafb917b6a6763<br>SHA1: 6950694ec93681fd09ee846a7f1c23f0ad42fa02<br>SHA256: 0f39c6218cf4b12c803d8a2d2982d5f7feca75aee2d9cc389337bf49f8c1f067</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>160.0MiB (167.7MB) – 2,569,149 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 726a1982a78e4f03612b0e760d0393ef<br>SHA1: 3a86955408f584baac0926ff548cc2c1d7532ab1<br>SHA256: bbaa82867bd07a97d1eadeb816846a6a5faf4f7718dd5d060ded6d574b8b4b6e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>127.2MiB (133.4MB) – 2,569,149 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffbefe5f6adca42568dca279e8a123ce<br>SHA1: db4df72c8bfb2ebf9a92150c8d76c7c821a1a381<br>SHA256: 459a6abaafbc3425452a861dbbeb94d552586125100ea70309f1c737fbaf192f</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>156.2MiB (163.8MB) – 2,569,149 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d3196c4e0d552c6afa222ac4e8e6f87<br>SHA1: c91d13b46fabf4ae6a996ed99377ab9fc2ae4849<br>SHA256: 9bb4350644ff500190799c3a9ee701783cc868cb54310f380eb5576f2ae81e3a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>131.0MiB (137.4MB) – 2,569,149 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e766ba950343ac2fcb71d1b3cb4a74bf<br>SHA1: 5a7e86fd79ff3585a7148abb4f5afc2061a3a4c5<br>SHA256: 7afc0dff976cd597ee9c12e6013cdac5710f3fa98c97b790532f66af7d3823ab</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>106.5MiB (111.7MB) – 1,149,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40be94e3972b449a1e7011a5c6a7f425<br>SHA1: 91fd530a3b1fb919c7f864ba2e25ac1a6b35b80f<br>SHA256: 548d6d173289c32752ba642cb7c2744eb2da72f2846a6856ae80cfff29b124af</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>110.3MiB (115.6MB) – 1,149,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1dc145d6d95371f69121bc656a8be675<br>SHA1: 77f6c129b4928a24cc544067ce6503b54e235188<br>SHA256: 00a8c9d51595600f0225f5b16fbcc49830cf5ce67e5eee074f7ec870489f34c1</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>106.6MiB (111.8MB) – 1,149,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 384134e25c4dec74f4126b87c6f87b67<br>SHA1: 1dcb166afc982d0cc710f53eec4a7495365f2ad7<br>SHA256: 9c09822571ca73cf07476e02950b38aa002e7cb47dd08fb79cfd4d6f5f0b4004</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>107.2MiB (112.4MB) – 1,149,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0d392f538a1e79c8d16887546e3402e<br>SHA1: 57ec4153ae9b243db158cce75954041b010aee9a<br>SHA256: 0fbf3277634d685b693067fd4b478b343abb1c8635183d21ddf51fc483fa4a01</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>117.0MiB (122.7MB) – 1,149,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e968dd3b9f4d588129ccd0298eec4d8<br>SHA1: 08995779ff66311f593f25820c07210f9ae1cadc<br>SHA256: fa357ae7f99ff29fcf8850980b3a6000e612d00babaa6c5db6e90a907deebaf2</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>106.4MiB (111.6MB) – 1,149,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7a758719514100349360fb014b987e1<br>SHA1: 695d87979c20593609aa84bfcbf9203e266676f9<br>SHA256: ae404d0d25ef590ab8cf5764567f20b447eed18640e31b9c9ed2c94dbe5622cd</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>116.5MiB (122.1MB) – 1,149,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f492d5f5eb64028a97d6190263b631d1<br>SHA1: db12c93f662694848e597b0a24f03918704aeed6<br>SHA256: dba0fbeb76052dfe7ef67e349bca1c4124f3b358d99221ad023ba9ea034aeec8</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>108.1MiB (113.3MB) – 1,149,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c445a909ab54d5cbf094b8c513a503df<br>SHA1: a462bee142633d96708cb9f67fe7383776e415c6<br>SHA256: 21736cb5e0320314e47066d73149542ad8c5a961ceb60e9ecf91ecad8cf94fd0</pre></details></small> |


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
