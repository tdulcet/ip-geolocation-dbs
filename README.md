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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-02-07<br>IPv6: 2024-02-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.796MiB (5.029MB) – 240,099 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d393bd86851291d11a461eee38dce0f6<br>SHA1: 5cfcd486348bf13b24e6c5e485b116d4f913b69d<br>SHA256: e3b3de3893bedfe1c068bb845a5a9d8a833b25402a6b8e51ffe044898461bc03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.575MiB (5.846MB) – 84,728 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7f0212e934a74cdf284cd72ee237879<br>SHA1: 43c124f6becee13326d056e46dfff74ab771019d<br>SHA256: a59b39bfe65c789e329270a2674d7027ec847a7ef673fdd0cac863930cb37ed8</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-02-07<br>IPv6: 2024-02-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.215MiB (8.614MB) – 411,398 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b1c9312ed2bafb61898a1502e385c46<br>SHA1: 7d116657f31bebb8d64336f4f3ff359cf4683e3e<br>SHA256: 18747acd0806bb50dd0a129023cf7eab34afb6d4ce650dc31aa1363a39f1a274</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.962MiB (7.300MB) – 105,919 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a07f018f1e57e60a465535c83099384<br>SHA1: 7e3d50d68ec542be01a9208b1145fd586aa37845<br>SHA256: 03891a230b9cdfbc244ab9d2e69bdc7e3d8574b8b80c740c6824c29e15b7074e</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-02-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.53MiB (18.39MB) – 878,053 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c817f04df13f4ca540629a7aa5ae05e4<br>SHA1: baadf7f0cbd58ffc1841e4a02e73922e6c3919f5<br>SHA256: 43f9362bdc62662ca9e1d4be3edf22486c994568066d406795867cb0f44ef8a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>50.60MiB (53.06MB) – 769,012 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf27afc5f24f1d1682bdbd375dc5c8c5<br>SHA1: b5871e92f6f9fde9cd68601014e58a410ef7b93b<br>SHA256: 230fffb2ab90e53401e86bcd7fd5a24793e63661d188f70daad845c3490c4145</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 322,238 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58dc67267f460ea3cf5cad59cd04fb2<br>SHA1: d7cd4a637354f5a5c457e96633e1f5c9cc5c059c<br>SHA256: 55313849f9b0eeefb503ca58aa485ebe95d325c7771a4b2e5e9def19ee8aa2f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.67MiB (19.57MB) – 283,667 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b73dc10990e7bef8c444f1cde6991f<br>SHA1: 07ae49b41bae3e257ad578c4bf31ee8040ccf1fa<br>SHA256: 7ea6211e834aaf328302ede30e6777fc4f71afb40ab1238cf0af2be151b5b248</pre></details></small> |
| | | Full Location | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>179.7MiB (188.5MB) – 3,143,531 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4796f68669fd62ff1776c3d247e13dff<br>SHA1: 8d63c70c0bd62e8829cfbd2dfba8d6b8e6c77fd0<br>SHA256: 04e5000cfd1d52386cf975f825886bb214085c10b75c2568efa51ce70fb6c3df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>291.6MiB (305.8MB) – 2,831,720 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 657b58a340f82d12479e96ce7f695a45<br>SHA1: 1b9c4719ee91d1e9da68e6f0dd1529e893bf9777<br>SHA256: fbe98efa467387f6ceb69603459abde1562d03903aa05b063edc68d9aa4e87d0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-02-07<br>IPv6: 2024-02-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.640MiB (4.865MB) – 232,256 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fec6f73486236c8d0d94598e079d6f<br>SHA1: 7f19645a2e7ae1f5579b6769363477a0ec58e5f6<br>SHA256: 7f7145aa700bc6d9b86d8e430377fb6751efd3a786e0455999aabe3401d275c5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-02-07<br>IPv6: 2024-02-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.9MiB (177.1MB) – 2,925,251 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434c9a2a5a5c869e663a7e206ad5962c<br>SHA1: f2e0c48f3ecc7d10f4697a8c5c698e1979b08714<br>SHA256: 8d5321147896799a07280f735aae4be97a74bdd31110778527dc8f4b77485f61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-02-06<br>IPv6: 2024-02-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.417MiB (9.874MB) – 471,726 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39c9737a02c8324765a22505d79e120d<br>SHA1: 8a491e717126c1f6641deb52a25a35a14dde9553<br>SHA256: d2341985baed735853058302b593f21a11f20cc80ba7f7ff41ec419aa8e56678</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.63MiB (19.54MB) – 283,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa042eefcf5d663a38219a9f9f291306<br>SHA1: b0bc98e78aed51e8551741907ec157bc3bfbc541<br>SHA256: f245d7af480804596c56e00e0c91cfddb9c1e90659c3e87d812b342e358cae96</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-02-06<br>IPv6: 2024-02-06 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>158.9MiB (166.6MB) – 3,376,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb1ca0cf9fcb80da7d22c8fd12792e48<br>SHA1: 9a5bfacf0dfab723575212d05e3380c911669a84<br>SHA256: 5dfe67372a7bc1371c16fcc32e9b61edceabed566561062b19c8c2846f9c7437</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.0MiB (194.0MB) – 3,376,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8867e44ab614eec3b8f2882184219e8b<br>SHA1: 13c02811299b8932e7bdc6527c58ab163d88f520<br>SHA256: 3ebaee89a2de80e7e513b4b1fab49b50efa6658098e29adf70594e14a4e97890</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.0MiB (170.9MB) – 3,376,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b4f0651a0dbc76906877b445cde19f6<br>SHA1: ad8cc6f431de8f3ff853e31c5e4b30c1d683ea66<br>SHA256: 791c25d1c5ce3e485876b7520ee9e5daa25480c839914f74d771c24b9d662927</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.4MiB (177.7MB) – 3,376,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f304ae214394ab97651bb0818d1ade9<br>SHA1: b5e49277e09079dd7ca16c53d520f6a55b068c5c<br>SHA256: b3f06c1e40f1a2c7978c1eafa6128d79ba2c3efbd27d4b09da0c539b6df62a1d</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>197.9MiB (207.5MB) – 3,376,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de90ef23a8458fbab5cf1e77b9248e31<br>SHA1: 3a36b17435f835675cf50b96a8fce6ac8b179902<br>SHA256: af5abd87edc00aeff163940e873f7cf2aed32daa7ac7b92fd370726e72a1955b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>157.7MiB (165.3MB) – 3,376,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d987f05f0bb6429848640c7d9843411<br>SHA1: a3c2524c9f50344e13bb8eca5517e3f0baaa4843<br>SHA256: c103fe59deda17ae79076f4257abe2f63d71b4f5028e09f498ba8513b383aa49</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>197.3MiB (206.9MB) – 3,376,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55f76921dee07c139aa9dd854b416b09<br>SHA1: e0a64c5c94e1b5645aaf845562cbb3527d82bb72<br>SHA256: a6a755ebb8009f1caa34ab72e8287178ea8469694e3c06041d4cd87e5b4de387</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>166.7MiB (174.8MB) – 3,376,481 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76288fbb5eee27ef08002bcfa4b7d9b4<br>SHA1: 7cf03443ee5e474adeb8e961f1a12525d1cbb913<br>SHA256: 25d081886a638eda31c39a53c492e64279d966cef77b08d1bd2311d291841096</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>105.4MiB (110.5MB) – 1,179,580 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9830e40e209d4677fb9b892fcd1e07ec<br>SHA1: bb295d4f4d11c271b29816e6f8136000e218ed87<br>SHA256: fc80227577b7554ef82f5941ed9a7698218c1de7ab16d479e90d57eb01bf6f9f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>113.2MiB (118.7MB) – 1,179,580 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4466ac7d027de64a306e60039204a88<br>SHA1: 7db10d2500c29a3c499c3b8731a976d339e5cd79<br>SHA256: bf3a8f8fabfd57bd3d192a21bf46d13d79125fef27ba9cc32d73a165834329b5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>107.7MiB (113.0MB) – 1,179,580 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2d59b8721f9f618dd1b85bf879a4e07<br>SHA1: 42a6a29c9d97be86d16f81bccbbd8cc8f9a2ca10<br>SHA256: a7ae92df13028d29a6c8bfc77effa90c0afe924e4ff007a39c0c32f57d8a5595</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>108.6MiB (113.9MB) – 1,179,580 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2de1d2986d9c730ac386785d594849f<br>SHA1: ad7b99078bcad834e7e518e97e4c8ee0c5a775a8<br>SHA256: 2bb760bb3aa5aba960fe8bae6662c8e86bded4da7206d307b6a1ad460d5cea78</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>116.8MiB (122.4MB) – 1,179,580 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f032befeee20d8bb276d682b68ed0421<br>SHA1: f72c58836b84cd268d114249a062d4d13c39d81a<br>SHA256: b59ba18ff88f462a1c8201f987c44aa43111c985c42bbd3ea839815277d0a330</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>106.5MiB (111.7MB) – 1,179,580 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cea2281a5bff56d515af890ea7605d6e<br>SHA1: 8ca99b55719be6a9935905d12f360720b3fa5ccf<br>SHA256: 0a43e4a854690b053c9c8b09e4572cc589b32e4c691f4bf29cf21637581b573a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>117.1MiB (122.8MB) – 1,179,580 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7460bc2a58ad42e9f10acf8403b3b150<br>SHA1: ab0fd377442c8d366bde694100b4f9f1dc006e2e<br>SHA256: 9449fea1f2b823d8ea40a0313d6485bbe2607ff45ebff99d7a8895f93eca63a3</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>109.5MiB (114.9MB) – 1,179,580 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78aac2dd8c293e66aff9bcb80ad5c29b<br>SHA1: 0deed6f4ae64bc54f0d380251f404ddb64faa77d<br>SHA256: 4d82e69f0ddf9d44913d3993f516ac77feab806f0935de1a719b75cd7390759b</pre></details></small> |


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
