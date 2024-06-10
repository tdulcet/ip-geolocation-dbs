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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-06-10<br>IPv6: 2024-06-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.731MiB (4.961MB) – 236,871 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2467965cb687d13c41d0ccede81fd1dc<br>SHA1: 2e672ae68fb927e0cea3974f63df0231b47280ce<br>SHA256: 996edda3ef71b4b844cd89a6d5e528b6137dd0a16979cf8c6e235841d84d2ea3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.438MiB (6.750MB) – 97,830 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 13fe6b003f888ea6dcc9ebcb007e433f<br>SHA1: af811fbb242af33e72f7d814edcdd223d17248e3<br>SHA256: 1d216165b2f16cfbc99e21d9824f11efb692db8382d05ae0b354cd37f4dcd32d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-06-10<br>IPv6: 2024-06-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.087MiB (8.479MB) – 404,977 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ba3e67697929273f2290a6becb56ba8<br>SHA1: e93582c84bfca630379773638014f523a92f807e<br>SHA256: 042412059892a17230dcdb38447751a0052857f4cbc73069aa55e3410b548359</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.397MiB (6.708MB) – 97,334 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0513649b52995d0ca11a2cb93ae0663<br>SHA1: caabe17ad69e9abb8d712f8105eadfa9755eed5e<br>SHA256: 169c3e3742da6445f0bf8b323585b2f2f56379dba71e97a9c54bab4f04d7839d</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-06-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.76MiB (18.62MB) – 888,480 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1eb704594429dd30a4a79a8f0f5890b<br>SHA1: c5e0b8d5ad674e4441ec4072991f5ad6bc3e3e4f<br>SHA256: b656d412e3ee4728e043c83820b29a778c2e255272e33eff563afb63e049281e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>81.67MiB (85.64MB) – 1,241,139 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fead5430e293e9bcaf23bb52d6335252<br>SHA1: 825bd3eb0817da00227ff99585a6b3fe8577000f<br>SHA256: 61375a0d11f51b0f94c85b7dbd1e3864a650f62e709970f39ef57826e77e3279</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.920MiB (7.257MB) – 347,790 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228d49dd4c10c1d4778473109614f06<br>SHA1: 84aeb9072586fe27e7a2fd0cdc62b4421b417010<br>SHA256: becc801a5b95a0c7e6dea789881460b3cce70a60f8b941077db5db9f24f332a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.87MiB (16.64MB) – 241,164 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77063c075f456a1e11f7a52af24ac9ce<br>SHA1: c787ab002266a3398026d5342c963fd1ea59f3b4<br>SHA256: 72503d5df7ba2b39c61d7f574dd167649fdff103e81019ba98b18c192a045f0b</pre></details></small> |
| | | Full Location | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.7MiB (195.7MB) – 3,261,621 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d700e342b096e0b5285fb98e7ea719e<br>SHA1: 95986a4433c4d6be7ba8f0d38d9ac62adeb2d962<br>SHA256: 48ea78edb396cd5b834f2a55d80909bfe196c2ba8756c47776a331bc1537686c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>341.2MiB (357.7MB) – 3,305,843 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8cd42e639e764b6915b74d34e29681e<br>SHA1: 59487357d7497ea585a66be963038da0bd3d8c79<br>SHA256: 093ad3c5b00a0620dd5ab55a96d31fdbde283e096d5d86611cf2e0af2cb6f688</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-06-10<br>IPv6: 2024-06-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.893MiB (5.131MB) – 244,932 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffde7736a4dce2d1dc8a9bbdbbed74a5<br>SHA1: b43b198dcef1ba6df65e58c1860df753727d07a0<br>SHA256: 8724d93cfde83ae2b1ecc823b3e74fd2991e6b70f24b1547c184c710023795dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.66MiB (18.52MB) – 268,413 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0affbc6694e8124ef8380a96f029473c<br>SHA1: ee3211b937aab5e966a663960fff6c4ebac1172f<br>SHA256: 1ab2b436fcbc1c46882e731a91c9c9ace7151e260ba27191c665827291450dad</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-06-10<br>IPv6: 2024-06-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.2MiB (179.5MB) – 2,966,969 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23fb370ce2d6e35cc080047ec96854e<br>SHA1: 6375dc2f3658701b80ddbbb07172e7979cfd3c60<br>SHA256: d5616074b0d3213fccda295fa79eab456cf538541040ad6d2b330f9b8e18e286</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>192.6MiB (201.9MB) – 1,864,338 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c773064f37ebb2a011fd7af63e5eb82<br>SHA1: 2b1c4e83df9f45b9539528f8dc4a01a661ce71e9<br>SHA256: a4a6a481f67fa24ccffea017ecff51d398b6046177a33e77ad479f97889e8457</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-06-07<br>IPv6: 2024-06-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.756MiB (10.23MB) – 488,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1053ab49c9ac0671d2dcb58716d6f6a<br>SHA1: 60cf697c66cbe0b7253d0fa932eaab68de180ebc<br>SHA256: 8b7713f289c85baadebf32161c3b1c9ff03fd582e56e77f5316cf42c066f8bc3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>20.20MiB (21.18MB) – 307,009 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1271053398c5993048a4fcba8420415b<br>SHA1: 059eaf8ec7abe23cf55320aa091e39a800edbd0d<br>SHA256: c9fedd0818f4a4dea2a3e9462d5be3c8e8a907216c63060cff765d35a4f0c9c3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-06-07<br>IPv6: 2024-06-07 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>118.2MiB (124.0MB) – 2,365,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14fa1067ed4b85a4373124da26b7325d<br>SHA1: 659c48dd23b5b8a78637c1a386225ce9c043a669<br>SHA256: f33f39dc9f1695cfe9e2df3c3fa788b666d41b1f6b861d01c476ddc0c7ef0cbf</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>127.1MiB (133.2MB) – 2,365,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2685f5e2f885cdaaafb29dd95ecb3ce0<br>SHA1: de2036a330c51126c675947031ef910c2862cdc4<br>SHA256: 55bd1f312362c8cbfe1a9f70b4f15ac54f084ac6252c203f1f8ffa54a2658d0a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>118.0MiB (123.8MB) – 2,365,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f60c13af01325f789bdb81f4939b2483<br>SHA1: 4ab55f9f1080a3c1dd24b5a5cbd0a9a5f7ca5116<br>SHA256: ac229061c268bac64e85e6cda7f3e68b41dd4756c683fe09260cb95cdf028d9d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>120.5MiB (126.3MB) – 2,365,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcbf1ffef8ee1b82e0d605039ac4f193<br>SHA1: 3d4ada787c8ab4c976ef3553370dbabd9e370322<br>SHA256: ad7a65f78bfdeca6b8a3103956acd9a0744d30f35d98c1a5c141eda33782aefc</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>147.6MiB (154.7MB) – 2,365,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64a66f3668459aecd6560fdaf2f991f5<br>SHA1: 2ba3fae71f97fe7dc0eb006bd496b66f685d35aa<br>SHA256: 376ba2eeeef8175b4de490b040a66047fea929c894b1e7723c166b5f50afc7b3</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>117.3MiB (123.0MB) – 2,365,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e82803b57a41c40e8a154c051bfd7456<br>SHA1: d52e2fea8e69450a617f345e4c6dfc2e2d9258b7<br>SHA256: 0637c0f17b547f47cd6ede9f756f2b976faf9578c09b78382fa3fe7a21607e2f</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>143.9MiB (150.9MB) – 2,365,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1673c5d6fdcd66e8fd258cacfea9cc2<br>SHA1: 04d2d8cb7a4be731832d9cbe3b25d7ccb6629330<br>SHA256: 956b55c0768312e1739fcd5b59af2f93b908c59aa3b3c99225986ff27d32b8b9</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>120.7MiB (126.6MB) – 2,365,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cbf1f68348a345e6bf81aff341e9c0<br>SHA1: 9ed292bcdf54a2eee3b6184ae2e00874a7cd5e13<br>SHA256: d6141da963d4905e43356dc206d1e4a7651c731faa9e5715bdab390ab0fc217c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>108.6MiB (113.9MB) – 1,160,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbdd8cd30f38c3f9cf42c5cfdd1caea9<br>SHA1: 23fd9f9195328e4d52d6cff37710d64b8b79aefd<br>SHA256: 6b09105fed696b44c98033903c68bde034aefe3157f79e21758cb54d04a3a536</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>112.9MiB (118.4MB) – 1,160,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76e5b3741e2f6345f9cc807e307edecb<br>SHA1: 56bb164781711b85d98a3c779bc6b69e6c5bc44d<br>SHA256: de34c342e9393d61a04c88a9aac183b8a40adf22ab9d8775466c7d8ccb3a8437</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>108.9MiB (114.2MB) – 1,160,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ced308d98f8a3f6aab33fad71ec1923<br>SHA1: d92e8e8519bcaf85361990cb659ed74b32457fe5<br>SHA256: a0dee0301de9d3ef512e8664e2f0aa630cdb1e27e91380c1f3137631826ea4de</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>109.4MiB (114.7MB) – 1,160,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a5581d57a187013bd4f3284e88fa057<br>SHA1: af263c985ee96afc6ac7c342bc09f685dd833967<br>SHA256: 8fd1fa29917da99d659ae329f3e2f7e15f63593a93a98c0a82fb50af6c4c5c71</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>120.6MiB (126.4MB) – 1,160,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7170758e653f32ea400a725231150c9a<br>SHA1: 9d817745ef1c07cd59995900b389658d40a97290<br>SHA256: cd6e3b455197e254b353d09ef532bcb4b0b1f3ae370d9f7e8f033aa9e03fbafa</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>108.5MiB (113.8MB) – 1,160,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 670311eadba41c64325f92d187844dbd<br>SHA1: 8b5cf7bf2c7c019c74df52502aaa44dbfc7d4de2<br>SHA256: c98b6a29945966a626de36ff05dfef29ccb234003f7d0a7625d0b0693edcadbd</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>119.8MiB (125.6MB) – 1,160,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8605b8d543800b89f002d28712cb8e9f<br>SHA1: 1a1a4f1675d36563a92a02b6058e325f929e10cf<br>SHA256: d898dcd403a09432d2a2f8065605406b4a85dbb3e88566e74e8c277df1dc1dec</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>110.5MiB (115.9MB) – 1,160,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb9f5de940cf51c60def7bdd7a74fd32<br>SHA1: f045d8afb975f62bcd2b4251db1eb43ccaa786ae<br>SHA256: 74c1687f075e838b812d7c5b14b215038e10ecaf90f7fa8399907a1947a885e1</pre></details></small> |


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
