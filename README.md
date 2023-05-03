[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases

IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Prepossessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [
ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Scroll right to see all the files »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
|---|---|---|---|---|---|
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-05-03<br>IPv6: 2023-05-03 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.131MiB (6.429MB) – 261,318 rows – 249 unique countries<br><small><pre>MD5: bd43795f5cdec5d1a5b09ce150349032<br>SHA1: e99bbc58327d4c808cd7a19043c67ec8952eec26<br>SHA256: 2d3cacae6b6aec344746576cf1804bf285c68f4628845d60e7569594a503a966</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.526MiB (6.843MB) – 84,483 rows – 250 unique countries<br><small><pre>MD5: 64e250f7fb82d2cbf48bc17e092feab2<br>SHA1: 09fbea815233db89af501328697891c8d9f3b9fe<br>SHA256: 6bc732bb87739987ef01bb00c089dda745c72fd950df930006f07df71d96c91c</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-05-03<br>IPv6: 2023-05-03 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.475MiB (9.935MB) – 402,448 rows – 240 unique countries<br><small><pre>MD5: 181e20850e373a0203e9574a5869a897<br>SHA1: 089c6ef0fed8398fcd1f0c7d2ac7900bddf7b623<br>SHA256: 419f2fa5e24719ff855cd92c3b4cd5874c5408932a917d1168f81d685bd56c4d</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.469MiB (7.832MB) – 96,787 rows – 221 unique countries<br><small><pre>MD5: 3c7bbdd4eecda620465a7cf55ef0e8da<br>SHA1: 74c189011c0a74f244ccdaf659123e76d41d26dd<br>SHA256: e5975fc90dc132db046a8e4ed82689051ea3c2b34c527ceb329535cf1931d3cf</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-05-03 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.88MiB (14.56MB) – 592,334 rows – 243 unique countries<br><small><pre>MD5: 087c8709b9e21131ea12002f04a71043<br>SHA1: 0730b404249ed2be6a9b9e922671b918cf263411<br>SHA256: b4c1a72ca1737cfde0eca1d365eda2fba9fd01062ddbe3a8f6c6dc114b5d2020</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>25.55MiB (26.79MB) – 330,690 rows – 243 unique countries<br><small><pre>MD5: 600df4fad44e83c3766493cfc58929b6<br>SHA1: b43fd27071459d1109e0ecd06b4704ee1e2bfe53<br>SHA256: 8177b87432644d961b850afdc99d3df869b7e4462a3e24bf1e1ff9d8850505d6</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.198MiB (7.547MB) – 308,140 rows – 243 unique countries<br><small><pre>MD5: 00b451f6412173581a7ba389f444f7b8<br>SHA1: 3581ae37ad536ccfc344035fac8da366e6f2a1c3<br>SHA256: 2632d03fe402810c0a5cd21cb01657e4bce6686f9a35a911a634e00376fe4fc8</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.40MiB (26.64MB) – 328,845 rows – 249 unique countries<br><small><pre>MD5: 6bb8a68614ae30eed99e534875572642<br>SHA1: 0ee22a19afac3f9a7cbd864af67674fe9cfc6161<br>SHA256: 7d06dc68c40737d45ad6dc84897a8b7371ad05211dc7716db73e16c197236656</pre></small> |
| | | Full Location | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>194.0MiB (203.4MB) – 3,206,976 rows – 242 unique countries<br><small><pre>MD5: 4ab320aa3a48e3e999f3451fbc5a2da8<br>SHA1: 0edbe11a0f197414c336d93dce71b581d19cd274<br>SHA256: e618d8745b11f6aff0dcb8f824c7f141c7fe734243d064f5f1fd7a093e46c571</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>365.9MiB (383.7MB) – 3,189,651 rows – 249 unique countries<br><small><pre>MD5: c56df0a8c49cfc4fafc1dd0e0ea9177e<br>SHA1: 5e57dbd6ea1ad42ff4e411c9606c8f23cb91e70c<br>SHA256: 78e7ce4abf723db571f358a92321ca5b197405f36485132b7deb8c48d31a8d5b</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-05-03<br>IPv6: 2023-05-03 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.555MiB (5.825MB) – 236,860 rows – 243 unique countries<br><small><pre>MD5: ed3a236afb3c81be58fd9e618311f040<br>SHA1: c2f909455631207019aaab2b2e46e900ebf570dc<br>SHA256: e9f4b3ba35664fef476b681b4bf974f40a7c2605e7528a86ad8bd7ec533ad95b</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.56MiB (28.90MB) – 491,350 rows – 249 unique countries<br><small><pre>MD5: 24b4cca038e3d4dcc0f42da6244a3a35<br>SHA1: 2621cb133d2002e631b0adbef75d4ea6e931756d<br>SHA256: cc4498b24a37bbe633f6502d077cf044fd12484833daf07542118c9c7c386bc1</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-05-03<br>IPv6: 2023-05-03 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,146,282 rows – 243 unique countries<br><small><pre>MD5: 88c13dfb1a052516749e7ea3a9487650<br>SHA1: 2e306a30fccb8fc193e5dd6bca9c2dc9b66b74eb<br>SHA256: eb792a298ee49d197c826b29bf481ad1c08529aa3138b1265dc37736edb20adb</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.6MiB (400.1MB) – 4,518,262 rows – 249 unique countries<br><small><pre>MD5: 7fdf49f6825c8d2c6839dbb6a75d33b8<br>SHA1: b3e158802b17935c7869bba17ff348eb8c749c91<br>SHA256: 5b247134a6e2438ebad87181e14b376f714b23fa9c8ca69d358366ad0778806a</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-05-01<br>IPv6: 2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.649MiB (10.12MB) – 411,383 rows – 250 unique countries<br><small><pre>MD5: dd4170c4e304bcd26597fd40b5dd18bb<br>SHA1: 1ac4ec7d4d003847cb695cb61fb505e41331016b<br>SHA256: 4a3a0348cb8181c1453603f59ae2ae151dba2879e551c6504edc2c924f164b51</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.86MiB (21.88MB) – 270,066 rows – 250 unique countries<br><small><pre>MD5: 77f806ea007b11bd05fea6fdf2f903e9<br>SHA1: f5642f284633628bb7359dcd204571980b24d6b3<br>SHA256: 8b01f2a7e06c5ada6570ac73f1671dc9e2405721ac5862abe372f5406648825b</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-05-01<br>IPv6: 2023-05-01 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>187.6MiB (196.8MB) – 3,734,358 rows – 250 unique countries<br><small><pre>MD5: ccc806bfc71a164f038607f9ec03e2ae<br>SHA1: 47c144a1fda4070c9cc5171b43a2b97cdae3dbd1<br>SHA256: 611919024051aa5756dcd6e556d90b2cabdffc1688a1a16b6a5346d01b3ed075</pre></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>219.8MiB (230.4MB) – 3,734,358 rows – 250 unique countries<br><small><pre>MD5: 4d8a7334c1322aee55a70665d64a0831<br>SHA1: f661221a7179a22d6996d9dfbd4aa70570ada92d<br>SHA256: 2b664e3a9d4306725473c97e22ec88e03ed036e8ee42945de82a490dd058b07d</pre></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>194.2MiB (203.6MB) – 3,734,358 rows – 250 unique countries<br><small><pre>MD5: 842c5a5dad2d5c064ef71a251868800f<br>SHA1: 344aa8b38aba780c2120ea80768e78afbe3e01bf<br>SHA256: ad14618f87aa1aa446ab502d9234b55b440dd34500bb7691d35c103be9cc3614</pre></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>201.2MiB (211.0MB) – 3,734,358 rows – 250 unique countries<br><small><pre>MD5: 20adff08c8dd85426b71ba666ee89bf3<br>SHA1: 656eba7c014c84c06997d442d44ad90d2779118a<br>SHA256: ccf745762ede524e4a90c0b1573c607976ae2ea895aa5611720a36f2f2e380b8</pre></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>236.2MiB (247.6MB) – 3,734,358 rows – 250 unique countries<br><small><pre>MD5: 76fe78f4f81a81d1d5abfab9c7d95d4d<br>SHA1: 820c65cfb8e9c90e9ce0e55e91523864e0d92ff8<br>SHA256: 9a01e24515910c1c3da3238a43505addf17c390d90de5c3699ea57d2c7ae6769</pre></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>188.9MiB (198.1MB) – 3,734,358 rows – 250 unique countries<br><small><pre>MD5: a37e0e84abf09ed45ff1502907439a51<br>SHA1: eb0fe9ff5f6e7fbfccd220cb6627657649882bc7<br>SHA256: b1f982e02dedfedb211486bb0246a4f29cc27db60c0f8ee49cffa7be273e5df7</pre></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>236.9MiB (248.4MB) – 3,734,358 rows – 250 unique countries<br><small><pre>MD5: 38668884012f1bdbf1eabc15c14d5a5a<br>SHA1: 94812a1afc27818ecc1ea2fc171b46e680b03669<br>SHA256: ac62d862077c3022e7f359c56c9e341d9bbc8ed228acfaa1909f437cfdbcec2d</pre></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>201.1MiB (210.8MB) – 3,734,358 rows – 250 unique countries<br><small><pre>MD5: 91a57da9bfeb223158b40f2ac7fc0d7c<br>SHA1: b4184ab5ba7b3a55348766b9bc3b41b451c3dfd1<br>SHA256: c2801fb4d1d01d2d03ff53c3b5ea21ed8abf7673c6eb348748b975c6e9bcd6c4</pre></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.3MiB (128.2MB) – 1,221,976 rows – 250 unique countries<br><small><pre>MD5: 8295fa78552ec7ac1aa27a5192ed05b9<br>SHA1: 303d509d1f488f9c88ed372f96824e9ea3055aad<br>SHA256: 33744da9f9cd969ce30bf4c603a316e155b082cc8da441a475358131192ca202</pre></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>130.1MiB (136.5MB) – 1,221,976 rows – 250 unique countries<br><small><pre>MD5: 4ccc8478f67c441d796a7919627ade15<br>SHA1: 36b79693a8aee92187bccef4679434f28b6cc25f<br>SHA256: 1f05bceaa7dceacc13fe42b25b281eed89c60990d6d62a851de3b1baf20cdfea</pre></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>124.5MiB (130.5MB) – 1,221,976 rows – 250 unique countries<br><small><pre>MD5: 34f65c33d9d041f2ecf3c5d38d82424d<br>SHA1: 6bc9ca6d164094681ab039bf4f3a8ca71d73ad70<br>SHA256: 36104453b5910dd4076b2fce60637889c1ea9af5d16d6c6a6040e392fde81c23</pre></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.3MiB (132.4MB) – 1,221,976 rows – 250 unique countries<br><small><pre>MD5: 17751bfec86102d60f92b0341442848b<br>SHA1: 56a05219855d16fe3d98c366efae648b0150b8e1<br>SHA256: de697231d4bd686b922012c2b60d42d88b664096655676dfad8e7ba1859a3f55</pre></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>133.7MiB (140.2MB) – 1,221,976 rows – 250 unique countries<br><small><pre>MD5: 1ad43ca5d77b4d9c2463637dee0d0ada<br>SHA1: f99b3fddacbda27e48b4750ed889ec5430e1f98f<br>SHA256: 60622ab046e2aa7484e2c3475df2ef2c76c8cbc956f5a2c2b25f01ef99bfd008</pre></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>123.7MiB (129.7MB) – 1,221,976 rows – 250 unique countries<br><small><pre>MD5: 8a43e756bd66c7f93a7555786a9bbe6b<br>SHA1: dacf512bf16f32466f62a3ac224cc84fa6134ae2<br>SHA256: f887cbb4cbc819e52a1b8085beb46e5253d692a1c1c1ede247a6f156e4d95c1f</pre></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.3MiB (140.8MB) – 1,221,976 rows – 250 unique countries<br><small><pre>MD5: 4f1295d4f0f69b4e859b2ff3df3b887d<br>SHA1: 27c3e7f1e30c17d5b24c1752dedf9e76c8d0823e<br>SHA256: 420a2a0f1979222798c3d6896720b07fbf6de7834859c9e4a70674bc894fab7a</pre></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.5MiB (132.7MB) – 1,221,976 rows – 250 unique countries<br><small><pre>MD5: 55247eb2aa5ecaab80dbcbd08915690c<br>SHA1: f138e4876abb6bfac4b5376b0f0ac3e553427a43<br>SHA256: 2a06e8e8b2a69c70dbae5c97eec545ac515529cc8650c7f1a36e2890d6871904</pre></small> |


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
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
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
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the ip address `1.0.0.0`. The numbers are 32-bit unsigned integers.
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
