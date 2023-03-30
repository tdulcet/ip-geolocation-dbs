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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-03-30<br>IPv6: 2023-03-30 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.138MiB (6.436MB) – 261,639 rows – 249 unique countries<br><small><pre>MD5: d8ea5dc28d96256d7f64bca3a99c3c6d<br>SHA1: 6dec64f66ed847db6d48ea70b94fde42f55ae4d4<br>SHA256: 6ac0930841f2f1f204c29c7d389cfbfe8baa74bb70183e6167c0d5d90b9b62fe</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.415MiB (6.726MB) – 83,041 rows – 250 unique countries<br><small><pre>MD5: cf704acc28ec4c73aedd8ff92559dea9<br>SHA1: f20c8a637ae2baf742ebef506d6a7c11285579c3<br>SHA256: cb92f264474d8fb3c5ca99f4e964825bfff613ff23807c384ce91e5350a6a6f0</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-03-30<br>IPv6: 2023-03-30 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.406MiB (9.863MB) – 399,511 rows – 240 unique countries<br><small><pre>MD5: e3b794f8ab860b1d4866e9f47e0657a6<br>SHA1: ca152f926607e4a8b6b2d4eafdfc98ab410b5f8e<br>SHA256: cee7b0bf20819f9148a378d36f6e8afc399464196de0c39abdde2f80d2e5d887</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.378MiB (7.737MB) – 95,612 rows – 221 unique countries<br><small><pre>MD5: 6eba1d0fc3afd164e3da63b46d70cc46<br>SHA1: e9138ff92b40fdfdeae65ac52f00d4a2872ad5e2<br>SHA256: 3c69f5ee7d8c03cee91fd61fc0d1e453209372ec4298e23c595da1fb48ac5064</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-03-30 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.67MiB (15.39MB) – 628,211 rows – 243 unique countries<br><small><pre>MD5: 81f4f55688995b34e4d7368f1e34f7c6<br>SHA1: 05e4805d92825dbf1d9133c6028ef610f5fafba5<br>SHA256: e678b2356713a3fe0454f89455f5208bb76e0d7e7e6f9957ceedff857e3e8598</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>31.40MiB (32.92MB) – 406,460 rows – 243 unique countries<br><small><pre>MD5: 8538401d644f9a90ae4088fdba1f8b7a<br>SHA1: b8650f303745e393f182404214f2cb86db72a097<br>SHA256: 0272a96f1bfbff3b3e96ff105e31ac6ac5eeeb395d18cd470b6ee8ecf4945d89</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>8.288MiB (8.690MB) – 354,199 rows – 243 unique countries<br><small><pre>MD5: a1d21d8f62a7c3f50510147c0eb79805<br>SHA1: cef8203b2cf2c56e2822c08c0550fc06171ce759<br>SHA256: 423c8d8cf8a614b4d9fb63c2a49616497a8cc0471c81db5ede712e2e6bc234bf</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>27.50MiB (28.84MB) – 355,992 rows – 250 unique countries<br><small><pre>MD5: 010e576eccbed46c235c9f1f40600f09<br>SHA1: f1295804bfa56f4fa5ef9842667b7cb0b9a0f0ef<br>SHA256: b07b46e8667f0b731e0478cb3dcaa3937b083138f4a8257cad27fa96d61a42a4</pre></small> |
| | | Full Location | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>198.6MiB (208.3MB) – 3,293,034 rows – 242 unique countries<br><small><pre>MD5: 688f39311d9ef3ae0dba52741233235b<br>SHA1: 52a53ef49218397baa93ef51035a1482140b4634<br>SHA256: e84aeb3244fc162911c5a436cc737fce85f6619f3e909a4b98b5ca4fa46ca9de</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>343.6MiB (360.3MB) – 3,013,737 rows – 250 unique countries<br><small><pre>MD5: a3926d0753e258e417a0b18a6d81430e<br>SHA1: 8a1946620f5f949f8a6274e1b473d30ae1b57025<br>SHA256: 2397151a392f426ac2facae01cfaa626480f5ad6d322c982304ec2b165ea38ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-03-30<br>IPv6: 2023-03-30 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.510MiB (5.778MB) – 234,959 rows – 242 unique countries<br><small><pre>MD5: 2bba27a2b99c35f4adfcdb1e3f2c3155<br>SHA1: 29a4b09cccca77c92d517cb4a7be4b66fafc3354<br>SHA256: b0df0b763ec5f15501f89a825dfa85b591361850246e30260d46c2498145ea2a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.42MiB (28.76MB) – 488,447 rows – 249 unique countries<br><small><pre>MD5: f754b5bde54b9a5d499f21e50664be91<br>SHA1: 638a2b52f5a21054aa3113b9a0b5d7cc9597443c<br>SHA256: fccdf823bfaa42d8f5e1b9338c57c955108fb976811a38544d113e9839da3beb</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-03-30<br>IPv6: 2023-03-30 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.9MiB (201.3MB) – 3,132,731 rows – 243 unique countries<br><small><pre>MD5: 3838c7e30ffdf6d0733a1183b8bc5f8b<br>SHA1: eabd91c83ed353e9c1772ef4c75790202a76b639<br>SHA256: 26f005f2f4c3afa282cd9a0622c8bbc26f7de72dcd77dedfa309adf8b89be8a0</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>382.5MiB (401.1MB) – 4,521,269 rows – 249 unique countries<br><small><pre>MD5: 84f8a06a23be4055c9018aad7e7e4024<br>SHA1: ff1af002a8f39309f8993c2c98f58478054f7550<br>SHA256: 0713b662001136ccee4d3f1c18f2c81c0615d7f3c0d2a1d536db02df4d676d78</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-03-27<br>IPv6: 2023-03-27 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.965MiB (10.45MB) – 425,162 rows – 250 unique countries<br><small><pre>MD5: a1dfa740ce65032d7ad68ff553a23440<br>SHA1: 90b9254f3fad3d9a66e8943ea98ce9058b9c34de<br>SHA256: 66b8fd78fc274c7929d4a6e828e7d83297e761a422562d6b62dfae8c8a69b3ee</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.18MiB (21.16MB) – 261,260 rows – 250 unique countries<br><small><pre>MD5: 99127b2b73f51b1960f6807c99763641<br>SHA1: 557fdf3b9941fe980341e4a8eb7e5b85e0b307e3<br>SHA256: 22260e18ede380dd4a08338d133d6c3a465e7acac5b40beae87fbb80a6fe920e</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-03-27<br>IPv6: 2023-03-27 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.2MiB (198.4MB) – 3,771,824 rows – 250 unique countries<br><small><pre>MD5: 89b6751d6886663b8e575a5b1db10a19<br>SHA1: d90963f6a73684c7e484603aa566643e71258795<br>SHA256: 2f00af5c87e4a83a1f1cba920e492052cb92956ba794fda6b8b201259ed1a2ed</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.6MiB (232.4MB) – 3,771,824 rows – 250 unique countries<br><small><pre>MD5: 9d65dbfb743850c017bc86cdc7c8b765<br>SHA1: 2711018fa12cf8d504e3841bf0131d87c0db4267<br>SHA256: 5a6222eb9ddc040baeffbb4035e4a0dd6ca1035e1acface94543c61e888c5861</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.8MiB (205.3MB) – 3,771,824 rows – 250 unique countries<br><small><pre>MD5: 8cd9b064f9174474ffa66ab7e266fac7<br>SHA1: 5c482f8336f6f0fdbbed57598c4e2c8ae43ddff0<br>SHA256: 65f9219ffb3799c92649de9e16a163a9eac10978b07080ce9190ad325615c7db</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.9MiB (212.8MB) – 3,771,824 rows – 250 unique countries<br><small><pre>MD5: 5249b19e9b68452481ce1638bbba538f<br>SHA1: 425efe97fc2680378a2ef9478d6fdd2d07a400bc<br>SHA256: 7c0c0d861782340d88f4e780e040fcfa183b0150100ffc19b14c04530dfe90f0</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>237.7MiB (249.2MB) – 3,771,824 rows – 250 unique countries<br><small><pre>MD5: 5e6276702551dd3e5741440826029020<br>SHA1: f97c352cb6d5fdacec24da5009d21ff0216de58a<br>SHA256: 2f793933e72efbcffefc57abd2309d0cf47808a0213512dd2b74b9bf68d422c3</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.5MiB (199.8MB) – 3,771,824 rows – 250 unique countries<br><small><pre>MD5: 546f4ac793ccb664033b4b6938efd2fe<br>SHA1: 7bf8fa9500327848feefe39b1c090098419d0c8e<br>SHA256: 65030c78c2367d703f0c9bfc6d1a733dadba81fccacc4d212d89e3143baaa877</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.7MiB (250.2MB) – 3,771,824 rows – 250 unique countries<br><small><pre>MD5: c4e6405b35f96127bfce4e10f9c4ee60<br>SHA1: 64661fdaf4ceac53fbcff3251db8bbf4601ee3b5<br>SHA256: b80cf83c0ac5c8c896490974ee427edc3532429c3dbe20d3442faf9aa2d31599</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.7MiB (212.5MB) – 3,771,824 rows – 250 unique countries<br><small><pre>MD5: 178705a77b080f9ccf9c58337b93808a<br>SHA1: 63ec942ba3f6e3302aed0b0ab4c2606a0d429824<br>SHA256: 942a3b46935da9e031b8dfcfbb825ee667d7444857fb8ce541d08716f4781841</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>123.2MiB (129.2MB) – 1,230,733 rows – 250 unique countries<br><small><pre>MD5: 45b12f48bdd3180d2d1794ede224fb57<br>SHA1: 69f70213819ad58fae906444fa1fd5a71038cb52<br>SHA256: c26541fab98ba3b6574920ac32503d8ce45654697f4b54f10b37dd9a8774aae0</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>131.2MiB (137.6MB) – 1,230,733 rows – 250 unique countries<br><small><pre>MD5: 4a2edf2b691568d09425da0352dbad0d<br>SHA1: 84637bfe5a7bee10d5cadfd0c96d5cedb96abc65<br>SHA256: 86d5d90860b534c4ccbb90499fe03b3cc095c4902ce5ba4858214c748cc8cebe</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>125.4MiB (131.4MB) – 1,230,733 rows – 250 unique countries<br><small><pre>MD5: e9b11dc3e6ce817d3610309891638b2f<br>SHA1: 25da225fc32fcd913d2059b58645054ff57eca4a<br>SHA256: 21825a3dd1f0bda8e6ddab351e83d2b5eb209c1c6be5c9de698b3caa22d40c3c</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>127.3MiB (133.5MB) – 1,230,733 rows – 250 unique countries<br><small><pre>MD5: 5739605a1d62b6c08408728ba4b96fe0<br>SHA1: 080bd6c27336b08a9d587805ad43b1d36576d3b7<br>SHA256: 7112288266cce1aee2da184ec2bbc8c4e5b9d689ef53d729f54c35492184db68</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>134.6MiB (141.1MB) – 1,230,733 rows – 250 unique countries<br><small><pre>MD5: e6d3dd0a3cf983e7759b957458ff51f1<br>SHA1: df9330e9aaa5a312dedf3e6fc01bf10dfd409cc8<br>SHA256: ceb83a3b760896befa6a1e9ae091b0d99aba4e7113f02390f7b137b7320ebf69</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>124.6MiB (130.6MB) – 1,230,733 rows – 250 unique countries<br><small><pre>MD5: 5198a9c6cf800672967143c159b0552d<br>SHA1: b7a2fd6b6f05311c03f08799bf584d1b0aa3a25c<br>SHA256: 3c26bf57399e4ac46b2083d57f28cdbcf8c2b382e199eef2159452a6463a6768</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>135.3MiB (141.9MB) – 1,230,733 rows – 250 unique countries<br><small><pre>MD5: d4d26837d86712b38f02ce03868e5fd5<br>SHA1: 29b1e961103b672f473fcf3743050dd7614696db<br>SHA256: 13064c18e439e3fb0a899a2c11d850f67187954d2122bfe2da3805a75b3e6547</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>127.5MiB (133.7MB) – 1,230,733 rows – 250 unique countries<br><small><pre>MD5: 7f95a8d55bb5fbcce5f6e148aeaa0a20<br>SHA1: ec9cd1e3667f96ba504ebcb0572218c513217795<br>SHA256: 3422c20488c2aa8d0e2a9b940ee9044218d897c67c9aad5d1338b4b8e2db5c1b</pre></small> |


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
