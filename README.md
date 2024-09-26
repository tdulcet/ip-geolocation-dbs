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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-09-26<br>IPv6: 2024-09-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.629MiB (5.903MB) – 281,840 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4e152b20cca847ab02ddb56cfb55e07<br>SHA1: 79e674e56cd0548bb984146e1b71751cb16e8806<br>SHA256: 3d85521893f9161f2d23fee4d136a6550c4111b9f5da8943bea559af47cb7c9f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.98MiB (11.51MB) – 166,840 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 995b285cfdb6b2360292554e7e09b080<br>SHA1: de4c4151ecbe694264a55c687834050f8c24d904<br>SHA256: aaa654d41fbec44c7aa243fd2d2d08fffc011c44f9185cd56134433761e5cb7e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-09-26<br>IPv6: 2024-09-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.168MiB (8.565MB) – 409,055 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bdeebe389c5b5f323ba80d232914e1bd<br>SHA1: 1d08d21ba2f140b683954d7bf0d7d4358b9485e7<br>SHA256: b00ffc0134983e1807d165b902fa56137d581bef2323eeb6f700c87f66daea8b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.763MiB (7.092MB) – 102,896 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d88aa1c77c6c9dfd436da5f32dbb4510<br>SHA1: 23a020e8ec99b89d583e4ba0103f3ebb6a6fecd7<br>SHA256: 653d6b49dcb3c97234fb4b23449478877babd9f1f153af43e7ad9e876156d0ab</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-09-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.79MiB (17.60MB) – 839,790 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70f1285160fb6fc941010ba04349b1c7<br>SHA1: 8515a5ff8c761a046200eb40e90d7e62129bd7bd<br>SHA256: e64d836fbef01a5c78b2d09a83e5431fabcdb549c90c0a7d7a37ff2dc3450c8a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>65.57MiB (68.76MB) – 996,468 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e38d5cbce633703463c6caab457a377b<br>SHA1: 9aef1761f0b712fc2587d071f6c99248be0a0cc4<br>SHA256: 6622866b919e90fd2d9e3752da6ad9f71713d0efd3a24b0c478accbbca26afb1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.026MiB (7.367MB) – 353,071 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcefe7ff67170edca76e960964754e05<br>SHA1: 27baa458e1a83274ab2aeac30e8c9e5fd89a29cf<br>SHA256: 462e24e1a1bb99827d9159c6ca57beed55617951e2ba210ac5d3ff2b406854af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.08MiB (20.01MB) – 290,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ebd3df44971fac41c81afc4e0b8e479<br>SHA1: e374278cdbc7551f55e127136a4623733504aeb5<br>SHA256: 5386c4b7b3b9edde1ed82d40af540593e3564055cf489bb7b99eb47057236d4d</pre></details></small> |
| | | Full Location | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.3MiB (197.5MB) – 3,287,813 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 454e55ae0fc4afbb509099e64b95780a<br>SHA1: 6b88a53921a475e7c1503a9fc3192726c88eee1b<br>SHA256: cd862087cb0a1f5359ee3534aa13b529d8eff5b1c700f8f97a19f0581998096c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>371.3MiB (389.3MB) – 3,603,634 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1073bf4bc29c411e1711e31e0f8593b<br>SHA1: f03eb167bbf14c750a0b060d043ebabe87ed9840<br>SHA256: 9f2c824922dadea859da67d03d96f92bd830c0efee37cf04ed4acf6cac6a1b6f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-09-26<br>IPv6: 2024-09-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.942MiB (5.182MB) – 247,345 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75be5fd9df21ddbc1fdbffc757c5c88e<br>SHA1: 617600a865f99d7027bf00861f55ec2f8fd1574e<br>SHA256: c577e4648304b379620b9b9b1a7b46685fe2b5a3719de872d7565971b4f67dd3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.43MiB (19.32MB) – 280,024 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 529fb8698467082348344b270ff7cc32<br>SHA1: 5e3253c77897a6f1833518163500372c619862fd<br>SHA256: 9289075bcac9e9a959f8009c5eae593e88bd3925aa371f097f4b54c6bd5bb9ed</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-09-26<br>IPv6: 2024-09-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.5MiB (182.0MB) – 3,005,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50ec8daacd5cafd5b2765884871d9b09<br>SHA1: 889e86b248ea9a4741e8399a0e67d17ad637cc38<br>SHA256: 5909cda69b8afb1da39fd44d4e35827b08820512a824be3f438aeb08bfbe1c67</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>210.3MiB (220.5MB) – 2,035,716 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 221fa2afd3b2e737797b4dd7b49d116b<br>SHA1: 42a7d10f6dcb092f867344cabddb6856eda16b19<br>SHA256: 138f90080a7371e27aaa532721e6449e41511cbca7244a5e31fdcc4081b48129</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-09-24<br>IPv6: 2024-09-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.767MiB (10.24MB) – 489,285 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a38f3ba67c2266fc8209d19474c170e7<br>SHA1: 98ba0df08f08250c425b01830b5475ee8674b814<br>SHA256: 67898b896858e21abee21b826e08049a0804314ea82abda15765b12ea0630911</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.22MiB (31.69MB) – 459,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59268ab2077db659dd3e8db5b168d883<br>SHA1: a0360c091cd1eb01d98c6c97327cb3054881e29a<br>SHA256: 18242d814c141a809ff06044e3becd7dfcee18992aa285ef9af6a6ed7da3cada</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-09-24<br>IPv6: 2024-09-24 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.6MiB (179.9MB) – 3,386,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d8b218f5f4b8601df0c0351fc4a0772<br>SHA1: b592349ba3aeff0b7f6f3c3e667576251c60cee6<br>SHA256: 3c7d1a0646c5c64c068d8faba32f7b30a07015a4cb259c2b29d8873940374867</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.4MiB (192.3MB) – 3,386,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70f8065748b184e704736cccf9df656e<br>SHA1: 75e81f041064b0df27830d6458071a8d4b689868<br>SHA256: 5ade702dc4c5e4c2814b8f7071c8d87e72514cbd91fbae74ad26c51a85312ff5</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.5MiB (178.8MB) – 3,386,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4aba0913f33181ee57417595e0473f67<br>SHA1: 9e67bab92ecc58f0c94a91db293ce0f135b5ec71<br>SHA256: 849ed9a8ad95f1b93ceb8e6b7c01d23c37aca175e0f2c5ef455b86ace6fdedf6</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.2MiB (181.6MB) – 3,386,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efbb0bb7e525c30c1b5a854384951a23<br>SHA1: fc41b8eedb797dabea8746a35b7f4ba83ec0f52b<br>SHA256: d4e46a2915842fbe0ea3c9cf7f7efa855f6ce2089b08a116f2646d56091fecec</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.6MiB (228.2MB) – 3,386,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9b1c7728e9da95fc530bd7f43331f02<br>SHA1: fbf074d7f0b157e58f110f1f35b86d07be6e1b93<br>SHA256: 8aa450a2627531678e14105ad48ff4a86e4965554a4935b8674c86e9213b7bc7</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.4MiB (178.7MB) – 3,386,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7856cdf1e854da9db0744b1902f006df<br>SHA1: 4c86288a7978b6a112541fbb2d3e5110e6827a6c<br>SHA256: 5048dcf2c8da36f5df47cd7842832dc05eab05fadd3ca4fa35023bb480bee9f6</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.4MiB (221.6MB) – 3,386,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c4af83c0356da0b3d4c059b27e349f2<br>SHA1: b7508dfa2930bf9da71f01e5f995f37a09ab48e8<br>SHA256: ba13e251dfba074fe8e591d365341ad00bc14b6af8f373a6b390de805eef28d6</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.7MiB (186.3MB) – 3,386,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16fa7edbeeee9c81459524bd128516ef<br>SHA1: dc1322ac8137d5b6fceed2acbadca4d722a4b643<br>SHA256: abb639984ae40268b4cc20b0a833631e9dd53a09ffbd95ac274a6422338db549</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>157.0MiB (164.6MB) – 1,649,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 404564db2be3c0fedca7c1f48ebc7134<br>SHA1: c301da826cd90afd0d85d3cbbc289c14319853b6<br>SHA256: f83075948da1877c9997efb227c8fc16b4173ea81b068c31bdd4d7384c8319bf</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>159.7MiB (167.5MB) – 1,649,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bdc0d090a85c67e670caa4c27bcce5bd<br>SHA1: 8518181cd3a852c83b43c9d84bdfa0ed6b6dd1f0<br>SHA256: 43663b0eae11e5042634036c141b1b39f4f7fa6e0fef6ffd861187c70e4c893b</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>153.7MiB (161.1MB) – 1,649,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 560b3449ddfbfe4464c3501539bc7518<br>SHA1: 0e09bfe104c4fee4974cfce3b3f8b5193e9ae32f<br>SHA256: 75900d2ef43e89b4d16e91c15b4f5787b685e298981c5f397d4d4ed062998fb1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>153.8MiB (161.2MB) – 1,649,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79db9b7434067459b2dfc559b017ecd2<br>SHA1: d7d9159b32b5f1e4047d1445b93992e9789cd8fe<br>SHA256: 822479be0ec4007aa7d8289914d32e25019d7a37fa43d770751a4b45d3b0e3b9</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>169.8MiB (178.0MB) – 1,649,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e228462c06d41f0abcfe23f3223bd7a7<br>SHA1: 3ba86f25622cc4d676cd728e58bc0159b797d1f6<br>SHA256: 7c2ad3e9bae478bfe189a7fb26f5de6688dbaf13f802c7f27d2c0477a8406cae</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>153.5MiB (161.0MB) – 1,649,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6415048fb8bd500938b4a78c3b833f7<br>SHA1: c48dac40d3d2a19cc84c4c0ea9c672820453e5af<br>SHA256: ab2eb9726d82f9b2777fa08a5e978fa27c080de99d5b8dedd7aae4ee6bf33ffa</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>172.9MiB (181.3MB) – 1,649,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02b238e5e698fe0149bf7977cfd34a18<br>SHA1: 1c510930a950ccad345e25800d6efc0e1ad7b886<br>SHA256: 8599e7932527c141f1917d284a8be4a641f78cc8c53b03079ba3ec2f59eae990</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>157.7MiB (165.3MB) – 1,649,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c33960b269bb016ae6c89c4dadb8dec1<br>SHA1: bc3603dae6ee8d0ef36c7d298de113dafe37e958<br>SHA256: 447587beab7a5a069106c983b4bc9ca88542c1b323bdb0c32b9aece21a6d372c</pre></details></small> |


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
