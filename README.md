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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-06-02<br>IPv6: 2025-06-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.260MiB (6.564MB) – 313,502 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0c5126095394349202f112d868ebac0<br>SHA1: 48ab4b35b033bdec1c490410875a623a4fc7cb77<br>SHA256: 08b5f0db8e6c3714a40881c1f02ecf7a2882659db2f1f459461bbe799c318525</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.28MiB (12.87MB) – 186,577 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67a5f31c3458574b33c84c264a4f6d4f<br>SHA1: e01aaa9d30ca2b279916b02495ca22adaf31b8a0<br>SHA256: 57d931679b28e4590eb000c5015c7f59ed18d12594fc53db02dcef0b4d814971</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-06-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.88MiB (13.51MB) – 644,838 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52001ec39e32fe34af8bf5f5c49c16ed<br>SHA1: a7b703a7bd266f1d433b4d25e65246dac51ea5d1<br>SHA256: 31e10d1b7d83bf65a0a6ad8a1e463826f48f768597aeaf46c1d97fd842e6cb95</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>98.13MiB (102.9MB) – 1,491,322 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3620475801a103edbf1c52a3c44b4137<br>SHA1: e7890689c4e5e2f8586293b9ad75b8d045468a59<br>SHA256: 2e01d2e9cbb3d926af78597f3c832d7ac3e07bb0d80c306b832acf12d91d667e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.020MiB (7.361MB) – 352,022 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5d6ce30939ecacab9e5fbbde143dd7a<br>SHA1: dbe45e91ef39b1de3ae5caecefe6dce72faff5e1<br>SHA256: 843f29bd3db6468809b0042da7a6b44aa5aa0f7b3378bce2344b427d7b8b2458</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.50MiB (17.30MB) – 250,746 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86b9bc39132e2d99653445ab24f13e89<br>SHA1: 04cafe97346c96dfaa2a0c192e271c1aa18bb99e<br>SHA256: d337bc1e4ec66010e25e0e0279f489bc7bb3f2218829c1b952e7b21620faf6b0</pre></details></small> |
| | | Full Location | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>189.6MiB (198.8MB) – 3,310,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1255823f4fa6d96cb2339938032ec17<br>SHA1: 7bcb7165d5248f918857090fad507b3b62aff99f<br>SHA256: f33143e90c472ffeaf3431c1f790ca9297c4fcb75c4f9b48690bbe6cb9d79c80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>401.5MiB (421.0MB) – 3,898,653 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50981857bc3865133c307de9e8f457db<br>SHA1: 915f84f9ac8ac491a0dc82f8e1c8a8b51e82b9eb<br>SHA256: af893c4ae1cfc50fe6b043a92e1ececd960d30f00aa8a0067646fda960aa8ddc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-06-02<br>IPv6: 2025-06-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.060MiB (6.354MB) – 306,250 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66813478af08592fdfc48fd31bff150b<br>SHA1: 811a9109b04c7e248ec3039089a3534799a0b45e<br>SHA256: 7438026d984ce77dc6a3c83ea0623314e8e04ce52f031ecb819c2211c10dda60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.18MiB (22.21MB) – 321,882 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dc7e513e52e0755f6fdadbaacc17b5a<br>SHA1: c9ee76ff47638d91e8db56f68fe6b0d1ca2f6cef<br>SHA256: 35bfcec7d2598e67771e9d918023c4280f9109650acfb7bc6d7776c000fa7505</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-06-02<br>IPv6: 2025-06-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,073,788 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5842c1e89d9e6a7ace62a726c41126ac<br>SHA1: e3950375fff9f4e7a1b551e841a320f17e1763f3<br>SHA256: 136c0e48f44d563e0a01829656f7c14024757ccb342856959d0a6797ee9afb85</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>243.8MiB (255.7MB) – 2,366,384 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e93be5d64be521626b8e98eb9c04690<br>SHA1: 8491599042ab2c0661a6d9968a86b0de5322e2e2<br>SHA256: 699e1f5782b93d7acd864659595c72dc1e8bf20e3457b3d9fbe5503103a35841</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-05-30<br>IPv6: 2025-05-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.91MiB (12.48MB) – 596,068 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c70a9121b62848f78c188d4518c5bbea<br>SHA1: 4248e418915199225cf0605dad8e18f5226ad9ea<br>SHA256: 3fa9a9022fe956cc85041934e96f29a88de0135dab7b53aed35a228c40440af9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.68MiB (42.65MB) – 618,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26f094e07e93b5f0dd41bdc197728e2d<br>SHA1: ab01322a23bfca27e8298a266f9eb68d3c9673da<br>SHA256: 09135653aebc777c0e0fe758c0498b56e4c777f56450b78dd81a9aa06e45a272</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-05-30<br>IPv6: 2025-05-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.1MiB (180.4MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec8c380f0bb9d9a5a9df1a1656d12909<br>SHA1: e49abed65d5686f50a4690535554bc3c106afd3e<br>SHA256: 09ffd7c64f9322d09cef37db31720d0359a57f9c520d0207ec8ae721bd528e41</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.9MiB (191.8MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e54adc160e27c57e0681e8edb14b2611<br>SHA1: 2be26e21011de5e241b7d9d069f467ebc48deea0<br>SHA256: 9a3b728598118194641eca69375e5ec1c56c02baced442ed26aff3ecd2c76c55</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>171.3MiB (179.6MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d975b556d13cd6f30371004bd50a0e97<br>SHA1: 672ee5e17d95a2e7759db9ff5b6b788a71a79d80<br>SHA256: 7b550b09daef994865de9ded2988bbb8685b6c398a3abc20de0cb68523a34402</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ac4bdb8d7e03018f65fae8ac00a0e9b<br>SHA1: cfafda6745f9a0bbb0e028dac6278d0894f52b92<br>SHA256: cefe3c4a9f362f800b6cb41d3b809d0b1c467f8b9c2f2f42c43f54d6892d53ea</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.8MiB (228.4MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67dbbc7775ab424339c8bea59c30e70c<br>SHA1: bcab2b3e8d739a942f4c74c07cb98060eb41780d<br>SHA256: 5b8daf8293a764e4e39e33fcf71b1a09bd31f95763ba605b243c3fd92094d309</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.9MiB (179.2MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c24d3ae69a8e20ddaca17b43231cc5b8<br>SHA1: f39e39e8c9c750a93546ecd1fda61694eb3b2d46<br>SHA256: 9d49c912292edc866e2a4a66aa030831f1b9cae53a4d887db0b3a693e2f48c2b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.6MiB (221.9MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf3bbbd5afc31fc3539579ee922256fe<br>SHA1: 968417c9d2a08367880eb89cec5424da59a50e91<br>SHA256: b3b41faee721f206978ef6d4bd85f7402ed54b4d132269f061eae1a1db3976c1</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.1MiB (186.7MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5a4d078c50f53421ad27bdddf569491<br>SHA1: 6f9ebbfd3df09400494e0b84e4183e8881c4842d<br>SHA256: 99fe222524141845b1d1044f957c452c838f36437c44260453825c83f85f32df</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>175.1MiB (183.6MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32c2ed691bc9169ae014b8fc9dd86313<br>SHA1: 4b069eb66bf31d66c444c514f86e1e692717a023<br>SHA256: b418313c5f07b6415d7f8ca4da8e59d0428f354f82e7e30eaf0494ca4b70344f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>179.0MiB (187.7MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25ba6b014f5190f1d9b38ae3f4810707<br>SHA1: 848de216ca055e32c8224fc473ab1e49a620e0de<br>SHA256: 35c934f1146f11b062c41a8879afc90848f2ac8249af66f9ed7a91c3d39f8ceb</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>173.3MiB (181.7MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9773b212f3ed70cef0173bcafa63dda3<br>SHA1: 7b1537f6ef01a8d115647f49ee8d01c810297cb2<br>SHA256: 3c471ae7bb78884a31beef3750e38a810ea9da3b8e29d8a8e42d291b9cbe1af1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.5MiB (181.9MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63182c214fbb0daf49c574493c5d3e66<br>SHA1: 06b01ce9877510b98f960684bed99bfd5f3bfe5e<br>SHA256: bd26f8730807e4b82c811026672bc35269b381a1cd62734d683817add0a7bcbf</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>191.7MiB (201.0MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97269922f2a231889fca4cb7433e2c51<br>SHA1: c1c1c0232735d2b5d3760117cb2899b91ed45d34<br>SHA256: c1776814f12a725334da7049057871858eb83c87b3cf1baac85b2b2a338bfbe0</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>173.0MiB (181.4MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf2c28397a5672784cd887128a2f7e19<br>SHA1: 55f49a9e42231063ca1a7b8373267c6223609dd4<br>SHA256: 98939cc079cecb280b09cb4448f5c0ed3135771b4de574144f0a55c9961f5a21</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>192.6MiB (202.0MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec9b47d9c303460924151ec0a39cdb63<br>SHA1: 8ca056e2b6fc1a335168a36df009bde1bea932ff<br>SHA256: d57e193b0779e70123bee36147ae2cf80c6de53b08bc1ab59cb7492e5739908d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>176.9MiB (185.4MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1042618f8a21b1b4d7f58075cc514af5<br>SHA1: e23328876c74eb40028ec5e82f1022e1d83a3380<br>SHA256: cac5dd9725be13c3c214b85955147bff4bf6c0d5f6df4f6389073b4496a9bc0d</pre></details></small> |


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
