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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-03-27<br>IPv6: 2025-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-27<br>IPv6: 2025-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.384MiB (8.791MB) – 419,814 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4e9bcea7e5eb2c6f4ac0564ecf704f7<br>SHA1: 88f12b42be7da721f341fa32407f767c0d499310<br>SHA256: d83a17c413dbc868375968b9ca1fc4c48342a50478e0e7485387e89cc5232a39</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.986MiB (7.325MB) – 106,273 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcb8fb2bbe155c21528d7ce0390c413e<br>SHA1: bd6d9a631142c5c0b39e728b1a81b8e5422d5317<br>SHA256: 956d7d0ffcdf398f02e2d17734edea64b993aa0dffa93eb6e2d00b0d2a4a4f10</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.60MiB (13.21MB) – 630,948 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be0d08dd420a9361bc2d03a1840389cc<br>SHA1: 8f58e13bc74708a4cf4982c5a2f679c4342e1fec<br>SHA256: acc692ab38e697e5cbb5a4b089eb3db7edc20d18a617ac743019242530baaeb8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>71.20MiB (74.65MB) – 1,081,939 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cbc20b68bd3a5f15eef92bd37a51a3<br>SHA1: 17f5a15969919164ed9be511afecc587b871808b<br>SHA256: 920a1bb34e127ff56c3344b31ebc5ab75405dc11a1850792a0ed4c02fa80f786</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.404MiB (7.764MB) – 372,055 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e5911df23fa4121906510a5a567b13<br>SHA1: 9325bb0b20fe7cf38b086bd997249c0ea0460073<br>SHA256: 388e526b141f72da365e6c1487008eaf5440f4e2a173bfada2766c55cb3eb316</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.53MiB (17.34MB) – 251,265 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609d7024eb89dc7bd684d0207b3733b9<br>SHA1: 956350aa870d6a38630af3f3a3b53278471d39bd<br>SHA256: 95146645c0293ed5818f1df79ae51e4c9c07a1f6c91ea0f9331b8da35b754bbe</pre></details></small> |
| | | Full Location | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,335,187 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d87186c64f981273c433100841370<br>SHA1: 62922290000ef7c4549382119783c2045e4d1e6a<br>SHA256: 51718b9bcaef22b3bcf85a754a3a5fdd48d4a0efd9af8a4e3532e918a7368b41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>388.5MiB (407.4MB) – 3,770,967 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a5296fc623ecf8f0caa811c6b1aa61<br>SHA1: a31112844edcf6b611b51dd56508b700f7dfd9d1<br>SHA256: 4018f4afbdecaeedf11e8e21fc7f50e5719bc241f3a50121788f441946a9b58f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-03-27<br>IPv6: 2025-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.118MiB (5.367MB) – 256,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced96baa8d12dd7a7473b62ca04f3ec1<br>SHA1: f15aed8ee671e3e27c23c736e23edc25368ae1b8<br>SHA256: c034868fc655de42297d14220caccea0ab330ee13028773c38db7c6de47b21b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,344 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cef1451430608ae8ad70e0f4963dff<br>SHA1: 43bd5d1e9844ece7eae20604c4d83f7960da31a0<br>SHA256: fed2a958c9ff8365cbd35a38e1b062b5237d9c3576831c5f27705c77a13bbff3</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-03-27<br>IPv6: 2025-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,062,954 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1de2b09cb2477a5e3a644739a02d816<br>SHA1: 2ab572bf0cc2040a312448643055f2f718ca5ac5<br>SHA256: 1d66b45f20fdcc805cf1b87b04dc600ee7e3bcce4b90b5400d770f1ca47a3254</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>233.4MiB (244.7MB) – 2,257,726 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d52faeae6d9b914518dee2695e772b<br>SHA1: ba805ee8a2f7aede9c579332c56ae8ddfc7f7251<br>SHA256: 87cd4c71031299fc55a0c464dac619478c748c283c398787e9e7547a3ae9b9e1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-03-25<br>IPv6: 2025-03-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.39MiB (11.94MB) – 570,137 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54705203b5aa1985348d9d11229c4b4d<br>SHA1: 6ac48f5b4c1c4026e9928d97cc1a54e8f800be73<br>SHA256: e70dd796aee12906da32634e2d5bd72dc1f6a0ab5f83c7258869722824a848c6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>38.54MiB (40.41MB) – 585,706 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45682be13913dd2317dbc777463078ea<br>SHA1: cf6dfa9b8e8bf978607dfbb4f51f215d0651c0bf<br>SHA256: de7fa6149b5778470d2aafc40db1c701fac0ebe254e2536d137f6908f3dda7d3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-03-25<br>IPv6: 2025-03-25 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>168.4MiB (176.5MB) – 3,327,284 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f4c6827fae0a9386e2cacaa3a66687f<br>SHA1: 4ce504ec2595a9825447b8734bac895182ce3db5<br>SHA256: bce9b76eb2f26f95d545cb3b1751c34152c1ee3ab1ed27a6db8a8042533ca230</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>179.2MiB (187.9MB) – 3,327,284 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8cb3d958c45c6eb852db04ef5c18996a<br>SHA1: 00d16f0fcada969339cf7c8c0d02843e4c782bad<br>SHA256: 87fd03288fb74c7726db49786b70b7d58c8bb45c317354e70d9a47c3375373d1</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>167.2MiB (175.4MB) – 3,327,284 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 039a9165f6aab5ac195aa2fb3f8bd220<br>SHA1: cb8ca9c371453d743cc17e27467c1525bf9c53ba<br>SHA256: 5dc70924cc53d643f8600a5dac5ce02837400bfb08d15438e4b84e0f0fa70ab5</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.7MiB (177.9MB) – 3,327,284 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d55f16d59f1119d3be76509921a8f045<br>SHA1: ba48429308ac85228abbd7f7b21908b548cea4f8<br>SHA256: 4ad0b2272ee83d4f860bc381bea5ba9f3280e5a1d5258c9c2d53577710628f67</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>213.4MiB (223.8MB) – 3,327,284 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c268eb9a0bd8a23a8895b0fb13ef1a5c<br>SHA1: 8d6f065b3dc160ef43332382666dc4047a5566fc<br>SHA256: 0e54d5ecfda29df9cd4a6798b59616e95f30429dfd5d7d3158afba6c56e4a34a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>167.2MiB (175.4MB) – 3,327,284 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b72651233efefbffb2440224b5f6df1<br>SHA1: 6a5f91bc04a4fcbe4615d5f98183f82716aa1e77<br>SHA256: ce7154fdf43c7681b721c94ebdbe504fa36fb0710ffff188977e0d892d08e4f4</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>207.3MiB (217.4MB) – 3,327,284 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1fe2b60d99a1129aafd5ac3b45210059<br>SHA1: d2f7854347745b3915c9a3127fd80ec6144b91cb<br>SHA256: e388068e9076d7600e5c191c019de5d53ad24e2765814bed6ae6807a568bc417</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>174.5MiB (183.0MB) – 3,327,284 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa827801c564d2ebc58e172acc2e219e<br>SHA1: f1aa264ef7459c277e5e8c7b06abe3d33983d3db<br>SHA256: 20d2ef8c21834f34acc7e86ab217c97fbdb085e1295b5d637c35328ad4472b80</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>173.2MiB (181.6MB) – 1,841,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1783196909242581e7fd3d374466732<br>SHA1: cfad1099c2c942a2e9027e0d44f248bd94951195<br>SHA256: 5594427b2807e8471d56fa9ef8b5b31669b9c9311c6be671b48e6795dddc0d20</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>177.1MiB (185.7MB) – 1,841,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9937f3f464bfe607ef7e716c5eec2b94<br>SHA1: 77a85ad3c90b2d66af91e847099c28ed5b7016f4<br>SHA256: 79a97f8deef6ef29f32bb9cb6e8f700868a33273f0fcdfec59833b034d23ec7f</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>171.3MiB (179.6MB) – 1,841,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5cb2aa14f11eade10b8d0caf346c1ca3<br>SHA1: 02a135afa6576c39f725173951d12617e527f5a2<br>SHA256: 8c1a5783de6a7b92309e8af71d7e9c27988eed43efdd3e351357aad91a5eb74c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>171.7MiB (180.0MB) – 1,841,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 186665bcd060e9e10ab59538590d3861<br>SHA1: be8e560e0c0d8c7a11d1c25169a61258bfb73356<br>SHA256: 9c9df09bc359ca8f948d6707df00922d5160bdbd3bced6c61dcbe4d74dbb1646</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>189.6MiB (198.8MB) – 1,841,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dcc19dd4d536ebafeeb32df43126e150<br>SHA1: 9ab128466a53054f7edb3814b08aa64d4b2b3b70<br>SHA256: 7ed97cd032af002e582dc63436fe10490cd9dcf96f3a4882ba446d8a2b4d6ca6</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>171.2MiB (179.5MB) – 1,841,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e7afe187df435bbc846d52a77bf711f<br>SHA1: 983e1b62f26859edec7377c3c3f2187f97effd69<br>SHA256: cbe597fa8b7a323d22fc4affdd8c23f9aeef16c48dd0943abbde40f703fa2d0f</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>190.5MiB (199.8MB) – 1,841,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5c4ac05c51bcdf9903f2e26dcf01142<br>SHA1: 21a430de40bb6dc6d5d33fbcf33de685139aeb09<br>SHA256: d19e4dc6512fa28dfddab4340ca0a710b14bc9003b12ff977a5d26e2829a4bd1</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>175.1MiB (183.6MB) – 1,841,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18526908efd07cf67e5f5ebf10c300e4<br>SHA1: 8f146dd51c6674754422d6719a3e79869be87408<br>SHA256: 9333ec8662819dc6e0f63c64d9ee9157cdec00607efd51ee0bcfed12db3291a1</pre></details></small> |


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
