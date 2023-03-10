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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-03-10<br>IPv6: 2023-03-10 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.143MiB (6.442MB) – 261,885 rows – 248 unique countries<br><small><pre>MD5: 112a2c17bf1dc42697f6860073dd1af1<br>SHA1: 9e8f369975299457d0be11e47f9d09c34a86bfcd<br>SHA256: dda9aeb0415b6d990a0fb78ae0e2b03a6521906bacd31b94129e778659b0163f</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.365MiB (6.674MB) – 82,395 rows – 250 unique countries<br><small><pre>MD5: 093fe2b0607a14f6b4396dcc70b53a93<br>SHA1: cf7cf01d4963afcce03fb0b12b7c894ff0b1f426<br>SHA256: 01a79e869d9fb57914b43fad8a99ac67619670d4ab5189a1805baf021a334fc8</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-03-10<br>IPv6: 2023-03-10 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.409MiB (9.866MB) – 399,789 rows – 240 unique countries<br><small><pre>MD5: 4bb2074effb1c1111746500c20aa4de5<br>SHA1: ef1e8a804ce939de6c27161b642a49ee4b0076a5<br>SHA256: 9d1c20c42aba832455c2f48f9ad8e9650b7488693f598bce1f432e0b43aba4dc</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.280MiB (7.634MB) – 94,349 rows – 220 unique countries<br><small><pre>MD5: d586eb8bdb0d36c8863a6ea4f9647525<br>SHA1: 798da258a11f733e87d60e83f9f951287337a57d<br>SHA256: 34d26ee2016f320a073477074dac470961e792fac3d46137b526058436d74040</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>8.288MiB (8.690MB) – 354,199 rows – 243 unique countries<br><small><pre>MD5: a1d21d8f62a7c3f50510147c0eb79805<br>SHA1: cef8203b2cf2c56e2822c08c0550fc06171ce759<br>SHA256: 423c8d8cf8a614b4d9fb63c2a49616497a8cc0471c81db5ede712e2e6bc234bf</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>27.50MiB (28.84MB) – 355,992 rows – 250 unique countries<br><small><pre>MD5: 010e576eccbed46c235c9f1f40600f09<br>SHA1: f1295804bfa56f4fa5ef9842667b7cb0b9a0f0ef<br>SHA256: b07b46e8667f0b731e0478cb3dcaa3937b083138f4a8257cad27fa96d61a42a4</pre></small> |
| | | Full Location | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>198.6MiB (208.3MB) – 3,293,034 rows – 242 unique countries<br><small><pre>MD5: 688f39311d9ef3ae0dba52741233235b<br>SHA1: 52a53ef49218397baa93ef51035a1482140b4634<br>SHA256: e84aeb3244fc162911c5a436cc737fce85f6619f3e909a4b98b5ca4fa46ca9de</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>343.6MiB (360.3MB) – 3,013,737 rows – 250 unique countries<br><small><pre>MD5: a3926d0753e258e417a0b18a6d81430e<br>SHA1: 8a1946620f5f949f8a6274e1b473d30ae1b57025<br>SHA256: 2397151a392f426ac2facae01cfaa626480f5ad6d322c982304ec2b165ea38ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-03-10<br>IPv6: 2023-03-10 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.187MiB (5.439MB) – 221,425 rows – 243 unique countries<br><small><pre>MD5: dd82d9c419bdf8d65292298d4da9f4f9<br>SHA1: 4574ddf1c97bda6f9d825016c43005b9659612de<br>SHA256: 28145a84e26234645bd43bcf99287610ec6de00f1543d96a5704cdd74600303a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.81MiB (28.11MB) – 472,772 rows – 249 unique countries<br><small><pre>MD5: 5fc339accde85c2b539a6efba2f8b174<br>SHA1: 35049fccf4492a4eab673415d9814f7b38dfcea0<br>SHA256: 2715c4e3a5f98f963ebe5b71a0628cf1597145a8f1e82444d9831ad0d331ab50</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-03-10<br>IPv6: 2023-03-10 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.6MiB (195.7MB) – 3,084,645 rows – 243 unique countries<br><small><pre>MD5: dcf12cb26141a65ac67b7630b5a635b8<br>SHA1: d453ffc842be214041820c134dd85e2974ce8839<br>SHA256: ae02057cfbe60a4cb423459a4e23f7203890d02d5461ecef35d0ca43faf578ea</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>374.0MiB (392.2MB) – 4,456,315 rows – 249 unique countries<br><small><pre>MD5: f3c102f8b4597403f757f4f87811aa1d<br>SHA1: 5143d96442128020b6a91dd2476fbf46cff231eb<br>SHA256: 11e03efe2ac1e72afde73d94a354137049a2531581c610190c1b8ded4123c619</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-03-09<br>IPv6: 2023-03-09 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.876MiB (10.36MB) – 421,371 rows – 250 unique countries<br><small><pre>MD5: 41c4a965df80772f1c8fe6380160ffeb<br>SHA1: 45062e1c3dcce22cf6a02490f94a58b0a1ecc358<br>SHA256: d74a3ba464428da1d4a7805e6b1765fecd1157727ee45ec54b2f15261b17791b</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.05MiB (22.07MB) – 272,465 rows – 250 unique countries<br><small><pre>MD5: f91b105cd28067c521535b6586c05e2c<br>SHA1: a7863a0472e4050175d142716219cd9a40403151<br>SHA256: 5dfb597f751eef7016cbf27115d5da63fcc5ff06ede9a676b1a3a09a0be8bbae</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-03-09<br>IPv6: 2023-03-09 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.0MiB (199.2MB) – 3,785,968 rows – 250 unique countries<br><small><pre>MD5: 32e4fd92f8d87603c314791cd75faa7b<br>SHA1: 48188dafa939ed97ade4fd2ccdb3df0dc8a5cb18<br>SHA256: a3bb90ec4105569363966a8a4667a18d3f634bc42be146c42cacd52b859292cd</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.6MiB (233.4MB) – 3,785,968 rows – 250 unique countries<br><small><pre>MD5: 959f921742d533b093c7bc5b58d89c03<br>SHA1: 984f9ed5f80ee1cd0783d595770e13aafe37c0f5<br>SHA256: b2c51f016380cf6ee3587ae9b1670b1c07d8dd54159719bbdc1ca66f08dbe2d0</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.6MiB (206.1MB) – 3,785,968 rows – 250 unique countries<br><small><pre>MD5: a980a9a2486272976cea92c39a33d713<br>SHA1: 78e9a0a0554180b400490fba336735778dd4b06b<br>SHA256: eddf5eb7e7bb086e75e8c200370366bd5c699fc1e82e6d3ab65dfdf069553b0a</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.7MiB (213.6MB) – 3,785,968 rows – 250 unique countries<br><small><pre>MD5: 3683415e63ec9bbfb1d58b265d7ffb69<br>SHA1: a2539f32e4d61aa7e1febdcad18554649b12155d<br>SHA256: d9452d920781c2b8312c5ed250eb0813361097789e99dc99f63248e2c1436f54</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.8MiB (250.4MB) – 3,785,968 rows – 250 unique countries<br><small><pre>MD5: a8b60faa1c475e3366c85b60d3560066<br>SHA1: 749d26d0967d9aac729243a63dba80de43bb70d3<br>SHA256: 686e76778b50ac7668dacbef68d41f716c8648ad969055cd4a79ab8fa8a33941</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.4MiB (200.6MB) – 3,785,968 rows – 250 unique countries<br><small><pre>MD5: 6de945111c9ac7a3d2fc11da4126b10b<br>SHA1: 5508b4114e48de6133f672f3f5d37f4b66b55156<br>SHA256: 0032a0d27e47b734dfe3bdfc4eb28a5d7942db0b40723075a0ee9f4e54035267</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.7MiB (251.4MB) – 3,785,968 rows – 250 unique countries<br><small><pre>MD5: 9ec663e972898de573159586b72e0441<br>SHA1: 2754a239e163b0c6fa695ff48ed9a59f2de1edf7<br>SHA256: ee0fd3d7dc9cbaf4a616da4df6985db74fb911813eabd01e490d2af45aa707a0</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.6MiB (213.5MB) – 3,785,968 rows – 250 unique countries<br><small><pre>MD5: 956d2966fd7f5a74d3da7f91f24b20b2<br>SHA1: 0e37f33bd320d2fd536902b54f9d1bea2253bdbb<br>SHA256: 0b2d03d0708043a8557aadee6b503d46a8a4a8fdb37b2f67b8a8670efa97b6f6</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>124.9MiB (131.0MB) – 1,248,360 rows – 250 unique countries<br><small><pre>MD5: 6df19a062ab70c25afb0c5da6b060278<br>SHA1: 0ff074828c3b07632417cde69ef81ef8edce16ea<br>SHA256: 19fa68cbb00e036b2e6e1ef0abbd46dafd1cea3e77e27568d49e4226b6e3f8ad</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.9MiB (139.4MB) – 1,248,360 rows – 250 unique countries<br><small><pre>MD5: a114b0f8335d307c0a61dc46088c8622<br>SHA1: 25b83395f418ef62523e6c870ce9f2ae023fc0c3<br>SHA256: 151a89e23ff438a258f4102c0b1d9d5f6bb6f0b5f1f2463b8468b9ffe8afaf77</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.1MiB (133.3MB) – 1,248,360 rows – 250 unique countries<br><small><pre>MD5: 00834d6de04f8acc578a7587bb50fa4e<br>SHA1: 3f435b0aab15f7019656d0ad587a4208e581fb15<br>SHA256: a3eeaae60dab9e50a48c9ea568d94309bfaf9093e2cf13b0bfd19c6ac8f15fc8</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.9MiB (135.2MB) – 1,248,360 rows – 250 unique countries<br><small><pre>MD5: f70434966f25582b13909ac4b464c9b9<br>SHA1: cc73c345074974c1a9aa82c2e67f66e6fa54b913<br>SHA256: 76d33ff5c7e5c45fe1e469f29ad61f18ac0d74425b4ce0b25cc6ffa3a65db69b</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>136.6MiB (143.2MB) – 1,248,360 rows – 250 unique countries<br><small><pre>MD5: 25131375353fa299bf286a14b3257243<br>SHA1: ecab3525f6554b22f11859567a07f18eb9358129<br>SHA256: dfecfee6155bd8bfee67d5e6d50c67476c92c2d382daa3fe808eab628d08ffcf</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>126.3MiB (132.4MB) – 1,248,360 rows – 250 unique countries<br><small><pre>MD5: 6161918160658acf3e0e218a4bd58108<br>SHA1: e946ce80c784186afe0497396fb6faed580e42e1<br>SHA256: 4455bb7db46720708096ffa940c96fa5396861537b988543b62ba6d20f2d5e42</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>137.1MiB (143.8MB) – 1,248,360 rows – 250 unique countries<br><small><pre>MD5: 5892f5290fc477514d95e3d9b19ee9e6<br>SHA1: bf37f8f6c11dee1747499a4a2b76111653d37482<br>SHA256: ee97a1dc6e3864c1cb1f883b77907e02503ed89921da1e57f458e4370dc89358</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>129.3MiB (135.6MB) – 1,248,360 rows – 250 unique countries<br><small><pre>MD5: 496f98202f53c75c20012bd8955e2712<br>SHA1: 489991bf5cc4de28f1ef315a976b96a82013cb13<br>SHA256: 4eb1ca0794e87e0d807a3d59ed6ca9524f71f18ec2dabd680b54b29825a05cff</pre></small> |


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
