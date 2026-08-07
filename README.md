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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-08-07<br>IPv6: 2026-08-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.403 MiB (5.666 MB) – 270,423 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdd65163b6f037bb6b734d3974d056a6<br>SHA1: a1dd9dd15b4df4df9541558c30c0fa302b587438<br>SHA256: c22d12d01861680e2811121b7c67da3dff0547113d18338e7c2f48bbe4449f10</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.74 MiB (17.55 MB) – 254,378 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d010b4247e99ea98206149bce5f69d90<br>SHA1: 4ee8735dfc571885436217558ec58561c2704227<br>SHA256: f8f562bd1f0b3d07e053ca9766e58259a54bd436fa9ead785dcfe3171c42d8fb</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-08-07<br>IPv6: 2026-08-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.039 MiB (9.478 MB) – 452,588 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 717411bad67bb5270526cef1cc039121<br>SHA1: c63175b94db2b47c0cc12a1fc8ca1f22b769ee7b<br>SHA256: 72436167fdc8cdefa9f411f88bff237621edf9fb3cf1c910bc4a41083b967c6d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.991 MiB (8.379 MB) – 121,546 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b123eab7d47e6e96b1e6d1d82755c80<br>SHA1: 23c3f83d73e0b463a5c756b13f7ab3fd380680c0<br>SHA256: 935d7ea73247358553c128efdc4d98d494d60c043f36d36610cee7a822de8549</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-08-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.27 MiB (12.86 MB) – 614,099 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c64fa189f94f6c2493b03c8ec0dcbe3<br>SHA1: a4017e12af48e0096cc517cdcaff404780460c8e<br>SHA256: fef128c181afb67163c6132cc798c9f3a928156f4d85712b4c6ad41797a80f78</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>45.52 MiB (47.73 MB) – 691,759 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6547a5b154cea3d56603cb5c4210aed<br>SHA1: cf25b09739e5277fbbc20376c243a00b2d6158ff<br>SHA256: da04ae0f03d692cfc82ed4de8bc1fde654b919b5e3bd616092991f67f6c03f2b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.149 MiB (7.496 MB) – 358,140 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d3e21d2da14fe2fa0da1db2f6424311<br>SHA1: f274f58aadcfa3311603218b88e8b24a01671e36<br>SHA256: f62294be209c966f38eb82e27717bc64116462241210756e85c31429048d1f96</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.92 MiB (24.03 MB) – 348,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60cc96dd0eef36fef003b9981e7aa19c<br>SHA1: 077fc11bdf3b1a16ed5a8e22cb9889e86b007cf5<br>SHA256: da4f32fc9e285ea393eb3d4fec4fb4a153874623b14fc77373e8f448758ac135</pre></details></small> |
| | | Full Location | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>208.4 MiB (218.6 MB) – 3,652,137 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68a79460a812a271884a0a50858ee1f8<br>SHA1: e1cb26165f0fc2b394c3f08d99642d1e5a3e653e<br>SHA256: f40963b044ff4637dff7dd3608244f6e065cc97e9bb7262d5fea4abeed6cf026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>440.2 MiB (461.6 MB) – 4,274,498 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e9801b97694446ef740a7093d24488<br>SHA1: c8e28d1130d3667d5b313b6e468c5d9d69ffb027<br>SHA256: 88971b264e462d0a2d37d85f793d5e488192b4d883a1ad0142a7c28d9a60af96</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.729 MiB (6.007 MB) – 286,747 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ce5cc1653ddb65db06474bab749714a<br>SHA1: 4cc40ea81eba37e4bdc9ce61fe9ce058d0c49372<br>SHA256: d3b805b3c0b083f2ac8b16100752f8ea3eeb8e224cf00f594602330d36cefcb4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.35 MiB (23.43 MB) – 339,594 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 518560be8d49e16a3856c31b0d0bd875<br>SHA1: b1f9595b2778075c3ff384176d6845d15decf465<br>SHA256: 5d25d7d5e32cc9f7b89b03e674eb90f100272a7f4bcd26c78e8a2b2c41efb36b</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.3 MiB (178.6 MB) – 2,947,098 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b12349e01828d4a4bac50e8c858fd50<br>SHA1: e99752a712b42043ecd9c65d3e9651264ae608de<br>SHA256: 3d436dcbd07ba02c6c6fac1fe6d1baa7bca22dd26ec4bd68d3029810ffe0e936</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>299.1 MiB (313.6 MB) – 2,898,359 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddbe75f08ad96059705bbdd5423bfa36<br>SHA1: abe287e78fb8e2391d170e4400975486e52fac90<br>SHA256: eef9c134b1787ced9b9492f2d3cf0bd3e4f7ddc7f71199e6c54374d9513c5083</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-08-04<br>IPv6: 2026-08-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.25 MiB (11.79 MB) – 563,186 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88e5fb221aac4e1c24fc1aaad2cf9512<br>SHA1: 668a8942f34d006911d281849fe9f9827fc7cd1e<br>SHA256: 35a57d4db27fd6eb94c5ff34fbc75f975ab7d72b841ff2560be32eb1c7cfad92</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>35.64 MiB (37.37 MB) – 541,633 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0f4c44ef09e26e773d424330c67a684<br>SHA1: 668dcd2bf8be628dab5b4103ee709b7e634cdfcc<br>SHA256: 40222e381dca95f3fa7e6f90431b5c5b7609bd1b51f289fe798f5f4d310bdeab</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-08-04<br>IPv6: 2026-08-04 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>192.7 MiB (202.0 MB) – 3,752,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e652d16b73d4ca62ac21917af726c981<br>SHA1: 28aa5f1732284fc95ea10b8f620597de3fceb821<br>SHA256: 5067cf2c03e506c28a0b44232908a3b23c32e90dd38f983e0fe1b59186e517f6</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>201.7 MiB (211.4 MB) – 3,752,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 268461b95f7589003ecfb5814890bb90<br>SHA1: 7d9d7b5e69da73d1c853eaa3dcfe50e96c6f55db<br>SHA256: fda069b33ce88d30b30fbd307420a56eb5049d4291969cd7c4ad8bcbb9800c5c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>191.8 MiB (201.2 MB) – 3,752,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bb2257dde5eb965dee4d0d7b95ef75e<br>SHA1: dbc6af0c64b0206b99eced50fac3f0b65d90ad68<br>SHA256: a0c6e05be56341dd63e9dd382f26a42195449cb564f7eaaa6b66d592d0f89606</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>193.6 MiB (203.0 MB) – 3,752,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bba6ddfbed297ae8265dc27f498fca4f<br>SHA1: 586c4fe11bfbad29698479bb1eed7552247716e3<br>SHA256: f2482d2724ae48a1ba1abf937c43ed68616cf4e3914a35dff043ad44328dbbb9</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.0 MiB (255.8 MB) – 3,752,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bb371662d309f637bec5f26e960977f<br>SHA1: 31d3f3ce7600a28cacdebeb8fd9250ff196d51cb<br>SHA256: a18f07a72ddef76aea5db4124a45657d3f8b744fe7eb770a2024636edb2b92bd</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.0 MiB (200.3 MB) – 3,752,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8aca02dbb62b4066165706a2f35c176b<br>SHA1: 223cb010a8a1526906c8394fa577653e1d2b0433<br>SHA256: e8ccf6b3224d76e1c6a994fbf9d4efbf41ae8ae56bdbb697a2707d75f290cf43</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>233.9 MiB (245.3 MB) – 3,752,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b1ebb23de88f2aac3631477f238d8c3<br>SHA1: 6608767ba0b101b5ab2cc60c618e4fd54cf1ff71<br>SHA256: 2119d6b76a676f543f69c5b3c0f5e842fdd09f887878403742bdc8167bf810f8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>196.9 MiB (206.4 MB) – 3,752,731 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6b4b72f8c8fc33b0f49d943a7db4b2f<br>SHA1: f6a4c8b34b06118f4cbdaee9226e2c794a75bc03<br>SHA256: 86f06afd47646b6bc127759b37d76260e0bbad35abdbd2eef31d25b84d333657</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 2,063,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91b770ecedfe411b67c0b5303e37805d<br>SHA1: d3a6cae685fc1a5e429a1cffa43fbdf513821153<br>SHA256: 5fa7993fec42a9e91c1d96908b7c5d037cccaec271feec84cd38dff658924391</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>200.1 MiB (209.8 MB) – 2,063,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74e218bf86ba5accec6b4e4663395ef3<br>SHA1: a05e6f178ec46e2a9e99ae151c2aea29f340865a<br>SHA256: 27367f483f8012d8a679f343dd99916c7941b97adfcca1f1723907ed2a6c87cd</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>194.4 MiB (203.8 MB) – 2,063,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72965b59d910f26aff73c814a9bf075e<br>SHA1: f86977da8e37994bb1c100fba79488b45be0a3c2<br>SHA256: f11ec54c444f7fa82d311e9a4dc40ad0234ef9c2c58e89ab33048b8773e6646f</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>194.9 MiB (204.4 MB) – 2,063,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38494f73a503156e26cef1d3164a4fcb<br>SHA1: c48f0c96b9207ffcdf60e51c79a49235954188be<br>SHA256: edabe7f2c1f88fa81f309241d3948bab8951a1c6ac5139e0e24a1ab32f70217e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>216.9 MiB (227.4 MB) – 2,063,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a57308127cdf7a644964975a05ab689<br>SHA1: a4983a53d7c715a485896c1043d5998995c15262<br>SHA256: 4354d9f358c98db4290345b145fa273a94ec35f9843e8c6adad90eb28d96e96b</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>194.1 MiB (203.6 MB) – 2,063,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8073be53b028cd7377e2b99d58f51aab<br>SHA1: a2fbc5aea05f8b1ddc494cc93a22eb9106e1473f<br>SHA256: 8f4b10f6083d53cb7ca0d31a7c5f86e8e3aa5122403d1a077e342eea716b5fa3</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>215.4 MiB (225.8 MB) – 2,063,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a030612cfcfd2d0494bef17f21007d2<br>SHA1: 99d931e2b380fad40e904b1eec299abe0d40305a<br>SHA256: b7c5fef1633bfb6949f3a9c887e99426047eaa28f21aa5ceeaab3ccb89040fb3</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>197.1 MiB (206.6 MB) – 2,063,109 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3cb1aea506d42040b07191c277dcf916<br>SHA1: 9455977b5201c98c6b749a992111406777816248<br>SHA256: a2ba9a05f01fa54b2f9dc4bf17e932fbc6dca26587edb4968ab8392ec71cb31c</pre></details></small> |


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
