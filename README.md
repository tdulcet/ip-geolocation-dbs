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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-04-08<br>IPv6: 2025-04-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-04-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.65MiB (13.26MB) – 633,276 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c6cc55efd4d84573d1647684e58c6af<br>SHA1: db24e04bf4f5ce93e7d8a4f22d6f9d9b23bcb714<br>SHA256: 45b4a16654e13d047c027c38e790703bf1e13d65b32a688eacafb97eec59108e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>72.27MiB (75.78MB) – 1,098,222 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6ce466f7f5ea5985829875a8ed6713a<br>SHA1: 2b029fc7d4b923e66ab72ff8313eba76e711007f<br>SHA256: 10588db6593d5f55b48a14512ef3a4fea939daea874585c8b3ddcc50cb10b2ee</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.260MiB (7.612MB) – 364,239 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6323d2ba185e1b9f3ad0f50d801a0f9b<br>SHA1: 16dc5d7ebdec40f2baa1d88ff7da010f59ac4497<br>SHA256: 293d6b40260235648ef04252b1d8933a3842ad77a8607f652586afd2f9534788</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.00MiB (18.87MB) – 273,546 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37e18de9e861fe6195c241addbce73f1<br>SHA1: 9b8025c07ca81352106f1f9a175f775581401bb4<br>SHA256: 5db20ec85f5df35a151ed3c5ad76bf218a2300bc443256e8fbb3a6321dfd1752</pre></details></small> |
| | | Full Location | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.0MiB (199.2MB) – 3,317,593 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2a1c4fd3709a1baa228a86fb6349eeb<br>SHA1: c5a710b509cfa7705e5aa4218167fcc793e610bc<br>SHA256: 358704998e340d2bd6120c6444b163e0e82cc6fe6d878e10100bd8de1eaaadd1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>394.3MiB (413.4MB) – 3,829,626 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be29c6502d46b9e480fb67d922e01ea3<br>SHA1: 02aec0bbf94ec53629be9ca6f1b6892d6b3e3769<br>SHA256: 1b33864ca1bac3f19cc64c993043c1d499502dd93f4327636b4996162189a533</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-04-08<br>IPv6: 2025-04-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.003MiB (5.246MB) – 250,409 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c808d0929974ac64a4cbae4fda9bf83a<br>SHA1: bffaec9caa921d2ee341e2e1a098930a4068a93f<br>SHA256: e0275d36b93a081a61463252624d169f271ab3384e9d14af58268a7a77cf2074</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.62MiB (20.57MB) – 298,186 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d43b73d17d6f7980ec7a1582fffe5b31<br>SHA1: 15b435fe375c644a3aa740948574ccbb124beecd<br>SHA256: 368de6c35fd3fbca8a04ae5e37bfd79a57e43bacebc9d57dbf3c694bda83eede</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-04-08<br>IPv6: 2025-04-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.5MiB (183.0MB) – 3,024,306 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 692f8461a81a05c2610693fad2cca5b6<br>SHA1: 03f4d5d1cad66a17fc712274fe339595c25f9a0d<br>SHA256: 81594aa4222fce1b4c40bda36bf2a037a7907f56884e1083170b63cc6c221002</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>242.1MiB (253.9MB) – 2,341,972 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09911002e391a82f391c8ca03e15eb9d<br>SHA1: 98dd17ef5340740c6dcad0ab8a29a9282129c031<br>SHA256: d9345db3ba4ae4c485a3248b615e8221d7c63c416c496f40e582c0992d190a6c</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-04-04<br>IPv6: 2025-04-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.45MiB (12.01MB) – 573,367 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d718094951dd199139a471b40357126<br>SHA1: 50c6329a53de130f2ff1c840195f7ab02b849389<br>SHA256: 196c6dd88529e590fce761549f18b79db2ebcedd629cc8d0c077182a1f11b8d4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>39.27MiB (41.18MB) – 596,829 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 568250d216cc5fb9943d1406a0cb5e0e<br>SHA1: 5c227866deb96359be36a93c7ce9a8a68f67109d<br>SHA256: 39f985ebffb8954a34ddd1dd02dcd0bf49f3d73ea97e083dd38288f7738a1347</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-04-04<br>IPv6: 2025-04-04 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>168.3MiB (176.5MB) – 3,327,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0abff52077a13f48741e3c0f9cd1bf47<br>SHA1: d9d4fa5c35ae8d2a2514ffefd9195a9cd1c9e971<br>SHA256: 853952e26bdd680c2965904d42231dd7cca7710c20837d33397c957438e8723e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>179.1MiB (187.8MB) – 3,327,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d57d0091c838c87a209ade0d4952d0<br>SHA1: 5ae7860c3532c870dac68e9c3622e1d9af577ad3<br>SHA256: 1b00d18a99cd9d4378e9f83e279e5f14019af41e3795cac1cba75ac3ab5c01d7</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>167.2MiB (175.3MB) – 3,327,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27d0ba53fc50d20572f890446daae860<br>SHA1: 2e37861869a68cc7e90301e753a46020a7972a90<br>SHA256: a221e19486827647e84426be682d072d8a77cebcc2c28db078de79aace43afd0</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.6MiB (177.9MB) – 3,327,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0159c2b66eed559e6793337b3bd2a8ef<br>SHA1: b505ee5c23334489aa098996a278ad673956f496<br>SHA256: b989449d582b1a55b0d659e70db8eba93e729b88acd72f3a8decfee29d148049</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>213.3MiB (223.7MB) – 3,327,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dec3dbff8e8750831408f159271cf561<br>SHA1: 7f357b085b1685c851918492a2b81d55d8fdb32b<br>SHA256: 06184e903aeab3c5bf3a2e33baa02b459aff3ece30aa83c7d0ab0eaa78e951c5</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>167.2MiB (175.3MB) – 3,327,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9388163ddb5586f4b6707dfb213cfcf3<br>SHA1: 26d0f76a8dbbdcb781d26e520151c4e4b0cbcb14<br>SHA256: 81263e5a59fcb414ba5be83eb691174858f3f843fc312deb34d8e611bab4b66b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>207.2MiB (217.3MB) – 3,327,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c57c15ddca696e41eba728812e8b95da<br>SHA1: ef46c45c934dcc7e3871fe4d9aaeaff89afbd0b0<br>SHA256: edd8f8ac59c966f2a1a15c9e618a2691313b2b5bdbcf908e15cc4357dbc3b33d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>174.4MiB (182.9MB) – 3,327,296 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 832f7c031c608236199614eca72d7566<br>SHA1: 98c2c90cf29df91dd98d0ee834bab7a2b56db7a4<br>SHA256: be67e5610cfc79faa7d395b5180aaea5f5d87bb15f7314f51ef345828a6c55e6</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>168.3MiB (176.5MB) – 1,793,441 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce6e7ba89cedab498c1045e648b49ea2<br>SHA1: 3abff9210d63b8ccd45fc2f36705ca35c703e049<br>SHA256: 558e899f02399bc017897899f3c60e59a7d38482564d3e0f4f42c9916236b657</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>172.0MiB (180.3MB) – 1,793,441 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d371661daf1b515661d60bffcee2f0d6<br>SHA1: 620704525447f7542359b10db6d09c97f82c3272<br>SHA256: 4af32a813a8929a5fe2beacb2747ff920760a342686d9d5d24f3f1fe1c916308</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>166.4MiB (174.5MB) – 1,793,441 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2e3a69d2ac2a7d814d722bc5a90a162<br>SHA1: 995489d76ae7c6be6d425b285941581107771fdb<br>SHA256: bceb9aa9182fbcd17d01a0d06979685947fbb4b17c44dd53b3aee009260e4b4a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>166.7MiB (174.8MB) – 1,793,441 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dcb8f44e061493e8bd2c1841025a6473<br>SHA1: a351e165562395b068bf0f199ed3c0adf3ff22ee<br>SHA256: bcdafc8dd419c0a17eeaa93fcc247f426b0b9d6ca4624f800ca9076072514a14</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>184.0MiB (192.9MB) – 1,793,441 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a469fca122e71db2f366665e42f9f857<br>SHA1: 6c95940f75269bc684fc6cfe1598da6a6f42aa47<br>SHA256: cc4634a5a7bc997b7eefb677b7a15fc5ff0fb46ac10c4cd16a510536c0f7cc3b</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>166.4MiB (174.4MB) – 1,793,441 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b5b34a390d53e1fbbd72baf2a2940d2<br>SHA1: 2cb6e2fff6fad271926cb7a2d038fef066e626df<br>SHA256: 428b839e31a9bb8ca3a10ba9a13d86c34cea9f7bc2a6f801aa7bcd837a378c99</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>184.9MiB (193.9MB) – 1,793,441 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0344143f6753d26aa36b1ce45ea0309<br>SHA1: 371fa51215d496b02e9da0e5c025a1c563140ad1<br>SHA256: f5adf1bbebee96bd9d42cb30ac663b04116fde0329dd86f9022ac8f3aa3129c7</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>170.1MiB (178.4MB) – 1,793,441 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8464ce159de87cb5543be0201face5a5<br>SHA1: e6e913e9fd32f90abd778f13ceee3ba66e137ad0<br>SHA256: 2f2b936e9301b0de674595bbe9cc8ea66441c8da504d523537630a16404e1392</pre></details></small> |


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
