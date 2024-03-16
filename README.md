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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-03-16<br>IPv6: 2024-03-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.813MiB (5.046MB) – 240,935 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e46bb966c8ab570fd6a0d5cffd158f2<br>SHA1: 5d4289105eca0acad87d050859754e061fd198e5<br>SHA256: c7b74d8f28f320d41fafca1efcbc864abb65372a855a0f335ff86ef8d57de06f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.033MiB (6.326MB) – 91,688 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc7880ba51e0184bdcd37713fb80f4e2<br>SHA1: 375d98b062e39ab1cf04fd4df7fc29b6c0ac8d89<br>SHA256: c66c3d8ebdc2a2de730a1f53116809bbc0935f4ff82ca501296490e96c51e011</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-03-16<br>IPv6: 2024-03-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.208MiB (8.607MB) – 411,054 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c5c8847372786146015367f49280814<br>SHA1: 963b9f64712ae32a097b60467a6fde578f6a27c9<br>SHA256: 0444dba4aa2f69901c5c221640ded1131d29affe79bb02e00f7e2f9ee6781a8d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.090MiB (7.435MB) – 107,864 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0c8e97d8005f3e2d6f9983bb395d955<br>SHA1: 5dc7167ca38a1c3c6fc81a1b1effb79fe67b424a<br>SHA256: 932d6bcaa6ce954e809531b6ccf411f4ec719612c363c1c84055fb07fe730a9b</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-03-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.62MiB (18.47MB) – 881,930 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7644b024b1bd543e68d37200cfa4cd0<br>SHA1: a3c1579a4a427af3049f019805096a01d3b5e984<br>SHA256: a8cec31b092702c1fbbda7b5a1ca9635d8cd6e77eb457974090db146ceff2108</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.14MiB (77.75MB) – 1,126,761 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4e565722128ddfd424d0978cf2a0ad3<br>SHA1: dcd4a3941b8a2470bef0202bd6f8f561a625756a<br>SHA256: 143f293755ced2bf18fffcb37f413a5f536667b60b57d806f537ab4662203051</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 322,326 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b232d78e18dacf266bba37244688a18f<br>SHA1: 2ea0bf2a68630d5c12c6fa1d18f2f3eb0845f297<br>SHA256: b9f2935f135d22119e5db5d8d8666980b07ac2e36359fd6dbdc9c26a8b3be2f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.03MB) – 275,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49241985f6153f5f100b60421257f25<br>SHA1: 51e0348aaa544a9b75aa17c9431f3745175c5c5f<br>SHA256: 3420806d6067a2579fe3eef92e4cd09b9b792cce9c418a3ca7f3c820f4edb887</pre></details></small> |
| | | Full Location | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,158,494 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd92465491c42b3844af48593793b1d0<br>SHA1: 53a3bac0d03e0e4bef95ad11b21c1a1e92eed9f8<br>SHA256: 6157eb8d8b93b5da65533893b6b1af8682e371476cd754957d56f3cfd1179aad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>307.8MiB (322.7MB) – 2,989,351 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a432fad1dde6398b8b6ee222abf32676<br>SHA1: 78d2ec063fa05a95bb17703a5111864cd91a5446<br>SHA256: 5974cc41b3872ea8fe373def59322db31b678ff8585a6e529b9737d648343c0d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-03-16<br>IPv6: 2024-03-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.826MiB (5.061MB) – 241,587 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53358947a90b798856b0f2491fbc6d2c<br>SHA1: 7c9c0c0ee1f075fe6d82ea2f7ca31f00a5b7ad18<br>SHA256: bf9da0021f243ed534ef8e2352a5fee71207c3b880a727cd5031b79c5c122185</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>16.63MiB (17.44MB) – 252,757 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05df7acc3edcfc49d6d0cc8e5b23185d<br>SHA1: de417cfa98cd08340a971a226b8075d8887c08b6<br>SHA256: e2904c3019400cf283bda389c8d7dc9f8c0b5dabc1bfd9dc40ea4326c79f404f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-03-16<br>IPv6: 2024-03-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.8MiB (179.1MB) – 2,959,758 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d837249426a59f38d52d9939db4c1a1e<br>SHA1: c71a37a88777bcc232ed0cec8b11f4b0b93ba955<br>SHA256: c25d6cf67e34fdd6f9b5042bffd4059449b156fc6b7bb6e3fd49ce1979642175</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>169.7MiB (178.0MB) – 1,642,006 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e91d25d35aa21837cbe8c01e725e1cb8<br>SHA1: b3aecd7e3f4493788fdc4c941a22f3f071cd5130<br>SHA256: fe72238b338f395cd55c98381ca41ebddfc893eb2bd92625551b9fe4d8d96a53</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-03-12<br>IPv6: 2024-03-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.584MiB (10.05MB) – 480,112 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ae932e4c7d909c0b0d331e33fdcea96<br>SHA1: 20736b48476f7b95a5503536ac72875d07f91cb3<br>SHA256: 26a87632fe19ea16cc695e5df04b7914563405704e9ee40432fcf797e2b40734</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.00MiB (19.92MB) – 288,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8081bf9032dc946b1b8ac60fc04e7e75<br>SHA1: 2e56b1c07b0afeacae7e3f11289710985a583ffe<br>SHA256: e79e6b638ecc0cb8b1035a66008608a59ad7e10543a92608faa375b8bbedf401</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-03-15<br>IPv6: 2024-03-15 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>134.7MiB (141.2MB) – 2,875,930 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30ca9d7e949f070a62700284b990303a<br>SHA1: 982b3b81b0f6b1f58f11a6b03298af8f62fe0a63<br>SHA256: c78d7b6ef0aa5cfc41fe51211fdba4f5f7e3383aed0dbab11224db7350e2cf0e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>156.1MiB (163.6MB) – 2,875,930 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ded3d435e1db500cdc338f996a6301c<br>SHA1: 6fccaa9f98da472d9ae308fcc45c8d567fff1ccd<br>SHA256: 369e9bc2dd84ff613eebfa854cc4e5f08f325385f7b25d4f2f387afc19e2e15b</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>138.4MiB (145.2MB) – 2,875,930 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1744afbeb4be92e46fd6503ff772da89<br>SHA1: efd9914a8cd342c135c65e1227db9c3a5ee462ad<br>SHA256: f18d35ee79b5285daed5b6af8fb9f35e4b13dfeb8c630a9ec20a629e1e34c584</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>143.6MiB (150.6MB) – 2,875,930 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55d6584a80571e640bc9651e8961d185<br>SHA1: e5aea449fab2ab3dec7a142d107876c9cbd26e97<br>SHA256: 4cdcdef6b636db2cd4c50edabceec9846f1d7a83d8cd6765cb11c38662ba706b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>168.0MiB (176.1MB) – 2,875,930 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46a8d0882628d3ecf5891ce2a1533369<br>SHA1: cce16b98c44460edac2e3f6b3d6666c80cd32142<br>SHA256: 03dad929e5361939e474c9e999c3361749b6a11eb028ac69d63b83c5b17dcdfb</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>134.3MiB (140.8MB) – 2,875,930 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609c29796d29597b413fdd818c581941<br>SHA1: 958c9c24d5c20882e95e83673509c4eff74bd92c<br>SHA256: 49be470c27b742bc3f3ab3a88613211b1c77b51d0a3a6a056c987a8a8fe3729c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>167.4MiB (175.5MB) – 2,875,930 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c435559c33d6524b90a60bcbc9937af9<br>SHA1: f387090f3922b3e508ace1101e1ec41ceaaa80a4<br>SHA256: 142d3b1ea7c232c3fa29effeae902c22680af3ac9e7802bc65b123f0d8830f6b</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>141.5MiB (148.4MB) – 2,875,930 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c3c5ec6438fed2914f4f1dd481669a4<br>SHA1: 7b73aef2f3017ee5fc0c279c105e65f7d373bcac<br>SHA256: b7b50c4ea46b2fecc0fa67e68b9265c6a37544b957dd2e98851fd47719257738</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>108.7MiB (113.9MB) – 1,212,287 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca3347045034719376a457de5cf3efb4<br>SHA1: 5b11bd6c7a61aeae9c9ed80b5778c4954f8e26d0<br>SHA256: c9e2fac2d0ea633c1a5b2e3b3c84d7f6b07c340edf40c39e0ec124e6a37b1161</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>116.5MiB (122.2MB) – 1,212,287 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46656541b92aa34de5bef2b35d3a6cc2<br>SHA1: 91aa6dc8e1b1e2a382e8e48a21e9393db22fb3a9<br>SHA256: 81408a769e7cbf4008db37c0afd3cc095d798c497da211394bed20ea635e9886</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>110.9MiB (116.3MB) – 1,212,287 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e31fc910afc6ddb01032518bb74a7417<br>SHA1: 26c345d41f3b2cfd9daff828c839e7a3d4758187<br>SHA256: cf9b337d32da3e4a4dd497a05836e705be95f5fda4011e330bbaf30ac5e7bef0</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>111.9MiB (117.3MB) – 1,212,287 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab3c0de8e0ffacc04af04b4d5ac4cabd<br>SHA1: b9d40182e5024a48e138c730ea203a03c07abc1d<br>SHA256: d5b296ef3f97ea6cb629457cc9eeddf420338e9bff2e795bf261a5a5ad76c0a6</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>120.1MiB (125.9MB) – 1,212,287 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 702f046d4a6147af8aa3a2e38cf6e764<br>SHA1: 845e2487a56b76a7bd7e3aade0407e92871f9176<br>SHA256: 503107d2c444db32e03b1cd6f4cc8ba1520b938f1bd0a49c6567e81ebb3859ce</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>109.9MiB (115.2MB) – 1,212,287 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05a4d98c9152bdc3cfe3d1d87656c611<br>SHA1: d578f6776cff8945659b4517fd54a1473d405f7b<br>SHA256: bad08f8ed872c51ef70488166ca8e5b0ad5428d13c0f6c1606a784724fd3a448</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>120.4MiB (126.2MB) – 1,212,287 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 484ed4e582c1be2543c88d4b649a9f2a<br>SHA1: 4fee19219b1fe5aba2d749d9b575305f5fa9bc9d<br>SHA256: 528a5cf4e94381072f21925f7032a94026bfc4a145d1a49cf1bdb4faeb568472</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>112.8MiB (118.2MB) – 1,212,287 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c76b8c62c1376263d0fc4868a576eb4f<br>SHA1: 191233493828823a49e258e2e6834e3fb215dd61<br>SHA256: 2b1474082d39059552dfcc52013a9afc6634ca59e0fdb24905abd4db4e35ea93</pre></details></small> |


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
