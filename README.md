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

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than three days (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-11-14<br>IPv6: 2023-11-14 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.597MiB (5.869MB) – 238,419 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43da84d1bd281c3e5ae94f1f50e4fb5c<br>SHA1: 9bf8da58fde3244442d6ed5f2f058a5e291dfa14<br>SHA256: c4bde2094a4d0d237a912a07091cd2df0381367c3563d05e9093f2bb65869acb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.280MiB (6.585MB) – 81,299 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7deedb677a6bfe3338232e61450a1bf8<br>SHA1: b7752f8af6365ea5c004c566a028843b8ed61dde<br>SHA256: e854e11c81842bff02e0ee9808983d487154615495ed7cc05e5fc7958378add6</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-11-14<br>IPv6: 2023-11-14 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.620MiB (10.09MB) – 408,617 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f08e47682accfe41e09533be5624f06<br>SHA1: ea62664236e804e7c9986c6c514b787a389e066d<br>SHA256: 73f5a8f63605a1f5526b9f52809636e4692f1dc411227ad9a715f3a1bb60767b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.093MiB (8.486MB) – 104,862 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38bfa93ad54aad6d51a5055613e2c54f<br>SHA1: 7c3e05a5f9b0e478f1f89059544312b3ebd6c29f<br>SHA256: 230db31fc8ec74261580e6b0d6f410e8d316c7ddab50c4455e7a0cb4dc486bb9</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-11-14 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>20.17MiB (21.15MB) – 856,716 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d69399c53c8624fbeb058b2a15830f36<br>SHA1: 91f335caa725bb33767248c9938ac6b9c96aa00c<br>SHA256: c0a20195fb4bf591a9253f1f1625e8486b004f5c1575aa5fde2bb5b0b13b8962</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>39.70MiB (41.63MB) – 513,950 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc5aaab996a08497c84ddb6705a50b79<br>SHA1: d6bb151514227aa1076bfd2472c21c7e6e77efce<br>SHA256: 9b16cb4719def03cd2d10bafe8d1020958fae0cd283b03cc55c447b3ebc584ba</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.260MiB (7.613MB) – 309,964 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7fc3106cf6c65db7d44df8b4fb1d16<br>SHA1: 6ec97588db0af32a305835217289c32883d23f64<br>SHA256: 9bc7152bcf323316fc78e69cfa190cbddf22834208f48cee2e624c18150c9478</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.63MiB (26.88MB) – 331,798 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264a68f442d85aea134072d7bca0f4fe<br>SHA1: 65171ab00588cb7f2ae029d9345b44cccc888d24<br>SHA256: f76d40c34e6881d9cf3d98b34ced8105e9bd9efbb3f55e2bc224ece181569030</pre></details></small> |
| | | Full Location | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>186.8MiB (195.9MB) – 3,075,320 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96e5fc94ee00f3349281d3d79c8e3e83<br>SHA1: cf6b55598525f02890d9596fefd546190401adc9<br>SHA256: 5dfdabdba40afb770f6ff5afcc35db6136e9e28182bd6b3fd23b3c203dca5d1f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.3MiB (303.3MB) – 2,504,397 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bcf1dc4f4611d3e39906c6048aa8fc<br>SHA1: 2cd36733f3043bb3d9985d20fa8416a68b122e30<br>SHA256: e3d5ccb9e02dd929dc48ad40f82d484f9ffe60f9098c5a3ac296e33c5b9c2a9e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-11-14<br>IPv6: 2023-11-14 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.446MiB (5.711MB) – 232,323 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f7d79b6a3ef8bc35c3c8381e7c028<br>SHA1: cbc8e9cbd5c151f0cdb02a21e5e6fe9d8b662cc8<br>SHA256: 9f3976e09ec875d7e97185503221656e80f41f531e268da1bbf874127de2583e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.41MiB (20.36MB) – 251,316 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df2ea3be7027267ebb1947b4220cc4b<br>SHA1: e94b6a993297b5dff456113130c22e323534e39e<br>SHA256: 44458ed651d7b4bd99ad73459d500395c410da1b2fce9fbb2c4e5ce318c4bcf9</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-11-14<br>IPv6: 2023-11-14 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.3MiB (180.7MB) – 2,814,468 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25688ced507227d7990066c41a0d58d6<br>SHA1: 28da5022ff88d543bba4e15cc01b703781801bba<br>SHA256: cf219cb6d358d6e4df364a87f28817e4aaf8322370b86495ef74cc1941c73f5d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>171.4MiB (179.7MB) – 1,495,017 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d4ab0c657ede6538d2756cef356f5f<br>SHA1: c2865c0d416ae7143165db8aca21627725b4b45c<br>SHA256: 66022701ed347d75f4f400e76024ae545696e742e4c0fd30bedf981c262b318b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-11-10<br>IPv6: 2023-11-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.62MiB (11.14MB) – 453,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb7fb0ef4013b9a28021f0a480fe551c<br>SHA1: 32868d3496d456b1ddbd04bca6b1325727d1bf5f<br>SHA256: 2d895e6318c90923e43b49cd95287fc89736ffe5da8339ebf48db9c505ae6eca</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.73MiB (23.84MB) – 294,273 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 111195e9cecaec7a6ca59acbf3c0ff34<br>SHA1: 0f44a38ad0aabf8787d3a70afd55013ada02d8d6<br>SHA256: 4a670362e83e42c9394cf9dc021ad3b17f151ab738d458ea9d9b59052a10f283</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-11-10<br>IPv6: 2023-11-10 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>160.5MiB (168.3MB) – 3,180,824 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9017e5937675fc45a883e0bc570b93c4<br>SHA1: 60f300b31279929dd5bb5583d79417beabf8a735<br>SHA256: 9bdd0254806ca6b4bc64adf39699d06ee6f61e88379a2d666912071e4b8d847c</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,180,824 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d95e58c4b1bac57242939fcc12dc67<br>SHA1: 96b8e8e7d4d6c65a1905c2b8d9523d4b67482ea4<br>SHA256: e02ceb57ac20c1d285f813ac897b5c5255cff5f04a3f4f3ffd0933a872ff9cd6</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>164.5MiB (172.5MB) – 3,180,824 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edcaf872bbf96bd46acae59ca6c3e363<br>SHA1: 9376c52c4230542ec029c3dd76333a41643e6a7d<br>SHA256: ae5877065e6a1e8b380750bd998bfda15e745d9e51f56e65088d52da341cb562</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>170.5MiB (178.8MB) – 3,180,824 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0deae96671be2a3bbb757ddd46155091<br>SHA1: ab88532aa69083ed933c3fcc2b73e6e97454036f<br>SHA256: 5d720bd167736fd59c6945447538a09a4f1c6c126b00eaf06f6579a5106b83b4</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>194.6MiB (204.1MB) – 3,180,824 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89f79f2e45c508d1479cd246f2127f16<br>SHA1: e3c9fe148872762f5246f0c5a5c2fa2ec86286c6<br>SHA256: dee2dd45315a8b51d0a4d91466936471dc1ee85ee35098b8a037e819d33a8e0e</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>159.5MiB (167.2MB) – 3,180,824 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4368239c84134711ba6167f756a55bc9<br>SHA1: 281f5d04061b534656c14f56d8af2d1f2a9216ae<br>SHA256: 6c0c7bafc4822e4fd851a9a1d9eb2a481414b0ebdc270ea7aca25cba9c9e3a3f</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>196.2MiB (205.7MB) – 3,180,824 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6abd2a1fa28ba6582ff599a866eaaec2<br>SHA1: 1cd67e911392bbeb642705c8fa9fb0c9f8dd127f<br>SHA256: fb142513e06de72569a68616a8a56130b5bca59df90e2a92002577c6e0995e59</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>166.4MiB (174.4MB) – 3,180,824 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61fb738e11676f7dcece3d27c1ebbef2<br>SHA1: 2f7e100f2d1be8817b56286c4fd0da4e747f3460<br>SHA256: 0f9d4be44dc85734b44b086bb849477ffd3e3c6c5d5ebc4c848867d6493e03cf</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>123.7MiB (129.8MB) – 1,228,766 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 057e3bc0d6fcebe087cf7105aed9efa3<br>SHA1: a32b471623e1b320a6d02fe0d827a7f3ada5b046<br>SHA256: a4cd227a3df5b20d9e5485eada20706d3f42ca3b31084f62d578c2a36aaf7859</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>131.4MiB (137.8MB) – 1,228,766 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f7a6be0c92acdb9c9db50f42894468e<br>SHA1: 96d6593ccbfb94dc64f0a53b94cfa6ca40fda48f<br>SHA256: 8782c8ebffa04ae7e1f386d4fe25102cb0ad9229f6a82b9a8334ce48711fe6a3</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>125.7MiB (131.8MB) – 1,228,766 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23356a407a7c5cb8e1c015c0821cd314<br>SHA1: 7a468cecbd9fad78236f6c2d168e4fc960c97d8c<br>SHA256: 04079f53602dfc21dc39348e4591af9debd0d92caa066dedc935b42319918ab6</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>127.4MiB (133.6MB) – 1,228,766 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a19c81a452e74b35097ef1ac8ee80932<br>SHA1: 09965c29e8587ff8e35fb221e746c937e1bd78f9<br>SHA256: 65dc0e949028f1d2ef8acd20b84da63caa55bf580c4db246b18e1f33f298c5a5</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>135.0MiB (141.6MB) – 1,228,766 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99eeed679eb5901afdf1dd065061c3bf<br>SHA1: b40c8ffd408965cad094391bca7453af56013bc7<br>SHA256: 55b240a795141f955604ebf8268b6f6884bc108ad6d286326021def42c37192d</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>124.6MiB (130.6MB) – 1,228,766 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd0413f6c9a87930a55ed99c78d77d14<br>SHA1: ed0c51975d7795038bb71e5a37201b8a82a1e2ed<br>SHA256: 9fbec909c9bf4ef7d75a182bc59aa39f4d5697b8394b2222782fa79d75698aa4</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>135.3MiB (141.9MB) – 1,228,766 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef3101e00b682309af97d21e546db946<br>SHA1: b7340cb73487ea7eeda30569beaa7c87edfe9961<br>SHA256: c40e0f0b12e7391f7ebb05d18d1b35ca8aa66679ce8f1921274de51e84cc7afb</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>127.7MiB (133.9MB) – 1,228,766 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f29b01893d7c90f2327248e3f842d1a3<br>SHA1: 4acdd7ce5d977018d8f03dfe83daea568d363408<br>SHA256: 962df590ae735834ceae36249210d31ffd0b91929fe33bb61be1a7fd2e58fb04</pre></details></small> |


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
