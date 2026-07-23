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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-07-22<br>IPv6: 2026-07-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.420 MiB (5.683 MB) – 271,250 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9a9961af3100f32462a5081dca463ab<br>SHA1: dd4228615f165eace3f31a584c5325c17dbb41e1<br>SHA256: fda8be733b3b8cc04e8fe29ba3ad6e8f00854c56e982998cfef334c008ed8f10</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.81 MiB (17.62 MB) – 255,388 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29b151c8792272378422aa9bca8b3da2<br>SHA1: 17daf7ced95fe59e46057de93d90b556d61a1e7b<br>SHA256: 7d0cb8be2e8dd0d1ec2d0ed3dc66d12b14891b8690e354c2d5439772972ac489</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-07-23<br>IPv6: 2026-07-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.025 MiB (9.463 MB) – 451,871 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 850495f0d36c0645abaa9a517a66d41f<br>SHA1: 6343afc7e13468128fcf7c39622ec3384246442c<br>SHA256: 78a22b4679ab3d7bdd1ce30204e9a21c69f990404fc04514e208d8fd1152163a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.947 MiB (8.333 MB) – 120,888 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bddaff787a19f83461dc4d2d91dc8b46<br>SHA1: 3ccf4f3ca385a0d167398013015a2a1e361a1e7b<br>SHA256: 99a44c7e4f5a0f9877ecdb832647fce2370d89f1f420bd53bbf0d7c3eceafa20</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-07-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.12 MiB (12.71 MB) – 606,813 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a927bc864e4a5e914496a26826952afa<br>SHA1: 715be0b4e3a18126a7cb04234d07760ffef7683f<br>SHA256: b1245e449b0064de5394f5a948530e52c56b270d1b1cd73e844dacc4f3f7a810</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>42.19 MiB (44.24 MB) – 641,148 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 963b394c9228f727faa2f409dd964fef<br>SHA1: d51f105b26a3c4a5f3b377e429707970ae12929c<br>SHA256: a0e7038804c1b6f04c821b18941af0fbfd5c3087a4cfaf33b39067bb13b37e4f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.078 MiB (7.422 MB) – 354,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ec835290735187164b1f2f622ad9c0<br>SHA1: 10464ef5eb489f4745096b1c71046b06409244b5<br>SHA256: 6bc4af63c1e15b4d99d5b9dd9cddeb67bbf2eafc2529ba5d9ec4525e0fe7964c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.51 MiB (23.60 MB) – 342,046 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569d0c6b66a745289f0e152318090f38<br>SHA1: baf1ef75355d41d9bc4380f97ed3b085db479655<br>SHA256: 8940a06c7f9a27f129048c5a7a0b1579b368020d88f2d2efe0fc813b6d2f97e4</pre></details></small> |
| | | Full Location | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.3 MiB (219.4 MB) – 3,666,805 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b729ab459cc2b765b3b4ea035f481b<br>SHA1: 1496af12b72ee784e304cd84eb7335c826bc3906<br>SHA256: 69fc5ebf5414a7a939fc25a35f3128451cf340211ae51ab9f82d53a331d8ca03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.3 MiB (473.3 MB) – 4,386,528 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f197b2ebcfed77f9adc3310fc7b6020<br>SHA1: 24b1454a40fdda39f37fa9367a6a6a5a88d3be33<br>SHA256: 0160ad6b5bca3517eb65f79d6db1f9e373eeb34cfccbf189a588bb330d17af06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.670 MiB (5.946 MB) – 283,812 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96cb0452e66db1c3a35242fa031ebe0f<br>SHA1: 28fae5a412332f0cedc711132a0dd6f337488ec4<br>SHA256: 2785f482dbf1f2dcb1bd3a9f253c708b1fa5f86773908ef7a2f2bb16c0dd1ff4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.24 MiB (23.32 MB) – 337,921 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1683effffd067b4fddf82095f002903<br>SHA1: 82f6a3b239649f9e8af05d58b628eeed874ad7cd<br>SHA256: a51cfe2b60d111ec234510abdd73583f12186f7fc35e3decd80fd4ef4b5ea654</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1 MiB (178.4 MB) – 2,944,788 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52717d3cc345c65ab5cb86167d9b2112<br>SHA1: 0ad1bd8bf0bdf711f51a9a37bb75090cbf4ffc84<br>SHA256: c92293057f12c2c364411c35a02de2cb229e7a21791a1bfd25cab2ba6beac1cc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>298.9 MiB (313.4 MB) – 2,896,639 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23b3d9e4addd1683ed707d17a98a0e22<br>SHA1: 572b0633e6453018a04db4c06504726ffcbeadba<br>SHA256: ba14acc8e2fc9ac380640ba99de27ab073d603598996f6737853e5a1ca4a8a13</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-07-21<br>IPv6: 2026-07-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.23 MiB (11.78 MB) – 562,349 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54eb4fe6dfa661b9e580880f0f06ef6a<br>SHA1: 119284d3ed1bca0dcfe60b9c4623aa6da1af0000<br>SHA256: 47a412e8fd41dee037cf2897523fbf75f7f8799598282e332d8e24333c45e840</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>36.44 MiB (38.21 MB) – 553,708 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 159b5543d7f166a77004c11518feecee<br>SHA1: 9d4271e557195efa33ee5f92f60ae642b087efb1<br>SHA256: fab3c78d29b6eb32feb8095d28019675f464dc96ee3bba527e493a79df752352</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-07-21<br>IPv6: 2026-07-21 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>193.7 MiB (203.1 MB) – 3,770,527 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c0c1706d93601a2ba11dff3e47599e7<br>SHA1: 2c8d9bdd9566af59bde399d9ec23ef4fccc67307<br>SHA256: e46a6e91e7dc0becf059d9c7307ea59e88baf783f2a33b2de8b9269a402000c3</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>202.7 MiB (212.6 MB) – 3,770,527 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae4ffd292f694d8b2c48e09c42a8d26d<br>SHA1: 915363f42fa16f4ae8893bc8801e7e60eda7880e<br>SHA256: 84fe329c4b3c83888c6e684732dc12d55de287feec8abdc890c726eb702e6682</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>192.9 MiB (202.2 MB) – 3,770,527 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52381f94068e098a79527fb8feb55584<br>SHA1: fc0512c58a5383fb108a3aa440a01dea00149b41<br>SHA256: b3afc64197d5b4467d43019f5d389b38d9446887ce9e25eaeb77dfa83de13324</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>194.6 MiB (204.1 MB) – 3,770,527 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 297e59d0a44c8c3ef9058fb241e8c711<br>SHA1: 1161df9b4af95ba1554a37487278662b6992514d<br>SHA256: ed9532fce5ec05e8aa19babb9823fbfc4cb4c1ab33a64c8a071399273fcf5e46</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>245.3 MiB (257.2 MB) – 3,770,527 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58879c07d4237b45e5f0d6f0cf50fb9a<br>SHA1: fabfc27e7302b775cd10b2801cc375d3238033e8<br>SHA256: fd6ae20900be0fddf63db265c53e2665e6b070e47353ce21519513a5498b03c5</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>192.1 MiB (201.4 MB) – 3,770,527 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ae31b4b9371eabc0f495ff51af1bffb<br>SHA1: 990f93a48d00f1d2419a0e4794dd374c4194d059<br>SHA256: 7a70997dc443268a619203bfb6bfd64e5a683c2eb73acc4308533c72abac00f1</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.2 MiB (246.6 MB) – 3,770,527 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ece62934f4909c42029f08941b137a01<br>SHA1: 20926d1ba891d84f630890ff84127d03e8e7cc69<br>SHA256: 8466287f10aa80cb1e31b2123b1f9a6315b9e646a0f3ae1c976343f74863002a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>197.9 MiB (207.5 MB) – 3,770,527 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5a7a1ed28b5ddfb68c39706ccd34835<br>SHA1: 429b767c190d4ada831d3d7686128ffdef3c540e<br>SHA256: efb3331c1612946cfef1b096c5d92cb7d9b5b712e38186984fa153252f38582a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>198.7 MiB (208.3 MB) – 2,082,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9371a84e6902e80cbc96485ebf3d9f78<br>SHA1: bb50bafcae4238270cd0a99abf488d84f343de27<br>SHA256: c438657e72cf8febc465b8649f864c2173bf7115569c384b2809032d26cc42c4</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>201.9 MiB (211.7 MB) – 2,082,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5baef3d13644c8f6ca7d04842ba6d85b<br>SHA1: f75602228b22cea218f438e53e12fb0d76261215<br>SHA256: 44a2bc856526d84ac5c65b2bd4e688d82db6a24ee6c8d7377ec26bc58215982f</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.1 MiB (205.6 MB) – 2,082,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4bdfcacf032eddcf4f3f5b73cd1286c4<br>SHA1: 16e5902a8b90a52aab63186e12a5167e3590d6e1<br>SHA256: cf4c366e2f935ed794ca32cbef2f1807e2296428dd9926ad0ab7a03af3c68226</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.6 MiB (206.2 MB) – 2,082,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcc3bb63aac01977f2549f01a9a3997f<br>SHA1: b66f25f22e2882182d42cc03c2fefcc0a35aba08<br>SHA256: 13170ee79c83f343553d00090eaf888cc64345f114ecfb4aa61484233caf7e8f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>218.8 MiB (229.4 MB) – 2,082,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd2ed55c1cf7f9467ea96ae3531b67b1<br>SHA1: 80e36bfc91041aa8f2e0e6948717387356d12357<br>SHA256: cb4e6dc787a05164e1f75307aaf6794daa02d8c3efe37474c9813d39fbc6cb4c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>195.9 MiB (205.4 MB) – 2,082,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3232fede00417ef37d7cdf5c48c4cf27<br>SHA1: e51f3b41172ea3f86fed63e37f4771680f690b0e<br>SHA256: 40b838aee507f0c130c2f6ea1eb949df247e87292eb6a0603cc75031989674c1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>217.3 MiB (227.9 MB) – 2,082,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b649c68107f6d7b5db49bb540350143<br>SHA1: 307f560ec414ffa1d964618b8648217a32713de4<br>SHA256: 74851a4b91e857bbcc8747ffad476c4239275d3179ab818fa26c25b11bd53fc1</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>198.8 MiB (208.4 MB) – 2,082,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6375e8b75b832ab057fb7d8e50ad4546<br>SHA1: 0cd302f06c0f4aee9e143465363242cc28d709b5<br>SHA256: 53a0aae69a960eeccc256a7aa406fe5d76ec99073403595618f6bf941683a185</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
