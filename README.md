[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases

IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Prepossessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [
ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

This repository is hosted on GitLab because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history.

## Database comparison
Scroll right to see all the files »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
|---|---|---|---|---|---|
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2022-12-06<br>IPv6: 2022-12-06 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>8.051MiB (8.442MB) – 343,153 rows – 252 unique countries<br><small><pre>MD5: 9416b195739c220736e0b288cb18c8c9<br>SHA1: e93541a5ccb7b00b1ef5e8d7ae12e2ef59bafcc0<br>SHA256: 13fda079e21e0e659246b0652c5858257c49456e27a8082d032f0477cfd4d882</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.739MiB (7.066MB) – 87,235 rows – 249 unique countries<br><small><pre>MD5: 8075b20b53b62683830cbf8f5f58b715<br>SHA1: 94460354c03fff1a76367be68a3f86ae6281771b<br>SHA256: 25689800db16a0a8065bfd1ea63ba8f0952017a560c1b79917f457e07c120f32</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2022-12-06<br>IPv6: 2022-12-06 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.417MiB (9.874MB) – 400,661 rows – 237 unique countries<br><small><pre>MD5: 27f65c3795c91083c05256dafb618e24<br>SHA1: 001e219a03d859069edb79fe23087bd720f17b0f<br>SHA256: b12a04b232fe10194a69c8760fbf59047050d7fb4318cc10e22c79e5202b0d6a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>6.695MiB (7.020MB) – 86,794 rows – 209 unique countries<br><small><pre>MD5: 74989c23c53a1e47b11a05d550a1a5a5<br>SHA1: 3c2bf05cc7a2ca834f58518cdbd89190ea033094<br>SHA256: 3ed929309db6ea5db5f23eba407e951b50b85a4d40b1219533a8f4e3f2aa3fbf</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2022-12-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.895MiB (8.278MB) – 337,688 rows – 244 unique countries<br><small><pre>MD5: 6fa50a8820a5f1f77f7042e65d9bb9c1<br>SHA1: 55ba8ec8273d1dfcda62af6ed9f2defa6d4913a6<br>SHA256: 11178cbceab21722fe20c1df3deb08a9a4eb643767683916e00ef4043e0a881d</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>16.71MiB (17.52MB) – 216,263 rows – 250 unique countries<br><small><pre>MD5: b26fd93073ec29d7f9a035eb8cf0eda6<br>SHA1: f653943414705ea9e5d4550c4ece64b4803ba885<br>SHA256: e85cb4247adb633e408dfe0447bacb00bf691832a66749f2cd7d684f3e85cab6</pre></small> |
| | | Full Location | Monthly<br>2022-12-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>199.3MiB (209.0MB) – 3,304,179 rows – 243 unique countries<br><small><pre>MD5: 39c76c7dd30cb5167a168873a7e9667a<br>SHA1: 91a1ca97766a6f3812da921378b34e38f876ddbb<br>SHA256: 72d6b5025381463e7d332b0dc62a678eaa146bc0c35aa455bfaa6770e8a64889</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>374.5MiB (392.7MB) – 3,263,628 rows – 250 unique countries<br><small><pre>MD5: 8c00d633b794d3e4c5d727cf862f99c5<br>SHA1: ae2c0ae0f91c07436ce23cf701bb00aac0080628<br>SHA256: 13b613ee9d93a76d2acdcdd7cd3534415404ab61f12cf16dc5df55e677308165</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2022-12-06<br>IPv6: 2022-12-06 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.012MiB (5.255MB) – 213,933 rows – 242 unique countries<br><small><pre>MD5: 56184d3175ab47868dffde348904e158<br>SHA1: f905d1480a377097b9a95fe74b5ffb9a2d116c23<br>SHA256: 9990d9178bfb07ce331a23ba79684c142f2b056449ee96e1b7f93ff7e8533da4</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.12MiB (27.39MB) – 459,678 rows – 249 unique countries<br><small><pre>MD5: be014321b4eb0f97c9dc69de42176f2a<br>SHA1: eab6fe44c6e53f60faaaf2ec0cd15c12b2459314<br>SHA256: 140b75a7a789e735106603ce76067a476dc2c88a0905fc716f8465262c49c3c4</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2022-12-06<br>IPv6: 2022-12-06 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>187.2MiB (196.3MB) – 3,095,554 rows – 242 unique countries<br><small><pre>MD5: c02bcc63819d89151ba76a2ae286bbe3<br>SHA1: 07ef852da1fc4dce01a0156d19ed4c99a5deac4a<br>SHA256: dadd32df785b91b703043032beccbb7c61464632354d3763c3502b0d9bb01868</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>425.1MiB (445.8MB) – 4,907,387 rows – 249 unique countries<br><small><pre>MD5: 037be0bebdfc294677348156dc7f4c8b<br>SHA1: 5410cdb0f38fac92ebe54fe19bf63e53370c6f60<br>SHA256: bd00e50f5bc9fb898ff8cef8deae0e8e898c4c949a9c13a16cd5a1a0d6b97dc2</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2022-12-05<br>IPv6: 2022-12-05 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.210MiB (9.657MB) – 393,002 rows – 250 unique countries<br><small><pre>MD5: 11e8317fc9c238a9b405cc47d1bc2ead<br>SHA1: ed9666b80db387b56113b4017b35da4b97a7b207<br>SHA256: 18f3585c2e2597babc1b90914eb6f7f74cbf35926ef86dfc9b66bac7baf0f290</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.69MiB (21.70MB) – 267,845 rows – 250 unique countries<br><small><pre>MD5: 101c95fb3665ab3d5b6a3241cdc008e6<br>SHA1: 350d84fa37046a231c9d911304ea8b4342d468bf<br>SHA256: 351871243f93fe86861a4f596a51ba5ce8dc8358e07c47bd19149a6ac582d94b</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2022-12-05<br>IPv6: 2022-12-05 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>172.9MiB (181.4MB) – 3,428,594 rows – 250 unique countries<br><small><pre>MD5: e356fdd772c4e626145fe3a64adf4604<br>SHA1: c7cea72fbd401e2cd418db321b3309b3c91cc98f<br>SHA256: 199cd12fd936e3563d1135b5cf8ba7bbcaca1fa7e02622f313fbeeaa6e8927b9</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>202.0MiB (211.8MB) – 3,428,594 rows – 250 unique countries<br><small><pre>MD5: b94f6899f841460897cb1957d9d31f48<br>SHA1: bbe817c07b8f44d827808f5fdeee24553a353152<br>SHA256: 8efed7baf3470e57e393f11b7adca728e1402d1b25739a8209a384de25fe284b</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>178.5MiB (187.2MB) – 3,428,594 rows – 250 unique countries<br><small><pre>MD5: 8a1e0b0cb7b71db877a53099b537fa38<br>SHA1: e1d6967f21d7bc51edc0210e2d550080a6d3d332<br>SHA256: 3ef2fbb3e480dc8bc987146a754bca461d12fbc0a9f8f6bc9f8add818c4b3342</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>184.8MiB (193.8MB) – 3,428,594 rows – 250 unique countries<br><small><pre>MD5: a80f41927e86129603ee883e1169cd14<br>SHA1: 0d957449184d13407e001e030eadf324fa3c43c6<br>SHA256: 8af63adf80b18f040020c18059c4159b4a4941af0b899fbd9330710278a068e5</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>215.1MiB (225.5MB) – 3,428,594 rows – 250 unique countries<br><small><pre>MD5: 0513f94cf3c90803be3860eb0fc7f496<br>SHA1: 0635ec47e724663babd5c77045460ab16c4da59e<br>SHA256: 60a791a330a4e5361981367baf65144dfaf95f35f038f76e3eaf4934bf2a67b8</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>173.5MiB (182.0MB) – 3,428,594 rows – 250 unique countries<br><small><pre>MD5: 2b9fe5a47ec882df985399c64bf97726<br>SHA1: cf08e85d1cedddbda2afa0352dc72c5554d59c9e<br>SHA256: 86abe3021fc8d7023c8474893e7b10d7676b114fa86276f9b1115e5b40393da7</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>216.3MiB (226.9MB) – 3,428,594 rows – 250 unique countries<br><small><pre>MD5: 4588b7f4f5fc2968a42f49d4ff52a1b7<br>SHA1: 6ed8e649918b3eec47da3af30ee2d13bd606eae2<br>SHA256: 79c947c0996089261790e26163db9a4e9b144bfb6e70b3194f262545860f869b</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>183.3MiB (192.3MB) – 3,428,594 rows – 250 unique countries<br><small><pre>MD5: 3b115f62f0ad43aabe333ded2a3698f9<br>SHA1: 9761a712f6c14146c6565120b35c7e067c50c74d<br>SHA256: 2b74f6a8f73c0f4f33b46a70109e548336662b7e74929ac31e1906aab0799f10</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>112.1MiB (117.6MB) – 1,124,423 rows – 250 unique countries<br><small><pre>MD5: 32f6c3edeb61088367a102a1d565e1c4<br>SHA1: ec76ee9ce9ddc1faaa6203d60c088ffba8f066f8<br>SHA256: d7571bfe48838016ef5357dabb98a6ee792d034198c3c7c9c667bdc7db240cee</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>119.2MiB (125.0MB) – 1,124,423 rows – 250 unique countries<br><small><pre>MD5: bac083c1e81e93a9f238a86eaf71765c<br>SHA1: 14fbd3ef7c5de8b385bc21248efc3b44838b6a54<br>SHA256: 579416dd9fdb4d7e62ad615103875c72872e306976def372e3a4e73cc05e549f</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>114.1MiB (119.7MB) – 1,124,423 rows – 250 unique countries<br><small><pre>MD5: e120ec7f68e7cdc12ae1a6bc516c9e1a<br>SHA1: d3d4abe9e34a41f2128cac6464d0e75fd54ced74<br>SHA256: 62d1b0bb19a9e95c7d8107f8cceace14795ac0c6801b3354c0a47b507138e27c</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>115.6MiB (121.2MB) – 1,124,423 rows – 250 unique countries<br><small><pre>MD5: 70dcfc95553d6d1dc9ee7dcfe2537d58<br>SHA1: 7af703085b4b63f8e601e73c751ce983462b866c<br>SHA256: 8072324f297c904e2105ec317a5271876925312937b89e4c9ef7b33c292a4cb1</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>122.0MiB (127.9MB) – 1,124,423 rows – 250 unique countries<br><small><pre>MD5: dfbec44a44082cc2ecb88ad4b8ec3db7<br>SHA1: 1417faf4fd5808ede63e37dcf6d3a824ef6777cd<br>SHA256: 4528d91be05645b0576362808f8b60d42061ae10ffa4baa3afdfb3e4081ee74a</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>113.3MiB (118.8MB) – 1,124,423 rows – 250 unique countries<br><small><pre>MD5: 93ccd5d9a2bb5fae02f8d9095d1d0239<br>SHA1: 97758303fbad4ad9145c874786771baf0542a6f7<br>SHA256: ae8561b4096c9263c87552d270efe2a7ebef666f154d9b615a96b8b282a9cf5a</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>122.5MiB (128.4MB) – 1,124,423 rows – 250 unique countries<br><small><pre>MD5: 2796f7a9cb5f4b7c9bb8cf4ad57716ad<br>SHA1: 00642a7dd8e8ac0920633bcd3f90298637e86247<br>SHA256: 3fcfe8564983db2ad41735547e5d724fecc5cd87dbd8c25f1d9aeda16930c177</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>115.9MiB (121.5MB) – 1,124,423 rows – 250 unique countries<br><small><pre>MD5: b89395b59700e271931783d3f36262a6<br>SHA1: 43c07fae5d3321f1dd5069133165e811b0939544<br>SHA256: 7650a05f83e9c7ef5481221f1c1d2cf036a6bad10b0980d9a2b488c5ff49e18a</pre></small> |


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
