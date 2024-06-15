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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-06-15<br>IPv6: 2024-06-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.735MiB (4.965MB) – 237,038 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9ba30de5b1b335f84e9f0ad78f968ae<br>SHA1: b973d2ba1248063b78c6245903d2f8ffc91d5abb<br>SHA256: f168add5fcf9f1fadc92340195100e6c2c0b3c57e07dbcd65e8ae502620c588d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.469MiB (6.784MB) – 98,315 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ac5220149d6bcd023ec64db3dacc723<br>SHA1: d6c11c04c7433a251effebd48e22ac6941481af4<br>SHA256: 4eb3d5a03955c68933943776d1d67ca8e041e335e4a715a8646383324ee0f639</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-06-15<br>IPv6: 2024-06-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.108MiB (8.502MB) – 406,065 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b27b9e6e2be614a23f3e54d1f4af9792<br>SHA1: bf4ad32841febc2e8011c93894a193d4af6c32d9<br>SHA256: a16dd690956771b7d034d3e77e4ced4a58a556362765c81456b6197f81f790c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.403MiB (6.714MB) – 97,420 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33d949b7fa4b8ae198b95761ea891741<br>SHA1: 0af78677bf307fdd59c0d834e3a8dfc883cfda21<br>SHA256: ac930ce2f4d0f143c12defcf7735882e0ac77064e10c4045196b15836e489532</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-06-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.94MiB (18.81MB) – 897,731 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15d8574fb9b8094f4d181bab57da07f5<br>SHA1: 8a4ea395536a34ee04f46fb98de32682429e8ecf<br>SHA256: 9a09c58e730a07b25b33ffeb71831392a1bfc3d6f616014db194c6c5ff23364b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>76.01MiB (79.70MB) – 1,155,125 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc6f445afc20fb361b0c68cd2c352b20<br>SHA1: 8698124f5395536e9b266f85b4704dceb8287956<br>SHA256: 7cffa8301a876a1158f216a89f9c905a8c0a3d2d21b11645bde8be70a06d5283</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.920MiB (7.257MB) – 347,790 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228d49dd4c10c1d4778473109614f06<br>SHA1: 84aeb9072586fe27e7a2fd0cdc62b4421b417010<br>SHA256: becc801a5b95a0c7e6dea789881460b3cce70a60f8b941077db5db9f24f332a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.87MiB (16.64MB) – 241,164 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77063c075f456a1e11f7a52af24ac9ce<br>SHA1: c787ab002266a3398026d5342c963fd1ea59f3b4<br>SHA256: 72503d5df7ba2b39c61d7f574dd167649fdff103e81019ba98b18c192a045f0b</pre></details></small> |
| | | Full Location | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.7MiB (195.7MB) – 3,261,621 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d700e342b096e0b5285fb98e7ea719e<br>SHA1: 95986a4433c4d6be7ba8f0d38d9ac62adeb2d962<br>SHA256: 48ea78edb396cd5b834f2a55d80909bfe196c2ba8756c47776a331bc1537686c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>341.2MiB (357.7MB) – 3,305,843 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8cd42e639e764b6915b74d34e29681e<br>SHA1: 59487357d7497ea585a66be963038da0bd3d8c79<br>SHA256: 093ad3c5b00a0620dd5ab55a96d31fdbde283e096d5d86611cf2e0af2cb6f688</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-06-15<br>IPv6: 2024-06-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.893MiB (5.131MB) – 244,932 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffde7736a4dce2d1dc8a9bbdbbed74a5<br>SHA1: b43b198dcef1ba6df65e58c1860df753727d07a0<br>SHA256: 8724d93cfde83ae2b1ecc823b3e74fd2991e6b70f24b1547c184c710023795dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.66MiB (18.52MB) – 268,413 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0affbc6694e8124ef8380a96f029473c<br>SHA1: ee3211b937aab5e966a663960fff6c4ebac1172f<br>SHA256: 1ab2b436fcbc1c46882e731a91c9c9ace7151e260ba27191c665827291450dad</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-06-15<br>IPv6: 2024-06-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.2MiB (179.5MB) – 2,966,969 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23fb370ce2d6e35cc080047ec96854e<br>SHA1: 6375dc2f3658701b80ddbbb07172e7979cfd3c60<br>SHA256: d5616074b0d3213fccda295fa79eab456cf538541040ad6d2b330f9b8e18e286</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>192.6MiB (201.9MB) – 1,864,338 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c773064f37ebb2a011fd7af63e5eb82<br>SHA1: 2b1c4e83df9f45b9539528f8dc4a01a661ce71e9<br>SHA256: a4a6a481f67fa24ccffea017ecff51d398b6046177a33e77ad479f97889e8457</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-06-14<br>IPv6: 2024-06-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.806MiB (10.28MB) – 491,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85261d7eb73577555180f85bb0f90ccf<br>SHA1: 1f723d4e242b5570ebd02447fa857cdeb6de102f<br>SHA256: d07195cbbdd95496d3c0774a2ad592f0694a37638046269fccab9f000079584e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.28MiB (20.21MB) – 292,945 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81b4fe7d80a1ed44cb8005b1177affd2<br>SHA1: f05a361b0da689f2c5bb3581da2df01bde706296<br>SHA256: d0875284a496f2ad089ff5ff7bfd01260ef56dff5d8a555242888835e7f5ce3b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-06-14<br>IPv6: 2024-06-14 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>119.5MiB (125.4MB) – 2,391,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0aa817aecea7dc51f6a53629a74f8e6e<br>SHA1: cdbd074627bef562ab225c3c2cb9da94b23eee30<br>SHA256: 32a565a62ebbc8951c5183dd529a0f3507c4db7f593712cec4bb84f13768af96</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>128.5MiB (134.7MB) – 2,391,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e5b508016167678554844d85c4e83ba<br>SHA1: 927daecd1d30b0322b0d014f0e1f578e864f7008<br>SHA256: 7485f4ee202e041f69f76ace8a0ee940a6de5a952b8690122fb22eea94e4afea</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>119.3MiB (125.1MB) – 2,391,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 481c45c2bb61ccff434305537314360b<br>SHA1: a119d4542a6bee77eac17dde7d952d5538e80779<br>SHA256: 3b16547737cd2bd9d61973e93ddbfc76637c18d605590ab1d8a649af0da50dd7</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>121.8MiB (127.7MB) – 2,391,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 632d6d2ebbb01c556ae58a9bf5370744<br>SHA1: 0f880de5d6eb7e8c0a75e5e401ccfa46c7ff3ea5<br>SHA256: 3729f40beee2330a101df1169539ee7d61f641e1b52cdc03f013132739a60c37</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>149.1MiB (156.4MB) – 2,391,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3d3bef13028ffe85cc9c082c93393c7<br>SHA1: bba93832ad5c187f16bafc00c055eb81542f5a79<br>SHA256: bbae0179cefb944708dba70b2e07a4901b100f87158ca64bec2020d8d838ed2f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>118.6MiB (124.3MB) – 2,391,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03b8964bf874291cb675583338c417fd<br>SHA1: 8694fb466b48b1aeeadcbb7c5e3058c610a084f8<br>SHA256: 45cab1df2aad6e73ed55f6296c082a213d6379352e9368ac91ad6581405091e4</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>145.5MiB (152.5MB) – 2,391,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0b778bd4628deed4a0b37112d2c838c<br>SHA1: abea1afdf354bb1e914b01d27335f8ff0b45d549<br>SHA256: c891cf54d8a0f4e292b3f30bcf86f8ef6558369d71c5b736745e347142d49fab</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>122.0MiB (127.9MB) – 2,391,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2bcd5ddf6dddc8223ffd5980105e181<br>SHA1: 09453b06511d9f820f15cbf5a8d16e6af047f168<br>SHA256: 580626665aa06c017e0aa78c433be275f987fd934771e16e9e73ece843945984</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>115.9MiB (121.6MB) – 1,247,237 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de813e660ad9e6175a39a32b5a8deeac<br>SHA1: d9b50073c01d0d466cbb01645ca24246b7f25b4f<br>SHA256: 99e46c26be2cabe5c79dd9ce12651cf1146ce4b0de01175ade3f77f981eaf607</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>119.9MiB (125.8MB) – 1,247,237 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c990e692c55c77da086423d56121eaea<br>SHA1: 0740c0140bf78a85dbdb0df0394a716f8473558d<br>SHA256: e4ab141d55c26bf967be22a7085e428935b4a07b6960630dc8cf21874fb63eee</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>116.2MiB (121.9MB) – 1,247,237 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26e8340966128def03edc5963587b6c6<br>SHA1: dde901945ec13b8875087dcccfe5870744aca369<br>SHA256: 684a371dd9c3b1fe656436d3270ee6c89e27528cae6c395d8d285cd3a58962b4</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>116.6MiB (122.3MB) – 1,247,237 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 399e403de388fea274ec4cf30c8c671b<br>SHA1: e4033c487fd49db434c869bd5e4d7b538f17e4c6<br>SHA256: 239680ad1ca3fa3f1ea8e9cedf15d2d9c2de6cb08dbdc9f5fcf55b7cf77a7e2e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>127.8MiB (134.0MB) – 1,247,237 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b10919d61299f846b20b054204815a3<br>SHA1: 0f6c2f91e1c6034f9af438d08b5a9a81dcfd6b95<br>SHA256: 452adffe97459f02c36eb14df1b8c4c34cb93f7f06b9bb36cff0282e7f659e35</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>115.8MiB (121.4MB) – 1,247,237 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8ec80a6323ef8390b3e614ac994767f<br>SHA1: d89accd9969ac1a02087745aff9de111f9079b24<br>SHA256: efa6a74d7e1987e71e0780510653549fb3582aec59564fd40cfde4cb27331c31</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>127.0MiB (133.2MB) – 1,247,237 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f6f0ae26e50efabb3468f89f2db806e<br>SHA1: 4814ae546c28aebe1e6ee75d3a4e62f7d9c78362<br>SHA256: 72ed5b74505aa014795044c2de392ed2d81cadd240e289f9d26f37ffe59dc49d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>117.8MiB (123.5MB) – 1,247,237 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46062a5c4587bf334841ad6b14cd67b3<br>SHA1: 3156b56750d19a32ccff2905730fc6cfc70e7dd1<br>SHA256: 9bd9738c304c5da50c9e2c9ddf82c5cc47489957c0297ba9d42b0e01d2906666</pre></details></small> |


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
