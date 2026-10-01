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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-01<br>IPv6: 2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.568 MiB (5.839 MB) – 278,676 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fe728a2994c606c16a0016a99e20f9e<br>SHA1: 2afcafa5b41440502d1200e7d1d263707cb5fca7<br>SHA256: 5a0b727b295ceaa605b3f6f8e103b0cefabee4e07b99a251639c7118d6af12b9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.78 MiB (17.60 MB) – 255,024 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34dd3b10d6698657742d506a14d4bba3<br>SHA1: 5cdc645e752d4e259e596860436fc8f3a439118a<br>SHA256: 94ad5043428864cac3a845d66956282e1089c477011c2e00e0bebcacd502a4c8</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-01<br>IPv6: 2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.157 MiB (9.602 MB) – 458,532 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b38f1493434968ccd540dbae7153731<br>SHA1: bb61f9364a211a6047778fd227798d794843d168<br>SHA256: 30806d9cfa8f49345ffc91ec101a07eb75417126de7abc6905c73e78e2607551</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.061 MiB (8.452 MB) – 122,612 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 298da2c08c106c36f6a9bcc0dc6677df<br>SHA1: 15d7fb3add2068de359e35af111c0fe44d31006a<br>SHA256: c7f90e353613a5a611e90a1607ad901464045bf810a1265320992df7eec9c435</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.28 MiB (12.88 MB) – 615,059 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b364f40262248924bd7b5d55180b7c36<br>SHA1: 1c895f7e20d40af182aafcdf230145350ff86839<br>SHA256: 909e1c9a160afec6233538f89ef5f8486545f55ad1af7b99359eb2bdbcc32b08</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>62.33 MiB (65.36 MB) – 947,282 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc7e7b7233898c14a29e9b4e2cfbe587<br>SHA1: 94543146f58381bced97ec9ca69b963f4c08d02c<br>SHA256: 090046ff7c8b4e293f1d834b12759363c1e9cd51654ec24c656c14d5e6578ad4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-09-30<br>IPv6: 2026-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.778 MiB (6.059 MB) – 289,240 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 037cbe9e49d48b0386b4034c7048c166<br>SHA1: 8c73a34d6c47e79b0badefc8537eed6ecf22a1ff<br>SHA256: ee638c1c30f847a38cdca18fb3e6e1a2eb2df7ad320e6337d67810c3bab16fb9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.89 MiB (24.00 MB) – 347,830 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4516b087eb6d889360de69e0e36656c<br>SHA1: a1976e56a08064be5a24f8e5c28ffb07262b4716<br>SHA256: 4e0d0b9bdcd967472b7f36cf1465613f3e2211b91a422044355cac7646b8c6b2</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-09-30<br>IPv6: 2026-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0 MiB (179.3 MB) – 2,956,846 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a313f9fc27ba37b673b099489446886a<br>SHA1: ece362877a757aed6d6ccdad1bf2fbcb4031e9f6<br>SHA256: d7ef0d3ca1e2b8198a0e007e322d5c964611e1ed6f900d9d2edeffda292f2aba</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>304.3 MiB (319.1 MB) – 2,947,358 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ef9a15cb810aba175baeb46886eec39<br>SHA1: a8a32cdd1c882bab942deeb72f2c8da534c8bfdb<br>SHA256: da31230883dbafd4f2ec3e54d86964a6ec028cfbcf767d5e30d1552eff280d33</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-09-29<br>IPv6: 2026-09-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.17 MiB (11.71 MB) – 559,415 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8e3914c7b2400cebb47f9e45b6a2f92<br>SHA1: 628ebd5e82a4f80bd05861e1ab1eb47e47286d2f<br>SHA256: 1fa7d3dbcb10ca3caee96ca70b63bc37f9a5e437d65b756cfb264482da7aa071</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.88 MiB (34.47 MB) – 499,639 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5ec059af62f9d09faf2b51eae77681b<br>SHA1: 5ce38bc71745bad96670804165573243b50a6c44<br>SHA256: 2cc7734232c0ac744f5b333d8b599eb6ac6d58b496fcdd1e2f9fb29151730e52</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-09-29<br>IPv6: 2026-09-29 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>186.3 MiB (195.4 MB) – 3,634,415 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00f1c4480fea98fbbf3f3701d950becd<br>SHA1: c902ebaff92a83cbd9a08d3e21bd335e12a7eba8<br>SHA256: 0d10897bf7cb7aa577ee8a31c0163828bc54b17a17e1e468779c6ebe89b02f90</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>194.9 MiB (204.4 MB) – 3,634,415 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de09e7001a79a4bd1ce89500e96ea526<br>SHA1: b3cc7361a480874bb2a449abfc71f489e13d4528<br>SHA256: e236d468ae0583fc3264fe631b690ee3d3ba009e90084d322bed0e03f4425fd0</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>185.3 MiB (194.3 MB) – 3,634,415 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7748c9168e31d24143e38baf9db48c69<br>SHA1: 43e2eb11fd9954b7e656bb42e85b7feff26e9e74<br>SHA256: 68e3f6e1b93d82aed26bfb639f767b98731f21d4a62eb42815894472e3756928</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>186.9 MiB (196.0 MB) – 3,634,415 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae61a411ce87ae8fa62014a601baaa7b<br>SHA1: 3585169f4acd3d517c9d6402affaf002281245c1<br>SHA256: b74de3ded093156da0d56487aaaf69142699c0bd68e5dc61390c260f941fa639</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>235.6 MiB (247.0 MB) – 3,634,415 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5f8ee0684cf8ae97582a8eb8b8e28d9<br>SHA1: b189b1483b09eb798b0777b7e86000b0e7b1f3fe<br>SHA256: d74cd349fca2621058f72fe1cff82516e81c494b7670b8a0ab78238d66122946</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>184.9 MiB (193.9 MB) – 3,634,415 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46842dece3c3869df3996e32d59c5998<br>SHA1: ab267816ed41ff3fa43de2ddbd0b8e03825ae651<br>SHA256: 85a895ec6fca47ec5187df83f2c1a1b37226cfeebaef172e7df080080c101243</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>228.4 MiB (239.5 MB) – 3,634,415 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58623cfbd5f050f1670f4b8a99a51d7f<br>SHA1: 8efb2860e44586a8b4ca589e7c987b3c8f346eda<br>SHA256: 01cd1b8895bc26c124bd9b9e47b11ac04aa4916a4373981ab715a0cd374cffbf</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>190.5 MiB (199.7 MB) – 3,634,415 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10f428d6b397e46939b472282a5bccbe<br>SHA1: 0a9a98dcaa3713d9b6ce1f32d5addf2855ec1a23<br>SHA256: 73e20ea6c456f787dbebe769f11e6fea6dec368fc2638b496ca417d1f01d30ef</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>197.1 MiB (206.7 MB) – 2,068,173 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f90e693e7de7b9bc4298023780bf016<br>SHA1: fe3a9712e9ad114761b210fd889f9d2505c0a7c0<br>SHA256: 8795122e1e9d5db58aefb382b3ae48c4aa2754753d4a93781b7e8415d0106ad5</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>200.4 MiB (210.1 MB) – 2,068,173 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c09b8f6e6f82331eee69cf87072f2ae<br>SHA1: 54a3f593b3b43dd742ecf6e34baf057c1ce231d0<br>SHA256: 4203c64c09484a69d5f935236cded31d429a67d066e5a78f34752b52238ca259</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>194.5 MiB (203.9 MB) – 2,068,173 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85a9cc430112fd689477537197f83183<br>SHA1: 007acf89681fa47a656b8ea8db9f563a0872e1b9<br>SHA256: 9e72425c7a647c3c68943d21ecd0a41d86ee33602b7de97553b73ab7eb8296d6</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>195.0 MiB (204.5 MB) – 2,068,173 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6263a8e9c63f0f4f446a5cbc2b992b95<br>SHA1: 385dbf94e69cf73801eb74a8935350facda9c7a7<br>SHA256: e1d58cbcf100b5d2a8f9eb7c98c61844ffa0885bd13d184d2977c8370b91b1b7</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>217.0 MiB (227.5 MB) – 2,068,173 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9daac5fa053e1cdf070477e69ec35f75<br>SHA1: 413e3add41415d37f3f36ba6422c0b69a64e37f7<br>SHA256: 03d1988e8b05b49e9bc1d87f727aaf2076815bfcd8b1efe49fddaa7a442d78e4</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>194.6 MiB (204.0 MB) – 2,068,173 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3d8cd0d02bbacd368aea385f5ed8d5c<br>SHA1: dd13a80ef4277fb009360acd6c162531a9927cf0<br>SHA256: 7f04f7aae9f836660f6dea80c3ff398a4f1087d6f935d3de7b0c68c7c6b80c60</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>216.5 MiB (227.0 MB) – 2,068,173 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0c663dcde9f2227d2d03d45b53156aa<br>SHA1: 9b80df06938086c30da278d24cd973d932bf8b4d<br>SHA256: 09c2a7b990ac0bafa35135ef3847e727dc8db5c2917bba8c01bd821f9251dd7d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>197.4 MiB (206.9 MB) – 2,068,173 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e9fcfd0c7b5cc4d5d172ba7cb357391<br>SHA1: bcb0efcbbe721a9c01c5e7f8f826574a9c868057<br>SHA256: 823a10402b68207fc64f75baae859ea3d474bff83b210b64e440063b5bd33ce2</pre></details></small> |


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
