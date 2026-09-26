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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-09-25<br>IPv6: 2026-09-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.558 MiB (5.828 MB) – 278,191 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01a6d4fba4eeb2112b612afc224438cf<br>SHA1: c9400ed8020f9c878e6785bde5e1db14a0a241cb<br>SHA256: 1d3ca0e4930d5546f67dc9222b61133a864b2b27644b63d84e5b0fdb2606f3fc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.77 MiB (17.58 MB) – 254,779 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31163c0425b4ff50de66aa10d210ae39<br>SHA1: 280eff917e18ae1ad179a42104f539cfea8d06c4<br>SHA256: b474badf81ae8e98957482b43cb97e0c38ff324b89285b869ee320212da9e772</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-09-26<br>IPv6: 2026-09-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.152 MiB (9.596 MB) – 458,250 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76bb7b56cdf873703429e0d1409c3753<br>SHA1: 585bde9f14bed68bbd6a0b81188e8c769c944c44<br>SHA256: 996bf9953c438b772ac10cee55abcd09e07b66af3ab51e079ec4a84d53b270f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.063 MiB (8.455 MB) – 122,653 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ba7fa463923ccc07d481f1ad3a4cd00<br>SHA1: 559f49ca254910a582183cc5de4204e110034f22<br>SHA256: e3a0c5676393e1f7a381b89877995cd7b206eef54b9b3310e51f8978cc2320cc</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-09-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.32 MiB (12.92 MB) – 616,976 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af6d4a92763a4c2971145022c36aeb66<br>SHA1: ab8e06e3536d104b26cbf1214a1fcfaf6657da81<br>SHA256: 5a2eb2910032142abbf827c546ae277856374318745459cb7126c465cd02d7e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>62.91 MiB (65.97 MB) – 956,094 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e690b67c72b89c8ed30ac6720f953d8a<br>SHA1: 4966c2c2620a723b32f89475fd8e72f73796a3f7<br>SHA256: 016ade621e418326e269edb88fddf542560e3d43bb48f6e6c907f150704fa779</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.133 MiB (7.479 MB) – 357,311 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c47fd01af8b18cc1d5cf2004691771<br>SHA1: 6b08ac2e1f8b48e55e72f8ba6ea0079e50a1af12<br>SHA256: 63aa3454aeef9769e4f0d68b4b93b23a7d195199a50487f4db5d258d90f8b08e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.68 MiB (24.83 MB) – 359,841 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ed7b2550b03a35e3bcceffa4ff9516e<br>SHA1: 2f8880592eb4dfde0c92576fbc78417988b521fc<br>SHA256: ecd35f269cfec0024d6ea639910b54c657f3f1dc08ab339c3d0b0384ed3cb607</pre></details></small> |
| | | Full Location | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>204.7 MiB (214.7 MB) – 3,588,539 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343b463b14a760e04ccbd188e88baa4d<br>SHA1: b7e446f674922e349cb17f01c859bc3bd62fd5e3<br>SHA256: ba1847bf8c90ff7f1ab0a19c20aae3512e9bf7a3f144673fad5d87dafbf7780a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.2 MiB (449.0 MB) – 4,160,441 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2542313832b0583d31e84cd0f9afbfe8<br>SHA1: f2d167034376bc0d28d3f5a38fe3c15945c4ba61<br>SHA256: 9c2aa7d6132f5be8f547273ac5e8f21c074f3d7a26b3f7795c642f4a3b6a9693</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-09-14<br>IPv6: 2026-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.761 MiB (6.040 MB) – 288,365 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6747ad281e6d203df87a7283739262e3<br>SHA1: 90c532db8f1cce14645149b8f5cc394de42a2c96<br>SHA256: 6a9d95b18e972f327a0f7a32b7b4d33f0e33eef14e127439bb12b976b30249fa</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.80 MiB (23.91 MB) – 346,477 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1bfa9fbed82c09b5db9b5982e8b6d9a<br>SHA1: 8ce51aafdc54a7b6766d611cfafb10502b38fca4<br>SHA256: 9bc47e288cb9732ba16dbdd489323efcc7ac2a64bf0d684bc731464539bd785e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-09-14<br>IPv6: 2026-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0 MiB (179.3 MB) – 2,957,517 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dab7122ae812dd44dc6c14b6519b1f5f<br>SHA1: 10115286d4268e45b97d687718e7f7a5030498c3<br>SHA256: 9fcf166e7c6b2ce4064e5878e3c5094a10efd8718e9f3a05b0ce3206d68189e2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>304.4 MiB (319.2 MB) – 2,948,617 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 802cd20efc7238eaddac6e73d1914581<br>SHA1: a16e3bf85f8d17952c77749f9a5547179a3e0bef<br>SHA256: 3bb02a5d77da37fb74e8ab2d2e8e28be7e39f3e0486c0af2178bdaa6b3ff86a6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-09-25<br>IPv6: 2026-09-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.17 MiB (11.72 MB) – 559,467 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f8d8253bd6ff7a3c8c07f2fbdb5cef2<br>SHA1: 04391b11bc537242c022382287c76a46bd2c51b4<br>SHA256: 54794f9b2ebc8c93e7f9f929c631365c1cde08bc6dd4a787d00f56cff6a735b9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>33.09 MiB (34.70 MB) – 502,850 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e05427193a03694bdb7aeb449b5c69d<br>SHA1: a34e3eabe47f65cc5ae0959584cb2522780c29cf<br>SHA256: 615665d6df37f44f02cf7c252940f9878dafa1207c0162efb84c5e5f4345df73</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-09-25<br>IPv6: 2026-09-25 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>189.7 MiB (198.9 MB) – 3,697,261 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aba70605d677e00fdd11ed47a03a753a<br>SHA1: e698991a2b19a3da74f32d0b20a16f62d8044663<br>SHA256: dfb55a2337e89b9a671367c7ae1ea2e887bb130ee1a62a3a57e06202ff106d98</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>198.6 MiB (208.3 MB) – 3,697,261 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53898162fea7e3d94f69f96acaa05a2b<br>SHA1: 89152c7f797f4ca06372766cf71e69f03520cc36<br>SHA256: 3d9d423552df694965904941a426fa35b8f14e87af2ed5cc771cbe5fe40303de</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>188.7 MiB (197.9 MB) – 3,697,261 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9baeb441a8c1597d493397ebe356e327<br>SHA1: 17c986077cd9420ae75299a4f3b913fab7a651ba<br>SHA256: ab55fe4edd023c620c3a17bc55285faadfc16e5b0e9ab6962d703def94439b73</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>190.4 MiB (199.6 MB) – 3,697,261 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0eb39e1639be6a9968a79c0e1570999<br>SHA1: 6db4cbe41f5c02c128576a51ded44b6e5638812d<br>SHA256: be987db675ca2288201a9759cc01aae545947778b98786795aab9a7f5f7863d7</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>240.0 MiB (251.6 MB) – 3,697,261 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2f789f66a724f98b1048ecb6035ecf6<br>SHA1: 605d32e8256210a2ab2f342ab51b01f103bd73b1<br>SHA256: 17383b8035470970ee640d5520e2ff8f8ec99bb3c4df566080678edfd42157c4</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>188.2 MiB (197.4 MB) – 3,697,261 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93f274c3324afb7692c72b518af62878<br>SHA1: 57f696f4bd4dacff6b82531540f3574eae3773a4<br>SHA256: fa95bb1673a775817d4d6e9635547773256df435974042cb9422153eb1534007</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>232.6 MiB (243.9 MB) – 3,697,261 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50f2505b0cad6a9e9c98d26d2240d690<br>SHA1: 835c8512691e01cd3af4fbe0142e4abea79f72f0<br>SHA256: 80f61b8e64333881a1f80cd77e4a181a9daa521446e07505c7a34fa0fe62978f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>193.9 MiB (203.3 MB) – 3,697,261 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f435d294726e29dcd025fa2bea1aa9b<br>SHA1: ff3effeeb80bee29a91c415ee1c6c9732e7e615c<br>SHA256: ce900964b03624af104f6d9554a10ef132676d50587b16b2465753d7f8cbcfdd</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>198.7 MiB (208.4 MB) – 2,083,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5fe6fb4329e2cac83dabdb22aa896e48<br>SHA1: 5ea435c25cd8d34e952b81c77a86df0048481908<br>SHA256: a221a1bdb32e8a9da82ef99d81d3556dbfd66c4326c7756346a8249d1a928b04</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.0 MiB (211.8 MB) – 2,083,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ab92903bf43638b737b2e20ec52ce11<br>SHA1: 1e4ea84ae97f9b13757a8a6d4115b9aa09bd0994<br>SHA256: 991fa024fbe528a8dc7096a0f5986326112efdd3f854a0e02342423776b3ec25</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.1 MiB (205.6 MB) – 2,083,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de2b6e49522c223406b55e02b725846a<br>SHA1: 00c9ddd92befa36ff0f70044909a45189e44bea6<br>SHA256: a92aa5dab036e39cb80bc5c41cdc827a1f0bf19352ccc7cd362b64f0ce203ba9</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.6 MiB (206.2 MB) – 2,083,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 610dbda8f6181d1f66bbab820714fc04<br>SHA1: 757ef802dcd917f5a460908223416310ecb45178<br>SHA256: 4cfe2a09222f1003af932ed37ffa208889506cc9967c7fd91be89c585f5b686b</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>218.9 MiB (229.5 MB) – 2,083,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a8034547a7c86f28e3d14e9713bf76e<br>SHA1: 99394d21af596bf97d7af443b0fde4f25c4d66e0<br>SHA256: 724e4814457edbe4a6419429f179dc85aece33136d69751accd461e2512225c9</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.2 MiB (205.7 MB) – 2,083,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89965542806b4ad371dd3ca118f7ebe7<br>SHA1: 3825043a3b8573a3ae6d8ba5f3ad2932d32dbce2<br>SHA256: d8964e57b496f7c98470ef371262e5aa3a28bf9b6abcde1185455221bc718a02</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>218.4 MiB (229.0 MB) – 2,083,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8204431f052dbd34291fb75e54dad7ab<br>SHA1: b37754e640e48bfd763320b0349b98052ca9f630<br>SHA256: 16cef3307a20267f4abc3e16f5a9fc57ba1c5d9c06ef5314957d29bc1d54d6ae</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.0 MiB (208.7 MB) – 2,083,631 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f714f42c308b729326c5610b44904a80<br>SHA1: be402fc67f296b27f2b8f69b53d0f83de4e03dfb<br>SHA256: 068d2d92457f312af9284c84605aceb8ae53ad5f8985ac8e406def8526c56db9</pre></details></small> |


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
