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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-06-27<br>IPv6: 2024-06-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.734MiB (4.964MB) – 237,015 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1acfa4d6a45419c0cee9024cf9e5726a<br>SHA1: 0aa00dc3796a9bdc5db6e5ed01030c92df993109<br>SHA256: 165561ec636d8bbb57ec281ee491c199829108bb60154fac57f65ac66360d72a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.512MiB (6.828MB) – 98,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a331a17c0b71470242280330c03026d0<br>SHA1: a460e2d16ba87fe9ca4ce8dcbcb7f5ea3cc0992d<br>SHA256: a1643bac1cf8c17d65a64c2d0b669090d861beba16a7493655eadc12819ffacc</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-06-27<br>IPv6: 2024-06-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.099MiB (8.492MB) – 405,578 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ce0fc18db4ed41e429545e8ca22e674<br>SHA1: 84ec1c38fad25712c2f1c229a70d56ff20071648<br>SHA256: 0ef73e57e172849d9e35098eead27826ce6a77b23b4f643062f26b2870632a1d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.467MiB (6.782MB) – 98,397 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd2c36a4bb794c48de0ce3c375c4f826<br>SHA1: 35ba26e36929e54f8e7bd2dc4c210245b12a1427<br>SHA256: 26840cbb6b8b8a4f7765b6916c191c0268862bb7014206b2300258612c528688</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-06-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.59MiB (18.45MB) – 880,271 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4eaef391ec2c113839e539d2ee170d99<br>SHA1: c9bdced290201fb6a130e2dd6d3698065520ced9<br>SHA256: 7fbc4f0fb2a49a5f0d3b0a739497cd01461dcb7ca9cd63515998c5d4fb1b964b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>78.77MiB (82.60MB) – 1,197,051 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95d1fa169cadfe18b750c51770efed17<br>SHA1: 485f69bb2234791115ae8f4ec675114048eff7aa<br>SHA256: 3d88e4f77e717d809d8c486281dd51cd679857bf4aa537081f6add571c093021</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.920MiB (7.257MB) – 347,790 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228d49dd4c10c1d4778473109614f06<br>SHA1: 84aeb9072586fe27e7a2fd0cdc62b4421b417010<br>SHA256: becc801a5b95a0c7e6dea789881460b3cce70a60f8b941077db5db9f24f332a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.87MiB (16.64MB) – 241,164 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77063c075f456a1e11f7a52af24ac9ce<br>SHA1: c787ab002266a3398026d5342c963fd1ea59f3b4<br>SHA256: 72503d5df7ba2b39c61d7f574dd167649fdff103e81019ba98b18c192a045f0b</pre></details></small> |
| | | Full Location | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.7MiB (195.7MB) – 3,261,621 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d700e342b096e0b5285fb98e7ea719e<br>SHA1: 95986a4433c4d6be7ba8f0d38d9ac62adeb2d962<br>SHA256: 48ea78edb396cd5b834f2a55d80909bfe196c2ba8756c47776a331bc1537686c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>341.2MiB (357.7MB) – 3,305,843 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8cd42e639e764b6915b74d34e29681e<br>SHA1: 59487357d7497ea585a66be963038da0bd3d8c79<br>SHA256: 093ad3c5b00a0620dd5ab55a96d31fdbde283e096d5d86611cf2e0af2cb6f688</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-06-27<br>IPv6: 2024-06-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.893MiB (5.131MB) – 244,932 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffde7736a4dce2d1dc8a9bbdbbed74a5<br>SHA1: b43b198dcef1ba6df65e58c1860df753727d07a0<br>SHA256: 8724d93cfde83ae2b1ecc823b3e74fd2991e6b70f24b1547c184c710023795dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.66MiB (18.52MB) – 268,413 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0affbc6694e8124ef8380a96f029473c<br>SHA1: ee3211b937aab5e966a663960fff6c4ebac1172f<br>SHA256: 1ab2b436fcbc1c46882e731a91c9c9ace7151e260ba27191c665827291450dad</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-06-27<br>IPv6: 2024-06-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.2MiB (179.5MB) – 2,966,969 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23fb370ce2d6e35cc080047ec96854e<br>SHA1: 6375dc2f3658701b80ddbbb07172e7979cfd3c60<br>SHA256: d5616074b0d3213fccda295fa79eab456cf538541040ad6d2b330f9b8e18e286</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>192.6MiB (201.9MB) – 1,864,338 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c773064f37ebb2a011fd7af63e5eb82<br>SHA1: 2b1c4e83df9f45b9539528f8dc4a01a661ce71e9<br>SHA256: a4a6a481f67fa24ccffea017ecff51d398b6046177a33e77ad479f97889e8457</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-06-25<br>IPv6: 2024-06-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.853MiB (10.33MB) – 493,563 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6cabdb24ff484ba40de345d930af78d7<br>SHA1: 0a59e72b4f2295d3e4ad5fdda274ca0ecb15050e<br>SHA256: 85933a22833a4eb148fef24dc3f62503765e5b75e4db03f20fc8b8be90e20c8a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.39MiB (20.33MB) – 294,596 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa2c430d7a86d993cfff2789fe89ac2a<br>SHA1: b4e7e88a7a3a8fab2b6d510c005f1f986001aeda<br>SHA256: 94c1b6c1c34bf3c6989503f5d8a0d4b6f376444c2daae555ed97da86fd76b4de</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-06-25<br>IPv6: 2024-06-25 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.4MiB (126.3MB) – 2,412,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d995586f587173a20292b147be10c06<br>SHA1: ab4f7a6a106bd2752f0ccde13bc3af7aaebb3486<br>SHA256: 4e73de636882146bae5ea960beaf5ea5823c3966d4c805f0f96d1c0851761758</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.4MiB (135.7MB) – 2,412,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e3b63846a2e1d34f2c3d1709eba7fc8<br>SHA1: 62a1d3bbd360f658c159cca17fba7628e8d978dc<br>SHA256: 3b19234d25823f76c69f740a4c4673cc04471fe3c3cde129432c32a2b3c1887f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.2MiB (126.0MB) – 2,412,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d59e93fa592433d0b8305d48fedaae2<br>SHA1: d14dc716c5f937ceb7314cdf34997690a7efff55<br>SHA256: 8f0a5b4a3bead0103f03e8fb1dca2013d7835a0feefe5e885172c90b7e921f16</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.7MiB (128.6MB) – 2,412,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3422117e471c813d469f4526966bfdeb<br>SHA1: eef36cf5376247916b72d20742121ec5efd622fd<br>SHA256: 09884b716abd191b835ed3d0a7bc60ebe56c7aacd80f616d494d90a2bb8449b4</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.1MiB (157.4MB) – 2,412,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e91b68c1856443a4bdc84a3b252f20d4<br>SHA1: 00cd7faad8b3767df66fe032e3e2cae8c7a1dd37<br>SHA256: 44f4791451312a30d5281d496a81d477365af25de54c61bc977b4a66f1e827d7</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.4MiB (125.2MB) – 2,412,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a053a411085bf74bc5fc6b7ce3c54df3<br>SHA1: 5696fba57f6a41a9ac40e61541353a494d9fa1c7<br>SHA256: c0e2f691a0aa16e6ac075aff76cc33195f39cfbafb2ba3dfcc4541eb7273de7e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.4MiB (153.6MB) – 2,412,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b2dee67eca5b53c26e27652dae3fb4f<br>SHA1: a93e911f370571c6606f6d4bf7643013ae27ef29<br>SHA256: 59f41b6f386f3fabbda2e1f5ca8eff17dcd10047b07831c09fe66bff680c0bd0</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>122.9MiB (128.9MB) – 2,412,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb8892427623cd8f02d5733996456e95<br>SHA1: 28c71fd28368b66141c69c7058795d06afaca68c<br>SHA256: d99934b6d8d62f4a16672651e8cc3a4e5566fc0e52114643e5fbb610b5a6271d</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>116.5MiB (122.1MB) – 1,253,086 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b85ceb61232731711f9f3059a6809f0e<br>SHA1: 6de98ac4cc8cacb4d0fa038e44396a9f6b597399<br>SHA256: cc665a09abcad487df427d5f40702a1020de574b4df5933a01c8c80daf6ed4fe</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>120.5MiB (126.3MB) – 1,253,086 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cf7b1fa27ef803afa3a941394e1f0d8<br>SHA1: 5e57da8c611c7ea6cc3076de6b4dea8caf931ea0<br>SHA256: 374aa2a60f4fa813a5ecb3a56d58d10862ec9ea5de59a5f99dd8432462b5a822</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>116.8MiB (122.4MB) – 1,253,086 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 601f5e442103c9cb58d689d82a4f8edd<br>SHA1: 88816ab4a7518ab4e3da41fb8aa4f6bbf9fa0bcf<br>SHA256: e12a9af7cdb57a35fb00cf940cc2906539d8ff32ea6c0b63d89c6fe485a52f56</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>117.2MiB (122.9MB) – 1,253,086 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d9f0e1096897c3c2cb801fa3a22ece2<br>SHA1: 17a75565627c4ae214d380ea40ca77cddc520028<br>SHA256: 0da3e6ee5dd5e4edae96465393091fccc201ff5b0775cd4759d7557c99058285</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>128.4MiB (134.6MB) – 1,253,086 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ac8a8b8d30869394c8ab817d933d40b<br>SHA1: 3ad86ab0919fdfed6d794f1ecba022da904ad4f2<br>SHA256: c33632def3a96b5beb7150928bd8c8e45df6d4f573763c113059419ceb1770bc</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>116.3MiB (122.0MB) – 1,253,086 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e90176dead520926aab6272c88fc8f1b<br>SHA1: ad5acf8fdbd060664a2f74605f6c13dc1ee6b673<br>SHA256: ad74d18c083a33a47cbc0d6ae065c6de9f8de67c8d5419ea1f63d1724b21dd6c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>127.6MiB (133.8MB) – 1,253,086 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a8b543916b677439c820cf16f44ef69<br>SHA1: b867f6d83d837856fa883a8a067a441be2887d10<br>SHA256: 17c80910fc9b15bbfa7a036860409de98bf82ad2d73fb86779421e515d0faf34</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>118.3MiB (124.0MB) – 1,253,086 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9d0bd3a4501789236012fe37dcf5f53<br>SHA1: f2bd367fb1382ed56b5adc239f520e9f31445db5<br>SHA256: 308604f4cbf4cabbe524f9ab94d5f618116ce813f55ff0ac3ccfce1801c8e475</pre></details></small> |


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
