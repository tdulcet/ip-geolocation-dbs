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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-03-17<br>IPv6: 2025-03-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-17<br>IPv6: 2025-03-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.365MiB (8.772MB) – 418,884 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ad64d451a41202941b6632a6040a15f<br>SHA1: 354a2e08a77b76c3eb03e88de79e5f4239ba744b<br>SHA256: 9ef61e20928d6d3028e1cf7832a471030c440e917e63756ad7fd2f4998226012</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.996MiB (7.336MB) – 106,437 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9db6d989c891103d9bdccce068c8c85<br>SHA1: f2680f9e74bd40403876025e16b1ae86dbb383c3<br>SHA256: 14d7d1b6cfd82d3c8c1de717a271914c02455576e26a555a1b11672d1ac2a0fa</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-03-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.66MiB (13.28MB) – 633,933 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232d6ee3fa90df3f7471444ebc0f1f51<br>SHA1: 105e50973118804daeba6a4bc74f5f84be36f155<br>SHA256: a9dc939f665a0c190bc5748cf2353ebe2e7c5ca8285fb1bb3275aa76453a6197</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>69.91MiB (73.30MB) – 1,062,376 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bed49f71cb2b872a1661d4a2d803d223<br>SHA1: c7c0e47e1b58a6b5b1841c6efe66c6a18ec96b18<br>SHA256: 73475a379904f42db6ada93adea17983f00148e72dd980e103902377126b8c05</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.404MiB (7.764MB) – 372,055 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e5911df23fa4121906510a5a567b13<br>SHA1: 9325bb0b20fe7cf38b086bd997249c0ea0460073<br>SHA256: 388e526b141f72da365e6c1487008eaf5440f4e2a173bfada2766c55cb3eb316</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.53MiB (17.34MB) – 251,265 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609d7024eb89dc7bd684d0207b3733b9<br>SHA1: 956350aa870d6a38630af3f3a3b53278471d39bd<br>SHA256: 95146645c0293ed5818f1df79ae51e4c9c07a1f6c91ea0f9331b8da35b754bbe</pre></details></small> |
| | | Full Location | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,335,187 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d87186c64f981273c433100841370<br>SHA1: 62922290000ef7c4549382119783c2045e4d1e6a<br>SHA256: 51718b9bcaef22b3bcf85a754a3a5fdd48d4a0efd9af8a4e3532e918a7368b41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>388.5MiB (407.4MB) – 3,770,967 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a5296fc623ecf8f0caa811c6b1aa61<br>SHA1: a31112844edcf6b611b51dd56508b700f7dfd9d1<br>SHA256: 4018f4afbdecaeedf11e8e21fc7f50e5719bc241f3a50121788f441946a9b58f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-03-17<br>IPv6: 2025-03-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.118MiB (5.367MB) – 256,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced96baa8d12dd7a7473b62ca04f3ec1<br>SHA1: f15aed8ee671e3e27c23c736e23edc25368ae1b8<br>SHA256: c034868fc655de42297d14220caccea0ab330ee13028773c38db7c6de47b21b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,344 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cef1451430608ae8ad70e0f4963dff<br>SHA1: 43bd5d1e9844ece7eae20604c4d83f7960da31a0<br>SHA256: fed2a958c9ff8365cbd35a38e1b062b5237d9c3576831c5f27705c77a13bbff3</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-03-17<br>IPv6: 2025-03-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,062,954 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1de2b09cb2477a5e3a644739a02d816<br>SHA1: 2ab572bf0cc2040a312448643055f2f718ca5ac5<br>SHA256: 1d66b45f20fdcc805cf1b87b04dc600ee7e3bcce4b90b5400d770f1ca47a3254</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>233.4MiB (244.7MB) – 2,257,726 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d52faeae6d9b914518dee2695e772b<br>SHA1: ba805ee8a2f7aede9c579332c56ae8ddfc7f7251<br>SHA256: 87cd4c71031299fc55a0c464dac619478c748c283c398787e9e7547a3ae9b9e1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-03-14<br>IPv6: 2025-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.29MiB (11.84MB) – 565,244 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a75b72ae87ec05283170676ed2c5415<br>SHA1: 13321bdfa43f13f6e7341c69ca4066a2fb532cae<br>SHA256: 1ce8ee46506fa58a7d7d2f581f3a484a73d73db0cd21562ec4c3f3d9a5646bec</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>38.27MiB (40.13MB) – 581,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a31c00846449499d6e074ce41fc91b0<br>SHA1: 82b36fa0aca813cf7c50c566aa1ee453665563bf<br>SHA256: d4eeb56a201c2be4612290e3d28cb71efa163a460aadb4716081164d7dcef122</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-03-14<br>IPv6: 2025-03-14 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>167.8MiB (175.9MB) – 3,316,612 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a22200be3e29dc3ad3852c1d181a26c7<br>SHA1: 46ad7962d93b4fae174bbb04669ac4f28f3f7986<br>SHA256: 8fcaabe1e8b5c80daa88522e4e3d89357fde4a410b5069d8513fb350984a27a1</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>178.6MiB (187.3MB) – 3,316,612 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 238c54b01d4845b577b5d1f5b7c4346e<br>SHA1: 0921e677d96d9fe294df54cf23508b127be032f1<br>SHA256: 924edc845c6fe364bb479838d932a773b6865232af6acd1f139676d7c6cea4ed</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>166.7MiB (174.8MB) – 3,316,612 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ffd1232f03259033cc81267c0428744<br>SHA1: c1a12aa547caacc2ffaf9e39147ea50a8969edd0<br>SHA256: 34d9201ed9c0e3e1aeca90b575e5c07400169964104b61713d9c1c346890f221</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.1MiB (177.3MB) – 3,316,612 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 781a35494cd9c356875847ce3325fcd2<br>SHA1: ed99114cde27036cad2deebfef0b9225c2713af0<br>SHA256: 381f30288f6ed1fc6df6514c2d78c5524bfe53c9050e296c62791b7cf10e2f21</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>212.8MiB (223.2MB) – 3,316,612 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5189c42a07ba8dab4f92eaa2933ea5b<br>SHA1: 0c1daaa145e30417dc3d9ab3a6674e0431eee563<br>SHA256: 3ccf396cbf5691b3dd77bd1c0330792bef933d560b67ef476218c817b590263b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>166.7MiB (174.8MB) – 3,316,612 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: abbd1a6ebf4d7a00e53b7d92b97da5eb<br>SHA1: a315b287407f193b06832f1022b7f14c0e5b8492<br>SHA256: 957cef548f78717b7c7865eb83443a6216aa583f75686f8b7bb954b1a61ca936</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>206.7MiB (216.7MB) – 3,316,612 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47eba8fcc8a0505e97099ff022fa877b<br>SHA1: af0ed863c940dcbdad7c387d510ae5d7f427202b<br>SHA256: 09eeab3fbd39f9b36d678da3b72f74713ffbf262f6512c14f42bbc8a934a0c63</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>174.0MiB (182.5MB) – 3,316,612 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27cdf562789d60f7b42e0108d2c976e4<br>SHA1: 23e36a76be70c0c05f5ac06b71357234d2c6f955<br>SHA256: 6e8f8bef612d534968ca507123262b78ce4ee67e5a5a3aa37318b3e58a75f0bf</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>172.2MiB (180.5MB) – 1,830,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ecac9d2b60b62a5581dc01ff10fc85f<br>SHA1: 7d953e60c9204186524411c5fef54ca1e1bc01c0<br>SHA256: 216e6736197e107691945019dad71ac36127e5781a84b390510cc1a07c194ad4</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>176.0MiB (184.6MB) – 1,830,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62692ac4b7f466beb6ba52125b8ed7fe<br>SHA1: 1f970d5bd0036a0acb6f5b4b7d660992339a8c49<br>SHA256: dd659b819693595f1b971adc70d45cb56b4e05e8f30c180bc0ec7e1b22511cb2</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>170.3MiB (178.5MB) – 1,830,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35d129cb5b0b2959bb6eb0af48096f3e<br>SHA1: ab98656388795c11ad1813b4a381bf74332c59db<br>SHA256: 5d4b01f54b1c53ed914f7f31bd3cc0bce969fd0de8e6f73e1563db23b65eea54</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>170.7MiB (179.0MB) – 1,830,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 101de642a3c1e1dc2949b47787aef582<br>SHA1: a6ce4536f5c356891f1070a89cbe7463cdd7cbce<br>SHA256: cb2e4a02c1eade3da7eaba7111c25bba581300724f8bfbd8adaf9c2e378e20c0</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>188.6MiB (197.7MB) – 1,830,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3afb998464b41be5dc867c19b9568ba2<br>SHA1: 029e38aa46c88a7a8ffdb05336d25affec8c410b<br>SHA256: 4fb05cc16d82fbc183e704114969765ce90eeb3323e843eb080a36ee03fc3298</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>170.1MiB (178.4MB) – 1,830,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8580df17696b9a1dc9ac2436e1ce6fef<br>SHA1: c5a59dbbd7c00a60083a32690c3f8bf71a599460<br>SHA256: 84024239035e51ebb69366bae7795d3ce886fe3f2553899aacadf4d843bd5fa3</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>189.5MiB (198.7MB) – 1,830,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84a9d595d9450641ed53bec9930850fc<br>SHA1: 22be58a46e4e44bc21840cdaa164e818feeeaf8b<br>SHA256: c999282c114f4441a091e82e96cd9398eacdeda187f84b2b85faad4dd252589e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>174.1MiB (182.5MB) – 1,830,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acc109558a0c3050a5b555c1ba9e91b4<br>SHA1: 49d157e558e6a3759e380a2b010b0b8af5728856<br>SHA256: 7cf14755b1ef8f13631ffc5944b9ec3e4b894e8860585bb0bb21c95d4f94ad7e</pre></details></small> |


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
