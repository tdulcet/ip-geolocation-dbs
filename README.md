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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-03-14<br>IPv6: 2023-03-14 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.143MiB (6.441MB) – 261,833 rows – 248 unique countries<br><small><pre>MD5: e66cccfe21007f5a6451b4c9134f2d61<br>SHA1: afe8a48e6890d6cee34ca8bdb740b531180c05a3<br>SHA256: 7735d070c20894913baa9f0dd5c3e8d3f0f25053ec5e9c741a6a3dbdb050866c</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.380MiB (6.690MB) – 82,592 rows – 250 unique countries<br><small><pre>MD5: 34d4e9d40e3e555f59ac1b5e2a175587<br>SHA1: 89de7801864d5be35067bfed3eb5deaec3e00f52<br>SHA256: f6a542f8eb0d87eadb929e7cc92d0bca584912143c17392f4b23e7d89442ba5e</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-03-14<br>IPv6: 2023-03-14 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.413MiB (9.871MB) – 399,836 rows – 240 unique countries<br><small><pre>MD5: ce479310c71b9d33d7513d87e0b7f296<br>SHA1: 8c0576b7a72fa000b5b3f840f163dedb500a19f9<br>SHA256: dfcaa34ecfcc25da9a537f577003e6c5671cfd8f1219452ae801c4cf12bdf28b</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.307MiB (7.662MB) – 94,688 rows – 220 unique countries<br><small><pre>MD5: 758ba624008e160e0249bab45e86e2cd<br>SHA1: f1a72c3abe5da7712327115c9b327c7eaf47062f<br>SHA256: 18adc3198e5f243bcde2acd2d0b5e3cf27630d41236d82251abe7c69647286dd</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>8.288MiB (8.690MB) – 354,199 rows – 243 unique countries<br><small><pre>MD5: a1d21d8f62a7c3f50510147c0eb79805<br>SHA1: cef8203b2cf2c56e2822c08c0550fc06171ce759<br>SHA256: 423c8d8cf8a614b4d9fb63c2a49616497a8cc0471c81db5ede712e2e6bc234bf</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>27.50MiB (28.84MB) – 355,992 rows – 250 unique countries<br><small><pre>MD5: 010e576eccbed46c235c9f1f40600f09<br>SHA1: f1295804bfa56f4fa5ef9842667b7cb0b9a0f0ef<br>SHA256: b07b46e8667f0b731e0478cb3dcaa3937b083138f4a8257cad27fa96d61a42a4</pre></small> |
| | | Full Location | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>198.6MiB (208.3MB) – 3,293,034 rows – 242 unique countries<br><small><pre>MD5: 688f39311d9ef3ae0dba52741233235b<br>SHA1: 52a53ef49218397baa93ef51035a1482140b4634<br>SHA256: e84aeb3244fc162911c5a436cc737fce85f6619f3e909a4b98b5ca4fa46ca9de</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>343.6MiB (360.3MB) – 3,013,737 rows – 250 unique countries<br><small><pre>MD5: a3926d0753e258e417a0b18a6d81430e<br>SHA1: 8a1946620f5f949f8a6274e1b473d30ae1b57025<br>SHA256: 2397151a392f426ac2facae01cfaa626480f5ad6d322c982304ec2b165ea38ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-03-14<br>IPv6: 2023-03-14 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.187MiB (5.439MB) – 221,425 rows – 243 unique countries<br><small><pre>MD5: dd82d9c419bdf8d65292298d4da9f4f9<br>SHA1: 4574ddf1c97bda6f9d825016c43005b9659612de<br>SHA256: 28145a84e26234645bd43bcf99287610ec6de00f1543d96a5704cdd74600303a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.81MiB (28.11MB) – 472,772 rows – 249 unique countries<br><small><pre>MD5: 5fc339accde85c2b539a6efba2f8b174<br>SHA1: 35049fccf4492a4eab673415d9814f7b38dfcea0<br>SHA256: 2715c4e3a5f98f963ebe5b71a0628cf1597145a8f1e82444d9831ad0d331ab50</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-03-14<br>IPv6: 2023-03-14 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.6MiB (195.7MB) – 3,084,645 rows – 243 unique countries<br><small><pre>MD5: dcf12cb26141a65ac67b7630b5a635b8<br>SHA1: d453ffc842be214041820c134dd85e2974ce8839<br>SHA256: ae02057cfbe60a4cb423459a4e23f7203890d02d5461ecef35d0ca43faf578ea</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>374.0MiB (392.2MB) – 4,456,315 rows – 249 unique countries<br><small><pre>MD5: f3c102f8b4597403f757f4f87811aa1d<br>SHA1: 5143d96442128020b6a91dd2476fbf46cff231eb<br>SHA256: 11e03efe2ac1e72afde73d94a354137049a2531581c610190c1b8ded4123c619</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-03-13<br>IPv6: 2023-03-13 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.895MiB (10.38MB) – 422,156 rows – 250 unique countries<br><small><pre>MD5: 3bd50f4db83061c6585207102bce6c86<br>SHA1: aedd128284cafe293203f5da8c1c944e19c3ef60<br>SHA256: 932542562d04e985b9810d63b07c3e70f9142e0f315ad512a380de4010c032da</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.36MiB (21.35MB) – 263,521 rows – 250 unique countries<br><small><pre>MD5: 56af6c5654f1c66c9157994da156ae12<br>SHA1: f68c5b523b2b39e8cd11ff635fae2cd3aa483455<br>SHA256: d491724bc7cef5d16b37fa068599f3de51cfdea4415e37e09e56788e4f7ed49c</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-03-13<br>IPv6: 2023-03-13 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.5MiB (199.7MB) – 3,796,580 rows – 250 unique countries<br><small><pre>MD5: 54b3338848f5dacefb0f12b9cedd214b<br>SHA1: 31b84e0faf5f019211f289c7b4d743442d9191fc<br>SHA256: 7b2ac482b0028b106572ee18055269595188b602620a57e9145fa46fb310a0ad</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>223.2MiB (234.0MB) – 3,796,580 rows – 250 unique countries<br><small><pre>MD5: fbb2f5f453dcdfec747c8612a6ee9db8<br>SHA1: 422d4fb4bd47fa564c78be1462b4c651f7e858de<br>SHA256: 598be60917057d1914278865213829351a8221e3694b6ebca9bd8b634e083c3d</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.1MiB (206.7MB) – 3,796,580 rows – 250 unique countries<br><small><pre>MD5: b6f55067c7fd748532da540125f891e8<br>SHA1: d22431cf167286242c655fb5b409a26659c3a14e<br>SHA256: aa150e17143686a5d2bc51728365806442d206f89e9375fe3c5ffec593cdefb9</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>204.3MiB (214.2MB) – 3,796,580 rows – 250 unique countries<br><small><pre>MD5: ceaf884f57aaf85d9e972f315953ece5<br>SHA1: b103c8a6628672980bb9666ee7b8fe51988eb066<br>SHA256: fd83ce532bf6d09618e2f4c63f37c2b9eae07c2560af17cdacd8a40dcab68c3f</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.5MiB (251.1MB) – 3,796,580 rows – 250 unique countries<br><small><pre>MD5: c29259b137e581a24226b3f74d437a95<br>SHA1: 7bcd637aaab49e5f3d762f8a7f610d150f109d18<br>SHA256: 7baa7ba0c22f54b94d22543f8037c3d722599539dcf0b1f52fa008aeda3ca248</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.9MiB (201.2MB) – 3,796,580 rows – 250 unique countries<br><small><pre>MD5: d476bf62c59b5641b8cfe6755c83f498<br>SHA1: 79c429c608fd39488a55d48c23556f2866a38f9e<br>SHA256: 93178c6bf63c18e401f0c5f0821fd432ab1ee6a25f784d72a85d7ea3b90330b5</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.4MiB (252.1MB) – 3,796,580 rows – 250 unique countries<br><small><pre>MD5: db4cf7ab4d4c3f305e6a3d7bab7290a8<br>SHA1: b49da5c0b50b35e54ba80e1a7df72f33642c962a<br>SHA256: 177478ec4de6e7d8448608cab56509535d1491636b3d19fb5453e5c242dd6463</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>204.2MiB (214.1MB) – 3,796,580 rows – 250 unique countries<br><small><pre>MD5: 3117311d1ea983f2da83a7bb0545a50c<br>SHA1: dbb73c34e43166c8be9726f6401572ca617e4e09<br>SHA256: a5a4bddd92ee603f0483d3b8f820f4b901638cc2a8bf351bdb5b5fbdb0f5f603</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.9MiB (132.0MB) – 1,257,278 rows – 250 unique countries<br><small><pre>MD5: d275081bc333860dab2d85a4eca3bcf3<br>SHA1: c79436b8e313d546c6c83b3ed2dc9fd28b47675b<br>SHA256: ee481a408e78f3d596ca2979790ae8d7cd1eadd14b3d93155bee98cc64be73a9</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>134.0MiB (140.5MB) – 1,257,278 rows – 250 unique countries<br><small><pre>MD5: 68fd3c8bb652b48184fa0666cff8ffa1<br>SHA1: 805b0710d2d5676383f75d31bfad18b6175fb1bf<br>SHA256: bcc9936101008866e76462d3a91fbf0b87456e0745ca8c999e9cf3a981ef49ed</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>128.1MiB (134.3MB) – 1,257,278 rows – 250 unique countries<br><small><pre>MD5: c0fb52b921c375ec9a13ba41f620b457<br>SHA1: affb29d8c1041dbfc09a791ff6f8345c5b7f275f<br>SHA256: fc1588c41fd46af735f083a05c55840a8c505531b50bc793128af3ad2ccc8363</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>130.0MiB (136.4MB) – 1,257,278 rows – 250 unique countries<br><small><pre>MD5: 73ffde37b6c9705c084833f3597e2fa6<br>SHA1: 542cb0c31099cde7eee12f59ebcbdecd8a99c80d<br>SHA256: 19fd02e217de265cf25bc2a391e61d73245fde6afbff613da7fcb02a1d0e121a</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>137.5MiB (144.2MB) – 1,257,278 rows – 250 unique countries<br><small><pre>MD5: 46e066312af97db8c9df2bf0bb7e04f5<br>SHA1: 406adc161facfbae705dede1d86cb70812eb4e27<br>SHA256: f4ba1f4b02091da2545b9fb0da35931497a574d4d27ea2dfe13e6b5fe993c7ea</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>127.2MiB (133.4MB) – 1,257,278 rows – 250 unique countries<br><small><pre>MD5: ee58f4d534e9ca8dc38c48c5b510d269<br>SHA1: c33176204eb939e49abd3b79b11ee7e37553be83<br>SHA256: 6cf3801f32628e6d428c3ec25f66094c22b29a889d4617ad7ba49eac6e5166fb</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>138.1MiB (144.9MB) – 1,257,278 rows – 250 unique countries<br><small><pre>MD5: 027626b5a57e41f013860220975a9df2<br>SHA1: ea7970a24aa1793c02f984e7947664dfab55c694<br>SHA256: 5a877d7f1eeb31ec1874be040e9f0a42c84080c38e6ea87ef6b2a34456f8598d</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>130.2MiB (136.5MB) – 1,257,278 rows – 250 unique countries<br><small><pre>MD5: bec6a09275f915f9c22c0118b740817f<br>SHA1: 8778dc55984492171d66d44e5a11af70f2760be6<br>SHA256: 1d26c5b029d82f20c04a7d97e4d2a58ac4c84c7fa2143fe8f8b0234ef8a31705</pre></small> |


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
