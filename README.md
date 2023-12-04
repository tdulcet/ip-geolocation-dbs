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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-12-04<br>IPv6: 2023-12-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.604MiB (5.877MB) – 238,713 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7870c000f873ca96d40732925d7957fe<br>SHA1: 57062c2e555caa2bb554d431f2b7ecf729cd5b2a<br>SHA256: d3bb8afb9ea9b5e8e27cff13433bc79c5926bf7f0fe8ed3def179cf1bcf83a04</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.353MiB (6.662MB) – 82,244 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca198f663d67300f86551ec6d7fec841<br>SHA1: 57cd89d17c2c7ef7b3bfa6120ed19b68845f7469<br>SHA256: be8cd565ac607978df3877542fc82037d40f6ee3b261b79109f9980542dcabd9</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-12-04<br>IPv6: 2023-12-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.670MiB (10.14MB) – 410,741 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5cc8fa24f99d37607d35c3142934742<br>SHA1: dbc25493a86b2d08f7270007031f6599d020d695<br>SHA256: 66ff3b27eb8a47e089c4fdb33eae5898a0e170149d6da5197ba1d65c0633146d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.071MiB (8.463MB) – 104,577 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d66a37a377a5f890a1fa4258da60e5d<br>SHA1: 6e42d1ffd92d358f444b8577374dff4c0e0f94ab<br>SHA256: 9790ffbf98bba7a886e5bcec4377977e279d243e9666e41830ea5707438c343b</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-12-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.48MiB (20.42MB) – 827,248 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52bf32b89bd8a0dc9139ba30ac604ecf<br>SHA1: cfb0185190178c654ac15052c8607b5f98ae3184<br>SHA256: 7a0366d074cdae869f2935cb6456b73a062fccc3cf81b3ef0ace36dc84b13d60</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>58.86MiB (61.72MB) – 762,008 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 940bf309139aa78f1d86c59a97a9dad3<br>SHA1: a86e80dd6c7271fb0d83547bbb68c831c5930e57<br>SHA256: 2d373658051ec86a6ab27c2c1d1ecbdad73a83cbdb12b4c69183ee6a011447a1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.227MiB (7.578MB) – 308,674 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7862828d186c4a916870bf5ee5c2dbf<br>SHA1: b2d61949f9d4cdf20a7bbe7858ca457da6437400<br>SHA256: cf718693f02d6570f872d99279b6729e48674fdf9a0ad17b2b5bd3a3004e7feb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.88MiB (26.09MB) – 322,049 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf9a945a8ed9ee1ba2168317dbed510<br>SHA1: 5488b48f6e283b58e14057f8bcc69c7a60073e80<br>SHA256: e724c992a57d034ab069e985589127206d0519f5cb5070ef4d8bc04d59937e7e</pre></details></small> |
| | | Full Location | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>188.3MiB (197.4MB) – 3,100,304 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e98adbd1d81ad4e7676a5bc97c6062eb<br>SHA1: 83a91e8b43cbdbea769542d684e8a2b61d6cbcb4<br>SHA256: 07faf7b0b69afe9bdfb83c30bf26ed6a6bc739fc4122230461107e862ca8202a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.3MiB (310.7MB) – 2,579,379 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b45c72d3f47f242ccb1124627ab028<br>SHA1: 46f55d20900ce13c49f5881ad197bc7a0d54d072<br>SHA256: cade24018cccb007f481018f12d82b3268ea4089c4223c710ce4213be2f799e1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-12-04<br>IPv6: 2023-12-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.454MiB (5.719MB) – 232,687 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7477aa0dc6695ad8d9200f94b8afd3c9<br>SHA1: 34d4e346c0da88e6d4f5988e17842c38d421b8b3<br>SHA256: 46a50da207a830584042870aa5b87c2dace68a946829e6fae37461d5b3427d52</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.74MiB (20.69MB) – 255,480 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efa7b87bcf99ba42fef37332f83b9e16<br>SHA1: dc9a17b5c1ee4e438d266c97c5aacd40da6bd740<br>SHA256: 24e3b2a9267c9b1de9614d05ec54385e3a732757a59c19eb3287899959cf7932</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-12-04<br>IPv6: 2023-12-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.2MiB (180.6MB) – 2,812,463 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4dbcfaaf8038ec905802f3bb4b98e60<br>SHA1: bb90c332e6a73443b2c214fd4c7c111fb053492c<br>SHA256: 1a5d0936e7c432fb29ae976e5de47f83fbae93c0e2d594781ab883143984266e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>176.6MiB (185.2MB) – 1,539,981 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa785991c752e8ca7a545029b778d706<br>SHA1: 641faab98a0a64a049fa166c4e4cee2698daa00d<br>SHA256: 7dec5cceb89309fb14723f22484df38d79bcc79adcd23394d5ce983d4a58e8f5</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-12-01<br>IPv6: 2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.81MiB (11.33MB) – 461,240 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fffd4e271ca9011f7229126248636370<br>SHA1: 6e13f3d04c0e7c92b01f966a7d6a95596a9a8bc6<br>SHA256: 70de801bbbef61a10c6449a3d50abce7bf2f40f5a25e4e71f6743764dc80007e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.65MiB (23.75MB) – 293,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79a4ee98ada6e2706dc3548e828182a4<br>SHA1: 081117b8f4cc00a9c071625031c6818c414e9696<br>SHA256: 8c50a94a8e4691e90a21035f634d8958f4af46fcd8832465b9073667e655c7e8</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-12-01<br>IPv6: 2023-12-01 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>163.9MiB (171.9MB) – 3,249,991 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 109cf90ed578e5ba3fd2d70521a56858<br>SHA1: 7ff55eec6692edbf0e39085b0d06be69ea3b2558<br>SHA256: 1e90a5068060f80fa4da9459aa4fe8f6d60b3b3029288c6a47c2a619255fd790</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>189.7MiB (198.9MB) – 3,249,991 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc08989d3b3ccd4aa806f9ffd96cf9ad<br>SHA1: d6db36c5e73e0ac6508fc76f00f23aff51418a1b<br>SHA256: 1c0381467d3d1656e0f0c51e5f230b55146335ff5f4f902d96f0122e7e677484</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>168.1MiB (176.2MB) – 3,249,991 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9e2854d3cdfaae5b49e935aa69078a2<br>SHA1: 3702d53ff1310b7edb87ce0e51a008ebb56b68af<br>SHA256: d0aa3ba62640581220b04e9a3a0c57f22c84a7ba63e03fa16cfa05d6ab5a8117</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>174.3MiB (182.7MB) – 3,249,991 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d234e1605b84ade30662cfc35e9af53<br>SHA1: 607ccf9a8cbd46f8ed813bd86d6701bb43dac490<br>SHA256: 106732c5b3e38010e4e52078f3788e88d91cbb29fe5718a14d3eb3f45fd5d741</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>198.9MiB (208.6MB) – 3,249,991 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75d86440384ed4620a829cda34cba73d<br>SHA1: 07971a68cf661be993e1d115073a47734f71bbd7<br>SHA256: 5f59ec16cb09fe96dbd6aaf989fb199a7d78a6064d9370ff67792cda0e164946</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>163.1MiB (171.0MB) – 3,249,991 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78bb5d45765fbfe49dfbe5e8a5cc3679<br>SHA1: 2c723c96ec1d1ae2dc99b1e40fc1524389d8bd19<br>SHA256: 3cceb94f91b232710dbd75ab6f69cb51f747db1938a0db79f4d9e8b18cab21ff</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>200.7MiB (210.4MB) – 3,249,991 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a20905169c280d024bb08a6971ce757<br>SHA1: 08cac987a8960550920f0b527d96bf96afaebf5b<br>SHA256: ff84dc18d747de17aa8d822a70e043c281bb11dc0c084a5ea301550bf2ccad57</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>170.0MiB (178.3MB) – 3,249,991 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5ba8f1cfbaedd0a9249af6d315f9d59<br>SHA1: 7bbcc4d29b004fe2eba6aae1ade4783dbb6f37ef<br>SHA256: 8fce6942653947741d5d0497e59a55b9eec6030e681ed50bb0503fa89559ba31</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>124.8MiB (130.9MB) – 1,241,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b1e2f66e523d25383329f04b0c3eb01<br>SHA1: 6f5f17ce42b4446de1dc60aef2bc14e24c29a253<br>SHA256: 0adf4c49542b6fb167c0d2c7dfaaa95b9579a5f66164010796e0a2072ec0f205</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.8MiB (139.3MB) – 1,241,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7f6438695e4c7b453834c4fd5687b64<br>SHA1: 388a5f2667b2c9ac487adba8ffb386a655aabc32<br>SHA256: 391407462b69faca481abd6e0b741bd5ab6ab9e35390be724a104e4e14c9c3d7</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.1MiB (133.3MB) – 1,241,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4b44455f4f07f72680220c96b0e318a<br>SHA1: c8dab20cb4061c316ffe04bf5c5f6cd1a083c980<br>SHA256: 0a30d5b4d12033f211f5a1cedfa57b9e33b6b8d380707f4b4324b0bef3ebeffe</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.3MiB (134.5MB) – 1,241,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8b7efd765d6d45d5c019f17d580c1f0<br>SHA1: 96c352afa7081dc35be3f59fde78388d53e6de0e<br>SHA256: 37ab55f43ac42c52a223aad43e2cdd51ed19adb9db132931d5a173d056bfeaac</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>135.9MiB (142.5MB) – 1,241,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d674ab693f647a65658b354630610d<br>SHA1: 8d16723f9dbda7d5af1d26f85f8b552371c087e3<br>SHA256: 860329cbb4191763e5f432c798b007f745b243a9009355d072f15b02e7662db5</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>126.0MiB (132.2MB) – 1,241,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2994d139647bb2e00f6b5668e9d79a26<br>SHA1: fcb25b770203e3b8feca2016da1433db8fec89a9<br>SHA256: 04d5f54a707585940d1e4b5164cfcb468ffc8b0bb7bf05e1255be436f7a06df0</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.6MiB (143.2MB) – 1,241,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d91a0946a4d7eccf8e23c1b0699387ff<br>SHA1: 6e5965982c65035cb524861cf2fc43506b5e84b6<br>SHA256: 14c77fcb7b4ecec0fe5c4f808a61e3c78fff1f836c5527ea71de740da3e1682a</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>128.8MiB (135.1MB) – 1,241,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d5505a6fd6570f1269f7a70a20b3393<br>SHA1: d29d265941ab9ab92aa9e5ac0dbf5060f73ccd2c<br>SHA256: 651a7f25559c39b6dad583637672c8474647464eef311a908b9ae324feb4a74a</pre></details></small> |


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
