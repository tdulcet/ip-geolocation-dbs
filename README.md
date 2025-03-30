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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-03-30<br>IPv6: 2025-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-30<br>IPv6: 2025-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.376MiB (8.783MB) – 419,432 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15079c114920d8e3c222dd651d998271<br>SHA1: 3d12135120c51dd99885ce621d05787be7b0d98e<br>SHA256: 6fa90723eea1525be0b0284d0c7009ec869d9bc7ace128f103c73a95cd95cf34</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.988MiB (7.327MB) – 106,302 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 175a4e8691dc5eb658ad8f72e6558ea2<br>SHA1: 0e28cf7b50ce884ab78ffcac5d35adcb0eb95937<br>SHA256: 8ae25748c78f36a34c820dd584b25a24988a6a1c2059b162728f0e079f40ce74</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.56MiB (13.17MB) – 628,797 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24c4db2b75dffed0f82e085706e351e8<br>SHA1: 3b3833696fc8cfbf4c9bc1e7cb48da23896ec0fa<br>SHA256: 2bcd4b67389691c11dc23d7a0d292a946cbb6f1f5b17b8e5d9f604870fec64af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>71.21MiB (74.67MB) – 1,082,214 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6170909edb51e28e031d6de9d87386d5<br>SHA1: c9118c8e2d328d2197ffe73bd0f346ec98c30ad7<br>SHA256: fde1cad4387c523302452714c562c88100afdbf815983c0bd09867c3066f96c2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.404MiB (7.764MB) – 372,055 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e5911df23fa4121906510a5a567b13<br>SHA1: 9325bb0b20fe7cf38b086bd997249c0ea0460073<br>SHA256: 388e526b141f72da365e6c1487008eaf5440f4e2a173bfada2766c55cb3eb316</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.53MiB (17.34MB) – 251,265 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609d7024eb89dc7bd684d0207b3733b9<br>SHA1: 956350aa870d6a38630af3f3a3b53278471d39bd<br>SHA256: 95146645c0293ed5818f1df79ae51e4c9c07a1f6c91ea0f9331b8da35b754bbe</pre></details></small> |
| | | Full Location | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,335,187 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d87186c64f981273c433100841370<br>SHA1: 62922290000ef7c4549382119783c2045e4d1e6a<br>SHA256: 51718b9bcaef22b3bcf85a754a3a5fdd48d4a0efd9af8a4e3532e918a7368b41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>388.5MiB (407.4MB) – 3,770,967 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a5296fc623ecf8f0caa811c6b1aa61<br>SHA1: a31112844edcf6b611b51dd56508b700f7dfd9d1<br>SHA256: 4018f4afbdecaeedf11e8e21fc7f50e5719bc241f3a50121788f441946a9b58f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-03-30<br>IPv6: 2025-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.118MiB (5.367MB) – 256,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced96baa8d12dd7a7473b62ca04f3ec1<br>SHA1: f15aed8ee671e3e27c23c736e23edc25368ae1b8<br>SHA256: c034868fc655de42297d14220caccea0ab330ee13028773c38db7c6de47b21b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,344 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cef1451430608ae8ad70e0f4963dff<br>SHA1: 43bd5d1e9844ece7eae20604c4d83f7960da31a0<br>SHA256: fed2a958c9ff8365cbd35a38e1b062b5237d9c3576831c5f27705c77a13bbff3</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-03-30<br>IPv6: 2025-03-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,062,954 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1de2b09cb2477a5e3a644739a02d816<br>SHA1: 2ab572bf0cc2040a312448643055f2f718ca5ac5<br>SHA256: 1d66b45f20fdcc805cf1b87b04dc600ee7e3bcce4b90b5400d770f1ca47a3254</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>233.4MiB (244.7MB) – 2,257,726 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d52faeae6d9b914518dee2695e772b<br>SHA1: ba805ee8a2f7aede9c579332c56ae8ddfc7f7251<br>SHA256: 87cd4c71031299fc55a0c464dac619478c748c283c398787e9e7547a3ae9b9e1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-03-28<br>IPv6: 2025-03-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.41MiB (11.97MB) – 571,421 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e9437a8ea79f4cd088b6003d01b016b<br>SHA1: a28999654018b5a66164df6b794f9d21f33b5ad0<br>SHA256: 4c3e0cbad0bbe9ae0eeb56320ae85743853fd0e80baea050aaa21ca6b6ad25a6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>38.72MiB (40.60MB) – 588,400 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ced3d87d2bffdc8cecd68a9b3a31974<br>SHA1: 4c63276a52de332c820d16eddaf2f2fa411ad760<br>SHA256: 873dd0980cdb330d9645a7a2b81390b35200bf7171ff09445d58512f692d90fb</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-03-28<br>IPv6: 2025-03-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>168.5MiB (176.7MB) – 3,329,736 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78d7e04e4c2956c6d7fe538cf1b05933<br>SHA1: 1db12cbaae57bdd2305ed9a6658f0205155a21e0<br>SHA256: c9d02cf7c4057700f51e3863f9d312bd3f0ad1e65279e62355ba89dc13ea2917</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>179.3MiB (188.0MB) – 3,329,736 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a1d9be0a68919b033488d128875b84d<br>SHA1: 1b5c139ac75de1c58902ccae4d85b618e486cf56<br>SHA256: ac7bafcd50a29a128febfc3e08def70f6ded8fb316e9261d808d737aaf2b45a8</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>167.4MiB (175.5MB) – 3,329,736 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6c0f38095727fb6b9ca5bba4379cff5<br>SHA1: f555fc0bcbced065587604c3e854d2357f1fa27d<br>SHA256: 143527f7842432aa641399d30ed491737603db676544690e48e82f18fb1a6f4a</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.8MiB (178.1MB) – 3,329,736 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e76f771b312395ca38cf0cba8a07106<br>SHA1: 4473fc4b0808caf179dd13dc1a236defaffffb97<br>SHA256: eafedc67396dd0d22fbc64508b913651ef5d48432b60b66034db4d4ab1ac2e01</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>213.5MiB (223.9MB) – 3,329,736 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 787f96bc7a8a4393f192a35657054f43<br>SHA1: e15bed3127f18ac9a7ef8c1cb0103c907c5bf946<br>SHA256: 54a652aed1cd4351aa0cfc8428d40cadf23846b1b10291f95737dd7159f64c72</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>167.4MiB (175.5MB) – 3,329,736 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54038780e41351664056e2b01eefa210<br>SHA1: 53a0bc9a51df3710532c71b8e9a1135fa9906b6c<br>SHA256: 68f54a128d9b86bfdedbd695207fe6b9c3c72219424d5eaed90dc945cce79aff</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>207.4MiB (217.5MB) – 3,329,736 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9b3018b900ea8030e2d4c62b9af6db9<br>SHA1: aa56443e9f654c616983d62d2642803af7114dca<br>SHA256: 2698a845ceab4fa633792f508a50913fd4d47c55d13fcc25dfb7f93fd0a7129b</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>174.6MiB (183.1MB) – 3,329,736 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35104a17c9ef3bbc2d30e69937533769<br>SHA1: 2ee57fdc0369c911ad03566709a685ea8662de18<br>SHA256: aa8a67ad1adfb8d2ddebe5cae7226f66a19a584f0e242659b3db548a54db215a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>173.5MiB (181.9MB) – 1,844,978 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a645fe1607841fc7eedbf340dbed116c<br>SHA1: 85190b811ea0928bcd41a119505e4d6a0b7f3d13<br>SHA256: 0a1c0a753e9f96208c1376970c61eee13feba3d53deffaa5cfbd1564b547506e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>177.3MiB (186.0MB) – 1,844,978 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c35fc397e1392b2b5550db238f85c87<br>SHA1: 2bc1ce9532d64fef80c0093d1c4d97e78630cb10<br>SHA256: c795c94b3ed98962ec67723d7f13e3a7a476e16e0a63bbda5bc08106c9a0008c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>171.5MiB (179.9MB) – 1,844,978 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d2278428b4f56bb4598f36d7aca51fd<br>SHA1: b87fa60fbc49b7abee689deafcbcc0661189d84a<br>SHA256: 69358caeb492b533c612dd8462e8d4014f7f20272d4e6f2a1709b4b01271f21d</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>172.0MiB (180.3MB) – 1,844,978 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78a0021c63bdc04145da0bfe6e19e09d<br>SHA1: d41e95cf8ecc8e5aa3caf5bb6acda9ebb7cff831<br>SHA256: 4856479b8354756cefe91692d583645359093706a2844e5986f30b46e2b751a5</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>189.9MiB (199.1MB) – 1,844,978 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d61aa76d9df056c723d86a2fca5b372<br>SHA1: 373c99cda73f26d13ba821b532965f3c2f9a87fe<br>SHA256: 2e16135532c748654bf7f0c121c31eb985bae3fc0d48e76bf5cb968e1ced41ac</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>171.4MiB (179.8MB) – 1,844,978 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a3a86864f1d09329e7583775b5ea4e6<br>SHA1: b63594686ce7763e434fb70995ed33b1eac3256a<br>SHA256: 8af67bc15bc9baf89b5e72dd80a0bf14402d39db1c56199415b7c6425b0df197</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>190.8MiB (200.1MB) – 1,844,978 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86fda7821b4ed256f4af5eb2e2dbca2b<br>SHA1: cb59743ec07a3c0f73165cc12b68383880389c3c<br>SHA256: 115a1fccc5677f74a0b6cc4498efe2a0ff2e40dc6c61b1609e3fd87beda34f54</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>175.3MiB (183.9MB) – 1,844,978 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19074ef5972c3614dc8e3e2a30789428<br>SHA1: 426efb7b693f3db175e088b05377d366d4cba16e<br>SHA256: f0d729ae919329ac874c7e71a5c8e9fb7c1a61963b2e6f34ec7e0bc1777a1045</pre></details></small> |


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
