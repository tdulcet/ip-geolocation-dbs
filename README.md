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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-05-27<br>IPv6: 2025-05-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.249MiB (6.552MB) – 312,912 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9d68ac32333918ca0fb97453c77f233<br>SHA1: d5c0d62947617220d17f09ce3ce82477789c897d<br>SHA256: 9d8c5e731171bcef0e687fc9a8eb11bdf6695d086294977b3c9dddf13cc1652c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.26MiB (12.85MB) – 186,248 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 708e0528775ad3b23cc4d1363b58a17c<br>SHA1: 1d23fd6e72637d9c73607b4484625c46f98008ba<br>SHA256: aea0124178a3ceeadd441af3b83101895b642eeca0e7dcbd3d00d9702be8a094</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-05-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.91MiB (13.54MB) – 646,375 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e57357f9665ab7abf861deb81c9fea4<br>SHA1: f43d6c728bb6548b97a2fedbb6ffde064977a5ed<br>SHA256: 5b49895ecab8c3308d1d19ab8e5ee54c3872d1f8d1da43626a44da0480be0531</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>98.12MiB (102.9MB) – 1,491,150 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: faeecf0a410e18e0ec68353921e7947e<br>SHA1: 5bb2b35eb5ac0ba0d11f42c82790e00bb7255cc6<br>SHA256: 678a2a6766d5581505f612da87fe4c23a8c2df8c0183b41080b16e9e2ab098d7</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.057MiB (7.400MB) – 354,084 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29dc016a76e5d1ce86f281b6be610e8f<br>SHA1: 91c6b4652acafb63416678a1a40d09acb733d81e<br>SHA256: 8c2e1dc4bcb582e63e3cf9a404cef7bbda49da95853a250d12f056cd6e928998</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.75MiB (18.61MB) – 269,749 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3faba08113ae8afbe0f9aeb0c0bc4db1<br>SHA1: baf9d49de9c133023e8e928090c9f50a291301bc<br>SHA256: 126f6ef6cfb9616fb3631b757bf8a7746130d673be4019cc177df52967b9cdf0</pre></details></small> |
| | | Full Location | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.7MiB (197.9MB) – 3,293,979 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc252212886dac7c40089289aaf5a71<br>SHA1: 67fd9db8ecf45ba433418c2361c87e2627dc8c3e<br>SHA256: 6fe5f2b32b1d809aac5a716539f4708f61c901ddad9c02b4ab613c7e262ccd06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.5MiB (412.6MB) – 3,819,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14c6250f6e4e959f775581c56c6b0abc<br>SHA1: 77ffea96762cadecd4cdca9183084900fec55cb2<br>SHA256: 1bc149f9307004c4ad7c60c0f1a25333a23792c5d431b1b374511792cbfab474</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-05-27<br>IPv6: 2025-05-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.968MiB (5.209MB) – 248,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d089ecb129beaeaf2a0c4ac1427eaf6<br>SHA1: 3b494cee2f0d5a67c96e8fd9ac320d9451b36a7f<br>SHA256: cd40baf1649b683953823e24dacd7a02626143eb798e879807a24d509beef71e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.24MiB (22.27MB) – 322,743 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beb56e4b585711434b2fde993d168a9c<br>SHA1: 55d2015800e048a7089193a246f2d5b1249d4440<br>SHA256: 9d5dd5a77dc590c2642e0f671432b7bf9450c4d0347d15a7d904c0c0b55c8ba0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-05-27<br>IPv6: 2025-05-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,019,379 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a68d931a9c3aafbbfc0ff557db9889f<br>SHA1: d3c7b6a63aa399a3a3bca849a9160e65422ac12b<br>SHA256: a6f47823a7140f643c6df5dbe10363559d6998953d47e61148fa9ce21dbf44bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>244.6MiB (256.4MB) – 2,371,820 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db0839b0b336b2cf8a46e6bd46836924<br>SHA1: fe99a8305efd24139243b32063ad92bc72cf9fc3<br>SHA256: c7e0b4a9c07317086b1a652dca4b3928e1bcaab9d1faa273e38c74a68ee151bd</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-05-23<br>IPv6: 2025-05-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.85MiB (12.42MB) – 593,216 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd23ed4b3de39c6524f21517f4963073<br>SHA1: 3ea1b697d2ce640c57b6213c132ee7a95b86af19<br>SHA256: 1f976e342fc96bd582c457c06799539793c13e75f4b32e9916aaeed990497d5f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.45MiB (42.41MB) – 614,672 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a16c647769eac97972720ca5d4bdbb80<br>SHA1: d50a8258c34adcbef5fc9ff99f7ee70de3a00a0b<br>SHA256: ebe46fdd80e58b539562640a561ad71e93aefe98c79ff3a99c12924069ff7e87</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-05-23<br>IPv6: 2025-05-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.5MiB (179.8MB) – 3,382,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 895a2765c147177c92c6b6b1376ad96e<br>SHA1: ffa4018485f1aa12986f5fb0c5038d2a2b43dc6f<br>SHA256: 212cd873ef6cfa60657a80b76953019731053463c931587ba3ddf10b3b305aee</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.2MiB (191.1MB) – 3,382,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ac678697ef97304f315582539f1cb7a<br>SHA1: f647a65dbef83bd3204aecdb36d3ca6cc48935bd<br>SHA256: 9d43741ebcdca2f9cda123ca1b374f94f9d1805b2c5c7d29f9423af563d2aff0</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.6MiB (178.9MB) – 3,382,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a57df5bb76123183f749555de3d98630<br>SHA1: 8cc5c42e0b5972382134fc205fc97553bc5e951e<br>SHA256: 6128a9d8d80c37227cb91a6c927aeda1fd024762d04ca7f4fc1aa0359672245d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.1MiB (181.5MB) – 3,382,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 12221846fc7c684df785ba208c6c43f6<br>SHA1: 0fd2e4328fe18ccc45fd8037581bc79c1f3ae2e4<br>SHA256: 8b4dda94fb8096c8e61654a49bc4362861237af15eaa9cab76114d149393706f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.0MiB (227.5MB) – 3,382,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8cbd62fbbbf26cd209cdad7fe0d63146<br>SHA1: ec3695e7f56940d286556a61d21978fa7e7c750e<br>SHA256: 0e2af651e14987175bf3446ed58746796e2b68c19caedc28d5b3fae67f0e781c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.2MiB (178.5MB) – 3,382,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66ad93a2ad0d5f6af872312bfe81ca83<br>SHA1: fe6df4da4da601e1cd297d1365199aaf56fc385a<br>SHA256: c77b9655781ed6b9992edf71d5a2272d1931affebcd6a64e2f68c6df83c29bd6</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>210.9MiB (221.1MB) – 3,382,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf941d1d61ead81a01082e0e5de5d5e0<br>SHA1: 505464e3df8a0858d451c5fd4799779aa3bdc9fd<br>SHA256: fe8d842d48c75330befbf0c9f2913746962a1b44164c531fff0738f00908e4d0</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.4MiB (186.0MB) – 3,382,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07aa2f8733494de5bcf4658381d20ba7<br>SHA1: e35fce2ae460e540088311be6256fea342ab75e4<br>SHA256: 32fc8e7c791fa991bf2e72f54d4b328ad04a8bec05ec2811dab704a734169584</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>175.7MiB (184.3MB) – 1,866,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22818e4c832d0e9c49f38a15027ce74b<br>SHA1: 3072ce5f7b9eb96af57a3ca0ebcb4d847c7ae244<br>SHA256: 098d7893e9b19fe80ac1de3e3557889b1a839f19b78b583655759183df80faa3</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>179.8MiB (188.5MB) – 1,866,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1f4acac366a9349f3878cf1999bdddc<br>SHA1: a22289825374d2cc8a391fab4f21ec82da064830<br>SHA256: eed12281f244a77a5934c8703b9bee2f5b6a8040163e54b4a94d9074a3e01349</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>174.0MiB (182.4MB) – 1,866,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4576178eea5495853d39dec9ae07baf9<br>SHA1: be651941698822e2f4f9f3978a91e74530ee3b94<br>SHA256: f4649503d0f970c9e03497f1644bd2e92a02c9f0459f3b609f67f4698380fa0d</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>174.2MiB (182.7MB) – 1,866,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10d18d3980f980bc7c611128b654e581<br>SHA1: 37f0a8fafc9156ab4777269a98b914c7a0c6a3c2<br>SHA256: 8e6049928d980d10ad15c5e3b9d164fc3f9f61a67f62aa679b153da066af1fe0</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>192.5MiB (201.9MB) – 1,866,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93fa487887f7ffeead13c1f00d588f17<br>SHA1: 0ba9ade262351a089edab7f107871bb6f4af07e9<br>SHA256: 6a76c092c60a4693c3f173f7ad4fa1bd8e6f06182d12443a98da73618d0ada84</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>173.7MiB (182.1MB) – 1,866,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86067258bb92cb43e3c54b31aebf8530<br>SHA1: e33abc68bc18636d2c6169bb795801df52339f45<br>SHA256: bece4049f7bc93181267fb7fb8aa54a750e3836044e95a39c82683185ca1b6ec</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>193.5MiB (202.9MB) – 1,866,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d78891ca1f7fcfab75197b5a1f323e60<br>SHA1: 427c0050286e276a327858e6f9181d4e06aa645f<br>SHA256: 20fdb28959ba49280f9575e9bc6c883bf366fb9a1c6e312657792c7eb70c7672</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>177.5MiB (186.1MB) – 1,866,964 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 607d8bc8cf197ad2816aff5bfa1b7281<br>SHA1: ffe45e3794a7935c2fd289eabc3f3f7daca3d4ae<br>SHA256: 831e9f96ebf09c2c61d6ba65a714f97c6c0a6434d96d7518265feee73832c379</pre></details></small> |


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
