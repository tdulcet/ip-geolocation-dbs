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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-04-28<br>IPv6: 2025-04-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-04-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.09MiB (13.73MB) – 655,657 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1201f0e7254fa0adfdb52e9bc1092f98<br>SHA1: 1427f629a3c2a75f137fd504b4013601d22744a2<br>SHA256: 7024d846f969c7ac317d508b036cc6b1b57dd82ce7dbe943265847fa72f33b06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>115.4MiB (121.0MB) – 1,753,089 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 053cadd85c9252a421a70d9db4d42e86<br>SHA1: daf31f888cd6a3e6e86bb5a43c5d222a7f7a38ba<br>SHA256: 01c28ad2df046eae9bc4b33b0256c2ca512f812fe3be7b4eec78e140f8898f2b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.260MiB (7.612MB) – 364,239 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6323d2ba185e1b9f3ad0f50d801a0f9b<br>SHA1: 16dc5d7ebdec40f2baa1d88ff7da010f59ac4497<br>SHA256: 293d6b40260235648ef04252b1d8933a3842ad77a8607f652586afd2f9534788</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.00MiB (18.87MB) – 273,546 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37e18de9e861fe6195c241addbce73f1<br>SHA1: 9b8025c07ca81352106f1f9a175f775581401bb4<br>SHA256: 5db20ec85f5df35a151ed3c5ad76bf218a2300bc443256e8fbb3a6321dfd1752</pre></details></small> |
| | | Full Location | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.0MiB (199.2MB) – 3,317,593 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2a1c4fd3709a1baa228a86fb6349eeb<br>SHA1: c5a710b509cfa7705e5aa4218167fcc793e610bc<br>SHA256: 358704998e340d2bd6120c6444b163e0e82cc6fe6d878e10100bd8de1eaaadd1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>394.3MiB (413.4MB) – 3,829,626 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be29c6502d46b9e480fb67d922e01ea3<br>SHA1: 02aec0bbf94ec53629be9ca6f1b6892d6b3e3769<br>SHA256: 1b33864ca1bac3f19cc64c993043c1d499502dd93f4327636b4996162189a533</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-04-28<br>IPv6: 2025-04-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.003MiB (5.246MB) – 250,409 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c808d0929974ac64a4cbae4fda9bf83a<br>SHA1: bffaec9caa921d2ee341e2e1a098930a4068a93f<br>SHA256: e0275d36b93a081a61463252624d169f271ab3384e9d14af58268a7a77cf2074</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.62MiB (20.57MB) – 298,186 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d43b73d17d6f7980ec7a1582fffe5b31<br>SHA1: 15b435fe375c644a3aa740948574ccbb124beecd<br>SHA256: 368de6c35fd3fbca8a04ae5e37bfd79a57e43bacebc9d57dbf3c694bda83eede</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-04-28<br>IPv6: 2025-04-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.5MiB (183.0MB) – 3,024,306 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 692f8461a81a05c2610693fad2cca5b6<br>SHA1: 03f4d5d1cad66a17fc712274fe339595c25f9a0d<br>SHA256: 81594aa4222fce1b4c40bda36bf2a037a7907f56884e1083170b63cc6c221002</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>242.1MiB (253.9MB) – 2,341,972 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09911002e391a82f391c8ca03e15eb9d<br>SHA1: 98dd17ef5340740c6dcad0ab8a29a9282129c031<br>SHA256: d9345db3ba4ae4c485a3248b615e8221d7c63c416c496f40e582c0992d190a6c</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-04-25<br>IPv6: 2025-04-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.59MiB (12.16MB) – 580,474 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b268115815ff5aea44e974acd66db6ed<br>SHA1: 6ae4992b2f9d29993848152de555ade5ddf9da7d<br>SHA256: 4166e608a7d6110e51b7c9fd22fff435d0044163ab59133040a21edb8896be63</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>39.82MiB (41.76MB) – 605,189 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ae4e4c33d05e9a77985850b6bdcbfa5<br>SHA1: 4368c08fd212f9d385198ef3cb731523f937c5e2<br>SHA256: ae8ed4c8f3f02022f4b15092b4e08055991b93346649906f6ef4ab2237e787fb</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-04-25<br>IPv6: 2025-04-25 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>170.1MiB (178.4MB) – 3,357,399 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48e8ad1c023b95f836bac5abd48aeb4e<br>SHA1: d06f4e6bb96a18f42ecf97323080b65bedc86604<br>SHA256: 7f7bbc00c59bc9f31778f36e530a71a27d2f62d81eb47da9872b69526336962a</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>180.9MiB (189.6MB) – 3,357,399 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23d10529aa51f4c1563680af7f89a576<br>SHA1: ea9873d79214ad2e886685b9c31be8e0cdb95a74<br>SHA256: 0cf3a14c69586e003f6bff90518ac49470198924f0b74ba45e606f0b869bf169</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>169.2MiB (177.5MB) – 3,357,399 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f021f2163376220b9b0fe44c8a4e6aa<br>SHA1: c40e040704586cf30e105aba19de0d653980730f<br>SHA256: c9e7c89cf281559a3bc08048ad4932c0952fc6517dfa51f978da6825c86b39d7</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>171.7MiB (180.1MB) – 3,357,399 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 323e1d811a8aacc5026668317023ddaa<br>SHA1: 8ba4e2682ebd0e1714065c127eb77970ca20345a<br>SHA256: 7b79bdc92610caa68f42e25346c95cc76980d7da760d8f26cc164626cbefcfb3</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>215.4MiB (225.8MB) – 3,357,399 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e4256bd58034d392b5f66da0bbd2568<br>SHA1: 04fab7312d944daad3a995901ec32bcda48d2909<br>SHA256: b6e368ac69760a57313f1b8f9d3f3950097cd804f733f8bdf3aef19d99a915aa</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>168.8MiB (177.0MB) – 3,357,399 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba02c60e1e0968b13f5619b2ba17b8ba<br>SHA1: 91a7f33a78bd7ad0253feb44c2b9446650ee6f01<br>SHA256: 4cc9f5d0019603b64b74b1efd30d1f92c40a0b064821fb18048d99fdaac5f710</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>209.2MiB (219.3MB) – 3,357,399 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4cdf3e5b075b8fd1bbad8348a23b724a<br>SHA1: 3134a303dfe7b49b319a95d79572d6d8e8f4c2be<br>SHA256: fe43b343b193125f6d9cb81af49e464700f95f8a4074cdef7d9e43ed69d66e6b</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>176.1MiB (184.6MB) – 3,357,399 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49578eaee82b63d35017fe329f6c4820<br>SHA1: 0afa24d7c28d8745abc6e97669bf357ff0b2bd00<br>SHA256: b2e745dd8825704aea83e463fd302bd8dc765886a7f338966b86eedc4e2aeb38</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>174.8MiB (183.3MB) – 1,856,320 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a777abd36803d03fc9d2c23b52045996<br>SHA1: e08a778b08eb533208e85ba41638ecb129d30397<br>SHA256: b9ca065b80468359eaef7f830938ea554ed6be1c28093c9f3cea70a05bb57f14</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>178.6MiB (187.3MB) – 1,856,320 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c61e18ed8f6768d33d1e89d4807a63a<br>SHA1: 05e6f8d329fcfdb0dc5a148028b26b0932dc693b<br>SHA256: f31618152d175944b11f38c0bcf8d4f421047b53ccbc104f0de46055a3b9f18f</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>173.0MiB (181.4MB) – 1,856,320 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2939b502b083fc74f6e5039ab58b95ec<br>SHA1: 49f8eaa4ddb0b7f594ce90531daf2e1314aa6e39<br>SHA256: 1a355ff07759e5603ba66fab5a56548dbc0a89304ff6d206e950246df5d20712</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.3MiB (181.7MB) – 1,856,320 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03cef7f942bdf4c78c0c010c5c92656e<br>SHA1: 2717bf9fb747f464eb2f7fdc3917846142686dbf<br>SHA256: 5bebe5cd8bf7756ada31a03cce257d6b7cd343036687281b30090fe269a1f043</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>191.4MiB (200.7MB) – 1,856,320 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4da96048b17957553de6cc85d3dc048<br>SHA1: 33f2912b2eda2051e9108549f493e25b3e9c2f9f<br>SHA256: 96bd6a46e8cbe351835959d50fb78e4a15c09a49caa4e8b2617a6c88bc1aa99a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>172.7MiB (181.1MB) – 1,856,320 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1bdaa74a8701b4e5d7ee589973c1658<br>SHA1: 2a876279c5805d6bb01c69063a7f095c7a35a0fa<br>SHA256: 0e8beaf750bd1aa7b8c20ce742b1a0ef89d9bcc0c47891de30ed9f0b165eb386</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>192.4MiB (201.8MB) – 1,856,320 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 865a903adbf785f2c29743e0b2837da0<br>SHA1: 5015e64ff3ba1a8c80a3b4ee49e2272fb407a78d<br>SHA256: 12ed23420658a711d516a77fdaab13eed422c0d9e67c4ca264c90bf58e4a3ca9</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>176.6MiB (185.2MB) – 1,856,320 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 006fd3e10f46e82abd683777eeb14aac<br>SHA1: 4a7cdf3e52c824e7901d8fcebf2ae1996b6a7e4b<br>SHA256: e9e2b149592765e4e081da9fed0370556313e353937f9f0a2be304eac6c4456a</pre></details></small> |


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
