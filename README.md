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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-10-18<br>IPv6: 2024-10-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.854MiB (6.139MB) – 293,131 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 691acc5c64b05302977b6ec1f2d73c94<br>SHA1: e1e0e2e2d33b66b5c98a46755c69cae77f7016ed<br>SHA256: 2ae2c0991073cf4dc76b4cf58182d3a6bc874ef1673c08dc6ed5253ae04b1746</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.51MiB (12.07MB) – 174,960 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d93781a3764cc80c50f73db9c783d8a5<br>SHA1: b772db06b079c034d87aacc8ecf204c5413cb2d2<br>SHA256: 344943da42704ab3473d41d90da764e82f1c74635ceb7783efaa2133543b618a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-10-18<br>IPv6: 2024-10-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.221MiB (8.620MB) – 411,668 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fb89405d249262a07563e4cd5369c97<br>SHA1: dc91ae4e6ce2eca17d2380af2b456b088467910a<br>SHA256: fdfce025edc2468c3c2e5582f65082ab847fce8e5eb2947237f4fbe4eeff7bdb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.767MiB (7.095MB) – 102,946 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c51a2d4021cf8b9eb891f3ab912309b<br>SHA1: acfbced966477deb802a0ff550a9afaa71201cfa<br>SHA256: e85200dd60068b6901f79934f393319cf6498b61f78d5d8433a0119c3160ea46</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-10-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.85MiB (17.67MB) – 843,130 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cac7f525de169eeb91880f3983e1af6<br>SHA1: 47a6827e28bc5f083e919510b1581650e2f401a7<br>SHA256: 6f8b3804bdb39ac98c90479a1274a69210a5272370cf9bed326f655ed69d2bcc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>61.99MiB (65.00MB) – 941,978 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9197741347f368e0c34fac07fa6db7cc<br>SHA1: c606d934b80d7fee0a682fe92e531d95b5b97b6f<br>SHA256: f23a0bc7bf4db43df68f4d9eff4e7a859bbd5c8e445cbabf66c8c290b8edb30a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.939MiB (7.276MB) – 348,549 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1934c9e84da4a70171fa8a58df792d1<br>SHA1: a9efc628d84ddb0c5ec270a44c413d6e2e413eac<br>SHA256: 8974ef5ef8832adde54bf8eff5b734fbc419e040b6a1ba06eee6302c327937de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.54MiB (17.35MB) – 251,406 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccee8212e47dad6f6d37a7875599a267<br>SHA1: f12a6f633e3f93b21d90f94868a5dce0099a8f68<br>SHA256: fe5508fad3836313166aa43d498d12d6277cae16fef7835d5e92fdcd53bb2de4</pre></details></small> |
| | | Full Location | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.4MiB (197.5MB) – 3,289,697 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a0426270d27872fad498a291900b10d<br>SHA1: 4f4a7ccb4910df8d359d2ad76a1bd80c4be37d61<br>SHA256: 6869bc8bd2854724fd6be12e1a0efa4bf028d598fe1d116783216884c78d9f3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>362.7MiB (380.3MB) – 3,515,904 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b742d904c555f3e530341708e40522<br>SHA1: e367baa432e03a59b81c286e5f9bfaeeb0617eec<br>SHA256: f946dbe0156a23fd65f4c67f8c95dfc19e8984bc7f84d8323fc5c478da017055</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-10-18<br>IPv6: 2024-10-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-10-18<br>IPv6: 2024-10-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-10-15<br>IPv6: 2024-10-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.851MiB (10.33MB) – 493,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60e435305d740585c36a6a9c5d6c8bcb<br>SHA1: 71538a35a8c512cff223092ca1840bebc34755b5<br>SHA256: 2ea8edf689d52c6756774e073c0c7f124fddf1c8e73d34d5702d74a29e03142e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.30MiB (32.83MB) – 475,734 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14bb5e8e032c685f6b0304cd9e50059c<br>SHA1: ceda819357fe81c18f7512c8a4103c0a113eae69<br>SHA256: d0324ce07b7cddba7818fea9546a91592b44567ec6a62c5b15f94c7b6f485a4b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-10-15<br>IPv6: 2024-10-15 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.8MiB (180.2MB) – 3,390,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d85913257134c208b77b006763db53e6<br>SHA1: 94a2a9ac0c923bec80a4886832e9b36b8bb276df<br>SHA256: 43105660e2d03784afed7a1859130df26c5b032fcdc42fcb16f99c5f0f02fd68</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.6MiB (192.6MB) – 3,390,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df5b2586d313be91b5a5afbd8ae98a8b<br>SHA1: bc3af22ca06ddac66bbe13b2986de7d180cbdb44<br>SHA256: 0ec2f94401d1481958c1e8605c23074092bf17bf093d3ac8fbcf81830420b4ed</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.8MiB (179.1MB) – 3,390,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9771f3e4449475cf96c144d99c045605<br>SHA1: 6d87755bd37c1b6e0815634ba8c61b736b36e0bc<br>SHA256: 9ffd5d686527f6717c9ced55909da8309f06aaa9f1927e0ab47d9f60763e52d3</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.5MiB (181.9MB) – 3,390,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27a3dfd07116c6076411e48edfaf667e<br>SHA1: 0bfefdaafd7ab7b1a52ef820535ab1f7b86caa54<br>SHA256: e417e38cfd0fb7e4b1d1c0b57792f3ae31c90aa24745c40c49a60ae4c0c07d82</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.1MiB (228.7MB) – 3,390,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beadc9942b08f10942edf4f34a31bfcb<br>SHA1: 4aebd7e70c34a6948e4285a4e5ff69734db18b3a<br>SHA256: f79b314eaa7ea8af9bb8ca76b1e076b7570d3b1106fefad22d959e60e3f7484d</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.7MiB (179.0MB) – 3,390,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b70c0551d6c8d1bf4238dea8a729331<br>SHA1: 6c28674db11c33ec918a943c93838e384310d55f<br>SHA256: 595d5533f447f6233ddda69227fa5d72560a953a48ea5587627b077090f6e4a6</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.8MiB (222.0MB) – 3,390,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eec15075f902b58e776850fca7fd4ecd<br>SHA1: eb5df7ff4157c358685a20f2563fbeb1b1604db5<br>SHA256: 97b6743ea6e87b2c0d7c9ddff6132225582c596f8be20c9e0897a823e8b0798a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.9MiB (186.6MB) – 3,390,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8d97bf2bbe109124806d9267b14f773<br>SHA1: 2b9a7a0208e8982131cd7ec7188563c3c1d34238<br>SHA256: b603f0b7bed36eef9abe2c7b63f403ba7a610b266986d86acb5bd5701fa7db05</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>158.8MiB (166.5MB) – 1,671,054 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc720058bc478bc30eac3e3ce674c48d<br>SHA1: 666ab4fec8c8f5b8087280524081185663bc2ea9<br>SHA256: 17e6572bb6e42f7873569152754240710d484458aeaf52e16cc1c73719fa79da</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>161.4MiB (169.3MB) – 1,671,054 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be70e051456bc608c36886bb1f9e9e83<br>SHA1: 23ea3aa9dfaea109b79c9f9f7d31a70d84998615<br>SHA256: 4f078d31a36e212c42ec55c0fe65402fe1df730a6f1794a242882667b3f06741</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.4MiB (163.0MB) – 1,671,054 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d780328b018c652d17b5fb43dd07268<br>SHA1: 6e461df654b294203399c50b00a386fb8df03bd4<br>SHA256: e4348744d0476612234ad4d3f9884853dc0acec04de36e12ece2c658d9df3f23</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>155.6MiB (163.2MB) – 1,671,054 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6e3309a3496fa60ea904a5e7a7289a7<br>SHA1: 17c8c4739dd43e9519edda8e47b0711e781080f0<br>SHA256: 389bf5c2c951d46b2d308505a3db12e591af92963ac04169cd01ef309ab9e6e5</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>171.6MiB (179.9MB) – 1,671,054 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbeb958b840fec7b77dd2fd509cc5bd0<br>SHA1: 5a2c66174bddc7857a5af8fc6116da75f1719d33<br>SHA256: fa8bf4eb49c05b5da4bc1b79ba08d2b25f197c3e63236cf2abc195b353e3a87c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>155.4MiB (163.0MB) – 1,671,054 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba81e6393d091145d4f68d98d937e6b3<br>SHA1: 2c0a7771f6928bd007a824d85dfee53ad549e926<br>SHA256: 6c44ed1e6d81192796ef3bd1da850b95a2245b7439282dc2408ba71091bb3efc</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>174.8MiB (183.3MB) – 1,671,054 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd23b3e2e7e122547f22cf6486d12b41<br>SHA1: 28879ba3e122b5309f0dffc23c48c891aece14dc<br>SHA256: ec1eee140c1f3038d14845128c397bd40344c4986d5bc77ef0b8149eb287ea0f</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>159.5MiB (167.3MB) – 1,671,054 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30097f12cb606bdc26d2b70d4f959942<br>SHA1: 866d9022eeccdc8319a2c64149a5c7f982a051df<br>SHA256: 14b8bc81326f1f04917af0666025739e75c6f3c91adca48de0ba1ee071301496</pre></details></small> |


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
