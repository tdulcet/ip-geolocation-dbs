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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-06-20<br>IPv6: 2025-06-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.205MiB (6.507MB) – 310,766 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbef70cb8958e18a48c57951f580aa65<br>SHA1: 14e21c76ee507108c0cee9889d02a47b11b230d0<br>SHA256: bedd7e3dd327c500e12ac56223081591a5bd79b83c5da0504b5e1236cc8a9caf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.20MiB (12.79MB) – 185,348 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 792f6f5bbaf3cb598bb885bcd0d3770a<br>SHA1: c33c535ef121d9f0e1f2609bfff2426faca17988<br>SHA256: b6a789ead0da2fe597eb7833439670e5b9b50a13b79b0ffa388b2edd5024a07d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-06-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.35MiB (12.95MB) – 618,448 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d20f17d731e1c7ac115aa47b59bf2aa<br>SHA1: 58e8d98c4386270546eb3b127f1633131428dd07<br>SHA256: dc9fad98f4b82632821394d356d0810bf91b8160836d000c60e40b2430bba1ce</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>85.78MiB (89.95MB) – 1,303,635 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d8d10f40dcd36121e57d1ec149ebc28<br>SHA1: 234a2506963336cb1ac7129bfdf488e019830cf3<br>SHA256: c516bfffb2b9b08b7135648e915614f1f4d1e2752cc7ad9fd76e18bd99d88531</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.020MiB (7.361MB) – 352,022 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5d6ce30939ecacab9e5fbbde143dd7a<br>SHA1: dbe45e91ef39b1de3ae5caecefe6dce72faff5e1<br>SHA256: 843f29bd3db6468809b0042da7a6b44aa5aa0f7b3378bce2344b427d7b8b2458</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.50MiB (17.30MB) – 250,746 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86b9bc39132e2d99653445ab24f13e89<br>SHA1: 04cafe97346c96dfaa2a0c192e271c1aa18bb99e<br>SHA256: d337bc1e4ec66010e25e0e0279f489bc7bb3f2218829c1b952e7b21620faf6b0</pre></details></small> |
| | | Full Location | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>189.6MiB (198.8MB) – 3,310,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1255823f4fa6d96cb2339938032ec17<br>SHA1: 7bcb7165d5248f918857090fad507b3b62aff99f<br>SHA256: f33143e90c472ffeaf3431c1f790ca9297c4fcb75c4f9b48690bbe6cb9d79c80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>401.5MiB (421.0MB) – 3,898,653 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50981857bc3865133c307de9e8f457db<br>SHA1: 915f84f9ac8ac491a0dc82f8e1c8a8b51e82b9eb<br>SHA256: af893c4ae1cfc50fe6b043a92e1ececd960d30f00aa8a0067646fda960aa8ddc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-06-20<br>IPv6: 2025-06-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.060MiB (6.354MB) – 306,250 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66813478af08592fdfc48fd31bff150b<br>SHA1: 811a9109b04c7e248ec3039089a3534799a0b45e<br>SHA256: 7438026d984ce77dc6a3c83ea0623314e8e04ce52f031ecb819c2211c10dda60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.18MiB (22.21MB) – 321,882 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dc7e513e52e0755f6fdadbaacc17b5a<br>SHA1: c9ee76ff47638d91e8db56f68fe6b0d1ca2f6cef<br>SHA256: 35bfcec7d2598e67771e9d918023c4280f9109650acfb7bc6d7776c000fa7505</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-06-20<br>IPv6: 2025-06-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,073,788 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5842c1e89d9e6a7ace62a726c41126ac<br>SHA1: e3950375fff9f4e7a1b551e841a320f17e1763f3<br>SHA256: 136c0e48f44d563e0a01829656f7c14024757ccb342856959d0a6797ee9afb85</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>243.8MiB (255.7MB) – 2,366,384 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e93be5d64be521626b8e98eb9c04690<br>SHA1: 8491599042ab2c0661a6d9968a86b0de5322e2e2<br>SHA256: 699e1f5782b93d7acd864659595c72dc1e8bf20e3457b3d9fbe5503103a35841</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-06-17<br>IPv6: 2025-06-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.19MiB (12.78MB) – 610,362 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d753eb57dada850edab38087a2441f2c<br>SHA1: 1e145a42efde5c6b2e34a5a977ae143252d425ca<br>SHA256: c27f0832affbe0a085ac044629ecd318784ca4bf97767f0a9ccd24fa24f88449</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.01MiB (44.05MB) – 638,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c05ad4054722eca596856f20a42efc9<br>SHA1: ab5bd8db256c0f39838052c91976193c711e6efe<br>SHA256: 4ff6770d71221f2e2c1f0554e0075f8856efa4cab6b86d1dc4b226edebf69d89</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-06-17<br>IPv6: 2025-06-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,412,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d107adc53972704b934e80893cebc5f<br>SHA1: c9282710de6c3b32b99c41013cd98c16ffd3a3d7<br>SHA256: 5a4fade1f7ac18c89a51c6549e709cff40959bf5c868caa5113c0985492d0a4e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.8MiB (192.8MB) – 3,412,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5a52499fde1d86e99410a901d067d1f<br>SHA1: fbfbe435e9a8b3ac6d7ef6e97213dfa1e6c61719<br>SHA256: b935070e40760f7f6dfcec31587633f717a13f0132c5a7cde3d32ae982cb2be1</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.1MiB (180.5MB) – 3,412,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f07180538e784ae730bd9bdaeca30d31<br>SHA1: 167cfb75265d251ed1655c917def02589bcbe873<br>SHA256: c9ec0e615374dd656969a712ebf0e013eb810c0ff8c2e2893ece5119f3e20a77</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>174.6MiB (183.1MB) – 3,412,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ac0ef7b6a9d7d9333fb93a48537da20<br>SHA1: 5ae5c6b51b9a898de6bd7b6c5286ea4a49a95304<br>SHA256: 47d200294fdd11f5ad0ceaf8c212bd59374eea472cf9e21fd4e5f149e9455ee6</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.1MiB (229.7MB) – 3,412,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a4246410e703dd7a83d5e6485ceb682<br>SHA1: 0f64659d5006b44cb42ecbf8b87c7cc39b2c6f73<br>SHA256: 79e86de0958595282a89380498936c19766dd64d290ae85fe45834b309e1a493</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.7MiB (180.0MB) – 3,412,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eff6247fc2640770614d380cf0d9da3e<br>SHA1: 5d507c01a6259ecdcc205d6115543c3decd274fd<br>SHA256: e2cd6d949faf979d4d7d3d188fcdd3d7f1c96f5fe6971c3ae81e1f01481827d1</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>212.8MiB (223.2MB) – 3,412,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fdb1a475ecb566b7f9ae13ce1da89e0<br>SHA1: 2123b70344fe2e52d04d87abd9f4e01cd91b9506<br>SHA256: 33fd5098c00e37c077e8a7156c1f6313e08e63b671ae117ee9fa06e6024ed28f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.9MiB (187.6MB) – 3,412,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac17dac8eb45e8a92d257be7d845e219<br>SHA1: a838fb95dbd9ad22b5af3f766c0ae5affde17efd<br>SHA256: 26a6e6a72b119e42ad941b651bffdaf80ea943ad90e9a4b20735e2ceaa3c98c7</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>179.3MiB (188.1MB) – 1,904,549 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 587b36608725ce83b96b33a3e53a3faf<br>SHA1: 0c31006ba05319f457d451ee7a6665b3622009d8<br>SHA256: 89a96b15c367ce7895d1f6c39a1262bf4180f2e5adf86c49612bc4de3579e28b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>183.4MiB (192.3MB) – 1,904,549 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74094cc924bee0fb5b7d3f88b296abaf<br>SHA1: ff3aeea6874ade9ae2c2016005258c769f907363<br>SHA256: 2c6bc335afbc167d320f85f96006e7497726303976623977a33c2ee7d72c9b89</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>177.5MiB (186.1MB) – 1,904,549 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d22da4939ebd4b909831d835ca2bd351<br>SHA1: 7de802ccf86faaf01d54a3230171e26a30dcdd29<br>SHA256: 226ce9e27f5cd3767d9f3ad7caba98ca75c69dfc6b4af1b1270b0d7fd12ece33</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>177.8MiB (186.4MB) – 1,904,549 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0be4ffb02524c869dd5141a76e9e6ab<br>SHA1: c834a52230bf677f78da637f7ac468aeaebda11e<br>SHA256: 6e6d0a91b6eb39bfb0edfa3463f1c59091a25e4be0b42b64d8b21d839be78b48</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>196.7MiB (206.3MB) – 1,904,549 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3441e2d9ea578b5f912c8647ea68bf38<br>SHA1: fa5eab02202f054f981102c53d9e9f23912b71ec<br>SHA256: 9ed3ce681b6739ec37735c1598dbc46ded11376202c97a0196bd1e4a44aef704</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>177.2MiB (185.9MB) – 1,904,549 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f66269ecb799126cd3b839b8b3a7d48<br>SHA1: 48e1af58939a472799f8c02f813a1efc5c90b0ee<br>SHA256: 288db633d462455d58c8895c9bfa178cb1791610cea8837945c838f82383ef5b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>197.5MiB (207.1MB) – 1,904,549 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8384666ae786a270c8793c36ebdbb5e2<br>SHA1: e887a904cf8511ab0d35af8f9b911610a363e680<br>SHA256: 0b7e77572711c8b3d7a67e4e8dd8e0c3f16467404b0d8baaf87fce844129f436</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>181.3MiB (190.1MB) – 1,904,549 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 324773b8c1747fa637e4defbd42e9d1c<br>SHA1: 19800e59541ce06776654d40f4a533c58e1b07e1<br>SHA256: caf34d3efd292f961b4b322fb901250b7f309afe52bcc367e2850e7c76b36df7</pre></details></small> |


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
