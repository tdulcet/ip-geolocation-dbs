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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-12-22<br>IPv6: 2024-12-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.909MiB (6.196MB) – 295,873 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aacb34506ac66cb19126d6c9b8fb4c60<br>SHA1: fd09911e5f18c5f6342a106c609b4669c3a286e5<br>SHA256: 76fba21292098136c6511fb8a54b6ffa9e55dad56118b7d79f2c183d21e94f4a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.63MiB (12.20MB) – 176,812 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38f47ad90810c0cb7314349b0ea26d67<br>SHA1: e160a5fffa28ed44590442a749f6f75280c13f73<br>SHA256: 351683aa0394206f3dcd33d005e0b0aa089d673cd728f8566e0a384d14d68abc</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-12-22<br>IPv6: 2024-12-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.265MiB (8.667MB) – 413,902 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 960ba97174cc256ffd8550ec4cc0afe8<br>SHA1: 68e80e08e182ebf7915d204576d836a0f9878811<br>SHA256: 96ab5ee7d28c43d0f133e8923af6bbb24eb65254e9f8c47070d798d68ea7bb69</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.953MiB (7.291MB) – 105,774 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28dda109ea89452ed0f4d71f614a28f9<br>SHA1: be38c905bba0fa034582262e8967a6167deed940<br>SHA256: 6d4c90fc205f5b436074834271e82ba2f0861b5fbe6e54bd37b41681d68afa0e</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-12-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.13MiB (13.77MB) – 657,359 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d6bc952b76ddf389b286831ebc61e63<br>SHA1: e3f58dc43783ca0bb9e1264d3865f90e002d0238<br>SHA256: 7d14ea0836b6fa9fa32ae9a420ce39e839de4f8ffa4058a3d3da7fea92747b1f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.17MiB (93.51MB) – 1,355,159 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94a712dc11972550f93117398912f122<br>SHA1: 808b2a371308f244fc261beb8e3075099f407f2e<br>SHA256: de3e5c3495872dd0937b92d038f98228a44c0c52c8b2053c97cd3f0182c7fdd9</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.156MiB (7.503MB) – 359,168 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4fa1848a017a51ce167e1b45ef180e0<br>SHA1: d025902fca69db441cbc83871eb99ffd4b92c75e<br>SHA256: f02df1b7ee71bf749e1e43de462a3f6c365d9ed6e72e1d5c6faa86f25acb568c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.24MiB (17.03MB) – 246,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fee62599a38c614b43a277a08de845d7<br>SHA1: f6f5eddc6f61250f0fef53e42d76288b85a9971b<br>SHA256: 258dacce2a418e7297db10bd484df83410a61ac130bc1a5820b6fb0c0c58cb70</pre></details></small> |
| | | Full Location | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.6MiB (199.9MB) – 3,333,541 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f97a8dfa3d2efa2169aa49e5067082d<br>SHA1: 69f6046d5bebaecbd09f512a07ad0279a8bad58f<br>SHA256: 193177f00477af08b776744f0aa5ea8ffe08fe54bbe785733206c3c6f5ea0b02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>381.5MiB (400.0MB) – 3,700,914 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60c57063e8597965c85a15738ce2271e<br>SHA1: e6cfa1c20dff9df4b9dedd101304ed4939827a3f<br>SHA256: f48cf620380d7f79c9d8d05702be678101a193a90ef351c28ff300bad2cb1942</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-12-22<br>IPv6: 2024-12-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.918MiB (5.157MB) – 246,132 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ef7e16cf2b6bbbd422ba2a934ef7df<br>SHA1: e1f77a047f5dba3e4ae075464e3761268e84b7fd<br>SHA256: 8dcac1f1779ff26fe9a26934fc72b4c423e9a2f1252d99e1436206cc2bf9f63c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.70MiB (19.61MB) – 284,192 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dce3866a2d21db59b0445d7ab2b5439f<br>SHA1: 62737a727dab8fc70aa7a79a6b203bedd659ee5b<br>SHA256: 2bc4972b559cd83a749cdf69acfcc9f7e1e9b63db44e48dc0e635dc639b29822</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-12-22<br>IPv6: 2024-12-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>167.6MiB (175.8MB) – 2,906,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1918be02cf5e40016993945dcdf9fe2<br>SHA1: 26d9a8404ce0b330647e6b9dec8e0dc1f37c9773<br>SHA256: beead4d706ffee13660a84a3a4fa8d161b26172c66d7d783002d7e5e9a446e97</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>223.8MiB (234.6MB) – 2,165,543 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58aa852f4471f22d59a91349fedddaa7<br>SHA1: 58ed488a65f8f18956e7b32e6e9c4c95283bd843<br>SHA256: eff43d3a7756d1032e8d1b53d8fc159639852e5511ede4f1a0b4456657557bb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-12-20<br>IPv6: 2024-12-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.10MiB (10.59MB) – 505,749 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3d5ddd625b8025416ce1ddbd613da44<br>SHA1: ea82d11688c968ecf259be5bedd6290165cf282a<br>SHA256: c7d2f6131c8d87f15cfb6c4e6460c3930ebfb6d2a9bc5b735d2b3185f4d8dc04</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.58MiB (33.12MB) – 479,955 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17418040b90360641f0006ea17cb95ed<br>SHA1: f6a984b45a4f4ac8123daf52d278a8ed1071a813<br>SHA256: f0d4388f7abf09401c8c3d81b3d0f32f4773a73ad51256eefba175c1d880ab99</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-12-20<br>IPv6: 2024-12-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>158.2MiB (165.8MB) – 3,128,069 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5b76cbfe10a12039ec4e10747d93537<br>SHA1: 5719b88ef5800e80ba2c713c28ac968cfd0fc7ab<br>SHA256: 8c04629ab3a0ad5978a623571c6c82636b61e444d1c484b4077ccaa0059f9dd2</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>168.1MiB (176.2MB) – 3,128,069 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6713f07bf9618d3881b5209db1755199<br>SHA1: 0d21000ec22b9ed0de81befa3cac40ab622ec6b8<br>SHA256: dc0e3fbf8a9401455d43ac886f9edf0b31715922f91f863948d14d02db299c35</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>157.3MiB (164.9MB) – 3,128,069 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37bee5e51a3a6d13db9d6aad8e1ba647<br>SHA1: b286c8a631c31e8371152de4478403403353be2c<br>SHA256: 7a5d56165eb9e4d1351aecd28fc9867bf56b63cf693714a536c438a1c18882e9</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>159.4MiB (167.2MB) – 3,128,069 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 043050f7c63b09dac8f7276968b38867<br>SHA1: 8ebf8544c35369895bac485afa656f3a01267504<br>SHA256: 1e4bcb168c239f0aed98e6527086dbd8433a4e7983b747b946092ff61d5436d3</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>200.5MiB (210.3MB) – 3,128,069 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b79fd258366e954a695ca842569fcfb<br>SHA1: 82daa4e1e145790f7005ce0c323254a27324ac15<br>SHA256: 417063f02c558ec8178dbe719b7a4d842357cd49ce590ab8258c4f2dc83b6fe9</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>157.3MiB (165.0MB) – 3,128,069 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 292db1462f82b0112799772b29990a89<br>SHA1: 36605fdfeed6fb2b567242e48367f0a9210d7631<br>SHA256: af3588826f380b278abdaa339ba1a4e5092396d7fac399b437bce12eacd20d75</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>194.9MiB (204.3MB) – 3,128,069 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f82d47ae03baac99df66c66736407c1<br>SHA1: 39e91c1bf71aeaaa38bce273262c50185fc82113<br>SHA256: e2d6765efb5cc7626f33f2dfe5daa6649258754a4bb94d4bab7057553a19f7ff</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>164.1MiB (172.1MB) – 3,128,069 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f63228060caf4889ee397f27988d70fd<br>SHA1: 0806bf02074b7499db1c87e51cc587886ed83d30<br>SHA256: 3322e327d6276df381a1d312ed40e293c6ffd3079b002eee0a754783ffa52f8a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>161.2MiB (169.0MB) – 1,718,476 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 838adc88932c7ba4e9f160742a177612<br>SHA1: 608c85f08fd5662ed2c895dbebd8a8311a99bec0<br>SHA256: 0ba8ea223301e18ae08fd7fb6c183dc95bef3c09aa5de6929843320db5e28e66</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>164.8MiB (172.8MB) – 1,718,476 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05aaf19215b8568abfbfefeb3ccd882e<br>SHA1: 21f83f3c3d88e1a3ef990b9aba038b08dcea3ffe<br>SHA256: a8627e861a0f443a9b714a278fb73b95f5e30c3aa6c20814ea0d6a2f76fef201</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>159.3MiB (167.0MB) – 1,718,476 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44a63dd804bf3aa9810fe568a357f591<br>SHA1: fbc6fcfd81973c72ccbf3bc94f7504fc8abdec3f<br>SHA256: bdbdf9094b9b71c404801f035ace9d344241f8b45c54f56ee0b60dec4457eeef</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>159.7MiB (167.4MB) – 1,718,476 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 366718c19905aa332b592360eea9b945<br>SHA1: ec9b801afd64511045f40340e3f85c9fe8d76f03<br>SHA256: 51117197f86c20d0644f74a74c91896f29e60c53f39c72755fdbd37a3b3d71e6</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>175.4MiB (183.9MB) – 1,718,476 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c37c49f9f956f469c739e7ac17457192<br>SHA1: c6e6d5c5bb2cf6ec8658d7ff32c48962dea89cfb<br>SHA256: 31c0511971912b90243bfe03a6e918e68f2bbc21250adb901bed0c8f6298477d</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>159.1MiB (166.9MB) – 1,718,476 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e75f6c048068e8c4b09eb2fea891b0c9<br>SHA1: 6c51be01b20a9ec975fcf5d030ed36b75a451883<br>SHA256: 811db92909212379617eb69d6cad10a691d82c1654f7983d9009b077c64756ed</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>176.8MiB (185.4MB) – 1,718,476 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b4bc79f471462d93eb3d63fc8efc937<br>SHA1: a1f1c228abe0b16a414e57e20b196f30de97ddf6<br>SHA256: 38a70955e01ede5b12062b254e6adc883304ed0b521c447c1c4686f2d125c1e5</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>162.6MiB (170.5MB) – 1,718,476 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cbe6d5eebf28ee8ac345dccc5b174b9<br>SHA1: f7a7631a517e77c42f4e55f7c0526312452fed93<br>SHA256: cacd78ed17d3deab2cefe77f369268f1d97d6e859d2763157a11917295d86c1f</pre></details></small> |


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
