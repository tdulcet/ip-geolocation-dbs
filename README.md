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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-14<br>IPv6: 2025-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.330MiB (6.637MB) – 316,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b331f9f0f7fbf8e53afc558967f0d03e<br>SHA1: 58ed82820375d316a416def40245550181b1ebf4<br>SHA256: 75f220f9e20d8fc87b8e0886accc6d1d44b51f6a1f9d4f9f665c88d58bf941c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.28MiB (12.87MB) – 186,571 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 285d005e109a5ca8573cad8be4a57b0e<br>SHA1: 8c315ecd0a6831c602b23470066c27d2099534bb<br>SHA256: edcb7336c750c10ff04e5b9fd2b18dfaade7a1513053d1897f1bb334b0173108</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.17MiB (12.76MB) – 609,381 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24b08f95db316819a2ebf5815ff6bbfe<br>SHA1: e2a377be8f521eb7126f0efe37c28683fb2057bb<br>SHA256: 03c477191290dce6dcccb52af3c21a5b44d7e4c5a4e3de5756219bcefcf605b4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.96MiB (94.32MB) – 1,367,025 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42bb1c719fef913b2beda2d39bdf67ab<br>SHA1: 942032cf58934438e1eea61e90438a6df68fa696<br>SHA256: 146d6f3caaa9579e576dbcfca8c2d9b338a0ca3237b46a992c62f1bfd88e05b9</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-14<br>IPv6: 2025-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.057MiB (5.303MB) – 253,125 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95ffb525ccf7554fce3b883e3c3e03dc<br>SHA1: cfd2058bddb8335014ef0155af9287eb4eb032a5<br>SHA256: 7f2d0669907805f467ba557b3f8a89f0cc365fe47fd8d2d06b459ef043b58cac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.80MiB (22.86MB) – 331,362 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba9c525bb7d6b096e7d2a8892fad8109<br>SHA1: 51c5aa6639dc0b1ba9137e7681566659089d3e9d<br>SHA256: 055c98ab2c55b531af78c6adefcb75267c71f317deda1d0e11cd3a5379f8eb41</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-14<br>IPv6: 2025-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.1MiB (174.2MB) – 2,881,364 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 857f03de59f847ebc914de35a0261594<br>SHA1: a8eb10b3a834af6faabde77d1402f59045791a92<br>SHA256: 4de98758f7a7f36de44db1501aae76db758f5a29bc7d70a9c2dad3a025af32df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>269.8MiB (282.9MB) – 2,614,886 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cf5e97154e6ed02edf8b16bd1ea2891<br>SHA1: c33d58815af98fa41a92decd4ae34875ecc10ccb<br>SHA256: 89eb5c59f64873edf5e3369de45be94f934ea8219710777955f08a65ad9b49fa</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-11<br>IPv6: 2025-07-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.53MiB (13.14MB) – 627,393 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5509c2d4cc6bbe2452e0b26064f49897<br>SHA1: 0044fa330fcd010977018b5a53ef8c7947b541de<br>SHA256: 7da7b77cfee89a0d931e02ba0e28daa2d892c23181f10ef22f57f0acb6b5b0da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.15MiB (45.25MB) – 655,811 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8cb11ef60adde6c0007a7de8b3fc7f2d<br>SHA1: c8b99a45a6eff144371baa159cf79fc402126d35<br>SHA256: bf737e29c27957dda8798ab4e5d84300e09ecf2be438c13ee69a04dcc12f04b7</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-11<br>IPv6: 2025-07-11 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.0MiB (182.4MB) – 3,431,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9726c15e312ae74a02fb3aadd83750f9<br>SHA1: 2ea4d50eb8c4ad4ce2b7652c3daeccccfc2def5e<br>SHA256: 0e551c66b3dc704bbb4a2ff59c6b4af56cfda296392f3151b8ba78c1938ac3ce</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.9MiB (193.8MB) – 3,431,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ea4f2a81f0ebda5b0335bfb75bfa80a<br>SHA1: d990ab10a248d73cab043a5aad2a395d30d687e0<br>SHA256: e21871c3e1b16ab3885eba7cad63121460f722494fd232d0b8815e313dcfeb72</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>173.2MiB (181.6MB) – 3,431,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 357ad7be5eb807441d000f7ef472b226<br>SHA1: cde53a5a99882e7655840b02595413fb37a0fe7c<br>SHA256: bdcda30b5d22c17efdd330f9e28ecc4a3da9f98047bb8841ec5f73b5da22dbb9</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.7MiB (184.2MB) – 3,431,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 955bf1678027bfdd6ca72a2c6ca121c2<br>SHA1: 3e312fb5f583e75896593a0eaeffc9ef17feb6aa<br>SHA256: ffb7f5342b80e45a9905597293512fc8f3fcbf2f465684147a03125fbef6973f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.3MiB (231.0MB) – 3,431,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a62ae5a16eb8b5d4b706914022acfa4b<br>SHA1: 15830781b009bd2b87eaa343825c63bf845452f2<br>SHA256: eb76b32f79a3540cd37d0e4bd68e363bdf86f50693c530cd0f1fa7e08da8624c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.7MiB (181.1MB) – 3,431,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 365a2413f118ef02f4382bc1235174e1<br>SHA1: dd006bd33ad3241692ef4ee59b7d2c8aa2aba1c2<br>SHA256: f39b48eb6f8d00ee2c912cbde739047e39ca9703b1c8a0c07294586e84d37b21</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>214.1MiB (224.5MB) – 3,431,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8729ece40969fa2631efbad7ff340b6e<br>SHA1: 529f4d6f3b5af1e055e93a0f7615b7d85fd65b3b<br>SHA256: 87490544b2b807bfbdafbca439c694a8a680f5ca774b05769b0844a8d5c802c9</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>180.0MiB (188.8MB) – 3,431,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc36576db7a1d0b0a1d9b062795a6326<br>SHA1: 3723680d0382b05a4bd05b86f06f1783f656907c<br>SHA256: 8854aafd94d7ce6821aeef1afd4d4ca6d29402b1f6d0576b1002f07486564e69</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>181.6MiB (190.4MB) – 1,926,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f5709d85e346f4acce80f14799d2dca<br>SHA1: 550f6ca5fa1226ff96f5e2588a6b054656e57176<br>SHA256: f884b2084894f0fb2d102980c4042e428de5a4e47ef431b0aaec6b2afa8ac582</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>185.7MiB (194.7MB) – 1,926,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6401f5da38ebd0c700b214f90769b7f<br>SHA1: 9b8313f940b623f237f6ded08b7e1ae9cf128d69<br>SHA256: adfd7835f62dd0256292be4d0ea5217d62cc4ba83f82e804665fac6d8416df98</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>179.8MiB (188.5MB) – 1,926,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d228c76f8ef21b37be1ece2d5c6a6e2<br>SHA1: 78d9fbfb9e27d018b08189f181cb3736b9ea0925<br>SHA256: 37da270f88163ae134573e78bd3c78e62d97b5ad81fa9e9639ae38ceb92cada4</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>180.1MiB (188.8MB) – 1,926,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 528126b858af55c7580f020906a936af<br>SHA1: 083eb164b2691662508cc07dcc8467a2298432cc<br>SHA256: 6ecd9de84a56ed5eedbbe5bf6d66704f3b3f386c3eb4473a0de714423d807fd3</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>199.4MiB (209.1MB) – 1,926,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ea99a5f141d681873abb8148e0d1599<br>SHA1: 67ee318bc9ad9a515dbf7621c0d69e773fc76e5e<br>SHA256: d869765d911406aa3438d3fe5a6096705b764d5b6e6d3aa0e78eff11b04f86af</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>179.5MiB (188.2MB) – 1,926,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb00495cd577c5c7d3c2bb0288847199<br>SHA1: 361894a728a7f92924ab27f7f2e0818583712053<br>SHA256: 4012a46584d8fc35f9263809dd574e72c69ffda206ab4fa79299a7b7229bbbc9</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>200.1MiB (209.8MB) – 1,926,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8db3545a53fa132309f8b63e5e931cd<br>SHA1: b2719b6d09b8cd2f460a5ece4cfcc4a1476d62ee<br>SHA256: 6a4a021441d148ea75c6c06b7f3e15c4c7d0d49cb9e473b71ffd65e1ca169ee0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>183.6MiB (192.6MB) – 1,926,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19de8204c76d55ee89cd3668e6a2b3d9<br>SHA1: 1dc72589bb395a950d55af9bbc22b23f0fd7c6bf<br>SHA256: 08563ba9a7f40a0ffa01ade6b17ec8b556a3a4cb5dd1c19917465b8f11b306e5</pre></details></small> |


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
