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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-12-25<br>IPv6: 2024-12-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.948MiB (6.236MB) – 297,796 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 567754d116225113871e637ca3784ccc<br>SHA1: 0635a833a30566e0da5afdef4295b713e1af041d<br>SHA256: 66a9eea70e66af00e33f64a958a65a4e3085756cc2005e5c73a04b9d4a9070e5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.64MiB (12.21MB) – 176,897 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f6c9519ab8742686d99a641f656aeca<br>SHA1: 8a8cbcc3b790e1dd518ae3da50925a9ab7b0ff26<br>SHA256: 7afdabba1e07c553538718d4e7cb5db3e2da26542ea619a4522633656f1a8fbb</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-12-25<br>IPv6: 2024-12-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.275MiB (8.677MB) – 414,363 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccb3c98c9d2f0fcc0b044df9b975f7a1<br>SHA1: 838ad4340fce10ebdb00156a6486e4f693ee90ab<br>SHA256: 8da97494902873c957a8131061225e338d1f5b925a2db38836c23266d6ce7c2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.953MiB (7.291MB) – 105,774 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38961f71b45bd1872f5764b0008c1a83<br>SHA1: 55ca5bd8cde8ca1ce35baacf7ad1d0b101f3b322<br>SHA256: 1c4e19137495cf485ec10819dc00ab6d1f60e67101de0e5b5968fb557645df1a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-12-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.50MiB (14.15MB) – 675,748 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c659af42363dff5badc2f23c020845a<br>SHA1: 8b0ce3644da0884d665ccfff0998541737934753<br>SHA256: e41a80feec3b70a0f6259589ab4847d3ab3ee566e80c9108dbcd235153e75ee8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.10MiB (93.43MB) – 1,354,008 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 024fc83196c16efa26b1763987b2fc9f<br>SHA1: 4a476185076056e122752c423f00ce2bce327ddf<br>SHA256: c539c6149c80a1bb9b28d05da3257dc55bbe218f4cef4bf12ed24e63c233a65f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.156MiB (7.503MB) – 359,168 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4fa1848a017a51ce167e1b45ef180e0<br>SHA1: d025902fca69db441cbc83871eb99ffd4b92c75e<br>SHA256: f02df1b7ee71bf749e1e43de462a3f6c365d9ed6e72e1d5c6faa86f25acb568c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.24MiB (17.03MB) – 246,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fee62599a38c614b43a277a08de845d7<br>SHA1: f6f5eddc6f61250f0fef53e42d76288b85a9971b<br>SHA256: 258dacce2a418e7297db10bd484df83410a61ac130bc1a5820b6fb0c0c58cb70</pre></details></small> |
| | | Full Location | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.6MiB (199.9MB) – 3,333,541 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f97a8dfa3d2efa2169aa49e5067082d<br>SHA1: 69f6046d5bebaecbd09f512a07ad0279a8bad58f<br>SHA256: 193177f00477af08b776744f0aa5ea8ffe08fe54bbe785733206c3c6f5ea0b02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>381.5MiB (400.0MB) – 3,700,914 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60c57063e8597965c85a15738ce2271e<br>SHA1: e6cfa1c20dff9df4b9dedd101304ed4939827a3f<br>SHA256: f48cf620380d7f79c9d8d05702be678101a193a90ef351c28ff300bad2cb1942</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-12-25<br>IPv6: 2024-12-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.918MiB (5.157MB) – 246,132 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ef7e16cf2b6bbbd422ba2a934ef7df<br>SHA1: e1f77a047f5dba3e4ae075464e3761268e84b7fd<br>SHA256: 8dcac1f1779ff26fe9a26934fc72b4c423e9a2f1252d99e1436206cc2bf9f63c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.70MiB (19.61MB) – 284,192 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dce3866a2d21db59b0445d7ab2b5439f<br>SHA1: 62737a727dab8fc70aa7a79a6b203bedd659ee5b<br>SHA256: 2bc4972b559cd83a749cdf69acfcc9f7e1e9b63db44e48dc0e635dc639b29822</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-12-25<br>IPv6: 2024-12-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>167.6MiB (175.8MB) – 2,906,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1918be02cf5e40016993945dcdf9fe2<br>SHA1: 26d9a8404ce0b330647e6b9dec8e0dc1f37c9773<br>SHA256: beead4d706ffee13660a84a3a4fa8d161b26172c66d7d783002d7e5e9a446e97</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>223.8MiB (234.6MB) – 2,165,543 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58aa852f4471f22d59a91349fedddaa7<br>SHA1: 58ed488a65f8f18956e7b32e6e9c4c95283bd843<br>SHA256: eff43d3a7756d1032e8d1b53d8fc159639852e5511ede4f1a0b4456657557bb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-12-24<br>IPv6: 2024-12-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.10MiB (10.59MB) – 505,890 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ace5ae80d541bc32fe8617f7c5e1ac55<br>SHA1: c14bcc0f2a499418225991f6d04187fa3547be7b<br>SHA256: 8af91359df3bb60f8809b924d0e5fca6c099b89df1824d636bb3453e29fe2ea6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.60MiB (33.13MB) – 480,212 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70d750006fe89d5803d143d8901c3cf6<br>SHA1: d47939ff314ee1f92bbd276f23e339df62ebc408<br>SHA256: a9c7be246f2a3fdf70084ddd27a2a811126cb072b1c22f4c361d124e4f7b5b63</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-12-24<br>IPv6: 2024-12-24 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>158.1MiB (165.8MB) – 3,128,134 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c4c120ccc46f04c2e5d317eaf8b8d18<br>SHA1: 4ed8ef86a67ec1f9474639f95cfb7f1883eb8e07<br>SHA256: c588ef2f8fa2d32c0f21ce888303051ac23a932311280fecdd937aaa2b3824dc</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>168.0MiB (176.2MB) – 3,128,134 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be75e7ade701867f2e5c7338bd6de2ea<br>SHA1: c837b72cc77dfba6bcc2bac1c9ca3bf2fec58cf7<br>SHA256: dd52e15b6f740770ade5407f8339e264d0363081fc6b6db5b0c5c71006a04213</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>157.2MiB (164.9MB) – 3,128,134 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62729679ec9113c2d9ace1e40299de06<br>SHA1: f81076686f5ef4b03fedc443543c240a24184750<br>SHA256: 3812f682591a4e69bf12027db73775d907f71f3141b2771dce88064b30bf53fd</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>159.4MiB (167.1MB) – 3,128,134 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41b39460b1e5daa24f338a560ed42cb2<br>SHA1: 00d29c16d7c7d55cbb84926b71b47608b8e20c19<br>SHA256: 0d7aa647105df235a31e029c0eb6446bad7249ed7d3deb764476bc78eb1dbd77</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>200.4MiB (210.2MB) – 3,128,134 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c8f1ea592af8c5b7780dee788daf6a3<br>SHA1: c3132da1961e641f2e5ae11d89a7bc18efb2fc1d<br>SHA256: df28dbfde04179d2cb3d828bdd91034d703e5c6d83219d130fd5a16aadaf8707</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>157.3MiB (164.9MB) – 3,128,134 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1dd502f9922e7be5c0e5d3384c1b9ed<br>SHA1: 5015e5680ee3fc0d1306560481191497e3a3e404<br>SHA256: 839a1c51d28a00b0e36b15f1a8f20965b76792ad78b4e36793ed85dbcd62722c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>194.8MiB (204.3MB) – 3,128,134 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ad1b803804779e90f3a7e549cce3af6<br>SHA1: 8c644fe5b297af832a0d5a0ab9cbe07cb79af7d1<br>SHA256: 8161c1fc902d2b3c8c987b13fd1107e930b65a09ff5a319c08c8633efec8b686</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>164.1MiB (172.0MB) – 3,128,134 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9244491c3aeb95dc8c5ada5090e31a05<br>SHA1: 50469b606f94236a37166b8ba1dd2be815d669d9<br>SHA256: abd18a206814d2d0a891d71f06821f31021154102b43ea005bb3a2ccfe53e05a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>161.3MiB (169.1MB) – 1,720,746 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b2bdb3114c6d63edf0617bec2ded81e<br>SHA1: 05fad7283a23a7edb2b8b3ced8cfa1b1f8ae1b0b<br>SHA256: 68dbdb539661e6161217e9d497d44d97f74d0212c917501092224a3d82f6c28b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>164.9MiB (172.9MB) – 1,720,746 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beeeed9d45ed8ebca42c3bb162594d61<br>SHA1: 34a6ce3a58ad2b0e73aa9ece831603bff8429f87<br>SHA256: 2c1ad90158a60197301068d7abebe2a6498e28496dae58e08a6ee272f0a1a5fb</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>159.4MiB (167.2MB) – 1,720,746 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 877577d8c94a738e743e718b49989727<br>SHA1: 4f42135f5d1880f0ed8e029b672961af55af3202<br>SHA256: 5e89bfacd94f056f0fc03e41e1691aee1b46ce4a0ef6931657b08373984d79fd</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>159.8MiB (167.6MB) – 1,720,746 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d656d0b38a3a5a3f607f56fa5bf25b37<br>SHA1: b2b89e13ed680f5ebd4cd35e306877d7ca58db73<br>SHA256: 26a0e6316155f8a59d77c223f3b2c39207fedb099c253854a3668a0390c405a7</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>175.5MiB (184.0MB) – 1,720,746 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea60853e1332f78f2a5f22352d76810a<br>SHA1: 507ae56651c319eccd85e198d9d1faa6b53e153c<br>SHA256: 0038e3642798d072244835380b1cafbd5b27714f1e3bbdb738602dc513b48b9b</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>159.3MiB (167.0MB) – 1,720,746 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3044b61ac71130e1c352b47c80d0a92c<br>SHA1: 27031975c7f7bb440c825037e3f8c45396924d44<br>SHA256: c04d27aee49dc9791ec60902530de501c33e0eb85b14afc7e213c2fa4d5d7a45</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>177.0MiB (185.6MB) – 1,720,746 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c77a566812163479a4957692db96214<br>SHA1: 511b99fe35360fcf8620572fc839754220e4a04c<br>SHA256: 977381a4490e75d99d08274efca258d6b3a22d0a6f1001860e2455d35fb41f79</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>162.8MiB (170.7MB) – 1,720,746 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e85c124734865261fa6a6ae698c4f7e3<br>SHA1: dba9b74b6df4ad1e93eb5c4696a9dc93330d0d90<br>SHA256: 0d4b13a3503a6c89142e775dc792cebeab2e06d75fca4f8e9e2a830ee4c7a0ac</pre></details></small> |


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
