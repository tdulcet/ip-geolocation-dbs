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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-16<br>IPv6: 2025-12-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.413MiB (6.725MB) – 321,153 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecfe7d5d38836729fae404813cc48d83<br>SHA1: 55198699ad855ec4a2dba98d1b40816d636d70ab<br>SHA256: e5d2fb37b0b5eb27b8b258d449261a21af247840778d3c5f91b8797d40c51050</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.12MiB (15.86MB) – 229,850 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54d728dae2801f25aa29886ed28b784f<br>SHA1: 2f0dba04b9e6c622bb6a49b9442c2065e60a664c<br>SHA256: bcf88cf3c0c667b175d3ea09156683186a8055357047fd31daeb69857875a284</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-16<br>IPv6: 2025-12-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.761MiB (9.187MB) – 438,707 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5846229cab14dff50a572f0fa0a9ab61<br>SHA1: 2ac2c3a88f3bb3821668edb3536f7d836379033a<br>SHA256: 9be8c552f34b8b092c6eef6216ae13e7c9babb6af764fa16994e488f9266fe37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.575MiB (7.943MB) – 115,224 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57dd7c77830e03ff88cbe3ce5104d2eb<br>SHA1: 90491f8c71ada1cfd32ae07c4a3fb30d7037275e<br>SHA256: 2261b09b650b043f55cb29904c09415a165e0d8807f1d6f3d2ee23062ce5fb60</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.18MiB (12.77MB) – 609,515 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 874eedf1850ba75ba4ef4966bb0189f2<br>SHA1: 271ba25184332c7b0b5018074bfeda83afc24126<br>SHA256: a94d58b673162b2ba9bf36583b3d181af03b9125001ab113e8ef6f2a6e3a83e1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>83.32MiB (87.37MB) – 1,266,225 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63689e7b9b308e1d8ca1ac7bb935a5f6<br>SHA1: ff663ac7ee7d16de45b4ff6d2d3201e91ee4da4f<br>SHA256: 333958493dd4e5ef49d017e850d2144201e48cbd30ba6ce9fd89fb0834fffc0a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.196MiB (5.448MB) – 260,054 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd1da47eecbcb1371255bdc50c718d77<br>SHA1: 750933e1de8cb3d548ac391160af871b871bed93<br>SHA256: 057d957bff860585d56f46ecfe886d386bfef914406c23dbc1816ac00ba37c62</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.00MiB (24.11MB) – 349,485 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78fac9141a055ba1200b9e4197d17a6d<br>SHA1: 2dad5e9fe9e6680a486b8de86a165bcc1d75629c<br>SHA256: 2f85601d58de0e24dd53e1f990a048c34f01bcf4433e39e78d3d87d89d39ae02</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.5MB) – 2,947,207 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd8aac3eeb88b310fa305cd0935ecfd9<br>SHA1: c74492fae9ff6ac08a5c5dbc08bed733d3da06ea<br>SHA256: 1dcc9f177867a631fe4c98c83a10cdb7d7578efba05eb4d13a9d34ff00ead1c9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.3MiB (305.4MB) – 2,823,618 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf7686fea78936ceeebd798c0594060a<br>SHA1: 3bf18b3cb9ecb79d04eff383fce69df36bae3d51<br>SHA256: a5bbe43965014f4f35c9262bd8e7ae3e3dceb030619ee951589b718687fc8ec6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-12<br>IPv6: 2025-12-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.35MiB (12.95MB) – 618,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b9bc1caa436bc0db195e950df170515<br>SHA1: 2e3ec94a246dae447c0cdec728a8a5ad6cdb405e<br>SHA256: 606248823fafb6ec9ba5e1eaa05b8671d6147281b5404a444f38f37fc463282a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.79MiB (44.86MB) – 650,213 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d86bc822c8ec1741620e867b7555208c<br>SHA1: 3d7fdaa1b021bbe0cc5f5cb8463a992a10807d91<br>SHA256: 97d0d8d4eddb844dd93ffa568fd383fec4ccdcc80dc7e228f869937f942f90bb</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-12<br>IPv6: 2025-12-12 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>180.0MiB (188.7MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2307bda53abb7f05b05742098dc6eaeb<br>SHA1: 346c2d8052c4cb4e0b902b240cac97cc472102b0<br>SHA256: 1c1002a96836a068c727fda1446f0f70b79bc54a5c963f686e2761f5762e44ce</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>191.2MiB (200.5MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfb766895ecf6d98d9edf08f0f1392ba<br>SHA1: a973751dab8ab70db391a1e6cfd33159e497e229<br>SHA256: d96fac80e0649b5c452dd2fc007f56018488a83c60d2b2e753f4f20e98f32a1f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4158c4a779bd5d1c4620a4244ad3113<br>SHA1: 09fc64a8c6b629c9432b24f6eeebba30f9d0a402<br>SHA256: b922ff3b3af049ad3c5a3741f96b01022f4b5d4c915575785c689e0f005936a5</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.9MiB (190.7MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0f7dab87c19aff03722d05cfa00c86e<br>SHA1: a964076f52d73b6a1fdcdb5478b96186937404d9<br>SHA256: 1a6bee308ea7aeeee86af2168ccac56bb50a992fe6f24b51581f965c3dea05b6</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.5MiB (238.5MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d20b11014692e12b6e15734c85fe1082<br>SHA1: 4e944d0a49fcaa67139ba4e12133875df1de364a<br>SHA256: d586f20932b496512e8c9424041618cc887a9ec57ab53e0e50e3958b55dea27f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.6MiB (187.3MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a7bede5b2984f2b4ed053489f533314<br>SHA1: 0d91d0ba3c0066b8dbed6ac0ed33b5e157d81727<br>SHA256: 05e90e7031e3b875c01788d065eadab156aae1c22454ecfb37d606dd06d45307</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>221.3MiB (232.0MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d399b0afa2eafa1d394c1c6b5ff859d2<br>SHA1: d9693491145c2b858d3db49a324ff51275ce5160<br>SHA256: da63173e3b3a4374720188dd0f4d00a08d1be4d155ed8a7a13839c2c4d2a272c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.8MiB (194.8MB) – 3,551,692 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61ba5b9db0cd9ed10d3aee8ad5a992dc<br>SHA1: cb3eb43ad18cc4d65501e1a37217d276b11a8823<br>SHA256: 690df7c3c31570c8181761b528b30b476dda436b411676160c57898cede6bb9b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.2MiB (196.3MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c42b4bc3a35852569745f0aba4111855<br>SHA1: a9936db361ca6cb8f42ca98b49ab21197b28f72f<br>SHA256: d0af5a29ad9c6c36220da83a569d1cdb12ad67eae198fc822f0c061fa98e9ed2</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.6MiB (200.9MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee801492d9366e0fe046cb574693c5ec<br>SHA1: 656cdb592a80551166896cfd04e727ba0ecef0a1<br>SHA256: 47e407801d8b0a3170b94fdcd66284f43bbde766546333aee81bb597fe901636</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>185.0MiB (194.0MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed30f389de68a22ae925cfde2e4fec3e<br>SHA1: cf3b33d465da8ec1aa38dfa73baad0bd54782a28<br>SHA256: e5daea18225945f28644763b077e11a52706e4404d68c1e75d45b0a98da42cba</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.7MiB (194.7MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d522200734e9f2743e511af411a288a<br>SHA1: ba4f08abe740083d7df2e4856f44b388430047d3<br>SHA256: 6a4eb485e49d2653231db6cfeaa736764c8390a3de10857bdbc9e15db6558020</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.7MiB (215.7MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90be09edc9e23818eac38b9b2e4d024a<br>SHA1: d68f8e5d2a7e88f7c92fb2ce6e90ae8e982df975<br>SHA256: f06f47a83626ecaef191851520370ad971a26089594899f2293b7f0c878a1728</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.8MiB (193.8MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8457111895a3957246e25c50be309461<br>SHA1: 625a2eb8300862bc333ac571372bc81beec10738<br>SHA256: 12ad9c1ca8eac049b92aab2e1f98d433cb6a7fcfcf6c4966fd6cf0547deca91c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.7MiB (215.7MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a20c8be1ee7f8b2690e031f8f47da235<br>SHA1: 6c0465e33456741073d45b882b207cbb912e1711<br>SHA256: fae913b946ece3c524d4d608b6dadee9a36b6eb96cf64e0c008d26cbba4e5ffd</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.3MiB (197.4MB) – 1,970,956 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4aa73c1c203a2540321867b649ba210a<br>SHA1: 27a977080a7bee16342df3055227c7f65b1b59f5<br>SHA256: f52377662c4ef365cb01976d5f432402e2f041d9437d296f919736a987468550</pre></details></small> |


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
