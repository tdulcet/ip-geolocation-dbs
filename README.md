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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-03-10<br>IPv6: 2025-03-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-10<br>IPv6: 2025-03-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.360MiB (8.766MB) – 418,639 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fdf9ed910b6299139afd68366ddf613b<br>SHA1: cc9f3df83805a5f3e7851ce938b9b373de0c3028<br>SHA256: 3da05ad450d66239b65f251f041277d80f577c957cdf32ae6d3c4c2492040785</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.976MiB (7.315MB) – 106,125 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc7317efe01ca3fc585959e18c372938<br>SHA1: 2ca7ed17a4e9ac3ae92a715b793c2c7bca360c44<br>SHA256: 22525528f3c2051dc4d69bd91b1a798999f6f3647b7e2f118319d48c7517e368</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-03-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.74MiB (13.36MB) – 637,912 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f346e945272d4e0ea4bd010762d94676<br>SHA1: 81811e3fe43fcc7f8b94c67b775efc2214182d6f<br>SHA256: d6730b11ec732b438f8e6d40c98a64cf07a4056d3bcb22ef1fb3ba739d7085cc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>72.31MiB (75.82MB) – 1,098,869 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bfe42cfb01686285428943949a387d4<br>SHA1: ece428f127fcb79b85f028899dcbabdae7dee8e4<br>SHA256: 51eb2604c6bdcbb2e4a5a0a73083a1c53299ad427e4da6ab7118c091e7ded1a7</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.404MiB (7.764MB) – 372,055 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e5911df23fa4121906510a5a567b13<br>SHA1: 9325bb0b20fe7cf38b086bd997249c0ea0460073<br>SHA256: 388e526b141f72da365e6c1487008eaf5440f4e2a173bfada2766c55cb3eb316</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.53MiB (17.34MB) – 251,265 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609d7024eb89dc7bd684d0207b3733b9<br>SHA1: 956350aa870d6a38630af3f3a3b53278471d39bd<br>SHA256: 95146645c0293ed5818f1df79ae51e4c9c07a1f6c91ea0f9331b8da35b754bbe</pre></details></small> |
| | | Full Location | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,335,187 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d87186c64f981273c433100841370<br>SHA1: 62922290000ef7c4549382119783c2045e4d1e6a<br>SHA256: 51718b9bcaef22b3bcf85a754a3a5fdd48d4a0efd9af8a4e3532e918a7368b41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>388.5MiB (407.4MB) – 3,770,967 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a5296fc623ecf8f0caa811c6b1aa61<br>SHA1: a31112844edcf6b611b51dd56508b700f7dfd9d1<br>SHA256: 4018f4afbdecaeedf11e8e21fc7f50e5719bc241f3a50121788f441946a9b58f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-03-10<br>IPv6: 2025-03-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.118MiB (5.367MB) – 256,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced96baa8d12dd7a7473b62ca04f3ec1<br>SHA1: f15aed8ee671e3e27c23c736e23edc25368ae1b8<br>SHA256: c034868fc655de42297d14220caccea0ab330ee13028773c38db7c6de47b21b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,344 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cef1451430608ae8ad70e0f4963dff<br>SHA1: 43bd5d1e9844ece7eae20604c4d83f7960da31a0<br>SHA256: fed2a958c9ff8365cbd35a38e1b062b5237d9c3576831c5f27705c77a13bbff3</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-03-10<br>IPv6: 2025-03-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,062,954 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1de2b09cb2477a5e3a644739a02d816<br>SHA1: 2ab572bf0cc2040a312448643055f2f718ca5ac5<br>SHA256: 1d66b45f20fdcc805cf1b87b04dc600ee7e3bcce4b90b5400d770f1ca47a3254</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>233.4MiB (244.7MB) – 2,257,726 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d52faeae6d9b914518dee2695e772b<br>SHA1: ba805ee8a2f7aede9c579332c56ae8ddfc7f7251<br>SHA256: 87cd4c71031299fc55a0c464dac619478c748c283c398787e9e7547a3ae9b9e1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-03-07<br>IPv6: 2025-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.23MiB (11.78MB) – 562,318 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7694f2ae9a237482d798328b08ddb03<br>SHA1: 73ab46760b9ee626b88aad60fc3ce12004689aa1<br>SHA256: 5f1684bc428321a6f46f741c88b820c50f9e5e96c771abe0e5af9f60bfef8ceb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>38.48MiB (40.35MB) – 584,739 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dad81d490ecae7c3664fb0ccf153c9a3<br>SHA1: b1dbfad6d709d5ae632011b49bf41b214e68393e<br>SHA256: e666ffc62c18332657bc260ac032885c3c61d2876d646c3af30c9a41c9bb7a61</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-03-07<br>IPv6: 2025-03-07 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>166.6MiB (174.7MB) – 3,296,677 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fe01fd69dc3db718e35759105a2e379<br>SHA1: d76e35fd175cd115c5bb8d9afde793e99ff9c8cc<br>SHA256: 426199151bbabaaa9514ef69e39774badad08a7b243dab5d0b3a24abf0b0a5a4</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>177.4MiB (186.1MB) – 3,296,677 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 073ae5d41fb277a3a337f3284146ece0<br>SHA1: bfc85e657c8083ca5310fe96bfd29b3417751c94<br>SHA256: aff79e71d59f13eae8d583d81989bd820c6624780d66a8b14d93f650f4738fc3</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>165.6MiB (173.7MB) – 3,296,677 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 618118b485151b1dff4dcbcc0451a9a1<br>SHA1: 59db5dbf146210ee876adbf48f8ba8600f8ee0ab<br>SHA256: cda2291241edc64c6160d1dbcda449d598170e83843112b76ecc0dedadf6e30a</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>168.0MiB (176.1MB) – 3,296,677 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f553fa0ccd83a5e2fa665da87d06353<br>SHA1: 88a8182402de356671acc0f8f5a7d9a699cf88ff<br>SHA256: 98316e22e801bc248ec2566cfde25844b5aa5dfaf6cd189a73f834cffb0626de</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>211.4MiB (221.7MB) – 3,296,677 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1723a4c42b26140fcd82c0becc1c7e3b<br>SHA1: d86aa40922ac13e9172bb47540d05b26cf10e3b9<br>SHA256: 67cda3819b722d904a516d8b8087d73343cc40316d0f0c27c42526a25ad602b1</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>165.7MiB (173.7MB) – 3,296,677 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17c0e37d185dc1f83bd0e2b162ec5e91<br>SHA1: 0bc242bad81de117e4ce87023fdd21c646e453c1<br>SHA256: 9c10724114c4fcde0cbc3dd84aa4cb8387e8be2b1f90688075474aebf90eb474</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>205.2MiB (215.2MB) – 3,296,677 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe9191ca1eb3349caba037d01f724631<br>SHA1: 676578a68086e865015fa4b58cbf3c96aba8d9de<br>SHA256: 62a8375e077d70af6c602a6b72fc560d406502784f9b742930f4aeb80cee67ac</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>172.8MiB (181.2MB) – 3,296,677 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6919048219c3e6e095e48e9d9e48fd1<br>SHA1: ecf2cdfdd3ba867e885c6fbf776fcc8567c9a8aa<br>SHA256: ba0b643660452d1942ed1474346bb204ceeeea9dc8e765968fc56a3a6c577df5</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>164.4MiB (172.4MB) – 1,753,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15987dd720fe7f28f3e410a8431561f4<br>SHA1: 162c4bd590e4e6ab730f9dc2b39fa99b46002b8b<br>SHA256: f21552253c21194d8a3b5742763ade78ed9b33e8d4278ad85acc6c9d0dcbc829</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>168.1MiB (176.3MB) – 1,753,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bca8bdc4c704b595895e3370e0add05a<br>SHA1: 9fe43c5ae803e6a6cde00740c142e332da582a74<br>SHA256: 705edc0d107c73b800d8a516c4cffab2100be8dfad2df62923f36375f9d8e721</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>162.5MiB (170.4MB) – 1,753,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6656893abc518115a45ff732e28e2224<br>SHA1: 6b14cf24ea3fd7f6f226806aa42fceb52fb41ccc<br>SHA256: 2c238664be7161b1fa2c167d3760d3308b500a2ec2c0e9062ab223c9409dd3c5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>162.8MiB (170.7MB) – 1,753,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9f4e65c5ffb2d8ceb672a9cf7639ae4<br>SHA1: 8b76d1c990a1fcea0a6b9779d65be40eea873fe7<br>SHA256: da23a91f90b0a256553c5e36ce643ebcb8ca110ea6b8d33cd44a840d8bb7e6d0</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>179.5MiB (188.2MB) – 1,753,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50f93ccb8cafebc61c82354580a0f5dc<br>SHA1: acb7e3763b5f62529cce20902cd9ba5984c1e447<br>SHA256: 7fee9a1db1950fed5f79b7ef76cb7d9cfa6f0251c43148802029ae66b702c3eb</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>162.5MiB (170.3MB) – 1,753,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 439ff322cea8e05b2947b9d9a3c61774<br>SHA1: c628b5458ae63abf434e5f064483b42797c112df<br>SHA256: 7be110837309b991694e2b763373f1497ff0d8528cdaebd2d27b3c777da7ce5c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>180.6MiB (189.4MB) – 1,753,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4514afafd2b0efae6622ac0c8b516bc4<br>SHA1: c89745a4d34d994443428b5de814d128ebf65b4b<br>SHA256: 78e1bd2ad4ad61ed40a9d32c8c44932f03c5b53f31b72cd7ddfc6525f02d0e6b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>166.2MiB (174.3MB) – 1,753,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03d6f2b1e86bf67911329c38fbcb91a0<br>SHA1: bf8814c3305317e15750b86c8d9e6c472e517df2<br>SHA256: c1efd4192f42ad189fc1f6f1103727de36d677afac32afffa963eede85d1bbd8</pre></details></small> |


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
