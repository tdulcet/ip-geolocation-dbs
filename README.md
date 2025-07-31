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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-31<br>IPv6: 2025-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.133MiB (6.431MB) – 307,093 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f74c23c9c2cd4a0752f7bb18e523e54c<br>SHA1: 0222f854ddb0e9235dad433eeba9ee702d21c2a0<br>SHA256: 575a2b02dbae75359e29e0daa989e464589f6e6ba8e3103af815bdf2b984c130</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.11MiB (10.60MB) – 153,671 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90aac6106269ad9d03eb665723414292<br>SHA1: 99aa6d9921bdc24b20bc5a42bd14c4ec0ee0b7e5<br>SHA256: 583330a2e3ab2b82b361510d970af78c5c3c0035ba91fc76a4fd43fe1abaf200</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-07-28<br>IPv6: 2025-07-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.553MiB (8.968MB) – 428,134 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b89aaa6860f40cde6ac2a4bdc97a45e<br>SHA1: dceebe5c47d6e84897ebc9fdf73fc53dbba308ee<br>SHA256: 77349eb3a20eba876c905d55245e65c82cb819c07d81bab823d67e9c3268b39b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.325MiB (7.680MB) – 111,424 rows – 226 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9a71834d9384d8cbc6a6e989859bcc0<br>SHA1: f293f7f62c2330f21db33787f023894ce82ba2d5<br>SHA256: 3b2a170af800dbda3611d6309b30ba03052da609109d1899330d743c86fd34a8</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.86MiB (12.43MB) – 593,626 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5416f84a230b4fb4f760fe97d53f63cc<br>SHA1: ceb2fd1e476f3c5bd9641f240acdfef5c0b3c598<br>SHA256: 33cc163b84d0931010c03af1fc9bf98e8932a60f49198ba90218d94c62628cfc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>91.66MiB (96.11MB) – 1,392,915 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea72a921c47397c5073a7117db3c8f6f<br>SHA1: bbe46f6b15a4c46cb15bf7575984f2f22601c6ba<br>SHA256: a7d65534d22d337b2e9cc823af22ae40ad1c46c6169a1be163cd51650b16cf79</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-31<br>IPv6: 2025-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.068MiB (5.314MB) – 253,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ddf95be39b948ff8a1f5f72a989f3db<br>SHA1: 53e521e70cdc7bf139a71019e836b80590d710b8<br>SHA256: 50c6f2769387e3ee7cedf43b469b7ba544e29e43852d8c3fccd14dbf39e376a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.78MiB (22.84MB) – 330,989 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43bd9e1f0cc46c204def11cc25411429<br>SHA1: bb110aabf0613079fa6821963cb9072ee8a672f5<br>SHA256: ef3129675278c4750cafd639f31a9a899cbc6468108504cf55d1a6439f90199f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-31<br>IPv6: 2025-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.2MiB (176.3MB) – 2,916,495 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec46eb0d6770f3a4934f80b9ba8b43ce<br>SHA1: f00f5138d48a37c35fcf9f170e21939324735351<br>SHA256: 16a49d4f2d09a24369e498fa18c855ad30e4610d4fb1424acea4ea9ccec6048c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>279.1MiB (292.7MB) – 2,704,923 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dac800448bd3a785c553531ef23da1b6<br>SHA1: aaef79ba06d4297b621a7688cc2224cb694528a0<br>SHA256: 6c59b673d7391b858e46d6527a0bce731c26713b44246050076e424d61a9f656</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-29<br>IPv6: 2025-07-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.62MiB (13.24MB) – 631,933 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40949a4f3110a16dea6a2bb856baab1f<br>SHA1: 93bc9330ff152b8bb8f7ddaf94121a30d14a5232<br>SHA256: 51c5475e9afb79f941e5187fefb0f453e00a54e2a3cee425c9edfe885fd7c830</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.22MiB (45.32MB) – 656,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ccc74685bbbb7b06e7f422017594467<br>SHA1: 2dcdebbca2baff9b239458c8fe738cfdc513a301<br>SHA256: 39f10fa91a15ab55b5da59473eb52d1ac404be7a933a00830ab5aef9f9e9cebf</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-29<br>IPv6: 2025-07-29 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.4MiB (182.9MB) – 3,439,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bffd85ae2584ce2fe1699fd5d70a373<br>SHA1: 9215d5d5d0fccee4857561abc7a9a856c5c07c72<br>SHA256: dd59f008d4a2495beba244cc378c0c870c01708f97188dd3da8f8d449c23f2e0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.3MiB (194.3MB) – 3,439,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce91a93d5e88433892a95135df844276<br>SHA1: 754c6b5d56df75552f15d3b573f57e6eabc29b43<br>SHA256: d12e31cb26b91c1343d1de4721313e4ec78edf97d842f16563a77e56e2e053c7</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>173.6MiB (182.0MB) – 3,439,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8a5c8ad4f094db2ebe1b72d2f8810ab<br>SHA1: cd5ceb899d8e7e625b616c616e66a48ac1ede70c<br>SHA256: 1ff976a7aef47b3a7c905c54d575f1d234b6e9d68ab2233339517962f6d1e033</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>176.2MiB (184.8MB) – 3,439,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64d811d091cf7af1603fc0f16bbf4797<br>SHA1: 8699c5d320927153cbb3153e28a51d947898b8b9<br>SHA256: 2874099105325c993ca70fff981794cb1dda5eaac3d3e6daa27574ca7c5e82b3</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.8MiB (231.6MB) – 3,439,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a97172fdb5dcb03bfdde2404a4ed3dd5<br>SHA1: c8ed495e70640c70e319ff1baec9b37c1076cf6f<br>SHA256: 9627ebf74966b6fbb2843f18ffb31af6a5a2a01df7cf0c3c37b55a2df5a508e5</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>173.2MiB (181.6MB) – 3,439,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d5e61fdc533e3a302175926c837c881<br>SHA1: 9591c586131374f74534cf556cd3cbaaa333587d<br>SHA256: 40943b62278b8bc9c366e7d8589adc500b7eed9f54fbdfc41444c440908f5561</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>214.6MiB (225.0MB) – 3,439,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53423bd03e76bb0a50dc2badeebb3b72<br>SHA1: 97df59178861e15297fdb1f3cec0c9be1550bd7d<br>SHA256: f2906d48f8b442902628fc9fdb319cf25cf63fa987bf290c6c0f43637ae3ef2c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>180.4MiB (189.1MB) – 3,439,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6916b815c9d606753ccc68c7a1157b1f<br>SHA1: ff9ea49f345f29debaff955dfb2cf45fb962927e<br>SHA256: e147ee4012cbdf33477df62727e00a826e53b5888ae976f6431ff10584026880</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>175.1MiB (183.7MB) – 1,861,518 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fd60ffdaeec86cb67d3448a83ef432<br>SHA1: 7d5f78c37674fe92141d9769e2829b180d299baa<br>SHA256: e4952376b91aab8216ca5e9a800a3226a68fe1c5623015c3ca03e05412841f64</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>178.9MiB (187.6MB) – 1,861,518 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d0da2b19afed9c5e98588e6c1443c33<br>SHA1: f10847840425d39c540845449fc1b0f81ad39447<br>SHA256: 776632b19b3da823104c2f3b32844fe78db71cbc5a2c6656b027f7b4f9df6a77</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>173.2MiB (181.6MB) – 1,861,518 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 756afe4b8ef7840fa765e5506e0a0fe3<br>SHA1: 58d742045eebe1a040c7ab56b30ba846b3f65d63<br>SHA256: 66091fa172cdc1670eec964bde9fda8c73f37d74a600de8a7861ff0eb9f04e03</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.4MiB (181.9MB) – 1,861,518 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8fa5bc907b5cec6d0686d5ab9db9bec<br>SHA1: 405fad5ab99444901e00f46dad82d59b3479d022<br>SHA256: e73869ba5038817add4e08a5c29ac930885f989f89490b857fe0424237a55116</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>191.8MiB (201.1MB) – 1,861,518 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f6eb20f2308b4d6ed31834bed682a3b<br>SHA1: 7e12307857f76ffbee4cfffd4f2acd246eb00041<br>SHA256: c98414ecbb35f9f49d2e699a84f190597d2d13cdd57bd8bb579a378d5dea1779</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>173.0MiB (181.4MB) – 1,861,518 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 640fa444e4e1e4d205ef1a1f766f723e<br>SHA1: d2cc8386e44b3e5f199da80310b18f4b8cafc11a<br>SHA256: 5ef69a79cbb979b87188af6214fe3a1ff57fed05742a0bcc38ef204441c010db</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>192.6MiB (202.0MB) – 1,861,518 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ac415569a5ef1ac89b330210f756def<br>SHA1: a977baa5a1317d8009afa1be38980a1a0596174f<br>SHA256: 44c74b756a7b0a7bebc94d0bc51e0d411377813699d2ee536c87d364b3ac7e9d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>177.1MiB (185.7MB) – 1,861,518 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dbb1cbdfe8d2933398d78fd8e408ce10<br>SHA1: b613e857a6fcc6817230acc8db1089c5fdc75559<br>SHA256: a45b447105917a584a63fd148561102d882ad1798028af5079bb65dc071d4d07</pre></details></small> |


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
