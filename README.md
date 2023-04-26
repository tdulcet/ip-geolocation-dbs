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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-04-26<br>IPv6: 2023-04-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.128MiB (6.426MB) – 261,175 rows – 249 unique countries<br><small><pre>MD5: e0edfa941c8c2e54957b87065c407ec4<br>SHA1: d9b5dedf8bc9e08717eabdf8d7a58f36d776e784<br>SHA256: 00999dbbce7ec0fdcf1d4d2a9c98d8affa5791e3213434257c9581a82da3481a</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.513MiB (6.829MB) – 84,313 rows – 250 unique countries<br><small><pre>MD5: 967c692d412730100f090197a6d53d57<br>SHA1: 08ed302f4cd3be49738e26ddf57a65dad6671058<br>SHA256: 756d77eed9086baf0ee07c97c893158e99ba215192c2f0d8e13efdc2fb844c52</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-04-26<br>IPv6: 2023-04-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.465MiB (9.925MB) – 402,045 rows – 240 unique countries<br><small><pre>MD5: 60e857eafdf147ab08191e9d5164feab<br>SHA1: 5e7993fdc5d7b63f42009fff49d99b3f1ac2551d<br>SHA256: 59a3cfefbba4bed8a28f10db1a9dcb0d5a099cf1a5aca72b82fe615c8b43ad8e</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.418MiB (7.779MB) – 96,132 rows – 221 unique countries<br><small><pre>MD5: 934a86c5242d3fa672046a34b745b55f<br>SHA1: 47bd59d4a2de5b29242b8f9bef40adf17ac3becf<br>SHA256: 0ae4706c8d0c77491b2ea8197e1fffe5b22cba20f495e9540dfe15e7b4f4644c</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-04-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.56MiB (14.22MB) – 578,875 rows – 243 unique countries<br><small><pre>MD5: 7c0b793b9f12018117b1bd61b0c0fbae<br>SHA1: eef0061d0842b2899cb070aa198add214b3c69f6<br>SHA256: bd488e1a24eb633ac16a87078b08606703cf84304db61c6b98a24c45b42ce4dd</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>26.61MiB (27.90MB) – 344,439 rows – 243 unique countries<br><small><pre>MD5: 95ebe975e47af7d7153b8d161dfaa82c<br>SHA1: d6704e3811179d38f214dcb3e9d6a8fb5d1f5fad<br>SHA256: 975603a56bea65056c3291d398b3b8becbcef0e2976987b37cb9024a8486974a</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.287MiB (7.640MB) – 312,180 rows – 244 unique countries<br><small><pre>MD5: 82354007656a327ea105907215d25ef9<br>SHA1: 67c794d1cec36d4b28bd7f519d16aaede697f7ae<br>SHA256: e4c6fbd5351ce06786a1a23d60f3cc152422ad29e1b7c48c0624da9761235e6f</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>21.32MiB (22.35MB) – 275,943 rows – 250 unique countries<br><small><pre>MD5: 4eec116f3dc312fbd1a82887804d6bed<br>SHA1: b2a486ba182d709c41684790f72cda40e767d382<br>SHA256: 1257bb248ef1d074a0a6abe23f9c54440744b5a8f37d6b2aca1e030d311dc9c2</pre></small> |
| | | Full Location | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>197.4MiB (207.0MB) – 3,267,813 rows – 243 unique countries<br><small><pre>MD5: 45d3670da1f2b31fcb68223a108be9af<br>SHA1: 37645fbeac5800a4ef57d4ce635fa5daa67ed21f<br>SHA256: d615d7817a3bbfdd4665c3bfccae8e6ae223c388323467fed143ca963313c64b</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>372.5MiB (390.6MB) – 3,244,362 rows – 250 unique countries<br><small><pre>MD5: 8aab3f0628a16d3290e30da4f527f4c8<br>SHA1: 19582f830e1b7052a98ed03d839aa97944679064<br>SHA256: 83e1d01ad2c49822595fcee1ca7abb10ae1c64dcd0ada5dff55cd46aa9ccd7ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-04-26<br>IPv6: 2023-04-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.510MiB (5.778MB) – 234,959 rows – 242 unique countries<br><small><pre>MD5: 2bba27a2b99c35f4adfcdb1e3f2c3155<br>SHA1: 29a4b09cccca77c92d517cb4a7be4b66fafc3354<br>SHA256: b0df0b763ec5f15501f89a825dfa85b591361850246e30260d46c2498145ea2a</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.42MiB (28.76MB) – 488,447 rows – 249 unique countries<br><small><pre>MD5: f754b5bde54b9a5d499f21e50664be91<br>SHA1: 638a2b52f5a21054aa3113b9a0b5d7cc9597443c<br>SHA256: fccdf823bfaa42d8f5e1b9338c57c955108fb976811a38544d113e9839da3beb</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-04-26<br>IPv6: 2023-04-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.9MiB (201.3MB) – 3,132,731 rows – 243 unique countries<br><small><pre>MD5: 3838c7e30ffdf6d0733a1183b8bc5f8b<br>SHA1: eabd91c83ed353e9c1772ef4c75790202a76b639<br>SHA256: 26f005f2f4c3afa282cd9a0622c8bbc26f7de72dcd77dedfa309adf8b89be8a0</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>382.5MiB (401.1MB) – 4,521,269 rows – 249 unique countries<br><small><pre>MD5: 84f8a06a23be4055c9018aad7e7e4024<br>SHA1: ff1af002a8f39309f8993c2c98f58478054f7550<br>SHA256: 0713b662001136ccee4d3f1c18f2c81c0615d7f3c0d2a1d536db02df4d676d78</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-04-24<br>IPv6: 2023-04-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.655MiB (10.12MB) – 411,596 rows – 250 unique countries<br><small><pre>MD5: 428bc851935311c63717244db58e6b4c<br>SHA1: a99a4b2cceb9159c026d8f71b2d5f907a42e5381<br>SHA256: d0fbcda9c5de303ef224900a49f00503e122dea50b4a00f95394fbb29ea877a0</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.08MiB (22.10MB) – 272,885 rows – 250 unique countries<br><small><pre>MD5: 8aa65d13ae07f547ddd9d64912844267<br>SHA1: 0154c4e162d6b625bac6d8d1a3311f2fed3f602d<br>SHA256: 8d1a8628e30f6c05c02be29dc22d92356b112da0e553269ab36e3021a2c15368</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-04-24<br>IPv6: 2023-04-24 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.2MiB (198.4MB) – 3,761,669 rows – 250 unique countries<br><small><pre>MD5: 4f4e86e3fb27ae04c8ac7977321bf807<br>SHA1: 742eabbcc6be0e626621a2faf4665a67cb03c536<br>SHA256: 069dfe3447dccb7cbee7e4a0b78ab1dda93e24fceee12823a44c3e2e7c82cfa6</pre></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.6MiB (232.3MB) – 3,761,669 rows – 250 unique countries<br><small><pre>MD5: ad6d719a62185c97754fb7ae647a80b1<br>SHA1: 2ec4713bf3a120c4801512c6ac93b9397fb5a4d8<br>SHA256: 7b1c99007ce2a9e798b41648d6c0332623ceed34f7f05dc2051116fa185f20a5</pre></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.6MiB (205.1MB) – 3,761,669 rows – 250 unique countries<br><small><pre>MD5: f806c86f52830ec3b8b7e4811fc2fcf6<br>SHA1: 55c514ef8495656a244b9b974e4cc3b9684b7a20<br>SHA256: 2931238ab5cb6bc3cf20ea18d33d3e09e0d56bc69e8a72cc964acd7918c3008e</pre></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.8MiB (212.6MB) – 3,761,669 rows – 250 unique countries<br><small><pre>MD5: 570d577f50b448835c0e71cb7921d391<br>SHA1: f7ffcd353f754f17d5cf7b7c8051590aaf2e281e<br>SHA256: 92cd32e1a30c5e76ed0b1bf565256c39626f55a755d9f0151f6449322dcf030d</pre></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>237.6MiB (249.1MB) – 3,761,669 rows – 250 unique countries<br><small><pre>MD5: cd4e0ddb6f347f2d1cd15170af8c5b53<br>SHA1: 8d476f9a53245989959b2bf720ff560daed5a758<br>SHA256: fee599bfee1b333e7c686501699b6491176ce51976d88c64df51a0a5ccbbbf20</pre></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.2MiB (199.5MB) – 3,761,669 rows – 250 unique countries<br><small><pre>MD5: 25784f0895b342248eded5cacd6fc428<br>SHA1: 239a402af64ec63d0031f237f56b44c075602835<br>SHA256: 6cd85c1ba92f3ec9f7a4cacef904d166c567ffa0c9e5793693e736b7799808fa</pre></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.6MiB (250.1MB) – 3,761,669 rows – 250 unique countries<br><small><pre>MD5: cc5f6b55445a1301b45afed60b3c87ea<br>SHA1: 915b9f6655d852edf63040305cc9d310c837b3e8<br>SHA256: a911478845c319ef2024d3681002bb3dbc9b6fa322f981fd1e0efbb842da49bf</pre></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.4MiB (212.2MB) – 3,761,669 rows – 250 unique countries<br><small><pre>MD5: 70fe84ce536ed699ba8fbc57a03374ff<br>SHA1: bf91df64bfae0fe1a6bb68db5c61ada45f95eaae<br>SHA256: d61c7fb561f3a5d5be71ec84ae18b77e93bd2e95303e2b8bfdd42829e3607892</pre></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.0MiB (134.2MB) – 1,273,801 rows – 250 unique countries<br><small><pre>MD5: 526c5320b47ab11095e87598bc4cc57d<br>SHA1: a4be0eb68af4fd058f541af7dc45eb8df07331d3<br>SHA256: 5508b22e1d95f005c2aa821117ce252875de41d0e46e668db0974ed5b8ff19ad</pre></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.2MiB (142.8MB) – 1,273,801 rows – 250 unique countries<br><small><pre>MD5: 2437fc7fa18b91c1988af0e52c92fded<br>SHA1: 345ecce17153d8ec76ef0d6043775b3fd0d0b89b<br>SHA256: 51e742ad451547bbd62b792c2410d1a4ccd021863e5acc6c64e02255d961fa8a</pre></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.3MiB (136.6MB) – 1,273,801 rows – 250 unique countries<br><small><pre>MD5: 493b83e7c80dc5623dc69351fb1561aa<br>SHA1: 112e2f942a6e1c6ded6f953a7387494618b6805c<br>SHA256: a195b63a7414e2c5c647fb92a5a7dc343adb64e035da3cda0b9ef6bef1c14d96</pre></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.4MiB (138.9MB) – 1,273,801 rows – 250 unique countries<br><small><pre>MD5: 061e7a10c5d8bdbe27e025ce7722c2ae<br>SHA1: 332fec015a2398a69533c7c547b4f7aabc25c7a3<br>SHA256: e276e5ac82fa7ebac997bf66baf795fa7a3e9c3b336e79d960fef5547796a8de</pre></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.9MiB (146.7MB) – 1,273,801 rows – 250 unique countries<br><small><pre>MD5: b8c439cc5ab8493f38818bd93512c6d5<br>SHA1: 3fee5a82c1f3631c420b7c1414e7b6ba3e643804<br>SHA256: ce2e297dd8e7864a63a79506993722e5f1b1b41f32f561b17d580b3da78fc15a</pre></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.4MiB (135.6MB) – 1,273,801 rows – 250 unique countries<br><small><pre>MD5: 5aff818820691ea3c1fe2ee1c945160e<br>SHA1: dd9f2857aa53cb7f21d92e4007c3ccf096091828<br>SHA256: 46b65e006ffe51e5ed465f6f499c916e2576fddb20373a1af7c15193d1846b15</pre></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.7MiB (147.5MB) – 1,273,801 rows – 250 unique countries<br><small><pre>MD5: 1b4159d995c17eda55bf47655fec3fbc<br>SHA1: 856be8fe825d6f815c1549d8c6c652f0e1f8d66c<br>SHA256: fff63ccc921df7f13eeb7c5b780b81f825780018f0c5d956e556cd3e9b20aa38</pre></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.4MiB (138.8MB) – 1,273,801 rows – 250 unique countries<br><small><pre>MD5: 9eb2d00ee1afe11e307b1efd5999799f<br>SHA1: c7b1e16b676af5e514fd338efa609565e1797ed9<br>SHA256: 199a00907ab5bb567d6cd6f2b54299c982874c84f360045326cdcf71d4a26094</pre></small> |


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
