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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-08-27<br>IPv6: 2023-08-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.635MiB (5.909MB) – 240,060 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62fd4a79c0b5aafd4c0b3b468ee73974<br>SHA1: f60a8f813ded78b1bbd254350abc648a879e6de4<br>SHA256: c85eec6c98dc02b5aa9505892f8c77f946f31e29dfe8ec2f9ba37915a1b95ed5</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.648MiB (6.971MB) – 86,061 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2846863062c4036dd31ef1390a808bb<br>SHA1: ab365d7cc81cce3951ba339520d57af4963c4ded<br>SHA256: 445155d4702c0d92e4fc539f547d25993a41a9fc8408e16c59971e28726a2c0d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-08-27<br>IPv6: 2023-08-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.545MiB (10.01MB) – 405,447 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d336f5c15262f62cbdb7b3f065d9072<br>SHA1: 3ed60ce4d7edc196792a43453bfe762cd7e956e0<br>SHA256: 3e63d2cb784580e79dbebf980674d21233f0566f6facb3c4a60ee2a1b58da9f1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.754MiB (8.130MB) – 100,472 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d1266c364892a746b329a1ecda3371d<br>SHA1: 8121e390f77d6ee70f47e524bd8b573747f8390a<br>SHA256: 8bba5b4c431c1efd7a7f8ca5bf5af2b88cd5a9bc396a19f809419957c665f924</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-08-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.43MiB (15.13MB) – 615,566 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e948b0f35fb63234f8b0f2ee9a0ffde<br>SHA1: 1062154371f953009692644869fcda9a4c82fe71<br>SHA256: c8158b30ae99daa388c206c3f2733518fa718afee306c0bcc1ecce10aecbd8d3</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>33.39MiB (35.01MB) – 432,282 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd90f646dc870adc8c3dc1394c88ab09<br>SHA1: 18da002cefbdc57f1140d6004b99487d6e46d495<br>SHA256: 3e054c6634978bc282dee9aa6cbfe784462c10def52752234b784b11165f1d61</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.354MiB (7.711MB) – 314,876 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca76b98b742610e14368fd012848c6e<br>SHA1: 5a246f7aa51c885d4dc479284c99db5643e6770f<br>SHA256: e98c856388c6a61108e688ede0fd4bb7b818be019a620f09abfa12f09f9d4af0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.39MiB (27.67MB) – 341,571 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956b52205bafb278c0610cfec5e8e6f3<br>SHA1: 6e3ecda1bff92e53f23bf2ef3885149bc6312eff<br>SHA256: 0edd51b1478170d678f6905901a1c6a3ac7486a66f8672ee06079354a8c40436</pre></details></small> |
| | | Full Location | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.0MiB (201.3MB) – 3,170,913 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e50f1d7e16995e4854b0f105bd6c8b2b<br>SHA1: 1dcbe021497af64af841ae21163751821541e06e<br>SHA256: fa28f36a198a238e8f503e858e7561b54fb9c909d90276f58d195afea9f75250</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.8MiB (311.2MB) – 2,579,615 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bac2a6b630483711e47113caedf6461c<br>SHA1: 234b956c8061d27a07de03503b53aafee1dae740<br>SHA256: 67b384e2ddde5241f818748e689acf0bf9c436ed15bc23bd12c76eb991bd4fa3</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-08-27<br>IPv6: 2023-08-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-08-27<br>IPv6: 2023-08-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-08-24<br>IPv6: 2023-08-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.18MiB (10.67MB) – 434,095 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ac8757312d11164aa0941221156090e<br>SHA1: e883794102b8bf558b368b4036b8f01f30a86320<br>SHA256: d72d7c86ba1ac93f3559f380bcd9128baa4b6edf80051cef65e38a1c4e0f7e20</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.62MiB (23.72MB) – 292,827 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04f39d8af8e7d6b0b3f3f1988ccb1ac9<br>SHA1: 1063cd287c6fcb0079e331a614375486b79ac17e<br>SHA256: cc84bf731b7ecb71d8372f64a242c91a97666e74ad7962daf5bec3adb8826d39</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-08-24<br>IPv6: 2023-08-24 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.5MiB (198.8MB) – 3,782,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b3ee3dc64bfac54b4fc3be1da497524<br>SHA1: 1d2541a57e4892605bc7628a970d4681b8b213d8<br>SHA256: f6cac045c26a08443ffc6cf249cddab347dc417d04eeba1cb3359e1a5593bfa1</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.7MiB (232.5MB) – 3,782,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a550010f7d89e8fd7300641a5f383f88<br>SHA1: e2241ffb0ce0b4738b02222c400ae88cba875bad<br>SHA256: 89f6f373c9ccbbebafbb6f9bc15884937b177f4fe866198143831cd5ca6fb627</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.6MiB (206.1MB) – 3,782,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77d652fc2591af2c64d3439b79753701<br>SHA1: b68bc1c1ae4e9a345dfccaadd5fac2e40995be99<br>SHA256: 024d31ace97dbe7f8b8e4acadb3329809db6fcbb18c4252ba4e3c7961fc48896</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.9MiB (212.8MB) – 3,782,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0579f339a5ed20247cd14182e2841dc<br>SHA1: 9edb18bc48adcd8cf52ca741efbbb3c375ead2f9<br>SHA256: 738aaf12ad5a3a88770db29f234ed0c4ebadc96e43f719d2eaf55e43033a8d3c</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.5MiB (250.1MB) – 3,782,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f6ea8d3bb1e996ad8b142decfff1f7c<br>SHA1: 2eac0a7704dab4cc3c555cba95c7bb6fa9c16ecf<br>SHA256: a20acd86abf8fc67b037bbc8fc323b6d3a663d2c3c85967432d8bba779df348e</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.9MiB (200.2MB) – 3,782,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 729e3017298b769fc0efe3da59efac2e<br>SHA1: a682581bc1fcce06d1b6b6b6ee28973c5e14acb4<br>SHA256: 4fa35892296272f9b345214533fc0f5894f74764a2353201647df810996304a0</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.3MiB (249.9MB) – 3,782,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2052f910f87054ee38dcae6c2d781b61<br>SHA1: 794b987c4ebc28c0686cb993e3ad7e065639d89f<br>SHA256: a045ce137330434f076c53826289329b0228877658252c8fde957edf1a41c9a9</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.2MiB (213.1MB) – 3,782,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b89d5523766d5d3a74d510d4a7a08b99<br>SHA1: dc94737497ba9cb5bd396640927cd9af879fa9e5<br>SHA256: 4e137ff0805a2e68e0f9dbf09f0fb78298a2987fa5ae9906826ecdb0a8dbac1d</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>129.5MiB (135.8MB) – 1,292,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b23ae36037e2f1f5ef732ee87accacb<br>SHA1: 530bb8f3cd251177ccb18364f75b5cdd6a4dc202<br>SHA256: 48fd02d27599c8198f243b6cf495ae3e999e70fb44b1152acd8b4aea85ae6cef</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>137.8MiB (144.5MB) – 1,292,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97de60ce0252e1d133483d2074d9f102<br>SHA1: ca4e5f9bbfc0b37661443ff288f592b337a26961<br>SHA256: 3e3b15cb334d3abbd21e2703301c90c129ca9fd35d1b692c51f0b83279a5fd89</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.9MiB (138.4MB) – 1,292,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b628dc111538527fd9a6d1bfa9b53fed<br>SHA1: ebe48cb616db6427e9593620ddf4224f2de8bb6d<br>SHA256: 7c76b141551edb47e0c67c0f086fea812f8c996ba4352d6b021521a7da14518f</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>133.8MiB (140.3MB) – 1,292,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f9eed237a328e4d0186085cf63dc6e1<br>SHA1: 9003e79d8cb04d290d3ee00032f15885cfb8c952<br>SHA256: 8a02b13450fa3763beff35c1f9d258c0bfa5761d243da13bcfe10cbb0fe2d37c</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>141.8MiB (148.6MB) – 1,292,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca48757a0168fa967e28df3071d2d2b5<br>SHA1: 4867dd51201cafe8e2dd1ec92b130508e56013f1<br>SHA256: 95bf5929f331f7ced12790ed0ae81a4441e02b967ff49f9666890a91556efe6e</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>130.8MiB (137.2MB) – 1,292,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8201d0381172bf405a0960e8b8f1f23<br>SHA1: 0166c6f7ed1d8cf7034c515886cdb3163584a630<br>SHA256: c8290fc4b52a4a24847d22d9092221188442c28d10d1363f1fb388e84d25de9b</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>142.1MiB (149.0MB) – 1,292,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7f2af4fdb2edb54a34907ce91c1d32b<br>SHA1: fa8392c25c481f601025a2de2e751f7e5938601c<br>SHA256: 471ed57497f1d29b17c7a0d1bc39f2f55770a70253d6e244cc46c28f1c0a3310</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>134.2MiB (140.7MB) – 1,292,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c9e367a8a4d3e90868a22de1df367ae<br>SHA1: 878c672f2da0b317268304fe3a534ea45cbc60b1<br>SHA256: af7ea87d6b59166a574cfea1e733f604b86df15cf698905a6f4c9054cb9ecd14</pre></details></small> |


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
