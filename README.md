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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-08-23<br>IPv6: 2026-08-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.466 MiB (5.731 MB) – 273,550 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d0c711c2e4752ab7e7b4324f22fec18<br>SHA1: 2cc777eff29bfcac75869c6819730543332cce5b<br>SHA256: 53420006a84fca364e55339203bd2258316e96bec4178243fc2f17aae8523e28</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.57 MiB (17.38 MB) – 251,829 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20f7eec40c8c98f27faece10fae1f6b7<br>SHA1: c438461bc183b61819ec8b3238d4afe756edf810<br>SHA256: 89ad9e1c87e58a6beac2614e3c825dcff6c8767e36c9e891ee837286151bbf6c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-08-24<br>IPv6: 2026-08-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.066 MiB (9.506 MB) – 453,928 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5e4fa20e936c0db2722460fd473c115<br>SHA1: f70804611809daaf52c663978152777b1e5783c6<br>SHA256: 22249c9aedbf38df00b02be124080d5b7338bab08ce2cb5b254ecf583b670720</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.056 MiB (8.448 MB) – 122,545 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc02a116e947662ba529e14283a1b7c3<br>SHA1: 9322ee3eb550592fbde3837f5fd842ab493802f4<br>SHA256: 7d822a3477f7b1920b040f3e6638d8804d29212ea417110fbf45d0c5a442a7b9</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-08-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.18 MiB (12.77 MB) – 609,782 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2e7ad7d62d0835b66033e268389cc13<br>SHA1: 957c478a6bdfd6a2169841ff444965f02d607f45<br>SHA256: ec7ad2ce6777035ea0009a6d667312491373e13816ce4b7c8cc1a54c68980fd4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>49.60 MiB (52.01 MB) – 753,808 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ce1ebdbe2466412fdf346d6b1ad5bd2<br>SHA1: 9f0f7ffe8e961a31cd6f1eea401bc7c8728facdc<br>SHA256: e0079606dc569c23fed666201f503699d834dc2c9c9ad8a1af6d231709aacfb8</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.149 MiB (7.496 MB) – 358,140 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d3e21d2da14fe2fa0da1db2f6424311<br>SHA1: f274f58aadcfa3311603218b88e8b24a01671e36<br>SHA256: f62294be209c966f38eb82e27717bc64116462241210756e85c31429048d1f96</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.92 MiB (24.03 MB) – 348,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60cc96dd0eef36fef003b9981e7aa19c<br>SHA1: 077fc11bdf3b1a16ed5a8e22cb9889e86b007cf5<br>SHA256: da4f32fc9e285ea393eb3d4fec4fb4a153874623b14fc77373e8f448758ac135</pre></details></small> |
| | | Full Location | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>208.4 MiB (218.6 MB) – 3,652,137 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68a79460a812a271884a0a50858ee1f8<br>SHA1: e1cb26165f0fc2b394c3f08d99642d1e5a3e653e<br>SHA256: f40963b044ff4637dff7dd3608244f6e065cc97e9bb7262d5fea4abeed6cf026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>440.2 MiB (461.6 MB) – 4,274,498 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e9801b97694446ef740a7093d24488<br>SHA1: c8e28d1130d3667d5b313b6e468c5d9d69ffb027<br>SHA256: 88971b264e462d0a2d37d85f793d5e488192b4d883a1ad0142a7c28d9a60af96</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.716 MiB (5.994 MB) – 286,131 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d282e141eb5464b8254973895dd4a19f<br>SHA1: 43ed365a77bcc1acf8efbfc3769c01a237bf775f<br>SHA256: 436d012d7deb50897534e496aeb1616f14ea008640929405f2664f5122ffbbe2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.50 MiB (23.60 MB) – 341,989 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51aa8116a79265830a4cc7cd4ef86053<br>SHA1: c18af12e87abaf09ccf88a3c0de5227c764e8a1e<br>SHA256: 374157270162797a62dd05862b45a4be9f350bd4c2e81ca0a48534910fb28817</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9 MiB (179.2 MB) – 2,958,317 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a7499b08d50db46b5cf9fb15cd346d<br>SHA1: c27a4fdfd31298e65e03fed44f2b36b4aba8504e<br>SHA256: 7e2727a2650e2ae9c6e50b6fbae1b77db0938c91593e6e1e1de5d7e195393e70</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>299.6 MiB (314.2 MB) – 2,903,507 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a92797de8e315b9794c5a75c021c7b8<br>SHA1: 3bad371e9bab711cade7d5e88cc542a34819152a<br>SHA256: 4479ccaf1ffb1b9388ae015e24ea8e3e1780c412777f1ee2b0a30bda83f5d0e9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-08-21<br>IPv6: 2026-08-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.22 MiB (11.76 MB) – 561,681 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a68d5fdda89e42fc15928857014fd4d2<br>SHA1: 339f83ff042ddd55ba4c270e1089f7e8f46dbbbd<br>SHA256: a1f13e321f35f0f8fdf02f81e35c7c996e79ddb538bb60791f22a3ad64a782c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>34.90 MiB (36.60 MB) – 530,421 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15ae2644378a23ef1c976546f9748909<br>SHA1: 573e5172ab99e3857a5fd0c9b799ec2a48aeb76d<br>SHA256: 46f328ab446b3867a9f878a8d7c131dbd1bdfe2f4a5981f7b006eb1860f9e695</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-08-21<br>IPv6: 2026-08-21 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>190.5 MiB (199.7 MB) – 3,714,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd94d3076fe5b6c04d62618a6661814a<br>SHA1: ae4d00d41c844932861ad7f3913944d68765f0b7<br>SHA256: 8c4e4d51b64b8ec225b75beffef958c02db7d595aa138b3b62348568ce0da88f</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>199.4 MiB (209.1 MB) – 3,714,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05dac27e5e6a4fe8b932fc858d32b6cc<br>SHA1: b1e012d68082af0b052495d0ec6fd9a2e8d5edbf<br>SHA256: 3c351a15b51ea7fceed8d800cc5927118fc466db874c6176264ebc9644d12977</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>189.7 MiB (198.9 MB) – 3,714,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9c038d074d7af7b98f3f4871f087626<br>SHA1: 252a7e68d26e606c606250f01316cf77b62d3f11<br>SHA256: a138ef5014804c1788e8143de91d91e6b504d484de7f1bccf42a8a58e2add09c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>191.3 MiB (200.6 MB) – 3,714,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79775a91ea5a94760a9e155203e7031e<br>SHA1: c2e2553e07bb209771e00c6daf30caed3afd5fc0<br>SHA256: 8f8dcf808628e747150029b5e1162823be694ab78a396d2753f9072bb51a0198</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>241.2 MiB (252.9 MB) – 3,714,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb1f1273b795878cc26b843f560d44ce<br>SHA1: 934faed2e36dcb0b0efa56458d9d618192b15fdd<br>SHA256: 8bedc3bc4d63cfc4e9d24041f7a8f9c2b7743d132c074509509c37b18447569a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>189.0 MiB (198.2 MB) – 3,714,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acb56083ca68dd4486ea2e5785a55b03<br>SHA1: cd1dcde767f67a3a32993b557afc62bc5df59074<br>SHA256: 8c2cf7e377604aa9081b6e4a215e567ec17b577de3109bd740b583e0c5cf7819</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>231.4 MiB (242.7 MB) – 3,714,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ebe59ad5f401e4622640a8d61fd2672f<br>SHA1: 33b16df99fe02826a5e694eb32367abcba01c380<br>SHA256: afce55df7601381a794b7a82e967590dfcb7bf5e60eba7d44d32faf569b32d6f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>194.8 MiB (204.2 MB) – 3,714,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 052cf97ae8816cff608e04d53051250e<br>SHA1: 9c7683338ef5d4c519d46c4b6fba3e9cdb8d856c<br>SHA256: f3c18ebba3be48a7f925c291a63354ccdbbd839295bb8aeb5b11e00dca000c0e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>196.1 MiB (205.7 MB) – 2,057,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0da49030234b603cb6e7879d0e50dddd<br>SHA1: 9712967e448cf2f5b54462bb9e0f9255e03464f8<br>SHA256: 4bf5d6fa150683d6f3f113cb63e1812c0c2d44f38e9e27a0c6a60029569647e8</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>199.2 MiB (208.9 MB) – 2,057,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87f6bc1a75e49ae7c43a01eedbb3a465<br>SHA1: ceab55a832d8c24172f31efff307ea5fecfd8f2a<br>SHA256: 39c56884cf6d6e7aa3dbef75a6685608936ce9973610ba5be23a2cf993d07368</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>193.7 MiB (203.1 MB) – 2,057,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0a0fd7e3ab37be0453d89d9ae00cae<br>SHA1: f8f5f030e98ee169e5f10669937963b11fc4c9a3<br>SHA256: ed15f69aa1437855bcf1f303dd7fd8b6d471e83e0eda2f4605b3dd3f6e260a63</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>193.9 MiB (203.3 MB) – 2,057,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76cd81669e7a4a3fa9db662ec413c12c<br>SHA1: 52b644b0e31361d9f55424fd32b331a857a9c6f4<br>SHA256: ebb8dc136e856f1ac96bcd4366ebe5117723f2e04dde701c700e8a3221e65d95</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>216.2 MiB (226.7 MB) – 2,057,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b8d5a2c5662c1f95baa1f0d20ddc8e5<br>SHA1: 5c173bcef75198ec028cc24a0c93a3dcee307e72<br>SHA256: e45ee950f2253e6f82274fc93f601eaf9f96643490838dd7200877b474a79b7b</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>193.7 MiB (203.1 MB) – 2,057,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1ff3d4c22fddcdee6dca2a38b5b4576<br>SHA1: b8c83b5319cecb4a94288c37b571cf1935c68f2d<br>SHA256: 02b40e1a02641ee1091ee25acace730fab43a36db634d6af561e3875dd379690</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>214.8 MiB (225.3 MB) – 2,057,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5aec54afbf28ed893b384840dcea423<br>SHA1: 7f3d1601a6e0caa52a1f0e0998ec99379d776409<br>SHA256: 2543de8b62fa563d341da83a5169101d3fae90c13ee593ea11ac8368c44f665f</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 2,057,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1f21d9a001ca33be861e8f59434f12e<br>SHA1: c627c7c4ab1feb6d6729e2a3f08941ba93e6c326<br>SHA256: a105e244e0a075c66fbea53b6f4856a541994178e9b70a139fa7d7f301ae5250</pre></details></small> |


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
