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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-11-26<br>IPv6: 2025-11-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.380MiB (6.690MB) – 319,463 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3693904befb9dff997554c805416955<br>SHA1: 7ee4c750216ab45e932fd340182cf5d1d966c422<br>SHA256: e889a7e0d4bded4509924cdac2e92d1250baac06deef65036f3ae04c37dba8cd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.10MiB (15.84MB) – 229,512 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e4e19c4091e989a41805b6194487467<br>SHA1: 70c513b011a8ba5305ac68f69df5fcbbed30b1e5<br>SHA256: b99398f70135b7b412e9fd5f72ed801f0cfc80f762d19f34753d6c507244a8db</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-11-26<br>IPv6: 2025-11-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.757MiB (9.182MB) – 438,465 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4bdbf7b264a7471f6d991fe6d23dd67<br>SHA1: ec096180f6e1531bee18a138264a9f4374f528c3<br>SHA256: 707c54a496aef79b9d3ab7b69877378bc6749f33522fb696b33045d7188dea00</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.515MiB (7.880MB) – 114,321 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0703db8f822419d37e80280d45482b24<br>SHA1: 6e32bc5df18b9000304b1732c04952cebd603435<br>SHA256: 5b665d605f52d6e01be63ecadec6ea3bf6e2d0752deb939a2488bef57428316e</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-11-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.19MiB (12.78MB) – 610,360 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7de01e1ed06393c3a665734d37a908<br>SHA1: c73308ec8d5d2093e0a1e4ffc34419b5060da539<br>SHA256: 001c2cdce40a4f4026aa5131acc13287544a64811ed620e44b60f7154bf6c945</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.85MiB (78.49MB) – 1,137,477 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 439ff38eab3452736e216e0fc628ed45<br>SHA1: 34d2eb19d3f160eb68521c073d17372e54a6666c<br>SHA256: d8c278496bc8304c0081f1ba018213eaffe677d117a618e405df5d9c06248b7f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.010MiB (7.351MB) – 351,015 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b145553d436fa9927d6cee221444f00<br>SHA1: 843b7bc7470f77f7a70889bca7f0073e810cf0c3<br>SHA256: a8d289151b074c668255eb1d321a0c2c24a2aeb5d42f6061a293505dba1162ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.94MB) – 245,486 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e455a11648304abcd99f5c6bb19d7c56<br>SHA1: c3ea6f03fa4fee059c88a1910284305da803f248<br>SHA256: 8f4586e376e7d38e45f03f638da9bba2d90a84820ec5114e2ce10da9e7b87624</pre></details></small> |
| | | Full Location | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,722,991 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8adb14693f593577d9641386622862f<br>SHA1: 4789a341532d78da8e6b9fd9df61010466508387<br>SHA256: 18d6fa0beb7252dcb6684069fa602d39f95517dc0b4ee10bc0092ef22f72d867</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.7MiB (473.7MB) – 4,393,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fe48bb05d21d396bfad13d9ca53f98<br>SHA1: e1c547a5ade8b7c473d8429a89dbbb42b7a679a1<br>SHA256: 0b7ad446a98640e9d471aa376d976a1b332132350201538914192826c2ba532d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.203MiB (5.456MB) – 260,415 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f989c8cc1375a70628f443e2261e0b3<br>SHA1: af432c43217f88a47a1bb37aae3c998d08c6dbd8<br>SHA256: 7c52eb73078912571cf8d6c1c9b0fc2a8155ca61ebe8696533a62b7bd683fce0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.77MiB (23.87MB) – 345,962 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c7351f85cc8bf8ebbd09e872ca70449<br>SHA1: 26b5c97c8c1e786117813a94e1761f466338da33<br>SHA256: 7e5ee75145dddaae0c0ba1bbcc85b2581cf85efa4c5ec911b2b5be917f16845f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-14<br>IPv6: 2025-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,012,447 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14972a135e393fd4070e78a15d5d3261<br>SHA1: d5dc58f3f923bd88ea1e5c331e171c885c687bd5<br>SHA256: 16bab4d2611d09c18b87bb7b5aa2baf1c02cb0ece3d5dfb6ec43f5284c1aab86</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>296.8MiB (311.2MB) – 2,877,050 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7858edf6f3f5863a2d75d78a638be99b<br>SHA1: 95f34ff240ac7dd9e679a1689742abd119dc431e<br>SHA256: b280aed124230c6c75d5f3f8ed64e2f3e757e31126f60c7fc0a853bd8de30ab9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-11-25<br>IPv6: 2025-11-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.40MiB (13.01MB) – 620,841 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec3c32520d29e64a5a7a677e26110f2a<br>SHA1: 76fa2c3ae4a4f805397f48fd4d4cc78e7e91e999<br>SHA256: 48a30c5750482d72d3d45a6972f090194c18ce4a099961461cd30fa90957fb60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.51MiB (44.58MB) – 646,063 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d715b812cfbad910e9b242eba983ad2b<br>SHA1: 9ecfa5a444b5af93b46b9f8bcd07e985e65c37f3<br>SHA256: a40130dcff9608ad9a40b8c3cdbda9719253c5c960996a2045c44575fc9f7778</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-11-25<br>IPv6: 2025-11-25 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.4MiB (188.1MB) – 3,542,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c166364ee9d8333178e9dab4dab85a5d<br>SHA1: b826e3190dc02f1c3fc6f1ab9f8b859fc40251e1<br>SHA256: 1b13c794b184b79a4e1ce04360a17d3ac36bd299035e9433f6c1629bb40b1652</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.7MiB (200.0MB) – 3,542,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14ea5e5d150668286de989d3406acbb8<br>SHA1: 42365fbf9acc6add15a062bd7cc4b36c0c5ee751<br>SHA256: bc5ff4380826da5361e58b0a737e86f41c0a48c8f514a6ed639a67bb076e5a8f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.6MiB (187.2MB) – 3,542,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: faaeea6c5bd08523485b0a70db2ceb71<br>SHA1: 28f27d339b8da7c4458a5e9a2a7da02122f79ee1<br>SHA256: ba679c5a2a310419655ebdea15ca394e0931c390e9a192d1ace8fd95185c0650</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.4MiB (190.2MB) – 3,542,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcf366a17a72372b7919a20804247b77<br>SHA1: 44a32dcbf1b0c8e981610c32eff40919231b7c24<br>SHA256: 7870a1bfa12914e159dd7bc6101207a4133172e327794613ea65b6dcc3df8550</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>226.8MiB (237.9MB) – 3,542,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cdefaf5f23774824adf8d8f3f97950a<br>SHA1: 85d1c19e1d4f34f74871770c888504309a755ddd<br>SHA256: e17ec88ef60c32c8d075ee155a15e7d49d57774bf583d858b3adc73fce61b96d</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.2MiB (186.8MB) – 3,542,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92a79360707dd9fb42352e62e4238c77<br>SHA1: 8e09a0889fa98e227fa7f04ee4881a12ab37867e<br>SHA256: 3f72117970ac6647e3901052f46c214dab5ff9f5aaa2ea4e16c0729e30dd43f4</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.5MiB (231.3MB) – 3,542,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0770ca4060afd67bc23cd313a87e4d74<br>SHA1: 996536a8aa80dc6b2f6d14043d15c60259578ba3<br>SHA256: ccd8d15886dddd20fa2113e82082fc2973a7f186a35545b8331b44b3030a71cf</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.3MiB (194.3MB) – 3,542,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 13168422578fe8369f4368b908c1ca7b<br>SHA1: b6583280a98e886c4e149b060ae7561bd6448ba2<br>SHA256: a1bd2afc555389ce251dfc23765426878a38ed1b552873bbeb5c787fc37ecd41</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>181.6MiB (190.5MB) – 1,914,461 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4c30fee87f0e5e17c38a1df03a1638b<br>SHA1: 7d3bb67c345e1260016c4af1eac3a4e43b245cc6<br>SHA256: 0d5fbd5fe616dca906bb1b5e28edd0d25b05db510fae6ba3704f79bdc58932bf</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>185.9MiB (195.0MB) – 1,914,461 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fae43669dbb7e4faa623c0ba0d79b0d0<br>SHA1: 5c2831afe0960a341075f04dce796548ebf06d68<br>SHA256: 3e1ccdbf9bb5f8d2fdfe15ae1538f4286bc8544a42cfbbcea527b1d17ef30ccc</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>179.4MiB (188.1MB) – 1,914,461 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37e0fa358635ea8ac2a1c98cbb51fab8<br>SHA1: 56b74248682024ed8e99c5168864eb374f38dce7<br>SHA256: 5d490598e37a8ed9c1c48fa043e99722de1be5f66166d934815d579f27cdee41</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>180.2MiB (189.0MB) – 1,914,461 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb1d7f0d06f7826f2ff909fc736f221a<br>SHA1: 723a74daf9c3d7d32af924e3d2b281a1b630912d<br>SHA256: 9e64edb76189cf047c947aed845af2df7067b3d5dfce13f2579817b4356e9d79</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>199.8MiB (209.5MB) – 1,914,461 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aef663bcf49a0685a395ef5c2ddcabdc<br>SHA1: a3703b0613f4e7d2a8d228938d485d138c41e3fc<br>SHA256: 4b6c445c58e417e96a9c34c82aef145b1429a34c2d3a8b756e297334140360ec</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>179.1MiB (187.8MB) – 1,914,461 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 843d9841b87a2112ccb4104817955978<br>SHA1: 527b9b3d01c574578e53e19e692e7140bea299e2<br>SHA256: c65a7e804ec4b322c07c2d6ea020a9e2a721c90ed9c7063d3088d8fc1fc2f49d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>199.8MiB (209.5MB) – 1,914,461 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 326c34683137f821f6709bca763881a3<br>SHA1: d05a2507195039c9253a21d548a6445fdb5e79e6<br>SHA256: ebb0d0f098835272c676bf9682bd9c1963e208b31863672da220c2b5dbc20650</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>182.6MiB (191.5MB) – 1,914,461 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 404735690a799119043703b13e8736e1<br>SHA1: ba922ccfe707169f98a885f0cf2f8f11453ef6d0<br>SHA256: 0b08b0b60d067fa66929daa4b10ef25137245dd0e84d4695d8ee622e4d53118d</pre></details></small> |


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
