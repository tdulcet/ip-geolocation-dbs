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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-12-21<br>IPv6: 2023-12-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.607MiB (5.880MB) – 238,829 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a4c1adfdbef5d325859df64d6585f81<br>SHA1: 50bbff889d1561fcbf73f782cbe912ab38680c97<br>SHA256: 30c4c00c8a62ed473b94d703b2d39cd91a133d66c8a904d6297dc57ae9297058</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.340MiB (6.648MB) – 82,068 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956776a372a42532a9efeaf3746e42cf<br>SHA1: 16c5675338aa33fc40e0a46fcf3bab801297ff4d<br>SHA256: d55e21f2ecfa5e1267e0984d243d80d4314238dfa0e60d9a09df4754ae82d698</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-12-21<br>IPv6: 2023-12-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.718MiB (10.19MB) – 412,756 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3cf29d8f76908a4e7c738f4fa6c3899<br>SHA1: bed4b3b496d0e48411f1cf8ae27b024483d90930<br>SHA256: 31fe6e7acc436eb3fe730aa60880a78319d7f395aafb701643768bc4d30a4742</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.079MiB (8.472MB) – 104,687 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c77b2db5e0a56ff4bc1d142bcc1bd6a5<br>SHA1: a1f0345b6ba7c3272688c36d6b6d08f35e38b3c4<br>SHA256: 545912cbb4167395508aa9f16b3ebf0902f4d56eabba9baeb9a8028a4aa3c9b4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-12-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>21.52MiB (22.56MB) – 914,466 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b7777509c18714332289128fa8ffb6a<br>SHA1: 798c28909e465e2929d9cf05674530be08cf622b<br>SHA256: 23769fedcbebed6d77a4b2c56b7bbf4fda88cc68122079d56707bc2c73321c46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>161.8MiB (169.6MB) – 2,093,937 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89dbfa47e1580a9493311d2364215179<br>SHA1: 1cf4040fb9506284096d3710d6b0bf928df686e4<br>SHA256: dd88a7a6a47983eb017be1c4d2559752bb2dea65a3d0b097cabbce35810f5680</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.227MiB (7.578MB) – 308,674 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7862828d186c4a916870bf5ee5c2dbf<br>SHA1: b2d61949f9d4cdf20a7bbe7858ca457da6437400<br>SHA256: cf718693f02d6570f872d99279b6729e48674fdf9a0ad17b2b5bd3a3004e7feb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.88MiB (26.09MB) – 322,049 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf9a945a8ed9ee1ba2168317dbed510<br>SHA1: 5488b48f6e283b58e14057f8bcc69c7a60073e80<br>SHA256: e724c992a57d034ab069e985589127206d0519f5cb5070ef4d8bc04d59937e7e</pre></details></small> |
| | | Full Location | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>188.3MiB (197.4MB) – 3,100,304 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e98adbd1d81ad4e7676a5bc97c6062eb<br>SHA1: 83a91e8b43cbdbea769542d684e8a2b61d6cbcb4<br>SHA256: 07faf7b0b69afe9bdfb83c30bf26ed6a6bc739fc4122230461107e862ca8202a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.3MiB (310.7MB) – 2,579,379 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b45c72d3f47f242ccb1124627ab028<br>SHA1: 46f55d20900ce13c49f5881ad197bc7a0d54d072<br>SHA256: cade24018cccb007f481018f12d82b3268ea4089c4223c710ce4213be2f799e1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-12-21<br>IPv6: 2023-12-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.454MiB (5.719MB) – 232,687 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7477aa0dc6695ad8d9200f94b8afd3c9<br>SHA1: 34d4e346c0da88e6d4f5988e17842c38d421b8b3<br>SHA256: 46a50da207a830584042870aa5b87c2dace68a946829e6fae37461d5b3427d52</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.74MiB (20.69MB) – 255,480 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efa7b87bcf99ba42fef37332f83b9e16<br>SHA1: dc9a17b5c1ee4e438d266c97c5aacd40da6bd740<br>SHA256: 24e3b2a9267c9b1de9614d05ec54385e3a732757a59c19eb3287899959cf7932</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-12-21<br>IPv6: 2023-12-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.2MiB (180.6MB) – 2,812,463 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4dbcfaaf8038ec905802f3bb4b98e60<br>SHA1: bb90c332e6a73443b2c214fd4c7c111fb053492c<br>SHA256: 1a5d0936e7c432fb29ae976e5de47f83fbae93c0e2d594781ab883143984266e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>176.6MiB (185.2MB) – 1,539,981 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa785991c752e8ca7a545029b778d706<br>SHA1: 641faab98a0a64a049fa166c4e4cee2698daa00d<br>SHA256: 7dec5cceb89309fb14723f22484df38d79bcc79adcd23394d5ce983d4a58e8f5</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-12-19<br>IPv6: 2023-12-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.70MiB (11.22MB) – 456,446 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: adf7e199147e8d80b71fd93be4f6bb30<br>SHA1: 146072c06b78a70e05f409b673880e7292e65873<br>SHA256: d2101a40212b390ee8b9dd63578a9be8dcdb83f159c2ce205e4d43b8176e98b2</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.19MiB (23.27MB) – 287,258 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 073f8d1b9d3ef87e382b405bf8ca1b39<br>SHA1: 7b96d894d6e8bc716f6c604c9616928afbcd1c2d<br>SHA256: 2f5b0b006820c9af890172b8debd3bca2b314b1fb3e040f05982cb77b3b15d7a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-12-19<br>IPv6: 2023-12-19 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>177.3MiB (185.9MB) – 3,518,876 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 170a25b48e64980dbefe77876ea98aa2<br>SHA1: d70e365389d38f1b0b4002502e5cda10b34d5696<br>SHA256: 445ecbd75fda60211499b5291f29cdba78a21d3cfe37e1d8dab7aaeeb4caaf6d</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>205.8MiB (215.8MB) – 3,518,876 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5477761c82150fa66442d01482a0ca1<br>SHA1: 43de84bd292811627687d112823226da9231e89b<br>SHA256: 48eda3392e134699ceb870875b2347bf0fa91a3de26d4fba74032fe4537228ca</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>182.5MiB (191.3MB) – 3,518,876 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 764813ba28c70dbd44d3592fe726624f<br>SHA1: 739b34a87e9c938485e4665dfbc9dfda237347bb<br>SHA256: 4d0da8f183c931c407518a149a58c791eba0c420fb668bbe66d2f7cc32b4d671</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>188.9MiB (198.1MB) – 3,518,876 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a46f72665ba25222fdfb07d8bf466220<br>SHA1: 62dc7cda5d3ff2e5cd0d9fa391bd34b57e7217da<br>SHA256: b066bb2dfb1dc658671dde1a4471eeb4f6ca8fdf7f10f1cd425c9371bfe5056f</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>217.8MiB (228.4MB) – 3,518,876 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 367c8d52f539477ef37a75800c6a495b<br>SHA1: 427bac1a0a2232b11eced3b31189c2b9ec880ee6<br>SHA256: f7a704e1bb38c1a7f891fd966e2f5f41efbb74e44fb377952ff87c1fdf8bf6f1</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>177.2MiB (185.8MB) – 3,518,876 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba91a202d7e71fa6245ad39ee285a877<br>SHA1: f65a67fef6baec3e57f56943a24cf50b554cdaa2<br>SHA256: 54c1816dfebe9e6c14ad693136131f79b256269792a1aae3001d0f7316fa8b3c</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>219.0MiB (229.6MB) – 3,518,876 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1199c06821e1e4ab7ef1cc5d6487bfe1<br>SHA1: a1fbfeb9825af290fb9fcf3ef6f07e271174d9b3<br>SHA256: 1c48deccda302deef1ac92522a58d0f27489fd3b121efc66258bd3e6215552c2</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,518,876 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6980d3f979313fc868f3c41397e8aaee<br>SHA1: e0f9d1a78aa2b10ee69f2cd977417ca1df7313a0<br>SHA256: 6ace6795fd72e219021d80b3da383c81bebba6ac746b4ef03f7a6de27d795f7d</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.7MiB (128.7MB) – 1,218,689 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83489960f3b26768b58ad460a214ec7a<br>SHA1: df54fabac7c3681602ecde0d7ebceb228c4f3625<br>SHA256: da386c4947b4298352555c7bc18e9fa39a5a29430b641546d66f73d0e12f0dd5</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>130.6MiB (136.9MB) – 1,218,689 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 470e6648394dfcf8fd0720b2c6389425<br>SHA1: 169c8802a756b2223ca98b99fbcc5a628d8254b4<br>SHA256: a24aec56ed07ab8039b7f7c5a5de4730169173e3d0322a4ca26706e2e2df3af5</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>125.0MiB (131.1MB) – 1,218,689 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8457bd66a5b4da6a7d3edea03f3d7c6<br>SHA1: f499c19f1e014b6694316f0affa82bf524c4d224<br>SHA256: 1a8a2dd5425ce409c318f5a91b7d034566dca0a94badd86401370840de5c27b7</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.1MiB (132.2MB) – 1,218,689 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3426eb930cf81c3a51527d3bc013652<br>SHA1: b18b2a688da8f851281a7181579c80a7e3016530<br>SHA256: 4d023b54c2a6b645f88fa9b2e995a679e81b1e481401cc6b9c48a263a80c0ac6</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>133.9MiB (140.4MB) – 1,218,689 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 538e33bef89e02c26f417a182a68d4e2<br>SHA1: f068c84cc49aaf9f905b7dceae7b2e070fdc2199<br>SHA256: 2efd044190fbb4805a549006e9dfb0114f5847ffb874276e225a9ce42a97578b</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>123.9MiB (129.9MB) – 1,218,689 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee27201bac8283eb5d27b21de45f63eb<br>SHA1: 6345e8721286da2a8591c987e2c97ab4bb6f2027<br>SHA256: 12e0fa6e2aa55130066fe984f0409927cb246921f74d6a8b9925fb4ad6f693e2</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.4MiB (140.9MB) – 1,218,689 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3370005d015f2b7cbfe113f560e07a1f<br>SHA1: 6761edc48dd98ff6dcd74d827bb7160bdb50b4af<br>SHA256: 03100373f6717a5e6e46a16fac3b8cfcca79ac25722f744679f7a5ba4470efc6</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.6MiB (132.7MB) – 1,218,689 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f13f325f8aef498b36f11933b4a17c3<br>SHA1: d1d4bee99fbd3a0ac3f06b63b3e866bc973120b8<br>SHA256: eed131c934628eb00c670a851e4e5c50c017064315fd3cca43d6e3cdbb93dcdb</pre></details></small> |


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
