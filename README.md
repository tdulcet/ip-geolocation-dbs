[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases are scheduled to change from CSV to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than one day (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-11-30<br>IPv6: 2023-11-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.604MiB (5.877MB) – 238,714 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90132ab4539d24fd1b46db5b31c17594<br>SHA1: 6d96bec014f56be8972ad66c4f521361fb99f3ff<br>SHA256: eca8a19797de7c28ccd37ddf6790b3eedff22991fec9e66356b2f878767d97d8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.364MiB (6.673MB) – 82,381 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1306a2b77213554b4b7e0940937ecd9<br>SHA1: 5a5aa2a8bff37f608072b852cd5952b4ad2806aa<br>SHA256: a999a2dc20184733c4e7ba74d8627c8b3e61e00f0112a153b82b46444ffa4e41</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-11-28<br>IPv6: 2023-11-28 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.670MiB (10.14MB) – 410,739 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 420ed11b93e12d0ae85fdc2c6801fa67<br>SHA1: ec7577a8b5a7e548aaeb6daa172c52866e47685b<br>SHA256: b91d4e3972c0ccc62b0362e9612ad0fe0c7052afdb18f5b477a6c9d35f697286</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.057MiB (8.448MB) – 104,399 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e924522d8135f60cac94b8f039fd14db<br>SHA1: ab01ded006710840f683a81d8a1f9aeb30d6e3af<br>SHA256: 8c11c8aeef6f0371463615fede80cfeb8c7d154f01cc2cc8954eb5333466848e</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-11-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.65MiB (20.60MB) – 834,272 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ea6164d8ea27b658503ec70acf369a4<br>SHA1: 33ab11db1533738c7cdac6faedf08a856c6e91c1<br>SHA256: 34e07ebbfed5a5081ef5ebe4565123a97ab3d4a9fa74a927bb71c12ca745ea0e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>58.08MiB (60.90MB) – 751,832 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03bf00acd260a230926a2868de03a176<br>SHA1: f3d73633ea868c72dc547e5fa1a81d11aa9465d3<br>SHA256: 23ebcb30cefd65c29c8599cb7e1c2849c50e8a415af2c59be0526941cb0af8c6</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.260MiB (7.613MB) – 309,964 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7fc3106cf6c65db7d44df8b4fb1d16<br>SHA1: 6ec97588db0af32a305835217289c32883d23f64<br>SHA256: 9bc7152bcf323316fc78e69cfa190cbddf22834208f48cee2e624c18150c9478</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.63MiB (26.88MB) – 331,798 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264a68f442d85aea134072d7bca0f4fe<br>SHA1: 65171ab00588cb7f2ae029d9345b44cccc888d24<br>SHA256: f76d40c34e6881d9cf3d98b34ced8105e9bd9efbb3f55e2bc224ece181569030</pre></details></small> |
| | | Full Location | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>186.8MiB (195.9MB) – 3,075,320 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96e5fc94ee00f3349281d3d79c8e3e83<br>SHA1: cf6b55598525f02890d9596fefd546190401adc9<br>SHA256: 5dfdabdba40afb770f6ff5afcc35db6136e9e28182bd6b3fd23b3c203dca5d1f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.3MiB (303.3MB) – 2,504,397 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bcf1dc4f4611d3e39906c6048aa8fc<br>SHA1: 2cd36733f3043bb3d9985d20fa8416a68b122e30<br>SHA256: e3d5ccb9e02dd929dc48ad40f82d484f9ffe60f9098c5a3ac296e33c5b9c2a9e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-11-30<br>IPv6: 2023-11-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.454MiB (5.719MB) – 232,687 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7477aa0dc6695ad8d9200f94b8afd3c9<br>SHA1: 34d4e346c0da88e6d4f5988e17842c38d421b8b3<br>SHA256: 46a50da207a830584042870aa5b87c2dace68a946829e6fae37461d5b3427d52</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.74MiB (20.69MB) – 255,480 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efa7b87bcf99ba42fef37332f83b9e16<br>SHA1: dc9a17b5c1ee4e438d266c97c5aacd40da6bd740<br>SHA256: 24e3b2a9267c9b1de9614d05ec54385e3a732757a59c19eb3287899959cf7932</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-11-30<br>IPv6: 2023-11-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.2MiB (180.6MB) – 2,812,463 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4dbcfaaf8038ec905802f3bb4b98e60<br>SHA1: bb90c332e6a73443b2c214fd4c7c111fb053492c<br>SHA256: 1a5d0936e7c432fb29ae976e5de47f83fbae93c0e2d594781ab883143984266e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>176.6MiB (185.2MB) – 1,539,981 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa785991c752e8ca7a545029b778d706<br>SHA1: 641faab98a0a64a049fa166c4e4cee2698daa00d<br>SHA256: 7dec5cceb89309fb14723f22484df38d79bcc79adcd23394d5ce983d4a58e8f5</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-11-28<br>IPv6: 2023-11-28 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.69MiB (11.21MB) – 456,068 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 174288b5d52aafb1b40463ed63a1f353<br>SHA1: b3371fb62814509ccf1363fc35b243c541b1388e<br>SHA256: ec42d65e548522aecf772c84f3303d32de153239aa6b7259d1d2f42a6cae511e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.38MiB (23.46MB) – 289,656 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca9e85e44b6c1371fd63e1bc443e5d43<br>SHA1: 1291b037c560943c806d82e32bb01ba33da9c9b5<br>SHA256: 489595823ff339ab2133fb1b919278097195e02ad730d647e575fa6799348d8d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-11-28<br>IPv6: 2023-11-28 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>163.6MiB (171.6MB) – 3,244,060 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3efef7562f359b4242331e425de3df1c<br>SHA1: 2cb768466e1b4b41cff89f7fa903794a8a4063d3<br>SHA256: 4b27f8cc48f05d99ab04506c7ad19f9f9fec840697f996cf0ce262a00a74f1f2</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>189.4MiB (198.6MB) – 3,244,060 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2851da38cb79fca0f8a9e8c0e85240f6<br>SHA1: 294455eb136b17b5501e07975c4b962f0d6f6f60<br>SHA256: 73315ac1e79628a3ca47f29fa4fceda02f6dc0367c41abe9c375c683175a921f</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>167.8MiB (175.9MB) – 3,244,060 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3588ea6f6aec455f9cda7455104811a<br>SHA1: 821f082f8d697de61488c428c69bca562694ea88<br>SHA256: faa086f91147b27ceff1fcc4d1d1e1be43433a0a827e4c0cb8867b9abae2eacc</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>173.9MiB (182.4MB) – 3,244,060 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232d78c6f3e6b0d239d10d0b746f576f<br>SHA1: f400e2ca05c5fb697efd95f56849208042f308f8<br>SHA256: cc65e8f603c84e2f41c69f41f953873954f91a5d4f8b0bf09a997fc6c6ccb967</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>198.6MiB (208.2MB) – 3,244,060 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f86569f72f7a7d6b839404f5c9c1ad2<br>SHA1: f2142d5085062c3b4d1d9253d4c19b95ef267383<br>SHA256: 2b22c89bb7012d594b681c83787245213e59ba38edab643993d0f40b1a24e17d</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>162.8MiB (170.7MB) – 3,244,060 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3504a3583ac98a4dff399331d81090be<br>SHA1: 9ff03334508d081f19c2f2ade9f5d2c3e4c2264a<br>SHA256: 3973284b648733edf2937d58f234a296cffe462cae259fca8fb355a8ec927283</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>200.3MiB (210.0MB) – 3,244,060 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4362c16794aa6c3382028afd1bfd8d9<br>SHA1: 24dc50bd1fe7869956434223563dd4aeb9d4f56d<br>SHA256: 29a7493a79b8771df201d5903ce71b169e92650e2d1f5c6a4328415f3fbb9db8</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>169.7MiB (178.0MB) – 3,244,060 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c2426956409e46382850407f693a4bb<br>SHA1: c603e89ea05755030840dfe6be2972a89a79027c<br>SHA256: 8979c860b23ec6a9823379e3352a8adb915216d7cbdb18831d73da997d721193</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>124.5MiB (130.6MB) – 1,238,116 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c6e80482d017722814aa92b6a69bc78<br>SHA1: 9492f628c5dbd965d515e4dcc166ee30a6bb3730<br>SHA256: 17346e8b122e5ef976bfebaf956d371941ecd5cd7534f710cab6eaeefbd23a35</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.5MiB (138.9MB) – 1,238,116 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d41bbcfec147adeb414894e52b1156f0<br>SHA1: edefc1e6abd4e10e2ef60df63ba2145dd74d52d8<br>SHA256: 4aab0af54572f42f01a890f2e468d23e4f2083c80a737366aad451b1be58b0ea</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>126.8MiB (133.0MB) – 1,238,116 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec1ad4402171a3c2ac46da3db8ad6d40<br>SHA1: 9d9ba87d7958993b4db8b00401eb7ac45dc27291<br>SHA256: 508d9c34d6f9bc65782597881aca40512167d2a99011e874d2c0aa35795cb1df</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.0MiB (134.2MB) – 1,238,116 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5428920e45d79be5328d540a4e7b62f<br>SHA1: 2d9e0bf7b050f77b8619c10ba0618a10604a9d98<br>SHA256: cdbf88bd5097fcaff2b00a6dcbfd5c47532fb50b0be3e7f4e5f892defd7d14e7</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>135.6MiB (142.2MB) – 1,238,116 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3bd21271cd7840dec3cef4b0bdb7cf7d<br>SHA1: a52a07374bf3b47130dbda64ef8fdff45b0f99eb<br>SHA256: e309d6ceebc59f178812d8b3e6060417741d5ec09a8c55d68aa27d7520895e35</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>125.7MiB (131.8MB) – 1,238,116 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49c9d6e903226b85dd4ae88f86218666<br>SHA1: d2ce001b324ea7e5fae6ac049a1eba3292978756<br>SHA256: e85a3066b40650f9dcba6472b1ab6d17ad0069e99d693f895603f5434f6dbf7e</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.2MiB (142.9MB) – 1,238,116 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e89344d66a0bd95a66dc4a380515697<br>SHA1: bc6294e7b6700cc73f89f680855d3547292e6f87<br>SHA256: 77bf706289c5984c2242bb9dfb1057b2018ff005e2374765220c169001614b4a</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>128.5MiB (134.7MB) – 1,238,116 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0c896977098bca2254804939fd32431<br>SHA1: 1a179aa7ad6269219761599be4aeed00b200926f<br>SHA256: 209a09118f5c1ffe4191d4ef60fd906b82a21145db6f09e8a2446dfd75f07b31</pre></details></small> |


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
	* Store the IP addresses in hexadecimal format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
