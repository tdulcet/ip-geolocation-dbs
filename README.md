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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-09-05<br>IPv6: 2024-09-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.761MiB (4.993MB) – 238,346 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee788188f002a142df3ad7c28cefbc78<br>SHA1: f62001ac7dc4bf6c805ac69a44aaf9f765b18438<br>SHA256: 5e3dca4d9435b792029a80e9674eac08605b900c5e8e09c0ed61f5a70f2233b6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.847MiB (6.131MB) – 88,848 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0163d093b494bcdbd1f1945326d859ba<br>SHA1: bb69481e6e5cbc1b967aaefc32ce4afbf696c432<br>SHA256: cd1ddac72735145ececc4a31d64dbcdf01dec173334f28f54b6493ce31b20228</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-09-05<br>IPv6: 2024-09-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.155MiB (8.551MB) – 408,388 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ca1d0ee1442f252c6d3b3ede43aa33c<br>SHA1: 826bf2e85d171c9ba44a5f6ffdd02c75c050ff10<br>SHA256: fe332df3789097f1153a549ba9edc000c6db539701c7eafe13eb0ed7da5ccf36</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.694MiB (7.019MB) – 101,839 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00c15d2d5380ce23f348d0cff8aefc16<br>SHA1: e6e0eae6221e12d694a65dfe04716c11a8f6489a<br>SHA256: d3ff0810a04df46aaaabcbf429b6d72353e9bf5115f017d88c6f2e5b83a20aa1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-09-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.88MiB (17.70MB) – 844,718 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17eb8b19d0e70907ee7e8d306434df98<br>SHA1: 0c0803e980747fe360b5502723cda491fe38cb23<br>SHA256: 58cc54f06dacd9cda6976aa29d17a06649add046a4721807ff89005694ba4242</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>73.41MiB (76.98MB) – 1,115,589 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d012266836bba9dffecbec06f451a8a<br>SHA1: 7895b6cfa4646ce41bfbc1c29ea7c7d07e2f2279<br>SHA256: 6b160116d339d2f4f8d1698c6af4c0ca6a0122fa6d88a1d3a3605e501ffb79d9</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.026MiB (7.367MB) – 353,071 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcefe7ff67170edca76e960964754e05<br>SHA1: 27baa458e1a83274ab2aeac30e8c9e5fd89a29cf<br>SHA256: 462e24e1a1bb99827d9159c6ca57beed55617951e2ba210ac5d3ff2b406854af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.08MiB (20.01MB) – 290,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ebd3df44971fac41c81afc4e0b8e479<br>SHA1: e374278cdbc7551f55e127136a4623733504aeb5<br>SHA256: 5386c4b7b3b9edde1ed82d40af540593e3564055cf489bb7b99eb47057236d4d</pre></details></small> |
| | | Full Location | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.3MiB (197.5MB) – 3,287,813 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 454e55ae0fc4afbb509099e64b95780a<br>SHA1: 6b88a53921a475e7c1503a9fc3192726c88eee1b<br>SHA256: cd862087cb0a1f5359ee3534aa13b529d8eff5b1c700f8f97a19f0581998096c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>371.3MiB (389.3MB) – 3,603,634 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1073bf4bc29c411e1711e31e0f8593b<br>SHA1: f03eb167bbf14c750a0b060d043ebabe87ed9840<br>SHA256: 9f2c824922dadea859da67d03d96f92bd830c0efee37cf04ed4acf6cac6a1b6f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-09-05<br>IPv6: 2024-09-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.942MiB (5.182MB) – 247,345 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75be5fd9df21ddbc1fdbffc757c5c88e<br>SHA1: 617600a865f99d7027bf00861f55ec2f8fd1574e<br>SHA256: c577e4648304b379620b9b9b1a7b46685fe2b5a3719de872d7565971b4f67dd3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.43MiB (19.32MB) – 280,024 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 529fb8698467082348344b270ff7cc32<br>SHA1: 5e3253c77897a6f1833518163500372c619862fd<br>SHA256: 9289075bcac9e9a959f8009c5eae593e88bd3925aa371f097f4b54c6bd5bb9ed</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-09-05<br>IPv6: 2024-09-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.5MiB (182.0MB) – 3,005,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50ec8daacd5cafd5b2765884871d9b09<br>SHA1: 889e86b248ea9a4741e8399a0e67d17ad637cc38<br>SHA256: 5909cda69b8afb1da39fd44d4e35827b08820512a824be3f438aeb08bfbe1c67</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>210.3MiB (220.5MB) – 2,035,716 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 221fa2afd3b2e737797b4dd7b49d116b<br>SHA1: 42a7d10f6dcb092f867344cabddb6856eda16b19<br>SHA256: 138f90080a7371e27aaa532721e6449e41511cbca7244a5e31fdcc4081b48129</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-09-03<br>IPv6: 2024-09-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.789MiB (10.26MB) – 490,378 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a97f8006719592b2c4f59bb98e9c30a<br>SHA1: 9d75bb21e6b8f68643541baaf9bbc6ec7b0251b1<br>SHA256: defcef2b24485a1efead311bf74d15e22d04b78f13d0feea7db1b3bd86a22287</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>29.75MiB (31.20MB) – 452,180 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d1d9d647daa3ae60dac595ea0b0f703<br>SHA1: 1171bb6fa06ba1b18d7e474393780f78f4c54490<br>SHA256: 83df6a60aad65ae3f0041d08640160abf101b3f42031058f5e8ca2de56405e92</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-09-03<br>IPv6: 2024-09-03 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.1MiB (126.0MB) – 2,404,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8eec7420e89cd04c0ce6b96cd3a5215b<br>SHA1: 5494a1e6a4bbe2ea91ea4dd78c0be8f902fce6b2<br>SHA256: 58fa00a4e368a79a3c24940b2b67f6370d810cf128893ee29d0892eea998a682</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>128.9MiB (135.2MB) – 2,404,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49dcf38207cbb93781576801b88c1056<br>SHA1: b2bdf972603d0a5793193a890cf0200f7ec5e488<br>SHA256: 5de5ed4b13860ed5990ef19584747fa37d5dccd49e4c2e0e79538f058cf1e3a3</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>119.7MiB (125.5MB) – 2,404,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbdab76e027fd8a3d849b241c7cb01ad<br>SHA1: 86f8e86172beba89e50ebb3d59eb5f14cae4c3f3<br>SHA256: b8b635f1c535825905bd59d82efc03c093733b49126aca491074297eb788d541</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.0MiB (128.0MB) – 2,404,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7fb709a432f0957c8108807d9f10b66<br>SHA1: fdb863b708e5728cd5a714c634fddcb82cf5c92c<br>SHA256: ad6fc53f60131c7d4f4c17cb8342cc480229dd8c2f4ceaa80c9cbb1a1105c3a5</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>149.4MiB (156.6MB) – 2,404,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c04e09d1e1a4250bf83469426d7342e<br>SHA1: c3627ed46aaf490ef97ac7bb577cb4109986638b<br>SHA256: 6339b5053805a9f4d7f150b14065159ef872b362f2fbf6641441c1b461082ff1</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>118.9MiB (124.7MB) – 2,404,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6749c45a7d9ad65e4c071e7338edb2f<br>SHA1: 2eb3ee3b6361326082b6aae0432c31905a8c8f78<br>SHA256: d68ba65336aeb4f513239890a70a02b9c172b10f9b23dd3d0113e9cb43a60f60</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.1MiB (153.2MB) – 2,404,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a9580fb7211ead8a954be80f0a3281b<br>SHA1: cf1d731485242abca1cadc417b6d8022d7a768e0<br>SHA256: 416450fe700465941d675bdd60771dfd6755154678b660f79955cbdeef06ac9a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>122.5MiB (128.4MB) – 2,404,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d91035fcc2e62b234d217c640153f59<br>SHA1: 753e40ce30839055006e4b9759ee1c592a6e539d<br>SHA256: 270486a9ea057948ba66bdddca9512e0e06e6f3e4dcaa44f30e7754f179a6327</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>144.5MiB (151.5MB) – 1,557,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3e8afcd6ab3e6419f653e1446a775d0<br>SHA1: a6bdbab36038c2beba8fd2fbdad5b994b718002d<br>SHA256: 112f0ae6e3e152f173c411689fa71304f844242086bc2e91ebd0d59814dd1516</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>147.8MiB (155.0MB) – 1,557,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51ff0447e82cd1755c1215efdf5e52c3<br>SHA1: d7ae1721dd8d770d274e9e28b3d5931469e83e41<br>SHA256: 88368972bc09d0f9fb3d857b28bfcece62720035a1ade626e78ea85bbc49f5d3</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>143.0MiB (149.9MB) – 1,557,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 211b8438618463bdc26c7a64c5e7ed84<br>SHA1: a423ed44cbc0e9113dc08065bed2ba9b47e357a3<br>SHA256: a934f71bbc0430f7537b98c2531438567456b87929c9ef73f6abe6fa4a98e613</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>143.2MiB (150.1MB) – 1,557,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91b4f58a5e226181cabd2dec829f8164<br>SHA1: 2ab38e8f32e5c9dd3eaeae7b0ba2a42787ce5cb2<br>SHA256: 64068b9219c8d82aecc64ff775288c6e1a8dbf31f908090a7b247b490e5e7175</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>156.3MiB (163.9MB) – 1,557,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac7ce5f57be8c882a14b6c53761a309e<br>SHA1: d507f47971c51e55c8406e17798481a87809fe67<br>SHA256: 363ec461f72d06856399706f335cf950f2ac1cacb0530c3deb1c7fa88125bd64</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>142.8MiB (149.7MB) – 1,557,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2fabca8ed340cfdd7d9a2b7b4c2f7ca<br>SHA1: 7420befe53f4a87691eb5dd29f3109208ff11b09<br>SHA256: 267c32b1eae54e630ed747540ee33308482b9de85eb33d2b3742ec51167a5326</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>157.4MiB (165.1MB) – 1,557,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03e363cc816ab1f1f93b5a4888f47455<br>SHA1: c0586cc3837c2252da9387b0b8adabb1816e6e0c<br>SHA256: 5deabda61d9a0ff45c7354c5415b1c1a1e251adfeeffbf83b898a89fa9965b62</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>145.9MiB (153.0MB) – 1,557,110 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 371c768400fdb76920bef913b0fc3653<br>SHA1: d7d30d3737cfdbcd11e6fa66dd02ac4c012a9c5c<br>SHA256: e77a1f949055ce4e636242c5271e2bb2c19cbeecc03b4369ccf5697f9fbb09ed</pre></details></small> |


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
