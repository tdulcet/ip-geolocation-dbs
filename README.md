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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-05-01<br>IPv6: 2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.131MiB (6.429MB) – 261,318 rows – 249 unique countries<br><small><pre>MD5: bd43795f5cdec5d1a5b09ce150349032<br>SHA1: e99bbc58327d4c808cd7a19043c67ec8952eec26<br>SHA256: 2d3cacae6b6aec344746576cf1804bf285c68f4628845d60e7569594a503a966</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.526MiB (6.843MB) – 84,483 rows – 250 unique countries<br><small><pre>MD5: 64e250f7fb82d2cbf48bc17e092feab2<br>SHA1: 09fbea815233db89af501328697891c8d9f3b9fe<br>SHA256: 6bc732bb87739987ef01bb00c089dda745c72fd950df930006f07df71d96c91c</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-05-01<br>IPv6: 2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.469MiB (9.929MB) – 402,224 rows – 240 unique countries<br><small><pre>MD5: 5d85a8a9ad13397eadce6c27b944a354<br>SHA1: 693a2b53d371a75c49849e843a9541a327d8e6f3<br>SHA256: 620286450f72d86757617a27a242c59825f520d932e03f6fcb9e48d67d2db764</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.438MiB (7.799MB) – 96,379 rows – 221 unique countries<br><small><pre>MD5: a4f04f65f9e7ed57a372816e0c49af9f<br>SHA1: ce3881a58c65925c5d1104f1c5355d9949796f47<br>SHA256: 421942faee9174eea2e7fb4bb615406323d5bcc4d5aa19a0bc5018e713afd0d6</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.86MiB (14.53MB) – 591,276 rows – 243 unique countries<br><small><pre>MD5: 397b5e62ad1d819a9031d996868f6fbb<br>SHA1: d9679cfb60ef4152a43f62ebde19da62e9ee23ad<br>SHA256: 49caf560dbf6a20cf33ebfb5bae67e5c9e7d6067e826c9b24f00c46f8258dd06</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>25.72MiB (26.97MB) – 332,965 rows – 243 unique countries<br><small><pre>MD5: ec671ab253917d75dec70adf33114b0c<br>SHA1: 5c5bc0c21bf454bc3f397a04c4829fb6cf9176d9<br>SHA256: 45873d976c06258265f0e17f1c5074df0839e6448c62da8290648bd06394a65a</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.198MiB (7.547MB) – 308,140 rows – 243 unique countries<br><small><pre>MD5: 00b451f6412173581a7ba389f444f7b8<br>SHA1: 3581ae37ad536ccfc344035fac8da366e6f2a1c3<br>SHA256: 2632d03fe402810c0a5cd21cb01657e4bce6686f9a35a911a634e00376fe4fc8</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.40MiB (26.64MB) – 328,845 rows – 249 unique countries<br><small><pre>MD5: 6bb8a68614ae30eed99e534875572642<br>SHA1: 0ee22a19afac3f9a7cbd864af67674fe9cfc6161<br>SHA256: 7d06dc68c40737d45ad6dc84897a8b7371ad05211dc7716db73e16c197236656</pre></small> |
| | | Full Location | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>194.0MiB (203.4MB) – 3,206,976 rows – 242 unique countries<br><small><pre>MD5: 4ab320aa3a48e3e999f3451fbc5a2da8<br>SHA1: 0edbe11a0f197414c336d93dce71b581d19cd274<br>SHA256: e618d8745b11f6aff0dcb8f824c7f141c7fe734243d064f5f1fd7a093e46c571</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>365.9MiB (383.7MB) – 3,189,651 rows – 249 unique countries<br><small><pre>MD5: c56df0a8c49cfc4fafc1dd0e0ea9177e<br>SHA1: 5e57dbd6ea1ad42ff4e411c9606c8f23cb91e70c<br>SHA256: 78e7ce4abf723db571f358a92321ca5b197405f36485132b7deb8c48d31a8d5b</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-05-01<br>IPv6: 2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.555MiB (5.825MB) – 236,860 rows – 243 unique countries<br><small><pre>MD5: ed3a236afb3c81be58fd9e618311f040<br>SHA1: c2f909455631207019aaab2b2e46e900ebf570dc<br>SHA256: e9f4b3ba35664fef476b681b4bf974f40a7c2605e7528a86ad8bd7ec533ad95b</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.56MiB (28.90MB) – 491,350 rows – 249 unique countries<br><small><pre>MD5: 24b4cca038e3d4dcc0f42da6244a3a35<br>SHA1: 2621cb133d2002e631b0adbef75d4ea6e931756d<br>SHA256: cc4498b24a37bbe633f6502d077cf044fd12484833daf07542118c9c7c386bc1</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-05-01<br>IPv6: 2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,146,282 rows – 243 unique countries<br><small><pre>MD5: 88c13dfb1a052516749e7ea3a9487650<br>SHA1: 2e306a30fccb8fc193e5dd6bca9c2dc9b66b74eb<br>SHA256: eb792a298ee49d197c826b29bf481ad1c08529aa3138b1265dc37736edb20adb</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.6MiB (400.1MB) – 4,518,262 rows – 249 unique countries<br><small><pre>MD5: 7fdf49f6825c8d2c6839dbb6a75d33b8<br>SHA1: b3e158802b17935c7869bba17ff348eb8c749c91<br>SHA256: 5b247134a6e2438ebad87181e14b376f714b23fa9c8ca69d358366ad0778806a</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-04-27<br>IPv6: 2023-04-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.645MiB (10.11MB) – 411,234 rows – 250 unique countries<br><small><pre>MD5: 302d06ba970fd766007b4952d35e5541<br>SHA1: ef3ca40e213dd9cd456c977f9f885b9f872dda48<br>SHA256: dfaa6ba1e0dd4c9b27eed64afb648780d3ce9d7f639b39601b03faf8df3b4c12</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.11MiB (22.13MB) – 273,258 rows – 250 unique countries<br><small><pre>MD5: 5b454599947eaa61264e19f017b66259<br>SHA1: 21013e1e74bbb992e46d8dde5662f1ff97edc655<br>SHA256: 7e9f9848e80c89234734f63227490e0fffa759294f03399cfc7e2c517d4f960b</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-04-27<br>IPv6: 2023-04-27 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>191.0MiB (200.3MB) – 3,799,896 rows – 250 unique countries<br><small><pre>MD5: 1518e1604889f859d547570ca6c11fa0<br>SHA1: fee8b6614b4c5abe57b265ef32615dd8a97eff13<br>SHA256: 2b6c912587ace4508e79486f71ae5ee71af7e2b2c89a26dc0e8f1f86f7c091fd</pre></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>223.9MiB (234.7MB) – 3,799,896 rows – 250 unique countries<br><small><pre>MD5: 7a0b5005bb6f9059c7c759a98e767af9<br>SHA1: fbb9eefd144019d4c920da826c83fa5630f45265<br>SHA256: d8f515e3455735688d051609b191d7226fa80e27ef85de40ea46326016069723</pre></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.7MiB (207.3MB) – 3,799,896 rows – 250 unique countries<br><small><pre>MD5: 19a11e42c2ee2a80ac5fb983432eb470<br>SHA1: ecca48c2af8a1d6ab6a49f8e7a184d26d5b5f282<br>SHA256: db25c8ff17e834fc0c0402fd81ee175a1b8f2101dfc53e8a66a26f3032129e47</pre></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>204.9MiB (214.8MB) – 3,799,896 rows – 250 unique countries<br><small><pre>MD5: 9d8f49f6d2fd9d7802e9d8896b6c069e<br>SHA1: 8c4f00bb7e8215013ecd995f6a38df9d34f2f6ab<br>SHA256: 010dbc6bc07fedeeb79ee5b456b1294b0b88bf516482a6b4f6a0cfb63faf44aa</pre></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>240.2MiB (251.9MB) – 3,799,896 rows – 250 unique countries<br><small><pre>MD5: 58d3a33175103875653d97d560229996<br>SHA1: 057591501acef7b1a1ebe5439f648c9bb2d1a39f<br>SHA256: 161173a173345359344511d35a4ba344abb024c99c949255504cad3d22c2ba60</pre></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>192.2MiB (201.6MB) – 3,799,896 rows – 250 unique countries<br><small><pre>MD5: a2c7ca6e90303b68a597d1b5bf71cc32<br>SHA1: 0387e936afeac918ce3b444dcf5363d41cd3515d<br>SHA256: 58685741cb61360ea542e1a2755fd0e09479b31f9fc55617e3f24439367bd4db</pre></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>241.1MiB (252.8MB) – 3,799,896 rows – 250 unique countries<br><small><pre>MD5: ace3d3713af245acb11808ad348d314f<br>SHA1: a8fc1f7087d9df74f380f7930780c3c20c8a3bb2<br>SHA256: c74491d751be81f33d992815492a3b6fde04d06fa728b5b06cd4db74bb220fd4</pre></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>204.5MiB (214.5MB) – 3,799,896 rows – 250 unique countries<br><small><pre>MD5: 8b6f36ed6cd1ec7f48cdbfb1ee42cb60<br>SHA1: afcabf131bfbdca18258191848372010a2f78a99<br>SHA256: b17edad2a62972c1168047452207c14448db101b14d1544afa8382295a504e4f</pre></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.6MiB (134.9MB) – 1,280,076 rows – 250 unique countries<br><small><pre>MD5: 9398b58b9e0e26bb69d78d6bdd0ccd8e<br>SHA1: 6405215eba1a167dd8be3b718e12ea42afa0cafa<br>SHA256: 6af4cf7bb008f9aa301b727c665ef3205a33a3b347baec14ed63a2c3ec0daea0</pre></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.9MiB (143.5MB) – 1,280,076 rows – 250 unique countries<br><small><pre>MD5: 7e57ea8cdb9a2f4cc276921ad9f0f810<br>SHA1: 26814f9ed1e5c686f04b2753d04ca5dde116c039<br>SHA256: 302393f65ef4ffe6e06598476d50392bb7752259e34ad4f900a11a9f93cd7211</pre></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.0MiB (137.3MB) – 1,280,076 rows – 250 unique countries<br><small><pre>MD5: 53c11cb113f1894613344db5a9e785fc<br>SHA1: eded1b2e57bca26e833dc770e8aea194e631936d<br>SHA256: 3daf44491f4a13993fd5e9d80240991c7b0b0c32696c4f85806c41aa0d2cb881</pre></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>133.1MiB (139.6MB) – 1,280,076 rows – 250 unique countries<br><small><pre>MD5: 0de12b0d4db35e31970b38d4094def7e<br>SHA1: 0d466419847e944d4515ce1a0b2aed6fbeeb230c<br>SHA256: d07ea65dd68a948cbff99b067f9fe72132e0d0d7eca8b85adc1c7e61ed2b2af4</pre></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>140.6MiB (147.5MB) – 1,280,076 rows – 250 unique countries<br><small><pre>MD5: e001c279019201c1a4b701821249e095<br>SHA1: 32f755aa8a55c330beff2daeae94f442237a1960<br>SHA256: dc8987e5b74882f01bb5421eabdb85c351732907c82f22a876cd2757d9f4261a</pre></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>130.0MiB (136.3MB) – 1,280,076 rows – 250 unique countries<br><small><pre>MD5: db898f03e0751acb60a95554932b6f2f<br>SHA1: fe8e0a2996fea564e7d349e762619a1aeae98c07<br>SHA256: cb5e48175f748b15e3a9acf73f23a8f688179b77d42922d43008c28380c9efe5</pre></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>141.4MiB (148.3MB) – 1,280,076 rows – 250 unique countries<br><small><pre>MD5: a8378c22bf9a6059012bdeb0a502248f<br>SHA1: c235fa767b5574d8db7de3be8be11ae0e7330b16<br>SHA256: d9ce134cdfda8c6ba7ba0640397e028d88024d50daed3d9eb7379f7ba94a0a93</pre></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>133.1MiB (139.6MB) – 1,280,076 rows – 250 unique countries<br><small><pre>MD5: 8771f27deaeb98122bf3fd68239e6cb2<br>SHA1: f2345fb87c4e79163a9d17e666e743355f7bb0f4<br>SHA256: bd019d6f5b8cda0015a633ca276c5f36064e0d41b12f2b0c35c5d860846b7daf</pre></small> |


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
