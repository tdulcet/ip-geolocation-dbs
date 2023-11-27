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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-11-27<br>IPv6: 2023-11-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.600MiB (5.872MB) – 238,526 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c7d521f56a9ceeee1b159e0b9abaa89<br>SHA1: fd00f296d5e108c9c22c2530cf7229ffd0bd0b99<br>SHA256: d0366b5dab8ab3043f358537542e1d830d065a8488db56576006616800d69eee</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.348MiB (6.657MB) – 82,181 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf608b77b831d665afab36aac17755fb<br>SHA1: 3978eed29e7033ce77015084def2f162841c3b44<br>SHA256: 2c6f489905203ae46a6c122532a81930615fb54164df45ef1469614d551c3922</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-11-24<br>IPv6: 2023-11-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.660MiB (10.13MB) – 410,290 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b436d5f5afb4b0532cc19ca22dafc78b<br>SHA1: 29b4434602c1e6c48ae95affd04a1dc1c4bbe0c7<br>SHA256: 5a6b30b2bb901a7d296c081ad2bdd1d96749a1e153ebff23ded3e45203cc43fa</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.053MiB (8.444MB) – 104,345 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dcbb3b0b7e496426df0aa9083cbf1ff0<br>SHA1: 5fd039997eb4a1ced0bfdcbb4775e7399dec63ee<br>SHA256: f5d17091fedb27617ad5f90fdd717c11683fda4cbcd9476f60a37ffa9c36dcdb</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-11-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.75MiB (20.71MB) – 838,599 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51cbaa2dea4ffc0602f50a808f3af4f1<br>SHA1: 143c6795217ede025776bcad1aa5bdd88b7043fa<br>SHA256: 7198296b8c6d51a3cfce1d7793d106763600ec53dd99901d85adc8dab64e8777</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>58.88MiB (61.74MB) – 762,194 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9629fbd82327a2e79560267eece1f56<br>SHA1: 975028b29021aee870839f0d153211576b54a68a<br>SHA256: 31c3ffc928309505bf7b2727fc8e6414aff8a72da0b153c962a0bd97134301d7</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.260MiB (7.613MB) – 309,964 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7fc3106cf6c65db7d44df8b4fb1d16<br>SHA1: 6ec97588db0af32a305835217289c32883d23f64<br>SHA256: 9bc7152bcf323316fc78e69cfa190cbddf22834208f48cee2e624c18150c9478</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.63MiB (26.88MB) – 331,798 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264a68f442d85aea134072d7bca0f4fe<br>SHA1: 65171ab00588cb7f2ae029d9345b44cccc888d24<br>SHA256: f76d40c34e6881d9cf3d98b34ced8105e9bd9efbb3f55e2bc224ece181569030</pre></details></small> |
| | | Full Location | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>186.8MiB (195.9MB) – 3,075,320 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96e5fc94ee00f3349281d3d79c8e3e83<br>SHA1: cf6b55598525f02890d9596fefd546190401adc9<br>SHA256: 5dfdabdba40afb770f6ff5afcc35db6136e9e28182bd6b3fd23b3c203dca5d1f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.3MiB (303.3MB) – 2,504,397 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bcf1dc4f4611d3e39906c6048aa8fc<br>SHA1: 2cd36733f3043bb3d9985d20fa8416a68b122e30<br>SHA256: e3d5ccb9e02dd929dc48ad40f82d484f9ffe60f9098c5a3ac296e33c5b9c2a9e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-11-27<br>IPv6: 2023-11-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.446MiB (5.711MB) – 232,323 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f7d79b6a3ef8bc35c3c8381e7c028<br>SHA1: cbc8e9cbd5c151f0cdb02a21e5e6fe9d8b662cc8<br>SHA256: 9f3976e09ec875d7e97185503221656e80f41f531e268da1bbf874127de2583e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.41MiB (20.36MB) – 251,316 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df2ea3be7027267ebb1947b4220cc4b<br>SHA1: e94b6a993297b5dff456113130c22e323534e39e<br>SHA256: 44458ed651d7b4bd99ad73459d500395c410da1b2fce9fbb2c4e5ce318c4bcf9</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-11-27<br>IPv6: 2023-11-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.3MiB (180.7MB) – 2,814,468 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25688ced507227d7990066c41a0d58d6<br>SHA1: 28da5022ff88d543bba4e15cc01b703781801bba<br>SHA256: cf219cb6d358d6e4df364a87f28817e4aaf8322370b86495ef74cc1941c73f5d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>171.4MiB (179.7MB) – 1,495,017 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d4ab0c657ede6538d2756cef356f5f<br>SHA1: c2865c0d416ae7143165db8aca21627725b4b45c<br>SHA256: 66022701ed347d75f4f400e76024ae545696e742e4c0fd30bedf981c262b318b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-11-24<br>IPv6: 2023-11-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.76MiB (11.28MB) – 459,096 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0da9c41ecb48466b7cc6e1129165bf4<br>SHA1: 3f06e4e50f0cad6788cd324ed48f488345e2155c<br>SHA256: 35730cd9dd24fdf0d6986c62112337c9152af8c036ca1539be30c4b5ebb7c93b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.75MiB (23.85MB) – 294,490 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b838cc6c79eebaabb3921822d742e405<br>SHA1: 973e43d289168b896daf5a76d980b07b4cf263a7<br>SHA256: 33ad365df3eb2d60e3b72ecf571ae0cd41d3aade0ca5f162639d789ba0fa8bd6</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-11-24<br>IPv6: 2023-11-24 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>163.7MiB (171.7MB) – 3,246,230 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 011e707e778473486b297758fb6d306a<br>SHA1: 27c35dd64fca175a0fae30f14bfb45f42bfd6aaa<br>SHA256: 57a3bfd71637e2fa844c6b6db90845c41efe6b9ee5480e283d71ed63ff535b56</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>189.5MiB (198.7MB) – 3,246,230 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: daae38360b8c747666846a9fbc6cfd8a<br>SHA1: 832fde0057fd5c01fb4c9898d5e778bd776658d7<br>SHA256: 49222807bd7beb942327165b28e20b09016b9ebb763cf77e96f47c42f344c4d9</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>167.9MiB (176.0MB) – 3,246,230 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73be4307ffb5827d9d12fef22f1723b1<br>SHA1: efa522f4d1cd7b758930d69e008d8c454803752e<br>SHA256: 5f457f028c42bd58485d28dceeb8c0e917ede7003b15b6a94200cc26bd78d18e</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>174.0MiB (182.5MB) – 3,246,230 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c87f695ab4ee51393f57541b4fe7eca<br>SHA1: 6f1d99a0c11f417b043f7d51b82d4521c80c4bae<br>SHA256: c1d041eff4bb0b9c41354bd33ec445eaeb5dc5f9bf91ca06346a3970021cefe6</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>198.7MiB (208.4MB) – 3,246,230 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afd3355668b9b7d4c5bbc581958ed3a0<br>SHA1: 09037ff48cbe5ee71078d6272581838f25481c6d<br>SHA256: e3091932b155dbab7e19819570c0e907b7943195467206c7de37cc7e90642db9</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>162.9MiB (170.8MB) – 3,246,230 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6004d3cde9dbf1dcd4564da33733ab0<br>SHA1: 24410dfa8a2029c3d7b8bbcd923ffb338634d4ff<br>SHA256: 6bbd41afbf0c006f00040ae0dd9db77dd5d8d56c8c20e6ad3c3114c33d7e6876</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>200.4MiB (210.2MB) – 3,246,230 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8977a22a144c64caee74aefa362d62da<br>SHA1: 3e79c0fb89f77829b0f18814472b662d85597f1a<br>SHA256: 3b5bfb152c5ebc1912e724f81d2e56d175cb06cc14a7793dea8a0046e958b4ca</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>169.8MiB (178.1MB) – 3,246,230 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ac8ad517bb2f8ba4909b55c24054ae5<br>SHA1: 8934ba047e18b4ff86721ffaa35b26d5957a7968<br>SHA256: deba7b60c9f36c4fd984f7f5f744d8f00c96231f9d2a9f207adcd88b4f5b5675</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>124.9MiB (131.0MB) – 1,242,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c47359f696de3bb6a13a2c4ee58c7fa6<br>SHA1: 6e8f868aa8aeb8f395642142214f57d104915c4e<br>SHA256: 536d2310b820cdd4c6858240fb502468778bc2b5ae2e24d153bb2593a88fa711</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.9MiB (139.4MB) – 1,242,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32959f517e793ae97413d2718377396f<br>SHA1: 2ed8ef7d96d36b6c036ce774de4d6c156b64c851<br>SHA256: b6f0bcebfdc4e6582826c06c6959fe2fc0717563726d179d826df4e294fdbb01</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.2MiB (133.4MB) – 1,242,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc5a5e24ebbb91edc28c03229081a8de<br>SHA1: e3073c89fdf6c28885b2f8b2bb7673860386a00e<br>SHA256: ee73934a6cc22943aba84c9d351701a2cc8b2433efdc501d35b68e9091e351ce</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.4MiB (134.6MB) – 1,242,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2bef5e14ac94f6416407f1220714392<br>SHA1: 71640c1b5d049d054873138b1275d741a9703d8e<br>SHA256: 43650ea1b5bd50a9e7492e5d0a2db1634680b5434852572bf909162493292543</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>136.0MiB (142.6MB) – 1,242,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3fdd9ba08cf4bb2c8938fd3be6b44aa<br>SHA1: 38d648b4c2e1a32786c194d1b257d887d3cd97bb<br>SHA256: ba81db4e7b617602d34bc7aec786cde91e4725c9b26b60b5f2b9744947246c88</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>126.1MiB (132.2MB) – 1,242,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03e362e4f992d7077e3d999436da6c44<br>SHA1: 659153e5a2e0201f0b27e4be678d6ded097b4b6a<br>SHA256: 57c4d1bdb308331e8ba3e05432281180aa430fa710715fe08407a307083e4a00</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.7MiB (143.3MB) – 1,242,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a50a0b28d0bb4e2cb55efd134a946c2a<br>SHA1: f3ba132ddd0ea70d0d8b3d0613ca91a04fa04b6c<br>SHA256: 01d3b091b98f38ac593f6ec8956d177693588ba2aac3294208252a247b738e39</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>128.9MiB (135.2MB) – 1,242,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9826e4c8369b246d7c3216315699c2d<br>SHA1: 367c65dfa7b9ea3c65f59c3df0ad6534f803f665<br>SHA256: 6159ea226437cdbfbc2ad5adfbf4fc6e973fd84c026e0fa6514e065f69f40084</pre></details></small> |


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
