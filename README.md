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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-11-06<br>IPv6: 2026-11-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.733 MiB (6.011 MB) – 286,915 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7419b0714903d3142f652f9a9ecc5c12<br>SHA1: 25894a8df30075149150b5c471ee69178fd58087<br>SHA256: 0f174d8cb68fd2ef314bcd493e99ae30619a84f30545f87bb026fb3d3cf27c73</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.59 MiB (18.44 MB) – 267,285 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fb54a576a803a63b399ef37bc0ade8e<br>SHA1: de1f0feab357007a87fdc284f9630645c8137ec4<br>SHA256: 4ab942070204f4f828fd392a2989b9c30559292fe2a42d8b99b9ef51cb7b39c5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-11-01<br>IPv6: 2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.186 MiB (9.632 MB) – 459,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84167ee008949c7e879c18eaa6df481d<br>SHA1: e998f760da828517741b8a57f76ceac532d2afea<br>SHA256: 03cc8544ec1d65aa3d43c09d4f8db8b5471fb5a48eb435c2e8626cb2c202790e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.883 MiB (8.266 MB) – 119,798 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93720f717969024f48fd382cad72f274<br>SHA1: 5173d179b24a928fce65b1c5c1194626035a37ab<br>SHA256: 645dfd169109e1cda747277411d71f68ca9d428d01b715756c1925f6ae7473f0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-11-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.05 MiB (13.69 MB) – 653,678 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a568e2df7784ca37d7dad7801ed40e3<br>SHA1: b1a49d709e45f14c522b335c899d05c6d6eba44e<br>SHA256: a9c5c37ad38a8814c23abf7884f6dfee1d7b13202125bc5a8d18ae632e061d3a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.58 MiB (93.94 MB) – 1,361,400 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75d8fe23f0ff5210cf903c5184825620<br>SHA1: 89b29eed73999ea6632c987a86778cc01a95508a<br>SHA256: 868f726c122dd3d8615b0bc30308fa9587d26fde464bf834723283bab005c206</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.244 MiB (7.596 MB) – 362,984 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1896a3d70d9c776ebbbc51174d2dff7a<br>SHA1: 6b153e2b071d13e45ab9795a9d41e7fcbf0b910a<br>SHA256: fb52bd209b940b70d4fa6772242238a7238e3fdf267f7232a326a283a172da63</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>24.33 MiB (25.52 MB) – 369,794 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90147b4da0ef46e810078a3ca7e5aa0b<br>SHA1: 9df64ba895edf447da29fd2c604e9ff223a49471<br>SHA256: d30738d906d231b000d8994f7a07aee2550e5ba72a4d6ed8b60712ef87862557</pre></details></small> |
| | | Full Location | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>205.3 MiB (215.2 MB) – 3,598,802 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a48535424fbcaaabbc7dfc056e39f5a3<br>SHA1: 4394336d775415fe1a653bacbda7921ede4fd2c4<br>SHA256: a320a6ae6f82cb61d2d9b36a2baf9ed6a69c127627aabc98a1c598893700a202</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>430.4 MiB (451.3 MB) – 4,178,996 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b774537c14ceaf921dbde58aa6fb3f09<br>SHA1: 7695b1a6e7b8783b8331d8935d87fb6691eb8b0f<br>SHA256: cee773355d5c7bcb515c4efd0abc0daeb0b545de5e714601f54daa4c6c03e77c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.813 MiB (6.095 MB) – 290,990 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c7072a914951e8601c9ceeada7a3d6d<br>SHA1: cf54f7394145aaf4cad9d5806cf033c5d2e05129<br>SHA256: ae75289541009f5e4e55f485a547f5969d05bf27e77319236873e0cbe6042b95</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.34 MiB (24.47 MB) – 354,673 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e0dc2b8d91b7ba4229624281d2e16c2<br>SHA1: 0b3d99b5bb726900a6a60d2a140865a09f6c202e<br>SHA256: 8c00dd52b8cad30ef157bea8292f275ce2427479b23834b052923df53c5ab3e0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.4 MiB (177.7 MB) – 2,928,935 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c7dfce82c76c40935365010e208451b<br>SHA1: ceefe3f4d1597102c1e20a15432939082505547c<br>SHA256: 25dd83a6bf875037466f23e735227da25d97c795213017cef409de7778c8671f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,928 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75980237a60e580bcf5a6bb2276cefaf<br>SHA1: 87785f70ceb15fdf9f19a474ecb10f6d04550358<br>SHA256: 63657dda83bd39e0d502cc12ad78bb16eb3be91705bad6374d45345f41c7c24d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-11-06<br>IPv6: 2026-11-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.28 MiB (11.83 MB) – 564,711 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5808ad8c3a079078de1c23a713e832d9<br>SHA1: 40b5a9bf2a5808d407346ee5139afb08160ef53b<br>SHA256: 22dc951fe66a53a07694dd100244d34243e3a8b3ce80c0ebb5e4cfb5dceda3ad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.57 MiB (34.15 MB) – 494,974 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8ff18e6945f903c2a76e435b63f024b<br>SHA1: 502a9402289a977b3788f53521adcdedb6421ce1<br>SHA256: f665d121f0727a1049aa90989e607a4915ae4309e1aeb859c626f0e491e587b6</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-11-06<br>IPv6: 2026-11-06 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>186.3 MiB (195.3 MB) – 3,636,256 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c80a1e3da7e42b3210e6614325ffb9d<br>SHA1: d5f53666bf1868cf93aa86e20df8166cf315dbce<br>SHA256: 28f20cda015958697c9b3da8fce52df975c9acbc847ccdb7428facee38ca8288</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>194.7 MiB (204.2 MB) – 3,636,256 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c38e7fb97695cb3fa7631b81c945a69<br>SHA1: 351ba51d69f96b5e7321cd8cf270a0e0f074b950<br>SHA256: abadfd5908e4c0d35ec3bd25b2a48ef678e235ae5562637246d2dd4f8d3ab829</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>185.3 MiB (194.3 MB) – 3,636,256 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2241ca978426b51ac69b47fe4c94fb3e<br>SHA1: b124837c2ac24f32c5da50ce1a38b3079a9249e0<br>SHA256: 3bd9595f14b636447eb52a54582a3717ae9dd6ad1c2ebb74e9d75267074807af</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>186.8 MiB (195.9 MB) – 3,636,256 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f30a1562a76d8b95c9fd2d161527ebe6<br>SHA1: acdea6eb296d15d2b4f96351d3600951ca5bfec9<br>SHA256: 4403bd16a6dc67d6ce538be879cddf2b75dce3e2c8c79383ae037cd5d6112e46</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>235.4 MiB (246.8 MB) – 3,636,256 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b6fbfda569adb074a1dd7b6433857a1<br>SHA1: 6c4041b1b9ddf940d86caf3d38b357d80c40a78f<br>SHA256: 3d1e0ebe2c2561cf245ebfd670ee518a46d731bfef3a8ca5769c87b43991df14</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>184.8 MiB (193.8 MB) – 3,636,256 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e2b6382bc0a01179c96e1a697437989<br>SHA1: 91f9a69305368d1821b40689f028577fcb7c6cb1<br>SHA256: 85a65c9682b00215ae63e94cfc40bdad59f5f678a960203dd5299cd39149c69e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.0 MiB (245.4 MB) – 3,636,256 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcd73cf9cbe6f96810c45b03951ba6da<br>SHA1: d670c826cf3d66ec0572969c62101fa471485e2e<br>SHA256: 71998b7fe8a8efb1ece89a8078fcfeeb4c33d48f295f3b11b233bdf3be35affe</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>199.5 MiB (209.2 MB) – 3,636,256 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 163143c3ae76ed9a593bc807c6f2fd56<br>SHA1: 4cb71d5e494d533e216f51a4c391a083bd0f3132<br>SHA256: 9e597021c9e71a881bf79949c26ed825696b1fd757c32e99018da7bcb3aa19ff</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.4 MiB (209.1 MB) – 2,092,880 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e21096a7caad8a6b92c1a6eed0517e7e<br>SHA1: 8c8543f46f2e94dc0cffe76265360a0bba213e52<br>SHA256: 178b874028b1902ad7bba044deaadd411bc31e36eb499cf34d72e4346ca0770d</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.7 MiB (212.5 MB) – 2,092,880 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f07600fc6233e85b4f8760972e05a24<br>SHA1: 3b8ee6a5659e61fdea3d7ed5d0f9273b8b7019bf<br>SHA256: 266994b8dc20a3945b2f70209ad18c2fc3e125629bf4b59e20213a82ce732ab6</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.9 MiB (206.4 MB) – 2,092,880 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1efaf97f23520c6145e22680226732ac<br>SHA1: 39fcf7c1f22ee3db80009c7e7a2e1a97d6ee410a<br>SHA256: 91bf0b98e8d7106b802448bafd9cd241b6c8043ec5633193e96ffa99aff0b2a1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.3 MiB (206.9 MB) – 2,092,880 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7fd398940f99daed36346731610cf47<br>SHA1: bddecab22d852839ae2a0b1cb1a6eee01c710c32<br>SHA256: 22aba623f1b3b6304c0c78f940d58fed008cb8a42eb2362f46a3cd2b6e2755ae</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.1 MiB (229.8 MB) – 2,092,880 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10fa6f3f6c0b3fb3ebdcb96470548056<br>SHA1: 324002c7fc68afe1b6a231bc76233244b6fc80d1<br>SHA256: 9a42ac5444ad33a0430deed5e8c80962e5e16eb57616213c0d5009218f3c6f3e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.8 MiB (206.4 MB) – 2,092,880 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de1e5ead622a08a2951c6168ab211036<br>SHA1: 270f8d50e497e7af2ccd2e93dee44120a03b367e<br>SHA256: c44548e519cfb7024f03a09b568974de343a3e910cc61c8afe7a30ea867ea7bb</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>222.1 MiB (232.9 MB) – 2,092,880 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82be259f0300fd8d3199102b070ff10b<br>SHA1: c286281ba806e8b1ec62641c110f3f20794c6083<br>SHA256: 00e605a2f48f1c857784aab4357950dfc2167e71e75c01b297c646651a18dd73</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>204.2 MiB (214.1 MB) – 2,092,880 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56ee425a08646089b791f3eef91c24de<br>SHA1: 41374adc30acea18e6bc26a80fc87311dce908eb<br>SHA256: 6f62f816236fbcdb39e5d591f2d938cc5678a65183843aa4a9adf4ab3e1ffad4</pre></details></small> |


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
