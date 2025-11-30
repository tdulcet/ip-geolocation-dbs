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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.425MiB (6.738MB) – 321,744 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc9cc3ec88d4a0971b314046b886ff0d<br>SHA1: 982aeb1bc91e432f695b399e089e2c7d1ffe47c6<br>SHA256: 12d107165cfc3850cae9a6ba0aefdf155d439b080cab24575d2289cb079070b4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.50MiB (13.11MB) – 189,953 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a762090bb781c02da5bd47fd08a6456<br>SHA1: 855451cbe8b9261c49a7c65719174baffe3e65b6<br>SHA256: 4f5e8ba5e2aa199c5e0645cc03d93631224e6f4577e1200121cf8ce3a80607de</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.770MiB (9.196MB) – 439,150 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c09d5840874d13e93bfc8162e0493a4<br>SHA1: fead287c53da66d737c2fd867af7291be81903e2<br>SHA256: 1ddfc2f84d6e84529b53b315655fdae64bde3f45bfd4757385a6b490a769b904</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.530MiB (7.896MB) – 114,553 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0fa1ece1c957417bf4b16ec9e2e96d2<br>SHA1: 17f4eadffc5abb9991722452a464f98fcbddb8ac<br>SHA256: c2b9dfede2df99a3966d3f4b7a1718290b2996b8ed579512862d08cf15f32887</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.20MiB (12.79MB) – 610,605 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 884e3879d41f0224c1c61b2a9300a264<br>SHA1: 0228af66cb4b017c2c83a1234e63396bf142504b<br>SHA256: f2c6902415739de4085521cc70813da6d6ab25cec27eb75849ab588039d2857f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.87MiB (78.51MB) – 1,137,802 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9519583fec72a6c5a612b4ae88a3872c<br>SHA1: 91cebef45db5a0aaa47a387fb62afbbff56e2575<br>SHA256: df9f6312b2510dc2e790b6ae348c730be8cf126b923279b245f22de2eef56854</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.010MiB (7.351MB) – 351,015 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b145553d436fa9927d6cee221444f00<br>SHA1: 843b7bc7470f77f7a70889bca7f0073e810cf0c3<br>SHA256: a8d289151b074c668255eb1d321a0c2c24a2aeb5d42f6061a293505dba1162ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.94MB) – 245,486 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e455a11648304abcd99f5c6bb19d7c56<br>SHA1: c3ea6f03fa4fee059c88a1910284305da803f248<br>SHA256: 8f4586e376e7d38e45f03f638da9bba2d90a84820ec5114e2ce10da9e7b87624</pre></details></small> |
| | | Full Location | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,722,991 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8adb14693f593577d9641386622862f<br>SHA1: 4789a341532d78da8e6b9fd9df61010466508387<br>SHA256: 18d6fa0beb7252dcb6684069fa602d39f95517dc0b4ee10bc0092ef22f72d867</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.7MiB (473.7MB) – 4,393,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fe48bb05d21d396bfad13d9ca53f98<br>SHA1: e1c547a5ade8b7c473d8429a89dbbb42b7a679a1<br>SHA256: 0b7ad446a98640e9d471aa376d976a1b332132350201538914192826c2ba532d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.203MiB (5.456MB) – 260,415 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f989c8cc1375a70628f443e2261e0b3<br>SHA1: af432c43217f88a47a1bb37aae3c998d08c6dbd8<br>SHA256: 7c52eb73078912571cf8d6c1c9b0fc2a8155ca61ebe8696533a62b7bd683fce0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.77MiB (23.87MB) – 345,962 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c7351f85cc8bf8ebbd09e872ca70449<br>SHA1: 26b5c97c8c1e786117813a94e1761f466338da33<br>SHA256: 7e5ee75145dddaae0c0ba1bbcc85b2581cf85efa4c5ec911b2b5be917f16845f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,012,447 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14972a135e393fd4070e78a15d5d3261<br>SHA1: d5dc58f3f923bd88ea1e5c331e171c885c687bd5<br>SHA256: 16bab4d2611d09c18b87bb7b5aa2baf1c02cb0ece3d5dfb6ec43f5284c1aab86</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>296.8MiB (311.2MB) – 2,877,050 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7858edf6f3f5863a2d75d78a638be99b<br>SHA1: 95f34ff240ac7dd9e679a1689742abd119dc431e<br>SHA256: b280aed124230c6c75d5f3f8ed64e2f3e757e31126f60c7fc0a853bd8de30ab9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-11-28<br>IPv6: 2025-11-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.41MiB (13.01MB) – 621,145 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c5a5efa68313c1f9a164fb2b236ec90<br>SHA1: 4048a2f5977e211d2e1db672ceb7fc16bf70171d<br>SHA256: 6d7e7922220bd3c7728792dc552d0df0a4f910c44c8e8cee6bb7e2649132a3f1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.53MiB (44.60MB) – 646,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccc69ea65bb3803422de701c0530dfd2<br>SHA1: cf95b7b9abd1e0ea78f40b07ed61f28fa757a118<br>SHA256: 53676db79f344e6d1afc3b3683cc524593d46cea5042a46368bf0b11b0e61f82</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-11-28<br>IPv6: 2025-11-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.6MiB (188.4MB) – 3,546,422 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce8f7be1da7f391159111ec28e404044<br>SHA1: e4b57280d76554d59abc1b9c44f4be75016ddd0b<br>SHA256: 1d147c028a16cf56ae7be1138f09d3c5279639acfeb7f5972cf0db64409d350e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.9MiB (200.2MB) – 3,546,422 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3777f139947d835a9a859b040551cc92<br>SHA1: 4cdf0627f37ca843f43f9a519d0c1d99c562ff1f<br>SHA256: 6514f5c5dfe9be35b39f2eb2e13acbf4e0b656bfc1d52a321c24a2431f9eac57</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.7MiB (187.4MB) – 3,546,422 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23d0c3b815ad8326afb0d6520b2987a4<br>SHA1: faaacd7872e388fe681439ca3d52bbab4deae0ea<br>SHA256: 90070f36e342095909465818a279ba9ff8030d44d3f9bec724c431136cff09be</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.6MiB (190.4MB) – 3,546,422 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 214f24f7d7c15cf6847b74121896dd52<br>SHA1: 46461bdb3fb5944ab89cc64c042aa9cd80dc3009<br>SHA256: f46ee22f0c10e9e33cf087065cc8d07ab1bc2496ecc22e848407fcdc24eac8ef</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.1MiB (238.1MB) – 3,546,422 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 515f0d2e0d2bcb4e540e6324fed9fd7e<br>SHA1: 6d8f3aff480a8c6945a66afd555279fc4836e1ce<br>SHA256: 6e12df3d5e08088863398f10af46f50f6f1190289d3216efdd5c9903c98ca552</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.3MiB (187.0MB) – 3,546,422 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8596540ada3bf8882ebf921b5bf4ba8d<br>SHA1: ef480501640e578f9e5b9bd7b3c651010a5eb1c2<br>SHA256: 369a2a2dafa73f8d7af72d691d2ac1766da148ee0cca9f83751a6b2b7fa1dcb1</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.8MiB (231.5MB) – 3,546,422 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4ebb2a82f33830cce9ccabce2640459<br>SHA1: 4f8b48cb5e2950a143de9473409f5cdd853b30b1<br>SHA256: 3926f7067d0c06c0470284209aa25b148aebc96b16e3d4dab61bdcdc30afd5d4</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.5MiB (194.5MB) – 3,546,422 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34cc63adf46d8034e865cc16fec3e43f<br>SHA1: de01a6036760878d1e0bf94264a25b3568b74905<br>SHA256: e8893753d4728d3d8cb035d6b16fb5e5e3d45fefdbe6d4f2e52df221179395ec</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>181.8MiB (190.7MB) – 1,916,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0701fdcffcea535d1103a08b59d9d769<br>SHA1: 153d2cbea8abf7dcd5b628c30dc9dcb1a4871461<br>SHA256: 8f17586afdf32e2661e0a71ccb0af43ff2268d426840c853a77259132bb38201</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>186.1MiB (195.2MB) – 1,916,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef86603cd698b0579712a87c29649ee1<br>SHA1: dfe96d6aa90996691a899ca11f6a8793a6e66a40<br>SHA256: 6f04b3a04bbe6e51a7f0a015dcdd06a3b1d540b44a49126b3c058663f0367952</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>179.6MiB (188.3MB) – 1,916,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05bd78a45d1e18db91cc284a7207d287<br>SHA1: a3a81b53b7d72d6a46be372b78fb0dc7d70b1aeb<br>SHA256: cedfca0b7c55b28825b9a83cc7ca8a8b928c96974a44914e9f22c12c155d1e41</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>180.4MiB (189.2MB) – 1,916,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94bcedd97e5c24301648f3a2ac697d95<br>SHA1: 8c18e4c611d5bd893d1ba0ff1089a24b1f4f99bf<br>SHA256: 60c77696167e8cb50fc156db6ecc50c237f5fdf4903f08616ca810fb86471a95</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>200.0MiB (209.8MB) – 1,916,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b8a6c8ceac7835e66f6e162e0c2bf0f<br>SHA1: aa2601d98e1fe3695f970ff9bcad1e86c3799857<br>SHA256: 387ba66cb2377949f5714c8d5370e150d235a9958042555fcc08eab792715c5a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>179.3MiB (188.0MB) – 1,916,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d091a0d51175cda08e50f648cc0b34a<br>SHA1: 19cf29b9fa1f388baa6b202a1589459f636cf2ce<br>SHA256: c989d19d405c3d138dcdaf6f6d756bef3fc64106cb884a022b7713f2603e6706</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>200.0MiB (209.7MB) – 1,916,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee5564a4350bb4b60679318f9c70b222<br>SHA1: f7d56f69241f6f4399151d7529150913c6a366e3<br>SHA256: b279125067aac638b327389cf1f76a6fdfff920e19acc262fb5b525203886c7e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>182.8MiB (191.7MB) – 1,916,495 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db600547e235dde9cb1f6ca7e5ed9307<br>SHA1: f740e741f47e91206c1cfbfc815f8af419ea2f73<br>SHA256: cadab00652503d421c8f8739f2521fc3c543e334e7c1e83d46c22cb476d8d5a7</pre></details></small> |


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
