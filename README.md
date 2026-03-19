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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-03-19<br>IPv6: 2026-03-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.503MiB (6.819MB) – 325,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 584adb670efe10b81f2bcae86fae53b4<br>SHA1: 14e43fce0b9394e21bb4007221b0c107f42bb665<br>SHA256: fcda39d901e19dcdd78177cc93e51ad30fd2e289d6de398366a078504fd0f71b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.48MiB (16.23MB) – 235,192 rows – 257 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ed8257dd07e0ccb6607e318137025f<br>SHA1: cf6d754487dcb498dac7a5d266b225ea23830922<br>SHA256: f1061d0aeae219150b4cee791b234d30ac0547f254a9a7b7019bd21e08e3c360</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-03-19<br>IPv6: 2026-03-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.814MiB (9.243MB) – 441,358 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7bd67290888e9c3f83621003eb6f0367<br>SHA1: ce31c8d513e590f33bdf3f4f8d4bce9b27c84902<br>SHA256: 54271fe22474ce635c9ffd16b1ddb4fed7bfb5aba55a1ef0b3c49ddde6a26659</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.678MiB (8.051MB) – 116,800 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 348cc1bae389d28902b96333c7478ce3<br>SHA1: f4fda040477cf12ef52749664ab0c103ecaf4478<br>SHA256: 1f520b4c1ab3e40d670f7c2be7408ecd7500a2d6b7689ca28ee0271daed63bad</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-03-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.33MiB (12.93MB) – 617,116 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21d03d6f12df06953d8f602ff4416cea<br>SHA1: b7837b4397bb9c40a4a86f637c83a2659b9eb4e0<br>SHA256: d942f69a17bc279a243983c0a1e99426f9271f421c43d2e1ffb2c3ac617f15da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.21MiB (93.54MB) – 1,355,720 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 351659e14d62eec5f86a96b1f739a2c2<br>SHA1: 8b98e680e187f027d7b8747fc5a80704eff43f3f<br>SHA256: 3964c9fb74d0e4117eb52b12bbd97da0cac387d2e1dc51961bce76cfc7f3d8ac</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.906MiB (7.241MB) – 345,970 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be67480ebe04792eaa1e993732e26bbc<br>SHA1: b9c086649cbd7a697ce8b1a6f1200cf343683838<br>SHA256: 97e3ba0306a918694a1abd35fb0fbe18e3275c023a00d3f378bb52d0381e6ca4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.48MiB (17.29MB) – 250,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614f4ebb16bfdb3cd44828a77fb774d9<br>SHA1: be56f3e3114c6c18c1b7e097bb867772c72bf90a<br>SHA256: babfcc027ee9656b7ebe280a391c73174b4990721bda2e7c584c23450f4c5452</pre></details></small> |
| | | Full Location | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.5MiB (222.8MB) – 3,723,444 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d34e3013a398743fdc3bdbd816dba48<br>SHA1: 4f4868afd37a86dcd98f0ff21e863db08c4c69b8<br>SHA256: d805d064a2ceaeb75e8ee847780d1dcf8f54852ffa98bc007b0894fd1c1d24d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>446.9MiB (468.6MB) – 4,345,257 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b0322dcdc11f95be5a5b01f4221151<br>SHA1: 5bcecfc1d1a51db165a9a209bc8f4b9a5e7e1bda<br>SHA256: 9a67a943e4fadd058173607911c45bce627c5fbebc2abef2f229894d2e8fc57d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.419MiB (5.682MB) – 271,203 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c176ca445d23383a4c5e1e2ebd9e541<br>SHA1: d9049c5c5fbb465dca6e199246fc0f4419435e17<br>SHA256: c56f984490695ab20d84eadbfd37f601c78de75f4958c1d1ee5927482ffa66cd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.22MiB (23.30MB) – 337,655 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c07180576fcf598a4054e35c7eca4e61<br>SHA1: fa9ee16f19dba3851f20083872d13d4acbc065ca<br>SHA256: 8e65ba7778f59ef63c1a8df94112a447927b3896dbadb00d080914b5ea37167f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.6MiB (174.7MB) – 2,881,763 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1614bd25a28d2b44922c3116279f804<br>SHA1: d2cd1e423c13e941548d01a453978c165e423b8b<br>SHA256: 8486e52f22f5c609925e25d4d0d4e74ae714d31b8ee7067d87a99f951d8352c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>298.4MiB (312.9MB) – 2,892,579 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85c1923ae57109129fbe714df2b92c0c<br>SHA1: 846479cc0828f79ca640a39a279ddc2fc7b8aa2b<br>SHA256: 1759b2d35ec83b135771dbe6a08ae383efaa2981f42a80b1dcd3ee4ffa98633a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-03-17<br>IPv6: 2026-03-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.95MiB (12.53MB) – 598,337 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14bcfe61c420c23dacb58848426a2df7<br>SHA1: 8358d00a58bb392f3d538ca1785e756c49c952ea<br>SHA256: 83f808a89b3e408b87bfc541fbf6f06271a337f6c798fa63d425530275e91b80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.45MiB (43.46MB) – 629,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b38c9132785d14e601c99eb092cfc858<br>SHA1: 5a5ebc8e93ee8856c1bac93ac823066db20c8c2c<br>SHA256: bcb0a62d1379593c358050ee52f337cc21ae4425df5f4769fb22927cac965e51</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-03-17<br>IPv6: 2026-03-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.9MiB (187.6MB) – 3,533,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0553e9a2b9da038b4f4237ad2a6cf481<br>SHA1: 1f814828941f18fae41adf73785552f701742b42<br>SHA256: fa4dba21810e681c5a86ccd1ddf50f2f59f31744cbc8546f9ccfd68f753e8646</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.9MiB (199.1MB) – 3,533,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7492c20cc0fd9ddf3552d38d6f371c<br>SHA1: b2746fb84b0c5c06178ea600785fa7f1e1e31722<br>SHA256: fd5ddea4aa964f0594f407670bccf787d30c71c7d0494fe34ee4cfed04fdb559</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.1MiB (186.7MB) – 3,533,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 686db40244d7fa36e5c6200d72637d52<br>SHA1: 697db19565284f051d6d5f11cbed3e01b0a98a5b<br>SHA256: e51db4cee143e0731c57d0ea8bdf5d237b18c68f232b47c62fcb2b082f1f9a68</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.9MiB (189.7MB) – 3,533,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70ee7e27d07b5d32d9177379448db071<br>SHA1: bef8886ebd4b5f67800115d54f8263a16ce271ef<br>SHA256: 6a3d0b53b6852be8809215e50dd91770e4fbf9b3fe9f9cfb307257b25a8c84d8</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.6MiB (236.5MB) – 3,533,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5221ba2a347ef42889623628eae7957<br>SHA1: 2c60706564fcd277c97f7431ae93804083b99d72<br>SHA256: f7f45415125740e3dd193c1f870fdff9b045e7a3b6ea03e4dfbb6bf5898df837</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.6MiB (186.2MB) – 3,533,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a08686f2a9b623e1c6b6bec6e6840bb5<br>SHA1: 4e2ce32694dd5015ff997054c55266041541ce9f<br>SHA256: d356dee865d3dd2b7bbafa483cd2a1dd2fe52473e55d507484a3c5488a34b905</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.7MiB (230.4MB) – 3,533,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a6d614e4b56a190423f140f14c4cfe9<br>SHA1: a12ee83d2a5f7a6df0ba513e9ae601d6e4dd94aa<br>SHA256: a4f4b4c38111029e226e6ff784675dc10c692564426491e9c2edde276c50e48a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.9MiB (193.8MB) – 3,533,968 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6feb6030a3c58d6d640e8fb4f4a050c5<br>SHA1: e569951b2d691a0aea916711100493ba7644bc67<br>SHA256: b2931bf00b1d851b75b32af0d803883b95de46e5391d236d29678a6866fa484b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.0MiB (196.1MB) – 1,969,643 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15799e9250151d10236eb773be8b56c3<br>SHA1: 9355419f37073a7b98303d6e89e5ec77a45461ac<br>SHA256: cbff6f2e10b189e18e15dafaf0277fc1f7fd622f02f4ac72895af0fbce542edd</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.2MiB (200.5MB) – 1,969,643 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8277dd7e7eddafb63bb6d9bc499894d2<br>SHA1: c489937082e8c976eb2b3f218e8f2107eb94485b<br>SHA256: d4a971c5b4b2603e8175ccafde0ec698232abcbf6c6bca61a365fbca97aef138</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.7MiB (193.7MB) – 1,969,643 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0cdd0980bea79f12a652bc237b0e498<br>SHA1: 734277833f4884216e55030e6adb158dac7de211<br>SHA256: 68b39af32a2c8adb5911fadea8a87f04c06a847c40032376bbe39a47278375f5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.4MiB (194.4MB) – 1,969,643 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb5496a00540af6ab0203d9c3718cf25<br>SHA1: b88b97a8c78aa98618fb57262afe908f51f01fad<br>SHA256: d8ca91285a44e93b64dab1215597e31bdddd3bb4368436cd92cf5689a1103ab3</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.5MiB (215.5MB) – 1,969,643 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9ed60f2988bb6095b2a35ecea1ed51e<br>SHA1: 771e473d5e791e2d1c1a31c1317bd5ca5c6a121d<br>SHA256: 83b42f6b92ccdddd59677e787ee7254e61c1eaeda2fa71e145938a2ea1c53e0c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.5MiB (193.4MB) – 1,969,643 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db378d842c6891625c19b2f55bdc9974<br>SHA1: 81ffd020260d1385b2233070c2f6883dbeb7c0ff<br>SHA256: 51fc4d185ee4d27a53dd0df8d512f7f94fbbdb8b1e60986d2040fe50f26294ae</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.3MiB (215.2MB) – 1,969,643 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c9c641c16afa7db9a962a505abf9af2<br>SHA1: 44116354c081e7dd2095fd3df7b3eee1c7b45cb4<br>SHA256: e7e13da2750247963ea43ab9c1e3250e80c025c23881ee7f30c3c50f4a29d632</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.0MiB (197.1MB) – 1,969,643 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf107c2e8602612ed77b25df97176570<br>SHA1: cb9bf5cde81400490e83963c8b73769977da2d68<br>SHA256: 72418be57dc7763a805cf1b4fd3f4771a7a3ad32c385eef69737e6a65df5ef85</pre></details></small> |


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
