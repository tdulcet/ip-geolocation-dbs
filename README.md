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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-04<br>IPv6: 2025-12-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.377MiB (6.687MB) – 319,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a7e8172be29125c261cf8e6990099bb<br>SHA1: 8853967ec985cb2b364a72e38ed2d17af1a5689f<br>SHA256: 42efc4f4015f7b9ede70f072427479c50bf44ccdfd134a65c7801a5de1d7b296</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.677MiB (7.001MB) – 101,466 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 896a0e699e0ee722e2461bcd3891d0ce<br>SHA1: 37d4046687ca66bcd054f7a417ebd6aa24be96f9<br>SHA256: 38c72fa381a37c6d24c3799011dcecde1b97f9f47c04de2380181f18ece475dc</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-04<br>IPv6: 2025-12-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.783MiB (9.210MB) – 439,779 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33884896aaccdab7fa2e976b61b079e6<br>SHA1: b8da120779514a95904064fd1b7781d9e4134ec5<br>SHA256: 1d0e74286732350bffa09d0e2a5154d9c0d9662b12ab5ddefd3b7527fce1effc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.535MiB (7.902MB) – 114,630 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4052cc4c7a2d24af2bde4f32d9846166<br>SHA1: 622686c9bc6a0a493e80086e307f2edea82e8fa7<br>SHA256: 84ba2fe441ff45af39f7dec1bd78a905ff9d6c0a71f7d0850c54408625a0dcfb</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.26MiB (12.86MB) – 613,840 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f48335a65ddf1a91beed075a853d918<br>SHA1: bcdf90e12ec18a5338193f37d7d83e37a08aeadb<br>SHA256: 16f440d97727200092ec14b4a58ba4537e15eaf26ec86ccfc3e0b7f4c5384561</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>95.54MiB (100.2MB) – 1,451,964 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5885888ba1621a5de3329910853bafef<br>SHA1: 09e0995a445000c784484a24693e9b6cf5480d5d<br>SHA256: a00fea0a19511a45cc7647f69f91cf1577d9976f87342f0c28cff6f5bd22f71b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.367MiB (5.628MB) – 269,273 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f62178d410cf3bce771f73d48e43faa<br>SHA1: f7860e76e84e2e025ff86a4e5640a5e924783fe0<br>SHA256: c1072a02c991020475c91925325c135d490b5d243b47ddaaf047c7cdef840cb0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>20.32MiB (21.31MB) – 308,850 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 594439a3c0811d183bfe5550c4fa8326<br>SHA1: 2cdad07afa5d0806f1da62dff5def384ca6b52c2<br>SHA256: 86d5eca80b132381a0466a85510652d17f94597f2ba2f6e7a930843309468a04</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-11-30<br>IPv6: 2025-11-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.3MiB (179.7MB) – 2,965,067 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a5854fc5ad699cdf214288eb10b070<br>SHA1: 02297fb66300226ae67a1dcf129bca4e4e77ed1b<br>SHA256: 2eafbe9230ee8d23f99e769b27da134fac2c62d6a74beda67c278e8823866eb7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>277.7MiB (291.2MB) – 2,688,825 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7579bd752fa4e59ed8578642ac57a02e<br>SHA1: dc5caed7e7217beea7fbec082ae0651c0f13d1b6<br>SHA256: 0d03be0ad75f92ed0fe8301ab4717341f744711cd9bce0dd880a1632aee11d8d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-02<br>IPv6: 2025-12-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.41MiB (13.02MB) – 621,397 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a44aeea9f24b18c37cfb04b995f111d4<br>SHA1: 49aacf9f2b57c32eb73a6395d8862937dd834560<br>SHA256: 4219d7bdb73095d5d314bc828f34a7b657ff92000466dd99e9c648ef446bdbfa</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.51MiB (44.57MB) – 645,993 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e17b448db7a83593a705abbb1190009c<br>SHA1: 27b0ee1de535e1601bfeff39af38c137b65cbb4e<br>SHA256: 3f8c43088b0ab02c40c330f6014f3106fd6a892d6fc6dd4e01e3105e8f23b167</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-02<br>IPv6: 2025-12-02 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,536,544 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84a6f884aeacc75e6b104d3f9c78382f<br>SHA1: 885801e107991d790af89e73ca96601af4feab4b<br>SHA256: 4b2ccd8cb4c126f94d44c13fc0534667564fe6cea4c32e4127099ac69a933280</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.2MiB (199.5MB) – 3,536,544 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e12368fd57ad47969d34586a9f1048c<br>SHA1: 83ff73cabd232c9a4b80fa2d0710101708a76bea<br>SHA256: b9be96286c3153aa786acb32de4b752d78cd78c0ea381da56bdd7cb70a671108</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.1MiB (186.8MB) – 3,536,544 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea5059afcaf5bd82286904e3fea7cd11<br>SHA1: 651cd4d5d4b6ae2ec4f37bdf76ce0bd1bc20804d<br>SHA256: 361f2c5a9b36ac99b0693427b7270470dcf11bc12913c80ddf4dae3df3bff5bc</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.9MiB (189.7MB) – 3,536,544 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 527e809dd18e3c46420c02f9507afebc<br>SHA1: 4dd62a956c5f876ab48c563b3b0af1d5396544c8<br>SHA256: 9033717b1d81b78f2ce6c81a7391ef5e2eaf101052f0f8e2f13b12ce2c3028a4</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>226.3MiB (237.3MB) – 3,536,544 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85e5ac17e23778657f524d7ae9df74ac<br>SHA1: c274faf87730d7f329ad64d5f63876661a546250<br>SHA256: 7ebc8dc2a5338d1561c9df1d79019cd878c48b723c8b57adca040fb3a33e6d9a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.8MiB (186.4MB) – 3,536,544 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5eaf5ca1ac41c45c52cf16aa952c5e82<br>SHA1: cd87a96716fe4e53673be616e0cfc7136fb98ae0<br>SHA256: 1588ce81b9951cd347c85a2aacb5d62b960a83075bfd7b86c7311b19dd8f2437</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.0MiB (230.7MB) – 3,536,544 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9124a8b3f969ce2d4a87de75fb4c998f<br>SHA1: 9eb378a7e7b76350df9fcb4343ee84545d34af55<br>SHA256: 614818421323f778c1ef8297db3bc96f97d7c2efe2117ed3d0a8d1dac653ca29</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.9MiB (193.9MB) – 3,536,544 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4800451499b05d76cc06fc2b87cf6a0c<br>SHA1: 742ebb8df5fd909cfb5482fae5146d366419fd07<br>SHA256: 3e211d6777ff9cc9265bb48f5e3f69f18f96994818b67300bdb495597fbcb7dc</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>180.9MiB (189.6MB) – 1,907,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 13ee68243d9fcec871e300d28a400436<br>SHA1: 7d1cae4e4f72ec6fb69d88fb59c9d7fdf4d9fc7d<br>SHA256: a58223ac52dac1578cf73680f47a8d2e3820625918fe7b2d4ab136c808433066</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>185.1MiB (194.1MB) – 1,907,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1a85be30a6d91021c125f8d0799ede4<br>SHA1: 35cbf48ffb62964a983cc2b328d08fa0e6e9f086<br>SHA256: 704ced3b52744b109d6ff86672a3117b395988a9c06489e90ac3394bd8ccccc9</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>178.6MiB (187.3MB) – 1,907,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9097bfe18731f06824c22cc14db0f8fa<br>SHA1: 3eafdba9dc3ac52b63b5638a8c0b7a14f903f4a5<br>SHA256: 71ce7175a61d18cd28d77393e789eef2bdf02ea379a01051709a5e9087327368</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>179.4MiB (188.1MB) – 1,907,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0570346d106f9512132d7f4ba9d69d72<br>SHA1: 429d8e940f6edd59a23da864997bea95a0783daf<br>SHA256: 280407d32241da40e1227794ea21cbb0461e12b4801dbe8f986f2f3fb720509f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>198.8MiB (208.5MB) – 1,907,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78f9a9b7b2ac6b3b287d19cfb2cfe706<br>SHA1: 294f0e1ec2733cad7d45c437de1621df16d8bc45<br>SHA256: 02772f68a48870a2654a63bf1089e0e4352f5c55d67660c3e2e598ba53cef39e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>178.4MiB (187.0MB) – 1,907,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 525d6227746f57c83d53778625521eab<br>SHA1: a76333c38846f83805fdad5c35f5938fa6aabed0<br>SHA256: 27b4269b96865dbfd54a43da8b84d127d7f9268fe8af09a4c8452a55a0d29753</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>198.8MiB (208.5MB) – 1,907,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb8f72d6931718d84bed3a820850fff2<br>SHA1: 7e04ce7fc6e01b898a20e633b60e9f7e89e81af7<br>SHA256: 4d111f3305858f9e47dafec082538f6ddd2e67db42544744a165d065ed071dbc</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>181.8MiB (190.6MB) – 1,907,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f4da2c136bcc2ed480d3536f6cd676e<br>SHA1: 5f2655840daec4dcb328390ec2148a9d75ce4a13<br>SHA256: 7d3ee742d05f7b82ad6235d69d9f68392680f8f84753a065478faef725b73390</pre></details></small> |


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
