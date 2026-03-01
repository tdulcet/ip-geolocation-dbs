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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-03-01<br>IPv6: 2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.468MiB (6.783MB) – 323,892 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33d9b3c5763bcb56db50d06e98f6193c<br>SHA1: fb9a4f472d66ce80ad56dec38210e159c8d52091<br>SHA256: c4707a42fd6fe151a24ba8cbf4962c35fe790db525068db1621d5beac58d1f2c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.23MiB (15.97MB) – 231,460 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fe54e5da0de8dbff79c97125fb7d6e3<br>SHA1: a99974aa06d22fa0ff28b7a47670b0b7cc7eb83c<br>SHA256: 0b8329da1a5a07ae12af36da335c4904549d6cced6f2e07dcb999f4af0a5694c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-03-01<br>IPv6: 2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.785MiB (9.212MB) – 439,888 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7bb33d641ab0a69a1e6fb0becb5dbe9<br>SHA1: f911d9e4a4b38682b5f8015fe4d3e4dd3b966c48<br>SHA256: 8a93a91bacdda417f0053ced030a1edf4a3c606fc66cd291835adf335169f70b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.638MiB (8.009MB) – 116,188 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9549231e5fa5a3e2002f3f7e134b689<br>SHA1: db46595bddc5f4f283407cacf011a72f731f56c2<br>SHA256: a7c06461ff0e1c67ad1e70fd09c117d511c1bc7b54b499ed3884981ef1988160</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.14MiB (12.73MB) – 607,604 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d39666d964f366a89ed9e57d10b80b78<br>SHA1: e744fce378597e88d360a8c7a05278df1bfd3c5f<br>SHA256: 073e16b8d21b9a1d919ef675a6584fb050ebf874557ef11ac3abafa4ca1ae36d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>124.3MiB (130.4MB) – 1,889,304 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f26bce3c168738904135ea6ac7a8b341<br>SHA1: 20aa43d463f77717a93ad740f576596d36d8d52f<br>SHA256: a3918af444e2b45a22abb266d26879ecbbee6206b1b9928e0a147947b321ade9</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.906MiB (7.241MB) – 345,970 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be67480ebe04792eaa1e993732e26bbc<br>SHA1: b9c086649cbd7a697ce8b1a6f1200cf343683838<br>SHA256: 97e3ba0306a918694a1abd35fb0fbe18e3275c023a00d3f378bb52d0381e6ca4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.48MiB (17.29MB) – 250,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614f4ebb16bfdb3cd44828a77fb774d9<br>SHA1: be56f3e3114c6c18c1b7e097bb867772c72bf90a<br>SHA256: babfcc027ee9656b7ebe280a391c73174b4990721bda2e7c584c23450f4c5452</pre></details></small> |
| | | Full Location | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.5MiB (222.8MB) – 3,723,444 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d34e3013a398743fdc3bdbd816dba48<br>SHA1: 4f4868afd37a86dcd98f0ff21e863db08c4c69b8<br>SHA256: d805d064a2ceaeb75e8ee847780d1dcf8f54852ffa98bc007b0894fd1c1d24d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>446.9MiB (468.6MB) – 4,345,257 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b0322dcdc11f95be5a5b01f4221151<br>SHA1: 5bcecfc1d1a51db165a9a209bc8f4b9a5e7e1bda<br>SHA256: 9a67a943e4fadd058173607911c45bce627c5fbebc2abef2f229894d2e8fc57d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.241MiB (6.544MB) – 314,588 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55b7e48f1421f550d07e7c9cd5a0c7e6<br>SHA1: 5829ad0a8b167bd9c3f282bdb56fc9da0cde4f4f<br>SHA256: b661ed747da0e7db38a9a7ca6e153e650ab993d9eb063344338112bed6c3748c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.43MiB (23.52MB) – 340,813 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22be91078ff2881cce88f5313d02663c<br>SHA1: e9ff49d744cc908134d45f03c6a3fd6f3c96ddc9<br>SHA256: 54e30994ac133e20300ece1b194f449e99133ba86186c397266c617d7c1351ee</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>175.6MiB (184.1MB) – 3,034,529 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a603fd61b83f3b01a6bd0fab4efb56b<br>SHA1: 549a8cf265cbaab5a3fac95599e772935530b533<br>SHA256: be491b62db5ba103e1882a77b8bec049946bc21467308bed51465880485d27df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.0MiB (305.1MB) – 2,821,922 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca035a43d11f3bbee80eee6143bd368b<br>SHA1: 76e4190ec1692c0d53dce534df44d5a0aa79d017<br>SHA256: e42b6b838e8a46bbdf531ffa62fc7a715422c417ce4d9dde2b90659fc71da684</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-02-27<br>IPv6: 2026-02-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.97MiB (12.55MB) – 599,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 607d953b3cf05524901d7d4950156b7d<br>SHA1: d9665142f55df5b278bdea17b3e1922f333de9d2<br>SHA256: 7f19c3611ea3345cfed39143414d6d806c88044c6474670ab60c141e7fff23ab</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.37MiB (44.43MB) – 643,875 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d17edb4001723fc08afcf892c42a52b5<br>SHA1: 95eba56cadf3b34b22f9ec1ba944746e1cb96b4a<br>SHA256: 1dba16f41b143c2d7d52f686947f9536e6c7a6e312cd4a2c68cd12c1d560c5da</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-02-27<br>IPv6: 2026-02-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.3MiB (188.0MB) – 3,542,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a6b1fb740322af03ca11ba5c4f0bda3<br>SHA1: 5e1b4c398ef5c8364ef06311ca81aa8558ce25ba<br>SHA256: 7c115d2a612bf2617f30e9aca75bbd13047f67fc05b7a9648cb5663438b37dab</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.4MiB (199.6MB) – 3,542,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 632bf8646b2e10c55ad6af8fa9dc2523<br>SHA1: 373e12eb037e4b7f93c64faef66c000a5fde396e<br>SHA256: 885567adcebd5ee29c1e05deeb49e39639407fbeb5094c45cae27906b741fbd0</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.5MiB (187.1MB) – 3,542,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d00bd0350bd87f0fd6dc3b4848283e<br>SHA1: 566b27ef9fd369411d511625cf89d540f055f167<br>SHA256: 8cebb51821713245761b93a017a8737f9a16b9098990beccbaa5e6d44e1a439f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.3MiB (190.1MB) – 3,542,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0fecdf2615b478a0e12a2c7eed210e5<br>SHA1: 905f9a9bd519875b0aebad4cef0564c2af2b23ec<br>SHA256: 9ab275664ca7e07a3f9b4fc4a4bf1e718411dbebd222d097bd34244961a1d1b9</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>226.2MiB (237.2MB) – 3,542,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9115f381355e4fe66cc8f65495c1d802<br>SHA1: e14b9c28774f38008ebe487d9ecddfd5d5186450<br>SHA256: 6c9c9a007dc0489e14d5f9fdd8ec7ff93809846c4de0bf881d76be90bb461ccb</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.0MiB (186.7MB) – 3,542,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a67950df3f838736660cc7e434e2e82e<br>SHA1: c9c5b0053cb02fdf8722c1f6efacda6b769f05aa<br>SHA256: 6d1fcfaf9d5cfa25287408268aa11491afd40a1498648e0be017dfbdd34acebf</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.3MiB (231.0MB) – 3,542,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0ed41ecfabf0c03b82bd9428d502ca6<br>SHA1: 9fc737a4577f973de312406c720548c290e81dd3<br>SHA256: 68eaaca5c7f8a987e9c8b78db85104e990ea83877f2984befbc77e4cf1f3bfc8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.4MiB (194.4MB) – 3,542,468 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2f63603ef6c931b02dd6c01cac9a5e3<br>SHA1: bdfc569899151a3ae0cc382053c04652f5eec655<br>SHA256: 02db7586614abd737de511eaf9b05ec9ae0a0e6b3316e448434d87115bde6636</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.6MiB (196.8MB) – 1,977,474 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d89850e8ca18966a68da1075a9f03424<br>SHA1: 8b6e568d414bafb2142d06eca1a1f085b4f2c2d8<br>SHA256: 86b62ba63d6cdf3231ad9c8195861e35dc5d705679736da2f806cfcc45b1a451</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.8MiB (201.1MB) – 1,977,474 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd4b0e93d81f94a041772f782f8c3379<br>SHA1: dd7b1a7cd1378e41ee6df2028d2fd704a3cd5121<br>SHA256: beaddb8d8cfc2dece91d9bef64c0790676974616673d54ef5747a91201c8ebfb</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>185.3MiB (194.3MB) – 1,977,474 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5fefe2b8166f602f077a47f15e138618<br>SHA1: 0e9380e169afda94ac81a6f45596dbe15913130b<br>SHA256: fa671ae98088ffd248d83caeb58836f1ee27c681bc0ece2a8ec263b909afcc53</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>186.0MiB (195.1MB) – 1,977,474 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 374a3cd346c6fed4f9d7135bfd2d312b<br>SHA1: 23fae7ebb286021673e23ebaa7973d5f533b8279<br>SHA256: c5cd5c745e257c6be87a02b77dbd7fb3181bbe052e0d8145bb7f94f0d49e9643</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>206.2MiB (216.2MB) – 1,977,474 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 039c991454a3fd23c971750bdd40bc9d<br>SHA1: c9c5a5b06fe17674eb5974cc9770a99e24ef7696<br>SHA256: 8b53f829585fb3bcd4c8989f4076d6cd14b93b24d704facacaf1b6c93c0f69e3</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.9MiB (193.9MB) – 1,977,474 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 938256bf646d84b264ea7555598ef505<br>SHA1: 3050277e911d3b7f119cb4ad331e037f0fcdc782<br>SHA256: 535748e38a38aa44ae5c73e86b2d3de065ceac14a5b16bf5aa552e16319187f1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.9MiB (215.9MB) – 1,977,474 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d348e40c257d9ba09230b9350eef9cfb<br>SHA1: 497fa9f22875b83ce2edf021281bcf9ba00f36e1<br>SHA256: 918d8925ff6454e63b7e6102efbc206615e8e5bb029f30c822a4a16cb599d47d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.5MiB (197.6MB) – 1,977,474 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 146487e669a8b76f5b252b6ac860d7a0<br>SHA1: e63ed8542f0feffbc4e0edcfd350cc5c0bf9e5e6<br>SHA256: 438689f45971621037117eba61eaebaf18658443931bdb01866f3195c44240d0</pre></details></small> |


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
