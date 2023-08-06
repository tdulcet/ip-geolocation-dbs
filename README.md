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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-08-06<br>IPv6: 2023-08-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.671MiB (5.946MB) – 241,587 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ee8b021f08be107bf25983f97218033<br>SHA1: 880fdb35ce6f1b1818a4b6b938434404b5a4e657<br>SHA256: 62b7e7f4115b9da4cb464a74b0fcdf0796f64d2fb3fe15e55b699770be2378f9</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.553MiB (6.871MB) – 84,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04e62fcb54c5415320901f6478d9b426<br>SHA1: 5d67c6558ef7a79c01867db11d128bae12794999<br>SHA256: 893304bf1b2729c9b42524b5ec5cfc5c56ebaeccfeaa1a3291a34e48cafbe5f2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-08-06<br>IPv6: 2023-08-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.539MiB (10.00MB) – 405,174 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: caf632d448ed21f9de9643de5f09ffb2<br>SHA1: 4473eb4cc399294c628a9e69431dbf69d9be860a<br>SHA256: e5a48d00ebf1ee806cf4731f5776544fbb55f63d0270f84fe8d6cfec79b25227</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.688MiB (8.061MB) – 99,618 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8cbb846515bf51776b70f91bcd07bad<br>SHA1: d2af357584bef6995dc0a293542bb4ba4571c110<br>SHA256: 3d2027607e74e989242d819f4826454fc20bcd8c15b7ec426650b6ff835f0027</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-08-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.69MiB (16.46MB) – 672,482 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc9402adeb393f3911ee17885ac8aa91<br>SHA1: d19f7e5df7c3a8cf9f77cc9bf5a211a2088f778d<br>SHA256: 32d2ffc93708efa119ead256ff4a4e8b381928ae8c74f2a922d4e9d0b47d9e1d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>38.38MiB (40.25MB) – 496,872 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 684f9db286a325814952d645b8ed657e<br>SHA1: 05e2fa0a75fc042860c1153dbd134e8e6fcf4cd9<br>SHA256: 9e7a7a83b08fcc22f7754f32b0878b4674703924f662b13b4f2433f96f4410aa</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.354MiB (7.711MB) – 314,876 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca76b98b742610e14368fd012848c6e<br>SHA1: 5a246f7aa51c885d4dc479284c99db5643e6770f<br>SHA256: e98c856388c6a61108e688ede0fd4bb7b818be019a620f09abfa12f09f9d4af0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.39MiB (27.67MB) – 341,571 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956b52205bafb278c0610cfec5e8e6f3<br>SHA1: 6e3ecda1bff92e53f23bf2ef3885149bc6312eff<br>SHA256: 0edd51b1478170d678f6905901a1c6a3ac7486a66f8672ee06079354a8c40436</pre></details></small> |
| | | Full Location | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.0MiB (201.3MB) – 3,170,913 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e50f1d7e16995e4854b0f105bd6c8b2b<br>SHA1: 1dcbe021497af64af841ae21163751821541e06e<br>SHA256: fa28f36a198a238e8f503e858e7561b54fb9c909d90276f58d195afea9f75250</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.8MiB (311.2MB) – 2,579,615 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bac2a6b630483711e47113caedf6461c<br>SHA1: 234b956c8061d27a07de03503b53aafee1dae740<br>SHA256: 67b384e2ddde5241f818748e689acf0bf9c436ed15bc23bd12c76eb991bd4fa3</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-08-06<br>IPv6: 2023-08-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-08-06<br>IPv6: 2023-08-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-08-03<br>IPv6: 2023-08-03 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.40MiB (10.90MB) – 443,660 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b23124dc44bf2fc20a85b9284e5c5943<br>SHA1: 8ccf16b34f50bb8165fd54a493b778b75570a41b<br>SHA256: 194f71f3a115e419930bbcb6effcf8a0d263262af4dd71a7e99e543e7ab60ebd</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.85MiB (23.96MB) – 295,765 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae9d1266b3d4572163cda49f09c20e4f<br>SHA1: d7949aed7d797c37fea0036fffe33540373582a4<br>SHA256: e2e9b26ee796542b48bd7dc2c9537adc45734b5f2a45f64e6554b30f66d6a290</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-08-03<br>IPv6: 2023-08-03 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>185.0MiB (194.0MB) – 3,693,694 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b8b5d3b89e77f2435d1075277e397d7<br>SHA1: d6728361af5f1e6547c30a10526d02090e516897<br>SHA256: 637b20c1f1311832acdf5f70389604d208acd7674396cd32cb8bb449923febf6</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>216.2MiB (226.7MB) – 3,693,694 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cbc2ec708316432a22f49bfb11eb183<br>SHA1: c139002fca3f86b90263553cdbf7776b0326de4d<br>SHA256: 49201598f48999a637851039807d4a588739a16491800a45a050352539cadf8d</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>191.7MiB (201.0MB) – 3,693,694 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee9e2655efff895acbe1def5acd08385<br>SHA1: 15b7ef85a4b99159fd49af094f6dcfa3e041d84a<br>SHA256: 700604d320721cc7559471b5ccfef1bb870a851e88b1c678f9cb77b97e54e94d</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>198.1MiB (207.8MB) – 3,693,694 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25e330525dda4836cf3f2e5439d3f07a<br>SHA1: ccb478cd1996033da93f6f95ae6a911f88e1808f<br>SHA256: 31071d1dfea1a515c0229b87e1fe97f6b2c32e0037ec474ec2931d1084a83e1e</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>233.0MiB (244.4MB) – 3,693,694 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65eee37a2abe1f49ca29191946715c2b<br>SHA1: 1a4c29cfc1895789631c8ef77a99ac829bebf6d5<br>SHA256: d8587390724f2a76396489affbebf380c141eb20afbbb0dcf21fe6087a62f9e6</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>186.4MiB (195.5MB) – 3,693,694 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4e03445d8e41fd148dcc4107957e875<br>SHA1: b9ff75e80726d10f072286b5d4263452036de47e<br>SHA256: 0c4f1abe4abe648c59df27e20da71c28b428a8db72ce0e6d16da2854c7e6e741</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>232.9MiB (244.2MB) – 3,693,694 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dccb41360baf9fd7601029840932200<br>SHA1: 337bd8574891b436c23774c551501f6bdb8589ee<br>SHA256: ec8d0e3d7e66f64834c58ca69545b014011fe93d5fade12aaa9fedc49174309e</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>198.4MiB (208.1MB) – 3,693,694 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a721ed424a93fa9d9a170079d9b19494<br>SHA1: 5db4cafad2b7e768228ecc266e73296c03124d93<br>SHA256: bb665b6fe0b59e752b964f4acd1f456c96dd8939f33bef014adc8cceebc41b33</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>124.2MiB (130.3MB) – 1,241,145 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ff98d71f688d12a34041f0132475bc0<br>SHA1: 4cca01566c810da6e1deda16fb955a0600b415cc<br>SHA256: a7e429b0ac2fdf8403e9adef2bf334c71cbb2b4c61c67ad5019ac2e25e47e3ce</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.3MiB (138.8MB) – 1,241,145 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 282e7c7eb60572ae7bd28201af3961a9<br>SHA1: 7634a1857dfd47d68af67c1b259dfdd7c59ffda5<br>SHA256: cafcbd29288c1895ddd1c7a38ef2f70bda9d90baa7a367e1cc7f1cc761ce5583</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>126.6MiB (132.7MB) – 1,241,145 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f5738eb841791c11872eb8840b056a6<br>SHA1: eeeb16213e831a2e9faa7c071b6bc0970667ba20<br>SHA256: f153a275bf25d2cc58aa3cfed03975c8a6d3917ddb5c495918cd1378d0f64373</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.5MiB (134.7MB) – 1,241,145 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2daf87f93d1bbcd153a5342471aa496<br>SHA1: 7b31e113f3d62c83cdd327e49f295e6ea3c0416e<br>SHA256: 0a26f9f1bb7724c80e04cf965384b6e8e1e5763f71fa5ff9959e18d2b9e5dd3c</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>136.0MiB (142.6MB) – 1,241,145 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0072f4ab18a2d4b4b662c89ea770415a<br>SHA1: ec7930054ed790ac0a89c4eb3af137f6a581e241<br>SHA256: 99df5650e99f558074ae1ef50a76938006c4683172bc11541ed39202dc09d31c</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>125.6MiB (131.7MB) – 1,241,145 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb9d860cc5829371a3ac0a2cd23c5610<br>SHA1: b0edac218efd185b0f425273d9f72d42011b9c7f<br>SHA256: 4d5ef1c1e80ad8015c42e3497ce69e024d80404a6cf950fde9895a31ac8b6aef</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.6MiB (143.3MB) – 1,241,145 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b14cc266a320247c9267d73ddfeb7c78<br>SHA1: 1082df0c464ecb6a00f2d9fe5d81d78e27e3fa44<br>SHA256: e1d9e5eed525a5f1325e77743ac6b656c2626242a576eedb5c1b553ad709369c</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>128.8MiB (135.0MB) – 1,241,145 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31fc121710bf0fca354db04a1347a9ad<br>SHA1: 7a11b7a1c136400e2b9058cdd47645bdb6492b83<br>SHA256: eb658c36caf9f8c85fcb94ab093dbbb7a5d5fd3300b9918af73b14f8a1281b6f</pre></details></small> |


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
