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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-02-23<br>IPv6: 2026-02-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.458MiB (6.771MB) – 323,348 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5857a64c651bc194eb5cb6acdc2402a6<br>SHA1: 6fa71c5b123366f4dbb8867d6eec9c2313080d90<br>SHA256: 325c176b85eb9e6736043b74c2c8bf3b6f038fa9228fb1337cafb4eccf999395</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.24MiB (15.98MB) – 231,558 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f448c53da1a771521f1c82b71d4b621b<br>SHA1: 67c42ec5b3e62c7b8d20e4cd02d31b016d46a2df<br>SHA256: adc11c0043e45a3f8bc42cb2720d5cde1b3f3fba70a56f2ee6c11d60ba99ecd4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-02-23<br>IPv6: 2026-02-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.790MiB (9.217MB) – 440,137 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36edcd4ccaaff04ec233f7cfb1e4e554<br>SHA1: f0d6a2368ba484935874b4e21b7e9445537933e2<br>SHA256: 7ac37f4cd297af65ddf1d4aada6c5606d30694f8a0c40c28b62c840f5e463ded</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.620MiB (7.990MB) – 115,911 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 462e4683d699429442cfafd836f1f3ed<br>SHA1: 2bd119c2c735abd7cf4742887620c28df3b175c8<br>SHA256: af22e58445b453cfd78c8aae82ec500522ab11d4980e5ac07c8deafe70dbb2ce</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-02-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.16MiB (12.75MB) – 608,701 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 540c8c24a4964d2fc54101d139c34d80<br>SHA1: 57e595980b29f4f98cfcaa76e2cd15f9a1255390<br>SHA256: 53200b484c87474b86160df6c83252711964f0f9da84422ad703e72ce41683c9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>123.2MiB (129.2MB) – 1,872,042 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e1385ffe2071424c759533dff3be4dc<br>SHA1: 936ea39932df4ce1d744c38c1446a57244d0b699<br>SHA256: 9803369276f2e70d0086b4375c69a504c91181ea928a37a6e6d24b89870c01b2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.768MiB (7.097MB) – 339,077 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0181205d24255559b4c2a13fdb0c95<br>SHA1: 77c5ed2ef6799485a1ff6d1bd9aa3aef442555aa<br>SHA256: f1a904010b8cf3e5db4f0ddc1b0fed4c77f852aa52effac37a04697ddb879a37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.90MiB (16.67MB) – 241,625 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f8f77acea5ee52ad5d81c9f3883d7a<br>SHA1: d3a894c2e7503a5fe5168eef49e53379425930d2<br>SHA256: 80ee4bf63ff4562160eda9ba68902de89a9e28a828c048003fd188647039bf1f</pre></details></small> |
| | | Full Location | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,746,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48770c63478550e9d616b0e8f11eb35f<br>SHA1: d754e9f10a536891a6f76b212ce1527fccbb205a<br>SHA256: 3abef96589717a094c9384cc0d2e88d16dcc6c1771a5eb42954efe056fe2caf0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>452.5MiB (474.4MB) – 4,397,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d15359a3c2245bffe65895c5939244<br>SHA1: a5622976378fbaa83dd68ce8bf186161f41252b1<br>SHA256: 3c33680bdbdc577647e1e500060fa0db02dc2af50f79e20bb78a7ae7ca1b33bb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.362MiB (5.623MB) – 268,369 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4330c0bbff3419f12c7f73fddf1cf704<br>SHA1: b4df563510fe7f5fc4e1d278ea041c62c7bdca5b<br>SHA256: e91c6b0f644a92d45674456c276b13846b9893bbf0eb311dae698ed2f3d44d57</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.43MiB (23.52MB) – 340,836 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a2d9ae09529fd0059afa4956f1793e0<br>SHA1: fdd2b4377c51cd148c50a2369808306b7c9e9c10<br>SHA256: aa8f17dc70c0dab48cba63b84addf77a95f2d154825fa5a1cc5a78e9b68ebfd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.7MiB (183.1MB) – 3,022,797 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63a84f26611e75064d6ca0974428a919<br>SHA1: 8280052bb209735824b9571ba8e1d3219f239f41<br>SHA256: cb6a41dd6ecfae830dbf227d07287c122fd823f9a56e968851d364746039495e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.5MiB (307.8MB) – 2,844,839 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a06e5ce285e86fe3c964abd92c36fbf4<br>SHA1: d5da4217a5c723981f96fe1b85823103e5248e1b<br>SHA256: d40b02049ece0c3e7ec8afcbbbece0eda05c646fb3a3a4719bd5bbcc13b321b3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-02-20<br>IPv6: 2026-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.08MiB (12.66MB) – 604,618 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0e68fb1b4d86e22c897da806811c68b<br>SHA1: aa9683bb6106d0a4ac35d193965950837b49f546<br>SHA256: 55b499fd515408f922b23199ca6a6074f64be373837dbeaa18de8de1a3d27e44</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.00MiB (45.09MB) – 653,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf05b37ad6c799c71a8fd1bd75a57683<br>SHA1: 6ce58dec3e90cc2aabec65ae24d0ff89b2b1e58e<br>SHA256: e803426feafd349ef6eb63fde47de2a711e41b487faa73fa4c171f9236895393</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-02-20<br>IPv6: 2026-02-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.7MiB (187.4MB) – 3,531,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f9faa5f524c8d9d34832da5c7513cf9<br>SHA1: 19f17a805f49666a386c6e32f8f519fafa969a87<br>SHA256: 87a3f465862418654709ec01e7aea77f8c039d3527e64e70fdeaecf1469666ad</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.7MiB (198.9MB) – 3,531,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ec08f0d60ff92a833b8e9af6cd507ce<br>SHA1: f5330923b1a94b1ecdae143d07c65dd51e92b726<br>SHA256: c1c41656bf2d2f15d25906d4ed0b393e7da07fe2810b6996fd579b23eee28098</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.7MiB (186.4MB) – 3,531,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b643e75f2b8e6d3f3486a3979bb7cfa2<br>SHA1: 9e3862dad8da074521bc53db0cc633f62158c31e<br>SHA256: 51c0c190a0caa5d95e5ea60371a5cd40390a5821885834dbb236c0a6c95f7763</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,531,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73464fc3f74d13120ff0232537ab1333<br>SHA1: b1de6f216a5ab86ebb60d886d132b0e214c35724<br>SHA256: 5ba93f4cb75a913fc4826fa977d83868619c3299b958c9c2ffd399eaedd94916</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.6MiB (236.5MB) – 3,531,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b74a9faad831cc1d3fc594cf1afa748c<br>SHA1: 86d75401c17a88ccfce0dc9ba916399dde869a96<br>SHA256: 99efab2a6c6285a57502888ec230f3cdfd24f109f32a330aefdf2d229d1dd76b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.3MiB (185.9MB) – 3,531,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c2b051a022f9163e5c12fdb4109c3a7<br>SHA1: f81f38cb16c12e15f333a87fc3f537bc6f4def9c<br>SHA256: c43e19a0bb74578f45c5b513ea3b39bb2fc28a889d8dd9ef5e092a48de52d692</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.5MiB (230.2MB) – 3,531,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16c91576c17710266e4854f93a4d6466<br>SHA1: 2ac1e34c4e8c0174ebaef19da4900c98dc2e49b4<br>SHA256: 1757ac3bb38964f82e6409a79faab79c2ce7ff2f45061a11a5cfebf57774e739</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.6MiB (193.6MB) – 3,531,833 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f3091874fe3c1895e6d447115b395c6<br>SHA1: edae7017c4e38b806ac27685fc69b149949acd9a<br>SHA256: b4fcd8da224cce2f86ec049d312643660f348e0b8844606e135b5c6713e455e7</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>189.0MiB (198.2MB) – 1,991,383 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c4cd81d8b7cb8fa25d32c884577e591<br>SHA1: a2dcdad3d1b0b9e2d1d2f3febd3e3c5a73f054bf<br>SHA256: f7436dc7756e240a31cd19ce1fd15ff600659bd7f7efb9de67f600e93797b069</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>193.3MiB (202.6MB) – 1,991,383 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d089cf77551cad7fdec4f0b378e6780<br>SHA1: b153cac0a2c6af850d1ffa7a013d832c7cd6ee5e<br>SHA256: 9d6792f7d3951b915db50c8acb09a9ac68f3f43f545ee7da880fa9b73e8cc9cc</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>186.7MiB (195.8MB) – 1,991,383 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e8553569e4792d81bd15914b3086485<br>SHA1: 75635caa95aff7a051bbc2a132163f3b1847ba15<br>SHA256: d6e21ffd80aa7e2ac96ae22fa6483aa9db6259047d4835f123c4e7b437c38fc8</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>187.4MiB (196.5MB) – 1,991,383 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 028333bf587bac99651cbb51f5f5d8a6<br>SHA1: 422b79ffd37486e0fa446c1f2621643bed70c8a4<br>SHA256: 2616329cef2e8d05692ab2651e5ece63669663a3c92858aa7bf174cee932706e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>207.7MiB (217.7MB) – 1,991,383 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5ed720140f6b97b471efbc72baff505<br>SHA1: f355d4462644f2fe31e2804e47cdfad763862d9b<br>SHA256: c31c2fa7f8ea9365dd48635d1421c8c9742632e1e32a6887f2b049355446b3ab</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>186.3MiB (195.3MB) – 1,991,383 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0072fb2e3716854c289696767b3b322<br>SHA1: 8f9040696534befc0f4953e823789a8d0cdad5e7<br>SHA256: 34065b03512f06cec4b67ab1b430cb7f4f4950be0dbdfaf7c54a4cc19061c3cb</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>207.4MiB (217.5MB) – 1,991,383 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1783d2a2fd8b47077a817f049e2b4cb8<br>SHA1: b0065ee9bb3cd26034a9cf55e5c911496e10f7c3<br>SHA256: 5f10cf25147c4f8c0a9b06bedb2afa4d1a979bd2836725a1967df63179f807be</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>189.9MiB (199.1MB) – 1,991,383 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0681c7cf2f656235d9fc05654ef1c05<br>SHA1: 920e976e529e7f9856a3f307ea315dac0c54397e<br>SHA256: 4dee5675eb72e3c49ee65e4002995f995a40cb9769bd5a62073c48a3b3d407ca</pre></details></small> |


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
