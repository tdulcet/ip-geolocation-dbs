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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-07-15<br>IPv6: 2023-07-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.667MiB (5.943MB) – 241,468 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6139b2a55fe6adbabac74a517ed0a6fa<br>SHA1: a1cd5a64d6896b517b1e6e4ddaf7ee4755b803e1<br>SHA256: 4eabfae3424a8ee504dc10175b89ecaecd683a9583333850374a4597b23b6a3b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.543MiB (6.861MB) – 84,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 849cbd95ca680804455ff9b924e2ed7b<br>SHA1: 89b7cd8c021eb5a859f01035bedd4b16f5f0ca3d<br>SHA256: cbc7a18978749d569ade3f2a1e5b42eb4cdf589c6c07f8160a719473af0c0c51</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-07-15<br>IPv6: 2023-07-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.514MiB (9.976MB) – 404,107 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3346fa027be723265dba06899680e23<br>SHA1: f01692e782915cf96d5540303a3ed82058b82732<br>SHA256: 67a326f6521e17f8c789ff37d537aca5b43ae09b62e3fd9a903ddea40a7434fb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.731MiB (8.106MB) – 100,177 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 097701855c2e4f1c46fccd805dcc1414<br>SHA1: 536c8f828821856453aec4bae9c7093ba0859757<br>SHA256: 1fe3eecc93a21994103640583901a01b43ac0ac911b9c548323d75620d83c4ac</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-07-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.50MiB (15.21MB) – 618,872 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb81417868f347df6195110e5b8676be<br>SHA1: c6300aba37da5e4cae6532035be8bbbc67beeea0<br>SHA256: 96d77b9d2a9202f437efe74190dbbefc7723761c157dfbb92baae35155dc036c</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>69.47MiB (72.84MB) – 899,294 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 987a8e6050c5e9e90516fa2bc986ab52<br>SHA1: 1f710e0cb93890628421c5a6878bf47b873fb792<br>SHA256: a5df9d88fcc4e0215d458f2993577e997d00f050da21e499338d28ff4f3400bc</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.175MiB (7.523MB) – 307,076 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f151f7f54b095b5ffda5d94059bb3dce<br>SHA1: f80142665d03d0371f800c5f959cf629ca3d8a10<br>SHA256: b490b03da5e813361b0ca08dd8f825c5991c8d4f9e21568776e4edd93746282a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.39MiB (25.58MB) – 315,780 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ccafe342cd0f83d168aa17033cc052e<br>SHA1: 18929b5d0a7ce12d7f3357fae4e283e3dd102ad6<br>SHA256: 55c042d3051eabf81b139c750768903bc3e9d8314dc416dc8b9ed715765677c2</pre></details></small> |
| | | Full Location | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,182,050 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3425f6eec44d17e75a144956ca9bedc4<br>SHA1: a6ae6d14f8e9a5705bee763c64c2bea6c879b127<br>SHA256: 9a1cffd22df1d59c077b7123b734f643ddf57a71c4d928ee793715e78400597a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.0MiB (303.0MB) – 2,522,649 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac831cafe688be22a072e63aeca50a09<br>SHA1: 8b579d16247db56f0e752f9c5566007ecce7b3c3<br>SHA256: f693430db94cf07b4b01343ab0d2e4ab2f16501d77f433b222ab16b8f015dcf2</pre></details></small> |


| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-07-14<br>IPv6: 2023-07-14 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.32MiB (10.82MB) – 440,334 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2dc1cd2807ccbecfcf7fb4919182bf6a<br>SHA1: 6f57a2bc2863b5815d6e3e3d8f04ef8561fd4e5f<br>SHA256: ecb3e90cc42d6da491faccac006b05c20b5fb00c997806e27bb98b61cbf1ec87</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.74MiB (22.79MB) – 281,417 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d25e32e0e09f6e1ecb555528f8c199c9<br>SHA1: 8c9b70bcde9c996aba028c16c56c697e13c06b17<br>SHA256: dbc33429bcf6a5e3aed2784660421f807cc421b6d3cc75b2b496aa3bbdf3db1a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-07-14<br>IPv6: 2023-07-14 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.3MiB (198.5MB) – 3,776,036 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 527a90fa0a802cb271e2f0317926e57d<br>SHA1: 09b5d3e13a7b5ba7d31386f22730af341e96c9f9<br>SHA256: ce6be75391145e247a602e1cef4ed195f198f577c27b9eb37278dd7b29616e88</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.5MiB (232.2MB) – 3,776,036 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 235285dda37f7c9df8bdb26ec7327cea<br>SHA1: 5b8db1e5e38c796578c5e744cc83f36b4fb9f950<br>SHA256: 541fb5d49a8e06f6d6052b0f0afe3a6c3bc89ead042c7d2f0d8ce907d47a52cb</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.1MiB (205.6MB) – 3,776,036 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fea771237054b5b54909d0f42a143d3f<br>SHA1: 90cf6c001dbfbfb1104e971169434bf5c8fc80a5<br>SHA256: bfa613e7c40b604c6f749575321ba406b12b4d30d1fbfc6b3ba45a2c434bc600</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.9MiB (212.7MB) – 3,776,036 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a4d422ca4e1d865595689c1840a1e0a<br>SHA1: 8501c0df7493873355464023c2140e2544342a27<br>SHA256: 44c750c52adbeaf4519c453282b0e8d7410f02ace27ab1144b075ff136d88dc0</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.4MiB (250.0MB) – 3,776,036 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e2f94a5216e7f67df8f43ea0a96c5ef<br>SHA1: c76de3b0fd567cb679b0602bbfabf6e26cf355c6<br>SHA256: 714bc94a261f95f2992fe55694b0b7688bf4ab98cda0b29251fbf2d48b25702b</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.7MiB (199.9MB) – 3,776,036 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e74e4bdda1c1be251d46427a55ec7f7<br>SHA1: 492964eefb6d1d38c434b998ad36beb077f22d2c<br>SHA256: 4b3cd1bb828a2fc2a7aa7725d67ea23b951c95bfff476f139633e85ebec9150a</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.5MiB (250.0MB) – 3,776,036 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92e7318b6cea949136f756757212c0cd<br>SHA1: 2593ccb15ad2056e895b746d6a5b8c2b272d6033<br>SHA256: 950c5bc6823034bbffee9c518c4c8e2f7b83aa0e6e4d88563b1fe8b5a396e81a</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.0MiB (212.9MB) – 3,776,036 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 916e70034072c9560eaaaf4dd13b3d78<br>SHA1: 55ac56cccd31370ba119fcdfce665adb4382d58e<br>SHA256: c12db1bd016f11d9e6616a47116e25b486a4ca2716ae134430215825b87224ea</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>127.8MiB (134.0MB) – 1,275,323 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 249031ee363a73b4d70d98ceaaaaf975<br>SHA1: 81ab1952a5442ba535b5c08c2c168e72abb6f5fb<br>SHA256: 933b4415010eb9aea8448ef61513bc0e3d2e14256b1e65e43fccd545c8162451</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.1MiB (142.8MB) – 1,275,323 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f5ee580f238dfcdfb13f7afddbdc332<br>SHA1: 9a75a73d149322389245cc338a39a87dd8c48d5b<br>SHA256: 6afe2a02cba1aae835e88dad11af5740b24b6f5eb162f971812fd2794228b64f</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.2MiB (136.5MB) – 1,275,323 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc3f2181a6c638730694fb86597a000b<br>SHA1: e36000e311191e030657c19dd296ccdd91e2a9eb<br>SHA256: e3d7061993a88a214d0849a6c3c1ceb0162c61fc0ad5a56f3715b3de8ba6294f</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.0MiB (138.5MB) – 1,275,323 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7863ca7d4129a492155ccf542b299cfa<br>SHA1: 1a8d25cb54768a30a29928807cb44f7e488fce8f<br>SHA256: ea691b5cf909403f12073caaa6b6a5642b8b7347a438468738bd56e6c7c0b4df</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.9MiB (146.7MB) – 1,275,323 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e32cc7a910c8722e8d1ff0499a1feec<br>SHA1: 1af9bf7468d9519b177fb78a9f3b780bc488bdec<br>SHA256: 60bb586b3dd050378490a665e69c83573bccd593abc523bcb8d0ed98d160f8d8</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.2MiB (135.5MB) – 1,275,323 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e62d8311fea4f7876eefed3232ab8b34<br>SHA1: 13cdc9a8712be015c6ab045d5ef7cac89d82b907<br>SHA256: 052a041a9961cc11ecb74122e3589b7320aad2ad0f288497545740ab6e70573a</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.5MiB (147.3MB) – 1,275,323 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b316020a6a540816881e75794691350<br>SHA1: cca00eadc3a5fd40c6f70a7ef67c967455141641<br>SHA256: 9a61d5280fa0e3120252071234ff154c723f323ec87d3da6879a45eb350511c7</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.3MiB (138.7MB) – 1,275,323 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca6abfe097ff811c2bf8ac315ca3b8b5<br>SHA1: ec308da362e819f3613a3dfaec39ed0ed944beee<br>SHA256: c2e76f29af5becd487dbc9758ac5cef48c5497cd4d12a395adfcbbe7cd10a606</pre></details></small> |


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
