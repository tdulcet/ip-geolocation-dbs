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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-01-23<br>IPv6: 2026-01-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.408MiB (6.719MB) – 320,870 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d2622a445adc12645d4e3f3f53b1812<br>SHA1: bf103d6a11a04f60f438dc04d95549cf19ff6cec<br>SHA256: 6d3f01122ff25db8aa060c81a16fabd1438b4ba1f543012235b29c9931a924da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.20MiB (15.94MB) – 230,985 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58a52704163a5824416f785bb5c2ffb9<br>SHA1: 4bbe9cef4d596f1c4b7a49cfe4b1487f2940fec3<br>SHA256: fbe2e51d088949db771358f8bd25304f3f5eb73e919adae4911a1ec261ba925e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-01-23<br>IPv6: 2026-01-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.210MiB (9.658MB) – 461,112 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63b8254effbb2f89a59d39bf0bb1c175<br>SHA1: ac166e24e8485ca55e1fcd343a2205d70aa6f9ca<br>SHA256: e050fc8dcc65ccac15bb14f04fa81490b75afda72b34ea17e2542cbcd1336494</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.556MiB (7.923MB) – 114,947 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 244a11542b638fdfea1173e133bd5cb6<br>SHA1: c61eacc3056d799fdfa4a7501d14e378ca59d136<br>SHA256: 87a8b9b57edd526d7b1a5792e27472db1c447742ead60e1cf81bd070f20c7bf5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-01-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.78MiB (13.40MB) – 640,495 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b5dcd787d96ea259d86a65c17746ae7<br>SHA1: 826b322f548314ff87a2862fff8e1d6d4bdb0de0<br>SHA256: f11e127457a73f82031a902143c17a332989f1c78b2f9bea41f4b5612a3a52a6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>53.38MiB (55.97MB) – 811,231 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 727c243d731aae28d11a4aeee927b031<br>SHA1: 5d9c9ee0ac9145c12b80bf0bb5a6e4c9f412cd38<br>SHA256: 8c622b1bed412b4659f6a3046d185b750ee36df942b651514c12206effce927d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.843MiB (7.176MB) – 342,905 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7f0c42b88b3ee5ac2070e71f756f963<br>SHA1: 4416542c9574226ce202070dc48ca08edc6fab0d<br>SHA256: 5393382f53c552965d88b65e40e02f63c643f2379a931aaecef8209586b9ced2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.52MiB (17.32MB) – 251,059 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232548602865156556e4ff9d7db331da<br>SHA1: 61d1e0b2cefeca101ea9e8530969dab152188ab6<br>SHA256: b004edb93559a31ded3baa727a5d781edbe90c29420b4d5691f44e917e83bdb0</pre></details></small> |
| | | Full Location | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.7MiB (223.1MB) – 3,730,744 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42e04cdc8d81a8ce6b440accea48b373<br>SHA1: 9c414f68d243d9ebdc8b7c65e081580b035b663c<br>SHA256: 5274313529b847bd8629fb44b41144c683552f55760a830f535892f20b8e46db</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>457.0MiB (479.2MB) – 4,442,155 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56e8f0cd6817f6807824ced45628cb9<br>SHA1: 316812aba9e80b97b08bfca58defd796b628d008<br>SHA256: 44317ed175935104135d379f2a9918ca97141e9bf034ee1bca6cdf894093d72c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.345MiB (5.605MB) – 267,509 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0604e023f5c6722d46ef6793af281ce<br>SHA1: 3eb54f1eebcd039df05135ab29260e09bdd4fefd<br>SHA256: 3c8d20a60ea0af489cb12852284187081cd8541958eecf909e2f4c90e9f0555f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.02MiB (23.09MB) – 334,578 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d24f67bbedc322d93d7843237e6d08bc<br>SHA1: fdf5e7611f467995a14f85f97c32c055b05d983f<br>SHA256: 122f2768c962576ccb07d18b092f50799b7b9ea494a23db97a4bb4754c05e303</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9MiB (179.2MB) – 2,956,256 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7eebf486d9c42702ac790a4ac4e81b3e<br>SHA1: 110fe57678506100a087eda5e8cea65a848958d0<br>SHA256: 80471fedc344947500ec0408ae5d771afe66c98c0ba3989ad3f556cb157c73ed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.9MiB (302.9MB) – 2,799,002 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bc462fd69a5966f640f89baf03f95e<br>SHA1: 51eb98defa6d6bc9f2d654be1fc3e566c1803852<br>SHA256: 122e835b4e22ab281b426d9e1eff933fe165e08f77812b4b427e046722b296da</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-01-20<br>IPv6: 2026-01-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.11MiB (12.70MB) – 606,416 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38059b76488f5ea66ff95774703d1fd8<br>SHA1: cbe71c92c0da30ac84bc1ad4ed7f390dc85b3f62<br>SHA256: 2e29372c320d97bc41196ca9057626e2fede8f814cb9ab7e4531826c9ce5e739</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.71MiB (44.78MB) – 649,017 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35736acc619131e2cef46d11eefd045e<br>SHA1: 82b9465cb76f4e636a2e175b87f846a3ac3c843e<br>SHA256: 59f96adeaa21cd0f681e2bc218fd2064c7432fb4bdecc0de8d9606a06d49adb6</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-01-20<br>IPv6: 2026-01-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.1MiB (186.7MB) – 3,517,640 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61fb461c3789ae9e53f62e76b25be607<br>SHA1: 47da20686eb8e3b29735fbe6158e59f347202781<br>SHA256: d4e9b9c8ef4d1c386a6b8148d2bd99cfc4d49e779b9e5778ae643250147bbea9</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.2MiB (198.4MB) – 3,517,640 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: caf52addd5462b6e33ca16787b90dedd<br>SHA1: c179df7145a7b6e855b7debf212a5ab62fa6fef7<br>SHA256: e51e238891988b63c7d8a0bd8bdc98ba8647c4435083c551e0854f1a5c192b5e</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,517,640 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a102fbfef9b3ae32468dbd7a6111b34a<br>SHA1: 71ffd9dc19fa2684e371466093b7e10ad473ad75<br>SHA256: 553b876c81bc404b0a0cd6ab63d4b07cf20b05501604a472b1e301b300e09d3c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.1MiB (188.8MB) – 3,517,640 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9ee38c7911faa3656853dd019a5491a<br>SHA1: 6aa7884e2a91e93c61d1da81ed4091e66c7314d0<br>SHA256: aa18a0012e3872559590310151adef6fecceaa6a21118255d2f9bf1c217910cd</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.1MiB (236.0MB) – 3,517,640 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d7f8d90a8c5b39107898943654333e8<br>SHA1: 0f7c7206cc0116f17670e24e39551d7f41dd5566<br>SHA256: 10e1ce63ede7120e98d9d7592ec2337d9ad41c15279c217e018008b8268bd83e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.7MiB (185.3MB) – 3,517,640 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03d725d78e0a8e3c5284bf370b7690c0<br>SHA1: b25436d05f45a2e31a6531e8f6c8689c63acaf78<br>SHA256: 9d7fc1df73ca78c3d7e76e7b7859b9e1da195486d59d1154fc3fe3b8e5d4f2b0</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.0MiB (229.6MB) – 3,517,640 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02dabe86a9530cbd9ebdd0e933e6cc89<br>SHA1: 38017f149f5e25926897c5d92306eb09d890b134<br>SHA256: 1e332f136f82fa6f177696012af5de02901e4809ae22ce51e992b4db28e353a8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.9MiB (192.9MB) – 3,517,640 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51d32306dfdebd8f86b164b7e1250d14<br>SHA1: c028cb5e543ee30f1fc7f353525d1a46cd621baa<br>SHA256: ef783006f6670b7d58863ae229b5ed686cdff94361a8fb48177bebb62761c1e2</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>185.2MiB (194.2MB) – 1,954,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9565db21404f188c17857634d172471<br>SHA1: a74759495ebc5e7c0e50f3bd9d5be862c3e8175b<br>SHA256: fc17e0a04254f4cbec0a8d523cf0891c949c4f5cc9754a508e552cc4ffcdc229</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>189.4MiB (198.6MB) – 1,954,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b326aded6e228de7d260689107d59c7<br>SHA1: 31c74c23cff42385e20eec5a846b9e592ae85d00<br>SHA256: bfe8af09937f4398514031ff09af6839b51b9f1b9b0c4c332bd6471d023851a7</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>183.0MiB (191.9MB) – 1,954,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9352cdf8ca1286528af9676d0cf23d7d<br>SHA1: 1d2e83980c926d09b02ba91f44e2427e577aad49<br>SHA256: afb797f908f67b41359b0c01d1a25e42bff72c3a5d2261840c9682879319533a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>183.7MiB (192.6MB) – 1,954,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 764dc755b5fbfd3a11e688132b9745d9<br>SHA1: 21ccfe17f3f88dd48bceef6d8879fe0e0e04919c<br>SHA256: 030747d0a370ab1a6c426436cd12728e6e201167ec1654288ece22e04dbe8ea5</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>203.3MiB (213.2MB) – 1,954,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1222eb399b087348b65e035d2dae9cb2<br>SHA1: d07b5264d96c093b1243c2b7527845c1f43f128e<br>SHA256: 3225b810b419582669a0b647ce329a5171f68ef066bec875b0a6e9f65cae94b2</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>182.6MiB (191.5MB) – 1,954,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ea74bd7df075a0cce673795651800ff<br>SHA1: b3aeff360ae13f8abf5f6323161f45558956a102<br>SHA256: e988fad5dd51a3a3c25f77f0cf748bdfddcb2cd3b02072e7dd4478d70a5763ad</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>203.4MiB (213.2MB) – 1,954,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eeedefb5de8b671515d21c7a956ff2ee<br>SHA1: 55187e38a20d4b661c9ce7d8672a4b7293b464b3<br>SHA256: 58ca6925f0c4aea1d867847ce8ba8b77a93fd3ffb1187364c085680d158c74b0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>186.2MiB (195.3MB) – 1,954,003 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ac447071941a1f7a678c3ea005d9981<br>SHA1: 34b1d5d1b06feabd0a8defff3459d7c436826a6c<br>SHA256: 99b97ed110ea4ef8a4e69307fe26d156b313af0b485a271825117c62b8861980</pre></details></small> |


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
