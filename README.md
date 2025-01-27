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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-01-27<br>IPv6: 2025-01-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.991MiB (6.282MB) – 299,981 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62b91f743a655265e616a0e03c46c25e<br>SHA1: c2e2548e57837e0033bcd0c95e5b5bd70bd6f459<br>SHA256: 68a53171dc19e24185fdcd7f95f6a6773e2accfe11eec34b4c91020738a7683d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.76MiB (12.33MB) – 178,714 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beac63c0226017fd376cdde8c72a7ecb<br>SHA1: f52e95b10d63edd0bfbf537561e1ce24e3688270<br>SHA256: de7c343e831569de5690dcb80c42dba4d236ae25750d17bbe0de9e26137075c1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-01-27<br>IPv6: 2025-01-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.333MiB (8.738MB) – 417,306 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f43d55ecc46bff6355ece18354bea9ca<br>SHA1: 6431be2755463b68760c17490b2c7ac5d97dd723<br>SHA256: b9fe537e6332f41c84337617a8925c4bbe53d2b3baae9a47cf5bbdef8d49f96a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.957MiB (7.295MB) – 105,841 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63531cfad706dd2a07d8e9954af9d4be<br>SHA1: db9fe2df798161076225594f17e65d9daa69302b<br>SHA256: ea5e0f05655087c1569e712f9c069a15927750c6c233bad5b42acebcd28badb6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-01-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.45MiB (13.05MB) – 623,316 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2439ba64184afbd0d7665f9ccd646180<br>SHA1: a019a539b64c9bc9b01f8471894e05974c918d16<br>SHA256: 7d0d396af507a693b4544a50285e80f6b817cd9c7d48d7a3c74bcda1d15bfcf3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>80.13MiB (84.02MB) – 1,217,658 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5966a437eb995dbb514aef48852716ff<br>SHA1: 35f2498f9d9b4a4364ef5da04e12feb6126338d6<br>SHA256: 675a4d86a87cb0064c03958dc482bc29f1003330d7a663cf6f9218fcc67c2e92</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.285MB) – 348,457 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83bc658c1ea05ee0c1dd67b508e416c8<br>SHA1: 70aa579150d7be548067432da89e0057b10e615d<br>SHA256: 636b0495d96e6e73c2fd6a2d599b3713d050acf8c2bc75556af8ad5d0fb3f95d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.36MiB (16.10MB) – 233,400 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea165adc6016bf7241db413dadd9d616<br>SHA1: c2e689ee2f5aa199cdf34e7bb0a4facf213548c1<br>SHA256: 40a1cbecef33f526b989ce930aa6fc2a0952064828188fe18df5b777d10b8d72</pre></details></small> |
| | | Full Location | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>187.6MiB (196.7MB) – 3,275,051 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ca665aabf2aee0b7c39b4545a5f75e<br>SHA1: 027d0a8a8014da5f6fc12e62c926c6933687bbf0<br>SHA256: 249e041ad20b36d2aebf8acd5c4d86a5f88957c86f3a7137f906df3200c6f623</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>347.2MiB (364.1MB) – 3,369,294 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb9eca947a082a3f2644b8c6907a6194<br>SHA1: 6d3040b4badad6d8c3e74a1fc773d997d8a618af<br>SHA256: 4d20b8e6b46f24b32ed9d99c2e5316f3c7e940a92aafbfdc42bea1eb6751282e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-01-27<br>IPv6: 2025-01-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.096MiB (5.343MB) – 255,041 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 385e7d39a49da4f7b26b8ca022e788dd<br>SHA1: 7bfbc318f06616719765ecf95f9c600ee41826cd<br>SHA256: bc2cb4bb17afe8e3962b87a8deb428f68ff7083def1f45c295c77d61751a71c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.13MiB (19.01MB) – 275,512 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3010eb9cc5eb5d69c08e40e6ada6b77<br>SHA1: b14d2ac80fc5b7043024cae2173668671a286f87<br>SHA256: cbf1a41317aa32c82f0ad9508afdfa47f673246f62711d998001fdfe0a7f5b17</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-01-27<br>IPv6: 2025-01-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.4MiB (185.0MB) – 3,056,590 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a976173ff14b69a2f374b84348a7b747<br>SHA1: ffcd6b20ec9ef8f0b9dc4f4c901e9fbf0f87075d<br>SHA256: b58bb3a37215ab1b1889208c52164428b5c56380cff711b82b6e54e5febfc1e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>226.7MiB (237.7MB) – 2,193,791 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fbc49d9a6e454cea9f8835d6e2277f3<br>SHA1: 9bfe0073a0141bc90622c08c9161a7283d562072<br>SHA256: 451e6a13f9d9293ed3e076c9bca96a945e2b1e2fd52e8171481f1a31a9e2be46</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-01-24<br>IPv6: 2025-01-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.17MiB (10.67MB) – 509,600 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b53fb4aec79712e4eb30de4f9d967eb9<br>SHA1: 54d7a924bfc991fe2777a5cee444a898c7218747<br>SHA256: d151260568361fa02868f5a1ef7f9b2c0ab8ac5fb03e52203ffb0923b99241f1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.54MiB (33.08MB) – 479,379 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b5fb4446d71b63d71f3faa792a8c8c5<br>SHA1: 6e4fb49b609e500b71953005f49432d09d593c7b<br>SHA256: 370d678e89495a6234a28d24ff77c5347eab36dfbdece15f39ca2edcfea84a58</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-01-24<br>IPv6: 2025-01-24 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.5MiB (173.6MB) – 3,274,124 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 178df9bf6133187c82fd3a088b5746bf<br>SHA1: 1addf88be574fb4873c5594316a86e6a037f7afb<br>SHA256: b8b19b5566058ff7d5cdc2e8e0d045d13a92215bd08526afe4a6c73b5bf64fea</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>176.3MiB (184.8MB) – 3,274,124 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef7927e63c8edfc81fd0c9bdb7eeeedc<br>SHA1: 08a6aefde4625d4d7a28f07e4492c12df09ce2ad<br>SHA256: f56c8d70659ccbb178765c0f116f0d3eb2516b964a50231df8898b7b9f9859b7</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.5MiB (172.5MB) – 3,274,124 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1586cedd600ea965c63ed53619f6ccb<br>SHA1: f9dda7c8df08db2cda1b557c14fd4bade1fb21c5<br>SHA256: ff805ee75f8673b52f871f53d0362e017455a4171b173d1232d7c22d465e6d86</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>167.0MiB (175.1MB) – 3,274,124 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f5c04a9563f0b048a211b086128e2d8<br>SHA1: a07f15457b8bfb21ae9cd1e7b79c6370ee9c1f7d<br>SHA256: 141e41f5fdda3c633883794bc831c840a5bf0d11263291deaedd35473575623b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.9MiB (220.1MB) – 3,274,124 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4c1c811e73dea33fd5bc50d831dfd2f<br>SHA1: ee3a2005dc0611864e84fc9d8ecd5f6c822717e2<br>SHA256: 3b0493c91890d668ace20783814d5bb497f659309d998d871280b3878fe21824</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.6MiB (172.6MB) – 3,274,124 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd2cc496450d0324a8bfebb8b7edf0c1<br>SHA1: f7da75f058b29edcf69fc33505961d81dd9d2a66<br>SHA256: 5a8d6d240a9dc8148740e6bda23454ac17810eb910430da2c819c2c480c9daab</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.9MiB (213.8MB) – 3,274,124 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 316bd4a6c7f1a621814bc2aa3d03c9c8<br>SHA1: 6b9323e3c863357f316528b6ebf39581c4599a30<br>SHA256: c3f7987e9c5698e79ed2315804fb87133ca0072afaa9a52d85aa57f04bc5c713</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.7MiB (180.0MB) – 3,274,124 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee8f2fce8418baf16d39082c83479db5<br>SHA1: 2b2b47ebda02088e09f1e75dc9f459c52f599753<br>SHA256: e911342238118cbe9733d21aa3c3d531de333efb124110f9dcd1e341fd827d68</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>162.5MiB (170.4MB) – 1,731,101 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbe97fc4c0df7db2270f95affc24f85d<br>SHA1: 4d35dd033e8b8f6b03abb9e7e262c278ffce4738<br>SHA256: 8c093900b284b7fc94400d956661637a12512ef19226e21e97270e07d46eeecc</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>166.1MiB (174.1MB) – 1,731,101 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40772550d788cb6b8d0e98309d2794b9<br>SHA1: 1d2860d57b7b24ca2529a40d00c9f4255b12c5ec<br>SHA256: b5785cb6a637ba0ae3179bace54dff91d4f4cbec81ae14a5450d7487ffd30655</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>160.6MiB (168.5MB) – 1,731,101 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70198011beee214c3ba5d2267db7b3de<br>SHA1: 262117c2fe94a245bfcc94470277779fc638e698<br>SHA256: 9f049401e4265d0982d3c2456db2485fb8eeaa3c9e7c76d962797cb440fe55b1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>161.0MiB (168.8MB) – 1,731,101 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db918e257becb0ad558c50630912ec24<br>SHA1: 1b1b09f224310f721efa4e16c44ae32e683cffcc<br>SHA256: 4e60dea694226bb78fdecd6f423da0e5e3ddd1341b1ce2a6fc4fdb32999927dd</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>177.3MiB (185.9MB) – 1,731,101 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d54d091a03464fd59a9b5e64c462a838<br>SHA1: 469e468440d91d2a27d5e6a100ae2383b54bdaa9<br>SHA256: 2ef9302b2ad469b5dac640c108241c92b69670441d2b40f26897e7e6ddb5832f</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>160.6MiB (168.4MB) – 1,731,101 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06b4177d4e061e5b995f087ce00f59b5<br>SHA1: 0540b40110c9ce427972671adb03bc53fa469a28<br>SHA256: 5497dcb68cc14bd8a89ede6f5dd245ead248f5c2d8a892f8ecbb4b41053c19fd</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>178.5MiB (187.2MB) – 1,731,101 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 834e333306c406d2c1689205ac4f7075<br>SHA1: 4afa7ab29d841e4f8846fa6486dbdd0f797ec6f4<br>SHA256: 22691181700a3faceffba3672e6913eba64c1ce943afff3a9e1f3b1a92fa7cba</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>164.3MiB (172.3MB) – 1,731,101 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7527cff25703e56122ac55a463b0debc<br>SHA1: 4986e1209944e6f93aa4f3073e1c98361efc75ab<br>SHA256: cae969a76980d4891b3e95e318d5253be91c2ad166af329ca6902a9dbcc23e40</pre></details></small> |


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
