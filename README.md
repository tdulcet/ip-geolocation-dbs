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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-12-28<br>IPv6: 2024-12-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.954MiB (6.243MB) – 298,106 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 218a259b6a4085d2b43e0c97a68461d5<br>SHA1: 6b850af7af6ca14649680b8362ab1a8e47d53a20<br>SHA256: 70f4657f2333bf28e5bd9b0e5c946918d5b25d707784d0caec0a7861c0e598b6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.011MiB (6.303MB) – 91,344 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41e2c1c570c4d87baf80fae84714988f<br>SHA1: 70fdaac921e31edf1cceb93b1e65cdbe5b0f5b2b<br>SHA256: 20bd2a82301359641af97f83515658b3a08b877481bd959aefbb839bd7a0b2ae</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-12-28<br>IPv6: 2024-12-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.287MiB (8.690MB) – 415,006 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d5c5c6abe2ea7da818f25802585a704<br>SHA1: cea881b2d3591e41f2f6d56b8946bca4e1633abd<br>SHA256: 5f00dc8a60e2f381f380367c4c68959c3a62e5e592547d9567c0bd0004a5afa5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.971MiB (7.309MB) – 106,043 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2c5313cd6bb586d781af00933167d45<br>SHA1: 27eb68d10f99e9c9268a2ec962f19f14b8f3bf9e<br>SHA256: d4e8ff1e3ab7d4f3e5210e9ca85eca00aaf5c71c7c2177a375222b278f5a6beb</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-12-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.49MiB (14.15MB) – 675,522 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79537720d280654fd71c3d544b137421<br>SHA1: 250f3968fa10f7587bc19a63afefa5c76b766961<br>SHA256: 79251958fa46c52c55d5e2f076ec41c50d93cebf0895a206913aa687a8025c95</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>88.95MiB (93.28MB) – 1,351,816 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 675ff745d6ce78855a4713ebb67a88ec<br>SHA1: 593196a17cf49ebd4d1c0eb4577bbb5b88665737<br>SHA256: 408a609dee9bdbbb3894e2b3bf017700b99ae6e27233630fb3834af00be2df9e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.156MiB (7.503MB) – 359,168 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4fa1848a017a51ce167e1b45ef180e0<br>SHA1: d025902fca69db441cbc83871eb99ffd4b92c75e<br>SHA256: f02df1b7ee71bf749e1e43de462a3f6c365d9ed6e72e1d5c6faa86f25acb568c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.24MiB (17.03MB) – 246,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fee62599a38c614b43a277a08de845d7<br>SHA1: f6f5eddc6f61250f0fef53e42d76288b85a9971b<br>SHA256: 258dacce2a418e7297db10bd484df83410a61ac130bc1a5820b6fb0c0c58cb70</pre></details></small> |
| | | Full Location | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.6MiB (199.9MB) – 3,333,541 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f97a8dfa3d2efa2169aa49e5067082d<br>SHA1: 69f6046d5bebaecbd09f512a07ad0279a8bad58f<br>SHA256: 193177f00477af08b776744f0aa5ea8ffe08fe54bbe785733206c3c6f5ea0b02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>381.5MiB (400.0MB) – 3,700,914 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60c57063e8597965c85a15738ce2271e<br>SHA1: e6cfa1c20dff9df4b9dedd101304ed4939827a3f<br>SHA256: f48cf620380d7f79c9d8d05702be678101a193a90ef351c28ff300bad2cb1942</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-12-28<br>IPv6: 2024-12-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.918MiB (5.157MB) – 246,132 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ef7e16cf2b6bbbd422ba2a934ef7df<br>SHA1: e1f77a047f5dba3e4ae075464e3761268e84b7fd<br>SHA256: 8dcac1f1779ff26fe9a26934fc72b4c423e9a2f1252d99e1436206cc2bf9f63c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.70MiB (19.61MB) – 284,192 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dce3866a2d21db59b0445d7ab2b5439f<br>SHA1: 62737a727dab8fc70aa7a79a6b203bedd659ee5b<br>SHA256: 2bc4972b559cd83a749cdf69acfcc9f7e1e9b63db44e48dc0e635dc639b29822</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-12-28<br>IPv6: 2024-12-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>167.6MiB (175.8MB) – 2,906,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1918be02cf5e40016993945dcdf9fe2<br>SHA1: 26d9a8404ce0b330647e6b9dec8e0dc1f37c9773<br>SHA256: beead4d706ffee13660a84a3a4fa8d161b26172c66d7d783002d7e5e9a446e97</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>223.8MiB (234.6MB) – 2,165,543 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58aa852f4471f22d59a91349fedddaa7<br>SHA1: 58ed488a65f8f18956e7b32e6e9c4c95283bd843<br>SHA256: eff43d3a7756d1032e8d1b53d8fc159639852e5511ede4f1a0b4456657557bb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-12-27<br>IPv6: 2024-12-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.11MiB (10.60MB) – 506,380 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afd64afb6c0f07ce0a681c26784a42a2<br>SHA1: a7c236e3c9850effc4348103f42d22dbe9276193<br>SHA256: 93231fbadcebaeb4ed587fdaaade3597193a6a93b29374151cc45de8aa87c2d4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.63MiB (33.16MB) – 480,645 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d49c9cf0beb22618ba7bd6c5bb701f2d<br>SHA1: a17d931d90a73f31468f190c1211b51822b36f21<br>SHA256: 87ef4a44f948a3acb900f38f871ae37dfc7a982ddcce848a2227e80b4a5b6d2d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-12-27<br>IPv6: 2024-12-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>158.2MiB (165.9MB) – 3,129,247 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9bf6ee914708d01a683ee291e802c94<br>SHA1: 6fc194d085b24f193d297e49f35a5d26333d9e48<br>SHA256: 2ffd279d04603a4b4dab3c1f35353ae5a9f4355f358637ccce35131567b1a2fb</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>168.1MiB (176.3MB) – 3,129,247 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbf61e7e7923843d244bfdf87e7d52ab<br>SHA1: 891da7baaecddc12c0ba2a8c57a6439a5d01fd92<br>SHA256: 731df9f5d67eb70e672f97e552b0386596397476b55ef1317c8c07c9823019f6</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>157.3MiB (164.9MB) – 3,129,247 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c8544eaf342b345f69c9dc626e3e091<br>SHA1: dfd8d66a1b3b2d6a628e3e7f1135204c405ae315<br>SHA256: 292e6160aa44497e98aa012fb1636b629b06fb0c4e7fe33c4aa68cf1210e3777</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>159.4MiB (167.2MB) – 3,129,247 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e6f0f6aa239df3dcf3483cd008cb56f<br>SHA1: 08ab8a0a30fac9bab6ddfb8468d18046f779d56a<br>SHA256: cfad960bf00f3b29ddce10f82f33a041c352d3b8a1ecfe486fabbdb0834557ec</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>200.5MiB (210.2MB) – 3,129,247 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bed6fba1d3f6de283328e6833168cffe<br>SHA1: 30668f6948c2ea46fb0573ed5a7de495ddfc1034<br>SHA256: 67c89fb67576d2e04ca824081c05414eb19de48ca2d0254f6369e6f22a74846c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>157.3MiB (165.0MB) – 3,129,247 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f701c630465bda029c8e19241d902524<br>SHA1: 85533a87bbdb3d50d4d526e2c29e51a006a18724<br>SHA256: 790697fe6f32d7a9c3f7a4a284f4e43624b61d08356b62f96af4614052efe7ec</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>194.9MiB (204.3MB) – 3,129,247 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2010721f194b1cc54a29798c82bb136b<br>SHA1: c32f92ea8ce9ab5780837f43f5b8576d4dde7e76<br>SHA256: 48e40a37470a494ced79cff39cf04b8deac1f9cfcdf881a6068260cb85d360bc</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>164.1MiB (172.1MB) – 3,129,247 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5e3a0a751829b25977ac7dd59139c2b<br>SHA1: f658a05d576838f168cc4e5f4a85d9d0aa285d13<br>SHA256: 1e388c47ddd4245d9d6c56279372a7b3877b4741ced1dca82a16722d14ad7148</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>161.2MiB (169.0MB) – 1,719,721 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c973d9908163af6cda9cda3d9528c4b5<br>SHA1: 27bace94084c750b018f0298be805d32cfce6e4f<br>SHA256: 336c6380c0b6d86f0027df7d3783dea245af249669f833d0ac9cf669ed07cb2e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>164.8MiB (172.8MB) – 1,719,721 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3172628c10f9cb08937a92a1f369b78a<br>SHA1: 8c2e4c196cf170779d134da68bea10c74ea8e125<br>SHA256: 280ccb395ba1e6acc327b489323f28b0d05a489e4675dd01f399f03ee67ab51c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>159.3MiB (167.1MB) – 1,719,721 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f207a54e8d0aa9939912d1c022dbaa<br>SHA1: dada2213cc959e8aad8688983567d3dd03888a77<br>SHA256: 25c32a4a1c7968638731d0afe798c2ae9984077b87b7ed8a65503d2188d762e1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>159.7MiB (167.5MB) – 1,719,721 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7746e75bf89532b4a9a849e97fcb6fc<br>SHA1: 90043e28e20e2a1f36ec46829e71199456649e76<br>SHA256: c7ff93b42ba27bd6fc231b5ddce245a20b31304b4f30f48b41dcc275e07ce46f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>175.4MiB (183.9MB) – 1,719,721 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc618173dcdd44ff4c35d959424ebc40<br>SHA1: c53d0ec38ec72d7bc197ac16a602da556c155250<br>SHA256: 31fa9f349ada2aa8a0c37361ed116786774ce35396067c50bfed1c35c7d23914</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>159.2MiB (166.9MB) – 1,719,721 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fdad9d1c6ac62ddf78fcb599d5046191<br>SHA1: 96613c259f8820cad000cb12ec7178e5242a1b76<br>SHA256: ad395c1202027562d0dc5630abf39c11c3acd0948f45a74b100ac8c7ee48589d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>176.9MiB (185.4MB) – 1,719,721 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10b71e681e44afad336331b073c75ddb<br>SHA1: 4a8bc6859f9bd17a26c3c2e1daf0ebe8f16b075b<br>SHA256: e50ed65306ff42d1708cbb3594648dc6bf28cdffe34a837f7dd383f054c67167</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>162.7MiB (170.6MB) – 1,719,721 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a522c3a95153da5d19613dcc9efd2f6a<br>SHA1: 5339ffbebf641a856abe6116e148243eebd1b498<br>SHA256: 384dcbb48f5271cf058ff11fc84d1a939bd447d110b2db16cb82b5ca4e1d9fe0</pre></details></small> |


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
