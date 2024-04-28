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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-04-28<br>IPv6: 2024-04-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.832MiB (5.066MB) – 241,876 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b74aabb917b17c0056bd9e99e3869b1<br>SHA1: 75ceb3eaea903bf909208063acf3c8b031ddc6b4<br>SHA256: d5850f471a5c10144532bcfbc16ff2da811e90754f43f0dab17b0c04ce1993e0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.227MiB (6.529MB) – 94,626 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbfe799b9558c1d52862fb64d39b5677<br>SHA1: ac1b10c2ecebbd63091c51a3bf6e3cb41f3f17f1<br>SHA256: 812e798b478b7901a568221e6026d1f16f71528b4604c03daf8959d703f3ac6a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-04-28<br>IPv6: 2024-04-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.244MiB (8.645MB) – 412,859 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 086aaf7e519fb438997658da5be89b38<br>SHA1: bf981c5ff20125ffad7630583e601ab7c817b088<br>SHA256: dd0d03e646199a5930bdbb6c32a36c0a39c5be498aa11be11168989d8b30d78c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.196MiB (7.546MB) – 109,475 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a02eb0afc438f7baa1ac862838397df0<br>SHA1: f93f991b9276e044f2c20acfc5798d3f3fc06159<br>SHA256: dd3756f545d7545e631228ab0ca44accb842f57bcfec679591bd90752317ef52</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-04-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.92MiB (18.79MB) – 896,966 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f18f5fbd990ddeb4452888e957d7b99<br>SHA1: b6000ef7b5815d2396b48f312c564d7efc5ce21c<br>SHA256: 1ede941eec8e5ba69b66d407821b7718cc49819f1140a25d78849897f4572f6b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>73.99MiB (77.59MB) – 1,124,453 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21519bb07e6177092b405b44cadb5ea7<br>SHA1: cf8b6b2f3a13338ad08a1f8396ef7eac1e3eb1d5<br>SHA256: aa04912665fea01d6c149e84becce6224e0ab16903208b82a567b64a857d8e12</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.603MiB (6.924MB) – 331,502 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed612f6829372d96d1503867a952099<br>SHA1: d545a9307049b4d56f79cfc1544864fa920d1b6b<br>SHA256: 91dde8f7a7970c4c1b8054b947e0cca9ae1b8735bdd19fe420e6e491a7427366</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.03MiB (18.91MB) – 274,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b254c68dde265fc8d6412499c6db3dd7<br>SHA1: 2cbecfceb25b68f5f0f9889993e2f4931f5e18dd<br>SHA256: e4727e6d32df38a7582a7b9172ee67820f196bd746046a5050cd654393436920</pre></details></small> |
| | | Full Location | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.8MiB (189.6MB) – 3,159,870 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e335ee8885a5e6286297a9c06a48db0a<br>SHA1: 9b10ee274410a884c26ab662fbabb41f315616a5<br>SHA256: fc15b0d16ccdb65b6da2de506405d685d02531ce5571558ba78ed3e9110dcbbe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>322.9MiB (338.6MB) – 3,132,412 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eb566a7a93d1e35f303a2978c1da77b<br>SHA1: 78d75aa920c86cb0b75dff47ca09bb4f55bb6fd9<br>SHA256: f95d154f7a461a32269f564496c943eb8cb5e61df0269c831e76ea2f52896979</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-04-28<br>IPv6: 2024-04-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.897MiB (5.134MB) – 245,145 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86953d84c1cd0d89d0994ab1cd100b39<br>SHA1: d3303729b5fdd4e92be0090d728786a641d6bdf4<br>SHA256: 9503103e96fef9a268f0d6e3e3e189c3c227ba6a962256a4be433fec98dd6295</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.43MiB (18.28MB) – 264,858 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dee1827a7716642179bea6a3edb75c4<br>SHA1: 6d32a09ab10cd650c38bb65962cded09532e32f0<br>SHA256: d1b625011cb76995dc6c5895dea53ec54db80bd372c0878631cf89b1e7957469</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-04-28<br>IPv6: 2024-04-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.5MiB (178.8MB) – 2,955,821 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 100c457dda8054191dec8cb248ef7116<br>SHA1: 5997f43cfa17dfe7406c1480e1305b0ee4d7d2b8<br>SHA256: 2e80f7bb769fbecd8a09c918b55397ec9abeb21f176c73e5c23ca937d52e974b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,714,136 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09506237fd701236f9a08be9c399f75a<br>SHA1: 012fc8437c33186fadb2add162e68a946c843774<br>SHA256: b25eb4c33c6657facc2a0eab8012f99200c9aa7dcbc9eb0f151bcbda5e02cae0</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-04-26<br>IPv6: 2024-04-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.691MiB (10.16MB) – 485,489 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d6090d80be1fb03ad5db7014056ca72<br>SHA1: 915a8aa356f98578a219d5f1b2ea20d16ac075ee<br>SHA256: 9c3503c78c3c9721a7b00ba1c441a9bc50aa4ecf1ff3a5ad35c94c2ac58f4ff8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.57MiB (19.47MB) – 282,183 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08970f545a0eeb04ec4a95d92a6a4da1<br>SHA1: a7640afdaa9e7709df79148f60eb0f714ee07e54<br>SHA256: 1656d77daa3446e6efaebd0b0e1775dda0aef95b4f7fd5a7319e172118c4d8dd</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-04-26<br>IPv6: 2024-04-26 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>121.5MiB (127.4MB) – 2,431,352 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d47af88713bf50dba4c91062fd3c7bcd<br>SHA1: 51b4341bab88c1d5e5dd48d6329af5dcde002be1<br>SHA256: 4dc6d8dd7c5fba2aa3cc6eea5619fa59b47e6f04ec6f580f55d26f0e7c2bbabf</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>130.7MiB (137.1MB) – 2,431,352 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38a7129cb2788a28df9b1a067771faaf<br>SHA1: c1c7dd7814d30a300a1e2ffef77a9a9c01291143<br>SHA256: 5b81eec448c1d585c15ac191053df8bbd694e4a6d74c7ad0910074feb8019b1c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>121.3MiB (127.2MB) – 2,431,352 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd66eb5aea550b7fcf0558b646033915<br>SHA1: 85e8fa73f16d3308b6bfa23958411e88fc610181<br>SHA256: cef8de44a9406515f85dd49136582835b3028d5c35b639631406a3d1d753ec22</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>123.7MiB (129.7MB) – 2,431,352 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1fcce2d800642c8e85c3095489f0a04c<br>SHA1: 3a66f7c29b7ccaed636dcbec226428b5be7a94e7<br>SHA256: 3dbbdd6e4c5a1c387263f5b2fe652f3f0c7280aa2699d71f3a62cfd5b4deae0e</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>151.4MiB (158.8MB) – 2,431,352 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47de12f45b2451b8fffccdcff41cb5f4<br>SHA1: d85de3158f99bc3180d7b9ac69383169ca8f44cb<br>SHA256: 5b65e01e1855af10fb818ae28022d148cba96d0662718bbb6d77a5683c6e5eb6</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>120.4MiB (126.3MB) – 2,431,352 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 079ee869dba93eb5e6512a659d8e4328<br>SHA1: dda0ebadcbe5e19f4470670feb94e3734a9fc6ec<br>SHA256: e91822361ad459f304cc9a95ec6b4b754a94e3bcffaa2811892b27ca29c25078</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>147.8MiB (155.0MB) – 2,431,352 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 619ff61b29c16e401f703b9bbe6543ca<br>SHA1: 266a1b33d66542f61e58dfe70c3f24eec38d6658<br>SHA256: 3504cbfea4208f155316289a6d48a4e7da416fedbc9a25dd2a540e8d327bd191</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>124.0MiB (130.0MB) – 2,431,352 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 864c38383c852333206ff70f0127b5e8<br>SHA1: 9dc8e10905d7c4ebb1184670020e5d42b5e87905<br>SHA256: 51e6e580cbb1cca2a16ef9b8d49f9d09efc857bcbbaf81fdc70894caa5affbde</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>112.1MiB (117.5MB) – 1,205,398 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a83f94cdd0df3310b5ea1eceaa3e7318<br>SHA1: e0e9621e1199abf3d11ffe53f5d2c8be08bf7653<br>SHA256: 01aeacdc8a162071958cfd3a5ae6cd065886b812ff76629e9e566bebd3c6c46a</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>115.9MiB (121.6MB) – 1,205,398 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1ff45584b2db99bce774e7a5d91e0ed<br>SHA1: 6345805bd591be8593a3beed25a635048c676d34<br>SHA256: e3ac6d42cb52b1979aeb056770a7ebad579c4576a34c8d38dbd0c0abff1940d5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.3MiB (117.8MB) – 1,205,398 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 728367e6dfd93f5311ca8f0e5769eeeb<br>SHA1: 370a44bb47d09636b9fa6bbe50b875f365d31306<br>SHA256: 898189d2211578c78527f1ca1df5a859226c8c15f6d03b4726ccc81904fa3ad4</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>112.8MiB (118.3MB) – 1,205,398 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2111cb257c17df2dd1b15b8f7060142e<br>SHA1: ca5cba92bdb3e201f750b003e484e720965f6dee<br>SHA256: 1b816eb50e8b998ef8e5ca7ed716e6a60368c8bf6785a6c31770e6cc7e53cc2a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>123.4MiB (129.4MB) – 1,205,398 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa12eeb0fcd717169dd44f5e74b809f6<br>SHA1: 7acc469b388e5dd84e6e21811e17b4cd445c458c<br>SHA256: f07cdeb3e5da99290bbc311fbe04f9641b6e72fc408a817d3b7c235af864ba37</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>112.0MiB (117.5MB) – 1,205,398 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01e836c9e6e821752aaeddbd229712ab<br>SHA1: f81b11ab1db26ab0c06b58a3081567f76f70992f<br>SHA256: e0f8093df9156b79144c290a8b20ca9a83b9378e712ccf4fe1cd580519d160c0</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>122.8MiB (128.7MB) – 1,205,398 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 808b31cfcb243aa14229d4d435fea86b<br>SHA1: 87d98f05d2844c63d861c4105f09797051289745<br>SHA256: 48e912fc08b004861b9e03239360429d7ac41ac26979d6cb93f048c0d7237c9f</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>113.7MiB (119.2MB) – 1,205,398 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e436580730373ff983d50bd493b456b<br>SHA1: 5e2c1b8dfa969089047e2d2cc1b7ef930252bf59<br>SHA256: 5bca63413030357e5f08c78bd92a42560c882bf9b602a0752379d0961234909a</pre></details></small> |


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
