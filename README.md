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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-09-11<br>IPv6: 2024-09-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.612MiB (5.884MB) – 280,959 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 666c4c4002eb074c69923b380459718b<br>SHA1: 4b31ea399e6a46554f51b912bf401a0b4f95a7ca<br>SHA256: 94d1b010ac50996db02d1d7d396c554e1cacceeb5f0ce2dcf717c3c052af788c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.90MiB (11.43MB) – 165,712 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9090be5092e8349f044d6883daad5df<br>SHA1: 5485a28f9f090153ca61036c409eff00b83fc904<br>SHA256: e9c7e673ab2be22532666a2ff42d48b2171d9de814631c51426f587de45d7126</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-09-11<br>IPv6: 2024-09-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.156MiB (8.553MB) – 408,459 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6b9d9bf7a58d2c556d25e9a3abeed7a<br>SHA1: 9f4cbabf541b607fc9b7ad309d92babfd0672e87<br>SHA256: 405f152fcd1da5ce36b66c8d4acede87d89442ddde3c75074007386d3ebf3eea</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.735MiB (7.062MB) – 102,460 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf02e446ef53272e79a2fc2966a7b9a4<br>SHA1: 2d6fe47f380d9135d6b41ad77b38e92c489af2dc<br>SHA256: e0a315dd63967cff071372c30a48b7b3c183e4acd6b808d83c278b444b45b0b5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-09-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.76MiB (17.57MB) – 838,414 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ab07db57352f28fc053a06a65079c17<br>SHA1: 056c5443dd8f1863af3f3ced8b536aa18ebfc52b<br>SHA256: 609b66a81e24279cd7f475030279eb3db355e29c47cb75179744c93b3413e021</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>70.80MiB (74.24MB) – 1,075,917 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63356877f53bdad01c533fa1c1b151f7<br>SHA1: f6a024771ad46e6deb4edd726c4a2e9a1254858e<br>SHA256: f8da98193c4f0635cc76f5ea50ca021fb80cc63a1ed835ebf2151c30f3f63162</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.026MiB (7.367MB) – 353,071 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcefe7ff67170edca76e960964754e05<br>SHA1: 27baa458e1a83274ab2aeac30e8c9e5fd89a29cf<br>SHA256: 462e24e1a1bb99827d9159c6ca57beed55617951e2ba210ac5d3ff2b406854af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.08MiB (20.01MB) – 290,001 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ebd3df44971fac41c81afc4e0b8e479<br>SHA1: e374278cdbc7551f55e127136a4623733504aeb5<br>SHA256: 5386c4b7b3b9edde1ed82d40af540593e3564055cf489bb7b99eb47057236d4d</pre></details></small> |
| | | Full Location | Monthly<br>2024-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.3MiB (197.5MB) – 3,287,813 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 454e55ae0fc4afbb509099e64b95780a<br>SHA1: 6b88a53921a475e7c1503a9fc3192726c88eee1b<br>SHA256: cd862087cb0a1f5359ee3534aa13b529d8eff5b1c700f8f97a19f0581998096c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>371.3MiB (389.3MB) – 3,603,634 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1073bf4bc29c411e1711e31e0f8593b<br>SHA1: f03eb167bbf14c750a0b060d043ebabe87ed9840<br>SHA256: 9f2c824922dadea859da67d03d96f92bd830c0efee37cf04ed4acf6cac6a1b6f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-09-11<br>IPv6: 2024-09-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.942MiB (5.182MB) – 247,345 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75be5fd9df21ddbc1fdbffc757c5c88e<br>SHA1: 617600a865f99d7027bf00861f55ec2f8fd1574e<br>SHA256: c577e4648304b379620b9b9b1a7b46685fe2b5a3719de872d7565971b4f67dd3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.43MiB (19.32MB) – 280,024 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 529fb8698467082348344b270ff7cc32<br>SHA1: 5e3253c77897a6f1833518163500372c619862fd<br>SHA256: 9289075bcac9e9a959f8009c5eae593e88bd3925aa371f097f4b54c6bd5bb9ed</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-09-11<br>IPv6: 2024-09-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.5MiB (182.0MB) – 3,005,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50ec8daacd5cafd5b2765884871d9b09<br>SHA1: 889e86b248ea9a4741e8399a0e67d17ad637cc38<br>SHA256: 5909cda69b8afb1da39fd44d4e35827b08820512a824be3f438aeb08bfbe1c67</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>210.3MiB (220.5MB) – 2,035,716 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 221fa2afd3b2e737797b4dd7b49d116b<br>SHA1: 42a7d10f6dcb092f867344cabddb6856eda16b19<br>SHA256: 138f90080a7371e27aaa532721e6449e41511cbca7244a5e31fdcc4081b48129</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-09-10<br>IPv6: 2024-09-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.778MiB (10.25MB) – 489,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 952093eba1c0ada54c680b0425e4733d<br>SHA1: ec4429f7bb99d32fa74fbe6627364c239a3289ff<br>SHA256: 1f3b44a32052f6443fc66cd3e523ab468268cdd389fc4e23743cf1d34a8c6575</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>29.81MiB (31.26MB) – 453,050 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 927206dc05d364f2aa36f614bb79bbb1<br>SHA1: 35d361efe71ff12552bd842fd65f6d7fc07bb67e<br>SHA256: 98ac15d8d8011b917398ba2f58700c41b12e8e15ff0b7eaadf3bc48530952596</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-09-10<br>IPv6: 2024-09-10 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>121.0MiB (126.8MB) – 2,419,472 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee401d373000ac66f5526cbef9a0b9d8<br>SHA1: 643690683b9ab965a58acf0e5adffd7d1639fd2d<br>SHA256: b9e9becd8cb9b9a97500586e0eec00e0f9aa6f9c353ca5926a851342df8bb8b0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.8MiB (136.2MB) – 2,419,472 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4de3df832373cb5c7fe79fd5801338a6<br>SHA1: 3e8c66a942cc8ed95302a15c055bc2fe8bd2851e<br>SHA256: 477cf477ca11b6bf4c887547795f04cabf745cd9b04e554fc071f5455577d920</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.5MiB (126.3MB) – 2,419,472 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3f67d13d7e9764eb805ecdcdcce22d4<br>SHA1: 6dbc006dca9ce6398f1c9cdf3fe796d87cf02a32<br>SHA256: 4f6fe7293e80c3d01f82226a054df22d7349f84f9f017c739f08c7edb4174407</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.9MiB (128.9MB) – 2,419,472 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4cb052a9cf96000bb960df0e4ae89e51<br>SHA1: fa82e0166603d28d65a3649ab5c7541578104a38<br>SHA256: 86339690193973ac7863fe76a1dd65ed5735ef3b1131dd728023d12ad7d5d419</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.4MiB (157.7MB) – 2,419,472 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ad28dc2d1766f3f17cf8830b352e6cf<br>SHA1: 0852541dc9adbf0c44e4b9328c0c3c2898c9499b<br>SHA256: 0d22e9af6b7d057906995072f9cf50f589c7183f0afa066051b1f48057a6c01c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.7MiB (125.5MB) – 2,419,472 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25957c04b7daae190226fca9c525e484<br>SHA1: 9b1c5161ea73f5c6bdc382e65fa428829abe1fed<br>SHA256: 1c75dbc862594510270168b6b2b22fe29d76258ce533a617804a06d0acc98e26</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>147.1MiB (154.2MB) – 2,419,472 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8273cda7d9cb279e3887ff2177e87fe<br>SHA1: 2f07ed07289fd1da01b46eac53a0da503ce9a972<br>SHA256: c55428c925979863dcaf8c68d0445ee3c007956e23fb4d6c202dc311b8e06a96</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.3MiB (129.3MB) – 2,419,472 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c54ca002216a64b3bff5065c26ea5fec<br>SHA1: 565852f937c7545a891441e5d63daeeab80bf4ce<br>SHA256: bf26133798f7776834a75e65c68652791d5d8ebee864832ea6ba9da9915f0b21</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>155.7MiB (163.3MB) – 1,651,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e714e80ee08524c54f65b12040c0d8e6<br>SHA1: 697ac439e1e3b52a450b7514a8c8a3e15e7c2a31<br>SHA256: dc4aa4067b6114c8f254ba2d23eea6ef52cf798781dadafef4622b45d564263e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>158.2MiB (165.9MB) – 1,651,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26cb078b56269fbeefaa081a9419fa5b<br>SHA1: 5f4a1aac89d96511b6a9d11588f0e8e4d16da6d1<br>SHA256: f3a3d56bc899ba69dc11600f2fc6805f6e157773595de48c971b26ed51ac9433</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>152.5MiB (159.9MB) – 1,651,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8abb84d9c0844866d4e13e0b80fd529<br>SHA1: 17ef68ebeb73e7b21096e41559c0ff8ccbf10c71<br>SHA256: cba178b3d0ee10399984554d4bf5f9841d7a8fa81d46ac0a51d76f119d940ce8</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>152.5MiB (159.9MB) – 1,651,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea43232bc8cd78fdbf94fe117fd5bff7<br>SHA1: a1d1d41fb59795c8219ec8b1830d98d4b60b70ab<br>SHA256: eb44f0d8e14398c5cb72c1927a00e5942e2c1d628473a3482382f3f0fe4c5f01</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>167.0MiB (175.2MB) – 1,651,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e6ca116c8419596c79464691f6efd31<br>SHA1: c38a388c65d70a6847602abbed69cf631d793892<br>SHA256: 256aa821e0875ebedf9c5b01a17c679dd4bfce5b2ffeed478df84f75259bb88f</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>152.4MiB (159.8MB) – 1,651,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca9bd1c9e762f881860ac51286fd606f<br>SHA1: f5ad1329589c7bacd99472c0a8b12dec7934bd2c<br>SHA256: 86498d38d493c2cdd1a4b5f4a70c4f94a29d70c09d0e9c299101138a81f13b8e</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>170.3MiB (178.6MB) – 1,651,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7b2d3d6e48c60f0ab93c88925c8eb3a<br>SHA1: 702599e0701a595d25e5ce9e938900465d98c455<br>SHA256: 7e9dc2bce2c50b1e499c8d614b7cc7df2270db2824b061dbb01df2acdfb35002</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>156.3MiB (163.9MB) – 1,651,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8381a6500b0aed322174786c902865aa<br>SHA1: 28bd3e66b6d2a17a8a1d4e1680272fbb6f005ae1<br>SHA256: 2cc21219fbea5ee69040e333b36711bb2b0cedb9388bf49aece2943940ebee85</pre></details></small> |


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
