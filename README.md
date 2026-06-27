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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-06-26<br>IPv6: 2026-06-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.366 MiB (5.627 MB) – 268,524 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57755537a345eabc8f0bc70167ab1103<br>SHA1: e003d6d9c47d185be22b094d246a294cfd9c35e7<br>SHA256: 7787c0ab21a7a72175d912757341a79e5ec008bec0fe84c9b923b06290b52639</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.67 MiB (17.48 MB) – 253,262 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c7e399411b79f6522439eb7ae523e48<br>SHA1: 96a87effbb5334b325a207c5a2e6c898115b1b4d<br>SHA256: f3a403c910890a94770a7b20272bab8ee6dc0659008abcb0d996c0d43451f66c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-06-27<br>IPv6: 2026-06-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.976 MiB (9.412 MB) – 449,424 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28efbefefce6dd1681724028728d1a3a<br>SHA1: 9f180affc9d39e29036c852e92906995291d81b7<br>SHA256: a33b36e1e4e5db3e3528f5baa4cdd886cea3d92f0c05111b071ddc7ea4f0bab8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.873 MiB (8.256 MB) – 119,764 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 381189785d22b056ad183e9083b63a00<br>SHA1: bdbed2a04600c6e77a4fd3186dff9adce1be1d3e<br>SHA256: b2315d5778644da3567d386fdd55fac7a51edc3d93b62f9223ce7c2873637df0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-06-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.31 MiB (12.91 MB) – 616,446 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a1b2090ff12d5a0a5b1b88ab9f7372f<br>SHA1: 2639f162ac2256cda29cb9beaeb055e6d606fb0a<br>SHA256: e887368f4ed8547c93a5c28a2c8fe7389205d737ed481043f4731952883210f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>42.09 MiB (44.13 MB) – 639,636 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6cca847913b591b8559c581356e3f48<br>SHA1: 34fd462bef1b55e01a1e316b4cbc878236868a99<br>SHA256: 67d9b886dce51a7b0a62915cd0cbc36cbacc525a9df7f274b8e15fefdf992036</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.102 MiB (7.447 MB) – 355,800 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9779b594fc4d7c5fedd39074456964b0<br>SHA1: f1857d5d01ebf3fffd9827c74bc65345e8916bf3<br>SHA256: e5a4bdfa0635b5b15ba6de9b49d90e62fdc6d79622966eb6537f28dac53b051c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.76 MiB (23.87 MB) – 345,871 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 497c17574013e7a97b85c3096a788e65<br>SHA1: ce6db4fa8555a208ce550a745e54626c76a15fe4<br>SHA256: d54904ffc2bbe63f286e6ab4f05a06d3b13ca72a6eaacc9fc485461fb377cd7e</pre></details></small> |
| | | Full Location | Monthly<br>2026-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.9 MiB (220.1 MB) – 3,678,369 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4771d4369237ec9c638b9e8d923d601f<br>SHA1: 78f138eefe0b10273a8276b9f040541938bdea50<br>SHA256: 7ec412bdf605a24ab29a226dda6484d376455e55822c57e601ff87151af7af62</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.1 MiB (473.0 MB) – 4,394,152 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8837bf0f7e2750e7ba4668512a3d7db<br>SHA1: d4dd5a772d18e489ebc3f56bb07f38de2356a4d1<br>SHA256: e5a86e86fbf963ded29ad111b47f71ebb826213e62860792a6eefd696415ae18</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-06-14<br>IPv6: 2026-06-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.523 MiB (5.791 MB) – 276,445 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbbd1728d91c2745210523a6529fdc9a<br>SHA1: 428e628787b425155adbfbda44a3c9411948ff05<br>SHA256: c4d05bb79508d6b8868e55e4dc13787882c726e9f81fc664788da2a2c54284e1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.01 MiB (23.08 MB) – 334,542 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3be936503a0ec98674cc818ddc466d88<br>SHA1: afb165445966f5013414caadd96e12242e208087<br>SHA256: 2bae14aa887830b648b4459a61049b1827d63d888be282525131d2b2ceae63d5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-06-14<br>IPv6: 2026-06-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.9 MiB (175.0 MB) – 2,888,841 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a54972a25283423152f1f5299bac8bd0<br>SHA1: 29508df74e7357541d9e0b46c0d0d9d4505b128e<br>SHA256: fbe8a8513442902221aefb078c32661bf1902a31fcce1dfa4590453640b602a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.0 MiB (307.3 MB) – 2,839,959 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5361417d086b848e71911e01cd058944<br>SHA1: e777a708d40fce9b09bdb1567f279dc2ffee2115<br>SHA256: 3aad3927d0c56daa68cdd500e638d15cd6f73a8eed65b8919b663ed157a67a4d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-06-26<br>IPv6: 2026-06-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.48 MiB (12.04 MB) – 574,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3a78c8af6fc43559bb6e5e002a07281<br>SHA1: 1c6563a3f70d7b3af31d4dda0a5cdd960bcd2acf<br>SHA256: da1b5289acccebedc502a98e73b4e5a2135b1c1a8e868893f413ebed6642c436</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>37.22 MiB (39.02 MB) – 565,575 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4776fa3fea95f5b52ea3123fb4fd901<br>SHA1: 147c062d00b75e3d9a556c38820f9375b9528663<br>SHA256: d3f7287054dd82bba0fcdb10ca521b78a72b9efbb9de7f1f32a391fb42a317da</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-06-26<br>IPv6: 2026-06-26 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>193.0 MiB (202.4 MB) – 3,763,162 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: adf0e2a83ae5768dc44b9f51d4e887e6<br>SHA1: 49143ea204e6f44729664717bb40f854c40319c8<br>SHA256: 29e94c4750be5e766586a9f832267d813ce2714ee8f3f918f71862e9cd05bf25</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>202.3 MiB (212.1 MB) – 3,763,162 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f42ed2367b11c61357096db56fd9adbc<br>SHA1: 18cda1ae7b38890758d40ac415a764bfbba2cfd5<br>SHA256: ec39ce10b1cc8ed12eca6564bf59855927c640d253fa6435dc5927e22538543f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>192.3 MiB (201.6 MB) – 3,763,162 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 775bcd5a4f5e5fd143efcc995d960665<br>SHA1: e05f5d29eb0b3cd744f74b93acd5b66ac544e9a6<br>SHA256: 7e98b3716f7d7e77712e8cec86d7483481694132d5fb423e72228d350f251bbd</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>194.0 MiB (203.4 MB) – 3,763,162 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4aac87e04d5017bfefdccc54bef6c62c<br>SHA1: ba920e1d2a965bb57d182cab2592a68368ed5039<br>SHA256: 02bac61b4fd396a4364b0e7d133f994be5049bbd068288eaf895a7d40c1e7d2a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.7 MiB (256.6 MB) – 3,763,162 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d721353a21864d92bc26536b654fb6f4<br>SHA1: 56fc98d9229672796cabcb2e5102fa3906215a9f<br>SHA256: 5c0cfd05f720de48ff6a9c71d50f3c082f56473ba7b2eadd7c2bead11d4171cf</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.6 MiB (200.9 MB) – 3,763,162 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4f5cb3f442e7d07ecca974d125e079f<br>SHA1: 6ee04a377049d8bc3a69b62c91b7dbbc6e69e38c<br>SHA256: cc16aa2171aafc270ea550b1b85b878e0d84632d7b38b45c52df62896adf1d4e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.7 MiB (246.1 MB) – 3,763,162 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a80ad6d1b57f2b33ead970d9efec7a3<br>SHA1: 9c2b285ba8672e0ad4f45661f87d4eaf95176e84<br>SHA256: 900ea63b0d16bcfb491829577f0a9d7bf5a702e814d46084a64124c01975ce51</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>197.4 MiB (207.0 MB) – 3,763,162 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f81e639bbc7dd6f31e7687bf33708147<br>SHA1: 6ebd173a28c369401bc0541ffdbdc132abf2cf98<br>SHA256: 5005d09644b97b6c2d0da2f421c34bd5646e11223625bdc5fbb52486733171e0</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>197.1 MiB (206.6 MB) – 2,069,061 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16f333a66d4de5b32641ce9ce7ad41d2<br>SHA1: 2fa5c358675fae9ec84399582444250a6f93ad07<br>SHA256: 37545f3dd5b3418ab316636137e7a5fa18d7a342697d0892ae1676aa49547922</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>200.6 MiB (210.4 MB) – 2,069,061 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccf48b4c93f32337ec85086032b65e24<br>SHA1: 857c66f566bd98c12fb48d0154a8370734d20587<br>SHA256: 5a8832e2297338971ce6d9f27e852671c4f484bfe01a7b66da0eccc6fbed8d12</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>194.9 MiB (204.3 MB) – 2,069,061 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db07182ec064d6268d9382e0ddf2e15d<br>SHA1: d8d8a673adfb44b17551b1de67dbd5b0d952d565<br>SHA256: b996bfcf9572413acac65418dceecc27899b64ee8305fd89b12e9505c4f5aafb</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>195.3 MiB (204.8 MB) – 2,069,061 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fd0a2da88cd2004a72ed2139b7f5911<br>SHA1: f0bb660078e4f306ff2c6a5a3ec250d87ec266cb<br>SHA256: 7379517c322970693b502f8fc74107d99b61e54bc323021738753ef2ca1d2a83</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>217.3 MiB (227.9 MB) – 2,069,061 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3309dd420f57ad275a25958111abdb03<br>SHA1: 7308a20274d12b543234a2db1609fe88d786ae94<br>SHA256: 86a0a7b7b4c9483b6d5a6619c2a7ca0d39dc23b8ab5cf0da40d8ead8afd13d6b</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>194.9 MiB (204.3 MB) – 2,069,061 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58ee05bfa836153e4cb03d780438eba8<br>SHA1: 9f98af3a2d1a1767f0669479d4f58ad8a6fa3d62<br>SHA256: f0603e7d5b93b101aecd23072490fdd9cf8ac1a09b8e361394621650af5a8cd7</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>215.7 MiB (226.2 MB) – 2,069,061 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 617f0b2e520c19acc7a5257fe0de0246<br>SHA1: c9ef6a4fff93a1dc8bdd3f96b99b862bd4c9d7f4<br>SHA256: af76b1a5892e5825dc20df786c4a95fa0ffd197432db69c88a33c7c014b243cf</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>197.4 MiB (207.0 MB) – 2,069,061 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: deee26643409ec69205b79d474836dcc<br>SHA1: 31da2dadf1c7006d18f1e99a435ff7aae0fb312c<br>SHA256: 831398efcaf8b5fc28633c1b6a14ab4ea66626d44132eb02f2588c362f1e9af5</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
