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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-11-08<br>IPv6: 2024-11-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.857MiB (6.141MB) – 293,272 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f2a7313c88f6decb981ed5cfaad9f4c<br>SHA1: 2c3dd91d187a46162376012fd1813c163c4202b1<br>SHA256: f6cc71fa38b66a0c861b0fb709f0d7332519d2c8885239593dbbe7b222135a62</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.52MiB (12.08MB) – 175,013 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f20d12791c4811d178e7259eec5ca1ba<br>SHA1: 062a4497a107b57db8bb89046a6ae4d01b70a0d0<br>SHA256: f8a22cc639127457f6d54d5ee5bf8573004b623f3a1d204818c9a6ee35849483</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-11-08<br>IPv6: 2024-11-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.232MiB (8.632MB) – 412,246 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27c1ee9024ff9b71ae176725b6dd0e83<br>SHA1: 457341be6203d57295f0cc1ac2af2427f52b31a2<br>SHA256: eba2f07296cf98155f49e87d624dcd798653b5558a8d159048c1ac534f06ef89</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.867MiB (7.201MB) – 104,477 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f9f3394727d652865716c718ce149fb<br>SHA1: f5225c8524a02b56babfe4b2d73730f1b4553e92<br>SHA256: 3078e4003e56d3fb81ae6659fba2b19db06908bd864a53ac81708ed283741eb4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-11-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.80MiB (17.62MB) – 840,721 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b9f13694478817b7e4c424829421b3b<br>SHA1: 7f776b831a1be7dec91d192e39a13073e88f1f4f<br>SHA256: 1f01b005aa4b3d1d88dad907e08332323ae46f69e6f45169bec797bd1bb7aee1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>63.97MiB (67.08MB) – 972,151 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04b60adeb16883586cd578dbcb4e2773<br>SHA1: dec51502bf12f16f71d2b934ab5b1998980c379c<br>SHA256: 0c5fe55c07dafc5e19326aade1ff7d9bed21bf43144f3fc6440d20b593709f4c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.056MiB (7.399MB) – 354,248 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d0746f47a1225271996460705211255<br>SHA1: a42a4bf19e2ebf577c82e10d3834e8df68696682<br>SHA256: 436aea2efe6e1523eea5e9ba484e5efba050d65a52ade285c3f9c0212c5ed301</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.43MiB (17.22MB) – 249,619 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efdc8aeb0b5fac8527fcc97613b42d4a<br>SHA1: 05d5c2e0b0a85115285dfae791b3139e2b9eab7f<br>SHA256: 45657f0c603e4d28c566dd5f9da450499802a059e8c1ff77082c945045a71fa7</pre></details></small> |
| | | Full Location | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.2MiB (199.4MB) – 3,323,413 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e766d2e8e0a2969d4ff92cf52388660e<br>SHA1: 38d95ed8fc01158d0f5ec9aa8f3bb385ef86d3d9<br>SHA256: 7656a9190b90023870afbde735c05ae68168d21190941a5da2be92e18c8b89a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>369.3MiB (387.2MB) – 3,583,553 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23856f8e31b066ac2b1f256c563a9300<br>SHA1: 4ffab13a7c3069f5a314ea0ee72c222a02103120<br>SHA256: 9d6307032c82257b206c839119decab677631aaf7e5d3138ed4b92f8cf07acc1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-11-08<br>IPv6: 2024-11-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.921MiB (5.160MB) – 246,296 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40e580b10d9fe17a204d4682e8caec62<br>SHA1: 86c3da422b58cf1b996348924dc8256bc7f8c0df<br>SHA256: 32168c3110bd3fb45b79eed0642def8db10a273ed5096e224c2de29a05e02fca</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.04MiB (19.97MB) – 289,357 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f83651873d1db0d8addc8985566a84fc<br>SHA1: acbfe44dbde35a4fdbd66b655d20885747b3b874<br>SHA256: d240a5da5dd52cc7a57780fad1a11415b8e2130d68731c1182f1798b90e567f5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-11-08<br>IPv6: 2024-11-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.6MiB (182.0MB) – 3,006,530 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3205f79a16c843aace3d3a8e3aec5334<br>SHA1: 8987d05a3901bd7ec7439251708d0c2228642999<br>SHA256: 807a107f4be6c9d0eaa439b6e63f93c3067bae3d0b264ed83a142d3318442718</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>215.9MiB (226.4MB) – 2,089,755 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e072b36b8644392e07bc9ec16c01aa89<br>SHA1: 4145eaccf7a8ff6d0571c6ac031eefdf75dee798<br>SHA256: 575d88a498458f0cac331d823e497dff499178b951353e2f6594814450a3a71b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-11-05<br>IPv6: 2024-11-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.971MiB (10.46MB) – 499,491 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24655c5102309cfbff3af812856618a0<br>SHA1: e50af7a931248844e0fda9236f7cfb25bb24281b<br>SHA256: 169a23c1d9a99dba50af0828a803bf1531549387655e0d2bf339d0e0d6d97b2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.97MiB (33.53MB) – 485,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78056d1036f76a80a1e52e4c9ecd4002<br>SHA1: c836e035d2f5e190a9259b5c9dcc44736ec42341<br>SHA256: f2be2277ff608ba68bebf7affc001e4024c85d3804fef76645cfab9259bce85a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-11-05<br>IPv6: 2024-11-05 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>163.8MiB (171.7MB) – 3,234,334 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a8c23c14fb1a4837cdd090b00771daa<br>SHA1: 2804220142c2971edd16422b30693242320c1d09<br>SHA256: 8708c078079f27aebeb18b5bf614ce79b74b305ed7d29ab0915e869c70351374</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,234,334 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6525229d1c5b92290adb6c863bf34f8a<br>SHA1: 4699ef4cbd5fa997fecd252c78b8d5b0a3daafe0<br>SHA256: 5a0cabb9130fc4a22d9637b63321fd791270ebba5268f3aa7c1408aceab5b150</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>162.7MiB (170.6MB) – 3,234,334 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a68271f97a3de2c97707afc35f128a6<br>SHA1: d074189f3dc840f0fac523cb0c00cb0573f2e30c<br>SHA256: 36332b466a2c1f2febd94cce69f060b88b52af0f9f3e783e12aba46a40c682d4</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>165.1MiB (173.1MB) – 3,234,334 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e30ccc48845a6a05eb23d2e343857377<br>SHA1: 90a4fb117f42e1d7e27961448422816472b08d6d<br>SHA256: 0f3ffe1bb611552d322543fa558c39997373a674be90af48030d00e83c6d8cc3</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>207.7MiB (217.8MB) – 3,234,334 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1eaa7b03970eacd3b29cf21e36369915<br>SHA1: d7ed71975343fd9ac503e39a8445f942ccb92468<br>SHA256: 13d67edbc1736a8518a177663c29c7464d60f7b5ec10003786a350771d802ce3</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>162.8MiB (170.7MB) – 3,234,334 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a74f3febe96f9905e2a0fc3f99e60504<br>SHA1: 5c7c5a2da3a7ad4ff472ca2eb2117c06f5d80d1a<br>SHA256: bcbe8d78ea7d7ff19d3eb4ce1ee62ed64905375738c59603071fc95883796a4b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>201.8MiB (211.6MB) – 3,234,334 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67da0c5d8136ebf2aed294855437516a<br>SHA1: 72cb25e3633edc0d2511a8ea102e0704cae8cadb<br>SHA256: 7c2a5d5129f483b39e91059819cfe01c8069215ea5266a3f8120e8344013b69a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>169.8MiB (178.0MB) – 3,234,334 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5850e8f6d8c1f25e2a697e12ab715ad<br>SHA1: 8f62b7c9d8d1d6f95218a4e3d759d4b0f6a9dda4<br>SHA256: 4ffb96e95dfae5e7c8c7dd63102325ec42bf4f9534df45b0a9395f4640f1b760</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>152.9MiB (160.3MB) – 1,635,703 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccfa22e81dfa12d26a4793ff99d1c0d2<br>SHA1: b12b642676bec0297059f09dd9d03adf18029e85<br>SHA256: 734a018b20451cd94070204abd6a15e4437511fdc60f5acdb3405df9ad6dde8f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>156.0MiB (163.6MB) – 1,635,703 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b69334479634a32e4fc635f114d79d7<br>SHA1: 391505a8dbdf2651d0e8182b032e5bdbe9787c69<br>SHA256: 2872be5e043e2cb86c0e646d1f46c054fafe2619d9d0ed27c81847315a303d4e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>151.0MiB (158.4MB) – 1,635,703 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c1d3ba2ea7ea978ca4175bfcd08a963<br>SHA1: 4cf6fc600b48bcd93477d9e9e40f02bb6a601f17<br>SHA256: 74d2d7470d98d972168ad3eea120689ef2c63ae5c1e13ab4642c4bf1f758c0fc</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>151.3MiB (158.6MB) – 1,635,703 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96f782533822e0471e2fa607cd5d1078<br>SHA1: 329930675eb4c6e28766aeed3702232ab592ce55<br>SHA256: 17fa88bcdb0fa5c19b6b581e7471ee397c0ea04e67d323afda052c7efbb1ef1e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>165.6MiB (173.7MB) – 1,635,703 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 845487aa0bf4ec5ad358d8ef5c07f791<br>SHA1: e210e495560b8ee93e5244769aa50db86618f488<br>SHA256: 4070c6ca888d5e6d5241ab0f154b95f2f73cbe7da190bcb562108aa857a234d5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>150.9MiB (158.3MB) – 1,635,703 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5129ae7eecf313ce7f85a26b9209ff7<br>SHA1: 863026efa30123f9293b4670f6f896d245286d6f<br>SHA256: 495c1caea0d796409390cbcec39596f12947abe1f44d1c470f3b060e860254e8</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>167.1MiB (175.2MB) – 1,635,703 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67eedf22f5e162f29080bd30aa98172a<br>SHA1: 90e74b8439f04d243e90bea0657f9b426a37594b<br>SHA256: d3376dddb90a2f18af1e7700bb78f4f2d68be28570202b31b64f65e1568d527b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>154.2MiB (161.6MB) – 1,635,703 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b653be70991768decdaeaafb4e99c5a5<br>SHA1: 7ce1326d5c96c0ed98124f0923064234b773c0a3<br>SHA256: f45337faa572bbe4e61e94c89288d31b2d43d23bb3a245385a797b57bab617ce</pre></details></small> |


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
