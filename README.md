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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-03-22<br>IPv6: 2024-03-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.815MiB (5.049MB) – 241,036 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a3961a8a388c4b6693fdcbd689a772a<br>SHA1: 58bf64e25af5b8d06b64355a1bdae2939994ecfe<br>SHA256: be13abc3bd0225946089850b7d633936732abef6d1b24174c7ce79ee165fca1d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.067MiB (6.362MB) – 92,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19f50bccd92acc185ebd3a33e65d0dc9<br>SHA1: ddd9b4bb894a40e428b15630a5696cf2125c9977<br>SHA256: e475fa8b91486ca80495abd80303a6328b1e04e634d5d7935c6898dcb420b1ec</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-03-22<br>IPv6: 2024-03-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.211MiB (8.609MB) – 411,179 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 553a6c0c414525a949a362e153ceb59d<br>SHA1: c049f90b99dc410823dafb65c6a40cb9653eba80<br>SHA256: 3405562c3f85f55ef0700fd951e29c286c3cf5574bf1c22714056c3a428f2a4f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.080MiB (7.424MB) – 107,709 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68487b9981a9a6ed595df5127779a357<br>SHA1: 543108ef2f41c1ee77819bd343dce8750799e5e4<br>SHA256: 081a1629f50f4149fd05fc0bb0568c46aef2feaf1b63299c611ac67ff147d956</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-03-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>18.65MiB (19.55MB) – 934,141 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1117b6c7efdd1e530dba7cb7fdb8751b<br>SHA1: a02036a669cc2993202386db5ca1d41f45d92392<br>SHA256: 8a3b4a46c5ab9303493be377ac49f09b6cb21facda3baf5e80fb3d965d0cfc37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>72.74MiB (76.27MB) – 1,105,410 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8510ed043aeff3d4842d7619550bd954<br>SHA1: f454ebbe28768dbab92bdd41831bbcde3866b3bf<br>SHA256: 1f769c0921c70e67f85c106d05c17df280b624c0e62d26d9413ebcb84b444366</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 322,326 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b232d78e18dacf266bba37244688a18f<br>SHA1: 2ea0bf2a68630d5c12c6fa1d18f2f3eb0845f297<br>SHA256: b9f2935f135d22119e5db5d8d8666980b07ac2e36359fd6dbdc9c26a8b3be2f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.03MB) – 275,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49241985f6153f5f100b60421257f25<br>SHA1: 51e0348aaa544a9b75aa17c9431f3745175c5c5f<br>SHA256: 3420806d6067a2579fe3eef92e4cd09b9b792cce9c418a3ca7f3c820f4edb887</pre></details></small> |
| | | Full Location | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,158,494 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd92465491c42b3844af48593793b1d0<br>SHA1: 53a3bac0d03e0e4bef95ad11b21c1a1e92eed9f8<br>SHA256: 6157eb8d8b93b5da65533893b6b1af8682e371476cd754957d56f3cfd1179aad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>307.8MiB (322.7MB) – 2,989,351 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a432fad1dde6398b8b6ee222abf32676<br>SHA1: 78d2ec063fa05a95bb17703a5111864cd91a5446<br>SHA256: 5974cc41b3872ea8fe373def59322db31b678ff8585a6e529b9737d648343c0d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-03-22<br>IPv6: 2024-03-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.826MiB (5.061MB) – 241,587 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53358947a90b798856b0f2491fbc6d2c<br>SHA1: 7c9c0c0ee1f075fe6d82ea2f7ca31f00a5b7ad18<br>SHA256: bf9da0021f243ed534ef8e2352a5fee71207c3b880a727cd5031b79c5c122185</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>16.63MiB (17.44MB) – 252,757 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05df7acc3edcfc49d6d0cc8e5b23185d<br>SHA1: de417cfa98cd08340a971a226b8075d8887c08b6<br>SHA256: e2904c3019400cf283bda389c8d7dc9f8c0b5dabc1bfd9dc40ea4326c79f404f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-03-22<br>IPv6: 2024-03-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.8MiB (179.1MB) – 2,959,758 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d837249426a59f38d52d9939db4c1a1e<br>SHA1: c71a37a88777bcc232ed0cec8b11f4b0b93ba955<br>SHA256: c25d6cf67e34fdd6f9b5042bffd4059449b156fc6b7bb6e3fd49ce1979642175</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>169.7MiB (178.0MB) – 1,642,006 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e91d25d35aa21837cbe8c01e725e1cb8<br>SHA1: b3aecd7e3f4493788fdc4c941a22f3f071cd5130<br>SHA256: fe72238b338f395cd55c98381ca41ebddfc893eb2bd92625551b9fe4d8d96a53</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-03-19<br>IPv6: 2024-03-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.630MiB (10.10MB) – 482,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f32de0e56e60a10cd083d0cc6a53be7<br>SHA1: 46a30582fd58367d5264200f79da55346cca696b<br>SHA256: c6d279f4f482bb841ad8c195beea6ef09285fbf2f436204cd84d09aba91fdcc0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.08MiB (20.01MB) – 289,980 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8bce7724ff44185e9f4d0603eca23c7f<br>SHA1: c1164ca894d44c5787c6a9b764b467688683cf3e<br>SHA256: 67740eb989927054baa49847888231d55f79bd535ef0239a8df9c598966cc5b7</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-03-19<br>IPv6: 2024-03-19 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>143.2MiB (150.2MB) – 2,875,480 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85ae514101507e1da2c93f70213f7e3e<br>SHA1: 91e29b048270961b9cba2155b7f365d1fa29388d<br>SHA256: 745aa442599a8b95acd5f23035098210c335c38ef5510f30c79dc5e7becfe7e4</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>156.1MiB (163.7MB) – 2,875,480 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3327443c5ee4adaadf1a54a2af610d0b<br>SHA1: ee28cc8835ad2a7f37c8d6ad71d918db7c032716<br>SHA256: cdaf3220c74b64ad3a34d28ebe269b63944c013c39c38ed4bca7046be4da2452</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>142.8MiB (149.8MB) – 2,875,480 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5050b1106c855a91a6961edd4a2d643f<br>SHA1: e06509d7b5aafc3ddfafb6e8f88309c9819c8884<br>SHA256: a66bca332786db4d041503ae34df379f9e718fdaa68624163accb389f2a6ab75</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>145.9MiB (152.9MB) – 2,875,480 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 931de88ea7105464045251687af6025d<br>SHA1: 7bcaf0a0aa649b8a657c5f0096e7df4deb6ad4f6<br>SHA256: 4f41a770d14f3c1819019337b734b734f92dc061b4800ac87d3f20e41523eb97</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>178.3MiB (187.0MB) – 2,875,480 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58b61a917d258fa10ba486b74299e6a4<br>SHA1: b69cdcdd66e900adee3ca0f2e48ebb8bf4471174<br>SHA256: aec9842ed9229bc425a9ee2275c48f0c533bd6825ad90616792cc9f97984e734</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>141.6MiB (148.4MB) – 2,875,480 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6f4215b7e231f0732050525e9e0af46<br>SHA1: b70db5478595234f9d2432213ba613988dba1357<br>SHA256: 0e28d1b86020ed6c421af8dbddbf8b72089096e92e9b732f0be71e13dfabab1c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>175.2MiB (183.7MB) – 2,875,480 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20ee87faf7fe243e20a76650b6dd4498<br>SHA1: 93f915e2a45715e7cac74fcb97c468f04590f1d4<br>SHA256: b1b4c0a889e690b21cd683f6b8772a668c25a01afadead56f5089e559bec8072</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>146.6MiB (153.7MB) – 2,875,480 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ab88a8230d01908b4e37617a191d1a0<br>SHA1: 132425404b0113c46d6f7516de95edaba551e7dc<br>SHA256: 79e59b342b4b9e0b2f8e20028a95ce7f25c91ca36eb39688690f8c47bcbd6776</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>112.3MiB (117.8MB) – 1,213,700 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd7dd4610d1703827902897a2e508be6<br>SHA1: 7d5f957d7dc0138a908b31de4803964fbf784194<br>SHA256: 3c3b9bbe135b058ffc0594cd55b96cab7bde793f90217eb4ae91501b95f8d991</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>116.7MiB (122.4MB) – 1,213,700 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d534bb369c014ca4621a891981cfd180<br>SHA1: 38a175ecfa784fb6b2547f0ef7fbc98e91e496b0<br>SHA256: 024d5c06979f554da67d378f4f232dc4f6aea2049c20027ad22b03f4677a766e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.4MiB (117.8MB) – 1,213,700 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44d29aac068273a65def4256e9bd3b99<br>SHA1: 2277277839f633139255e909110a715faabf7552<br>SHA256: ba20d262306722785351387558d27f1ece301a8cff7c82d597ae38697077d55c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>113.0MiB (118.5MB) – 1,213,700 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d49a30854430ccf8fcebcd24b05541b<br>SHA1: 1c0939105570c5dd23440ac6a40ce41ae74d38a0<br>SHA256: c69a5269e30bea2cbecfd9c2956bebf8b92a7e9a55a267e6788f37658d73142c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>123.8MiB (129.8MB) – 1,213,700 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 306bd3e619c3fd87d7c577fe78c01159<br>SHA1: 78a61cf302783f21249f06bf108e917c50cf4728<br>SHA256: b00e7da83bbc9fd0ea628ca558b3858c57e1af9dfd49d986d8ec2503935ec29c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>112.2MiB (117.6MB) – 1,213,700 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07bc9a8749a9b3ac3127801c74c1af2c<br>SHA1: 987c67c5b73f58f3a95509451f428a47f40d4055<br>SHA256: 24b167afa44e5c0410a9da547c48d2e1c7dffcbbb82dfc8e3a7f39947acdd1ef</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>123.3MiB (129.3MB) – 1,213,700 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cca4f2baa5acc625fce89e8e50b52e00<br>SHA1: 807a3864d57180f78d48abe49353e5e47b5772ea<br>SHA256: 706c48191e9f87d7cad2e7708954fdd6b00a747c24ecafc813352e234f9fdd76</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>114.4MiB (119.9MB) – 1,213,700 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0be0e0bb91cbd00e40b9d4cda7bf3d4<br>SHA1: 212024e91ed194c9a2c6e44de7bd001e3011fe5f<br>SHA256: 1f506add5333f05fd2886748871848287c2ead6b5182a764de4d7141372bfa7b</pre></details></small> |


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
