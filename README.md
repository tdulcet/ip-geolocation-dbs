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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-03-17<br>IPv6: 2023-03-17 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.140MiB (6.438MB) – 261,727 rows – 248 unique countries<br><small><pre>MD5: 3e410ab1cba2ae465212c6e15698e5d4<br>SHA1: a57fe9261a5320dc15201c5c93f8914c0378c41a<br>SHA256: 0626195fb2170fce5264e5c536210246e87f03c9087ac2f72668e96923e52bcc</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.386MiB (6.696MB) – 82,669 rows – 250 unique countries<br><small><pre>MD5: 745273451e52ecaf1b6d7bcda99e47cc<br>SHA1: ee236bfee8a7d1d1e88ebe797032892f99ba62b8<br>SHA256: 6ef013c9d70ff04456df10b71658b5bbc2a520819845f14cfe5d332abae5a06a</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-03-17<br>IPv6: 2023-03-17 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.425MiB (9.883MB) – 400,290 rows – 240 unique countries<br><small><pre>MD5: 506546c854f9da8bbe298e35a1613a15<br>SHA1: 84e411942ae4e4e4ee39af815505442261b643a3<br>SHA256: cfa501b0af0e7399e1ce0b3914c7e7756852a7c8700f50654ebfd89ebcd30b4c</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.303MiB (7.658MB) – 94,643 rows – 221 unique countries<br><small><pre>MD5: c8a94cf1666e2360fbed1c44f403c76e<br>SHA1: 66e1f0ce817662f2c73c11cd0acad64d9ed3799f<br>SHA256: 8dbf2857d427a72d200ca27c121e18cc0f8b733a8d7f9646556a4c821bca7b16</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>8.288MiB (8.690MB) – 354,199 rows – 243 unique countries<br><small><pre>MD5: a1d21d8f62a7c3f50510147c0eb79805<br>SHA1: cef8203b2cf2c56e2822c08c0550fc06171ce759<br>SHA256: 423c8d8cf8a614b4d9fb63c2a49616497a8cc0471c81db5ede712e2e6bc234bf</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>27.50MiB (28.84MB) – 355,992 rows – 250 unique countries<br><small><pre>MD5: 010e576eccbed46c235c9f1f40600f09<br>SHA1: f1295804bfa56f4fa5ef9842667b7cb0b9a0f0ef<br>SHA256: b07b46e8667f0b731e0478cb3dcaa3937b083138f4a8257cad27fa96d61a42a4</pre></small> |
| | | Full Location | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>198.6MiB (208.3MB) – 3,293,034 rows – 242 unique countries<br><small><pre>MD5: 688f39311d9ef3ae0dba52741233235b<br>SHA1: 52a53ef49218397baa93ef51035a1482140b4634<br>SHA256: e84aeb3244fc162911c5a436cc737fce85f6619f3e909a4b98b5ca4fa46ca9de</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>343.6MiB (360.3MB) – 3,013,737 rows – 250 unique countries<br><small><pre>MD5: a3926d0753e258e417a0b18a6d81430e<br>SHA1: 8a1946620f5f949f8a6274e1b473d30ae1b57025<br>SHA256: 2397151a392f426ac2facae01cfaa626480f5ad6d322c982304ec2b165ea38ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-03-17<br>IPv6: 2023-03-17 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.187MiB (5.439MB) – 221,425 rows – 243 unique countries<br><small><pre>MD5: dd82d9c419bdf8d65292298d4da9f4f9<br>SHA1: 4574ddf1c97bda6f9d825016c43005b9659612de<br>SHA256: 28145a84e26234645bd43bcf99287610ec6de00f1543d96a5704cdd74600303a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.81MiB (28.11MB) – 472,772 rows – 249 unique countries<br><small><pre>MD5: 5fc339accde85c2b539a6efba2f8b174<br>SHA1: 35049fccf4492a4eab673415d9814f7b38dfcea0<br>SHA256: 2715c4e3a5f98f963ebe5b71a0628cf1597145a8f1e82444d9831ad0d331ab50</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-03-17<br>IPv6: 2023-03-17 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.6MiB (195.7MB) – 3,084,645 rows – 243 unique countries<br><small><pre>MD5: dcf12cb26141a65ac67b7630b5a635b8<br>SHA1: d453ffc842be214041820c134dd85e2974ce8839<br>SHA256: ae02057cfbe60a4cb423459a4e23f7203890d02d5461ecef35d0ca43faf578ea</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>374.0MiB (392.2MB) – 4,456,315 rows – 249 unique countries<br><small><pre>MD5: f3c102f8b4597403f757f4f87811aa1d<br>SHA1: 5143d96442128020b6a91dd2476fbf46cff231eb<br>SHA256: 11e03efe2ac1e72afde73d94a354137049a2531581c610190c1b8ded4123c619</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-03-16<br>IPv6: 2023-03-16 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.917MiB (10.40MB) – 423,104 rows – 250 unique countries<br><small><pre>MD5: 9d2d1a147c7204dc48cbb51ea694047d<br>SHA1: d0bac5e215d0290b1f825b912e06eb5b14d2cb77<br>SHA256: 6128851b9c2333badd64b353dd8d7f4dd814f0461b255ae527fcfe009f8e6947</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.37MiB (21.36MB) – 263,682 rows – 250 unique countries<br><small><pre>MD5: ad195d63f42267f7ec13fb69470cabb7<br>SHA1: ca33b69ed6ad9804fb95053a239d1787c07dff2c<br>SHA256: 5c5c192dce64db326efc4d0b8d6ff3e7a891f1f20b5c419adef6156372f13c91</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-03-16<br>IPv6: 2023-03-16 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.3MiB (199.6MB) – 3,795,796 rows – 250 unique countries<br><small><pre>MD5: 0ecb4d9e8255056ec537055f65fdea64<br>SHA1: a8ce8b99324969f2e36e1619ebffc78d38631416<br>SHA256: 0a7c8e9ff3d160146bcbbd2c595f22418931d74a6c0705180243e706d930f3fd</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.9MiB (233.7MB) – 3,795,796 rows – 250 unique countries<br><small><pre>MD5: 262d12bc6035b18cfe1ef0f2bf5f55c7<br>SHA1: 4f549eb6f937b6f5625d546f07b1999c5286c08f<br>SHA256: be1f2dec640008267c16381675327a3239d28b4cfb7e4869d9095ef6b213986e</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.0MiB (206.6MB) – 3,795,796 rows – 250 unique countries<br><small><pre>MD5: 4a7f7690381c7103ee75e9877a5928e5<br>SHA1: 637ad2289e3af953eb8274f1d4b171565f0e276b<br>SHA256: 87fb398cb9196ca789c03f8c850a6a96bc533ed73522345fd97ec56988b73980</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>204.2MiB (214.1MB) – 3,795,796 rows – 250 unique countries<br><small><pre>MD5: d940cb2373e70976d6b1aae370075679<br>SHA1: 6d535419622429d314e574d98bc6b0db3559e5da<br>SHA256: ed663cdd9dcc755d20d074b3f3c46c7c0c0eea23d2da692db2948cc6080e00e5</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.3MiB (251.0MB) – 3,795,796 rows – 250 unique countries<br><small><pre>MD5: 913f14890dbb51483fc357fbd1b6f30a<br>SHA1: aea7f32cf249dfb4cef1b4a8595ef09ef79459fa<br>SHA256: 722a67c6b465fcc8d641f04e8eb996e95c697fe40e5311aaa11fdd8dddf92d48</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.7MiB (201.1MB) – 3,795,796 rows – 250 unique countries<br><small><pre>MD5: 679777b7ce13a79272ffb887d6c33ddb<br>SHA1: e8dd6bad256a8c918d6844c71ea152c0ad0ad3a8<br>SHA256: 6b0de8156f027738304800a021b5795e6c49e9e8f9c4853ebac680d360584e87</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.2MiB (251.8MB) – 3,795,796 rows – 250 unique countries<br><small><pre>MD5: 9d866f42c22dd1fdb6c7eb71a8978c16<br>SHA1: 63d031f7d1a0e6222abcd5af126e3e35bc6c0df3<br>SHA256: cd2b9d0f04f44e9c09eee384164103ce3ba3cf2ca240adefcc449cbd6d7dab41</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>204.0MiB (214.0MB) – 3,795,796 rows – 250 unique countries<br><small><pre>MD5: 34892a078e8b37126f2aa63da451ec28<br>SHA1: e8202f27ba238ffc1c6f2d759e132201ed96a71b<br>SHA256: 5df7e936f60748437b2b2ea46e08589f07028921aef06c7106a075be26b2f444</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.7MiB (131.8MB) – 1,254,921 rows – 250 unique countries<br><small><pre>MD5: 0e4da20c2c0d11006a1048ffbe1c6a05<br>SHA1: c69391a05590cfcd2ba1bc17ddc12a1dcbd54eba<br>SHA256: aa9c91d0528b254c15565a7b1a92c8ec5074a9a76bf01cf2a99d08c120a18286</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>133.7MiB (140.2MB) – 1,254,921 rows – 250 unique countries<br><small><pre>MD5: 07d4b2b1ee7afea5f8dfc68eb3777d2f<br>SHA1: fd0f584d7485fecc1044a88f67fa29d2752a34e6<br>SHA256: 0357917628f07f4e0927d0f1a7f0db88e2f015156f0f4f1a0de551749e26ab5b</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.8MiB (134.1MB) – 1,254,921 rows – 250 unique countries<br><small><pre>MD5: 93c81e90f3685d1f4887e91e4756db06<br>SHA1: b5edbaf88fa132f7cad6a673fdd9ec100edc26f5<br>SHA256: 03e1a7c8dd0cd5a04f64d7448cd17816c74a312c829e8ce8d20165dda9310667</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>129.8MiB (136.1MB) – 1,254,921 rows – 250 unique countries<br><small><pre>MD5: 25bae5aa770a761c7298b019612839db<br>SHA1: 3d80e664c298dab0b5d682de905570131256ef70<br>SHA256: 1cb65dba040bf9549c12b543b07f5b0aa99f7fcb139284b5f372d471fead123e</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>137.3MiB (144.0MB) – 1,254,921 rows – 250 unique countries<br><small><pre>MD5: 2aeb1e5bb4ef167e60da3540cb4a4b5a<br>SHA1: a395e1f3bfcf5b9bab2d21e4960df61710f0aabc<br>SHA256: 8a7c9c2ec4adb0ef375041aef6edb307b5288da33a5d412a49acd3dd60e27be2</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>127.0MiB (133.1MB) – 1,254,921 rows – 250 unique countries<br><small><pre>MD5: 5555b6682c7287516402223281b82e0b<br>SHA1: 776bc0516bc0f81d347d34e8cecbc912095a5417<br>SHA256: cb04532aa5897cf7b95067931a300c81d87d2367748cfcb498b94464ffd6a15c</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>137.9MiB (144.6MB) – 1,254,921 rows – 250 unique countries<br><small><pre>MD5: ddf2f862264417e490aacc0bd3809b94<br>SHA1: 4d72cf061abf119aeca3e77f34b3f65784f3dcb5<br>SHA256: 1d87e71361f0903b126d242129436031b4d6b4788a123014508b34b9dfe0d107</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>130.0MiB (136.3MB) – 1,254,921 rows – 250 unique countries<br><small><pre>MD5: 81b92317c849c97480f34b044b5f7b36<br>SHA1: f235f505f14022bfe6ace675fab8cb639c9e6c84<br>SHA256: 1a085d684cc271e0f632beecdff3717983422f97166d294e4e478ba1a3dc61cb</pre></small> |


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
