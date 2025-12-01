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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-01<br>IPv6: 2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.309MiB (6.615MB) – 315,915 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11cd3200ae96178ce80baee1507c9d5c<br>SHA1: 4ad44f1ccdfd8bcf0832984906c5a78aadeb6c00<br>SHA256: c447212204654c704d8317bc2a716af789461876413a80c6c9a0bcea5906497b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.671MiB (6.995MB) – 101,383 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc0359567898277d84d3440243627572<br>SHA1: f673446f15ac391eaba8a8e3561a49dadc538699<br>SHA256: 5ef0912bb6139d77ee90c50181ac442f4d0b78c4455f9859ca2683f57e10bd7d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-01<br>IPv6: 2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.774MiB (9.200MB) – 439,323 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 960a7e6e13254d4bbc3386363a6af380<br>SHA1: e13b90b5c92bd0031331871f35abad075e6511e7<br>SHA256: ee9fb6059246d930e5eec5c630c60aeb332b5e88f07e84b531acf03825399fea</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.469MiB (7.832MB) – 113,619 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 926ef3be8421ba5418fdabf4bb92667e<br>SHA1: de0608a9d70555e931124d0c94b8e6e2348abeb2<br>SHA256: 472eb10ff7d32cccb611134feef4a9bfe016a97dedb98f6b6533ab6de47fb966</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.20MiB (12.79MB) – 610,605 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 884e3879d41f0224c1c61b2a9300a264<br>SHA1: 0228af66cb4b017c2c83a1234e63396bf142504b<br>SHA256: f2c6902415739de4085521cc70813da6d6ab25cec27eb75849ab588039d2857f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.87MiB (78.51MB) – 1,137,802 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9519583fec72a6c5a612b4ae88a3872c<br>SHA1: 91cebef45db5a0aaa47a387fb62afbbff56e2575<br>SHA256: df9f6312b2510dc2e790b6ae348c730be8cf126b923279b245f22de2eef56854</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.367MiB (5.628MB) – 269,273 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f62178d410cf3bce771f73d48e43faa<br>SHA1: f7860e76e84e2e025ff86a4e5640a5e924783fe0<br>SHA256: c1072a02c991020475c91925325c135d490b5d243b47ddaaf047c7cdef840cb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>20.32MiB (21.31MB) – 308,850 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 594439a3c0811d183bfe5550c4fa8326<br>SHA1: 2cdad07afa5d0806f1da62dff5def384ca6b52c2<br>SHA256: 86d5eca80b132381a0466a85510652d17f94597f2ba2f6e7a930843309468a04</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.3MiB (179.7MB) – 2,965,067 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a5854fc5ad699cdf214288eb10b070<br>SHA1: 02297fb66300226ae67a1dcf129bca4e4e77ed1b<br>SHA256: 2eafbe9230ee8d23f99e769b27da134fac2c62d6a74beda67c278e8823866eb7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>277.7MiB (291.2MB) – 2,688,825 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7579bd752fa4e59ed8578642ac57a02e<br>SHA1: dc5caed7e7217beea7fbec082ae0651c0f13d1b6<br>SHA256: 0d03be0ad75f92ed0fe8301ab4717341f744711cd9bce0dd880a1632aee11d8d</pre></details></small> |
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
