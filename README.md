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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-03-06<br>IPv6: 2023-03-06 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.143MiB (6.442MB) – 261890 rows – 248 unique countries<br><small><pre>MD5: 3ace2f120445a1bbd8064a9c7d3688e7<br>SHA1: a3041d72836313cddb8a81b886e794d3465afb37<br>SHA256: ccaff52a8d3277f1c5891eec2a5b9dff47e2e2b0cea204f355f47f3107e5085e</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.364MiB (6.673MB) – 82380 rows – 250 unique countries<br><small><pre>MD5: 1a60e5c4e40908756565b68da8a78655<br>SHA1: 588ab23e1ffdd02a516a29b71ebbb1d6bbd367c5<br>SHA256: 4da47afb499ef7734e632d581f082d13210142a7d365bb8dd625e89cbf3fc6e9</pre></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-03-06<br>IPv6: 2023-03-06 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.388MiB (9.844MB) – 399387 rows – 237 unique countries<br><small><pre>MD5: 1a899ffbb9ca04d75498964d8fbe37bb<br>SHA1: 4af61a4f9902434f63678c859d6b539d4f7da533<br>SHA256: 072d24167b2c1b1a296f5c9cb6db7f2f3b0ddb2186f76b4618951249b591b2b0</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.248MiB (7.600MB) – 93956 rows – 215 unique countries<br><small><pre>MD5: 72579a916a225e9c4f8475dead7e0d0a<br>SHA1: c45883065893b0b31eef06b9026ef1e36659696e<br>SHA256: c95e94aa998f14487179e4923783a0ca4edfc902d9abc3be24f8f8ecbd585369</pre></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>8.288MiB (8.690MB) – 354199 rows – 243 unique countries<br><small><pre>MD5: a1d21d8f62a7c3f50510147c0eb79805<br>SHA1: cef8203b2cf2c56e2822c08c0550fc06171ce759<br>SHA256: 423c8d8cf8a614b4d9fb63c2a49616497a8cc0471c81db5ede712e2e6bc234bf</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>27.50MiB (28.84MB) – 355992 rows – 250 unique countries<br><small><pre>MD5: 010e576eccbed46c235c9f1f40600f09<br>SHA1: f1295804bfa56f4fa5ef9842667b7cb0b9a0f0ef<br>SHA256: b07b46e8667f0b731e0478cb3dcaa3937b083138f4a8257cad27fa96d61a42a4</pre></small> |
| | | Full Location | Monthly<br>2023-03-01 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>198.6MiB (208.3MB) – 3293034 rows – 242 unique countries<br><small><pre>MD5: 688f39311d9ef3ae0dba52741233235b<br>SHA1: 52a53ef49218397baa93ef51035a1482140b4634<br>SHA256: e84aeb3244fc162911c5a436cc737fce85f6619f3e909a4b98b5ca4fa46ca9de</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>343.6MiB (360.3MB) – 3013737 rows – 250 unique countries<br><small><pre>MD5: a3926d0753e258e417a0b18a6d81430e<br>SHA1: 8a1946620f5f949f8a6274e1b473d30ae1b57025<br>SHA256: 2397151a392f426ac2facae01cfaa626480f5ad6d322c982304ec2b165ea38ce</pre></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-03-06<br>IPv6: 2023-03-06 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.187MiB (5.439MB) – 221425 rows – 243 unique countries<br><small><pre>MD5: dd82d9c419bdf8d65292298d4da9f4f9<br>SHA1: 4574ddf1c97bda6f9d825016c43005b9659612de<br>SHA256: 28145a84e26234645bd43bcf99287610ec6de00f1543d96a5704cdd74600303a</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.81MiB (28.11MB) – 472772 rows – 249 unique countries<br><small><pre>MD5: 5fc339accde85c2b539a6efba2f8b174<br>SHA1: 35049fccf4492a4eab673415d9814f7b38dfcea0<br>SHA256: 2715c4e3a5f98f963ebe5b71a0628cf1597145a8f1e82444d9831ad0d331ab50</pre></small> |
| | | Full Location | Monthly<br>IPv4: 2023-03-06<br>IPv6: 2023-03-06 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.6MiB (195.7MB) – 3084645 rows – 243 unique countries<br><small><pre>MD5: dcf12cb26141a65ac67b7630b5a635b8<br>SHA1: d453ffc842be214041820c134dd85e2974ce8839<br>SHA256: ae02057cfbe60a4cb423459a4e23f7203890d02d5461ecef35d0ca43faf578ea</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>374.0MiB (392.2MB) – 4456315 rows – 249 unique countries<br><small><pre>MD5: f3c102f8b4597403f757f4f87811aa1d<br>SHA1: 5143d96442128020b6a91dd2476fbf46cff231eb<br>SHA256: 11e03efe2ac1e72afde73d94a354137049a2531581c610190c1b8ded4123c619</pre></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-03-02<br>IPv6: 2023-03-02 | **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.659MiB (10.13MB) – 412072 rows – 250 unique countries<br><small><pre>MD5: a0628aec0fe646f031835b4ff58ffd02<br>SHA1: 3e47905cef60efa537a4f173b631d740f104aeeb<br>SHA256: dceb5e0805c02463fbfd651edf8bceaed66ab145cdf343c62719d11c7c401e09</pre></small> | **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.46MiB (21.45MB) – 264868 rows – 250 unique countries<br><small><pre>MD5: 336ae72c31c4770efd1b7de0370d7ccb<br>SHA1: 092a704750df62b8d1835005d5490ba496248c4b<br>SHA256: 8fb37ecad37c1ccc98a061616179645b50d92707c76d2392cedc80c305384bfe</pre></small> |
| | | Full Location | Weekly<br>IPv4: 2023-03-02<br>IPv6: 2023-03-02 | **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>187.8MiB (196.9MB) – 3744183 rows – 250 unique countries<br><small><pre>MD5: b7b1d663d0f32d43a3d3704b60324b86<br>SHA1: a7d8e7a86478aa8ab53dc3f0a73d17daca170a9d<br>SHA256: f87dc8714263315e0093758fd891c3669faca9a40b18ac3dbe1130322e80bd82</pre></small>**[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>220.1MiB (230.8MB) – 3744183 rows – 250 unique countries<br><small><pre>MD5: e5900737412d3e56054ca9a404462e8c<br>SHA1: a965e23800b1ec052c25770a151aecfbd2fc0bf9<br>SHA256: c68a46afa7294c80bc2e4eda49e166f3554229bcd79969204b8116359fba53b1</pre></small>**[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>194.4MiB (203.8MB) – 3744183 rows – 250 unique countries<br><small><pre>MD5: 57d17f0ae46e92a00253268fd95a1761<br>SHA1: b75a32a1fadb3bd7b0b2982d885d038b7dfcb7fd<br>SHA256: 596220006009bac02d3007731c6e5cab2cc617f17b314590bc242520d419c6f8</pre></small>**[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>201.4MiB (211.2MB) – 3744183 rows – 250 unique countries<br><small><pre>MD5: 5933a943481112d6de013cf67a410a2e<br>SHA1: 5a780f07a96cd06dc0d954166bff88eb41c818c2<br>SHA256: 1f637596731fdb067a64341226fbddf62715497fb5714d24105c692cd4815fe0</pre></small>**[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>236.0MiB (247.5MB) – 3744183 rows – 250 unique countries<br><small><pre>MD5: 644ebb4853b528009d6cd90159d827b6<br>SHA1: 76db714b49f2d1683d40480c3560beb8647f5e39<br>SHA256: f3597129c094ea95034bb614fb096217bf6f582412b152c6d03a24c4e441d385</pre></small>**[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>189.2MiB (198.4MB) – 3744183 rows – 250 unique countries<br><small><pre>MD5: 6a88e04e785c2816ff8f4b2d6215772f<br>SHA1: a106d8489036f04e8b14ad22ae6a1a5da6b827db<br>SHA256: e37f52e335a7121fdc0468c0cd5940b5741089a4d19189a5755c5b073d9d7f32</pre></small>**[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>237.0MiB (248.5MB) – 3744183 rows – 250 unique countries<br><small><pre>MD5: 93531149582963b91951ffb367bb896c<br>SHA1: 96c89ad70da7ad45411c23f53fd3e0d0cfd1d1c8<br>SHA256: 7c0120563b12fde3ab428b60986475af2b5d4d302801a51415ad8cefe1530490</pre></small>**[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>201.3MiB (211.1MB) – 3744183 rows – 250 unique countries<br><small><pre>MD5: 4a6015c025ee5edb67b7b769059f7cfc<br>SHA1: 7e220640d706f4c2e2c6ccd482daa82b99fe6e12<br>SHA256: 6ac519eea09a8677feef54b29f7d7009689065cfdb4781ddeff7e1c3ea01e179</pre></small> | **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>121.9MiB (127.8MB) – 1218807 rows – 250 unique countries<br><small><pre>MD5: 8d816924d1a69322d2e5e920e45d106d<br>SHA1: 07a2353e5215c6bd00629da1e0f242fa6bd8e87d<br>SHA256: 19da9b7f67f02dda445db7bfd56b6813cc7d1e11ae833aea66ff0693cc6d516f</pre></small>**[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>129.7MiB (136.0MB) – 1218807 rows – 250 unique countries<br><small><pre>MD5: 0be304ea7e2c78cc149babcbc08164c8<br>SHA1: 00e812ac433987b814584f35b4a3a6b63db5d022<br>SHA256: 215b5bc3add4688df250722cd6cdb353c5d9c6f7727131fc6a453232780fd3c5</pre></small>**[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>124.0MiB (130.0MB) – 1218807 rows – 250 unique countries<br><small><pre>MD5: 938c77025f58d57c198bd5f617c82d2b<br>SHA1: c24138923e62bcf2bbeb5547b1074d85183afd6b<br>SHA256: d332aa8d879981202bf5de054164e4f4f3e7addc504d4ab2558d53d730547503</pre></small>**[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>125.7MiB (131.8MB) – 1218807 rows – 250 unique countries<br><small><pre>MD5: 337b3202138d949949e07695eb6b7e56<br>SHA1: aef737025f4b54b5adbc1ae732ec98c40d4e361a<br>SHA256: 42154a7a65b8170186afeb070629375de88b0908b4d56a7f258765496e9d4e2c</pre></small>**[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>132.8MiB (139.3MB) – 1218807 rows – 250 unique countries<br><small><pre>MD5: 214cae776db9e1a1bc942eb7ff6d1c7f<br>SHA1: eaeeb065e859581399c64381d72b43531e4a80b4<br>SHA256: 59d6aaa407373e5570e52e83274ee8557cd3e4fd910c315422edf2d9d30adf99</pre></small>**[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>123.2MiB (129.2MB) – 1218807 rows – 250 unique countries<br><small><pre>MD5: b16bbf93c3c23f2a5c5fc4cc17f6c195<br>SHA1: 4a5acdcfb747498a182177a7e95a8f30adeff085<br>SHA256: 8ffaf2e67d7ae8d5b9d6c3fa286a70413f867138a0051bb492425409fbd1e9a0</pre></small>**[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>133.5MiB (139.9MB) – 1218807 rows – 250 unique countries<br><small><pre>MD5: 6a2ceb5fe679ffd0ed8071e92477937e<br>SHA1: 879aa70f8fcee4aea5dcd1ddba1ae9da42835333<br>SHA256: 54bdf6913bc44991614ac96786be5810158e7786e744bb42fbe24cd6e8266fa6</pre></small>**[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>125.9MiB (132.0MB) – 1218807 rows – 250 unique countries<br><small><pre>MD5: 906f5543dba278838a3c2c851dcb4966<br>SHA1: a06885dae96e23f2c1cc3b0ae81af3f008fb0209<br>SHA256: 148671a8cecafbf702b3774f1d7760d3d992f34e9ef8b01acb90085c0309a037</pre></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

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
