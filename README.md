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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-03-29<br>IPv6: 2026-03-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.505MiB (6.821MB) – 325,841 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0eb59155931b12697313e985b230210<br>SHA1: ccd16c52783dc5e0800030dc2585cac0cda59249<br>SHA256: fad6ad6f45145f78d45b7856383ab1c64e660d08d2fdbb57f262165dc2fd2758</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.52MiB (16.28MB) – 235,898 rows – 258 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd2a84d65cecdf16933a14dbd131e650<br>SHA1: 531a9775e448e3ca9c978d4a015fc433bf862f02<br>SHA256: 55ee34847aed4bb5affdd2e4698090de54caf28684c6167bd6d993809d48a579</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-03-29<br>IPv6: 2026-03-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.816MiB (9.245MB) – 441,464 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3abb2b5d58d6cbb2c5efc7b44280d1e3<br>SHA1: 88f47e4fc298a98f84095f02f67f75066629b8b2<br>SHA256: 8bf54e8abdca81b541b9e28309b19321ee39aacb7ee51182d191c4910bc10f0b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.690MiB (8.063MB) – 116,975 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e980b224045d7b743420e45a257c2912<br>SHA1: 5159f18beea62659526674e19f4d03a4e773e120<br>SHA256: b23fbda2b1b52075eeaf71828f75370737ffa2301444983c603c26652b4f50af</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-03-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.39MiB (12.99MB) – 620,209 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a39bd250839b0034f4212f848a4dfd8b<br>SHA1: 0490a9f48fbd1db01e2951e9bc553c97315407f8<br>SHA256: c3f51c5bd91b3ad0aa469b0f2847565d70f3dcff42b56ac908ea256ecc1d0b92</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>108.1MiB (113.3MB) – 1,642,340 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d21b23d773c00586b3667400c12abb0c<br>SHA1: 264ab5d34d7a3c3b036291611ade9fe1eb269314<br>SHA256: b8d5c5df9680f3b08e59e9302562d2705cdd113ef12f63fb8e4d13dfca74ed42</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.906MiB (7.241MB) – 345,970 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be67480ebe04792eaa1e993732e26bbc<br>SHA1: b9c086649cbd7a697ce8b1a6f1200cf343683838<br>SHA256: 97e3ba0306a918694a1abd35fb0fbe18e3275c023a00d3f378bb52d0381e6ca4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.48MiB (17.29MB) – 250,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614f4ebb16bfdb3cd44828a77fb774d9<br>SHA1: be56f3e3114c6c18c1b7e097bb867772c72bf90a<br>SHA256: babfcc027ee9656b7ebe280a391c73174b4990721bda2e7c584c23450f4c5452</pre></details></small> |
| | | Full Location | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.5MiB (222.8MB) – 3,723,444 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d34e3013a398743fdc3bdbd816dba48<br>SHA1: 4f4868afd37a86dcd98f0ff21e863db08c4c69b8<br>SHA256: d805d064a2ceaeb75e8ee847780d1dcf8f54852ffa98bc007b0894fd1c1d24d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>446.9MiB (468.6MB) – 4,345,257 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b0322dcdc11f95be5a5b01f4221151<br>SHA1: 5bcecfc1d1a51db165a9a209bc8f4b9a5e7e1bda<br>SHA256: 9a67a943e4fadd058173607911c45bce627c5fbebc2abef2f229894d2e8fc57d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.419MiB (5.682MB) – 271,203 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c176ca445d23383a4c5e1e2ebd9e541<br>SHA1: d9049c5c5fbb465dca6e199246fc0f4419435e17<br>SHA256: c56f984490695ab20d84eadbfd37f601c78de75f4958c1d1ee5927482ffa66cd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.22MiB (23.30MB) – 337,655 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c07180576fcf598a4054e35c7eca4e61<br>SHA1: fa9ee16f19dba3851f20083872d13d4acbc065ca<br>SHA256: 8e65ba7778f59ef63c1a8df94112a447927b3896dbadb00d080914b5ea37167f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.6MiB (174.7MB) – 2,881,763 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1614bd25a28d2b44922c3116279f804<br>SHA1: d2cd1e423c13e941548d01a453978c165e423b8b<br>SHA256: 8486e52f22f5c609925e25d4d0d4e74ae714d31b8ee7067d87a99f951d8352c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>298.4MiB (312.9MB) – 2,892,579 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85c1923ae57109129fbe714df2b92c0c<br>SHA1: 846479cc0828f79ca640a39a279ddc2fc7b8aa2b<br>SHA256: 1759b2d35ec83b135771dbe6a08ae383efaa2981f42a80b1dcd3ee4ffa98633a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-03-27<br>IPv6: 2026-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.92MiB (12.50MB) – 596,812 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0591274ec0e5817e24148e8e76478b8<br>SHA1: e1888c1216a21728fff399e2f756ef23fc350db7<br>SHA256: b6b036f8e4e89fd154901f4f8380fe6bd8dd44b61386582f50d8de03c99593b1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.64MiB (43.66MB) – 632,734 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a671cb1ea9f0a2665fb309f90600aee7<br>SHA1: a24e23c013c01c2c5e522140ef42b6785d15fbdc<br>SHA256: 27242102a9b46450f33f11a7e787c98d21ed38c26a09c7a6f3d7458ca2142d62</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-03-27<br>IPv6: 2026-03-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.9MiB (187.6MB) – 3,535,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e11a08d002e5621739d262b4eab01ae7<br>SHA1: 00d24acff210ab9d61d99ddff87c9b9d7b9dd1ca<br>SHA256: e682e5caabf36b8c73b13dd1dc96c045a43fab64b8cac5650f83a9e56a53b239</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.8MiB (199.1MB) – 3,535,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 259e0b00630a0e4a55b1c7ce410863dc<br>SHA1: 289679a1dd8d9e3a086294f2d6bba5317e265e0d<br>SHA256: fbb343cc10b511a0bdc4e2a8fe72462d0df4ebff3d6c429598b27981b10b9acd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.0MiB (186.7MB) – 3,535,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 793b9d00b6d1c99d7ada56aab1419ace<br>SHA1: e5b71e3a17bcd05b98f1b3b9ab9a142410af10f4<br>SHA256: 1c2c35df537ebd7e9d3922ce3e3abdd5ad00f31311fe528a29ef61dd8edf44ca</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.9MiB (189.7MB) – 3,535,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09e70babfd5946fa3866dbace5e867ae<br>SHA1: 204d16578b1c54b4a4a269478cb348779bc7519b<br>SHA256: f190b875784da4f4e8fcb8031766054a63b0070313ca8d4ed6c8e78107b571fc</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.5MiB (236.4MB) – 3,535,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59e45d4d38fabfca8dde716379c2ce47<br>SHA1: c3a5cddea41614611d22305bf7699b4c86af87f2<br>SHA256: 411b10fd49aa42e66fb39c45c7b794c2f7df10492030b7ce3c628bd9703492eb</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.5MiB (186.2MB) – 3,535,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7136d23803edf6489cc3b0008cd2423<br>SHA1: b0322739dd2c90472f575f9b84a85c73c623c738<br>SHA256: df93cc1684413a9ca867f940d41f3cf3aaf6af16530c026a94fc321c349b315d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.6MiB (230.2MB) – 3,535,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c853b3f7ed4dc521faa6217873afd036<br>SHA1: 2c4113cc760001d79ec22de2f2ac153098aef288<br>SHA256: 8d7b049660bd0ff4410e8142552357deb588d445c955230d69f6a866b715232b</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.8MiB (193.8MB) – 3,535,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 451e5e9c51ef2838b428157029e5b28b<br>SHA1: 38338510afc1fa3eae65714ec882f96485320aaa<br>SHA256: 7a98112e39a192dd0b590b4e393cf66a4afdab43beede7ee8f5bcc54a932de83</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.9MiB (197.0MB) – 1,980,282 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dba789c32d5955512af5f24887365837<br>SHA1: e46960f7dffe8573d37dd7c2d5ee8293b2fc46ed<br>SHA256: b1f48cf4edf5bf58ef51e59a1eaff8ac6d2d13654ebffb6d2f817eacc8ec0256</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>192.1MiB (201.5MB) – 1,980,282 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e550618facd221b1a4daa31d7fc8aa2<br>SHA1: 5ca904210a03d3c69f455dded4b51a5e69cbe95e<br>SHA256: 23b04a537eb72dcf043b77503f7d81909497f20aaffa1c5d6ab1bbd508552228</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>185.6MiB (194.6MB) – 1,980,282 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4a3d1ce73e12a8e3f56124a1d2b59f4<br>SHA1: dc6ebc0e9490e3ca81682e7759f7c557e657f883<br>SHA256: 880b0b7325f034cc9256a6515b499f1e22e310c6c0528ab080719606eacec7d6</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>186.3MiB (195.3MB) – 1,980,282 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e832e120086788e3f317c616e67b971<br>SHA1: f4cf6b34bdab0974aa2fa5ebbea2f29c7e0fcbd9<br>SHA256: 49c1c1a5eb95d1aaf4baba8c53c2a5faf1b03e1f4284c2d0c5e7fc45a3894e3d</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>206.5MiB (216.5MB) – 1,980,282 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1181456f63fd0f0b327dea6850e52fb6<br>SHA1: 237d4d4e46441be53034a889749fc88ac971be40<br>SHA256: c88b8bbcb0d42110ddc028487cbbbecd84d16522b24e9bcc266d4236a1c95740</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>185.3MiB (194.4MB) – 1,980,282 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97efda29e522f342fba39c3931952795<br>SHA1: 5b0cde6d0fbb6095391a30e088a8c1e8ec769602<br>SHA256: df7e9e1801eb7b1694f6c75abc749d88b456806e8c8d9910dfff5fb18afd1902</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>206.3MiB (216.3MB) – 1,980,282 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc03934e0111b34fc7c482cebd79d754<br>SHA1: e9690032deb15445c957e27961d03e9feede9db8<br>SHA256: 506aff8b7f56086b9ecbe1aaf2713eec74f93143c1e24d64a873f2dd09c959d4</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.9MiB (198.1MB) – 1,980,282 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95e82e96a21c18ed8fb498e030482204<br>SHA1: 74ef0e3d20a230b7164ae388b88fabe1830ec1cf<br>SHA256: f1ddbaea34e5732906c68d7879c20c66e418d9a9337cc1b5c3e6d10e003f2f6b</pre></details></small> |


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
