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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-09-15<br>IPv6: 2026-09-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.537 MiB (5.806 MB) – 277,096 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e44b0111a3a631afa7bc5587e542cbb1<br>SHA1: b589447240d8121c91b463fd11133459c9d12c21<br>SHA256: 94839c5f0d9afb5d3d7cd454a3abeb2dd9cefd795341fba2219b2269c00b1e08</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.72 MiB (17.53 MB) – 254,116 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf101aaf592219f1b10b094d7abe2da8<br>SHA1: 8b84014ca92e26612a05209f8eb2c32b538ccf7b<br>SHA256: bb93905b49db92a6afc90991c20ae38d25cff58fafdc9c1ba01e7a8fa14735bf</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-09-16<br>IPv6: 2026-09-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.143 MiB (9.587 MB) – 457,806 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b9949c9de1242dc2b5df27b5ed1780b<br>SHA1: 9ef2bcb78bb02ab6fdbfa0de42a5abedd0254c20<br>SHA256: 5bdc9e1c75170935127ee7048527e0d6929b2a84451e6de8525d329737720632</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.023 MiB (8.413 MB) – 122,041 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fd9a828c9d86fbb197f9a38a6f6a02e<br>SHA1: 1cdaab70b0a81eeb4797b6279e9691d32a81bd25<br>SHA256: d60bd3b1c0ad314ae641631b7c6ba7d83906d3771e0fe20eab270dddef856a20</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-09-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.43 MiB (13.03 MB) – 622,221 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd91b83c4fad257dab9c28e3653dff83<br>SHA1: 8665b1166bb4160ad13c3ff92734ae06f2556262<br>SHA256: 1a38f94f6a5ccd06228383eeb0bbf8712957418c61fbf83a15034bb395af02b3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>53.04 MiB (55.62 MB) – 806,041 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d96c07f95c9ae29e338cdfb02aec0bea<br>SHA1: 00a75fc9c861fd0a0dc0fd7637be51480ffe3b66<br>SHA256: 89349548782339c54a129adefd47d49b1597e7f4e6b786b08aaf31b5fc664ce1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.133 MiB (7.479 MB) – 357,311 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c47fd01af8b18cc1d5cf2004691771<br>SHA1: 6b08ac2e1f8b48e55e72f8ba6ea0079e50a1af12<br>SHA256: 63aa3454aeef9769e4f0d68b4b93b23a7d195199a50487f4db5d258d90f8b08e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.68 MiB (24.83 MB) – 359,841 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ed7b2550b03a35e3bcceffa4ff9516e<br>SHA1: 2f8880592eb4dfde0c92576fbc78417988b521fc<br>SHA256: ecd35f269cfec0024d6ea639910b54c657f3f1dc08ab339c3d0b0384ed3cb607</pre></details></small> |
| | | Full Location | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>204.7 MiB (214.7 MB) – 3,588,539 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343b463b14a760e04ccbd188e88baa4d<br>SHA1: b7e446f674922e349cb17f01c859bc3bd62fd5e3<br>SHA256: ba1847bf8c90ff7f1ab0a19c20aae3512e9bf7a3f144673fad5d87dafbf7780a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.2 MiB (449.0 MB) – 4,160,441 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2542313832b0583d31e84cd0f9afbfe8<br>SHA1: f2d167034376bc0d28d3f5a38fe3c15945c4ba61<br>SHA256: 9c2aa7d6132f5be8f547273ac5e8f21c074f3d7a26b3f7795c642f4a3b6a9693</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-09-14<br>IPv6: 2026-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.761 MiB (6.040 MB) – 288,365 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6747ad281e6d203df87a7283739262e3<br>SHA1: 90c532db8f1cce14645149b8f5cc394de42a2c96<br>SHA256: 6a9d95b18e972f327a0f7a32b7b4d33f0e33eef14e127439bb12b976b30249fa</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.80 MiB (23.91 MB) – 346,477 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1bfa9fbed82c09b5db9b5982e8b6d9a<br>SHA1: 8ce51aafdc54a7b6766d611cfafb10502b38fca4<br>SHA256: 9bc47e288cb9732ba16dbdd489323efcc7ac2a64bf0d684bc731464539bd785e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-09-14<br>IPv6: 2026-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0 MiB (179.3 MB) – 2,957,517 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dab7122ae812dd44dc6c14b6519b1f5f<br>SHA1: 10115286d4268e45b97d687718e7f7a5030498c3<br>SHA256: 9fcf166e7c6b2ce4064e5878e3c5094a10efd8718e9f3a05b0ce3206d68189e2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>304.4 MiB (319.2 MB) – 2,948,617 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 802cd20efc7238eaddac6e73d1914581<br>SHA1: a16e3bf85f8d17952c77749f9a5547179a3e0bef<br>SHA256: 3bb02a5d77da37fb74e8ab2d2e8e28be7e39f3e0486c0af2178bdaa6b3ff86a6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-09-15<br>IPv6: 2026-09-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.19 MiB (11.74 MB) – 560,537 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 989a590549544ed0c2d1f23e3e1f3ec0<br>SHA1: fc82154eae9fe1d2dbfe7bc7ebd8d696fa3c9e46<br>SHA256: 82703fa6cc147841d64a99dab85555be63a83d43e960ebeccaf7f3044e355506</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>33.98 MiB (35.63 MB) – 516,425 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e08dc028d9bae0dd12a8610637c8f77b<br>SHA1: a3d168bcc6e13e453e42706d660a9a0ba37e74ce<br>SHA256: b4e1d5efb360e1523bf5fde896782fcef9533cc4ba13f8d33da190c778a7a254</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-09-15<br>IPv6: 2026-09-15 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>190.8 MiB (200.1 MB) – 3,717,075 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6733a15393cdf80589937d78e03f3420<br>SHA1: d9bd764bab8df417f14ab9d66bffd429b19a2d30<br>SHA256: 93d108eb58364433b5ffe0217bc6f00de015c602a75d6e705492826b75b46562</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>199.8 MiB (209.5 MB) – 3,717,075 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ef2bfc30cd12e4db14afbb9f2558172<br>SHA1: 84ee160fcb52e93ac1ddd3229518e1655b521684<br>SHA256: b42f82eeb98d9defda73f0f03ef948c9ffc3fdb07da5c87cd762a04fd98fe174</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>189.8 MiB (199.0 MB) – 3,717,075 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a96441cfbbcc0b515f58f8649fa021f<br>SHA1: 629b4039e8e33f2b46abc8b0b80c2333a41d312d<br>SHA256: aa7e483b52137387394a7d5a24571ee4462ead125ad76d2faa11ff08a7cbca75</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>191.5 MiB (200.8 MB) – 3,717,075 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1feca157acd25f6c8136e32fc120d2e4<br>SHA1: c0dd3908620e2e11e26289cbdb56daf35834b4d9<br>SHA256: e0df7a8647e425e4a4b7c69e1d66cc1476862025624cf2dbd15fce7050d66256</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>241.4 MiB (253.1 MB) – 3,717,075 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3deff83a949b2dea902e377f9160ea3b<br>SHA1: 588d27736b5b242d59d38442297466137c2019d3<br>SHA256: b5599aa41896dfcecf4469ae234f85194f5316edd0d70326a600f7a7f6f68256</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>189.3 MiB (198.5 MB) – 3,717,075 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a298d53f2a5e3f3e1b08f904c72e7cc7<br>SHA1: 065a8020dc48d3f203491de93c4af0a07bb8031f<br>SHA256: cd7c282bcfdcdfbdec09f79c4c3f332ec687f2177fb713e94d655fd90f69182c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.0 MiB (245.3 MB) – 3,717,075 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ddee5d261d861f4acc5c45b7f83746c<br>SHA1: 86949cc920e70de8715384cbfa7b33cd89707b3b<br>SHA256: 4b46a4f5da1bd13cf2691d53c73afa6900e85009c38ceffb978e32dadb01be48</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>195.0 MiB (204.4 MB) – 3,717,075 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86a5398aa4c061c43501f587851ed86b<br>SHA1: 1c564a4db5559a6aab46c0ddf7e6577f2597a33e<br>SHA256: 61a645a16fe38c118289a3f9dbe20e508acdc35d2700f12268fc3c6d39e55632</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>201.1 MiB (210.8 MB) – 2,104,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5cd50dbd3312d7d6a58295c59daf21e<br>SHA1: d06c38acecc70ff631924ff4937069228188373d<br>SHA256: 59cf82bcf232b973ba79590713d15d5a40eb5933b8b62469d02c3f9bc56fed8d</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>204.4 MiB (214.3 MB) – 2,104,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c641b875aec20b30cca765f547fbf8cc<br>SHA1: 1c5957e2eef23dd8af844810f1d074bbec9b88a1<br>SHA256: a4468762b2277fb0286730a4fb638c5b585a19629585c77e37bd8382e0f88aa6</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>198.4 MiB (208.0 MB) – 2,104,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15b78cbbbb2658a9967f334679754b2d<br>SHA1: a2b1bbd80809646fd83466c0da5289f387544ce2<br>SHA256: 342e8ecca71f255dee1731af1d0b2b0929e21e2209295c560a4bbe8d0d9fde0f</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>199.0 MiB (208.6 MB) – 2,104,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31d6d00714b417f15e99212644b1af52<br>SHA1: 72be9c37e9fa9b329d76304065060b979865c00e<br>SHA256: 6b778c611d6c752bb94e86af0a7453a82fd588535cdf1fda893eb707df78e450</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>221.8 MiB (232.5 MB) – 2,104,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 177701b3af58d88201fe276b9ea7de30<br>SHA1: 9a5dcf7d623028feb0ce4d56797e423442cec66e<br>SHA256: 3f276d6f02f36b852b0f54543e4c0f733f3f9ede42aedf5d23666c5aa9ab3d5e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>198.5 MiB (208.1 MB) – 2,104,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a03f101b9a3d67ac7d0908f2024b1f7f<br>SHA1: 07246f908a1138cb6ded4c1f31a72ebe53449477<br>SHA256: 25ba884a48178bcfdcfd54d7bff8805b21722d3805fd3a9d53f71482661b99d6</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.1 MiB (231.8 MB) – 2,104,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d947e5d7fdc839b12ef29fa4de175a83<br>SHA1: 63deb2b8189d846a125d9a2183fc92664f1e673e<br>SHA256: 0be6425330b10e37d975089e06cacbc0dad77d16a0677f4d694a6ca0ad56ab3b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>201.4 MiB (211.2 MB) – 2,104,411 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fced12017f0988c5f23e954910c80797<br>SHA1: 0fb39bdcd785b6f1a32648aff253a1beb639d21e<br>SHA256: 7816927ff6ec1bd0bb2ec249e6ca829fbd2ceb06888a35e5b4a71c5942c1fe72</pre></details></small> |


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
