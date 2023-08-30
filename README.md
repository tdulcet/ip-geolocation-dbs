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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-08-30<br>IPv6: 2023-08-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.634MiB (5.908MB) – 240,017 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd183760ea415c79521e808b25928fe7<br>SHA1: b45e12fc326ac99f76895c53d8cc05692a984bca<br>SHA256: 3b3632f69ef3b95bd6aea9d5cde1aecaf498dc25350a04a15f4581cade547b2c</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.655MiB (6.978MB) – 86,146 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e532c2c52a264d15c623e8f96610540<br>SHA1: 3055ed8d5fe7458662ffa37fcbb0549a1d9dc5ae<br>SHA256: 3a6801eb18006580a7b093e9f3c2cb6b9d8aacf91cb543dfcdd589c5f264b488</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-08-30<br>IPv6: 2023-08-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.553MiB (10.02MB) – 405,798 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 532fe9e1a1d44548266d9185027bfa8b<br>SHA1: b634a81aae3aee7801eca41e73bf30ffb86fd446<br>SHA256: e0e7ff2964a649e8998601b45dc93fa810b083ac19a25bf2c7178fdc56ab71b9</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.770MiB (8.147MB) – 100,680 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 183554df28472e0638d8745c6353f711<br>SHA1: 7a062905696e7c4d60661998228e1aae6db9df21<br>SHA256: 19aad3e26fba7cd7251210bddaa7f4cf7b9c7510df3fb17d48ad1bbfc1ba0a19</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-08-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.35MiB (16.09MB) – 654,758 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8888f582f867fa5c7a0c6b9205215d81<br>SHA1: 634b8bf5798f647b79bf2c3863ed140fdfcf9e2e<br>SHA256: 41852c3c0076d6e8777f4e2ac17cff4f5032f281cd6672ca4e02c96d89f22f9d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>34.30MiB (35.97MB) – 444,078 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cfaf2f84cec19b1b0083551e926766d<br>SHA1: d7e42656058d4c63232b85afd717af8198708924<br>SHA256: d8383e16a23b99bfdbadbab3c504180892cdfe8c92f5ceea6d57a6c6aec04b85</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.354MiB (7.711MB) – 314,876 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca76b98b742610e14368fd012848c6e<br>SHA1: 5a246f7aa51c885d4dc479284c99db5643e6770f<br>SHA256: e98c856388c6a61108e688ede0fd4bb7b818be019a620f09abfa12f09f9d4af0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.39MiB (27.67MB) – 341,571 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956b52205bafb278c0610cfec5e8e6f3<br>SHA1: 6e3ecda1bff92e53f23bf2ef3885149bc6312eff<br>SHA256: 0edd51b1478170d678f6905901a1c6a3ac7486a66f8672ee06079354a8c40436</pre></details></small> |
| | | Full Location | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.0MiB (201.3MB) – 3,170,913 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e50f1d7e16995e4854b0f105bd6c8b2b<br>SHA1: 1dcbe021497af64af841ae21163751821541e06e<br>SHA256: fa28f36a198a238e8f503e858e7561b54fb9c909d90276f58d195afea9f75250</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.8MiB (311.2MB) – 2,579,615 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bac2a6b630483711e47113caedf6461c<br>SHA1: 234b956c8061d27a07de03503b53aafee1dae740<br>SHA256: 67b384e2ddde5241f818748e689acf0bf9c436ed15bc23bd12c76eb991bd4fa3</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-08-30<br>IPv6: 2023-08-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.512MiB (5.780MB) – 235,008 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f5b6633d21428ca1b77b02bd93ccf8b<br>SHA1: 52d80d0117cb022e501c545e2ce94f0292f49302<br>SHA256: b7ec29dd99ff8c1b7df35a0e90a87fb1ac93c22dfd85334670687358c1b14288</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.53MiB (19.43MB) – 239,903 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0828735b19358ff575bc94aeb9fd5e5d<br>SHA1: 89731a1b44a22cddc2b7f5cd9cee902f9ea0134b<br>SHA256: 32050d76fcd8c0b1edb50d74e670dcdd6ec2c415a0c478c78b5b036bbb262e48</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-08-30<br>IPv6: 2023-08-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,035,503 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25939bb2ee9379027c7ed8b48c581ef9<br>SHA1: 0cc26f98398ad29837f913a430a0614477064fba<br>SHA256: a228f642ae927e8d72503c3daf7971e53068c745a86162a71f7c0ee85e3fcacc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 1,407,049 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9148267828dd02b4a07b8d71be61e05<br>SHA1: 3385387c9e1e91d9a4fefb58750dbd3ecf5b473f<br>SHA256: 84af78d046b164d3df6de0dbc9ec0d4555678bffc281df97f9793acfc4c09d03</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-08-28<br>IPv6: 2023-08-28 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.47MiB (10.97MB) – 446,542 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52810a995b497cabe4c2221cdf5e147a<br>SHA1: 75487f9623e205c23ac89c2f30524838ed0045a4<br>SHA256: 48847a4ddf07467384ec4b88df7be23c7c943385c3bfa8a8db891200a6ec07cd</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.93MiB (24.05MB) – 296,870 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5c664388ab57680fd207275219a9ba5<br>SHA1: dfd2e440e4036eea9787de5010bc9a8d4db86628<br>SHA256: cfef4934a479416d5def86d5858e3c48cfdff1f27092f5bded07b283eac71696</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-08-28<br>IPv6: 2023-08-28 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.9MiB (199.2MB) – 3,790,584 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1e93b63bb6896b11bed3dc56ae0a300<br>SHA1: e1616cad301769db6ae5024e848bac9e1864c72f<br>SHA256: d530c2c374c0a6d4050e09ab039abbf9c2806c7acaa4282b7de255315b103d2b</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.2MiB (233.0MB) – 3,790,584 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eacd94d7cb6081447c1cf75215523679<br>SHA1: df9e589ca85bfcbf30ea63b116f3967da228b30c<br>SHA256: ddee636b1255ac25337b9d2f5c1710b986902517c2b5691b19aa9fe9f6c23ed4</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.0MiB (206.5MB) – 3,790,584 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59c5fa5674f1806134cc3c8b43edfb52<br>SHA1: cd940864e7c7d55021a203e26ba60d9d9d947270<br>SHA256: b9abcaa4ebc5da17ad66f1173fcaf9e27774e3c926e16cf2b70e0a0f7989303c</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.4MiB (213.2MB) – 3,790,584 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 539867259f71702c225b0c595e32c250<br>SHA1: b8bd943fa7a95d09dfd37dedbaa460c90d8b8699<br>SHA256: 3019782de3bf91aa5aa9a43af2f75e20308f33081b261dacb27f6e085945f64f</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.9MiB (250.5MB) – 3,790,584 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 215a502abc4c5fc0f07aa295f8363525<br>SHA1: 4e76d93fd1dccb67ad5af031b5e8fe5fb6803f57<br>SHA256: c95d9e10d243b150c22f8aee2774d092ff062e93f1fef429dad02019480b0325</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,790,584 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 472693b9a9140f55d5e3eb1913b1e5e8<br>SHA1: 64e673001544fe7e762eec9748551a55cbd364ff<br>SHA256: e06f0dd2c1e33882fbc0f643c83a388121772594a6c59d9d5bc3eb001a168da8</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.8MiB (250.4MB) – 3,790,584 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66d25d957f0c168b97aada55fe9bcf43<br>SHA1: 370c06a5b917b0e79a79c5954f1f8fd408c9fe87<br>SHA256: 7992ad6a53bd77655105a7c43bdf4a2e1c5a597bcc98909440206df07153857a</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.6MiB (213.5MB) – 3,790,584 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e9133313ce7ad14cef14f997b3d3ada<br>SHA1: e8d11537f926f76042f14b5dc0298cefdc131a16<br>SHA256: 7d438153b09c1ed2e91af14ee3ca2467bddbab9732c8cfb29491a315c88e0e2d</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>129.8MiB (136.1MB) – 1,295,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dbcbddababc438d202ac15df5e321e6a<br>SHA1: c8c19e7c24ad47b8a5e9f6c85f97050004626975<br>SHA256: afbc2784d14f5cd352aa4781c79424d0a6ff423c06833dbc890eb59dbff394c9</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>138.1MiB (144.8MB) – 1,295,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e8f43418fa271fb4e1afcaa334801c<br>SHA1: 2c570b8b41484e014b2793dc0b162f5752ae6169<br>SHA256: 227cd3682dca8dd78688b58dc7fda1e8a127e0a7d314982ff5b7e9156933c659</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>132.2MiB (138.7MB) – 1,295,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ba7c4fb6b838b4d7b9870aa6d456878<br>SHA1: d2beeb2f99a434ce1c1f26aac7b0588cba46eee4<br>SHA256: d3aadfbc80661533c0b2db66e49b4c979e904928312ea6ade9bbf623d424f006</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>134.1MiB (140.6MB) – 1,295,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dead8a092f9d17441006beef3be2fcf<br>SHA1: 86406e836c3768632f919049022ef7fea3290399<br>SHA256: 62e7798aa998f7d2a207ecd37e913ff5348919bda8011329dc287222d0faadf5</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>142.0MiB (148.9MB) – 1,295,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acb68743af7b957717e9afbd1d8193b2<br>SHA1: 0ff2882e794e3933ed104430c881b1759450a925<br>SHA256: 48f446c7aa13573f0b3fb7de961b331f2ab13ae1665bd5bbfcc227900b7c0e0e</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>131.1MiB (137.5MB) – 1,295,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a61489b612db00b96f075ea191adc18<br>SHA1: 661038035b93b1ff2c2d0d6b8bd0f6f90ac02bb0<br>SHA256: b3b7b98a2490e2671fe8e6427728a4c80e48f7540d0fc5a50be0ac7654d3612b</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>142.4MiB (149.4MB) – 1,295,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1aa8466bce5f7a9aa792c83b719f5d83<br>SHA1: 5e1c68dc81a14d703fb5f6df76ec5a1cd3aff35f<br>SHA256: 3eaa8f1f9ddab3903ec58d2f9279b11e8d2e64bde2c130de5ed5a1f96b816e59</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>134.5MiB (141.0MB) – 1,295,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efabde554c826af0a0ad79f840ea75c1<br>SHA1: 0f7efd84ea28b5989bd126c4a068fa7cd2712c76<br>SHA256: b2fe1904963dc246109fcd0e0e12f9e895ab15130d9b73f0973259a6bbe3ad67</pre></details></small> |


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
