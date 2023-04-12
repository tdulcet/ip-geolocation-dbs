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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-04-12<br>IPv6: 2023-04-12 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.133MiB (6.431MB) – 261,403 rows – 249 unique countries<br><small><pre>MD5: 6a33f9df6232679f53b184cbaff9d37f<br>SHA1: f015877a3c6347fa880d60904b31be73da879095<br>SHA256: 3fe27fb79ec4ae0c822a846629fa35b13a2d896cac1909d1e8e6f91abb986465</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.483MiB (6.798MB) – 83,920 rows – 250 unique countries<br><small><pre>MD5: af3a1f541a168cbefd002ae82a9cae19<br>SHA1: 9284c245cd811a3d901aedf8dbe3bafce7762ad7<br>SHA256: 1c52cf56b7b96d0f06b83f09888cf03d5a8dc7fe7c3da5789703293fc15b844f</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-04-12<br>IPv6: 2023-04-12 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.454MiB (9.914MB) – 401,567 rows – 240 unique countries<br><small><pre>MD5: 66e567af027ec74757c3373d96a7c4ef<br>SHA1: 8bc2be324f67d563e19449d7cf1d4138db9f324e<br>SHA256: dcaa8bfcb775fe5eb4b5cb938f5c6df331b36e0b29e48dd0d0d831e114421a81</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.414MiB (7.774MB) – 96,071 rows – 222 unique countries<br><small><pre>MD5: dadabc37bfd5726584e56dee6995e19e<br>SHA1: 5d181a33bf529ef30ef1efb03b880cccce61e0c6<br>SHA256: df5f11fe83b09065525bb89d46a23a24817d65ce99b5b08d8f8099c402b44817</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-04-12 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.49MiB (15.20MB) – 621,142 rows – 243 unique countries<br><small><pre>MD5: 29c298b4269dd3b533b3b82ccfe19ba9<br>SHA1: 78ed0bfee2acb13488adbc1b092396f05988a02b<br>SHA256: 759ccf1d55c667333bfe5b882aa5da276e0e4a34bb594c59148c622baa1283fc</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>26.74MiB (28.04MB) – 346,112 rows – 243 unique countries<br><small><pre>MD5: 74ac67bf09a64330829e0ed2e71feb14<br>SHA1: f04e7f6eee8120d2d9849e1a71aae7aad2a04ada<br>SHA256: d50bc35ec3f79517dd2f93ba4be285266a9642e61a44c1475af9092504eaa19f</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.287MiB (7.640MB) – 312,180 rows – 244 unique countries<br><small><pre>MD5: 82354007656a327ea105907215d25ef9<br>SHA1: 67c794d1cec36d4b28bd7f519d16aaede697f7ae<br>SHA256: e4c6fbd5351ce06786a1a23d60f3cc152422ad29e1b7c48c0624da9761235e6f</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>21.32MiB (22.35MB) – 275,943 rows – 250 unique countries<br><small><pre>MD5: 4eec116f3dc312fbd1a82887804d6bed<br>SHA1: b2a486ba182d709c41684790f72cda40e767d382<br>SHA256: 1257bb248ef1d074a0a6abe23f9c54440744b5a8f37d6b2aca1e030d311dc9c2</pre></small> |
| | | Full Location | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>197.4MiB (207.0MB) – 3,267,813 rows – 243 unique countries<br><small><pre>MD5: 45d3670da1f2b31fcb68223a108be9af<br>SHA1: 37645fbeac5800a4ef57d4ce635fa5daa67ed21f<br>SHA256: d615d7817a3bbfdd4665c3bfccae8e6ae223c388323467fed143ca963313c64b</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>372.5MiB (390.6MB) – 3,244,362 rows – 250 unique countries<br><small><pre>MD5: 8aab3f0628a16d3290e30da4f527f4c8<br>SHA1: 19582f830e1b7052a98ed03d839aa97944679064<br>SHA256: 83e1d01ad2c49822595fcee1ca7abb10ae1c64dcd0ada5dff55cd46aa9ccd7ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-04-12<br>IPv6: 2023-04-12 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.510MiB (5.778MB) – 234,959 rows – 242 unique countries<br><small><pre>MD5: 2bba27a2b99c35f4adfcdb1e3f2c3155<br>SHA1: 29a4b09cccca77c92d517cb4a7be4b66fafc3354<br>SHA256: b0df0b763ec5f15501f89a825dfa85b591361850246e30260d46c2498145ea2a</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.42MiB (28.76MB) – 488,447 rows – 249 unique countries<br><small><pre>MD5: f754b5bde54b9a5d499f21e50664be91<br>SHA1: 638a2b52f5a21054aa3113b9a0b5d7cc9597443c<br>SHA256: fccdf823bfaa42d8f5e1b9338c57c955108fb976811a38544d113e9839da3beb</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-04-12<br>IPv6: 2023-04-12 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.9MiB (201.3MB) – 3,132,731 rows – 243 unique countries<br><small><pre>MD5: 3838c7e30ffdf6d0733a1183b8bc5f8b<br>SHA1: eabd91c83ed353e9c1772ef4c75790202a76b639<br>SHA256: 26f005f2f4c3afa282cd9a0622c8bbc26f7de72dcd77dedfa309adf8b89be8a0</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>382.5MiB (401.1MB) – 4,521,269 rows – 249 unique countries<br><small><pre>MD5: 84f8a06a23be4055c9018aad7e7e4024<br>SHA1: ff1af002a8f39309f8993c2c98f58478054f7550<br>SHA256: 0713b662001136ccee4d3f1c18f2c81c0615d7f3c0d2a1d536db02df4d676d78</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-04-10<br>IPv6: 2023-04-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.564MiB (10.03MB) – 407,682 rows – 250 unique countries<br><small><pre>MD5: b04f7b641c20bc973b475282dd1b43c5<br>SHA1: f2b1534e57ff820c83167f8d87e9a4f11065feba<br>SHA256: 2dc7f76c6b594f53d990bd691bc66637c63c1f9ae37971b8d4467626e18382f4</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.80MiB (21.81MB) – 269,232 rows – 250 unique countries<br><small><pre>MD5: 4367eb9bcfda5372f15727064226444a<br>SHA1: bf1ef9d432b8560cd65c9fbed42377be5f6b3e1a<br>SHA256: cde6d1d51efd1879e707e89d8db0e7b12721367227f218ba37c24c5f2fa41515</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-04-10<br>IPv6: 2023-04-10 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.9MiB (199.2MB) – 3,777,698 rows – 250 unique countries<br><small><pre>MD5: 5e230a25e55f49826f4606ef78002f89<br>SHA1: 9e95d6b34ddf3307d2ecc21ae148dea455fb9602<br>SHA256: ba5cb2d13b206c2344b4a44791973980a9017459cb0ce7ad0e7129725f8de072</pre></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.5MiB (233.3MB) – 3,777,698 rows – 250 unique countries<br><small><pre>MD5: f2478627b16f0b497bc6ddcd76f804e6<br>SHA1: 7dc491da79bb418ae33436830b45f1d1b6d1b028<br>SHA256: 6b6dc69010d2df832a554bce2d8a0f4824205d4b28792faf157afd14ec12566b</pre></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.5MiB (206.1MB) – 3,777,698 rows – 250 unique countries<br><small><pre>MD5: 0f548295457e9756bfd2f489da9a8cda<br>SHA1: dcf47465e329b55b521a230b7797f073f1bd00b7<br>SHA256: 5e88826d8f1d25393f4e59ca61a730ad385476e2db0fd60e218e87c29e54a633</pre></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.7MiB (213.6MB) – 3,777,698 rows – 250 unique countries<br><small><pre>MD5: 6a3aaba36b05c6234f1b8ac304020fd4<br>SHA1: 0b1abb3d26775d03bc7f2d6583526844fcd405f1<br>SHA256: e921564d4247bb5644daa8c76e9fc1d916a46a138352bcbe336b9b41e1b61ce4</pre></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.8MiB (250.4MB) – 3,777,698 rows – 250 unique countries<br><small><pre>MD5: 6866e7f98bb0bce3c7ad69384f07ae1a<br>SHA1: fb7cd064f50a212cda30aac432e1bc4d322b195c<br>SHA256: 78ebaa8622a9cf74c0d784aef9d553ee373b1b818deb2bd442c426de850a85b3</pre></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.2MiB (200.4MB) – 3,777,698 rows – 250 unique countries<br><small><pre>MD5: decf7fd40799b678b8e30a568d597d01<br>SHA1: 98c005ebe91960ac0eb7c3755694609867e9e18e<br>SHA256: 5d7ec25c0b9187f7a146dc312346cda848d936d5afd501779b00d0d1b647c498</pre></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.8MiB (251.4MB) – 3,777,698 rows – 250 unique countries<br><small><pre>MD5: e4c2c7e75b9411445844bb2e28e442d2<br>SHA1: ff18fb1383768037b21669840b959234c6635dd8<br>SHA256: 1a37f955c0726d5f0e2afbf52d89060407188e674b2dc7184eee523f66826363</pre></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.4MiB (213.3MB) – 3,777,698 rows – 250 unique countries<br><small><pre>MD5: 19531bf93947292f4ebca66708342f01<br>SHA1: 2da9efc64960d730dc409a42bf2ac0efff82ea2b<br>SHA256: c150e169bc0cd360f14c05b53023a31b549471bdc0b15494d169bbab07566470</pre></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>127.4MiB (133.5MB) – 1,269,549 rows – 250 unique countries<br><small><pre>MD5: 6463524c2b65ad126c018dffcd9db37a<br>SHA1: 2b349f7903ad6afd075dca2ed66e54a685582ecc<br>SHA256: 209bd3dbe5556ea05577b80dfba28f6dc81f529680d88909eb027190275caf97</pre></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>135.5MiB (142.0MB) – 1,269,549 rows – 250 unique countries<br><small><pre>MD5: 84b8a00483ce8095645cccbace62d7e1<br>SHA1: aba2712af1586817fef4b075e80bfde0cd4fc328<br>SHA256: d6266a4fdb0ac50492b028c32559dddfd2878102a9f60e3522f3d2116ea0c06f</pre></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>129.6MiB (135.9MB) – 1,269,549 rows – 250 unique countries<br><small><pre>MD5: eb182de5b9e69193958065aa03941705<br>SHA1: cee594d096a2690ade7964dcb1bc7ed01df2632d<br>SHA256: 49a2020ffe663685cb640508371378c7762b97fed5286e95291f97158943352b</pre></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>131.6MiB (138.0MB) – 1,269,549 rows – 250 unique countries<br><small><pre>MD5: 28b313fd5cad88506130edfdf45564f1<br>SHA1: 73797f4e6071a32dcda5ca8ab177d15843b65d2f<br>SHA256: d88f97fcbc48620b767d68a15da46c42d5e76972ccad43e691c990723be43959</pre></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.2MiB (145.9MB) – 1,269,549 rows – 250 unique countries<br><small><pre>MD5: 41001dd8576ad3aa1a72a42bfb94517e<br>SHA1: f2dca3029082cb4bdcbe4b32fab1f71e5d9df2c8<br>SHA256: c1cc3b9dc1ea56580bc544d67dd4534a59d5043e6e19514c1441da7b84fd2139</pre></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>128.7MiB (135.0MB) – 1,269,549 rows – 250 unique countries<br><small><pre>MD5: 43c4b02d9be315b6718a31925588f6c8<br>SHA1: 4a6c6ceac8476ee71b15de760a71d8573d437c0d<br>SHA256: ede7926c7d47644489399b24313ca6fd905f35b8c5cceffa0e66f534cca4f50d</pre></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>139.8MiB (146.6MB) – 1,269,549 rows – 250 unique countries<br><small><pre>MD5: 16c54144ed074845acd45e0d4f9bfce1<br>SHA1: 312270261296f03bcbaa0401fa909cbef1f80cfc<br>SHA256: a567148538702deac2a45eaa0fd25be32cba3824956cb4c82e1dfa3de9337048</pre></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>131.7MiB (138.1MB) – 1,269,549 rows – 250 unique countries<br><small><pre>MD5: 39d8cba469fbb8cf8e2279fcb2070ac6<br>SHA1: 9396d3e0dbbd18505dad61f9856771147b192112<br>SHA256: a678bba596d85f9e57e72a5f36dc2e7231bb47b4929626b0c9c0183365001f22</pre></small> |


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
