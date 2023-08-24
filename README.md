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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-08-24<br>IPv6: 2023-08-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.631MiB (5.904MB) – 239,898 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a542e2dcfcdc70a0d6aa975c451a8b29<br>SHA1: 7c785733efc6eb5a36b123b32e8eee1b58b6c9e9<br>SHA256: f21555a67c08c4937a583397d0fcf67f2f369e9faecef2a2ef630ecc05fcfd3f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.639MiB (6.961MB) – 85,938 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc9d3e43a04fe1287f5dd843741a2d9a<br>SHA1: 6e136ef8efa81483b19dad806b2b042c213cf7e6<br>SHA256: 3d2dcf22c4d884970bc6aea52da2ffc284c5a8121a757a5b151a93c723c3cac2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-08-24<br>IPv6: 2023-08-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.555MiB (10.02MB) – 405,866 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3208eb64f460792c6e6da71b8bf9122<br>SHA1: 4758417c2a592fc2fcd58732f41440008ec49b77<br>SHA256: f8cab48c9add560612d60cda374bdf8c2bf9d98b70d9e4fa1ce2c91db0ee3879</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.739MiB (8.115MB) – 100,287 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7646ac8706d5b2f4d542f9cd266656f5<br>SHA1: 47613e88c147b45f963444b26a8dcba722181218<br>SHA256: 948f95375fc3c8b17be7695459e5ba20cd73505d92034b176fde10d678ed21e5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-08-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.43MiB (15.13MB) – 615,566 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e948b0f35fb63234f8b0f2ee9a0ffde<br>SHA1: 1062154371f953009692644869fcda9a4c82fe71<br>SHA256: c8158b30ae99daa388c206c3f2733518fa718afee306c0bcc1ecce10aecbd8d3</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>33.39MiB (35.01MB) – 432,282 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd90f646dc870adc8c3dc1394c88ab09<br>SHA1: 18da002cefbdc57f1140d6004b99487d6e46d495<br>SHA256: 3e054c6634978bc282dee9aa6cbfe784462c10def52752234b784b11165f1d61</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.354MiB (7.711MB) – 314,876 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca76b98b742610e14368fd012848c6e<br>SHA1: 5a246f7aa51c885d4dc479284c99db5643e6770f<br>SHA256: e98c856388c6a61108e688ede0fd4bb7b818be019a620f09abfa12f09f9d4af0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.39MiB (27.67MB) – 341,571 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956b52205bafb278c0610cfec5e8e6f3<br>SHA1: 6e3ecda1bff92e53f23bf2ef3885149bc6312eff<br>SHA256: 0edd51b1478170d678f6905901a1c6a3ac7486a66f8672ee06079354a8c40436</pre></details></small> |
| | | Full Location | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.0MiB (201.3MB) – 3,170,913 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e50f1d7e16995e4854b0f105bd6c8b2b<br>SHA1: 1dcbe021497af64af841ae21163751821541e06e<br>SHA256: fa28f36a198a238e8f503e858e7561b54fb9c909d90276f58d195afea9f75250</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.8MiB (311.2MB) – 2,579,615 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bac2a6b630483711e47113caedf6461c<br>SHA1: 234b956c8061d27a07de03503b53aafee1dae740<br>SHA256: 67b384e2ddde5241f818748e689acf0bf9c436ed15bc23bd12c76eb991bd4fa3</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-08-24<br>IPv6: 2023-08-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-08-24<br>IPv6: 2023-08-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-08-21<br>IPv6: 2023-08-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.49MiB (11.00MB) – 447,687 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 501be66eb2c030dc8ba76886c468b8ed<br>SHA1: 98f7e8dfd7d3bac810a0c92e405d20ac71ec63a3<br>SHA256: fc34d96f09049841332e15f5362a5e865ec5e94329a2f50e4154e26d0057a56f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>23.01MiB (24.12MB) – 297,839 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51b68f6769955232ac9239387bf04d91<br>SHA1: 3fb7dfcdc402046853e42cc0bac2f58e942614d9<br>SHA256: f1a0723bff0b89c7ee11ec43257b7703bd4dd5420fd06113d1b9ecc54b3461dc</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-08-21<br>IPv6: 2023-08-21 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.0MiB (199.2MB) – 3,792,009 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd4ac759adbd0be2649f2f8813342060<br>SHA1: 3c0f9f3d50a384ae3d5582e1611f1632331aff1c<br>SHA256: 7e4f6a2b4938da03e5823783ce1ace61311f6a5b8854e0ff16e772ca4465bd1b</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.2MiB (233.0MB) – 3,792,009 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 872f4e377d8f79bb03939a8d527b704a<br>SHA1: 120ceffb3a3e29d03914c597b72dfcdccf9bf4e4<br>SHA256: 5950401c048dcbc1d058dd531a7ff20f3ce0fa3945637f525aa78687003ae706</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.0MiB (206.6MB) – 3,792,009 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ea299431d71cfdf33c9149c7734c24f<br>SHA1: 488851f55dc4c2fcee74e8f45db88926d5036111<br>SHA256: 0ee52ab0bbe0f516ff5f0ee6a5f1677daee65f1b6b8bc8a176cff84440e23272</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.4MiB (213.3MB) – 3,792,009 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d15d6b11ff3b4e98553447f36668a8f<br>SHA1: e75cd116b3e0d30433d84d86edbec7a00a8e4ef5<br>SHA256: 2f4d56d08fb7e7cd76479b6f116d8db51e2a22a04d9f7be0f1359cea27dbc64a</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.0MiB (250.6MB) – 3,792,009 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5ba54384a61795466eab19273d5b65d<br>SHA1: 3a9754db7a8d3d97e5fdffbfbe3ddecc1046f9e1<br>SHA256: 968c95e3d1ecf33b15e3658d5255a3db28ea07df6a79fdb406e6bae4f1059624</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.4MiB (200.7MB) – 3,792,009 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71671c4e8c585db5181398e1bbd2c81a<br>SHA1: e09e272623b814fed24efac510d08c79c9af8636<br>SHA256: 9e4092bd63fd830f4a1c21b46978a1d18f4f34193d15748d8fd9daf92e1bcc47</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.9MiB (250.5MB) – 3,792,009 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3448171b0a4bfac8a512e188fd764827<br>SHA1: 6631bd0025eb53456f2979cd27c435e164725c09<br>SHA256: 862d3a5d00576dfe92f5d73396adf7c343c933e0df885f91826f95aab7bfba2f</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.6MiB (213.5MB) – 3,792,009 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75febed45563dc198645c1746149cf52<br>SHA1: 007432b483e9dc8ab11361941c13d4f42d7f1877<br>SHA256: e1cae5fb68959e0947e75d5b3a5cd5ee93a8cc900646f7be906fee537389faf1</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>129.5MiB (135.8MB) – 1,291,994 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b7b6aa0fbe45ad2ca64646adcfe4f2<br>SHA1: 6546250740412b54f70e2efac88a9370741dd38c<br>SHA256: 50e7708fc3927b5a2becde53053be684bad03e803e56370043ac62f325391d90</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>137.8MiB (144.5MB) – 1,291,994 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea1303937fdef64464b1136a2e4beee4<br>SHA1: 304e23d4259cae299a7a5b65b60571c581fc2748<br>SHA256: 60d62d4f45290feacd7f102a8fbf8a49921abc05bb0e1a704f8deb80c34745e1</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.9MiB (138.3MB) – 1,291,994 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06f8b2b2862470836475713db9a535a8<br>SHA1: 18086837335963e629a0e946bc548edd6c9e0d64<br>SHA256: f4c0d47294caf4f258b3a6727bb5f113c42ecd0ec90ffd6010b4441ac048e2c0</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>133.8MiB (140.3MB) – 1,291,994 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30aba4dd199e306866a4976e2bfb1ec3<br>SHA1: bfb6187ac7c0d70c235f2767eba2a72d7169f79f<br>SHA256: 1730eefd50b58b170888fe27b266bca683bb77afcf5b11fa89d37439bcbd27b8</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>141.8MiB (148.6MB) – 1,291,994 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9553292a4ed92d0da80b7e5d2b5e23e<br>SHA1: 9f8613a07881850139a1b1dfb4d959fd384e91b2<br>SHA256: 80138ecbb8e0d21dbdfeee368041f283bf10a1a2c53d9a78adba979978e12d4e</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>130.8MiB (137.1MB) – 1,291,994 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ee07b8a4d3bc8b79c90f11492b20eb3<br>SHA1: bfb9e991d6c38420518ad9bb61311fa723333dff<br>SHA256: ae57f1315fe4c2aaf329c10d3c97a13b100a8e4c8963455e07c9669444d5eae9</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>142.1MiB (149.0MB) – 1,291,994 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e721f5e6378ca05012592e1479341f82<br>SHA1: 87a0759a15ac1a85e36c81ab2b2f309b000a15ba<br>SHA256: 4283b80ec82fbb0093ecea6c12f2fec81d5604e2a03145748a8538c6d2fa50b7</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>134.2MiB (140.7MB) – 1,291,994 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e057c79138c7016cea4b04e83284e668<br>SHA1: e868c1713465712c9d83c95d479922d00784a859<br>SHA256: 0da3e7287b0a616eda00c7bffa15c65508bcc0fccf40aab1209e4006c2d51f05</pre></details></small> |


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
