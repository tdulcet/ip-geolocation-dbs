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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-01-19<br>IPv6: 2026-01-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.453MiB (6.767MB) – 323,121 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b2833ec474a81677e44cd29681aff57<br>SHA1: 6e5c9215e473b229d495c883832e682e4bc7fd7c<br>SHA256: 9a3229529173793e05d9108a934b9bcf577a87732492baa053bbe09c074aefae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.57MiB (11.08MB) – 160,593 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d4444086ce7f24717d4ffe141968c8c<br>SHA1: 9cff1dfa1a0a69b4a3840d0faf0c4c7e8681a487<br>SHA256: e3d3f038995fb6419eb30b156ffba8cc81a508b8e16902f54066bf3cd77ac6d4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-01-19<br>IPv6: 2026-01-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.207MiB (9.654MB) – 460,935 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46a9d2a215419f6fc0753fdf435493e0<br>SHA1: cf59028307e2b42d68fb66945a03be57e78641e9<br>SHA256: 8070b0bfc214979685d1802b49b06a397b21ea084bfed2b2ee7525854525707c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.544MiB (7.911MB) – 114,761 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c7f00344b0f03a4bab12b72960227a1<br>SHA1: 5d68268598b60419fe2d4cb506b236ebbed1bf3d<br>SHA256: 3eff4a685175cde4926a3f90293963de67364c068faabeef87b7d8204f70c799</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-01-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.42MiB (13.03MB) – 622,115 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42349c2cf6130472ea35443052bafb51<br>SHA1: 7bcbcf42aa4c9dd6287be33b01f2cf80de2eb674<br>SHA256: 4a68579504e35b28143599c2e045cf2d78469a3c9f36167191e922008aaddc24</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>59.56MiB (62.46MB) – 905,188 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3992b6ad9f96e87e756b83b9780da425<br>SHA1: 479144472aca55a0db8543fd228401601c93d0f5<br>SHA256: 0ab6fc26f5a032f30a818c562a3edc080a4a9368432ecddf3e3a69f0f400c26d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.843MiB (7.176MB) – 342,905 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7f0c42b88b3ee5ac2070e71f756f963<br>SHA1: 4416542c9574226ce202070dc48ca08edc6fab0d<br>SHA256: 5393382f53c552965d88b65e40e02f63c643f2379a931aaecef8209586b9ced2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.52MiB (17.32MB) – 251,059 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232548602865156556e4ff9d7db331da<br>SHA1: 61d1e0b2cefeca101ea9e8530969dab152188ab6<br>SHA256: b004edb93559a31ded3baa727a5d781edbe90c29420b4d5691f44e917e83bdb0</pre></details></small> |
| | | Full Location | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.7MiB (223.1MB) – 3,730,744 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42e04cdc8d81a8ce6b440accea48b373<br>SHA1: 9c414f68d243d9ebdc8b7c65e081580b035b663c<br>SHA256: 5274313529b847bd8629fb44b41144c683552f55760a830f535892f20b8e46db</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>457.0MiB (479.2MB) – 4,442,155 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56e8f0cd6817f6807824ced45628cb9<br>SHA1: 316812aba9e80b97b08bfca58defd796b628d008<br>SHA256: 44317ed175935104135d379f2a9918ca97141e9bf034ee1bca6cdf894093d72c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.345MiB (5.605MB) – 267,509 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0604e023f5c6722d46ef6793af281ce<br>SHA1: 3eb54f1eebcd039df05135ab29260e09bdd4fefd<br>SHA256: 3c8d20a60ea0af489cb12852284187081cd8541958eecf909e2f4c90e9f0555f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.02MiB (23.09MB) – 334,578 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d24f67bbedc322d93d7843237e6d08bc<br>SHA1: fdf5e7611f467995a14f85f97c32c055b05d983f<br>SHA256: 122f2768c962576ccb07d18b092f50799b7b9ea494a23db97a4bb4754c05e303</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9MiB (179.2MB) – 2,956,256 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7eebf486d9c42702ac790a4ac4e81b3e<br>SHA1: 110fe57678506100a087eda5e8cea65a848958d0<br>SHA256: 80471fedc344947500ec0408ae5d771afe66c98c0ba3989ad3f556cb157c73ed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.9MiB (302.9MB) – 2,799,002 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bc462fd69a5966f640f89baf03f95e<br>SHA1: 51eb98defa6d6bc9f2d654be1fc3e566c1803852<br>SHA256: 122e835b4e22ab281b426d9e1eff933fe165e08f77812b4b427e046722b296da</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-01-16<br>IPv6: 2026-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.14MiB (12.73MB) – 607,548 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5354da80ce4338ed3f8e4839c77636a5<br>SHA1: d88c0ad8da42bb0cd5648eb51d679846b43789b1<br>SHA256: 8c19657e94d6973d194c558c5f492cacc49adb01fdbf1ffc31237e41f3303d86</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.63MiB (44.70MB) – 647,830 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcf7134a374e5da130c9a6583a168dd2<br>SHA1: 2d124d6732e61f625fd8b917dd0672fa2ccfe67f<br>SHA256: 0896b337a7d94c65e9c06026b0b95a0a0d4602c3f78490019332cb503584fd21</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-01-16<br>IPv6: 2026-01-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.1MiB (186.7MB) – 3,516,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d43c6de855b4905b57b9b36142b5f10<br>SHA1: 7f29b39051195a9e9b7956971fc5907d65a2748d<br>SHA256: 2a161b7bf083219672794edcea7c2340f9fef17bc175106c355bdd18b636b8a0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.1MiB (198.3MB) – 3,516,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7406299056d50598a66546f74df7199a<br>SHA1: f49f8541cb2d28dfb9787ee0c1168e3a9c2a3ca4<br>SHA256: dbc6825fb778509b8b333a8bb7d82b17e0b5d83f2f07262dcee7153f61ef23e9</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,516,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9bdfe241aa74f87db0caeb228834f7a0<br>SHA1: b4091cfb44df4aad13958a5b930ac37f097f451b<br>SHA256: 874c12baa41401ef12359e063ce60f050123a45277dd88a2423beced34cbdcb6</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.0MiB (188.8MB) – 3,516,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89b513fcc222eec424abf5c0c74115e1<br>SHA1: cbd9f85c553bdf43e5c6407a1c1e428b2bcd3b20<br>SHA256: 7cd33774846a280ba4d165b759a69ca1c09d50365fd066f49d6833a7b73fab89</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.0MiB (235.9MB) – 3,516,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e3f635f7ef13f5c8b2d23002f43edc<br>SHA1: d54590aa3896768394299d0ae0574d16168d5392<br>SHA256: df54e6e046a1b57644271429b265be7d8a007b2971c52336dea7bd1b6426f46b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.7MiB (185.3MB) – 3,516,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e864e26589dd4f0b5e2bcf8850c33292<br>SHA1: 5c52c382e02c88ef0e430e593fdbf59fbe2dd11c<br>SHA256: d4223686d80a7dfebdda95d780c91dad9e98d21abc5390592b26629100264a56</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.0MiB (229.6MB) – 3,516,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4e094ee574fdade5a781f963724fc4e<br>SHA1: ca284d309a7d9fe4f61ac466c6f094b28a5eb42b<br>SHA256: a7179a082c48a32e9aac2816edd0c62b9181c5a097b4a0be40587a085925675e</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.9MiB (192.8MB) – 3,516,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3d080f8563eaa9da0f0f175a30732d4<br>SHA1: 38985a16bd50bcd97523ff7b5be6385b695a0767<br>SHA256: f2503d2dd2621c268dc04db6cf21acced761a5c5316c8cdb3a826077d31046a4</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>189.1MiB (198.3MB) – 1,990,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cddec1567935f0de7f7130b115308fb5<br>SHA1: e3b215bf304c61c5aa188d15478c604a05203034<br>SHA256: 3c239ce6ec5e8651901dd08377c6ff0791320c216fa6d00e46fb50680e74f7d9</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>193.6MiB (203.0MB) – 1,990,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 144a2ddbd5cfe38c1a44f259fd145a82<br>SHA1: b711b83974054676a103cc317788ef0e84dd2ccc<br>SHA256: 38afcbba562365c4051a642543b1d04a2fd8dd85c36f4f0b4b25031afb1080f8</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>186.9MiB (196.0MB) – 1,990,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71de87ee71f9258844e0c4906dfc4116<br>SHA1: 382554b1ddd96fee096ba45cd2efa046e56a18cc<br>SHA256: 4767b90534703158a7c686235c78a306c120d11b026f55e91a723daa85a3b159</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>187.6MiB (196.7MB) – 1,990,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23a223cae920fca4f9f260a080517dc6<br>SHA1: 89a10eaa25b289977037b3e4ba18d8e6a4e3afbd<br>SHA256: d250e80d004a139576c9b2c4a90046933f79caa3abee5879b363b9ddb26834ca</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>208.0MiB (218.1MB) – 1,990,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5de6f0050b89c3320f2fdaab7cf38ba8<br>SHA1: 545314b679e737051ba207b15ee2ace63657a1e7<br>SHA256: 36fcc9a8668b5dafb27972d906c23613a3dc70fd88bd7e109dd7238b3228158a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>186.7MiB (195.7MB) – 1,990,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b978961219ae97ac233458d69a7ae12<br>SHA1: ea2a4046d14aa8b044b7e1774f11d1fa9998353f<br>SHA256: 6c412ebb1629f7a36c0c743479715245eb5aa57fbc5191d6dde01ef54f27e003</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>208.0MiB (218.1MB) – 1,990,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 783f276d89d1e53b4d37c968d49c4bb4<br>SHA1: a7ff620b5b9d40daaa2f1a98e4f4b98b46273baa<br>SHA256: c66c773d361f1ed308a9900acacd00d41ec00fe02e6945246cf81fea74d722b9</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>190.2MiB (199.4MB) – 1,990,015 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76933cc852089ea9dc4e43b309195fc5<br>SHA1: 6fa36464df042ae64efdbde7d7158f4691a09516<br>SHA256: 896bb69d69a762cf2339723094b4627c422d91560c84954450b63239c36d785b</pre></details></small> |


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
