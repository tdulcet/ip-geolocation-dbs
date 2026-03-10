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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-03-10<br>IPv6: 2026-03-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 321,967 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 467962d9e37b202f2ab96eab7f75f26e<br>SHA1: e7afdb66a54de8a6d8689ba75a68042caddbf7c8<br>SHA256: 5cd2d0588c94e9554e4052b40faeab47baf366ad9156fa4a9a8a707ad1b4f5e6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.12MiB (15.86MB) – 229,798 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b08f7c95196cc5a4109c4101a76d9742<br>SHA1: 895efcb0a4085a92da1ac3070d438d063241fcf1<br>SHA256: 9d78a08cd7067aeafb445e317e67365da9a7605150eaaf4f287ce08e1bd197d3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-03-10<br>IPv6: 2026-03-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.793MiB (9.221MB) – 440,289 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a8e9df236d3ea751ab3b3b9f5c4434b<br>SHA1: 9086c4ea63b6365c71e39b6c9aaf23cd5793f9df<br>SHA256: ccb6773f578dcb9fb36ed8d45d036d3a84b617299da76be2c7147133bdcb82d4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.671MiB (8.044MB) – 116,690 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35eaf6a3f8fa3f117d7d39c08e517c45<br>SHA1: 35f09046fb6472c86e722b04933adc290bfc7248<br>SHA256: d70dd08a5e38170fd97139123bc738d92d33542511b500dbfd177b8aab723c94</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-03-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.18MiB (12.78MB) – 609,982 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2be925c1befd62f05e587b5d3825688<br>SHA1: 075f46905d76960098c96a0a83a8a3414981cc8c<br>SHA256: 2b23d0676ef3c7fc8a5e99be4c19167bd6b27c8abb5015ac459566d03c46720e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>109.9MiB (115.2MB) – 1,670,254 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73d07ca9421185677a423f75ed382d04<br>SHA1: 0621e765f591df70679f949a63da1cc7ff6fbd50<br>SHA256: 074d7b1709cbc44d6fb669a6fe717fc39c52cb08a426a1bba60e516308ab41f4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.906MiB (7.241MB) – 345,970 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be67480ebe04792eaa1e993732e26bbc<br>SHA1: b9c086649cbd7a697ce8b1a6f1200cf343683838<br>SHA256: 97e3ba0306a918694a1abd35fb0fbe18e3275c023a00d3f378bb52d0381e6ca4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.48MiB (17.29MB) – 250,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614f4ebb16bfdb3cd44828a77fb774d9<br>SHA1: be56f3e3114c6c18c1b7e097bb867772c72bf90a<br>SHA256: babfcc027ee9656b7ebe280a391c73174b4990721bda2e7c584c23450f4c5452</pre></details></small> |
| | | Full Location | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.5MiB (222.8MB) – 3,723,444 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d34e3013a398743fdc3bdbd816dba48<br>SHA1: 4f4868afd37a86dcd98f0ff21e863db08c4c69b8<br>SHA256: d805d064a2ceaeb75e8ee847780d1dcf8f54852ffa98bc007b0894fd1c1d24d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>446.9MiB (468.6MB) – 4,345,257 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b0322dcdc11f95be5a5b01f4221151<br>SHA1: 5bcecfc1d1a51db165a9a209bc8f4b9a5e7e1bda<br>SHA256: 9a67a943e4fadd058173607911c45bce627c5fbebc2abef2f229894d2e8fc57d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.241MiB (6.544MB) – 314,588 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55b7e48f1421f550d07e7c9cd5a0c7e6<br>SHA1: 5829ad0a8b167bd9c3f282bdb56fc9da0cde4f4f<br>SHA256: b661ed747da0e7db38a9a7ca6e153e650ab993d9eb063344338112bed6c3748c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.43MiB (23.52MB) – 340,813 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22be91078ff2881cce88f5313d02663c<br>SHA1: e9ff49d744cc908134d45f03c6a3fd6f3c96ddc9<br>SHA256: 54e30994ac133e20300ece1b194f449e99133ba86186c397266c617d7c1351ee</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>175.6MiB (184.1MB) – 3,034,529 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a603fd61b83f3b01a6bd0fab4efb56b<br>SHA1: 549a8cf265cbaab5a3fac95599e772935530b533<br>SHA256: be491b62db5ba103e1882a77b8bec049946bc21467308bed51465880485d27df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.0MiB (305.1MB) – 2,821,922 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca035a43d11f3bbee80eee6143bd368b<br>SHA1: 76e4190ec1692c0d53dce534df44d5a0aa79d017<br>SHA256: e42b6b838e8a46bbdf531ffa62fc7a715422c417ce4d9dde2b90659fc71da684</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-03-10<br>IPv6: 2026-03-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.96MiB (12.54MB) – 598,800 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a852e1e6569b04954383b386b1e11703<br>SHA1: 47daa83f529d47817e847a00f26c041cca743a66<br>SHA256: cbc9da91157d251ad69c81c94ce564da87ace301fed8b6cd9749032402d8a5f7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.98MiB (44.02MB) – 637,967 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 738a120220566522ef0dc51eb107bae8<br>SHA1: bf1b3efc08f4edcb274177339c55a3af775e59a2<br>SHA256: 0186ae417f5ce7c9b43d3a4662ecc9c2053715b5a8a5039ebaf7f984e2ffc4f0</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-03-10<br>IPv6: 2026-03-10 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,535,509 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0aa8b72a490883d9bec29b32ccf471e4<br>SHA1: 285ea7f74eb5c9e56a806dfa8eb26c5d910fbede<br>SHA256: d62f8169da2b62eaefc3af3a573c23e336054d7904a576aa794ce9a04058f8ad</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.0MiB (199.2MB) – 3,535,509 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5794cbbea842b6ca67c5ae9cd45ecbbd<br>SHA1: 245df4620b21b4888f6882638a232d3764f77be1<br>SHA256: c5a7af3090bcdb9580cb06aa28ccb157cdcc93ef551ce8dc5852cb1c45c934dd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.1MiB (186.8MB) – 3,535,509 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5141222cc9d9d3fd77172bd45f57904<br>SHA1: 38be53068def0e26592f236e81522602e963a34e<br>SHA256: 0b190fbaa97cc360c88da140410039a23a8a68b7a026de1db3beca6debaaf158</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.0MiB (189.8MB) – 3,535,509 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14b9ef90f3978a0b70edf32815053cd7<br>SHA1: c05fe7e2721dc56fecf23259545453f98d20dedd<br>SHA256: 494458deed76d456dd4ff21751cb3d42101b84d9957638b89c63cba59c1b963a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.6MiB (236.6MB) – 3,535,509 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82568acf92b2052c5f6b6f15be9f99aa<br>SHA1: 24d67ff4e92048f501bbec6dc71b57b2d5447766<br>SHA256: af2d08678d2581f80dec0b88697b04975f88615546560f839247eba849b8cbe1</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.7MiB (186.3MB) – 3,535,509 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38b01745c25d097cb061a35b333a1ae7<br>SHA1: 8783d0ed265ad2085830bee1b3707bff2434820c<br>SHA256: ed715702da6713e5d2b52041300d54ba93f6e62d5b2e3bdae292d70cac7de0ab</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.8MiB (230.5MB) – 3,535,509 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f026070698d239cbd2df6a9e708a1e62<br>SHA1: 2945fdcf1a1dc5fee5350abc47081cd6848ceb63<br>SHA256: ae729ee0a0d591f414b2e774bcb774837f9b9e61928e588555d63702e3d20484</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.9MiB (193.9MB) – 3,535,509 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 326a863a39fbea8d48f2f19da918b5c0<br>SHA1: a1a296e12bf844090ecfd9a9a7586cc07d96ec49<br>SHA256: 9ad783d61ed71cc13b2764d71618ef8a30b4704c772e2721683f25f157871503</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.1MiB (196.2MB) – 1,971,971 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fc5aaf55c0efc2573ab11ba6587a61e<br>SHA1: 0e272527df05f38c3853006610ffaa9bbf45d057<br>SHA256: 8414b040c0f7b677b085ae80e172c26ed0963bd87b046a31f49a04c87af1e556</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.3MiB (200.6MB) – 1,971,971 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eedce98170691b52a533723c85411a9a<br>SHA1: dca4a07e5dde1ab0291bda80e4d56f339eaa32d9<br>SHA256: 0308e9e88f6662b8d8dc4cb40a467e2f257c0aca2042d7c6ab755a0b638e19ff</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.8MiB (193.8MB) – 1,971,971 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53e9aa19de9f5a37073305686670de95<br>SHA1: 75e1ce01551d12cde112fa12567ed98436ba4d76<br>SHA256: 9be3967f8d107d69669078b6cb7e3aa2f5ae0dc4b64d226e13d7c3e5c87617d3</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.5MiB (194.5MB) – 1,971,971 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 366296cdf60e3108481e35de546e80a7<br>SHA1: 1c79f23d0d54bb8ec93fba994bfa86ef4a8aebb9<br>SHA256: e6819eaa7b5cd642a1a670b6a48aada815a06e97f4fc9d16ca99d6e3ecf5fc66</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.5MiB (215.5MB) – 1,971,971 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 729e274b66e18ff94a79d19e4ff5d960<br>SHA1: 2314567f92dd6fbde37bd5c61e31e7b2186b930b<br>SHA256: ea48897410e059aa8f94e97aa0e678ea3a57c61a2d2ba860d13525a2d6c4d7fb</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.6MiB (193.5MB) – 1,971,971 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f4724e73b5bd7b25d9b151c713e2d0b<br>SHA1: dc24e7f50ac03756455d1c25d9edd7c307b97fb1<br>SHA256: deada9266a66581523e2f5e359fcb28cf835a6b6885ba98b1b6d294afd1e5c1b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.3MiB (215.2MB) – 1,971,971 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf58db4222f6d7308faf11de1ea3d942<br>SHA1: e55ca4bfcb6aa6b4122643ca202c8928a7a3ca0d<br>SHA256: af7f2af50f8c276e70f2747f15318385984558d0f8839944b3af2ff670c6389e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.0MiB (197.2MB) – 1,971,971 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a8b90d8ebebab03797780dbbd0d00a3<br>SHA1: 8b1c445c66f0255291e09d264298403cad4a44a3<br>SHA256: 5c1bf1ac85fd9aae4bf8cd16b704ea9b478b73f2f4d1684798c016d5912e3244</pre></details></small> |


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
