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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-01-02<br>IPv6: 2026-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.437MiB (6.750MB) – 322,348 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40b5402b79f0446ea2366a1e52714964<br>SHA1: 36de08d1b3388e16ae04e96f8acd70aff29dee39<br>SHA256: 9807182797fcd4fe938a90978748454611d6f16a7a79f6100168e1fb95243e9b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.13MiB (15.86MB) – 229,927 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2afb2c69e11a485b25f6b1e70ea67661<br>SHA1: 7be0871eafb9d13d2933307131233efaf4ee7e88<br>SHA256: 9ec107dadd46b6becaaf37621bd354031b53c59ff248efa339d4eb6cb1b87d88</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-01-02<br>IPv6: 2026-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.182MiB (9.628MB) – 459,715 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef38cc33303892bf51aa949f49432dd6<br>SHA1: 684a429c63bdb0be28be2312c5617650749ff337<br>SHA256: 3505948fbd0ceb6722d5b2d9efd0c869bb14c582eaf14fd237da37e5026e28ce</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.490MiB (7.853MB) – 113,933 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8e4f5e62d9d3d6003398763bf803a5e<br>SHA1: d45f669f9a0679c20b12a3cafa77273c6b81e794<br>SHA256: 44e5ab803284004d5da97a4a9bfc3f93af269ca9d7344f19d7a40bb018e6921a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.56MiB (13.17MB) – 628,919 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f816d9cf46e35539d88d2b6fe29573cf<br>SHA1: 183232a2ae199964a45f541d4129c7dc5eb1c561<br>SHA256: 9ccc35eee34cd424553888f18e469e50af715ce73d9dfd76ce2187bcf47229af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>64.58MiB (67.72MB) – 981,470 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98abfe38493f092216acf6d405d7543c<br>SHA1: 0b2817bb746e153c60119653675e0270401e7526<br>SHA256: bde98f49229322b41f99a71dc1025c37e6bdb86d3075a476431e7483852f56ce</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.843MiB (7.176MB) – 342,905 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7f0c42b88b3ee5ac2070e71f756f963<br>SHA1: 4416542c9574226ce202070dc48ca08edc6fab0d<br>SHA256: 5393382f53c552965d88b65e40e02f63c643f2379a931aaecef8209586b9ced2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.52MiB (17.32MB) – 251,059 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232548602865156556e4ff9d7db331da<br>SHA1: 61d1e0b2cefeca101ea9e8530969dab152188ab6<br>SHA256: b004edb93559a31ded3baa727a5d781edbe90c29420b4d5691f44e917e83bdb0</pre></details></small> |
| | | Full Location | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.7MiB (223.1MB) – 3,730,744 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42e04cdc8d81a8ce6b440accea48b373<br>SHA1: 9c414f68d243d9ebdc8b7c65e081580b035b663c<br>SHA256: 5274313529b847bd8629fb44b41144c683552f55760a830f535892f20b8e46db</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>457.0MiB (479.2MB) – 4,442,155 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56e8f0cd6817f6807824ced45628cb9<br>SHA1: 316812aba9e80b97b08bfca58defd796b628d008<br>SHA256: 44317ed175935104135d379f2a9918ca97141e9bf034ee1bca6cdf894093d72c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-12-31<br>IPv6: 2025-12-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.249MiB (5.504MB) – 262,700 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1336d51547e70ff41f1e470101d76301<br>SHA1: dbc5c69176db1e71290241508d9bf23d3fbc7c99<br>SHA256: e1be0793199e009b2d581c68300def944a9534d67b3357dba466bbc4e29c4608</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.00MiB (23.07MB) – 334,332 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7de5c30d61a35275c4463ba1939d47a<br>SHA1: 187b58e38e8853be50cbc6bce0c609f30fbb700c<br>SHA256: 6dd9378a342492e7af6faaf3f48f8ef56f75a9870b6cd6cbbdcdff264db76afd</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-12-31<br>IPv6: 2025-12-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.7MiB (179.0MB) – 2,955,286 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb75d526f52d515d850e10a62f3ce7a1<br>SHA1: fc0b4e2c3eedc461e42d5fa445bfd64c25832111<br>SHA256: add4cb25ee97481f007b554ee596a004318bf30a9034a47e9fac209eb7947e29</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.3MiB (302.3MB) – 2,794,225 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfbae8186489381f9b07bacec41f902b<br>SHA1: ab0c06ba27f24066c49aa9282addd61ee7f70de4<br>SHA256: f67f46b0227237d8454f4b74ef88bd4742945b80e8efd3dfbd080bb0de4e5229</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-30<br>IPv6: 2025-12-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.22MiB (12.81MB) – 611,578 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9213560b36d3ca4b1be014bba2a17fbf<br>SHA1: dac878bee1cd33b8be90ffb1e10f7a54a89b38df<br>SHA256: 56ac623c338e2b817bcca9b5aac5f2b922441eaf7517b3b2207c680b6bf505f8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.59MiB (44.66MB) – 647,293 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ed416ec0fc988ba1cccc8a5aeb94580<br>SHA1: f8cc7efe08758eb7a4d764899a81f2d123b817d3<br>SHA256: b185aa8566df53f45fbf286a4423b44bc4a767252f8603bfa3aea63c481cf956</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-30<br>IPv6: 2025-12-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.1MiB (186.8MB) – 3,516,937 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d096fbad9c0dc5b240d0fac5928a98ae<br>SHA1: 90885b1e04901e44754a2ad61c3553ba95c0b445<br>SHA256: a45b169718eac2c743c68b91021a21ac4fa4ecac359ab7c6b9ebf5c5182d9bec</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.2MiB (198.4MB) – 3,516,937 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 870d688b59764bee6aa5f265c2c88e80<br>SHA1: 5cf7de59a1d7cca012ac5f5e75fa9f61a1c27f0e<br>SHA256: 295f4b14d0d68cac00d93ad25ed308c998230feaece38710e861dc59a300c476</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,516,937 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 440c4fd81af70170b6c70787fa93000e<br>SHA1: 514ff703d68cf74394b34848f69c309e6b3512b0<br>SHA256: e033f553403b63ccd24cd3973f38d6145109ad1ff5f0cff57d5d86e9958f3042</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.1MiB (188.8MB) – 3,516,937 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c94aef2916d26024678e01b87f7bea9<br>SHA1: 0629432a7321df910915bd94c3078448f1dd2ed7<br>SHA256: b621483abba2bde5391518dcb3217093fcc592cdfd47918786e72d4a28187652</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.0MiB (236.0MB) – 3,516,937 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 930071b42da4b93179b0b4c654848c8d<br>SHA1: 73219074a973241fd2cac367251aaf2190b67833<br>SHA256: 09ac4c4d93149a7ec756e24d8567b666023519b739d7dc94906ea18219e2c92e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,516,937 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01ef7dffa492be36c330c5e40b3cc985<br>SHA1: af557a5891a2139069320181c953b5fe9014757b<br>SHA256: 2dc751dd001b241eb9e0553c331a5afddd036810485398f8457a0a6c57914c9d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.0MiB (229.7MB) – 3,516,937 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0440178763e0abc062bd858d077f9a2<br>SHA1: abbd420e9a4a6507623e71594ad356f96754d81e<br>SHA256: 8378c7ae375024c675cf78a0cc74af26bc4b4a49a12a484d757942764781f993</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.9MiB (192.9MB) – 3,516,937 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fb460e193cff5eda8c2f7f09c3e03ac<br>SHA1: 1b084dcf0643924ad99eb6e3e7a00d67aaaadb6c<br>SHA256: c161de9336d5d5982638d6715f76c532500b7fca2ee4e32a87d2a2c36e999bc2</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>183.6MiB (192.5MB) – 1,937,153 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11b4fd20747b2e369870677c49f16e06<br>SHA1: e1d238b40101f23882050bbe9bb12448ac3cc29b<br>SHA256: c72d2a29b85d6d13e1bfe94ac6b19bf6f08acfa345337cac532305871aef4f92</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>187.8MiB (196.9MB) – 1,937,153 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5393059ca93cc88ff028054e13520460<br>SHA1: 432e2f29baed57c58724ba00cba41caab9574d8a<br>SHA256: 8a14c08a4ec756bd8ab34d758b9f67afd07fa74ab07881c9248d4e4331037697</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>181.3MiB (190.1MB) – 1,937,153 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e19e304170fa6bab9f595d7ca32e2b35<br>SHA1: a31b77fc0c4a9fd1a74eea40e90f3c931f472b07<br>SHA256: a528366883f269e6ca0b25ec5527d2680e66f87a27aa5706ff6dc561a56475c5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>182.1MiB (190.9MB) – 1,937,153 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fa61d6882eb24b35b466e5f86a55705<br>SHA1: 8721ba492af53a7fe0cf8f1735f4c8124269cbc2<br>SHA256: f4fe09e9906450e252d20320bc7c23d117e88ed8600ccfbac9dcb68799ccd99e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>201.5MiB (211.2MB) – 1,937,153 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8f3ed303ec3f46c85e329aa00911efa<br>SHA1: 8ac20dd8205a2463be81ee10f7df43656cd20387<br>SHA256: cbe9fa3c882d4d5ebae956910f19e002598ca262e90245617909a29ecd202a1a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>181.0MiB (189.8MB) – 1,937,153 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 617b00d96e785ee70de9b6fd495f307b<br>SHA1: c7ac74d104eeb0656ca773a252642d5963ffd0ff<br>SHA256: aa0eec7080a331a55ccbff4332249f38036e1f99be3c30c8da7dda4b69a8c8f8</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>201.6MiB (211.4MB) – 1,937,153 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 317a91278a2ff9f22a355b1dfc5a9472<br>SHA1: e9e5ee09bd9b7209c27bb488b45c4a6eeb22ef4a<br>SHA256: 834cf2288e4e21b3dfb4fcd425c23f2d2b585d263c86aa23dc371420e5a83f4d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>184.6MiB (193.5MB) – 1,937,153 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0c2502793cd4d81242f1ee994510c14<br>SHA1: 08f6f62b0b4b2eae624806fa584ac2608d9ea25d<br>SHA256: 02dd823c953b0994534584473ce244ef869953e4376de03f1ef41084100e27fe</pre></details></small> |


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
