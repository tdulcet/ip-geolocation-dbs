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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-10-09<br>IPv6: 2025-10-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.194MiB (6.495MB) – 310,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5d3ee613eeaece8c3d61e1c1c918ed3<br>SHA1: c05664b4008316f6625417dfb9af2edcb31c7af2<br>SHA256: b9931646e7336f0585402c5c2b8aec10346f46c404861898d82b863ca2e87b82</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.779MiB (7.108MB) – 103,014 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd990a9fbc57c8b415ff584fadab0a3a<br>SHA1: d4a35a9908f319f74f5b208c561bab5fa504af89<br>SHA256: 59060dc4ce83b7a1d688789abca2ba773fa906a08132933afd48d14d607737d4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-10-09<br>IPv6: 2025-10-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.685MiB (9.107MB) – 434,870 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ec82c4e2307f75a741529ba3a8d225b<br>SHA1: 5c47fe8cc810b1ae9d0b2fde2cba1f6ebacff666<br>SHA256: fb066a367e2d26cb9a09b2e94b94511262be89b91ca9f83e11b0ab2995c82845</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.369MiB (7.727MB) – 112,105 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f078a6370f88e06704c718d43cd49b2<br>SHA1: d09aea0c77478a15260100d62a260249cad291b0<br>SHA256: 8f668f4ca51f844f08b84108a72c0530d986d02a7c3776a0ab256b45d8e37a43</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-10-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.30MiB (12.90MB) – 615,881 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c878974cde310b3e6d7e84c6f290380<br>SHA1: 80cd777733a1c34fcc47ebef88ab407db7500679<br>SHA256: 7c9f10f06e41d9912de0d594e7456b338d0e84c9b803aa7f13d16f8337035891</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>71.32MiB (74.79MB) – 1,083,897 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8a273430bc221a38d9e4931c69b81e3<br>SHA1: ae38a5c75667a75dbceb9e78913c107feb7fb88f<br>SHA256: a4e2804a9fd8e3288ef7b1576de10af3997bdaf4033846b04f9c195db74256aa</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.915MiB (7.251MB) – 346,209 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e6d674990e0f107fbd088e17b77f819<br>SHA1: e21f5ede55e9a68287555b79c322fd01792544ff<br>SHA256: ee56d76f9c227d305e7f5b79e40e5d3a11d30d9b4b4a21b0a814bc5fc6ccab58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.87MiB (17.69MB) – 256,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf6418c75d48ec2ce4a2a1c5d27690ea<br>SHA1: 9b685f6a9fe8620ee6003242f3c5acf610337b72<br>SHA256: e1a598f6d63830a2bae69310a4cc6608adaede1395648f0431135c9239a1caec</pre></details></small> |
| | | Full Location | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.3MiB (220.5MB) – 3,682,011 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42145ba207725adfe20cd9225ad15164<br>SHA1: 1d40332c6092241cca96d8e93cd7fb5c58e051bd<br>SHA256: c60c91128d39be7572205c3f816d9173c65edc218778bf32f3d1094e958cfd2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>464.6MiB (487.1MB) – 4,514,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f22f776ceeb745f6db78a0eef703371<br>SHA1: 30ac2eb9a7fa4373473059683b5de9079a24fedb<br>SHA256: de1e8fbe3abd61a6d689615765352368449ce489b189853826fcfeeff7321137</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.161MiB (5.412MB) – 258,309 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f26d4302c7fd76db0d0260380f6bd166<br>SHA1: af4522cf5b0da7a4f55fdb43eafd9203505afe55<br>SHA256: ccd12d01d176de876028be848cfde48c9259fe6937a9d2b5860504143663fae5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.39MiB (23.48MB) – 340,241 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6eda0fd5aedd731b1e43a4c8d35f5168<br>SHA1: 6cc4cc30710f6cbe42343b9494b486362bce385e<br>SHA256: 7cebccd5d4724480dfa8ce7feb46df8346a377c9663e9c706a42f95c27d002e4</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.6MiB (178.9MB) – 2,958,155 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe165abca69867578e8e23a850e260e3<br>SHA1: 28aa8e4206a34c7c19baa2c8dad557e3e7e29980<br>SHA256: 395f8c3845977ec0aa9aeb6377d2342a1e06c37721d3b8e06ec2ffe85d3cc7e8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>294.2MiB (308.5MB) – 2,849,176 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84c795dd4c828d0cd8fd981934d68c7e<br>SHA1: 2745be7c734086c09f40f1d7190fb4ec6cb937f0<br>SHA256: 7db0021ec3c03e994dd396ac728595c5a9f0c6bc1180ba247056935d66e38a9b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-10-07<br>IPv6: 2025-10-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.81MiB (13.43MB) – 640,999 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e5cef1c2b8fac8d200df039951cdaca<br>SHA1: 2c89f2422c938ca5dfe8ea7d4f802f9d77bf7381<br>SHA256: 95442a5091541960717ccefc671d2fa1d06492494f0cadf0cbd6c2a53b7fb20f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.01MiB (45.09MB) – 653,551 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d36c9c6de66889e6fa0bd81c1cea44b0<br>SHA1: d213cef3d13fbbe39b87354c3fa920bf38a563b2<br>SHA256: 89f458c5121281cdd830d2724d8d76861a4588ca9c1a4ffd8ff077489efb198a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-10-07<br>IPv6: 2025-10-07 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,488,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d34e1a77dfab2f0c6c6abcb6cd82f04<br>SHA1: 559b4adde94dcaae650f0f09e7dddc2c9e569ca8<br>SHA256: ad8d7d21258d2758699ca0ffb1a4f52b7dd00425aee4881c104dbe344d435baa</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>188.3MiB (197.4MB) – 3,488,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5b0b3d620b0ea1aa240a7da38b9ac39<br>SHA1: 787b4bc0c04999f3cbca6efaf7a1bf189053ccc2<br>SHA256: 7e5d1e1c078c072cd61599b54dfce839e0a852038219d9217a05c8797ca1d995</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>176.1MiB (184.7MB) – 3,488,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db241aa99c0eeda89506da44bb86c44c<br>SHA1: d3d165859f3dc3f2cbb19f15e5ef18fbf8dd01ee<br>SHA256: 7ed1d16369cc99e732ebe214f6fccb88e69ec1acbc628bf9f549a4bc683ce5bc</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>178.9MiB (187.6MB) – 3,488,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc422091f0cc2a8e5bfdcb5589147e14<br>SHA1: fa368e6a0acfc039d3b1fb9436fe786bdb923881<br>SHA256: 82c3fc79203fd9c5abad8ba860b632b5ae5a52aaa036469f582ac4af72a0b4a4</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.4MiB (235.3MB) – 3,488,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7a460f70ab2d838f0111d5c8c92e5e7<br>SHA1: 9c46eb3ee141c5354e8389100fc3776b711eb07c<br>SHA256: 1d84690fbd31075e3fbc7144d76086b779852040ac14388bdfd6383d7d55193c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>175.8MiB (184.3MB) – 3,488,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dbc65b093f8a993dab7705730ce6cc8c<br>SHA1: b22fb4e126553539daad8e612e2022dd738533ef<br>SHA256: d0f872c0c0aef8c57c6cdbb6bb0d0ab426169d3cc2a0230a51c2db52203de810</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>218.1MiB (228.7MB) – 3,488,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25211d838e23eee3f107ca52cfbbbcae<br>SHA1: b69a81e73bfbcf346a0d848604612f10ebeab9a9<br>SHA256: c150f10e4ecce8a5fcd63352d62ff2a3c2cca100ed60d341f50900b1fdfb3a0d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.0MiB (191.9MB) – 3,488,787 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15e0ce83af5eb5e8e268b786122af34c<br>SHA1: 0193c96382696d02acb81637b6c022946ccc098d<br>SHA256: ff51c2bd922172653c1a95065af85e382aefea26fc155c44923fa652c564a975</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>179.2MiB (187.9MB) – 1,898,990 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 043e00cef703663be966014b5734023d<br>SHA1: 597819a50ae892d05c022499188af0ffd3e81e59<br>SHA256: 4857c027e02e7ff590f6e4ce415d8bff8ed9b4ebb7b6c13b3653c18325ef2fdb</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>183.3MiB (192.2MB) – 1,898,990 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8dac20b513e7f9c6c51f05655f34c400<br>SHA1: baf0bc86834670f43df06d92c5e863d280d8304d<br>SHA256: c31f068d9d3082fb419f12da0e7fbce3fdeefd5846c6b82b8dcf70233688f76b</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>177.3MiB (185.9MB) – 1,898,990 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aba8980613c5574e0cbea366e4fd97ab<br>SHA1: c1789ab1863e43a343d7044df47cfa7916f4f925<br>SHA256: f531ac77b2b61662ddba7cc13b30f63fa47708eeb16ff15ed9c91d3451bba7d7</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>177.6MiB (186.2MB) – 1,898,990 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d061659452437844b015a4c04cde7dc<br>SHA1: 742f7482ba5ab13eec311cea761c22271ef77c2b<br>SHA256: 3419eb0f63bf3fc4ceacc0eddd4cb983ce67a92752e7c5f9f384985447149706</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>196.8MiB (206.4MB) – 1,898,990 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 934e5ae17c61c137d9ca04badecda2d2<br>SHA1: 3ada824c02c48612d553347b36cee2416def5261<br>SHA256: 248942ea5735d3066dfedbb1f5921bd86cb379856c0f302dc05c82114690e8e0</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>177.0MiB (185.6MB) – 1,898,990 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 715683b28e2f1cbdd867f0b826e0704a<br>SHA1: 5fbd85fd72ad4d45ba20399bb1ba579b518c4a35<br>SHA256: 359484f0bb2000daf01512572aa432eb6b4e29a0cef51b9a21e2a4a24ea71365</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>197.6MiB (207.2MB) – 1,898,990 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c3b9835b3e8d0e354bd9ba4e81f84cf<br>SHA1: 16645af613f736985307d8beffcd2aefbe4bd7d0<br>SHA256: 67157bb0ba5aebc13d9f5efde534ac7ee008e0352f33d92aaaa4a01cdb8b7d0b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>181.2MiB (190.0MB) – 1,898,990 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 710bd12b99b0fcbc124dc85678062273<br>SHA1: db2d75e67460535cb097e380091f37634a00705b<br>SHA256: c491c076cc637ca7744f50d3243693cac3255457b9914ea4e4971ee9ff7e0d4a</pre></details></small> |


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
