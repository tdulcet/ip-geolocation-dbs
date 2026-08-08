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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-08-07<br>IPv6: 2026-08-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.409 MiB (5.672 MB) – 270,718 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bd8d50a28a4e824159817e04dcc139e<br>SHA1: fc56afc5cb4e4025510c10c381f21e13f6ed3ee5<br>SHA256: 4db41eb0a28a229565ea799c26e5164a5a3e03f4444f60f42f8e8a283d8a6678</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.75 MiB (17.56 MB) – 254,506 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e8d253e700ae83538694c83a7d6a842<br>SHA1: c98ca2bace6f049b710a7f6c03ff470dace8be22<br>SHA256: 81a7aa5ba7bd8b31ae0fcad986a63b417c113e9bc5ab2fa12a5d5ef961d4b170</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-08-08<br>IPv6: 2026-08-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.039 MiB (9.478 MB) – 452,591 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c997ea4838868d3d9dd405b1be82d820<br>SHA1: ce49e325642cca6911a82ab3b072c6ebeffb9d63<br>SHA256: f9f459c50c0ab9a80e1ad215efc3797477cfc5eddd72e94695aec9a6d9421459</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.992 MiB (8.381 MB) – 121,574 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f8d66d67801fcfeb3dff711591c6681<br>SHA1: 854824c4d9b0e49d19ba27717a37771540490c9d<br>SHA256: 37d4133bf6dec1c2e7c2cc05b53cfe224aed6858c341ecd16e7b4f4c7433fb98</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-08-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.19 MiB (12.79 MB) – 610,547 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9dd44efb59f32b4daa144e40bf72398<br>SHA1: d651c172e3554952e7a65d60b427260f86e118a1<br>SHA256: a9821b78a0d53307b78b3ffba7d0a20c3ac56f5c55728419e829a7ecb489d235</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>45.51 MiB (47.72 MB) – 691,640 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83d5d030a68b40fd0122808ef6c011b1<br>SHA1: 770c87c2edd7fca7accab869d0bce0234f2783e9<br>SHA256: 1821b7bf5d49ac47a797a84941e940dfecac969d36245f1ead5769aef1c168a4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.149 MiB (7.496 MB) – 358,140 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d3e21d2da14fe2fa0da1db2f6424311<br>SHA1: f274f58aadcfa3311603218b88e8b24a01671e36<br>SHA256: f62294be209c966f38eb82e27717bc64116462241210756e85c31429048d1f96</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.92 MiB (24.03 MB) – 348,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60cc96dd0eef36fef003b9981e7aa19c<br>SHA1: 077fc11bdf3b1a16ed5a8e22cb9889e86b007cf5<br>SHA256: da4f32fc9e285ea393eb3d4fec4fb4a153874623b14fc77373e8f448758ac135</pre></details></small> |
| | | Full Location | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>208.4 MiB (218.6 MB) – 3,652,137 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68a79460a812a271884a0a50858ee1f8<br>SHA1: e1cb26165f0fc2b394c3f08d99642d1e5a3e653e<br>SHA256: f40963b044ff4637dff7dd3608244f6e065cc97e9bb7262d5fea4abeed6cf026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>440.2 MiB (461.6 MB) – 4,274,498 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e9801b97694446ef740a7093d24488<br>SHA1: c8e28d1130d3667d5b313b6e468c5d9d69ffb027<br>SHA256: 88971b264e462d0a2d37d85f793d5e488192b4d883a1ad0142a7c28d9a60af96</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.729 MiB (6.007 MB) – 286,747 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ce5cc1653ddb65db06474bab749714a<br>SHA1: 4cc40ea81eba37e4bdc9ce61fe9ce058d0c49372<br>SHA256: d3b805b3c0b083f2ac8b16100752f8ea3eeb8e224cf00f594602330d36cefcb4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.35 MiB (23.43 MB) – 339,594 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 518560be8d49e16a3856c31b0d0bd875<br>SHA1: b1f9595b2778075c3ff384176d6845d15decf465<br>SHA256: 5d25d7d5e32cc9f7b89b03e674eb90f100272a7f4bcd26c78e8a2b2c41efb36b</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.3 MiB (178.6 MB) – 2,947,098 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b12349e01828d4a4bac50e8c858fd50<br>SHA1: e99752a712b42043ecd9c65d3e9651264ae608de<br>SHA256: 3d436dcbd07ba02c6c6fac1fe6d1baa7bca22dd26ec4bd68d3029810ffe0e936</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>299.1 MiB (313.6 MB) – 2,898,359 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddbe75f08ad96059705bbdd5423bfa36<br>SHA1: abe287e78fb8e2391d170e4400975486e52fac90<br>SHA256: eef9c134b1787ced9b9492f2d3cf0bd3e4f7ddc7f71199e6c54374d9513c5083</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-08-07<br>IPv6: 2026-08-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.25 MiB (11.80 MB) – 563,396 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 314541faa68ec233007acf74ee9b1056<br>SHA1: bf2bfe70edd1c386e196438cc7a7dafdc5929356<br>SHA256: 52a80b06f1567d68cae5c585c5d71bd46edd82c970d74065baa7cc82c52a59d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>35.55 MiB (37.27 MB) – 540,211 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0b2e7ddc37726c43c01243a6822ccf3<br>SHA1: c7821fd9f85608b07a23a18c25d9435a2a9c709a<br>SHA256: a35e8c97642f71afeea600c34756db09bf2db34ed8cbba7d6b406b522a32f5ea</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-08-07<br>IPv6: 2026-08-07 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>192.7 MiB (202.1 MB) – 3,753,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe9fc6006b79ebcf70969459d23b9f6c<br>SHA1: 6e7a361f67a0a9cf963552b7886b00ab07f26ec1<br>SHA256: 5e8b01a24cd97d75ed14059ef95a2038412b2b433c681f026fa04f1d1b0867b1</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>201.7 MiB (211.5 MB) – 3,753,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a03cc4282758e5274636e70b50353fb9<br>SHA1: 0a2bc1df94b078ac88c4349b90e0b1df5b217372<br>SHA256: 91251a8ecbdbb0bf8f243bce1c02fd5dbd25b4bfe9770d582f7a4ef5da004668</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>191.9 MiB (201.2 MB) – 3,753,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0bec0551739964614f7a336d59ecf4fb<br>SHA1: b97395d551869bc199c1ce9256e5584b99b97dbd<br>SHA256: 0dff0a97f6169ac1d0f40c09fdf54d80bdbb65512e5ffdfaa1b31e7b1e3a13e5</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>193.6 MiB (203.0 MB) – 3,753,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38f3275e1c7a6db0a845f56e6ec79389<br>SHA1: 721106d6d0d1bca77611d3f1e2348d89b8f6be61<br>SHA256: e0618041916c486ec34651c903ba10e770f8bb37e11ad5cac076df7ffbb069e9</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.0 MiB (255.9 MB) – 3,753,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80f4e9369668ff46dd22e47170dac8a1<br>SHA1: 1ea24b5418b601fcfeb2b95cac4a9e99140ae83e<br>SHA256: 5970b57a76e868547eb7b4edc71a8e532633c93e3601654ba6441553c88c139f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.1 MiB (200.4 MB) – 3,753,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3e57d73f1521c35af8782f3a62b4bf4<br>SHA1: 8f8324a7d6e0dff9ea8c0ae7c1e4fa8d833002eb<br>SHA256: e414f6388f4d25ee9fa8f01eef7a490a9796000dc225e0deb8a9fe566014ca7b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.0 MiB (245.3 MB) – 3,753,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ba24f8133ef9f14d6ff47d065153c1e<br>SHA1: 2a1a8a369c9a66db8dfb845f41179b6fc84e7227<br>SHA256: 4ce24f594b3f66a6d4e7026f0eca2c0fb65b9d34dbcd10259d198b5ab52bf88f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 3,753,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02da9e4a3bc821ecfe6f9fabf4aa0f09<br>SHA1: 2a1618cffd263340807e0642f1217523509132a5<br>SHA256: dba5aa5ca6941aed5113f5b235985d534b9b2aa7a5c32bde64ab1f3ac061d449</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>197.0 MiB (206.6 MB) – 2,063,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d590f60c32cdb2312834132181f2d34d<br>SHA1: 9a4ba63f91cfa5ed544812e648e0d196b086cc3f<br>SHA256: 98753bbb86f3145a0bf9280435e24bc5f06028474a86fde1cc3748d70f11802d</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>200.2 MiB (209.9 MB) – 2,063,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fe6f61a8a3c17e0e342757e694506bf<br>SHA1: 209cc36534a5d0ebe16b4fe5f4d28097e653ce3a<br>SHA256: 2346dc8fd1b3f9562f5d7dceb3412a388333f317d88620a7bfbb70f401b14ba5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>194.5 MiB (203.9 MB) – 2,063,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d79612a9b143dcdfc89c66cd6fad2a6b<br>SHA1: aebe7b47445a3122d10a5f6c4233ea6ac3bfbc26<br>SHA256: 96dc8e1de1c2b4d79a7fb5a8f0cc04af45bc504d5d21b01794bab03217ebcb1b</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>195.0 MiB (204.5 MB) – 2,063,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9bb79b4b4204b45cd6d827eb22e1ff6<br>SHA1: 27900491733cd5a66f9d701000cc0f2766212412<br>SHA256: 599b693bb2963362b5ff4cce21fdd0dc95fc540e3a1f73ac9f9e623637e95375</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>217.0 MiB (227.5 MB) – 2,063,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 745351fee843e492ff51ec5cea118601<br>SHA1: 033a34f18e71f7a3c7dec9bd06ddd3fe8e5656a9<br>SHA256: 78ea8abc317ff061f222a0eaf73db322fd24e271583e7aaaf7f32492693050d0</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>194.2 MiB (203.7 MB) – 2,063,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d86638d564b31d7543c677497d8d34f<br>SHA1: 96effc17b2aec9cb651fcc999dccb3c223fb0ebd<br>SHA256: 72fa5bab5b007137932566c975474fbb2fb8a02d5a4656f0658982836ae4585c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>215.5 MiB (225.9 MB) – 2,063,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c824126de2b3125df42e74a0e8a49be2<br>SHA1: b1bf98321e93b1c81fad9ca92a5c50437af543d0<br>SHA256: f866d9057251c5c68f1e8c45d197e2dbd513746fe83b0f3b351fa37b1b8fe723</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>197.2 MiB (206.7 MB) – 2,063,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f88abc1b65e3fd354834c21a32e04ba<br>SHA1: fedcc2850e28ecf142588b2a05d6c9bdb29f923e<br>SHA256: 5ed99e116478841ca0b721beae227b5cf438b9af071e4ffd6b5c09c58cc148b1</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
