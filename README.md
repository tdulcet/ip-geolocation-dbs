[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases are scheduled to change from CSV to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than one day (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-12-13<br>IPv6: 2023-12-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.606MiB (5.878MB) – 238,790 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8350aeb912b9af6364b9283ca6a9f8a3<br>SHA1: 8b201805f3b20d87b808c90bdc554f631bddbcb9<br>SHA256: 012c936108e8a0d5e5ce78780a0983f8b224cce8e7919d12697c685fe91991bd</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.319MiB (6.626MB) – 81,807 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 724e42447c2c1847ee5fa40f7e8ac085<br>SHA1: 54966e46e9c5ddf37a3f41f0add6994f9ca7b729<br>SHA256: 084e686db6164412fa47c38f2e673b9a1797ae08edb1c2257e1f191df369f3fa</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-12-13<br>IPv6: 2023-12-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.710MiB (10.18MB) – 412,425 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25f44c706555b0d2e03581a41e2a8dad<br>SHA1: 4d10952a19ba64b54a656dd6cacad78177d672d8<br>SHA256: 3308c3f5ae2bab7f15323ca632b022826ff49abc0a1a497b22f83dc69cce8a0a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.062MiB (8.453MB) – 104,459 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 279f9a8fcb908d0f57d401676162c211<br>SHA1: d4532b880c932ce6ec390892179c0f9a62355892<br>SHA256: 53a1ee949642181e64c2944a9deff4f5ffb93b74b8128ebb1b4efca1b768a52f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-12-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.42MiB (20.36MB) – 824,955 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92bd8f50786b2c71e93a5502daacb69d<br>SHA1: a424a9f0b329516a7919fba81b6efcde2469436b<br>SHA256: 34316cf5b0aa3fee27bdb627b2d610f3f584b75bdbad60d11a7ebad98da623ee</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>63.70MiB (66.80MB) – 824,655 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 12d9cf889499beddfd24b9ee7f0d00e7<br>SHA1: c01e0697202bf5b68d4e5bc553ba1239c54c4e3c<br>SHA256: bc48bd289dc46c8a65233b07ef8db7dbb720ba2e3e20a32f3c4db05e9653c239</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.227MiB (7.578MB) – 308,674 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7862828d186c4a916870bf5ee5c2dbf<br>SHA1: b2d61949f9d4cdf20a7bbe7858ca457da6437400<br>SHA256: cf718693f02d6570f872d99279b6729e48674fdf9a0ad17b2b5bd3a3004e7feb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.88MiB (26.09MB) – 322,049 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf9a945a8ed9ee1ba2168317dbed510<br>SHA1: 5488b48f6e283b58e14057f8bcc69c7a60073e80<br>SHA256: e724c992a57d034ab069e985589127206d0519f5cb5070ef4d8bc04d59937e7e</pre></details></small> |
| | | Full Location | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>188.3MiB (197.4MB) – 3,100,304 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e98adbd1d81ad4e7676a5bc97c6062eb<br>SHA1: 83a91e8b43cbdbea769542d684e8a2b61d6cbcb4<br>SHA256: 07faf7b0b69afe9bdfb83c30bf26ed6a6bc739fc4122230461107e862ca8202a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.3MiB (310.7MB) – 2,579,379 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b45c72d3f47f242ccb1124627ab028<br>SHA1: 46f55d20900ce13c49f5881ad197bc7a0d54d072<br>SHA256: cade24018cccb007f481018f12d82b3268ea4089c4223c710ce4213be2f799e1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-12-13<br>IPv6: 2023-12-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.454MiB (5.719MB) – 232,687 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7477aa0dc6695ad8d9200f94b8afd3c9<br>SHA1: 34d4e346c0da88e6d4f5988e17842c38d421b8b3<br>SHA256: 46a50da207a830584042870aa5b87c2dace68a946829e6fae37461d5b3427d52</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.74MiB (20.69MB) – 255,480 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efa7b87bcf99ba42fef37332f83b9e16<br>SHA1: dc9a17b5c1ee4e438d266c97c5aacd40da6bd740<br>SHA256: 24e3b2a9267c9b1de9614d05ec54385e3a732757a59c19eb3287899959cf7932</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-12-13<br>IPv6: 2023-12-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.2MiB (180.6MB) – 2,812,463 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4dbcfaaf8038ec905802f3bb4b98e60<br>SHA1: bb90c332e6a73443b2c214fd4c7c111fb053492c<br>SHA256: 1a5d0936e7c432fb29ae976e5de47f83fbae93c0e2d594781ab883143984266e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>176.6MiB (185.2MB) – 1,539,981 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa785991c752e8ca7a545029b778d706<br>SHA1: 641faab98a0a64a049fa166c4e4cee2698daa00d<br>SHA256: 7dec5cceb89309fb14723f22484df38d79bcc79adcd23394d5ce983d4a58e8f5</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-12-12<br>IPv6: 2023-12-12 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.68MiB (11.20MB) – 455,781 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce86eaab135a7aad04b6a479395c09cc<br>SHA1: 334bc7b692da9352229320940b20b4d0afe7a43e<br>SHA256: 06b7dd2a8a856d64b3107d2698399ede8b72962fdcaefc72178611b9cf3526bb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.19MiB (23.27MB) – 287,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 904df8634845d8385ce44d1850e1b885<br>SHA1: ac68f0051f8db5e78391b4d74d69808465bfc9c6<br>SHA256: d2c330e0879f692bfb316b1d0b636e04f836fdc8e5ae9bca3fa55ebbefeefbfa</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-12-12<br>IPv6: 2023-12-12 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>176.4MiB (185.0MB) – 3,500,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5d72130ac3d617026896f7013518db0<br>SHA1: 854d6151de2d615e4457b30a44ff60550ef9c3d9<br>SHA256: 7cda4fe25b4452607f0eed6bd46bccd6f15eaf6122427b5b71b6ed66d581d5d4</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>204.7MiB (214.6MB) – 3,500,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f28fa1a2c24861f1be6327f276cc0236<br>SHA1: a26460a32f4c313372fa118246bfdc5d997fea20<br>SHA256: 95874db484decdd35e11ff5747b04b832d2db7e68c26e2922fbdcaf779de858b</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>181.5MiB (190.3MB) – 3,500,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2710f36158c5958094f08dc717848f5<br>SHA1: 302dac63cf8fa6c820e078b16f066e2129016ce9<br>SHA256: 56224b7326ce9548b63b257e9000ad9d99d0b77e370e759d9b435faf1a182292</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>187.9MiB (197.0MB) – 3,500,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f922461f05b5238aab957d9773e356c1<br>SHA1: 99013405fb089ee1adf1adf1f5e7ead3b613f06c<br>SHA256: a47aa5822f728d46a6a3782ffa6adbd0726783d0585500263aac5c544bcb9ee3</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>216.7MiB (227.2MB) – 3,500,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80a51ae35ee5bb6663f4d5e55a00a672<br>SHA1: ab7cd6bdf1dcb761ab998950644d5390fc244dcc<br>SHA256: 2d46cd4aa73a83d9c8ff8fcb7524a147576f53b983543b97d3d91ebf958ae840</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>176.2MiB (184.8MB) – 3,500,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d2203f737b00125ee448a56a2b9ce31<br>SHA1: 6db190cbc1e827c51d21e1c56960c72529a67f99<br>SHA256: 6da12b8dd510e711600ca2bacc6ccbcb0935b2c5245cfbb99510dd5740c591b5</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>217.8MiB (228.3MB) – 3,500,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ade1f54fe7f45161e4f1352199b192f9<br>SHA1: df1f009dbcd0091d2bd619e69965cdf3ea9be336<br>SHA256: c804f237e3bad69b208d39236a32c8d015627337262b9aaad1e066649e45ec0c</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>184.5MiB (193.4MB) – 3,500,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44b798a0f8b6267d2aab24087f7be4cb<br>SHA1: 72e7d5b2584ed885c846eac01ab9c85db22feb10<br>SHA256: 912a8a05559df66dc52a9b96f3a4dfbbfc0bbacbe215039bade2ebbfd66679c9</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.8MiB (128.7MB) – 1,218,942 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d639fd3d481ddcc6bfaf85a89613cc7<br>SHA1: 90a378999accb6db629128c94022dea2f0755367<br>SHA256: 42194d07d55bcde866db3dc4716cec63758a7482cce2a4202ed7f43ab9fa5c12</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>130.6MiB (137.0MB) – 1,218,942 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e600b151d8628da810dec6fcc4f0f85c<br>SHA1: dbb80ca8711fca04d4318427d8883347f7d277dc<br>SHA256: 007684c22360d8bd8fe329dd0c0c2a282b0bf7f72d4819e31018068f17caa492</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>125.1MiB (131.1MB) – 1,218,942 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1398aad5c117889902a72812c19ccee3<br>SHA1: ed87065ddda4b9c3897842fe496ff0767ae9443c<br>SHA256: b3a27f10612a1d8b7d95a56ecc4f9637c9571f73331a9b7ed75f9f9d1d3015df</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.2MiB (132.3MB) – 1,218,942 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7c8b96aa105f90379134f4574fd44ee<br>SHA1: 8a32f9a335edfc4ade0bb2637110781c9e5aa15a<br>SHA256: 8af2acba50b0d908adde1567778f782d6e87fc52b9cafca209eb5a86ceaf9f12</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>134.0MiB (140.5MB) – 1,218,942 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc2c6e9ba4775c526d0ac34719645290<br>SHA1: 32f0f54a5acb7b29dd2ffed10877c0a74d344679<br>SHA256: 3a18aec423bc0d0f0b821cbc88ed50f7fdb4c408b94eccb9d5bb8913ba5ea5b7</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>123.9MiB (130.0MB) – 1,218,942 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d73d458f6237e6d14bd2fe12daa29f6e<br>SHA1: 771159f93775a94f3fbc884d92c83eafd9219e44<br>SHA256: 34ae6f3b614ee2b3254d69402fefeb1289adbc9d5ff4694541f76a29bf762ed8</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.5MiB (141.0MB) – 1,218,942 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41f4e76560f34a1c2643d281470b9e02<br>SHA1: 9161c32bc22fbc820d9c99fe23d26b933d0ff79c<br>SHA256: da0001d09b32c04586830ec4140bff43bcbedf2b542a3652e020109ce3c48147</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.6MiB (132.8MB) – 1,218,942 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d213c856f49e3ee2a8fad3f1b160ace0<br>SHA1: db411d55b3ab9199f5618d39b173b1bc683efc52<br>SHA256: a17cd7d6794ecf58a6a7442ab5afde78a8211cd8486a7eb23eac18854b36063d</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hexadecimal format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
