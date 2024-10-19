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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-10-19<br>IPv6: 2024-10-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.836MiB (6.120MB) – 292,237 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acff82cf5e3aab671a4990824dcb55c7<br>SHA1: f25b0fadd38d5b65e8fe0581395a072c6709043b<br>SHA256: ceb1e5a8cc05c6af1ae035d5dc7055de49c93c64fcf6a5cf3dbac3ca94580ae3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.39MiB (11.94MB) – 173,067 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c51ca870012abbd7bf79ab0b1708c4<br>SHA1: 850979641b7246dc91186189ac8200af5f9befc0<br>SHA256: cbbd9087565abdffb880458bae766a4c8f3c7d78913b0bf63374c554895ed7bd</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-10-19<br>IPv6: 2024-10-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.218MiB (8.617MB) – 411,531 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b7eb8e38de2f753b7fc258904ca097f<br>SHA1: 08e4c1656941b2e6df16421901907ff03815634e<br>SHA256: 74145fc6e5dd98f02b45169efa9bcdd534b9fa9fd13741b478174a93328b6253</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.773MiB (7.102MB) – 103,038 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8e202ed388635ba71e6b70f729b7f65<br>SHA1: 0efaf7c033b86ada1047ff1b8d30d334b8c76252<br>SHA256: 974bd91507f5ff4f24c2ccab2a4ea8568e62ddc247f47525effd3707aadcb291</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-10-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.92MiB (17.74MB) – 846,503 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b6150605dc82591cb3ce64d8f47599e<br>SHA1: cca731070bcf1b19a253a3110dde1e1e40964312<br>SHA256: 03a07b2b0dd838566fb72a348675370a7ee86f82729aa54c8c949b202f38531f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>65.00MiB (68.15MB) – 987,747 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3c738aa515342fe71f4abd127ea68d2<br>SHA1: 7e6a9b10088d0c59fdf9814bfe9fe3af139be598<br>SHA256: 7137ba2929621a89445a410d706b723c680c633f6e9b3b22e3739ac870776e8c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.939MiB (7.276MB) – 348,549 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1934c9e84da4a70171fa8a58df792d1<br>SHA1: a9efc628d84ddb0c5ec270a44c413d6e2e413eac<br>SHA256: 8974ef5ef8832adde54bf8eff5b734fbc419e040b6a1ba06eee6302c327937de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.54MiB (17.35MB) – 251,406 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccee8212e47dad6f6d37a7875599a267<br>SHA1: f12a6f633e3f93b21d90f94868a5dce0099a8f68<br>SHA256: fe5508fad3836313166aa43d498d12d6277cae16fef7835d5e92fdcd53bb2de4</pre></details></small> |
| | | Full Location | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.4MiB (197.5MB) – 3,289,697 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a0426270d27872fad498a291900b10d<br>SHA1: 4f4a7ccb4910df8d359d2ad76a1bd80c4be37d61<br>SHA256: 6869bc8bd2854724fd6be12e1a0efa4bf028d598fe1d116783216884c78d9f3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>362.7MiB (380.3MB) – 3,515,904 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b742d904c555f3e530341708e40522<br>SHA1: e367baa432e03a59b81c286e5f9bfaeeb0617eec<br>SHA256: f946dbe0156a23fd65f4c67f8c95dfc19e8984bc7f84d8323fc5c478da017055</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-10-19<br>IPv6: 2024-10-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-10-19<br>IPv6: 2024-10-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-10-18<br>IPv6: 2024-10-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.838MiB (10.32MB) – 492,835 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b02be1fa0071032470acb8ce6859322<br>SHA1: 5a681631b3619da9f2a43560dece2e6d6d5b4b3e<br>SHA256: e02232fa781f6b2f8ef0a7a956920805b09ca6f3c89ba8c9746326622d6d113a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.25MiB (32.77MB) – 474,872 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 785ad33d9ee6634fb54d55578780df2c<br>SHA1: 28364b64bda44ef3fbfe2e25fc82b4e91a071a71<br>SHA256: 75df17a63953fdd89253ccff948d4e37192ab00a66ff46df1dfe5d910b62421b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-10-18<br>IPv6: 2024-10-18 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.3MiB (180.6MB) – 3,398,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8b970e307aab0e280b6e0e7c25f57b5<br>SHA1: ffbb681e7cd1e882db8c37497ad46e4d283a3aa4<br>SHA256: da8c222d4b65dc27edfac62f9aa1747731cd592a0f1026f9c444453c9a64424d</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.1MiB (193.0MB) – 3,398,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2d25c94b7fadb215b8bdf27cb80014c<br>SHA1: 22c6a39383f96bf0cca895ef951fb1415cde1a7e<br>SHA256: c04876bf08ca096d510bf2f5243af3d6fa02c808e222925a4977b34fdd651e34</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>171.2MiB (179.5MB) – 3,398,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba6bef06e1e1fc392274b32f5af9f4bb<br>SHA1: 2ec044f82e39b56802cd540794783f807104a5a6<br>SHA256: 3a0e018f7ee9cd1f2418560255c9d60cb62226c842d12efbd787a3f51382ba7b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.9MiB (182.4MB) – 3,398,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e94fdc8de2134213a5474a1891b7f53a<br>SHA1: b6a03339974fd6eeb047b0033481632838305eaa<br>SHA256: 312d04a5c813a8baf3cba1648456ba44d9494506382f979b0abe6b58c87b8cf2</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.6MiB (229.2MB) – 3,398,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48a575d08f0be8140c5290db4eb687c0<br>SHA1: d034db2a2d79cdac2936dbca5258a6ad225ccaeb<br>SHA256: 28da3ae231ce8716b6cfeea425fe93b1df27b06c4146c2baf8176d3333e0fcca</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.1MiB (179.4MB) – 3,398,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f6eec148ad90fcd8b716ceb76210e9c<br>SHA1: 32a54442b80dd397450504d5e275694e0ccab4df<br>SHA256: 9059a7dbe69c7b94d08288aaa741c43f1e243cceeeb86e556f9c9daed30dd3f0</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>212.3MiB (222.6MB) – 3,398,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8759c24277e0d4c18910607ab69f5395<br>SHA1: 0e8124e33bab6c0f2af4f02f2905aeb58a9d5d82<br>SHA256: 266c5140c0ee97363c999bf51539149975dcd9c5e0ca414a366dc8434eccb31c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.4MiB (187.1MB) – 3,398,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da8225336e1e5b07aa397b807aff78d5<br>SHA1: 8d38628d4029ca1b2bdbcf8e807e474a4bcefcc2<br>SHA256: 89091e5ca89959277c8e7243c7e07c7e059fd42083b4fb1c2e315d07f634e652</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>158.4MiB (166.1MB) – 1,667,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4975ff9a188ff7ea8600dcb854b50ff<br>SHA1: 6ad2ce41a13381505e60411d92f63f9611875c9a<br>SHA256: bedbf432635113b3a927173c1b7536bafbde1050b111a1da3c261b83da2acdf6</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,667,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c496cfc6a7c73649f24ff748021927a3<br>SHA1: 694db091ddc13e6fe87daa5e74bbabe60806616f<br>SHA256: 31f5f240fbbdd70117e0c1e64ed4d2e277098e03db60885b02b4bf4754a08f15</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.1MiB (162.6MB) – 1,667,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 415f86338661c9bd4fc1815cf2edfeea<br>SHA1: 92e9e9b1ea58231cf0432e14fa73dc32a6cdd178<br>SHA256: 2d463fb4f7a84f7ed8263f9eb07cca7a22382f10cd180e583582cac8f8f67760</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>155.2MiB (162.8MB) – 1,667,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb241c2ccab9e0c470794652d30cd517<br>SHA1: f56ee00c3a64b9aba39c3910b8af8b7971df6b76<br>SHA256: 7e3e6b4e27060407fd7909737b5bf22086e54ef1ab1ac9d5be7f053b8670a490</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>171.2MiB (179.5MB) – 1,667,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1153c45675cb2c0d78a5e2829497d5de<br>SHA1: fd3d788efc5c2b2f84e0f3bb69d46dec2ca83af1<br>SHA256: 6c096c288e8b29c204d0f6201c7d186a9dc01791cc0c17c1338b484571fe7e30</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>155.1MiB (162.6MB) – 1,667,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8a96226e5c8c8caa1c066c338ea3260<br>SHA1: b81e3be90182ca52ed640fdb084608256623182c<br>SHA256: 29f3736e0a18d0b0f2a35f1d72623d87e1216e588fcbe5f68de578ceaf20cc94</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>174.4MiB (182.9MB) – 1,667,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f04d4a066ae52b422e1d51ba1da08083<br>SHA1: 76e3082b2fa5180ff613e2301f74ba12d90ae935<br>SHA256: c8817aee117ea5beb62084db025167dec361f907dfeb539ba5d004d1f50bf87a</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>159.2MiB (166.9MB) – 1,667,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9627e19c580ed367556bb0c4f12aaaf0<br>SHA1: c5397f268f196d38d48f20708b188d69200134eb<br>SHA256: 87309bb45eca3a2673741a567c57f19355083285a4730fada4e7f2572dcdac94</pre></details></small> |


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
