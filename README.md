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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-01-29<br>IPv6: 2026-01-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.421MiB (6.733MB) – 321,517 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b6b742523a525f4e88f6b58cc75a73f<br>SHA1: c587516b91370924395e8cd929897a56d1593db6<br>SHA256: 138a8160d8400b7bee67ffdb6e83413163308a0766254683d1a9d46a1b12ea03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.21MiB (15.95MB) – 231,162 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b653e3e0465e1a57add20948e5a05b89<br>SHA1: aaf55035cd2ac71da2e6cd8471285b027560268c<br>SHA256: 5d6d1f0fff4435528d8c7ddd4bc50c60ee98211cc553117cf952714216d47c5c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-01-29<br>IPv6: 2026-01-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.216MiB (9.664MB) – 461,401 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f68a4e6ae08fcbcd25f7aa3dd36fff75<br>SHA1: a2848f1357fd29b654f150a7ce50709ca41fda22<br>SHA256: 0292a7beeea0496c53ff61536821dcb7a5554c84b43284206cc5654a062a8de7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.558MiB (7.925MB) – 114,969 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb82885242668832eeb93eb618c11b06<br>SHA1: 4373bebddaf1f22130223004a6dfbc0fd55ef78d<br>SHA256: 13df378687965b94a58422f98a3a86514d69ea093cee0aef970f68a0ab5aa4a1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-01-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.07MiB (12.65MB) – 604,072 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0810e7f94206d75f687e0dd3b3d6d601<br>SHA1: 0206a06f3f9ee1bbae3e52d928ba39f8c392fcd4<br>SHA256: 10a73fb2732b965c62218be742a3f2d795e0ba83e7653364b78429d4cb2d6a11</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>54.73MiB (57.39MB) – 831,754 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea8e4d03eb4ef85e88a9ecb33ee1f903<br>SHA1: eec00111d8e6a5348e34bf46c8d12ea0d91e6885<br>SHA256: ac8a84347480f92ad1eff93f8ff52df299873e723a82bec4e09b412edd48d046</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.843MiB (7.176MB) – 342,905 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7f0c42b88b3ee5ac2070e71f756f963<br>SHA1: 4416542c9574226ce202070dc48ca08edc6fab0d<br>SHA256: 5393382f53c552965d88b65e40e02f63c643f2379a931aaecef8209586b9ced2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.52MiB (17.32MB) – 251,059 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232548602865156556e4ff9d7db331da<br>SHA1: 61d1e0b2cefeca101ea9e8530969dab152188ab6<br>SHA256: b004edb93559a31ded3baa727a5d781edbe90c29420b4d5691f44e917e83bdb0</pre></details></small> |
| | | Full Location | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.7MiB (223.1MB) – 3,730,744 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42e04cdc8d81a8ce6b440accea48b373<br>SHA1: 9c414f68d243d9ebdc8b7c65e081580b035b663c<br>SHA256: 5274313529b847bd8629fb44b41144c683552f55760a830f535892f20b8e46db</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>457.0MiB (479.2MB) – 4,442,155 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56e8f0cd6817f6807824ced45628cb9<br>SHA1: 316812aba9e80b97b08bfca58defd796b628d008<br>SHA256: 44317ed175935104135d379f2a9918ca97141e9bf034ee1bca6cdf894093d72c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.345MiB (5.605MB) – 267,509 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0604e023f5c6722d46ef6793af281ce<br>SHA1: 3eb54f1eebcd039df05135ab29260e09bdd4fefd<br>SHA256: 3c8d20a60ea0af489cb12852284187081cd8541958eecf909e2f4c90e9f0555f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.02MiB (23.09MB) – 334,578 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d24f67bbedc322d93d7843237e6d08bc<br>SHA1: fdf5e7611f467995a14f85f97c32c055b05d983f<br>SHA256: 122f2768c962576ccb07d18b092f50799b7b9ea494a23db97a4bb4754c05e303</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9MiB (179.2MB) – 2,956,256 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7eebf486d9c42702ac790a4ac4e81b3e<br>SHA1: 110fe57678506100a087eda5e8cea65a848958d0<br>SHA256: 80471fedc344947500ec0408ae5d771afe66c98c0ba3989ad3f556cb157c73ed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.9MiB (302.9MB) – 2,799,002 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bc462fd69a5966f640f89baf03f95e<br>SHA1: 51eb98defa6d6bc9f2d654be1fc3e566c1803852<br>SHA256: 122e835b4e22ab281b426d9e1eff933fe165e08f77812b4b427e046722b296da</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-01-27<br>IPv6: 2026-01-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.11MiB (12.70MB) – 606,306 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e7abb1b5d196d91839f3e1cb468a09f<br>SHA1: b5674e02ab98edc5ffa96ae22eaced5856e57be6<br>SHA256: 3f18badcb63416e997fcbeaf3a769a1e3fa0e46ae0ac8f6c11c694a0ab74a4e0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.85MiB (44.93MB) – 651,126 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2c3165cbcf4dd629ff0be983f58c537<br>SHA1: b1a5bb55e8cfb3923d8a1d08249b5c1a14354c72<br>SHA256: 2c2ba055774ecb2679ad05e344504ab3a00ccdc420b598c3b8dabd9e82375dd0</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-01-27<br>IPv6: 2026-01-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.8MiB (187.5MB) – 3,531,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5b10e348a5b38cdc9fdfee349d3d79e<br>SHA1: b16dc1f253d51f792c9bd8b9cd6fd7b569ce2c7d<br>SHA256: 4a22efde1bf924f71389e352fa5a55456c968e0cdba7d6f8ddaa5e57e47e99a3</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.9MiB (199.1MB) – 3,531,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 667f6ddbd4fbecebf2dc55aa13da1a12<br>SHA1: 6aead62c8e53392b5dadfc7f720bd0938a098034<br>SHA256: d1dc762047aae2db9f63fab5650618d72e4c0dd7200828915f501cc7bdb715c1</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.9MiB (186.5MB) – 3,531,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acdb63a1709e00b457076a196da1d275<br>SHA1: 5f3b90843c744f4dd59b21ffd06ba1fc7323875f<br>SHA256: f5124e297fe26755f7a9eaf348552e9cb997af9e801ccf4d49ec306a77cfa984</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.8MiB (189.5MB) – 3,531,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fd76b10fda4c976ff32b921608af233<br>SHA1: c5330abef5f2fb6f7df92ab498f2f3236073fe1e<br>SHA256: d28407cdfd96309a5371f4f13a1672ea5c76049d11d19af9a40e03e50cb9d1da</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.9MiB (236.9MB) – 3,531,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60f39448813f74c1e20153de8042824b<br>SHA1: 1755810823bd1fb38d4e2a1f5714c21e9eb8118b<br>SHA256: facd7332446c5a8a130756c12308f928550fc3d3add3be117d0ae0c4fc12105d</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.4MiB (186.1MB) – 3,531,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3185bd2dd0ab746dca6f11c361f24871<br>SHA1: 24dec923ee9b71716cdede94c2b1ed181c44978c<br>SHA256: 723c0784d05def5e34ca7411fcae80b810d5a53de2d153a0002fde0bad25efc6</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.8MiB (230.5MB) – 3,531,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343fa28dd7b33ec585d9a8d7bbc167ce<br>SHA1: 5be93ac92a5e62acad0c29482a8b7b594feecd26<br>SHA256: fdb8330d7bda2c808065762087e391a2a3af03eab7c604b1ccf381128b46f07e</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.7MiB (193.7MB) – 3,531,592 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d5003317c542ad1f8e6c9b26da519b3<br>SHA1: ebdef76fc8ab0ef57ba44eb1bcf5742cd8d51b99<br>SHA256: 93fdfd466e70d6ff42c99fcc78678fb78795f0559484d2c0cfc682b1526ebfa7</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>186.7MiB (195.8MB) – 1,969,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f10635ac3dfeee210b849a03733faf6<br>SHA1: d37057dacfb5f184207317c1bb3e91e20005bcec<br>SHA256: cdd6f5cbf9d68e134082efd41653f48786ec16ebb90ea859a18631eaaa7cba5a</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.0MiB (200.2MB) – 1,969,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aef5fae4804e9160cfe8ac877a38de48<br>SHA1: b9882acffb55347743d340e6712f90b17c97912d<br>SHA256: fc661a94b1c880cb28a6c60b23c5c22bf9044b66e0434fea175334814d1a557f</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.5MiB (193.5MB) – 1,969,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b63b6e7e33e4b577b71d5446123d4faf<br>SHA1: 065c6d31f9d733ea30de01751a9dce839790a5d5<br>SHA256: c18650c536c46a591e556c564c07a4ee3a341bff175690d2e6c6f7890eb6b9ca</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.2MiB (194.2MB) – 1,969,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d97e6e5b28a216e035eec0afd9ac7854<br>SHA1: f5ec3453666157d96a7716e89f4defed6334b6e4<br>SHA256: 1f269ccb4c37e5778f66dc6a7c7a277c3a5ef1e4b4a15db30ee44b60a4d6232f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.1MiB (215.0MB) – 1,969,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 723c80e58cdf7b0a17d0db13331204e7<br>SHA1: 6a0b321e5ad71012ccbb451ebcd297ae90267e51<br>SHA256: 56db80617275ff3d30c5f5026435c097d2c169d1d82086c111d4e76f0f1b1709</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.1MiB (193.1MB) – 1,969,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27ad954f75afb941c821111b3f658900<br>SHA1: 595fe3081abbfee70f9fe4e2f07e8dc7bdd7fa2c<br>SHA256: abe803860aae0f8c0451f8eed9776b6e8a14743a08da9a7cd2235b4f852cab54</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.1MiB (215.0MB) – 1,969,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfff30ae1fc1975c030c7407fac0cf8b<br>SHA1: 53091c7b2c855000912c819ce8d39c0283fea57b<br>SHA256: 9b81668f84002ff83f985d18da32b58a07b674e8be7925c265a6f72b6933b230</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>187.7MiB (196.9MB) – 1,969,684 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c86d237da52cd5f004b861ddc8f82f3<br>SHA1: ba7b2246489bb59cc853ba0da95e116815bfb4c9<br>SHA256: 8257c6f85951d1d36b9802e653474516a68392f97c13c4e6f78f60b1997d7395</pre></details></small> |


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
