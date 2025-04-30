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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-04-30<br>IPv6: 2025-04-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-04-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.08MiB (13.72MB) – 655,066 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5af156eee8bfaa78b4a7370ebd92d08<br>SHA1: 6e71eb5ef072aff2394ff36c4808c4b73939ef46<br>SHA256: bab6016f05614a22c200acb00287b06333f6f13ef8f279e7e7e0b153bf9d4fe4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>116.7MiB (122.3MB) – 1,773,046 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5ee017f82693240dba4c250826f0751<br>SHA1: ca3e18e1d493fe138066c04f2759e244fa00bf13<br>SHA256: 45ebcfba87a25e61ec070c2e93ffe197ca8490266a066c176fb4342232dc178b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.260MiB (7.612MB) – 364,239 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6323d2ba185e1b9f3ad0f50d801a0f9b<br>SHA1: 16dc5d7ebdec40f2baa1d88ff7da010f59ac4497<br>SHA256: 293d6b40260235648ef04252b1d8933a3842ad77a8607f652586afd2f9534788</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.00MiB (18.87MB) – 273,546 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37e18de9e861fe6195c241addbce73f1<br>SHA1: 9b8025c07ca81352106f1f9a175f775581401bb4<br>SHA256: 5db20ec85f5df35a151ed3c5ad76bf218a2300bc443256e8fbb3a6321dfd1752</pre></details></small> |
| | | Full Location | Monthly<br>2025-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.0MiB (199.2MB) – 3,317,593 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2a1c4fd3709a1baa228a86fb6349eeb<br>SHA1: c5a710b509cfa7705e5aa4218167fcc793e610bc<br>SHA256: 358704998e340d2bd6120c6444b163e0e82cc6fe6d878e10100bd8de1eaaadd1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>394.3MiB (413.4MB) – 3,829,626 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be29c6502d46b9e480fb67d922e01ea3<br>SHA1: 02aec0bbf94ec53629be9ca6f1b6892d6b3e3769<br>SHA256: 1b33864ca1bac3f19cc64c993043c1d499502dd93f4327636b4996162189a533</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-04-30<br>IPv6: 2025-04-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.948MiB (5.189MB) – 247,660 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6fe91411896d2bd0850805b7a989ffe<br>SHA1: e174beb80e780103862f29b6c94af9e0ef9177bb<br>SHA256: b87a246f35f8ab19000e4b03570a4f4ecab3b39030a59f3a0aa85ed1d9e08881</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.21MiB (22.24MB) – 322,286 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b00218e174dc90dd477d24f62635f15<br>SHA1: 0ab3977e561a987e0b15d1a8be0205ebac054d5f<br>SHA256: 36edd6e07b549795deba3fd441761515c9b3c1de7473204e1c404450d0d55912</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-04-30<br>IPv6: 2025-04-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.0MiB (182.5MB) – 3,014,341 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e5928c437bc1359f10928eea58d53ac<br>SHA1: 56e6f902c05b10bf03427836d717eb319b757e58<br>SHA256: 41b1b08e0f3d5f222ba4d3c8fa9dcf3dc9a59cee01cc75e498a51bb86544fbc1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>241.3MiB (253.0MB) – 2,331,339 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a21e885b78b78cafaf3824ba7bf0c642<br>SHA1: c1752c9a4f5acbc2c70be89ee9f7ec75ac016871<br>SHA256: ccd89a113fc7eef739896cdbeaeebd590070c9dc4febf6bdccc49e105e5d022f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-04-29<br>IPv6: 2025-04-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.64MiB (12.21MB) – 582,930 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7eb1e9417c49b8164f4f0f4194054a2c<br>SHA1: bb561bdb5e403bee1f7ab1e4e59c6229bf8a5969<br>SHA256: 30d8af8d3ecf6c4c0b82fb938dd14c0f4679517caf71726c9d75fe6dc6254a2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.12MiB (42.07MB) – 609,672 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: baf6d048961a312dd90cbb9cc84addd3<br>SHA1: 4d23057595ea618e8dc1c60418454f6bd6aabddc<br>SHA256: 3b6e1f87760897b0136264fb936e120401b0a684308297687e68a404b151be9b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-04-29<br>IPv6: 2025-04-29 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>170.1MiB (178.4MB) – 3,358,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7491684179e5431a72bb52e03d135d2b<br>SHA1: 143851b1d772d45b53847a406845c19947b37ecc<br>SHA256: 49d0bfd56ae51f7b288d259293389cc17a6fc2f591d019d6d44cb85d072028a8</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>180.9MiB (189.7MB) – 3,358,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7006424544ffb99a31f2d172df5f3704<br>SHA1: dc3bb16c2acd11442c5d636def892f2cd25e8f80<br>SHA256: 9f75a5632a1872bdff48d0aee6ff0174cae20766855690ddc6425772dcc26088</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>169.2MiB (177.4MB) – 3,358,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00a879922b7c2a2dc7520f0f1e03174c<br>SHA1: 308e2a12c649eb6b9dfc139230d042dff0d67849<br>SHA256: ac99b4337d469c251891efedd4f190b237f9a4fbe742649eeb3a60df2f7a62fb</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>171.8MiB (180.1MB) – 3,358,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c59d0fcf0caf6a7d75a85e9d60374a9e<br>SHA1: b1f39f8dafa927f33320e2fd491f2d37250b3a73<br>SHA256: 9434a411500ad4cf3f69e558d3a1dd9a8801b617624137a846cbe08126493917</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>215.4MiB (225.9MB) – 3,358,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 770a2c63d536fb588aa2f4abe4d14ebe<br>SHA1: a2eb6a20103701657e5ab2534cc0658f6fd97a21<br>SHA256: 321690d402abba00f53181c510dd28b48e61b1db7e4f83789831a193a0236311</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>168.9MiB (177.1MB) – 3,358,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af2a09b51930dcc70fda8d1b00601b62<br>SHA1: bacd7c5e7ba3368ebe2aa889a126a0b7531097ed<br>SHA256: e2cafff8bce32354b72c4a7336f2e29fda02354dcdfa58224a08cdef3d8c220c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>209.2MiB (219.4MB) – 3,358,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43646d7665125901f7984b9cbbc7091f<br>SHA1: 1ee18f2847c7dd9ab38bf5e2fb68e309b6901c31<br>SHA256: 64ec70d30942038395bd0fa9fff1f5e79b70d5dd9f54860b09b87c4364afe5f8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>176.1MiB (184.6MB) – 3,358,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f25aa17b74ca27673e206bf1b4aaa9e3<br>SHA1: e77b7805d386bd4841d03922d6c9d6d9914d8eae<br>SHA256: fce52dcbad7a618b58e1919e694058f994c4f562f3654efc42b466a6a7834d79</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>170.5MiB (178.8MB) – 1,813,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6fd27066f172e2d434d6b173a69524c<br>SHA1: b0e61f849a7ea7daf8f5dda38d945b5b8eb8eacf<br>SHA256: 0c0046649ea7c69f04895603902d72418e9ab5a5dec4348f23c5b294e288fbcb</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>174.1MiB (182.6MB) – 1,813,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb7ef1f8b7097e9381203a8965357f2b<br>SHA1: 71ad0a092000ecc701212f0c79b175ddd3adfb5c<br>SHA256: f708b14b0a310046d30f1798e61c6f63268b329864f69ec51270432479365983</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>168.6MiB (176.8MB) – 1,813,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 465c272c8de13a852163232b687fdb3c<br>SHA1: 3a2982c2e91baada1469817836f90ee5cc8a0c54<br>SHA256: 6cad0546a6cfa76140288d596cb5e6c1764a33d2f44ece6c3ba783dd207844bd</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>168.8MiB (177.0MB) – 1,813,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7267e52e4a82656ded2c824ffc373f7e<br>SHA1: 689a6ddd586b2b500ca3507dc909690f6e876728<br>SHA256: 43e99dac64ef74ace970889cea02770b8eb205b9c6b30852ab4dbc8eb1f04b40</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>186.4MiB (195.4MB) – 1,813,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8473218cfd81f6b68807bff2c350cb6e<br>SHA1: 93864de1abdef0917aef5372b53e4b82e82fccc9<br>SHA256: c9ce59afb95812a3c3e088f783d794a052fbfa4fe11abf1dccd305135e96cf30</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>168.4MiB (176.6MB) – 1,813,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 255b6c8a79db19a98b14a3c86a3a221c<br>SHA1: 22bbbc8de9e31ab662e5e9e6a9bbdb1b74ad9dd0<br>SHA256: b166ee12b5ef48acf9fd0de653ef1eb8be3f3e74ba2ce8a88f562c65ce25080a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>187.5MiB (196.6MB) – 1,813,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ace77f0e75301ad7d7cbebbeeb7e45f3<br>SHA1: a08065347ea5f3ba30dea48f61552577dd7c181c<br>SHA256: c8879c61fb8cfcba6f8d8adf6f658ae095037ccb6c2f36774bc0f20dc51c274b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>172.2MiB (180.6MB) – 1,813,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f976c744f852c39659ef4fc6a83554b7<br>SHA1: f9dd0a686117fadbccd790e0f6f4c05239578e98<br>SHA256: 47b176bc9960467134e49c27ea0980b348634c4cdbbc3c92a4b65ddc269ae48a</pre></details></small> |


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
