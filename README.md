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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-11-26<br>IPv6: 2024-11-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.841MiB (6.125MB) – 292,482 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 389c9a069d4de8bd4ff10393b5629294<br>SHA1: 17f15138c590eef965d1db6e7d370ad3606c0a67<br>SHA256: d1bccdbaa6ca2ae4b81fc8bf241bafbab3448a50c2538652d0b92437702acfbc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.55MiB (12.11MB) – 175,456 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa4d92da742890912e157054b0f99b66<br>SHA1: 3f517efd19c8b9a9df46ef23baac317e0d182955<br>SHA256: deffc452f6aabdcb01a5a02213452f5a990116c9fa3fb81ec7b8a279789f71ef</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-11-26<br>IPv6: 2024-11-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.248MiB (8.648MB) – 413,023 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7b1da3fcb7a0495665d19c6f09753db<br>SHA1: 364b607f0f86cd23ead68a340129c889efc08e13<br>SHA256: bb89852140469246bcf5080e2b6fe7c2363b292f06e0130c44fd0bbc01a19982</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.911MiB (7.247MB) – 105,138 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a67bf7fdd295cffa518ff6104d932046<br>SHA1: 25107c84a02d5a2a4d247d372f1be8765c593750<br>SHA256: 4bba519ce47bf083f8dfe2d3e9f8b0620b279061a1e061cd837e1e3748652967</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-11-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.25MiB (18.09MB) – 863,063 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d455051f91ff4224ef22868d1b5a3c7b<br>SHA1: f8705d4366a05753b42b6a89744fe72393fbe879<br>SHA256: 2690d648587abe1f62cf7783cb19ac67c7c1dd82d067e0b3a2349208f8e1eac4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>79.85MiB (83.73MB) – 1,213,526 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c73e90f74bc0d25ac13a82ffbb4e19a<br>SHA1: cf387b661edadd31c9fd7210cd738cfa5453c1a1<br>SHA256: acdf669cfe0b8cd37a535f4d709be8ad541559728521c9466c004004ad21b3f9</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.056MiB (7.399MB) – 354,248 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d0746f47a1225271996460705211255<br>SHA1: a42a4bf19e2ebf577c82e10d3834e8df68696682<br>SHA256: 436aea2efe6e1523eea5e9ba484e5efba050d65a52ade285c3f9c0212c5ed301</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.43MiB (17.22MB) – 249,619 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efdc8aeb0b5fac8527fcc97613b42d4a<br>SHA1: 05d5c2e0b0a85115285dfae791b3139e2b9eab7f<br>SHA256: 45657f0c603e4d28c566dd5f9da450499802a059e8c1ff77082c945045a71fa7</pre></details></small> |
| | | Full Location | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.2MiB (199.4MB) – 3,323,413 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e766d2e8e0a2969d4ff92cf52388660e<br>SHA1: 38d95ed8fc01158d0f5ec9aa8f3bb385ef86d3d9<br>SHA256: 7656a9190b90023870afbde735c05ae68168d21190941a5da2be92e18c8b89a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>369.3MiB (387.2MB) – 3,583,553 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23856f8e31b066ac2b1f256c563a9300<br>SHA1: 4ffab13a7c3069f5a314ea0ee72c222a02103120<br>SHA256: 9d6307032c82257b206c839119decab677631aaf7e5d3138ed4b92f8cf07acc1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-11-26<br>IPv6: 2024-11-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.926MiB (5.165MB) – 246,523 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b65d4763afb899ebad44d8601c4a4990<br>SHA1: 8bd20289ad5b22362c490ef2ad87bb040144c58e<br>SHA256: f7aebea3b623de1bee2349bcc7ee3f82183617838781052edfcba6d52b007268</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.04MB) – 275,881 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f11ddd1e6ba253a1dcb084442e38371<br>SHA1: daa137a952d33b33ca13482857f06e22c04e4de3<br>SHA256: 3c06071a088143b211f2daf1ee846920b62170ed33e0bcfb866ca24d62f88932</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-11-26<br>IPv6: 2024-11-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,018,795 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8a4e6340df7e6348b98025cba6c876a<br>SHA1: f5e6d82e8c5aa0282f73a857b7aa0817b689bdb1<br>SHA256: 42764697d53f138d6988d09099fd34cd0215bdc2ae86ce1f0ef8181c4a0bf79e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>222.0MiB (232.7MB) – 2,147,643 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a3ad0ce3e97d8698462c6efbd0b983<br>SHA1: 39b2430a2a62e400d659a0218fda59402e4382ee<br>SHA256: 979307d692a1cc91c6c103a0f51cdf68654c3ff286af4df15fe284354e67234f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-11-22<br>IPv6: 2024-11-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.05MiB (10.54MB) – 503,400 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a285ba76fbb19be24dfc88af66fa99d8<br>SHA1: 63baae19dc512f539f93bd400aac89bba1ac8b6a<br>SHA256: 10549c3a4b2f0a7940af85874d13942ffacda33e53d462e6b633458fbdc3b6fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.24MiB (33.81MB) – 489,941 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4491899bc3fcfacd9047097896d5fa8f<br>SHA1: cd7f67b93877b0c6a3ca5692e6eeb900e90a7ca3<br>SHA256: e6d7579c5930412a7735051f86c2259217f5d362636a1d489db8d64e02dfa843</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-11-22<br>IPv6: 2024-11-22 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>164.5MiB (172.4MB) – 3,247,515 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b97bdd6e7138291f64168713a240a28f<br>SHA1: 85c57ee7a132a80a699ba8181afd5b4e2ec17274<br>SHA256: a276d41161ee402a1aff647f25cb8702c7e1717aedb102a786180933c77e1982</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>175.1MiB (183.6MB) – 3,247,515 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbc518df8980dcd0012b08db61b3945b<br>SHA1: 041658ccdfa6683035a78c0d7c8c44c94f025f6a<br>SHA256: 36cf8ca1fde53537487395ef3b96b7a26ac82a59485f6131f959a0f148b8f473</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.4MiB (171.3MB) – 3,247,515 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22a0bd15d57896e59ee6d82b243fca2a<br>SHA1: cacd63c2c1095a60dcb8152663bb27d01d34c259<br>SHA256: abd952cddeebbd3f3b22cd81494918ab595db45491177ac2c7f1d5c9a61a2ec2</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>165.8MiB (173.9MB) – 3,247,515 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 016f5819fa8d9ce4ca002a97a047f142<br>SHA1: 63ee2741e44c4ed8bbbf744dc555a914302a9205<br>SHA256: bd10170c45f09fe6058c3ddf2c0d19e6df17547ae13f849da0fc39b4024b262d</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>208.5MiB (218.7MB) – 3,247,515 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53b1763d844f1a3767da465fc28da684<br>SHA1: 3dd5123816336268c1c1bf6067a9e5829e4373ae<br>SHA256: e3ebc9245d83b779a74b3c22e6a352b613e61b404fd44ce8f8d5979537324fc6</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>163.4MiB (171.4MB) – 3,247,515 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e2e4e93eb09d8f88729745ee83ec405<br>SHA1: 0db97fca4a36522bfd32269ec285c9899efbc812<br>SHA256: b3416cee90b95a13cd72d70f1025d60b11ddf54ea50c8222cc305e221bf9a0c9</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>202.6MiB (212.4MB) – 3,247,515 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 228c25ec6f8acfb845bc6ff6921d3824<br>SHA1: c5c5f3c5eaa12207faec9e537f64b405abcefd13<br>SHA256: 5bc8c5453033640da39affb60553819c38576a0186c62bd5e58c4f267228af83</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.5MiB (178.8MB) – 3,247,515 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1e6e5a9a58a2350859bee656b86b55e<br>SHA1: 53e4dbec45411f6a8cbbcdcd1cb9c6bae832bfdc<br>SHA256: 1e465fa99f982284e1ddbec4cffff12745ff7885e68e78525a87316abbb7326c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>156.9MiB (164.6MB) – 1,677,169 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a8019866d675470db2be4efa027cc57<br>SHA1: 5a3d8b6996472c0dbd807f0dc0c5c950a58bd220<br>SHA256: 414220fa7d8183e63964b71a3baa973e8f004c17e9f1c1300357597f991d9b9c</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>160.2MiB (168.0MB) – 1,677,169 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67bba57d4893acdf81d1913a5e0140df<br>SHA1: 669eee845cc3d982c8a43134ca607e9a308269fc<br>SHA256: d2e7775943e776df77a469e284b0fa62de20484d4418b1a8fc341714458a062f</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.1MiB (162.7MB) – 1,677,169 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd65a14b02d2faf4538dad9ce80e5146<br>SHA1: c585153ceb3d326b9130214522c76587c7612c0f<br>SHA256: 87bacfb4da09925ced2a9097f4b5b0af1ae98c617e4cd290e662156322399e6c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>155.4MiB (163.0MB) – 1,677,169 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45d4bcc8a87e808e9569c015694139fe<br>SHA1: 848eaedce43447a54a6b68404cae8ebbd9d8731c<br>SHA256: 30005950ea078e133ca9665bddd44decc62c49c53251c1884a4f2e51ef243aaa</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>170.3MiB (178.6MB) – 1,677,169 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a3b7382cf8e8743403527478762195b<br>SHA1: ebf9ffbb930541f89b4729147716bdc297190d4d<br>SHA256: 4743b3bfddb4fc7d857d4ae3a11080e2e67bd0c3dcd95dfc51bdcc71505e2555</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>154.9MiB (162.5MB) – 1,677,169 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c5642c144a8eb71eb2f41da9d6b2939<br>SHA1: be9bc20a80ef4fc05dc4276c2cca3230957a5662<br>SHA256: 14ae8852c70d146d0ec07662d63d23fa9cb4cddf53055654a8108de052e3076d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>171.7MiB (180.1MB) – 1,677,169 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3bdae9821c04ded703fe88061a1c677a<br>SHA1: e5c2c2a35d2eb12a7942cce43f798aa9da35b2b0<br>SHA256: 75aa61ad7dcd6d4147875bdff703c81eb73eb087eeddccfc9812e172db7e38c8</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>158.3MiB (166.0MB) – 1,677,169 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a80adf557a1ed83c13886cd3eee7d66<br>SHA1: 32eba80d4fcf3b78e033e615491969ce176e0a05<br>SHA256: 7b16414a04eea0fa3d297ba519699866650b1acedce9993eb037c01ba5b79af8</pre></details></small> |


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
