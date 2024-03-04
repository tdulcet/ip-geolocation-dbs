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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-03-04<br>IPv6: 2024-03-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.807MiB (5.040MB) – 240,628 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11ca31b46e0b92263146c6f8a26e3d98<br>SHA1: bfea24628a7c44676400a94fc2c9277a00b65c4b<br>SHA256: f997725d32f009ef48070f1aab44c3197968f2ec0a55d7a8ba908b26d9dc522d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.711MiB (5.988MB) – 86,784 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92429b028bf4a2af62db5be4ef58a8d3<br>SHA1: 0a679bb7dee9dff1947e1ce7ad743789b0896a5a<br>SHA256: 8d48be607272ffe42d47111ffe842224a84335fb8dfde035d995986231a90007</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-03-04<br>IPv6: 2024-03-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.191MiB (8.589MB) – 410,187 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a60f6c5ca1ace01aedad1ddad11dcc4<br>SHA1: f68dd2732df6af379f9371403dfae545c485b7dd<br>SHA256: b32b438e95b4097f42548b30655e3f789280b3f69f9c0b7ec2bcc06db1ae6458</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.030MiB (7.371MB) – 106,945 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca65941267ab98d1747cedfe9c545f07<br>SHA1: 26d5ea0008c6b80502935ec93fdaa80716a9e630<br>SHA256: 5522c994c315aaff08c19df248c461d1cb319762749c29f08ee8938cf5407317</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-03-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.47MiB (18.32MB) – 874,785 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63982dde957cabdca0fb02dbbcdd2278<br>SHA1: 05e8ced509df254dd329cdb07e17962fb7039794<br>SHA256: 0d9f893041d494585ec65ce9137893126cdbb9b2d63c7b67dc6a422e7f9c6821</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>57.95MiB (60.77MB) – 880,658 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35bfb835bf24b30aec8d887fbdb4f19f<br>SHA1: f4d1268bf210db9ca5c3b6e3794b5e897cc6e4a6<br>SHA256: 6041fbcabb0249eda6bd2c84b0b9b22aedf5a77dfb0bd55018f6169624ad4ca1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 322,326 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b232d78e18dacf266bba37244688a18f<br>SHA1: 2ea0bf2a68630d5c12c6fa1d18f2f3eb0845f297<br>SHA256: b9f2935f135d22119e5db5d8d8666980b07ac2e36359fd6dbdc9c26a8b3be2f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.03MB) – 275,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49241985f6153f5f100b60421257f25<br>SHA1: 51e0348aaa544a9b75aa17c9431f3745175c5c5f<br>SHA256: 3420806d6067a2579fe3eef92e4cd09b9b792cce9c418a3ca7f3c820f4edb887</pre></details></small> |
| | | Full Location | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,158,494 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd92465491c42b3844af48593793b1d0<br>SHA1: 53a3bac0d03e0e4bef95ad11b21c1a1e92eed9f8<br>SHA256: 6157eb8d8b93b5da65533893b6b1af8682e371476cd754957d56f3cfd1179aad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>307.8MiB (322.7MB) – 2,989,351 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a432fad1dde6398b8b6ee222abf32676<br>SHA1: 78d2ec063fa05a95bb17703a5111864cd91a5446<br>SHA256: 5974cc41b3872ea8fe373def59322db31b678ff8585a6e529b9737d648343c0d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-03-04<br>IPv6: 2024-03-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.772MiB (5.004MB) – 238,843 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c15a8429d90e259b5d89e46f363cb94<br>SHA1: 11590e995ca6469691aed3ae703c69398c77a07d<br>SHA256: 36416d6d7e8c82177e05f1950529ec607ca389a020fb40fc49b45bdf0bcf638d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-03-04<br>IPv6: 2024-03-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.8MiB (178.1MB) – 2,942,325 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8bf036b2620260eba08c4b59f30ad2b5<br>SHA1: a99847ab6732f596cef7ddc2da1038c4ceb123c5<br>SHA256: a2351d207b79faebc18456f39c7c525677f4083269f536c4bf18267d2697cc0e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-03-01<br>IPv6: 2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.428MiB (9.886MB) – 472,258 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3086185af9f461ab19939f91c4b591b1<br>SHA1: 24c83c64996178778b51d19d50d5d04037f8ee55<br>SHA256: 4d2be040718cc71843543a5d8318e8f264ea4b110c2b49fd12daf52e17dedbc2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.51MiB (19.40MB) – 281,220 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 939d1118085aeff499cb619fcb2731e2<br>SHA1: 4f92bb298060269d8b3b26f964e621fa3a96a68a<br>SHA256: 08c38fac6580d0d0ba7d3eb405da952cee705bf9c6338682eb928d8fc6c522c7</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-03-01<br>IPv6: 2024-03-01 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>157.3MiB (164.9MB) – 3,340,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c74ddf7f0c38952f56c3d288e98abdf1<br>SHA1: da9dd36092458951a889049fea0312dfde1f10e6<br>SHA256: 769b6bd18c81cfc466028b8956d8b563ef968b01b66eef5a5136dd24468893c0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.8MiB (191.7MB) – 3,340,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 864f4e970970048b199f6bb82c48103f<br>SHA1: 4070a555f900dd6d0292142a8ec9171b373fa016<br>SHA256: e9ffd92f110f851b198d79167e5c568d0c618fc7de014a45a7260d500d2d1421</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>161.5MiB (169.4MB) – 3,340,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96893e63bdc11bbe642dbef9106b5a0b<br>SHA1: 6ca176668a446a5293e9ec1285dd060b19474150<br>SHA256: 98db7a4456ffd8b678e836525c8d6c85b216ac14974d244679404b9f961fd7bc</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>167.7MiB (175.8MB) – 3,340,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24fd4482e08bd681f500ff498063945b<br>SHA1: ad265ae152f7315964a4f1cb5104f00b18da10f4<br>SHA256: afa96c79c80f4785ddf7d427583729d44504a6062e3dd58ed181c92b36a0f750</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>195.9MiB (205.4MB) – 3,340,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3af767e14b84680aeea4099a63fd0e53<br>SHA1: 38f3102ba2f9c24ddbcd0629184574f0e6e622b7<br>SHA256: 5b1eb279bc7d2dd8f76c29281051c1f0e6afa62bb7ff87c425489d03afa28433</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>156.2MiB (163.8MB) – 3,340,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86c93f495c8adad1b3e408170b3f17ad<br>SHA1: 458a8110e701938b518a39b0a6ac1b622e4e550b<br>SHA256: 02cc235ab0d00850f63731823f9c325f67427b5545f94970a5ec716dd173a75b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>195.3MiB (204.8MB) – 3,340,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f0badf9397ae9b2036ac46b5378eea2<br>SHA1: 62f98f42299c851813995849cf0c0b6c93bae69e<br>SHA256: feabfe4c330e6eff306183312ae2d5d87b2c0b2a32c4fb08f1b589403927f757</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>165.0MiB (173.0MB) – 3,340,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc88d159afd1fbf08b01b267c98d5887<br>SHA1: a07bb49b41ceee0f0bbceb7fb0b9a930e506ff07<br>SHA256: af92598dc2487e9615823210aae55e2dca7d9d43eaf3d1d505470a7419130fe0</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>104.3MiB (109.3MB) – 1,165,438 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8a20459f8f8cfcaef4a4c8f113650d2<br>SHA1: 60e7fe13f02fef6928aac25e6bd281c3ce2db7d3<br>SHA256: c3d642e5133e70e30983cf3a30e82cffa0a3c46ee169a6190387b5c4d692675e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>111.9MiB (117.3MB) – 1,165,438 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736b4324afee2cbc3bc69895178044ce<br>SHA1: 541d3d9b700867e7e14b6be0ac6eae6ca39cdefb<br>SHA256: f2b2f0ba9532d8a8e79eb9e4ebb9c973e2d9b9f70ccdc9ae5f27e4fbb58fa237</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>106.5MiB (111.7MB) – 1,165,438 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 983be047114a704d5885e9203c20069a<br>SHA1: 61b670e382ec27aef7e3aedd74a077c316984963<br>SHA256: 18175c27254f59dbb1564b2b247cb9aa5f87a62f109a17a2b3d582980ccf9dee</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>107.4MiB (112.6MB) – 1,165,438 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4de8b7af0ec04635ee933f4cbcea59bb<br>SHA1: 637d24967def1944d5db0226b423da8ac9a942d4<br>SHA256: 7ad784cf4925d36b6b9ae01141388f3f398584a6dfa5acffa6e447bd045d3467</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>115.3MiB (120.9MB) – 1,165,438 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed8f82dc4c2e3303dcc514c835878925<br>SHA1: 9ef724009c3f6b668621514eb20581c2c60059dc<br>SHA256: 28ddaffe945cb51939dcf560d1a7c72a972e75aefb568426ac15c71030b7e7a9</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>105.5MiB (110.6MB) – 1,165,438 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 026fe8aba53f2d192bb6a0d9b8d33fbd<br>SHA1: 9fe59a66579a578f39204cbb5744903457acb437<br>SHA256: c2d657d9b6bf03bd2c04d80ec2d90d0d18b9959fbd86ab4bff27e5f81096a9ae</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>115.7MiB (121.3MB) – 1,165,438 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f826810f46be237d27c14c1ad04e49df<br>SHA1: 1116d7fa2510aeffc3ddd42b5d670e0f80622750<br>SHA256: d19eead9cb041be4d376e941239e3e80cdec7daeb077c7485336af3de0e2a79b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>108.3MiB (113.6MB) – 1,165,438 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1a025e2b084c2c45fd490372e6510a5<br>SHA1: d5df0216397fb37648a69d40cf9f7c319e1fb045<br>SHA256: c23f5b0cc42b0661351a5493ee2479f7e43d597f35c3fd10f4c341d6dc2cf969</pre></details></small> |


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
