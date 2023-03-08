[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases

IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Prepossessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [
ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Scroll right to see all the files »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
|---|---|---|---|---|---|
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-03-08<br>IPv6: 2023-03-08 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.143MiB (6.442MB) – 261,885 rows – 248 unique countries<br><small><pre>MD5: 112a2c17bf1dc42697f6860073dd1af1<br>SHA1: 9e8f369975299457d0be11e47f9d09c34a86bfcd<br>SHA256: dda9aeb0415b6d990a0fb78ae0e2b03a6521906bacd31b94129e778659b0163f</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.365MiB (6.674MB) – 82,395 rows – 250 unique countries<br><small><pre>MD5: 093fe2b0607a14f6b4396dcc70b53a93<br>SHA1: cf7cf01d4963afcce03fb0b12b7c894ff0b1f426<br>SHA256: 01a79e869d9fb57914b43fad8a99ac67619670d4ab5189a1805baf021a334fc8</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-03-08<br>IPv6: 2023-03-08 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.401MiB (9.858MB) – 399,655 rows – 240 unique countries<br><small><pre>MD5: 0d04e13a12fdc963b785d730049477bd<br>SHA1: 2b6249b48006e8a99adebfaeda8ec0e34857e9a7<br>SHA256: cb908e74cbc60888da178da6790b1af59e3d730fdfdb18848061989153d526a4</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.267MiB (7.620MB) – 94,192 rows – 221 unique countries<br><small><pre>MD5: 829e8d953f3bf9c260845111fbae387a<br>SHA1: 5f841b80b06126a2a8b2103f6812f7beffba3d8a<br>SHA256: 98538021c770e3272d66f843a602fd52d83a1e7efad7fcfad28a2844d4fd046c</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>8.288MiB (8.690MB) – 354,199 rows – 243 unique countries<br><small><pre>MD5: a1d21d8f62a7c3f50510147c0eb79805<br>SHA1: cef8203b2cf2c56e2822c08c0550fc06171ce759<br>SHA256: 423c8d8cf8a614b4d9fb63c2a49616497a8cc0471c81db5ede712e2e6bc234bf</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>27.50MiB (28.84MB) – 355,992 rows – 250 unique countries<br><small><pre>MD5: 010e576eccbed46c235c9f1f40600f09<br>SHA1: f1295804bfa56f4fa5ef9842667b7cb0b9a0f0ef<br>SHA256: b07b46e8667f0b731e0478cb3dcaa3937b083138f4a8257cad27fa96d61a42a4</pre></small> |
| | | Full Location | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>198.6MiB (208.3MB) – 3,293,034 rows – 242 unique countries<br><small><pre>MD5: 688f39311d9ef3ae0dba52741233235b<br>SHA1: 52a53ef49218397baa93ef51035a1482140b4634<br>SHA256: e84aeb3244fc162911c5a436cc737fce85f6619f3e909a4b98b5ca4fa46ca9de</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>343.6MiB (360.3MB) – 3,013,737 rows – 250 unique countries<br><small><pre>MD5: a3926d0753e258e417a0b18a6d81430e<br>SHA1: 8a1946620f5f949f8a6274e1b473d30ae1b57025<br>SHA256: 2397151a392f426ac2facae01cfaa626480f5ad6d322c982304ec2b165ea38ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-03-08<br>IPv6: 2023-03-08 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.187MiB (5.439MB) – 221,425 rows – 243 unique countries<br><small><pre>MD5: dd82d9c419bdf8d65292298d4da9f4f9<br>SHA1: 4574ddf1c97bda6f9d825016c43005b9659612de<br>SHA256: 28145a84e26234645bd43bcf99287610ec6de00f1543d96a5704cdd74600303a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.81MiB (28.11MB) – 472,772 rows – 249 unique countries<br><small><pre>MD5: 5fc339accde85c2b539a6efba2f8b174<br>SHA1: 35049fccf4492a4eab673415d9814f7b38dfcea0<br>SHA256: 2715c4e3a5f98f963ebe5b71a0628cf1597145a8f1e82444d9831ad0d331ab50</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-03-08<br>IPv6: 2023-03-08 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.6MiB (195.7MB) – 3,084,645 rows – 243 unique countries<br><small><pre>MD5: dcf12cb26141a65ac67b7630b5a635b8<br>SHA1: d453ffc842be214041820c134dd85e2974ce8839<br>SHA256: ae02057cfbe60a4cb423459a4e23f7203890d02d5461ecef35d0ca43faf578ea</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>374.0MiB (392.2MB) – 4,456,315 rows – 249 unique countries<br><small><pre>MD5: f3c102f8b4597403f757f4f87811aa1d<br>SHA1: 5143d96442128020b6a91dd2476fbf46cff231eb<br>SHA256: 11e03efe2ac1e72afde73d94a354137049a2531581c610190c1b8ded4123c619</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-03-07<br>IPv6: 2023-03-07 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.860MiB (10.34MB) – 420,680 rows – 250 unique countries<br><small><pre>MD5: e255138a8dd725cfd57bec1e561fa99a<br>SHA1: 39b23142f3378face676d02b1bed9403534d29d7<br>SHA256: bffb74c62a3e46e01a97bca5e08c2a91a6c87cf21125fbb5e78fc554035e18db</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.02MiB (22.04MB) – 272,068 rows – 250 unique countries<br><small><pre>MD5: 554ccc219480169f063da452ed1d239a<br>SHA1: ee50de6e79fb5007b718a430c253723331f1482c<br>SHA256: bcfdcab8047551b06326315810ec3a80d5213af9d007cf4688231501d966d23e</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-03-07<br>IPv6: 2023-03-07 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.4MiB (198.6MB) – 3,777,563 rows – 250 unique countries<br><small><pre>MD5: cd6ed4097ebe3bd7bffb8f57d1821cb0<br>SHA1: b55d6cd4226805c3a5610b177727a24b7cbb65a1<br>SHA256: 07b4a0f041a8ad58f14af9ab7a770c0e91cb9d890a45bb25fcfebb36366363ab</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.8MiB (232.6MB) – 3,777,563 rows – 250 unique countries<br><small><pre>MD5: 0fdafbe1a1e7c0427aff5661a2b32d02<br>SHA1: 6460e8e299ca2070dc85bebcac830e66e67f35b7<br>SHA256: 74bd353e0d314af40566aabcdd166e6762a48f81193f4c3f0aa174081b446dd3</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.0MiB (205.6MB) – 3,777,563 rows – 250 unique countries<br><small><pre>MD5: 1448bf3aef5f998026bdddca4b6898bf<br>SHA1: c44cd886bf1d5db53fdffde921498d2876e0de91<br>SHA256: 20cf9971f8da023e2dbd7f596047aa33ef90a886d16553c3221d4447a0b57459</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.1MiB (213.0MB) – 3,777,563 rows – 250 unique countries<br><small><pre>MD5: 37bdf49687a3dd779e3372aecc66bdeb<br>SHA1: e0888b56a459c7e466aaec876b27c8ea92ef756c<br>SHA256: a842f288ae115f94e90562b0db6789f31099736e0d21952447b533e51a3212dc</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.0MiB (249.5MB) – 3,777,563 rows – 250 unique countries<br><small><pre>MD5: 8026ccfebbde4c43ed8b3f1fe60597ea<br>SHA1: 5161e9951185c1d032f594278200c6d4a7004342<br>SHA256: 2294df215121ad884ea02180b1415f38c2fadfbd34fdf365a3bdfe1948a2d1e5</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.8MiB (200.1MB) – 3,777,563 rows – 250 unique countries<br><small><pre>MD5: 50f44594957355b624f6fd343e29154f<br>SHA1: e3fd3ca9fe473afd0d40e937cf234e2f025f4693<br>SHA256: 79eb19c5273328d6239559054ab3cfeab815f4843e1d083cfe09ab5bdbe1d644</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.9MiB (250.5MB) – 3,777,563 rows – 250 unique countries<br><small><pre>MD5: 22895939cf0a303945ab74302b50f5e6<br>SHA1: 2f132e100781a6d386758b52e7bc57b3a303a156<br>SHA256: 50890634eafd4a050b5a20fea71380fe9ebf08c61c44fa6f66a3985d3a41abb4</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.1MiB (212.9MB) – 3,777,563 rows – 250 unique countries<br><small><pre>MD5: f19cf1d0abebfe2353cd5aa5d4058133<br>SHA1: 5c2433983dfa2c46848805db1d70b317c9883065<br>SHA256: 70d1c4f4da29173e55eead1e77bd5f2614c38cdc96dcc6dedc4bd600a43b6549</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>124.1MiB (130.2MB) – 1,240,571 rows – 250 unique countries<br><small><pre>MD5: 7c7baccbfa0482e3613c9dbaba3964e4<br>SHA1: d54a146a3b6e712370479976db2efd2da9d58127<br>SHA256: 871c369927838ab116e12fd00a3eba7d2afd8cc858d71fe3a1f8860e5183cb3c</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.1MiB (138.5MB) – 1,240,571 rows – 250 unique countries<br><small><pre>MD5: ab623c4fa669256dd72d405d6f5a507d<br>SHA1: 99ca41e83dc3b0feab626d4d1a3d73e58e033645<br>SHA256: 156bd1cfcc8056d6cd7621b564ca518691b84824a50157a695022a88d903987d</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>126.3MiB (132.5MB) – 1,240,571 rows – 250 unique countries<br><small><pre>MD5: b3044fc7ce3ccb9ce8ae7cf3d2be267f<br>SHA1: 2795dd78d44ea2430a3ca10ec0f096eadaa3dfb1<br>SHA256: d49387e591183b2727694144b48e631dc613e6659a490130341e40c295959de0</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.1MiB (134.4MB) – 1,240,571 rows – 250 unique countries<br><small><pre>MD5: f6ffcb09bdfb0479f439fa724ba13016<br>SHA1: 6edbc55cbf51c66e7a2c52fc9cf3e84e3d090749<br>SHA256: dfd75cbd4207717ac9be241a2c8682f5ef1c35c0705f52f7af3d661bb7169426</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>135.7MiB (142.3MB) – 1,240,571 rows – 250 unique countries<br><small><pre>MD5: e566c0add2d38a08dc9a53741c3740a5<br>SHA1: e1cd129127c64815ca66242d969a8377144f1168<br>SHA256: a1211f1c32cdd2d393bc28c11632919cfefd2a37185864e6f3bbb3649175afa5</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>125.5MiB (131.6MB) – 1,240,571 rows – 250 unique countries<br><small><pre>MD5: a8fb36851ba4c72bef7fca0160014492<br>SHA1: 928ea2e2f0b5ba8368beaab974c9efb05397e85c<br>SHA256: ea68eee1f60bf21622198face2c39bc781ba4e7d8f2c965b382d90e15f3ee243</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.3MiB (142.9MB) – 1,240,571 rows – 250 unique countries<br><small><pre>MD5: 73f472a1d0394bb23da53f7c3a525526<br>SHA1: 3afc85008e9aec0e3fd822cbaab0ba6fbe9c4312<br>SHA256: 10b29fa39a8ab39d0b40849fcbda19185661b4c69aa5f1eeff0206a77deffa1f</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>128.5MiB (134.8MB) – 1,240,571 rows – 250 unique countries<br><small><pre>MD5: 977cd8a06bfb2bb04f6a1e9bd75842a9<br>SHA1: 237948c9933772272f076a2a2627485812de6e15<br>SHA256: 153c28c161d50e76234028d4cecd55bca942089051d07a13071cc888de7e5808</pre></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

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
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the ip address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
