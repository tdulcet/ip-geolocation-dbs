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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-05-10<br>IPv6: 2023-05-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.131MiB (6.429MB) – 261,314 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d18b2ff529724b4396572ee10606408<br>SHA1: 1b5eb055fc88a3143634f4479e800da2ab10b1bc<br>SHA256: 257b17d14448ea20ce48441af1e10e7dfe3d6f6ff442acca22798ba0b0af9c33</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.482MiB (6.797MB) – 83,915 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b023de2587cb13ea48ca42b3c1843140<br>SHA1: e94412cf5e22afbd33591365ce48c1d0034c971c<br>SHA256: b9283f0927177075782d97f6d231050065421caf8eb964c67f9ef578808e2dc3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-05-10<br>IPv6: 2023-05-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.446MiB (9.905MB) – 401,244 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6312c64ff5236fa4bf5f301f410fe45b<br>SHA1: 22281aae4be3b786505253a52ee0f3b0d13ce55e<br>SHA256: c12fa55b9da09d5f3ec2f42996961a472f38c3bb2d22fb4e1cd1cbcec94482f3</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.525MiB (7.890MB) – 97,508 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edbe4bab810850b33c6a79dbcbe66112<br>SHA1: dfe6de1b06a89557103979a65ddd8b45b09c33a5<br>SHA256: 253b98636ed1a2c556b77557e111e769d1cd9ef184b4b4721204332d6668d91c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-05-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.66MiB (14.33MB) – 582,957 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20fe9ddccd89d1ada5d31e89ee00f314<br>SHA1: cdcbee8348b9bd3cf2c149efd2f9e0521a38b753<br>SHA256: 119d967c9e28ce98bf09729860ac63848ac445ab9f7984a317da3ce1d4c8637a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>27.99MiB (29.35MB) – 362,305 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2839f1832d572dd3f564bc8632c3d585<br>SHA1: b8f9cf010cdfc1b860d15ba72068be5a667133b7<br>SHA256: 2c10100e7332f50613a1ccaedd23b8501a782ac6af17f187451a04ebc3e4218b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.198MiB (7.547MB) – 308,140 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00b451f6412173581a7ba389f444f7b8<br>SHA1: 3581ae37ad536ccfc344035fac8da366e6f2a1c3<br>SHA256: 2632d03fe402810c0a5cd21cb01657e4bce6686f9a35a911a634e00376fe4fc8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.40MiB (26.64MB) – 328,845 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bb8a68614ae30eed99e534875572642<br>SHA1: 0ee22a19afac3f9a7cbd864af67674fe9cfc6161<br>SHA256: 7d06dc68c40737d45ad6dc84897a8b7371ad05211dc7716db73e16c197236656</pre></details></small> |
| | | Full Location | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>194.0MiB (203.4MB) – 3,206,976 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ab320aa3a48e3e999f3451fbc5a2da8<br>SHA1: 0edbe11a0f197414c336d93dce71b581d19cd274<br>SHA256: e618d8745b11f6aff0dcb8f824c7f141c7fe734243d064f5f1fd7a093e46c571</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>365.9MiB (383.7MB) – 3,189,651 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c56df0a8c49cfc4fafc1dd0e0ea9177e<br>SHA1: 5e57dbd6ea1ad42ff4e411c9606c8f23cb91e70c<br>SHA256: 78e7ce4abf723db571f358a92321ca5b197405f36485132b7deb8c48d31a8d5b</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-05-10<br>IPv6: 2023-05-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.555MiB (5.825MB) – 236,860 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed3a236afb3c81be58fd9e618311f040<br>SHA1: c2f909455631207019aaab2b2e46e900ebf570dc<br>SHA256: e9f4b3ba35664fef476b681b4bf974f40a7c2605e7528a86ad8bd7ec533ad95b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.56MiB (28.90MB) – 491,350 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24b4cca038e3d4dcc0f42da6244a3a35<br>SHA1: 2621cb133d2002e631b0adbef75d4ea6e931756d<br>SHA256: cc4498b24a37bbe633f6502d077cf044fd12484833daf07542118c9c7c386bc1</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-05-10<br>IPv6: 2023-05-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,146,282 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88c13dfb1a052516749e7ea3a9487650<br>SHA1: 2e306a30fccb8fc193e5dd6bca9c2dc9b66b74eb<br>SHA256: eb792a298ee49d197c826b29bf481ad1c08529aa3138b1265dc37736edb20adb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.6MiB (400.1MB) – 4,518,262 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fdf49f6825c8d2c6839dbb6a75d33b8<br>SHA1: b3e158802b17935c7869bba17ff348eb8c749c91<br>SHA256: 5b247134a6e2438ebad87181e14b376f714b23fa9c8ca69d358366ad0778806a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-05-08<br>IPv6: 2023-05-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.676MiB (10.15MB) – 412,534 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8305900e5bc8791949b9d881f75cdbd8<br>SHA1: e2bf5c5fb970af52f118136b37c6d9397aa16907<br>SHA256: 2c865ef29acc2f5cfd7ae37a4be99756764e4b6ff321faa35e38bcf3589497a4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.86MiB (21.87MB) – 269,990 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55d4b0ca5f268e9f8748a9f007bb870a<br>SHA1: 41fc7e996aeb3ef53f839d0c88ac1b4b5d24806f<br>SHA256: 416cff444d16811ec478aac1b7092caf510a379125167ab8a868ceb9891e4b3d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-05-08<br>IPv6: 2023-05-08 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,840,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68afe5b1263666d73302f2926c3e60d7<br>SHA1: 9da94e965fa3c80c44c395c752b13b1c365d10aa<br>SHA256: 2346bcafbdbfc74f044e9ef99a738ee9975396c2dbe6a58cfbf905a3785840a7</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>226.3MiB (237.3MB) – 3,840,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16372edd03a1b1dda65546074b306cd8<br>SHA1: 9bd1b629d3df09a5fbef2edcbbbfa99541858325<br>SHA256: c34f23be15704570c069bfffec9b63a21201efb770fcbf91c4514b27301adce1</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>199.8MiB (209.5MB) – 3,840,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fe18a207fdc8c426c18e3d3935a9fe0<br>SHA1: a17ae2510fb7fa6c7627f02d1ecd7625908a7ce9<br>SHA256: 7a9c8a68aaf7df1c1dfb5cfcb3db5abba343ecd3ae4fb535d2a3a46c3fec4c16</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>207.1MiB (217.1MB) – 3,840,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dca6f471e55ec18a2310afcd7fcf0960<br>SHA1: d38c1b6c930c452f40178171a5a6b0b63a4e82e2<br>SHA256: 970403e9e5d661b378100b823c3ca0f22761c48450e6a892af6270d28c62c119</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>243.1MiB (254.9MB) – 3,840,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8fe3a610815b7f45d4571463f8a1b55<br>SHA1: d8d8708855335c4f73cf827dba6ecd037e4ef9c7<br>SHA256: 7d2d21eb958a850f2a3d5002aae1ec1cfe35916ad90364b8471d2d7736156ff6</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>194.4MiB (203.9MB) – 3,840,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1f67125007eade97eb99027de98cc5b<br>SHA1: 18bdf56cd74328a41372295c731515171adfe3ca<br>SHA256: c505c70f013eb89ecf86fd4760c692c42dbff9dc865f0ad566056ab07c25024c</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>243.8MiB (255.6MB) – 3,840,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a96aea22365cfd3f7f6aadf108aab2d5<br>SHA1: 18cd65638235496be4055bf32fe468b578d84252<br>SHA256: 8d64729c507421178be775b4324ad3876f11965e32c29c7d943f9841319915f6</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>206.8MiB (216.9MB) – 3,840,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21d9f1a6bdebefd0420542a12206055d<br>SHA1: 234ebf21cec7b5464195e4b532a77c6b361fb374<br>SHA256: 5a723a5d3cf50173a2a1a705cd9b393f493c59f1de2b956f550bad5db597da16</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.1MiB (134.3MB) – 1,276,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5b4cb64e7a0cb0f1ad99b0fe8075fb2<br>SHA1: 7bd719c78a4c03a832f2c9dcbefa3362e8cc291c<br>SHA256: 0bdd2a9dc6d9e11e203dfd3ebd1d2a80a9252a095e76f6a2e73082908b924767</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.2MiB (142.8MB) – 1,276,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63dff2aa1fead1e0a653bdd2ea9a40a4<br>SHA1: 820e193869341f6f8c5b29d03bf2c5c374b10c07<br>SHA256: f22aa153080dd0ad91925fa4a938aca4f14c9ec875ab8ea1f966c2b94db905a5</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.3MiB (136.6MB) – 1,276,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6a08a7df24b6dd570b99d84f4a4941d<br>SHA1: d41dad68d52b5a65a91f63a6b16793779876a9ac<br>SHA256: a1088515ceaff35e14dc37316d170456773417ba2ef201a51b29794b99c48805</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.1MiB (138.6MB) – 1,276,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c62fdd9e64d844b044c5fe8da049414f<br>SHA1: 778b9a766b52135fc3ae03914056a247e826d1c0<br>SHA256: 07b2445aab63706e0ad6492a5eea09b0d0e4f4aba5c13f9aceac2e8c2edc95a8</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.9MiB (146.7MB) – 1,276,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d887b5f1c6e4d52c42f5b828a4f368c4<br>SHA1: 4cee868217590dcdf3aabfe96f3048d00796fe01<br>SHA256: 090ef33c87d4966e7921cbf5078538441e8efb7ca1fed57d6f54d15e53104fb7</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.3MiB (135.6MB) – 1,276,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9347a8b7e81b9ee8c882cd8ee7dfffe5<br>SHA1: eafafcd121d6c46ec6822547fbaa2087942bcd35<br>SHA256: b55d3f4d009cb73d99041619c59c21db45da01124033a49ab6d3557e567a9003</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.5MiB (147.3MB) – 1,276,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff83a31833cf550c05fdf874f02ab52c<br>SHA1: 1f0949b499dde69ed981bd81ef255d10ebb95eb4<br>SHA256: 5ba2778b6cf901d1672e1c1f4fe3570cda4715ee134e64cf9840f4860559f283</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.4MiB (138.8MB) – 1,276,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8cd496e7b4540014efa15dcfe58a0a4<br>SHA1: 996b76c402e5edbee7345efdf41041fb29fcb529<br>SHA256: f9d87fb32134691f22aff5a185af40ca5108ca5e0f1abcfe900b04ef077c0e8a</pre></details></small> |


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
