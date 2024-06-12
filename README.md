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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-06-12<br>IPv6: 2024-06-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.733MiB (4.963MB) – 236,960 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 407303426f42670d1b08ee65b040f0ae<br>SHA1: 97b2bcbfd2799be94be771e65817a01df65f588e<br>SHA256: 92b072d2d62896d8d88e874c6e786ab6ba8f470d9423c9bce695ae77a0a5aa13</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.452MiB (6.765MB) – 98,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 961f390f7babef34a4f5513fbdf8f36a<br>SHA1: c40aa51a68b1694cd6887e1ddbad036380d5f64e<br>SHA256: 66ceb266809677435d003f6c78d46267bac5b489dbfc95ec753d45e0f6c2d951</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-06-12<br>IPv6: 2024-06-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.089MiB (8.482MB) – 405,078 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81d8db77766d7b487fd46111dcc9d305<br>SHA1: 9ada73a0db03bb669ef1d27b684c9d87c4c9a9ab<br>SHA256: 159deb920f26a32bc1c83f26a808b049b00a8aec07a7af4764c9d4045a66721a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.407MiB (6.718MB) – 97,478 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c20112618a5b6a1ec687840c401e1b66<br>SHA1: ad1c079c0df84e7e217eb7c5e91f8f21ad26200a<br>SHA256: d41a0b60bd8e54ecea4ab851cc14e49ab053e1ff94754089b871998947fede21</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-06-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.76MiB (18.62MB) – 888,480 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1eb704594429dd30a4a79a8f0f5890b<br>SHA1: c5e0b8d5ad674e4441ec4072991f5ad6bc3e3e4f<br>SHA256: b656d412e3ee4728e043c83820b29a778c2e255272e33eff563afb63e049281e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>81.67MiB (85.64MB) – 1,241,139 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fead5430e293e9bcaf23bb52d6335252<br>SHA1: 825bd3eb0817da00227ff99585a6b3fe8577000f<br>SHA256: 61375a0d11f51b0f94c85b7dbd1e3864a650f62e709970f39ef57826e77e3279</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.920MiB (7.257MB) – 347,790 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228d49dd4c10c1d4778473109614f06<br>SHA1: 84aeb9072586fe27e7a2fd0cdc62b4421b417010<br>SHA256: becc801a5b95a0c7e6dea789881460b3cce70a60f8b941077db5db9f24f332a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.87MiB (16.64MB) – 241,164 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77063c075f456a1e11f7a52af24ac9ce<br>SHA1: c787ab002266a3398026d5342c963fd1ea59f3b4<br>SHA256: 72503d5df7ba2b39c61d7f574dd167649fdff103e81019ba98b18c192a045f0b</pre></details></small> |
| | | Full Location | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.7MiB (195.7MB) – 3,261,621 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d700e342b096e0b5285fb98e7ea719e<br>SHA1: 95986a4433c4d6be7ba8f0d38d9ac62adeb2d962<br>SHA256: 48ea78edb396cd5b834f2a55d80909bfe196c2ba8756c47776a331bc1537686c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>341.2MiB (357.7MB) – 3,305,843 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8cd42e639e764b6915b74d34e29681e<br>SHA1: 59487357d7497ea585a66be963038da0bd3d8c79<br>SHA256: 093ad3c5b00a0620dd5ab55a96d31fdbde283e096d5d86611cf2e0af2cb6f688</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-06-12<br>IPv6: 2024-06-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.893MiB (5.131MB) – 244,932 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffde7736a4dce2d1dc8a9bbdbbed74a5<br>SHA1: b43b198dcef1ba6df65e58c1860df753727d07a0<br>SHA256: 8724d93cfde83ae2b1ecc823b3e74fd2991e6b70f24b1547c184c710023795dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.66MiB (18.52MB) – 268,413 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0affbc6694e8124ef8380a96f029473c<br>SHA1: ee3211b937aab5e966a663960fff6c4ebac1172f<br>SHA256: 1ab2b436fcbc1c46882e731a91c9c9ace7151e260ba27191c665827291450dad</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-06-12<br>IPv6: 2024-06-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.2MiB (179.5MB) – 2,966,969 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23fb370ce2d6e35cc080047ec96854e<br>SHA1: 6375dc2f3658701b80ddbbb07172e7979cfd3c60<br>SHA256: d5616074b0d3213fccda295fa79eab456cf538541040ad6d2b330f9b8e18e286</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>192.6MiB (201.9MB) – 1,864,338 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c773064f37ebb2a011fd7af63e5eb82<br>SHA1: 2b1c4e83df9f45b9539528f8dc4a01a661ce71e9<br>SHA256: a4a6a481f67fa24ccffea017ecff51d398b6046177a33e77ad479f97889e8457</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-06-11<br>IPv6: 2024-06-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.828MiB (10.31MB) – 492,353 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b8f901e2dafb85699626a46ccf12122<br>SHA1: c8900edab7c2e334c7a87ed986f660d359153132<br>SHA256: a007a0e25305ea8d8c2b81522f5eb5ee7274b8ee74eb585ae10c2c457b03f58d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.21MiB (20.14MB) – 291,921 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2543da32cd98e025e444d4eb16d94a9f<br>SHA1: 1c48a7c0a10e13b318b33f01e27491d3baeb9002<br>SHA256: 049263ebf9f2072a3120bf522cd06cdc36f2c4c705ac4ee1b01b71f659425459</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-06-11<br>IPv6: 2024-06-11 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>119.5MiB (125.3MB) – 2,391,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c8b80175216df36f3356783da8d4ab4<br>SHA1: 92446e4d55da32b42c93f55f23d80b137f80ae33<br>SHA256: 0fdc8f4f2e2474016b99aefa179d8ddc8495974266cf7934d0a343b8a1d9bba7</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>128.5MiB (134.7MB) – 2,391,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ef87e33418919d9d54927d0e1d9c71b<br>SHA1: c078abfcb839c419fa61d06d47b0357d2248ad97<br>SHA256: 87e7a9b4e216dd0ea27e4b9f8028953808a3aef95c7226b9a7e44910c2a18579</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>119.3MiB (125.1MB) – 2,391,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9cc73dc6f9312341cbf0f0fd55850da2<br>SHA1: 42659797d9ac6a791a7c74e864ff86b94d584ef0<br>SHA256: 9c34ca0a0fed2ab2152a38b3948e03cb95df786f9c7b5138237cd65c15d1a1bc</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>121.8MiB (127.7MB) – 2,391,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b0e691666a35a81f99b402d5436b618<br>SHA1: c7bab206ae06178e66e55a9847a74172eb98ee7c<br>SHA256: dd05273785a50873d8c2a196139c7044209ad6eec3073f4e93504db0abd07885</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>149.1MiB (156.3MB) – 2,391,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1722b0e9e6d04874bccb8e581bbb792a<br>SHA1: e4b3e9b3efdea90e56aaad22cc8f29f49ca2fc4f<br>SHA256: d4ac11ec1ab10b52456c5eff2bf44f39ea3fed264436aa7168b80a66bafbc384</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>118.5MiB (124.3MB) – 2,391,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4541c5591dd4cf519cc82260877ecba6<br>SHA1: 6cf9e5204d8e82830188d7069f400968cf40cff7<br>SHA256: 0f34e8eb7fbdcfa259942ba29434f50a0aacebb6dc53fb0d5e90d192bdb72bce</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>145.4MiB (152.5MB) – 2,391,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eebe853c2be25035ddffadd75a7850ab<br>SHA1: ecff44a11b2e9a56435d25e386177b6afbcae137<br>SHA256: 623e5bc8f8d57559d1d26b53477d7d36c4e451a54686599c91586caa24e8614f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>122.0MiB (127.9MB) – 2,391,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e22257d6439f228d976c65d16037cac<br>SHA1: 5b2af3df2a425b059fc4f343b22cc60c2bafc50a<br>SHA256: bcf3c1d15a4b39b1a7b73a1385b6a97698222a83070a82d6a7a47cb0b0b7da7c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>115.5MiB (121.1MB) – 1,242,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e432afc49273096934f0294f74aa465a<br>SHA1: ecc0554e74f1a0f194c2b23b2cd0de23b313f2b8<br>SHA256: b3f3009cc9463e83ed16e0856e7c8969a3dd3d9bfd2c54f525d6444d1bfa2097</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>119.5MiB (125.3MB) – 1,242,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7acdd1fa3d1ce615e5469fcb59531949<br>SHA1: 0c7d06172ab370ee32c81d0384f4bda0c53ba88a<br>SHA256: 73bc01ff9894e0e9b263e094fd4f55e1f3e79fb0a62498904f468e794493491e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>115.8MiB (121.4MB) – 1,242,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d11133cf23f5cb85e19ad1ee23ca772<br>SHA1: 0aa5651841028399445220278fff9b802647dc11<br>SHA256: ca3e5665c4846cb292c83939dda5bdbefedfbd35d4a60e373c00703b5a7ce371</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>116.2MiB (121.8MB) – 1,242,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8db9dd506b03e202f19c34aac54a476a<br>SHA1: ced8494dd8b9666b818a5fbd4ed08bfdf6698a47<br>SHA256: 365d79c4b46ea180a4d472dfd855703b29a49e2c7dee710591160e956bea8411</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>127.3MiB (133.5MB) – 1,242,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae7c8c42e3dd8371b062b4973712cf08<br>SHA1: d83ecbf1404044042e852c3270db05b65602f258<br>SHA256: 9ee96038c3faa3d291e69ed13b3f806fd3e2be18f270f980044316f6381a26b5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>115.4MiB (121.0MB) – 1,242,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75e8d9f23c9ad6c0176c33190b1be74f<br>SHA1: ce150fcfe3b8b00fffcdc606e799182209caf41b<br>SHA256: 2b68d04bf4ca473bd77d856a3bc44744255927f5a5b6982b822499c9afe293ce</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>126.5MiB (132.6MB) – 1,242,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c6e751ba1e958ea79fffcde21544cd9<br>SHA1: b7fae4349b69c3e78057efd7054c27a535882831<br>SHA256: d239124dea2af8c7d5939e62596ec9df47729359b3af0ff11b21a495c7f526f0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>117.3MiB (123.0MB) – 1,242,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5394302f0dc1101ed0d6ad79fc1947a6<br>SHA1: a295aeb0ca11981a654b7ca54b88b8bd32955d38<br>SHA256: 588636a387f6eea99c69eace383ec5bebfbaac5e375cb0b7a427f228859f9b1c</pre></details></small> |


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
