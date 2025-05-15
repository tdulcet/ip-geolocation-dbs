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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-05-15<br>IPv6: 2025-05-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.229MiB (6.532MB) – 311,911 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a40eef63dbf5f1bb370d2b8535ed0a8<br>SHA1: bdd2be4aa5b76fbb07f91e5e6fdb10f57336e7f4<br>SHA256: c6f0d5b59350c348b356d2e0b1852918f4f1a984c62df970fac88a776dd49bea</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.22MiB (12.82MB) – 185,743 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c03d8551362ece61ea7de99b90efc259<br>SHA1: 15cb0078b0ca1cac57c12e5d7fea74013399fd08<br>SHA256: 1f40b508bdc1ea3eb534e7863f609c3ea259af7c13e3d36514dd956044145fe3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-05-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.91MiB (13.54MB) – 646,310 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26311cb179ecd1e44922bc3393cd47d0<br>SHA1: b294f87d8dbf176de91a69784c2bbfedb724b64f<br>SHA256: 99370bdc7d4bd9beaf101dde2b10085aa89dccc1dbfe6d647b2135469010b866</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>126.5MiB (132.6MB) – 1,922,201 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8cd6dfaa328dfa6f77f911110f8e40df<br>SHA1: 135b83eb26aab4fb81d51984e7ce088dc0002dae<br>SHA256: 9f6a5094982e0c3aaf3c82305ae1d375af0ea9a43ad6b6541ce8f4eef649fc14</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.057MiB (7.400MB) – 354,084 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29dc016a76e5d1ce86f281b6be610e8f<br>SHA1: 91c6b4652acafb63416678a1a40d09acb733d81e<br>SHA256: 8c2e1dc4bcb582e63e3cf9a404cef7bbda49da95853a250d12f056cd6e928998</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.75MiB (18.61MB) – 269,749 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3faba08113ae8afbe0f9aeb0c0bc4db1<br>SHA1: baf9d49de9c133023e8e928090c9f50a291301bc<br>SHA256: 126f6ef6cfb9616fb3631b757bf8a7746130d673be4019cc177df52967b9cdf0</pre></details></small> |
| | | Full Location | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.7MiB (197.9MB) – 3,293,979 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc252212886dac7c40089289aaf5a71<br>SHA1: 67fd9db8ecf45ba433418c2361c87e2627dc8c3e<br>SHA256: 6fe5f2b32b1d809aac5a716539f4708f61c901ddad9c02b4ab613c7e262ccd06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.5MiB (412.6MB) – 3,819,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14c6250f6e4e959f775581c56c6b0abc<br>SHA1: 77ffea96762cadecd4cdca9183084900fec55cb2<br>SHA256: 1bc149f9307004c4ad7c60c0f1a25333a23792c5d431b1b374511792cbfab474</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-05-15<br>IPv6: 2025-05-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.948MiB (5.189MB) – 247,660 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6fe91411896d2bd0850805b7a989ffe<br>SHA1: e174beb80e780103862f29b6c94af9e0ef9177bb<br>SHA256: b87a246f35f8ab19000e4b03570a4f4ecab3b39030a59f3a0aa85ed1d9e08881</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.21MiB (22.24MB) – 322,286 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b00218e174dc90dd477d24f62635f15<br>SHA1: 0ab3977e561a987e0b15d1a8be0205ebac054d5f<br>SHA256: 36edd6e07b549795deba3fd441761515c9b3c1de7473204e1c404450d0d55912</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-05-15<br>IPv6: 2025-05-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.0MiB (182.5MB) – 3,014,341 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e5928c437bc1359f10928eea58d53ac<br>SHA1: 56e6f902c05b10bf03427836d717eb319b757e58<br>SHA256: 41b1b08e0f3d5f222ba4d3c8fa9dcf3dc9a59cee01cc75e498a51bb86544fbc1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>241.3MiB (253.0MB) – 2,331,339 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a21e885b78b78cafaf3824ba7bf0c642<br>SHA1: c1752c9a4f5acbc2c70be89ee9f7ec75ac016871<br>SHA256: ccd89a113fc7eef739896cdbeaeebd590070c9dc4febf6bdccc49e105e5d022f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-05-09<br>IPv6: 2025-05-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.75MiB (12.32MB) – 588,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4d0410048f6a3f4dd9167587e6a7452<br>SHA1: 0b5f83a9949ded266d3b1edfc0272fef5fcbe160<br>SHA256: c57986063846a2d9f2da8761073d76354d1bb218e48009b23e7fcd63a92e2cde</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.11MiB (42.06MB) – 609,522 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95f0934ba56f78e8bfd8530c8a7f1400<br>SHA1: 11c944b7f670b74f4150de6cb4415d2023af9720<br>SHA256: 36d3ebf94f522302401e24630d51ce60d56d5e6d2d6bfe0a2ad58e0c70b13fea</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-05-09<br>IPv6: 2025-05-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.3MiB (180.6MB) – 3,399,519 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 018a2ecca8c0f495cc4300f43313fbd5<br>SHA1: 857fc9e898385c78d98052f538f5b190fda86099<br>SHA256: 6606aef9f7ad8880cc7c56eaf47b84e45ac82af203d7fe8458eae32080094b16</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.1MiB (192.0MB) – 3,399,519 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97acdfa783ff6bc01bf1a6f9925af4ec<br>SHA1: 2e737ff52d9d5f2f5a1bdc1902680db372f8fb6a<br>SHA256: 1ea962d64ed84aa5f1d676caba5dcf492ea5ee3beb28af9ae3a7ad5d6f63cef6</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>171.4MiB (179.7MB) – 3,399,519 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1bc73a1cbdae98794fdc9c69aa6b06a5<br>SHA1: 5ed59fc3ed22a8b57e023b37a021c5ba2969405a<br>SHA256: 42502054414fc93d5eb41d641c737dad44fb266559a5af42b5a9b71389bb8501</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.9MiB (182.4MB) – 3,399,519 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f748c0210a252d947629f3cffb55856e<br>SHA1: fbed7eedd3442ad04891778bfcc9893b527a0743<br>SHA256: 22d9be94e1455766230714cc4d8911e234c8c4d5aa41d0191f7ca4919843bb2f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.0MiB (228.6MB) – 3,399,519 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c24fba02fbb48e3e81f813ebaac375e<br>SHA1: fb451cbecb33715be68e767d2ed3809163d4305b<br>SHA256: ae040cd86ac212bc0c443e4ab90c442f9896bcebec4ee8891deac0a703347217</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.0MiB (179.3MB) – 3,399,519 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f4f6e377daf52620193879361e83b1<br>SHA1: 259ab041d80f031783fbd9b4c3d68f720ba64e2d<br>SHA256: fde02e5c8b932fe7e884a7f7289ccbafb0bb3bb409cee8670a4609a42bd9dd69</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.8MiB (222.1MB) – 3,399,519 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 362089cc6a18a1519ee9612b46eadd9f<br>SHA1: 4b48441addd3714cf1229618079cb69c382b374f<br>SHA256: 9b922dbb8317e8ce0071e0b803c4656adaf46bb237c12bfe134ae98729e5cd75</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.3MiB (186.9MB) – 3,399,519 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5cf614a06882587d75c868d3a124d2ac<br>SHA1: 984ba438908939fd8fd656984b5d0f4fef2007e0<br>SHA256: e4f1cb5c14d499c6efe9882bffb460a3dc7dd873e2f4383d6a1d787f2060c1f3</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>174.6MiB (183.1MB) – 1,856,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2e47cef9b96bf4cc873ff368dc908e6<br>SHA1: b708af181a131b6f1589263c528ac86c284b3259<br>SHA256: f9bf1da908b18d72d71bbdcdaa8ee066623b7b30ad2bc925b117e8b989cdbd75</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>178.6MiB (187.3MB) – 1,856,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9676f4c344648002e265da08b53b0d6f<br>SHA1: 36a690a4b957772837f50aaa942177263c7f963c<br>SHA256: 5997f3bd18f398dc82b86381c6921918302c984b1488d3f0a640526d332afcda</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>172.8MiB (181.2MB) – 1,856,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cea19e24e79cd4d3be5d88f9dc803f6a<br>SHA1: eb131fa31403ec1dd91f8db2068a4a2caf45ce33<br>SHA256: 732bb14d28844303852e41480152635a031f0a128e3a70834ce6db76132576f0</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.1MiB (181.5MB) – 1,856,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2520f4376685a29427caa6b21d7692a5<br>SHA1: 2a11cb5adbeac6351c207f910a949873206da96b<br>SHA256: e2ec588aa44b5e4710055120940ac9cb48c8fa0254b051fe41b3772dc5d8319e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>191.2MiB (200.5MB) – 1,856,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2649d725574bc518d78b05a1281f4740<br>SHA1: 1bdbfe953cdabbedc1dd29a135ff980068b44cd0<br>SHA256: 4f8dbb3ee97adfffd6bdf952b80ff7ec4b452b6c311f3b1022283e5ad49eb91a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>172.6MiB (181.0MB) – 1,856,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 004bc7b9a20f8f2195d0f2ea776fe616<br>SHA1: 1a24f583683ca27b23d6ab6d3c1187f1fb7d279a<br>SHA256: 8b9a3daa8aca2bc3bd9816f1c5d6ac8f7174d4f2f4b2fcf3df4b01ed22d85a61</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>192.1MiB (201.5MB) – 1,856,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01f587cf7f208be43bdb593f981bec05<br>SHA1: 8bfb77a8bade82bb07da3d39ac7836768b39e98e<br>SHA256: a5f291ea57eaa880ef06691dd619a1e7ffd058cb5008473c1b931bbc6f5b2dd0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>176.4MiB (185.0MB) – 1,856,469 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a15cbb9d5da9a3cc56eb1217b583b4a4<br>SHA1: d3e9433711e6660246212b7cdcbe1046d6502b10<br>SHA256: 161715579ef2fc4d4a4b96781d10e87fd86ef4607c46796e9e05752c0168dd92</pre></details></small> |


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
