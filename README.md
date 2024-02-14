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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-02-14<br>IPv6: 2024-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.801MiB (5.035MB) – 240,366 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa950edaadb1b3c6dea5fbcdb649f821<br>SHA1: 746edcd6156f2fd551ce9d66437b53a7a3412264<br>SHA256: 3e537e0080c0e53b3dcbf031781b71b129f3c8a570108308294185495e199461</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.636MiB (5.910MB) – 85,645 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a890d34ee58e2cf885feff2322b649e<br>SHA1: 2aff03eb2c90d4aac3a8d9efa2d86450f02e8448<br>SHA256: 49d5c672ead5718a6f6c1d95f17e73c28eee6f0e9f1edd25d33853468cacc2b0</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-02-14<br>IPv6: 2024-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.187MiB (8.584MB) – 409,980 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 057d8748934daa34aee1213073b04c41<br>SHA1: db6bab2a4c0a50c3c6e616c50ccfcf67506bb307<br>SHA256: 38a92f8ca501278c7febdff35bd6289e6256d59c1353ae8431c8b0e9c5f01ee0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.971MiB (7.309MB) – 106,045 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc51e0bc12539ae4d2165f881e10e483<br>SHA1: e8824b8bd49cc8d9c353694166cc745694087ca7<br>SHA256: 8d75ae6513b91c02f9a5a9b79583344a3c141fd697670300156fdaaa1f81aa04</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.03MiB (17.86MB) – 852,859 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b863a641d9bb69e372afb8e2813a422<br>SHA1: 32193b91c66cb257a3294958fdcaa31652809f6c<br>SHA256: 88a5fdd3a0b0a825baefc10b06116da0e47a8c4a95f9e2220c821a51046aead5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>50.42MiB (52.87MB) – 766,244 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7378442e5e10e015c0b02c95e900c144<br>SHA1: eee2bd308e24c8f15b2111a27448a78b52bf782d<br>SHA256: c2de6f1e99584d966413a2acba5b6ebf2e5585f091e618c26bae6325fd9fbdf9</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 322,238 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58dc67267f460ea3cf5cad59cd04fb2<br>SHA1: d7cd4a637354f5a5c457e96633e1f5c9cc5c059c<br>SHA256: 55313849f9b0eeefb503ca58aa485ebe95d325c7771a4b2e5e9def19ee8aa2f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.67MiB (19.57MB) – 283,667 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b73dc10990e7bef8c444f1cde6991f<br>SHA1: 07ae49b41bae3e257ad578c4bf31ee8040ccf1fa<br>SHA256: 7ea6211e834aaf328302ede30e6777fc4f71afb40ab1238cf0af2be151b5b248</pre></details></small> |
| | | Full Location | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>179.7MiB (188.5MB) – 3,143,531 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4796f68669fd62ff1776c3d247e13dff<br>SHA1: 8d63c70c0bd62e8829cfbd2dfba8d6b8e6c77fd0<br>SHA256: 04e5000cfd1d52386cf975f825886bb214085c10b75c2568efa51ce70fb6c3df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>291.6MiB (305.8MB) – 2,831,720 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 657b58a340f82d12479e96ce7f695a45<br>SHA1: 1b9c4719ee91d1e9da68e6f0dd1529e893bf9777<br>SHA256: fbe98efa467387f6ceb69603459abde1562d03903aa05b063edc68d9aa4e87d0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-02-14<br>IPv6: 2024-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.640MiB (4.865MB) – 232,256 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fec6f73486236c8d0d94598e079d6f<br>SHA1: 7f19645a2e7ae1f5579b6769363477a0ec58e5f6<br>SHA256: 7f7145aa700bc6d9b86d8e430377fb6751efd3a786e0455999aabe3401d275c5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-02-14<br>IPv6: 2024-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.9MiB (177.1MB) – 2,925,251 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434c9a2a5a5c869e663a7e206ad5962c<br>SHA1: f2e0c48f3ecc7d10f4697a8c5c698e1979b08714<br>SHA256: 8d5321147896799a07280f735aae4be97a74bdd31110778527dc8f4b77485f61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-02-13<br>IPv6: 2024-02-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.434MiB (9.892MB) – 472,565 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 649a923a4e54a137d6549d4e73c90e68<br>SHA1: 03ed890709117a23b444643377214dbc28795cbe<br>SHA256: 671cdea0cd58c7f0fc704a33c550c3203f622960dcba153747c5289381b0e140</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.62MiB (19.52MB) – 282,890 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37d06ae2b736a8bf3c2a1e4effc9f6de<br>SHA1: 793fecdcbaa1f105c925b0404a3e2192981188d2<br>SHA256: 533e7671b9e745d6c5b128beac3151e5aca6ed6880d380e1815fb6d13e19955e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-02-13<br>IPv6: 2024-02-13 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>159.4MiB (167.2MB) – 3,387,567 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e327813a952e28c55cbb0fbe3bb6c3ce<br>SHA1: 011f074a22a7eadb9eb06de5dc8d83d978c8cd0b<br>SHA256: 63800933a72bdc9f7000a979b2c093c5d7cdc54b2a0e56aaeabd2b0b473de5bf</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.7MiB (194.7MB) – 3,387,567 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58ee5db45af221c0c66be9ae28bf27d2<br>SHA1: f0b5cbe5fdbe4ee1e86de4c76e64bf991034901a<br>SHA256: 27a7d415b6eb30a6b215c6aa870c47bbf9b4267430a79c293ff1e1373902b2f5</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.6MiB (171.5MB) – 3,387,567 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b82cb299ed0bc1bcbdd25fedf3724e4b<br>SHA1: 36f2df3f002c60ae4b385f7aa42d3a48c73534c1<br>SHA256: 045849f7380154e1e0134b4dc6b247362c71be82aebe2fd2d8b93c74efba77fa</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>170.0MiB (178.2MB) – 3,387,567 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2e3c69ead9bb4cbc72f29870b33e2ac<br>SHA1: da982703ffd56f18fd42b4b9acd559d4e71515b7<br>SHA256: cff6108ef9bba334de019f3ef955cdd7d805918a5408a494a7fbbda58c6a7693</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>198.5MiB (208.2MB) – 3,387,567 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5269de024438f4f0539a1c40ec965564<br>SHA1: 07b03de719b42a76c7bf7fe5713d8673878db72e<br>SHA256: 885d647092f0c1a04b4067e6e039ca137ce2f87d80c7e522c0c8fc51eaa180b2</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>158.2MiB (165.9MB) – 3,387,567 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1aa9620fe7d9535194452eaddde8ef53<br>SHA1: a9da00438353d1f53a2c8866b2aceae4e382958e<br>SHA256: 0ff93fce1d3e862457d5d7c858366d1f40b79397d94e02e7965352d573a9f169</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>197.9MiB (207.5MB) – 3,387,567 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 381e83ca8f3890742183e0021640b0bd<br>SHA1: 4ce4979defca50d6b335ef780f561357caef3d5d<br>SHA256: c235048daaeb02c0f96109653bd5b12d68f7a6f5bbb153cc538333d4c28f498a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>167.2MiB (175.4MB) – 3,387,567 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1672b26dbc99928ca02629a5972b25f2<br>SHA1: 7445e32a31f78a3aa0487475f04208ebca283fa2<br>SHA256: 27f8d13dafa54d1249a158b766e12e360e000d37b54c666c19d52efbad436522</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>106.6MiB (111.8MB) – 1,190,994 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ba6cbfc0066d14919f36138d5f8818d<br>SHA1: dbc3d477a08666c0377c26fa9005e336009a510e<br>SHA256: 09cac6d93429e99f0d6d7851bf2c2d545d5469fc331046b6df0c32fa39323993</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>114.5MiB (120.1MB) – 1,190,994 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b9c6405c8aaeb40a25f9057ad635b7f<br>SHA1: b197d109447bb2f03f0606518d1053749d4fddc6<br>SHA256: 5750f51f5fe83f8dd03526f47c0729d8a7cc8ef13e1c85542b7b16ca13327981</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>109.0MiB (114.3MB) – 1,190,994 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c271290f0f339fc921aa4c71ac1c296f<br>SHA1: a4b41a94470c63eec10f911a2edbad2014c057dc<br>SHA256: 8e9c95dc7e84be32437cfb7b64072cdbc8cc21e471ad16d8f3b525051a6236a1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>109.9MiB (115.2MB) – 1,190,994 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 770903b50818c873948046de7085713d<br>SHA1: 9cd7092710279bd07307285b8bcf6f85ab1b03a4<br>SHA256: 4ec8f32cd60b2fb1ce4c25ec9782ad4277d1b3ce01ee1187a87b3f8bcadf24f0</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>118.1MiB (123.8MB) – 1,190,994 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d5941e1fd92ce356c855b9472faa73e<br>SHA1: 1c1a62eef26cf0af1c48478050a1ab6cae7b5f90<br>SHA256: b575405b253a6505615038fbfaca3768b23a821873fc6d17c2b7c66f4e7dbb88</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>107.8MiB (113.0MB) – 1,190,994 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a55199781761226941bc8199f131de49<br>SHA1: a0f7ac4bee5b57c0aed37ce0d5364c7954977fd8<br>SHA256: bc9f46a9b9263ae270aa4bc46cf3b43d61af48dadb4cfcbddae450281221086c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>118.5MiB (124.2MB) – 1,190,994 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 945ab829147e6751f20f4e9eafe421d0<br>SHA1: 51e778d9200d15756a23eac70b9fec327a449480<br>SHA256: 874e18b572b4bfb847a815e44562f4be04af00a2c6f2289e8c7140f8ccc3a8de</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>110.7MiB (116.1MB) – 1,190,994 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91eac6e2b1415771cafc635b2addbee6<br>SHA1: 22bf12b4b8892f0841a8fd27e2e084ff305339de<br>SHA256: 25093fcf651e4103dd284d66cf7975d7c17121f77ae0d1f843ed794566dcfa2a</pre></details></small> |


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
