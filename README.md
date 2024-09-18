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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-09-18<br>IPv6: 2024-09-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.621MiB (5.894MB) – 281,412 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74688841ecdea9c31cdfd39e661da22a<br>SHA1: 112cd19fe78523c740b667efc9e8b416434223ae<br>SHA256: 06978192f89f74da93c316dd545e05622a66a145b4347f4889215f93e95ab33a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.94MiB (11.47MB) – 166,193 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8dcb804b0b89b4840d0d4acc7db31fd9<br>SHA1: 3445baf1263da59543e296ba1730fbbc9880869f<br>SHA256: eef7dbb795540c9e1aa3061805f29b7184ab7e4360352057e2ca3122a4800861</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-09-18<br>IPv6: 2024-09-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.160MiB (8.556MB) – 408,618 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b425abfca1a9b38ea11f447cddff9539<br>SHA1: d13cb65f63f06f3c59f6154922601c085fb9e1da<br>SHA256: cfe92f37ae7b199396a1afdca561f9de2dd967139571e02500d222480778fa51</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.739MiB (7.067MB) – 102,529 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb8a2243c79f9ae5db6bd9497fdc357b<br>SHA1: 625096ce361be5383a0d1a4e189145670bfcfa09<br>SHA256: cb75ef11e361eb34583136287bdd9d21923c9fe07e5744c66ad9b73272fd7e49</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-09-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.83MiB (17.65MB) – 842,039 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8d2ae29ba8566719af0ee12f58a0e3e<br>SHA1: 3eda926992fb7ccb600299ed67539789b6d769f1<br>SHA256: 28ae2068ea9698bbba0ef80ac84bad1e4e9685eacf7792b90f769eda806550ae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>62.08MiB (65.10MB) – 943,473 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8824891f4b774c6ad161c590a3ed24a0<br>SHA1: b9343b4892df1a29e65fdfe55bdb90068f5bdb2e<br>SHA256: d1a8bc785d2a795178e49e08c8e4df47f70535d3582648332aa650a29e738129</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.026MiB (7.367MB) – 353,071 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcefe7ff67170edca76e960964754e05<br>SHA1: 27baa458e1a83274ab2aeac30e8c9e5fd89a29cf<br>SHA256: 462e24e1a1bb99827d9159c6ca57beed55617951e2ba210ac5d3ff2b406854af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.08MiB (20.01MB) – 290,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ebd3df44971fac41c81afc4e0b8e479<br>SHA1: e374278cdbc7551f55e127136a4623733504aeb5<br>SHA256: 5386c4b7b3b9edde1ed82d40af540593e3564055cf489bb7b99eb47057236d4d</pre></details></small> |
| | | Full Location | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.3MiB (197.5MB) – 3,287,813 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 454e55ae0fc4afbb509099e64b95780a<br>SHA1: 6b88a53921a475e7c1503a9fc3192726c88eee1b<br>SHA256: cd862087cb0a1f5359ee3534aa13b529d8eff5b1c700f8f97a19f0581998096c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>371.3MiB (389.3MB) – 3,603,634 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1073bf4bc29c411e1711e31e0f8593b<br>SHA1: f03eb167bbf14c750a0b060d043ebabe87ed9840<br>SHA256: 9f2c824922dadea859da67d03d96f92bd830c0efee37cf04ed4acf6cac6a1b6f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-09-18<br>IPv6: 2024-09-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.942MiB (5.182MB) – 247,345 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75be5fd9df21ddbc1fdbffc757c5c88e<br>SHA1: 617600a865f99d7027bf00861f55ec2f8fd1574e<br>SHA256: c577e4648304b379620b9b9b1a7b46685fe2b5a3719de872d7565971b4f67dd3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.43MiB (19.32MB) – 280,024 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 529fb8698467082348344b270ff7cc32<br>SHA1: 5e3253c77897a6f1833518163500372c619862fd<br>SHA256: 9289075bcac9e9a959f8009c5eae593e88bd3925aa371f097f4b54c6bd5bb9ed</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-09-18<br>IPv6: 2024-09-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.5MiB (182.0MB) – 3,005,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50ec8daacd5cafd5b2765884871d9b09<br>SHA1: 889e86b248ea9a4741e8399a0e67d17ad637cc38<br>SHA256: 5909cda69b8afb1da39fd44d4e35827b08820512a824be3f438aeb08bfbe1c67</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>210.3MiB (220.5MB) – 2,035,716 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 221fa2afd3b2e737797b4dd7b49d116b<br>SHA1: 42a7d10f6dcb092f867344cabddb6856eda16b19<br>SHA256: 138f90080a7371e27aaa532721e6449e41511cbca7244a5e31fdcc4081b48129</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-09-17<br>IPv6: 2024-09-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.754MiB (10.23MB) – 488,596 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5055861d99572f9327f848b0f0491b41<br>SHA1: 13bd344656b81e0676d3412c9bd16ba0ccc19ee1<br>SHA256: 8730efa8c960ae03614a85a383391528bcba6ef484f1863ef3949a8e124de2b7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.23MiB (31.70MB) – 459,480 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2ab45f894c248853602df4b778114e3<br>SHA1: 11e278765189491d05d7caf078658e3cecd59465<br>SHA256: f55b51baff3dae1b685b58e531379c7995ebf3f8fbc67a23cdb85b16e3e58ee8</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-09-17<br>IPv6: 2024-09-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.2MiB (179.6MB) – 3,381,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cc370822374c3e3f028436d55747a23<br>SHA1: c88b3d7afa345800852466a97eeacbc8ead7ffbc<br>SHA256: 50507a2995a39e39016d68e45c4a9272b638f9b47166cc107feac74929b28c8f</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.0MiB (191.9MB) – 3,381,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed4fcf0f5082cfa823d66ee94a45274<br>SHA1: b1f8bd0436d1eb73f41b8abe376152f8354dadb6<br>SHA256: bf078b71b10dd065f3ebe87eb2b3f34a341390f651a1592edae51696c5b05be6</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.2MiB (178.5MB) – 3,381,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17cf4ccb8ec25bf59488dad0871743c5<br>SHA1: 693d9712ffa4366f7405dcb52341f9fa88ac9f49<br>SHA256: b745e32a4a19272eb9048bd3b80695b06bad1c4a60762440e1cedc5bf202e181</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,381,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 905ae8cdb79a2873449df9e4b7bdd873<br>SHA1: c61006576e80b3b7b9059d3a544cc9ffa0f4bd0b<br>SHA256: fe97c55842bea046770f850b97e1a2c3f8f593d8184f642b824e71bef6d6e071</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.2MiB (227.8MB) – 3,381,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0ca5440128c7877f160e46719c364d3<br>SHA1: 65a5ec79ac5ed5ce29e06326d52a39506624779e<br>SHA256: 63639d196547f42b9bc74fbb5ef80e4a1de27c05b83ff3c789a25b92267da83b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.1MiB (178.4MB) – 3,381,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1262f66ac332055e234204eaf35669bd<br>SHA1: 7778fdbe1acb0adaa994af9160c49efa8c92e870<br>SHA256: c45e848b9518c6e33d5dfee17be21ad3a4434b49d6ce851f546d2c34dec975cf</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.0MiB (221.2MB) – 3,381,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9aad64cb69c5859e7c7fdaee824cdca9<br>SHA1: ed1f777d680de120a343c1ea697d0dc9380c8495<br>SHA256: 07c2b8ee0d1b0d9a1709f97263e9d5bccb57a2562c60ebc3378c9fe7ecfda78c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.4MiB (186.0MB) – 3,381,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cb4c3914640cabd72c7a839783179c9<br>SHA1: 2466fa626216ac27282ecd67031dd352a5f73dd6<br>SHA256: 37d8e8f07e70c7e1dbd60141ed2b848cfd0b791eb9dfd0bb86b684408e461de4</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>156.3MiB (163.9MB) – 1,643,959 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5874917b1e8ec23c843c66bd0b5df238<br>SHA1: cb7da2211c74b0c79526b366b9924b3d83046d2b<br>SHA256: e303d7ccdd45353d58fa622d316ef8d508d7d4bc17a2c40989b0c52c59c3ba65</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>159.0MiB (166.7MB) – 1,643,959 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 604a75c060113746c91466752f242fce<br>SHA1: 5da937b7278a2e3c99c3bea35d24688c71768a79<br>SHA256: d4e1a9886e4be3d213a065564cc255678f5fc1433d859e5b2f2e68955ce328b0</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>152.9MiB (160.4MB) – 1,643,959 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f69a1a1d3be9a8f113b08d2c69b2029<br>SHA1: fd3195459f5e5aa01a1218808c7da751a11d17d7<br>SHA256: 606e5d9836e94f9db597ee4ef16106a672f7009b05c32085d55fbaf2f1dc3f4a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>153.1MiB (160.5MB) – 1,643,959 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: caf88c0ec41ebe1fe6171aa46e0b0c00<br>SHA1: 4bd9b20f9f2be53489537a0b326f4c8769f233df<br>SHA256: 4a7ea7dfe8aa2c1f47b3bb13b9011d5008978b9d63ee2e9086745df7be71bb55</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>168.8MiB (177.0MB) – 1,643,959 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cde44813c00a40901427e590440c8a78<br>SHA1: 91aad0a8a46ba77f14046151f2e3d4955ce04f8e<br>SHA256: 649f4f9c151a5b745a312e9ec5e405edf5d5c2468b0bb535a058f7e00bac8244</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>152.9MiB (160.3MB) – 1,643,959 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65c979cc644bcb904760dc0959e4db9f<br>SHA1: 3ac794494bd385e6e22bb2cb44c3b0e94ed3f1f9<br>SHA256: 28b5891205d54bf720aa9f9211b0e524c48a836b5326b435b35a2ee06c7fc301</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>171.9MiB (180.3MB) – 1,643,959 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fd21f0faa407a627a5b785bdcf4178c<br>SHA1: 40dc1cef9dece685e8e8836d1f88adf9a17278b9<br>SHA256: 7d446b52008a5fe8267051b338863faf9122d3955390ca44d870ee70a24d2da3</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>157.0MiB (164.7MB) – 1,643,959 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b315c9bceee1cf4d4091ea7d31a699ad<br>SHA1: 14cc57765f61265efa35fa9c7a2c09c6345f9835<br>SHA256: 34a7744d9bcf20a416f34e9a816cdc2b4d14b79f14332d914503ffefbd56469c</pre></details></small> |


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
