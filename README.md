[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases

IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Scroll right to see all the files »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-05-17<br>IPv6: 2023-05-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.138MiB (6.437MB) – 261,634 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ae75afb0c608e38d75e64776631606e<br>SHA1: 3a01a09b1ccd9376002da658ab08c11ab4830fe8<br>SHA256: 4246c520c984e25f1e35289155bcb68cb81ab388afedb582b9d16dafa10c8380</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.495MiB (6.811MB) – 84,085 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4670ba0a4455cfe950f6e2aee05a2877<br>SHA1: a9d9c183fd4d644f1238c38dbf24227c8708fdfd<br>SHA256: bbc40d77a6ca4f2a69b7ab731884b0c1d9a92b2d817d1c57e4e83231e4b52bca</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-05-17<br>IPv6: 2023-05-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.447MiB (9.906MB) – 401,272 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cda458cd499ed73689ba5c58194d1a4a<br>SHA1: 1e3e4ad8ec4127d2ab432b0cad93e58ad7d3da55<br>SHA256: cd414edaac7648ed15000dceb2915f28c971b9e44e25a743b00640e4ffcb61a8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.586MiB (7.954MB) – 98,298 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce38134033f64ac6de6b20df53ce9e95<br>SHA1: 1283d1919638d51203fefddc0d6a76edd4ff11bc<br>SHA256: 1e0a009a7d1c0df9e5ac284e5335cdb8bf3e653ee9b287a661ef13126c56a125</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-05-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.68MiB (14.34MB) – 583,653 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3fe970f854c82ef5568aa78dc45cb8c7<br>SHA1: eb343a08f3ce153407c8ff8512f606237d48bf77<br>SHA256: 0634f14e78318d0599605c349f1895bdd784f74f30e16162ef9d3579cfb29fc8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>28.19MiB (29.56MB) – 364,967 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4096eaa763becbd19bd1c7cd00e0f65<br>SHA1: c1c9d12c56573e66753786482d33fb4f6a27cf2a<br>SHA256: 0fbf81aafc64aea128e3b51b42293b41c6be217394bcb8463b078a3cdfe34604</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.198MiB (7.547MB) – 308,140 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00b451f6412173581a7ba389f444f7b8<br>SHA1: 3581ae37ad536ccfc344035fac8da366e6f2a1c3<br>SHA256: 2632d03fe402810c0a5cd21cb01657e4bce6686f9a35a911a634e00376fe4fc8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.40MiB (26.64MB) – 328,845 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bb8a68614ae30eed99e534875572642<br>SHA1: 0ee22a19afac3f9a7cbd864af67674fe9cfc6161<br>SHA256: 7d06dc68c40737d45ad6dc84897a8b7371ad05211dc7716db73e16c197236656</pre></details></small> |
| | | Full Location | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>194.0MiB (203.4MB) – 3,206,976 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ab320aa3a48e3e999f3451fbc5a2da8<br>SHA1: 0edbe11a0f197414c336d93dce71b581d19cd274<br>SHA256: e618d8745b11f6aff0dcb8f824c7f141c7fe734243d064f5f1fd7a093e46c571</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>365.9MiB (383.7MB) – 3,189,651 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c56df0a8c49cfc4fafc1dd0e0ea9177e<br>SHA1: 5e57dbd6ea1ad42ff4e411c9606c8f23cb91e70c<br>SHA256: 78e7ce4abf723db571f358a92321ca5b197405f36485132b7deb8c48d31a8d5b</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-05-17<br>IPv6: 2023-05-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.555MiB (5.825MB) – 236,860 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed3a236afb3c81be58fd9e618311f040<br>SHA1: c2f909455631207019aaab2b2e46e900ebf570dc<br>SHA256: e9f4b3ba35664fef476b681b4bf974f40a7c2605e7528a86ad8bd7ec533ad95b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.56MiB (28.90MB) – 491,350 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24b4cca038e3d4dcc0f42da6244a3a35<br>SHA1: 2621cb133d2002e631b0adbef75d4ea6e931756d<br>SHA256: cc4498b24a37bbe633f6502d077cf044fd12484833daf07542118c9c7c386bc1</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-05-17<br>IPv6: 2023-05-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,146,282 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88c13dfb1a052516749e7ea3a9487650<br>SHA1: 2e306a30fccb8fc193e5dd6bca9c2dc9b66b74eb<br>SHA256: eb792a298ee49d197c826b29bf481ad1c08529aa3138b1265dc37736edb20adb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.6MiB (400.1MB) – 4,518,262 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fdf49f6825c8d2c6839dbb6a75d33b8<br>SHA1: b3e158802b17935c7869bba17ff348eb8c749c91<br>SHA256: 5b247134a6e2438ebad87181e14b376f714b23fa9c8ca69d358366ad0778806a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-05-15<br>IPv6: 2023-05-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.705MiB (10.18MB) – 413,774 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3cca34216c2479acd9f483dd60211240<br>SHA1: 96d5d65e08acb290aafa50c868f16cb0d6f351e9<br>SHA256: 37707219103d52299f2bd1eaa2e42ec92a8c8d869f7a170ea3f9d9268ba04ac0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.77MiB (22.82MB) – 281,786 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5bcaa885d81b6c63c9f13e3bc39fbc2<br>SHA1: 974d6ff9991d49475abc62da145bf1d4fe1f32be<br>SHA256: e8568105d951a016dc44624e5367b42fe88d5ec67ec32116924d86760e9f0289</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-05-15<br>IPv6: 2023-05-15 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>193.3MiB (202.7MB) – 3,844,516 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ce2803005873df5aed884b20293e9fe<br>SHA1: c38143ed4dfe2b69244581231ee7c86634e0c590<br>SHA256: de64105d7bd97b11f18002e3d919bfbcec8f1bf3fb11e76278d94ad76decab8e</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>226.6MiB (237.6MB) – 3,844,516 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba090ae73249ec86b117fc73f6fa8fcb<br>SHA1: 8b56fb59272ad4008441c74dbd855724cd8ba027<br>SHA256: c37430a1ac4ec038347980af177c3a1b463cf792ef495c1938de5460c9dfccfc</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>200.1MiB (209.8MB) – 3,844,516 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6740d81cabedc8eda94dee3c1c298275<br>SHA1: 468805954c5f577c93ca1a0789abe4f33e73c989<br>SHA256: 5cc5fa9f7767853afbceb6b084716389fc3543887fad41202b1f962e3724eaeb</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>207.3MiB (217.4MB) – 3,844,516 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c9ed7477e69d3c51b3a324992bbe090<br>SHA1: d040971c0798e39d55a098c529525e746e4056c2<br>SHA256: c91bc74a9390c897c65503b4c4acc8a2e4da1d90655a407f4cab8b8273e3ea34</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>243.4MiB (255.2MB) – 3,844,516 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a3adb96923643eeeb8aad8f1c336412<br>SHA1: d8805971d15ddaeb6f197b50af4b8ce8db93267a<br>SHA256: 27f0efa1072a9c1a3691eb979f9765d9a1f63351d59499030c466806642d8ad7</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>194.7MiB (204.1MB) – 3,844,516 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2174ae0336709b1e99dd2add240eb36<br>SHA1: 5234a22809195a361dc26b6d7c97ff3eb09f630f<br>SHA256: 4116f17b28cd7f8cba0560d8cf825d19e9abf54b0c7544d0bc2b16dde56ea3ba</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>244.1MiB (255.9MB) – 3,844,516 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90783af7012057b216f8de71dec87652<br>SHA1: 3bb69e305ede778e5fcb60c133308f68c48f72a7<br>SHA256: 97d5016f26e2f9aafb3f8b5026d074fc7bc57cc50c272ef1b08c73bed6b3245c</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>207.1MiB (217.1MB) – 3,844,516 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56d0c81df65d82b69d628db296de259b<br>SHA1: c3a95ff3aa7c271b9fa33a811a29d5e7a634bc31<br>SHA256: 8e0d461db6356990718826de138e7675367ea6f0add79bd73bac01502f9980f0</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>129.0MiB (135.3MB) – 1,285,591 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9433549395c7a1fb517ab56495486b52<br>SHA1: 93fb68d63ad033cb5106f8e3211ebae628759124<br>SHA256: e4c46e2277e390d454666832b94d24809975293bb508f4c06059e4aa64b8878b</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>137.2MiB (143.9MB) – 1,285,591 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7b9f2fcbcb12f08163933c4a82c838d<br>SHA1: d554fc1d49de8c0a30838894ff987ec03005858f<br>SHA256: c5c3efe3457631465b6889b7ef7bb9bd38d35740eac4588a029b0e030e09bf79</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.3MiB (137.6MB) – 1,285,591 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 943c557008ffaa6f2d30d7b523ce8a5a<br>SHA1: 87f664236e8995616b04ec40e623e5f2ba6cbfe9<br>SHA256: 7321b1b9bd73d33fe0c19574382f161d1ad241ca3724f2aba12cd3b879443d06</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>133.2MiB (139.6MB) – 1,285,591 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7386377b25107603cbe96647dfffeee<br>SHA1: 8f2897ccc4c783efe5867ec0011390a404c4d736<br>SHA256: 8e17a1779c247cae3bdcead852f2a60031a1edab97f3a00e155c8215b9492b53</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>140.9MiB (147.8MB) – 1,285,591 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7db789fe865a075d1eabc8a93adc35fd<br>SHA1: 7cdfa6c4bce25c63c92d3b5fcd8650dc78663f0c<br>SHA256: 98d0be40367a6f950c938a0ce02a6ec19514867ab519336ff23572d9bbdc7488</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>130.3MiB (136.6MB) – 1,285,591 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d0e8ec63fad7b2f6a753a51468ed93f<br>SHA1: 10bebaccf4bfd963931a06e913fdfe888b99acfd<br>SHA256: 11491e6b5af4c4233491997be47a80e2ad1f1dff03a78799410f1c30a5aa2a53</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>141.6MiB (148.5MB) – 1,285,591 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6744502f74640cdfd0bfd5b62136eb7<br>SHA1: a798b540da680327128ee909eaf3015e0dbeefdc<br>SHA256: 98a677d29c1d17cfa73997915ac3c75679677109ea3ebd9bde3ea7d7739e5475</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>133.4MiB (139.9MB) – 1,285,591 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 539668a0268594b9c7040e7e6c13d0ce<br>SHA1: a72c725070f59fe73cd1d7b60fadc8719340bc72<br>SHA256: 052ddea94c64b2d435aa82684582e9b6c7419c096326cd20f7d88bd72dea2d2f</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hex format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
