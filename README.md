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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-01-22<br>IPv6: 2024-01-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.789MiB (5.022MB) – 239,748 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d15e04e1adf84213662a3ab574bd2e3<br>SHA1: 0c96468b4fb46e78ebbe3cac28a53ef2e3808583<br>SHA256: 3beff22bc62d1b64c418e1aa5a31d39a07063322c8a3b8e070514513b1424ffe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.529MiB (5.798MB) – 84,027 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcf036c774cca251f4bad44682d9f9a3<br>SHA1: 44f7a372ad26cf4621e7d102e23ddf0055221474<br>SHA256: b94b9e72d5f12c6de287937ab8fda3882aaaf6a753281e679d9c7be67465b95e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-01-22<br>IPv6: 2024-01-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.226MiB (8.625MB) – 411,928 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 155ce751cd4207d45e8715c425ffdf0c<br>SHA1: fe8d58decab087600bbc143926da3e1dafad7abb<br>SHA256: c5f55f2f32e40da92b38461e56fe09b85772b3410d56f5435a97d0dac316197d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.924MiB (7.261MB) – 105,345 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49b7e51b81c0312634e57d64bc90a831<br>SHA1: 9bc6fea6fe4db76107cf6bc894b5eae9ac5e4745<br>SHA256: f3e3d1b13e021730cc04784f44a8a81eaae9180da1be4f060ceff20fe6d75e2f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-01-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.73MiB (17.54MB) – 837,650 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02cb22142bde655750a3b3bfcbe48c62<br>SHA1: 8f294bedb21cc5cb7860c9f283befe08d67da43f<br>SHA256: 06e6b8b357583133947ff491a6115699904db1f941ec10b44d8ee23b3f957a0e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>53.03MiB (55.61MB) – 805,951 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b58f572a44d011b46225091e22ae4b9<br>SHA1: 37c326198de40ed656408aa91e41d72b743e9368<br>SHA256: fc787d5e1b6fd8a04eff55d4ca3ac7c28ee4e3bf0d453f0deba49f2c8ed08995</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.162MiB (6.461MB) – 308,408 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736158b820db1062b003cfce212076a4<br>SHA1: f3b03108eb0edf83c338abed05e010c2b0e9cde1<br>SHA256: 68e446a0380ab263a21743f68ab8aa6b249b213af0d6ffdac0780fe4912cb7c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>21.05MiB (22.08MB) – 319,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73819723f00de32c17c8aeca84d93383<br>SHA1: 71d954fffd9f9f5979ff89981fcfae6f73cadb05<br>SHA256: 1328a782f89b58d1f6fabcf3542ce4bb259d89c1f28a0cc70abfe70b5e573eea</pre></details></small> |
| | | Full Location | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,096,472 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b990a48af772fbc4cf7093aa51d35b4c<br>SHA1: 8ddfa8795c4c534c0bfd99b2472382b368d7fd5c<br>SHA256: 117938f84386f9ca627464e7c42856b6d9ff4f68bbcac12a393b73ea1ac0836f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>243.3MiB (255.2MB) – 2,358,639 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c61e48446e598bab5cfa16234f5f136<br>SHA1: c3373a6fe2e2f8e08a48274939c4b494fb99b5f1<br>SHA256: ff81c189923d299847f5b5e0e5c472fe10d836d11e24fa5379a2def67c998406</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-01-22<br>IPv6: 2024-01-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.626MiB (4.851MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24caac24a9c72bc3caa6451ceab08833<br>SHA1: aa114043e64d74ecd9e8ccd339b80c62d3fcbabb<br>SHA256: 6d48a0384e6e4d38820ac8d2936c12db7eb726dfe20c59600d4f14d173e3b15f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.10MiB (17.93MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fc970b50f7b01de0d0c6bd29224c13<br>SHA1: cb1fe32e67d0561cefef5f2908570ae3af446a24<br>SHA256: e0f36200f10f817a89b6cf80d8d459900c5428a669cc706af32d15b709a8b624</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-01-22<br>IPv6: 2024-01-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4MiB (176.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4104f39d8c379ec8967157286f495717<br>SHA1: 440c75c20491f104948897ce552c95510badba7d<br>SHA256: 6689c6e63153fcbdc00272e2ec6cf04f0c6877860b4a667b3972dfa08c898747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 142dfb0f4dc0ceb4f5a41b018ea53524<br>SHA1: 284b510184f46179e9e34f60dd0db14fc72f3e50<br>SHA256: c57159c9a8879702623a2ef4d0c2fad06d21e96f1836db2d3a09f9216aee1641</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-01-19<br>IPv6: 2024-01-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.290MiB (9.742MB) – 465,385 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 818b5c71dd8b4601d3380c3f0704411c<br>SHA1: bc6e35c7aa37cee81f04ef40c9c2966af7dd35d0<br>SHA256: 2b196f62763a0bc5089e98e7db0130a13644d32d3f13522f1c01186dd972e9ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.06MiB (19.98MB) – 289,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9a2c0a9b9aec7d39527fc7d7df14d8b<br>SHA1: fdcaf8950c2f1056c508605edc3256bb075b3f5c<br>SHA256: 941e729d02f3b5c38241d2942e2fd2bbe5a86d0c2b68fea56a5316c83ba28a9c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-01-19<br>IPv6: 2024-01-19 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>161.6MiB (169.5MB) – 3,441,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 243f8155c31ee0f9e135669280fc9a23<br>SHA1: 4afa04e0c3df97d54caf04d95197653a52a9685e<br>SHA256: 3897d3068a69a912259909422e04eb8672747445ca94f4e2949df2cd0f148052</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.3MiB (198.5MB) – 3,441,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fb9fe3b26920d4bc7c037c7b918d9df<br>SHA1: cab91351586233fb4df3ec6b0279bab7a9c49a9a<br>SHA256: 3921cc5f1dfe86a9f3ab8b4f1ea39ff0d1e1370b1accabbec3601ba503dca8cf</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>166.4MiB (174.5MB) – 3,441,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98f0dae8a8f95274a1bf7a03d35292aa<br>SHA1: dc1ea5a810b6eb3c7c9868e7bf41a69288908777<br>SHA256: 0c33f3f2b74558cf861abf65c6b149da7c953062e48b3416a86ba10d3221f50b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,441,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ef0bcccad862151dceb570846fa1d72<br>SHA1: ab85bccb1c6ee27def2a2436583095129060958d<br>SHA256: 0449759d9dd17035d3115267fbf074645dc8416642f3848c10bb1ea7b6c4797f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>202.2MiB (212.1MB) – 3,441,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20d94ccd2f957417c04d70c797799ac1<br>SHA1: a54e362642912010d8232eb59662cdc30ac90d42<br>SHA256: 37e1d4ddd7dc7ee81c727ecdad1afcbf83c72e471c02259fc73e77e0975d6352</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>161.2MiB (169.0MB) – 3,441,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c53c3be3bbcb27ffa1c8ea298d9752c6<br>SHA1: 70e279f06d2fec96acaf22e973b2154299b54e8c<br>SHA256: 12ffd3f47b24786b2c6b7f8748323a8e33ac1640c0559ae860e9299b83bdc6b2</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>201.7MiB (211.5MB) – 3,441,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae926b5b315a383d3112fc1f49e58e12<br>SHA1: 2c2f0a26b185676637f77de645dbf56c6c9bf726<br>SHA256: 084aeaecbbcea87f8a9daf4fedcb72fb9e04e2891b18890b370bc6ebcf3b6fea</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.5MiB (178.7MB) – 3,441,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d34251ed04c31d27d15c76f3b5dcbd92<br>SHA1: a706ce10c0d3f3eea4e027c397867a24e701cfb6<br>SHA256: 9977f122b5d81a7b31cbbc369d7374deb486481f512dc296ab1c1a060a8c1bd3</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>109.6MiB (114.9MB) – 1,227,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b602f5de1d1ade91f717589e2089e349<br>SHA1: 1c21a4c2741fe7b3abaaabd4c275cdc9745e52de<br>SHA256: 3106b91bff202ad27bf77f5591dd24faaa41da74fbdda04c62e5229848b26116</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>117.7MiB (123.4MB) – 1,227,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2836751d07e0fcf982c5137c34347fa7<br>SHA1: 4f1e003e4de1291d94dfa7b7e91787bdd8e1adc3<br>SHA256: 513215568a19945d1c59ebbd3205ca43c1cbf5c12f4d2afa99c57e9bd394bcaa</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.0MiB (117.4MB) – 1,227,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9f6a1f8019aeb65a06d76df188b7f52<br>SHA1: 5a44b569735253b3d59bb2888648acb4cab54f65<br>SHA256: e10c0bc5da6c22f1addf42180162fb3ea284b071257a69d08d24a9fe95a61f87</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>113.0MiB (118.5MB) – 1,227,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a749980805de493757578b07fb1c1028<br>SHA1: 903e3ee86dbac696084395b147cda6c0acb6f66c<br>SHA256: b8b828ba559b9bc67a9295e4744fcfd034850476175600e0bc0d95ddc9619ffb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>121.4MiB (127.3MB) – 1,227,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54cf8c337bb797c44af9bfdb49309509<br>SHA1: 0dae4b441ec0dcb94cac16cc1819660f20735c59<br>SHA256: 18a14bf0fa4eb50e4278cf6b6ff7c7e4188f36410c0b296c7d7971ea99c74013</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>110.8MiB (116.2MB) – 1,227,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb1b74deaf7183e5d2536eb381593847<br>SHA1: 7d12093f4fc706520f9e80246651d1b0aaae75a1<br>SHA256: a7f67dc624f2d9810409d5d3f0122bba359ae138a0856f056302950cb6e4e044</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>121.6MiB (127.5MB) – 1,227,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65d63a802b58316e3f8443ad4f2ea5de<br>SHA1: 9bf6ec58b7fe26016d5c16791aeea5d1788a9185<br>SHA256: 4d9516696b101389fd54249c1887735f2d79df575d77d6b363eace69cf0e0c62</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>114.0MiB (119.5MB) – 1,227,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3bee7f58c412023660af58a87ecae712<br>SHA1: 29c83c1dc3b71ff05f9ea6da7e8619f1fca94585<br>SHA256: b663eddd3b3a0c56276218aacc2e140f15df8f886e149b791cc4d742c8f73f13</pre></details></small> |


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
