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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-09<br>IPv6: 2025-07-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.317MiB (6.624MB) – 316,346 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4d6a77f465df0978e5c2dd86024a26a<br>SHA1: 6afc3d51e7801ac5a168d16105bc8203ece49250<br>SHA256: 6260208376e464f857f7d7cee85e82013624ddfa7389d72da14ca34a4e394a1f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.27MiB (12.87MB) – 186,459 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91797198c53a89b0f2fad6b24e60a012<br>SHA1: a6748fc3fbf0887578b078a6fdeec52985a30132<br>SHA256: 952390539fbd2587803738ceed1a3def72d3416451b47ec0e492c29a7928034f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.13MiB (12.72MB) – 607,069 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc854e4e4e9f23e69d497dd0d672b541<br>SHA1: 363fb5529dcfd997e12f5b0282f7716168980112<br>SHA256: 5c1a435eb8df375fb5d9c0124d950fc5a8bfbf25e8eb7eb28e3c32b254f9ded1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.89MiB (94.26MB) – 1,366,070 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcffee4e07aba7877fed00fc9d9b21d1<br>SHA1: 08212ccb75ac9b7b5d59a4f88bf2f250217af99f<br>SHA256: 00bcb219501fd35355aa950cd8e8ac38154c40d8c242cf65f764a7b76e580779</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-09<br>IPv6: 2025-07-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.057MiB (5.303MB) – 253,125 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95ffb525ccf7554fce3b883e3c3e03dc<br>SHA1: cfd2058bddb8335014ef0155af9287eb4eb032a5<br>SHA256: 7f2d0669907805f467ba557b3f8a89f0cc365fe47fd8d2d06b459ef043b58cac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.80MiB (22.86MB) – 331,362 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba9c525bb7d6b096e7d2a8892fad8109<br>SHA1: 51c5aa6639dc0b1ba9137e7681566659089d3e9d<br>SHA256: 055c98ab2c55b531af78c6adefcb75267c71f317deda1d0e11cd3a5379f8eb41</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-09<br>IPv6: 2025-07-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.1MiB (174.2MB) – 2,881,364 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 857f03de59f847ebc914de35a0261594<br>SHA1: a8eb10b3a834af6faabde77d1402f59045791a92<br>SHA256: 4de98758f7a7f36de44db1501aae76db758f5a29bc7d70a9c2dad3a025af32df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>269.8MiB (282.9MB) – 2,614,886 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cf5e97154e6ed02edf8b16bd1ea2891<br>SHA1: c33d58815af98fa41a92decd4ae34875ecc10ccb<br>SHA256: 89eb5c59f64873edf5e3369de45be94f934ea8219710777955f08a65ad9b49fa</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-08<br>IPv6: 2025-07-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.51MiB (13.12MB) – 626,386 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27fa88e2c27e1e204c76111641bde8db<br>SHA1: 517f01d01358a72bdb78fa682bb474a19512b55e<br>SHA256: 6b24f330829ac56e8518f20c788db4f811e7173ecc65efa8bfe7072d4531c40b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.08MiB (45.18MB) – 654,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 469cd6a3c389fac10d4c9d28e35e1925<br>SHA1: a690b711a9ed6f45bb99a413293e6f6951532cb4<br>SHA256: 2582448c8acb09d40f0235f259548aa439623774ab0ecba31f9aa2fec7bf525b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-08<br>IPv6: 2025-07-08 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.9MiB (182.3MB) – 3,429,868 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 370ddd51d9944a590e3312b61e0e2b82<br>SHA1: 6935948b4202512ca2725760f255d4579462b462<br>SHA256: cf49870eb418854c4ad268eb2ea78e6846d22456fc7ca168b4060daded7bc4fa</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.8MiB (193.7MB) – 3,429,868 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e446136ed84f580bfe823953515e3c5<br>SHA1: 5a10fc85919a301c0abfd174e4f1192059a586d8<br>SHA256: 3d94332fbc6ec8721b2d9c6048bbaedd3ae1c7c8a498cd09afdda909413b0023</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>173.1MiB (181.5MB) – 3,429,868 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6633a22a0e83a23d6273e281b0f9e5f<br>SHA1: 75017a330b35890f6165904538c22fae685d09e3<br>SHA256: dbbd079b0f2fe91e71f5ccd3d1ad004fef3e03785d6c8da21024364fa822fa8e</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.6MiB (184.1MB) – 3,429,868 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fffe7366592fc27b6bf1faaac9db85c3<br>SHA1: 716bcc2479487d82c91e42c06d20300865ffe243<br>SHA256: d7cf2884ed54f7b524aced81ecdf8075073d2bce6aa71458b7b0db7dc82b1c23</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.1MiB (230.8MB) – 3,429,868 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc9827df6bfb837c87954d33591840f5<br>SHA1: 77ca0e6b9aa48349c811e8a01daa8f459c23f156<br>SHA256: d65cc59670adb1c1cde0974767c897df71e1846f2c8864485d4728ec7f8d529e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.6MiB (181.0MB) – 3,429,868 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffcd374cb944fb6bd86122daf53ca3d1<br>SHA1: 829e2569f4ce8a0ad10da25480dd10422b8daf32<br>SHA256: 071f76b2e6d7c7028bd65668cee1b4ad15b80b2a9f98520bd750cd6cb936ec6c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.9MiB (224.3MB) – 3,429,868 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 252318d11377959076087b6021e18b74<br>SHA1: f1f55a1fc757c919d25b7f91a2c0d50ea05358db<br>SHA256: 7572b02db3ec79ce0c6af1b368f917c8dadfb85cbf70844bc339b4e9cb80a47b</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.9MiB (188.7MB) – 3,429,868 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7643c941897ba77ad521122c5e826b6<br>SHA1: ea7c5ace621073462edb0546d0e7d5d8696da8c4<br>SHA256: 8d88c5a03c1f7d8fc6d6d39dabbf3653dadb9deb0de24aa66469f63636117aa2</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>181.5MiB (190.4MB) – 1,925,256 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06d393cb85090dafe0702775ecadbeaa<br>SHA1: a4e8363dc45913523cf9cd0818739c40efc1e1c1<br>SHA256: 3988456baed73262d7204be0ebdc4fd20a8eac6d307190f2ae4b49d31e7e12a1</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>185.6MiB (194.6MB) – 1,925,256 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3cca91f8661d0b2c350af7c203240694<br>SHA1: 5082cd4a517220e514e311e60f35dbf41817d058<br>SHA256: 786578f21c27cd01a69bc796517065de0c082468196928a4cd0e5d13f63b17d3</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>179.7MiB (188.5MB) – 1,925,256 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14ba1bddd96ae24ed2131d1778443f43<br>SHA1: 0e253fc8a80e660490c7103790eabc94cc3af811<br>SHA256: ca3a42664f33024aa16ae747d8430cb339f0b78eb27baabc0a9910d26a878f6e</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>180.0MiB (188.8MB) – 1,925,256 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f993eed9fc1393b6825f4c847101539<br>SHA1: bbc5d3076d0c0db4abb67c9779f8b63e8561ce82<br>SHA256: b2e78fc279d16f3730875795b43325987af54681f4053b126c26d9f45976f991</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>199.3MiB (209.0MB) – 1,925,256 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de9c28dc64af9ba2461e8c82aeda07b2<br>SHA1: db5c38146a23687f2fe202e495720c02604549bc<br>SHA256: fbc419e9d8e75881000158f1f587a289aec4041d6e1b5260afa9204c9d979139</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>179.4MiB (188.2MB) – 1,925,256 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69a6f4d6d234c8e226c615eea318ebee<br>SHA1: baabb9cd96e8c7ed996e6c25f319d7c0a80f3566<br>SHA256: 8a5be870b549d621a99179c7b55d4a77034216b6fa8ac63d6786ae766af2e341</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>200.0MiB (209.7MB) – 1,925,256 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1db50960dd1467a50ee1b660127bf6b1<br>SHA1: 21014b9ab4c44dbd292b5b9f02421b2733aeb1a7<br>SHA256: db8cfc934899b6537650b98394db908cea2ab40194efc9a98cf10f9484b7fe5a</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>183.6MiB (192.5MB) – 1,925,256 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1988a11a9ddaa9482618618891e7a61b<br>SHA1: 1b26723b052c716055b8ca44f7dab97c44f3fb2d<br>SHA256: e8b4830fcd62a57fb1d534d550efdef63d58336f7a899cec9bd055fce4f43a5e</pre></details></small> |


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
