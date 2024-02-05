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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-02-05<br>IPv6: 2024-02-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.644MiB (4.869MB) – 232,496 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f120e2dbec44734af7a2cc1e88028ce2<br>SHA1: ed9029efdb884bb87daf195ed4a5095073da2261<br>SHA256: 0cc679bd4b1514c328eb50df6505665b488d2da85ff3f230afbf008e3b2f2a5b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.611MiB (5.884MB) – 85,272 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a51d0b30435aa41788b03b765e958d6<br>SHA1: 4d651039763bc610fcf780443ebbf4f5eca470d1<br>SHA256: 37959b2df441beeae2ab76b39867ddc0b3d00600cf79fb5e2a46d0b9f58b9b29</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-02-04<br>IPv6: 2024-02-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.211MiB (8.610MB) – 411,189 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8db19bc9bee42f2181f15a0b3469bca<br>SHA1: 9467c7c853c717d3e208502a99f8a8adb06a9863<br>SHA256: 41424ac31d336e75611e9dedaabe38603a75100da88ea84c965272e44dd8b159</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.946MiB (7.283MB) – 105,665 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17d7f963b9784259b3126cef48869c3c<br>SHA1: 207790d578496eb6547781565296e3d64504b3ff<br>SHA256: cfdd37fcaaa3a4f5b304915f984d27f85b1f805cc817cdd0aa08298eca80f58b</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-02-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.50MiB (18.35MB) – 876,522 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a37dbbc91c265fd8ac48398178533bd<br>SHA1: 207024826653ba0d9bfb5586dd245c5da06fb8ce<br>SHA256: c3eae826cdb58cd89b70d145dbe854aab4fc4a28a50fe207112ad1b8a71fd89a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>51.73MiB (54.25MB) – 786,193 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2537a633671755eba78bdcd0feceb8d3<br>SHA1: 5be136f15309a30fd0a664f4a64159428e38afa8<br>SHA256: ca895900cc5744d02c59230d1431ac2954c472120d19e67ce70fdf35f8de3cbe</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 322,238 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58dc67267f460ea3cf5cad59cd04fb2<br>SHA1: d7cd4a637354f5a5c457e96633e1f5c9cc5c059c<br>SHA256: 55313849f9b0eeefb503ca58aa485ebe95d325c7771a4b2e5e9def19ee8aa2f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.67MiB (19.57MB) – 283,667 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b73dc10990e7bef8c444f1cde6991f<br>SHA1: 07ae49b41bae3e257ad578c4bf31ee8040ccf1fa<br>SHA256: 7ea6211e834aaf328302ede30e6777fc4f71afb40ab1238cf0af2be151b5b248</pre></details></small> |
| | | Full Location | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>179.7MiB (188.5MB) – 3,143,531 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4796f68669fd62ff1776c3d247e13dff<br>SHA1: 8d63c70c0bd62e8829cfbd2dfba8d6b8e6c77fd0<br>SHA256: 04e5000cfd1d52386cf975f825886bb214085c10b75c2568efa51ce70fb6c3df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>291.6MiB (305.8MB) – 2,831,720 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 657b58a340f82d12479e96ce7f695a45<br>SHA1: 1b9c4719ee91d1e9da68e6f0dd1529e893bf9777<br>SHA256: fbe98efa467387f6ceb69603459abde1562d03903aa05b063edc68d9aa4e87d0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-02-05<br>IPv6: 2024-02-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.640MiB (4.865MB) – 232,256 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fec6f73486236c8d0d94598e079d6f<br>SHA1: 7f19645a2e7ae1f5579b6769363477a0ec58e5f6<br>SHA256: 7f7145aa700bc6d9b86d8e430377fb6751efd3a786e0455999aabe3401d275c5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-02-05<br>IPv6: 2024-02-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.9MiB (177.1MB) – 2,925,251 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434c9a2a5a5c869e663a7e206ad5962c<br>SHA1: f2e0c48f3ecc7d10f4697a8c5c698e1979b08714<br>SHA256: 8d5321147896799a07280f735aae4be97a74bdd31110778527dc8f4b77485f61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-02-02<br>IPv6: 2024-02-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.339MiB (9.793MB) – 467,816 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa85865502c623a87578d33cf93943ca<br>SHA1: bd15284f72fb5dce688af181ca11f107718209dd<br>SHA256: 1eef89f675ee2f3aaa95c911d1e8f971a07c157baff517304eae7f751ee70a3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.29MiB (19.18MB) – 277,988 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1daeed8b883ab34a986c326576b37a72<br>SHA1: dd858639ca64c48b165b0a733f3f43acafe4a869<br>SHA256: 50daaeaf83b13e568a23d23deddb104158915aa60d72edcf4db5e52da518edfa</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-02-02<br>IPv6: 2024-02-02 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>158.3MiB (166.0MB) – 3,364,357 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7bec4a442326156ce5711d5588c8120b<br>SHA1: 5b536af2bcce5725317e11760f8eb03d17a1cb2e<br>SHA256: 116fe2376141a779054e5e89bd66bbc7ebc0b2c84c7033db60ef814b42c7b359</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.4MiB (193.3MB) – 3,364,357 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cbb741f7aa89beac50cedc98e1298a1<br>SHA1: abb831cfad9692b608e5f79064e94d5a775ccd32<br>SHA256: b6c112b9198d3587da5031ddb328f2bc7f493f0b90a32668faea745a04ab70b7</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>162.4MiB (170.3MB) – 3,364,357 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8bc00869bb4dc9da90a3273c05edc105<br>SHA1: 41ba26194603f44713c904c3d1e5008058e71b46<br>SHA256: 7bb37f3ad95610b4b71c9727d182fdaba269a65bb98eb7ae4974574154087434</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>168.8MiB (177.0MB) – 3,364,357 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80741cc789feecb6c54b9a462f347591<br>SHA1: 449266786e5c73395e49908048e462e601adb3e3<br>SHA256: 3b6610b28aaeaf6ef613f627f5da4a6fa30cf45d7303d5ccf38d1ea9077ef077</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>197.1MiB (206.7MB) – 3,364,357 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f43de37a517202c7d4eeb0dc516dc987<br>SHA1: d3e8973f9f153982783c07e2bec4ed6ef02b7c21<br>SHA256: 03c3288a0e62ad7a12cb445e3e8971689ab436557aa7e2856aacaac21d7a5264</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>157.1MiB (164.7MB) – 3,364,357 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a659a96a343a80a8fc54c2c13654cdf9<br>SHA1: 909a3a1731dc7f7b3bb8d7e86861863f7f487f36<br>SHA256: d93a799f81e834e18ed1adc373280463a5faa43c3a71cb402d756d0c26dd9883</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>196.5MiB (206.1MB) – 3,364,357 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c1bf570c7617ab0c5516327508264c4<br>SHA1: d9048a68f8f8d1cf554c6411144973673b39d133<br>SHA256: 6b54f8df493ee7de65143e3bf1adb663ee6f29da0f1f9dbcea016943787e57cf</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>166.1MiB (174.1MB) – 3,364,357 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8fd19f7456418a0e6f3db694fc1e744<br>SHA1: 8a2419b7a268722f763470e4966c4da2d5652c8c<br>SHA256: 05cd7fa2525abe4f1ccbd8db0eea1aef85eb69127bfe8dfc309af0832f880553</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>100.4MiB (105.3MB) – 1,122,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db4766280b0eaeb0e6d6f6df2fca6455<br>SHA1: 67c62ba7f819311122514e5250863676273c36fc<br>SHA256: 80387d4929d102cbe9c1009e79412c8e5232217e408c382806d0837a479ef674</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>107.9MiB (113.1MB) – 1,122,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 797313e9ec0eb9e2c6cd1735bbd7491b<br>SHA1: 1952158e8f00a87896546a892bbaa9a02eb0e28e<br>SHA256: 0745c22609741c80e3012f20594f8e3d8319c9f36aaab18e4a5d245d34c134e5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>102.7MiB (107.7MB) – 1,122,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd1847073a0d835af9a0911aa80ff99d<br>SHA1: b8dab67d7232e47e154ec44180805431e2902562<br>SHA256: e1f05200b9cd82631a486c9c46cc7431bdceb1042a1ff0d3bb220c1d6148cfe6</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>103.4MiB (108.5MB) – 1,122,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62ff9a99b0cbafffe655f6e27a54fe96<br>SHA1: 390fabf3726b21cf7567031cf95556a6e52e3308<br>SHA256: e54f58197e6d0ee485530c1e1798fe4cba3efc6ec3cbbc86d6e5ca55fa7ba62e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>111.2MiB (116.6MB) – 1,122,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 211a82237e890f7a166638bbdec4de8d<br>SHA1: 62d4612d07f5f2bde39dd89e2c18f5f8695d9f66<br>SHA256: 2c9cf01a919f59e03b8160393be5b8bd1abd19dbc307e047f8f98c06483c64aa</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>101.6MiB (106.5MB) – 1,122,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da4913477f4d107161dcbbb659d71ea0<br>SHA1: df417bbf0d7815bd08825b60cee05d6f7a047d96<br>SHA256: 369ce989e077fccefbd15d261f200c2586c66785b144989c2e98fc445ecdd57f</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>111.5MiB (116.9MB) – 1,122,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0b5314edf016f32e2ebdf9084f82e31<br>SHA1: 713db6b9512745da4603bb62a59ab9ea5fcd3c1a<br>SHA256: 119d68ec979813f530ad41f5013155c51065fd5c2f4f58e1411245a378511704</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>104.4MiB (109.5MB) – 1,122,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c7a9dd398039e95d770e2494ce0a48b<br>SHA1: ada89ff3ebd96802fa882f12557780e7a6060a14<br>SHA256: 25af43e1b23f441ba064ed3c5c171936028ae0f431b67112954c02dea312c9e3</pre></details></small> |


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
