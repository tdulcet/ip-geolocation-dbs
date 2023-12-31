[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases are scheduled to change from CSV to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than one day (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-12-31<br>IPv6: 2023-12-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.608MiB (5.880MB) – 238,841 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ffa0fe5d80597e6c2ebb616f38291a4<br>SHA1: b0e00e17bf5ea2af5de62235c75564e82c1f520e<br>SHA256: 233647b25ce834df13a138b1af1b9b41cd584feef14935da904263846ad5f048</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.391MiB (6.702MB) – 82,740 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b3cecb5130bfe8f08324b3988037e3c<br>SHA1: fc361d2ebaa423263cd4830d601bd5f87789f8cd<br>SHA256: ad9005f3177bf23253c4dfb02eb567beb0dfbdeb4ec86ef2816bd4606518b3d1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-12-31<br>IPv6: 2023-12-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.724MiB (10.20MB) – 413,026 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 440f73492ebe533d79ef79208a4c6fa8<br>SHA1: 0ee4c981254c0eabc399d6a7a832695c2b4cce96<br>SHA256: 5ddbccef98c211ff3ec119a3dda5957e3b2c50f36c99bffae5420b22691f6be1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.078MiB (8.470MB) – 104,670 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffbd74d3f6d505432fae5b34f8c421a0<br>SHA1: 6edc26e3554d5f7ce2cb822dd1b87fecd6a63674<br>SHA256: 5f93d6f06f0909571ee74c0035f19ee12cd470f11b0c6d5c140944302aef114a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-12-22 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>21.47MiB (22.51MB) – 912,531 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a300ff77934b7044128e9e3d0cda3c0<br>SHA1: 62b2513e142deb3d2728d0f3aa50b0968cf46dc0<br>SHA256: 0cc2224ff9e1f16358462772a12116eebb6404b4cc982a88a96fe728a3aef76f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 2,090,652 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 778937c5b9624aa9c6606e1b1bf40e51<br>SHA1: a5593a83d5aa682e4f9221c8ea17018105df1686<br>SHA256: 879856b4bee7da9503cadab9623a8a691a677881719bd4cc299aa3f3b87b2a33</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.227MiB (7.578MB) – 308,674 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7862828d186c4a916870bf5ee5c2dbf<br>SHA1: b2d61949f9d4cdf20a7bbe7858ca457da6437400<br>SHA256: cf718693f02d6570f872d99279b6729e48674fdf9a0ad17b2b5bd3a3004e7feb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.88MiB (26.09MB) – 322,049 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf9a945a8ed9ee1ba2168317dbed510<br>SHA1: 5488b48f6e283b58e14057f8bcc69c7a60073e80<br>SHA256: e724c992a57d034ab069e985589127206d0519f5cb5070ef4d8bc04d59937e7e</pre></details></small> |
| | | Full Location | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>188.3MiB (197.4MB) – 3,100,304 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e98adbd1d81ad4e7676a5bc97c6062eb<br>SHA1: 83a91e8b43cbdbea769542d684e8a2b61d6cbcb4<br>SHA256: 07faf7b0b69afe9bdfb83c30bf26ed6a6bc739fc4122230461107e862ca8202a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.3MiB (310.7MB) – 2,579,379 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b45c72d3f47f242ccb1124627ab028<br>SHA1: 46f55d20900ce13c49f5881ad197bc7a0d54d072<br>SHA256: cade24018cccb007f481018f12d82b3268ea4089c4223c710ce4213be2f799e1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-12-31<br>IPv6: 2023-12-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.426MiB (5.689MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f1168f938cf9939a4db2627ea0d3aab<br>SHA1: 3d4f791a4ef9f8391ba4970939c4681bb739baf9<br>SHA256: 0be742468ea1b736effb939648093be1986202293187170826d147402251e44a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>20.07MiB (21.05MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a23a416cd5ce5dc03b9cbe11228f3a3<br>SHA1: 765e389ced957809c29feb7d42217e0e3eee8df8<br>SHA256: 73bc73bae2b14496056b243da3b2e2638e3246fb911159cadd9be315d7fb59f6</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-12-31<br>IPv6: 2023-12-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>178.9MiB (187.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88dc7b190a561ded04490bc5546295d6<br>SHA1: fbca2a42d89544e9dfd8835511d5852f986e439a<br>SHA256: 7a5ab9f0e69bf6ae1b57fc9778a0d5f844624e9fab7242c30f1a4845342848a9</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>179.0MiB (187.7MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6f4b0298a0cfd2f8debb7ac65c9ae35<br>SHA1: da1eb06030ca04ae9e61aa7723f34727d9474af2<br>SHA256: 6cc5ef9a70e83e77fdf8ef506194884f379b8a96081ddf2650b8b7dc2787f773</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-12-29<br>IPv6: 2023-12-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.77MiB (11.29MB) – 459,327 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 207a54fadf33aea9c6838915d9934dea<br>SHA1: 9ccfc25182a354101727c0add85b176ce1540190<br>SHA256: 81eb9ac497d47446c377019742cac1f65cf1c11455e545e2436041cf8c8302cc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.21MiB (23.28MB) – 287,471 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09cf645278b2420e8c4dab1246b14113<br>SHA1: 86003af1dccfab75869667de3c88a1d6f428e4e6<br>SHA256: 8a8f75c22d2cac5399e52033f9b04fb7f907dfeb4411c1ffc0b98599433a344e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-12-29<br>IPv6: 2023-12-29 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>176.8MiB (185.4MB) – 3,506,613 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3afcb53d412a7a0084f778c229e8ba2c<br>SHA1: e5d78294955efc564cf109aa49a98c8b8f942ab7<br>SHA256: c6e934063e81fc31100d130c2c158389f5085fc5bb2fdc369f528959e9d4c3af</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>205.2MiB (215.2MB) – 3,506,613 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4468a15752df71330534e41b16e264a4<br>SHA1: 82293f953f1d857ffcdc601899e35fe057065dba<br>SHA256: 5152268bc850b3ee496e1b07720ed6fbc6775bedc960a104a476558f44986c62</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>181.9MiB (190.7MB) – 3,506,613 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d242f2619d6a01f835be2cad0632a81d<br>SHA1: 32a8e11725194ae1860e69677ff67246f4fc4168<br>SHA256: 5bfd5ec33fff27dc86db6cd286e839fa7281877a04fa2e12b77ec7b9af64914b</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>188.4MiB (197.5MB) – 3,506,613 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc8631ee071b9ae9593e45f40dd001b2<br>SHA1: b2709ca63639ee6f687818c7e05cd0484af9dfb1<br>SHA256: f43e1111343c05ebee2b5145ed1d519f01863515599d8e720e958b7a01c0c190</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>217.1MiB (227.6MB) – 3,506,613 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bf6d31a1034e4fe14eb31d0f1cf14f2<br>SHA1: 4514433647cfea7673a5fcdc3951e6bbab81f3f6<br>SHA256: baa0df849a6d487a8e3c9b12de92c1d8310701b201ba0d1a3dbfe768ab7db9ad</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>176.6MiB (185.1MB) – 3,506,613 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f331004e9d62ea8dea06438f3658f37d<br>SHA1: db78ec0049b1d7f8d709ed34c64e27d5e622b58a<br>SHA256: 2c43d7adcc8d181e00590547915ea847a622db99eea3e661b4450a4020da341a</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>218.2MiB (228.9MB) – 3,506,613 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae86c81a0360f6058af09baa82e9ea0c<br>SHA1: 3e4ffe15ed17472513703377765e1fbdec97ade3<br>SHA256: 1b95eddb240783855a4d71bbdec01edae4689fb3a740903c7306446c35696559</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>184.8MiB (193.7MB) – 3,506,613 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cda536fe823c79f9d95d1392e9f48e4e<br>SHA1: 56965c8ef49db3852acf077da32e50c06c6566fe<br>SHA256: fd124261902ae479b457d5c0789e36db54c70fbd39506b6cce16d332ae3fb9da</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.9MiB (128.9MB) – 1,220,923 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f708b09094945c1043e1b72420a5884a<br>SHA1: af13d1e94cae74921e8c1ac3700319bf01d5e4bd<br>SHA256: 23fd5926a1881c8bfc264c75a48c03b1514b6ab564ff6309147764dbca60c346</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>130.8MiB (137.2MB) – 1,220,923 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4109dd7128ae0caa82e0ec5ef8659e56<br>SHA1: a9ccd2fc50355b3669f6f10f9cd5a8a5621ebd96<br>SHA256: 71d06becb0e4704c1c421572a28f72449d32caa17cc5e4d0ed660bf3c70e816d</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>125.2MiB (131.3MB) – 1,220,923 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95b0102dd4f6c5d3a0bb7d4521b4cea7<br>SHA1: 948aff0db6d9521b4fdb74cf1a09e6e9da9bcd0c<br>SHA256: 10cb1c2e813f7d75f75d83cee7a729f0ddabc86b0ee2460042e9b586b8f87138</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.3MiB (132.4MB) – 1,220,923 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80b845c7701865907580d7c07e09e963<br>SHA1: 9163b6b02f9db5d951a7f4d17f804a6987bb9d32<br>SHA256: a147573a431db407344c3a3269b99e46803e19c4b35a42d159293047fef0f8c2</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>134.1MiB (140.7MB) – 1,220,923 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65a3430f61c48b81b5c3eac18dbfa164<br>SHA1: 7b1a846354c1b382b4a5b49c66964e7ae1f42fbf<br>SHA256: b632e6e758e62c41d2c95a76a0a9a7c3c98f5e0eb95017a04b3f32e924b047f3</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>124.1MiB (130.2MB) – 1,220,923 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ffbd129e8958ad058523884b54ff5fc<br>SHA1: 1630cd57bde6e1a5e80da90c100242c6cb9546e6<br>SHA256: c7478edf9ff5a85b00aa9288abe1e52c652b7360d5a56cefbb48ba261c0b9bdd</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.6MiB (141.2MB) – 1,220,923 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d74912d21ab8cc1e0d84e72e55c7f98d<br>SHA1: 40571ed55965f307c5a962726f3a849aa1f432ca<br>SHA256: 4a63a191da6109158811cb3ef3e46b676b3c189843210b065ec996bfc3c20637</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.8MiB (133.0MB) – 1,220,923 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca624abb48ceb1930efc92c60ae3b0c8<br>SHA1: 7effeff9cc90ab185d7948e97a9072009d5b6e32<br>SHA256: a45e759038325885941b266e1c3c9657cba642f97620729f7d9c28edf38fcbee</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hexadecimal format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
