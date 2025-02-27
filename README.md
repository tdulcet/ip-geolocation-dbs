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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-02-27<br>IPv6: 2025-02-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-02-27<br>IPv6: 2025-02-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.362MiB (8.768MB) – 418,705 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4617d1ac3ca66330d6e001dc5fffd753<br>SHA1: 55a55012d01a77b65fdb471b9035313e21f0ae42<br>SHA256: 98922415e3581385faf87f89bcfc77870448fb1100fc82ce21c59108495bcb37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.963MiB (7.301MB) – 105,928 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70b518d871725c64168400f9c2753174<br>SHA1: acec4d4de942d1436cdc64d6ea4fe666cb6d3a58<br>SHA256: e1c19c64af10477ee29c91a82c73376211eb71914dd3c0af23d2f48dba9451f5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-02-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.59MiB (13.20MB) – 630,229 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f9ebadce46386246d3e75a77e1d0a1a<br>SHA1: cd89011e6106ea85b32405d4bcf20cfbe496eddd<br>SHA256: bc091dc4433559d86be456faf27f1569bd8e1e5d154b2b849dc29e930484e14d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>75.32MiB (78.98MB) – 1,144,582 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 122c4336bda3bc4d276dccf50d7b4caa<br>SHA1: 760a056414b3e7b361324c40c9374396259c54d3<br>SHA256: d02d2589c42f11655a7b798cfda1b90a60ec13437748c7ca015deca582d8b4f5</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.300MiB (7.655MB) – 366,133 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1883f9d3b66b213c9652b2754f1edf29<br>SHA1: eabd8daf3b6851fcbcdc502e271ee563eec33de9<br>SHA256: 48be6b4f7ce5d49e0aa80354a2b3fa8091ee7ee9484b2e9e86348dca5ad725ae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.67MiB (17.48MB) – 253,386 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d55b4d9f7f247f6d719dfe6f22af97e<br>SHA1: e4000c982518636457b48c0db654339bbb107992<br>SHA256: 7e96626938329706c08fd7182845e644e7fc4ce49380ee1a2a98ba94e239a30c</pre></details></small> |
| | | Full Location | Monthly<br>2025-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.4MiB (200.7MB) – 3,348,947 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60485671c8df462635efe9a1ee688a7d<br>SHA1: 88209afd2bfcdb478271d4ffeece8c99574845b0<br>SHA256: fb480016b5d4f38aff4b0de3ca0ac0c3208eebccfe5e646d41fe4244daba799e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.8MiB (412.9MB) – 3,823,929 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b430dc9cb96e643623c473cf6e961f4<br>SHA1: 606c5485a9e97b4d4725ee4f6d1690f279e22e77<br>SHA256: 5ffa4c3b8b38e31395832d320455ced8ec5507fe92acd68682b97b3d566815a6</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-02-27<br>IPv6: 2025-02-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.106MiB (5.354MB) – 255,506 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80e1c64b5c125fb46702d19882d68845<br>SHA1: d20869dac975135625842bbcc7b817f2b47da8b2<br>SHA256: 399a14c794395d001176ed9793dc27f299e4ec2de8f90dfdedc07c6a433b0214</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,282 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63b017b1edcd0613c72b27eb077caab5<br>SHA1: d04cfc8b0738a636a2e7787d56061329ecfc4174<br>SHA256: 75f4cef5e2d3c06892367ddaf51c9842b12960eb86547e026e2e127a0d551591</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-02-27<br>IPv6: 2025-02-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.3MiB (184.9MB) – 3,054,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7e63fc3f917acbfd3385aa01ee6b4c9<br>SHA1: 32e4cd6190262bf917d8b7cf206924ffc9d12809<br>SHA256: 8ea4b66fa2628df42fdc49f527c411ef1916e77a858644aa2bd10598df1d2140</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>230.8MiB (242.0MB) – 2,233,220 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d3ee6ff5b739344f91652d949eaf994<br>SHA1: 2eb2eda60699cd7653ca6509c327cec4e486e798<br>SHA256: 5bb91a2e35c6d95f3c0a40e6551823c1ce8cafeda7cac1926bf871dadbb045a4</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-02-25<br>IPv6: 2025-02-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.965MiB (10.45MB) – 499,124 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 323e3e1929108f4b9e2307f21beaee7b<br>SHA1: b9c091ece802e1ecd2fa3e2d777eefe7cb422323<br>SHA256: 27258658fe60b17124b5a060c32622c2398dd7ef97db66c5c4a9dc143a0a158a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.18MiB (32.69MB) – 473,829 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47e058a61f1d578df153131d6434b5f8<br>SHA1: 40d8e9798e3b0f3d5afa1df0874c3a7e1698e534<br>SHA256: 0d98f1d50ff58456eda640dd0eebd6d6798e401bdadcfeb1a3dea1c90c34a6a1</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-02-25<br>IPv6: 2025-02-25 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.1MiB (173.1MB) – 3,265,315 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43c9e57e21ed0607f02b2f5b0896ffca<br>SHA1: 49642dfe3e24395ca2511e59f64c1b95105e2593<br>SHA256: 08438220940ec31dfe9f31611ba5596efaacc5455773f7ffcaa3213d3c146540</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>175.8MiB (184.4MB) – 3,265,315 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37ca03d3f78862545743aae1a572eda3<br>SHA1: d019c1f7a10a29d6928aaaac350a3a20a5da95e7<br>SHA256: ee600b7f74b8153ecdc60d8edef778858676f0b1d7ed42365f5cb96565237413</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.1MiB (172.1MB) – 3,265,315 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3109aa529ff45c6326d8a4c04d9b3c49<br>SHA1: 56cd8ae00639068fb1a13e6dda5252391bdfbccd<br>SHA256: 7f373f0401d0289f0d986e79b8a5207d4bf089a94c629ea5f50b5ef6d26a6456</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.5MiB (174.6MB) – 3,265,315 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99e816f5e484c22cd7971cf1c279a617<br>SHA1: 2eb723762cf41402fb420116a838440988e10a41<br>SHA256: 166209adf3381c7b8a2fed0419832ca1494902c56c6cebc080ea5eff7b4d739f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.4MiB (219.5MB) – 3,265,315 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca9f263324f9b11e00f4d20dff2e0541<br>SHA1: 0054826252c2607acb7d3701438cc11b9b60a4a7<br>SHA256: a208fc68df7030af7c9f797031f9c7b37b45690fe1d54fc5b3ea1d820b50c4ad</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.1MiB (172.1MB) – 3,265,315 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa1172432d47071adcaa90e60fa168e5<br>SHA1: 0d5f6a729891286b350c28292877296baf65b8a1<br>SHA256: 094cc0b233e83f2de2d227a2682371b5342ef5696d60012a8ab67c5ace600cde</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.3MiB (213.2MB) – 3,265,315 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b59cc48b7f8e478a8103f4aa83fceee3<br>SHA1: e34ab44bd0ba0fc315dbfaa83ae80183efb8d102<br>SHA256: 29e887e180de2ba463e625d557dca5d0ad282c433a1304d6438a832da32492e9</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.2MiB (179.5MB) – 3,265,315 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d20c573f1ae114c69ab13ea8d880edd<br>SHA1: b94e1a7d2df42a65664532be58d30ebdbf92acbf<br>SHA256: edda77980a6548a5149e6191665d42e4eab422bd5b6eb5fc820ca5cf04fd2a69</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>163.1MiB (171.0MB) – 1,738,488 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fce61fbc4a2278f5f2c41c8c751ebb5<br>SHA1: e042def217b3236a17c995d6d178c010fd22187a<br>SHA256: b00f000ae19515d2d4932f05a5c8e59ef8983189afd5be6be8fb7341cc8c7b52</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>166.8MiB (174.9MB) – 1,738,488 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93b7a7ba376c5ab93eb21b8d88b79ebd<br>SHA1: 0b07de5e375135bf9cdd4114141cbb8529c0e994<br>SHA256: 165f22c9bae41dcdbb2d8e3dc4f8e442cf3b434c69bced2e55e330f2a4af8506</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>161.2MiB (169.0MB) – 1,738,488 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39759e84fe7e262ac3db86c046bd8dd<br>SHA1: 117f7422a00b33a3fba5ee206fea1d657f42bf96<br>SHA256: 3a7486b31e2ab2fc2c7e45335802672149a822bb0ec6d322e9e312bc0c9e0f5c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>161.6MiB (169.4MB) – 1,738,488 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2433f4d4ae24f7abdbb455a01bdfdf0d<br>SHA1: 251e1f9a5de8af4158512982bb676c4b21b7feb9<br>SHA256: ea8863c10147320ba58e374b5cba866cf2d4f35d935f077031edd8f016324956</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>177.7MiB (186.4MB) – 1,738,488 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ac55774cb2817117332387b3716aab8<br>SHA1: b232baf45dce2f74bd89b6e7fce319cdfc8a8446<br>SHA256: 9666f20f2ce4a4e8a5565d22f638636e5f7353248580918bb7be663ed6f86a63</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,738,488 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84a28a63f56987966b938a91cfc7eacb<br>SHA1: 0dcb6044a292dadcfef14de9f0c5965d8e040dfb<br>SHA256: 3f20363baef8c0e5f9cfeb625408bf28ca297c71fdef6e3763fdc9540130314b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>179.0MiB (187.7MB) – 1,738,488 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad09d351bf9887557df43c56c5bc00cb<br>SHA1: f618f33b3b840e8beae33306aabf00102e5e8d01<br>SHA256: b148f74ca8798c92fadf54a72136ef57ed137a96ec4b1951740cc76ba8aa6032</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>164.8MiB (172.8MB) – 1,738,488 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7df8c9105db62b85190a7df0b2e271b5<br>SHA1: be5dc5d82ef75740e29e75460e662a4ef2f90664<br>SHA256: e147a68f196d481d18c02d476d12b280d1bef79b9445a82308bc5cdaa9949394</pre></details></small> |


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
