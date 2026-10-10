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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-10<br>IPv6: 2026-10-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.635 MiB (5.908 MB) – 282,014 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0da07ab452b10a75c13d3d70a3b93791<br>SHA1: 291ed5ad56590e70f633a4b527a93d909af04c6e<br>SHA256: 6101db2871d86df3f5690569ea17dc00e5606564280f2e58e1ebb46753773eb3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.35 MiB (18.20 MB) – 263,704 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c850cfce3fdec5e94f69ce947b3db71<br>SHA1: aad388a5a09d3694d02c827c0dca11aee7659138<br>SHA256: 8fcc938b210bdb15dae89fae70d5dfa91f500ae02f0fafb09a03613c4250f6a4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-10<br>IPv6: 2026-10-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.166 MiB (9.612 MB) – 459,000 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9be377c40f7bec90be3716f66f54f697<br>SHA1: 97605f12e79800a4ee4a8490b0b7abd7ac987c4a<br>SHA256: ce9e343c279f3c661d65666d27e5fd95aa191de42a339916a851ef717a1909cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.109 MiB (8.503 MB) – 123,339 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 026ed26247df109bdb92479c1b3ef79b<br>SHA1: 220c4d424a3379dc236ad44a6c02a522498ae22d<br>SHA256: feed422305b35bcd6ad68d1311e06c017e5e25711d6542995accf5357f0c651a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.30 MiB (12.90 MB) – 615,759 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56de47958ab0164f2011d3ca0ae1d08c<br>SHA1: 796690a3b6dca1807d42c22a19da88b621403e39<br>SHA256: 43d234dd78d06d56588bafe8baacab818660802861180ec4ab78ec86a31a797a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>68.51 MiB (71.84 MB) – 1,041,158 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efed889467fe7b3735e6e1e646163411<br>SHA1: f94ab6ae353241c0874cc55a2864740a5d3ddd33<br>SHA256: 9df82feebb58379c1307699d24773ad63caec1b0bf1dcf9b08ea36cb954d9ec8</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-09-30<br>IPv6: 2026-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.778 MiB (6.059 MB) – 289,240 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 037cbe9e49d48b0386b4034c7048c166<br>SHA1: 8c73a34d6c47e79b0badefc8537eed6ecf22a1ff<br>SHA256: ee638c1c30f847a38cdca18fb3e6e1a2eb2df7ad320e6337d67810c3bab16fb9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.89 MiB (24.00 MB) – 347,830 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4516b087eb6d889360de69e0e36656c<br>SHA1: a1976e56a08064be5a24f8e5c28ffb07262b4716<br>SHA256: 4e0d0b9bdcd967472b7f36cf1465613f3e2211b91a422044355cac7646b8c6b2</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-09-30<br>IPv6: 2026-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0 MiB (179.3 MB) – 2,956,846 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a313f9fc27ba37b673b099489446886a<br>SHA1: ece362877a757aed6d6ccdad1bf2fbcb4031e9f6<br>SHA256: d7ef0d3ca1e2b8198a0e007e322d5c964611e1ed6f900d9d2edeffda292f2aba</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>304.3 MiB (319.1 MB) – 2,947,358 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ef9a15cb810aba175baeb46886eec39<br>SHA1: a8a32cdd1c882bab942deeb72f2c8da534c8bfdb<br>SHA256: da31230883dbafd4f2ec3e54d86964a6ec028cfbcf767d5e30d1552eff280d33</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-09<br>IPv6: 2026-10-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.26 MiB (11.81 MB) – 564,059 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 836158a019975c8c088a518665505f41<br>SHA1: d0a9888290b30189eae9b17f23a13254c70da1f7<br>SHA256: bf327903ae3c03b90ac42548d98e4ceeb9b1cf4cde8728bb9dc0a8ad2aa02e6c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>33.06 MiB (34.66 MB) – 502,384 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f63dacebc225cb269d750660533c3f6<br>SHA1: 74b5b9381361b0afeb345517a461400f7ac008a2<br>SHA256: 08af512420caa4bbcdc6a545558585a234f86426964fab9492ecd6afa1c4ee08</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-09<br>IPv6: 2026-10-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>187.8 MiB (197.0 MB) – 3,662,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7664b57af361a8230a84f8ecb212dfe3<br>SHA1: 4395ff7954b3ab29cc62238d582daa5a94649a12<br>SHA256: 3cc7067739cd45b4af17fcc993a4b78bf162c001bbdcbcbfe95da26c2e9c7e4e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>196.5 MiB (206.1 MB) – 3,662,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a42a5e9ef0124b0fa7344f3e94d69554<br>SHA1: e77d38cb634a4ebc286f201b82eb1157e07c6ca9<br>SHA256: 14d4f3c16312a6c085322dae5d4d52ee43df6c6118a34f854becbb67e94dcdeb</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>186.9 MiB (196.0 MB) – 3,662,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1868ff87d1434480c258b4954976b47<br>SHA1: 538b8ec4a29207ee22927590a5ec672435646915<br>SHA256: fe8904f633ba5e74388340f0fe3d9bbaf10267839a6d7768ca12020d15b1c327</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>188.5 MiB (197.6 MB) – 3,662,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af7d5c4ed3e35be4c4d65214d44ea451<br>SHA1: 9f9c8db567e16a68c8e1f34656abc07aea19ca75<br>SHA256: d94f94bab6dc3e54815757c7d8568353153e11aaaeed64362477840c555036a9</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>237.5 MiB (249.0 MB) – 3,662,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2f7447e6552bb1d27343b550db0493c<br>SHA1: 4e6f85ca90ad817e08a012fba0b175fa73201f46<br>SHA256: 5591773453053528951defb036e23cd9ab156c5f459906c3c0bc420a153e71b5</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.4 MiB (195.4 MB) – 3,662,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba059b1a604b868e7ebe789cb2c756ee<br>SHA1: 90889d779c80d105f102c9c55a6a2644c47bc2c3<br>SHA256: 5d32012ffb8dc4a616d7bcb89b84b4dd53caaa8eeee37d553c2db5edc4655991</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.0 MiB (246.4 MB) – 3,662,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 294da52f07df2294aa923f00b8712f0f<br>SHA1: 1563c276265ea5792256770b7215e051b517a78e<br>SHA256: 069461e7b74c3d919d916e866930525aa50d98ffbcd367cd65fdbe217deb7dbf</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>192.1 MiB (201.4 MB) – 3,662,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b4ea5cef4b6d6cf14a7e3c7489d0884<br>SHA1: af4794eea00d7ca919706f7cd448f24883eb3c68<br>SHA256: 2084b2425f6e0d1979330a25bf1676ddf915dea391b48db5b15b8ad9e5817aed</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>198.8 MiB (208.4 MB) – 2,082,705 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df4b4d56ffb859470f6d54f885189e81<br>SHA1: c40dcecbae1d38212c0ce802493af8c82940da81<br>SHA256: 173be8ee02b63266bd6368cce88851f73b2b23f37ffe664bd16e6f6796930747</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.1 MiB (211.9 MB) – 2,082,705 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6dc85fff4b4d483a7d7f8a267dfab9c4<br>SHA1: 4b558427c0cbd1e4f5be72663700c17f3a0f9a26<br>SHA256: 6d1c5f59424954c0a75f24e45141c5d32c79c689a1a0918dccb07b139899495a</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.2 MiB (205.7 MB) – 2,082,705 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dbe66cfd8d69ce85d5321284ba13d99<br>SHA1: 82c3486666c2f1bf86d23f5f41841fa8b079fb1b<br>SHA256: e39f26dd60b05f13716ea61296a76e19ab092bc6093bbf98e23b6fbe51dbf5ca</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.6 MiB (206.2 MB) – 2,082,705 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5cfdc576e63d96e4a1851983643a4719<br>SHA1: f053f6aa66e1a1478108e8f8b5423b77a4299818<br>SHA256: bf2ddbccc4a12e69b59e9319bde6244437b75d29843e10a5014f9e265947dfdb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>218.8 MiB (229.4 MB) – 2,082,705 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c422d9c994534e0f0079e6810b4ac41<br>SHA1: 7cdcbcb30820f0cf4eeb6b88c314e486025d8391<br>SHA256: 4aeb0c41e77effb842db05f4918d12088a183f53d08698b7266e662efffc3211</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.1 MiB (205.7 MB) – 2,082,705 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8186b8426e31b5963f8f8ad8ef3fc9c0<br>SHA1: eb188e47cd04f3ce4332f15790d67010a177d2cf<br>SHA256: d6876d296c25644a67b36e0245b018aab176e75403919da53b0652eafa540bb8</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.1 MiB (231.8 MB) – 2,082,705 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32a75e961741cbd9c6754c86f7371a42<br>SHA1: 895deeed5668fa2cf30c42db0def7898b7d69cd1<br>SHA256: dfca927df8514311f61c92c62de96f3451af64d6addd240f26de4d2a23b9e03c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.1 MiB (208.8 MB) – 2,082,705 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 137966abedc15a09f2634ebd5f062948<br>SHA1: 83dacfcb41cc07ee50f7b8e20a8d4916de92b4ff<br>SHA256: 226352c7914c7370c51827d16af303844bf7e01bd235e0b7d16706194023dcd5</pre></details></small> |


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
