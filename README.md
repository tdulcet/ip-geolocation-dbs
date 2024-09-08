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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-09-08<br>IPv6: 2024-09-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.764MiB (4.995MB) – 238,455 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b5f8e82b95cfb1c765ce50cd70ab4d7<br>SHA1: 347e76e5837bfbea8a4fcc7c5eb3ce2fb20b5e51<br>SHA256: 07684e7f6ee6ea9540645f475380991a0d07ca1db48bf045b3597c0bb667b4a3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.852MiB (6.137MB) – 88,938 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86fab6d1b63f0adb6a29c756c5bcdb11<br>SHA1: 27ef6d4a0df2a422e66dc49d653fc9320411ba81<br>SHA256: 4f7f665f7983194878a455fc387951a7061bc7fcfaec5463b4a9d39be76854e3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-09-08<br>IPv6: 2024-09-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.153MiB (8.549MB) – 408,287 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fe4b590f7116c96657046be7e2a5ad4<br>SHA1: 05fe8ed8a20d3775ff21c52bec21ef5e53755be4<br>SHA256: 86c0d56ecd7246512c1101031ae04123df9e1ed4016ecc461a3e41f16651de79</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.721MiB (7.048MB) – 102,254 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34a3b0c32cbae92a187807a80c47064c<br>SHA1: 411b7d03339020766d324b47195245bdab6d88d3<br>SHA256: 3b6df92e5dc7d3ffebf6d185becf1f211ed8ff1e6bcab5190941e59f42ef2207</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-09-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.88MiB (17.70MB) – 844,647 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf880d311714211a30e9b408d5ef972b<br>SHA1: 7b069d328356bf59a543d1a2110d59d450f03aca<br>SHA256: 051a6187d188bdda1be1949bcf2077af89029fb7141fd0f84d6b46aed25353bb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>73.84MiB (77.43MB) – 1,122,199 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b99c5a397525c8baee7fccd85d0d0ed3<br>SHA1: e6dbce47070c2d0a2c7f57451dd1d67f0bd0d1eb<br>SHA256: 8fb4a8d318111636f5a2d7cf6e5c493e1fe22f87a6c715963b0298ef48d82f3d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.026MiB (7.367MB) – 353,071 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcefe7ff67170edca76e960964754e05<br>SHA1: 27baa458e1a83274ab2aeac30e8c9e5fd89a29cf<br>SHA256: 462e24e1a1bb99827d9159c6ca57beed55617951e2ba210ac5d3ff2b406854af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.08MiB (20.01MB) – 290,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ebd3df44971fac41c81afc4e0b8e479<br>SHA1: e374278cdbc7551f55e127136a4623733504aeb5<br>SHA256: 5386c4b7b3b9edde1ed82d40af540593e3564055cf489bb7b99eb47057236d4d</pre></details></small> |
| | | Full Location | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.3MiB (197.5MB) – 3,287,813 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 454e55ae0fc4afbb509099e64b95780a<br>SHA1: 6b88a53921a475e7c1503a9fc3192726c88eee1b<br>SHA256: cd862087cb0a1f5359ee3534aa13b529d8eff5b1c700f8f97a19f0581998096c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>371.3MiB (389.3MB) – 3,603,634 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1073bf4bc29c411e1711e31e0f8593b<br>SHA1: f03eb167bbf14c750a0b060d043ebabe87ed9840<br>SHA256: 9f2c824922dadea859da67d03d96f92bd830c0efee37cf04ed4acf6cac6a1b6f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-09-08<br>IPv6: 2024-09-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.942MiB (5.182MB) – 247,345 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75be5fd9df21ddbc1fdbffc757c5c88e<br>SHA1: 617600a865f99d7027bf00861f55ec2f8fd1574e<br>SHA256: c577e4648304b379620b9b9b1a7b46685fe2b5a3719de872d7565971b4f67dd3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.43MiB (19.32MB) – 280,024 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 529fb8698467082348344b270ff7cc32<br>SHA1: 5e3253c77897a6f1833518163500372c619862fd<br>SHA256: 9289075bcac9e9a959f8009c5eae593e88bd3925aa371f097f4b54c6bd5bb9ed</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-09-08<br>IPv6: 2024-09-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.5MiB (182.0MB) – 3,005,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50ec8daacd5cafd5b2765884871d9b09<br>SHA1: 889e86b248ea9a4741e8399a0e67d17ad637cc38<br>SHA256: 5909cda69b8afb1da39fd44d4e35827b08820512a824be3f438aeb08bfbe1c67</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>210.3MiB (220.5MB) – 2,035,716 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 221fa2afd3b2e737797b4dd7b49d116b<br>SHA1: 42a7d10f6dcb092f867344cabddb6856eda16b19<br>SHA256: 138f90080a7371e27aaa532721e6449e41511cbca7244a5e31fdcc4081b48129</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-09-06<br>IPv6: 2024-09-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.780MiB (10.25MB) – 489,894 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c78d210cc11f8932040f582b6ec6faca<br>SHA1: 3656b5f73723c2d9c1c92d15ee023b06ab0eedc6<br>SHA256: fa697966cb2d5b3e2ec10cda9cfed77a0dc21f3204aa4c2e951d4dc29b0b19dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.40MiB (31.88MB) – 462,020 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c7aa40e41ceeec4f2dca0c59c210485<br>SHA1: 263be3ee098379bd7aba3b3d65c1d3359f1f915a<br>SHA256: 2a9a1cd5a5f9a8f2a7fdea75109639669d0660d8c8bfca2c744a504d30c48eb4</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-09-06<br>IPv6: 2024-09-06 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.2MiB (126.0MB) – 2,405,000 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d609debd268c1429563642c2f5c14afc<br>SHA1: 0c6e6ae7458391034c021ba1923667cc4909efde<br>SHA256: bd7349eac2c9d40f3fa964b740000da87d681bdda5a718be23482673e6839e6f</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.0MiB (135.2MB) – 2,405,000 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5aea018cddef299f64e4854412d4cee0<br>SHA1: 25585f291cd09ec866dc5385d4776e82c0323f34<br>SHA256: 2b8f0e6ac5bd6ca0857149835f98cc169ec3751437953673e8297ae33e1c198a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>119.7MiB (125.5MB) – 2,405,000 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f4cf1acdf6a918d25f80c662aaf459e<br>SHA1: 1187d2f652773a93562f1bac00f880dce65aa69b<br>SHA256: f93c7055c9badbf2543fc975cdf33869dc4458c82865320efe59b081e17b3b3d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.1MiB (128.0MB) – 2,405,000 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e74d6ac5f8c599868f954b5c0de7354b<br>SHA1: 265f5ad558e3341f9fa94d47054a523553cb59af<br>SHA256: e7f21d90a8f04a28eb7e693073d362b4175316514506e45fd9458e65e7a53631</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>149.4MiB (156.7MB) – 2,405,000 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fab535a23b42405ab3931df43b9c218b<br>SHA1: 4c31d24a71c2f05a6b8ae1effdfa6d8addbce4ed<br>SHA256: 4cb0a0d40dc38a7303deff44e37bce71295b0ee30d3fa4d50ce87477ef08530d</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.0MiB (124.7MB) – 2,405,000 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 985c792f81bac0961ae768eb22532af5<br>SHA1: 90acb4e84b8cc7224f0c4224d77dfc7b6e27c1d4<br>SHA256: 3b7a63510d3a34b59a645fef18787d1ea99fd2a2fe0e80bc382363f5a69ddac8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.1MiB (153.2MB) – 2,405,000 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1cdc29b82c4b692824371072da3729d<br>SHA1: 68afb9712a8093fa884c2d9e32aec377199ba1f0<br>SHA256: 7c77d8def1317fe6fb2783e1b071d786a745c957ed8e215d83490f090219dcd9</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>122.5MiB (128.5MB) – 2,405,000 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55e78bcec3ade47e9b95f12dd1f28269<br>SHA1: 83829205abcd5af0e8653e62bc041daa04c54d2d<br>SHA256: 2b37a9c2a28c05637b40e980f90c753c77cd9b812bc2161b0fe1c4ba044b07b5</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>146.7MiB (153.8MB) – 1,578,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88e66e5b85a388be34cf99a352d56397<br>SHA1: 401cd1246af0bbf3814924efafda131f6f6680a8<br>SHA256: e474af7d42a96b15dd955dc5bdf2afce4200207c1ea62689024ba17b2f924f3e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>149.9MiB (157.2MB) – 1,578,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d02702459429435265bc64e1080103f3<br>SHA1: 2a671a68058737685f118c4f1825b3d69eedf283<br>SHA256: e7db9ce6b3b1f544277f55f1640fdbf713304a4051675b32fc21edef2fe3fe30</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>145.0MiB (152.0MB) – 1,578,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b169cddf95a35c00f7d7832046efa0ef<br>SHA1: 0b4e7beb7bdc6fcce88158ec7290099aff9056b9<br>SHA256: 5995d06c16b1163eeaecb40385e167bb71fd98a5973227e899beaff3390fc7e3</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>145.1MiB (152.2MB) – 1,578,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63254e3cccdf4794897d5d48b4bca0ed<br>SHA1: 065ad4325220d873ccb740a790299e325d8e9dc3<br>SHA256: ce40951a59260bcc5178b810920739140f7c580812bb68a0b9a1b121a738f5dc</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>158.5MiB (166.2MB) – 1,578,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56b65656c76b592885e6dcce5bdbf4db<br>SHA1: 7e4dbb9e7a6a046663436eaa9ad3edc091426f3a<br>SHA256: d7d3abe6b63a18dd63fc4c7e6b2ad1c4704f8d33020c04de0ce975cd29bb1210</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>144.8MiB (151.9MB) – 1,578,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06f42c38a87370439d611abcc3fe9bfb<br>SHA1: 46196285277bb466f5d72c6561391d2a0908fc2e<br>SHA256: 4dd64489cd25af2e488f9b18b0700bafac87843388c2b2f8573f57bebbe78cd6</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>159.9MiB (167.7MB) – 1,578,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72dad56a44ff7314c627bb32d84c9a07<br>SHA1: b8493734b06c6d621e3ce27fa285029cc6f1da84<br>SHA256: b3d887f51ded075f1318882ea8e0925cb262a6e3fde7c743be336c326b9bc798</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>148.1MiB (155.2MB) – 1,578,413 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f440599101adb1c3a2ee0a59b19646b<br>SHA1: f39f8c57518784f3cc43ced2059e85a7c29d5e52<br>SHA256: 2a77d974ebec2b6421be7c50c75849c7927dee3279a8bc855cf86e57a50f6d95</pre></details></small> |


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
