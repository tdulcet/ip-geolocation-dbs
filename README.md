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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-04-15<br>IPv6: 2023-04-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.132MiB (6.430MB) – 261,367 rows – 249 unique countries<br><small><pre>MD5: c3991eb2eac7f89733dc07ca69654358<br>SHA1: e9c5447c8b79353615f85b2fadc2bac9bed0810d<br>SHA256: bb77456395697f5ec87047bbb51870796a64163b962c93796a2b54e446091a4a</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.492MiB (6.807MB) – 84,040 rows – 250 unique countries<br><small><pre>MD5: b3f8a63d5655e19f342ea5ae185df434<br>SHA1: 8c50749a6d55e75f088627215bfd68a39f8de78f<br>SHA256: dfa9cc258089472248e0e0f1d393ec16eaeaae25663afb9e9867b851430703ba</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-04-15<br>IPv6: 2023-04-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.483MiB (9.943MB) – 402,757 rows – 241 unique countries<br><small><pre>MD5: 5a4dddf4967b718edefa30c3e20562c0<br>SHA1: 905433fb1fa88218ccf40a3fe98f54e9a0e3bf67<br>SHA256: af63845bc9780f9d4e0260a19b010d42a258e81c011dabe74ef267bc5cfacf7f</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.420MiB (7.780MB) – 96,148 rows – 221 unique countries<br><small><pre>MD5: 596866542b35ed087bdfa331d33f694e<br>SHA1: bc94263b6c09f213fe255721a782a095ce424662<br>SHA256: aa1e1d5700a257d1f8f8c237cbed215cea62a2ea99bb6dd02d757bb2eabb4b0a</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-04-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.12MiB (14.80MB) – 605,816 rows – 243 unique countries<br><small><pre>MD5: a0a1d02b70b6469624ef6bd9856f903a<br>SHA1: 5761fed0f9c8d63fc7e712fab5b2c3d1d52db828<br>SHA256: 4eb6d6107c2bf04d4db72c80e85c6ab4e59cb413310919fa6a332fe21f3dc235</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>26.84MiB (28.14MB) – 347,447 rows – 243 unique countries<br><small><pre>MD5: 2356d61854bcfa1222b251479723990f<br>SHA1: 97391763338b58e41afc2e5dc4175f1632d3fd44<br>SHA256: bda2ab6ca7637cc68576164916125ae0f0fed035e34bc4bc159854283c967bb9</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.287MiB (7.640MB) – 312,180 rows – 244 unique countries<br><small><pre>MD5: 82354007656a327ea105907215d25ef9<br>SHA1: 67c794d1cec36d4b28bd7f519d16aaede697f7ae<br>SHA256: e4c6fbd5351ce06786a1a23d60f3cc152422ad29e1b7c48c0624da9761235e6f</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>21.32MiB (22.35MB) – 275,943 rows – 250 unique countries<br><small><pre>MD5: 4eec116f3dc312fbd1a82887804d6bed<br>SHA1: b2a486ba182d709c41684790f72cda40e767d382<br>SHA256: 1257bb248ef1d074a0a6abe23f9c54440744b5a8f37d6b2aca1e030d311dc9c2</pre></small> |
| | | Full Location | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>197.4MiB (207.0MB) – 3,267,813 rows – 243 unique countries<br><small><pre>MD5: 45d3670da1f2b31fcb68223a108be9af<br>SHA1: 37645fbeac5800a4ef57d4ce635fa5daa67ed21f<br>SHA256: d615d7817a3bbfdd4665c3bfccae8e6ae223c388323467fed143ca963313c64b</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>372.5MiB (390.6MB) – 3,244,362 rows – 250 unique countries<br><small><pre>MD5: 8aab3f0628a16d3290e30da4f527f4c8<br>SHA1: 19582f830e1b7052a98ed03d839aa97944679064<br>SHA256: 83e1d01ad2c49822595fcee1ca7abb10ae1c64dcd0ada5dff55cd46aa9ccd7ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-04-15<br>IPv6: 2023-04-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.510MiB (5.778MB) – 234,959 rows – 242 unique countries<br><small><pre>MD5: 2bba27a2b99c35f4adfcdb1e3f2c3155<br>SHA1: 29a4b09cccca77c92d517cb4a7be4b66fafc3354<br>SHA256: b0df0b763ec5f15501f89a825dfa85b591361850246e30260d46c2498145ea2a</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.42MiB (28.76MB) – 488,447 rows – 249 unique countries<br><small><pre>MD5: f754b5bde54b9a5d499f21e50664be91<br>SHA1: 638a2b52f5a21054aa3113b9a0b5d7cc9597443c<br>SHA256: fccdf823bfaa42d8f5e1b9338c57c955108fb976811a38544d113e9839da3beb</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-04-15<br>IPv6: 2023-04-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.9MiB (201.3MB) – 3,132,731 rows – 243 unique countries<br><small><pre>MD5: 3838c7e30ffdf6d0733a1183b8bc5f8b<br>SHA1: eabd91c83ed353e9c1772ef4c75790202a76b639<br>SHA256: 26f005f2f4c3afa282cd9a0622c8bbc26f7de72dcd77dedfa309adf8b89be8a0</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>382.5MiB (401.1MB) – 4,521,269 rows – 249 unique countries<br><small><pre>MD5: 84f8a06a23be4055c9018aad7e7e4024<br>SHA1: ff1af002a8f39309f8993c2c98f58478054f7550<br>SHA256: 0713b662001136ccee4d3f1c18f2c81c0615d7f3c0d2a1d536db02df4d676d78</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-04-13<br>IPv6: 2023-04-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.575MiB (10.04MB) – 408,158 rows – 250 unique countries<br><small><pre>MD5: 9e9c3e9d8cf1c6a4fe4d3a8a7160246f<br>SHA1: c6379d14fa94596c59f7679502aaa949b7d7ede9<br>SHA256: f59a480b441baa844a7621f1de2458fda7e758f4eeb083704b73a6af502998ec</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.84MiB (21.85MB) – 269,785 rows – 250 unique countries<br><small><pre>MD5: b01d37026bbbb2affb4afed4f4e35629<br>SHA1: 6adcc880624557b7b6320bbed8dc9af29df5d5bf<br>SHA256: 7c2bf3d3e6ac143fb58b5da3454b885d491e3e013205d20e4a1f2074c01b0192</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-04-13<br>IPv6: 2023-04-13 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.1MiB (199.4MB) – 3,781,623 rows – 250 unique countries<br><small><pre>MD5: 29395390a2077add0d0f588fd657fe1d<br>SHA1: 5023721aa556946fca2b83753cf4be9fb8d606f4<br>SHA256: 45a55acddb8b7bde3274d37385f2920f514682febf9a247c24ec5435d87875a8</pre></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.7MiB (233.5MB) – 3,781,623 rows – 250 unique countries<br><small><pre>MD5: 5e140cd47eb1bda30c5dc495066ee138<br>SHA1: 2ca9fa0d7e6ee0137034b507d5d0cce24147f9dc<br>SHA256: 0e67d617fc84f3f20740d26c25406c6c903b0e6ae3cfbda9c82383cdb9bffc23</pre></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.7MiB (206.3MB) – 3,781,623 rows – 250 unique countries<br><small><pre>MD5: a81ee8025b25acd1de63e568f5b5026b<br>SHA1: 65789ea8200acdee5bc6e1cd1feccdf69b6b54d9<br>SHA256: 322ab7aa4a9b7ca31e225266644c52e2de9c878bfd900b0b79edec646fcf7302</pre></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.9MiB (213.8MB) – 3,781,623 rows – 250 unique countries<br><small><pre>MD5: a4f46bbe93c02a58cc6beb121f6586bd<br>SHA1: 044c16a117dc93155001de64dd8ea5726716ebd6<br>SHA256: ff47240d2401f8f20747f1f6bb2b7715855a074a6d9640d0134e36a0414d9834</pre></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.1MiB (250.7MB) – 3,781,623 rows – 250 unique countries<br><small><pre>MD5: 102974470a0c511c32570127ccb06217<br>SHA1: 673fd0d8b2d2335e391fb9fc6754b3ad5eead320<br>SHA256: d108baf32206b194db79e883330e459ae6ea9a985f3d6119eb038349813b5da3</pre></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.4MiB (200.7MB) – 3,781,623 rows – 250 unique countries<br><small><pre>MD5: 92c64b9524edda26c229d86b60d237e4<br>SHA1: ea25c6561331bd9994efba704eeed19933457dc1<br>SHA256: caa86bcd1a72f493883758e68c82e46f5fc33f01c6a607088d077d39a2c82d45</pre></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.0MiB (251.7MB) – 3,781,623 rows – 250 unique countries<br><small><pre>MD5: 085e4a6ba5b622281be4fee48ef1f3f5<br>SHA1: 6a1579a7d199c07fd1b067d19e86858f60198d9b<br>SHA256: d0a130f15b435b81e028b5876278fb21e2e0d5d86ceee58481c1dcc3bb0ac304</pre></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.6MiB (213.5MB) – 3,781,623 rows – 250 unique countries<br><small><pre>MD5: 5638e04f7ff7cb8794168de9b08a0669<br>SHA1: 019ff6d40a8996427c90ea1bd43ef22185e74375<br>SHA256: 1d8b7581d8ffbce2d57b89b57f219af8bfb08a77db28ce11156001deb8e07040</pre></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>127.5MiB (133.7MB) – 1,270,872 rows – 250 unique countries<br><small><pre>MD5: d1c16a9abb20ba9ce9b3aa287362c257<br>SHA1: 4833b2af78098004b3f46390fc38bd3b125d70af<br>SHA256: a726fddf1f3ca55dbb68c321fb232df9f3a35dea5195afc859ed5596936a80d8</pre></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>135.6MiB (142.2MB) – 1,270,872 rows – 250 unique countries<br><small><pre>MD5: 53748e5c1d9b965ed32006a726678f7f<br>SHA1: 1b39002f49b0d99028436be6b973c2ec10271974<br>SHA256: bb1381025a85433ee5d682713e6b366fd0cc53ab9074247902316c86f739aaa8</pre></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>129.7MiB (136.0MB) – 1,270,872 rows – 250 unique countries<br><small><pre>MD5: 13d9037c3bc8e8c09538f7dc7e969207<br>SHA1: 63b4601f26c76823fb286708809fa6b1d439a326<br>SHA256: 98253c3a36b26a92c361a7724e6a35be47ef902f4b93bf359105b9f104c1ff50</pre></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>131.7MiB (138.1MB) – 1,270,872 rows – 250 unique countries<br><small><pre>MD5: 50cb12f2a5ea2d5053b1b9b63e0b6813<br>SHA1: 7018c7c5a47bcae1f940873afa883a48bffded2d<br>SHA256: 956d88c26758aef6d93821aa2289fa51e9b4cefd4ac8d093f8bb062cb59bbde1</pre></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.3MiB (146.1MB) – 1,270,872 rows – 250 unique countries<br><small><pre>MD5: 8fdd6f1383f8433ada7a54a0c5b6f12d<br>SHA1: c3129957177dfe9b66dd31549615f3bf38ec48d7<br>SHA256: 80e06c88859e7747b02aacdeb0271697af3d1a4181ac1a923e9e31e1b21dc571</pre></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>128.8MiB (135.1MB) – 1,270,872 rows – 250 unique countries<br><small><pre>MD5: 396ade43b51cb409f137b378ef15d686<br>SHA1: 1f39014028ff543525ccc6ef3a4ca480310f839f<br>SHA256: fa665d6966cbd3b38b46bdbb2a5db333d9b3a10623b1639ac6be70a6276e70a1</pre></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>139.9MiB (146.7MB) – 1,270,872 rows – 250 unique countries<br><small><pre>MD5: 204bda567f92d2fab38d39755b998787<br>SHA1: b380c07e831d3e97777e22f1e553ea6db3bd6e26<br>SHA256: d8a61ad4ae424afd9ddd9accdbdddd7b189fb20d42b7bc2a40d0ce4d6356c543</pre></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>131.8MiB (138.2MB) – 1,270,872 rows – 250 unique countries<br><small><pre>MD5: ac362919ba2537a2ccc35b31195e63ce<br>SHA1: dbe3772a83bca4f1a47c4ce3c4f36f7c655e7cdc<br>SHA256: 8574ee38166a0a092c4aac066c08b5c4bbe3abfdcb5d41594d73435ca2533547</pre></small> |


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
