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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-05-07<br>IPv6: 2023-05-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.135MiB (6.433MB) – 261,476 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22802b5361ca763772deeddd0164a690<br>SHA1: 4bf47d1b1a9c43bebfa11e45e20bab3cf4abae03<br>SHA256: 1b66aa54fc31950e277bd682e877d373c25a6802f096834eb578ab4595bf81fd</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.478MiB (6.793MB) – 83,866 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95e89eb26f286d85dd157a3b3cb54776<br>SHA1: 1c9a1f7b0f8b087b73625c5d75131632cd5e176b<br>SHA256: 839c1f0f964ab9b11a86a9dff084868499992191f0d5721595500c8cb483567f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-05-07<br>IPv6: 2023-05-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.437MiB (9.895MB) – 400,844 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c75e24ff28097ffc8ce0f759bc2dca9b<br>SHA1: cb3a5aa7f1ecf610d25756454e685bdd6dbcd8e7<br>SHA256: ef363150b916ccdb09ba0680024695ade59377556ec3fb3f48a33247dc0583ec</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.510MiB (7.875MB) – 97,321 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37e0525e3c85a07532c239164e5e6327<br>SHA1: 55442120dae8ed8bb6df458ccfea3685d221734c<br>SHA256: 151d4f3ff8acaf189496698a810e59271b893e3f343bb92847f6d2c209a0d407</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-05-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.74MiB (14.40MB) – 586,115 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9985ff2a26bd27341c1d391e11782f6f<br>SHA1: fb405b304af8a2528268dd8b6208215656333236<br>SHA256: b5ddeedc6fc351d8c12701b0b3046fbb63b30c5b646b213af50f5540c36aac3c</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>28.25MiB (29.62MB) – 365,711 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9ada78fb6b87f8aa3e9d74ac378642a<br>SHA1: 0b1be8740ef1b38ffbc482874409e0684f493f4d<br>SHA256: 1abfaf172c9c5e8566da3c2e51f6eb02b08ba47e64ee91965b27fa4c1148ea59</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.198MiB (7.547MB) – 308,140 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00b451f6412173581a7ba389f444f7b8<br>SHA1: 3581ae37ad536ccfc344035fac8da366e6f2a1c3<br>SHA256: 2632d03fe402810c0a5cd21cb01657e4bce6686f9a35a911a634e00376fe4fc8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.40MiB (26.64MB) – 328,845 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bb8a68614ae30eed99e534875572642<br>SHA1: 0ee22a19afac3f9a7cbd864af67674fe9cfc6161<br>SHA256: 7d06dc68c40737d45ad6dc84897a8b7371ad05211dc7716db73e16c197236656</pre></details></small> |
| | | Full Location | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>194.0MiB (203.4MB) – 3,206,976 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ab320aa3a48e3e999f3451fbc5a2da8<br>SHA1: 0edbe11a0f197414c336d93dce71b581d19cd274<br>SHA256: e618d8745b11f6aff0dcb8f824c7f141c7fe734243d064f5f1fd7a093e46c571</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>365.9MiB (383.7MB) – 3,189,651 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c56df0a8c49cfc4fafc1dd0e0ea9177e<br>SHA1: 5e57dbd6ea1ad42ff4e411c9606c8f23cb91e70c<br>SHA256: 78e7ce4abf723db571f358a92321ca5b197405f36485132b7deb8c48d31a8d5b</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-05-07<br>IPv6: 2023-05-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.555MiB (5.825MB) – 236,860 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed3a236afb3c81be58fd9e618311f040<br>SHA1: c2f909455631207019aaab2b2e46e900ebf570dc<br>SHA256: e9f4b3ba35664fef476b681b4bf974f40a7c2605e7528a86ad8bd7ec533ad95b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.56MiB (28.90MB) – 491,350 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24b4cca038e3d4dcc0f42da6244a3a35<br>SHA1: 2621cb133d2002e631b0adbef75d4ea6e931756d<br>SHA256: cc4498b24a37bbe633f6502d077cf044fd12484833daf07542118c9c7c386bc1</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-05-07<br>IPv6: 2023-05-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,146,282 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88c13dfb1a052516749e7ea3a9487650<br>SHA1: 2e306a30fccb8fc193e5dd6bca9c2dc9b66b74eb<br>SHA256: eb792a298ee49d197c826b29bf481ad1c08529aa3138b1265dc37736edb20adb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.6MiB (400.1MB) – 4,518,262 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fdf49f6825c8d2c6839dbb6a75d33b8<br>SHA1: b3e158802b17935c7869bba17ff348eb8c749c91<br>SHA256: 5b247134a6e2438ebad87181e14b376f714b23fa9c8ca69d358366ad0778806a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-05-04<br>IPv6: 2023-05-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.671MiB (10.14MB) – 412,300 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37c33c7307527a426bd36fb319c26888<br>SHA1: c8f14454de6705b407996bee6d15914845fe9c07<br>SHA256: f5a022112d40332b65d8cc6a50af2275a78fd9b84dd157883cfa73ca37c75c50</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.90MiB (21.91MB) – 270,511 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f714e79199431c054bb1a8b3f3e5668<br>SHA1: d6284faf1c2fc68cb4d06f20d036707773a97733<br>SHA256: 92961c3b691eeed78c5e78860c6462514d6ed150b485ea5342a7c6fe9186222d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-05-04<br>IPv6: 2023-05-04 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>187.8MiB (196.9MB) – 3,736,623 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9462addc19eeab70c1944b9a8c82c8a<br>SHA1: a13bbdf491544675f6d68de276cb80fe519be749<br>SHA256: 68bef2234d76de4b63baa2df9d9eb92123a7800a822408bc8d28bb32d7ad3e58</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>219.9MiB (230.6MB) – 3,736,623 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e941091842461b0a39f63e46e533651a<br>SHA1: 56ad8fb0800229b79fcc3bb394271ae18f422ce7<br>SHA256: 4b6a9ba63e1d5678b6ff897e9a2ac0ec18e38ed448c55954d7233b26c2826b7f</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>194.3MiB (203.8MB) – 3,736,623 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d359163d87de08d3d6d9b250a4eb641d<br>SHA1: 03df0d4e080939fada02c2c04fb9e04f93ed368d<br>SHA256: a673c98fd3e2993e856ae79c03966a3c0e0f8e3e1f00f358c48b2a4d7e4f3427</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>201.4MiB (211.1MB) – 3,736,623 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 965b435d18c349b8bb09a4daecae13d7<br>SHA1: df9858a0b9d7c695d6c7381085163255b009c86f<br>SHA256: 1f099d31a34a50efcdc5d8c2f9a8753dee4d04d5f782b3639dda88079494ceed</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>236.3MiB (247.8MB) – 3,736,623 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 310561a8f4b66988c7db268b652f2919<br>SHA1: 5b091acc1f2a7f30a393ad4fdd248de5a8de7469<br>SHA256: 7bb60c266358fb72fd5e4c59279987d4b34456a1639383758e169dc1695ca4e4</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>189.1MiB (198.2MB) – 3,736,623 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bed3ac6613c42a8bb7922cf4bda43781<br>SHA1: 8e84e4df2c4d820d3cea3876fd4fd9605d29afdc<br>SHA256: 61899c72a5f5e4a4e36d51d13b8ebb1951fba2c3bbade92e0666d68da913645e</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>237.1MiB (248.6MB) – 3,736,623 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f3a068365beede1f9668633f9c49e20<br>SHA1: 5dc4393785be10edaacc95582049bd9b71e20d6a<br>SHA256: beb47721b63885d9d6ba7f7196d4f30d97b8bb885e7d035de03343be037d1640</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>201.2MiB (211.0MB) – 3,736,623 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3a5bf9aa6241daf149aa989e9fe6437<br>SHA1: ffe0d329ad3d89674d8ea8771dab8b433e24f145<br>SHA256: 3214fb99cd0bd6b66af345aca712205f14a89a1765342aca1346455fd7737fb0</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.2MiB (128.2MB) – 1,221,335 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa3c9bd4225d1ea54f348e54189e1299<br>SHA1: 7429e8f7dd7672405f61a8cb702eafac16ec841d<br>SHA256: c65edf3c35528934b34f25a7f8cf28f87ec2867084f39c38fd77a6ce31cab7ad</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>130.1MiB (136.4MB) – 1,221,335 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98cc3e7934af34f6c685498f1b788789<br>SHA1: 845088ec2667152b6f63141563f9e8ba6e4e6702<br>SHA256: 284b68b903ea7fc47ad6fb8fda97529bd8219fb64db0631b65d8e145f64a7138</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>124.4MiB (130.5MB) – 1,221,335 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 161b51ebc6cfab91b73590ed9a227a2a<br>SHA1: 1f5cb581a4d8f1fe51a02cc3f9c9e89d013afc9e<br>SHA256: 861bb7a9ad5d2959bd80d24e799ced8b445e9f31cc0672d3b41d4ba78bba7a1c</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.2MiB (132.3MB) – 1,221,335 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fb3da1ffb6513a6625c33376f473120<br>SHA1: 9c8aeb071cc38c18ba9b827dcac087a4390e9a8a<br>SHA256: eeef71d349ef4feecd65d8248920ea61aaed70427370d93fc68a344c2c5cc01d</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>133.7MiB (140.1MB) – 1,221,335 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65fbd87431ef294c00e41d16208b7f91<br>SHA1: aee640bd3623e7d15340f6fafc8f8ba9bce1f8a8<br>SHA256: fca91711d16cdcb914ee6d4a94d9170f1ca14074594ebf416b3be77f64ceb817</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>123.6MiB (129.6MB) – 1,221,335 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 838c79db4f75ba35edd369632a0c9759<br>SHA1: 6289707ef09dab6cb499925d40a990d6008ce3a4<br>SHA256: 77e53a1a6b9b7fbd3f5daf0cf260f39d626f3b50deae6d9430026e004f8305de</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.2MiB (140.7MB) – 1,221,335 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51a563c673d517337152c401b57bd75a<br>SHA1: aa9023afd18eebf39857834a306c0fd9e75aa03a<br>SHA256: 5126265870a095cfbba63240b639af3c50c838b57af02b00792f4b65fbb05a72</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.4MiB (132.6MB) – 1,221,335 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 969eff4851a133b2c1524646f5ea8baa<br>SHA1: da1d8f07098455fbe7251134a895c23c460b937b<br>SHA256: ed5c38731fb0ee7d0ef6362e5477a90ceb81fec2752a0f6728ebbdd21fa1f8bf</pre></details></small> |


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
