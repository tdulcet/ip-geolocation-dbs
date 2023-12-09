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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-12-09<br>IPv6: 2023-12-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.606MiB (5.878MB) – 238,766 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 748fa8c3137131c7b6c999c710f0a9ec<br>SHA1: 8e1377a42d86230a719a78dfb2643f0577528fc3<br>SHA256: fd37ccf0f7cdebecc4298e3f6ad1665c80d34638d60248b643be357293e06153</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.368MiB (6.677MB) – 82,435 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6f470c772699734da1909b2b0db46bf<br>SHA1: cd0d59ed2e2e1704700ef5018bcd87aff833e475<br>SHA256: 608c98ec68526ee95bfa7d1d552a95527a7aff39373be78880174243f22a1bc9</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-12-09<br>IPv6: 2023-12-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.704MiB (10.18MB) – 412,168 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 992373fba878e7b625cd48cf89bc2a38<br>SHA1: dc8b36b61d0cb3440763ece4995e3e4192ee81bc<br>SHA256: 5b97ee2f3814a8d7d1868a5868839f8169ebdcb16e95e27783a37c9b1cdfc1b2</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.062MiB (8.453MB) – 104,461 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a73c1c4636309278dd56eff396da1ce<br>SHA1: bdc3f8fa7d77f626b06dc1bcf80fc3cf0d3ead8c<br>SHA256: ebeded6378904abdf1569bbba032a1d050edd56c6f2ceec6563ce0e3f2535193</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-12-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.35MiB (20.29MB) – 821,922 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b4c0c32b708e3ebbdf650a7cf211eac<br>SHA1: dfcf8e9f84f49b2efccd7e0ec6c5151a607d2531<br>SHA256: 765e6e81a8745e7caa300f1135eab9101280b3830c51ff9cc682c694bdcce3b4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>59.10MiB (61.97MB) – 765,017 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bf51a0766f0c90330cbd893b3d6ae23<br>SHA1: 6ac6eca8092a54af2bf6f249602b9421d17f450d<br>SHA256: 0652db0bf3a472653afe04f1fefb95012c41e64337f28fb4ad7d61a1b86b53a2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.227MiB (7.578MB) – 308,674 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7862828d186c4a916870bf5ee5c2dbf<br>SHA1: b2d61949f9d4cdf20a7bbe7858ca457da6437400<br>SHA256: cf718693f02d6570f872d99279b6729e48674fdf9a0ad17b2b5bd3a3004e7feb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.88MiB (26.09MB) – 322,049 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf9a945a8ed9ee1ba2168317dbed510<br>SHA1: 5488b48f6e283b58e14057f8bcc69c7a60073e80<br>SHA256: e724c992a57d034ab069e985589127206d0519f5cb5070ef4d8bc04d59937e7e</pre></details></small> |
| | | Full Location | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>188.3MiB (197.4MB) – 3,100,304 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e98adbd1d81ad4e7676a5bc97c6062eb<br>SHA1: 83a91e8b43cbdbea769542d684e8a2b61d6cbcb4<br>SHA256: 07faf7b0b69afe9bdfb83c30bf26ed6a6bc739fc4122230461107e862ca8202a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.3MiB (310.7MB) – 2,579,379 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b45c72d3f47f242ccb1124627ab028<br>SHA1: 46f55d20900ce13c49f5881ad197bc7a0d54d072<br>SHA256: cade24018cccb007f481018f12d82b3268ea4089c4223c710ce4213be2f799e1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-12-09<br>IPv6: 2023-12-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.454MiB (5.719MB) – 232,687 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7477aa0dc6695ad8d9200f94b8afd3c9<br>SHA1: 34d4e346c0da88e6d4f5988e17842c38d421b8b3<br>SHA256: 46a50da207a830584042870aa5b87c2dace68a946829e6fae37461d5b3427d52</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.74MiB (20.69MB) – 255,480 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efa7b87bcf99ba42fef37332f83b9e16<br>SHA1: dc9a17b5c1ee4e438d266c97c5aacd40da6bd740<br>SHA256: 24e3b2a9267c9b1de9614d05ec54385e3a732757a59c19eb3287899959cf7932</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-12-09<br>IPv6: 2023-12-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.2MiB (180.6MB) – 2,812,463 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4dbcfaaf8038ec905802f3bb4b98e60<br>SHA1: bb90c332e6a73443b2c214fd4c7c111fb053492c<br>SHA256: 1a5d0936e7c432fb29ae976e5de47f83fbae93c0e2d594781ab883143984266e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>176.6MiB (185.2MB) – 1,539,981 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa785991c752e8ca7a545029b778d706<br>SHA1: 641faab98a0a64a049fa166c4e4cee2698daa00d<br>SHA256: 7dec5cceb89309fb14723f22484df38d79bcc79adcd23394d5ce983d4a58e8f5</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-12-08<br>IPv6: 2023-12-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.81MiB (11.34MB) – 461,347 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6117c4f176fe3149e9146c6763a85bae<br>SHA1: 3e2207767df26a5f81b87105cb7f98c271db3b4e<br>SHA256: d37acef9a1b689c4564de03d21c826a54c1b7d36b065d0bd2591775d972b877f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.92MiB (24.04MB) – 296,756 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7be91c478de3e63c02f72d28b21970ff<br>SHA1: 9cf5a6b305edddcb6c20fb9f9911c45cd35e5663<br>SHA256: b48547a4ffa3a6ab121d7650a18daa76930abd0f4e931bf099269119fe3ef36b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-12-08<br>IPv6: 2023-12-08 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>173.1MiB (181.5MB) – 3,427,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a47c5c11bed6a32e6766c2b2b7f3eada<br>SHA1: cc6c83e809a8f6d49cea6401bad658d966dfb2d9<br>SHA256: d55a331b884ad1ba1c0083392809805f0763ada2d60f5730c75f732c1029e656</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>201.3MiB (211.0MB) – 3,427,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddfab9afd5971a80e740eb394e61f21f<br>SHA1: 8cdc275ade79fcfda22146bb453b60d3be16e81b<br>SHA256: 5e6b4e546165346c0c8cad9521767b2991ba5940c08f3436246ebf01a3024dbb</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>178.0MiB (186.7MB) – 3,427,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a29e75bb62da2146f6e98d94f267cab<br>SHA1: cba23a3f0b262cfbee6ab46d60d81e5fe74fb787<br>SHA256: 91d1058ea26a5389c352e3e270a09f09e8065fc83726f95db66bdfbbb98ae4ff</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>184.5MiB (193.5MB) – 3,427,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47be1fbd0c12458a559035e847492ec6<br>SHA1: 5e8e4b8b8e76ff067b62c6eda93136d0a9d57691<br>SHA256: fc1b2a210a5feb8e7c16a034d3a5fff63e56f4dab91386f89ae863d88b436f5c</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>213.1MiB (223.4MB) – 3,427,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eafa55f4c29077b6ee67a518dc61d5aa<br>SHA1: f228812ecc3e369fb8de3d4869d6533c0ee70526<br>SHA256: b6c5aa290e74121a76f7a8fb380a5a8b9f11b4ea9c83059f8b8724e1b29da41d</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>173.1MiB (181.5MB) – 3,427,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ed9c4c10487b7d5dece4325b360502a<br>SHA1: 1a9f3a6506e4b3ea768c958e73014b052c8bfc52<br>SHA256: e1bff6773044c58bda84baf99007790b72b3728bef41cb2f47390ae573b7b1b2</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>214.4MiB (224.9MB) – 3,427,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f97ee5fccb20fffa442dcabf39d08d10<br>SHA1: 9dc6ab985818f396ca70f794033cf9824c970e00<br>SHA256: d1d7955a5d6b2c46e133d518f2dad9006df0c440a21c1184f85b2775af58d4c4</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>181.4MiB (190.2MB) – 3,427,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 139b4398866a2aeb9a9a784078a48751<br>SHA1: 7716a4ebaccde1431a7a48fe202c4b4604e244a7<br>SHA256: 799b65f146b37a1f25b38fe270782762f9c11a6e4f2f2d375e5cac271042b482</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>121.0MiB (126.9MB) – 1,201,509 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92a61b94fc8a4aec58cf9a663c30152e<br>SHA1: 55eb43b5bb273532c365f0fb3f43d01ef716da84<br>SHA256: c33fcf2229291d2e2c69faeaf6aaa52b3e3707a1bf8c4434eaebea177a8adf0c</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>128.8MiB (135.1MB) – 1,201,509 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 711057cd30a795887b60b96c84e5e905<br>SHA1: 2777b25490d1d0c5237151c2fb9d1c6fcf5375fd<br>SHA256: b2f9b7d59248f5f0a91b56942757233399fa8110c08cecabae67bd85b5d2a4fe</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>123.2MiB (129.2MB) – 1,201,509 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d007b80a028ba14956dfbc65f653c0cd<br>SHA1: 72f062492327e32b649a3138102dc0faaef3b12d<br>SHA256: 864fad1bca396dd5a9b0bc239520e6584d9829ab31b1a3cf9a92015aa6b7be91</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>124.3MiB (130.3MB) – 1,201,509 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68ab598bc6784ddb97fc5402014fd5c1<br>SHA1: 55cdcf8fd8a1b7f81c6a2fbe1d0d6333eef13a0a<br>SHA256: 40b121f5e5989d465132cf86a96677aa770ae346f45701efe38d9a96692cea3d</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>131.9MiB (138.3MB) – 1,201,509 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f5f4fe1d8699e317ce00d9646eed626<br>SHA1: e315f63dee7c09e4884a9e0c6023e4b8227357b1<br>SHA256: d31db78517ef5d0be846188ae1d43ac2bc13cc2bca040b05f7cc4ac74dd4b499</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>122.2MiB (128.1MB) – 1,201,509 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9b719da9be2f8522191dd07d63920a0<br>SHA1: 3c0464b16f72a5eecbe3528dcbc366266bc255cb<br>SHA256: bdb039b49d6c6d10ca51a98a75290a238317c094bfa3b742eac50f3b70423b72</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>132.7MiB (139.1MB) – 1,201,509 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d146adce080317034bff3cf2d3f2594<br>SHA1: c63e335961c859d82fe2856b558432d07cc30d00<br>SHA256: 7871fc45e0bc217cbf91b2dc1ab1fa77713899d2e5f5b35b051ab054b1f3e5d3</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>124.8MiB (130.9MB) – 1,201,509 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3fa1633869c1482e3dcb518da6e6bd25<br>SHA1: f624d8ab520a09c8858c3efec4369f54d64db4bb<br>SHA256: 19c9e4717169b6949b9a924c8231eea488fb981ec54e8f14b72031663cc32b02</pre></details></small> |


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
