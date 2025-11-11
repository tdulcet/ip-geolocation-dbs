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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-11-11<br>IPv6: 2025-11-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.318MiB (5.576MB) – 266,389 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb869070df27fa8adca7274755855e7d<br>SHA1: 8dfadc692bf150be6a105d97748a8360334ab9ae<br>SHA256: 115e54ae28bcb159a15650d899e526950c11ddd4aaa30e8c5003bf7f8ed071b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.840MiB (7.173MB) – 103,953 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d8b296cf7de6679a1e1044ab025688b<br>SHA1: 75e3b54553984d9ecc88440f45e8887de2f4731f<br>SHA256: 2e9f277771b2e6bf886b3416884b1c413ddac1afcc7fdf9b59e33d53ba0b3c5e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-11-11<br>IPv6: 2025-11-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.707MiB (9.130MB) – 436,002 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cac3e97982153772d4961860f9b149<br>SHA1: 208c6fec2e8745aa95ab563fd1933b1a6036ab07<br>SHA256: a6a335fa53568ba7c1c19d69887632ef74713a450b937bb074ecbd09b834cbcb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.481MiB (7.844MB) – 113,797 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b64a789239c9e86abe463be9a2f655b<br>SHA1: 770e9844d301e7bec9084d5d6f7588edc03c26be<br>SHA256: d76720ec84a3abab892ef9d25e2bcb3cfaff41d9f58d1b0fcbd7b1722ca1c94e</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-11-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.36MiB (12.96MB) – 618,857 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb1e35664541d627715d72ba353d0294<br>SHA1: 1cbe9f6cbfed9d9ad40d36f739a64d11fe25ee5b<br>SHA256: ad918397a58a35d78354c46a3903dcdda81972190861ffff42259d173b3dda0a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>65.92MiB (69.12MB) – 1,001,700 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14ac7a1f3a3064a26384d8695052608c<br>SHA1: 2638a41ed142f4d6c4303582a4fb133e16556423<br>SHA256: 30c9f0b55f0bb679618536b23772244d9421a40fa9e7a6a1c9bd62bececdac27</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.010MiB (7.351MB) – 351,015 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b145553d436fa9927d6cee221444f00<br>SHA1: 843b7bc7470f77f7a70889bca7f0073e810cf0c3<br>SHA256: a8d289151b074c668255eb1d321a0c2c24a2aeb5d42f6061a293505dba1162ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.94MB) – 245,486 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e455a11648304abcd99f5c6bb19d7c56<br>SHA1: c3ea6f03fa4fee059c88a1910284305da803f248<br>SHA256: 8f4586e376e7d38e45f03f638da9bba2d90a84820ec5114e2ce10da9e7b87624</pre></details></small> |
| | | Full Location | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,722,991 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8adb14693f593577d9641386622862f<br>SHA1: 4789a341532d78da8e6b9fd9df61010466508387<br>SHA256: 18d6fa0beb7252dcb6684069fa602d39f95517dc0b4ee10bc0092ef22f72d867</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.7MiB (473.7MB) – 4,393,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fe48bb05d21d396bfad13d9ca53f98<br>SHA1: e1c547a5ade8b7c473d8429a89dbbb42b7a679a1<br>SHA256: 0b7ad446a98640e9d471aa376d976a1b332132350201538914192826c2ba532d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.163MiB (5.414MB) – 258,420 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71af8f36a1397b54f07095e46ae8647f<br>SHA1: 4e7eea5925834f1ff4f956802d8305814f9d5f71<br>SHA256: d19b4141eb99c7f37b587dd2ce5a4dc9b0a4369860115050ed1938a6d4e42eae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.52MiB (23.61MB) – 342,190 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2d25b5f83304f5ab3963662d1d82459<br>SHA1: bb6059c49131cbfda3baf36ae84efd715bf63f7e<br>SHA256: d8aa367d610898959d5d76a083e838cdbb5319f8a54b6a6b269f0bc3dd7d4e3e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.6MiB (181.0MB) – 2,992,474 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8caf582afb85da7035ab080370960f1d<br>SHA1: da00b833f91f14149ca4e947ed9c030f7c66ece6<br>SHA256: a7b0f18c2da024f4ae25e028eb1834d611e0f6a4c58fc63ec6db40af5830bdb9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>292.6MiB (306.8MB) – 2,836,100 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc6b2a9b8fe3ed4d35e4b406d54dc4ed<br>SHA1: 40a84eef0f2ea3d6ea0fbc3a2c011d0993367c32<br>SHA256: 5b38c04d1cbde28d1234ab83322bf6d65bf2c6fd480c757260db36e3be83f37f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-11-07<br>IPv6: 2025-11-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.54MiB (13.15MB) – 627,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 745d1c80b48d4b3eeaba5db46cbea2dc<br>SHA1: 8304351ff78171b58721b29aed6f70cd4d8a32a7<br>SHA256: 318962cf72708ccf487a36f5e9f0fcbe7ceccf0c91fb1454dd25a3f338f39c85</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.25MiB (45.35MB) – 657,268 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38567c4c450e3f009e86cf962a38b2c1<br>SHA1: 75f084157dc6f0c8e756f9dc7a216554271038aa<br>SHA256: d4a2fc2972685361a498c8cbc3d6ee712ad0122c09657609c2cc298f86c5e2dc</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-11-07<br>IPv6: 2025-11-07 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.4MiB (188.1MB) – 3,539,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6ff89161f897125d78ebed3972b8949<br>SHA1: df23b70c5051c735bd02d139b23be37936bd5ee0<br>SHA256: 529f8b4a04db4cec54b590e30e5f87fa0635b7fd0ac2960b17c0f6ed4ea4f421</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.7MiB (200.0MB) – 3,539,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad5f739a03603db3e0df40f4f1531fef<br>SHA1: e13acc3c83446fbcb12f8471bff9895a905e0e9a<br>SHA256: 744240f3b5b65486e95f49eb3e4aa5b8da9d7eeb2dc980f1a1087a49df17b6d2</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.5MiB (187.1MB) – 3,539,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e569bbbfc67e37579b8f5ac58f6436da<br>SHA1: a40ad31f85139b3cbb93bcd8a60967a2977688cf<br>SHA256: be3b459ce44258a6d4c4de7594460f3f6c7fab2b4826f803d3160ad6bd869372</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.3MiB (190.1MB) – 3,539,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b83998008fdce7cf7bee76923ae471cc<br>SHA1: 61e4cb49e9ed31a9e884d2186b462335d836f3e4<br>SHA256: 212f784044256dfba26f9c97277ffb53330a7f0396264dd55d7042d87fd3efa4</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.0MiB (238.0MB) – 3,539,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffd7ff4c5d1d354cdfdaafd058f9a895<br>SHA1: 26c9e03d9839fa0177f72e4505533ec125cb3a7c<br>SHA256: 340acf8229cc6fa68fc0e28ddd7f8ee3d778cdc70c59b2453d54600e33579db9</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.1MiB (186.7MB) – 3,539,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96db443ebecbcb884ab817247873c6c4<br>SHA1: 676b7df9e402bbd1ef33ebb252a4929758d435e0<br>SHA256: 911464f573a3f8d94fae5e052dcf9275b2792fadc82eaff3dd5ac8a5d51a10e7</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.7MiB (231.4MB) – 3,539,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36bea7ac77e93c737f9af1539b46c137<br>SHA1: 80459a78144d0dd071a511eae4d1643021a4652c<br>SHA256: 8d19aa62381392b696748a742096a5ddc7c0369f7f0bf8fabcf3969d7daf6255</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.4MiB (194.4MB) – 3,539,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c15046ea7108598e520656a11c6c784<br>SHA1: 1185c50a5d01247c09bd75e929762dfddbe97027<br>SHA256: eae5821c919a199e53036c42aa679c6bcec77a6264b56d6dac365791a41ba5a8</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>183.3MiB (192.3MB) – 1,934,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff029e41f7283465f5356b2faa6dc075<br>SHA1: 586882f1ca3ebe266010179a6ae742c66841be77<br>SHA256: f78e57900752418934259219b6062faa4d0d94825abfbca9bfbed8dbe81ae059</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>187.5MiB (196.6MB) – 1,934,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e2877d9940e2ee6a1f52484e6bd05f9<br>SHA1: f3491c97fc5e07530d966868392d413a7378439e<br>SHA256: fe7a6d0a1b81ac66e351858d60776ba5293d57e8fd02d7c5fc30cb6f6e05a5e4</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>181.1MiB (189.9MB) – 1,934,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a4f21a714f4b5394be6f3e23581f947<br>SHA1: 2c126b5552f32822bd56d5e5219385c99b796b55<br>SHA256: ab5053b2aff8bb7d73f96c984cf28a07973bbd3945c03b7229bd3424316f905f</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>181.8MiB (190.7MB) – 1,934,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48b16014f9f0d5136d97c30abbadd1f8<br>SHA1: cd68c563ea910aef095d918406025d009cbfd535<br>SHA256: 30aa83660ecf94c957bd31055b03b650a6b18f12c5a5f5029751eb214defbbe8</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>201.2MiB (211.0MB) – 1,934,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 989b1f866b94d293fe6e998de275c28b<br>SHA1: b6093bbc0710d1c156e9ac25a660a06ad9884627<br>SHA256: 5f19045bb478dfdeca669ce233ddc461756efb4ebfb964eed0d71821ee292702</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>180.8MiB (189.6MB) – 1,934,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c23ad56743e925bb95bec28eb551762<br>SHA1: b2490a1cfe5ec515106b2874c7b5ad5eba026ae1<br>SHA256: 2abe6b064aac9f5bde45340b04b5567d55f118e39fb1470f12eec6a34c53c17e</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>201.3MiB (211.0MB) – 1,934,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c165e615bbfcfeb639846742c957913<br>SHA1: bca252e07aab97f8815b1b1d33bae745165cbe33<br>SHA256: e9da7330b32e6bd495b65a2feb35c1d4be616f96fb5793650efb1e5c444506e3</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>184.2MiB (193.1MB) – 1,934,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 222e500f20cbe8c96ad869cacbf8d862<br>SHA1: f0b459af0f8f2f00bfbbc622d5f7420bb5d4b42e<br>SHA256: 41b6d1ebfe7a0ad4c5c93e8f21f37dc4ce9d9453e63c4881d2bfff475e85bce6</pre></details></small> |


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
