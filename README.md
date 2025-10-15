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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-10-15<br>IPv6: 2025-10-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.337MiB (6.645MB) – 317,335 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0154dec9499646fd237a5c30ba431315<br>SHA1: 73b92532bca5054c9f1e2eb5c262129acf5d8164<br>SHA256: 5eee6a9ef9e2f53a770f4efc0e8a59abd1f5c759add719db189c7f169134efaa</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.94MiB (11.47MB) – 166,227 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb115b0cf059a44ce76f581685893f0c<br>SHA1: b0603d1c4217cd8ec32c7e553e0e3b818e7f3ce2<br>SHA256: 413effbb94d27acea5385aa1bdadbad24f0c09cf4b7a2bb157c4a7345a5388b5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-10-15<br>IPv6: 2025-10-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.706MiB (9.129MB) – 435,927 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d70fb02f96dfdf4a095e5c5ac65bf80a<br>SHA1: 34aea1de6bdb6e8cdcf7cf0b73acca64d3dcc8f7<br>SHA256: 190728c1a0d9dd2a7e62509a4cefd8b0d076e07d705155748f29e1ceaf500e0f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.390MiB (7.749MB) – 112,418 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52406eb467d2373e7e0c25b396e83987<br>SHA1: 239cb6cfb96018870cc38f5b3672f70a617edb03<br>SHA256: 0edf300c56baa5ba5db01a8b79688853394eab872ec4474763b612e542bccca4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-10-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.68MiB (13.30MB) – 634,807 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48f1c2741a49ffe4e4e3d532d701013f<br>SHA1: 7eb9dfcdbabdd5624588a6fd6a7a8712badca90b<br>SHA256: 005a7389bca4f2c931ad6dcee96fabbdfb38405cd32d2479911862f081b50611</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>57.56MiB (60.36MB) – 874,720 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7800805af5945b75ef4c27cf303e93ea<br>SHA1: 599e67027340a434a28774ef2533dc9a196bc7da<br>SHA256: 7cdfac4b588eb9328ccae8d26d9d890f3d5f26d695fbf7ec408690a3ccc24faa</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.915MiB (7.251MB) – 346,209 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e6d674990e0f107fbd088e17b77f819<br>SHA1: e21f5ede55e9a68287555b79c322fd01792544ff<br>SHA256: ee56d76f9c227d305e7f5b79e40e5d3a11d30d9b4b4a21b0a814bc5fc6ccab58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.87MiB (17.69MB) – 256,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf6418c75d48ec2ce4a2a1c5d27690ea<br>SHA1: 9b685f6a9fe8620ee6003242f3c5acf610337b72<br>SHA256: e1a598f6d63830a2bae69310a4cc6608adaede1395648f0431135c9239a1caec</pre></details></small> |
| | | Full Location | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.3MiB (220.5MB) – 3,682,011 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42145ba207725adfe20cd9225ad15164<br>SHA1: 1d40332c6092241cca96d8e93cd7fb5c58e051bd<br>SHA256: c60c91128d39be7572205c3f816d9173c65edc218778bf32f3d1094e958cfd2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>464.6MiB (487.1MB) – 4,514,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f22f776ceeb745f6db78a0eef703371<br>SHA1: 30ac2eb9a7fa4373473059683b5de9079a24fedb<br>SHA256: de1e8fbe3abd61a6d689615765352368449ce489b189853826fcfeeff7321137</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.151MiB (5.401MB) – 257,820 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8f9908959f108cbfadfc9e7ab6b5884<br>SHA1: 972f263b1d19a67871258f42188f94e931d59854<br>SHA256: 975f5d9342bd724b46443117938bdbe68a26f1a6a67fbe877c780fa1f2a80930</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.32MiB (23.40MB) – 339,151 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 899eeee26f538ee8debffc108e588d79<br>SHA1: 0d77580077bcc05fd3f417a87c32cb013c8833c7<br>SHA256: 113b63ab10291245788982a1804bdc42917c5ba1431bd06f83e8db90d898c105</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,996 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f1a80c418d402b73fffc10b5e33b367<br>SHA1: 477f8a255df756d19d1c4c62f148143d63c6cca2<br>SHA256: 1e61d957caf16f9e8b581bb50ee239a27b4df55d443d3189a6df269d1e4a412e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>286.6MiB (300.6MB) – 2,780,123 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e193b09ce3e796f7ff230a3153398e6e<br>SHA1: 9fb3a062296faffa1023004232fb6fc559be1308<br>SHA256: 65b454a0db4cc428574b15646da49862ae8240441885272744911821e2cca9e3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.88MiB (13.50MB) – 644,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb9fd5b3beff8ce5e7662819701da8b0<br>SHA1: a9386d5094b9d20400edd26038f6b0a1da9b4eb8<br>SHA256: a10db38e67c1f0aeb177b920dac0c06b37040c2099a28bff88735c7745455902</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.30MiB (45.40MB) – 658,000 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 308e1a0a016cf6caadedb50c330e486c<br>SHA1: 9f1e4979e20cfc576a5c2cf3eb106632aa346d8e<br>SHA256: cb81ae14f9f256367ba6366d56d493d81b79f6873955c04d40aef45419f681dd</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>177.0MiB (185.6MB) – 3,488,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3de630bd1c19e2acb03c5669829175d8<br>SHA1: 8fd539d2fdf4076d5f25a0903502f3b2e4aa15cf<br>SHA256: fa4a9edb0c06e0624a3d56e6afdf333b4b4bfa3ae9a03d90b504627c539ed866</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>188.2MiB (197.3MB) – 3,488,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff8c77234af54f6d076218c619f7d3f0<br>SHA1: 689892f0d853c253251ade324be159e3fd78b695<br>SHA256: 10fd2b57592549d53f95e812fae67e4f820192d2f0f85d0c7f033395c046d99a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>176.0MiB (184.6MB) – 3,488,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 072f1fc058a4efb32183ca1ece1c69e7<br>SHA1: b05bc031b1b7012fab33b74c2c0fc72a46ded5ef<br>SHA256: 1a73f2e5aaeb195ce82a58add717558132b4cd0540a11d7fe800f1ff3934c972</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>178.8MiB (187.5MB) – 3,488,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43aea42a3d6e1a3d84b5a63407a9fbc6<br>SHA1: a9acf4441fd26b2faf578f302260e58468d679c4<br>SHA256: 4c1b18edf7448fe1db7af5843a8bf47f23c12fe2b1a63ef6e7874ee2cc52ef80</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.3MiB (235.2MB) – 3,488,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01e8159d155d8203bc306feaf8022d0f<br>SHA1: 032bc87a249f89f1711f47dd9def960dac950a9c<br>SHA256: 5788476a6aa16af390b4f9dc29ac7defa5cf4003ca19950c6c7414ce31c6a811</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>175.7MiB (184.2MB) – 3,488,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cec3e0aee6c8c4243b8ab253484d8125<br>SHA1: ee74f2246c1c30f7be4d0bfe6296f229f785b277<br>SHA256: e31b4478f1e251fd3531c904be513dfb3298ed9b523a6561404bcf6fa7d88c88</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>218.0MiB (228.6MB) – 3,488,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65539848c1674e1f6c8cf5d66354c925<br>SHA1: 7548fa9879ccee6e591293d26ccda719109bca8b<br>SHA256: 776786830b12be03efb5817525feb1e6122e6d739928df6a3ce7f38e7225e48c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.0MiB (191.9MB) – 3,488,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d2b83ba8f91c46e03face4f26ad53d3<br>SHA1: a45e23c2cc9aad381fdade3aeaf435461899fa52<br>SHA256: 15e156af067c9f39d129559d38116272069a269ee3cc7f2953c8a3f7976b943d</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>179.6MiB (188.4MB) – 1,903,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47f0a8d5db78aa23779b580374213198<br>SHA1: cee007c5886a284e09df8241e3509897c8eba9c3<br>SHA256: abbac7f68694654c99a6ef6050c516789dfd3ce58fda9577e7af161340f2726f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>183.7MiB (192.6MB) – 1,903,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 13d7f38331c4ca471a73e76439501a52<br>SHA1: 57cee317fac74da300bbf45895f773f28b854192<br>SHA256: 44f233b7ebfb9c857a27eb1783899780d60c7b784125abe84d21e96113933c09</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>177.7MiB (186.3MB) – 1,903,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 813e03ee75b23d6029a3046c3ffa4fe7<br>SHA1: 14639ba1f24fb48a0f809527cde7ecccd98c0424<br>SHA256: 5cabc811d5c39102111fc7fc0470abe9bc4a45055ec92dad349a27cb5a0974c1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>178.0MiB (186.6MB) – 1,903,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5e726e95dcc0cfedd31b332e9b563f1<br>SHA1: 7a62f2f661c29703ca82085747e0277f9cd470aa<br>SHA256: d5c7f81d24beef27bd7937fcb2b61c16786a1f9ceffcef50f650cf3d561fbcdf</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>197.3MiB (206.9MB) – 1,903,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6c469debf48dab77349f01ed197636b<br>SHA1: 9d3435ec03fbf65f7cbaa098151a6b0279787451<br>SHA256: b4cfd09d82cfc25bb642f7ea13f3e9b10dbb73f5e1695939ee3f2e4de1305c8c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>177.4MiB (186.1MB) – 1,903,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b68f702765f77e6daaf1ff7e8dd93302<br>SHA1: 5d31220848707867902e8f3a1a49d2e3f2233d64<br>SHA256: 561c7dc1134a51accffb3fd4e1b26d9263f8586041e6fee51df9f3ccb61f93fd</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>198.0MiB (207.6MB) – 1,903,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eda18351f2da6ee3a504f435a822f8c1<br>SHA1: 6629bb96d7765ee42bd012640428cba237509bf5<br>SHA256: 8c52c69b55147b15ba7a095f04aa774e2b4fadce10ac6aa3fb6261f85565718a</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>181.6MiB (190.4MB) – 1,903,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a84147a228bf646ebc0364fbdcfbfc1e<br>SHA1: 13378b6b751f4071abd87c6fa4c76cccaadb3875<br>SHA256: 0dae18877a14cb719ceb15731e9a72ac28805c4912c5a0301ddd59a84e27b546</pre></details></small> |


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
