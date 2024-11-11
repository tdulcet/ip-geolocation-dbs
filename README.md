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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-11-11<br>IPv6: 2024-11-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.894MiB (6.180MB) – 295,111 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 941eb3863805fbeb13cb38c4ca49e1d4<br>SHA1: c0af5bfdca675562e02e94c46993366aa45ff025<br>SHA256: f781b96684026c36ab0daffc2d3f76c09d46ca979db162c30c9b99aac0202ad6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.52MiB (12.08MB) – 175,043 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dbed3f555260ff5a6d2d50211142cddd<br>SHA1: 228c14eaa73bb5d347a98754597c43a35bced799<br>SHA256: 69df9bcc5ccd2149e0de0227f9509683d51e24b295e5cc4c0f7a482efde11834</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-11-11<br>IPv6: 2024-11-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.224MiB (8.624MB) – 411,862 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02b20335914de39c63f7c42fff445a0d<br>SHA1: 7286b6d8c057bc15515ae171422ac59a74f33535<br>SHA256: ef0f583fd6c6d1a7372bec4d3815d2b70d012915a95a259cbc48da9b4a86d207</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.859MiB (7.192MB) – 104,345 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d876a74cf2b4345428e11c5c47ae3d10<br>SHA1: 886fc8f4d41e0c76fcf4a303a6cbdcd9b8b030a0<br>SHA256: debc243903661480f411fb37a6eef72058ba633652aaaa5590ebd389bd04db65</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-11-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.01MiB (17.84MB) – 851,198 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dff4d4492164e78ff671209513b1fd97<br>SHA1: 7ee40cff4974ea82048c92bb3946b19978cce3ee<br>SHA256: 2aa2d6ac7863e24d6fa6f915a01b9f455204c20e78ef130378bf8ef4cd545821</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>63.32MiB (66.39MB) – 962,211 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46f200e7569bbc2b39bf9f2944077f2d<br>SHA1: 6f4c3541cb570fdd504eb9f7dec5ce705b913000<br>SHA256: 8b6afd5aeeb02e93a4d477d74675170b2c48fa5ce7e5ecf08fb4ff89c83025d8</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.056MiB (7.399MB) – 354,248 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d0746f47a1225271996460705211255<br>SHA1: a42a4bf19e2ebf577c82e10d3834e8df68696682<br>SHA256: 436aea2efe6e1523eea5e9ba484e5efba050d65a52ade285c3f9c0212c5ed301</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.43MiB (17.22MB) – 249,619 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efdc8aeb0b5fac8527fcc97613b42d4a<br>SHA1: 05d5c2e0b0a85115285dfae791b3139e2b9eab7f<br>SHA256: 45657f0c603e4d28c566dd5f9da450499802a059e8c1ff77082c945045a71fa7</pre></details></small> |
| | | Full Location | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.2MiB (199.4MB) – 3,323,413 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e766d2e8e0a2969d4ff92cf52388660e<br>SHA1: 38d95ed8fc01158d0f5ec9aa8f3bb385ef86d3d9<br>SHA256: 7656a9190b90023870afbde735c05ae68168d21190941a5da2be92e18c8b89a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>369.3MiB (387.2MB) – 3,583,553 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23856f8e31b066ac2b1f256c563a9300<br>SHA1: 4ffab13a7c3069f5a314ea0ee72c222a02103120<br>SHA256: 9d6307032c82257b206c839119decab677631aaf7e5d3138ed4b92f8cf07acc1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-11-11<br>IPv6: 2024-11-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.921MiB (5.160MB) – 246,296 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40e580b10d9fe17a204d4682e8caec62<br>SHA1: 86c3da422b58cf1b996348924dc8256bc7f8c0df<br>SHA256: 32168c3110bd3fb45b79eed0642def8db10a273ed5096e224c2de29a05e02fca</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.04MiB (19.97MB) – 289,357 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f83651873d1db0d8addc8985566a84fc<br>SHA1: acbfe44dbde35a4fdbd66b655d20885747b3b874<br>SHA256: d240a5da5dd52cc7a57780fad1a11415b8e2130d68731c1182f1798b90e567f5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-11-11<br>IPv6: 2024-11-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.6MiB (182.0MB) – 3,006,530 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3205f79a16c843aace3d3a8e3aec5334<br>SHA1: 8987d05a3901bd7ec7439251708d0c2228642999<br>SHA256: 807a107f4be6c9d0eaa439b6e63f93c3067bae3d0b264ed83a142d3318442718</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>215.9MiB (226.4MB) – 2,089,755 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e072b36b8644392e07bc9ec16c01aa89<br>SHA1: 4145eaccf7a8ff6d0571c6ac031eefdf75dee798<br>SHA256: 575d88a498458f0cac331d823e497dff499178b951353e2f6594814450a3a71b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-11-08<br>IPv6: 2024-11-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.980MiB (10.47MB) – 499,938 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64ea08e68cea550b54c9b5c3bd48e9d8<br>SHA1: 8461e140a43e1598640ea7aa75d5216d56e3ade0<br>SHA256: e59ae0f49c0787ccde08cea357c91b111e8ef178104a1c9b1cd7045fac48892a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.00MiB (33.55MB) – 486,239 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa63e57c5f9afb91c23bd187919e4778<br>SHA1: f9cd5af2223371c5995edc1aaa3c97f40646426b<br>SHA256: 623f4c2e599487af7b9cc4a0c0e38add46e7f1593c48034dcdcfc88c154753f6</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-11-08<br>IPv6: 2024-11-08 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>153.2MiB (160.6MB) – 3,024,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4602d3e0826713f7d9c8df40f43b2eee<br>SHA1: d912078ecb22bc79a562017373b28e3fe0e38143<br>SHA256: 838484d982191876c75e279fc976e272e284dc454e948127f6e00834278ebfb6</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>162.6MiB (170.5MB) – 3,024,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f141490896239ea60e90793e5e7de703<br>SHA1: 02cf58821b8767d7a4468ddc5852dbce12a4471d<br>SHA256: 56907623732bcb319b42398edcd0f2e762be5152505267cd5e3cacf9c5641b0d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>152.3MiB (159.7MB) – 3,024,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2050c2add1c637b55b8a177143f5a61<br>SHA1: 997f8f83cae96cc86a849cde98c6649ebf0a5cb7<br>SHA256: 9e59849751b8e9336bf745f681c1e06243356d29a38af309d6413b699b12f386</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>154.7MiB (162.2MB) – 3,024,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7caa280d74aabbf70b7249da77bac256<br>SHA1: 9fd8640e1d3af39fb571ee4f89a952d1a5f0d690<br>SHA256: 090b58016de602aff666363d507adb6b5dd2e9b180909af6614eea84724f7db0</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>193.9MiB (203.4MB) – 3,024,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e9b6f1f15d3dbf3afa9fb37bb888fb1<br>SHA1: 96c0c09c310c4ff790c2df904853171479da8d7e<br>SHA256: 08eab92a3b84895dacb0e8d5b8c00da7736b39d93c742f95bb99e9f1944784ac</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>152.2MiB (159.6MB) – 3,024,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f70480712f230180de8ecc89e24b32a<br>SHA1: 7c48c83bbf9753dd9c13b8e38e4acaf674054218<br>SHA256: ed686cc01ce17ff0bf88fc7a4b4887bafe130cf47266a857318a9a861d5c553e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>188.5MiB (197.7MB) – 3,024,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b15263b8ef1dcd69fcb3e6ecb35ab0f<br>SHA1: 04ca13e9e00a4dcb6e2064f441548543bd109eeb<br>SHA256: b59ac08803f982cc92d910780fb6a046246c052596cb5d24080deae2f19b72aa</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>158.6MiB (166.3MB) – 3,024,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1ecf21f295db6fef33de6f4d189f2d<br>SHA1: 54f8e34a76794e71baaa4d58d4c337620c9f338a<br>SHA256: ebf9cf66f10c290b473bec5a035e85ab172648ae35fb7ae9fd2e7e37beb78cb4</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>152.7MiB (160.1MB) – 1,633,523 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d68d6abeead06ba4f3d7da6056ab1cf<br>SHA1: 91efd302ab66acc080a717fb9ff9fadc9c90e011<br>SHA256: 5e1d46c079c84db1bad5dabcfdd90a3c7b035896a3919927ccb751cf13468169</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>155.7MiB (163.3MB) – 1,633,523 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62cab3b6b745a001cef9f40e5841c51e<br>SHA1: 6a63548f06c5445e1ae678e5bdb9f1b507de9b56<br>SHA256: 2e78d8095bcd283f39e3620ef6b0367595759e5f6a5bd6990f6491d2227b56ab</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>150.8MiB (158.1MB) – 1,633,523 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d8146217ed91ebbdf9e0c9b330144c3<br>SHA1: 0a2133cb5c5569e50e071f20963d8adfc9284465<br>SHA256: 18bcb03c280b7dba8092a646e01f7488fb0181228185b8c9b88936f6510343c3</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>151.0MiB (158.4MB) – 1,633,523 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6788526a8dff604f075c34606872b844<br>SHA1: 04bcbf7dd96f07ba1bcc7bb4e000a64221738822<br>SHA256: f24355e96d8cdbae6cc5c54439949475c94ff82131971f745a56acdee9c005e6</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>165.3MiB (173.4MB) – 1,633,523 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 698a26637310511d9044cc50b49eadeb<br>SHA1: bbf5964ea661a68089b96c5f6b7e880c2420f307<br>SHA256: 7f7256c635a8069250a20034371209b3059b2c82a2c8ce00e706cc53ad3005ce</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>150.7MiB (158.0MB) – 1,633,523 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa9a1d25bff9b69016c09df3f872b15b<br>SHA1: 77cb4d7d2174f8881b75d10dfcc9e0a0cdca45dd<br>SHA256: f83b4dfcce3f94b988481fb8ee5d7f9cdd791cb6388f910cb24c6877315f345b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>166.8MiB (174.9MB) – 1,633,523 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bd1666630a098b8aaa5b6acef6e1d53<br>SHA1: 35e2498a6b51ea4f876104605f75c819da19d520<br>SHA256: 20209e9c29a0dcc00bc63baa3fb677182a069358ae8ade61de0d50298bd453a0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>153.9MiB (161.4MB) – 1,633,523 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 960c9d4dcd4284151294e10e6075b86f<br>SHA1: fa41a1860a103589b8722d3cd73143d3736b6e3a<br>SHA256: 6751dde1228020988efbfa00165571b255013bfa9a4160d5c9c58b9415feef8f</pre></details></small> |


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
