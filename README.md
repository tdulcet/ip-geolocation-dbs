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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-01-31<br>IPv6: 2025-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.994MiB (6.285MB) – 300,103 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b78ef38485871508beb6a08b937b90e<br>SHA1: 701bedf2b35ad210a62d22bcf84f11416746b641<br>SHA256: 52fb85f74039f8ef5d2477e920e0dbe6b0cd3b959fdfae0cc6305147e1477449</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.73MiB (12.30MB) – 178,298 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c2203eb41c152dec5b3ea9b83a65d69<br>SHA1: a51f82e41be3a4f08229f3b85f42d5deba0430d6<br>SHA256: 1728a52a372050f06648ee69004d31ee25abe18203830fa116d2902945be9bc0</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-01-31<br>IPv6: 2025-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.347MiB (8.753MB) – 418,014 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d93f07ac48e56a4099fa32262e02fd75<br>SHA1: ed7f76b779d83d9f419bdfd2400ebf94ea2bb8b6<br>SHA256: cf843eae8df562c4d850acf2d6402bd998443a7f36031ad9b528d86ead9b0f43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.967MiB (7.305MB) – 105,985 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 763a92debbd2334af8ce9d4e59473f35<br>SHA1: e939499b2885c27e5408244ac6c3aafcede507d2<br>SHA256: 8cc271cc2594991413c5cd91943242526f06e3615dec8d1a2409e6f5873aca36</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.35MiB (12.95MB) – 618,202 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae892be38a2febc15978c99d14e0b47a<br>SHA1: 2ec383d7fd9509f89dee9358d5b73fe1c7bc17e0<br>SHA256: 725e95f3d82704e2de9694c26addfbb736e01c7a50fd19f06747e67f43b233d7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>82.84MiB (86.87MB) – 1,258,926 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 372a10b18aa784d1947a5b80d26537c1<br>SHA1: 5ffcbc62bb01f92af22f119d2ad18e709d227d11<br>SHA256: 7100cfebbf2a1be533747c0ec1cd46de271487842f62ca02203f288dd2e1ed91</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.285MB) – 348,457 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83bc658c1ea05ee0c1dd67b508e416c8<br>SHA1: 70aa579150d7be548067432da89e0057b10e615d<br>SHA256: 636b0495d96e6e73c2fd6a2d599b3713d050acf8c2bc75556af8ad5d0fb3f95d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.36MiB (16.10MB) – 233,400 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea165adc6016bf7241db413dadd9d616<br>SHA1: c2e689ee2f5aa199cdf34e7bb0a4facf213548c1<br>SHA256: 40a1cbecef33f526b989ce930aa6fc2a0952064828188fe18df5b777d10b8d72</pre></details></small> |
| | | Full Location | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>187.6MiB (196.7MB) – 3,275,051 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ca665aabf2aee0b7c39b4545a5f75e<br>SHA1: 027d0a8a8014da5f6fc12e62c926c6933687bbf0<br>SHA256: 249e041ad20b36d2aebf8acd5c4d86a5f88957c86f3a7137f906df3200c6f623</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>347.2MiB (364.1MB) – 3,369,294 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb9eca947a082a3f2644b8c6907a6194<br>SHA1: 6d3040b4badad6d8c3e74a1fc773d997d8a618af<br>SHA256: 4d20b8e6b46f24b32ed9d99c2e5316f3c7e940a92aafbfdc42bea1eb6751282e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-01-31<br>IPv6: 2025-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.106MiB (5.354MB) – 255,506 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80e1c64b5c125fb46702d19882d68845<br>SHA1: d20869dac975135625842bbcc7b817f2b47da8b2<br>SHA256: 399a14c794395d001176ed9793dc27f299e4ec2de8f90dfdedc07c6a433b0214</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,282 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63b017b1edcd0613c72b27eb077caab5<br>SHA1: d04cfc8b0738a636a2e7787d56061329ecfc4174<br>SHA256: 75f4cef5e2d3c06892367ddaf51c9842b12960eb86547e026e2e127a0d551591</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-01-31<br>IPv6: 2025-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.3MiB (184.9MB) – 3,054,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7e63fc3f917acbfd3385aa01ee6b4c9<br>SHA1: 32e4cd6190262bf917d8b7cf206924ffc9d12809<br>SHA256: 8ea4b66fa2628df42fdc49f527c411ef1916e77a858644aa2bd10598df1d2140</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>230.8MiB (242.0MB) – 2,233,220 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d3ee6ff5b739344f91652d949eaf994<br>SHA1: 2eb2eda60699cd7653ca6509c327cec4e486e798<br>SHA256: 5bb91a2e35c6d95f3c0a40e6551823c1ce8cafeda7cac1926bf871dadbb045a4</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-01-28<br>IPv6: 2025-01-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.18MiB (10.68MB) – 510,160 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3a54f0afbe9ebf4d84f892348b47e81<br>SHA1: e6d0ab8d900c7a7fd153f6cef83e7eb5d076a285<br>SHA256: e1fd74983d36d66e5f43c4ccd71416763a0ef263400bd086dc9396a816cade29</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.58MiB (33.12MB) – 479,979 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0453493641a5d8a088b694adfc1f4e0<br>SHA1: 99b8c0b96dd5057754e6485da08ba3eff4dcc0c2<br>SHA256: b57e215987bbbc48d1e6a5101fa28c15c4cf31d3cc1811f939982a3b4fbc1a77</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-01-28<br>IPv6: 2025-01-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.6MiB (173.6MB) – 3,273,952 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff277cc6291f10e239d10351b18c09c5<br>SHA1: b774db21ba993bad7eb44df2ab06cebb07b92641<br>SHA256: d1a6dd897c134dd6a053026222b5f752310b4654a9f3b6286a85811fdf9ee280</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>176.3MiB (184.9MB) – 3,273,952 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65bfdb99ca45fa8e002e9ae759b0e715<br>SHA1: 62b03e9ce24908aa5463fd068949c2604f641479<br>SHA256: 30b1479a81db548040bc994f8dd73ea161f4330dbe93f4bb052189daee0da9c4</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.6MiB (172.6MB) – 3,273,952 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad76514f00e53b447be09d5d01e56910<br>SHA1: cd9a5fa3d4aefec328cb302b8dc8c9e72c93acbe<br>SHA256: 0febad21c36c704a5bf32060e7bf17d21241294bc0d3a7828b1c70e67a0af091</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>167.0MiB (175.2MB) – 3,273,952 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f08d863c7eb56d3eb5958f69917f0cf0<br>SHA1: 96d12ff277e184752d16692fb333009b84d4ae60<br>SHA256: 8dc94fadc0cb2d908b26e524614577153f1a1167e0a3ebec03fe2e95c41cef06</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>210.0MiB (220.2MB) – 3,273,952 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 194f704598900b896dad29f0093510d8<br>SHA1: e32ae681758e46d5dd4f37dd9f4156bed4426436<br>SHA256: 53964e3671ada9ae3537b8d536b67fe8d9f51ac35a55e34a7c98c56b2d461ee2</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.6MiB (172.6MB) – 3,273,952 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d60fbdfdc9ba38b53f860ae5824d9790<br>SHA1: ffb56550447dba06e1f2d7013597fb209b993792<br>SHA256: 927639263d7f86be691cfe5a06a1f6372da5019e5f8b500ee8008f8843eeea85</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>204.0MiB (213.9MB) – 3,273,952 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 528a84fb07b314099d716391b5aed134<br>SHA1: dcd1db4b0a9e60b270251a4bffa3f341eb4f6886<br>SHA256: e2ec6ce59841dd4b740fd783535883ed4d0d3ef68588faa6faf3ca2410529413</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.7MiB (180.1MB) – 3,273,952 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956a2e691fffd39d684965f0064e9897<br>SHA1: 62faf5487af020bb1558b6a78efc85aa6bee1267<br>SHA256: 5e128790f5f5bd4c26a31533cfa912ea099ed5e098813ee58ed551b111d039c1</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>158.0MiB (165.7MB) – 1,685,251 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cedbdcaf8145cf623f1283032f11dc43<br>SHA1: c84919d1fbaa3694b96fcca8506167e72704db4f<br>SHA256: 415074887a2acf325d154a5a3bda2b7184a7c54f9480bfc5fcaf09b598ed83e0</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>161.3MiB (169.2MB) – 1,685,251 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef3e53978a47c999971993b9c2b8bbcc<br>SHA1: d5384caf1673568fa1b84ec12c80acbf3be4745d<br>SHA256: 02b1542b0f1741761b9f5f5a699ee66120a8ecea2e70076538987bf5cbb65606</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>156.2MiB (163.7MB) – 1,685,251 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28f4b0406577e6724b129d58cb7ea956<br>SHA1: 960012ff9c342d051003843bd68d1355427f33cb<br>SHA256: b2b4c2da8fff7cd8ec293b976baad6296ae84f361add915479358bf44750957a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>156.4MiB (164.0MB) – 1,685,251 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80d946f6054e8e999f10ebe2fe98e40c<br>SHA1: c55a4e20de9ba9510a09741248b68e7bb58627ee<br>SHA256: 475c371b39a5c98d295b9b55782430066117b80b6c37129b703d5c0471c905fa</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>172.0MiB (180.4MB) – 1,685,251 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d297e392c845685d25971709d2f1530a<br>SHA1: 8cc6fce9ee8ac48b7502d6f7766b894d19cc9414<br>SHA256: 58de41119b220c9df5b0f552687d916e4d4fa735bf471746c6001d7fbaea34ed</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>156.1MiB (163.7MB) – 1,685,251 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74f2ed7850a1c4241909bcd92f1d6f8d<br>SHA1: d3e2f9369e7d8f9a3df81d79c41bb1b01270efca<br>SHA256: 2e0a6a6c5b1b835e8e81957aea36567e76e1ed968119dd7abc1f04ec121b1fae</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>173.4MiB (181.8MB) – 1,685,251 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1a66fc1db1e26b75b312db89842b1a1<br>SHA1: 902f6109f6d6d520ca2b9c33496ce2d805bbf362<br>SHA256: 5ba299c34dd231c4ba9e01c2f47030ddf150ac783faa1bcccdb9e64411da36b7</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>159.7MiB (167.5MB) – 1,685,251 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 339d459966d3504b851e736de1e740eb<br>SHA1: 246afb977b1547a1b94d9124cc4c66d8e34b7f99<br>SHA256: 058dbe69587954deff36072f4d43c1da8c973e806152ebe636fa0f2b4924d76d</pre></details></small> |


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
