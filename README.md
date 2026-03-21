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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-03-21<br>IPv6: 2026-03-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.476MiB (6.790MB) – 324,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ccc41421f8736d052c3726e8b03979f<br>SHA1: 2d070333c42cf3dd7d123ad92e5b2404e1990bf5<br>SHA256: 141732d88a144c975375130b0630a402262d87c269be99d489ad83493b7b2e2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.47MiB (16.22MB) – 235,139 rows – 257 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 085565cdb39b3570b7c0313223620b9c<br>SHA1: e336c82ff262ace115ee3a4fef2e948b6b990eda<br>SHA256: dfe44bf2f6e0f5f384afa0e1fd458bcef41f41e81a6af16345b3a605b597b962</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-03-21<br>IPv6: 2026-03-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.824MiB (9.253MB) – 441,857 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58756fb626f108418a0011229a1bf268<br>SHA1: 879f875e4c2e2fab1693f31e69de7f80d35854a9<br>SHA256: 2176502711351213cd41136d217a6f3003d899457be4e3cb86b619791df95232</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.680MiB (8.053MB) – 116,819 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 069080cba393ebc9ccf9d4d6153041be<br>SHA1: 3940b694c9cbf44ee735e5028bde0cfa56f2d034<br>SHA256: 0d052d6cb94394d07cabe122eaa91a749841f7730e8a43beba9a2456491a9826</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-03-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.33MiB (12.93MB) – 617,352 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16c9043a1e5ffe615e8a4134da43877c<br>SHA1: 0a3297b7a30f97879ef60c231ca0b05792af13a9<br>SHA256: 1be38df676ab6a6d26ba38947bc33dfa480fcad5ee445079d1d8ab57e247d6ba</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.24MiB (93.57MB) – 1,356,104 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40cfd7065880b4ac0163b1b11aaf127a<br>SHA1: 9bb50a42338aebd9c883f4ee79e269bf9fbc3e52<br>SHA256: 9fff9987334582a8148e7279de9d35f482a4dd7ae260ccf80ac8893802f34930</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.906MiB (7.241MB) – 345,970 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be67480ebe04792eaa1e993732e26bbc<br>SHA1: b9c086649cbd7a697ce8b1a6f1200cf343683838<br>SHA256: 97e3ba0306a918694a1abd35fb0fbe18e3275c023a00d3f378bb52d0381e6ca4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.48MiB (17.29MB) – 250,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614f4ebb16bfdb3cd44828a77fb774d9<br>SHA1: be56f3e3114c6c18c1b7e097bb867772c72bf90a<br>SHA256: babfcc027ee9656b7ebe280a391c73174b4990721bda2e7c584c23450f4c5452</pre></details></small> |
| | | Full Location | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.5MiB (222.8MB) – 3,723,444 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d34e3013a398743fdc3bdbd816dba48<br>SHA1: 4f4868afd37a86dcd98f0ff21e863db08c4c69b8<br>SHA256: d805d064a2ceaeb75e8ee847780d1dcf8f54852ffa98bc007b0894fd1c1d24d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>446.9MiB (468.6MB) – 4,345,257 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b0322dcdc11f95be5a5b01f4221151<br>SHA1: 5bcecfc1d1a51db165a9a209bc8f4b9a5e7e1bda<br>SHA256: 9a67a943e4fadd058173607911c45bce627c5fbebc2abef2f229894d2e8fc57d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.419MiB (5.682MB) – 271,203 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c176ca445d23383a4c5e1e2ebd9e541<br>SHA1: d9049c5c5fbb465dca6e199246fc0f4419435e17<br>SHA256: c56f984490695ab20d84eadbfd37f601c78de75f4958c1d1ee5927482ffa66cd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.22MiB (23.30MB) – 337,655 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c07180576fcf598a4054e35c7eca4e61<br>SHA1: fa9ee16f19dba3851f20083872d13d4acbc065ca<br>SHA256: 8e65ba7778f59ef63c1a8df94112a447927b3896dbadb00d080914b5ea37167f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-03-14<br>IPv6: 2026-03-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.6MiB (174.7MB) – 2,881,763 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1614bd25a28d2b44922c3116279f804<br>SHA1: d2cd1e423c13e941548d01a453978c165e423b8b<br>SHA256: 8486e52f22f5c609925e25d4d0d4e74ae714d31b8ee7067d87a99f951d8352c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>298.4MiB (312.9MB) – 2,892,579 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85c1923ae57109129fbe714df2b92c0c<br>SHA1: 846479cc0828f79ca640a39a279ddc2fc7b8aa2b<br>SHA256: 1759b2d35ec83b135771dbe6a08ae383efaa2981f42a80b1dcd3ee4ffa98633a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-03-20<br>IPv6: 2026-03-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.98MiB (12.56MB) – 599,572 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 271a873dbc4ca4878f98fa46ab140042<br>SHA1: e74cb111f66b94044c6047415de7d5a410059b98<br>SHA256: e9d53dd96dcfd05a332ca2451e11b91e1048beae20ab7753bd4b4c758f0b85dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.53MiB (43.55MB) – 631,129 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1833b28e51292ad39525c6f1e1366c54<br>SHA1: 296e028bfb8b4edcac09734940c49cc926572e13<br>SHA256: 2f35ef5114c53bd120bc83b1a5580805976299e81b392c2a04a82938817a4c1f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-03-20<br>IPv6: 2026-03-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,536,212 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8c0466097d20b425fe3f8e9fcea2a4a<br>SHA1: 151dfdb07318c4b6f0d7d90f6f664c80d88f93b5<br>SHA256: 4ccdc685b19c3ef15531ac7330ae0c9820732ebf5f45ac1ffcf7254083457fdf</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.0MiB (199.2MB) – 3,536,212 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d927e18ee1bf442120488bb1d36f7223<br>SHA1: 8bf71c6f15c57896c48626a605ef8dc52cfc155f<br>SHA256: 2ab1cea9803765e00ef06826660cd99a152286663ca5fbab8831f58645a73f16</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.2MiB (186.8MB) – 3,536,212 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 442adb18646b0b6db89807dbef380b2a<br>SHA1: 0594f72dec1917f1e18de4809959b4d7cdcf1155<br>SHA256: bf4432a6b65a30d02447ffce5fee6285ea1318687c242245e27a3264f2617c11</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.0MiB (189.8MB) – 3,536,212 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 044f29d555536ccf2d13f81e1a19f09d<br>SHA1: 1aa6b369f48ea8b84443963710ea0eb4b7529579<br>SHA256: ae6dd13403a62b67f363b2b2e7725c69260f29334c51d6f6185d23da6a5857d2</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.7MiB (236.6MB) – 3,536,212 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1573a6c7490d05aab7844819ff86c0b<br>SHA1: abdabbcf00ced600c9dbb962eb6309a93303d446<br>SHA256: 96809c18499a2850f441a762eef2034f60526b814d66a97a45be5f55ad1ad777</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.7MiB (186.3MB) – 3,536,212 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14333e458ab3a328dbfcf7b5d59a5d8c<br>SHA1: 50ab9f18feca75e5060ed6c8ef1e56a5935c1f50<br>SHA256: a7d41aed0432057a43de1293632f40b797940869008a1aae27dea18a807492d3</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.8MiB (230.5MB) – 3,536,212 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f18d64e9f0d2357de796453699456c0f<br>SHA1: b1531c131e4edda165950e5dddfc6041f768d879<br>SHA256: 7fc7bc8736caf8a6076b6e306938d48b31a6a346d7ac6643b83eba65f1d9552c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.0MiB (193.9MB) – 3,536,212 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0906d3f8793dee815e9585fa5b2e407c<br>SHA1: a67677dabea04c58a38034c62187389b157ff103<br>SHA256: dc6224bf1b171a2ae11acd2b1903ee4bc81d21d1b8215cbea54a5b9a3c5466eb</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.1MiB (196.2MB) – 1,972,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d46b5f157a028ae9a76f3c0d82ad92d<br>SHA1: 245cf00d0e7c23a3ad5ed1e6a242a904d647b6a8<br>SHA256: 9d3fee5ac7ba751472e903f9c291600e7a36518da0f5eeaa11709e73808b7061</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.4MiB (200.7MB) – 1,972,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e74e57b2c714bcbe35ad09c87bf012c<br>SHA1: 6d53ded50cbe7eeb593d2ade2bb1f642f58d4b77<br>SHA256: 1c472707df9ede93cc73e2a7032553daa21b1595fc5616cd446ee68ea47cb173</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.8MiB (193.8MB) – 1,972,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 725307a811af20fabb4834624f97d0f8<br>SHA1: d6603ee5d0b331118a951d6760835211af008053<br>SHA256: f4018bca788b9d3996f95c9e8fefeccb9dcb0219892c0e4d7008856cf57503dd</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.6MiB (194.6MB) – 1,972,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9caf783c9a5d74e20dec9eedc97d64cf<br>SHA1: 4b1d4cbfba28bcdf1bcbe073900239a08df1e3b4<br>SHA256: 8c9db17726996e4f4fd8b0a7a89dc9ccc36a6e9a3421c51c57ccc6f7700f1914</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.6MiB (215.6MB) – 1,972,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 611911637aa41fa134c300ebfc2db5a6<br>SHA1: d5c206354b01977b7acb440e5dc635ce8671d507<br>SHA256: fba3fe99f115a972f1e4a0908b674c8b0cd7c81a3547ef15a57bda74af1ca7ab</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.6MiB (193.6MB) – 1,972,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e21b8bc9b8e110b9585f31507ba8a54d<br>SHA1: fa93e0b33f705a5bf7024d67ac77a8cbdb85f4da<br>SHA256: eb094e10f0dad88c0dd139d5db9345e10096bc0fd4a907ef0ffdc02e65ad8abe</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.5MiB (215.4MB) – 1,972,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8474309de25d052e8c2de0559240548<br>SHA1: 5f6710860518eccb180e4cf2ea533270c11ab5ef<br>SHA256: 3d3ae2caa90975d9fef884bdb409a598d1bf8b83d189f55765f2c6af47aca967</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.2MiB (197.3MB) – 1,972,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e302757a0548e7532e8b84b5d9c36d68<br>SHA1: 6780bad1946bb64814a9431d9e8300acae465523<br>SHA256: 6f182607c1794022868b8b94c0d40eb7471335bc60c6deaf2b76e17c7a99bb66</pre></details></small> |


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
