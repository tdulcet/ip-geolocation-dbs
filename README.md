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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-03-09<br>IPv6: 2026-03-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 321,933 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5483ac9895399898db6d7f82b5748ea8<br>SHA1: 878cffb95a0ffc7d4fc823ee6cf83a26ce9a3f4c<br>SHA256: ab6623973a716c56296a962b6ce41c7624212d03d63b60b47e182a633983e9ad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.15MiB (15.89MB) – 230,232 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ce54f70132b0815c07e506f02556a02<br>SHA1: ee78019835417f514df9cce68143df354d00228c<br>SHA256: e57c19cf3f3cd8d4c88581edd1abec9bd28b20a93ba244a7b1cdcfa1990d6532</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-03-09<br>IPv6: 2026-03-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.788MiB (9.215MB) – 440,029 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e7bf69bfd2be413e3deb820a12f471e<br>SHA1: 8e586e708d496a44be75223ec7dda0e2ea856d80<br>SHA256: bd81a8b561a895b3146f2d1f5866e50f4f3333829ca612714da6e93bb3945e5f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.666MiB (8.039MB) – 116,620 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f064b3a85437a5ee5fe4f3192819b0ba<br>SHA1: 32815d5fab9c2911eb8978c741f9aed686565565<br>SHA256: 3b8a048d01ac1c5f2062e734887218e2c016b20e3584756a8ecfed5d7ff7f488</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-03-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.32MiB (12.92MB) – 617,024 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b9acecedbf179b6ba904d5d0667729a<br>SHA1: a5678e6f31adb886b633286d189217c8cef061c6<br>SHA256: 62df58a1f1423a1127975f8dc08f3b4460447eefe4bb29b2cd3866092bf36217</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>112.7MiB (118.2MB) – 1,712,937 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0178ecd8c22a9e32859dfebbc72c985<br>SHA1: 9754100d531d34810bbcf23887241916a8202c80<br>SHA256: 43934d0f88561225cf51cfdb00753a9949fe48d228ce6dcfeaaac4d492bdedfb</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.906MiB (7.241MB) – 345,970 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be67480ebe04792eaa1e993732e26bbc<br>SHA1: b9c086649cbd7a697ce8b1a6f1200cf343683838<br>SHA256: 97e3ba0306a918694a1abd35fb0fbe18e3275c023a00d3f378bb52d0381e6ca4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.48MiB (17.29MB) – 250,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614f4ebb16bfdb3cd44828a77fb774d9<br>SHA1: be56f3e3114c6c18c1b7e097bb867772c72bf90a<br>SHA256: babfcc027ee9656b7ebe280a391c73174b4990721bda2e7c584c23450f4c5452</pre></details></small> |
| | | Full Location | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.5MiB (222.8MB) – 3,723,444 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d34e3013a398743fdc3bdbd816dba48<br>SHA1: 4f4868afd37a86dcd98f0ff21e863db08c4c69b8<br>SHA256: d805d064a2ceaeb75e8ee847780d1dcf8f54852ffa98bc007b0894fd1c1d24d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>446.9MiB (468.6MB) – 4,345,257 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b0322dcdc11f95be5a5b01f4221151<br>SHA1: 5bcecfc1d1a51db165a9a209bc8f4b9a5e7e1bda<br>SHA256: 9a67a943e4fadd058173607911c45bce627c5fbebc2abef2f229894d2e8fc57d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.241MiB (6.544MB) – 314,588 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55b7e48f1421f550d07e7c9cd5a0c7e6<br>SHA1: 5829ad0a8b167bd9c3f282bdb56fc9da0cde4f4f<br>SHA256: b661ed747da0e7db38a9a7ca6e153e650ab993d9eb063344338112bed6c3748c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.43MiB (23.52MB) – 340,813 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22be91078ff2881cce88f5313d02663c<br>SHA1: e9ff49d744cc908134d45f03c6a3fd6f3c96ddc9<br>SHA256: 54e30994ac133e20300ece1b194f449e99133ba86186c397266c617d7c1351ee</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>175.6MiB (184.1MB) – 3,034,529 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a603fd61b83f3b01a6bd0fab4efb56b<br>SHA1: 549a8cf265cbaab5a3fac95599e772935530b533<br>SHA256: be491b62db5ba103e1882a77b8bec049946bc21467308bed51465880485d27df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.0MiB (305.1MB) – 2,821,922 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca035a43d11f3bbee80eee6143bd368b<br>SHA1: 76e4190ec1692c0d53dce534df44d5a0aa79d017<br>SHA256: e42b6b838e8a46bbdf531ffa62fc7a715422c417ce4d9dde2b90659fc71da684</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-03-06<br>IPv6: 2026-03-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.96MiB (12.54MB) – 598,749 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8aca77cfadeb621b98b01f911775f45<br>SHA1: bff18b9295babde71d1e637ffb9d450e977cc563<br>SHA256: 2085868a8df0cd1ec27ed3eb8772fa80f2f519c736e64934735c8d6c99a82de2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.79MiB (43.81MB) – 635,004 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec275fc5136323169d6bced6261beca0<br>SHA1: 40f0d6c25bac556f42f68027470d35641c521992<br>SHA256: 45c8cbfb33fbf1895a4a19114b85a294be1789629c2cfa5804b01c0f406e73ce</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-03-06<br>IPv6: 2026-03-06 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.4MiB (187.1MB) – 3,525,648 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97a394e6980f63df077ee98e76b11a4f<br>SHA1: 33f8738bb8d504aa15f6023d6711e3f2656bda9c<br>SHA256: 6bccafe9facfd12a1e021e4a3b8f75b5a6d30bb4c5a931ff94e6d3cde899c69b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.3MiB (198.5MB) – 3,525,648 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a96efb8a36969ed68f753bec114ee54<br>SHA1: db14044880717caf3f5b39d6e7c22e293749cead<br>SHA256: 6915e7e583bc660066209e9ea9e1295a7cc92322c86ffb6232f0f149639e69fe</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.6MiB (186.2MB) – 3,525,648 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a83bf14c57f8dee7895900d1655e1f2b<br>SHA1: 8bc63585476ba1b0eaf0da64ca6573be649fb12d<br>SHA256: 00297714e8dcb394439e8756b5a4924b1dc73ca5bf6dde1c6928c23338e75483</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.4MiB (189.2MB) – 3,525,648 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf918af25971be5b1aaaa29a74f4cccf<br>SHA1: 34cd11fdaaca4c136b060ff872d65404e943a6f9<br>SHA256: e9699c72db510fcf6b7d20c18527eac9271572d93ca274b671f6290cfea9c5f9</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.9MiB (235.8MB) – 3,525,648 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4932d32f97b9fb0a076c247222dd8c3f<br>SHA1: eb10eaffc63db42c01c7281410a06468bca2ef92<br>SHA256: e34acdcc4ade40233cc97ab937698e89dd0d7081ddade6047383773e054e8793</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,525,648 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c730dc76ddd1abb19bf385d835364cfc<br>SHA1: 0254f7954303b0955a38eac43c4615dc67cd0153<br>SHA256: e234f3887e232baeec855f886e6cd5d89709405f2526a3f052924f85ccc72a28</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.1MiB (229.7MB) – 3,525,648 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdc50350d29b9401319a20b01d97342c<br>SHA1: 029cc4dd7b8937046a3e181d75cded2d2cafb768<br>SHA256: 9832c4e45ce1393bf8ad21a3047082ab0231bf56b58d9c3930b7b614119eaf17</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.4MiB (193.4MB) – 3,525,648 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a478c34bdf42b9cd7f87072e5c9e74a<br>SHA1: 17f5364f43288f328ef9fb4099dca41f9b215765<br>SHA256: 4d79d185994b2707865e7e7fd2a0d236640160669c346f131c69b4b55d20f15d</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>185.0MiB (194.0MB) – 1,950,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa5db7e3005491e1a9cca60ded463b84<br>SHA1: a1f296108d4f43e90d2e621d5805164d791f8b43<br>SHA256: 524eabbe0e405b1f8839f862dec79637ffe0177d833c9e1daecbe59c002658e4</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>189.1MiB (198.3MB) – 1,950,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92f2b377ea78a29272d9757ffbf5add4<br>SHA1: f610c42fb4496a7b6cc1bae83106fb35ec5c3c32<br>SHA256: 8d8e9d3471c85445ca987d9e17e4ae5dbc1625e05962d25b8435ea0c262543e1</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>182.7MiB (191.6MB) – 1,950,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67401407960037630d45a45f5ab8d194<br>SHA1: 33f98ecd7a165924afdcc0643da9f93d6d168dcd<br>SHA256: 1a4575223c9b99a5ea3800fa7d82adfa370976bb75d6f3324c3952f9c9135d5a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>183.4MiB (192.3MB) – 1,950,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 050db5635d2d04e734cb736062dc8b16<br>SHA1: 6315086cda476898009e6612fe7606ee8f23b0d1<br>SHA256: cc7df44cd9d18b26124cab943595c7426009dd5e33bda4195696e66d59b8fceb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>203.0MiB (212.9MB) – 1,950,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eff52de24b4a51db33536612666a9a58<br>SHA1: 0b23d5d100a8e84d4426d677bf5322f84304df9e<br>SHA256: 60c96f2d4e5c4b0687f9a7ad8c1c16017a6cef66f5848fe9e611495ed63ddaed</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>182.3MiB (191.2MB) – 1,950,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afc21d85f3c37d21126c3ee103a32560<br>SHA1: 89d4ffd4002cf6d111971b2214b108a1717111e4<br>SHA256: 5998c8e7b1aafff75a2631330263cc34516ff15a84e8d4d1a26b61ab697ce7e6</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>202.8MiB (212.7MB) – 1,950,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 962adbffd38618edb33b43b7ff17ffa6<br>SHA1: 8917645e194f305866daf4a6e5472d6ac048d137<br>SHA256: c83775ddf74a5c955c7e2ca25dbc6012d5913e17428d12f92dea973b6f95d5d3</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>185.8MiB (194.8MB) – 1,950,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7dc3dcdcc75c737d758bcb9eb96557f<br>SHA1: 7b94e28b7d25b468018fbba6b6e5f14d6be2bb2c<br>SHA256: 8fc3cc5645cff873b15bd373098a68ad36b63d5f8cb332c023969c110dc289f8</pre></details></small> |


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
