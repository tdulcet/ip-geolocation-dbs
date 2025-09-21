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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-09-21<br>IPv6: 2025-09-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.281MiB (6.586MB) – 314,497 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22f8de68ee9230f246b2fb580bec90ac<br>SHA1: 5568c4bd4beff52cd185e04ba3b5221d8a589e9c<br>SHA256: fc1d04ecb26aa1a908a8dbe16e2ffeba161b30c607f1d4826f30b37e628cdc24</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>14.85MiB (15.57MB) – 225,668 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9f8f1f06094ee50c79e41ddd5409b3b<br>SHA1: d65ff448483749e70610610e50db9bee5604b44a<br>SHA256: fd3b6d24ed03c38c98247f4dc40c65419412478b16329bdd3956cfe85170229d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-09-21<br>IPv6: 2025-09-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.645MiB (9.065MB) – 432,895 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ec2d4c32d4526fe3d169316561bc02d<br>SHA1: ede438100fe2bc3b16e19698f35ee8e45f951d47<br>SHA256: 38d8dc6097ca4e3494721724e8aa3a1d79e144e14fb67f791fdfc461c43778ff</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.285MiB (7.639MB) – 110,829 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be30ff1f179fec9c0b8a404c83ed90f5<br>SHA1: 46d7a3978ee198971f8e4b214b9e2eaa48aa1ddc<br>SHA256: 087ddfe4bd831fbd2c14995ff2a6203e0aa461803030d0e6c4dbec6c535e3784</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-09-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.18MiB (12.77MB) – 609,809 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87ea041e60c2e356d2d15a0e5179f833<br>SHA1: 9707f7f03a6cfb38f52ab54c6a7686acac8fcdaa<br>SHA256: 977ace3c2627bfe886a979d7b36c9cd0b91f468f93edc9e0b106e9ea657f6099</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>66.26MiB (69.48MB) – 1,006,955 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40d2276151513157f75ed20cf91017b5<br>SHA1: 61884c691e16ef922f8b1c05d69b940c93e0a8b1<br>SHA256: abd4a5188e71ea24378fb92e4a21d3410ed12e49c4f6c76602ca88ff3414ab3f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.825MiB (7.157MB) – 341,824 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dae1f431e9d10a462dae84888365884<br>SHA1: c0cc78c9aa347b8d712850c57537fc0dc50f1dfd<br>SHA256: 3f57c286e145770c2ac0d5d3c14088a919db312a222bfef2cb85941399367b2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.93MB) – 245,375 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f7e3a8bff7f09ee7cfd621ef044564b<br>SHA1: feacd88a985ae6ef5d668ffcf375eefeed7948b4<br>SHA256: f554d05a841ea0162859a713eecebb3fb0dc814ea2d39b91150dd45627c31fed</pre></details></small> |
| | | Full Location | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (217.0MB) – 3,624,799 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7154efa553f5c77576cadbc5c42ec9c<br>SHA1: b63ba0a183e94bf6cd1aa8a15db942b52d55841e<br>SHA256: 00286d8f1fc1f8f801a25f123213615fc637aa494c49fb2537047bdab4b1aaed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>448.8MiB (470.6MB) – 4,362,462 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7375867bcf97ba785ec1fa3d092fb0ae<br>SHA1: 37a209470da0930c2308178d77c0c1cac376d849<br>SHA256: df10547da1aed72a27d58d5fbd860b66dc9bfc40df34c5dcca2b7da7fdf24ca0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.185MiB (5.437MB) – 259,491 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50d719d1853e86e8da56334658c35eba<br>SHA1: f811bb310275e7b7653fa90e869cf112fe526acc<br>SHA256: bcbf902929f7d249538703a8dbbcc64d8fae4900531479cf0e3063367391f946</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.57MiB (23.67MB) – 343,010 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff677ddad3772ab36197d2ef84bf42e7<br>SHA1: 8be3a4e0ee14af3d087f70294904f7aa883b6743<br>SHA256: 0f288add4994bc16d4d6387a5818de57f3def88cb259fb8fe4a8f6b507e4c820</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.4MB) – 2,949,463 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ec6ef92605faf0c8ed3176f371a4f89<br>SHA1: cd21e0629e442168ad794701d10639489e2d7e3c<br>SHA256: 3470fc0e8a3432aae0bb7caf8d995d20c8043b2486e3fbc23fd209fe4a11d530</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.9MiB (308.1MB) – 2,846,052 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8446667c1feaa357c25104ee40c7db47<br>SHA1: 1631c4d82f37dbaa7ece00c99dde97aa5483e6ea<br>SHA256: a265bc2be67ada5c65a6d3631fcbea01cc1272b1b51f27002bc5f3bffbf061ed</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-09-19<br>IPv6: 2025-09-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.67MiB (13.29MB) – 634,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bd37bdfc0879f4d811a227ef36f2338<br>SHA1: 61d171256e13cecc197827a8b7d14b0091a18537<br>SHA256: 10aab26d49041f6339f9ea264e815f7663ec070c19434048545083fec93a943e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.31MiB (45.42MB) – 658,230 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2db2860570bd70a2983ea8511f9a1eb<br>SHA1: 962e0b4bf9cf76d7be27507f34ddf710ff683344<br>SHA256: a4b6fa1573b27342962ed02da227beba982e96edd646ac8542c12b27c88a8351</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-09-19<br>IPv6: 2025-09-19 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>175.8MiB (184.3MB) – 3,463,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 379e58ad3fdc6d2a525fe0ec6c59161d<br>SHA1: 3c4c08d180ef4c6cd32c5ea9d3c2aee1ac18eb10<br>SHA256: c5d2bfc2a07e3467564b8663fac0d405952610cc0ea5d89c51a18e3ab49c2e9d</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>186.7MiB (195.8MB) – 3,463,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8df32fb2cdf852f640f5f1bfdf964d00<br>SHA1: 37987dd1168e74bd7bc43bafd71af32d570b7b06<br>SHA256: 4c80c2fbf53f99aa85bf8f4feef306f982c26d392f9e2531306865801f793a62</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>174.8MiB (183.3MB) – 3,463,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 994d7aab79b438c542d075166c1f01ab<br>SHA1: 0fc75980150ac4269e38c9ccb42f06e8f75ea2a6<br>SHA256: 8f9942fc5f60c56707a3fcf7c9d8a64b48f768430cb7c567be774ceec6df1c11</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>177.4MiB (186.1MB) – 3,463,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c0ea45023761c0d813a60a86af526fe<br>SHA1: 242efc6e08fe6668d4a0057e268ab8dda2ade73c<br>SHA256: 5f1a671e0fa8d6c04a520aad0cda401ea00a917b5e4dfc2101971028078b0448</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>222.6MiB (233.4MB) – 3,463,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ac5b4b8a12db69fbf543c7e841f6ded<br>SHA1: 38ac78809fa6a96863e472bc3d38eba0309aadc3<br>SHA256: c5ed6fd60db220e25c4483aa4f2d0e7d7967357146f1249fae82c7cda7a4d311</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>174.4MiB (182.9MB) – 3,463,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b0572c24557d21163c10df7d16c94fc<br>SHA1: 6090e144a0fa8f84d1372e999a82c48b9810cded<br>SHA256: 0379002ecc087732df7e6402e984334acac9ec9e2bf2090da3acbb0431404644</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>216.2MiB (226.7MB) – 3,463,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7bff26ac88cb89aabc5d3d26ac7e7e42<br>SHA1: 1f832f1ef6708eed013bd911086cccd51d33c321<br>SHA256: 886e1f4cb2064a4bf2f3487061926b4936edff69e9989b56e0cfd767406dd460</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>181.8MiB (190.6MB) – 3,463,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 662344a8723d826c72332a65592ad153<br>SHA1: a484068b09969276c9a5a9a684baed8cf5d64261<br>SHA256: eb4f632f8d56d8910ccddf4f039c8cfde4facfbf5298832b5a6eacd00ea61c60</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>177.9MiB (186.5MB) – 1,886,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7649af7f83b853a764373d34f3867a2c<br>SHA1: 64e3ade1a6edc5ee9630926324c7af7828fcde14<br>SHA256: 122c7db500208c4b1606b72baa67623d513b637a639692a9c8dea88c651b9055</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.1MiB (190.9MB) – 1,886,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 466c8141076f66b61c5daaf5584d4a20<br>SHA1: 4ee799e44e88a2418c9bfd484f7d96fe35709afc<br>SHA256: d3196b5a9ad18e9cbf38124804ce14612414b1face0b90054ea4970116a830d8</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.0MiB (184.5MB) – 1,886,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de1e1431e5ed0bb8743b5baa9b08dfb5<br>SHA1: 41b82f55e68a265ce4572513c40fd8cd50b37751<br>SHA256: 9153961591616d362e34aaf4a7b961994795d22560cabb25d8145bb7927b5aef</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>176.3MiB (184.8MB) – 1,886,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 404e52d061db7d674534c53e85bde2f1<br>SHA1: 71e7eef5614a79ef589b0c9e26feb9476944ed8e<br>SHA256: 9f118ce143c101ec7e9991b214de3cbb50ec208e1d108558b0adeeb533260780</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.3MiB (204.8MB) – 1,886,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75b85026eed930aa9fdc0b062befa32a<br>SHA1: bd7218fe761993dccde6406c390266340c8ac28e<br>SHA256: 3b05c422515b0ba10d11b88036de191bd43743fa367fe86e86d8f8d44a0770f8</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>175.8MiB (184.3MB) – 1,886,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7347989346dddab683025cc9d134c3db<br>SHA1: 91acafc052ae995d58f9ca9ae510b8d1da130be0<br>SHA256: 9823658a138fcd5c5f2e9166e3f1a81c37e5e99d7344ced8021affca170cda4b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.1MiB (205.6MB) – 1,886,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0bba5532c1b3490788c47217da19c4fb<br>SHA1: 33dbb615e1991156cd1eed29da0148fae12eabc0<br>SHA256: 2658c82affcd8ed1fe700a252db73a77556807b2296a6f2adecf3f73ca97ab49</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>179.9MiB (188.6MB) – 1,886,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 211e03c184bf229ad87d664e201caa55<br>SHA1: e76b4e9f08d54f67807373d94c755edf2e2fba3d<br>SHA256: 5cb0fef11f0fdd24277be3e8fdc1ef564f42b38166b01e4038045ea2e16dd87c</pre></details></small> |


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
