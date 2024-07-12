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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-07-12<br>IPv6: 2024-07-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.744MiB (4.975MB) – 237,501 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdc2b1ab9dfb821e84cd9f338099902a<br>SHA1: 3c1dfdc32e87094651008ae26333aa3c8f33656a<br>SHA256: 47921a7cc2eff20bdf10710f1f2f6ab9d45a216eb4f03e9c480b35e8570540bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.543MiB (6.861MB) – 99,435 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f178b2de18fdc1dfcc4812fd541bb548<br>SHA1: 3c04bff62fbc36c0855572addce59033bfb6a0ea<br>SHA256: fe3eae0e9e31555ab5d91207c6fa87a56d15ab3865d8d51fc81b36afaefcc14b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-07-12<br>IPv6: 2024-07-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.098MiB (8.492MB) – 405,552 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cee63fa818f52d6526b75d7a3e1f58e3<br>SHA1: 8e050993fe84283d9e6c53d3a4b15a25b835f42f<br>SHA256: adac2587a70a547d4012b4ceb33299d92df11a978569f763dfce776bac800377</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.572MiB (6.891MB) – 99,982 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33d74745cbcb1ccccea0930d669e8ebc<br>SHA1: 652fc5c464577708b485c2dbd7a915f7984a7442<br>SHA256: c1ec45e49267b2aa84ec48c9eb422cd37c88cffc07d6cc0dfcf4b3ac2658a66a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-07-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.16MiB (17.99MB) – 858,387 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f489fd3e8fc6dc725cc8825269b9c4a<br>SHA1: df6fcee6f9f30321ac756f9238ebcee9579b9c55<br>SHA256: 9cd5d5c520c311fe3d434fd25b42daad4351eaff68133d5306a9c9e2f60f791a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.19MiB (77.80MB) – 1,127,503 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca716c130f6eab3430d1f6ef16420988<br>SHA1: beca832ae72e20450e87fbd732a31cf141215ef4<br>SHA256: 646d3e0fc9dab8b2e0ff41b82f0c6fcd2c0092fecb56d903c1cae5a41e360022</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.909MiB (7.244MB) – 347,080 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cc33d54c3bf6b9175e0b145f7c4118<br>SHA1: a3816e7df4ffb8f7c8a3e26e9ecc5b337da78413<br>SHA256: cacc1ada016c1e717e0b0224945498ec7c02f45e18e6ccc3f699cf925eb98541</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.77MiB (16.53MB) – 239,599 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d8002e2bd70b383a55c26aa6c39879<br>SHA1: 2e8b5538dfa991864d56253287cfea899c731ec6<br>SHA256: 417be26de93d6c5b8d2da113e60494952f0235ed696211cedbd93a8683cecbc7</pre></details></small> |
| | | Full Location | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,260,981 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1931ab257b12ab9982e2e837f7a344a<br>SHA1: 265a511f4b4152bd6a0cba4302e7e551263bf78e<br>SHA256: af747f9dd2423c564835352c37e87e14cf8cec475eff93b3c6b458b8ad3a8e43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>339.4MiB (355.9MB) – 3,295,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3cd81e94c6b15797cf1a60147cbd224<br>SHA1: f49f6c791890b20c1ca8c05135f5558493b09356<br>SHA256: b412df8ef796f81fa4522b3051247207cb9af864a32937188218b559f4a52daf</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-07-12<br>IPv6: 2024-07-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.882MiB (5.119MB) – 244,344 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f71b297b6d31124fb4d85a0573420148<br>SHA1: c19cd0e022cce41cdad248812b6ed96ce01f3d96<br>SHA256: 4f6fdac09cbc5c0e25e4305fde012ad03b4b27ba701095ec557f2c1ed1c594bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.18MiB (19.07MB) – 276,325 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 455753ce19833b0e8aa5a719617562cf<br>SHA1: b7cdef244498f6ea069a0523ddc0f9997aed06ad<br>SHA256: 7da4ff6463125871ea8fa12c1e2c0bb4c82cbd5eb13603b15bb06a6c12f21dbb</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-07-12<br>IPv6: 2024-07-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.9MiB (180.3MB) – 2,978,355 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec317919e654aaf26ba2956cba42987<br>SHA1: 5a1d6e846a17d001ab2649860d9e68064c6a788d<br>SHA256: 5099491c3b03773fa74caf9833a9dbb55e732c359aa505587dcd7b44b8c904e3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>200.7MiB (210.5MB) – 1,942,692 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 038ee21bebef5c2336a17368fd32209f<br>SHA1: a21d0b165419264ad815c5d369b16dde7b1ffe6c<br>SHA256: 7d3aaf19058abf9358cba535f4f8cc3c6475d21045808f084c2bc63c0857a3df</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-07-09<br>IPv6: 2024-07-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.855MiB (10.33MB) – 493,678 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2ca4ec19e216e0d62d00050f802aad2<br>SHA1: 8a03dc3158911c630fc8c7f86f7228e1ec006ec7<br>SHA256: b5ec35f24048a8458a53926d413205cea10760d943f980e1ac7f63ef41b5ac9b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.46MiB (20.41MB) – 295,775 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b96ee41ba0546705642eb43a1b5a2f41<br>SHA1: c3051e6b2dcab49bf61530fe9188d8fd7c9fbd74<br>SHA256: e4be5e0dc5c7f0e05c759e85a08a02cb5912f9f0d23da71afe12dbcb01149dcf</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-07-09<br>IPv6: 2024-07-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.6MiB (126.5MB) – 2,416,647 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5b24f24658b2e5da7402975864518e7<br>SHA1: aa8072fca08c1368df894c9ce12b06af0c371446<br>SHA256: b57f67658f1373af96585c79e49a137eadb3d2623cd575d98c119bea2eebdcf2</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.7MiB (136.0MB) – 2,416,647 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c61a666ab7440ba237179fdfba4ee450<br>SHA1: 2b42b0c160ef222049341ed46d148d91fe294fd9<br>SHA256: c3007aaa508115dcbdc43760c1c9516491a5dd92713ecc4f3701c37a7f909418</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.4MiB (126.3MB) – 2,416,647 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5ba28c541d0817adc32dbde6c986ac4<br>SHA1: e0e45ff4198cc1e189cfc7c5eabe05a57abbe967<br>SHA256: ad4e82fe654c29788e4c7395f21b015f0795b2f9692fbcdd0c112858c4abab7c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.9MiB (128.9MB) – 2,416,647 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba37c4af0269ef76621af6d32a632628<br>SHA1: c97828ee7c736c6bd1df4ba36e370c7e78ae2963<br>SHA256: 819463b4d35711f450f87c63be3e04cc71932a16a75329d7970051694e6d4552</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.3MiB (157.6MB) – 2,416,647 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0439460e90df75287efdcc1cf4880840<br>SHA1: 906dcb4e00ae3a8792c5fc8696ec9f36f17ea9a7<br>SHA256: 178f4bdd76f11abbf128c7db7a3ad656eee7c3704c6c787c4538575146dbbdad</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.7MiB (125.5MB) – 2,416,647 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd30b04868869e2a3f2b188a7d50df25<br>SHA1: 3bc4e9d65ba5212003624817c51d5c5b78cb06ff<br>SHA256: 027c9f26282d5fe6cc06c783141f2902d23c6b9bda1689631619a595c6dddee3</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.7MiB (153.8MB) – 2,416,647 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b86d149bb59d69fcef1a988724c7df5<br>SHA1: 7e91403472ebdbee441f26200239797b74de1feb<br>SHA256: 7c1ede827aa1a5a6d41e40e2c36825bc40c0bbac9270f856c2f291dd27e89040</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.1MiB (129.1MB) – 2,416,647 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55ff0dd33345b77e55134152387a31e0<br>SHA1: b10ab4ea4796d9821f1b9e6065c30ce4a59a6ad8<br>SHA256: 872486b62ec14615c32bd042fae4ea2ece1869017eb465a3bf40d785f8813b9f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>117.3MiB (123.0MB) – 1,263,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5002ebf8d834b467b9507c2ce5f71d83<br>SHA1: fee2d9ea09fe314865fb66cbf6e24145de9c6d63<br>SHA256: 2f039ecf744da3996ba6468bb5a70dbd5f06a4a6c01fd31e92a2d52c2d49db34</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>121.4MiB (127.3MB) – 1,263,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1604b737645916eaa55846f6ae996e87<br>SHA1: e728640bfa30bdf2734efd06358f5f07ea0e69f7<br>SHA256: 878ad45e2ac4a4005529c06223bb22eba0ee793a5a14dd7164369e81201d3145</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>117.6MiB (123.4MB) – 1,263,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1deefbf212231ce8f8f0f8a7b0abf1f5<br>SHA1: 24d65e256e310ea6f0c204b021ca1451cf650e95<br>SHA256: 473f1380e181c28a15dea7424066ee5e20173301cac3110204e92c2ab67edf48</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>118.1MiB (123.8MB) – 1,263,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b6c5dc224b74b16de70593b8458a2d8<br>SHA1: 9d675dc05b608441abde91667d68e91c83582e53<br>SHA256: 5226f881650b548c13d101d89c906f2942bbe47269d6b5dbfd811d2f02cc0fdf</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>129.3MiB (135.6MB) – 1,263,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 079b38c189b9df2010763b1a9f7578e1<br>SHA1: d4209b5a91ad2d2bb58ddb40ef0a2c1e56da0c2e<br>SHA256: fd62da176c93e0704320585945be9c20498b7b029850644df8d83f209c9c8630</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>117.2MiB (122.9MB) – 1,263,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8af8ca006643582d8787d2f19fdf94b<br>SHA1: b6e7669540175b4b63360f29b1626eb2df28d7a8<br>SHA256: b507205caba05cd6deeee838c4dd177961bffe100a377b80bfdfb26b71d9bef6</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>128.5MiB (134.7MB) – 1,263,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4de55222a7edad0b3c19855747290ea2<br>SHA1: f97ae39220453ae3d81f53712bc75190bbbe855b<br>SHA256: f435b3d60bbd5e6066b7d26dea95862a6c358a430862804567305276aa0d8bc2</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>119.1MiB (124.9MB) – 1,263,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 292a839d97a9c32251f2afb270d22ef3<br>SHA1: 831275e93972bbf16c24ecaa619970ef547de556<br>SHA256: a9cf177f9f5f0f700130548ccf53417027fef04994de91f6bb91afff7220650e</pre></details></small> |


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
