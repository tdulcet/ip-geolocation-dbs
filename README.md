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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-04-24<br>IPv6: 2024-04-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.828MiB (5.062MB) – 241,678 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c4aaf80ec29bf589e3cdd78ffa78c0d<br>SHA1: 27ed1cbe76134a5f68e338ff9fb09f76ca4bdd63<br>SHA256: 178d63f38dc11228d4bd4c32500ecc3f6b691814408ad3ca8502be13a050ae9f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.200MiB (6.501MB) – 94,219 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e263ebf116955578c2046f399956fb5a<br>SHA1: 9a7957c5f869ab6b9e0e93de9cf48a770a361682<br>SHA256: 7b59c0c88ec57a203c8660aff81050fd223af223101f1fd263511ac9959d54f9</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-04-24<br>IPv6: 2024-04-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.241MiB (8.642MB) – 412,714 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 639b79a0ef507935661ba53f962346e3<br>SHA1: 98a3ca7a548f60b819f3a18d4c618a2280e43b71<br>SHA256: 7e138deac600d6101793bec8863f38009769500f4fbe0bccecc7233f942b5d08</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.175MiB (7.523MB) – 109,149 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 12a09062d5612583e44912a40c63e970<br>SHA1: 7b9bf8be2fdd80144712ad112fb5f6be21eda261<br>SHA256: c779ccfbb597a8a97d7541c09c0dd7ee497d364124f4950844813821fedb9b31</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-04-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.58MiB (18.43MB) – 879,904 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3203c1f9519dab44f208e02181b484d4<br>SHA1: c77422b1237f43f8ccdc26e4a5d1c79e1932beeb<br>SHA256: 25ce57acd3311c447a12e68ab34e663e6078980b71210277129d7dc959e9c726</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.65MiB (78.28MB) – 1,134,461 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f3f0cc689e7f3fcd69c2afb78e9e72a<br>SHA1: 53b0a928dc45e267752824ab3362d1abd37e3272<br>SHA256: 299da7645837c97bb4f841b2399d70eb865316ebe1ff3dd879a1eea349eec291</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.603MiB (6.924MB) – 331,502 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed612f6829372d96d1503867a952099<br>SHA1: d545a9307049b4d56f79cfc1544864fa920d1b6b<br>SHA256: 91dde8f7a7970c4c1b8054b947e0cca9ae1b8735bdd19fe420e6e491a7427366</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.03MiB (18.91MB) – 274,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b254c68dde265fc8d6412499c6db3dd7<br>SHA1: 2cbecfceb25b68f5f0f9889993e2f4931f5e18dd<br>SHA256: e4727e6d32df38a7582a7b9172ee67820f196bd746046a5050cd654393436920</pre></details></small> |
| | | Full Location | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.8MiB (189.6MB) – 3,159,870 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e335ee8885a5e6286297a9c06a48db0a<br>SHA1: 9b10ee274410a884c26ab662fbabb41f315616a5<br>SHA256: fc15b0d16ccdb65b6da2de506405d685d02531ce5571558ba78ed3e9110dcbbe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>322.9MiB (338.6MB) – 3,132,412 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eb566a7a93d1e35f303a2978c1da77b<br>SHA1: 78d75aa920c86cb0b75dff47ca09bb4f55bb6fd9<br>SHA256: f95d154f7a461a32269f564496c943eb8cb5e61df0269c831e76ea2f52896979</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-04-24<br>IPv6: 2024-04-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.897MiB (5.134MB) – 245,145 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86953d84c1cd0d89d0994ab1cd100b39<br>SHA1: d3303729b5fdd4e92be0090d728786a641d6bdf4<br>SHA256: 9503103e96fef9a268f0d6e3e3e189c3c227ba6a962256a4be433fec98dd6295</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.43MiB (18.28MB) – 264,858 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dee1827a7716642179bea6a3edb75c4<br>SHA1: 6d32a09ab10cd650c38bb65962cded09532e32f0<br>SHA256: d1b625011cb76995dc6c5895dea53ec54db80bd372c0878631cf89b1e7957469</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-04-24<br>IPv6: 2024-04-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.5MiB (178.8MB) – 2,955,821 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 100c457dda8054191dec8cb248ef7116<br>SHA1: 5997f43cfa17dfe7406c1480e1305b0ee4d7d2b8<br>SHA256: 2e80f7bb769fbecd8a09c918b55397ec9abeb21f176c73e5c23ca937d52e974b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,714,136 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09506237fd701236f9a08be9c399f75a<br>SHA1: 012fc8437c33186fadb2add162e68a946c843774<br>SHA256: b25eb4c33c6657facc2a0eab8012f99200c9aa7dcbc9eb0f151bcbda5e02cae0</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-04-23<br>IPv6: 2024-04-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.714MiB (10.19MB) – 486,674 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a87fef2830de7382341f118de65b1ba6<br>SHA1: f89026a106a20fa94988d1ad89b17f11afd3f7c9<br>SHA256: d8dd41b1012bc8944b37a0786cf7204157d8f9222acfc870c98ed58f1b8ea784</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.56MiB (19.46MB) – 282,060 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 408db61f3ad824d7cc576053e68a2193<br>SHA1: a62873137a0109ce3891d0d28bdf6437e3ec0a78<br>SHA256: 1432cb6424de4e91f08e65d6389c5e601b64ab0082d13799fb7eb5f3d2c5c745</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-04-23<br>IPv6: 2024-04-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>121.5MiB (127.4MB) – 2,432,252 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71c9f3be63bab44a92c7bdf405e21f40<br>SHA1: 6a53a6a5547b56b706730c194e96869c3a73abaa<br>SHA256: a093ba835b839f86185b0afd1db2a97d234f43fbb9d0010a934926463c294cf9</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>130.8MiB (137.2MB) – 2,432,252 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15b4ea5587999aebb835d5b2fb7c008a<br>SHA1: f7dabb5a3d3aa393276eeb289d8a2b8b09b8708d<br>SHA256: 79ebff50c4fe61d6b1c8958bf3eeab6d00c37170797874f7f88d1e121fc95997</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>121.3MiB (127.2MB) – 2,432,252 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f30fca1fad52a1ccf69468a2557ce85<br>SHA1: 98c611d613e0a7a8841d245d4e7f4b68b0a4c391<br>SHA256: c26bbdebcdcf613d1b326a4ed5f03f7914a5edf2e8fdab20fbad42bf3f10e0c2</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>123.8MiB (129.8MB) – 2,432,252 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afbfa21523f0d30386e7c412e38d90a9<br>SHA1: 5c117b178729f631957314a9b6381c08fba7867a<br>SHA256: 1862d9a6d17eaa24e0728467a3e066d7a69c3b4b4e3b01096cf225c9a27c7795</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>151.5MiB (158.8MB) – 2,432,252 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69a010dffeee2d072ba1c06f4445dc23<br>SHA1: 201ee3bcec1a15eb1d22ac8624248f483185795c<br>SHA256: 598177933e127ba2a598137c389a859e4ded5cadbc4f831200993b6f2c1c8c89</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>120.5MiB (126.3MB) – 2,432,252 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edda016303946f292183fff29cac4d67<br>SHA1: 0fc538d2a266c1f6bc796ca0b85f6205a1bea01f<br>SHA256: 00e40dbf9db94414c619c280526e1ebccb00f237dead19fd3e79fb4d8de693a1</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>147.8MiB (155.0MB) – 2,432,252 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1e09ff77b4d19944391e3f2d595151d<br>SHA1: a576887851a41a65e0e2a2200030a7100a88fdea<br>SHA256: 35f56e35630fc84a9978fe47de9b0977f5e99b8d3bdd34422c79037bf638405c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>124.0MiB (130.0MB) – 2,432,252 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3431b02933b1bda3b97c9e4849a623b8<br>SHA1: e68ed6b14d1e08630e2226aa2fe9abb7c65cc936<br>SHA256: c16421b014b1c35c17b17c07648acaa8ebe06ab44cd6c00ed82f8ff68ea2c70c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>111.7MiB (117.1MB) – 1,201,642 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e385e4ffc55af4fdea864994c52f1241<br>SHA1: 3ee0107932a82168ffde17f75bf3f80529b9b19e<br>SHA256: 2af1d9b3ee81875faa264ae02cd643ccb196b850c2ddc65ab23fa269b54a1f8b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>115.6MiB (121.2MB) – 1,201,642 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 573c32f797450ff7bd5ebf9acdbb48c0<br>SHA1: 3b7ff3460bd4c0547decbcc0b05918e3e95364f7<br>SHA256: 6e4c31c95997710333631440fc6d3f19e09155fac22b0fd1040c42f8bd6b3507</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.0MiB (117.4MB) – 1,201,642 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c84936e98bc1f0ee03009362173105e7<br>SHA1: ee13bd9d2796229e3593ff118a0bcf72d2dd5121<br>SHA256: cc7d340eda91797e024f0294064f104c8cc2fe155f2171d973d74da89258d00e</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>112.5MiB (117.9MB) – 1,201,642 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74baab005cc249a34aa1833eab2a94b9<br>SHA1: 254a5ea845b7890800d68129c6ff932933256000<br>SHA256: bad6e873379e781a9e56b7b8ed4705f7b1c94a4902b3f9c97c25fa31870b3b7e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>123.0MiB (129.0MB) – 1,201,642 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9fec3d0d7bdebc21cfe9dc5a483d7642<br>SHA1: 72e981fd2d855d075749c4e110b1bd7a6f6a6fd0<br>SHA256: 0d7cd8781a3d35f00d445379b7a7d1a204fb8e1d08eff052d25f7a8d1f5a77c8</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>111.6MiB (117.1MB) – 1,201,642 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83784d02212d131fa97f7e852a831c20<br>SHA1: 5b81324c6db2eb1086dd60879f7e6e79286c21f5<br>SHA256: 2156a955748316ab2671d93ab17cad5a76b16735fa3f6d049324c7feb3f25cd1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>122.4MiB (128.3MB) – 1,201,642 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c60f7528007c955548f6375e97a3421<br>SHA1: 50d2a02bbfef51c480133ce80cb60d52b8e57dc7<br>SHA256: 5c3304b307984e3694fa4e52ad26324fa769fd970c8fb333f79adf1d27bbf0f8</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>113.3MiB (118.9MB) – 1,201,642 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f746a4d18f2bd00fb0dac8cc324e14b8<br>SHA1: 3418e7ef36e008e88ab8ecc174ff8d30eac5a0e2<br>SHA256: a502472d29fe81556a00cc754c73b69217bff55584ac987a1f0b401b59fb1101</pre></details></small> |


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
