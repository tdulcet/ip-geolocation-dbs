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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-29<br>IPv6: 2025-07-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.127MiB (6.425MB) – 306,800 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88d50534e0e2b401bdc2b3012a494906<br>SHA1: 0eedcbd10b35aaf7e8eb944f5cfed9eda17c1792<br>SHA256: 45cb3f06246a3bc88d593a7f8f589e840cc5abf53b0e24940418b4670cc24ec6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.12MiB (10.61MB) – 153,749 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c45fafd22b02033beffb9c19df41db3<br>SHA1: 0140b96f30634bb1fedd6abfcf0a01d9c2f4c87b<br>SHA256: cb076b9b332d83d7f36378c6bd9101d6896e3c1f75cd540bfc73a9418330f91f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-07-28<br>IPv6: 2025-07-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.553MiB (8.968MB) – 428,134 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b89aaa6860f40cde6ac2a4bdc97a45e<br>SHA1: dceebe5c47d6e84897ebc9fdf73fc53dbba308ee<br>SHA256: 77349eb3a20eba876c905d55245e65c82cb819c07d81bab823d67e9c3268b39b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.325MiB (7.680MB) – 111,424 rows – 226 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9a71834d9384d8cbc6a6e989859bcc0<br>SHA1: f293f7f62c2330f21db33787f023894ce82ba2d5<br>SHA256: 3b2a170af800dbda3611d6309b30ba03052da609109d1899330d743c86fd34a8</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.85MiB (12.42MB) – 592,971 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c9a8c5a3e76df07a9c4b642529bcd5e<br>SHA1: d860ee0c6a26427c954de2180b50d0fed1c0b9e1<br>SHA256: 45a1f2d5bbc7ff298603c95c15e507e16c6b6afa0fa4c2b64e54ab644e83eef9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>90.79MiB (95.20MB) – 1,379,644 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8a57021e1599d1397afad5edfb87603<br>SHA1: 861ea76bfd1cef4cfab38e08fbbf45f7b3233d1e<br>SHA256: c81a571a4eba3a9fc9aeb239f1640f79a373d025867874b0bcbd55e727edbd41</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-29<br>IPv6: 2025-07-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.068MiB (5.314MB) – 253,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ddf95be39b948ff8a1f5f72a989f3db<br>SHA1: 53e521e70cdc7bf139a71019e836b80590d710b8<br>SHA256: 50c6f2769387e3ee7cedf43b469b7ba544e29e43852d8c3fccd14dbf39e376a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.78MiB (22.84MB) – 330,989 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43bd9e1f0cc46c204def11cc25411429<br>SHA1: bb110aabf0613079fa6821963cb9072ee8a672f5<br>SHA256: ef3129675278c4750cafd639f31a9a899cbc6468108504cf55d1a6439f90199f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-29<br>IPv6: 2025-07-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.2MiB (176.3MB) – 2,916,495 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec46eb0d6770f3a4934f80b9ba8b43ce<br>SHA1: f00f5138d48a37c35fcf9f170e21939324735351<br>SHA256: 16a49d4f2d09a24369e498fa18c855ad30e4610d4fb1424acea4ea9ccec6048c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>279.1MiB (292.7MB) – 2,704,923 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dac800448bd3a785c553531ef23da1b6<br>SHA1: aaef79ba06d4297b621a7688cc2224cb694528a0<br>SHA256: 6c59b673d7391b858e46d6527a0bce731c26713b44246050076e424d61a9f656</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-25<br>IPv6: 2025-07-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.59MiB (13.21MB) – 630,438 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd748be9040b700943d3d30948cd048e<br>SHA1: 458d9b1f82c8edbb90096b24b6e42bc8f70288c7<br>SHA256: db444313becff0b08665a258079f8be8e81e1148308edbc7f0e17c83a49d8a21</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.47MiB (44.53MB) – 645,436 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23def96f1244ca9e744c1dc5aa7b0ea9<br>SHA1: 987b9cf07e6198364b51d83bacc7b72411189ec9<br>SHA256: 40b6a5270b4e141592f80947d69551112dd8f3da37b2bf6c24967403dd51b7f7</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-25<br>IPv6: 2025-07-25 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,427,668 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02b640ff6939a4acd18fd064db9f5451<br>SHA1: 6a890bb8cf9f2bb156b3d9c028fd9bc950ccc6d7<br>SHA256: bc4024cb870dc41a05fc4612173ca306fa1141a4bef2adb5768a05687e156ebe</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.5MiB (193.5MB) – 3,427,668 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 101474650a971ea6ffbe4f843e8a45a8<br>SHA1: e75a0b929458c7e395eb556005d3a8e9a333ebed<br>SHA256: 298d2588a6473a1b24784d8b8348c159862029d56ee8a1dc8181374a83b9afcd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,427,668 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 116493c041737872f146328486f25e80<br>SHA1: 1fb87d1ab1ac4921011b9635f952038dd6f9f4cd<br>SHA256: 384e003131186789339c84b5aa96a086fae269ef04043cf84f8cf9ead0e55ebf</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.4MiB (184.0MB) – 3,427,668 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a6242e22a88d39e6c9c9ec758d3166f<br>SHA1: 9487c3070d1e6f17bf4dbe65c0b740df1af83fe3<br>SHA256: 661b26ae7d1c39fca3ae1131d9e992e75a47a635705e96ecb24a8b575f2b2b5f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.9MiB (230.6MB) – 3,427,668 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8ea2b0aa767c2e66d27c8d7695949d8<br>SHA1: 5c5ebbc18fc1edf285d08df0830da7747b1ea57a<br>SHA256: a87f2f423966a770f1f98238114861f90c248668a7e81fe7f8e8904c3dfae1ec</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.5MiB (180.8MB) – 3,427,668 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b68c41da44e4c5d9dad4a4b42e7e8106<br>SHA1: 81c74ea52079effa835cb2ee62093cdae2bd06c7<br>SHA256: 563fd0d44f301ab997216de6e16a71d54eb9d277cfbc1ff73936fbdf6bcd4dc5</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,427,668 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e81f1ecd925b0af69175616f6b4b8da<br>SHA1: 818b9aaaef9a9957ea94b310ed696673badd3766<br>SHA256: 9781a1ea873869af3a48f17ca631c73fdc207b6aa0697632967761621f8f365c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.8MiB (188.5MB) – 3,427,668 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b4ff0a7a1c328302b6675c1b9c90e1a<br>SHA1: 281db7959322ef758062805d292e00fe6d3365c7<br>SHA256: 9e82ffc78585e29bd229a5e648fb0fd789c500ecf840d31aaf3c1794a47a2c27</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>178.6MiB (187.3MB) – 1,895,910 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4de43d84d6e9f3b0f831a03e0da7d067<br>SHA1: 885a355b10d55ace4b3f1827084a2a0cc78481aa<br>SHA256: e17c4cc79015f5c58e8983be3c4d13347c8c360bc2b20be1b0a08b902072f0f4</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.6MiB (191.4MB) – 1,895,910 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a655a15db6c6b6ee69de028f36b0c3e<br>SHA1: 1484cdb0c90dcd3e5dc710b846b0892f9099f66c<br>SHA256: e73c25875a0ed8d86e440f10736acfa6ff9e2e47cb342993f318c6a8af1e2276</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.8MiB (185.3MB) – 1,895,910 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 058a1225a08c9111cf134976061f686a<br>SHA1: 373cdbfcc6511f5f327b1e11c65798e86b37c23d<br>SHA256: 78b492a4699bf0ab6b6fb1d2b36c0e98ec8b20a07e1f80c1d0d65c7f1196a89a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>177.0MiB (185.6MB) – 1,895,910 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 671ec7f60af66f6a4ef1b49375c4ebb0<br>SHA1: 0f0a322c0fd72e70e2eb669ee2ae08207a981823<br>SHA256: ff0b7b9330c70fbf6e7cd4cbc1fe8b0dd16dd31b8eaee8b18ca7d4e57b978dea</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.9MiB (205.4MB) – 1,895,910 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a12df522b0f4d52779cba13d4ffbfcdd<br>SHA1: 6fdfbc4c86bacbd60b4474cf0f2c51f06727c01a<br>SHA256: 1eaf29fef178c5938611f6a7c952a0a07b10f60791a4aae68c329dbf5456b422</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>176.5MiB (185.1MB) – 1,895,910 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8f86945871b34d83e1f5ab37d471c6e<br>SHA1: 8af1f0f5ff3cd64e3b1212cc40b3cddb7c1eadd8<br>SHA256: a722b3645a20c2587abce22ebb9c1707bee91742ff489c1024488bcdac4e8951</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.6MiB (206.2MB) – 1,895,910 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee9ca2e86defdfabcebcf22b4f758503<br>SHA1: 316c354d80e574656857133652f6df8983239630<br>SHA256: e03558a02f7da9bfe541e1b36912d71199e05b7b9b34c85cb3301e4106958e76</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>180.6MiB (189.4MB) – 1,895,910 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d3e2a7014489c1109fb5cd1bdbc4384<br>SHA1: daa49ed20fe87eff217b9b21d50aa67f7f7d078f<br>SHA256: 41aaaed1f7b874ce7e0cb6cc60b036d29ce0ddd46030f6409236ecb8ccb14562</pre></details></small> |


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
