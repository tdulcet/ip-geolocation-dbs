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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-23<br>IPv6: 2025-12-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.425MiB (6.737MB) – 321,718 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b2e46efd6ace87f3e494014571cbea1<br>SHA1: 71e1699e9c2f1efcc1b81425a62bb6dbcf50d780<br>SHA256: 510c63f570bb1d809e601c7e59fd298ca795cf016c9ec7182000b17662cb6b28</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.18MiB (15.92MB) – 230,692 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7d359180e30a683aa33e25a4de564fc<br>SHA1: 2e1ea6248c5d352a5590d13b4c13adcddfb5b73d<br>SHA256: 35f62800a19eab32476bf9eb227c28e3c813b582990662bc4b1bbd63d2b28be5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-23<br>IPv6: 2025-12-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.176MiB (9.621MB) – 459,378 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19ae7e837fe80747e05bdb0a0dfe6abc<br>SHA1: 41557193d82dc7caad8666a1ea9fbe3da1b032e4<br>SHA256: 183dd3b8b8437881cab0781a0b080166b14b3702352b15d6dbd2e46a8961a267</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.495MiB (7.860MB) – 114,021 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d56a941a5f3e9d803b3b5f89f63b183<br>SHA1: 473f4e9f17daa3c8c5d95551f5493d3c5bb46e7e<br>SHA256: 50f65504fd653c2334ebb8c0960570f3e77448ec93346b6227f752ae7d81a018</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.31MiB (12.91MB) – 616,563 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9381bfce1e180287cb2efba092a1901<br>SHA1: c96b66e33313aab026323719b8656454012358e8<br>SHA256: d9e726a049bec02e3c404800ce48e5d5c2ea9755802052b4fec2f6bf33dafe1d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>82.63MiB (86.65MB) – 1,255,752 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83404cb0fefe13383c05d7265dfb4aad<br>SHA1: be179d36b24114f0a8c2557e49030b5a4bf9b92b<br>SHA256: e2ae212e45f0efe0993a013236e9327305ed4d6e6c083282c1dd4fae3dc57642</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.196MiB (5.448MB) – 260,054 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd1da47eecbcb1371255bdc50c718d77<br>SHA1: 750933e1de8cb3d548ac391160af871b871bed93<br>SHA256: 057d957bff860585d56f46ecfe886d386bfef914406c23dbc1816ac00ba37c62</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.00MiB (24.11MB) – 349,485 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78fac9141a055ba1200b9e4197d17a6d<br>SHA1: 2dad5e9fe9e6680a486b8de86a165bcc1d75629c<br>SHA256: 2f85601d58de0e24dd53e1f990a048c34f01bcf4433e39e78d3d87d89d39ae02</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.5MB) – 2,947,207 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd8aac3eeb88b310fa305cd0935ecfd9<br>SHA1: c74492fae9ff6ac08a5c5dbc08bed733d3da06ea<br>SHA256: 1dcc9f177867a631fe4c98c83a10cdb7d7578efba05eb4d13a9d34ff00ead1c9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.3MiB (305.4MB) – 2,823,618 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf7686fea78936ceeebd798c0594060a<br>SHA1: 3bf18b3cb9ecb79d04eff383fce69df36bae3d51<br>SHA256: a5bbe43965014f4f35c9262bd8e7ae3e3dceb030619ee951589b718687fc8ec6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-19<br>IPv6: 2025-12-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.29MiB (12.89MB) – 615,274 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83db6023af8e35d702c41155774a50f2<br>SHA1: 3636cc669a7588d4922604863e22635d1a369bb7<br>SHA256: b06b20f7c37f15453d6cb5eb4e36c3c8801a8a4a30dde9ea6b67261dd6723b35</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.78MiB (44.85MB) – 650,078 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ceb8e89b22acd239c589bd124aae4548<br>SHA1: 6139c12c560df6a7e6cda1cdc5472d575cfd2dbb<br>SHA256: a4a1b0489bd930011899e8d6038e262c6906b900405ae7ed810142235f3d0770</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-19<br>IPv6: 2025-12-19 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.6MiB (187.3MB) – 3,524,931 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96baf3301fe0cd7c8fc81215161cd40c<br>SHA1: 39fae84e9b3441c71fb936b7468618ff491b3d35<br>SHA256: c8d2f5529009ebc3b30d92b9a51580b71219b7c6b446983839b6307c05198e91</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.7MiB (198.9MB) – 3,524,931 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c9d026aea6047feb748c7e532ea2e61<br>SHA1: 8a5b239598d94be1cfffc8588fd2c66bdc2c4da7<br>SHA256: 9c9eb5a244111983e858f6e7cbc28d99d63614f7547fbf4aa29c04d476fef974</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.6MiB (186.2MB) – 3,524,931 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d01792b540f639a51a11b79ababb374<br>SHA1: 7a2dd1b5ba310c0037c94affc7aa0350650d6c2f<br>SHA256: 4ba34c7c682713eb2e9468734aab43b361b2ee8485457902d50e04386fabcfc5</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.5MiB (189.3MB) – 3,524,931 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b24e06d459e5620c8b841edcfebc7ce7<br>SHA1: 8a54069c35ad0bf80a57eba9e91deafbabf55683<br>SHA256: c59586ae251b45dc25750ca606908b612188e02d22822f6293ee6409b5f97e57</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.7MiB (236.7MB) – 3,524,931 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c9679075f1aeb4bad319a455fcac8d3<br>SHA1: 702d86577e16f014dc264bb6cfe46c5e1bd05609<br>SHA256: 0e9ab1d27bc947dfa47bc1892f001bc471fd8b254bbd1e56a96a5d986791aea2</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,524,931 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f3257dcf1ac666b5104cae624c36b3b<br>SHA1: 9ffad030c5786716ce0f0263dbc66111d1d5b43e<br>SHA256: 24ce5b7fe63efbb94e40165f57e6e260fd4c7d890bc4b906c8253ee0a4f23be6</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.6MiB (230.3MB) – 3,524,931 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c31406a307d1f2d5f04986b888e8433a<br>SHA1: 349c714db3a6ed0086b728ffe164b171e9f612cb<br>SHA256: fa300d1971e0af54884f71d4bbdb84233f499449d0f2fde7f9e03a4d44fd642d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.4MiB (193.3MB) – 3,524,931 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a9dc9599372d92f5f70cf67254e6c91<br>SHA1: d04fd606fc15f6eeacb8b11e4dbc786663679c5d<br>SHA256: 1b150305b188ed1c42cb55e0387ec80c087bbd48f88a9fc0b3bcd1ec5211cfb1</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>186.1MiB (195.1MB) – 1,961,167 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4329b7056886fe13a5a48a5dabe1dd3e<br>SHA1: 08fe0ec7114ca63444a621b97512e79fb6173b87<br>SHA256: e41d940209deba52d86c58647dc84084d7d3b76a2fe999279bbf0f76d61aa4db</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>190.4MiB (199.6MB) – 1,961,167 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97437756a5ee5ae579b04fc3cbbee695<br>SHA1: 4ffa7bbcc652a42200d5fcdcad00f54f5e53fdf9<br>SHA256: 363c9fcc2318f667d5e5a60c9e4f80f5cda2377d69cf866048f09e890291396e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>183.8MiB (192.7MB) – 1,961,167 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0743eb3502cb56a732b1353e99906227<br>SHA1: b8dd1210136ebad5610b5250783007d9862cbb30<br>SHA256: 5eb529b904e9139b4bbe7314a2c51df84d3ed1ffd6baa58faa6a03bd18e45934</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>184.6MiB (193.6MB) – 1,961,167 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea3ccbb6b69e959aafef5080b2c03305<br>SHA1: 82513ac7255607877dd2d69c1ed5649a5cc1fe2d<br>SHA256: bcafd5c8f6f7c3e96ce8f4e08cd10cbde1fa529a9109f0ff13077e0829f3a3d3</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>204.4MiB (214.4MB) – 1,961,167 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 497f36dc6bcd70c063f66c411abcfee4<br>SHA1: 826c0b19347944acf9ee6df4af2df8103856dd76<br>SHA256: 8563ae1a7d6320ba49984aeb192a73821f0be2aeb53f8293fbf281db877d0758</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>183.5MiB (192.4MB) – 1,961,167 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4402420e5cf732cf0cf9b75e6c7548df<br>SHA1: dab140442c5d02a42e700c8af67596291a2272a2<br>SHA256: 52b090cd3720a93cec3d0742b1454a545c4fa84cc153cfe763e1e338317ac3cd</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>204.4MiB (214.4MB) – 1,961,167 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88bb272e97b03f0694f8a2e31e094b6f<br>SHA1: c5f7123af01bbc8b8af2ec7cc6e6e7d29d12b84f<br>SHA256: 17bcae06d6a1d64fc4f97bb81d9c028a32880bd747171c00908aa847455dbcb9</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>187.1MiB (196.1MB) – 1,961,167 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea38a45dd412d87de87f044d8f274a16<br>SHA1: dc26de3aa5ad50d954c5d2dfa3de2a1cafe825f3<br>SHA256: 1d6e097821523ffd9662ee31f2846cb97f57d70f192e457980c4486b36d92af5</pre></details></small> |


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
