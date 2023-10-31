[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-10-31<br>IPv6: 2023-10-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.584MiB (5.855MB) – 237,857 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6693554a4108a807d545cf2c1b0e7e7<br>SHA1: 05d3620840445a041d27831724e44d268dafd23d<br>SHA256: 48d4fbab1098572d2d1035fe13224daabf638e3fbec98c2985314ac323f7850d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.266MiB (6.570MB) – 81,110 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05484b42442a42220014908e80ced0e8<br>SHA1: 9d839af0f40772e3c2ba3c08e725f34e393be1ce<br>SHA256: 9a69629b1ae44fb14cc3a165e85b1ceba5841e79c22c7808714ae1b26ae8ada3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-10-31<br>IPv6: 2023-10-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.639MiB (10.11MB) – 409,406 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ede49245d180daf111064225154bdd5e<br>SHA1: 97e7a56d49f955ee4dbf2cf08593e82de62ca7b5<br>SHA256: 49e099a5ffda2f8640dc204b94ea9eef1c28111594f79b5bab5f14139f1d836e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.031MiB (8.421MB) – 104,064 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e1ff00982eddb7a6bc91d0cf5be0c55<br>SHA1: 34b5afcb3213f12683127cd8d0631f33927a7ceb<br>SHA256: 4bf69adb2be60e0afb0bcc9d74cab6b897d5dd66564c0fe8629f623b6bfc2e86</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-10-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>18.49MiB (19.38MB) – 786,051 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5542cb3a8fcfdd472462d5b60c2967c<br>SHA1: 34f39d3301e3070f303d9201ed65b590848c5086<br>SHA256: 3bd7cbb92ef4e37f2972da585633c7f56a633fe75318363e67d46526b2626887</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>41.49MiB (43.50MB) – 537,073 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5d3e3abf2b4e14d1e6b989a6aab2c94<br>SHA1: a6188af0b25562ef7139cdd9b6193db3afb9f694<br>SHA256: 7658c5d801866b7ee409cf7816dea1c76a2125b714beee3b74e8d94cf8cd75c6</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.207MiB (7.557MB) – 307,820 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ff8d81d8ce4efd3476359318175af0<br>SHA1: d105d1c4490b536a83d0461759256799109a17cc<br>SHA256: 4cb45f08b0bbd6d6c4fb204e776835b939ac663761aea652d12ae2ab20494228</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.54MiB (27.83MB) – 343,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3256ab7e4df24ca9917bf92c70b9ce1<br>SHA1: 832b96b707911579f91d2a42cc84b0766c5db738<br>SHA256: fdb03997e4b7c1a6bdffa274673b7756d8dbfb2ede55f1186b3957ade7042544</pre></details></small> |
| | | Full Location | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>184.9MiB (193.9MB) – 3,048,591 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed65f47a5f866d476bde81f05015d0ad<br>SHA1: b0ef2e2cdf8875da35c99816df76f9fa88d3de9e<br>SHA256: 5bca8efa9618ae69c9fe4228342c0ec4bfb4d581ca0766a3a8e45978d1fe7875</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>269.4MiB (282.5MB) – 2,345,213 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f854d9364b9ab55744dfdc557c9f9f6<br>SHA1: f419e9a0b9db7b3c78b5c98927c74c8427f3fcd0<br>SHA256: 3d1595b762a094dfd2f9ac1525dcc77a67ac87dec747f420b0fa63ac4fe51cbb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-10-31<br>IPv6: 2023-10-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.446MiB (5.711MB) – 232,323 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f7d79b6a3ef8bc35c3c8381e7c028<br>SHA1: cbc8e9cbd5c151f0cdb02a21e5e6fe9d8b662cc8<br>SHA256: 9f3976e09ec875d7e97185503221656e80f41f531e268da1bbf874127de2583e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.41MiB (20.36MB) – 251,316 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df2ea3be7027267ebb1947b4220cc4b<br>SHA1: e94b6a993297b5dff456113130c22e323534e39e<br>SHA256: 44458ed651d7b4bd99ad73459d500395c410da1b2fce9fbb2c4e5ce318c4bcf9</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-10-31<br>IPv6: 2023-10-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.3MiB (180.7MB) – 2,814,468 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25688ced507227d7990066c41a0d58d6<br>SHA1: 28da5022ff88d543bba4e15cc01b703781801bba<br>SHA256: cf219cb6d358d6e4df364a87f28817e4aaf8322370b86495ef74cc1941c73f5d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>171.4MiB (179.7MB) – 1,495,017 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d4ab0c657ede6538d2756cef356f5f<br>SHA1: c2865c0d416ae7143165db8aca21627725b4b45c<br>SHA256: 66022701ed347d75f4f400e76024ae545696e742e4c0fd30bedf981c262b318b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-10-27<br>IPv6: 2023-10-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.59MiB (11.11MB) – 452,125 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee9b88ca3a6324ebc889a04ced4fb3e1<br>SHA1: 0556f063a0ff5c19984a502150dc6332e66e264f<br>SHA256: 4d658011592a8725c02c2094bea94ee4f7cc66ac897fd88f4514dd01641abaa4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.38MiB (23.46MB) – 289,669 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e6027aa30df6be243d88b2136de674a<br>SHA1: 2d1118200ad114fddbae99c80ed7c3aa35d48834<br>SHA256: 26fd32df2a01e886e317f5aa2a1f6ddcfe79700266b220f62a42cb0b775de7fd</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-10-27<br>IPv6: 2023-10-27 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>158.3MiB (166.0MB) – 3,141,279 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 393742bbfa66e07165e598dd9d865f9d<br>SHA1: 08294c3f6a5ba956bbc645ad935c1e34cd9aec79<br>SHA256: fc42bbdd5bad5240db4ce8fa681f26fba002ccfa01458687000a9a5030daed19</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>183.1MiB (192.0MB) – 3,141,279 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69a9a93399200ca80f02b2bd02aaa48e<br>SHA1: bffb3fbc0060b1d85eef009b17d1c53c657ab664<br>SHA256: ac5a2369980c3efe5fb84658cd7b9aa56e23def34853e2c28fe831ec8ab6c3d8</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>162.3MiB (170.2MB) – 3,141,279 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23081d4b81b76bcbcc49b1ecf92d3168<br>SHA1: 2c12a9126981c7690569d2a36e43ab15ffab8235<br>SHA256: e82717e35bd8c48f21725f7a929d24990b825418b67ccb0316ebb63010b95d3e</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>168.3MiB (176.5MB) – 3,141,279 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 798a618f78dec9555f5f6736f1b511af<br>SHA1: 61f2120d4e25b7cd6aad3de15f7a3dff5d706284<br>SHA256: 4e5e18b4a2a2b41dc93c685a8ba940fe79c2138580bcd8900638b58e926ed775</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>191.8MiB (201.1MB) – 3,141,279 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 619a868cfc5bc989df5fd1cb500e9f56<br>SHA1: 89c998ce9a7a6441f3e34df2d45da69a0ab240a2<br>SHA256: 02c624f95f0698ca81d8571f5e824efa629c4a3217cba46108fc5e798405e839</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>157.3MiB (165.0MB) – 3,141,279 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fcd092aede8a6b516119d42d47da2b6<br>SHA1: 5114f577ed15f8d4d821115bb58c15a1f5dca8ee<br>SHA256: 88b614171699fcb105b3b652f68cc532f5eeb00c55a8cca37035dc68e875a8d0</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>193.3MiB (202.7MB) – 3,141,279 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 885a9aff65fbe294120066240efaea29<br>SHA1: e900421d2c4ebec687ca9f3838cd24d6f01705a2<br>SHA256: 2517b9974ddbd6a5e1660473ba74009ef9f17a54a869d1387449b50ccf790122</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>164.0MiB (172.0MB) – 3,141,279 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76af17405a77f983d4651448dec4fbd6<br>SHA1: 77f03c3aaf641156c1540f3f615e5a8ea8500662<br>SHA256: c8f77b7dbe1ea39d3ff7e7e96c5bbb04481075c64d548da26b00541e4979de5a</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>121.7MiB (127.6MB) – 1,209,107 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44a032d82f2369cbb8c7bedbeba9ca8d<br>SHA1: f2ce7a2ca63e90881ef2cf6112f8cfaa566e2c11<br>SHA256: 4cc00aa3c7d47f0705b6acf4b842674d890cacd368007c4875a016cc182f8000</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>129.2MiB (135.5MB) – 1,209,107 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 990b83af137a0bf7648adf90bad3dd11<br>SHA1: 1e76e1bd3bc1a821b37f2873d5218e3226028661<br>SHA256: 1be5e37347eb18897b80e936496c46a2d32276ea6c0d37e2825459a2ec984202</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>123.6MiB (129.6MB) – 1,209,107 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61897b12069ec27a1e4bb32ef9fb690a<br>SHA1: aa65e4697602a776c6fab56c4129043e44b815e4<br>SHA256: 0631ee97c0c686716b8e8e857c957cc5ef07490a16dd39e1f0a626d747408918</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>125.3MiB (131.4MB) – 1,209,107 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a73418dba4cedaa6c5e330070b263e20<br>SHA1: d3b60138f641d07ecb02410da5b1ec7d710177e0<br>SHA256: 4af5a6628bdcb941fb90b4308794e3f76c05398b79908ed05dc03203d1d6736a</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>132.9MiB (139.3MB) – 1,209,107 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e735883ff1a5bd37771ce873d8d4bd1<br>SHA1: 2862483eae04c9b22ef6200812d03bfde61e4006<br>SHA256: 315fc58d8aaeb204f816c0c1618f8c9cafe554d3c55c11499a1e72d7f344cc35</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>122.6MiB (128.5MB) – 1,209,107 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cc5297f090e82cd078f59a78c61aba6<br>SHA1: 0b215e03addb97011bfea948cdf9361efaee8180<br>SHA256: 142ffcbcb3ef25e4bbf4d072a4e648bd77f7b43cc0011ee168c010183ede7eac</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>133.2MiB (139.7MB) – 1,209,107 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fd765b28bccaef28c532cb541ff1a63<br>SHA1: 5291fb307f57e65c94d69efe4375a803157e3acb<br>SHA256: 45db3918a1f2c740e956c2500d65b6aba962ba94fcc8fe6b148672966e9987f2</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>125.7MiB (131.8MB) – 1,209,107 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd2681a3015a691f19a16b40c563ec73<br>SHA1: e85fde281f62f97cafe5042f623a3c386c416cb3<br>SHA256: 42d085f43f9d7e9fd1b08f2d5644308cabcb3b78654f260a5238cf5fc8003d2e</pre></details></small> |


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
	* Store the IP addresses in hex format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
