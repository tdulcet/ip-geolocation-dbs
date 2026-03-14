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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.432MiB (6.744MB) – 322,083 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0365c5eca9440e1b55c5881a6e4921e<br>SHA1: 18cdd82941bd5116534c36040592fa1c14568867<br>SHA256: 43de6a44003716b49d5d88373e3d2634e6a0b0a4c344f2a38399e94220314cfc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.18MiB (15.92MB) – 230,762 rows – 257 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35da3ce2cc86eefead956e5eb4eb3d81<br>SHA1: c8412861f93fcd13dd5ae90891a0a3cdbb3287e9<br>SHA256: d7f96353fecbe3e552a2a3abee4ba8cb4cd856a6df8b7e448ba9028fde2bf6d3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.806MiB (9.234MB) – 440,944 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfa7252ad980131d40bc3aa25a96df55<br>SHA1: 9a6b8c7fdacc8889276c3c14d0492c15b5cb425f<br>SHA256: a069d748a9581c7116a0b6839aaa67095c81f7c7886fb513aae111d0a453c6d4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>9.861MiB (10.34MB) – 149,963 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 396aff9c6c562308bc70e92e853e0d24<br>SHA1: a5c4bc206f15f09d61b2e2a09ccc1e87987e63a3<br>SHA256: 70ffe378f40022e48dc9535b2a1b6c6e15015d0b7d07a8d94e834117209734a6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.20MiB (12.79MB) – 610,706 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f217f3befe46cbcc3599eaffd8578bb3<br>SHA1: 3d7155805561143dd13ba9c0ff391b2177a7a513<br>SHA256: 0c9f781840255913b4cac081a3210b33d1ac7c996cb82c73e823af9b279c29e8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>108.8MiB (114.1MB) – 1,653,412 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfdcebf30b1df139d3b74402fad02585<br>SHA1: 39657bc0dd801a0e825e8602253c023f329bf021<br>SHA256: 7fcb3d15a10e6e6d81bccd5fe57d4edf915e6bf50bd73c5eff34b5c6a9c22f81</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.906MiB (7.241MB) – 345,970 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be67480ebe04792eaa1e993732e26bbc<br>SHA1: b9c086649cbd7a697ce8b1a6f1200cf343683838<br>SHA256: 97e3ba0306a918694a1abd35fb0fbe18e3275c023a00d3f378bb52d0381e6ca4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.48MiB (17.29MB) – 250,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614f4ebb16bfdb3cd44828a77fb774d9<br>SHA1: be56f3e3114c6c18c1b7e097bb867772c72bf90a<br>SHA256: babfcc027ee9656b7ebe280a391c73174b4990721bda2e7c584c23450f4c5452</pre></details></small> |
| | | Full Location | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.5MiB (222.8MB) – 3,723,444 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d34e3013a398743fdc3bdbd816dba48<br>SHA1: 4f4868afd37a86dcd98f0ff21e863db08c4c69b8<br>SHA256: d805d064a2ceaeb75e8ee847780d1dcf8f54852ffa98bc007b0894fd1c1d24d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>446.9MiB (468.6MB) – 4,345,257 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b0322dcdc11f95be5a5b01f4221151<br>SHA1: 5bcecfc1d1a51db165a9a209bc8f4b9a5e7e1bda<br>SHA256: 9a67a943e4fadd058173607911c45bce627c5fbebc2abef2f229894d2e8fc57d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.241MiB (6.544MB) – 314,588 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55b7e48f1421f550d07e7c9cd5a0c7e6<br>SHA1: 5829ad0a8b167bd9c3f282bdb56fc9da0cde4f4f<br>SHA256: b661ed747da0e7db38a9a7ca6e153e650ab993d9eb063344338112bed6c3748c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.43MiB (23.52MB) – 340,813 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22be91078ff2881cce88f5313d02663c<br>SHA1: e9ff49d744cc908134d45f03c6a3fd6f3c96ddc9<br>SHA256: 54e30994ac133e20300ece1b194f449e99133ba86186c397266c617d7c1351ee</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>175.6MiB (184.1MB) – 3,034,529 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a603fd61b83f3b01a6bd0fab4efb56b<br>SHA1: 549a8cf265cbaab5a3fac95599e772935530b533<br>SHA256: be491b62db5ba103e1882a77b8bec049946bc21467308bed51465880485d27df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.0MiB (305.1MB) – 2,821,922 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca035a43d11f3bbee80eee6143bd368b<br>SHA1: 76e4190ec1692c0d53dce534df44d5a0aa79d017<br>SHA256: e42b6b838e8a46bbdf531ffa62fc7a715422c417ce4d9dde2b90659fc71da684</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-03-13<br>IPv6: 2026-03-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.96MiB (12.54MB) – 598,820 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a70e1ee8d3812fa283594091f0f6951d<br>SHA1: 09458475ac44b374cb4601bd3055affa1a641d2d<br>SHA256: 718875b5788e1e2f2252efc686efa3ba1dd5881f37ac3a484b74ff7b43d31551</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.97MiB (44.01MB) – 637,873 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eafe08b4156880fda2566d25f8adf821<br>SHA1: be8cd8c9076201a9ffe972f18078fa7f212264a7<br>SHA256: ac06408f96a076b29cf06d78d59f7d5d5b587cee45d6bf0c5aa73efdc1cd331a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-03-13<br>IPv6: 2026-03-13 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,535,712 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 615f292e867b56d297b82c890b1c78a8<br>SHA1: 1d1eb7913ed106b24c104338dab8392f001711f1<br>SHA256: d311c2736f1fbed40e591acfd5355da6e1cbf4ab5fecab87bc08c15779f503b5</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.0MiB (199.2MB) – 3,535,712 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3fa9859ca6df4e0605e34f9d53c5fc92<br>SHA1: f269924e2cc301596faaaad082b828fad3fe8dc9<br>SHA256: 10396d42adacc8dec1ea51d8ff9b79dfd871b0ac3f7ccbf71ecb9133ff4afd5a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.1MiB (186.8MB) – 3,535,712 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc93b5643605ff659e00134cdb80ad23<br>SHA1: 9d58a3d1efcf8980988f185432d41abdecf8df40<br>SHA256: f93e076570e45b58884e3934852fcb860eec5edb4e64c55314760f82f47e47ee</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.0MiB (189.8MB) – 3,535,712 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1f91ae828afdd8272864bdd736b123d<br>SHA1: 4979bd550f30933a7c7bc3ae5a4c75d52d417f1c<br>SHA256: 2d7afd14a50bff4d4c82cd7d09e529c8bedb778bd7378294655e13706d4d158b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.7MiB (236.6MB) – 3,535,712 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07e9281fc4f9602963b93cd0c57e2763<br>SHA1: b15bf5037dad450b28889b3734f8558f5e490f35<br>SHA256: b9e922a6268bd23fca95332ffaffaf7df4a1366314de652541c9063061cb3e75</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.7MiB (186.3MB) – 3,535,712 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb0bf7e165f7ce35588f3be6108c4d12<br>SHA1: 5ac63a9226e4d3b673d9b99619b95a11eddebfb4<br>SHA256: c37223f77479004417a60ffd1dff057f9f8c74f0720053085e304ab35639d9f7</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.8MiB (230.5MB) – 3,535,712 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa10db651942c0efb10148f83b7c84b4<br>SHA1: 63374f405dedee026166c1f2af49bc0dbac5e623<br>SHA256: 99a35bb19f4486ce42d68f1a71c51802703256eb365922ceb7599e9464301d60</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.9MiB (193.9MB) – 3,535,712 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a2800532c466adbd57d09371dd33d97<br>SHA1: 622a26047a0ecd68dc39fcce22b8102e2a3f1a80<br>SHA256: 3e328a612d9bfc597d5516a7f3ee1b7bc156343561618b3f907c7005b2b0adfc</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.3MiB (196.4MB) – 1,974,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d55d3bf10b31809535ebb6dc011bc314<br>SHA1: b25dbd762a96ab862abf9cdf0b0fd3b9f820cb44<br>SHA256: 855a49e806725ce17765766123aebc62cb783d0d547c94b7b53bed79eeb3bc04</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.5MiB (200.8MB) – 1,974,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32b16e8fc88d25f30ef6691237683f90<br>SHA1: c04eceb41670cc7faa8bfd5bec448fe3f67f6ee9<br>SHA256: 09fcf12cdf78dc4879ebec76b131c8269b37dfbfc90bc5fd4344df106c83eb99</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>185.0MiB (194.0MB) – 1,974,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac463a7555dfc790e72fbe0ffc74e866<br>SHA1: 1e5ac0f82527b825e369c9737cb9f700d6733634<br>SHA256: 615dd2ad28755483b5eee2fe042f2ee10344276d707d276bdd47acab688dea84</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.8MiB (194.8MB) – 1,974,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffb61bc9f6dee2db8bf1d64191186398<br>SHA1: 39cfb585b5a044ee82bea7fd2cea7e37fc60370d<br>SHA256: 1561b62db03f55832ec317ebec7e1c1a37736a9617a4ded46f25ae4c5f3d9806</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.8MiB (215.8MB) – 1,974,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52123ed074bd6fd3b1bf8c8e0455b412<br>SHA1: 41d3e43c5f4365932a3adcd2b09b6c69edb7f235<br>SHA256: 146377a2ad279e8465cfc717991774fb0922808d0e702cef5071010ee80b4f23</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.8MiB (193.8MB) – 1,974,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5655586f97c216680773146e566f59e1<br>SHA1: a2377a35d277063459e4981584f27fb0c24b3773<br>SHA256: b8a014c86f9f1acdac623b5daf88f9efb14cab31797ebba5cd20644212e1db51</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.5MiB (215.5MB) – 1,974,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f08c467e253b95b1e5d167d92d9d0cca<br>SHA1: 5dda02a87bf29b195ffa1fa8001ccc24643723c1<br>SHA256: 3541ac73693f0e29a37bf3f223802fab9a06d8cb6d3420dee86c6c6b94e96d48</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.3MiB (197.4MB) – 1,974,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e02f171d2cb1f08eaf6fb4f3ae47f3af<br>SHA1: 47e1644b2842a5d13ec7e3dac98dcb8a249d65d1<br>SHA256: d4cf1ab31668619526d3ed535bc1170ddb1b4d4aecc1c95ca7f82f4bedf8bc69</pre></details></small> |


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
