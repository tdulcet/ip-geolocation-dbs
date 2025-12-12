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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-12<br>IPv6: 2025-12-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.361MiB (6.670MB) – 318,514 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7625c0e770abbdee8b2ce9d22b5da41<br>SHA1: db347c01f35b20e1e94c83b70d5505bf481e709d<br>SHA256: 360c356ebfee54258086e16c520b7476ff6abde6851fca10dd564a09fd4c397a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.20MiB (15.94MB) – 230,970 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a12533cc402b0b7cdaaaf67e9548eec4<br>SHA1: 0067f061931792d2bb5ca59366244cb0ebc830a3<br>SHA256: b1a4ba2361aadb9959b960860b6223710517fbf3e54be4e85932e537127fd8e5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-12<br>IPv6: 2025-12-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.749MiB (9.174MB) – 438,079 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9760e45b84face384bdd231bb4f8661b<br>SHA1: 98c251949377e532d77cd8341390b3389b9dfeaa<br>SHA256: 38a0ff98cd7531d053716d36d4dafe95a7fa882ea691e93b3176069c42d00afc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.558MiB (7.925MB) – 114,968 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0b33a63a04892329bdfd2844c057cca<br>SHA1: 263f0cf3abf7c6cf0ff1c9bc660f7cce3287b232<br>SHA256: 507f70e82f8100c66faf76792b7c4b51eb6cb556fcd212e988187daa0006a9b2</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.15MiB (12.74MB) – 608,096 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bfa52cc294c63700b126d4958ef431ce<br>SHA1: 954caca67a57c89669f711f5904257b9aafaedbf<br>SHA256: 811f0432772a3b657f130cdbe35802df1bff972cedb5722ada83bd2f3c25a7f3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>83.01MiB (87.04MB) – 1,261,517 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7f1339356e48010212c09737aff6c2a<br>SHA1: b65b23a09ff9362a714f426628c20be4408f8f63<br>SHA256: 3b581d6fbd74f23e538e44eb21c7b8bb7d487572160e55f6d92ed858f25e3799</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.367MiB (5.628MB) – 269,273 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f62178d410cf3bce771f73d48e43faa<br>SHA1: f7860e76e84e2e025ff86a4e5640a5e924783fe0<br>SHA256: c1072a02c991020475c91925325c135d490b5d243b47ddaaf047c7cdef840cb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>20.32MiB (21.31MB) – 308,850 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 594439a3c0811d183bfe5550c4fa8326<br>SHA1: 2cdad07afa5d0806f1da62dff5def384ca6b52c2<br>SHA256: 86d5eca80b132381a0466a85510652d17f94597f2ba2f6e7a930843309468a04</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.3MiB (179.7MB) – 2,965,067 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a5854fc5ad699cdf214288eb10b070<br>SHA1: 02297fb66300226ae67a1dcf129bca4e4e77ed1b<br>SHA256: 2eafbe9230ee8d23f99e769b27da134fac2c62d6a74beda67c278e8823866eb7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>277.7MiB (291.2MB) – 2,688,825 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7579bd752fa4e59ed8578642ac57a02e<br>SHA1: dc5caed7e7217beea7fbec082ae0651c0f13d1b6<br>SHA256: 0d03be0ad75f92ed0fe8301ab4717341f744711cd9bce0dd880a1632aee11d8d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-09<br>IPv6: 2025-12-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.34MiB (12.94MB) – 617,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfd0524eaa3941c2e76170c816b22549<br>SHA1: 2c639b56018395c9cb939d5faa800ad25d8632ce<br>SHA256: 28c06e5414f147838cd4bda12c8e4f21420647eadeb9ba2e67fd975cdda36df8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.79MiB (44.87MB) – 650,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edc68fba4d615365478763795fab828e<br>SHA1: 1586371331e0a752fd0bfe97255cd0814348d28c<br>SHA256: b2e1afb2b903fcf54ae82a8d46308d918a9dbda9c862c840a9e09f6bf4bc1329</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-09<br>IPv6: 2025-12-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.9MiB (188.6MB) – 3,550,840 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 351c237e8f93c7595ecf9288da9dda27<br>SHA1: 83fa5b8aac65b57c48016ff8a4f60daef011a51d<br>SHA256: 163f58b0b1ae4631f2b4ca81f7e918a03e43c100f7ea9ef7d02b6fdca42e715a</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>191.2MiB (200.5MB) – 3,550,840 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df75a4a08581970f12982d7505ac5cc6<br>SHA1: 098ad5acc9f44ef0cda8ecc529028b366f304761<br>SHA256: 321df5d650e24aee0a60baea0e58349b6039b7225074d2a3a63a26aee0ac91df</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,550,840 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 971c2d87fecbedaf723238a30cd22fe0<br>SHA1: e655ef574b20eae3b397a7eba2bfec41de9857cd<br>SHA256: 805f2a03deae11dfa902b46ff253ef08b2aed2cd885fafa012d2b9da187826a8</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.8MiB (190.7MB) – 3,550,840 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bea56b5e7e9d8fffb0450f35fcb4c8e4<br>SHA1: 6c71435a4de098514bc517a3dc2feef84929c2b9<br>SHA256: ec0a4d20ab4fdbc6574278ff67aabc66366aa970cd899120cca04a0cef03ae08</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.4MiB (238.5MB) – 3,550,840 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d07c6748945c28a56f161bcb6d16059<br>SHA1: 73c3543c29592793a9c91f67fd2290ee20c7ff54<br>SHA256: ffdd8c875240f91675c7678d896149b03a8c696f9373fc6d537f6848f127a47c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.6MiB (187.3MB) – 3,550,840 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e55b45f1b1746e850a586b0c2760d5b8<br>SHA1: 5b0f6aa9e327a1b65debdd37ede34987295b269a<br>SHA256: 44eb8975f6e8ec4222724d28ec482bc6037ff48ae353ed45b4e3114fbb22837a</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>221.2MiB (231.9MB) – 3,550,840 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fdbf5bc7e1d3c302647dcb2400817e<br>SHA1: 0f12141b6f98ce99222bc159a88e3f8a4e3b540f<br>SHA256: 70b2442298ba28a0bc58c2005fc261b971293a1002ad54345e612b67e18ad078</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.8MiB (194.8MB) – 3,550,840 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 061b74c57e56609852d8d6c87ad7b674<br>SHA1: 2e91da29f66338e40bb5fee191602498095faf2d<br>SHA256: 9f6392862c7aff10521325acb03637d8ca859d41bf913af6bd36a4f91d8e3c28</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.2MiB (196.3MB) – 1,970,466 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf478964a2076fbdccac95213c7e69a6<br>SHA1: 98b49513bc2b021545029b95ffaa8d8dc45909f8<br>SHA256: e20ffe6d608d3e52140376d41a2f9914cb97ecba17954633f818730f270e5380</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.6MiB (200.9MB) – 1,970,466 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d2f255fab53fdda560b78db69dbd827<br>SHA1: 30e2d951983a534fc56e52735d117f5ff0a62bbb<br>SHA256: 03f4e606947ffcc1016d08bfff61cad8360e38eedea9a85999dea41c52692fba</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>185.0MiB (194.0MB) – 1,970,466 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1761488dcc7bad402cdb3fce27e813ad<br>SHA1: af4e44522ee979362fa810728d7b82686f90e5ad<br>SHA256: f6e4b4f62ce6a2ad49b375de396b2b6d90547997efb18a8252bf74a5d9d71381</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.7MiB (194.7MB) – 1,970,466 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c350b04f905f45b7bb521fb0b87ddb61<br>SHA1: c7c07e6c4cc75145e970a3eeaff04ed4458e9797<br>SHA256: 875674423d109e7abf4de15f0ff69aabb377055f603dfcf49a7ba3b7a51b5035</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.8MiB (215.7MB) – 1,970,466 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a90db7f001eb6d8386fc93e2a60c47a<br>SHA1: b018fe2fbd5ade37bc3f705bb521247f8b5d0919<br>SHA256: 288889c2a024ee75ee1d9156fb14a60cf650cb85e59d22251a7d768ffc6ac9a0</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.8MiB (193.8MB) – 1,970,466 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3c81932cef49237792b1f7633502a12<br>SHA1: 62e60db3a42766fe8823a563f6eadb37bb3d2bc4<br>SHA256: 6e3f1192cbc72bd75586d3c2421faacda9add3178a024ee55399329232381587</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.8MiB (215.8MB) – 1,970,466 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e9ddd58be906a62ab96a64c98b4364a<br>SHA1: 764ea4717ff7392b6f032b4d6f2c65ad543f9f7f<br>SHA256: b57a567899dac92af853d5a998fad0d3d07187c06d83d66bbd383a291e39c164</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.3MiB (197.5MB) – 1,970,466 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f7f69c4078d7f4bc15e48ff830b86df<br>SHA1: 46442a9e699dc4381a04f09fd5c526fc9ca66ef9<br>SHA256: a1cb49a1d6b26b2a8353827222c28c8e3c2d2b00a4ae9f99c8d4d96dd87a7589</pre></details></small> |


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
