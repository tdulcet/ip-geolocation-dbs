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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-03-24<br>IPv6: 2025-03-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-24<br>IPv6: 2025-03-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.371MiB (8.778MB) – 419,171 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c951c4921495d02a24292142f462fed<br>SHA1: 213a72f352acaf451227b57f7f8d5ea8def85c90<br>SHA256: 4fb4f1385f68002ed2ae92858dd0ba583cce51ccd8723ccc45374b6aa7004b01</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.002MiB (7.342MB) – 106,514 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0909844cf71230c0ce8a752c300a2014<br>SHA1: 29e1815a631a954883526b3eb60fded8918e437f<br>SHA256: 2eda22cb0aee7717454d455c48b62542abec00038dff1179959dcdcf4652316c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-03-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.62MiB (13.23MB) – 631,882 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd6af5de2cdcf2d52be5ab1d0dba9104<br>SHA1: e370aa44e5389035112e2466e6fcb1e28a2386b1<br>SHA256: 8ac128b84620a279506a2b2413998cf2707b2e17e1b20846a197263aa754829a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>71.31MiB (74.77MB) – 1,083,658 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3d0888ee8f6732bb6715c2f159fa966<br>SHA1: 5df82e5302194141443c0d24ece3d76b4e33874a<br>SHA256: 1bdd735893bca940d95d9c8a3b95232b0a54a1762d07a6b0ecf2ebf0cc74c365</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.404MiB (7.764MB) – 372,055 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e5911df23fa4121906510a5a567b13<br>SHA1: 9325bb0b20fe7cf38b086bd997249c0ea0460073<br>SHA256: 388e526b141f72da365e6c1487008eaf5440f4e2a173bfada2766c55cb3eb316</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.53MiB (17.34MB) – 251,265 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609d7024eb89dc7bd684d0207b3733b9<br>SHA1: 956350aa870d6a38630af3f3a3b53278471d39bd<br>SHA256: 95146645c0293ed5818f1df79ae51e4c9c07a1f6c91ea0f9331b8da35b754bbe</pre></details></small> |
| | | Full Location | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,335,187 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d87186c64f981273c433100841370<br>SHA1: 62922290000ef7c4549382119783c2045e4d1e6a<br>SHA256: 51718b9bcaef22b3bcf85a754a3a5fdd48d4a0efd9af8a4e3532e918a7368b41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>388.5MiB (407.4MB) – 3,770,967 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a5296fc623ecf8f0caa811c6b1aa61<br>SHA1: a31112844edcf6b611b51dd56508b700f7dfd9d1<br>SHA256: 4018f4afbdecaeedf11e8e21fc7f50e5719bc241f3a50121788f441946a9b58f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-03-24<br>IPv6: 2025-03-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.118MiB (5.367MB) – 256,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced96baa8d12dd7a7473b62ca04f3ec1<br>SHA1: f15aed8ee671e3e27c23c736e23edc25368ae1b8<br>SHA256: c034868fc655de42297d14220caccea0ab330ee13028773c38db7c6de47b21b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,344 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cef1451430608ae8ad70e0f4963dff<br>SHA1: 43bd5d1e9844ece7eae20604c4d83f7960da31a0<br>SHA256: fed2a958c9ff8365cbd35a38e1b062b5237d9c3576831c5f27705c77a13bbff3</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-03-24<br>IPv6: 2025-03-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,062,954 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1de2b09cb2477a5e3a644739a02d816<br>SHA1: 2ab572bf0cc2040a312448643055f2f718ca5ac5<br>SHA256: 1d66b45f20fdcc805cf1b87b04dc600ee7e3bcce4b90b5400d770f1ca47a3254</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>233.4MiB (244.7MB) – 2,257,726 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d52faeae6d9b914518dee2695e772b<br>SHA1: ba805ee8a2f7aede9c579332c56ae8ddfc7f7251<br>SHA256: 87cd4c71031299fc55a0c464dac619478c748c283c398787e9e7547a3ae9b9e1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-03-21<br>IPv6: 2025-03-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.37MiB (11.92MB) – 569,087 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea33403090bd4f9ad150e63842d4e048<br>SHA1: d9adf98fd15eda78b9d41fcd7bc0555b40702578<br>SHA256: 2a88ffb2424de499a93b67c2a765ef5abdcabf6ae4ae91393bca5dc1a5e3b602</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>38.55MiB (40.42MB) – 585,842 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9661e85e6adcce2ef728d6d0c15f65d<br>SHA1: 3bf2e76018d2cd86edb88e3de5b021e1833c23d8<br>SHA256: 2039d39ac9c0006cbe2a6344181d4f311e6decadc7e8dcd186f459aba5a2d2f5</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-03-21<br>IPv6: 2025-03-21 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>168.5MiB (176.7MB) – 3,329,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad51b8fc4e000c5c85563c4c591e19b1<br>SHA1: 5cd6023f089791a79375dc47f3ed89f4c410f8e7<br>SHA256: 6e115b2212b6918b97296ad697ca5087a19866625081b7e274809cdb72e8d80b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>179.4MiB (188.1MB) – 3,329,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88c053fa001cd980284e2689da3bca00<br>SHA1: ec1c3250ce55cf6c88f718cadcbc45b6b28975fa<br>SHA256: 6e6aaa25546d2febd14c71acbb31e74ff7d8c4abecd3d1032412afc78a5c025e</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>167.4MiB (175.5MB) – 3,329,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a18eb9e60d8d63e364d5df45d5188ef<br>SHA1: c864419aaccc044e3aa053214ee3e4806107051b<br>SHA256: e6caf5fb1fececfd84c99eaa68fce968e6f873d3128d57bd126c2c2fe72f5d03</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.8MiB (178.1MB) – 3,329,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97ea4dd2dd5e7313a365592aa7037078<br>SHA1: c592bc0fac9881db814d9e026174b981edfab704<br>SHA256: dd1db174ffdf09407d162cf98ac1c005e9ee1bae92c78f229dbb5eb8ab50fd66</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,329,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30ae9222ba5f5287918b64fe12ae3306<br>SHA1: 76dc7c3777cd92d9354cf237bec81beb0a500be0<br>SHA256: e57371a0acb8350df1f59ef147354bc56d3f24e8d272a767fe11070f87c90877</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>167.4MiB (175.5MB) – 3,329,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7b179ac612470e50d2d6126862c022b<br>SHA1: 9b9c25e0ef55f8126bfbd357261f79a8130cf0bd<br>SHA256: e1c9eb9ea69384076f3fe670b602489bf3b6ff0ca51c1005f82500dc139529ff</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>207.5MiB (217.6MB) – 3,329,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec3827c699f485539b4d409b66348787<br>SHA1: c8e73a0bd8e5eceb682511527b79698f9ce91f71<br>SHA256: 72f0f751d0774ae1b78337210835c0048ec3f3e37691251843781fb6a206c9e1</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>174.7MiB (183.2MB) – 3,329,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a9b2ca3a5b02ca82278251e92be6028<br>SHA1: e3f3fc2f59e98f44c26a7dd60456e0a18bf5c6c2<br>SHA256: 284bbdc4b59ae47018cb650684f08532ffebb21ad36b1781e0fa5a23726cbddf</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>173.0MiB (181.4MB) – 1,839,198 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3aa903ef48006c89dd3acd10ac671ae5<br>SHA1: a584ac9e4a82e1be02a3b1d6e071caae8f57a9a9<br>SHA256: ab10f0a16793b49f6fc80e9fb1df4ae72c62926ec13e68f67a30b30234e3d079</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>176.8MiB (185.4MB) – 1,839,198 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 419c4ef533d15f6edf3efa65ba9cfcad<br>SHA1: e73b60c0b40d30cc77a76c41972dd911129c4247<br>SHA256: 1d802a6cd96982eb18c4f63d80d5f034422ac0958753f99009ee18851dea5a39</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>171.1MiB (179.4MB) – 1,839,198 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05e16cc89b5f462d3e47d89783d3d776<br>SHA1: 69b8e24211a3f9eb87a24b296e9ac0ea4a01e8ea<br>SHA256: f53bbb6d5ff01e1892c05d245fa08faaac5b14c698fbf91fa423a9292ed9ac2e</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>171.5MiB (179.8MB) – 1,839,198 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f708777eafc9391f2fd67580c14c51a3<br>SHA1: eac67e90425f832dd70461918f62a82d61b15a2a<br>SHA256: 1ca25d9494dd7564dff6667505161d50b2c853130320864044f5713c09486085</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>189.5MiB (198.7MB) – 1,839,198 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7bfb23dd0d23e52a6ac6e80b3681827e<br>SHA1: 2fe8e4929329abda1a0b1d8116be273a258bf580<br>SHA256: 8d71307d3130d1e64be5d5acfa6ea6effd29707b2f43caac6e61edae228f6f91</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>171.0MiB (179.3MB) – 1,839,198 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63c22ddee4ef967b05b10ee6c8e0a4d4<br>SHA1: b8da004bb6d43e5fb2f7a5c021858f80762a959b<br>SHA256: c335e6bf4690c3d22c516c89205f5082c9c1cd25388426d439f2ca2eb3af2513</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>190.4MiB (199.6MB) – 1,839,198 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcdd92c7d0c4ffee9772a4c637533e61<br>SHA1: 77cf0b493b614307538cbe70d7248b55ad22b002<br>SHA256: 7574a2475540e694d410a07b70aedd9419c256ce89048c3cff74edf0637f4295</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>174.9MiB (183.4MB) – 1,839,198 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9beb049db3662c5b39e4e817c628878<br>SHA1: cdb4bd2aca74b9f889975392757f9b8af918884b<br>SHA256: 4406e51aa6013f947a7d268f71ed5486949b1c8ab4b8361ad07cd9289cf2e176</pre></details></small> |


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
