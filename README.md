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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-11-23<br>IPv6: 2026-11-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.814 MiB (6.096 MB) – 290,974 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b30c7295e5258e13e548c4f802e46f40<br>SHA1: e5660406f3d129acaee74cc86560bbbfd1afc644<br>SHA256: c0e900bb8b001ada648d63b5d52708ab6b360b5ac362d1d7e9631dd49a70b927</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>18.12 MiB (19.00 MB) – 275,313 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e01cd45211b3c34feca7a110f2107db0<br>SHA1: d1c97e3274bd3ce8b3519b79fdeb80607bb8eeb3<br>SHA256: 5434a6ff29638ca8b79834461017b1372af64489de8208ec474b8abf7e7094d4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-11-01<br>IPv6: 2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.186 MiB (9.632 MB) – 459,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84167ee008949c7e879c18eaa6df481d<br>SHA1: e998f760da828517741b8a57f76ceac532d2afea<br>SHA256: 03cc8544ec1d65aa3d43c09d4f8db8b5471fb5a48eb435c2e8626cb2c202790e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.883 MiB (8.266 MB) – 119,798 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93720f717969024f48fd382cad72f274<br>SHA1: 5173d179b24a928fce65b1c5c1194626035a37ab<br>SHA256: 645dfd169109e1cda747277411d71f68ca9d428d01b715756c1925f6ae7473f0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-11-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.34 MiB (13.99 MB) – 667,884 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d55a4392cc3b4004ca1a49425a238e<br>SHA1: fc87f5e59e624db405a08782fc7b213533bce593<br>SHA256: d3be9515d7dac33982449dc98dd1b92b9f229920aee1a3dfffa92102b17ff0a4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>51.03 MiB (53.51 MB) – 775,510 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19de11cd08ea20083c880fe65e4ac873<br>SHA1: 8d1d425dabfa9ec9cd2b02108dbc95a04b0674c6<br>SHA256: dcc949bb0dbf86c0b9184880b104766ad76096a7478a0b44082b83d107aa3e45</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.244 MiB (7.596 MB) – 362,984 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1896a3d70d9c776ebbbc51174d2dff7a<br>SHA1: 6b153e2b071d13e45ab9795a9d41e7fcbf0b910a<br>SHA256: fb52bd209b940b70d4fa6772242238a7238e3fdf267f7232a326a283a172da63</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>24.33 MiB (25.52 MB) – 369,794 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90147b4da0ef46e810078a3ca7e5aa0b<br>SHA1: 9df64ba895edf447da29fd2c604e9ff223a49471<br>SHA256: d30738d906d231b000d8994f7a07aee2550e5ba72a4d6ed8b60712ef87862557</pre></details></small> |
| | | Full Location | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>205.3 MiB (215.2 MB) – 3,598,802 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a48535424fbcaaabbc7dfc056e39f5a3<br>SHA1: 4394336d775415fe1a653bacbda7921ede4fd2c4<br>SHA256: a320a6ae6f82cb61d2d9b36a2baf9ed6a69c127627aabc98a1c598893700a202</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>430.4 MiB (451.3 MB) – 4,178,996 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b774537c14ceaf921dbde58aa6fb3f09<br>SHA1: 7695b1a6e7b8783b8331d8935d87fb6691eb8b0f<br>SHA256: cee773355d5c7bcb515c4efd0abc0daeb0b545de5e714601f54daa4c6c03e77c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-11-14<br>IPv6: 2026-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.657 MiB (5.932 MB) – 283,201 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f559d3d04d0b023ee00044c37313155f<br>SHA1: f2851744febf1ec81c0fb7678ea93c854509da1f<br>SHA256: 9f2d57ba5bd15600148ec8af11bb5d1c73c5df8d92d43a7b8a2f04b570234a71</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>25.36 MiB (26.59 MB) – 385,339 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdf132961e4276d4847e99f3e8a11394<br>SHA1: d6d8d534b0c26e7d9435a5baf39b738f96ae35b9<br>SHA256: 5d4536a256517e52942cc5cbdae8d65712adad9f30f5d40bc77a31a922337bbd</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-11-14<br>IPv6: 2026-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.3 MiB (176.5 MB) – 2,912,900 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 172467e52d3011a3e293a609cebc0b99<br>SHA1: 0d251ec08fa282eabfa086b49c7435c45f6ba71f<br>SHA256: c92d9b5f9f80250491431f7cc1993e1e07425841790dab124810a2868f53ee98</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>318.0 MiB (333.5 MB) – 3,079,222 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71bfec8cda51cd5a447bb2f7d9a32287<br>SHA1: 1e76c265df3cb7a6db6a8e501ddd8bd0fbbc498b<br>SHA256: 71ad483d60ebeb8e24249a5f0ca2595d67654b77b66044c6d204581783aa8d62</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-11-20<br>IPv6: 2026-11-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.41 MiB (11.97 MB) – 571,548 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a59c3d6bcaa3aac09715d8aafd1b85f<br>SHA1: df194148e1564705f3b63432486c2f0b4c562d62<br>SHA256: 1567c2b4f3567c28a550037171c88e2d372dd08ea9224d6a73ce59f32f5679f8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.66 MiB (34.25 MB) – 496,335 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d53211c6e21e443e270ef9a8c1209e7<br>SHA1: d18e6c3209c784e4d2dd35c60c3c0991c40d93f3<br>SHA256: 8b87f174b8ac797fb1d7bb5fd2af7381277fa568d9be431c8a01d0548691cdb1</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-11-20<br>IPv6: 2026-11-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>187.8 MiB (196.9 MB) – 3,659,289 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42bb65c11e1b87c0c9f1a755d1b86fdd<br>SHA1: 137332945f95574e4e603be137df661b7ba150c6<br>SHA256: cdbfc3852420311ae267170d59539c11949e8f8ba02cc763ccc7b8b69a259cc3</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>196.3 MiB (205.9 MB) – 3,659,289 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e88f059e53fea69ea7d752f36f186d3<br>SHA1: be3618827360613c1e82ff4bbd01b71ab524434d<br>SHA256: 97073e09d1834feb3f32f0318a8e192eabf91c7e5b6475eba079d98bf7b297dd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>186.8 MiB (195.9 MB) – 3,659,289 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64f0983c3269f7f9bc259e8660805bfa<br>SHA1: a4dc077a684af9bb05d3c71852ef9ab727f35fc7<br>SHA256: 60ff58f16434eae20dd85ceb308561a27091710e4d4181832c08b86a01189787</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>188.4 MiB (197.5 MB) – 3,659,289 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9dea913abb4be52dc1f7f6380bd0754<br>SHA1: ebfbf113a3a88cabe2eacf1b5a80427a2cc60585<br>SHA256: 03d7c6bc1492a6b77571c24fb59fd76fa9da6731042e413f18c6cf884f98ffe8</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>237.2 MiB (248.7 MB) – 3,659,289 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc459f4a684542494c4403c1251e2c0<br>SHA1: 1e15d6c82a8214ec6a29f7a72321d8ba6a34f740<br>SHA256: 46f778a85c748325ccba7afc1aecbc2dae5e1c77b0dd5f8f9437eacd58b2519b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.2 MiB (195.2 MB) – 3,659,289 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65e35aa10b61fd7baf669bbd5677652d<br>SHA1: 5bb1b40951516353d4a410b7edb7c2f5d6db94eb<br>SHA256: 6d1da19ecfb42a0723a90786e839d0dff35df2a8f8baacd12f0c6bac7865956b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.8 MiB (247.3 MB) – 3,659,289 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52ea64fd3e04894040e573d7c18d9556<br>SHA1: 5dff554bfcb880e491525ba102fe92280f066fd8<br>SHA256: 75a4ba367653a44492ed19a6249f2df89a7dfa18f4a92c8893650da918b88b3c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>200.9 MiB (210.7 MB) – 3,659,289 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a143d00176be04fbf977db93dd490072<br>SHA1: da8938af8683a4c1691aa2ca09def848c7e91959<br>SHA256: f0f2bea3f02d98f10e390c7209da3e2c454ee09c06d8eb6b822f5a90fc2be132</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>201.9 MiB (211.7 MB) – 2,119,614 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e37c5fd14f8db207c3e9c8f54ef5ee98<br>SHA1: 3a0b1d5f8e459dcbb0a5c90069e57fa21df169e4<br>SHA256: 7d6ed889d61f23ad96e8e7414d3454cd7a274a596572c841fbcd6398f904897f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>205.2 MiB (215.2 MB) – 2,119,614 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3549cdb12f6831e288f6b6207b342b4e<br>SHA1: 42a6055221c8d5d9d0c3d733d60e20d2f5fdcd21<br>SHA256: 8f7fd120c8791434ad937c36fb50e6edc7c830c76b76484fd68c6baa25b75f6d</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>199.3 MiB (209.0 MB) – 2,119,614 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3319c839cd5263de14d2453c9a25049b<br>SHA1: 6a89fc961247e66e98d57e2c4a3183f53e980557<br>SHA256: 53987cf2d9b15d3da73b16ac8a84b2e8447af19a7adf2c48c1b36fb4726e1504</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>199.8 MiB (209.5 MB) – 2,119,614 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dcf8a9718dc87297cb0359f8cf2622df<br>SHA1: 38386feed742f6f4ca33fc67c2ac4bbb032ecdfb<br>SHA256: 7e310037e6682ef847750f7fc1889851be35f7c5d669a36ab416e79110852cc8</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>222.0 MiB (232.8 MB) – 2,119,614 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f369b5038e639199fefe7f08c84ab32f<br>SHA1: f87234e9e992b19c4b24a7a7d586b2f0674616f1<br>SHA256: 62d5fea7640527801a47f2793c8f7ad1b52e0dfc03d5708563283b3b1783fecf</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>199.3 MiB (209.0 MB) – 2,119,614 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 435297ddea2db4d95430a1420eefb310<br>SHA1: d8e96a92f3bb0cf2c081fc68a8758edaa89504b6<br>SHA256: cbeabd2cf5fba75ce85616aadd1885f145854130dcd90644e9c12e825e2d71ff</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>224.8 MiB (235.7 MB) – 2,119,614 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47d9da3630e31a5d43010c1bed0e809e<br>SHA1: e1cafbafe154bc15dbb1975a72f7a07290c1313b<br>SHA256: b3862e88c074ef7f2a3c7af3ea9418c750e89021965ed08f4ae699720daf77d7</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>206.7 MiB (216.8 MB) – 2,119,614 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccd8bfbcc53f1fc4e4b3d2d9dadf7111<br>SHA1: a39a93cc7fc1d6f97f69af944fa83fdb4410a75c<br>SHA256: d851adc081013a013bfc564894778b674e70dde9165ded5a23a7d7fcf386b425</pre></details></small> |


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
