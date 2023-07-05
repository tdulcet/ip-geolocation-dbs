[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-07-05<br>IPv6: 2023-07-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.657MiB (5.931MB) – 241,014 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a03a00c5dd923426ad6f56cc19060bed<br>SHA1: cd720a86a54f47ea5d715eefa9e2e5d34e828374<br>SHA256: b9708f9f50791a74aa1cff8ed15d7e5992bac21643c9164fb24f1287140347db</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.541MiB (6.859MB) – 84,674 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a60fc4e7c813426989404623ff3be00e<br>SHA1: 289793398b1d6f9b774c1edc30f330042814b1b1<br>SHA256: 0c5c27e77d8a44e23969631ec05c01a67da3a472a6a9738338849bde099f4889</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-07-05<br>IPv6: 2023-07-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.495MiB (9.956MB) – 403,273 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5cfb98db51e5d8a485b5a40d8cf6730e<br>SHA1: 98395a882d651fb331dec66b4f5180714278b848<br>SHA256: 61cc8f9d118877825a3414847fefadef1305c262b03c1552155526e822197a36</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.700MiB (8.074MB) – 99,776 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40dcf7574a4dc64c8c3cb1a0bac16786<br>SHA1: 895112f9eb650a0a8fd90d779c09e975051dd7e1<br>SHA256: 16d4524ac70ad6ad1b572a936606f91f40dd308932f0e6e5b3c494bd96d000bf</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-07-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.53MiB (15.24MB) – 619,790 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9612c323813af2a370bcfb430b13bb3f<br>SHA1: 6964da0096af151e02c2c301d8c23746bafd94e7<br>SHA256: 47496badb21506be236a823287c609a28c1a29095adeebf6165c59212f2d5c6d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>26.74MiB (28.04MB) – 346,157 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4c907f7539c364fd6eaaec79c24d77c<br>SHA1: f75647ea8647afe540dc4cc1c8f28348a46d5cea<br>SHA256: 02239bce2b87277119fb2a87b22b92443bdbbeb85ae8fb97dc03f5eb74d3f383</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.175MiB (7.523MB) – 307,076 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f151f7f54b095b5ffda5d94059bb3dce<br>SHA1: f80142665d03d0371f800c5f959cf629ca3d8a10<br>SHA256: b490b03da5e813361b0ca08dd8f825c5991c8d4f9e21568776e4edd93746282a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.39MiB (25.58MB) – 315,780 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ccafe342cd0f83d168aa17033cc052e<br>SHA1: 18929b5d0a7ce12d7f3357fae4e283e3dd102ad6<br>SHA256: 55c042d3051eabf81b139c750768903bc3e9d8314dc416dc8b9ed715765677c2</pre></details></small> |
| | | Full Location | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,182,050 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3425f6eec44d17e75a144956ca9bedc4<br>SHA1: a6ae6d14f8e9a5705bee763c64c2bea6c879b127<br>SHA256: 9a1cffd22df1d59c077b7123b734f643ddf57a71c4d928ee793715e78400597a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.0MiB (303.0MB) – 2,522,649 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac831cafe688be22a072e63aeca50a09<br>SHA1: 8b579d16247db56f0e752f9c5566007ecce7b3c3<br>SHA256: f693430db94cf07b4b01343ab0d2e4ab2f16501d77f433b222ab16b8f015dcf2</pre></details></small> |


| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-07-03<br>IPv6: 2023-07-03 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.856MiB (10.34MB) – 420,274 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efb57001c04e06eb19d38ebac6a83bb7<br>SHA1: 225334df10c090c9bb71c25330f6a352b1389093<br>SHA256: 6b28c5e5fc996e2c2d62b2b5ff57f012cf4c413ef48cf15bf011c1a63da450ec</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.75MiB (23.86MB) – 294,545 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9556a6194d4c8661970ee7bc3e3fb2fe<br>SHA1: 958cf301a4c56c3ce9a17143f6a8ee92106cef5b<br>SHA256: c112091dd561467001a8c6a44e3fe25ca9250fb410b7aaf1027b89d464e33603</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-07-03<br>IPv6: 2023-07-03 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>185.6MiB (194.6MB) – 3,699,373 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c9059c71005b3f4a04b43e42398b545<br>SHA1: 82c96609433a2c9b1ff168e5a7defc6cf56c1136<br>SHA256: 83818c7178f3e9545d4c53bc64c0ff8693424da2ba05aa92bc3fb1e42251a984</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>217.1MiB (227.7MB) – 3,699,373 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d467ea2d7facaaf2d0200dc9095c6171<br>SHA1: 920c17d0a077e5b69bbb453a35aa5f6583bf09f6<br>SHA256: 2887a9d924042c75fd9cc8005deebef2b20546ac7e792cd7b777b8921a1f5380</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>192.4MiB (201.7MB) – 3,699,373 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c30c85ff91a52b89b7bf321ebb5f2118<br>SHA1: ba8878dba23a13b50ae79cc03640d2e6be139b66<br>SHA256: c7fb54f5c40734288f5b02cdcffd9d2f5525b562788df589dcacd97100794f82</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>199.1MiB (208.7MB) – 3,699,373 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f23d04c5fdadd0eee0246ad82d57c23<br>SHA1: d41bfe62bfeaed59dcee52452cad235d01ce09de<br>SHA256: c076a64677f55244877fc848f5a4dd325ecb6edeff4ad205921143518b90d96c</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>234.1MiB (245.5MB) – 3,699,373 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b942b83a954b7bb47109d61df58eae2<br>SHA1: c20299ca37f96f740f72798092da6bca2288c395<br>SHA256: a8d8548dceae89f529b2b1fb4f9648d3fa259d8322968569a44de2fcbd3ae53b</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>187.3MiB (196.3MB) – 3,699,373 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e7f2373d4f1eab530c9c131bb0e70d4<br>SHA1: db67ad443b82e3e9f7487b6686847649b0750174<br>SHA256: c18c99bbf8437112d3cf6439eeaf0ef942c38a7eebe9bc3e51b3b53c565c3905</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>234.4MiB (245.8MB) – 3,699,373 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4aa5566dada2c8bc1e5d99b602dc884c<br>SHA1: 20f1cf5e217f4e4d75ff8da6f5541e720c00d94e<br>SHA256: fe9697e35cd01545effb9b465dd7b6c90a4080b0c79055049844323d136eb58f</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>199.2MiB (208.9MB) – 3,699,373 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e74fc345e9c65a7781d31e74738c0e27<br>SHA1: 8b3dad82964598f5694f3046ffa247b923576d5d<br>SHA256: 75e0c83114a158c742bda518394a3948f3f2a715ec94f57beb45e3df10734547</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.3MiB (128.3MB) – 1,223,802 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf8333601b2abb95cb16bff01cd469a<br>SHA1: 05f306bdcb53402871a691b3d270554215a3499e<br>SHA256: 400253de1616153245bfc7dbe6b2cd7644c5357f59c177d0d52379c21575ae06</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>130.0MiB (136.3MB) – 1,223,802 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 531115c14bf574777283f6ed064dce69<br>SHA1: f59bea7799bab1416856b27ec949dabb3038efb2<br>SHA256: 5c986d330fa464b9d818e1aadd37c429ccde470ab78927f17b656413f97f6c78</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>124.4MiB (130.5MB) – 1,223,802 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d0dacc12bb4f9d0b2d135f1747076f5<br>SHA1: 53bae6c44447d9493585f17796c61de29eead1a1<br>SHA256: f6c09b92ca2f45323ad807d3920c9504de4078230da8a1a32f12b2aecab56065</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.2MiB (132.3MB) – 1,223,802 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e52db8bff836bd0ef200225b74a671b<br>SHA1: a47fc9f689f21959d63ae3ef41470c56b2364174<br>SHA256: bc294079d397c659b4c5939619abce6c7450ba8e6575d955c931a5b692810a1c</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>133.5MiB (140.0MB) – 1,223,802 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d6ce73ea839ef7dbad8661f970b607a<br>SHA1: 654745f1a61633fdf4bbe91441f4a9d52f7f673c<br>SHA256: 1a279dbcc3292d8a2e36a0bf2088e8265aca7c879320dd41d602c664f1c8d2df</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>123.6MiB (129.6MB) – 1,223,802 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8efc302dc6fe394581641976af28a33<br>SHA1: 81f6596f70b55072f6305ab7bea3907b21dfec60<br>SHA256: 3ff8adbfc058a6123c2e7c93e57ab7e06b38ed98987cdef5d8887c6bec32ab3b</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.1MiB (140.6MB) – 1,223,802 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7dffb41f5bd0d37581ba9b2bfaef3ab8<br>SHA1: 8d5147162b198317c2a8a0bc99303d9bf1524817<br>SHA256: 5f9d64741f5b7316eb4aed5a715b89d06ccf6b49bf65c931c2a099c62a37a252</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.5MiB (132.7MB) – 1,223,802 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a86673f05c30aab1c1b03b3550c2bb3e<br>SHA1: 210d97fe15dfd101cfe558ebd5714e8f1b4e196b<br>SHA256: 769ef25bb01e6c040925d016b44030b018145a99634e918718a35ae71870b0d0</pre></details></small> |


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
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
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
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hex format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
