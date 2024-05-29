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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-05-29<br>IPv6: 2024-05-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.856MiB (5.091MB) – 243,077 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f7c2f3a602c4ca93df714ed1e88f7e<br>SHA1: ef77c4151c6952f4df4fc0631190620a76c21534<br>SHA256: d1909d5fd9405c09a6a0b1230333786229f96525b72f37a164c0b230e1399893</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.353MiB (6.662MB) – 96,550 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76b78567db34ccdda8dab6667cc9f4cf<br>SHA1: 558db0be717b92bd93c01f00786f6f79980b6797<br>SHA256: c7711f73223add107d4236cc34462ea746e30fb175a7345bb898e9bb79d74f12</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-05-29<br>IPv6: 2024-05-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.261MiB (8.662MB) – 413,698 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2172fc76a3dcc6b78e8ed0122b729dc6<br>SHA1: 431a1b223a22beb2f61bee13fa1e5a3b7ea164d0<br>SHA256: 4239b903cabe6b187e67e5ef2a11dcd997ce7c73b9062939362d9faadac68478</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.407MiB (6.718MB) – 97,473 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 365f28d67762f782f7dbe6b99428d2f9<br>SHA1: 921a7524543723aaf02bc306ffd2e80be6aebb4d<br>SHA256: 763a8f18366a3646f149a8c0496e6bf4c5a4ca03d96af895969f0cb4181e0759</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-05-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.68MiB (18.53MB) – 884,464 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37f482e45b1a2c0412ae8556aaea53ec<br>SHA1: 228f91469b820709d8bc4c05c833bb3b913f5796<br>SHA256: 8f988200cac121b104919f01ebe308181f961208196dfa80a9660cb84432c8cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>76.81MiB (80.54MB) – 1,167,299 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7d943cbbe91fcfa356f8224c1813d88<br>SHA1: 12f9752826739d8ead237bd4368267578dbaf8e0<br>SHA256: 42e8490333d898a5e891d873ce403f5cc56737e7d1fcd539db6cf6923c6f3ed4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-05-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.812MiB (7.143MB) – 342,272 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6a0dcf5757ea0e706a0c94568280620<br>SHA1: 03bfb92700023a7d01c587329c906e922cc5547c<br>SHA256: 0701b9503a19f2b5ef4f8f0658a2a534df0822bfbef51efb3a1bda57a55e3f99</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.66MiB (20.61MB) – 298,729 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2849001e67a02bd3a08a527da352e577<br>SHA1: 9f755c138f40a70c4ae69708dbdc5e8ef7f7767a<br>SHA256: 5130d7be5953b435bb330affb2fd878e7d5cf8b2c52a1d894258152ceabae370</pre></details></small> |
| | | Full Location | Monthly<br>2024-05-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>184.2MiB (193.2MB) – 3,220,410 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 370827b267c010e93a9e283b93c295b7<br>SHA1: dc5b7559d75d79ed88de26ae4281be2075f11796<br>SHA256: 540ecb934cca1d5d8c74a0a6af24ad0a1ff60fd114c0d10e34c816f2c71f0407</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>352.3MiB (369.5MB) – 3,417,644 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 390cb4649597293b6f658c2539043819<br>SHA1: 083b6f7c90866d15cb38d7c80161776a233b8efa<br>SHA256: 390822a76bd90dd6a9a255e68aad76890959f99892f2f5b9db086ce9aea01a06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-05-29<br>IPv6: 2024-05-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.940MiB (5.180MB) – 247,251 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01186f618906e8a86cb19644d41d20da<br>SHA1: deec7203d4d1b7d2f6e570d2f9b266e527f70d48<br>SHA256: fac2f5169a0d09163c490a15ed2baf33b320d045d4a322e303615ee1c529ed30</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.59MiB (18.44MB) – 267,259 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22d3e3bcaa44ff5f7c9bba501be8f19d<br>SHA1: b8157b22815f05f6188687637be52c92d39ff65e<br>SHA256: 3fb81be267f86c69bb8805e4daa892738a3a76558767d4ef27bbf6f95a18210e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-05-29<br>IPv6: 2024-05-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9MiB (179.1MB) – 2,960,692 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14506da570232614ab1a76e45735f421<br>SHA1: f139b51a9c5a9421c67b1965ac5401befe35b734<br>SHA256: c51306ec8cf048271b6a8e500f942292deda452f14197c48b83c1baab6ddfc01</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>183.1MiB (192.0MB) – 1,772,190 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8d155edcd26a365c0bb0cd5ec2bb347<br>SHA1: 940de771ad10e3cfcc813ce70bbc1ec58c7e922d<br>SHA256: e0b1c26467bacd38d3d9abf3057b61a9343e6a869d9ef21906a2030ef276cd49</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-05-28<br>IPv6: 2024-05-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.768MiB (10.24MB) – 489,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56153a6e9f3b3308e06d23cebb1833be<br>SHA1: ec754e006fc2aa5243fd29070b889deffbab2f67<br>SHA256: c2399fcdbf83502fb9252bc896060aacd1f252dd936ecc85e3399dcdaf0e3df1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.86MiB (19.78MB) – 286,641 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ffb963f12d47206b2b60f4c283e1ab8<br>SHA1: 197b928d940c4fab10ddb8e52497ecf74fbe0fb1<br>SHA256: b2a6b96ba085bd66f633d1b9c663447b4a2100048b5f485467ecb4a7711b08e3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-05-28<br>IPv6: 2024-05-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>118.6MiB (124.3MB) – 2,373,346 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 299813bf9092531516ba193d3ecbf822<br>SHA1: db08b59150759341afd7702e8104790bac98ecea<br>SHA256: 5539343ac6ab4936e10e723bf9640c46833c448202e429dc93d5013132dd2be1</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>127.5MiB (133.6MB) – 2,373,346 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 320ce80b6cd7208ada0c1be2fde5b937<br>SHA1: 5796db93cbc7a4e85ebfc5a4255ef55beeef6648<br>SHA256: b9d9ae578e4d8c703a370f454787a46df8edfda328b4bbf70751d4f026e99068</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>118.3MiB (124.1MB) – 2,373,346 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1efd883f6db9bb535ed9e5c3e578d9b<br>SHA1: 957fd614252c52e0ec898cf99c72ac2943300132<br>SHA256: 6e34c2d246050a87a445cb4f9479d285855b789893904cf6681d44d5c0b42ca0</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>120.8MiB (126.7MB) – 2,373,346 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02def9d6554473c36d3a550c2ee827e1<br>SHA1: ea3fc2d2ad22cd386b6d0cdf8326733ce4962502<br>SHA256: a8da63f60aaed1dfe50a08ba33dd0094f6a5d8ddb8bf5f0c1a90d207442152c0</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>147.9MiB (155.1MB) – 2,373,346 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 946f48375888d03b2a89e3db1b9c68f5<br>SHA1: 527b3c07516be60c692d8b49a2f97ef05373978b<br>SHA256: 8c7acfe471cd0831bf3062af0f5e58028547ab2590718489055f248de70f99ed</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>117.6MiB (123.3MB) – 2,373,346 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b5c70187a116ed538f99a9d6bdc0b5d<br>SHA1: 52f72f7065c80e9f9662bd2c987927ead2b8eb50<br>SHA256: 294a4704eda5b6c44cfce36f8b6667f507bb2aa3446421c6fb457d37095a2f6a</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>144.2MiB (151.3MB) – 2,373,346 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3784319657a42fd5294d4551675eae07<br>SHA1: d003cd59463f8d1575377ec759af374a4b9734eb<br>SHA256: ce0888540efde97bf459e27aec4b7975398e33f354b2ab9e55ea86c0223434f9</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>121.0MiB (126.9MB) – 2,373,346 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bdc8479a35cd57c3d69a1875cf88d8d9<br>SHA1: 5648f9b47a9e3e41e7cd81faf1bf9bb669ce908a<br>SHA256: 7dba14748991b8d3c02473d45ad832a95e7c068bce8dc5ebdfaeb747dd3daae6</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>110.1MiB (115.4MB) – 1,183,943 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a94c8b05096aeb2895eb15af4e85887e<br>SHA1: 10261794542e7c4297a626ad4876fdbfcdd2e92c<br>SHA256: b6f4854274d73a7c36f10d3d7cec6133cd62644404fb6fb2bf24f0bf6c9ad6a6</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>113.9MiB (119.4MB) – 1,183,943 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9d58e94867c73dc2e9618dc27dd49ec<br>SHA1: 0d8f045f5610edd798733f1981b3e55b964800ed<br>SHA256: b103aae5ec279e924ab6a03c7ed7d99be5041e355db0a833dd0171f7046cc569</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>110.4MiB (115.7MB) – 1,183,943 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b5b7861a8411f656ef4ab050e968dfd<br>SHA1: 5a1efebadb88b6f78cdf8d172f5b3fe259d071a9<br>SHA256: df8a8dbcfc377f3de76b023ce59a2edf69188440d6cb12e5a3cae8d2a1f3dde9</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>110.8MiB (116.2MB) – 1,183,943 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d8ca21cabfde5068514b0480a20634b<br>SHA1: cdf99e801ba8a11b2c28398e883bf72e689a8114<br>SHA256: f9f5fefae30334c9ec7d3966b7e86afabfc0e0b75f05cedc1f544b1c33c329f9</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>121.3MiB (127.2MB) – 1,183,943 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d57f2c4fd83310f0cbc0f64e62fb1a58<br>SHA1: 175526b2f5fbd151e9a959cb0d41a30b56dd6704<br>SHA256: 32499f33f3439670e3ce5de661dc83ea4b21af0196d4fb305bdc02fd80827bb5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>110.0MiB (115.3MB) – 1,183,943 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41d3d3b6afcee0ded41425fd40e3d69c<br>SHA1: b66cfddc2a6c1fd03dcf178065cb87535ef2d30e<br>SHA256: 3e4938f5524cc73bf3c283e532f32c97d4cdc0ebe49bd4d54b6f8db3f693fa80</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>120.5MiB (126.4MB) – 1,183,943 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a428960452ca6e631420b4f5009f85f<br>SHA1: e051160fa3bc264f6d397f1fb31cdcc7b12f6621<br>SHA256: 3c53b004db7ce6956a86a3f05409d62c4183322c895ddf1c10f300d0a8fe39cc</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>111.7MiB (117.1MB) – 1,183,943 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c80255ef6bcdacb62dd56a0ce3602085<br>SHA1: 70c591349a026754dc3af8a9f495f249bec06d12<br>SHA256: 40b6f13f7f14deb78082bf103d43f0a167363026a60179aba12e9d852ddf72b7</pre></details></small> |


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
