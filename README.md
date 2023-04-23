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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-04-23<br>IPv6: 2023-04-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.135MiB (6.433MB) – 261,480 rows – 249 unique countries<br><small><pre>MD5: f23969275f475173272a6ef01f932030<br>SHA1: 636f352156ff19fcf18b1534809b0450d12791f1<br>SHA256: 9e05d1a00cb511e9f0879a8cb056793889a786c7b666b632b7b2227ab6932ad9</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.510MiB (6.826MB) – 84,269 rows – 250 unique countries<br><small><pre>MD5: 1b5d7b87d42503d8876d401d68e38a49<br>SHA1: 463e3e11796d9b6b30bcf1487d239d634ed27896<br>SHA256: c80743837ce5c46bce629b2c5539950f05109d465f67ca52a75c27debdab1de2</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-04-23<br>IPv6: 2023-04-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.463MiB (9.922MB) – 401,934 rows – 240 unique countries<br><small><pre>MD5: d07e4383ed8857da11fbf1c3e3e2b6dc<br>SHA1: f4c167d42bd94ba44d005b3468ffa5c75122f618<br>SHA256: 5f5d10662c7ce7d92ecaca300e3c9c91ca8b3cc8b9b933b3c0fb2b2f73633994</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.414MiB (7.774MB) – 96,072 rows – 222 unique countries<br><small><pre>MD5: 4c1ec30348676bf61d5049930819a4f7<br>SHA1: f365e78212615de702e88de308efec45a7e91b08<br>SHA256: 38717a8a2e90e43ac777997d9556c6a72d0837e6e873475d727d779a4fa4d894</pre></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-04-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.11MiB (13.75MB) – 559,327 rows – 243 unique countries<br><small><pre>MD5: 93bb225379a960abe93a2be6aba730bf<br>SHA1: 7d6c31b610a1755674725187e9bd2f1e09e777ef<br>SHA256: 1c735bf3d5788c14242dcfd172ca789b8b34253b37d167c11feb5da8cb731637</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>26.10MiB (27.36MB) – 337,815 rows – 243 unique countries<br><small><pre>MD5: 577c7863dea84aece89dccca2cf9fc82<br>SHA1: 6a81d2281ba2c69e5367e1ca2d45db3b55fc1b45<br>SHA256: 72de22165555debe0b1dac2bec50d67f2727f42ab697c8967102c58d7f035018</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.287MiB (7.640MB) – 312,180 rows – 244 unique countries<br><small><pre>MD5: 82354007656a327ea105907215d25ef9<br>SHA1: 67c794d1cec36d4b28bd7f519d16aaede697f7ae<br>SHA256: e4c6fbd5351ce06786a1a23d60f3cc152422ad29e1b7c48c0624da9761235e6f</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>21.32MiB (22.35MB) – 275,943 rows – 250 unique countries<br><small><pre>MD5: 4eec116f3dc312fbd1a82887804d6bed<br>SHA1: b2a486ba182d709c41684790f72cda40e767d382<br>SHA256: 1257bb248ef1d074a0a6abe23f9c54440744b5a8f37d6b2aca1e030d311dc9c2</pre></small> |
| | | Full Location | Monthly<br>2023-04-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>197.4MiB (207.0MB) – 3,267,813 rows – 243 unique countries<br><small><pre>MD5: 45d3670da1f2b31fcb68223a108be9af<br>SHA1: 37645fbeac5800a4ef57d4ce635fa5daa67ed21f<br>SHA256: d615d7817a3bbfdd4665c3bfccae8e6ae223c388323467fed143ca963313c64b</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>372.5MiB (390.6MB) – 3,244,362 rows – 250 unique countries<br><small><pre>MD5: 8aab3f0628a16d3290e30da4f527f4c8<br>SHA1: 19582f830e1b7052a98ed03d839aa97944679064<br>SHA256: 83e1d01ad2c49822595fcee1ca7abb10ae1c64dcd0ada5dff55cd46aa9ccd7ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-04-23<br>IPv6: 2023-04-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.510MiB (5.778MB) – 234,959 rows – 242 unique countries<br><small><pre>MD5: 2bba27a2b99c35f4adfcdb1e3f2c3155<br>SHA1: 29a4b09cccca77c92d517cb4a7be4b66fafc3354<br>SHA256: b0df0b763ec5f15501f89a825dfa85b591361850246e30260d46c2498145ea2a</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.42MiB (28.76MB) – 488,447 rows – 249 unique countries<br><small><pre>MD5: f754b5bde54b9a5d499f21e50664be91<br>SHA1: 638a2b52f5a21054aa3113b9a0b5d7cc9597443c<br>SHA256: fccdf823bfaa42d8f5e1b9338c57c955108fb976811a38544d113e9839da3beb</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-04-23<br>IPv6: 2023-04-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.9MiB (201.3MB) – 3,132,731 rows – 243 unique countries<br><small><pre>MD5: 3838c7e30ffdf6d0733a1183b8bc5f8b<br>SHA1: eabd91c83ed353e9c1772ef4c75790202a76b639<br>SHA256: 26f005f2f4c3afa282cd9a0622c8bbc26f7de72dcd77dedfa309adf8b89be8a0</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>382.5MiB (401.1MB) – 4,521,269 rows – 249 unique countries<br><small><pre>MD5: 84f8a06a23be4055c9018aad7e7e4024<br>SHA1: ff1af002a8f39309f8993c2c98f58478054f7550<br>SHA256: 0713b662001136ccee4d3f1c18f2c81c0615d7f3c0d2a1d536db02df4d676d78</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-04-20<br>IPv6: 2023-04-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.637MiB (10.11MB) – 410,763 rows – 250 unique countries<br><small><pre>MD5: 60058117a4dc1e70431ed847705e7382<br>SHA1: b13869d4923f6d3c5c1358d3235cf9918fad9b3c<br>SHA256: 43f0ab2702c8ffe573fe2f1aa8aced52cab2c1677cf23747496e1ee4033e4eb6</pre></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.10MiB (22.13MB) – 273,198 rows – 250 unique countries<br><small><pre>MD5: dd9a357ba119962f13c6da2828ff64a1<br>SHA1: 402015c971bd5c6390b3e2a9b8efab8f887c9926<br>SHA256: 6a4fb3fee252c5a76d5ac68bbe6abde0979084c120f092e7d4b9d3bd144cb323</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-04-20<br>IPv6: 2023-04-20 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.1MiB (199.3MB) – 3,780,457 rows – 250 unique countries<br><small><pre>MD5: c549c42a677db17df26968ba72b4217f<br>SHA1: 478b29d52e46b40ac5364af76b5f68fee361bd4d<br>SHA256: 0f94b00fb9b55cfa4c5a3eb6eae162a1a1e4c7f204360b0f2ccafa8eeaf956dc</pre></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.6MiB (233.4MB) – 3,780,457 rows – 250 unique countries<br><small><pre>MD5: 9b077b21a71abf166d34e4600d85deef<br>SHA1: fa437e667396b1c6ada695a540bce067093a0c0a<br>SHA256: cdd87a2280339005f4f62e5a751b870d3742c321980f0eeec0cbb98065e102f7</pre></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.7MiB (206.2MB) – 3,780,457 rows – 250 unique countries<br><small><pre>MD5: aa2161d37b3f39dc86f1386a647fc57b<br>SHA1: 48338f892824a26ad33d02b2b68563a98e2d4610<br>SHA256: d91347320143136f8e9df86da2b291c075974c90a265329185a341fa8bb03995</pre></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.8MiB (213.7MB) – 3,780,457 rows – 250 unique countries<br><small><pre>MD5: 066389f715afd13825737c1d38347fc2<br>SHA1: 26f4a93fe7972142e8f4c47bccff7949042478d9<br>SHA256: f46dcba0438b29e60fc1abe3e87dd09b9204f5d18f4da7df7aaff037b2b1d640</pre></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.0MiB (250.6MB) – 3,780,457 rows – 250 unique countries<br><small><pre>MD5: 785179bbd421230a939d0f0f0c5e7259<br>SHA1: c12890b99e9501fc3aa6db71a55adb6be9ee6cd4<br>SHA256: d2637856e49d43304a86c9acbb581a4acdb925fecb879660d7758a003e6bc16b</pre></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,780,457 rows – 250 unique countries<br><small><pre>MD5: 99fdd1c89f1e4a93aed41ed3bbb51e59<br>SHA1: 9c208d4a2036fad78318cd8f3cd55690673868cc<br>SHA256: ce0604c7a997b0dcb33ce07fd2716c38750d9dd06b509b3f68ab86ccfd2a2ff6</pre></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.9MiB (251.6MB) – 3,780,457 rows – 250 unique countries<br><small><pre>MD5: 690af5596f1ade865a3509c2c3ad4bea<br>SHA1: 716388625fb8d58ac38ab825d7ec10e552c0a72e<br>SHA256: 839e7108dc99f74209bb4775061648e46f2a016e83e61a165eab292b4e46315a</pre></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.6MiB (213.5MB) – 3,780,457 rows – 250 unique countries<br><small><pre>MD5: fa21a243d38ccc24884d1436c43fed7a<br>SHA1: bee8d0bbcdf899ccda6e9c2ced6bd7ad292fe3e9<br>SHA256: 4a292379e36fd2873d945b380aa41430201d5247a40c7ac10707b57e1e32ee39</pre></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>127.7MiB (133.9MB) – 1,273,387 rows – 250 unique countries<br><small><pre>MD5: 7a0d407cc0e042f7fdc7cb20bffcfa2b<br>SHA1: 40550db6b149ca3a6e4127120a1314db2a49d38c<br>SHA256: 3da65c49200f9a591cc61a2afe75f851018cfee27273c52a7db0aa672bec7b6c</pre></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>135.8MiB (142.4MB) – 1,273,387 rows – 250 unique countries<br><small><pre>MD5: ffb00610de8a5cb471bf463f5e585122<br>SHA1: 9fdeb9d2a62f40c2a87d4e3d7a500f6f7b49815f<br>SHA256: 0fa057c9fff0233878a1dd7764d61794d686dba7662be0ea33c00f20b898580a</pre></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.0MiB (136.3MB) – 1,273,387 rows – 250 unique countries<br><small><pre>MD5: 5bc7a951acadcee1264b43506f7cc4cd<br>SHA1: 49f267166a5033c76404a97c4b2c62870825fa1e<br>SHA256: e74973d89db92817b580e77fbb22afab1778671c6bb2101fa8935f998e0c217b</pre></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.0MiB (138.4MB) – 1,273,387 rows – 250 unique countries<br><small><pre>MD5: 32725bec1d3bbd9820c3dfbba2972a87<br>SHA1: db36a44f45da8300fd253080d3d475f9be3c0f61<br>SHA256: 75e8cef083bc9a9008567ecb9e69a6da453ff237d99f6091c367bfb6b3734a4c</pre></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.5MiB (146.3MB) – 1,273,387 rows – 250 unique countries<br><small><pre>MD5: b1aa7aa1dfb3165112527e7bd3c8eb2b<br>SHA1: 2f930095021d685d8d49a69ffee61ca5b897818c<br>SHA256: e2c7126be67c955a4c2fcccb3d5cf45698006de850b77e0a1602c5b2a6485bdd</pre></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.1MiB (135.4MB) – 1,273,387 rows – 250 unique countries<br><small><pre>MD5: 62e255d78be12b90dfd53db1ca7c04ef<br>SHA1: 0f26e7e0eaf1984dab59459287d0d6d68e6117b0<br>SHA256: 4d147dd2fcaae2216c6e0b49a46d9c20190d34b2f2b52da53c5c0dcd057e5d45</pre></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.1MiB (147.0MB) – 1,273,387 rows – 250 unique countries<br><small><pre>MD5: fff0fe5369bec2c8ab47259810f6bb81<br>SHA1: 6e8ce6271cb67192818f959700e0a6e58e3e0ba2<br>SHA256: f8c5a3af640572b566b1a462ab6557c5fd9e6cdb3536886086370ad00f9847b1</pre></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.0MiB (138.4MB) – 1,273,387 rows – 250 unique countries<br><small><pre>MD5: 531390d8611252b7ed92c62ed57fb38c<br>SHA1: 73e2021315b560f84262b2a082b494fc702f72df<br>SHA256: 33e2324acaec21721f3ca79019a9a5fd12ce49b6057f158a218f33a7d97d4a50</pre></small> |


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
