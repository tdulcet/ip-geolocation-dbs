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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-03-30<br>IPv6: 2024-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.819MiB (5.053MB) – 241,236 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9bb03fa139198e774c08ea058c4a23c2<br>SHA1: a11ed23bfc6cbb88d29cf5cc0d18ffadd09b3cd7<br>SHA256: 7f83d05b8cc7e58d5c0b426f4562407eeb1a30feae3b13b8a63f3379f16071ba</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.090MiB (6.386MB) – 92,544 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a827ff4ed2c744979cf58ca4d3795885<br>SHA1: dd255c18b2a71ad34849c2e370c817691f7b974d<br>SHA256: 7910810688c24bcd94af9a0fefa5dc637f9037ef5153b8217271569e8b055857</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-03-30<br>IPv6: 2024-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.211MiB (8.610MB) – 411,225 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f37bd7595434bcf282ce93ed3e66adb6<br>SHA1: 4e58818123b6acb81980b985139d678a80c6aa58<br>SHA256: 41c76e150dcca15d6164e24331ba308c464b26537823f8cdd54b50d5bb825170</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.089MiB (7.433MB) – 107,838 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00c0681d6c25c16953d5d78f2caca16f<br>SHA1: 084fb0b6a1d172afb63afc92565651299e54c747<br>SHA256: 9368654b555d886c1ee6f75e1f8ac905930448acfbcc1e728dc562d11658e068</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.63MiB (18.49MB) – 882,689 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a1a55722e27f3f09e44ba18a8917e45<br>SHA1: 1237ca6f6abe8be6c92beb991a4cd55e66b9a26a<br>SHA256: 3ad27aeebfc141f219b5327383b0215244b8ea0a39d27c180ca35b6ec745bb1d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>110.8MiB (116.2MB) – 1,684,499 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b753e4af560460d6f57e70ba0abfd71<br>SHA1: 5d3bde270f15b5b01516fd2bbc4c551c0f5f2a37<br>SHA256: 297665ff9465669cf90295bf3afee6322a236eb7a468a82cdb48a9d4ea288ca8</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 322,326 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b232d78e18dacf266bba37244688a18f<br>SHA1: 2ea0bf2a68630d5c12c6fa1d18f2f3eb0845f297<br>SHA256: b9f2935f135d22119e5db5d8d8666980b07ac2e36359fd6dbdc9c26a8b3be2f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.03MB) – 275,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49241985f6153f5f100b60421257f25<br>SHA1: 51e0348aaa544a9b75aa17c9431f3745175c5c5f<br>SHA256: 3420806d6067a2579fe3eef92e4cd09b9b792cce9c418a3ca7f3c820f4edb887</pre></details></small> |
| | | Full Location | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,158,494 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd92465491c42b3844af48593793b1d0<br>SHA1: 53a3bac0d03e0e4bef95ad11b21c1a1e92eed9f8<br>SHA256: 6157eb8d8b93b5da65533893b6b1af8682e371476cd754957d56f3cfd1179aad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>307.8MiB (322.7MB) – 2,989,351 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a432fad1dde6398b8b6ee222abf32676<br>SHA1: 78d2ec063fa05a95bb17703a5111864cd91a5446<br>SHA256: 5974cc41b3872ea8fe373def59322db31b678ff8585a6e529b9737d648343c0d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-03-30<br>IPv6: 2024-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.826MiB (5.061MB) – 241,587 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53358947a90b798856b0f2491fbc6d2c<br>SHA1: 7c9c0c0ee1f075fe6d82ea2f7ca31f00a5b7ad18<br>SHA256: bf9da0021f243ed534ef8e2352a5fee71207c3b880a727cd5031b79c5c122185</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>16.63MiB (17.44MB) – 252,757 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05df7acc3edcfc49d6d0cc8e5b23185d<br>SHA1: de417cfa98cd08340a971a226b8075d8887c08b6<br>SHA256: e2904c3019400cf283bda389c8d7dc9f8c0b5dabc1bfd9dc40ea4326c79f404f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-03-30<br>IPv6: 2024-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.8MiB (179.1MB) – 2,959,758 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d837249426a59f38d52d9939db4c1a1e<br>SHA1: c71a37a88777bcc232ed0cec8b11f4b0b93ba955<br>SHA256: c25d6cf67e34fdd6f9b5042bffd4059449b156fc6b7bb6e3fd49ce1979642175</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>169.7MiB (178.0MB) – 1,642,006 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e91d25d35aa21837cbe8c01e725e1cb8<br>SHA1: b3aecd7e3f4493788fdc4c941a22f3f071cd5130<br>SHA256: fe72238b338f395cd55c98381ca41ebddfc893eb2bd92625551b9fe4d8d96a53</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-03-29<br>IPv6: 2024-03-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.653MiB (10.12MB) – 483,602 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1db29a4d71a6a4dd2e9e8f522e15c10<br>SHA1: 76568a9e7ae549cf165b7cfe5ad1e47a2cd524ba<br>SHA256: 79a14095f495fbe22ca8a1a25b7f2b9815d0f2ce5adba5e7d3a2b8f29b352cfe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.62MiB (19.53MB) – 283,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7512ee8449410d6852a417049e948f1<br>SHA1: f43b4ad19e7149e0bec57d65749ad39282a614b3<br>SHA256: 4323bd781263a13f816eedce2a46c7ec33e68b424eaae0f6a959cd7926d222ae</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-03-29<br>IPv6: 2024-03-29 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>143.3MiB (150.3MB) – 2,877,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4650827dbd4c332d6566ccae56dee9cc<br>SHA1: a18ee298d255a3abc570ea8ccd6aa7efccf2c7ff<br>SHA256: b960158f43b9f12ca339bb3a340ef5509d0e773216343bb433eda6b4f18d12da</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>156.1MiB (163.6MB) – 2,877,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 029c8dc3735f3bf0ec00d2b14e753135<br>SHA1: bf235f79bf963cd9fdbb8fcdb79f79a47f2a093f<br>SHA256: cf9fd539fa78ef106a12ccec110ae7ac336be2fabf428d55466ef0f8082587c8</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>143.0MiB (149.9MB) – 2,877,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cad386724c4ef83c88bfdc8c47a6b88<br>SHA1: 6869a397ac21f78bd66ca18dfebb45b98e90c42b<br>SHA256: 76ed0428cae400e6c3d44f15aa7e05f405f664e1987f4e851430b12eeadfa336</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>146.0MiB (153.1MB) – 2,877,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64e38abdfd5e63668b60cad0d4f444ba<br>SHA1: 65f188d41ce740dfae6b7a2175d8ad5ed00a11ce<br>SHA256: 0215929e3c27df359bc2ea193deb74a8737dca15f3cb385aa29ad3b49c4612cb</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>178.4MiB (187.1MB) – 2,877,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91f4f9137f18569cfc4ccf089ee494c3<br>SHA1: 075fdf43c97e6fa276604ce0498593be5c748507<br>SHA256: 620d27bdc411ccf1ed69ef72d8e622cf75eb929c2af9808083ee9d4f989b1c42</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>141.7MiB (148.6MB) – 2,877,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6272695b693f8c6a3b69fe6a1df0db44<br>SHA1: fd0327e96a5fe7bf1002c45898fc7625ee8b4874<br>SHA256: 3b812bcb052e64f722bdb1cc9d3391659cc8afd700dd19c77fffa20b27463409</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>175.2MiB (183.7MB) – 2,877,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94cfcb93dbb1f2340426c3ad0b43f897<br>SHA1: 8fc2eab53610a055201cbe1d78a0703656f602b1<br>SHA256: b5d31ad6693e101083aa4e28f44c4d97975bf430457d3fb0ea4bcc04a008f3d1</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>146.7MiB (153.8MB) – 2,877,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16cc3116a611d0be65a42f998174e60a<br>SHA1: 542457aef6e2ec49922ce32525961a88906dd3c2<br>SHA256: 8665207886c9f331af3b890edac8dc5af7755619ffa6f7332c84bf48cf7ddca4</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>112.7MiB (118.1MB) – 1,217,447 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c90fde65b23bffb602c194ba3a95c4f<br>SHA1: 2621919e28c9666e35c49104ff606045bb8771ad<br>SHA256: 8886ffd2494c13bd75417894275defb86779ba84ece5e0e4790c4ceacf5da347</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>117.1MiB (122.8MB) – 1,217,447 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0790111f34e66013f53585424dbd830f<br>SHA1: b0a5cfeed017423043190b399c00570d9da28294<br>SHA256: d38c6b0b3d6feff0d9d77e75ee9df5008f73c75df2b92882e5ab4aded6e0d682</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.7MiB (118.2MB) – 1,217,447 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ab30a6bafb2802832b19a42ee0af902<br>SHA1: 85d80c4f2088df07e97a75bab7859cee3251655c<br>SHA256: 91fd0ff838ecb8008df790333ef5163586b18c70a5eec73446c685127d1c27a2</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>113.3MiB (118.8MB) – 1,217,447 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42069779fc92f3068f0a31fd702a41ee<br>SHA1: 2e0fe6eb8d5ca43661a66fe9e004db84782baf98<br>SHA256: 7a1d8d641e25928c7dc20081c3cc0da0002729954c845f55b94c2b8923b6f715</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>124.2MiB (130.2MB) – 1,217,447 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72aa8f993db8e4c83692b19d4f233640<br>SHA1: e8a6d413200480d20a29019c0eef927b89add9db<br>SHA256: 0a3005541335b34e115ba024c766d6d3568b8f531b64a7d5ec35252cbc304e61</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>112.5MiB (118.0MB) – 1,217,447 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0660a05bdc1edadba9f0b4ac11a67180<br>SHA1: d634b5106dd32f4d5d88425aa17d4add82403ad1<br>SHA256: 323269fc627d8b8e1e4cdf03371ea709886dfaa68a6f3f54287c1d29abdf3e1a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>123.7MiB (129.7MB) – 1,217,447 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ac69439c96484f60b883d6688ce1824<br>SHA1: 83a436e88cdd705398fc998b32f7d791fbfa8bb3<br>SHA256: 5cc010378c2cb5923edd61befc0d00c71758df8a52024704addad209a7e92e6f</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>114.7MiB (120.3MB) – 1,217,447 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4dcbc2de774099e08cc5184fdf6bc25c<br>SHA1: cb87d67d100d5e1c00c07173eb3b406db0bf5dd9<br>SHA256: dff706f816107ea684c07e6c7beef0d3e3347acf2e9e81638f274ca50ec0e563</pre></details></small> |


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
