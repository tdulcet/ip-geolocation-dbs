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
Scroll right to see all the files »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-05-19<br>IPv6: 2023-05-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.842MiB (6.126MB) – 248,824 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5421b464da555b3956b18602bbcaa81<br>SHA1: a41158085026b269916185738da22f41cfee9cfe<br>SHA256: 50062993e7d0a8b5f100879e0368c121fcc2665c2a1b4795d7fc76a18447978c</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.508MiB (6.824MB) – 84,243 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c57582e828afdd30cb8c9cafc5454956<br>SHA1: 2e5fe83ad34a948568ae25dbe564f33140b9edcc<br>SHA256: 95c281a9cde87fcf2faaab33328802d932823e11d041d3de4265f285c4fb8991</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-05-19<br>IPv6: 2023-05-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.456MiB (9.915MB) – 401,637 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf7348e9959ad7e06a1a4b381b2d888a<br>SHA1: 5234d531eef078163d3c3bf955495339c0fe9c7b<br>SHA256: 4e32a9c75d9733c42a98208b683eecd6cc99624bef4062dd1703402224e7b253</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.586MiB (7.955MB) – 98,305 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48a0a7fcf61e94c7fbb5259d58159e0b<br>SHA1: 1483ddabe3da8599af388b21ece44da07e11082d<br>SHA256: c80ec9b24b4bb65356891afd7f5ccab7048e05a8b790887f2bdf39433ef0e1ba</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-05-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.74MiB (14.41MB) – 586,457 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e52e84bc03de1089c176a9f4e4d80afc<br>SHA1: 42ee1321e6bc5b74fa188486725521d09a4c5f28<br>SHA256: f7075fecb990126bc89085f7ad36aebc360a3b7e1131f0e0c72ad0aea7cfcbc0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>34.79MiB (36.48MB) – 450,310 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b4d6f210d81b75f33b60ffd96be2639<br>SHA1: 392a7a63e6c0ca5de8d787769f840aecc8f7bc77<br>SHA256: 7ecdfc5c51657d81fb034127b2e03bea102711e43ae45abdaf75898c66476382</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.198MiB (7.547MB) – 308,140 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00b451f6412173581a7ba389f444f7b8<br>SHA1: 3581ae37ad536ccfc344035fac8da366e6f2a1c3<br>SHA256: 2632d03fe402810c0a5cd21cb01657e4bce6686f9a35a911a634e00376fe4fc8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.40MiB (26.64MB) – 328,845 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bb8a68614ae30eed99e534875572642<br>SHA1: 0ee22a19afac3f9a7cbd864af67674fe9cfc6161<br>SHA256: 7d06dc68c40737d45ad6dc84897a8b7371ad05211dc7716db73e16c197236656</pre></details></small> |
| | | Full Location | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>194.0MiB (203.4MB) – 3,206,976 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ab320aa3a48e3e999f3451fbc5a2da8<br>SHA1: 0edbe11a0f197414c336d93dce71b581d19cd274<br>SHA256: e618d8745b11f6aff0dcb8f824c7f141c7fe734243d064f5f1fd7a093e46c571</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>365.9MiB (383.7MB) – 3,189,651 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c56df0a8c49cfc4fafc1dd0e0ea9177e<br>SHA1: 5e57dbd6ea1ad42ff4e411c9606c8f23cb91e70c<br>SHA256: 78e7ce4abf723db571f358a92321ca5b197405f36485132b7deb8c48d31a8d5b</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-05-19<br>IPv6: 2023-05-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.555MiB (5.825MB) – 236,860 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed3a236afb3c81be58fd9e618311f040<br>SHA1: c2f909455631207019aaab2b2e46e900ebf570dc<br>SHA256: e9f4b3ba35664fef476b681b4bf974f40a7c2605e7528a86ad8bd7ec533ad95b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.56MiB (28.90MB) – 491,350 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24b4cca038e3d4dcc0f42da6244a3a35<br>SHA1: 2621cb133d2002e631b0adbef75d4ea6e931756d<br>SHA256: cc4498b24a37bbe633f6502d077cf044fd12484833daf07542118c9c7c386bc1</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-05-19<br>IPv6: 2023-05-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,146,282 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88c13dfb1a052516749e7ea3a9487650<br>SHA1: 2e306a30fccb8fc193e5dd6bca9c2dc9b66b74eb<br>SHA256: eb792a298ee49d197c826b29bf481ad1c08529aa3138b1265dc37736edb20adb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.6MiB (400.1MB) – 4,518,262 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fdf49f6825c8d2c6839dbb6a75d33b8<br>SHA1: b3e158802b17935c7869bba17ff348eb8c749c91<br>SHA256: 5b247134a6e2438ebad87181e14b376f714b23fa9c8ca69d358366ad0778806a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-05-18<br>IPv6: 2023-05-18 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.718MiB (10.19MB) – 414,352 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c14ba4a280cd111ac1f27688df5690bc<br>SHA1: feea6477b7e773f4f547fdc880121c40439159ab<br>SHA256: 6b0887f6bef3cd31ccb70db234af0dcb3c6e8145ce5f552e406b6be3ce70e992</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.79MiB (22.85MB) – 282,118 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00f5a8e5c1a9e1fb1cafeb05f11a81cc<br>SHA1: 0590f27ec7dcd89109ea945ee30f31c799aa7b05<br>SHA256: 4e60b75725907fade37a861dffbe3ed356b8faf0010e8aadfb11b85ae1c9016d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-05-18<br>IPv6: 2023-05-18 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>193.4MiB (202.8MB) – 3,846,750 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e64d9728d71374b1084e1d49a6bb59a<br>SHA1: bfe14b622cc4d3469e3a2f7b1c311abfd607da80<br>SHA256: ea6d543c40d63c0d35274202336238a2863219517cf20872b4555f0c7c38634a</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>226.7MiB (237.7MB) – 3,846,750 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9ce352be1c2bfe09aed8a4d99112299<br>SHA1: 24d4ebc33da87cca757cafbf985b60adec001d90<br>SHA256: 8eaaf257701b16bf48aac8ea318e265f933428d942de4d5eaaf339678452cce8</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>200.2MiB (209.9MB) – 3,846,750 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf641fd672e351a4b80e7081b56e5d17<br>SHA1: 98a8549cd981b998c99a9805f500446f440ff748<br>SHA256: b9e7222c1d2df93a1f8cfa41a05395311ba76ba7ea20033ad23c70679b7415af</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>207.4MiB (217.5MB) – 3,846,750 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d54b56127ada40b3c05b1a575f2811bf<br>SHA1: 457768072f9fd2d3c1511ec8281a3ad8c96718d3<br>SHA256: c6757fd7a2a31076ca1c38b58bb2fa253150c56024dbd9638507eac9d86e9d44</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>243.5MiB (255.4MB) – 3,846,750 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dbe436047feba7ad8172a670e276eb29<br>SHA1: 7ed73fdcecb8a1062b9e9a0d162820999e164035<br>SHA256: a74a15d2e60c745ea4a7c910bac41792210dade9df56e18213842f36061af7fd</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>194.8MiB (204.2MB) – 3,846,750 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b5068a72a0c7fddfd19b9029520549a<br>SHA1: f51a1c3015b824a950eacc8f6c31773bdb8d8a76<br>SHA256: c382aeb84b239888998767111a26af72f686c0794841f30d40d4d8c717ea8c1b</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>244.2MiB (256.1MB) – 3,846,750 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9c70eb9ff6c01cb0bbb0742abec58ba<br>SHA1: d27fa43f9641b1402b69755db7067148068f0ef7<br>SHA256: 2d6fac1f9fd693f5a92d872ab81f759c3e2a9966c4ba424e55e26b63acc0ad38</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>207.2MiB (217.3MB) – 3,846,750 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05fbb585cd7f5669b517885c2bd2f21c<br>SHA1: de4df0a772589a68d18ec10e5ac0c028fce7459b<br>SHA256: 89e1de49ce3516280fac893154f56a5f8b46f3e2a6b7b7090c96f5017797b914</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>129.2MiB (135.4MB) – 1,286,821 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 376d1d519fec72c2c292a4e7cff063f2<br>SHA1: 8523ef153bdf86523ff7a3a7b70bfb8e0fcd24a0<br>SHA256: afcc069c36676764708ca2e44d464162d2b010197a7cb45986e983f4ecfb9154</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>137.4MiB (144.0MB) – 1,286,821 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6d9c02211a0233cf9832f9ea7a684fc<br>SHA1: cb572d7c473d57b2471cd1ee06363821ab07b2a0<br>SHA256: a1344db65c58b03c0607e1de9d53dea3855e5a1aca40bfd29b13017f7b548939</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.4MiB (137.8MB) – 1,286,821 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c08d919ba61dbbc78233924740143ed9<br>SHA1: e3830d6c03d45067302ac68254c1397e611010ba<br>SHA256: 2a4c9c78208e5462ea952a6bdeb4659223a6616e790d9e50d9fcf25d63cdf8a9</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>133.3MiB (139.8MB) – 1,286,821 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81e73cea32795f9512ff4ec3ed329481<br>SHA1: 5484efd534f07f82a4008cf40f364590552968f1<br>SHA256: 03363b76c7900c2067e56332184c9448d67c6dddf2b2f9422bb3ce83759e2bb0</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>141.1MiB (147.9MB) – 1,286,821 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e63bfd11003c77119c4fa59bf0b6160<br>SHA1: 6d817bb3b92a66b47437abdc79830dcfa45f50ea<br>SHA256: cae5675d0e90d157a998494d84d91a246263eb9c2fc2d7f86bf6787a67f04078</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>130.4MiB (136.7MB) – 1,286,821 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd7bda9a0efff06ee26d349325b9adea<br>SHA1: 9b9214f15f1ea40dcf7755ce90c2b756e1cb8e88<br>SHA256: 25a08289703548958b9134b6c2823a1cc48a2a5a218fa5f95b2aa75e137b6d7d</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>141.7MiB (148.6MB) – 1,286,821 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 417beed3a3a0e2ad62a7881eb721009f<br>SHA1: 597187d0cedacf123b08a4f3fa43b55c74937d07<br>SHA256: 2307356513ce4d085dcefca1352d82601768e590e38c466db9747faf3ae4fc6b</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>133.5MiB (140.0MB) – 1,286,821 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45bcd62b0dbfff9b2f99340d46e000a5<br>SHA1: b737fccd054c0414a5f4fee84ea9bbf9de0e598f<br>SHA256: f76c01d746a8d0661d8277116c6cbee35658cef2580253ae83563e9719767b60</pre></details></small> |


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
