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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-04-03<br>IPv6: 2025-04-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-04-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.09MiB (13.73MB) – 655,526 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59741eee79186277446a8abc6e16c979<br>SHA1: ad143953f85bd75d78f0d39fdd6ac293b611cb0e<br>SHA256: 9345131adcc7facd7db11f6e3190654c81b49dec78a9caca79f67c9e05c6f1c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>72.50MiB (76.02MB) – 1,101,769 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e28e83a7381e0c8ee2b48cbc5c09ecb2<br>SHA1: b4465ae09652c4251e29679b8e1d60cb8a0ec88b<br>SHA256: faf1c36c9cf30054577b4eec0982fae85f96d1266db5348f16191cbbfe85a3c8</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.260MiB (7.612MB) – 364,239 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6323d2ba185e1b9f3ad0f50d801a0f9b<br>SHA1: 16dc5d7ebdec40f2baa1d88ff7da010f59ac4497<br>SHA256: 293d6b40260235648ef04252b1d8933a3842ad77a8607f652586afd2f9534788</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.00MiB (18.87MB) – 273,546 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37e18de9e861fe6195c241addbce73f1<br>SHA1: 9b8025c07ca81352106f1f9a175f775581401bb4<br>SHA256: 5db20ec85f5df35a151ed3c5ad76bf218a2300bc443256e8fbb3a6321dfd1752</pre></details></small> |
| | | Full Location | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.0MiB (199.2MB) – 3,317,593 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2a1c4fd3709a1baa228a86fb6349eeb<br>SHA1: c5a710b509cfa7705e5aa4218167fcc793e610bc<br>SHA256: 358704998e340d2bd6120c6444b163e0e82cc6fe6d878e10100bd8de1eaaadd1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>394.3MiB (413.4MB) – 3,829,626 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be29c6502d46b9e480fb67d922e01ea3<br>SHA1: 02aec0bbf94ec53629be9ca6f1b6892d6b3e3769<br>SHA256: 1b33864ca1bac3f19cc64c993043c1d499502dd93f4327636b4996162189a533</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-04-03<br>IPv6: 2025-04-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.003MiB (5.246MB) – 250,409 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c808d0929974ac64a4cbae4fda9bf83a<br>SHA1: bffaec9caa921d2ee341e2e1a098930a4068a93f<br>SHA256: e0275d36b93a081a61463252624d169f271ab3384e9d14af58268a7a77cf2074</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.62MiB (20.57MB) – 298,186 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d43b73d17d6f7980ec7a1582fffe5b31<br>SHA1: 15b435fe375c644a3aa740948574ccbb124beecd<br>SHA256: 368de6c35fd3fbca8a04ae5e37bfd79a57e43bacebc9d57dbf3c694bda83eede</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-04-03<br>IPv6: 2025-04-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.5MiB (183.0MB) – 3,024,306 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 692f8461a81a05c2610693fad2cca5b6<br>SHA1: 03f4d5d1cad66a17fc712274fe339595c25f9a0d<br>SHA256: 81594aa4222fce1b4c40bda36bf2a037a7907f56884e1083170b63cc6c221002</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>242.1MiB (253.9MB) – 2,341,972 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09911002e391a82f391c8ca03e15eb9d<br>SHA1: 98dd17ef5340740c6dcad0ab8a29a9282129c031<br>SHA256: d9345db3ba4ae4c485a3248b615e8221d7c63c416c496f40e582c0992d190a6c</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-04-01<br>IPv6: 2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.44MiB (11.99MB) – 572,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a042cfbe297587f967fff4fb10ef164e<br>SHA1: 4e5a3f74d918af494fb2e7548d3d921ca5257824<br>SHA256: 9c4c4d08928421d739ac59f2f479b77a217fd3fea68cd4896d1507f78538435f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>39.11MiB (41.01MB) – 594,293 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e8d794f4ae222d5ad7db223c8a9bcdf<br>SHA1: e0e0680d8788898bcad92f839596df53106befac<br>SHA256: 5e340cfdb4077be6fb43e70678f2f19a67a95a0a89e4a3a5e7f539b115d76175</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-04-01<br>IPv6: 2025-04-01 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>168.1MiB (176.3MB) – 3,322,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b41cb7c4166caddad6ea68f8138054e<br>SHA1: 4dec55d864e0e1b3fab1df01285748d4a736db44<br>SHA256: 67d678b739cd6345f75908e89ea32b2981f24d684541c96001ae7130db10644a</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>178.9MiB (187.6MB) – 3,322,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d7573a918c5fa79a846b10faed7128<br>SHA1: 771a20feb56dde14c59e243e7027aab21475f9fe<br>SHA256: 2f91dc668455b9779e9026ec840ad3f548e494f5bfe4cb62c1e345e69990c827</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>167.0MiB (175.1MB) – 3,322,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56ed9b2c02144617e406ae76f096581a<br>SHA1: 7ce337723365c2c17373de702de90b0719322f68<br>SHA256: 612a7a0df223edb1937bf8bc39755119a93a28d163d80749e3a2c32f47577e62</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.4MiB (177.6MB) – 3,322,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa2fd651e0246a2704a3f255fe4f5335<br>SHA1: 0f63bef384300128a9c32c95d626b6c669d5395d<br>SHA256: e2edcc0c2c59a1488bf1062223e3a76e1e9cebbc8219613b483b2bac0299407a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>213.0MiB (223.4MB) – 3,322,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0db70b963357867812560686d7dbce0<br>SHA1: 629572b5cd1dd8152e61f03ba3d495f987d8f502<br>SHA256: 2f0a50baac3b0a50c241db10a44fe9c8588094ffaa424a1f87bae644f591e30f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>167.0MiB (175.1MB) – 3,322,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4bb8cb2acf98b35ba966157acc45e3f<br>SHA1: 1f9ab0ab90008e8941e379a5a0ce6c1dde4781e5<br>SHA256: 31317391c1d0e8b2359f98cca950e3ab441d645f22cc7e06e1051dbc1a8cfcfb</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>206.9MiB (217.0MB) – 3,322,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 302266a567ce1ab97308eacff666182b<br>SHA1: 97337511817b715c5c451e754234a24289b5b586<br>SHA256: 74634402b53b3bec77e8df6d5ebc7050c25f1720a46513b49a0dec1e962a5b29</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>174.2MiB (182.7MB) – 3,322,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54a7bfaea5c66b2e766979ccbbae33aa<br>SHA1: 7974c49c1d07a29439955ace6887d2637fce2beb<br>SHA256: 1addbc3072b9988fa663365a2fd85cde7abecc6c4696f19ae213acfa8ec8c437</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>168.0MiB (176.1MB) – 1,789,497 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5d56e9500acbe0e44004858a0f351c0<br>SHA1: 731658babedecf22994260fecbf555b39e9240e1<br>SHA256: 813e82b4ead317f0035a32247cdc5369857a5000fe16a331254dfc81cc0715e0</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>171.6MiB (179.9MB) – 1,789,497 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a64d54cc9ff87556a077f8d02924237d<br>SHA1: 96835391c2755ce75eb1527220b36f47933827a4<br>SHA256: df65ee4fcc9fd802dd3c0e3915ba03f89ef0843698f7f0162bae83fd4faaebc5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>166.1MiB (174.1MB) – 1,789,497 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0df52979aab789d9e30a476a8108e7c<br>SHA1: 04e4449c05420d839667d336b052933bfeb5c549<br>SHA256: 40458321894f6e4feb4d3b87f53de832b10fc8cf6a3f8a7b3509b5397db91017</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>166.4MiB (174.5MB) – 1,789,497 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22efaf2839fe83319aef03002652e25f<br>SHA1: 47a239d1856162057e87d7259f92924b62b36750<br>SHA256: 71e1610807d0b87beafda140e98147e1cd99cc0c221177e28f8f57ed8fc2a72d</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>183.6MiB (192.5MB) – 1,789,497 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3827f5719a99e851281575a47cac4f1<br>SHA1: b20e7978d76bd49d958bc06a8a98266d4a0e0f28<br>SHA256: bbb2b2ef44a683e24125153aa0ec68f4950b4adc7e7ebc3e2557cfcdd6f63fb6</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>166.0MiB (174.1MB) – 1,789,497 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8923e9271508b819c75406a8937915dd<br>SHA1: fac44f410b6333cb3151ddcf4c096f2e87e0d1a0<br>SHA256: ecb0ab6efd89452af611af422abab1a54c0ad82fad299637f1ff6ec46062cdba</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>184.5MiB (193.5MB) – 1,789,497 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ce74927cd18f72f80890b3c51b22154<br>SHA1: e3fa361b373aba0303dbd387132de169c9abe309<br>SHA256: 4eee05ba3bf666d9d57ee4fd867484bbfaed322dc6989cb1368918c4a210147f</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>169.8MiB (178.0MB) – 1,789,497 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70cf1fcc605ddc66b30ceb233805bf2b<br>SHA1: 209fae9ae2ef0e7a9e49b3c91818460235066f73<br>SHA256: 0bb570c629a209159af901bfa426f59d706fcce1e3823fcb0769c18e17a681b4</pre></details></small> |


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
