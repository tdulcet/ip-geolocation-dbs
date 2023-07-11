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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-07-11<br>IPv6: 2023-07-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.664MiB (5.939MB) – 241,336 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9f3e33d95dfa814c5816f619e225b64<br>SHA1: 3c9220412c05db73488c7815713a0e315fd7d023<br>SHA256: bed2ad6e80ae8d198600f5cc95e6a33e927bd2bb6c9ba2c87fb9a6734743422d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.543MiB (6.861MB) – 84,700 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee4ba1af1fe1c78aadc91df29a30a81b<br>SHA1: 852e97de79a893207c11882f77af2c85f74d28dc<br>SHA256: b2298a92a4e9d765f5b3c3488c2d1cde7982e3bfcbddee405f70c55b4bb90ef4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-07-11<br>IPv6: 2023-07-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.518MiB (9.980MB) – 404,257 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76eec0bc0c9061af54ee6ccc0408c597<br>SHA1: 9ec6ccbd32acfcb6723a3f6eac753ec62b16e694<br>SHA256: f12c283cd448a8fa081a216422e06a2f4eedd6cfd7c3408ab1dd6a69d0c981be</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.713MiB (8.088MB) – 99,947 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1c29254c9707ed4444337b7423c2925<br>SHA1: 5987d15c144d78018bb8274a41eeff869c09031a<br>SHA256: 6c3dfc33401b8e1c4bf0014b0546b87b379f0df0dfa31acf987328fba59c9c81</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-07-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.44MiB (15.15MB) – 615,660 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2cfb4968334ffe43017dde5d312493fb<br>SHA1: 353708035fa22c6f9e7f8018649d35a8066c6888<br>SHA256: 613b987eacab35b4632d20ad5dcbe90ef00f62d829a4f53a6bb58bb56068a5f1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>31.36MiB (32.88MB) – 405,965 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6a21d8e3505da7cd08559dd29da8248<br>SHA1: cbf95e10c541afbeed0118868c603cebc92b4a6b<br>SHA256: 1c1f34f9f84066329e2068dae7b7b47fe999626e100c782ea2fe870facffd185</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.175MiB (7.523MB) – 307,076 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f151f7f54b095b5ffda5d94059bb3dce<br>SHA1: f80142665d03d0371f800c5f959cf629ca3d8a10<br>SHA256: b490b03da5e813361b0ca08dd8f825c5991c8d4f9e21568776e4edd93746282a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.39MiB (25.58MB) – 315,780 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ccafe342cd0f83d168aa17033cc052e<br>SHA1: 18929b5d0a7ce12d7f3357fae4e283e3dd102ad6<br>SHA256: 55c042d3051eabf81b139c750768903bc3e9d8314dc416dc8b9ed715765677c2</pre></details></small> |
| | | Full Location | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,182,050 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3425f6eec44d17e75a144956ca9bedc4<br>SHA1: a6ae6d14f8e9a5705bee763c64c2bea6c879b127<br>SHA256: 9a1cffd22df1d59c077b7123b734f643ddf57a71c4d928ee793715e78400597a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.0MiB (303.0MB) – 2,522,649 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac831cafe688be22a072e63aeca50a09<br>SHA1: 8b579d16247db56f0e752f9c5566007ecce7b3c3<br>SHA256: f693430db94cf07b4b01343ab0d2e4ab2f16501d77f433b222ab16b8f015dcf2</pre></details></small> |


| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-07-10<br>IPv6: 2023-07-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.939MiB (10.42MB) – 423,844 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae9b12e118a6b9744adcbf1a48251748<br>SHA1: 7952c63d44f9c29816105cceb156aa76bc4b26db<br>SHA256: 168b9c2c71df3ac50a9ef91c11996101a500529673747bf1e9e52f6c0a76f7c9</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.79MiB (22.85MB) – 282,080 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 295c0b0bfd28a61f3f976adce11c8da1<br>SHA1: f903dd6da733de68d64b4976675a98076163671a<br>SHA256: 57dff2960005dfa8f0221bb0a62bb76c08708684065b59e9716615338a5dc805</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-07-10<br>IPv6: 2023-07-10 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.2MiB (199.4MB) – 3,786,786 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a265b339d8bf5d4fa1d9b0c659aec755<br>SHA1: 6fdf0575e3d8d5e79606e33a5094bc4cc9b25078<br>SHA256: 855e0f0a02ef3d5f37dc7a81462e7d203f6d51e94810e5311657848df1c95011</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.5MiB (233.4MB) – 3,786,786 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 263a9fa9560f3195d197b7a825ecd436<br>SHA1: f85b2e033a63de1f6c9f9d44fed5ee95ad993bf5<br>SHA256: 86e8f9b77e17104a02a0c9090eb13242792934b200b7177ceb4ec194580341b2</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.9MiB (206.5MB) – 3,786,786 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d313f122da0ec56b69a593d91e72e3f6<br>SHA1: f4631a2e5f8668ee162991c02be2a966cdc74964<br>SHA256: f3f341b0483be1fdd72a2c593e284f416f70bcb9ff1aac391cb7e402d0263635</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.9MiB (213.8MB) – 3,786,786 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 339d62b0cd00e24ccdb8a3cc51035662<br>SHA1: 76b59757dc5b204233683a7ed3a541b8b6fd5a27<br>SHA256: c8959918e356bb554ca7b54f3dc54c139739ca3dc7c0ada309cd180059fa2fb8</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.6MiB (251.2MB) – 3,786,786 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e616ba79aa86249967966e6c1782487<br>SHA1: 27a587efff1af786d7abe7bf47f72faff527c51c<br>SHA256: eb999fa4ee1a4758b2f8014df970ef57c208f63a42dfe07e603e6525422194c6</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.7MiB (201.0MB) – 3,786,786 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fdf07be95983835b38aa1c85b9789a56<br>SHA1: 99a84b8593698f6a6952e9f9fcb913ee75d2ec5a<br>SHA256: 6740f40065412906eab026aa9e786e0146c72770cf4f7cf4dfb344d4aa13caf3</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.9MiB (251.6MB) – 3,786,786 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c656ecccc64a631b213f92e4536707e7<br>SHA1: 5115533f4c93bd710d870971f6467ea0e443337a<br>SHA256: d936f233c7c19ff28715c8e11093de4cd3d64c6bf4747f0c18740f63fd03ef65</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.9MiB (213.8MB) – 3,786,786 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7dbe7ccabc4f179b5ce2f97025266340<br>SHA1: 853bf63b709b6c6e6f455c31bf4c44118f7f6073<br>SHA256: 1c60dca7e9b689e4954e3f5ce21fd0bc4bbb708e7dc526d9f451d6af4d908f94</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.1MiB (134.3MB) – 1,277,781 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1420a031fd94823c75b08b03fc1fa86a<br>SHA1: 323f260d5d947ab1fbf9f3b21b7f5d66a298539f<br>SHA256: 728c96d624c7d88571a23bf46934fb08ac9ec843d81692c181b866f8e85a53df</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.4MiB (143.0MB) – 1,277,781 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 602b7304b753b4552d0856e6c6ee9948<br>SHA1: 32466c0aa3a9820168d02cb15c6b02f1cc9956ff<br>SHA256: f3aebc852a9ee0b1344e52348e1ecbfcd4c84484aa0b8dccec8f0beb64ed7355</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.4MiB (136.8MB) – 1,277,781 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f691c6dc7fa1bfacb8138e7928b08248<br>SHA1: facf18c57fdf8ee706a670afbfde6403225f602b<br>SHA256: 11223a03cc4e3e195fd43e20f445aaf949ab1f24e5afa86a237ca0b89d3b91f5</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.3MiB (138.7MB) – 1,277,781 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59a77a35d719ae2c15747663eb9080c7<br>SHA1: 98b6bf294ba0a0b741e73b1cbc466f742b0684a9<br>SHA256: 5b6165795db80d4f97602039c12937e51702828417c5df17444c1ee746532949</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>140.2MiB (147.0MB) – 1,277,781 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e244bb2ad0d6130825e12bfe0ce94cf7<br>SHA1: d025ac69d501bac5be7217553c7353b11cf2a615<br>SHA256: f8dd145c61e5aba4cab62466c43a644fe7f4e821e5275108d22afd2af850cf27</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.4MiB (135.7MB) – 1,277,781 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33d60d9fe38c3a7e0d7584e247064a10<br>SHA1: 5c6c6f11ed6f9ec446616146e447f70cec5ccadf<br>SHA256: 8813e97461d261988e5d7e99ac84ee27aaeb22bc764bb81190eebf8826d9d0f6</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.7MiB (147.6MB) – 1,277,781 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c6630bfdd9b95a03301109e25d33435<br>SHA1: fe289bad882ce715507f66ccad87d64a6a263bc4<br>SHA256: 357b2416bcb82213f16dfa4ec103a053f7f61ff94058d54c1057f87ea610911e</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.5MiB (139.0MB) – 1,277,781 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b0d307e6128c946e628247b50a8e5a7<br>SHA1: 346275a738773f6229f9677bfe9abcaeff8a70de<br>SHA256: 4b0e35c79fe053ec6166f257a0073cda0ea90398d9ce5f6ec6eb847a9b1f60ca</pre></details></small> |


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
