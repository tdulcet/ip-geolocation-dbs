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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-07-12<br>IPv6: 2026-07-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.390 MiB (5.652 MB) – 269,725 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10511e40d84fc39fd77abd507e2c00d0<br>SHA1: 85df22524e7766d73343f818ed6e9352e74b8346<br>SHA256: 688ff51708fd0807429b2bf881269df8413e4038c22a2a95a93f48a5fa633ce8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.75 MiB (17.56 MB) – 254,560 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8328afd42fd35a83d78ab262f306ccc<br>SHA1: 380b2f5c328a90c19255e5c42cc9817fd7a0c10a<br>SHA256: 3d05059331febc504805bb0e10908178b7fed7011bd847be834fa41fecc400ea</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-07-13<br>IPv6: 2026-07-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.007 MiB (9.445 MB) – 450,990 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ae72693f6ce4387601ea507cd749bf5<br>SHA1: dbce98d493a1dbe811c7401aae914ae638332433<br>SHA256: f260f37b409df402b3b94eeaed42bcc6dc18ab2b64f312d2d0081be3d8ac5e74</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.943 MiB (8.329 MB) – 120,825 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a93da5247f0c9b53131fd3b2c7f19aa6<br>SHA1: 3eb8ede68a6231cdc6aafb358b98275acf3b2b57<br>SHA256: ffd225cc404fd6ba136081c323e0e9f2a1c2623e28f8c492101d405c00056d03</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-07-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.25 MiB (12.84 MB) – 613,138 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf3068ed91881cb7326bc57b8ab98ae5<br>SHA1: be2165d8943664960435219278f7b536d28aa99c<br>SHA256: da6ecb6cdafc629404f70fdd80ca09f3f3ad3bc33b1e1ff9a448fe9eb37dbeea</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>41.60 MiB (43.62 MB) – 632,244 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2222ba66330d0ace8ab94fc7fc6e6c7<br>SHA1: 5aed7f87d31595f41cfc841c27f815b4f42c13a0<br>SHA256: ff42a9f2f9a850024235eef87ffa2ed0907361e043fa2298768de4431d36b0e6</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.078 MiB (7.422 MB) – 354,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ec835290735187164b1f2f622ad9c0<br>SHA1: 10464ef5eb489f4745096b1c71046b06409244b5<br>SHA256: 6bc4af63c1e15b4d99d5b9dd9cddeb67bbf2eafc2529ba5d9ec4525e0fe7964c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.51 MiB (23.60 MB) – 342,046 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569d0c6b66a745289f0e152318090f38<br>SHA1: baf1ef75355d41d9bc4380f97ed3b085db479655<br>SHA256: 8940a06c7f9a27f129048c5a7a0b1579b368020d88f2d2efe0fc813b6d2f97e4</pre></details></small> |
| | | Full Location | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.3 MiB (219.4 MB) – 3,666,805 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b729ab459cc2b765b3b4ea035f481b<br>SHA1: 1496af12b72ee784e304cd84eb7335c826bc3906<br>SHA256: 69fc5ebf5414a7a939fc25a35f3128451cf340211ae51ab9f82d53a331d8ca03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.3 MiB (473.3 MB) – 4,386,528 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f197b2ebcfed77f9adc3310fc7b6020<br>SHA1: 24b1454a40fdda39f37fa9367a6a6a5a88d3be33<br>SHA256: 0160ad6b5bca3517eb65f79d6db1f9e373eeb34cfccbf189a588bb330d17af06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.663 MiB (5.938 MB) – 283,439 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5e0b2b6a8aeacf3ff5598adb8880765<br>SHA1: 8804233331909b27cede1b5b43c2f97e3e0fa7fb<br>SHA256: b76b958024d8951ae29a80cf988f69d1e662dcc0bea8d923f50bdc702ec7cf2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.09 MiB (23.16 MB) – 335,708 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a285d07eeae37dd9fc478666744fc01a<br>SHA1: 088c9efb11f726ab15157c87e8ea1f653a7ad960<br>SHA256: 276a36ba7f5863bec8cfdfc9f38541e0dfacd40d41312852daaca8be67b6585a</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4 MiB (176.6 MB) – 2,914,372 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77a6d0d39cccc6773bd841068fea21aa<br>SHA1: 2b573d6c293a367a2052b0737018f62a9b4b74c1<br>SHA256: 63c79df13cea9f7d90cb141a952a0ec792fe5f5c39e6a4cb98f1caae5055b951</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>295.0 MiB (309.3 MB) – 2,857,634 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78f9a0f50b954077a7222ec29768405c<br>SHA1: e7cf8076d18ce13f2ca1ddb68037263adaac2c3f<br>SHA256: 8eb07f6e7f6d570b63e6735ef434d9dbfc7a394946b35bb3ecbb67d2c31d9863</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-07-10<br>IPv6: 2026-07-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.32 MiB (11.87 MB) – 566,994 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a83b1d014cc9a71972e72aa441aea43<br>SHA1: 0d76a7378894d7d8e1fea03d31db60e610a1b42d<br>SHA256: 678380821b96e37b84ef76988f2e29e1d2e49a9cbb937c46ce1717d70c303a12</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>36.88 MiB (38.67 MB) – 560,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e2019a5d8b65cded78b7651814567f8<br>SHA1: 9e3c9809c3b981e032f1e52d6cbdc2497aec429d<br>SHA256: c5b0b756cca456bd583a481577a84ceab2ddf7e736a5b016a7eae6a3b9eb2d94</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-07-10<br>IPv6: 2026-07-10 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>192.8 MiB (202.2 MB) – 3,754,046 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29d539c7f2df158a448258cbf6814e35<br>SHA1: d5018f8cd3b4b2c22a92085edda45c0b4c7e843b<br>SHA256: 2ccdc58a93ac56990bcf271cdb7ff86469cbe03599c8dbdcf028afe15156cd37</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>201.8 MiB (211.6 MB) – 3,754,046 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca1391e74d06e684536a7b985d23bcca<br>SHA1: 05f87ce85002f694f84eccf1ed6eed6892849819<br>SHA256: 4ab3bbe363ff3cf245f71063111d770e3b8f415925676e484499bd00716f2929</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>192.0 MiB (201.3 MB) – 3,754,046 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 209a06a754a97bb8c72f43e4477fb902<br>SHA1: e770bd33f5eaca554d199019b9d454e01794b94d<br>SHA256: 53be336bf42aff5a899297a632c17efa8f3e33ea9e6048607ff9bfb81a94f99f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>193.7 MiB (203.1 MB) – 3,754,046 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80a2ecdc3248567a5b79a15ce29da960<br>SHA1: 5b7814e282e8605f7d35fe2f43ed6c001fc20b6a<br>SHA256: c3abde79c37a65b8fd31a81c56b5b08f4110bbb45ab73cfcc12f0f65153ad88b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.2 MiB (256.0 MB) – 3,754,046 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc8dd9f2c4735c8b3f29c1e31cfb5827<br>SHA1: 5dcab74f112a3407352f13bb66bbf694d895af62<br>SHA256: 294526c2426b72f8d609d79de035fe62dd6a8116504f755c955a21897b7fac45</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.2 MiB (200.5 MB) – 3,754,046 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f05e8427958d5b313a5e238198f6553b<br>SHA1: 98280ec5b14f17bf3489f79b0e992230210569c5<br>SHA256: c89d27e86c4278c7b7c19c73e55ecc24cef3b28da250bed4b646df33fe976904</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.2 MiB (245.5 MB) – 3,754,046 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bef233e6a87ca3a08c5cf6c1af293e98<br>SHA1: 7f9bd768c8e21d6290576baf49477f6294af31a8<br>SHA256: e12909f17214ffe45297c34a44874ccf84c62a46b9deeb2f19c19a37ee8ef16d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>197.0 MiB (206.6 MB) – 3,754,046 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d44035b15757c6bbc233e5902914a4e2<br>SHA1: deac2793aa8ceaab4d01eaccc7677bb6b734b323<br>SHA256: 63922ea08d078c6e3b6f30a16deda660de70e4ac4f1fe6dd2e3ce25be15fd600</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 2,064,609 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56e3413265f11de564226ab126264e28<br>SHA1: ef3ed28df9cff6a7f5206d20136b4bd5cbf4bd0b<br>SHA256: b55d65323dee37c7ebde45e81b69eb50f49e002c36678106b2c530b2068aeddb</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>200.2 MiB (209.9 MB) – 2,064,609 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7698534dc26c38ec7ec07d9899a0eb19<br>SHA1: bdc0837b59195ac5a365b80104c3f0fed164252f<br>SHA256: f2f53ae036714b537e29cd7bb8bebe7cdd74d90981409258b547b2c21077a41d</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>194.3 MiB (203.7 MB) – 2,064,609 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ea2ac70992033b48dd250c1d7985f1e<br>SHA1: 49c9947281502cc0335345998dab82857193d323<br>SHA256: 5ad851ed5a18c5539f1ce3ca4114d7553ca62857f71c143a1a5846a0ed5a7f41</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>194.9 MiB (204.3 MB) – 2,064,609 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec6eb42c1d468062607bbb8226e1aec5<br>SHA1: 75b36722316202458f8483db6297c52e201b311b<br>SHA256: 04910f8e1aabd090bd9b96933eb3213ebda84efac866708a32733d89ee1ae781</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>216.8 MiB (227.4 MB) – 2,064,609 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3adeee31b4019ac43e8e506f4c76ee02<br>SHA1: 00167f2aa3673e76d0292a60c8ea5b1f45643027<br>SHA256: 6b330516f12d85e0339fe3b2267c5ed9d88854c099f98086920c6fc428e0e1ec</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>194.1 MiB (203.5 MB) – 2,064,609 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 136ab2ba28d68e8f9bd0acdee862d219<br>SHA1: 475978b956e0658092bb88a70f1da782b8c21fef<br>SHA256: e1f302673910ab6b003da448ab29281ba1a938011863c8f30ad94d34ea069241</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>215.3 MiB (225.8 MB) – 2,064,609 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc702158961bcebba0e7366ff15702c6<br>SHA1: 1ccb0e5dfd2a5175148010f6a1c8a3194cff49ec<br>SHA256: 4e7a494b4d07333394ddff91b618c8b6c7f092ade265626b5e602bd13990eb18</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>197.1 MiB (206.7 MB) – 2,064,609 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28f3ed259f354db3857e716e12fcbef3<br>SHA1: c81de0468e8e111d755bb3f4920120dda0f79c87<br>SHA256: 7bd6b0ffbd8b35142f61cc1e095a5d464c88bf716aecec023d64c6eb14b6d6d5</pre></details></small> |


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
