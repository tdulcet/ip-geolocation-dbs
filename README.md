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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-09-12<br>IPv6: 2026-09-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.528 MiB (5.796 MB) – 276,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d46d361feb043267d951e0e9bc6cbbca<br>SHA1: fa71caa9afbe51d0e60aae4be25fcccd4fdc86f2<br>SHA256: 262380aa4b0651b83736559fb2a6025355c7497272bc43a598926bc060c600fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.69 MiB (17.51 MB) – 253,708 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcdb0fd6238d911da462583f2f42b5b9<br>SHA1: 5ec3bb4384a512c09a0cddb0b997ecc58e935b1c<br>SHA256: f068d06f9406a61b4ab9e6d0e7e3115392847e2a4923e845401a4efb80b6ba87</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-09-13<br>IPv6: 2026-09-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.132 MiB (9.575 MB) – 457,262 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95a244bcbf6bcc7448c445820a6b9a56<br>SHA1: 329534c88502e439ab54d810fb0e0b2150aef09d<br>SHA256: 91cced3fe62e82e0feedd463bba44f82dc60df3814662ac9c5e1da145b3e6bf7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.017 MiB (8.407 MB) – 121,954 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 228d854ce1072afe84eb1b6b85799cdb<br>SHA1: 1b02447de73da3190911207583aa7af4a3f4b9ff<br>SHA256: 34272422039b749504e6cc76ffadbacc9e94bbbdb19c0335959316b504244086</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-09-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.27 MiB (12.87 MB) – 614,485 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3c6ca29d03bbbf2bc04482d6754b81a<br>SHA1: 6476855dfe9aba6f7be5a3206774b8e69f766dfa<br>SHA256: f5bc2cdfe1e704f925261b430313e646854935682daf2ba0705ae029df1515a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>51.09 MiB (53.57 MB) – 776,413 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac09b1ff4c0dd8668c61859cc53c69c9<br>SHA1: 24077f3479cea1e33e69b930b95658bedd328a05<br>SHA256: 0a0e98f7750bd32a9727fc3f272c88fb70f33222897f7bc7062880d92b8e4b80</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.133 MiB (7.479 MB) – 357,311 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c47fd01af8b18cc1d5cf2004691771<br>SHA1: 6b08ac2e1f8b48e55e72f8ba6ea0079e50a1af12<br>SHA256: 63aa3454aeef9769e4f0d68b4b93b23a7d195199a50487f4db5d258d90f8b08e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.68 MiB (24.83 MB) – 359,841 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ed7b2550b03a35e3bcceffa4ff9516e<br>SHA1: 2f8880592eb4dfde0c92576fbc78417988b521fc<br>SHA256: ecd35f269cfec0024d6ea639910b54c657f3f1dc08ab339c3d0b0384ed3cb607</pre></details></small> |
| | | Full Location | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>204.7 MiB (214.7 MB) – 3,588,539 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343b463b14a760e04ccbd188e88baa4d<br>SHA1: b7e446f674922e349cb17f01c859bc3bd62fd5e3<br>SHA256: ba1847bf8c90ff7f1ab0a19c20aae3512e9bf7a3f144673fad5d87dafbf7780a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.2 MiB (449.0 MB) – 4,160,441 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2542313832b0583d31e84cd0f9afbfe8<br>SHA1: f2d167034376bc0d28d3f5a38fe3c15945c4ba61<br>SHA256: 9c2aa7d6132f5be8f547273ac5e8f21c074f3d7a26b3f7795c642f4a3b6a9693</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.693 MiB (5.970 MB) – 284,967 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97d1441c258db85b80d0e10e763efc3a<br>SHA1: bba017e67350bbb91f08c10880ea6bbf6075ce56<br>SHA256: 9f5f3b2e3fc347c2c22172f226a573570d8ea695da978d00eff31b6ec4c0bcb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.63 MiB (23.73 MB) – 343,947 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b535c7a01e55c212ad6026f97094c92<br>SHA1: 48d55f71ae24b9f77ed2ef0926558ff6cf80dc3d<br>SHA256: 864a57987908eceeceecd3527d4e34630a58ff489bc5b2f73ef46eeaaf2f0e90</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-31<br>IPv6: 2026-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.2 MiB (177.4 MB) – 2,928,511 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ccbf72a4307bf248403aef0a149708c<br>SHA1: d217e8012b6f3ce376e14989cd982f9ac5ce09e7<br>SHA256: b13b48ae2e8f41dc7d68a5dc01260dad043b4d119d3facdfbdb8af15a20226be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>302.1 MiB (316.7 MB) – 2,928,220 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c526d9a3e207b31b76b3907454601b0<br>SHA1: fcd803fede475e876008bbda8d9640e03c187231<br>SHA256: 1f6a62357734817fd3ced380fd7dcae8e1b8636e8143e3169f12b64ad522d539</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-09-11<br>IPv6: 2026-09-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.25 MiB (11.79 MB) – 563,211 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83ce2a7d76005a4c4810d3568aa65268<br>SHA1: 6a73065b00df7fc78614af3af2b282435936743b<br>SHA256: faac40a35e74a88c33d39cf2948437fe9e6e4a0f07e19d944a356bc714461395</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>34.19 MiB (35.85 MB) – 519,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 130760f2a08d6922cbb3148f5fae5715<br>SHA1: a02dc694751ebb88f5d89dcc990f38aed4f7540f<br>SHA256: f9e414390c4bfaaf6a080ba4cd13fdc00a6e70f5ef69770bfee65ab14507c075</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-09-11<br>IPv6: 2026-09-11 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>191.2 MiB (200.5 MB) – 3,725,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 400445c496319a4ee57d887d863ad115<br>SHA1: e0aa2f9beb16d87ca9198bbedbcaa7f6c9ce4a33<br>SHA256: c827a1e8c3ddb00ae8c5aeafef4c55d456c4396b6791578593caad5e74c7f435</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>200.2 MiB (209.9 MB) – 3,725,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dca2885367fe3641d44f2a4c3400c43f<br>SHA1: a35d5cd020b91b9d1fe9d85bcb015a7832aff831<br>SHA256: c313c19a1cb74b81766eda1cbbb80fe039e79ce21ebee4674eecf7d9a7c56f85</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>190.2 MiB (199.4 MB) – 3,725,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 480780b43d195b3fb055ef4a1d6eaeb9<br>SHA1: a8337187e4d9b5888c0deb46ceefcb5a583da160<br>SHA256: a08f8a356f10a003938869741a4811eaa2aa5310dbb3fc62a7a89d0edf480688</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>191.9 MiB (201.2 MB) – 3,725,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54d45f88f4b4d79375dbc3eddbf6a461<br>SHA1: 20897e796f22abd822cb3cd325d4906354e7d44e<br>SHA256: 4e7fdc9df6bd25a7244561ee2b64f99935a38cc0fbb4cff67fc5c3550dc6bbb5</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>241.9 MiB (253.6 MB) – 3,725,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bff82c98119a38622342d19d425e4a09<br>SHA1: 5352e64fb2fdbeb7f947b6e3f049df25d11b165f<br>SHA256: 65da7ff5515d81a568f538f3bca76c6182d98e1bb21f6958a3ab5d7af8e61bf8</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>189.7 MiB (198.9 MB) – 3,725,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7266a6a6cff625719b8f92dadced1bc4<br>SHA1: 70f775050a7ee6d1250b3cf75e1e6b7397f8ddb2<br>SHA256: fd2454868734ffc09264b0c9c7cf673e4ad0e039b15686b2d52f42a9fa25019a</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.4 MiB (245.8 MB) – 3,725,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aab8985e4b46fde1e4819653780506bd<br>SHA1: 407ff89c9e004b92502ad2d11c47e75d42bc1b39<br>SHA256: 43941422959247c5ac094f4651a9d9a2fa72799a4fdcb9cf8132b8558832273c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>195.4 MiB (204.9 MB) – 3,725,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae2f1c8477de913eb5156c2422c42c12<br>SHA1: 1af0e618f66265383ed52f309f9b4f47ec7dee73<br>SHA256: db5fd1563ff6257915793cc4d64b285067476706d9e3af07955cd728691015c5</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>201.1 MiB (210.9 MB) – 2,104,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7c7c75f78f66d15a333a4000686f886<br>SHA1: e2fe2c14633b7899ecc536f257079dc96c215501<br>SHA256: 6182d4562d06d03ac2a587ac4c97664dc22a10b1a2f13ee3bc6bc8ab6ffa25d7</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>204.4 MiB (214.4 MB) – 2,104,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a2f7237c1584cbeaaf2f16990d0cddc<br>SHA1: 4e446a53992400dd941a22f015b3a23c507ced04<br>SHA256: d3fe8b4e0569b2579d52723bb229c56fe7b6ff572ac14fb0acaf7e4bc1b61bf1</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>198.4 MiB (208.1 MB) – 2,104,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 557c1f3d320497f78dbc00707a095d9d<br>SHA1: c150be4cd1c882c9a6e1217f7b5718d08588f44d<br>SHA256: f7a6bdab7b2f0111ee1a8eac91ab565cf59a7a7f00609c6a3897d09de82bac24</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>199.0 MiB (208.7 MB) – 2,104,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c5c686c4a4a8b851840eb5e89b6137f<br>SHA1: c91ed755000d0f8a9c46b6e9b13272eefdb9f198<br>SHA256: 675eb691f3ed96ce208654098d9c491304af0380d727bb441a63740fd78c6855</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>221.8 MiB (232.6 MB) – 2,104,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 245c244163f645f9088827b6598547bf<br>SHA1: c01e3bfcba9434ec3d3d534887871852499c289d<br>SHA256: 2e69b8eab3e7b2b38f5a1d6793fd125fd21da54865e44e57b2fc4fe833df0606</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>198.5 MiB (208.1 MB) – 2,104,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8364953c767107c18af4b45ab269bbdc<br>SHA1: 36e9efe3f48eb171e2d98fd368af0ddf8647a37b<br>SHA256: f0a58bc762b638768f3c164288b161d62ce9dd7154a92669550d0db8a1b9e6b8</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.2 MiB (231.9 MB) – 2,104,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a4f1195bf7c7f54e5640c62775922db<br>SHA1: ff943a0c97015b5c0da7faeed10103497aa50af0<br>SHA256: 4712ea11c162a0c65d8e5b13ec586d14a9cf616d7f7a5740a2f78fde4cbb9947</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>201.5 MiB (211.3 MB) – 2,104,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 538d32d5658493341a5cf8b6bd562a8a<br>SHA1: f92e3547a7ae0b813797e09ca94d41b2566cb439<br>SHA256: 37cd9ad31bbcf974e2aaed3492a78882ab762cdfc11377a45510ae1b07217242</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
