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
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-08-16<br>IPv6: 2023-08-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.677MiB (5.953MB) – 241,846 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b974c423b1e7c72110b32a36b7e5850<br>SHA1: dee2deef1405c6b5be9f0f0df17b9939194a274e<br>SHA256: 01fbe69c85927595421a55e1800bfb8e23b191a8838413333bb80593a449e734</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.589MiB (6.909MB) – 85,299 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1740705e510b84128bc79507e2edc80f<br>SHA1: e59de9da77434c623f1036e84aeabdc24daaf611<br>SHA256: efa7f7ba65a8b39ee33fe28b77ad283c479175b720222d8bb98cff91ac82b281</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-08-16<br>IPv6: 2023-08-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.541MiB (10.00MB) – 405,255 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 238b36163adb2a1d8059f55024dec67d<br>SHA1: 4566173cd398881e9b52c09324a7aa7431d0110c<br>SHA256: 1e30f8b40692423377856288f7f432161bddd22f7e5bb4e5c355e3d14dca3ea2</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.724MiB (8.099MB) – 100,082 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc074e7fc2502fa82fce638944e16b8d<br>SHA1: 6ccf7b74eb9971a5c56120ede595da1e4d59b580<br>SHA256: 6a61d6c4a49d68f9de4331425bba9c4f5e069c3d45fa01c6b81527fa0943ede5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-08-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.85MiB (15.57MB) – 633,452 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d0e0644899e99bc65fb4f163349c794<br>SHA1: 7a0a57aa92ed37412bb3a8f6c22175199d1b5ffd<br>SHA256: aff21ba06560a26e033874c554b091291cf35a328f7d80ae0eae414904b2f2ac</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>33.05MiB (34.65MB) – 427,794 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11dec23f3b086a2c9a3a08c858e6259<br>SHA1: 3cfb52d7f5ee048bdc97ed83d82ed4c9e14e9ca9<br>SHA256: 5110d80f2273504b7633c6987439b1b59234a5f0e089c8f421652326aafa758e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.354MiB (7.711MB) – 314,876 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca76b98b742610e14368fd012848c6e<br>SHA1: 5a246f7aa51c885d4dc479284c99db5643e6770f<br>SHA256: e98c856388c6a61108e688ede0fd4bb7b818be019a620f09abfa12f09f9d4af0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.39MiB (27.67MB) – 341,571 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956b52205bafb278c0610cfec5e8e6f3<br>SHA1: 6e3ecda1bff92e53f23bf2ef3885149bc6312eff<br>SHA256: 0edd51b1478170d678f6905901a1c6a3ac7486a66f8672ee06079354a8c40436</pre></details></small> |
| | | Full Location | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.0MiB (201.3MB) – 3,170,913 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e50f1d7e16995e4854b0f105bd6c8b2b<br>SHA1: 1dcbe021497af64af841ae21163751821541e06e<br>SHA256: fa28f36a198a238e8f503e858e7561b54fb9c909d90276f58d195afea9f75250</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.8MiB (311.2MB) – 2,579,615 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bac2a6b630483711e47113caedf6461c<br>SHA1: 234b956c8061d27a07de03503b53aafee1dae740<br>SHA256: 67b384e2ddde5241f818748e689acf0bf9c436ed15bc23bd12c76eb991bd4fa3</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-08-16<br>IPv6: 2023-08-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-08-16<br>IPv6: 2023-08-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-08-14<br>IPv6: 2023-08-14 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.47MiB (10.98MB) – 446,834 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a904eb2ceb9bbe2b01855c00f417ff2c<br>SHA1: 52d0e5e76693989fecbb4b1de57f28f08c66cab6<br>SHA256: 901da354fcd5146476f0975fc629f3bc02e17953a10c6801eac800bbc663775a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.70MiB (23.81MB) – 293,892 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62b0018c9e0dda8066fb3322d0bc769a<br>SHA1: b4e14439582ae2ab737e938c3b5757e8ca994d6a<br>SHA256: 04416e1de86afc26c9964a06beb1714d176856c3b29452f180fc32cdcc606f17</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-08-14<br>IPv6: 2023-08-14 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>191.1MiB (200.4MB) – 3,812,336 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0afdc245003b517c0cac8f278e8da2ec<br>SHA1: 0a33f258fac0a0e3391f735ad17992d641dcb522<br>SHA256: a8e768ed23a64f959725403213e9799f4d49456731a43b49811852d53b6fef74</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>223.5MiB (234.4MB) – 3,812,336 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31376b9ba4ed010a5f7f6009f80f49fa<br>SHA1: 27ab2d7dbbdcc55030c493be7241f848f789e287<br>SHA256: c86cf6df8306fa5a71c3611119e7157e070553f1748715002f1f575ee47fca0b</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>198.1MiB (207.7MB) – 3,812,336 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b5183feaea41ecadea35b0db1eb5cf7<br>SHA1: f95d3117709a1c0bddc2d820765eca543f55a241<br>SHA256: c920c467a01ae3d626ab8d5cf0d3c5eafe84616dc4f2edab440e15719e27604d</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>204.6MiB (214.5MB) – 3,812,336 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9e2f1b9a8a75e6b0dd40d850856eea1<br>SHA1: 60ae4fffad1120aa5c2aecaf99f7a453b83e193c<br>SHA256: ec527d7002f420e9a7bb5909ebadf09c7d0da06ceeec16aedac08f8d63b8ec85</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>240.4MiB (252.1MB) – 3,812,336 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edd43e68e1f0721601aefe2683270863<br>SHA1: 586b369acb17dbaeab03a98b383f371dc6a98b5c<br>SHA256: 634c637a24bfe66289381769b2fc001399fc4ad50316bcf6a78753ddd0d58c89</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,812,336 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd9918cd94043a1b35f6bb9c9f658ccd<br>SHA1: f24e1045f90529fcbba73c91e85b11bbd5104ca2<br>SHA256: afeb20269573e3b61a15c8292e15a574513ed6487cb1fc67cd51e52fdf376f2f</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.3MiB (252.0MB) – 3,812,336 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e79c162d4fafe80accd6f15a6436e33c<br>SHA1: feedf93a4c15e500a08a149894c3b82e3c4bc300<br>SHA256: f7ed0dab59c6caab4c42b2b8ef9d207cf2111efd88f2be4a6b457c0378aadcec</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>204.8MiB (214.8MB) – 3,812,336 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53200b6e05fb3c0f4c5476dfd495bf4d<br>SHA1: 01b05837ee8bcbf48766aa8786c89c60b4b307f3<br>SHA256: 2f1923471081eddbb6e0dffe822ac295a4a1117e7abd5370cdf24cd230037ff8</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>129.4MiB (135.7MB) – 1,291,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d3f5c0f70d02c78dd9627cf5a2102e4<br>SHA1: d25bd5a14dfdd0ae100999f4fc274f98c79cee35<br>SHA256: 0edccb0368b58df02781b58aed9f33a273ec0712f8354dfcc8ebb4d9d5ddc620</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>137.7MiB (144.4MB) – 1,291,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b84ce4c33ee852a3a975e6a603906e8a<br>SHA1: 978090dc507a23292d78a743c2c2de98f9e39f0d<br>SHA256: dad8ac69c58379cf3950d4dece46c23e17fc1a5d9410ca577375dc1f9221a5bf</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.9MiB (138.3MB) – 1,291,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6acf56e1064f82eb12d0eed78584c64<br>SHA1: 55612d6eb2372861f762f3cd250bfeda11d7b248<br>SHA256: 9460dde85ab0cf49703d34f120ee1855f4f78a38f5ccc5cca2475a5e8efa6876</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>133.7MiB (140.2MB) – 1,291,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd989d139c0eed1c51a8a68df649cb10<br>SHA1: 3c743d765ab48bb3b8e89e416631689a7b4b4911<br>SHA256: 4db8358e03d1a24e61f0c0ec6b3db5712acd0354d439052032d7ddf46f84e63e</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>141.6MiB (148.4MB) – 1,291,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 573432c4457b8013c3caeb709fb58615<br>SHA1: aa490cce5544e90d834dafdf5e83a83a550d6d63<br>SHA256: 779b925acf235bf271ec4f9ccfd1527173a73509a537aa66cf1b4597d402cc2d</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>130.7MiB (137.1MB) – 1,291,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd2269a46f08563a39c118d1e7aef303<br>SHA1: 5a6245c6540bec0c5db3b78a9efff8a6547f3060<br>SHA256: 76d1d74150db29d5e298b1e467714e2a6935884bcada5df849c435294f2b3856</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>142.0MiB (148.9MB) – 1,291,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92b34e33d8f460615ac1215d4a9f036f<br>SHA1: 5bab1d499a7248ea79c2d4e00b9a5cf450b7fbaa<br>SHA256: a5575daf18fddfaa9d3b3364dfed507e8d6346230208d30d2ce526011a802a71</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>134.1MiB (140.6MB) – 1,291,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 479d67436e989722b1509e8a257bcf10<br>SHA1: b4e2f3751ddaa48ddcf9a14177233f30327728ed<br>SHA256: a31035ff16fb0199315244d1941d32a9b1ee38573783825a082e751a3c32141e</pre></details></small> |


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
