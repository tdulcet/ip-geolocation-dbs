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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-03-01<br>IPv6: 2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-01<br>IPv6: 2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.365MiB (8.772MB) – 418,893 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cfb5bbb430bf1874dca487a41cdd96e<br>SHA1: 914dd09393334291a84d84eca6c50f8c5dfd7e19<br>SHA256: 03a63064afeba0ca3606940a0cb0e8e6ed1dc98dd68c78c1c37b466996f73b81</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.976MiB (7.314MB) – 106,121 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: caa5d312db5b8296246c49077556c371<br>SHA1: b81cb629e481ca9d6edbfeaa6e9d2ae9f6561192<br>SHA256: 1628b9ec8b57be87654311842efe0e9e6f1542fb8b28e9d7cfcfd7cc70dace6c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.57MiB (13.18MB) – 629,361 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d913f5fa8d0443a955ec7c7e80e7590<br>SHA1: e09a17fb5db358926e938103a8f311456d0ae7d0<br>SHA256: f7badaaee7fd56f566fb616414d7dcd49c5f38cd2824f941be532c773e7a56ad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>75.36MiB (79.02MB) – 1,145,241 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86207679d13b30570e3f6f0d089ea51c<br>SHA1: 23c2ce05e77fcce7b5886c16950be7770da53433<br>SHA256: 4ef940c4488b00895634de97a80e5face78f5108a5816e1b828a354b2eeb54df</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.404MiB (7.764MB) – 372,055 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e5911df23fa4121906510a5a567b13<br>SHA1: 9325bb0b20fe7cf38b086bd997249c0ea0460073<br>SHA256: 388e526b141f72da365e6c1487008eaf5440f4e2a173bfada2766c55cb3eb316</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.53MiB (17.34MB) – 251,265 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609d7024eb89dc7bd684d0207b3733b9<br>SHA1: 956350aa870d6a38630af3f3a3b53278471d39bd<br>SHA256: 95146645c0293ed5818f1df79ae51e4c9c07a1f6c91ea0f9331b8da35b754bbe</pre></details></small> |
| | | Full Location | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,335,187 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d87186c64f981273c433100841370<br>SHA1: 62922290000ef7c4549382119783c2045e4d1e6a<br>SHA256: 51718b9bcaef22b3bcf85a754a3a5fdd48d4a0efd9af8a4e3532e918a7368b41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>388.5MiB (407.4MB) – 3,770,967 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a5296fc623ecf8f0caa811c6b1aa61<br>SHA1: a31112844edcf6b611b51dd56508b700f7dfd9d1<br>SHA256: 4018f4afbdecaeedf11e8e21fc7f50e5719bc241f3a50121788f441946a9b58f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-03-01<br>IPv6: 2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.118MiB (5.367MB) – 256,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced96baa8d12dd7a7473b62ca04f3ec1<br>SHA1: f15aed8ee671e3e27c23c736e23edc25368ae1b8<br>SHA256: c034868fc655de42297d14220caccea0ab330ee13028773c38db7c6de47b21b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,344 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cef1451430608ae8ad70e0f4963dff<br>SHA1: 43bd5d1e9844ece7eae20604c4d83f7960da31a0<br>SHA256: fed2a958c9ff8365cbd35a38e1b062b5237d9c3576831c5f27705c77a13bbff3</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-03-01<br>IPv6: 2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,062,954 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1de2b09cb2477a5e3a644739a02d816<br>SHA1: 2ab572bf0cc2040a312448643055f2f718ca5ac5<br>SHA256: 1d66b45f20fdcc805cf1b87b04dc600ee7e3bcce4b90b5400d770f1ca47a3254</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>233.4MiB (244.7MB) – 2,257,726 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d52faeae6d9b914518dee2695e772b<br>SHA1: ba805ee8a2f7aede9c579332c56ae8ddfc7f7251<br>SHA256: 87cd4c71031299fc55a0c464dac619478c748c283c398787e9e7547a3ae9b9e1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-02-28<br>IPv6: 2025-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.976MiB (10.46MB) – 499,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 12ead17aa49b4bd84264e192b59a45ad<br>SHA1: 30a9d8ce2e3aceaa7737ce96ef4bdac67af8ae30<br>SHA256: c32947e5304071245ab7d2b38452c0301842299eca1139b97916718aae21bdcc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.21MiB (32.72MB) – 474,268 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 865107bb85075778632272c6b7e7df13<br>SHA1: 08d2fd395c5b4dc22dac1da4fe80bcc1a306db82<br>SHA256: 6aad2c263fd95e1998d8746243f9d5d4bd577f5e57550149a64fb325e59dcd56</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-02-28<br>IPv6: 2025-02-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.1MiB (173.2MB) – 3,266,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 382b641a8fb58dc616fcc1d5892b240c<br>SHA1: 209b3bf21e550fd32e3c3e885bf323ccd12bb121<br>SHA256: fbbcbbf2331e2223ea3f5bb0592848cc3691e714ccc768770713fd31eaadcf91</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>175.9MiB (184.5MB) – 3,266,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f65416e6b27037e09be786cd0f9cc95<br>SHA1: aec5efe5498155c55e0b7e64ee3220a7b09bd131<br>SHA256: b646419fbe132bd5f5d012de5824c6fcafde1f036f42f7b1437ae990c53c7838</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.2MiB (172.1MB) – 3,266,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c95575b0300a2ce68675bedde2e15c5f<br>SHA1: 5a32dd30b64bef5872ac14246be6e510307d1987<br>SHA256: 21490029ab13dd41fcd64f5b8ad4803fbedfc60e32821a6ea09b29667a53cd48</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.5MiB (174.6MB) – 3,266,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab94b5906ff9ed614277b465926a4e47<br>SHA1: a977f7da6781285bf383669ce7e67e5205940886<br>SHA256: 15bcdbd957cda6f6ebdec42839d0bf55c40e02b5bdef7183a77e0bcfd379fd62</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.4MiB (219.6MB) – 3,266,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9b1121912cc958a253eb41aae09ec56<br>SHA1: d6fc62d30329a0dc4c33aa9ccdab998fb5caf67d<br>SHA256: 9f824a640f89ecd4be0916f8d90871bb3a9235a02b9326e3ffadedb76c476388</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.2MiB (172.2MB) – 3,266,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d937f1057abb83ed6d3b0ca647752e4e<br>SHA1: e21497ae022e3dc9c801a30365041ea0a0a86a72<br>SHA256: deb20b1f847d340171be99ab2c38f86f2221dd50a7982de47178debfeeebd987</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.4MiB (213.3MB) – 3,266,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 760c08151940749632b16df04964f1e3<br>SHA1: a9e6f96a4aff5327d6056e076d7684392ebcfa76<br>SHA256: c371abb44a83f70b848e43150788643662ca9fd89bc636061fde121d956e4d99</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.3MiB (179.6MB) – 3,266,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a56bf7f8e109fc4b2b69581c587dea4<br>SHA1: 8110e4a7ec2c7135eb12478de6076760980fcd8f<br>SHA256: 9fb02c6fc1afba519278fd160cb9ed4399058f3267db36fd1edc7e31d4917c16</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>163.1MiB (171.1MB) – 1,739,301 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a795ccee11b12ac6231f393302f55f59<br>SHA1: 2b33523e16c114ab7e07afe70ccc1ca4a9c790eb<br>SHA256: 0f743f80a71095a5c9f697c8aba704f9a9b0c85c1dea842b9af8c1d0db1e8845</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>166.9MiB (175.0MB) – 1,739,301 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01d750ade2e38bc4c0478c120d25be71<br>SHA1: 0315a05c63885b0c93870153deb83b02f4f37ad2<br>SHA256: c20b7fcf83ddf0123b9c868bc573a5b64899091172df267f7109537784ec5d34</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>161.3MiB (169.1MB) – 1,739,301 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a2733e65fcb57c0bed23a48aa538713<br>SHA1: 700a08dc494e98f4f2f9ac190b22f50e1341327f<br>SHA256: c39df0ec56b512305e74df2ce2a629baaaf23ffca172ebf5bf31da0ded04115f</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>161.7MiB (169.5MB) – 1,739,301 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f22673b52ef2447147cd85c8b18263c8<br>SHA1: 00538c624c3bd3e0fcb76377e655a92a51135018<br>SHA256: b3a18fd41dfe7053779f7b6b3e40757729f5f211deb3e33912b29c05e78d40ed</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>177.8MiB (186.5MB) – 1,739,301 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3de3587a2ab1b8ce74bdaaa083f5eba8<br>SHA1: 07dd74ae47c97a5afc08c967c9ac4aa2d261d2b4<br>SHA256: 2ee87f8a8ce803b0a91111ebc942b7326dfe97bbccf81bc03bb4932ea27c00b1</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>161.2MiB (169.0MB) – 1,739,301 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b1d151493d1ff69d22f10a555706a9a<br>SHA1: 769784e411c795fade0d6044f044fec15c792f8e<br>SHA256: 3a0b441a2958c74c1d78a8407a87916565023552da87028dd55415d94e64399d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>179.1MiB (187.8MB) – 1,739,301 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 415d1f946a2d8ec08c94134dc24a4f4e<br>SHA1: 29331473769597e1791ff957b2608a5b4b24675b<br>SHA256: c16a7bd9e07efcca8823ec9ca80f4e71279935136857e31dd4117fbfb8beea98</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>164.9MiB (172.9MB) – 1,739,301 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f9cbd2def7b9533e92d5b430ff3e913<br>SHA1: eef2df0839249933e42053ff3f8182f27d82b4ac<br>SHA256: e215124b08565b5f3d6ceaf3d96a44fff91876037d9c8f259c242090ffc83a60</pre></details></small> |


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
