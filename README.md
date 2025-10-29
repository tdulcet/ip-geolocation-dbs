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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-10-29<br>IPv6: 2025-10-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.312MiB (5.570MB) – 266,130 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb1f1b5a5add4b4b2fb89ad61b1c1754<br>SHA1: dc4f19e08c21e158cb6e2d8417f33d9d94388954<br>SHA256: 6cdef311700da8612004cc94dfe2dfa3db592fa85b7f30c7ac28ac61b2c36717</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.814MiB (7.145MB) – 103,553 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8049d6f462b582ad4a14497210b9ca1c<br>SHA1: 19b98d4c6fcceff060789e51d0fd42c1d0cbc075<br>SHA256: f328bb62bb54398de886eee4ca7f36d98440eb990c784dd0c37d24754e04ffa5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-10-29<br>IPv6: 2025-10-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.737MiB (9.161MB) – 437,462 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a980a3e12c283b093dbd4eb71f595d18<br>SHA1: 809f76cfc1286cc12b1d1338024302e70b05c25b<br>SHA256: 268f8b84676d66a0888bf09f1c46c28f03c1fd329f193496b36777b707d09830</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.446MiB (7.808MB) – 113,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a67b51018e1ea58a69e057be2cdf9dc<br>SHA1: a3d834d29dc2de9f75d41de40a27c30b78b8dd92<br>SHA256: 484fa91d1ae870fd049334b8b044eb57fb0f9ec31f6e09d428344437e8457acf</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-10-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.22MiB (12.81MB) – 611,818 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d01c93a6d584521da4d5581fa1445a13<br>SHA1: 22b4d8499d6a72e6c7788fa7b4fb408d9f033e12<br>SHA256: 607ba607e01015b2b4bec5237c88601e982fc92557aa8b9ba8e8cf98d62af6cc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>71.41MiB (74.88MB) – 1,085,228 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90d992f369edc6fbc899731b2fc80e9f<br>SHA1: 159c251e38961ca84cb09086c2103c329a2e1613<br>SHA256: da92cb0563b36e9a539b51b4b0ce748904054c2fbb5426907342a7fca85d9e09</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.915MiB (7.251MB) – 346,209 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e6d674990e0f107fbd088e17b77f819<br>SHA1: e21f5ede55e9a68287555b79c322fd01792544ff<br>SHA256: ee56d76f9c227d305e7f5b79e40e5d3a11d30d9b4b4a21b0a814bc5fc6ccab58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.87MiB (17.69MB) – 256,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf6418c75d48ec2ce4a2a1c5d27690ea<br>SHA1: 9b685f6a9fe8620ee6003242f3c5acf610337b72<br>SHA256: e1a598f6d63830a2bae69310a4cc6608adaede1395648f0431135c9239a1caec</pre></details></small> |
| | | Full Location | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.3MiB (220.5MB) – 3,682,011 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42145ba207725adfe20cd9225ad15164<br>SHA1: 1d40332c6092241cca96d8e93cd7fb5c58e051bd<br>SHA256: c60c91128d39be7572205c3f816d9173c65edc218778bf32f3d1094e958cfd2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>464.6MiB (487.1MB) – 4,514,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f22f776ceeb745f6db78a0eef703371<br>SHA1: 30ac2eb9a7fa4373473059683b5de9079a24fedb<br>SHA256: de1e8fbe3abd61a6d689615765352368449ce489b189853826fcfeeff7321137</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.151MiB (5.401MB) – 257,820 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8f9908959f108cbfadfc9e7ab6b5884<br>SHA1: 972f263b1d19a67871258f42188f94e931d59854<br>SHA256: 975f5d9342bd724b46443117938bdbe68a26f1a6a67fbe877c780fa1f2a80930</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.32MiB (23.40MB) – 339,151 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 899eeee26f538ee8debffc108e588d79<br>SHA1: 0d77580077bcc05fd3f417a87c32cb013c8833c7<br>SHA256: 113b63ab10291245788982a1804bdc42917c5ba1431bd06f83e8db90d898c105</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,996 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f1a80c418d402b73fffc10b5e33b367<br>SHA1: 477f8a255df756d19d1c4c62f148143d63c6cca2<br>SHA256: 1e61d957caf16f9e8b581bb50ee239a27b4df55d443d3189a6df269d1e4a412e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>286.6MiB (300.6MB) – 2,780,123 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e193b09ce3e796f7ff230a3153398e6e<br>SHA1: 9fb3a062296faffa1023004232fb6fc559be1308<br>SHA256: 65b454a0db4cc428574b15646da49862ae8240441885272744911821e2cca9e3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-10-28<br>IPv6: 2025-10-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.95MiB (13.58MB) – 648,036 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d37b69b9dbaa77f06d294dfac7c7b8ec<br>SHA1: f92a966bfeb7fdb28df646d1d87e608e676b2d2f<br>SHA256: 907756e88a99b2c00bf6414d5cd46c4ba8b7d64a5241bd290f7fb9ce02888b15</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.30MiB (45.40MB) – 658,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c2ab2402702e0edabef074515fb3e6f<br>SHA1: 695c9707e6db028b096d09763363852d11e22751<br>SHA256: 3fc3c04f8210207354cf9098b65c0a2417b8f0e479c5e85b320a3c8415ca8e6b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-10-28<br>IPv6: 2025-10-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.2MiB (187.9MB) – 3,527,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91189ced2fbe0eb4f963baa15b4fd6e7<br>SHA1: 6dbdf067adb7d8b886f6246f86d732fe050cb30d<br>SHA256: ebef8900e473bd97c28c4c266c4048a1d318433c327041fe022b03985bbfff16</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.5MiB (199.8MB) – 3,527,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1beca7ed90c55e6c460ce6d0b0f8bb5<br>SHA1: 3def74cadddc55a3e894d53bf91b9bb3640f40c9<br>SHA256: 39941556dd0a86f3c3de2464fd192c309ab98f26c5b4868cf1b9cababc1a7dcc</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.2MiB (186.9MB) – 3,527,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8453ce3fa904fdea86c97ef19dceb8ee<br>SHA1: 533283d19ac8e862a4ce2b8a0519e2f928dba49c<br>SHA256: d859b818c92ccda0b01a097afee028e45d2b1942e1581aa0077ef1d9d133a7d0</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.1MiB (189.9MB) – 3,527,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c95173b45c3095c978e21206264d6b7d<br>SHA1: 5bd46b610915b2c9ad61aaa89465c7eafeca4d5c<br>SHA256: 7c17e3dbe8f2beacc6ae3458257e30a9453d245487f08036ced20cd5183893a5</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>226.8MiB (237.9MB) – 3,527,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08ac7570ad5e92160ae2e8631464ebd5<br>SHA1: c2b6107f5094acf0bd7cf2124cf25c881a3e8727<br>SHA256: 1f7413c637b70f8c56bfdb532f8ae338d039a01930faff34fce9810c25a0327f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.8MiB (186.5MB) – 3,527,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3088e7e8935d6155eb3e24d4fe12eee9<br>SHA1: d125132d8c3b6b6c454983a0cb304327ec9b3c42<br>SHA256: eb4aae48689292dba7df59d98d0541ebe520e5b2596b49c4f34171019c861bb4</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.5MiB (231.3MB) – 3,527,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1593c27a2ed0a6508d4baead5ae5eb13<br>SHA1: 2f83ccb720fbf180f9d253a8a350b3e2bce81f65<br>SHA256: 502fc77abfcc853b55023c1b159c12851953d92a970fffabdc4672b8dc3e3178</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.1MiB (194.1MB) – 3,527,511 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ea3d5db2c64d92a8cbff40dcca9b01<br>SHA1: 0199aad44906b1ba5619351e28d248692d8951ac<br>SHA256: ae937ad8dfa82f3696548532c8701dabd6c56e6f2fd05b09a04d917c42f6bfa3</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>184.9MiB (193.9MB) – 1,950,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d01eb5be3da90fa2342e561c178ce574<br>SHA1: b604a81bf5974082f5552a5b92aa807c2524a878<br>SHA256: f917976db50ae06dbca2ba4bbc0afa6d908dd4d5edeb706cee265eaf25b842c6</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>189.3MiB (198.4MB) – 1,950,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f20499b06302df6a092a9483ad25d1e<br>SHA1: 7f2b0c3d3d8c424d8bad17ccf34c61c8502d9959<br>SHA256: bf85175cb8d73427afae0e13b8078e3349327200e840a8d51070dcf9682a8ee6</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>182.7MiB (191.5MB) – 1,950,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1fcc2eb66cf7e5b02f6d0168090e1851<br>SHA1: 7e8efe4301961c37b1fc909084ea6ac45c7aad86<br>SHA256: b2de1a683849bed4ca2adba8f9a399b9b064d9c9fd4c7f1c0e5ec1f9a7358325</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>183.4MiB (192.4MB) – 1,950,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d35507372bfa9b4f62e2fea41303719a<br>SHA1: ba2344da02c2823d0277058a858fea7ff92f9247<br>SHA256: 9ed4d0afc454a515eacf51779b6637c4224d02ef1826178c8934cfc2f2f35413</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>203.0MiB (212.9MB) – 1,950,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aaf95efc7766c2ad8a1509d87fd57947<br>SHA1: 6b437af8243cee819cae5afd5942f224b6ab01a1<br>SHA256: ce6f404840eab7451d0591ce479c59934087106443bc8a07d7ba796bd548bb93</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>182.3MiB (191.2MB) – 1,950,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3aefb37f4a9df07ebe4f2885c07191e4<br>SHA1: 5f2685358846fd7ad45f1366f6dbd024181bb9a6<br>SHA256: c8b5c92a98fbda2e7728bf36f10b46e5b2a155eb7226b1ff91eb10e9fd8f80b8</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>203.0MiB (212.9MB) – 1,950,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c30c8079b2ee46e2cfd43272d73bef90<br>SHA1: e0cc42151b2fc9f11ab64417c75af8448f60fe8a<br>SHA256: c877d1bb3d8b31507b434b34bf9841cd4603a1a26ecb7366f622cca75ba1f827</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>185.9MiB (194.9MB) – 1,950,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1be98d39e2cba530ab96dc4703ece3c5<br>SHA1: 627fd9925a4b8fced4098bf278e2344704b33e1f<br>SHA256: 742e4f07e1215c58a3d16f0fbdce5415ea2ccbe62122915f0616de62e8c5b0ed</pre></details></small> |


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
