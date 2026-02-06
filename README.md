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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-02-06<br>IPv6: 2026-02-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.743MB) – 321,983 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45b5fb70de641f369dbe6c7ca582eaef<br>SHA1: 7eca180f4d5fdad2985ceefd6bb85922ac569133<br>SHA256: 386c9e1767e89731eda711a3e641d5708af6c825f2e2580ca86eaf2cbb2e6f3e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.15MiB (15.88MB) – 230,205 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 902338fdaea8eea9718b19baed206f6d<br>SHA1: d6bf02564782f14efc239fb85d641797d2d58540<br>SHA256: e03998afa796e042edd6735768b26ba7eaece4d6a0e0d6af96b39c45451a48f9</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-02-06<br>IPv6: 2026-02-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.769MiB (9.195MB) – 439,106 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d86bca5d6bb086f15e4f4b2fb665e75b<br>SHA1: 94de73ff8a4a1bae8fea7d9a0f5bfa537d31dcc6<br>SHA256: 4bc17995d89147d0515d008f900a92fc9199130b91038423fdd184abcfdccaeb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.587MiB (7.956MB) – 115,413 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9968cde8935abc53f5422ba6fdca5af4<br>SHA1: b7d62985991efd0b4bdaf7f8919df8f8bd87c810<br>SHA256: aee59d7f2d1f061697dad042c016298d048c08f360fe3532db690787e04ace37</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-02-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.16MiB (12.75MB) – 608,791 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f6c2e71f1386efac16eab93cdcc4a5b<br>SHA1: 017674684d197f5b15b2f8c1e81d023986392fcb<br>SHA256: a10b686f352f662eaa3e73d2429dfbfcb02893efa36761a45b113becbc06d352</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>52.32MiB (54.86MB) – 795,039 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41790a9aafcb8c4f47ce6af4051aebe1<br>SHA1: cae96e360f5e5227fb58a413b17a9078e4fe40b5<br>SHA256: 7e3dd0faa6639714f28010ac84930a58acd81fd3dd1154a360deb35fb7bd4b16</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.768MiB (7.097MB) – 339,077 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0181205d24255559b4c2a13fdb0c95<br>SHA1: 77c5ed2ef6799485a1ff6d1bd9aa3aef442555aa<br>SHA256: f1a904010b8cf3e5db4f0ddc1b0fed4c77f852aa52effac37a04697ddb879a37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.90MiB (16.67MB) – 241,625 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f8f77acea5ee52ad5d81c9f3883d7a<br>SHA1: d3a894c2e7503a5fe5168eef49e53379425930d2<br>SHA256: 80ee4bf63ff4562160eda9ba68902de89a9e28a828c048003fd188647039bf1f</pre></details></small> |
| | | Full Location | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,746,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48770c63478550e9d616b0e8f11eb35f<br>SHA1: d754e9f10a536891a6f76b212ce1527fccbb205a<br>SHA256: 3abef96589717a094c9384cc0d2e88d16dcc6c1771a5eb42954efe056fe2caf0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>452.5MiB (474.4MB) – 4,397,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d15359a3c2245bffe65895c5939244<br>SHA1: a5622976378fbaa83dd68ce8bf186161f41252b1<br>SHA256: 3c33680bdbdc577647e1e500060fa0db02dc2af50f79e20bb78a7ae7ca1b33bb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.379MiB (5.641MB) – 269,229 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8df1f43c6aabf7404b9835918b8fde47<br>SHA1: 601b465ff0736111423be419aac3f6d5972b42f4<br>SHA256: 80bbfe7421ce68520f39ab366b0fc481427602add22c34ee6881ec43a96b1488</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.19MiB (23.27MB) – 337,206 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48696b7a642ffca450b564a365389e84<br>SHA1: 2da10da7971a84e435865041021aedd433c35db5<br>SHA256: 360124b18db3ea1ff8adc37d7d8c7432d236ac9d3e5c9f77123d8069ac8cd7ff</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.6MiB (179.9MB) – 2,969,494 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5343189d8e7d3b6229056c21a834739<br>SHA1: 8489f2c88b7fa2b7726299d47a687a5af88b7259<br>SHA256: 5f47bc0d8ce6968a1388a93536b1e895b0ddb335cd76007a7b142ca0fa206970</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.6MiB (307.9MB) – 2,846,346 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c67fa86a08014c894bae1e43237dbf3a<br>SHA1: 1bfac6af73658923732d9bf178d37d1b4cf1e23d<br>SHA256: f5b735e687c937676bc7cd2a6d383e598ea54e61f46b9863d97f53062b1634de</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-02-03<br>IPv6: 2026-02-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.12MiB (12.70MB) – 606,536 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4800cf33a272c6af83b255806eeb3f58<br>SHA1: c8f8449d3353b1716a698d1d2c5f1bbd23b4b239<br>SHA256: c5c7ab5d2d561cd427fdcc6081aca57e45c950310ba58246e2d11804c1d910f1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.87MiB (44.95MB) – 651,434 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9bbac2c220f1f6ba795a443aace7f08<br>SHA1: 43174e8ac2bbd27cc2edf223ab9be87b79fd44e1<br>SHA256: 94734425b5281edabd8764de0ead3872a1d37b038dfba2e821bff29a2eacf702</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-02-03<br>IPv6: 2026-02-03 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.0MiB (186.6MB) – 3,516,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 045965bea3871c506023d34c688dd982<br>SHA1: d696e7e9d3a23b584cdb691b0dab1e77638c1ee7<br>SHA256: d295fc8e37fd99dd09e7b01a8ebd61a0e95628f4ab7a88e22c4b106aea0990fc</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>188.9MiB (198.1MB) – 3,516,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8f2affaf9ecad4505f32171916eb93b<br>SHA1: 1979223b67d0d1b08e938fa00b17fff44d8f956e<br>SHA256: 1919cb1ee24901bc9593bb311b261d6c38d0e5b83247e798352988a55808a539</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.0MiB (185.6MB) – 3,516,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 013a957b56b301801a874496b9754b50<br>SHA1: 687c446b47165f05adde43eda11a2fad354c0d92<br>SHA256: a340bd6d76611508a99adf366b0f038d7923126c84642c293ff7348965ee6b15</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>179.9MiB (188.6MB) – 3,516,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38e175a836da3facde48b3f051cb565e<br>SHA1: 9524379ea9ddcf36ea70d016a1ff590dcb56cd65<br>SHA256: 0d1c4e0d079b2c395d40dd6857513abe9432f61346718cb61c65f94c3fe1db20</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.9MiB (235.8MB) – 3,516,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4967311ce91dd99d5d4b40ec96b6f1f4<br>SHA1: fa22d5a69d0c68d5e70c19cc3b6195339efc3409<br>SHA256: 195cb4199e49440e913a72bd8d864f28a910724aa219dd318f256db08e63bfc2</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.6MiB (185.2MB) – 3,516,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18890d173961a90cc8d94afc83d186e9<br>SHA1: 5437e4dd28c2bb316f2836a820936666643b40d9<br>SHA256: beb1916b9dd089f74a1989be2d26d965427d3a200c5ee4a4ffb71a0f20ff24e6</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>218.8MiB (229.4MB) – 3,516,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9436e79c6191ce1fae6d859aac95ce12<br>SHA1: 5cde1d798bc389928345cf3287a162987cfffe58<br>SHA256: 24fc137deeaaf83145ab8dce13e73d4074c94b5f66b46a4d6ad5f782dae9d172</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.9MiB (192.8MB) – 3,516,753 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30776a5a6b5b5412b7f77fe13169e367<br>SHA1: 9b16f15598d069e4c92c73e8fa98e500db842c79<br>SHA256: ca129b61f005230a41f338bf3df75dc0045153cb42df8efd1e6c638ccc88b0dc</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>185.4MiB (194.4MB) – 1,956,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37ce7c986b653904f0225926edaed40d<br>SHA1: d630d632d75cbf1b85f008cbf83d120469b48d3d<br>SHA256: 4998f4018e1fb18535f4042d666199c72ae3704a14df92239aab5e2c651ac358</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>189.6MiB (198.8MB) – 1,956,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4bccf02ce38d4f54f58131991bcb3d66<br>SHA1: 57b6801bde2f04f25bbe6f47f2569fb866617247<br>SHA256: d883679bd3ba2094173df78ada29020070c1c0b21e33e8a5e0ccd6d6958ba1d3</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>183.3MiB (192.2MB) – 1,956,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614379a012ba2de9d1ba4b61c117e088<br>SHA1: d6d42c4e924cd4c54d7cfd55aace003b525a773f<br>SHA256: 983b6668f0d71da6c1d628a3e26b88c2cc70fdfc44a91b98ac05d4718d80da28</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>183.9MiB (192.9MB) – 1,956,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd7212679d60a6b2f56ace6fab8192f3<br>SHA1: 9453b287af9df87bc8b7b10026d0a5176baa0e80<br>SHA256: 2d17475bf0923b9a9154f9b023737c47ec3f1db6f8fbe39f9753b8565a1365e8</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>203.5MiB (213.4MB) – 1,956,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81042c5ed59bcbd9c432b88a5996f456<br>SHA1: f94580cb13a7919da4a604b9c799c12964903447<br>SHA256: fe299c0bcd4a7a77e7e548ab1cc0bf4b14c4dad5992484d88243e73e4a6239ed</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>182.8MiB (191.7MB) – 1,956,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7dbdb52d8334cd141cebe34159f6a83<br>SHA1: 83c447ce6233473cc308116c7f180d135ed5506e<br>SHA256: 92fd0913794a47d958ca7bb3e241011f1a66f5b46a8ae17426d61f228b659d41</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>203.5MiB (213.4MB) – 1,956,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a308110edc61cd5cecb8e679db6c9b6c<br>SHA1: 32ef2290e5e67c38ce19d2e4b17662b1d00639a1<br>SHA256: aed967a5e17bc465965ff7df94807ac5d4f94f791424c2207953bbae06ffa600</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>186.4MiB (195.4MB) – 1,956,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b83869d882c644ffb49e320ca0e69a4<br>SHA1: 73d333bf375eefb822f59d62235fe3aa9ab1603a<br>SHA256: ea26bfbc96439ab9d0da7f3ff474c19bdf5b95209865b53cfd8272adfa0290a1</pre></details></small> |


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
