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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-05-07<br>IPv6: 2025-05-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.206MiB (6.507MB) – 310,754 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2998c753b85c8eae6aa5f6c0a77597fd<br>SHA1: 1e9c1491ab7633e05bc70e0aba429e5864608f85<br>SHA256: edb3538fe72039e2c80015628e07d7cfcf320e234ce0ccea97c2696b86434cab</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.19MiB (12.79MB) – 185,323 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e5882385f46442e8601f95f722ab883<br>SHA1: c97bc4bcd47a57e9c73089d8f3a3a50057a13411<br>SHA256: fa5b3d57db6dca730172b34cd013252b0b18f51e81412c7a06dc1df68da04f2c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-05-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.32MiB (13.96MB) – 666,622 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2638d5145807cc598a4caf67838e208<br>SHA1: bd025953bc76c45744c6e7293441393596f9927e<br>SHA256: d6be3d027dfc260c71ed54da709af8f799d70cbc8e5f5b3b6bcc402443f600b8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>114.6MiB (120.2MB) – 1,742,305 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b3331d7cd852d377bef1a98d5e9b550<br>SHA1: c7b3c45e6d80cc692d233c5fe65e53e387925458<br>SHA256: dfb461504ca8ab9b6f7397904fd88663b9fbd1e2b4e96763c4ef3b81bce5727a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.057MiB (7.400MB) – 354,084 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29dc016a76e5d1ce86f281b6be610e8f<br>SHA1: 91c6b4652acafb63416678a1a40d09acb733d81e<br>SHA256: 8c2e1dc4bcb582e63e3cf9a404cef7bbda49da95853a250d12f056cd6e928998</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.75MiB (18.61MB) – 269,749 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3faba08113ae8afbe0f9aeb0c0bc4db1<br>SHA1: baf9d49de9c133023e8e928090c9f50a291301bc<br>SHA256: 126f6ef6cfb9616fb3631b757bf8a7746130d673be4019cc177df52967b9cdf0</pre></details></small> |
| | | Full Location | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.7MiB (197.9MB) – 3,293,979 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc252212886dac7c40089289aaf5a71<br>SHA1: 67fd9db8ecf45ba433418c2361c87e2627dc8c3e<br>SHA256: 6fe5f2b32b1d809aac5a716539f4708f61c901ddad9c02b4ab613c7e262ccd06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.5MiB (412.6MB) – 3,819,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14c6250f6e4e959f775581c56c6b0abc<br>SHA1: 77ffea96762cadecd4cdca9183084900fec55cb2<br>SHA256: 1bc149f9307004c4ad7c60c0f1a25333a23792c5d431b1b374511792cbfab474</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-05-07<br>IPv6: 2025-05-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.948MiB (5.189MB) – 247,660 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6fe91411896d2bd0850805b7a989ffe<br>SHA1: e174beb80e780103862f29b6c94af9e0ef9177bb<br>SHA256: b87a246f35f8ab19000e4b03570a4f4ecab3b39030a59f3a0aa85ed1d9e08881</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.21MiB (22.24MB) – 322,286 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b00218e174dc90dd477d24f62635f15<br>SHA1: 0ab3977e561a987e0b15d1a8be0205ebac054d5f<br>SHA256: 36edd6e07b549795deba3fd441761515c9b3c1de7473204e1c404450d0d55912</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-05-07<br>IPv6: 2025-05-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.0MiB (182.5MB) – 3,014,341 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e5928c437bc1359f10928eea58d53ac<br>SHA1: 56e6f902c05b10bf03427836d717eb319b757e58<br>SHA256: 41b1b08e0f3d5f222ba4d3c8fa9dcf3dc9a59cee01cc75e498a51bb86544fbc1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>241.3MiB (253.0MB) – 2,331,339 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a21e885b78b78cafaf3824ba7bf0c642<br>SHA1: c1752c9a4f5acbc2c70be89ee9f7ec75ac016871<br>SHA256: ccd89a113fc7eef739896cdbeaeebd590070c9dc4febf6bdccc49e105e5d022f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-05-02<br>IPv6: 2025-05-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.73MiB (12.30MB) – 587,262 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b1518844df22b9c9b5b760c6f9d57d3<br>SHA1: b20d4fcf3226ffd22acadcf7c30d485883a39405<br>SHA256: 109a949cef77aa38bc580527e3a4d9755b79eab46b3ed331638ff532d389fa5d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.13MiB (42.08MB) – 609,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bff6987be827427e68e031216e446abf<br>SHA1: c704790d097b9341de28a2517d92bdf0fef543c9<br>SHA256: 8180097c768cdb5a929758dda3ef1cd9d519886dfebdc27abcacf394b8828873</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-05-02<br>IPv6: 2025-05-02 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>170.4MiB (178.7MB) – 3,363,570 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 083a85381decd9bade5cf1969dad4464<br>SHA1: f189a23f2400c1870de153a0c182ed0591c1994a<br>SHA256: b493525774c304a286510c7088d117ea118167d5497767649f3ef63913ab7a3c</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>181.2MiB (190.0MB) – 3,363,570 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8cdf860478ae461aeebbbb375e023d42<br>SHA1: f4b96752f14ded2b0320a1424faf343c64cb3a9f<br>SHA256: d50e11b80de11abdcbfb4cfa4f8e32202ea3c604466ee6298a78676c1cbe8291</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>169.5MiB (177.8MB) – 3,363,570 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60681ff4bb84fc6a30711b7ac295130f<br>SHA1: 006a4ddd4c550656a1e4c4a68ad16a504689480c<br>SHA256: 00fbbc8eb5cd15b999d4c63c227705e7cc61ebc46b5ffcd884f34c86ed8f3adb</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>172.0MiB (180.4MB) – 3,363,570 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00e6957a5e989102c34501ef294b6113<br>SHA1: ecc38b0a8f8c7a8f94f9d4d57ff79d95700d4c39<br>SHA256: 8f274a2ebfff4a2e23ab21b2fafebfc993668eb401ef9e399b398bdafd5d6f7c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>215.7MiB (226.2MB) – 3,363,570 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a3b614f2db369d586e57cc0e63abea8<br>SHA1: c5a367040405ea19a45794dc027f3caab9de350d<br>SHA256: 38990730434f9c052014987cf857a2da043d8607ea3972102e223a91d89907e8</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>169.1MiB (177.4MB) – 3,363,570 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02598742535f16a60e65d0a1378223a3<br>SHA1: cc7372235530b2bc167613d76e3c3bc29984f1fd<br>SHA256: b2e824e798ad8932609fdb2d021ada3a151e13b1deb93bfecc34aa69d2b13f14</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>209.5MiB (219.7MB) – 3,363,570 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23b08ca6b741475ea5ad1224a5f7b3c8<br>SHA1: 75c82e9c694720f43b244ae127ab0dbcb754546a<br>SHA256: 11ccb3acfb80bc9f87013dcd52f25439f701d66d24a0790819900b2234c1b343</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>176.4MiB (185.0MB) – 3,363,570 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb1b0eff0ec54604a491e1b76a859a95<br>SHA1: d07a10a8ff07be0895ecad7c5b59489f6e050446<br>SHA256: 32429a99cc48ec3d15a6dc865bc53d75eeb825d80102685ebe1bd82cb5fe8a59</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>170.3MiB (178.6MB) – 1,811,525 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c741bed1bb0e0a5c2df1c1b81751bd37<br>SHA1: 1c6e6b08ee079c05eb5de065dbbf53c8a56885c9<br>SHA256: f16aae80f5577f66f86d04bc4df2f45b9db95c108d70677de18f477a9c9cf1c5</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>173.9MiB (182.4MB) – 1,811,525 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4f00d7e20c03bacfc30ee9c21aa4d29<br>SHA1: 5e030bd5ae90a8ed0af23b84a6293b657b357400<br>SHA256: 3a4dd952611ff5532e54e3c6f0edabc9957122222e669b60b4b83ddb1d1e6195</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>168.4MiB (176.6MB) – 1,811,525 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11b48f95137016f3e06c37151bb3c02a<br>SHA1: 8bf17b25d3e15f15bbec13311e71ed818d7449e8<br>SHA256: 90d5be70c0600b3bd3ebc7dfd797bdb654ffdd739cacac8bb82d8b734d8f3acc</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>168.7MiB (176.8MB) – 1,811,525 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d805ab8ffcd0f130e911d496bf9b3a56<br>SHA1: 42be6020c8067fb585c38fa8ed367c45b0181df5<br>SHA256: 7b0bc95d58681e81f8feb51b635fafbe6d0c805e01411e9a8ccd5557a7ca629a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>186.2MiB (195.2MB) – 1,811,525 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c1c557b7d4cec4dcf2cd41a1c05c7e7<br>SHA1: c9be9b9b581e751e0423af19f6999f10bdefda5a<br>SHA256: 7da63dbd3d77ae72df2cbf73002ccd0538146e70bd4226fe32d1a36dcb5d1f1e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>168.2MiB (176.4MB) – 1,811,525 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91d851e9c72f5dfcd37bc615c6131dae<br>SHA1: 16b0f2278afd318e69cd3528a3e520fec51849c6<br>SHA256: eea7bac7cdbad04775bdd09bcae3550e9a48719971c274ea96601fbc21cb1052</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>187.3MiB (196.4MB) – 1,811,525 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6abca0af7de8038c6e2d0d0e70caec0a<br>SHA1: 618422c28b5bcf063e38e22fb4114dce5d277961<br>SHA256: 92853eab9d70445f8bb11aa05ab11f3ff633779af5247dfa22e3a7c82178507f</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>172.1MiB (180.5MB) – 1,811,525 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecf88c43b7cbdcd1e821374efee7dcab<br>SHA1: dee7e386f930f1c55a428bc4567eb22c1eddaa26<br>SHA256: bded1c7ff13ec7d2574df6b6cd703983d8366fd5811e2ae793a9c9a6422f6308</pre></details></small> |


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
