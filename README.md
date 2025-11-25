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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-11-25<br>IPv6: 2025-11-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.529MiB (6.846MB) – 326,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef6141cbe7d16d9a91188bd4cbe283af<br>SHA1: fc23d604dda6e17dfdc10ffd2177dc3aa0f1a8d5<br>SHA256: c606f7d0c5f5daf39a834f30969dd01d141c2b19c4ea688e757a18048c870576</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.32MiB (10.82MB) – 156,849 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfc6281d1cc437f5a9904877a8b2813f<br>SHA1: 0e5b5fbbbc213ff14f7fc79529a384825be355bc<br>SHA256: b8dd5cc5d2cfbb1c80b2218ce39b6c3b96b535dcf7cebd1c61eee8f889a1e049</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-11-25<br>IPv6: 2025-11-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.751MiB (9.176MB) – 438,160 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b967cf1545cbf07156d687801fd256a<br>SHA1: 32fc2fb87c276f6242c3fdaaaada0b0f56dd4a9d<br>SHA256: cae06e064f8c3850c3f06869c15262f50536483c7fc40656dcc0045f51a9031e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.518MiB (7.883MB) – 114,363 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e606126ba8df008c48aed9570cae890<br>SHA1: 4d1f2b7b9a13064bd619c077a4e7531eefdffbc3<br>SHA256: e823b0eed3c5036da9cc4f4b98347ba5fc09a66d9a391c33e80ec6f1c3412566</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-11-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.19MiB (12.78MB) – 610,360 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7de01e1ed06393c3a665734d37a908<br>SHA1: c73308ec8d5d2093e0a1e4ffc34419b5060da539<br>SHA256: 001c2cdce40a4f4026aa5131acc13287544a64811ed620e44b60f7154bf6c945</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.85MiB (78.49MB) – 1,137,477 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 439ff38eab3452736e216e0fc628ed45<br>SHA1: 34d2eb19d3f160eb68521c073d17372e54a6666c<br>SHA256: d8c278496bc8304c0081f1ba018213eaffe677d117a618e405df5d9c06248b7f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.010MiB (7.351MB) – 351,015 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b145553d436fa9927d6cee221444f00<br>SHA1: 843b7bc7470f77f7a70889bca7f0073e810cf0c3<br>SHA256: a8d289151b074c668255eb1d321a0c2c24a2aeb5d42f6061a293505dba1162ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.94MB) – 245,486 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e455a11648304abcd99f5c6bb19d7c56<br>SHA1: c3ea6f03fa4fee059c88a1910284305da803f248<br>SHA256: 8f4586e376e7d38e45f03f638da9bba2d90a84820ec5114e2ce10da9e7b87624</pre></details></small> |
| | | Full Location | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,722,991 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8adb14693f593577d9641386622862f<br>SHA1: 4789a341532d78da8e6b9fd9df61010466508387<br>SHA256: 18d6fa0beb7252dcb6684069fa602d39f95517dc0b4ee10bc0092ef22f72d867</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.7MiB (473.7MB) – 4,393,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fe48bb05d21d396bfad13d9ca53f98<br>SHA1: e1c547a5ade8b7c473d8429a89dbbb42b7a679a1<br>SHA256: 0b7ad446a98640e9d471aa376d976a1b332132350201538914192826c2ba532d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.203MiB (5.456MB) – 260,415 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f989c8cc1375a70628f443e2261e0b3<br>SHA1: af432c43217f88a47a1bb37aae3c998d08c6dbd8<br>SHA256: 7c52eb73078912571cf8d6c1c9b0fc2a8155ca61ebe8696533a62b7bd683fce0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.77MiB (23.87MB) – 345,962 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c7351f85cc8bf8ebbd09e872ca70449<br>SHA1: 26b5c97c8c1e786117813a94e1761f466338da33<br>SHA256: 7e5ee75145dddaae0c0ba1bbcc85b2581cf85efa4c5ec911b2b5be917f16845f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,012,447 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14972a135e393fd4070e78a15d5d3261<br>SHA1: d5dc58f3f923bd88ea1e5c331e171c885c687bd5<br>SHA256: 16bab4d2611d09c18b87bb7b5aa2baf1c02cb0ece3d5dfb6ec43f5284c1aab86</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>296.8MiB (311.2MB) – 2,877,050 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7858edf6f3f5863a2d75d78a638be99b<br>SHA1: 95f34ff240ac7dd9e679a1689742abd119dc431e<br>SHA256: b280aed124230c6c75d5f3f8ed64e2f3e757e31126f60c7fc0a853bd8de30ab9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-11-21<br>IPv6: 2025-11-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.43MiB (13.03MB) – 621,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a5ba6d7acf40edf17927111207a3624<br>SHA1: 32b8025c73a2e5bd5ffdb539fbd1c039211530de<br>SHA256: 522db3409bdd516bd9ff265b95c4afa2903a9052a2c94eb9e29286ab4d36d469</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.22MiB (45.32MB) – 656,796 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5faf92e8c0270bbadcae36affb68e9a<br>SHA1: 3363da7c79707c8696d4c623ae1c09e9cd60d6f0<br>SHA256: 122dae54b5cc8760ef86d02e163c5bbb1cc53603154991fa657a0b04425a991a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-11-21<br>IPv6: 2025-11-21 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.7MiB (188.4MB) – 3,545,652 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47a6ac84579c2657ed99384f9b8cab06<br>SHA1: e5b3f508dbade3f1a3427093e0b916b25b9a4ffd<br>SHA256: 94c701c1a711d0e9f63e13a495bdf73d462e4a962665b3a3f7ba5b26ed478775</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>191.0MiB (200.2MB) – 3,545,652 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c40e4660d8666c8537ec26ed9595c807<br>SHA1: c55b89632b7f138d477a16a732b1a8d0aaa1b561<br>SHA256: 1dfa6015ec3fb90957d8a2f565e987fe2fa49b1fb1e1ddb279aabed1f1756fca</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.8MiB (187.5MB) – 3,545,652 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6110ffd467449743d2df6bb997f0954a<br>SHA1: cce0b2ebc3d72237c5ad0741613144be6cb15644<br>SHA256: 34c62c3655afd04e1ed5f46f979786d33b943b6a1bdc7e13799657c6e0f72f7f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.6MiB (190.4MB) – 3,545,652 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d8c6e1727886c5a5c73afe33d58fc93<br>SHA1: 384034361a45afabca09606d80a22451ed49aef4<br>SHA256: ef50046d63c8e29bc0c40089d784367674ec672c258a24e963b79525f8ca8545</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.2MiB (238.3MB) – 3,545,652 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32941eb9b4f09fac2f3e5c8cdd1ca0c2<br>SHA1: 8a4bc6a336a4151ed3ba8d1f79d55fc09c558864<br>SHA256: 1b3d6529d2d45348c887368f75f23271003001c60c6b38233a7c62592a6b265a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.4MiB (187.0MB) – 3,545,652 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 836745a3ebd870347d91c8e7cecf4e50<br>SHA1: ff10996f49210a33396b5f8fe63a96df3fdf19da<br>SHA256: 6fadae58e71b301ec38afe5f6bdd78a5b3f90b13e62abd22a98bc668c2af233f</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.9MiB (231.6MB) – 3,545,652 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c98cc2824a7c12508f3c5d754a89514<br>SHA1: bf294795009c615305554d5ba7748d467c8174e6<br>SHA256: fbf59f2d2c874c0e6b29f0725227a849d3ec11acb5e67a12f85e90805a807fb7</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.6MiB (194.6MB) – 3,545,652 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87626477d1c9ddcf251214cd9e2b7449<br>SHA1: c48580a63fc7654a8d5ba08c461e52b4ee9c3740<br>SHA256: ee07dfa34700fa2eff1c7d0086b8dfc2372181bb1f5a6ed7753cbe95996fa5a7</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>184.3MiB (193.3MB) – 1,942,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bea645188ef8d41006af0cb4e68ab26c<br>SHA1: b10404a82d2b04edd141400b5f8c0bdfdc2a6d30<br>SHA256: aee1d3e2af8f3839284d62a7082aaa3ce38693a3a45852a26cb8f6d6c8653a25</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>188.7MiB (197.8MB) – 1,942,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3c8b652b9763668404637462260638a<br>SHA1: 020617a5bb4dcfe104f6e71b4b8cc3bd77774f67<br>SHA256: e1f33f652d43fec4def154d10ca5d8b733002dce0e9fd6784fc707ab942d8ad3</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>182.1MiB (190.9MB) – 1,942,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fce91ee9d4e3ef8edf3294f6e075a0f6<br>SHA1: a874e3f4a762878a38589790070e6a9c02f134da<br>SHA256: 7fc29a7c102a49cd02a8283c29c4fe8ee2c39d8bfe7af39ff84385b74056c137</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>182.9MiB (191.8MB) – 1,942,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43fe80a4e8a84fab88e5ea27f46785bc<br>SHA1: 6ddd17d410fdf0ef6182c3c8ba81473ac0f520bf<br>SHA256: 30a5d6f4a21b606ca3cb5f497ede59c401b68486f294596abc9774515ef5041e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>202.8MiB (212.6MB) – 1,942,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6cbe271e37b58d75bbce094e448e21ab<br>SHA1: a2206617d1526e6b74e6d78161d6efbd7cc7e56e<br>SHA256: 27fb1ec62c0b78906f6d86f8c55804393c229605273810a7e7a25a269a95ee16</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>181.8MiB (190.6MB) – 1,942,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11f73bfad9658fcc15b405d2a8dfa313<br>SHA1: 6ea9b696a0ebfb9e312a236327469e17bbb007d3<br>SHA256: 12d95095bc530f3beb1af51f7faef4d911ca1ccfbbd461136fb866b23f2762d1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>202.7MiB (212.5MB) – 1,942,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 217df566c4747e1f89a5e229807c7fd0<br>SHA1: eb90e6e3e981d151a93b92bd1e42bee0212eebaf<br>SHA256: bfe911a456c3d2495ea9930ef3bcfd98fdc8a46a0a8c9afc30f70342a37fa2ce</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>185.3MiB (194.3MB) – 1,942,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6591519869b1321c553e49d8e95c2121<br>SHA1: 3197e902d5e1ce11805f72feee37834a1dcd434c<br>SHA256: f5b4b5a7f52024748168f556f5cbece2fad6b77f4cd258851b013c777ce050f8</pre></details></small> |


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
