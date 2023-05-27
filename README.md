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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-05-27<br>IPv6: 2023-05-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.835MiB (6.119MB) – 248,530 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99409e7196e8c54bef5375c32981c3af<br>SHA1: c55b5e4f998857cf4c8fae81fcdc786a5e528c7b<br>SHA256: 2e1922df15c93f49a8c1497d8bee3635ac001123f2f02b7bd54a913b34baeda7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.525MiB (6.842MB) – 84,470 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1a434c758e5c837e41b3b662854ab41<br>SHA1: 65f8339305c9ebf5c4d57189e4a0ca8562158652<br>SHA256: c7b388636e777c33a802e1a7a9c030602df686005defe4a0774bf196646107d3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-05-27<br>IPv6: 2023-05-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.467MiB (9.926MB) – 402,083 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fab3c9f6b197aac17039fc61a2a9085c<br>SHA1: 2cf127f99f72d102d0e2b9ff2cac71b5e59f7e56<br>SHA256: 51fe7601fb1049d0d4b222c831930822fb6895a54f195ce521e1b19217254db4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.592MiB (7.961MB) – 98,380 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a2df789f578740c451c65a21c3e77da<br>SHA1: 8c08068b92a4a6bb9b54959905b866a37d60a048<br>SHA256: 9703f0f0bac7651bfaf3b68486d800be8e9d2a954ee397d36cf9c6decc96f9c8</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-05-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.79MiB (14.46MB) – 589,678 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 089f9afb49bd273cf264b120221fca16<br>SHA1: 2a94b1eb601507b97795e166e2ba668ead121f5f<br>SHA256: 9b9b9d1753763b4a496f38df3f0ec6f7165dc565a55c346c0ecd56de7f17131d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>22.78MiB (23.88MB) – 294,854 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed4d35e0a67195a5e36bd45670c5c18b<br>SHA1: 6cb68ba41545191cebd11df41181da766c7fd717<br>SHA256: 569b2b081e12d9d8bad7aaacdde5019cfc9603f38550ec83ba55319bdcf0131a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.198MiB (7.547MB) – 308,140 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00b451f6412173581a7ba389f444f7b8<br>SHA1: 3581ae37ad536ccfc344035fac8da366e6f2a1c3<br>SHA256: 2632d03fe402810c0a5cd21cb01657e4bce6686f9a35a911a634e00376fe4fc8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.40MiB (26.64MB) – 328,845 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bb8a68614ae30eed99e534875572642<br>SHA1: 0ee22a19afac3f9a7cbd864af67674fe9cfc6161<br>SHA256: 7d06dc68c40737d45ad6dc84897a8b7371ad05211dc7716db73e16c197236656</pre></details></small> |
| | | Full Location | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>194.0MiB (203.4MB) – 3,206,976 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ab320aa3a48e3e999f3451fbc5a2da8<br>SHA1: 0edbe11a0f197414c336d93dce71b581d19cd274<br>SHA256: e618d8745b11f6aff0dcb8f824c7f141c7fe734243d064f5f1fd7a093e46c571</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>365.9MiB (383.7MB) – 3,189,651 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c56df0a8c49cfc4fafc1dd0e0ea9177e<br>SHA1: 5e57dbd6ea1ad42ff4e411c9606c8f23cb91e70c<br>SHA256: 78e7ce4abf723db571f358a92321ca5b197405f36485132b7deb8c48d31a8d5b</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-05-27<br>IPv6: 2023-05-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.555MiB (5.825MB) – 236,860 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed3a236afb3c81be58fd9e618311f040<br>SHA1: c2f909455631207019aaab2b2e46e900ebf570dc<br>SHA256: e9f4b3ba35664fef476b681b4bf974f40a7c2605e7528a86ad8bd7ec533ad95b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.56MiB (28.90MB) – 491,350 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24b4cca038e3d4dcc0f42da6244a3a35<br>SHA1: 2621cb133d2002e631b0adbef75d4ea6e931756d<br>SHA256: cc4498b24a37bbe633f6502d077cf044fd12484833daf07542118c9c7c386bc1</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-05-27<br>IPv6: 2023-05-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,146,282 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88c13dfb1a052516749e7ea3a9487650<br>SHA1: 2e306a30fccb8fc193e5dd6bca9c2dc9b66b74eb<br>SHA256: eb792a298ee49d197c826b29bf481ad1c08529aa3138b1265dc37736edb20adb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.6MiB (400.1MB) – 4,518,262 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fdf49f6825c8d2c6839dbb6a75d33b8<br>SHA1: b3e158802b17935c7869bba17ff348eb8c749c91<br>SHA256: 5b247134a6e2438ebad87181e14b376f714b23fa9c8ca69d358366ad0778806a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-05-26<br>IPv6: 2023-05-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.709MiB (10.18MB) – 413,926 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a042571e286b1f4d2e613769eef46de<br>SHA1: 34b8581ed3df27523cc7ceffeeef7b1dc388866d<br>SHA256: f965b2c98e89aae89a9921efc2984d3dc3c9124ed76d191f1a0cd0f49a26c073</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.74MiB (22.80MB) – 281,439 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ff2588854a48f84233b0af60f0ea69b<br>SHA1: f742149ed748c31859ea2f9089b963794b010293<br>SHA256: ea710afa5677bfadc0565e0d6be0331bf74a87d73a95ce85b8ae269c806fcfd7</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-05-26<br>IPv6: 2023-05-26 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>192.4MiB (201.8MB) – 3,829,792 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 522b2859ed01d150625983c72c4bae2a<br>SHA1: b752da2daa4033c69fc263da0bb8befe9fe17793<br>SHA256: 04d02c698f7744fcc78e55dc9a6447dd4a1fa8200cd6bc7db68bd26396202efc</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>225.5MiB (236.5MB) – 3,829,792 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68f23a98674b2786b3790f5bd9290a91<br>SHA1: c2455a3ea942ad6777cffc6053b3f985c9ae4415<br>SHA256: bb3f99aabc80f12c95193ea304fa620a81cb157ebd19f20600f86a4e87e3ef5c</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>199.2MiB (208.9MB) – 3,829,792 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f21d48c856410e3118c222084db56a9a<br>SHA1: ad4c187c54f2522a181cf5c9ea8d711faadabc1a<br>SHA256: 3667577d610ee6ebfd6c81ff28ea209e125ab27d1ae09f471c37d5f7aeb148dd</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>206.4MiB (216.4MB) – 3,829,792 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb6fad1d633dff7585e9ea0c5be8ecef<br>SHA1: 3f07b5fca81018cc6cadc6a742bf85fd8f2343fb<br>SHA256: eb28d7bcd6264e0786b8264690edfc69c19512603c374569bb9cb12d894912a6</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>242.2MiB (254.0MB) – 3,829,792 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 438664503bc35e6d7dd531854c370f0f<br>SHA1: d9ef5d5bfe0f9392b68fde67fb0ea7e5f05efbc9<br>SHA256: 9f6fef17c0995890d5390ea9ea8e796fa2c505879edc18f3bd34c2ec323e0ffd</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>193.7MiB (203.2MB) – 3,829,792 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72b51b8117c3ecba856411b43a2278c5<br>SHA1: 4f48a1e5d70bdcc74db19737bdf1d1a5ffa67217<br>SHA256: 8f3f9f016e6e0897ae4f7f558ec693351ebf5b1e20f6061164f5eca98de72a45</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>242.7MiB (254.5MB) – 3,829,792 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3c8548ab321752a2bf6c4e7b15662f3<br>SHA1: 553875212b69374ca3e7a67db60f8fffe3b5e802<br>SHA256: a4790d5bf6372322a3182037685e1049b57e25a1a44d606f42ee05050371c4ba</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>206.2MiB (216.2MB) – 3,829,792 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c30899c25bc4fcbb37913f34e8b6358<br>SHA1: 7a21055b0bb160ed58abfa3a204b7e0ac8dc6a45<br>SHA256: 2e5f2d7e8e02a7d0b6c6e02c8f48ac984e8d151d6aa8c21b1ef3a0693f0f9da8</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.3MiB (134.5MB) – 1,278,604 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af72a8fd7e9eae9fb1d19d5520c921cb<br>SHA1: 5bf192cbe1cf677e55c621e2fa65878adac76023<br>SHA256: 0ecfe9716054d66c735c52b5bfe5b9c9477ac97cd3e3ecb580bb03d8c903ccda</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.4MiB (143.1MB) – 1,278,604 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83d6dcb5937bd9ebc6615b3b138aeb00<br>SHA1: 4e8016c7e62b8700b9f8bdb3fda2f9e93f53727e<br>SHA256: a6897ab1bf97c03b12566be1ad0ddc78fbb5204168fcb4d6d0940d8813db21fb</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.4MiB (136.8MB) – 1,278,604 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f21712056236b7f0e391e5c3dd1b1d04<br>SHA1: 4e096093929457dbf79577bfad6c01114d7b5578<br>SHA256: 0a3619f5dc050faa2c552b573c838586123a97334a36be8577ed724eeb2b79ae</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.3MiB (138.8MB) – 1,278,604 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2cfeeaebf17e6de103865047404b4b1<br>SHA1: 0170ea001a59dae6be77b238515ee78b6ad58093<br>SHA256: b355d96761a713cbde9f378b71c3ffc801203ca5396dbd910600fe6e7671a05b</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.9MiB (146.7MB) – 1,278,604 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9a311e6a4530f527c5fffb322572a4e<br>SHA1: 888a0892373fb8b122b9966b13e7af540d046411<br>SHA256: a41e1a79d664b06603b636c69a4643a8b54de44a291090306fa530887ad3eda1</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.5MiB (135.8MB) – 1,278,604 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a004efb8953c783a8a2daf6e5ec90652<br>SHA1: a8998649ef67180568410f8d880ce6ab7ffaa5d0<br>SHA256: 418e0c992722e9c0a86ffbe9c8f04613ebbeeaf99d08b2700ad5cf7b0ab0213a</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.6MiB (147.5MB) – 1,278,604 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4607a998dfbcd4c68b735596f0caedb<br>SHA1: 89d0ec976f336c1c168a3ff1d01adb0945bca710<br>SHA256: 109639c5ec6abea6595d1096519c356cf3156ab135eaf6426c453841a2192195</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.5MiB (138.9MB) – 1,278,604 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e970c2afab30f852d6f339d6f6a64499<br>SHA1: 043ee770b92e9f91ff3874e896d1f7106d2ea9c6<br>SHA256: a94f67a4b3f2ad521cfaa6a189a270f942081aa1ebd2658f79d2024a07e1fd3c</pre></details></small> |


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
