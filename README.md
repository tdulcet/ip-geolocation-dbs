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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-09-30<br>IPv6: 2024-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.634MiB (5.907MB) – 282,056 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f50142c6536f9eb78874aa5f128e7ee5<br>SHA1: 7bc61c9a5d0025f190d69beb8695856326bc7283<br>SHA256: 0311605cd25b6b40a367b8443cce067849ef7aedf86a92aa9f96af33f0d4791f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.99MiB (11.52MB) – 166,945 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 723e3d15aa1f0e680575eac880a47873<br>SHA1: 080fdb5c6a9efe66c7bb828ca7012ab27472fc9e<br>SHA256: 7ad35bbc002adc41cba9152eab131fc7e42bc253dae914bee10a6a4a0ad8d964</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-09-30<br>IPv6: 2024-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.164MiB (8.561MB) – 408,844 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c549f2e23ee77b6f1bdacb588b85f767<br>SHA1: 82e04a6feb932d278fc29180209d087de1cbab40<br>SHA256: 7f0587faecf2985f5b243c81ce13979021e5a59d66c6c5d2275bda071abf7d49</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.788MiB (7.118MB) – 103,271 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d76f66a6bacda9cb15304e121ab9b353<br>SHA1: 77d694eacfc2ae88234a58e708b021987ce92f40<br>SHA256: 2571ee1db97ba508bff70181a1c0e8e6c2ecabd7a8e000e465e7d329c07446c4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.80MiB (17.62MB) – 840,573 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a852aa342b352ae41b7bef3773b70231<br>SHA1: f4fd1464e9536821a5cde6d0b30a00ecd6acdd28<br>SHA256: d25f6d9c1e3ba91041ddc61d6c010f81c36aa43eb052f9a15c92912e2def96c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>65.41MiB (68.59MB) – 994,009 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51f97b68e1e9c3fc52350371d5fc8089<br>SHA1: 0e9c69af7372d33d78d630b8e7636b3635e1edc8<br>SHA256: daefc8100cdca5705c42e6a95fc86aa67bea4cfb8f7212da8194eb3dc58d10b1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.026MiB (7.367MB) – 353,071 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcefe7ff67170edca76e960964754e05<br>SHA1: 27baa458e1a83274ab2aeac30e8c9e5fd89a29cf<br>SHA256: 462e24e1a1bb99827d9159c6ca57beed55617951e2ba210ac5d3ff2b406854af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.08MiB (20.01MB) – 290,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ebd3df44971fac41c81afc4e0b8e479<br>SHA1: e374278cdbc7551f55e127136a4623733504aeb5<br>SHA256: 5386c4b7b3b9edde1ed82d40af540593e3564055cf489bb7b99eb47057236d4d</pre></details></small> |
| | | Full Location | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.3MiB (197.5MB) – 3,287,813 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 454e55ae0fc4afbb509099e64b95780a<br>SHA1: 6b88a53921a475e7c1503a9fc3192726c88eee1b<br>SHA256: cd862087cb0a1f5359ee3534aa13b529d8eff5b1c700f8f97a19f0581998096c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>371.3MiB (389.3MB) – 3,603,634 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1073bf4bc29c411e1711e31e0f8593b<br>SHA1: f03eb167bbf14c750a0b060d043ebabe87ed9840<br>SHA256: 9f2c824922dadea859da67d03d96f92bd830c0efee37cf04ed4acf6cac6a1b6f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-09-30<br>IPv6: 2024-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-09-30<br>IPv6: 2024-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-09-27<br>IPv6: 2024-09-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.800MiB (10.28MB) – 490,928 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17f21d2ef0ba52ebab5544a9616c0038<br>SHA1: e43cac91cca515a1059700a208b39a39932790df<br>SHA256: 2bb1de76196002a36ecb478e2d28ed220cbcf95e3258112d14b5e4f2a212eab5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.24MiB (31.71MB) – 459,558 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b314e2c18b48fec2436634b16dafe5a<br>SHA1: 31b9c1b2851f8cee003921d14850352e83d7c327<br>SHA256: 1f73bc1586cb15ee199d1ee99869cc998de49a7b2096a69b2acc2252b1df7eab</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-09-27<br>IPv6: 2024-09-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.7MiB (180.0MB) – 3,388,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e25fc4d30f9bfe68a98ad8dadb55637<br>SHA1: 4556f6193b89d2fad8abcd673e4d26fef1c1f5f1<br>SHA256: 016637a4cdbeee3a6e43f7afc99b5b4030417febc556d03972b67972c4d74214</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.5MiB (192.4MB) – 3,388,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 652feaea9ea8ea30a682d754c4b3f258<br>SHA1: 9cd66735e5c6c78d9b1c6a094d679cf91f2f3e46<br>SHA256: f27fdad08851d8e912d171374a86536eed95b24b1c070b2bec0b327f28f5c10f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.6MiB (178.9MB) – 3,388,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba82546f80afd8d63ac2f91830ea4ef1<br>SHA1: fe92087e08065dbb0888b31058700f990f308a64<br>SHA256: 7a27020f388c5a7199d239637bdec3194f6ecdc57a0364ce2748a9605b5864c6</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.3MiB (181.8MB) – 3,388,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a24fb3197734bc0e8ae83aac1de6c6ab<br>SHA1: eb19b05bd66cb436c8e5f104c4997b01ad773f11<br>SHA256: 85769dd03886620a171d6c1aa6b2926023efa40a9a6b06bfd177a86aaaf1ae69</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.7MiB (228.3MB) – 3,388,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b99ae900bd43680326374decf02db97<br>SHA1: 14b38acee6dc357166d702913934c92a2f755678<br>SHA256: 08be4b5a704719c76ca8ee8923194126e209be85178b5aac78a0e09819526f11</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.5MiB (178.8MB) – 3,388,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 925a1d71f4951d283db5509c7392cac5<br>SHA1: d910b37f558063999db7da2821fc1826a5d1ad35<br>SHA256: 410708be308bc6438bcad012f393ad493dcc5b6ae081ea81d727ba8c51c1bacb</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.5MiB (221.8MB) – 3,388,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5eef98b2392406f559fb46dd40d82185<br>SHA1: cc05ca7297c94705edab8caabc50af4bdc9a1172<br>SHA256: 3f1112f7612ceab309d25937385be1045819eb53c1ec2cae91e18157fd3e7b9d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.8MiB (186.4MB) – 3,388,638 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7961619eb3beefc5cfbe385479ee0c28<br>SHA1: c5499473c6a0d28348f9fa57c011d7a69d897213<br>SHA256: e36dec14597601a1e460a95fd1b3ac0efef3a2dfd2f8e16bbcae927c00a7b56c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>156.9MiB (164.5MB) – 1,647,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35399ff509ad664fcbb0207a69b98ebd<br>SHA1: a044459e9bbb63e3dd3610eb54902c149a9a2ba3<br>SHA256: fd18fca4c915a8237c6e3bf38994ef2452985c62de94da67a0953f4e4b52c4b2</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>159.6MiB (167.4MB) – 1,647,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c74ba71e50d4da71adf798fe744e7256<br>SHA1: eda15b0c119a95d5205818a24df25ae28ad3e3cd<br>SHA256: 9b0f08df18aca4c77520bcf422e284496811a31600d820f77d776a69aa09a288</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>153.6MiB (161.0MB) – 1,647,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c90a3ff94851f7813c1224c43ffd03a<br>SHA1: ed82dd7a0e85568a6b56669459e31364ab711f47<br>SHA256: 2f001f1c1a2af9da2321b965049f77b7454ee91d8ed41116e8b92b4a82fe2ec6</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>153.6MiB (161.1MB) – 1,647,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd43892f6be3496ef89d22d2a7ce122b<br>SHA1: 41a2369a1c4d7db03c89eb9599eceb77489d2d6d<br>SHA256: dc84d1137f4a02ee50050b1e1894461f90316f1ab7efb6e2b70a9a7bfb710da7</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>169.7MiB (177.9MB) – 1,647,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f22fe4f9f283102d6b00ca70b75e62cb<br>SHA1: 6b05aa6b54f56f9442616ca7eff6b50c8f229de5<br>SHA256: c07d35d2f6dee6148b1e3abce95b1167106eb35e6133cbdb108ea1e131105570</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>153.4MiB (160.9MB) – 1,647,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7d5a1a6557ea73ad0d11efba7e2f637<br>SHA1: d5035a58d9087322deeb6834ec2a221c90a3cd9a<br>SHA256: f0e44f30ab378ca5538d5b08db4c9491e45809cdd241c87248fedb9c4199f345</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>172.8MiB (181.2MB) – 1,647,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfd3fe48e4d98e10ab122f4c261cc372<br>SHA1: ad7e5646f17509bce5789df9b82e71263d672dd7<br>SHA256: 146544dd08d1a84b7439e5c0e81bf3ce0235102905728c516cd3847585ab6957</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>157.6MiB (165.2MB) – 1,647,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e63cbfa1efcec626baa4b1f7937e3b8<br>SHA1: 77ca8d486ed5d99021d54f31cccc6153fe5fb3db<br>SHA256: d376e07dd10233c1c2a8b3769b81585a56b2feddbfea0ccb228019dc87ca408b</pre></details></small> |


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
