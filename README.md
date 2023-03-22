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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-03-22<br>IPv6: 2023-03-22 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.135MiB (6.433MB) – 261,491 rows – 248 unique countries<br><small><pre>MD5: 52c566d83b5264cf08f5d7c378f2bdf4<br>SHA1: 2d5219c992c8da54ef468a806572c04ec36c5ade<br>SHA256: 6d511b625c634461f6379543e8035891a65e59fe8c467b1b7711875b9b1acd7f</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.395MiB (6.706MB) – 82,786 rows – 250 unique countries<br><small><pre>MD5: 2452fc789e9433960b31c33c2c0d6bee<br>SHA1: 4e6fdd5b2d874e0899e0269ae68c0d211cef2c9c<br>SHA256: c08f6238c32eec4425b60bc9ae5def12bbc0280603831cdcbf255195fb996aca</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-03-22<br>IPv6: 2023-03-22 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.428MiB (9.886MB) – 400,421 rows – 240 unique countries<br><small><pre>MD5: 7ff059fd14d327be4f70a62ecce83319<br>SHA1: bc407ff8d6c406d6744bf206adab64518bcc1f3a<br>SHA256: c483b8356134bc272afab4704dd9d0462ce7ec7bb1bd977739858cb39773190e</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.323MiB (7.679MB) – 94,900 rows – 221 unique countries<br><small><pre>MD5: 171f5b125ff3d6c025eff6d59c6dace7<br>SHA1: d867f8d4834f6f8975e098baecde92524ab30829<br>SHA256: 803e21a819b99735bb659ccc7f7c3ee4c3479805b6edc9ed1422866fe68e7396</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-03-22 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.75MiB (15.46MB) – 631,219 rows – 243 unique countries<br><small><pre>MD5: e5464179b71887f048789a0b068d0f75<br>SHA1: 7ce07961df6eca814d881c2ae89fbac1a000293c<br>SHA256: fa38dd0014d758444df8926e1b7d8a269f45fa20cab7d86aae3b52bb354d0a0a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>36.23MiB (37.99MB) – 469,064 rows – 243 unique countries<br><small><pre>MD5: bf7fd1020ae38c35b5db5d6bb79e5158<br>SHA1: 1a49ff5d480abf1df8120abef7f22390ca39bf90<br>SHA256: a0a3a6737df3e4f8680d6f4d0b0f43a3dda0ff8b59e8382fff4927be54d9b55a</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>8.288MiB (8.690MB) – 354,199 rows – 243 unique countries<br><small><pre>MD5: a1d21d8f62a7c3f50510147c0eb79805<br>SHA1: cef8203b2cf2c56e2822c08c0550fc06171ce759<br>SHA256: 423c8d8cf8a614b4d9fb63c2a49616497a8cc0471c81db5ede712e2e6bc234bf</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>27.50MiB (28.84MB) – 355,992 rows – 250 unique countries<br><small><pre>MD5: 010e576eccbed46c235c9f1f40600f09<br>SHA1: f1295804bfa56f4fa5ef9842667b7cb0b9a0f0ef<br>SHA256: b07b46e8667f0b731e0478cb3dcaa3937b083138f4a8257cad27fa96d61a42a4</pre></small> |
| | | Full Location | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>198.6MiB (208.3MB) – 3,293,034 rows – 242 unique countries<br><small><pre>MD5: 688f39311d9ef3ae0dba52741233235b<br>SHA1: 52a53ef49218397baa93ef51035a1482140b4634<br>SHA256: e84aeb3244fc162911c5a436cc737fce85f6619f3e909a4b98b5ca4fa46ca9de</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>343.6MiB (360.3MB) – 3,013,737 rows – 250 unique countries<br><small><pre>MD5: a3926d0753e258e417a0b18a6d81430e<br>SHA1: 8a1946620f5f949f8a6274e1b473d30ae1b57025<br>SHA256: 2397151a392f426ac2facae01cfaa626480f5ad6d322c982304ec2b165ea38ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-03-22<br>IPv6: 2023-03-22 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.187MiB (5.439MB) – 221,425 rows – 243 unique countries<br><small><pre>MD5: dd82d9c419bdf8d65292298d4da9f4f9<br>SHA1: 4574ddf1c97bda6f9d825016c43005b9659612de<br>SHA256: 28145a84e26234645bd43bcf99287610ec6de00f1543d96a5704cdd74600303a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.81MiB (28.11MB) – 472,772 rows – 249 unique countries<br><small><pre>MD5: 5fc339accde85c2b539a6efba2f8b174<br>SHA1: 35049fccf4492a4eab673415d9814f7b38dfcea0<br>SHA256: 2715c4e3a5f98f963ebe5b71a0628cf1597145a8f1e82444d9831ad0d331ab50</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-03-22<br>IPv6: 2023-03-22 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.6MiB (195.7MB) – 3,084,645 rows – 243 unique countries<br><small><pre>MD5: dcf12cb26141a65ac67b7630b5a635b8<br>SHA1: d453ffc842be214041820c134dd85e2974ce8839<br>SHA256: ae02057cfbe60a4cb423459a4e23f7203890d02d5461ecef35d0ca43faf578ea</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>374.0MiB (392.2MB) – 4,456,315 rows – 249 unique countries<br><small><pre>MD5: f3c102f8b4597403f757f4f87811aa1d<br>SHA1: 5143d96442128020b6a91dd2476fbf46cff231eb<br>SHA256: 11e03efe2ac1e72afde73d94a354137049a2531581c610190c1b8ded4123c619</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-03-20<br>IPv6: 2023-03-20 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.925MiB (10.41MB) – 423,464 rows – 250 unique countries<br><small><pre>MD5: 57269a5e07b446938c73b0cca72e9482<br>SHA1: 93749b4037bf8dd697cd9c65a94de7773fe14d5d<br>SHA256: f34d1cc8f74615c38458f54a4edef08d771bb02825819e3dba6c7f3f993de277</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.42MiB (21.41MB) – 264,336 rows – 250 unique countries<br><small><pre>MD5: f05a32485000d69cffc8496233f7b2bf<br>SHA1: f677bfbeb62cca0c1ce433b9428802845be1f619<br>SHA256: 0eeda9f38df30dcf6f6e254b30e92cca49c22204e6f5faa743e1ea57f1e65555</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-03-20<br>IPv6: 2023-03-20 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.7MiB (198.9MB) – 3,780,037 rows – 250 unique countries<br><small><pre>MD5: b441b546c0f2ef16090af2957052de87<br>SHA1: 6476f47c9e4db6dd509ba9d2f636fea39fe241b9<br>SHA256: 87038b3cc98dc491addbaa1de68de39afe18a9bc153d0a300e288c73dbf9deeb</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.1MiB (232.9MB) – 3,780,037 rows – 250 unique countries<br><small><pre>MD5: 4a0d3ee8f9b732db1b3dfe8891ceae53<br>SHA1: 75b3c611f97abb202a1b31bc5522e4fd7083d237<br>SHA256: a2d68f0cce835b8413975bc68fd574a5833c4e9c38fa3a1a9e312aeffef35ef5</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.3MiB (205.8MB) – 3,780,037 rows – 250 unique countries<br><small><pre>MD5: 620da34247b3c08b7244c32032916d89<br>SHA1: d8e2c49d972808fd61971ff2ba0ccbdbaaf2c30e<br>SHA256: 07e08f98ca872906bdc3cf85f9684a778bfb15148e95c673d938ccd549d29ac0</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.4MiB (213.3MB) – 3,780,037 rows – 250 unique countries<br><small><pre>MD5: 052091d50cc23f1289395111567a2ed9<br>SHA1: 09c001c926b6899a220615d5eed494562b4bab19<br>SHA256: 0358ee07c97a5b77cb64b19d4c325b90fb9b7cbe6b8589da71e4e5fa01fcf795</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.3MiB (249.9MB) – 3,780,037 rows – 250 unique countries<br><small><pre>MD5: 13f16c2b134bd790acb6c6d9b9c3a4f4<br>SHA1: 8eb105aa81e22d7a77b5e7d141702aad352231f3<br>SHA256: 58345b4034786888ce04ed516be5f33346a48a3d3971f7678e76b9b49714a8f1</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.0MiB (200.3MB) – 3,780,037 rows – 250 unique countries<br><small><pre>MD5: bfd60f18b3103ff3b0aa6ca747f6b398<br>SHA1: 4b027b10b54b28a541d2aa260e2ceff38a058f88<br>SHA256: ff98901520a8876d45e96d10ac1053356ff40c9583753c89be100471d9fd77a8</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.3MiB (250.9MB) – 3,780,037 rows – 250 unique countries<br><small><pre>MD5: 48fef5c46691df0ff9c8e412b01ec626<br>SHA1: da696fe65d87fd19868bbed8bee30fbb173466e7<br>SHA256: a74f3a75bd6463320011f1b4ee6a99bba07aa64ddbf6849e8fc024aec228f862</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.2MiB (213.1MB) – 3,780,037 rows – 250 unique countries<br><small><pre>MD5: 581c3ad5685ec11d4bcef50480b632cb<br>SHA1: eb288e93fc44775a18019676506ef0d7f4a914a0<br>SHA256: f04c0b0548e118a28a0f1b333f42b3af8bbfb5d0bd8cd65a456c46163c6aa70c</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.7MiB (131.8MB) – 1,255,258 rows – 250 unique countries<br><small><pre>MD5: 64a59cb6a6afad39342e8aae9b979cf1<br>SHA1: 99d4155de1bfd318bd2a3e692c63305670e35fa8<br>SHA256: 6c3543d4df93ab117c543b3654c08bd0fe7367aa392ac80bcdb5225c3f91afde</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>133.8MiB (140.3MB) – 1,255,258 rows – 250 unique countries<br><small><pre>MD5: 46a009aca6d30be30f36b1275b740776<br>SHA1: e19d3629f887276f0865044142af1406b3cd9bc2<br>SHA256: e388deee5c5947c13240d875ca390614611826ef1b06574a72f4053eb46d260d</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.9MiB (134.1MB) – 1,255,258 rows – 250 unique countries<br><small><pre>MD5: 9e7b8566dfa376c334cb94a9403f2618<br>SHA1: 4e6d8f5c35441abb8121a4a2481f365c9d28fd2f<br>SHA256: 1555a153b5d14841f3965e13c85afe5ee3a51e1aede9a916a809ba0d9f117de5</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>129.8MiB (136.1MB) – 1,255,258 rows – 250 unique countries<br><small><pre>MD5: 54d7080819e9d1d08dd44b728dbc03dd<br>SHA1: 7c34a7dac26f927d6284b013adefa53c186695d1<br>SHA256: 8bfbe36915330f05971633e21e930dc7f693662df34e9d1f92b3d58b6b192edd</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>137.3MiB (144.0MB) – 1,255,258 rows – 250 unique countries<br><small><pre>MD5: 3e77402ea9711dafaea4196145c9cf74<br>SHA1: e4fe707838753d017c4c883ff3169165e26fe9c6<br>SHA256: c2865d6f7cb14bd465548934a81cd8cc43b881e576c00c6219d8b709d9471d7c</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>127.0MiB (133.2MB) – 1,255,258 rows – 250 unique countries<br><small><pre>MD5: 160f988bc7f75c11ef04f7e198618c56<br>SHA1: 724b79e4ed8fba386c9e8934ab691fb07fdef288<br>SHA256: 86fca21e4fd22c2e84ea4aaf8ea4394f2f270120f6b8b6a5597ab36529d0c704</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>137.9MiB (144.6MB) – 1,255,258 rows – 250 unique countries<br><small><pre>MD5: 69084c0ee25922319afd140ef07e01f2<br>SHA1: 6bf2cf3ceefa7f096be8a83b6e9bb1af5c33170a<br>SHA256: 147e2968415da58a9b1114eab781ecb128e5e3dc6e4ffb59d229fd3080c90ab2</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>130.0MiB (136.3MB) – 1,255,258 rows – 250 unique countries<br><small><pre>MD5: 12de7d0e828a2869cd425cb5bb5288c8<br>SHA1: 1998290c5c8fbb5136dae23338632a910a48a4c0<br>SHA256: 7f08eee7f0c42925102fd2765008527c021cbd7f24e3c22d00c31526ef32c620</pre></small> |


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
