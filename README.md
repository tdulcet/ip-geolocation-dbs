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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-04-01<br>IPv6: 2023-04-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.143MiB (6.442MB) – 261,841 rows – 249 unique countries<br><small><pre>MD5: 21466250ad091e4da25a1e5022155710<br>SHA1: f3ec8c9f96ead3bb1cb8b992d1896fac85e9b82c<br>SHA256: 0431b55539609bb360ef0d40f0c4f26b4c7c50d410982d87c4f8af290ce6bc65</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.429MiB (6.741MB) – 83,225 rows – 250 unique countries<br><small><pre>MD5: 3d691c2e584b8027da3b8766656df113<br>SHA1: f235795dca6af9d2ebf020ccd0526ebb4bb0da10<br>SHA256: d2b18b1bc284ea0921591464448b25fd20c8590ef870defb11524129d2ec2d47</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-04-01<br>IPv6: 2023-04-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.439MiB (9.898MB) – 400,921 rows – 240 unique countries<br><small><pre>MD5: c6ab7690c38d5107bcf4a0d252b0177f<br>SHA1: 6c5afe3843a4713592892748cf92bd49d6d64d22<br>SHA256: e9348a94acdc4bf2d772a1f538486eeadcac3f425d0aa1481d54aca205d27dd2</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.382MiB (7.740MB) – 95,659 rows – 221 unique countries<br><small><pre>MD5: 57fb70506fe6857e9c50772f68f91709<br>SHA1: 5da04a40381a97b38e0190a206266173e47e8b95<br>SHA256: b8adb2f82de9444291a515204d938f05b0f116654e366051d1293d33387091ab</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-04-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.64MiB (15.35MB) – 626,785 rows – 243 unique countries<br><small><pre>MD5: c5d84bb23806968e29af9f87b3766292<br>SHA1: 4e015f5c4a7bafa8f7d5914114e453f1ed572b50<br>SHA256: 1a94947eaf0fbe5740162bfe3339e9e9cf9f30968047518f25b1b17ed8183af1</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>31.48MiB (33.01MB) – 407,480 rows – 243 unique countries<br><small><pre>MD5: 700886c50f8dbcfa4c3498e316dc117b<br>SHA1: 4c11dc32f4400321bd26791f0981a9919a576703<br>SHA256: de5aea18ee253dc3dd10ddeb31bd82b6310fca70320bb66f52421946a19f1eba</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-04-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.287MiB (7.640MB) – 312,180 rows – 244 unique countries<br><small><pre>MD5: 82354007656a327ea105907215d25ef9<br>SHA1: 67c794d1cec36d4b28bd7f519d16aaede697f7ae<br>SHA256: e4c6fbd5351ce06786a1a23d60f3cc152422ad29e1b7c48c0624da9761235e6f</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>21.32MiB (22.35MB) – 275,943 rows – 250 unique countries<br><small><pre>MD5: 4eec116f3dc312fbd1a82887804d6bed<br>SHA1: b2a486ba182d709c41684790f72cda40e767d382<br>SHA256: 1257bb248ef1d074a0a6abe23f9c54440744b5a8f37d6b2aca1e030d311dc9c2</pre></small> |
| | | Full Location | Monthly<br>2023-04-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>197.4MiB (207.0MB) – 3,267,813 rows – 243 unique countries<br><small><pre>MD5: 45d3670da1f2b31fcb68223a108be9af<br>SHA1: 37645fbeac5800a4ef57d4ce635fa5daa67ed21f<br>SHA256: d615d7817a3bbfdd4665c3bfccae8e6ae223c388323467fed143ca963313c64b</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>372.5MiB (390.6MB) – 3,244,362 rows – 250 unique countries<br><small><pre>MD5: 8aab3f0628a16d3290e30da4f527f4c8<br>SHA1: 19582f830e1b7052a98ed03d839aa97944679064<br>SHA256: 83e1d01ad2c49822595fcee1ca7abb10ae1c64dcd0ada5dff55cd46aa9ccd7ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-04-01<br>IPv6: 2023-04-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.510MiB (5.778MB) – 234,959 rows – 242 unique countries<br><small><pre>MD5: 2bba27a2b99c35f4adfcdb1e3f2c3155<br>SHA1: 29a4b09cccca77c92d517cb4a7be4b66fafc3354<br>SHA256: b0df0b763ec5f15501f89a825dfa85b591361850246e30260d46c2498145ea2a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.42MiB (28.76MB) – 488,447 rows – 249 unique countries<br><small><pre>MD5: f754b5bde54b9a5d499f21e50664be91<br>SHA1: 638a2b52f5a21054aa3113b9a0b5d7cc9597443c<br>SHA256: fccdf823bfaa42d8f5e1b9338c57c955108fb976811a38544d113e9839da3beb</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-04-01<br>IPv6: 2023-04-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.9MiB (201.3MB) – 3,132,731 rows – 243 unique countries<br><small><pre>MD5: 3838c7e30ffdf6d0733a1183b8bc5f8b<br>SHA1: eabd91c83ed353e9c1772ef4c75790202a76b639<br>SHA256: 26f005f2f4c3afa282cd9a0622c8bbc26f7de72dcd77dedfa309adf8b89be8a0</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>382.5MiB (401.1MB) – 4,521,269 rows – 249 unique countries<br><small><pre>MD5: 84f8a06a23be4055c9018aad7e7e4024<br>SHA1: ff1af002a8f39309f8993c2c98f58478054f7550<br>SHA256: 0713b662001136ccee4d3f1c18f2c81c0615d7f3c0d2a1d536db02df4d676d78</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-03-30<br>IPv6: 2023-03-30 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.991MiB (10.48MB) – 426,265 rows – 250 unique countries<br><small><pre>MD5: 29e3ad44b0da1b76f203e25d8083eddc<br>SHA1: 0ecb9e2e02513b4107320bed02e0fa6a90faa7cd<br>SHA256: a5a5cdbe5f06c15a21ec74f8363fa60f1030faee3a26a0d2963f19bc29afccb6</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.53MiB (21.52MB) – 265,720 rows – 250 unique countries<br><small><pre>MD5: fdd6fe883e4f98879a2892915f10bf38<br>SHA1: dfc810190f2dc22af7f7afdc50dffd3bfcc3baca<br>SHA256: bebdbf7fec390e329cc14fef9304e93b2ee0bd0a9a1bf053af9cedb7ad9ab166</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-03-30<br>IPv6: 2023-03-30 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.4MiB (198.6MB) – 3,775,231 rows – 250 unique countries<br><small><pre>MD5: 26e53884cfdffe17b38c610b07d74fe5<br>SHA1: 00698f35f0637e8d79ddd75421633d2909e670d8<br>SHA256: ef3f5ded2e59a274184913fe4ecb552fca58ff8f095620d591dec5d905fed9a7</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.8MiB (232.6MB) – 3,775,231 rows – 250 unique countries<br><small><pre>MD5: 06af832aa56e14238ed997ab9d291b49<br>SHA1: 81db6a208fdc9215b4c95d07ae4945df60759c22<br>SHA256: d2bb393aad0af262587071aa2743ed23f3242935d4de8c9f6f895f8c04ba1ce5</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.0MiB (205.5MB) – 3,775,231 rows – 250 unique countries<br><small><pre>MD5: a56a0a193e95bf7402ea445cd1b417e7<br>SHA1: 25efe32d466acafa591aa4eb7d6823b82fae58a3<br>SHA256: 4daec8253ffb4626de27fbd78ec4aad62ff013f76eaa2112b7ef23f61cd9e031</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.1MiB (213.0MB) – 3,775,231 rows – 250 unique countries<br><small><pre>MD5: 2eeb1db1198706b6ab8671e92b6194b8<br>SHA1: 956e2cf64133465df68dc28f086111981bfd853a<br>SHA256: 81bee5a4d92a91fddb5d70f6987cbb654f105fd0ea9f4ed01baf50cf04e546cf</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>237.9MiB (249.4MB) – 3,775,231 rows – 250 unique countries<br><small><pre>MD5: b63b04c05cf017c64851b5e0ac9448d9<br>SHA1: d3567e13a0cfa215d17027b41651d15929af3031<br>SHA256: b03922761d84c9e7ca5e49e920016aded6a0a4faf54269abc5b29475b8a2ad00</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.7MiB (199.9MB) – 3,775,231 rows – 250 unique countries<br><small><pre>MD5: 08c4edb089c6cff3e282dbb701fbe53c<br>SHA1: c3752cc3a0f4f59f08cfb7902572f191b37d61f6<br>SHA256: 6c1a54eca1771828c89d30ca1c1d143e5ae9ada93aba1142559fe073943dbc5a</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.9MiB (250.5MB) – 3,775,231 rows – 250 unique countries<br><small><pre>MD5: 8cae9cca2ffdc76c1d5f539e40e4205e<br>SHA1: fb318c028ee940c8272fe0f231301bdeff106a61<br>SHA256: 18cac27a6838c313d284e29ee677ea19856dbe11b3eeee68d72330f0069184bf</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.9MiB (212.7MB) – 3,775,231 rows – 250 unique countries<br><small><pre>MD5: 31e8d8cdcaac1140c7a7fc5b877c8ccb<br>SHA1: 801f0dce9aab982def23ca02ad8e407b4cfd64e8<br>SHA256: 57a5775b7ad3c2f1b6891419c64d97fe6e67c38216afc34873d34f7024747dee</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>123.9MiB (129.9MB) – 1,237,127 rows – 250 unique countries<br><small><pre>MD5: 3fe4a535074765b7ea714ffd57a21b65<br>SHA1: b60431509f375ebea3fb72748f62b118a73ee719<br>SHA256: e42ffdd82598766d60735fd090b9e93ad6ef0ce82c036d3f69415c37691d33bb</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>131.9MiB (138.3MB) – 1,237,127 rows – 250 unique countries<br><small><pre>MD5: b4255ae8e3b3a40bca594986ea10b1bb<br>SHA1: 157a499b85f6d151a823b5aa1e23f7037aec4cc5<br>SHA256: f09edf144507d908953bf97e524a206d4d02f6db26e68f1cf0c9611d8c0c8437</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>126.0MiB (132.1MB) – 1,237,127 rows – 250 unique countries<br><small><pre>MD5: 92a694853367859fcf2bc4c9a34e8d67<br>SHA1: 5f43f299c76281e95ad65792864ae3938306a85b<br>SHA256: ad40b71fb795f5fbb3f0675ce063eda68db77c8f1096852377230f985af7fcf1</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.0MiB (134.2MB) – 1,237,127 rows – 250 unique countries<br><small><pre>MD5: faa610fedb95716fe78fdae3e351bf64<br>SHA1: 268f17d8fceb127e6511f720a776bf9929916adc<br>SHA256: d16f7c60d3be8d5346ea406bce2b89ddac172d6e49b0dd16131b52877e2f9f9f</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>135.3MiB (141.9MB) – 1,237,127 rows – 250 unique countries<br><small><pre>MD5: efe44dcdeb84c8b1dcfa1fc3569b9f29<br>SHA1: 975c36f6c8a58ce1de0c195e11eb5c568b22173b<br>SHA256: e35c042f8d87d76d29d4d43b9df958b87bc737cb48936d1ccd9823b912f92e4e</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>125.2MiB (131.3MB) – 1,237,127 rows – 250 unique countries<br><small><pre>MD5: a7e0059e07c5b8311923d6a4f7eb8ac0<br>SHA1: 0cff89530f0eb874f93017d1bc018491cdb32b22<br>SHA256: 98bf167bd6199bd35b0f95c17d4555c8c0771d270e6db80cd01658d2f04b5c71</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.0MiB (142.6MB) – 1,237,127 rows – 250 unique countries<br><small><pre>MD5: 80b9818c403daf2bcbb26773cfe4f4e3<br>SHA1: 84b49f623ead1705a27538f8993ed4b95bf5ac01<br>SHA256: 26f0150c58c82177018ec21c122d70c524db64dea2ff648f426be09b085d7fd5</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>128.1MiB (134.4MB) – 1,237,127 rows – 250 unique countries<br><small><pre>MD5: b39ac30909c53d86e39f511cf72ef705<br>SHA1: b99e4b4c1ac5501ae2d1dbda8482bcdab2625ea4<br>SHA256: 5d4464c6df3bb1d2d336be2f4d4bb102040fd458b217ced6f40e2c5d6590b02a</pre></small> |


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
