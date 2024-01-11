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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-01-11<br>IPv6: 2024-01-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.776MiB (5.008MB) – 239,114 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: faf82c13267cacdbd07ff7475c9749b0<br>SHA1: 63bf6ed6940516d9b607c98284fb35aeb0436e21<br>SHA256: 7649335c57a2fb4896f48b869fe65dbadfb553d6805d9b9baf4461f61cff4b60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.473MiB (5.739MB) – 83,170 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55692d66c70cec26ce6ee3ec69e1b03f<br>SHA1: c2a569ddb8adad6cb22d9669b8a9f43b434f85e4<br>SHA256: dc56d8d6de9a424db9bfcbedf4fc36eb6376a843341df44dd550a55cc78b26fc</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-01-11<br>IPv6: 2024-01-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.241MiB (8.642MB) – 412,698 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d50ace4d55da90ed82287235d324a520<br>SHA1: 751289af72242e88bffb4c8e4a0fccede5cb0b5e<br>SHA256: c55a1b1d623f96381109d8692f8b22736eb0a2f17cf5ec4da46da7ace6f9eb51</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.905MiB (7.240MB) – 105,048 rows – 226 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82ab6718bc5fee45cc6a2e658345d911<br>SHA1: 19f0da2bd1f3a3c28d35f558e9c4a066ec1d4f09<br>SHA256: 8964afac43449708fddb9a33c85457864c0e6c1449783353e7ff5435dbd06a63</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-01-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.57MiB (17.37MB) – 829,513 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 942d5336188591ea8b40f3b546193c46<br>SHA1: e672c0fdbc47ae21e94c2b480aa6adf5c1883582<br>SHA256: b01c938d267adab60e98c486a10f0cfd75b3306a17183c57441df212b3a61ae5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>50.66MiB (53.12MB) – 769,834 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c49f95aa9985b2c56dfc9b4da9ca08c<br>SHA1: 08d856a45b3152b0c33d703f8cba0053898d2b6e<br>SHA256: f73c2f0bc80b3cfc63bcb9712fceec42dd89094888fd3b07f76a7754b7b9e207</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.162MiB (6.461MB) – 308,408 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736158b820db1062b003cfce212076a4<br>SHA1: f3b03108eb0edf83c338abed05e010c2b0e9cde1<br>SHA256: 68e446a0380ab263a21743f68ab8aa6b249b213af0d6ffdac0780fe4912cb7c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>21.05MiB (22.08MB) – 319,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73819723f00de32c17c8aeca84d93383<br>SHA1: 71d954fffd9f9f5979ff89981fcfae6f73cadb05<br>SHA256: 1328a782f89b58d1f6fabcf3542ce4bb259d89c1f28a0cc70abfe70b5e573eea</pre></details></small> |
| | | Full Location | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,096,472 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b990a48af772fbc4cf7093aa51d35b4c<br>SHA1: 8ddfa8795c4c534c0bfd99b2472382b368d7fd5c<br>SHA256: 117938f84386f9ca627464e7c42856b6d9ff4f68bbcac12a393b73ea1ac0836f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>243.3MiB (255.2MB) – 2,358,639 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c61e48446e598bab5cfa16234f5f136<br>SHA1: c3373a6fe2e2f8e08a48274939c4b494fb99b5f1<br>SHA256: ff81c189923d299847f5b5e0e5c472fe10d836d11e24fa5379a2def67c998406</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-01-11<br>IPv6: 2024-01-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.626MiB (4.851MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24caac24a9c72bc3caa6451ceab08833<br>SHA1: aa114043e64d74ecd9e8ccd339b80c62d3fcbabb<br>SHA256: 6d48a0384e6e4d38820ac8d2936c12db7eb726dfe20c59600d4f14d173e3b15f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.10MiB (17.93MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fc970b50f7b01de0d0c6bd29224c13<br>SHA1: cb1fe32e67d0561cefef5f2908570ae3af446a24<br>SHA256: e0f36200f10f817a89b6cf80d8d459900c5428a669cc706af32d15b709a8b624</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-01-11<br>IPv6: 2024-01-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4MiB (176.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4104f39d8c379ec8967157286f495717<br>SHA1: 440c75c20491f104948897ce552c95510badba7d<br>SHA256: 6689c6e63153fcbdc00272e2ec6cf04f0c6877860b4a667b3972dfa08c898747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 142dfb0f4dc0ceb4f5a41b018ea53524<br>SHA1: 284b510184f46179e9e34f60dd0db14fc72f3e50<br>SHA256: c57159c9a8879702623a2ef4d0c2fad06d21e96f1836db2d3a09f9216aee1641</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-01-09<br>IPv6: 2024-01-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.268MiB (9.719MB) – 464,305 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b669397c9e0bc9de55e9f2efff3d6ff<br>SHA1: 80e63edb422ecd2be65d961e12fb382f502a3f6c<br>SHA256: 5b12c3a826c74eaa51f3cc706021a87e90e1298ac90bbe66bb83c33e6c953a9b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.41MiB (20.35MB) – 294,936 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20f23ea1f0ff2fe0c99c2c62ec542466<br>SHA1: 152d9f831100b976742c09a99d353f32f4fb73e6<br>SHA256: 70cb8d31ef9c18ce2b9ebb080fc32d84d4f99953f32646f4200ae249db0ccad5</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-01-09<br>IPv6: 2024-01-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>161.4MiB (169.2MB) – 3,437,604 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20ee1054d7681c4d5a34f3d760112f07<br>SHA1: 18a17de8227b56d4215e9ba92384262f32c5f085<br>SHA256: 40f70381ea4df92fe87258ccde45f6ad9a1693956751d2b2ad4a09153ccaec27</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.0MiB (198.2MB) – 3,437,604 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e502e99448b47fecbb6cda67cdb0c613<br>SHA1: 21aba15d5888dc2261240838b3455b2b95286ec5<br>SHA256: e3beb1694bbee417155c9aad25cd0ac7114392965ac9eccd2ed1aac996bfd55f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>166.2MiB (174.3MB) – 3,437,604 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a3248ce0a24490244ecbf2a8a9ce472<br>SHA1: ca93d9de7a0794ec4b4e7391e6a18cd729fd390e<br>SHA256: 9d449a3930cb213d774b5b18fdfd4aeacff027334f52ab1602487bc1987e1685</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>172.6MiB (181.0MB) – 3,437,604 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98b73b38844fdd710903f03f621fcd32<br>SHA1: 6190d91c8cc667bc17eb28f0d7a7c8030e8a999e<br>SHA256: ef83bfbdc5bb2b4d0c300c0e4eab7f4070c322835c44e7236fc49d5e51deae16</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>202.0MiB (211.8MB) – 3,437,604 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ebebf8804a0d886e622fc198584fdd0<br>SHA1: a6c0fc41efff038841b5e7f14bd4b1605b2a1b6d<br>SHA256: 56773f5190c3e2db2012f510394a3c3e9b448b6e8d544d10c39ebe1b1db0ee7d</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>161.0MiB (168.8MB) – 3,437,604 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90990c72ebb7932cbaccb3c939ef1f1a<br>SHA1: 35535b0a3eaa431b1460f4172677d3a135a142d0<br>SHA256: 6a339b282e97fa70953a5a459e40a5daf325df3c17227cfba8693dae3cd4c6d4</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>201.5MiB (211.3MB) – 3,437,604 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87a16b20bb46a4917427c444ef77c632<br>SHA1: 0319323b9be0ac21dae040d7c4e567a455b9d6d2<br>SHA256: 05a6a38fdc5f5333c995b348c150489e3d697ee30d0e2a39c972709595338ccd</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.3MiB (178.5MB) – 3,437,604 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 137786bcd1a9bde3257299a3ca526a53<br>SHA1: f4c443720a3d9895da8e3c911e44c2745ed5f164<br>SHA256: 4610382500f245f3825f8f9be89f9cde838b9023ea484108705e74ae77486785</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>109.4MiB (114.7MB) – 1,225,837 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dfefb465efbd0e06912143e886436a<br>SHA1: 49bc53496b6d25a97c30150dc36dd208a0143582<br>SHA256: f0d16842c7beaa0231692198a422777920fbf0efa01ad435dabb9dd493a85b30</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>117.5MiB (123.2MB) – 1,225,837 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52ff65e0735b302992c351cc48b3b4a9<br>SHA1: acd8519cc7fc639b666b58d749dc7a4ea8257c76<br>SHA256: 1b45836aed64ea26b86f3eb5c340035d8170291fc84019b23f85b9beedacec13</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>111.8MiB (117.2MB) – 1,225,837 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aee174d55002ec1f9de180679a9f79ce<br>SHA1: 33a4a9f1f5aa21cac9ae15aabe481c58d7a202ef<br>SHA256: 85e009ce244be0779ad2906556037b5863de48898f35c54430d9a4a769ac2925</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>112.9MiB (118.4MB) – 1,225,837 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69aa9d299215d85a6f489ace47dfc94f<br>SHA1: aea583397704a0816f299a97aec35521fbfcb8b2<br>SHA256: 6203f80c8a647b7ebde1dfbc60c2d2096d5ad56dae9eedc5d515fa99bbdd0bbb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>121.2MiB (127.0MB) – 1,225,837 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bcde83574ac4d8d0da564a5456779cb<br>SHA1: 223feee9bd639e5d7b3dc44dc2dff4bb7651b4c6<br>SHA256: 87c1aec666710418c6dc2a39a68ca2e6d17efb1673f5112da100bf29f36283f7</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>110.6MiB (116.0MB) – 1,225,837 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fea79e73e0c0f5cb35d39f2b7a833426<br>SHA1: e8abf29167d77b7cc78904ce8437831b73a9951b<br>SHA256: 379070be46127c1a470508913c29b8f323c824e36b6d545d990a96970a6a627a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>121.4MiB (127.3MB) – 1,225,837 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55511801b017e68932905752924a9f06<br>SHA1: a4f297826ae381e28b173dd1a3b9d20e498d335d<br>SHA256: db6030c339cdc56c8035903924ab3c796d550b70d100803c756b3459f936258e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>113.8MiB (119.3MB) – 1,225,837 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1149e572815a06277bbf57e8afaed508<br>SHA1: bf550e1d72e32acf76a021b3d9584fb6467e66c0<br>SHA256: a083a7adcf1cd53e8c9c70c5bba090129cf3602c30292992b1a7ca14bc199ddb</pre></details></small> |


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
