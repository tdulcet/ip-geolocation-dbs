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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-01-26<br>IPv6: 2024-01-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.790MiB (5.022MB) – 239,786 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69efcee4cfea86197de6fd63f0ae8296<br>SHA1: 9df38c53533d0afecc91df3e85815267856de0d4<br>SHA256: e593880045409f487c8d81d390e5b04d1cd0713b99a6fffb02d234c9e10ff05b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.560MiB (5.830MB) – 84,495 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ced91e0ada90cb740b913cf1617b6ca<br>SHA1: b135abd77c6d1499e67bbc8bbdd17462c2ca02a7<br>SHA256: 41e9e22353100fab4d8e1d0fe94fe80ed19f4c096484f9ef771c5de0ecbe79ee</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-01-26<br>IPv6: 2024-01-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.256MiB (8.657MB) – 413,443 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e57fd0f7bb392e775abc801af02909e<br>SHA1: a773972a93970e570fcbfe6c30c45adbc15d1101<br>SHA256: cb12db813f8d6b9740f1554e851a3bab61b28a8a2a1a729f8a18b30f084d331d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.917MiB (7.253MB) – 105,234 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f066eb9e89d6aebb2614d7039538e0a7<br>SHA1: bb896487225b702caf1605d018e0ca2164b738a3<br>SHA256: bfebb4c8790a5751a30171d83a69811394c10a69293f1e61eac74d9ee5393564</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-01-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>18.57MiB (19.47MB) – 930,033 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7aca21c841864b2645d6823642ad4fb3<br>SHA1: 8a1af36dd10ef212553c79434444f3a2ba774dc5<br>SHA256: a104b0a51042a398e4114516266cfc4556c23cd0f2e6b6566e0230631f5ef869</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>52.64MiB (55.20MB) – 800,017 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 893253d9f437f36da854054d25c25aad<br>SHA1: 7fa52b85b7b5072a94b77e60f6a2fb7b96058c59<br>SHA256: ef87549fbc3e5b08dd6a83a80b3241b18f2f23831fa5ca17d4b0eb35353f03c4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.162MiB (6.461MB) – 308,408 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736158b820db1062b003cfce212076a4<br>SHA1: f3b03108eb0edf83c338abed05e010c2b0e9cde1<br>SHA256: 68e446a0380ab263a21743f68ab8aa6b249b213af0d6ffdac0780fe4912cb7c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>21.05MiB (22.08MB) – 319,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73819723f00de32c17c8aeca84d93383<br>SHA1: 71d954fffd9f9f5979ff89981fcfae6f73cadb05<br>SHA256: 1328a782f89b58d1f6fabcf3542ce4bb259d89c1f28a0cc70abfe70b5e573eea</pre></details></small> |
| | | Full Location | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,096,472 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b990a48af772fbc4cf7093aa51d35b4c<br>SHA1: 8ddfa8795c4c534c0bfd99b2472382b368d7fd5c<br>SHA256: 117938f84386f9ca627464e7c42856b6d9ff4f68bbcac12a393b73ea1ac0836f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>243.3MiB (255.2MB) – 2,358,639 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c61e48446e598bab5cfa16234f5f136<br>SHA1: c3373a6fe2e2f8e08a48274939c4b494fb99b5f1<br>SHA256: ff81c189923d299847f5b5e0e5c472fe10d836d11e24fa5379a2def67c998406</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-01-26<br>IPv6: 2024-01-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.626MiB (4.851MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24caac24a9c72bc3caa6451ceab08833<br>SHA1: aa114043e64d74ecd9e8ccd339b80c62d3fcbabb<br>SHA256: 6d48a0384e6e4d38820ac8d2936c12db7eb726dfe20c59600d4f14d173e3b15f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.10MiB (17.93MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fc970b50f7b01de0d0c6bd29224c13<br>SHA1: cb1fe32e67d0561cefef5f2908570ae3af446a24<br>SHA256: e0f36200f10f817a89b6cf80d8d459900c5428a669cc706af32d15b709a8b624</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-01-26<br>IPv6: 2024-01-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4MiB (176.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4104f39d8c379ec8967157286f495717<br>SHA1: 440c75c20491f104948897ce552c95510badba7d<br>SHA256: 6689c6e63153fcbdc00272e2ec6cf04f0c6877860b4a667b3972dfa08c898747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 142dfb0f4dc0ceb4f5a41b018ea53524<br>SHA1: 284b510184f46179e9e34f60dd0db14fc72f3e50<br>SHA256: c57159c9a8879702623a2ef4d0c2fad06d21e96f1836db2d3a09f9216aee1641</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-01-23<br>IPv6: 2024-01-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.383MiB (9.838MB) – 470,001 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f66c59e4eba0f05d3a93846528db588<br>SHA1: a492ec0a7ccf27c91dad591ee8dc84f47dd3c2a7<br>SHA256: 2129a98c051ecc15c559b8186aae04f8d9b362dfe3835c83cbd93de31bad1785</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.86MiB (19.77MB) – 286,576 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45d9b5b9d58451646fa8c765ab0fedc5<br>SHA1: c20d66ce15e9701f6d02143cb4745cc4174ee13d<br>SHA256: a9c2a6ba3c813892e39916d5c2a17066c2968cfb694d59432d88c8a9c8d89344</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-01-23<br>IPv6: 2024-01-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.1MiB (182.6MB) – 3,694,535 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e97e98777a225b28213fbe0d1f04a881<br>SHA1: 6f971fc392b08604ad92791bf2480d04740c287a<br>SHA256: ef254394b54ddae739b18a49e8571943baa0e4317ae2efdeb461cdd58f455d87</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>203.4MiB (213.3MB) – 3,694,535 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ac86394010a460902a139745f1cb43e<br>SHA1: 3a631724e40887f037663bd51dae2bc0675eac65<br>SHA256: 1a3a307c215c88c82dde84427c4250eb19a0e3c78b0aaa2bfe0d8983b5fc167d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.8MiB (187.5MB) – 3,694,535 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2794b6d7424132ae07a499f9d63e674d<br>SHA1: 962d2eb67b30cd101e44b0e4033a12746b4fa9a8<br>SHA256: 7176133c4356aa6b7942f5d0c97d5f8513f04ba796015a0789a84e296dc61441</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>186.0MiB (195.1MB) – 3,694,535 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 606a0a29eddad2288082cc8c850ad93b<br>SHA1: dec9af459a45e227e17ea4f47e1822fc784c6acd<br>SHA256: 46e20b7448b630cfc56c8e96938560befcec428df7b8593e67485742d2ec172c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.2MiB (228.8MB) – 3,694,535 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bf9bbae984a966ed8c179311ce34d50<br>SHA1: 7ced86e53e6f79e39f58318561cfb09970908e2f<br>SHA256: 25d9af573159bc04b01cb7bad9074bdbae53133f00879835b17ddb89f3006a47</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>173.1MiB (181.5MB) – 3,694,535 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10ba3159e5b45bc65deb693ea0780a65<br>SHA1: ca3321826fb007ce81c21e3becb8b63ce6f22b46<br>SHA256: cdb23ccd6cc69a27d17820162afe82e62794bdd99bcf84438a4d21041be5a6f5</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>217.2MiB (227.8MB) – 3,694,535 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31ef003ff55531c62c622e3c921d2474<br>SHA1: a7cfb39b9652d10f2d7bdf3eabca5f4f884537c0<br>SHA256: c9df1a336ab6062e20ead754c3b7353a69d9ec32d713fbbc5add49cc03be5f8d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.6MiB (192.5MB) – 3,694,535 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33fe644dbebfabb3693258cb84c28bd6<br>SHA1: cea04bc187c3f36633fdd3e18af18024dc717fc2<br>SHA256: c2c8d785730f602752065626c337a0243cf3001706794846556176355a617132</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>107.6MiB (112.8MB) – 1,204,546 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b28433d7bad21f9a9c9b0b05ebbb6d48<br>SHA1: 35e734ecd93a1000014e0da4175e0264b45ff548<br>SHA256: f09bc0c219ae581027b319d7cd1de958450764c61626c4aa5806cbaf0cd0f54b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>115.5MiB (121.1MB) – 1,204,546 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f987d877dce2863540b02c9633171fe8<br>SHA1: 0eaa0b53dd6c07f860043a34f082b909a7167979<br>SHA256: 1a98e9eddc4229123da90edcde77bf21aeb5135422b208f11bbda5c6c1de70c0</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>110.0MiB (115.3MB) – 1,204,546 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e7b36646137aa0c6091ab5992963398<br>SHA1: 6a863b4bc501d9935c530563b870be3c03827359<br>SHA256: f277688b5703cd3c6b394c69ac080505db5ff51075eb74a34842a2b8813b8575</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>110.9MiB (116.3MB) – 1,204,546 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79d504789da7b6a371ddf298a679737e<br>SHA1: 1b3709f8d95f14439092eca161f215ca95217601<br>SHA256: bc7e6b9a6d22ab07a1f8924cbbb98007db6f687f62400aa15a5ae4132e472b39</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>118.9MiB (124.7MB) – 1,204,546 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c21ac4463eb43b11599da44bb2cd3fd<br>SHA1: 6824842a053a7ca44c2d52a1ce94eedea4d37c4d<br>SHA256: 6e3a2892ec28e4611eb2cd88201c737447e1a7255b522950b44f031a0832d7de</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>108.7MiB (114.0MB) – 1,204,546 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f216737bc04b286361a570658d767d38<br>SHA1: 4b0d466bbf01b012774cd3accdefd31724b2ca2e<br>SHA256: 58dfcab9547fc02d05201f253d0f79b7edf9e1068588d7558b5e256edce7de77</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>119.1MiB (124.9MB) – 1,204,546 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f44b8d5987fe13c923e26a92fd93564<br>SHA1: 3eeac4052811b05451d0d61a07da32d1915d2ed9<br>SHA256: af7dbd25c00348a6bf741a4371424cd0dc4d885595dce74864a130012c191c29</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>111.7MiB (117.2MB) – 1,204,546 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6674e10e90a165c4609050c9a8b1372<br>SHA1: 37764eef3330a69a47bfbe973cd622f92f5f2ff3<br>SHA256: 7c2d98d5429415535eee4e84b2ce5a6c9dd38d4da06a65d5482cb4c36af8b5b1</pre></details></small> |


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
