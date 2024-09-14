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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-09-14<br>IPv6: 2024-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.613MiB (5.886MB) – 281,050 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee6a509ddf65c0ab9dc686ca1c57eebf<br>SHA1: 2988b2f229635f287c79987447471d4e431b412d<br>SHA256: 78e79c2d5fce9f0a999a7bd26123750c74a7e58232ebd73863be0820ed3edc00</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.92MiB (11.45MB) – 165,926 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e5a38f3c9367083c68b387f2a0a2f3f<br>SHA1: 86ca1e288be55d2be889298c24db870f46d96fa5<br>SHA256: 4c802d4fed061d7854567c64ed7d9e435fe07dee5cc3de31056104cecbea6dc2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-09-14<br>IPv6: 2024-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.157MiB (8.553MB) – 408,499 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e2e30d6f8256281eb490c02541c267e<br>SHA1: 6e3f7b79d45309dd7926f2dfa751d0ed25bab8d3<br>SHA256: 106956358859ce78f754e9c65411b1ed6e30e2104de016b2f5a657530148a8f7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.744MiB (7.071MB) – 102,597 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d461a723957b3585b6fe8fa005b7c6b<br>SHA1: 7650bcac134f240fa386a801fa4439d433f34891<br>SHA256: d8fedbf288841a7c7e3e969d5bee220a9fc71f4d79661bbe44bc512d86c172c6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-09-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.78MiB (17.59MB) – 839,343 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2a4c4273006e1c154a9369f48404829<br>SHA1: 9a30a86f3f03082cb355a17bef96481ac77d7158<br>SHA256: 990181feff94646e404fe4253157bb4e764ddd7e51fdfe64574aa96d9dd17d1c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>61.97MiB (64.98MB) – 941,715 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f29f7310702ddba5432514b4d66ab6e<br>SHA1: 95f6430c3cb42245aebf0393bc8defa20bcbf356<br>SHA256: 9180b44ff64debf3bd47722b99c16d82b8e7a4e985d15752292d363fedd52671</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.026MiB (7.367MB) – 353,071 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcefe7ff67170edca76e960964754e05<br>SHA1: 27baa458e1a83274ab2aeac30e8c9e5fd89a29cf<br>SHA256: 462e24e1a1bb99827d9159c6ca57beed55617951e2ba210ac5d3ff2b406854af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.08MiB (20.01MB) – 290,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ebd3df44971fac41c81afc4e0b8e479<br>SHA1: e374278cdbc7551f55e127136a4623733504aeb5<br>SHA256: 5386c4b7b3b9edde1ed82d40af540593e3564055cf489bb7b99eb47057236d4d</pre></details></small> |
| | | Full Location | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.3MiB (197.5MB) – 3,287,813 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 454e55ae0fc4afbb509099e64b95780a<br>SHA1: 6b88a53921a475e7c1503a9fc3192726c88eee1b<br>SHA256: cd862087cb0a1f5359ee3534aa13b529d8eff5b1c700f8f97a19f0581998096c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>371.3MiB (389.3MB) – 3,603,634 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1073bf4bc29c411e1711e31e0f8593b<br>SHA1: f03eb167bbf14c750a0b060d043ebabe87ed9840<br>SHA256: 9f2c824922dadea859da67d03d96f92bd830c0efee37cf04ed4acf6cac6a1b6f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-09-14<br>IPv6: 2024-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.942MiB (5.182MB) – 247,345 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75be5fd9df21ddbc1fdbffc757c5c88e<br>SHA1: 617600a865f99d7027bf00861f55ec2f8fd1574e<br>SHA256: c577e4648304b379620b9b9b1a7b46685fe2b5a3719de872d7565971b4f67dd3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.43MiB (19.32MB) – 280,024 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 529fb8698467082348344b270ff7cc32<br>SHA1: 5e3253c77897a6f1833518163500372c619862fd<br>SHA256: 9289075bcac9e9a959f8009c5eae593e88bd3925aa371f097f4b54c6bd5bb9ed</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-09-14<br>IPv6: 2024-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.5MiB (182.0MB) – 3,005,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50ec8daacd5cafd5b2765884871d9b09<br>SHA1: 889e86b248ea9a4741e8399a0e67d17ad637cc38<br>SHA256: 5909cda69b8afb1da39fd44d4e35827b08820512a824be3f438aeb08bfbe1c67</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>210.3MiB (220.5MB) – 2,035,716 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 221fa2afd3b2e737797b4dd7b49d116b<br>SHA1: 42a7d10f6dcb092f867344cabddb6856eda16b19<br>SHA256: 138f90080a7371e27aaa532721e6449e41511cbca7244a5e31fdcc4081b48129</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-09-13<br>IPv6: 2024-09-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.766MiB (10.24MB) – 489,193 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d96d0810d6a14dd9d14353ca874a7776<br>SHA1: b8163693ee336111cf87385024871627e247a91a<br>SHA256: f90f9040f56090d86b947c22607b081408f276e6de5614d7358a1e75dc74ce80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>29.85MiB (31.30MB) – 453,637 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 860fbb616b96d63b476b9026e4ceedf6<br>SHA1: c5f4833417e5dd404df55ee696eb6fa876cb5b16<br>SHA256: dbf401c301e4d532efeab97c40e0216e103d4216242178baf9ddc63fe8cfeb2e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-09-13<br>IPv6: 2024-09-13 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.5MiB (179.9MB) – 3,387,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62dd7ead6e61def75d8be574a38e3b3c<br>SHA1: 8ce017ddc7580c9155d7862deba494cd6dbbdf73<br>SHA256: a93edc3dbad843257d8f3e701daef9bf54418c6fada1ea60810a26886741e4cf</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.3MiB (192.2MB) – 3,387,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 876bff90a0c7a21827f0a2e3014586ee<br>SHA1: 7c0f5be78327ede1432e8a4371e6fbbd79f8843a<br>SHA256: 018fd9d8b8742eaaa95706cb1f4ab3d0bb2f5048571bd523516b2e776776c0e9</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.5MiB (178.8MB) – 3,387,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c449ccf22dc6493380d7b49bcf07fb93<br>SHA1: e8a81aec7c9e739390022d65ec149c63a7152ee8<br>SHA256: c296bf3810cd53069999819a6929828a4c48be8999800f1506d9d19d1b01392c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.2MiB (181.6MB) – 3,387,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de769f8a0ac63ecea564c0f8680354a9<br>SHA1: 8d2e448f10c026eaa63d6702e9b40bd286b42655<br>SHA256: b639d83e74801298f84f8bae106e98aa05233a34e74e53b4e18e05709eb8ee95</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.5MiB (228.1MB) – 3,387,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2408d48424c5042086a59d36ff3ac67<br>SHA1: 598399691f6b17b10cd2f5ea73347aa412c51b1f<br>SHA256: 5479740cd45ac660de81d7a853e518822bc8ab25e1aa38ad0b49bec9680721c7</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.4MiB (178.7MB) – 3,387,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f8de6cca22a5b754da5988a87593e92<br>SHA1: 8fdebbb128fef61f3b31f28991b505a7be5b1b98<br>SHA256: d4bc03296a410991dd2a4465f6dc2920a66fd0127466f4389af60e6f4834812d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.3MiB (221.6MB) – 3,387,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03c1a99add1c036809886c7eaf9d02cf<br>SHA1: 36dd606603c5ca98b88cfc7bf2049ae6c4669ed2<br>SHA256: c09d21736bff08549cc95bb3c21f91b7bb01c7626a6119bb94bd2d3ac48b91aa</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.7MiB (186.3MB) – 3,387,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed0b5f2283c3039c8ed7f62d28ca40a2<br>SHA1: a7d070577ee31b82b729bbb8805fdf86fe18b542<br>SHA256: c32d4640ca7d2b647bc46cfde7a1b5c0ffee2ac944c13c92e95fb871fbd89f13</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>156.7MiB (164.3MB) – 1,662,071 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a15ecef908b3160c93a77c704d7f2765<br>SHA1: e2f8bd8be5124bd4d1b7d191f24b01031a5d05c8<br>SHA256: a1fb4e8bbd193d0c5c89d4fb1ff2b2dc36bc90018aa2a5769be5d15fed233914</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>159.2MiB (166.9MB) – 1,662,071 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feee2a598b1a40f8d6211cb979c35e2e<br>SHA1: 5d41e0ee6ba819601b9d284128556a704160da22<br>SHA256: 583077ffa398be200ae3057ba9cbea0a4f29164104ea9ccddebe8dd545c7c454</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>153.5MiB (160.9MB) – 1,662,071 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 464b371bad0539d5e98a4e023e2e826a<br>SHA1: d92d31eb70d583d13e1dc522de63b890398adfa1<br>SHA256: 781c2cd3dd5d0c2a3b4842ca92a05faed8943484bc77bc9a22bcc4bb6c5b30ea</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>153.5MiB (160.9MB) – 1,662,071 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45c8a3f15d4093a3246f18154df88bfd<br>SHA1: f6401b6b656d91b216fac974fe51c3b581c764d7<br>SHA256: d1d20b724b36c24d2c799d948856772fd76c41ad62c2fd843692aa94d593f816</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>168.2MiB (176.4MB) – 1,662,071 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f6ed3f1a1b8b7e450e5e83542cf7cd2<br>SHA1: ea6ef8de5a23a1e850ac6cebacc3e59890cf51f5<br>SHA256: fd58ee5237a5a5e6200013bd24acaca4883c7e8e359cdd25513d447645b7efdb</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>153.4MiB (160.8MB) – 1,662,071 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8f3b0d2c6f82561e48434b2a72f26bc<br>SHA1: 379e2f0455e359ca99c4baaa924dd98d4126fc13<br>SHA256: 4fddac18e79c53d0dafc64e98238620e38d4adffb78b187878842be6a73c33ab</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>171.4MiB (179.7MB) – 1,662,071 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbc0116664fd5f8d28ac349667038b26<br>SHA1: cfc8f486a3568dbfbb199bd87ee5a453715fdd6d<br>SHA256: eac03a45652e9408aca800ae7e47fd177671499fc8ed4f1ea27fd02e57e27e46</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>157.3MiB (165.0MB) – 1,662,071 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 351fe0620ca935e5ad75dd2ea0ad6624<br>SHA1: 31e74a95cf38e120ba21ede8a4be95ed3739da0c<br>SHA256: c8627a8967968503990f17dec1c75ac6a5b2c9f6f5fcca153e861453c3c8c90b</pre></details></small> |


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
