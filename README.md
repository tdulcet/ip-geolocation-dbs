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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-11-02<br>IPv6: 2026-11-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.722 MiB (6.000 MB) – 286,381 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 400787e9dab69918665612b2ed4e800f<br>SHA1: d95410862997db049d6c182ec34081e1e4033df8<br>SHA256: bc59ca74ac29980f7e52705365d054fdd66fa60f813ce599f99d8c0a7a456846</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.56 MiB (18.41 MB) – 266,876 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02e5520ab4537d42f5b82d98d00ace96<br>SHA1: 0cbf14e81d58bb518cdd0a4314423cb053597580<br>SHA256: a5b968a6309db5b6c4c67e019a96fa7b599119d8b854f0edc64e61910b09d70e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-11-01<br>IPv6: 2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.186 MiB (9.632 MB) – 459,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84167ee008949c7e879c18eaa6df481d<br>SHA1: e998f760da828517741b8a57f76ceac532d2afea<br>SHA256: 03cc8544ec1d65aa3d43c09d4f8db8b5471fb5a48eb435c2e8626cb2c202790e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.883 MiB (8.266 MB) – 119,798 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93720f717969024f48fd382cad72f274<br>SHA1: 5173d179b24a928fce65b1c5c1194626035a37ab<br>SHA256: 645dfd169109e1cda747277411d71f68ca9d428d01b715756c1925f6ae7473f0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-11-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.44 MiB (13.05 MB) – 623,022 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34c571e226525312767b3deef1fd1eff<br>SHA1: 69fdc49923aa3c34b8d30d298c792ec1e3cc1e60<br>SHA256: fe6596bbc1c383e32240ec2a26c31c2e5db5c673b2b4d5f2b3205dfde4e8ab8d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>85.52 MiB (89.68 MB) – 1,299,678 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f0e851a5d7131f910a36d892ceb9a72<br>SHA1: a1d9514f2706fef37e76bd5182233a6b9d33daa8<br>SHA256: 9c32f3f1a97d23e8da95c65cda43fd3d882d322b6ea8eeb8dc380d01c923ba69</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.244 MiB (7.596 MB) – 362,984 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1896a3d70d9c776ebbbc51174d2dff7a<br>SHA1: 6b153e2b071d13e45ab9795a9d41e7fcbf0b910a<br>SHA256: fb52bd209b940b70d4fa6772242238a7238e3fdf267f7232a326a283a172da63</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>24.33 MiB (25.52 MB) – 369,794 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90147b4da0ef46e810078a3ca7e5aa0b<br>SHA1: 9df64ba895edf447da29fd2c604e9ff223a49471<br>SHA256: d30738d906d231b000d8994f7a07aee2550e5ba72a4d6ed8b60712ef87862557</pre></details></small> |
| | | Full Location | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>205.3 MiB (215.2 MB) – 3,598,802 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a48535424fbcaaabbc7dfc056e39f5a3<br>SHA1: 4394336d775415fe1a653bacbda7921ede4fd2c4<br>SHA256: a320a6ae6f82cb61d2d9b36a2baf9ed6a69c127627aabc98a1c598893700a202</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>430.4 MiB (451.3 MB) – 4,178,996 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b774537c14ceaf921dbde58aa6fb3f09<br>SHA1: 7695b1a6e7b8783b8331d8935d87fb6691eb8b0f<br>SHA256: cee773355d5c7bcb515c4efd0abc0daeb0b545de5e714601f54daa4c6c03e77c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.813 MiB (6.095 MB) – 290,990 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c7072a914951e8601c9ceeada7a3d6d<br>SHA1: cf54f7394145aaf4cad9d5806cf033c5d2e05129<br>SHA256: ae75289541009f5e4e55f485a547f5969d05bf27e77319236873e0cbe6042b95</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.34 MiB (24.47 MB) – 354,673 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e0dc2b8d91b7ba4229624281d2e16c2<br>SHA1: 0b3d99b5bb726900a6a60d2a140865a09f6c202e<br>SHA256: 8c00dd52b8cad30ef157bea8292f275ce2427479b23834b052923df53c5ab3e0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.4 MiB (177.7 MB) – 2,928,935 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c7dfce82c76c40935365010e208451b<br>SHA1: ceefe3f4d1597102c1e20a15432939082505547c<br>SHA256: 25dd83a6bf875037466f23e735227da25d97c795213017cef409de7778c8671f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,928 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75980237a60e580bcf5a6bb2276cefaf<br>SHA1: 87785f70ceb15fdf9f19a474ecb10f6d04550358<br>SHA256: 63657dda83bd39e0d502cc12ad78bb16eb3be91705bad6374d45345f41c7c24d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-30<br>IPv6: 2026-10-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.29 MiB (11.84 MB) – 565,442 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bac0df30c82408acb34ecb47e4fddcd<br>SHA1: 4d15ecb965cede6b4f6c40319af977a31a5514bc<br>SHA256: 2be7788fd1872cd627fea14fc8fd5bd94d7008c4e89f95227ea666a8817e8717</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.79 MiB (34.39 MB) – 498,343 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5238f5bfbb7f29923483fa5a345de094<br>SHA1: 07c50f22d019ef17acbb71f6ab34ab84550f93a9<br>SHA256: 2dfed78af005f7d29fef3b268e8ea2de99d5c28713c2de8338a837e185db40ac</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-30<br>IPv6: 2026-10-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>188.1 MiB (197.2 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94efa7fe7cca6656cc5d15fcbab7ce65<br>SHA1: 7b67b511ee3159f1898176044487b0779f6ab499<br>SHA256: 522ddf6ca7ca3cdcf81b5bd130d561ed9a8cb7d761c3d8577b98daedf9a5342e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>196.7 MiB (206.3 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 926b081348ca9f9ccb3c48897470bb2d<br>SHA1: a35de7f07eeebf05968832a47ba6612456f52fbf<br>SHA256: bec5fdf0bd5bc87d689672086004ac3b57e92b6ec5ccba8c8737d79309e7d0a6</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>187.1 MiB (196.2 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8914fbf4e18827f1f7a556b60932d9f5<br>SHA1: 09857368081dc0abacc908a6a9b42c9375d53503<br>SHA256: 94b1e6b5ffc663a109fb6bb5f11a1697b715de3c8103432686818b73e1cf6d53</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>188.7 MiB (197.9 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8007937400b05a1ad4737e5243b4ce2<br>SHA1: e36749f4772b9f779c82414e1782256b6dbda73b<br>SHA256: 9411bd9a106ba884c3c82af7ce415e8f049443ba2e07b892d612c46727203057</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>237.8 MiB (249.3 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e206c9cb4a9130ced5ea574bfc464f8<br>SHA1: c7d3311f38aaec964f992a7c3cc047688e20de89<br>SHA256: 073c80c14b28530cfd7df3e8b659dd4c76ec1c8f7d4f6547fc75f87b37a3c844</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.6 MiB (195.7 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c17f7c1ae6d41ff77ff4b9de5b7daa8<br>SHA1: 1300cb8e7f406370ddfb489535dba9142967a875<br>SHA256: 7244c0dc25bcdfe93228384a6ecbbf592e4fb55acc49d77fd251c7d889be6b38</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.3 MiB (246.7 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3671fa6b427585a84297ecc656cb3650<br>SHA1: cc87bb6c04c019e185cf1a7f9258262b9522fa96<br>SHA256: 9190a1531dcd3e5477f28cc5e2ef404914e70c2ded1a45e4c2e5cf4971ae6c36</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>192.4 MiB (201.7 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e426307d2f2ee99ff71333ad9690c89<br>SHA1: 4f039a54b788fb00ba012d60c79159e892ba74cb<br>SHA256: 73c2fdd97b41aaf366dbc8f498460f753f51c321acc264b8d813527477f8c0f4</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.5 MiB (209.2 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a58a984bc62aa2389e1d4b4e50c968c7<br>SHA1: b4f80673d30b41b4991deeb7e146cdc334694e8f<br>SHA256: bdd7c9378b7ace18e0c931df3bc01faccef6289692cd8e702438fdba4949d897</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.8 MiB (212.7 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38f51318f7860a76cef157e4e908af12<br>SHA1: ea30b83dad68f8d63703de9272eb85f6eb965046<br>SHA256: b35cb808a1feaf9c8b0e4e1e472e2d569b690d63140b86b4bde6b1f9436a93dd</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f839252958a56f0564a87e4c2be426c<br>SHA1: 69f0bdbed0ae7651dfd491ec0147bd0d9b0b7c9e<br>SHA256: 6075c44cf5c062fbec03bd649f33403dd220e4bdaca720efe795001a4e78edba</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.4 MiB (207.0 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f711d4675567bcc9c5cefe1e6e1cea02<br>SHA1: 88ab2072cb7110f5a43b79a08cbd627a1deff1b5<br>SHA256: 3ccdf7a4f2118b07627a697acd0c046f0f0bebfaecbd1978674670568d2efb9f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.5 MiB (230.1 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c02bee173afc7a153598bd86f3585c57<br>SHA1: 63ac70901cb0bfb09539216b6ce292914aac58c7<br>SHA256: 3f79108192ff9c8a397f89626e6579ffae6163d2e9fb9075e159b971e4a08271</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.9 MiB (206.4 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba6fdcca211de06e09b9bdfe4a84e3ce<br>SHA1: 8b597ea024755aa6c5c44da606e0f5112a5953dd<br>SHA256: 8d310d4fc794455bc5fd005c0ab70085510028aa4d4d32f4f02480cce9780938</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.9 MiB (232.6 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e68ce272a9a0fd0844d7fab1cd971aee<br>SHA1: f7a77565a94bdb6ef279b332a5a8d047a228cbfa<br>SHA256: 8175ecfa43d4ba782a594408e5a6b44384f8cfd95b7904490812368c2b9f9be1</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.9 MiB (209.6 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23e5a0ad75bbaa93d22358f3c390b95<br>SHA1: 855a88ef3169cdc5faf814ec09cf8a8d4d211862<br>SHA256: e35ce7d4e6a33c39380eac9032702a9425cbaea64b853c390b29269b20bccf22</pre></details></small> |


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
