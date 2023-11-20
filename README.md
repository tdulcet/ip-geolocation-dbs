[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases are scheduled to change from CSV to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than one day (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-11-20<br>IPv6: 2023-11-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.600MiB (5.872MB) – 238,548 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a835701c08b41eb9177ed44d127ebad<br>SHA1: 937724dab4fb9420bdf61f289e3ea75e7d962ba2<br>SHA256: 46d20175577150b32139e2cf31cc3770e3ad521ec9e70ce20c737e67ac64423e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.315MiB (6.622MB) – 81,753 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9635314f4446a700b3c32c4bad32e0f9<br>SHA1: d753dc10aca0e84d83c8bdf3ce7bf7a8c20ab621<br>SHA256: 0b28c53d4662716acc009b00b14a74d993de38f741c91541a05fd6fdaf97be45</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-11-20<br>IPv6: 2023-11-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.661MiB (10.13MB) – 410,354 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d641a327885b742f7ea3e235be8f491<br>SHA1: 4c157039e53746bed40612ff1ccd03849c05fe81<br>SHA256: 8d494d1188e137d958a2722d509bedc84672c8a3b96a77ec400498f0c12158c4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.038MiB (8.428MB) – 104,153 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d215f7aaeb7ff9a617e8fc622c92a62b<br>SHA1: d713a32a6a538831733e4805d7c821162bcec33a<br>SHA256: a381c28c45bf270cbae4588b60779ff6bdf4a46c2283a6f6b80250fb8a6445b6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-11-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.94MiB (20.91MB) – 846,641 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3231dae5445a09dbce50b4e08959e6aa<br>SHA1: 266283e3fb7f4c675e0b35cc7e258feb899b8447<br>SHA256: 3c2a5d5510b320b70b57ec111f1adaddb50c90911e92adbd7c52e1ab8506ab19</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>103.4MiB (108.4MB) – 1,338,413 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfe0012dab226b6a94060cb36304fcf2<br>SHA1: cb92d7c01a42db7a7833f4819247b7f3d5ac1592<br>SHA256: ab82c6847a319b14a8fa3b08eff9bd65f22704942cb77662cd3d61c197c57a2b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.260MiB (7.613MB) – 309,964 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7fc3106cf6c65db7d44df8b4fb1d16<br>SHA1: 6ec97588db0af32a305835217289c32883d23f64<br>SHA256: 9bc7152bcf323316fc78e69cfa190cbddf22834208f48cee2e624c18150c9478</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.63MiB (26.88MB) – 331,798 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264a68f442d85aea134072d7bca0f4fe<br>SHA1: 65171ab00588cb7f2ae029d9345b44cccc888d24<br>SHA256: f76d40c34e6881d9cf3d98b34ced8105e9bd9efbb3f55e2bc224ece181569030</pre></details></small> |
| | | Full Location | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>186.8MiB (195.9MB) – 3,075,320 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96e5fc94ee00f3349281d3d79c8e3e83<br>SHA1: cf6b55598525f02890d9596fefd546190401adc9<br>SHA256: 5dfdabdba40afb770f6ff5afcc35db6136e9e28182bd6b3fd23b3c203dca5d1f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.3MiB (303.3MB) – 2,504,397 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bcf1dc4f4611d3e39906c6048aa8fc<br>SHA1: 2cd36733f3043bb3d9985d20fa8416a68b122e30<br>SHA256: e3d5ccb9e02dd929dc48ad40f82d484f9ffe60f9098c5a3ac296e33c5b9c2a9e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-11-20<br>IPv6: 2023-11-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.446MiB (5.711MB) – 232,323 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f7d79b6a3ef8bc35c3c8381e7c028<br>SHA1: cbc8e9cbd5c151f0cdb02a21e5e6fe9d8b662cc8<br>SHA256: 9f3976e09ec875d7e97185503221656e80f41f531e268da1bbf874127de2583e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.41MiB (20.36MB) – 251,316 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df2ea3be7027267ebb1947b4220cc4b<br>SHA1: e94b6a993297b5dff456113130c22e323534e39e<br>SHA256: 44458ed651d7b4bd99ad73459d500395c410da1b2fce9fbb2c4e5ce318c4bcf9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-11-17<br>IPv6: 2023-11-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.75MiB (11.28MB) – 458,946 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2dd86a68d8a3064e321d9611aa6bcad<br>SHA1: 0313b838fc949bcf0cf2db23fe1334a40d0c2f43<br>SHA256: b5669f61840aaf9784e60cf78054acf8d2124f04c23a943201e4db9de6c2f973</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.85MiB (23.96MB) – 295,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a57543d99b5e7ebb8c6bc7e972d3bfb<br>SHA1: 1aee4cbe30ddfc33624229cea08700f58765f98d<br>SHA256: ae5eb3083c5d5752c784f327870d0c01ca6c9dc082da52f29b87a268ade1c670</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-11-17<br>IPv6: 2023-11-17 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>160.9MiB (168.7MB) – 3,190,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 722265f5eaa9f771a13465da452bd50a<br>SHA1: 02e91b50cb91840703b7dbdbdd85afc6d9f8b9ad<br>SHA256: 3e006d8220d80515158b485819dae5607d2e94dcf8bf96276841ca2a1a3b47b1</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>186.0MiB (195.1MB) – 3,190,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c552704e18c0e7f335800fd48286f19d<br>SHA1: 3076c00f962b2d23417136a41e291aa4f7c78e9d<br>SHA256: 777f9df8c0c707a45512502d587fec9e79cf97c799a1a6615a985559cf8e9153</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>165.0MiB (173.0MB) – 3,190,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 693813b3bcf2000e19dcf76e2228dc1a<br>SHA1: 7804daf14e9c8dc132c7da28fe1c4732334901d4<br>SHA256: f256bb1cf83849cee77b1149f60e5930a2bd72233024634311befcb2ec627715</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>171.0MiB (179.3MB) – 3,190,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6a96fad3e4b2d0203355c46ad4722b4<br>SHA1: 3a21435aaeb0950a9df62b923ed93a317e89e214<br>SHA256: 351f751066dc7af0e1b5e21f3ca5d1b137808f008e72c4c0b8c8b3e2503a8f0e</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>195.2MiB (204.6MB) – 3,190,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d89beb5c1bab499915465c9ffed09f4<br>SHA1: a231e43f67a71168b09b6a79ca030fa1535d56d8<br>SHA256: 3e22c63f1ade3b436252b3a8f200053896d5ce6dd4394e9ed1dac714e4312cfb</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>159.9MiB (167.7MB) – 3,190,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c2aa308fab0927b1ae66ab7587abea0<br>SHA1: ee1948b422c3eca9e14ab03aa63af7f91ccf1c6a<br>SHA256: e6bcded028999a4d17265bc1be626122e2a262e10aac2c4f889a1fd19389c875</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>196.8MiB (206.3MB) – 3,190,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de1be56ff3480a75ec804891e4d05bf4<br>SHA1: 5f61dd8b6b73ee4a645ff286cf5505bc7bc375a3<br>SHA256: 4db33f28301fd150277d00bce2928cfe6078c525524dac7e78bd04d77aac55b2</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>166.8MiB (174.9MB) – 3,190,468 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8afb0d18c550c04f7d4d49e54fda6ae8<br>SHA1: ce8478bba78ad434beca885633c17b3000db4c18<br>SHA256: 1944b0dc25088d68877456c4a3d33f5ede097954eaf9ee605331f72a35f01bf8</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.1MiB (131.2MB) – 1,244,193 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51c4a942fcc436ebbaf90ae015ed5adc<br>SHA1: 2e2316ab60c667f14af4a74105eb03866cfc5fea<br>SHA256: 882f7c7dace562a59c0d95d271f0c3b8b6463c9835706a22c2f7f40c83420e00</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>133.1MiB (139.6MB) – 1,244,193 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cbf1887e7ce136ccfb56cfdeba3c89<br>SHA1: 5fbb763315b6239a06612ce4f019e1766e848cad<br>SHA256: cc2ffd2c0258a26d083406898786de61a19a62c8d583fb4b0bba71242967b7df</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.4MiB (133.6MB) – 1,244,193 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f0c8eef0b5cd532c5398f81add9adbf<br>SHA1: e493dee9d77d7aa7ab9f0e79185f4609d6a7da3e<br>SHA256: a38d1342a27dfd69762d431c317541e3db5d7a729f4b0ace3abfe60835fdbbcc</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.6MiB (134.8MB) – 1,244,193 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2498366827e2867868429ca3d33e6e14<br>SHA1: 685373609d05eaaba571e7d30608971d6ebe576f<br>SHA256: 01a7cd48d07e179098cedfbf76266f0e73a3a8a58546f159283a4772d83d9099</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>136.3MiB (142.9MB) – 1,244,193 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33892657ef0dd7dd9fac768404dd8632<br>SHA1: 8b8a68195a78e524bfc123dbdaa30751a8ae2cd8<br>SHA256: 4ff633d4f63fc3388c82cafca69c1db13275b66a57717f87045095ae59352bdd</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>126.3MiB (132.4MB) – 1,244,193 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62d3f4960633ed789c85b9475b853541<br>SHA1: 54a7c23f40e2deabb910980a326e408f0aa399de<br>SHA256: b9c829a0416147fd88e2ee403ecd9065e8fae97e3d1c857007e55e3b05c1fb1a</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.9MiB (143.5MB) – 1,244,193 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aea1d9a2e43aa440cdcc017c1d63b119<br>SHA1: 58559b1f7ddc69b460bdda3472e3ea970eb150c9<br>SHA256: 0ec99471a192ef49e33fa46b6f5ad48454da5a586d8095121c57d0848e618cdb</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>129.1MiB (135.4MB) – 1,244,193 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee603ad283ab37bcb3a42c75e88e5f5c<br>SHA1: 0593f30f4b6822245d45367590243940516d07ac<br>SHA256: 5d3a122956edb5e560b28259edf8bb9f17eac89d9f21d0dbfe81d09f87757eb6</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hexadecimal format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
