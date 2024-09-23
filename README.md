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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-09-23<br>IPv6: 2024-09-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.626MiB (5.899MB) – 281,658 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 441f328a74c82805dd96afa6a92f4a78<br>SHA1: dfde9e32350d7bb17d61cecf651a6579edd997fd<br>SHA256: 0fdad6cb0259b05aafa8f45294a98a1b96496d3bedaf886f5e2e2968b2c81341</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.97MiB (11.50MB) – 166,654 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73744ec3a7118f4129700d884db0f5f5<br>SHA1: f6cf4ace59f8a3f89f5a027f3be9ce9fa596e29e<br>SHA256: cdbd0c6139fd82c12ceb94f8d04a9ad5a66228d45d408bd9c7950d778a10bb76</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-09-23<br>IPv6: 2024-09-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.163MiB (8.560MB) – 408,809 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96612cb339feedba54841b78967358af<br>SHA1: afc78f854d88344bb41ec6cdc5faf519756051f5<br>SHA256: fea34eb053abe31f842f1f1fd4ff90e34f4d69edb52c17ac5d721ca3ee83425b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.760MiB (7.088MB) – 102,838 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d23d4be30ac85500811daaa6915f77d<br>SHA1: 488310127b989876e1aa2702e9eda5a623e3110c<br>SHA256: 41b3f4d353b7e0293b20a05777ffc0a97ca3e9674cf3aeea6f796337d8d84411</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-09-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.85MiB (17.67MB) – 842,968 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 168c0d89996d0391e0170e8d7e3a13ee<br>SHA1: 2a16eb85d34966d686ad0e6d12b0057dd215a534<br>SHA256: 31766901700a7333855681091586d389d1315bb8792fadb2777bdf9eacf31fe3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>66.08MiB (69.29MB) – 1,004,147 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a55fa3bbbd3cc4a28f81b75948d36ef6<br>SHA1: a5d738aced9e38bcf15eaadb3d9ba9a5305ab6c5<br>SHA256: 33cb54c5532d5187b2e8b5661ed14397d7b1de3d50eb539b14ac39efe5be2a63</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.026MiB (7.367MB) – 353,071 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcefe7ff67170edca76e960964754e05<br>SHA1: 27baa458e1a83274ab2aeac30e8c9e5fd89a29cf<br>SHA256: 462e24e1a1bb99827d9159c6ca57beed55617951e2ba210ac5d3ff2b406854af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.08MiB (20.01MB) – 290,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ebd3df44971fac41c81afc4e0b8e479<br>SHA1: e374278cdbc7551f55e127136a4623733504aeb5<br>SHA256: 5386c4b7b3b9edde1ed82d40af540593e3564055cf489bb7b99eb47057236d4d</pre></details></small> |
| | | Full Location | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.3MiB (197.5MB) – 3,287,813 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 454e55ae0fc4afbb509099e64b95780a<br>SHA1: 6b88a53921a475e7c1503a9fc3192726c88eee1b<br>SHA256: cd862087cb0a1f5359ee3534aa13b529d8eff5b1c700f8f97a19f0581998096c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>371.3MiB (389.3MB) – 3,603,634 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1073bf4bc29c411e1711e31e0f8593b<br>SHA1: f03eb167bbf14c750a0b060d043ebabe87ed9840<br>SHA256: 9f2c824922dadea859da67d03d96f92bd830c0efee37cf04ed4acf6cac6a1b6f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-09-23<br>IPv6: 2024-09-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.942MiB (5.182MB) – 247,345 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75be5fd9df21ddbc1fdbffc757c5c88e<br>SHA1: 617600a865f99d7027bf00861f55ec2f8fd1574e<br>SHA256: c577e4648304b379620b9b9b1a7b46685fe2b5a3719de872d7565971b4f67dd3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.43MiB (19.32MB) – 280,024 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 529fb8698467082348344b270ff7cc32<br>SHA1: 5e3253c77897a6f1833518163500372c619862fd<br>SHA256: 9289075bcac9e9a959f8009c5eae593e88bd3925aa371f097f4b54c6bd5bb9ed</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-09-23<br>IPv6: 2024-09-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.5MiB (182.0MB) – 3,005,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50ec8daacd5cafd5b2765884871d9b09<br>SHA1: 889e86b248ea9a4741e8399a0e67d17ad637cc38<br>SHA256: 5909cda69b8afb1da39fd44d4e35827b08820512a824be3f438aeb08bfbe1c67</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>210.3MiB (220.5MB) – 2,035,716 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 221fa2afd3b2e737797b4dd7b49d116b<br>SHA1: 42a7d10f6dcb092f867344cabddb6856eda16b19<br>SHA256: 138f90080a7371e27aaa532721e6449e41511cbca7244a5e31fdcc4081b48129</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-09-21<br>IPv6: 2024-09-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.772MiB (10.25MB) – 489,528 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43df367fb71494acdcd9fcd2c410fd7c<br>SHA1: c9cb726ed9e250fffdf833dc793ef00b015848d6<br>SHA256: 717c36b0e86afee0599f31f94aa6641af6a6acadedc7ea54d62249bba98c7060</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.22MiB (31.68MB) – 459,204 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fe9483889b47af043a7ec98beb3902a<br>SHA1: 0034a9d5ae3bb338fcfacb75093b000e11bc7867<br>SHA256: f249968d0e6bdb7aafd12cc73198e45d988ff6e555774bf76a0006daeea891b9</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-09-21<br>IPv6: 2024-09-21 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.6MiB (179.9MB) – 3,387,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91ee4abe40c1e941745cb022a6212e02<br>SHA1: a18048350c4d2672328bf4d71cb796af63dd0936<br>SHA256: 91e450e95b23b529b03fc0ce2aa3b94f7b8d50cd81088a491045622f601f2247</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.4MiB (192.3MB) – 3,387,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78872f903cdee256764bde742674516b<br>SHA1: 9909900c2e93adaa18292b9aa2be98a01deb036d<br>SHA256: 1aca1789c37bddfadb2e193d3dd88ec051e40a81cb20993a6d36bc801d53e99c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.5MiB (178.8MB) – 3,387,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a700e06c0d1c094db8a8de0cd3c1b42<br>SHA1: b4cfa798700f04d6f9e4fb8d29c356c97db26e7b<br>SHA256: 5624bee6ebde58e45ed759c462e0622f31bf39c7c44cdb812ba6ab2c8d74b834</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.2MiB (181.7MB) – 3,387,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18f2031b53e05e81e98fd7ccfd7df5f3<br>SHA1: 671e8d23b6b35520c68cf192b3635b271c31a27e<br>SHA256: a21edabf6785e93fd5fe8768280ebf2893c52cc485ec51aa538566e0c03beb63</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.7MiB (228.3MB) – 3,387,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8a19971a9cff0d70c2df6db799709ed<br>SHA1: ef329af99124d2b8fec36db5551c588b163e44c8<br>SHA256: 1900169807f28ca50a81feeec03293488f1b582d52d896c3583a10ec9dcb5f1b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.4MiB (178.7MB) – 3,387,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6884014e373cd06a6712890de6f6096<br>SHA1: 559221ca3d2baa34b550d2775f96821a3fc913eb<br>SHA256: a56d86e6e88a855ccb5014e181dd0874024c9595f21eff8939befdfdfe29a75e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.4MiB (221.7MB) – 3,387,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 393410e614a85b03f2f36df6f80f34f3<br>SHA1: 5b3940a1d715f9245171c0d11ecbfc52d36c487d<br>SHA256: a443c1988fb4945ee9a1f76b04c39ca60fafb69727b25ab44f76de631d2ca266</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.8MiB (186.4MB) – 3,387,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52a1bd338f9f9e5e9bc3634d7fc78762<br>SHA1: 0658a8c6fa0194645bee9a1ba4edf68701065cf7<br>SHA256: cf13a3bc6c6684bb6e7676f627ab038f17b92e0d6141ecf696b8e50b8a801ef5</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>156.3MiB (163.9MB) – 1,643,799 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93236d72f94606f616345062b2bed8ea<br>SHA1: 3dfe0985744068eb013b1cab47d456c790206bd0<br>SHA256: 0565171880239b39b1893b9092e123b590cfa746a99f474013be82ba50788b65</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>159.0MiB (166.7MB) – 1,643,799 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbab6e92b150c7c97dc12aea3a0a15e5<br>SHA1: 84a60b016e39fbba39fd6293c86022240e23916d<br>SHA256: 7d48d09392eb7f9f8210d8a323f213ace53c9d90868a426fffea1d5dc8e7ba65</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>152.9MiB (160.4MB) – 1,643,799 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d67dff043ebb9fde54fc38738adce18<br>SHA1: 72be4eec49b96e379c6b8fc2e7c7df2c8f769cbb<br>SHA256: 140115efe4ede60be78b1bea119f3552f7dbc58d287f4447e2b92307232b369f</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>153.1MiB (160.5MB) – 1,643,799 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f30948b9997f939a44bee0440d1c407<br>SHA1: 5c0187a36dd1b0794373a3ed120dcd5dadee8fa0<br>SHA256: 7673069157b1a9f5cd9ef101ac136aeba217b5746d311f3109c139e7aa3b7aa5</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>168.8MiB (177.0MB) – 1,643,799 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b257f014d7cf6c51f0304d15d43a91a<br>SHA1: 8df0cefc84f9da221c08e1e61cbc4a7061989452<br>SHA256: 9e5305caee04e363847bf3695ad8e7f7f23f3d4eb725f0b9ee8c2878a5e2578a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>152.9MiB (160.3MB) – 1,643,799 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17843e989f3cd5207fe21e3160c1f334<br>SHA1: cce7dcef099c3e933d78f3bcb018e077d719626f<br>SHA256: cbdd18745408aa277b8001f73c5da763a16064bbaddc78863ddcdd7515f37c91</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>171.9MiB (180.3MB) – 1,643,799 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d5fed2a6829be86060d6eb8ccfdba2<br>SHA1: f40eff4fbcaf84e65cc079919892866f41a04925<br>SHA256: b0a5c3e40c7b0f8a0c0c65ce1072da52d1a5495db5485f6008fa09b6bf2358bb</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>157.0MiB (164.7MB) – 1,643,799 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5603da4fa1d520d11ced4de79d44706<br>SHA1: 93325977ab3cddf13d74f61d13ea61cc1f6a9dd5<br>SHA256: eb21206137eb52e37c114bd6847ac23c31619f1d76cc2156e76ae0501cbc06fc</pre></details></small> |


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
