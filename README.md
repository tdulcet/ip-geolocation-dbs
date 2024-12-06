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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-12-06<br>IPv6: 2024-12-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.863MiB (6.148MB) – 293,569 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e52a56cf74fe9964682c9a92775ec3d<br>SHA1: d419ba1fb9d1f9774aca04e067841cafb504d3c3<br>SHA256: 63e13464a997b75808cd1db62621a7225eec4193f3d79df37d4265c922ea9db6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.50MiB (12.06MB) – 174,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b21fcadce3f9c1642375dd43abff0128<br>SHA1: 6fbdbcbfabd5a8030672e0888625ee769b4f8e39<br>SHA256: c2a971495997a92934effb45ee9745ca1f70af520ae533d60ed204f81282ecb6</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-12-06<br>IPv6: 2024-12-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.248MiB (8.648MB) – 413,028 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd72c235c0226378cffb14a261ea8c1f<br>SHA1: 292d49a29f433b71edc862e9f084fb24208b693a<br>SHA256: 7134eef7f5407a89a340d7fb8c1fe6229eb93ec8927102c76656e19d59078dc8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.933MiB (7.270MB) – 105,479 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0e71411bddd50071c9a1c6a5c0113f8<br>SHA1: 9b87d278c9bf03de50dd3aacd494096bc5af8aaa<br>SHA256: 73b0a589cfa4a7eabd66facc1826b32a43eacac229f4a6c2f775d0961f232d9f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-12-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.64MiB (18.50MB) – 882,702 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38814f3b0d60a06c1776ee1f7a2c9f72<br>SHA1: 035762f1b11e6019546489c360f507bb1fbfd461<br>SHA256: 753905074f33bd0506122bf2bb6f4f99fdc84cdf3320862e171e90524b994981</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.21MiB (93.55MB) – 1,355,754 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5afaaa90259b9842dfa6eb8b30cbf8c0<br>SHA1: 5ec48773faecc440c743d25bc02753964055f9a8<br>SHA256: 9334d24efca8437ea7c1ec51117d712e4f129fe6b6791eee9712b6f5dd888b4d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.156MiB (7.503MB) – 359,168 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4fa1848a017a51ce167e1b45ef180e0<br>SHA1: d025902fca69db441cbc83871eb99ffd4b92c75e<br>SHA256: f02df1b7ee71bf749e1e43de462a3f6c365d9ed6e72e1d5c6faa86f25acb568c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.24MiB (17.03MB) – 246,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fee62599a38c614b43a277a08de845d7<br>SHA1: f6f5eddc6f61250f0fef53e42d76288b85a9971b<br>SHA256: 258dacce2a418e7297db10bd484df83410a61ac130bc1a5820b6fb0c0c58cb70</pre></details></small> |
| | | Full Location | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.6MiB (199.9MB) – 3,333,541 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f97a8dfa3d2efa2169aa49e5067082d<br>SHA1: 69f6046d5bebaecbd09f512a07ad0279a8bad58f<br>SHA256: 193177f00477af08b776744f0aa5ea8ffe08fe54bbe785733206c3c6f5ea0b02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>381.5MiB (400.0MB) – 3,700,914 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60c57063e8597965c85a15738ce2271e<br>SHA1: e6cfa1c20dff9df4b9dedd101304ed4939827a3f<br>SHA256: f48cf620380d7f79c9d8d05702be678101a193a90ef351c28ff300bad2cb1942</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-12-06<br>IPv6: 2024-12-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.918MiB (5.157MB) – 246,132 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ef7e16cf2b6bbbd422ba2a934ef7df<br>SHA1: e1f77a047f5dba3e4ae075464e3761268e84b7fd<br>SHA256: 8dcac1f1779ff26fe9a26934fc72b4c423e9a2f1252d99e1436206cc2bf9f63c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.70MiB (19.61MB) – 284,192 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dce3866a2d21db59b0445d7ab2b5439f<br>SHA1: 62737a727dab8fc70aa7a79a6b203bedd659ee5b<br>SHA256: 2bc4972b559cd83a749cdf69acfcc9f7e1e9b63db44e48dc0e635dc639b29822</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-12-06<br>IPv6: 2024-12-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>167.6MiB (175.8MB) – 2,906,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1918be02cf5e40016993945dcdf9fe2<br>SHA1: 26d9a8404ce0b330647e6b9dec8e0dc1f37c9773<br>SHA256: beead4d706ffee13660a84a3a4fa8d161b26172c66d7d783002d7e5e9a446e97</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>223.8MiB (234.6MB) – 2,165,543 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58aa852f4471f22d59a91349fedddaa7<br>SHA1: 58ed488a65f8f18956e7b32e6e9c4c95283bd843<br>SHA256: eff43d3a7756d1032e8d1b53d8fc159639852e5511ede4f1a0b4456657557bb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-12-03<br>IPv6: 2024-12-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.02MiB (10.51MB) – 502,125 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b44af2ccaa1e4f12e576475f8575636b<br>SHA1: 4c782e74935fe4543b6ee1f27028807213ac8fdd<br>SHA256: 2d1f76d51f769e539a8c9001822518435b243acfc2ac70f11663fda5b82ef2bb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.57MiB (34.15MB) – 495,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d19734a2bb9b32a8bb427ca4c6eca87<br>SHA1: 975343bb4167afba1a5b928130e7fb8916791d41<br>SHA256: 3f0c8b6594039f831a88df70a8910f8edbb3576d60aa32f24ce48abcf6e88ca7</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-12-03<br>IPv6: 2024-12-03 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>164.1MiB (172.1MB) – 3,243,059 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d14a7fb92b0d007f5a24dbfeabffc598<br>SHA1: 040188a96d4e7d3adaae4b7644249611a599aecc<br>SHA256: b7b6c4b55981ccb87f93cda1027034646bf1506df91eb12c5b13a227f72cb176</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>174.6MiB (183.1MB) – 3,243,059 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed0ce870a532995418cc80a62bf91ac0<br>SHA1: 85322f310052078c3d33ba38f42f12c0d75c1644<br>SHA256: d548d46e3bc8bd94e3d2bb436a2fbb8df8418fd22714c0a9a9da5a7045a1ca4c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.1MiB (171.0MB) – 3,243,059 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264c9ae087dfa70e739978c730fb13ca<br>SHA1: 6539ae9f832208119f125202aee184f363646420<br>SHA256: abb7133e1c19faea2e44ee97f4fcfeb307c2bad21b1dcd98ba91b9b805a85ec8</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>165.4MiB (173.5MB) – 3,243,059 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 454267ca198e418a76b776191bf64444<br>SHA1: dcf769914fd99ba23969352292f0154e5d1ce3a9<br>SHA256: dd1736bfd92839aeac7051c9aa6ead8262939f175307ed3f23cab24c0f4edd65</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>208.0MiB (218.1MB) – 3,243,059 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb37812e9edd9e665e71e9bc1b02b039<br>SHA1: e0aba3b4fbcb81c0f1fee08eeb996d94c853c4ba<br>SHA256: 92562ea8e8e7fec1362057224408f8b0e38290c8149982d664c0bc146202246a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>163.1MiB (171.0MB) – 3,243,059 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ad296eba5462d6b9738aff1755ba999<br>SHA1: 28602efd7387e162895ade6bff5479491f96036d<br>SHA256: 08bd5abab94f2f52abc0aa5dcb89e0c0005bea074fe0cb6ab136b003283b1bae</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>202.1MiB (211.9MB) – 3,243,059 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80b0077c7efa2879834a4e8cee5979bd<br>SHA1: 301b7308a29b642921b72e51f0008c4f52aa4f78<br>SHA256: 6d204ea3e9fac552093d2672f0588507ceca8ad20ae8d0c576c009ae9574aed2</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.2MiB (178.4MB) – 3,243,059 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee568bfc86c88bde8681246e85a04988<br>SHA1: aba223b0fa123c1326aebdace873e691a241cad3<br>SHA256: 91329573794b705fac2279fd94d106f9992cafd646c31dd96d194a8b1bf1dff9</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>152.2MiB (159.6MB) – 1,629,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c869d9713d7546b9a44cb38dd6caf30a<br>SHA1: 8df6ff3469719fc44d762bd9a7b299213aab745a<br>SHA256: 58e87610e597f49ae8892bb60ca4c44e6b1cb1ea6f44aaf7e1b8d204e4838d04</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>155.3MiB (162.9MB) – 1,629,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f9521eea5b4a457bbc5f475115f36d8<br>SHA1: 5043d29f9ab7374e9e56b7f2c395768d68852b9f<br>SHA256: 4040d5c7dec880d73015e8e8f2378fc6a861f8d829f02cf1c2e7acf705777148</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>150.5MiB (157.8MB) – 1,629,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c3ec7c96257d4483cf82619708b56e9<br>SHA1: 4fef716a77602c85766c6211e71eda3a869d3b88<br>SHA256: 8761c5b81facbb3c0140993ada7fd781d46fa344647e3c56b236bbe7c71fa424</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>150.6MiB (157.9MB) – 1,629,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af5da0def51f8b063028f206a60776e9<br>SHA1: ac065498b453e72478df6636859247debda4e9d0<br>SHA256: f346bb39505014b7fb4384bc24eb7864394ff7aab21f43ca29bd6f6e097c6446</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>165.0MiB (173.0MB) – 1,629,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c25c4df44f98b469da5c155ba349f8d5<br>SHA1: ebaa00ab947062e580798d4b95d0eb872f807638<br>SHA256: d3890c3723ddbe0c95e9f57e466f6a7cd6ea1885e8abacccba27a5d479f93dd1</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>150.3MiB (157.6MB) – 1,629,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5248bbe3576f980085dee01012bce91c<br>SHA1: 2b93d5a0c329ea231de59c071a2fbd99dbde7afe<br>SHA256: 805a5cb7d8da238c1ef648d0b7c0b44cc3489f848132efc5a2b4f52cd939ad86</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>166.4MiB (174.5MB) – 1,629,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa06be0438e0d8d8e3b89535daadce3e<br>SHA1: 4dcc92b37cde9248f275396b2597c33009d63e89<br>SHA256: 4ea9c23578b99d6ff2f1905bc850f47a43ebce4e9f6def7d0dee4f401439571d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>153.6MiB (161.1MB) – 1,629,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f69d170d11ec296b417713df5aa75661<br>SHA1: 489f5e9315091431d6a7cdebc087acafb6def80e<br>SHA256: 95e325928f19f0518cb5740921592b5266f3e8ddda8e451175fe5675d310997f</pre></details></small> |


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
