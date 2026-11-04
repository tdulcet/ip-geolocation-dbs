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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-11-04<br>IPv6: 2026-11-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.711 MiB (5.989 MB) – 285,851 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccae8eb387f267d3e64ffc58ec02e3d4<br>SHA1: 586b00289dbfe07041671b82c87b54bbfa959f5f<br>SHA256: f4b442eb4706c0a2c18365ce55bf186fec115244114d395cee5edbb79a9f318e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.56 MiB (18.41 MB) – 266,877 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f560fad09f6997c1d63dc0dedf86077b<br>SHA1: 9ca00f016896527773552bfaab4b260b39fe652e<br>SHA256: feac17f4b2f243de964e2721fd68b48f858b42fa011cd99a674e2a0b09e218f4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-11-01<br>IPv6: 2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.186 MiB (9.632 MB) – 459,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84167ee008949c7e879c18eaa6df481d<br>SHA1: e998f760da828517741b8a57f76ceac532d2afea<br>SHA256: 03cc8544ec1d65aa3d43c09d4f8db8b5471fb5a48eb435c2e8626cb2c202790e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.883 MiB (8.266 MB) – 119,798 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93720f717969024f48fd382cad72f274<br>SHA1: 5173d179b24a928fce65b1c5c1194626035a37ab<br>SHA256: 645dfd169109e1cda747277411d71f68ca9d428d01b715756c1925f6ae7473f0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-11-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.04 MiB (13.68 MB) – 653,300 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce23e2f71cf07a3b92a81971cd13bee6<br>SHA1: 5b55ac95c7491a16c1445798853fb4d192de63c9<br>SHA256: 3b5be4a6b6590259487b2053813312606d96456a001beb926aef6c5045d80b3f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.46 MiB (93.80 MB) – 1,359,476 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 876627deb57d99347b2de4a71fa4d318<br>SHA1: 82d6265424ac3c70fb9e8ae678b8affe900458a2<br>SHA256: 3dc13ef523789f9f177a036ad2dd208ec7f079af3f11ae23841303ae6b249265</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.244 MiB (7.596 MB) – 362,984 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1896a3d70d9c776ebbbc51174d2dff7a<br>SHA1: 6b153e2b071d13e45ab9795a9d41e7fcbf0b910a<br>SHA256: fb52bd209b940b70d4fa6772242238a7238e3fdf267f7232a326a283a172da63</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>24.33 MiB (25.52 MB) – 369,794 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90147b4da0ef46e810078a3ca7e5aa0b<br>SHA1: 9df64ba895edf447da29fd2c604e9ff223a49471<br>SHA256: d30738d906d231b000d8994f7a07aee2550e5ba72a4d6ed8b60712ef87862557</pre></details></small> |
| | | Full Location | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>205.3 MiB (215.2 MB) – 3,598,802 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a48535424fbcaaabbc7dfc056e39f5a3<br>SHA1: 4394336d775415fe1a653bacbda7921ede4fd2c4<br>SHA256: a320a6ae6f82cb61d2d9b36a2baf9ed6a69c127627aabc98a1c598893700a202</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>430.4 MiB (451.3 MB) – 4,178,996 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b774537c14ceaf921dbde58aa6fb3f09<br>SHA1: 7695b1a6e7b8783b8331d8935d87fb6691eb8b0f<br>SHA256: cee773355d5c7bcb515c4efd0abc0daeb0b545de5e714601f54daa4c6c03e77c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.813 MiB (6.095 MB) – 290,990 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c7072a914951e8601c9ceeada7a3d6d<br>SHA1: cf54f7394145aaf4cad9d5806cf033c5d2e05129<br>SHA256: ae75289541009f5e4e55f485a547f5969d05bf27e77319236873e0cbe6042b95</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.34 MiB (24.47 MB) – 354,673 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e0dc2b8d91b7ba4229624281d2e16c2<br>SHA1: 0b3d99b5bb726900a6a60d2a140865a09f6c202e<br>SHA256: 8c00dd52b8cad30ef157bea8292f275ce2427479b23834b052923df53c5ab3e0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.4 MiB (177.7 MB) – 2,928,935 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c7dfce82c76c40935365010e208451b<br>SHA1: ceefe3f4d1597102c1e20a15432939082505547c<br>SHA256: 25dd83a6bf875037466f23e735227da25d97c795213017cef409de7778c8671f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,928 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75980237a60e580bcf5a6bb2276cefaf<br>SHA1: 87785f70ceb15fdf9f19a474ecb10f6d04550358<br>SHA256: 63657dda83bd39e0d502cc12ad78bb16eb3be91705bad6374d45345f41c7c24d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-11-03<br>IPv6: 2026-11-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.26 MiB (11.81 MB) – 563,803 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0208ae860e0216e4f1e3df37b6d084f1<br>SHA1: 8711a0cdf76bb612d2cfefa60227762738d31dbe<br>SHA256: 38cb0bebb7ad90d5fa180c9ec3cdcd0d712406e98c9f84d5c80ce1b2e5ab2e84</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.58 MiB (34.16 MB) – 495,128 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb48f387512ebbe7a8c927c57398e7a1<br>SHA1: 8cd2854983e71c1384f4d652d0c46c3c3ff3a12b<br>SHA256: dadfc21d8ab9cbf6e341215fc72ba0bf79f8b8ffe9d3125fa1511371f0980c21</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-11-03<br>IPv6: 2026-11-03 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>186.1 MiB (195.1 MB) – 3,631,988 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be7146761edc5036cc8726d08981f34f<br>SHA1: a557cccee0b9f9f7b76cf874428d8b675f3b3ae7<br>SHA256: bf6e2ec0f18f29bd3e43503a73f6ecb2d60f2de76247dde17a31fad487574d84</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>194.5 MiB (204.0 MB) – 3,631,988 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba47363439332b1e71bd2579cecd50dc<br>SHA1: fc68bda45dbdae0245dfec12454e613854713a59<br>SHA256: 66f8d67ad921a5ff874e9091e8afa92bb0eba80fdbc30c9326a08e7290346809</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>185.1 MiB (194.1 MB) – 3,631,988 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a33cff290dfd6ffe27e5b3e27225e9c9<br>SHA1: cc7584eedcd690bdc6cefbe3bd9a34a8b4f42a79<br>SHA256: e5daa4bc0979859961ed0aa4657dd78341d678d3e5dd32aacf81f2327079847c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>186.6 MiB (195.7 MB) – 3,631,988 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1634e5bec1dd1b832de8e1273ab3d752<br>SHA1: 53ded65fb92904ef62ccda684dfe298513c95213<br>SHA256: bb4e0fca55ebc13fa5a1e3c3f1bb16fba0204c8bced483214b9b92938ffd0bc0</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>235.2 MiB (246.6 MB) – 3,631,988 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 394348a954012cabb7ab1edd9b583e0a<br>SHA1: 69b722a90caa41768116bd9f3922a3db9de12fed<br>SHA256: 1b0b26c1015de614cf0e34816651ba839388a1945d4cdfa2995a62172da12970</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>184.6 MiB (193.6 MB) – 3,631,988 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f108f4e3e72a83d6a5c05068c9afcf66<br>SHA1: 21f0439b00af1645023a070e443ac15300d7bbdf<br>SHA256: e4d5abb5b702c5b1c71bf31d07ca11124d4d79b2d3ffbf44c9ef5e3b948d26c3</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>232.7 MiB (244.0 MB) – 3,631,988 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56e7cd6022e503e15586f18b9e105fd4<br>SHA1: ee022b412ec0e602802bfc6e3e2a9041d97ebfc8<br>SHA256: 6d7f1b0e7428b54a00b1a284c14db62cc7bd009f2c7bcb5e339bbdf2034e8ff8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>190.4 MiB (199.6 MB) – 3,631,988 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af884adcd39f25119f04dde158ee8620<br>SHA1: fea0b9894ff7b4819cf54c3d573a27427ae34413<br>SHA256: acc1ff807f89449bcb0e8a307b57525c8b7811629cb52ec2a99d084b0584a8d8</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.3 MiB (209.0 MB) – 2,091,218 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bb61b99dbbd99e50145f83b3d74bfae<br>SHA1: 7db962f48946b3f1c0d94a90adac3b4fb5c747c7<br>SHA256: 8727fc1f8a4c20c18f7e96b54a5d5c3c05534458832b43a23fa36388c4f4678c</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.5 MiB (212.4 MB) – 2,091,218 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46661d8cd62154a059136598b0199996<br>SHA1: e6ba9f5098858517a6a4dfbc09dde72b1c4d8b8f<br>SHA256: 8dfa119f25f6a7d110f25319b4c1508231a282b63ba1feb7b9875e3676f2e7ae</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.7 MiB (206.3 MB) – 2,091,218 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 266371e4dc62aeebe8ff679dcb07b502<br>SHA1: 7ab885e422a3d4faa2848c9bc52e5f1d9614d992<br>SHA256: 0dd0a291aa6559ea2b4cda35c2d816e99e23c16a80c335d04b01c1a64f437012</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.2 MiB (206.7 MB) – 2,091,218 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f513adfd6bd26c3ccb4aedf7af29de65<br>SHA1: 88a3ebe0d85aa925f9f5b0d14b32642527086b71<br>SHA256: 798129eb6ac1eeafd82a8ebcc2b89de1cf3dff2f2c777747d86453ee6ed7cea7</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.0 MiB (229.6 MB) – 2,091,218 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 385ee5d1e5ac01a2e7534242c3cce0a9<br>SHA1: 1fb3414aa0c73d15405bad52e863c7a0fa9af039<br>SHA256: ad60ec45a87b92e24d76a83bbf4d2421f4bd5476a69e7da2beacefbbbf6c0664</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.7 MiB (206.2 MB) – 2,091,218 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c6772d9e5b19393b696bee60ce0236b<br>SHA1: b6dbcbe3d725984851c98ebdbcbd7ec598bdc347<br>SHA256: 94d0a55568ba10b94615422604332d77562af4cff20b9e0c4abfe61c3a1f99d1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.4 MiB (232.2 MB) – 2,091,218 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e6a177ba20546aee772dae439586480<br>SHA1: 257b1061baf347e59f3b1c2fcd56a988a6611f4f<br>SHA256: 98dc46ea30a31bd062c0a2f679dac4958c81f3050218d39511e4ccb38a9f128a</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.6 MiB (209.3 MB) – 2,091,218 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0800d596fceefa729a0979af1f5be4f<br>SHA1: b05ca649f0e763bbba7ace3e5ee0f5c80601ef68<br>SHA256: 62b26903999a7073ccd028095b425fe57b06cc835e88c0af17c47232bedb8a87</pre></details></small> |


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
