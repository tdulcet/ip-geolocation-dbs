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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-11-19<br>IPv6: 2025-11-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.533MiB (6.850MB) – 327,102 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e0cbd2dd98d3a4786c37b8b6099d781<br>SHA1: 3fc906684a0be7e19cbdec68991f1ea38008f60b<br>SHA256: a7def1e115a265c07cd52d1defa6ddb1136b273572909f9773c394fb9e584152</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.33MiB (10.83MB) – 156,917 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f5b7778786f5142009ce26aaa251427<br>SHA1: 7c0260719e503df8e4d0da739e6704600982ace0<br>SHA256: 74a86fe3f5f4a1a9fb86f57bfaa3a035a5807203ce0e4b0a6e50a754cf585195</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-11-19<br>IPv6: 2025-11-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.730MiB (9.154MB) – 437,135 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a50b98e15582d14a6d63deec04ce5b3<br>SHA1: bc40626c4fdf36d0ae6fecf4f13b3e22b710015b<br>SHA256: 9dee0171ed0f440efa886979f21d8c3705c5f1798eb15105aeea520b5a8f6929</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.506MiB (7.871MB) – 114,182 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 516c4cb6e5199c74cbd75bf2bbde9965<br>SHA1: 3dada2869ae40a62811704da38fa2d382e504383<br>SHA256: 0af3546ebdc1232cb93238ae3a308c79b2f9e5d885da011a40f8b06566038c96</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-11-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.19MiB (12.79MB) – 610,479 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6be8005ef68ad566b77dc20fb93c708<br>SHA1: 83ef822f54b5683a91e579b9333277eb13f2dad2<br>SHA256: f3917fb3dba8b5201377631c36e429189ec4909c1c926a3454f09bf97596d5b5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>69.55MiB (72.93MB) – 1,056,913 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11aad40c150aca7cadb5473adab3a205<br>SHA1: c1d4296f70889ccc193037972380d90d58d39e00<br>SHA256: 6491e43e4b6fe6b3913e9b70956d20f3f3ca325853c2909ffa9c2406c9608316</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.010MiB (7.351MB) – 351,015 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b145553d436fa9927d6cee221444f00<br>SHA1: 843b7bc7470f77f7a70889bca7f0073e810cf0c3<br>SHA256: a8d289151b074c668255eb1d321a0c2c24a2aeb5d42f6061a293505dba1162ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.94MB) – 245,486 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e455a11648304abcd99f5c6bb19d7c56<br>SHA1: c3ea6f03fa4fee059c88a1910284305da803f248<br>SHA256: 8f4586e376e7d38e45f03f638da9bba2d90a84820ec5114e2ce10da9e7b87624</pre></details></small> |
| | | Full Location | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,722,991 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8adb14693f593577d9641386622862f<br>SHA1: 4789a341532d78da8e6b9fd9df61010466508387<br>SHA256: 18d6fa0beb7252dcb6684069fa602d39f95517dc0b4ee10bc0092ef22f72d867</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.7MiB (473.7MB) – 4,393,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fe48bb05d21d396bfad13d9ca53f98<br>SHA1: e1c547a5ade8b7c473d8429a89dbbb42b7a679a1<br>SHA256: 0b7ad446a98640e9d471aa376d976a1b332132350201538914192826c2ba532d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.203MiB (5.456MB) – 260,415 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f989c8cc1375a70628f443e2261e0b3<br>SHA1: af432c43217f88a47a1bb37aae3c998d08c6dbd8<br>SHA256: 7c52eb73078912571cf8d6c1c9b0fc2a8155ca61ebe8696533a62b7bd683fce0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.77MiB (23.87MB) – 345,962 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c7351f85cc8bf8ebbd09e872ca70449<br>SHA1: 26b5c97c8c1e786117813a94e1761f466338da33<br>SHA256: 7e5ee75145dddaae0c0ba1bbcc85b2581cf85efa4c5ec911b2b5be917f16845f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,012,447 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14972a135e393fd4070e78a15d5d3261<br>SHA1: d5dc58f3f923bd88ea1e5c331e171c885c687bd5<br>SHA256: 16bab4d2611d09c18b87bb7b5aa2baf1c02cb0ece3d5dfb6ec43f5284c1aab86</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>296.8MiB (311.2MB) – 2,877,050 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7858edf6f3f5863a2d75d78a638be99b<br>SHA1: 95f34ff240ac7dd9e679a1689742abd119dc431e<br>SHA256: b280aed124230c6c75d5f3f8ed64e2f3e757e31126f60c7fc0a853bd8de30ab9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-11-18<br>IPv6: 2025-11-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.42MiB (13.02MB) – 621,536 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c739b19b5f5f55770411cb4619bd09b<br>SHA1: b743e34c16fbd382fe38c1855ae2d9f3cbb71fb9<br>SHA256: e78cee1ee670fdcd39a8a4646a8549c9121c228175918047a605dd4cfab6fb0e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.31MiB (45.41MB) – 658,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac9c32b6729ab7132c9a55bcf8e8adf8<br>SHA1: e7c7ce14f14d2c8a711f01671dbacd06d833aba8<br>SHA256: ccf278197df479e7c844c8d9be32f8943a56369cfceadb279e3da8d56506ca6c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-11-18<br>IPv6: 2025-11-18 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.6MiB (188.3MB) – 3,543,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a52d46ea7f44d4df7985a9ae6edf1744<br>SHA1: c7bf8d6b23e3a143ad73eceb2ea6d02091a1c611<br>SHA256: ab8fe20432317f7c7d6c9424b2b839ae5f6986dcc884e0d16cb6805ce3aae419</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.8MiB (200.1MB) – 3,543,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51ec4304e680bb8bf644fd94c52e4b9a<br>SHA1: 94b1d5ded4877cf27fe2a52de30dbca173daddff<br>SHA256: 252eb23305957499f78812acae263f6eae16ef4f380b792a90337d56b58730d3</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.6MiB (187.3MB) – 3,543,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06eaa64cf6ceb484f795280d1b6c0076<br>SHA1: 87c33244e7a1b23d5c1845b218399433d9390491<br>SHA256: 6a0c6b611739c42709f39a06bb5fec40c3c00125dd81c6db70359335a2700086</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.5MiB (190.3MB) – 3,543,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9abcab04694b41ba33a3a80936f69318<br>SHA1: 21cd61a47205a2abb14890f32076a8cf2e4380e8<br>SHA256: a874855a0b57c42a241a9d6d913a10fc6fc7ad8dd3577100821d0642aa5380ba</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.1MiB (238.1MB) – 3,543,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1fcd28ec85ad942a13ef4445662f88c<br>SHA1: 4023ec23848f06132a7c991165e3e77134251e11<br>SHA256: e334207e16dfa3d482eba70e1f920e519775874371c01d20c66834a1c037a07e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.2MiB (186.9MB) – 3,543,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3c7009dc61b5fe6f0a729f0ab84f714<br>SHA1: b9aabb649dfa647b2ac7a25da9ef25d23f1c71ae<br>SHA256: 55a6766295e1cf8ea55a32342c32f89e0a2cd914d20e495d1b2409e21aa626ee</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.7MiB (231.4MB) – 3,543,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f63d191ba2b6009f45c7de1c911d6cb0<br>SHA1: 5c225cffb2206b60a3e218a3d24a8d9423b80656<br>SHA256: dc9bca18127cbf3ea9d645e96915a7861683653da1bc81587d17be91a6bb49eb</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.4MiB (194.4MB) – 3,543,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 711d70684bc40445622a299b687e91e2<br>SHA1: ebb33f561c8ed957e44a9503f4da00b204de8902<br>SHA256: e773b645fcf5ad8f1d8112b61652111cb41f64b8c170b35f20677464fd39438e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>184.2MiB (193.2MB) – 1,941,722 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b67470e58f0585ec7743445f6b1c41f<br>SHA1: c2b8637816d77e4c675f68cf4835227a1377eeba<br>SHA256: 39d2836708a9f542f67c35d29b13f9ed41b6d481eec46e6587302d1075c68060</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>188.6MiB (197.8MB) – 1,941,722 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4d4433cde9cb32fe0e09c6a7134b6cd<br>SHA1: 27dcaa33d0f36234eb7ebce7d008411e2571f22d<br>SHA256: 07db83f5f1879ccd51e017f35a26573ffa5dbcdf0e79f4231f1c61d600f98c02</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>182.0MiB (190.8MB) – 1,941,722 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 593c0661df1be7f3f39635d98e033dfe<br>SHA1: e612cee155491d49e1cfc2cb2e56aed397d06aae<br>SHA256: ad661df04bbe37925294320cc6bcc8cfe184c22dba90065b4f773cfddcde49c5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>182.8MiB (191.7MB) – 1,941,722 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b505a019000ea0e7d0f2b365457e50e6<br>SHA1: cff73027b4f65e3331ecb0f16e9a79c4cd912333<br>SHA256: aea97335c2207712cdbc93bb9aab0d126758d6cfea8f6cf27f2958d04c1f2d41</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>202.6MiB (212.5MB) – 1,941,722 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 562e9964cc0ea4be68005ee5d011b36d<br>SHA1: d5377ec02a64c02b42e7bec3e066525ff4403808<br>SHA256: 5c930970c18e3fe72918d08c82170e17de036845ca437e8d09eb1229179f1626</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>181.7MiB (190.5MB) – 1,941,722 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc1726211be36a9012800b08b99dfdb1<br>SHA1: 83f8c63bee948eebab09663f749218c86b1b328d<br>SHA256: fc4703e1e9d6226d33e6e5bac500a78dc4da82c073a01bea863b1b83f8f8d40b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>202.6MiB (212.4MB) – 1,941,722 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0180ed23b73beb990e4b9da54a027878<br>SHA1: d317da7161e5a98c31b299c5fe6354e4e30a1a43<br>SHA256: c9274dd25654638c630129303667e8a364a48e1e58768fb443d38798a2684d76</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>185.2MiB (194.2MB) – 1,941,722 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a03c548e98f205807387fc84bbbad9b<br>SHA1: ed2a6643303169da5b2a02dac1ee3311147b1c55<br>SHA256: dfa0ea4d6222618be1bca4dd36be1c5825879f60d80b498792cc6f78680a7a75</pre></details></small> |


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
