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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-02-13<br>IPv6: 2026-02-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.447MiB (6.760MB) – 322,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 843f9fa6a064e6242017c286355ab5af<br>SHA1: 5b5ed8b0424cfb52c27928e4ae38212d2bc2bc9b<br>SHA256: 14d38064bcfcf11aa011d4beb6f94a92a21df2fe70301ddad7397f82f6655c09</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.24MiB (15.98MB) – 231,555 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aedeeea6ad949982a44349a559dd2085<br>SHA1: 7c03549ce0a6805f389e37091e396f58b7e99a0b<br>SHA256: 13b51c676ef39ce655dde0746d93977ed88ba1882a60740db25f70ed7e8e97ba</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-02-13<br>IPv6: 2026-02-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.784MiB (9.210MB) – 439,816 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 976956f3fe0e5f61135c5a512f773677<br>SHA1: bd915ec20fe2002805967d53a4876f90526c0107<br>SHA256: 43db9308bb76fbcc66e36f8426ffd04ef6e7b3cf7fadf3adf063d412198eaa59</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.615MiB (7.985MB) – 115,843 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46891575cfe1cf119862cd38956608ca<br>SHA1: 6e7e84fcd8a4ceadef1266ec7d7684bd5868e526<br>SHA256: b3d3c53be08baf7d37812b7fbbdbc2b930423e2a30b2bf41ce7123a33a56629a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-02-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.19MiB (12.78MB) – 610,051 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6e567050e1d8aad1fe3c4e6fcc3fdf8<br>SHA1: 70ab7ef295a5d2f6a245183a240c8b9916e78272<br>SHA256: 7f380f5b77f4350a52bc21ce6b5472d18c84f22a5a636b31474720a5465d0756</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>97.91MiB (102.7MB) – 1,487,889 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2f9aaa2739ac332dd9924b6ff033aab<br>SHA1: 28bd06bfd91ab752a80d4f4b71bd817d61a37605<br>SHA256: 5fde1ec80b9c94569f5c537f908eabebdc78f0dd4994cffe28fb0138af9a2c3b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.768MiB (7.097MB) – 339,077 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0181205d24255559b4c2a13fdb0c95<br>SHA1: 77c5ed2ef6799485a1ff6d1bd9aa3aef442555aa<br>SHA256: f1a904010b8cf3e5db4f0ddc1b0fed4c77f852aa52effac37a04697ddb879a37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.90MiB (16.67MB) – 241,625 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f8f77acea5ee52ad5d81c9f3883d7a<br>SHA1: d3a894c2e7503a5fe5168eef49e53379425930d2<br>SHA256: 80ee4bf63ff4562160eda9ba68902de89a9e28a828c048003fd188647039bf1f</pre></details></small> |
| | | Full Location | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,746,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48770c63478550e9d616b0e8f11eb35f<br>SHA1: d754e9f10a536891a6f76b212ce1527fccbb205a<br>SHA256: 3abef96589717a094c9384cc0d2e88d16dcc6c1771a5eb42954efe056fe2caf0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>452.5MiB (474.4MB) – 4,397,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d15359a3c2245bffe65895c5939244<br>SHA1: a5622976378fbaa83dd68ce8bf186161f41252b1<br>SHA256: 3c33680bdbdc577647e1e500060fa0db02dc2af50f79e20bb78a7ae7ca1b33bb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.379MiB (5.641MB) – 269,229 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8df1f43c6aabf7404b9835918b8fde47<br>SHA1: 601b465ff0736111423be419aac3f6d5972b42f4<br>SHA256: 80bbfe7421ce68520f39ab366b0fc481427602add22c34ee6881ec43a96b1488</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.19MiB (23.27MB) – 337,206 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48696b7a642ffca450b564a365389e84<br>SHA1: 2da10da7971a84e435865041021aedd433c35db5<br>SHA256: 360124b18db3ea1ff8adc37d7d8c7432d236ac9d3e5c9f77123d8069ac8cd7ff</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.6MiB (179.9MB) – 2,969,494 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5343189d8e7d3b6229056c21a834739<br>SHA1: 8489f2c88b7fa2b7726299d47a687a5af88b7259<br>SHA256: 5f47bc0d8ce6968a1388a93536b1e895b0ddb335cd76007a7b142ca0fa206970</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.6MiB (307.9MB) – 2,846,346 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c67fa86a08014c894bae1e43237dbf3a<br>SHA1: 1bfac6af73658923732d9bf178d37d1b4cf1e23d<br>SHA256: f5b735e687c937676bc7cd2a6d383e598ea54e61f46b9863d97f53062b1634de</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-02-10<br>IPv6: 2026-02-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.07MiB (12.66MB) – 604,349 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50309fbd968f98a6d30a3fe2075deeaf<br>SHA1: bf8164489a7d4c06fea3f0ad9aa60a6adc53a735<br>SHA256: f8bc4c76c6a7029db84e704ed25e8668f755d26bdddfd8b188dc966986b44e6e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.15MiB (45.24MB) – 655,671 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1c99af1bdceced9d7facf66a1b93d6c<br>SHA1: 82eda785ffd3da16fb11ced2a3bbf5b0f49ea8c7<br>SHA256: da8adc39ed0526b94650440f74abd4d97a62091d74bb5267a47f6b242e23ecd0</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-02-10<br>IPv6: 2026-02-10 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>129.0MiB (135.3MB) – 2,584,585 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c588269c197c6bf268dba82bfc22e04<br>SHA1: 96bebd37c7596f0b1219cc806f609fd9b0b9462d<br>SHA256: e60097c90ee3622a7f6de8b8301f8ead2067ed7199a10ea76bba8c7b4c462ff3</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>137.5MiB (144.1MB) – 2,584,585 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8465d622e2c74c6b184ebdb6dbe21dc<br>SHA1: d0d651255c928656b53d578e0f92032c35adbc5b<br>SHA256: 1381af135d09935a1210fcacc86c804cc8d2c95fa813fe5ce26c3fcc8f5bbcda</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>128.6MiB (134.9MB) – 2,584,585 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99b3dcff150bfa616f4f1826a3e7c09e<br>SHA1: d5dc7a40ab4bf650f8bb8582bde7a16189a16ba7<br>SHA256: 432a1a5074081780d89c7c4ec70b139580477ae6468ac7ac661baebd659e9625</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>131.2MiB (137.6MB) – 2,584,585 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22c7adc2f34ea61e37326e7979246298<br>SHA1: e145aeffc45439ec442fb811111272e5ed444c1c<br>SHA256: 835134e095493355356b658dfdd53bc45911db4e6fb7574394f5a58ef93fa6eb</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>159.7MiB (167.5MB) – 2,584,585 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f96569b5e2258da828582a5a8d3091c<br>SHA1: 29eed4a0e0e57e28dafc063eb16432fdfe0a024c<br>SHA256: c79931dc5f63a6c280fa9edf9ee78bec96af23aa267d04d1153f3f90bed828ef</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>127.5MiB (133.7MB) – 2,584,585 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e4ecfc15b4e6ef01c767dc4479079b9<br>SHA1: 33b41299a1ed431c7a6ae4ba29047bfc30c90dbd<br>SHA256: ce85dce1e75eb602097a76f96d6bc90be7f1e87095a19db7a4d153f39ac2f519</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>156.4MiB (164.0MB) – 2,584,585 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5ff0c962c9d0b4f75510e75d4416745<br>SHA1: 2a83f245941eeae459d3ee7a5f54d2cfb3dee7c7<br>SHA256: 2720ea0d391ab28dd5a7ae748c46c268699fc75c6185d42a7e1f4311156aacd1</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>131.2MiB (137.6MB) – 2,584,585 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73c4307038540b666b80bb8855a8f3f3<br>SHA1: 632830be5159bd8348700b594e838dbd336f693c<br>SHA256: dc2222edc0b9c5e805b5141e9e511502c6707af838fc805ff590ea2c68f7fdb6</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>186.3MiB (195.3MB) – 1,963,861 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20f42c239ca2061c37ab901504b2b05a<br>SHA1: 6a06d543ffebf68b87e12d1d8a00288423a9331f<br>SHA256: 79cf2e21eebaba44f1f95b754e28d93bd1ca89835fa567ae0b39999914374384</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>190.4MiB (199.7MB) – 1,963,861 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5405fab67dbef210609cbaf507a30473<br>SHA1: 46eacd208fbeba97aea2517db7921f45c3a9f844<br>SHA256: a2fecdf39af46bd1c2bd75b03a2c71e71749efd0ef3ade2711d6ee80beedee74</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.0MiB (193.0MB) – 1,963,861 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a9cb6ac1213743968c87c050c32045e<br>SHA1: aefde7f53353b089138a16d8bd066325c606356d<br>SHA256: daf073c50f06f3debc7010eee54d8181f11b1c41ac5fed9029dd2b117d31b47e</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>184.6MiB (193.6MB) – 1,963,861 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19e7b4a841568881ad70f21ad667916b<br>SHA1: a5f2e11c43a082b5a100a95821104a665b1ddb88<br>SHA256: 7d99bfbbbbf648184bd306292eb974e360bf2a487b34ef0c3f2222828cd019b4</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>204.5MiB (214.4MB) – 1,963,861 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72189374621fd5d4a0943afc54158a05<br>SHA1: 292846d71a15178fce0d45ed6b4e9d38a06fc077<br>SHA256: e4c7bcaae81fbf8d4333b3151d912cc42e3182237521cdc24e772559e830da6f</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>183.6MiB (192.5MB) – 1,963,861 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6975d09a8dd272c75fd8ba5aca9b3808<br>SHA1: 672522462335263d4be2ca52d36d6b84ee438170<br>SHA256: 65a20c5a1dfa28a0c0d22819ccb9479ddb923283894fcce286ef818a2c6272fa</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>204.3MiB (214.2MB) – 1,963,861 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c53eb9a67af2a3f0ce31b62b1db28f6a<br>SHA1: 579e265396364a2b67f0b5f065794b0f0b36b5d9<br>SHA256: 7fa88dd6c8040acadff11ed7e54f77ff34083c08f2d33946cc435094ec58d04b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>187.1MiB (196.2MB) – 1,963,861 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a87ee2772612ef7a9d7d9d09f01ad91<br>SHA1: 13b0d6aedb7592e84077d7fcb7b046bf87ea43da<br>SHA256: 033d0e91154983029e8a883ab1809c6d5751c6d090943ab9b3cbdc5ea04c6f60</pre></details></small> |


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
