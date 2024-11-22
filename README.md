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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-11-22<br>IPv6: 2024-11-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.870MiB (6.156MB) – 293,943 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6988be1c269fd46b251a88fea0ddb136<br>SHA1: 71e089bf7adda7c89334490c2011c2ca3c72b240<br>SHA256: a04d8281573d9b2cde4906b735b126914564a2f181dff354fc3818c26e855746</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.52MiB (12.08MB) – 175,103 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e071cc83963ebcec31e1b9cdd2cfab7<br>SHA1: 00f8af9ed6ba094f0b33e5997f7427f035318b73<br>SHA256: 43b054a932e19c558513ebd6f3f5784a392c88663b67e8879c4d512046b7c102</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-11-22<br>IPv6: 2024-11-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.237MiB (8.637MB) – 412,496 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd594143be564a03b46e28c280d33ff4<br>SHA1: 1c57f5b0276c929c283f0f631a505672021be7b2<br>SHA256: 9a1db786a6ab66c721d5f09e05f10b2412f91a8d69f1c1d42551b62d9e723d61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.900MiB (7.235MB) – 104,974 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c073f3754db62bedcec9be09354ab94<br>SHA1: a436bb40891ce22f1288fbfad9b50fe7253dfdc4<br>SHA256: 4c61686482759fa355d8054c68dbb1750f9a9daa6c32c97e0fb6f07409c26658</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-11-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.10MiB (17.93MB) – 855,433 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17c6805a12ec24d00844ef87633d26de<br>SHA1: 662820502a2e76126725e2d5b59930f4940800f9<br>SHA256: 86a3eca88af62cec44d986a06847d0d54ded128f5b23e5c70199f71507e667e6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>81.90MiB (85.88MB) – 1,244,638 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29b52ad61179db2d8c697cf8a65515f3<br>SHA1: d12d97b325e9310fc4f44e565e6cc2dcead8c82a<br>SHA256: d6cefd7c4da199d1f6b7ebee9c9a76a5316a5ec5d23a94a6a6d3118d4fc2cd7a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.056MiB (7.399MB) – 354,248 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d0746f47a1225271996460705211255<br>SHA1: a42a4bf19e2ebf577c82e10d3834e8df68696682<br>SHA256: 436aea2efe6e1523eea5e9ba484e5efba050d65a52ade285c3f9c0212c5ed301</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.43MiB (17.22MB) – 249,619 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efdc8aeb0b5fac8527fcc97613b42d4a<br>SHA1: 05d5c2e0b0a85115285dfae791b3139e2b9eab7f<br>SHA256: 45657f0c603e4d28c566dd5f9da450499802a059e8c1ff77082c945045a71fa7</pre></details></small> |
| | | Full Location | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.2MiB (199.4MB) – 3,323,413 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e766d2e8e0a2969d4ff92cf52388660e<br>SHA1: 38d95ed8fc01158d0f5ec9aa8f3bb385ef86d3d9<br>SHA256: 7656a9190b90023870afbde735c05ae68168d21190941a5da2be92e18c8b89a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>369.3MiB (387.2MB) – 3,583,553 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23856f8e31b066ac2b1f256c563a9300<br>SHA1: 4ffab13a7c3069f5a314ea0ee72c222a02103120<br>SHA256: 9d6307032c82257b206c839119decab677631aaf7e5d3138ed4b92f8cf07acc1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-11-22<br>IPv6: 2024-11-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.926MiB (5.165MB) – 246,523 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b65d4763afb899ebad44d8601c4a4990<br>SHA1: 8bd20289ad5b22362c490ef2ad87bb040144c58e<br>SHA256: f7aebea3b623de1bee2349bcc7ee3f82183617838781052edfcba6d52b007268</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.04MB) – 275,881 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f11ddd1e6ba253a1dcb084442e38371<br>SHA1: daa137a952d33b33ca13482857f06e22c04e4de3<br>SHA256: 3c06071a088143b211f2daf1ee846920b62170ed33e0bcfb866ca24d62f88932</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-11-22<br>IPv6: 2024-11-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,018,795 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8a4e6340df7e6348b98025cba6c876a<br>SHA1: f5e6d82e8c5aa0282f73a857b7aa0817b689bdb1<br>SHA256: 42764697d53f138d6988d09099fd34cd0215bdc2ae86ce1f0ef8181c4a0bf79e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>222.0MiB (232.7MB) – 2,147,643 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a3ad0ce3e97d8698462c6efbd0b983<br>SHA1: 39b2430a2a62e400d659a0218fda59402e4382ee<br>SHA256: 979307d692a1cc91c6c103a0f51cdf68654c3ff286af4df15fe284354e67234f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-11-19<br>IPv6: 2024-11-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.03MiB (10.51MB) – 502,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8dd4c0650550ec1253dc017368877996<br>SHA1: 62ebdce34355cbac16649dca4fd74ed1c263aaa0<br>SHA256: 0d7d4fc76fe73882ce81ba0eae6acfa5e8fca4f3c28c2d28218cbb79de6f6813</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.23MiB (33.80MB) – 489,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27db342a54ddd1cd45895bbaa049b249<br>SHA1: 17db2522fc61fded99bf02c74ab77e6bc6456890<br>SHA256: 1e09d443ae1c9f2a3a6a56c2f3fa131bf366f969979818fcdbd938dad218078a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-11-19<br>IPv6: 2024-11-19 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>164.3MiB (172.3MB) – 3,244,855 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 290be4de78476210b63e0fe5f0c75eab<br>SHA1: b6b8eafb076ededac76420f867110b42b5e55c50<br>SHA256: 9005cfa14b7fca2336893d4235015ea699793e3553efbade124aea84e11ba3b9</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>174.9MiB (183.4MB) – 3,244,855 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0afa694b10a32d2bec93855a89cdf066<br>SHA1: 417e5287631f8c307e42f4fc7be40a53647220b3<br>SHA256: eb159ee752995d30869e19c4540f1c9dd3f7bf456a43d3211da09fed388cb33f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.2MiB (171.2MB) – 3,244,855 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d94ea090a9cbf847aa84f9fc2350aacd<br>SHA1: 86cd4f713cd53b7c523fbff5d0f69ca447550fee<br>SHA256: aa80237769e5b084cec75932b7aef249e6b083a3e466ca257e54e01a6820c140</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>165.7MiB (173.7MB) – 3,244,855 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4a8c133ffcdd4bcff0be6f7d757915c<br>SHA1: 35fb6e71e572dfc4de0857b63b7827e58792f1ca<br>SHA256: b5a681e63fe6dfe0728c9d5385cd2f874017d0b023518da2018dc5830e839fe3</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>208.4MiB (218.5MB) – 3,244,855 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc380209e1decdd97359d6bf89f1b855<br>SHA1: 41346cbb1d42da1599774f59be1f89a64c432036<br>SHA256: 31ea6ccff7cab544d6761c505850e9a6b506279d6fab94a47a1513264bf08c86</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>163.3MiB (171.2MB) – 3,244,855 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7d3362c87ff255120d0b73ba64db021<br>SHA1: e042eea7f0c3bfe602b14a56627263ff6243d793<br>SHA256: a820dc79d91a655e8194d4ba57095d4063e65e5fb8aed1439bd38415e0516bf9</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>202.4MiB (212.2MB) – 3,244,855 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9713c487f874b7f01b3ca413854be909<br>SHA1: e15c4e268825cb35dfffc76c51ad29fc74b6e382<br>SHA256: 4322438fdeddd54f41ad3427c76b0a0947fa2fbe665ddfb66042fd4be1d91e7a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.4MiB (178.6MB) – 3,244,855 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43705e16a34efa31ab2b3bf5b755f9cd<br>SHA1: 99d65973e0a6ad0f19e0a90b4446bf85cf042e82<br>SHA256: d22ccb14d65f59507639d37f90d05e86df69c6d86763d2d8c4a86e7e4003b309</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>156.9MiB (164.5MB) – 1,676,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e2450b6155d021aeec339ae0fda77e4<br>SHA1: aefe0696b75c3d9155e97ecb433f66c637f34b6b<br>SHA256: 7496620e67db5b80016626ced7a640aa981ca7494d40a427a179439437f9a6c4</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>160.2MiB (168.0MB) – 1,676,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d27fa91e7ff5258053931caadf98789a<br>SHA1: 5ab175f7265d25280136ddb101d9b470ad06269c<br>SHA256: 79b09c67cf9c9a7a9368e1a4ca8bbc26cbce2b854d7515b65068f23728cbf343</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.1MiB (162.6MB) – 1,676,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72beaffb841d1cd9dc22449da57fc464<br>SHA1: 78491809f89ffca590f8acf58377c804a62a59fb<br>SHA256: c83be884ef8a331efe24d1bc44f6e4d42e994d29f829b060cc2abb7cb62092fe</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>155.4MiB (162.9MB) – 1,676,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e052d62c82a865a3a2d486fcb81806b<br>SHA1: 51b5b7f0b23028fa1202c1910e54fd8a6848083e<br>SHA256: aec6acc6e352e622f3f983fb5627859126daf0056dba0d1a5322429223077874</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>170.3MiB (178.6MB) – 1,676,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2163cfea8e77a5e76cd8d436e7edbc80<br>SHA1: 9e9eb1b02b228d07b696add7364ccc6e3586cb3b<br>SHA256: d12cdd4df130caddb105db6f2cfeb2ae4a668fd6cde454eb38a7ec4047ed547a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>154.9MiB (162.4MB) – 1,676,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c72ad9371c76ae7360f737e9d1f66b98<br>SHA1: b145b2f5642e9a4eb60943a8856c729dbd86899b<br>SHA256: bd8e0c0d2f3d52a88f29cc565efddc9bd180470ac781b4f576b0aafad9ed9cff</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>171.7MiB (180.0MB) – 1,676,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c4acf11fc660b0dd31dc6d566593746<br>SHA1: 625464fbe05f2cb4ef861f76f8cc308d8f614653<br>SHA256: 8cdea2195b6d5e11d8d8c7b6b6642138d13a5b440bbaca44c8fb64fcba44cde9</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>158.2MiB (165.9MB) – 1,676,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 312b54437ff77ba3b8109f2da9833d4e<br>SHA1: 60f073597337ca0ba968e2872466fef2024cac2c<br>SHA256: c0454969628d0f67867e43c6637d6b7afb3606f0ae0956dbd233548073b3aba4</pre></details></small> |


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
