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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-03-26<br>IPv6: 2023-03-26 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.139MiB (6.437MB) – 261,662 rows – 249 unique countries<br><small><pre>MD5: bee6eb1b6e887592d148ef1a4de2c92b<br>SHA1: 1f29ec35bf011949b005d7bb9d74db1cfb7a62eb<br>SHA256: d99ae894ad47a58d7d2b34bcc32c25d216207290b517fdf8b76344d984c401ce</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.409MiB (6.721MB) – 82,973 rows – 250 unique countries<br><small><pre>MD5: 1538e8644517fe1d4ed4785f1beb5a8f<br>SHA1: 9ed1d3ec642d4b0da7243fea383d813b50f257a7<br>SHA256: 792edba5b2d6b61e9b06b8aa30b8c0c3249236968f2dce44ca2e5b7a96c122dc</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-03-26<br>IPv6: 2023-03-26 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.433MiB (9.891MB) – 400,633 rows – 240 unique countries<br><small><pre>MD5: 702a0159aff309bf4621d93d6b474798<br>SHA1: 56f3900e96ebf802299a4eb288e9eb7096746812<br>SHA256: 9d7b28327e01b779208f49c354336102f497c1817c8b354833ede7bf94802046</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.348MiB (7.705MB) – 95,216 rows – 221 unique countries<br><small><pre>MD5: fa62a044825343c251a8197ed2d12f48<br>SHA1: adf39cab4beff97a1cc19d5a557a41b440bb4d0d<br>SHA256: e99e424f383b885eccb625d840c8b88c8c06a13ff40f016b5abc703d14a1d5e2</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-03-26 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.60MiB (15.31MB) – 625,189 rows – 243 unique countries<br><small><pre>MD5: 05dfb2eef5d2fa62867ef3c2c1d8e3ca<br>SHA1: 8850f096100c3f04a03a9b4120eec12028cb081d<br>SHA256: 18cc9c32ea806e6539e10550034208a5b86d7df304492d2d0799d206093c1cfc</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>25.74MiB (26.99MB) – 333,240 rows – 243 unique countries<br><small><pre>MD5: ac773bce10c213d7b252842bc7e61046<br>SHA1: 8d732767a71cbdbbd074cae154878e0d135fb901<br>SHA256: 68ef8389cc5461ce6697a53887b63474dd02d82f431e511449147733bfa266a5</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>8.288MiB (8.690MB) – 354,199 rows – 243 unique countries<br><small><pre>MD5: a1d21d8f62a7c3f50510147c0eb79805<br>SHA1: cef8203b2cf2c56e2822c08c0550fc06171ce759<br>SHA256: 423c8d8cf8a614b4d9fb63c2a49616497a8cc0471c81db5ede712e2e6bc234bf</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>27.50MiB (28.84MB) – 355,992 rows – 250 unique countries<br><small><pre>MD5: 010e576eccbed46c235c9f1f40600f09<br>SHA1: f1295804bfa56f4fa5ef9842667b7cb0b9a0f0ef<br>SHA256: b07b46e8667f0b731e0478cb3dcaa3937b083138f4a8257cad27fa96d61a42a4</pre></small> |
| | | Full Location | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>198.6MiB (208.3MB) – 3,293,034 rows – 242 unique countries<br><small><pre>MD5: 688f39311d9ef3ae0dba52741233235b<br>SHA1: 52a53ef49218397baa93ef51035a1482140b4634<br>SHA256: e84aeb3244fc162911c5a436cc737fce85f6619f3e909a4b98b5ca4fa46ca9de</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>343.6MiB (360.3MB) – 3,013,737 rows – 250 unique countries<br><small><pre>MD5: a3926d0753e258e417a0b18a6d81430e<br>SHA1: 8a1946620f5f949f8a6274e1b473d30ae1b57025<br>SHA256: 2397151a392f426ac2facae01cfaa626480f5ad6d322c982304ec2b165ea38ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-03-26<br>IPv6: 2023-03-26 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.187MiB (5.439MB) – 221,425 rows – 243 unique countries<br><small><pre>MD5: dd82d9c419bdf8d65292298d4da9f4f9<br>SHA1: 4574ddf1c97bda6f9d825016c43005b9659612de<br>SHA256: 28145a84e26234645bd43bcf99287610ec6de00f1543d96a5704cdd74600303a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.81MiB (28.11MB) – 472,772 rows – 249 unique countries<br><small><pre>MD5: 5fc339accde85c2b539a6efba2f8b174<br>SHA1: 35049fccf4492a4eab673415d9814f7b38dfcea0<br>SHA256: 2715c4e3a5f98f963ebe5b71a0628cf1597145a8f1e82444d9831ad0d331ab50</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-03-26<br>IPv6: 2023-03-26 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.6MiB (195.7MB) – 3,084,645 rows – 243 unique countries<br><small><pre>MD5: dcf12cb26141a65ac67b7630b5a635b8<br>SHA1: d453ffc842be214041820c134dd85e2974ce8839<br>SHA256: ae02057cfbe60a4cb423459a4e23f7203890d02d5461ecef35d0ca43faf578ea</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>374.0MiB (392.2MB) – 4,456,315 rows – 249 unique countries<br><small><pre>MD5: f3c102f8b4597403f757f4f87811aa1d<br>SHA1: 5143d96442128020b6a91dd2476fbf46cff231eb<br>SHA256: 11e03efe2ac1e72afde73d94a354137049a2531581c610190c1b8ded4123c619</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-03-23<br>IPv6: 2023-03-23 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.951MiB (10.43MB) – 424,575 rows – 250 unique countries<br><small><pre>MD5: ce5185a8432caaabcfc9703d576c68cf<br>SHA1: b541880260ae400bbba968c44c688998657a69a9<br>SHA256: 02e5379d8ac8927d9de3cce9f5528d6f5b906230b7c399fff91b95f0444d63d0</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.49MiB (21.48MB) – 265,248 rows – 250 unique countries<br><small><pre>MD5: ff81728c999745e4271133ee327b1b72<br>SHA1: 261f648a44af44cf87af01105efdb835847ab529<br>SHA256: ab8b451f00c15ff5a32b4bd15fb49dd123555171d37b27386b6e2527bd90c665</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-03-23<br>IPv6: 2023-03-23 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.8MiB (199.0MB) – 3,783,344 rows – 250 unique countries<br><small><pre>MD5: 7c79d60c67696b515304143ef952406a<br>SHA1: c8429681e264ae2368ef6ec1a1d2a3162cb87078<br>SHA256: 3736c9d88dc565b19e2dab28242efa672a49a151fbf2253736ec169fef0551b0</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.3MiB (233.1MB) – 3,783,344 rows – 250 unique countries<br><small><pre>MD5: 1028376013130e89ea8cc75478fe3028<br>SHA1: 08f3666248a16a7a73faec6ab6c81cba0822e3fa<br>SHA256: ec6c76100fceddf95ae72fac9ad6737dfceeb4140dcc528e3e0ec585e52576f6</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.4MiB (206.0MB) – 3,783,344 rows – 250 unique countries<br><small><pre>MD5: bf6b9a5b6c891e1912e78bd6239360e5<br>SHA1: ff31e0e9101c1d00c3de9977aff3c451d2e23a45<br>SHA256: 1a96ef454a46d93388b3b5edcd149c6bb596849bb46e64273bb32e533f6ec34c</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.6MiB (213.5MB) – 3,783,344 rows – 250 unique countries<br><small><pre>MD5: fa734237627cc86b39d28513b322e2cb<br>SHA1: df3e37301861af37286e0e1b23f86b07f856975a<br>SHA256: 2931bd72b094ee38ef217670d9b80baa22e6356fc6e8e454989c0b7a8124f94c</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.5MiB (250.1MB) – 3,783,344 rows – 250 unique countries<br><small><pre>MD5: ce5be3b5b89167fac90feeeb6bb1e9c3<br>SHA1: 35ca949f0b6f89192bf13cec19a18fa5516791f1<br>SHA256: 19eb5805120734e2fc0e0d3d81c3dedc394450b02a7653ded063cc5bb0f88d2c</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.2MiB (200.5MB) – 3,783,344 rows – 250 unique countries<br><small><pre>MD5: b5cd177c84cf43c4273ab84176edd201<br>SHA1: 1604c5e968e98df66217777a5e03b4424122e442<br>SHA256: 8f28b792b167db6cb32f3ae332a84ddcd5cc2c33f4e95d7bd24dc3c03a296550</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.5MiB (251.1MB) – 3,783,344 rows – 250 unique countries<br><small><pre>MD5: c1da92439266b19814a0d4863ac69045<br>SHA1: 4369f2f8e68184bb37fec00bc7f9fec6dd4d6d5a<br>SHA256: 76ee92111eacf2511287d5bff1313f497474d11051a741ccc66f13f2d4fe90e3</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.4MiB (213.3MB) – 3,783,344 rows – 250 unique countries<br><small><pre>MD5: 3bb1cead3cac090a5c6ac221488e111e<br>SHA1: a5bdd654fd61321ae5fddf5146f651da4bf3984a<br>SHA256: c356d549c261a191acc1dd1755ba52c8ab486b3c70a3d1ea40288dd8bc01cf8f</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.9MiB (132.0MB) – 1,257,258 rows – 250 unique countries<br><small><pre>MD5: 033733a358e366f3f414a521addb63e7<br>SHA1: 3d2de03e4890f02fe58b2c49ebfa80bc5ad89404<br>SHA256: 6c3709fa542b91cb45aff1e2d4fe2a8a072159814409bafae6d2f808034a7f31</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>134.0MiB (140.5MB) – 1,257,258 rows – 250 unique countries<br><small><pre>MD5: bd86135da472f88f287a94fb214f9490<br>SHA1: 73b5f637a984dac65dd832e1c9d43e8dcd5a975a<br>SHA256: f022e6aa4ca373c03f11d5ac74a6d45922ca22347f89940e63a9ecd4dd7576e9</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>128.1MiB (134.3MB) – 1,257,258 rows – 250 unique countries<br><small><pre>MD5: 6e6b1f7ec5d458062bbd0385a1f2db3b<br>SHA1: 1af3dd49f84977346b0d5e2d9427ad57d1561ecc<br>SHA256: 8aaa71f9ff0831090176acca6cca61240407a893201c79a92ea01b545641902e</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>130.0MiB (136.3MB) – 1,257,258 rows – 250 unique countries<br><small><pre>MD5: 0f499ea8f963bf11fa133888bd9d98dd<br>SHA1: 0c5ef1fdaa9cbacbb004841ed613c4e77b8cd182<br>SHA256: 6c714cfcce7a31046d0045a58a6708cbbc1edd17f738ee65f783758b9732119d</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>137.5MiB (144.2MB) – 1,257,258 rows – 250 unique countries<br><small><pre>MD5: 0ff2c4f49b74bf18fa6fd3e95b0afaaa<br>SHA1: 66423b0195d9df0021c3307d04b4c427e368deb8<br>SHA256: 456d32bfc436221178d5d353d866be0e0fddc5490b4f2b67482264163add94fc</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>127.2MiB (133.4MB) – 1,257,258 rows – 250 unique countries<br><small><pre>MD5: 9e860fdf2a5561463fbe6a5e162ad1f7<br>SHA1: cd0195071cd878645c0c9006c8deff4b0bf8740c<br>SHA256: 4cf0897fd31103b37e2c1a3fd98633361bb9123c5fb3b039719e6f19b50b8405</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>138.1MiB (144.9MB) – 1,257,258 rows – 250 unique countries<br><small><pre>MD5: f350fcfe4db8af3112cb094e00318d69<br>SHA1: bccb068f1290c5b058e27c6e333d6c8ac201c888<br>SHA256: 65f5607a2fb15451d468ffbc318a797060940aff9793ead0ecd47f3e768c794a</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>130.2MiB (136.5MB) – 1,257,258 rows – 250 unique countries<br><small><pre>MD5: 9ac7109d8ba396fe2810a1b7c4a07cd1<br>SHA1: e0489f09fce1e54245cf6a2d66ec205c19dc33f0<br>SHA256: f3be1692027e65e535da25b5339fa3784a76bc36d5e4ceec23b5bbfbd944efbe</pre></small> |


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
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
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
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the ip address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
