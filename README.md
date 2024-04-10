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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-04-10<br>IPv6: 2024-04-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.825MiB (5.060MB) – 241,573 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a04c160f233151032a25acacaedc97b8<br>SHA1: f0b8fd20410007242d7ffbf092105ab5e4481941<br>SHA256: ab76088fc4fe3647261c6151655ecc1810f300a2209fd717e13c8c2c56562b40</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.112MiB (6.409MB) – 92,890 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2951b982a12b0521104e448a627e40b<br>SHA1: fade7af24f4540610f6eb4a39ef2b3c971c28db2<br>SHA256: b5e86c8a5751583e318b86d3d551d1d0031bda744a5aca641b90cf2fac1acd5e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-04-09<br>IPv6: 2024-04-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.228MiB (8.627MB) – 412,026 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db864f6e3185424d6520313c2a1c0a63<br>SHA1: 63822e4698ee037c115e215268b1c4f9b036f8df<br>SHA256: 7d9a65ecbaaf3940653490f4b16b7e9325d2861cc69ef63181c9de0eb7daf083</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.153MiB (7.500MB) – 108,812 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c547c4889a03c933ba3205f38681bfc7<br>SHA1: 0d6067f2986036944e25319afd71ef505c85c70d<br>SHA256: fcaf0d82b07dcfd2e9a37c31792427b4d1ab7f7065be372b3a899e4afdd81b85</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-04-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.94MiB (18.81MB) – 898,157 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9cd73e707df8530eb7cfac8b958ccaf0<br>SHA1: 374e5a6eb07dfb6af4df3ba0d7d50de43e387463<br>SHA256: c524ad358e1a695fd59f12ce42637227045eb33fc0c73f97c6007ed58cd57646</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.29MiB (77.89MB) – 1,128,903 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 514b2e8420b29ba96cd30478349c5ab2<br>SHA1: 7bd2360be571737f2048a3294b8ec5846432881f<br>SHA256: ec50d6b938362a74461d2caf1b154faa69790c68409d5e33ed562dab52aaf522</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.603MiB (6.924MB) – 331,502 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed612f6829372d96d1503867a952099<br>SHA1: d545a9307049b4d56f79cfc1544864fa920d1b6b<br>SHA256: 91dde8f7a7970c4c1b8054b947e0cca9ae1b8735bdd19fe420e6e491a7427366</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.03MiB (18.91MB) – 274,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b254c68dde265fc8d6412499c6db3dd7<br>SHA1: 2cbecfceb25b68f5f0f9889993e2f4931f5e18dd<br>SHA256: e4727e6d32df38a7582a7b9172ee67820f196bd746046a5050cd654393436920</pre></details></small> |
| | | Full Location | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.8MiB (189.6MB) – 3,159,870 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e335ee8885a5e6286297a9c06a48db0a<br>SHA1: 9b10ee274410a884c26ab662fbabb41f315616a5<br>SHA256: fc15b0d16ccdb65b6da2de506405d685d02531ce5571558ba78ed3e9110dcbbe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>322.9MiB (338.6MB) – 3,132,412 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eb566a7a93d1e35f303a2978c1da77b<br>SHA1: 78d75aa920c86cb0b75dff47ca09bb4f55bb6fd9<br>SHA256: f95d154f7a461a32269f564496c943eb8cb5e61df0269c831e76ea2f52896979</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-04-10<br>IPv6: 2024-04-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.897MiB (5.134MB) – 245,145 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86953d84c1cd0d89d0994ab1cd100b39<br>SHA1: d3303729b5fdd4e92be0090d728786a641d6bdf4<br>SHA256: 9503103e96fef9a268f0d6e3e3e189c3c227ba6a962256a4be433fec98dd6295</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.43MiB (18.28MB) – 264,858 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dee1827a7716642179bea6a3edb75c4<br>SHA1: 6d32a09ab10cd650c38bb65962cded09532e32f0<br>SHA256: d1b625011cb76995dc6c5895dea53ec54db80bd372c0878631cf89b1e7957469</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-04-10<br>IPv6: 2024-04-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.5MiB (178.8MB) – 2,955,821 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 100c457dda8054191dec8cb248ef7116<br>SHA1: 5997f43cfa17dfe7406c1480e1305b0ee4d7d2b8<br>SHA256: 2e80f7bb769fbecd8a09c918b55397ec9abeb21f176c73e5c23ca937d52e974b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,714,136 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09506237fd701236f9a08be9c399f75a<br>SHA1: 012fc8437c33186fadb2add162e68a946c843774<br>SHA256: b25eb4c33c6657facc2a0eab8012f99200c9aa7dcbc9eb0f151bcbda5e02cae0</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-04-09<br>IPv6: 2024-04-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.668MiB (10.14MB) – 484,364 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c686d70641cb1c70e030208ddf41c1e<br>SHA1: b8697bd64a32550c4dc37bb6961cf0cb60bc9d1a<br>SHA256: 73f53da17d1b066764c19d04451d8cad96fd253f542a0c9c71b5f0eacc0f19d6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.54MiB (19.44MB) – 281,772 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f95e984ba24be562a21a8f7407c810d1<br>SHA1: 7afe3745a57c30588ca358df06cb1124586f2d72<br>SHA256: 87c9e509ecd945c7f4d4c5423c91b9d163b67fd94b2dd57e0b0a7e77f8cd851e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-04-09<br>IPv6: 2024-04-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>130.4MiB (136.7MB) – 2,605,161 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb0fe0b075ec493a469a8c85d6c31bed<br>SHA1: 04bd49593465c93fe51ea98b32e83f334ca50ee0<br>SHA256: 53d8e1839b20562d0fce993af9f4595b20d5b9c6f2f98c1cad06c8d2d148fcf4</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>140.5MiB (147.3MB) – 2,605,161 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70d3e5ae4b957939f54c1172c9a3cfd4<br>SHA1: 5a564eb2812dcd842ac9c85c518df78c7c64cafa<br>SHA256: baa3d5ffb8c92d70f30b4660c2bfd8e4347c19f98dc719aadd11a39d384e1de9</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>130.2MiB (136.5MB) – 2,605,161 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e82c7e224f9608293c975a3a07845813<br>SHA1: 2553d250b09f0dce180beb341c5320057eaa6fb4<br>SHA256: 5c8d702cf895ee0df87bed86f8a5b3646af40a48126cb1f568aeb662ea4aaf4f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>132.9MiB (139.3MB) – 2,605,161 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c48f74a8c7dbb42664ed595b50049c21<br>SHA1: ebb42762b1de4b64a0bc45300918aaa98ed89c10<br>SHA256: e9a362b3552d85108853687259ab53ea9f7d386cf7f38054b7d8593e63dea5ac</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>162.5MiB (170.3MB) – 2,605,161 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42f2cc4ef0934f6436eeece286890497<br>SHA1: 2962a19378189f5334464a5e5959004a8f7f0e3a<br>SHA256: 3634190b2d5aeaf8f6c39fb29d1af0ad39263140f13dd3be60c248409e406603</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>129.1MiB (135.4MB) – 2,605,161 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 623a346c4988d039b56ac33731193ed4<br>SHA1: a5e26b9229ab1e0ffdd95a6f5db4c67c5e012ba0<br>SHA256: 304d704faa109ca22254d124c9a8c34073aef3fbae0cb8db3e872f1f71016d85</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>158.6MiB (166.3MB) – 2,605,161 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c013089704c748512edd45b303f1bf18<br>SHA1: 74da48cfb1c86b5ec12d946977c6e0aa21840c88<br>SHA256: b1b54b5e13327b0fcdf262610277a83623f1e251cdc7c5bb1f935bc55b396b3f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>133.0MiB (139.4MB) – 2,605,161 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1a98159c819b031766f20ac1a0df372<br>SHA1: bcdb32fe73120695c1e0add9fccaf30afd97901a<br>SHA256: 8ce3cb77eba3ad2d93a8e59d68cb8ab38afb5062df52f05ec65d17c46cf01b01</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>113.5MiB (119.0MB) – 1,220,909 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e6aec845044e72615bf65a4bac07732<br>SHA1: 454618b16c454e0651075354106ce2a3128e1f48<br>SHA256: 05bf10e85fdeb888924b496e6d747c76d0feab8147cac6ba55afe7ba41610aee</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>117.4MiB (123.1MB) – 1,220,909 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4b3f4bd8d74668c577667a517f3c475<br>SHA1: 6a431034a6195fc10b1abf756e2d7f13aeb93218<br>SHA256: 30d756d16ed3cb2efe749e1cd753d37aea302fad2127828d650748629eab2661</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>113.7MiB (119.3MB) – 1,220,909 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 716096507e0a43c57a9f3fb320e04b5c<br>SHA1: 4de215b82e50c2527bd8a63576b2d5c40d2e2da0<br>SHA256: eb3d4559ffcbea551b31e89c8f31a48315be3952d4521138388b55cd048eafc1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>114.2MiB (119.8MB) – 1,220,909 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8678222bfd47530d0d665dcb6ea6ed21<br>SHA1: da83972b9b24c12f416cef8db100ecc11ffdda94<br>SHA256: 8563fbcf6404f935ac85ab0f635b56ffd6da78100921f947ad61edca4f3d00ea</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>125.0MiB (131.1MB) – 1,220,909 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f199b7c0c0c25d761c3ddbbf477656b0<br>SHA1: 6f3bf112266d60d2ce3426a4311c7126d9abb7a8<br>SHA256: 63d0097c3130f52867033d17ccc121ea3900da44d8e599f3ad8f977021450209</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>113.4MiB (118.9MB) – 1,220,909 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a03be8a3f82c165c4f5b37eddba5992a<br>SHA1: 3f103d0434a216363d861ab922a15a46a08df32e<br>SHA256: 7b2968d4aa1abcc3ced4596ba560dbc5c40123d6b8e22c81ef3d26a2b4240ee0</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>124.3MiB (130.4MB) – 1,220,909 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3146a38fed9f4ece8e9830c6f80558b<br>SHA1: 523cc632f80da1bed37a51c3eebbf957d67a03ca<br>SHA256: 79339a28ed29c6233005970669f6a2bef02a2b9b0ea06544d9718a276ea8e1fb</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>115.2MiB (120.8MB) – 1,220,909 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54c8fd29a884d5192ba40fe0ead55005<br>SHA1: 2bc21a11402c2e523084850b26931c86838e5e0f<br>SHA256: 7c88792cce5fdf87635141e843ed04986c99273e1d262f0224e737ed655d4b72</pre></details></small> |


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
