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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-04-20<br>IPv6: 2023-04-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.135MiB (6.433MB) – 261,474 rows – 249 unique countries<br><small><pre>MD5: db27b87656813b8590555b85edb5459a<br>SHA1: 0914077a7e3333a608afc9a9b4697e1a1bd0ec05<br>SHA256: d2ab92a1a7f6c6d01b88806a6782a12e3b5d4b9dc41dac6308343d1e63aaf5cb</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.498MiB (6.813MB) – 84,115 rows – 250 unique countries<br><small><pre>MD5: 28562a382f863f1bd97631c0fd10d1d5<br>SHA1: ac1b3535f7f6ffd3c31e18328b2f36ec84ec327d<br>SHA256: ffc79a4bcaaab597ca12e9b8fcb75869557ec894636cdf62bf16a72729b3408d</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-04-20<br>IPv6: 2023-04-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.469MiB (9.929MB) – 402,225 rows – 240 unique countries<br><small><pre>MD5: 1b55d85a6e170a9e4db1863e00fd867d<br>SHA1: 481e7d99e406b6a7bed7e20f96144c7eb01e7b96<br>SHA256: d15d7ac48059918636f26af98fa5acbe7773c05e808b1c2e339e16ccc30ffd22</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.417MiB (7.777MB) – 96,109 rows – 221 unique countries<br><small><pre>MD5: 3feda17c5b3eb2f66720a6d72207b5d8<br>SHA1: c8eb14ecb10ef7e17fb761c142f4445868099eec<br>SHA256: c781a29d1544b32092dd5b08430f5871d96d7692da4e4bcbd2159bd3ba7f43b2</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-04-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.15MiB (14.84MB) – 607,344 rows – 243 unique countries<br><small><pre>MD5: dec894484f3350e8a3c50e2037f5bfd3<br>SHA1: d205d50eef69555913d20fb346938436fdb5c3b8<br>SHA256: 04aafc0f2ca04be029e56eed42d2bc88e69f84df88964d889d9e3ab3c12e052b</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>26.92MiB (28.23MB) – 348,482 rows – 243 unique countries<br><small><pre>MD5: a19f77f8d72c9d46576faf914643fa52<br>SHA1: f5ad472c540cfe5f1c5c8943c73949518bf72930<br>SHA256: b63a871d79931820ed43dfefe76f81fbc5ece7f7d268480bbe14c36b50105bd6</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.287MiB (7.640MB) – 312,180 rows – 244 unique countries<br><small><pre>MD5: 82354007656a327ea105907215d25ef9<br>SHA1: 67c794d1cec36d4b28bd7f519d16aaede697f7ae<br>SHA256: e4c6fbd5351ce06786a1a23d60f3cc152422ad29e1b7c48c0624da9761235e6f</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>21.32MiB (22.35MB) – 275,943 rows – 250 unique countries<br><small><pre>MD5: 4eec116f3dc312fbd1a82887804d6bed<br>SHA1: b2a486ba182d709c41684790f72cda40e767d382<br>SHA256: 1257bb248ef1d074a0a6abe23f9c54440744b5a8f37d6b2aca1e030d311dc9c2</pre></small> |
| | | Full Location | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>197.4MiB (207.0MB) – 3,267,813 rows – 243 unique countries<br><small><pre>MD5: 45d3670da1f2b31fcb68223a108be9af<br>SHA1: 37645fbeac5800a4ef57d4ce635fa5daa67ed21f<br>SHA256: d615d7817a3bbfdd4665c3bfccae8e6ae223c388323467fed143ca963313c64b</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>372.5MiB (390.6MB) – 3,244,362 rows – 250 unique countries<br><small><pre>MD5: 8aab3f0628a16d3290e30da4f527f4c8<br>SHA1: 19582f830e1b7052a98ed03d839aa97944679064<br>SHA256: 83e1d01ad2c49822595fcee1ca7abb10ae1c64dcd0ada5dff55cd46aa9ccd7ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-04-20<br>IPv6: 2023-04-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.510MiB (5.778MB) – 234,959 rows – 242 unique countries<br><small><pre>MD5: 2bba27a2b99c35f4adfcdb1e3f2c3155<br>SHA1: 29a4b09cccca77c92d517cb4a7be4b66fafc3354<br>SHA256: b0df0b763ec5f15501f89a825dfa85b591361850246e30260d46c2498145ea2a</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.42MiB (28.76MB) – 488,447 rows – 249 unique countries<br><small><pre>MD5: f754b5bde54b9a5d499f21e50664be91<br>SHA1: 638a2b52f5a21054aa3113b9a0b5d7cc9597443c<br>SHA256: fccdf823bfaa42d8f5e1b9338c57c955108fb976811a38544d113e9839da3beb</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-04-20<br>IPv6: 2023-04-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.9MiB (201.3MB) – 3,132,731 rows – 243 unique countries<br><small><pre>MD5: 3838c7e30ffdf6d0733a1183b8bc5f8b<br>SHA1: eabd91c83ed353e9c1772ef4c75790202a76b639<br>SHA256: 26f005f2f4c3afa282cd9a0622c8bbc26f7de72dcd77dedfa309adf8b89be8a0</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>382.5MiB (401.1MB) – 4,521,269 rows – 249 unique countries<br><small><pre>MD5: 84f8a06a23be4055c9018aad7e7e4024<br>SHA1: ff1af002a8f39309f8993c2c98f58478054f7550<br>SHA256: 0713b662001136ccee4d3f1c18f2c81c0615d7f3c0d2a1d536db02df4d676d78</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-04-17<br>IPv6: 2023-04-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.618MiB (10.09MB) – 409,962 rows – 250 unique countries<br><small><pre>MD5: d912daac1f3f0f23b40341767d8f10f4<br>SHA1: 21abfb30236395db2733ac5a425a92fc183ad965<br>SHA256: 983fd6e0e9de8e5f1df31fa5d925f76da62014667731a84862ce94d39ae8df86</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.07MiB (22.09MB) – 272,710 rows – 250 unique countries<br><small><pre>MD5: fc43b9ae111a7240f6546c0ee2112c65<br>SHA1: 6ae8f83740dd6a5aebdcc3d428bf6889e27c8640<br>SHA256: a6c0f1f4b898651ae0e77a954d3470eeb01dd6ba6c8ec1704bf3cbc592df692b</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-04-17<br>IPv6: 2023-04-17 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.9MiB (199.2MB) – 3,777,575 rows – 250 unique countries<br><small><pre>MD5: f46890ad80b6bb10293022ad4c58688e<br>SHA1: 48274a0b37aa715966deab8cc784a227f706ed6a<br>SHA256: 009ce11f34ef3c43635f1727966a44be65098e224b5f7afa1dbb1f06520bc7e4</pre></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.5MiB (233.3MB) – 3,777,575 rows – 250 unique countries<br><small><pre>MD5: 8865690cc38e77974438845c2b206031<br>SHA1: 6318867cbdd99d9a36b4262e4e883396b8db9481<br>SHA256: c91535b99818736808d73453c2c8d01c476db3e84f3b6ca38cd25fc9fa1d67ac</pre></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.5MiB (206.1MB) – 3,777,575 rows – 250 unique countries<br><small><pre>MD5: 26486b5683c64178a7c7c5bcfdc3f15d<br>SHA1: 3cf96f7047eafd9b2a21d8a6c9b6a18dfb559b25<br>SHA256: db82e22f564c00e7ddc45c4b75a158e056531e0b9ae5fd71447fa65c0f30e899</pre></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.7MiB (213.5MB) – 3,777,575 rows – 250 unique countries<br><small><pre>MD5: 56c157a6be2402032c5106776efc969c<br>SHA1: b1b5c77e03816127dedf2f4b51936f0cf23ead4c<br>SHA256: cbd91cf02d7130770180d820140cb176f3ae4d1f5be9ec311b63b37fcdfeaca0</pre></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.8MiB (250.4MB) – 3,777,575 rows – 250 unique countries<br><small><pre>MD5: 0f7e166ac5bc18f6cc05c93a88fc49d8<br>SHA1: e8ac749e82cf242e6b400c0af4bb9086bff38e79<br>SHA256: e5b0f9888821452f373e9dc48120a73268f7a84beef2fb5bb671b60f8f2b0e86</pre></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.2MiB (200.4MB) – 3,777,575 rows – 250 unique countries<br><small><pre>MD5: cf36a9a06e2eb43ee44104754cef15ef<br>SHA1: 47c0ecbfb907da93e640cd9454e9d000cb9c441c<br>SHA256: 25b82804e804ffe39448ef60a1fe63fa12f902afa6445e1bba909dda145c736c</pre></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.7MiB (251.4MB) – 3,777,575 rows – 250 unique countries<br><small><pre>MD5: 8b065cf8f946d6cfcd8489fe3c60bd70<br>SHA1: e3ad52c247de0b4020e2665ec14be39b9e9b8909<br>SHA256: 43cefa1084d4065d42d4b07f129b13871bafd5396fe0bfdb2e43584ff89fb76e</pre></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.4MiB (213.3MB) – 3,777,575 rows – 250 unique countries<br><small><pre>MD5: 4af07b4537f8f12cd9f598c221c36e53<br>SHA1: 942b045af1016ec87177e8ad3d5f9f79b1ee7cf3<br>SHA256: faa3531329fba8e149eecb4908bf6768784433b0c3c65d6ae2a85399bd38d21f</pre></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>127.6MiB (133.8MB) – 1,271,808 rows – 250 unique countries<br><small><pre>MD5: a5b9fb8893565de8c7619bd12edef5e0<br>SHA1: 2263883dedc5ef2f124304807ac8d76bb66c6e88<br>SHA256: 89fdeac3f634b953902446ae3f840303a52008b59b7eb76fba4bd8b0f35712a5</pre></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>135.7MiB (142.3MB) – 1,271,808 rows – 250 unique countries<br><small><pre>MD5: b0aea8b367329f894dd7a92640e058fa<br>SHA1: 844124dafae47ad12b3227edb0e5a82ac8c72827<br>SHA256: 22def828be3a1b77f8372920c550b816755c244d04fcca7923f021975be97876</pre></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>129.8MiB (136.1MB) – 1,271,808 rows – 250 unique countries<br><small><pre>MD5: be4ed4ccc84eda717185031bd289d0e8<br>SHA1: c2a206a4214241df5ce4e652a36fdfb7af1a9250<br>SHA256: 950759abca1f6df445e406274c8fd40f59b374e25d44e12244c7b58825ee4c54</pre></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>131.8MiB (138.2MB) – 1,271,808 rows – 250 unique countries<br><small><pre>MD5: eba091a7445a986b2a6c3be79f7bef3a<br>SHA1: c986ae515e4a8ac312b8fb524fc63d7d6cea391e<br>SHA256: 01a5d0f42c1e1b4205d73acf0f4cf342d11b807f11b976c68e8656b230e63cb8</pre></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.3MiB (146.1MB) – 1,271,808 rows – 250 unique countries<br><small><pre>MD5: 6c3bf91d8ce2efee374429d75e049539<br>SHA1: a3bfc8094c5182801e8c4631d3c0ad178288f0f5<br>SHA256: 3df00c80f0c5cfe34f1d36051eb434d6820fc235e3335fd24f3a049353177039</pre></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>128.9MiB (135.2MB) – 1,271,808 rows – 250 unique countries<br><small><pre>MD5: 012f76243c1e3bcadc5b23994a9221f0<br>SHA1: 2fa0dff87c68bc7e66adac6302e383ae547de097<br>SHA256: 70ce6016a859c933d8e9e7b6c7819c1e538da7484d60b1557847f621e3a0055a</pre></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.0MiB (146.8MB) – 1,271,808 rows – 250 unique countries<br><small><pre>MD5: ab6a88bab782747a857cc44d6d60a782<br>SHA1: f9c64dc707d40e3580bcaf6076acec88af2d0dba<br>SHA256: 2d75baf43aea7e82b45f1c82b8963c6acfc80c3c1a38ac77911d62e2b1546873</pre></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>131.9MiB (138.3MB) – 1,271,808 rows – 250 unique countries<br><small><pre>MD5: eae0169e30c5494d10ea9959d3f3b006<br>SHA1: 0e972a57d814a5b50aa02688c99a68f559daf481<br>SHA256: f962d4a1478183fdd55c684c088285da704dca9ee4ab0bec5dd704605f695bec</pre></small> |


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
