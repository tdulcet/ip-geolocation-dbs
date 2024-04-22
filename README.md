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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-04-22<br>IPv6: 2024-04-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.828MiB (5.063MB) – 241,718 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10d170acd69eab95ce91315d7cab502e<br>SHA1: fef0db270831dd4da1986af8cbc0f5384bb23f37<br>SHA256: 767c1a7dc46392bfaccf86b2d3416158d65ca680654f1ab28baf70a7a889ae5e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.188MiB (6.489MB) – 94,045 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e2b5d5d3e4850a34574b6efbd6d63d3<br>SHA1: 46f73c9d333a2aa188a6d0cba1fa8dec5e24f441<br>SHA256: ed676dd634019e3c6e20bb5a531e8e575abb2871ab631f1139520bea597e71ce</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-04-22<br>IPv6: 2024-04-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.235MiB (8.635MB) – 412,381 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 195253213b70a36c90e6a2e9f661dbe0<br>SHA1: 9189de2e0759c05a130301dd5047608d3c7d63fe<br>SHA256: ce5e6093cbdc0b2166647538f250ebdbe6a60e9fa233eedaecec9f7243005dc6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.202MiB (7.552MB) – 109,559 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a397b455461043e61243ce4a20b8384d<br>SHA1: 9ddb902b5a307ec9acae521a4d030c6a7b814c9c<br>SHA256: b5640518d85408540aa9a5e13e3d5a324e1394e433feb60ee26122728f354123</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-04-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.52MiB (18.38MB) – 877,272 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35bf39c17d7dcd51416f00c8dd8ff705<br>SHA1: 78f74ccb95d88fea710d18e4debf3644b31467b8<br>SHA256: baab3eb7349943ef4d4864612b760449c79096a3d49bca23d38dd1acc0a6bfb4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.47MiB (78.09MB) – 1,131,771 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4df5ab758a9f2ea205b7a765b7e6f7df<br>SHA1: d0e2a688f983f774dbca3d2b571393c9fa535bba<br>SHA256: ddf25a9353a1f04c64b423899544539980644bf5230e37cb64cf6207a2c07e38</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.603MiB (6.924MB) – 331,502 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed612f6829372d96d1503867a952099<br>SHA1: d545a9307049b4d56f79cfc1544864fa920d1b6b<br>SHA256: 91dde8f7a7970c4c1b8054b947e0cca9ae1b8735bdd19fe420e6e491a7427366</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.03MiB (18.91MB) – 274,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b254c68dde265fc8d6412499c6db3dd7<br>SHA1: 2cbecfceb25b68f5f0f9889993e2f4931f5e18dd<br>SHA256: e4727e6d32df38a7582a7b9172ee67820f196bd746046a5050cd654393436920</pre></details></small> |
| | | Full Location | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.8MiB (189.6MB) – 3,159,870 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e335ee8885a5e6286297a9c06a48db0a<br>SHA1: 9b10ee274410a884c26ab662fbabb41f315616a5<br>SHA256: fc15b0d16ccdb65b6da2de506405d685d02531ce5571558ba78ed3e9110dcbbe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>322.9MiB (338.6MB) – 3,132,412 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eb566a7a93d1e35f303a2978c1da77b<br>SHA1: 78d75aa920c86cb0b75dff47ca09bb4f55bb6fd9<br>SHA256: f95d154f7a461a32269f564496c943eb8cb5e61df0269c831e76ea2f52896979</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-04-22<br>IPv6: 2024-04-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.897MiB (5.134MB) – 245,145 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86953d84c1cd0d89d0994ab1cd100b39<br>SHA1: d3303729b5fdd4e92be0090d728786a641d6bdf4<br>SHA256: 9503103e96fef9a268f0d6e3e3e189c3c227ba6a962256a4be433fec98dd6295</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.43MiB (18.28MB) – 264,858 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dee1827a7716642179bea6a3edb75c4<br>SHA1: 6d32a09ab10cd650c38bb65962cded09532e32f0<br>SHA256: d1b625011cb76995dc6c5895dea53ec54db80bd372c0878631cf89b1e7957469</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-04-22<br>IPv6: 2024-04-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.5MiB (178.8MB) – 2,955,821 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 100c457dda8054191dec8cb248ef7116<br>SHA1: 5997f43cfa17dfe7406c1480e1305b0ee4d7d2b8<br>SHA256: 2e80f7bb769fbecd8a09c918b55397ec9abeb21f176c73e5c23ca937d52e974b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,714,136 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09506237fd701236f9a08be9c399f75a<br>SHA1: 012fc8437c33186fadb2add162e68a946c843774<br>SHA256: b25eb4c33c6657facc2a0eab8012f99200c9aa7dcbc9eb0f151bcbda5e02cae0</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-04-20<br>IPv6: 2024-04-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.717MiB (10.19MB) – 486,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 112e80b7219ff74bf71443dd513d7b24<br>SHA1: 99386f57a5d5fb56b6dc41bf7e61c73fc27fbc8d<br>SHA256: d5d1b32bcefbe38d6fc5a0d8ddbd92fe8d7f1a6cef7b28e5b0c4d59c462ecbbe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.62MiB (19.53MB) – 283,029 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ec22bbf72b7fa62a193d62fdfd7048d<br>SHA1: ff5f4f7ee2be112248eea70be21625302dab4a5f<br>SHA256: fdb73af19a15874ba7622e51fb773bec3babc54cad672bd7d33e9051897a12e6</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-04-20<br>IPv6: 2024-04-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>130.2MiB (136.6MB) – 2,603,403 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb5de9ba59b96b5881d5ac87714f853e<br>SHA1: 0906574b6a5125905231be576920562c44cbe6ba<br>SHA256: 0dda4a608f1b31741a336b47cbdb1d11227496640a52fbac5d7753e426c4f822</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>140.4MiB (147.2MB) – 2,603,403 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d160912e7e639c0685a31a1c48830d4c<br>SHA1: 1afeeb50af01c722d5d43759342d97717ee2b6f2<br>SHA256: dee2320e5240c93439ce473dc9f93d19848494e62b61927440b4f9b00e2579bc</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>130.1MiB (136.4MB) – 2,603,403 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f85419a0f128b3d70f5d482bbf0303fd<br>SHA1: 2e0fc7cd794637911fcba2d9bee7e592399c4f08<br>SHA256: e0a3b8bc4fc57bb178daa5ed52b309ddf4926a04297862d84b45d40504e268e9</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>132.7MiB (139.1MB) – 2,603,403 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3721ff21816a541d32c9187bff40a1a3<br>SHA1: 50a0892e964aee860de1c079241c8768eff5e316<br>SHA256: 6b8a7eb00c5d5bc96fe2b247d20f3483f733dfe3b7c19b240100551b6ab483cf</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>162.2MiB (170.1MB) – 2,603,403 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51f841da3ab1b30d76f953604e997c13<br>SHA1: cf1c3c2fe1659886c69e7015eca0bfa322cbd392<br>SHA256: 1b32c9f865206b7e9b7416789a3bd49e6f3bb1fc0c34c1f352b523f0b80ac25c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>129.0MiB (135.2MB) – 2,603,403 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95f5e091cb4fe8f679904a52f77614b8<br>SHA1: 62a07b76066ca991e39a9198474c9e1cc8f037bd<br>SHA256: cde679e87ebcf3d31dfb42112f0a2a8ba333b43ff30f14062bf10a6eb7def368</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>158.5MiB (166.1MB) – 2,603,403 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3aa95faabb1d95a809eb683ffddafb94<br>SHA1: 5bc5da3b128a5c79234ac43dd778d4896a582a64<br>SHA256: 8e02d8931569094c48af35983a822b8885d9012c3c0e6f77f42cacdebbfc2dcc</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>132.9MiB (139.3MB) – 2,603,403 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbd42d800e5fefc10433cf073bfb826e<br>SHA1: d03f3aa9f74fd7f721d9fdd0abbdb4e794c74ad8<br>SHA256: 6a43a3ab9c29d64d4556cfdcfb0b3bdaffc8c4dfe74e175d342b74d187f2d66b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>111.8MiB (117.2MB) – 1,202,557 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb026688b2b665e30db57d7cd2951b34<br>SHA1: 0c8cf2dcb6b313510462e8df28f259e82c8a8b2e<br>SHA256: 7a56be9b5278955b8bb4e72665c7e3ae411660def4036b714f7d286caaad01ba</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>115.6MiB (121.3MB) – 1,202,557 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ddb85fb5a41788aa46025b03380f437<br>SHA1: 51b87e24454da131d01ec3d69170fefeb78ec2cb<br>SHA256: f6fe474b05430338c2739bd8ee33ad412ef57b8644443b106fad548fc4fae53a</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.1MiB (117.5MB) – 1,202,557 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28be87e945eae486b9294eadaf42142b<br>SHA1: 03e46eac79f76e34d43831ebaaaed7c03a638d4b<br>SHA256: 34746644272059febab588402070dea77736cc9620adcb14bdaf932166cee503</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>112.5MiB (118.0MB) – 1,202,557 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8081185de4280a4af412c21a6c776287<br>SHA1: c72cff7b4ead1705e8d8a75209bf4b64d88a683e<br>SHA256: 0f4cf55ad79ef943e7552f4a75fe2b0ae28fa373b57d9cb59ddf44de4d4a7caf</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>123.2MiB (129.2MB) – 1,202,557 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c42b5b43754ad87024d1ff0cf5aea519<br>SHA1: 0d83957c842230f7806368c600ba9d0b9b42b522<br>SHA256: fb9d61e5382cb0da7cb7b77259a18d1f6162701220b1d82cfc9e61158b812c7c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>111.7MiB (117.1MB) – 1,202,557 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c7ce01f18589a995152e2c36f0e64d2<br>SHA1: f0f06ea70ff5e63ee1896341a299992c31b33d84<br>SHA256: 77c60a9ca0cd116b6c578a48ea4b380854f0019608253f9cebdeb8239824d753</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>122.4MiB (128.4MB) – 1,202,557 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab5d6ddc2505872e9072fb11a1e158a2<br>SHA1: 319d8c35dda0372568996cfff8412375de9106d3<br>SHA256: d23bb0d205e430fae1bea2fbfb2b61077920a4188c933f9eb971350805cee553</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>113.4MiB (118.9MB) – 1,202,557 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a907a6937305fadcca732f3a2d98bd43<br>SHA1: b9cddb0ec804464e02d330ab2463cacdcc8875f3<br>SHA256: 546fa9495744cd3e4488afd5df7edaa6f18bc29b5ad31978f06f151dbca58f7f</pre></details></small> |


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
