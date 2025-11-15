[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent TSV format with no quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases changed from [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) to TSV format and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than one day (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-11-15<br>IPv6: 2025-11-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.528MiB (6.845MB) – 326,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6dd9011b0169f8df9f561550088ac912<br>SHA1: cada73c190f1bbc282b2d8564dc8930bc0afc655<br>SHA256: ede6237284c93032bf1d03378c94c5e721f981b67f20a83d74f4ffd7f6d23878</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.34MiB (10.84MB) – 157,138 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8f961ff7d71ea488d810f14505f5871<br>SHA1: 333435e175a72bbb2f8c4c89298b3c105b80f5a8<br>SHA256: 1b4ed49b34e0dbb58b8357614f60ea034ccf711e842cc9eccd5d7c411978aded</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-11-15<br>IPv6: 2025-11-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.718MiB (9.141MB) – 436,505 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e0ed48935cbe096b41ea668a9006248<br>SHA1: 296822f5152c7c72c89399a1967c842bd0e0c0d5<br>SHA256: b2fd45e965868c14e6f373907fe65ee1b880686bd809d93bc790f6a193fb8f8a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.494MiB (7.858MB) – 114,001 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a306a37b46afbc981c5a3bfee200e7b1<br>SHA1: b6fd94f7c79e7f364dcdaff086b9af04e72092f0<br>SHA256: c4e66435d1b958129127c0ef59d65aa466e516f761dcdd4cfb42d946ea2a3fb3</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-11-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.34MiB (12.94MB) – 617,949 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca692d5efb8019d007092756ca9916b8<br>SHA1: 571922dcd6e0ee899f45f719741cb1d6068c4795<br>SHA256: cfc569d93ff869f685e26c561f80efc965d9caa7a7425eb36bcb536bf54227ac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>65.95MiB (69.16MB) – 1,002,280 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f10cfa16c7a311467078f54cd756ae2<br>SHA1: bb59059727f76112a020d97c6908b73f0f2a452a<br>SHA256: 74a27eac8e2a2a0e1031600ffc444134838430bc20b964d884730edaa5c5b910</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.010MiB (7.351MB) – 351,015 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b145553d436fa9927d6cee221444f00<br>SHA1: 843b7bc7470f77f7a70889bca7f0073e810cf0c3<br>SHA256: a8d289151b074c668255eb1d321a0c2c24a2aeb5d42f6061a293505dba1162ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.94MB) – 245,486 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e455a11648304abcd99f5c6bb19d7c56<br>SHA1: c3ea6f03fa4fee059c88a1910284305da803f248<br>SHA256: 8f4586e376e7d38e45f03f638da9bba2d90a84820ec5114e2ce10da9e7b87624</pre></details></small> |
| | | Full Location | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,722,991 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8adb14693f593577d9641386622862f<br>SHA1: 4789a341532d78da8e6b9fd9df61010466508387<br>SHA256: 18d6fa0beb7252dcb6684069fa602d39f95517dc0b4ee10bc0092ef22f72d867</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.7MiB (473.7MB) – 4,393,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fe48bb05d21d396bfad13d9ca53f98<br>SHA1: e1c547a5ade8b7c473d8429a89dbbb42b7a679a1<br>SHA256: 0b7ad446a98640e9d471aa376d976a1b332132350201538914192826c2ba532d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.203MiB (5.456MB) – 260,415 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f989c8cc1375a70628f443e2261e0b3<br>SHA1: af432c43217f88a47a1bb37aae3c998d08c6dbd8<br>SHA256: 7c52eb73078912571cf8d6c1c9b0fc2a8155ca61ebe8696533a62b7bd683fce0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.77MiB (23.87MB) – 345,962 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c7351f85cc8bf8ebbd09e872ca70449<br>SHA1: 26b5c97c8c1e786117813a94e1761f466338da33<br>SHA256: 7e5ee75145dddaae0c0ba1bbcc85b2581cf85efa4c5ec911b2b5be917f16845f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,012,447 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14972a135e393fd4070e78a15d5d3261<br>SHA1: d5dc58f3f923bd88ea1e5c331e171c885c687bd5<br>SHA256: 16bab4d2611d09c18b87bb7b5aa2baf1c02cb0ece3d5dfb6ec43f5284c1aab86</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>296.8MiB (311.2MB) – 2,877,050 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7858edf6f3f5863a2d75d78a638be99b<br>SHA1: 95f34ff240ac7dd9e679a1689742abd119dc431e<br>SHA256: b280aed124230c6c75d5f3f8ed64e2f3e757e31126f60c7fc0a853bd8de30ab9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.49MiB (13.09MB) – 625,022 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df13f4b08a5f319a71aa2a284468a54b<br>SHA1: 071c3969926239f2ef4f0568bdf99330fc6b885b<br>SHA256: dfe750506c2d42c37f860bdf8c1baf9497f6531a13b0aec8a90cdc7daf5b6ce3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.42MiB (45.53MB) – 659,824 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434cf168a95abd11c8440b17d964fa30<br>SHA1: f773510e69fd488752011a1eb20fecfc29199f06<br>SHA256: 0a7dc85f13f6280df8d6c4e76b5c04e90a04e58eb7c7f5e0dbc5f47a1a01978f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.8MiB (188.5MB) – 3,547,412 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 798f79f498baf148b30255bc5f39cd2e<br>SHA1: 8412ea231e2e38499a78f49f7539e1b92e5ae1cb<br>SHA256: f0f3172c2d467641cbadf8a019ed6f9e73bd44b395799be789e6572ed629b38d</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,547,412 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 170345081f292c8f9c56ab5a4001b929<br>SHA1: 636058d3cf47caac8db0ddff43eaadfc868c7f15<br>SHA256: f1bf02730fb83b2dc035c7bbf6a8e58408926e5fc6412b35c8081f759e7e7e56</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.8MiB (187.5MB) – 3,547,412 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c4b19afabcfe1eda39e429c22ccc862<br>SHA1: da61cc94e4dcdf5ee0f9161d49edcb6f8ef67344<br>SHA256: 26892ac2b2730b82d9d41e3cbc99dd555eb3731719d4adcb71b8dc851754a13b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.7MiB (190.5MB) – 3,547,412 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ec402be74461fe17d51861459cb8f1b<br>SHA1: dc25d6a3ddb1f2f5c0229715a05f48f96c5a5194<br>SHA256: 3431fab30314840163969bb84907b44507fa12f0597feb67a2412c3fe6631d54</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.3MiB (238.4MB) – 3,547,412 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3f733805c277ce6951d84384c7e3e32<br>SHA1: 0ad7ae4845adceab91047a1f413a3fa7452f9997<br>SHA256: 3c4968e059baf4f83991bb705681de0b90910e90905ba9418e4a4dcb2f17d623</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.4MiB (187.1MB) – 3,547,412 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4bb9a2b79718b5d81ca0f24a60de1532<br>SHA1: 4c6bc318a36b9bbb7232b11b573d2660b97c386a<br>SHA256: e2a5f01ff2f263d1f345ef9515ee61d50edfbe627e95913441466c1cfeb3d2d2</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>221.0MiB (231.7MB) – 3,547,412 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c69d38af68ba42e0137cb85a64f9c54e<br>SHA1: d6fb93c906883fd5f8c44743587a48bf7ac2d663<br>SHA256: 238ada8892887eea7835f8bb74f394d1d1267aa3bbb1bedd2fb174bed911d032</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.7MiB (194.7MB) – 3,547,412 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f16cc40f3bdd23231eac186b08373708<br>SHA1: 27d3477365e2dbfdd0c0e4fc08cda0cdd9814951<br>SHA256: 20b702db238554c400516677b32704f33c9ac7c42fb57794828a1ccd2dfc311a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>189.1MiB (198.3MB) – 1,994,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c11442b02839c62fc8c398b0f7cc4b0<br>SHA1: 941a1604e3745b303c68b947cd95ac11d3088f84<br>SHA256: 0c32903eb9be0e5b1fb70750d753c4a14e3cfb444472d3cd447575b728d5f1cd</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>193.6MiB (203.0MB) – 1,994,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe8f9b54117add7178c45659326ff8be<br>SHA1: 784f730b041bf00d52a9a4a343ca451d3ad92e4f<br>SHA256: 9fdf8a16a083b5e3745d4840d4f71882c98392935764c4eb50bcdad0251bce9d</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>186.9MiB (196.0MB) – 1,994,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5f6ba573c9cd2492edd595890a165c6<br>SHA1: 7a05aeabaa8b0625a735f7bc7b140dca163c433b<br>SHA256: 3ea3bb9d61c134309f6482a020e4c74648968e6b78f27426e5438b45b957c580</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>187.7MiB (196.8MB) – 1,994,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ff929b2a73c69fade9a140c918b1622<br>SHA1: 6edb2e6939221a1ea439408aed2d469757288a47<br>SHA256: 5061a1b0aec5cd7b783d25e0a40a630b285c48b709dc179d6cca85fdec289d0a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>208.1MiB (218.2MB) – 1,994,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00b5c052b9bdf98f7c0075bad7de6428<br>SHA1: b1f7e434a40d03fe36f6d7ea2da9808c0ab87082<br>SHA256: ad6ca669d5a0a6c0b8f7d44317b8ca6962ec568b058bb2ed4371ff7b9d1625ed</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>186.5MiB (195.6MB) – 1,994,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4be8a3fe92b0ab7c63b39fe66ee483b<br>SHA1: c6092ed6dc43fe3e3e1a6a2f91cd681750b2f4f8<br>SHA256: e3dc0399fd34a20d5d5586361b684f6ac4cc22b5000f7f59b3571da78a9c11e9</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>207.8MiB (217.9MB) – 1,994,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569a7292b770c569b0f7235b5a29256b<br>SHA1: ffe0395fb1d0ab1ad37d9097e1f6075495fd2564<br>SHA256: 0b971ca685114d106e1fd3c94ba8d14fd3f887d2ab0c14c249ea04a4ad80749c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>190.2MiB (199.4MB) – 1,994,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ab03e1bbcd608d5c96e83c726c74f35<br>SHA1: 99bbd1754efa9a76f5f521fad3b76c151a57b154<br>SHA256: e83f60294211e094d5d44e1d6ee546a38b3441583d8f009d0aaa75d8c0205935</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### TSV format
`ip_range_start	ip_range_end	country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in TSV format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### TSV format
`ip_range_start	ip_range_end	country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### TSV format
`ip_range_start	ip_range_end	country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country TSV format
`ip_range_start	ip_range_end	country_code`

##### Full location TSV format
`ip_range_start	ip_range_end	country_code	state/providence	city	latitude	longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country TSV format
`ip_range_start	ip_range_end	country_code`

##### Full location TSV format
`ip_range_start	ip_range_end	country_code	state/providence_2	state/providence_1	city	latitude	longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country TSV format
`ip_range_start	ip_range_end	country_code`

##### Full location TSV format
`ip_range_start	ip_range_end	country_code	state/providence	city	latitude	longitude`

Note that `state/providence` and `city` are blank for some rows.

## TSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `1000000	10000FF	AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `1000000` is the hexadecimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `20010200000000000000000000000000	20010200FFFFFFFFFFFFFFFFFFFFFFFF	JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `20010200000000000000000000000000` is the hexadecimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
