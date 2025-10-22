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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-10-22<br>IPv6: 2025-10-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.303MiB (5.560MB) – 265,637 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d5bfe7ede84d93181cb07339a987a3d<br>SHA1: b9ce59ef4aaa83b79139d21cf8b45cf4cfdb51aa<br>SHA256: e1c68bf0f973458e2a041d16beed1bd70ab3e2d8831dbcfc27c46f04fa4302f8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.806MiB (7.137MB) – 103,433 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5914bde62cdac1ed7918d58c8ad682ae<br>SHA1: c2962f09204b91b8b596c153a2607339d96d7ba9<br>SHA256: d27324c2d7465642eea8934eef52f43c79c2929dcbd8cca572f00c17658e5fbb</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-10-22<br>IPv6: 2025-10-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.716MiB (9.139MB) – 436,405 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd1359259947df514801c89654397567<br>SHA1: dfa9c3ef936fcc106d86233ef8eb7e766f49172b<br>SHA256: f2761bec601f96035d6c24236dccfa979175c731e6ff75dff6e3e159457d3ea9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.415MiB (7.775MB) – 112,801 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecd5de1127831747932a78f58071acb6<br>SHA1: 15c79cda59d800d9a55be48e042ecca472e71b97<br>SHA256: 9cc99e9b59eafb271cf04cc6d1ad361466df63b290c17b571320447a481ca5f0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-10-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.28MiB (12.87MB) – 614,561 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7567f20d29559511b661b3624a1418a<br>SHA1: dc5f3c0b966957cf15a64a3415a7131b1331db3c<br>SHA256: 52fd25b2ea60bb6155d24c573dcc015e6ec81bddbdcd352befa91715d0cc1d1f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>54.96MiB (57.63MB) – 835,218 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 402c89ee4db12367bf7314fa7b26d6b5<br>SHA1: 80f5efc654ae2d2f9f9e775feec45330c55dd356<br>SHA256: c5567e3f4a11c92582bd387bce17ed71f4f097c47a53da21e1cfd8516410886d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.915MiB (7.251MB) – 346,209 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e6d674990e0f107fbd088e17b77f819<br>SHA1: e21f5ede55e9a68287555b79c322fd01792544ff<br>SHA256: ee56d76f9c227d305e7f5b79e40e5d3a11d30d9b4b4a21b0a814bc5fc6ccab58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.87MiB (17.69MB) – 256,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf6418c75d48ec2ce4a2a1c5d27690ea<br>SHA1: 9b685f6a9fe8620ee6003242f3c5acf610337b72<br>SHA256: e1a598f6d63830a2bae69310a4cc6608adaede1395648f0431135c9239a1caec</pre></details></small> |
| | | Full Location | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.3MiB (220.5MB) – 3,682,011 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42145ba207725adfe20cd9225ad15164<br>SHA1: 1d40332c6092241cca96d8e93cd7fb5c58e051bd<br>SHA256: c60c91128d39be7572205c3f816d9173c65edc218778bf32f3d1094e958cfd2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>464.6MiB (487.1MB) – 4,514,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f22f776ceeb745f6db78a0eef703371<br>SHA1: 30ac2eb9a7fa4373473059683b5de9079a24fedb<br>SHA256: de1e8fbe3abd61a6d689615765352368449ce489b189853826fcfeeff7321137</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.151MiB (5.401MB) – 257,820 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8f9908959f108cbfadfc9e7ab6b5884<br>SHA1: 972f263b1d19a67871258f42188f94e931d59854<br>SHA256: 975f5d9342bd724b46443117938bdbe68a26f1a6a67fbe877c780fa1f2a80930</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.32MiB (23.40MB) – 339,151 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 899eeee26f538ee8debffc108e588d79<br>SHA1: 0d77580077bcc05fd3f417a87c32cb013c8833c7<br>SHA256: 113b63ab10291245788982a1804bdc42917c5ba1431bd06f83e8db90d898c105</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,996 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f1a80c418d402b73fffc10b5e33b367<br>SHA1: 477f8a255df756d19d1c4c62f148143d63c6cca2<br>SHA256: 1e61d957caf16f9e8b581bb50ee239a27b4df55d443d3189a6df269d1e4a412e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>286.6MiB (300.6MB) – 2,780,123 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e193b09ce3e796f7ff230a3153398e6e<br>SHA1: 9fb3a062296faffa1023004232fb6fc559be1308<br>SHA256: 65b454a0db4cc428574b15646da49862ae8240441885272744911821e2cca9e3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-10-21<br>IPv6: 2025-10-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.92MiB (13.55MB) – 646,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbd9444e99c33bfb540fc632537b4030<br>SHA1: 094dd951135045e5568884b93c21bb286c3be7d3<br>SHA256: 39f5872c274af0abf26c89954b64428d19a55fadeb4fcdc9601491e548b98fd1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.37MiB (45.48MB) – 659,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b76e85d19cbe3b9f0404c7bbb2d85c6<br>SHA1: 9d1fda4b3e5ec32051cbbd13831fdb80d565af0e<br>SHA256: 676fa3d5679cbfa546df0513499d22884e6abf5bfd6b2ec37423003261dc7eba</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-10-21<br>IPv6: 2025-10-21 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.0MiB (186.6MB) – 3,505,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7723b231db77a828b5340d94544a928<br>SHA1: f01690f0a53cfcebec5e509846fa5e7d9e275304<br>SHA256: 614d63c12c66794029f2ee69ab5ffa323ce8601b7f51d4ff69817748fcf63e93</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.2MiB (198.4MB) – 3,505,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90f3769f694e9634ac1d3fb43e24df15<br>SHA1: bcbf9e5d9e7a4d5f811fa7a0b92b346276a0e837<br>SHA256: 1fffe79d350f6a321a85f69592ac2119b451efc81dd924e630e5ee7a0295b86f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.0MiB (185.6MB) – 3,505,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f4b970e41eb67be3a072d8cc778bdc8<br>SHA1: 76d5dba7127bb5647cfd81dc7c32df077ec6e95e<br>SHA256: 45ab08e9d8fe8d8fca323c8bb81074699def152899785f77ab27a1d81fe86ba5</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>179.8MiB (188.6MB) – 3,505,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4c6e4198be52538481dbfbf50dd09c8<br>SHA1: f63177864008cef360b5b83499e51ec79124fea4<br>SHA256: f050d3deba8fdf3821fbb77ba60f47c3fc38f6770c65160836994e66951cbdcc</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.5MiB (236.5MB) – 3,505,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59bc3216ad631ac048b2efca52bacbe6<br>SHA1: 01d8a7dbf9dbee8f05c55ce56b8d7607c6e0ebd6<br>SHA256: 2fd5943297fc0ea773c4cf87215b8e67a58010d410f51837b7a24478794b78b1</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.6MiB (185.2MB) – 3,505,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba7df19b625efc6df5caf3c6a01ed0f8<br>SHA1: 5e102e9d7de1d56d1e87d6e28a3ea5054b54e597<br>SHA256: 05b181237dcae26cfc900c008d99800b903fa7fabc4f2fbc7b1dc37a90cd0c5d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.1MiB (229.8MB) – 3,505,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a0f59c3c224e070eb7fbf61d263ed34<br>SHA1: 7e6865f67a609dec5d707d905f90fee21b7a9ce8<br>SHA256: 26ddf3c5d203d2a443b0e7660e33e7f532979a44a989cd002bf0522ae73f10a8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.8MiB (192.7MB) – 3,505,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 932c6e5b21824699e525abcbd29ef1d9<br>SHA1: d8fdfee527362ab3adeb322fd88f60fcc3d4122f<br>SHA256: d7e1c47dd7052cd199830f2efa0a794183072ff3e39c2e71b04ef2ff9632bf25</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>186.1MiB (195.2MB) – 1,961,342 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ac462a1285eb95d81bd463813bb0635<br>SHA1: 0c5ee18a4ebcb500fc44a32c526827990f2d2619<br>SHA256: 2ce8abb07ae6e9d539a1bd4ce80591385e52c15a69a84e71993b6f6baf840d0b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>190.5MiB (199.8MB) – 1,961,342 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 697303e595a2b3e331d4d021d7698532<br>SHA1: 839ed2caf6e5f9166aa497d4af9130bc02e2f9d0<br>SHA256: c13c1001521b9ff92719c06e1794a9144aa461f86dacfb3598c43916034e1350</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>183.9MiB (192.8MB) – 1,961,342 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1ab6e7ebb01a99de75a14258459abf6<br>SHA1: 9357d69bb8e6cdb0341bcef311680a8257fac6fd<br>SHA256: 9708e19b7b2cfe4e32ec0db5e728faf6ecd08ea5f4aee3d71c8d4be3eafc3ffa</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>184.6MiB (193.6MB) – 1,961,342 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97508ca93cd152dcda011e22863b8c26<br>SHA1: 38ea8969f12868b06918f69f7baca51b06cf4812<br>SHA256: 4281d6ef5f3ca8835878f1c04589d85246cff8bf4416fbbae14f37d7ad5c471f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>204.4MiB (214.4MB) – 1,961,342 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8cb2ee04fd6625687f9bdd4e03a835e5<br>SHA1: 811bf5275c872a6a415888d4f114a731169471fa<br>SHA256: cdc176c368ea77f54c4d89c94943bced39fb4c44cefdb48ff52a18cfe0b140bd</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>183.4MiB (192.4MB) – 1,961,342 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 985ccd82143a5b7411038159f0b1c426<br>SHA1: 1729ee0f72045aa7ff3f0b7db967d9252fcdfec8<br>SHA256: 4dfe8b53f15e51c315bfbaacd2004fc17652ada712797e19aeef6dd9b9346f93</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>204.4MiB (214.3MB) – 1,961,342 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66538e3f476eb6dc3bcbfb027d6370b1<br>SHA1: 866934cc34f50634ca03b56bcb6020d2ea7e352e<br>SHA256: f10181f16c6d1cb37f74977b7baf037278c24e0850847d89a6a48ba2c660cc4a</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>187.0MiB (196.1MB) – 1,961,342 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 625585fb899df4490af9cb88f45dcad6<br>SHA1: 407ab77f56f06e215035be8a1b53b4c835dcbb98<br>SHA256: 96072d314c9061aa2162d35d12379c424596992f7e627a1e4529d9624a565aa4</pre></details></small> |


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
