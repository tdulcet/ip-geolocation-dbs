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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-12-14<br>IPv6: 2024-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.922MiB (6.210MB) – 296,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4850a5410119fcfc30936481cd114714<br>SHA1: fed75487686ef94ff11036ff44b8f8a5c8b63344<br>SHA256: d3d28df392e326091621d4127e60c10f6615b4bf46bd3d00034e5ed276a0baa7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.53MiB (12.09MB) – 175,199 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc338a71b5ce507e92a899bc35fa9190<br>SHA1: 2a38a4f5a20daac6116766704b22f2652f3cff4a<br>SHA256: 15dae0514be7e5373abcd53d865f6152df5fbdd7e6ed26fd980fa236b27be43b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-12-14<br>IPv6: 2024-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.264MiB (8.666MB) – 413,855 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc1b07d9f416230c423ef38fb0f7d1b1<br>SHA1: 8bdbb8b9c7246bd81b3b6da66f4a6ef2f10da603<br>SHA256: fcc9e5d7777d0ead4d1639f264a9c13529ee6700f34515c599ebc141e865e832</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.939MiB (7.276MB) – 105,564 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8586b6a4a266a8faccad8d77c35f2e31<br>SHA1: 36bad26f418beb90684c747f94368545361b3cde<br>SHA256: 5753aa82d99c72d122d65f2c92586f6a20e34c7d453092a02277b8b6ae24b263</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>14.33MiB (15.02MB) – 717,130 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81f61433c004f73e535f20c8a069ebfc<br>SHA1: 187d52497022b4a1a8cef6ccbd28fc97d38a8168<br>SHA256: 89d7c8bda625dcdda86edeb130c0a52cb47314e72dbd62ab7e5447153a88317d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>81.93MiB (85.91MB) – 1,245,050 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fca1292adf45e95a1fe8425cf9f27a6e<br>SHA1: 1ddec757f9e046d14d962289a47725253d892d06<br>SHA256: 357569aa033b6f4e8479f89384b1f5ce3cc9a3642e5fbcbef954b29f29af469c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.156MiB (7.503MB) – 359,168 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4fa1848a017a51ce167e1b45ef180e0<br>SHA1: d025902fca69db441cbc83871eb99ffd4b92c75e<br>SHA256: f02df1b7ee71bf749e1e43de462a3f6c365d9ed6e72e1d5c6faa86f25acb568c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.24MiB (17.03MB) – 246,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fee62599a38c614b43a277a08de845d7<br>SHA1: f6f5eddc6f61250f0fef53e42d76288b85a9971b<br>SHA256: 258dacce2a418e7297db10bd484df83410a61ac130bc1a5820b6fb0c0c58cb70</pre></details></small> |
| | | Full Location | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.6MiB (199.9MB) – 3,333,541 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f97a8dfa3d2efa2169aa49e5067082d<br>SHA1: 69f6046d5bebaecbd09f512a07ad0279a8bad58f<br>SHA256: 193177f00477af08b776744f0aa5ea8ffe08fe54bbe785733206c3c6f5ea0b02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>381.5MiB (400.0MB) – 3,700,914 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60c57063e8597965c85a15738ce2271e<br>SHA1: e6cfa1c20dff9df4b9dedd101304ed4939827a3f<br>SHA256: f48cf620380d7f79c9d8d05702be678101a193a90ef351c28ff300bad2cb1942</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-12-14<br>IPv6: 2024-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.918MiB (5.157MB) – 246,132 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ef7e16cf2b6bbbd422ba2a934ef7df<br>SHA1: e1f77a047f5dba3e4ae075464e3761268e84b7fd<br>SHA256: 8dcac1f1779ff26fe9a26934fc72b4c423e9a2f1252d99e1436206cc2bf9f63c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.70MiB (19.61MB) – 284,192 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dce3866a2d21db59b0445d7ab2b5439f<br>SHA1: 62737a727dab8fc70aa7a79a6b203bedd659ee5b<br>SHA256: 2bc4972b559cd83a749cdf69acfcc9f7e1e9b63db44e48dc0e635dc639b29822</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-12-14<br>IPv6: 2024-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>167.6MiB (175.8MB) – 2,906,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1918be02cf5e40016993945dcdf9fe2<br>SHA1: 26d9a8404ce0b330647e6b9dec8e0dc1f37c9773<br>SHA256: beead4d706ffee13660a84a3a4fa8d161b26172c66d7d783002d7e5e9a446e97</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>223.8MiB (234.6MB) – 2,165,543 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58aa852f4471f22d59a91349fedddaa7<br>SHA1: 58ed488a65f8f18956e7b32e6e9c4c95283bd843<br>SHA256: eff43d3a7756d1032e8d1b53d8fc159639852e5511ede4f1a0b4456657557bb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-12-13<br>IPv6: 2024-12-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.06MiB (10.55MB) – 504,031 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27e7c6146e558b2a3c4cf2c8c31bbec0<br>SHA1: aa4cb6d25288df906b744a94a2144b145dd8f760<br>SHA256: 64fdd8f571157e2636ee0d76c7cc8f5915b869be94c8144e10cb697e97da2831</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.20MiB (32.71MB) – 474,118 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 335ba8c8790ed460ac700ebfb881cc13<br>SHA1: 046fddb8b7a2b64360955e14fd41f80fa14a8d14<br>SHA256: eb6bed4c189701b074d9108c96b1163aac20e4c4d1e02f85f4f49b228863b748</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-12-13<br>IPv6: 2024-12-13 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.2MiB (173.2MB) – 3,263,934 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfd11f73ba8b4507122522d510b722e1<br>SHA1: 988b4e79afc5e44f6c7f9301078d842290f1dfeb<br>SHA256: 634d778f178f635ea321cbd99751dd02a6a3f924be7e4581627e649143b1f3e2</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>176.0MiB (184.5MB) – 3,263,934 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b34e2131a8ef82a11ac0c664afe81f81<br>SHA1: 1579d46bf004a50a4e384d58be9c9fdf9ae8c892<br>SHA256: a77d9f7b74e9b66910179d87fbb146d047ca33247b2bd34e0a83c5de0a6114d9</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.2MiB (172.2MB) – 3,263,934 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24d064d345e8dcaa57d316f2e71426cd<br>SHA1: 40471dd21a8218eb19a76c3dd75e5920594e4d19<br>SHA256: fd5d1181d828fe3e49e33a1e515ea7d47f24b8f650a2eaf8e50d6bbc4c87f31f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.7MiB (174.7MB) – 3,263,934 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70f33ef1a620b9e803c0122fe5c1c26e<br>SHA1: ccc8d8f8a870dfc099e195fd00a244136b2a60c6<br>SHA256: 2fc5048fc2515b8815d18ae534916c88aed833285899cdcc6aa79579a133f339</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.5MiB (219.7MB) – 3,263,934 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a006e030e8ee7267c497fbe34ca6a15<br>SHA1: a322a1adb1dfa8bea737b54f01964d4b01b18323<br>SHA256: db248cb243ffc63cc10d204bf6f8c260de2609af138eea91e3d9caa7ce032f7c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.3MiB (172.3MB) – 3,263,934 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3618755b30f543689ad7ae9422bfce3<br>SHA1: fdb101b6c1feb6899bb0922a3c7a151455742171<br>SHA256: ae39c1619e1a9f6b48870dc9eb83bc4055e453d67b6ca961d9ca83403e8902f6</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.6MiB (213.4MB) – 3,263,934 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ef6a1010344dc50408e7e81ecb4842e<br>SHA1: e10ee6c9f7692b354d80a0a2364102b2234d5b75<br>SHA256: 40a797f5ed4706ecd36bcbca481de0f5f02e964ec3bd36ab42e281b17cc9a132</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.3MiB (179.6MB) – 3,263,934 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f363250921dbcf613c93d869643c31c<br>SHA1: 5536aed408edba9c29b08c759863959a59d8e7b8<br>SHA256: e99610c790b0d21f2f3df63d3e23439623d32124e43e9ebf876ac1c07bdfa4df</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>162.0MiB (169.9MB) – 1,727,791 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26b3dd7d1fc7625150060bbba2e28ce0<br>SHA1: f0769f6ff06719a404347771283b5166301a74c1<br>SHA256: c8de999ba2c3102e3e0e0168a98dcfd9e4915822f0fa970e5dc98bf78ad7e334</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>165.6MiB (173.7MB) – 1,727,791 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcf59492c61e62eb1e61bfd2e7fff7f7<br>SHA1: 96af3c0326c08e3d131794206f421a36f11dace8<br>SHA256: 391fd04633df1e2914a28e4f1896d4433f0f4eb13f080127250be45aae07e318</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>160.3MiB (168.0MB) – 1,727,791 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0d02a9f7720e6553b87c40ea109057a<br>SHA1: 11fd0a068d868d26557c86cd09827b276bd818c7<br>SHA256: dd9692c67463e77d1daae4db72b0e51a734c663ef644e9424fcdcf4bcee324a8</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>160.5MiB (168.3MB) – 1,727,791 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44d0f4cd35258c163f2c91841fdb5aa0<br>SHA1: 8da832c71e9b7a3d570d89a3b5803de6a79dfb2c<br>SHA256: 4798dbe5e6094fc9cc24a8326f6409dd18f8806de41ec3dbe1e085c696c34f4a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>176.3MiB (184.9MB) – 1,727,791 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e386bd5a197f8d172c664f4dff88b6a7<br>SHA1: 1958bfb1a58d0d997e6f06bdb9bb0c49f72adfc9<br>SHA256: 8ca3342e74fec04d031246c7e1264d5920886534529cfe0d77c4dc525de277c2</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>160.0MiB (167.8MB) – 1,727,791 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f30088991864ea40c6fa2e9c9fcde87<br>SHA1: 422fa47de86612bb0ebf75c42a93063f191d3d82<br>SHA256: ff5d284c961c21beaf79be9be85600c195c191838ab7ad58eacd63eb0bf303be</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>177.6MiB (186.2MB) – 1,727,791 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fa163d1f8c3fa00278d90a1a13f1450<br>SHA1: 07d7b5e0417cf957cc133a2a7fe8489dba8c5c35<br>SHA256: b98d764ba9e8dfd0eba39fc86f7e23a9e7986f008b800300a2a8cf979a15eaf5</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>163.6MiB (171.5MB) – 1,727,791 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24c7c57c593e6a7075e0ebce74a1ac56<br>SHA1: ea138882d8c44b934887c51f8a0a0a0a326784d3<br>SHA256: 0d4407bf045d42851ad79cdc1cdb8b0760980e9cf8962fd98ee873e1c399f293</pre></details></small> |


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
