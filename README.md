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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-03-13<br>IPv6: 2025-03-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-13<br>IPv6: 2025-03-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.367MiB (8.774MB) – 418,981 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79769618b486db83fbb99ef315187c30<br>SHA1: 2fae90ef975194bf59f1ff72f60a7ccf54b834aa<br>SHA256: 5515502d93c332ca45b69b6539d3b706f34efa746d64404a6d12fd5d2b255611</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.994MiB (7.333MB) – 106,393 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c69b5a4f6f58c7a91e4f65474459f5f5<br>SHA1: 27a65688dc89d9bc63555df1c06ace0af2b8d65e<br>SHA256: af13f2351b7aece86b1a45c7f25e16c67b8f69bb550c7ffb603725c0dccc459a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-03-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.73MiB (13.35MB) – 637,346 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d65ac1457ff71004d8318efd20083431<br>SHA1: f3e5a007edce19ea0e4a9943415d4334ed0882e7<br>SHA256: 569d02dff81c51a1cf9a54f8118fba6c1de6daf1bb6f046315ebb4e0f259f0a8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>72.33MiB (75.84MB) – 1,099,195 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d838d34854d62f0e1ebe7f021761172<br>SHA1: 92f6101dacc0b1b959c44aaed45b81e24578a26c<br>SHA256: b5bdb71fbff64bb2768a291b9773e484cbda6471256f50168f2181a8bfcc79a0</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.404MiB (7.764MB) – 372,055 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e5911df23fa4121906510a5a567b13<br>SHA1: 9325bb0b20fe7cf38b086bd997249c0ea0460073<br>SHA256: 388e526b141f72da365e6c1487008eaf5440f4e2a173bfada2766c55cb3eb316</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.53MiB (17.34MB) – 251,265 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609d7024eb89dc7bd684d0207b3733b9<br>SHA1: 956350aa870d6a38630af3f3a3b53278471d39bd<br>SHA256: 95146645c0293ed5818f1df79ae51e4c9c07a1f6c91ea0f9331b8da35b754bbe</pre></details></small> |
| | | Full Location | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,335,187 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d87186c64f981273c433100841370<br>SHA1: 62922290000ef7c4549382119783c2045e4d1e6a<br>SHA256: 51718b9bcaef22b3bcf85a754a3a5fdd48d4a0efd9af8a4e3532e918a7368b41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>388.5MiB (407.4MB) – 3,770,967 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a5296fc623ecf8f0caa811c6b1aa61<br>SHA1: a31112844edcf6b611b51dd56508b700f7dfd9d1<br>SHA256: 4018f4afbdecaeedf11e8e21fc7f50e5719bc241f3a50121788f441946a9b58f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-03-13<br>IPv6: 2025-03-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.118MiB (5.367MB) – 256,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced96baa8d12dd7a7473b62ca04f3ec1<br>SHA1: f15aed8ee671e3e27c23c736e23edc25368ae1b8<br>SHA256: c034868fc655de42297d14220caccea0ab330ee13028773c38db7c6de47b21b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,344 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cef1451430608ae8ad70e0f4963dff<br>SHA1: 43bd5d1e9844ece7eae20604c4d83f7960da31a0<br>SHA256: fed2a958c9ff8365cbd35a38e1b062b5237d9c3576831c5f27705c77a13bbff3</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-03-13<br>IPv6: 2025-03-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,062,954 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1de2b09cb2477a5e3a644739a02d816<br>SHA1: 2ab572bf0cc2040a312448643055f2f718ca5ac5<br>SHA256: 1d66b45f20fdcc805cf1b87b04dc600ee7e3bcce4b90b5400d770f1ca47a3254</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>233.4MiB (244.7MB) – 2,257,726 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d52faeae6d9b914518dee2695e772b<br>SHA1: ba805ee8a2f7aede9c579332c56ae8ddfc7f7251<br>SHA256: 87cd4c71031299fc55a0c464dac619478c748c283c398787e9e7547a3ae9b9e1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-03-11<br>IPv6: 2025-03-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.24MiB (11.79MB) – 562,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 204510b5d13f614195ede983e135301f<br>SHA1: b986cac35192d9454ee251c18282de31cc9f2ef2<br>SHA256: 0d3b5ef7bd5a8b29fe49533fbbe636f5e2c3ea6a06e95e1c7db1f67cf21ca66b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>37.94MiB (39.78MB) – 576,554 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6cdbd9149fcf1ff8e809c07f0861e64<br>SHA1: ad3a73bd5adae45b329e867a9c046dda7c051275<br>SHA256: 74617029659fa24bc50482750774f5beadc3133484693a8a52cbc51bc5547dfe</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-03-11<br>IPv6: 2025-03-11 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>167.6MiB (175.7MB) – 3,312,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c67a98996e9f32b6165300f29a037e1f<br>SHA1: c5ecb1bac0e52dc13957fe3b317c97f6aa44f83e<br>SHA256: 12f3565104e0327a84d759317fe9888e7b0a68e9d18e4657144bdf6e13554c0f</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>178.4MiB (187.1MB) – 3,312,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d052a458dbf78005689adc5e889b488<br>SHA1: e8cee766554267959439ca85d59b97b9bc5a3646<br>SHA256: 5c7757ea0b576198b559e6ab7ffb5654220c159c4988471c8af30310875ee962</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>166.5MiB (174.6MB) – 3,312,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b1b4a22690ac5abcbafc0be914fa262<br>SHA1: 5bbc14d1a597e15b523054b6578397f5e482d108<br>SHA256: 840ef57f7f0add9d15b97bb27d743f5cb036db290207644bb34cc2f966f35c42</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>168.9MiB (177.1MB) – 3,312,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 903967bc6ae13ee6852172dcdf4d1450<br>SHA1: 5725a1c660a3af9fd344745a622f75b1ac98fd8d<br>SHA256: 91458c182f869929892ddf6f5eb004d8b48906897edeb764e6524bee4a8b771a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,312,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6dbb1cab1883381784b96584d9a55e6<br>SHA1: b21fa9fd8a7c4e63c34b4858aa2479672c33e485<br>SHA256: 53dab9bb1694b759d3332f22b498e0791fcf495ce401574933d9d70f4c8b8f20</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>166.5MiB (174.6MB) – 3,312,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b13d4429fc130685081c1a6d40847958<br>SHA1: 38eca0cb8d9b13ca4cfcae277251e6c1a1c7fd00<br>SHA256: 72f3ae8399ea870091cf27361e9f8681de1252dd1466d10ad77c625d02ee40e9</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>206.4MiB (216.4MB) – 3,312,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42ff31b10b396e6f6bbb9b93c0a0618b<br>SHA1: d410cb034c851047dd31d0ed7d8eace044bd4eb6<br>SHA256: 642e2a097d10354e43e3578c5bf6adba5a7d423b40113cf002da1ac8197acb53</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,312,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8fa9f2b2de5c58ee4214c992f00bbe7<br>SHA1: 71e2d507e4698940cbe97a75182267cadafbfc43<br>SHA256: a3dfe2e5fbac8130068f037f38fec80af84ed727459fa52b9193135ffdd9a319</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>170.9MiB (179.2MB) – 1,816,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c97d22f711f49b9953d72757033e18f0<br>SHA1: 2d09e348cacc888edb69da2d0c8512ce6f5726f5<br>SHA256: 92e9c20d5cb8f3aa9d571a8eb8cd83ed15e85113f855646701b559d95249ea3e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>174.7MiB (183.2MB) – 1,816,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48d56814ab336328aff1b7421a1f2db8<br>SHA1: 6be9ea47b82a8316a4b4830f59f58a31c8429ed7<br>SHA256: 2dd6ba4e888da4b58b088b94490fefae17ef666640ffd1b1f4f311aea71142c0</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>169.0MiB (177.2MB) – 1,816,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b834e3e9a89fc150fe079cb9537a08dc<br>SHA1: 5e5f8f361b0a525137618ca9b7655b1b1f4776de<br>SHA256: 0d7e8dc2942efa73c4b1815aab65695326166b4654df47604460b84ae3b4da37</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>169.4MiB (177.7MB) – 1,816,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c93ba34bba0fe900cffe19f9b55f3144<br>SHA1: 4325e78ed90257393269757ce3757a2b02c12914<br>SHA256: bc29f5c75232ace5aecc5f31075242a46c7944efe0f49c393df182235d466477</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>187.2MiB (196.3MB) – 1,816,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0846c43e50e7691f6ad894d386f8ad34<br>SHA1: f0b5c5ecc66873ad15d2a9fe61970e316bfd9077<br>SHA256: aed9596b55973098253ea34d0217495fb27ad317ed34bcd327cafa350ac584ac</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>168.9MiB (177.1MB) – 1,816,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 132c4faa4a8876de3e710b9e13a82878<br>SHA1: edb135ee77cd410fdf4ffe8a9d89ef0eb4b1c01e<br>SHA256: 388ff656cb93c285b1ebd10bf9f4505a574bbfc1a7a8758647edbe71e55cfe5c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>188.2MiB (197.3MB) – 1,816,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05d9ccc77f776471117dca8dfec85a97<br>SHA1: e04b97cb7a1692e5042ceb4274f43b8fd46220fc<br>SHA256: 90107059991e7efc6c1aef5aa75c3fdd4cdc9505461f552884d770b7616a56ab</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>172.8MiB (181.2MB) – 1,816,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0290087ee08b0502019729aa156892a3<br>SHA1: 4cc905c9b1622793e8fa63cce5af143f45afd456<br>SHA256: d728e59ba0b7dfabe2eaa12b2163e505313a6915c59f269fafc4141e9b6ec235</pre></details></small> |


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
