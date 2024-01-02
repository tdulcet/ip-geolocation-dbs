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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-01-02<br>IPv6: 2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.771MiB (5.002MB) – 238,833 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a34d5dcec4c8898756a28b06909b6ecb<br>SHA1: 78cd6b9a331e31229ff4db42c2d80e5dbd758c7d<br>SHA256: d1dfabcfac3d51cccdbdf8ee635e42c87913e5483e701f63f916c6005c389d2f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.445MiB (5.710MB) – 82,748 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27f5f2f1fdfc0a43d2b0dfcb51f13293<br>SHA1: d4378f72daf1ec3bbad53e1c55f2ae8183ba7c3b<br>SHA256: 15b49ef5e60e260d89fedb23bdfe9d74f442b8c977ead012db625c4b39240f3b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-01-02<br>IPv6: 2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.245MiB (8.646MB) – 412,895 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e9480b1232a959fda8bb7694a74ec5b<br>SHA1: 326b818341f719dc6832006d2db3f2529c04e8a5<br>SHA256: 06497c21af1be3ffc627f5d8fb93be9262ad7f6017a9596fee61937142961264</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.888MiB (7.222MB) – 104,784 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb6a301a431487f7eb54b55234ac54b1<br>SHA1: 5451b4f00bdbd4301f3ab0c46a86ebcb13df2c64<br>SHA256: 9d7a29308d7cc146f57a5a0c577f51f7857fab40eeee54be74d2667f5487342a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.78MiB (17.60MB) – 840,188 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ae7584ffff9ddde1a2c5a9e495aa6de<br>SHA1: 7148547f2888b2c657b541c18ee910790cb2f26a<br>SHA256: 5874405336bc66b18b0a7d26338e12339144037f10067b11e1b64ee3ec7244cd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>51.34MiB (53.83MB) – 780,185 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 431e7b64699fd5dd1eed9e26e611a357<br>SHA1: a9593af3cb9b5446817b11be70124284aa502f6c<br>SHA256: 6610ec5d02033e4761ae88283a6fcbccb27908462c6e5dcbab7904d7d7fa6bc3</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.162MiB (6.461MB) – 308,408 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736158b820db1062b003cfce212076a4<br>SHA1: f3b03108eb0edf83c338abed05e010c2b0e9cde1<br>SHA256: 68e446a0380ab263a21743f68ab8aa6b249b213af0d6ffdac0780fe4912cb7c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>21.05MiB (22.08MB) – 319,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73819723f00de32c17c8aeca84d93383<br>SHA1: 71d954fffd9f9f5979ff89981fcfae6f73cadb05<br>SHA256: 1328a782f89b58d1f6fabcf3542ce4bb259d89c1f28a0cc70abfe70b5e573eea</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-01-02<br>IPv6: 2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.626MiB (4.851MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24caac24a9c72bc3caa6451ceab08833<br>SHA1: aa114043e64d74ecd9e8ccd339b80c62d3fcbabb<br>SHA256: 6d48a0384e6e4d38820ac8d2936c12db7eb726dfe20c59600d4f14d173e3b15f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.10MiB (17.93MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fc970b50f7b01de0d0c6bd29224c13<br>SHA1: cb1fe32e67d0561cefef5f2908570ae3af446a24<br>SHA256: e0f36200f10f817a89b6cf80d8d459900c5428a669cc706af32d15b709a8b624</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-01-02<br>IPv6: 2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4MiB (176.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4104f39d8c379ec8967157286f495717<br>SHA1: 440c75c20491f104948897ce552c95510badba7d<br>SHA256: 6689c6e63153fcbdc00272e2ec6cf04f0c6877860b4a667b3972dfa08c898747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 142dfb0f4dc0ceb4f5a41b018ea53524<br>SHA1: 284b510184f46179e9e34f60dd0db14fc72f3e50<br>SHA256: c57159c9a8879702623a2ef4d0c2fad06d21e96f1836db2d3a09f9216aee1641</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-12-29<br>IPv6: 2023-12-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.170MiB (9.615MB) – 459,327 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a07c5df42de67bb07e5f9b3c590c4d2a<br>SHA1: a53ddd7278ed514651edef388881cf2318f38985<br>SHA256: 959e83420b47f8ceb3ccf33d71f4e39a4e3c9424dd71637b7945f2986b3fb6f1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.92MiB (19.84MB) – 287,471 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e2d583c968a1962b934437229db9f5f<br>SHA1: 59a915b80f2d11c0362ee9d1c7b42c006cfde659<br>SHA256: c410fea0759eed5f6ed49b1bebe55089647c6fa258a0ed0704e3c7372e197699</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-12-29<br>IPv6: 2023-12-29 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>164.5MiB (172.5MB) – 3,506,613 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 723340c6dcc25b27238e08a061ac8e39<br>SHA1: bea3e4923ec92f4cdad9d3c5fcf044472606d67a<br>SHA256: f33c5a43f354819d0a50df878287b79bb3ff37b4c95192d23972c5a90892267a</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>192.9MiB (202.3MB) – 3,506,613 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89dc67064b85be0f027186c7468a2cc1<br>SHA1: d6066223dac75af7170e617d799593e40811daad<br>SHA256: 6af05444ce5487200c2c3e1b43ce961909066cf0ba4f004bd5a786c6a823ec27</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>169.6MiB (177.8MB) – 3,506,613 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4cc31211b575a3dcb7a4238f8bb9f9c6<br>SHA1: 3d10bab3598bbc09c3439bd893069c0809a79f63<br>SHA256: 16cd9791e402e96f9f21348e5ee9c48c7e6b9979ec0915d16477d78fe3736d09</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>176.1MiB (184.6MB) – 3,506,613 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d58bb83ce568d26cf70b09f9f842b4f6<br>SHA1: b08c97da88320305352acbfec0005a28d99f0a51<br>SHA256: a8372885a09e8799951fc5665dbf30a170cab92d62473156b86bb28f1042e15a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>204.8MiB (214.7MB) – 3,506,613 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2dde9c1419f535d3430aaf7b136ca92d<br>SHA1: 5631b44109c6568920586cc3044cc69c40ed26e2<br>SHA256: 80a132a2fc900f3fb9e5103172036864c2316bb95449becf87a330fd2565dae4</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.3MiB (172.2MB) – 3,506,613 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c00ad917bfb7211599ccc8479dfb4252<br>SHA1: 0ce9ebba9ed73d0913a84216138aa0bc0595c9fb<br>SHA256: 980b09520f5174367df5d7f55565feb6495443a801c3225306cc7d13aad75617</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>205.9MiB (216.0MB) – 3,506,613 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d26166404e3030a06fb688d5e39ea5ce<br>SHA1: f4ea9e0f9d23993dfbc71d928892dad5b22ff69c<br>SHA256: 9287c627019308560cf368e307e0f144813986bf66bf1b72adfd42ff544da9d3</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>172.5MiB (180.8MB) – 3,506,613 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0bd55b31dd23949ce1d193f0343cc754<br>SHA1: 503ca6160edf017d11c54a63d3228b51c69d315e<br>SHA256: 7ab672753db706c8a621c8794d5cd4555e13c14843395f805fbf9dc4da9a300f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>108.9MiB (114.2MB) – 1,220,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5e362980f3e0a4ca38d96577c082b03<br>SHA1: 187baaf352f5c0ebbbd5444a8aa010a2296a9374<br>SHA256: e95848ba2e9b8d506e1a14e0a4ec3da2473fedee20a94602910c8ae2f4c0251e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>116.8MiB (122.5MB) – 1,220,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4def7cbdf01c9c76ae63c8ca446160cb<br>SHA1: 0dc3eac8695703a192987c68c70c2ac825088c6b<br>SHA256: 95fe686d14e1bf0fc5939faebb15011fb3b108eb6c1467e5313b1d3313df71e5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>111.3MiB (116.7MB) – 1,220,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a5db8853013ae5fd320a5a5062495e2<br>SHA1: 4320e64b62bea206e51b07a73836c548f72bb167<br>SHA256: 5d396b8b0b774748d8a17b97f99d26149c10b34c193e0d7a2d81e7f97b389dd4</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>112.3MiB (117.8MB) – 1,220,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 607145a542d169bfa0db8aa0a1fd2fba<br>SHA1: 1fa9c99cb4bd0b4c3d3f1bf7cf9b012ef58721ab<br>SHA256: 41acdc312f224b7d3dc4726936f1f51e31c6a5138c232f6984c6f85a7962947c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>120.2MiB (126.0MB) – 1,220,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2131f3891b9482fb76885ecb705c2599<br>SHA1: 48ea15a5105a6226a658326c8fdbabd240b2fc7e<br>SHA256: cae07e7de0d91250c1656435c5bb8b98b79841f3a916631e579c99d29f516ca6</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>110.2MiB (115.5MB) – 1,220,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e34c64c07e91f5652aaf20bc2e25a946<br>SHA1: 7c330fa999b639ace1193aa45da06f47b6ff7451<br>SHA256: dbebd2c82ba378a46b718f04b3b2b355513982de04eed614a7dd4c92da906162</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>120.7MiB (126.5MB) – 1,220,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e45ccbc6cea102c01f9e578b7facf703<br>SHA1: ac3531eec4346ad8bcde094319cc95633ad94fb5<br>SHA256: ca93ecd7ebb9ae049b8be8540568009bd5a752604c8f984f122bfdbb51d46aad</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>112.8MiB (118.3MB) – 1,220,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7611ee5f361e4a2d17b4fe041a348757<br>SHA1: df8a7f1708936523554f1645b3ae39cc0583523a<br>SHA256: 7e24e5458005d63555a5751d2d2bfd936abf0676cb8b217c906dc0ddacb93936</pre></details></small> |


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
