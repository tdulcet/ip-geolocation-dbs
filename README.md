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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-04-24<br>IPv6: 2025-04-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-04-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.90MiB (13.53MB) – 645,904 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e08038eac0e9364ae0232015f4a1ed68<br>SHA1: 63e47969bf9f8b89a9d999df34789600ff50bdd9<br>SHA256: 6e0ac1a3fe3a9a7e0ab72433e03005c6c6891271e735da2a39b3a997cffec224</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>101.8MiB (106.7MB) – 1,546,463 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aaab3aab573303ccbdf2de9223da7d19<br>SHA1: d3c5e7e5036e984350890ed1da53baf2154f9138<br>SHA256: 5b7449faa7ae419ad7359d4989a4b17c941a62b3032871dfb5462783d83f5381</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.260MiB (7.612MB) – 364,239 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6323d2ba185e1b9f3ad0f50d801a0f9b<br>SHA1: 16dc5d7ebdec40f2baa1d88ff7da010f59ac4497<br>SHA256: 293d6b40260235648ef04252b1d8933a3842ad77a8607f652586afd2f9534788</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.00MiB (18.87MB) – 273,546 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37e18de9e861fe6195c241addbce73f1<br>SHA1: 9b8025c07ca81352106f1f9a175f775581401bb4<br>SHA256: 5db20ec85f5df35a151ed3c5ad76bf218a2300bc443256e8fbb3a6321dfd1752</pre></details></small> |
| | | Full Location | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.0MiB (199.2MB) – 3,317,593 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2a1c4fd3709a1baa228a86fb6349eeb<br>SHA1: c5a710b509cfa7705e5aa4218167fcc793e610bc<br>SHA256: 358704998e340d2bd6120c6444b163e0e82cc6fe6d878e10100bd8de1eaaadd1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>394.3MiB (413.4MB) – 3,829,626 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be29c6502d46b9e480fb67d922e01ea3<br>SHA1: 02aec0bbf94ec53629be9ca6f1b6892d6b3e3769<br>SHA256: 1b33864ca1bac3f19cc64c993043c1d499502dd93f4327636b4996162189a533</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-04-24<br>IPv6: 2025-04-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.003MiB (5.246MB) – 250,409 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c808d0929974ac64a4cbae4fda9bf83a<br>SHA1: bffaec9caa921d2ee341e2e1a098930a4068a93f<br>SHA256: e0275d36b93a081a61463252624d169f271ab3384e9d14af58268a7a77cf2074</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.62MiB (20.57MB) – 298,186 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d43b73d17d6f7980ec7a1582fffe5b31<br>SHA1: 15b435fe375c644a3aa740948574ccbb124beecd<br>SHA256: 368de6c35fd3fbca8a04ae5e37bfd79a57e43bacebc9d57dbf3c694bda83eede</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-04-24<br>IPv6: 2025-04-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.5MiB (183.0MB) – 3,024,306 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 692f8461a81a05c2610693fad2cca5b6<br>SHA1: 03f4d5d1cad66a17fc712274fe339595c25f9a0d<br>SHA256: 81594aa4222fce1b4c40bda36bf2a037a7907f56884e1083170b63cc6c221002</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>242.1MiB (253.9MB) – 2,341,972 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09911002e391a82f391c8ca03e15eb9d<br>SHA1: 98dd17ef5340740c6dcad0ab8a29a9282129c031<br>SHA256: d9345db3ba4ae4c485a3248b615e8221d7c63c416c496f40e582c0992d190a6c</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-04-22<br>IPv6: 2025-04-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.57MiB (12.13MB) – 579,387 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c49717314cbac82c70a139dd943d0a36<br>SHA1: 057d4e0ef6b3c6a202855d24240b407425ba3586<br>SHA256: 3b4dc0d86fa0bfde80679206a6f25d248419f18c3a431428f2b19cd2ec06b018</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>39.78MiB (41.71MB) – 604,557 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c66af004b95c555662990c1fc480eb7<br>SHA1: 3e1f12c023024f11412e36da6502095db8994392<br>SHA256: b2d87d5fd7eb69f880380dffe50bf380282c8efcc82ef4de2aa1eccf4fc923ec</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-04-22<br>IPv6: 2025-04-22 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>170.0MiB (178.3MB) – 3,355,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d737aa0c54f9c0e9e7b98b035a04650b<br>SHA1: cccf800de882138e091ed31622505e2178ccb90a<br>SHA256: 4773e1748ac7bcd10264272c4c8203f54e859d7c50a0cf6fef199e19a971f166</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>180.7MiB (189.5MB) – 3,355,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3206bc764f8a1c34e8363ddc479124c4<br>SHA1: 844cb32fad301bb6419980597567000844534adb<br>SHA256: 1be4ecfaca71b150a7f4593b6e267e8a91a1d47910c487583bd16cff30afd4d3</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>169.1MiB (177.4MB) – 3,355,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98872b979e4fa9c0cbf77f2ff0f374a3<br>SHA1: 6aad5d6e66958f0bd6db678a9f2daaf1ff675960<br>SHA256: 4f814c990b4948e55a0a72138dd003313d7354c8233f35464f917728dec0143a</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>171.6MiB (179.9MB) – 3,355,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ac7fdafc5bd92f0db4e517105419350<br>SHA1: aa481f11f7347892ec56cc50a903a189c21f9147<br>SHA256: e68780c6cc5f4efa3575b92f49e2b988b8d205f92ef510fb9891243ec0f89bd8</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>215.2MiB (225.7MB) – 3,355,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07303bd1738c442f82d67d1e123dd6b1<br>SHA1: fa38ebc29dfd022c3302f9bc998c12c87edcf314<br>SHA256: 5f044dd54c311a61661fdf06553de94c2be598b706cc72c8202cee7174a386a5</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>168.7MiB (176.9MB) – 3,355,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1616ad1c5e943810de5061b722ec9402<br>SHA1: c265153d41423a4a0d74fb18ec3cc7694c29cb6b<br>SHA256: d506945ece9c8a535509f9ccda9ef2c9dc6975500f5ac104ce9738c57d733a02</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>209.1MiB (219.2MB) – 3,355,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5113b584b9c6a80309c60c3b3374bc81<br>SHA1: 2e0b1e52527f139eb9a38c04f4ba676dc22be78f<br>SHA256: a7d1743f3c6c5341caf34b59853afde48aee962b307e20de0b79505f1ae3acaf</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>176.0MiB (184.5MB) – 3,355,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56da1186f04ea747628c637416d26b21<br>SHA1: 75cc9917b435db0fde0a8af2099ae536449848c4<br>SHA256: 743db6c84ef631595947abae95b4c81fd3a84c9466ea97c845a521d49db30e0e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>174.7MiB (183.2MB) – 1,855,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 327892e3f963425b7829ad129da76149<br>SHA1: 3aa433d007fd4d0b8859278782d03cac05893e6f<br>SHA256: ac1bb089c9df0fab0e22a81bd4fdf8b351c57c13da34ecdf4a60e3b566943213</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>178.5MiB (187.2MB) – 1,855,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2b93305e283a1033e953a875a1687e3<br>SHA1: 33e9d4268d79d194947250bb974e266d62cf0518<br>SHA256: 5dae9bcfdff3c9a1a166f35dd62cc37d95db0fa083f79b3865d18419abbe1be6</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>172.9MiB (181.3MB) – 1,855,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 921be419cb75f650bd79f29f623ae15a<br>SHA1: 273789d15271cd391d18d172d1d6f90c9133a452<br>SHA256: f9d0e0e3d476abab353cb343edf4d498c016b849e4c29fe5533008f314293fa2</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.2MiB (181.6MB) – 1,855,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b0eb24ee438a81bf33b811d2fbc0a10<br>SHA1: 3897814715905e606ecbcd64d322c3f4e14cb16a<br>SHA256: 56fac3c7e01750aa5ce21404c234a0105bcac0b5d05f2685474afed48c343871</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>191.3MiB (200.6MB) – 1,855,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d706b449481474381b98fed6d68d735b<br>SHA1: beebf22955a1952f1418f5cf28a49b4ccac99b27<br>SHA256: ac3f101bf9f5f4acca7de702f0f9f94754e79c51eb9049f51836fbacca9cec7d</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>172.6MiB (181.0MB) – 1,855,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b83c7e701a67fab47cfa6895ba0faec4<br>SHA1: c6af4ad1e8dbf7c4811377c81ec5ae60052c1da7<br>SHA256: d8e9d3d0a8003b52a14798270945cc4bfd38e79b0c5d7d26a787b4ed9556e688</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>192.3MiB (201.6MB) – 1,855,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94d6826c169c5c173612157ddf2b9702<br>SHA1: d7f7cd4dc313d34f3ea5e9d29ff6927eb859d068<br>SHA256: 2f6df18a2a2230de1d9e821b31eb1e69d0a7d89cf95a083fe45ab4a1a83e52aa</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>176.5MiB (185.1MB) – 1,855,420 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56df0ea511bc2c4b4c455f1b9937873<br>SHA1: cff2974d127686ec56a235336f74cce40490b219<br>SHA256: 8c4b48891b041cd6fa01b4ec88d3860f1de94328a3980f795795d7748f29d117</pre></details></small> |


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
