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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-06-22<br>IPv6: 2025-06-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.208MiB (6.509MB) – 310,893 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecf3b0827519be7ad521fc975d773eb7<br>SHA1: 0dce406a3749db6615de90cf9c7c103faf034260<br>SHA256: 6a3a6cca91165149b6cf148f8f29d25c9547262af8f66db0e1e91b077d1b3362</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.20MiB (12.79MB) – 185,433 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63e613e7004f1e7b2faca3bedd0ca793<br>SHA1: 642c2cd8d09e9038f7424c95303fdfb65cba553a<br>SHA256: c0fe6c1604149b0de746f58c73a738c8c747d2c56e9bf95f8c8c605559af565e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-06-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.31MiB (12.91MB) – 616,108 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9d4915486ef77c1a1596c99c0f4344b<br>SHA1: 02bd8e4ce74451eea03b72869b9012c64e9eb16b<br>SHA256: df81043942779aceb3a2ac56a6382c595cb60592be844c5c0a44504dc4b5953a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>85.03MiB (89.16MB) – 1,292,115 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1426a24c5db08fe5b2c826ae98aa3d7f<br>SHA1: c2cb44d6fd257c18d1bc562d962eb1a533620a5b<br>SHA256: f10746e3a90d3033e3a2dc4cc8f140678371f8ba7aea6fb0bcd6b449260f201b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.020MiB (7.361MB) – 352,022 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5d6ce30939ecacab9e5fbbde143dd7a<br>SHA1: dbe45e91ef39b1de3ae5caecefe6dce72faff5e1<br>SHA256: 843f29bd3db6468809b0042da7a6b44aa5aa0f7b3378bce2344b427d7b8b2458</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.50MiB (17.30MB) – 250,746 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86b9bc39132e2d99653445ab24f13e89<br>SHA1: 04cafe97346c96dfaa2a0c192e271c1aa18bb99e<br>SHA256: d337bc1e4ec66010e25e0e0279f489bc7bb3f2218829c1b952e7b21620faf6b0</pre></details></small> |
| | | Full Location | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>189.6MiB (198.8MB) – 3,310,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1255823f4fa6d96cb2339938032ec17<br>SHA1: 7bcb7165d5248f918857090fad507b3b62aff99f<br>SHA256: f33143e90c472ffeaf3431c1f790ca9297c4fcb75c4f9b48690bbe6cb9d79c80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>401.5MiB (421.0MB) – 3,898,653 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50981857bc3865133c307de9e8f457db<br>SHA1: 915f84f9ac8ac491a0dc82f8e1c8a8b51e82b9eb<br>SHA256: af893c4ae1cfc50fe6b043a92e1ececd960d30f00aa8a0067646fda960aa8ddc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-06-22<br>IPv6: 2025-06-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.060MiB (6.354MB) – 306,250 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66813478af08592fdfc48fd31bff150b<br>SHA1: 811a9109b04c7e248ec3039089a3534799a0b45e<br>SHA256: 7438026d984ce77dc6a3c83ea0623314e8e04ce52f031ecb819c2211c10dda60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.18MiB (22.21MB) – 321,882 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dc7e513e52e0755f6fdadbaacc17b5a<br>SHA1: c9ee76ff47638d91e8db56f68fe6b0d1ca2f6cef<br>SHA256: 35bfcec7d2598e67771e9d918023c4280f9109650acfb7bc6d7776c000fa7505</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-06-22<br>IPv6: 2025-06-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,073,788 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5842c1e89d9e6a7ace62a726c41126ac<br>SHA1: e3950375fff9f4e7a1b551e841a320f17e1763f3<br>SHA256: 136c0e48f44d563e0a01829656f7c14024757ccb342856959d0a6797ee9afb85</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>243.8MiB (255.7MB) – 2,366,384 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e93be5d64be521626b8e98eb9c04690<br>SHA1: 8491599042ab2c0661a6d9968a86b0de5322e2e2<br>SHA256: 699e1f5782b93d7acd864659595c72dc1e8bf20e3457b3d9fbe5503103a35841</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-06-20<br>IPv6: 2025-06-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.25MiB (12.85MB) – 613,461 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5b89364687897da08755f6e8896a80c<br>SHA1: 999475f0a5f3ab0bd2ad1878fddfdb4861afc802<br>SHA256: c62fa515779eb33d11a6e3871c117d85d003d0cde1bde2a8b5bae8a5fc69cfc7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.32MiB (44.38MB) – 643,198 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0df80e61f6d2b5152a9156aa98dab564<br>SHA1: 6d8cf6c53feb795a771beeee48249b0e7f268b05<br>SHA256: 9f48693932a016de1867e5ee0367635c9f954b44deb3b30b0ee1e32f45a2fe11</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-06-20<br>IPv6: 2025-06-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.1MiB (181.5MB) – 3,415,229 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d9929c758f8d493aa8d4e500ec169c2<br>SHA1: daefd28894806c92908a6b33694133b5f22184c0<br>SHA256: bc3c63107cee3d6eeb875b451c9d5cb65440d3bc002bf683affcbbfb1eaec992</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.0MiB (192.9MB) – 3,415,229 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b6488e3de7533486f1d93dfe6f2e7ce<br>SHA1: 11790e8fc17518db5859a4d1e4c9de951c9f8c2e<br>SHA256: 47d415b26a7500bbdef561f0eb2d0540944f85a3e1f19be400a77d186bdb7428</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.3MiB (180.6MB) – 3,415,229 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7829262c706725c14e830f7491cde8d6<br>SHA1: 767eb7ecf3018e78a3911b6b7f74129701e1be6e<br>SHA256: 3c4edd4f30e8309c26ea200dad258bdbe00d28c39a7a86aa892ea207d3c58580</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>174.8MiB (183.2MB) – 3,415,229 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa0ae31b902e247e73a44068a3cd4356<br>SHA1: f1c80fea578851740aeb77b96bb6fcf131da82be<br>SHA256: 8bf937f5a917469d7c71ef2fe7b986473d5393eef41ed735e5b3b59ae170c4fd</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.3MiB (229.9MB) – 3,415,229 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 242fc2c8a615627dec266e66642b72f3<br>SHA1: 1e25e414dc84080a8ad10510414ed932ea4f787c<br>SHA256: 8a802913db02e4d131f0203bd1111d9facb0b494e61419b7dd5ec44576bc968b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.8MiB (180.2MB) – 3,415,229 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e964741e739f76fa6180fcf46dcd7f09<br>SHA1: 4a5bf963ec2d306b0c52a2c499354ac92941e8a5<br>SHA256: 186f47ffc555972d9946cc1174a8454f32fe5a955d63c39182166bf0dd9f6690</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.0MiB (223.4MB) – 3,415,229 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 015adc341e8f33b419bae055f24c9686<br>SHA1: 5765bdd9983a3ebd51f47ff917acab87304bcc47<br>SHA256: 1e21c777b183d1d2fc1c4140fc841efba7d2f6b188092624b57d2dcab21b4adf</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.1MiB (187.8MB) – 3,415,229 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b846d76db085a7cd1e22cf712be02b1a<br>SHA1: 3ed944a519c882357f984fcf439d41b54610f453<br>SHA256: abd3522e9faea130d27d793a7cfb45f66198950e3b1735cf2bb1e2e57d7b8959</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>179.7MiB (188.4MB) – 1,908,225 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 707fc24185d89aeb7de426a5f1572709<br>SHA1: 20e405b1c6c6c75350eec0e1a3853b96a4dac002<br>SHA256: 781246ad54ce90503fa9bdf3025d8bd4ce8d850f707b67f7d527faeed8096e33</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>183.7MiB (192.7MB) – 1,908,225 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e52fce09d7246fae729a15d82ea04196<br>SHA1: 60c838f24e54f11030902544a3e464f4d692fdea<br>SHA256: 659e6c69db6b7d39abedd89254431ab28e11c607c82ecda977a5e947f1a3194e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>177.9MiB (186.5MB) – 1,908,225 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8daf20f99f569d729d4a24014520e172<br>SHA1: a3153f73cfa872d4641ba323e24b84888395e432<br>SHA256: c65105eb64812e83066cf085da1b02acd95a3ebe43fb6ddaee36163314fcfdaf</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>178.1MiB (186.8MB) – 1,908,225 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f2e1b47f16cbfe15168e67853a545d9<br>SHA1: f28cafd07c8e79f0cc3bda1714aec50ac32bb446<br>SHA256: 7f51e84d6281865fd2b373de7ddaec2e280f551d03e07ef55efd53c429f55fb0</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>197.1MiB (206.7MB) – 1,908,225 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e89328287e354facc3138ccc292394ae<br>SHA1: 6a79905db4fff13629dc439ed5cf24cfaa3661ed<br>SHA256: 38fa1e7842d829147c4c4bf0bfe427355b48d79f174c270868b230610f6986f7</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>177.6MiB (186.2MB) – 1,908,225 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfbbe8063fc468a8bb0790667fb1972b<br>SHA1: 9589e982ecf4a660ae91cee09d6afd77eff7a2b1<br>SHA256: 902f6fe463d52d5ea22a46e5ecab10ccc9ec372acbbb38cf43d2d2c2c9dc7368</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>197.9MiB (207.5MB) – 1,908,225 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f92a82c9a644b2f743ac680f7f6b0d77<br>SHA1: ec2edeb6b62c73e24918ae025d243f421d5f5754<br>SHA256: 06af32d1a394ee5d6ef3533e08aa0fa2ed14a9ce09d287e15a53c4eaaa4dc476</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>181.6MiB (190.5MB) – 1,908,225 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e8a6cdfabc13bcfaa8f28861ec423a2<br>SHA1: 438ce5a6cb53d0d4dade0ca6bad6dcd8942b2274<br>SHA256: ffa7881465edac9cd904b72c6c55c44a5ee71ff8a1bc069b2df018624af8d5a1</pre></details></small> |


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
