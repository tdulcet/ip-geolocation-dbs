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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-11-17<br>IPv6: 2024-11-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.864MiB (6.149MB) – 293,637 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95bed2f519e41afe090df3747ee8d8ea<br>SHA1: 1b3a85e871c0b61ed1bfceb7040d814b6117e707<br>SHA256: c286d5b92ee962f1abce67f3b5c79f53112452bb7d4e928ededf35c5c13950fe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.46MiB (12.02MB) – 174,182 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab3ec8ed0ab577a8d2fde64e273b38fc<br>SHA1: 7462d8201c86214ab1768b52e0af476cdabde34f<br>SHA256: 01495e06853a2cf6800ab95d77043ae982069523fc280a8e8da972a2fc9869c3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-11-17<br>IPv6: 2024-11-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.228MiB (8.628MB) – 412,055 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dabf05235d4dcba414ac6333e1d59b11<br>SHA1: 8c4fb775c5104f8bcd5b199f812dd346701f65d6<br>SHA256: 64b0217ca21a680333eb0f1831e08b1f60c890992021bf54b87b46f6f26e4e13</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.869MiB (7.202MB) – 104,493 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82efc4201d67901ea71fcff15768cbcc<br>SHA1: c2593da1dfec1c0088afbea35ab1ee53b76cf695<br>SHA256: 34ec4432c08c2502623991ae2f66345c35a837ac44d0f122ed87f96809dff20a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-11-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.90MiB (17.72MB) – 845,235 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92224696ced2bcbe469239a9d291db6e<br>SHA1: 4be4324d14b52af98d29f31ca71801a85c0ee324<br>SHA256: f39b77e8f997195de1db19d1451f11f4fd87755a9ae3f36911b507f984845c3b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>82.16MiB (86.15MB) – 1,248,620 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc38b92755765fc76cd6459eccf99f51<br>SHA1: 9be2cb5c314c4cb6acc62695dfcc44bf0dd13d35<br>SHA256: 11f01bd3012965747d4792a10cb2c35fe513b18109ddb4fccda9f1fad263684b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.056MiB (7.399MB) – 354,248 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d0746f47a1225271996460705211255<br>SHA1: a42a4bf19e2ebf577c82e10d3834e8df68696682<br>SHA256: 436aea2efe6e1523eea5e9ba484e5efba050d65a52ade285c3f9c0212c5ed301</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.43MiB (17.22MB) – 249,619 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efdc8aeb0b5fac8527fcc97613b42d4a<br>SHA1: 05d5c2e0b0a85115285dfae791b3139e2b9eab7f<br>SHA256: 45657f0c603e4d28c566dd5f9da450499802a059e8c1ff77082c945045a71fa7</pre></details></small> |
| | | Full Location | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.2MiB (199.4MB) – 3,323,413 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e766d2e8e0a2969d4ff92cf52388660e<br>SHA1: 38d95ed8fc01158d0f5ec9aa8f3bb385ef86d3d9<br>SHA256: 7656a9190b90023870afbde735c05ae68168d21190941a5da2be92e18c8b89a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>369.3MiB (387.2MB) – 3,583,553 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23856f8e31b066ac2b1f256c563a9300<br>SHA1: 4ffab13a7c3069f5a314ea0ee72c222a02103120<br>SHA256: 9d6307032c82257b206c839119decab677631aaf7e5d3138ed4b92f8cf07acc1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-11-17<br>IPv6: 2024-11-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.921MiB (5.160MB) – 246,296 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40e580b10d9fe17a204d4682e8caec62<br>SHA1: 86c3da422b58cf1b996348924dc8256bc7f8c0df<br>SHA256: 32168c3110bd3fb45b79eed0642def8db10a273ed5096e224c2de29a05e02fca</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.04MiB (19.97MB) – 289,357 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f83651873d1db0d8addc8985566a84fc<br>SHA1: acbfe44dbde35a4fdbd66b655d20885747b3b874<br>SHA256: d240a5da5dd52cc7a57780fad1a11415b8e2130d68731c1182f1798b90e567f5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-11-17<br>IPv6: 2024-11-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.6MiB (182.0MB) – 3,006,530 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3205f79a16c843aace3d3a8e3aec5334<br>SHA1: 8987d05a3901bd7ec7439251708d0c2228642999<br>SHA256: 807a107f4be6c9d0eaa439b6e63f93c3067bae3d0b264ed83a142d3318442718</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>215.9MiB (226.4MB) – 2,089,755 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e072b36b8644392e07bc9ec16c01aa89<br>SHA1: 4145eaccf7a8ff6d0571c6ac031eefdf75dee798<br>SHA256: 575d88a498458f0cac331d823e497dff499178b951353e2f6594814450a3a71b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-11-15<br>IPv6: 2024-11-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.01MiB (10.49MB) – 501,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd44fa336ffd5c6045840994a0fa3b9a<br>SHA1: fbb89e92df02f6e7201eb54d380d04a2bc92ad84<br>SHA256: 4ab833caeb6dd014faa75a9c694020eac2005bac2bfa8069059f0b100e6f48b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.22MiB (33.79MB) – 489,687 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fef3a69fd8d1ffdb620ba870fb194d5e<br>SHA1: 5f2df3baf6cba0baaeb64c93445e63d1e1afa8e8<br>SHA256: 39a49993d7f54c6d8e14eec3c44850f162f536ae56fabd2db7750dc7da8a56fc</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-11-15<br>IPv6: 2024-11-15 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>164.4MiB (172.3MB) – 3,246,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c72bff458e5ed8a14f55cd80527bd9f<br>SHA1: fc0cd4577ed5d9bcd431fd349e529302ce87420d<br>SHA256: a44a5e02fa3475b2d312a35c1659642c89495366eaca920bef50f53d5598c5d0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>174.9MiB (183.4MB) – 3,246,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b96798cff8592edc1f51d9b2cb095b2<br>SHA1: 754a42131e8a2bfa51312bd7c8afd1c9ef125363<br>SHA256: a6e202c288382238ac7b0164734fa1f179625c3cb31348bb241a89be4aba8296</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.3MiB (171.2MB) – 3,246,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6748a94dbb18f5ff9ff15b9698824631<br>SHA1: 5f022819c93689c8d22c153bde71ca0d58715cff<br>SHA256: 1555f92948ea82833c7ec1fcd09eabb16e56b2c18a8125e1ad01b62aecff85a3</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>165.7MiB (173.8MB) – 3,246,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2872cb82676f488bc615457e4c859a0e<br>SHA1: 6386b9bc74bf8f2c9e31aaf9b47c1e28fa2940dc<br>SHA256: d458ed8c7a895fe54c79ef66fbc62c831c0b025733feba879086921b24da14d4</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>208.5MiB (218.6MB) – 3,246,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a825a9dc048b2390c251a173133ed7ad<br>SHA1: 10ae04e821fcbffee3c8839e2ae47f64420148ca<br>SHA256: 46af823b50703d7473d46ca90ba180708aa7e429c9e8e55b4ec7d92d86d1fd1d</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>163.4MiB (171.3MB) – 3,246,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b6bc89c0e5182e7733919ffa7c122ed<br>SHA1: 5a54bdae17f57382ccb24049d14ac2a9e9e974ac<br>SHA256: 33c95934d92481ca357a9933406a338efa586a189daa5307ae22de617e74a004</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>202.6MiB (212.4MB) – 3,246,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d16c6f3e64afc4937274033c6193549<br>SHA1: 9956a8461ec9e26e35f8f507154ed71af03b9827<br>SHA256: 7ba3b60cf987a3b9aa678970bbf0e7360fc6f79a54504ba6719f94d03a469fed</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.4MiB (178.7MB) – 3,246,114 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d26ae94b9dc55bb7ab6bc79cbc6e7c8d<br>SHA1: 2b3e1ccff7404cfaf7a280c1bc31f7186a852cac<br>SHA256: f54ccbbe04b9d27e4eb46fd98ac33fecb32f95f45bc768e17bd579b89a17e184</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>157.4MiB (165.1MB) – 1,680,877 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36911fc8a73f22785eeceba51f9a02cc<br>SHA1: a78ac41d8b01c5014a1696005d44d42ef2e7a23f<br>SHA256: 45c527e88f74e22999454e7e51e9b0a924eed181ef5426a027bcf3799d10f053</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>160.8MiB (168.6MB) – 1,680,877 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ec22e86cc24d6f8f61432dd01da7a7e<br>SHA1: d9eba38e532d63a65ae3f4db804010754b8ef18a<br>SHA256: 0f705497e990c50fb2849692207bf40c03ed349ca8b43bd2f695a6bfd3332706</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.6MiB (163.2MB) – 1,680,877 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1efa148e7e31caeb83fe7516fe1547a8<br>SHA1: 50b777890d41240363cb5dee407f6bc5cf0eb0a5<br>SHA256: c2fe4bbb922a4ca8be703bb3fad295433a9f39f48a0fb2545917a5b7e430505b</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>155.9MiB (163.5MB) – 1,680,877 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 961a66550e1082467a5a6fd63e294472<br>SHA1: 25e96fb6e35c8a8f537917d3d3a9e921d62a3050<br>SHA256: 341feaa6e9bb7ee1a38ccaba7f8e5a726c5400b568dab6287c0da274a9b548d0</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>171.0MiB (179.3MB) – 1,680,877 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b8e4e0470f9bd73929bd310b4617924<br>SHA1: c70469c9ef9b2c620b88484ceaa7a3a6a6dcfa2f<br>SHA256: 432abb1dbd4fde31f9746bf66883517484227b216a05d1a468f4a2de8434c75f</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>155.5MiB (163.0MB) – 1,680,877 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78dc7036a1741c3692c45e99f52772aa<br>SHA1: 8463eea4dc8a98aa08c38bb841f3adbe8f7fb45b<br>SHA256: c5ce7edbfcecd75a7a54250faad85b5954fcc79475733f52eda7a0f1732a77bb</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>172.3MiB (180.7MB) – 1,680,877 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb7e4bd5c49c8b3a27f3db62463cd3ab<br>SHA1: a38e4bc32a11dcf6de6078c739e3bec9cc5491c8<br>SHA256: 582b5a89278d9d948c48253c36f92751714fedff967d7b444cf8afecf0025869</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>158.8MiB (166.5MB) – 1,680,877 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b926fc80828d787debc4216494ae72e<br>SHA1: 566bd7152b04d5e68418cfcdeb2c0e4bddea8179<br>SHA256: f06d753b8087214252edaa2592d08e5be15dc2797b3efedc062f6e3a75ca5337</pre></details></small> |


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
