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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-03-26<br>IPv6: 2024-03-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.817MiB (5.051MB) – 241,125 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a2b8e37d54a52d227b8562fe118ce3a<br>SHA1: d9aefbf604fdb336ca0f19a2c9e7ffc4ebc6ba38<br>SHA256: 9e67b95f0a83a769a8470c027e7ea072bcf568a909edae61b357c3a9fa48356a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.081MiB (6.376MB) – 92,411 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f876445c24635e75a4b4cbc78e4fd408<br>SHA1: 35fcbc17bc4777b5a03d4631a09d0216cb11aa50<br>SHA256: ba37cd084829d493344fc9c91f85de95fff3cadaf0e2009510d3a9946fdebab6</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-03-26<br>IPv6: 2024-03-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.211MiB (8.609MB) – 411,182 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5cf21bb8ad1de408ed0b581bc3ebd096<br>SHA1: 8a6b73c02e04dfd4021dd49e772881a7bc62f147<br>SHA256: 1f52aecd7583fd0c69c1088a57cb30c0539159fa8b03dd0df42eb39e74c95d04</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.070MiB (7.413MB) – 107,555 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d89f400f889b5d4732137378118af1f1<br>SHA1: c55fdb71c73802f94bf246ee902f180dc4b17f77<br>SHA256: 4407e20a9c7c452a9e02331194f8fe1190551936c6a82dafacc2aa6107f3ef1d</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-03-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.92MiB (18.79MB) – 897,894 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49934034da61f72f864d4f3746a5ff8f<br>SHA1: cd14e6b5a3bc395310b9ba14ed7dbbfb0b32ecdb<br>SHA256: 5bf7a12b3bfa92b9b12ef32ae44d36103ae3e69b2e2c935e12a573cc1743e0e8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>77.50MiB (81.26MB) – 1,177,727 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04a9dfb26e47508a9908bf0ef609c024<br>SHA1: f3ebcad0c669af8bf5e3bafa8ab0266b6756d780<br>SHA256: d4d07d9eb4231d24c417cba9949325275c6a09a24d74a6a2cbde1ab8796fdb1e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 322,326 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b232d78e18dacf266bba37244688a18f<br>SHA1: 2ea0bf2a68630d5c12c6fa1d18f2f3eb0845f297<br>SHA256: b9f2935f135d22119e5db5d8d8666980b07ac2e36359fd6dbdc9c26a8b3be2f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.03MB) – 275,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49241985f6153f5f100b60421257f25<br>SHA1: 51e0348aaa544a9b75aa17c9431f3745175c5c5f<br>SHA256: 3420806d6067a2579fe3eef92e4cd09b9b792cce9c418a3ca7f3c820f4edb887</pre></details></small> |
| | | Full Location | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,158,494 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd92465491c42b3844af48593793b1d0<br>SHA1: 53a3bac0d03e0e4bef95ad11b21c1a1e92eed9f8<br>SHA256: 6157eb8d8b93b5da65533893b6b1af8682e371476cd754957d56f3cfd1179aad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>307.8MiB (322.7MB) – 2,989,351 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a432fad1dde6398b8b6ee222abf32676<br>SHA1: 78d2ec063fa05a95bb17703a5111864cd91a5446<br>SHA256: 5974cc41b3872ea8fe373def59322db31b678ff8585a6e529b9737d648343c0d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-03-26<br>IPv6: 2024-03-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.826MiB (5.061MB) – 241,587 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53358947a90b798856b0f2491fbc6d2c<br>SHA1: 7c9c0c0ee1f075fe6d82ea2f7ca31f00a5b7ad18<br>SHA256: bf9da0021f243ed534ef8e2352a5fee71207c3b880a727cd5031b79c5c122185</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>16.63MiB (17.44MB) – 252,757 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05df7acc3edcfc49d6d0cc8e5b23185d<br>SHA1: de417cfa98cd08340a971a226b8075d8887c08b6<br>SHA256: e2904c3019400cf283bda389c8d7dc9f8c0b5dabc1bfd9dc40ea4326c79f404f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-03-26<br>IPv6: 2024-03-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.8MiB (179.1MB) – 2,959,758 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d837249426a59f38d52d9939db4c1a1e<br>SHA1: c71a37a88777bcc232ed0cec8b11f4b0b93ba955<br>SHA256: c25d6cf67e34fdd6f9b5042bffd4059449b156fc6b7bb6e3fd49ce1979642175</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>169.7MiB (178.0MB) – 1,642,006 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e91d25d35aa21837cbe8c01e725e1cb8<br>SHA1: b3aecd7e3f4493788fdc4c941a22f3f071cd5130<br>SHA256: fe72238b338f395cd55c98381ca41ebddfc893eb2bd92625551b9fe4d8d96a53</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-03-22<br>IPv6: 2024-03-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.640MiB (10.11MB) – 482,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7429b5acc1a53eb762ed348111507f37<br>SHA1: 7074fe743fc2bd4d711aa68f12f55fbfd496ef22<br>SHA256: 9c76be781576b1f8ec9c3b48528de43b7aa0afac55fa334de23b096362e9904b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.13MiB (20.05MB) – 290,647 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55571197f51be4ad9b969ac122525a0e<br>SHA1: f00531eb4138822625faa82ca8447ca26bc4fff8<br>SHA256: 5ab2aea2ebed24d472cee901c6e7abca23eeeb256fd2b4536a6b4c923ef46a8e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-03-22<br>IPv6: 2024-03-22 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>143.4MiB (150.3MB) – 2,878,611 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e342e2a46ae7de3c14d84349c53d88ed<br>SHA1: 8c2548a80ca0bcd9d3eb78320d778508e6d401c4<br>SHA256: 4c6c993159c38b8708102f9662e612f7dd6461affce7669182f049b78d20a7ee</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>156.1MiB (163.7MB) – 2,878,611 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a1c0d90d24f0dfbbffc8e81b3330972<br>SHA1: fcfd77a5134b1f51191b543d161d4fd8e2e1853e<br>SHA256: 9010e5a829e79adf14581d9b4520769744c39ff00532d94e8f36ee98f3422fae</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>143.0MiB (149.9MB) – 2,878,611 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6eed7c1b71eef07521d4b9ce2408679<br>SHA1: 424833f01972770cdc18fcab6d62a8d81c4b792c<br>SHA256: d7e33f380d9991c0983dcd8da9b5cfece62c0b192328708cb006d8be5e69b5b9</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>146.0MiB (153.1MB) – 2,878,611 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cab02dcccfd945970c8d71cbda434b1d<br>SHA1: 32dd800a13a81ea57052a6a030e90e932a7b898b<br>SHA256: 7a8df8b95970738ef326a1407f2d3c1588b15a83e509c2b6c872f512815d0d21</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>178.5MiB (187.2MB) – 2,878,611 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffe8d1109d1aca5a19e12bc8d48cdc11<br>SHA1: b1c5972f2171d854a8136cd241ce2602435a2b07<br>SHA256: 15e79a84a59f2dfbbd9e59433709a9cb14648797b3361350f4011e32bcf3347f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>141.7MiB (148.6MB) – 2,878,611 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64eec90e68d6c83d4caf4c68db1bc25f<br>SHA1: 2520db93661817a7ea5ae71087aaa03a37d18dfe<br>SHA256: 6ecbd1f6b2413e1b5a8f0bb47c0857e96024d14cf8466a5b2f7dc2accc744361</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>175.3MiB (183.8MB) – 2,878,611 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d8dabf6fea58a853e69ddd395cefa50<br>SHA1: 7f825d7e6ecc34190b0ca9b2583536030f49dc94<br>SHA256: d31fcbf857292cc959ff08abce3f7eafc4222dae690cdb4af65a20e0061b486b</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>146.7MiB (153.9MB) – 2,878,611 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e88766f9d24f9d964df38d6f41da946<br>SHA1: b7e15eaafd0808efabab955c7c0b728c73fcca1d<br>SHA256: 28c558e34ccfc2d4d8ae0348b1241fb1d129b9c688c2b1488e95beac67bb37dc</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>112.5MiB (118.0MB) – 1,215,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6da7fb91df6d89330174b8013cfbc244<br>SHA1: 197f2a5c27cab03fe050a05d3ecbacbbe2863e37<br>SHA256: 040081707a8e1d2d8c65028e19909a113f96e2488d380e633978183c90f74001</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>116.9MiB (122.6MB) – 1,215,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99ac8ea04635b8fba1c8e3326529239c<br>SHA1: bddc634bb5882c38db2a3d4b53bfbb1d07771878<br>SHA256: 82d83243fcb3009f20972cb858dfa006e19d3b46cc5ead9644d5c614f9ae0e82</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.5MiB (118.0MB) – 1,215,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01dbce62092593e32c6b7d35162d8cdc<br>SHA1: 864824ba669363639b6c634922097d28c3ded4b6<br>SHA256: fbae049f6908c88e85c5fb3b630358e513de5a7737546caf34e0bc993a242de3</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>113.2MiB (118.7MB) – 1,215,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c93b9f307adb1a5a632ede0d5271bdc<br>SHA1: efcd5bea306de19ca465738624ff4ff1dec3e133<br>SHA256: 84f246a7b6af786f02946392a9b9c8eb33c2b18af2185cd2de3001284187949a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>124.0MiB (130.0MB) – 1,215,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e5e9e3f8511d3c8efb85a2336036f6b<br>SHA1: 843e5a5055030532f00a064c4dbfd0a4a8bdb0bc<br>SHA256: 42ccf4e2df89c0c03a61bd86f417c0e5a539aabc093152affb3bf0c5df33e381</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>112.3MiB (117.8MB) – 1,215,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81d5867bad9270d43c53aad857554d8c<br>SHA1: 781842c27327b2f30e7d8d7132150bf8c27541f6<br>SHA256: 541596e7490f9fd122c954c824c91b88c7833c674bc7f778b61e22c289b0fc40</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>123.5MiB (129.5MB) – 1,215,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 835d68654c00965ca6c066ae0bb019ca<br>SHA1: 9e8b72fd5017ec95804411ad17676f970248887f<br>SHA256: 424539cdbb47a5a780a4bffae8390d163428951b3426012c158e6f78f014da83</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>114.5MiB (120.1MB) – 1,215,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c64e9eb527b0f2f5f4354c2cf420341<br>SHA1: 125eb914a58f9568a74eba939285170c9b466b0c<br>SHA256: 9dce468646df8e2f02966b0f8294e71c11999dde8f777953b763c5199d2add10</pre></details></small> |


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
