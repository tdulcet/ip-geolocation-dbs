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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-11-18<br>IPv6: 2026-11-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.777 MiB (6.057 MB) – 289,131 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41c6abd0fdc54220ce673325ca883989<br>SHA1: 764e93c6c73e82498d42fb501cef02ac188c4c34<br>SHA256: 9e1473e1cb2b350cbd55fd7b3f203e31d9f56508e23c49c11eb97e8018b9fc54</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.98 MiB (18.85 MB) – 273,224 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38f328bf8989824fe933281382046a33<br>SHA1: fec274d46bf71bde9fb602407bae58ed252a6410<br>SHA256: 9064a4ab123d53253ef7b75c60f396f805105ab8542414e0be5ca2541353d703</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-11-01<br>IPv6: 2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.186 MiB (9.632 MB) – 459,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84167ee008949c7e879c18eaa6df481d<br>SHA1: e998f760da828517741b8a57f76ceac532d2afea<br>SHA256: 03cc8544ec1d65aa3d43c09d4f8db8b5471fb5a48eb435c2e8626cb2c202790e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.883 MiB (8.266 MB) – 119,798 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93720f717969024f48fd382cad72f274<br>SHA1: 5173d179b24a928fce65b1c5c1194626035a37ab<br>SHA256: 645dfd169109e1cda747277411d71f68ca9d428d01b715756c1925f6ae7473f0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-11-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.10 MiB (13.74 MB) – 656,022 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b82d75bd6ea99bf76d78649ecd414061<br>SHA1: 179f26fbba4679594fc21b651b025fba90925a4e<br>SHA256: 402f8544ab6468dc6e6f9e8d3bb8dc4ba99640a227d7dbfeb26293210ceff2be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>98.19 MiB (103.0 MB) – 1,492,105 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26e06a0703bea0aaa70bc577d41882b3<br>SHA1: 6e12e1625839a1584f08d62d44b0ab85fd276004<br>SHA256: 658b2c199d4edf5a617e0ca9f73155bcee76a730d04afdf9bd8bb7215508aea1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.244 MiB (7.596 MB) – 362,984 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1896a3d70d9c776ebbbc51174d2dff7a<br>SHA1: 6b153e2b071d13e45ab9795a9d41e7fcbf0b910a<br>SHA256: fb52bd209b940b70d4fa6772242238a7238e3fdf267f7232a326a283a172da63</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>24.33 MiB (25.52 MB) – 369,794 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90147b4da0ef46e810078a3ca7e5aa0b<br>SHA1: 9df64ba895edf447da29fd2c604e9ff223a49471<br>SHA256: d30738d906d231b000d8994f7a07aee2550e5ba72a4d6ed8b60712ef87862557</pre></details></small> |
| | | Full Location | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>205.3 MiB (215.2 MB) – 3,598,802 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a48535424fbcaaabbc7dfc056e39f5a3<br>SHA1: 4394336d775415fe1a653bacbda7921ede4fd2c4<br>SHA256: a320a6ae6f82cb61d2d9b36a2baf9ed6a69c127627aabc98a1c598893700a202</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>430.4 MiB (451.3 MB) – 4,178,996 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b774537c14ceaf921dbde58aa6fb3f09<br>SHA1: 7695b1a6e7b8783b8331d8935d87fb6691eb8b0f<br>SHA256: cee773355d5c7bcb515c4efd0abc0daeb0b545de5e714601f54daa4c6c03e77c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-11-14<br>IPv6: 2026-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.657 MiB (5.932 MB) – 283,201 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f559d3d04d0b023ee00044c37313155f<br>SHA1: f2851744febf1ec81c0fb7678ea93c854509da1f<br>SHA256: 9f2d57ba5bd15600148ec8af11bb5d1c73c5df8d92d43a7b8a2f04b570234a71</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>25.36 MiB (26.59 MB) – 385,339 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdf132961e4276d4847e99f3e8a11394<br>SHA1: d6d8d534b0c26e7d9435a5baf39b738f96ae35b9<br>SHA256: 5d4536a256517e52942cc5cbdae8d65712adad9f30f5d40bc77a31a922337bbd</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-11-14<br>IPv6: 2026-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.3 MiB (176.5 MB) – 2,912,900 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 172467e52d3011a3e293a609cebc0b99<br>SHA1: 0d251ec08fa282eabfa086b49c7435c45f6ba71f<br>SHA256: c92d9b5f9f80250491431f7cc1993e1e07425841790dab124810a2868f53ee98</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>318.0 MiB (333.5 MB) – 3,079,222 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71bfec8cda51cd5a447bb2f7d9a32287<br>SHA1: 1e76c265df3cb7a6db6a8e501ddd8bd0fbbc498b<br>SHA256: 71ad483d60ebeb8e24249a5f0ca2595d67654b77b66044c6d204581783aa8d62</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-11-17<br>IPv6: 2026-11-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.35 MiB (11.90 MB) – 568,077 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73bcec145caff72bdb3dd678ccc7fe05<br>SHA1: ebd86f65e1b72d2a4ac8e319cbfe42aa6844b49c<br>SHA256: 16e6e464ee43252dbd8d86ac6b9b11301cb8de7e93ac20773b4fc060a2104059</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.61 MiB (34.19 MB) – 495,575 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15f0890ac83e6b2a402a8804b8ab792b<br>SHA1: 20d7dbccdd0e8206a8752c6fd67847beae972b7e<br>SHA256: ab2f7eabdbb51993cbd1c7e60cff99c081c43994c41874ad2acf5d4a0df9f27b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-11-17<br>IPv6: 2026-11-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>187.6 MiB (196.7 MB) – 3,656,190 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27a6d6cccbb0dbbdb984c34e635f1277<br>SHA1: 85ed87e47acd9187af84c18a0ff643865c87ccee<br>SHA256: 79a3a8001c85083bdca9a1a9170096741ee50d27da4627c2bc20c00aae3e9332</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>196.2 MiB (205.7 MB) – 3,656,190 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d5802178c9db78da4db65eee582e639<br>SHA1: dcdcf60dbbe785762bab2e5c93701bf1b6b8655f<br>SHA256: 1df071b42f9a0615fcd83723b488668723dae5cba441827b7ef9104e4e715a5f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>186.7 MiB (195.7 MB) – 3,656,190 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 958b5234524456dcbbb9152b120fa3a3<br>SHA1: e621f3db55737179d126ac8c0e597a71f598f556<br>SHA256: 957adb1079140be878113d9ce0b6ba0f2101566660c37777515b012146012cd0</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>188.2 MiB (197.3 MB) – 3,656,190 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3be374ecb40f21caba4484f1eb20cfaa<br>SHA1: bbda4f8a80f804308ff375de70fcec848d4c7e32<br>SHA256: 9273c82470ef9512a1fc9a42f8f5d9fdc0add3099c1c8cd1b94921621d70e7dd</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>237.0 MiB (248.5 MB) – 3,656,190 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52a1ec51bf8d0b042fe68513a7e70c98<br>SHA1: 09ada08aa6c91a85752c8496cf74686411abe152<br>SHA256: f1f0f224d540406d1f1da74327425a6c655cb42367a96118c2a58f5afe85a9a3</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.0 MiB (195.1 MB) – 3,656,190 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 518968fb6951b7fbdcbf01379ab834c9<br>SHA1: 456574e10311c07a1cad715784d21c2835afffd8<br>SHA256: 3a0adb67b09a40df8933fd8f3c3d514fdceea0f7abaa9e4f3bfd3a358373c05b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.6 MiB (247.1 MB) – 3,656,190 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 384553fc9661fdc64cca0411c48e9c22<br>SHA1: e6ccbe2fa5f6d0876b304caadc7582289a11a212<br>SHA256: 1c90dd03ccd3817ef190e8a465defd705185337c5d45e2fe0f03c99e5487d6e6</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>200.8 MiB (210.5 MB) – 3,656,190 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1893023cc24046918172e52bde611e5<br>SHA1: e5fdc458dabab68364ae58832c9eba7f17dce350<br>SHA256: 60d559e908321918aa64fd6ae91a8ba0bdc930c139f2e893f373fa4a9de984fd</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>201.7 MiB (211.5 MB) – 2,116,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32fabc5c22d34721c3b8880c633b715b<br>SHA1: bd0cc6df2645672aa142431bf3f1f90ee6f5c316<br>SHA256: 62ba6138f05c6ddec8525665c6ca2a4fff04ef4fbae0bc701321eb9ca0af53dd</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>205.0 MiB (215.0 MB) – 2,116,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31ad355c112142619c7ce53f98965e00<br>SHA1: a742c89ee97c355c4da63e1553010d235ea9ab6d<br>SHA256: 50e82f4616ded8155114fd4a8ab8b6f99d39e06abfdcffacc9691de78ed42fa4</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>199.1 MiB (208.8 MB) – 2,116,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b5b8d3ad8e757305ceabc70e12eeca0<br>SHA1: 00d785735b8756a62f772d391b6729c98f5abfab<br>SHA256: f03727aca7a5ae84e3c3e6ac4b36675caa6c973a05f33242b124b2138ed3030b</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>199.5 MiB (209.2 MB) – 2,116,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ca14be76b1871916d3cec679baa7367<br>SHA1: c08f54bad22005f6c26b6ffab034a63e15b15476<br>SHA256: 0921bd8b6a1e40b507f0f8fc4133b3289cae3b37b989fd778151244dbc1c8282</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>221.7 MiB (232.5 MB) – 2,116,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d2a3aebbeff8361ed562c17d0a290a<br>SHA1: 184862e2e5b514cc9335570ebdba1df2eef1cb53<br>SHA256: 0e52b9f7de327607b8e428cff9a1cd83f7b7b9bbffb891a76e89b9ab912d8535</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>199.1 MiB (208.7 MB) – 2,116,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f4563733ef10aa16929fcaeebcba3a8<br>SHA1: ca681bc5c9d63fef448ceaafa2b7c908b3549c92<br>SHA256: 488ab795563958f9c3523de79c7445c2856a4f5e11780fb52dfbcc0da98f8073</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>224.5 MiB (235.4 MB) – 2,116,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e148f4610635e6c4de0d56c4bceb59d8<br>SHA1: da3f03faa73b799d96bc4a91c2d129e57e4b04c8<br>SHA256: ac3f2dfcde8c0e013b8ebda4c626b50cc81549bd86eeb02941815e56391c40a4</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>206.5 MiB (216.5 MB) – 2,116,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 075d582032992ff20402b1372e2fe454<br>SHA1: 164f8ec13a0728b27ea596077304c72b3a7faba6<br>SHA256: dd598518de33bd1ba751d35a5db834f8193596a4978ba245cd1031947115932d</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
