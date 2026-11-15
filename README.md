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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-11-15<br>IPv6: 2026-11-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.769 MiB (6.049 MB) – 288,751 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88f6be2b2e2c4928c4a97d6da3bcb77f<br>SHA1: 8837b18c4e91cc34ebdbed0f70017e37f67b2013<br>SHA256: 22153f13ba3f8a38c98e55fdb68214097532e7491a9f8acf3d7462698c43a793</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.91 MiB (18.78 MB) – 272,131 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 827e9fce551b885e760afe6123d6e46e<br>SHA1: e1108937c14b1bea72232e96bcec2adc454c1338<br>SHA256: d095143600d885cc5e2dcbc2604348d22d310f4b08a00294262579a08019f982</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-11-01<br>IPv6: 2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.186 MiB (9.632 MB) – 459,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84167ee008949c7e879c18eaa6df481d<br>SHA1: e998f760da828517741b8a57f76ceac532d2afea<br>SHA256: 03cc8544ec1d65aa3d43c09d4f8db8b5471fb5a48eb435c2e8626cb2c202790e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.883 MiB (8.266 MB) – 119,798 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93720f717969024f48fd382cad72f274<br>SHA1: 5173d179b24a928fce65b1c5c1194626035a37ab<br>SHA256: 645dfd169109e1cda747277411d71f68ca9d428d01b715756c1925f6ae7473f0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-11-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.07 MiB (13.71 MB) – 654,585 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b56743d28b754e88a814f0b388d8184<br>SHA1: 6c3304e92c04ca2bf2cf3ee8868e104e766aceb2<br>SHA256: 108c3d1f550e9d4dc2549899e7a8dd4103ddf9c7a97868b63206d27e39c5a97a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>92.29 MiB (96.77 MB) – 1,402,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bee234abc04f3b02c7e7b22480d69791<br>SHA1: da0b6739767c4d663ef7e6fc8477c4969a3b6505<br>SHA256: e9d6e7fd1c852f406901a99c2ea3385e756928b9138c2393193e9618523ea3fb</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.244 MiB (7.596 MB) – 362,984 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1896a3d70d9c776ebbbc51174d2dff7a<br>SHA1: 6b153e2b071d13e45ab9795a9d41e7fcbf0b910a<br>SHA256: fb52bd209b940b70d4fa6772242238a7238e3fdf267f7232a326a283a172da63</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>24.33 MiB (25.52 MB) – 369,794 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90147b4da0ef46e810078a3ca7e5aa0b<br>SHA1: 9df64ba895edf447da29fd2c604e9ff223a49471<br>SHA256: d30738d906d231b000d8994f7a07aee2550e5ba72a4d6ed8b60712ef87862557</pre></details></small> |
| | | Full Location | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>205.3 MiB (215.2 MB) – 3,598,802 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a48535424fbcaaabbc7dfc056e39f5a3<br>SHA1: 4394336d775415fe1a653bacbda7921ede4fd2c4<br>SHA256: a320a6ae6f82cb61d2d9b36a2baf9ed6a69c127627aabc98a1c598893700a202</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>430.4 MiB (451.3 MB) – 4,178,996 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b774537c14ceaf921dbde58aa6fb3f09<br>SHA1: 7695b1a6e7b8783b8331d8935d87fb6691eb8b0f<br>SHA256: cee773355d5c7bcb515c4efd0abc0daeb0b545de5e714601f54daa4c6c03e77c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-11-14<br>IPv6: 2026-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.657 MiB (5.932 MB) – 283,201 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f559d3d04d0b023ee00044c37313155f<br>SHA1: f2851744febf1ec81c0fb7678ea93c854509da1f<br>SHA256: 9f2d57ba5bd15600148ec8af11bb5d1c73c5df8d92d43a7b8a2f04b570234a71</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>25.36 MiB (26.59 MB) – 385,339 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdf132961e4276d4847e99f3e8a11394<br>SHA1: d6d8d534b0c26e7d9435a5baf39b738f96ae35b9<br>SHA256: 5d4536a256517e52942cc5cbdae8d65712adad9f30f5d40bc77a31a922337bbd</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-11-14<br>IPv6: 2026-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.3 MiB (176.5 MB) – 2,912,900 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 172467e52d3011a3e293a609cebc0b99<br>SHA1: 0d251ec08fa282eabfa086b49c7435c45f6ba71f<br>SHA256: c92d9b5f9f80250491431f7cc1993e1e07425841790dab124810a2868f53ee98</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>318.0 MiB (333.5 MB) – 3,079,222 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71bfec8cda51cd5a447bb2f7d9a32287<br>SHA1: 1e76c265df3cb7a6db6a8e501ddd8bd0fbbc498b<br>SHA256: 71ad483d60ebeb8e24249a5f0ca2595d67654b77b66044c6d204581783aa8d62</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-11-13<br>IPv6: 2026-11-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.31 MiB (11.86 MB) – 566,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b5248f107fc695c4eb2ce1021524fb0<br>SHA1: 8915a4096a257a94079c3aa208b3e13ca89fea5b<br>SHA256: dd244eb82e753d234a56e53278611c3f4fb7a294d543cea6f414f9f82546562d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.52 MiB (34.10 MB) – 494,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8cc25a076d439eb3cc539d148f55d6ba<br>SHA1: 9e77bec9131792bbbd6b1ef01000348ba496d62d<br>SHA256: 307ca29c0a715d3d1005d31e4028f2bb1bbfcba5a8fee2e03d308ebd13512b11</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-11-13<br>IPv6: 2026-11-13 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>187.3 MiB (196.4 MB) – 3,649,827 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd9359ee621dae0636e2be9c931e98b5<br>SHA1: 5b53c4610971b698a1036ebfbb501955267e86b7<br>SHA256: b52ac10e403fa6d3346d5109386e2fe5ee312ca8fe884e33d6c8b3c67fe21eda</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>195.8 MiB (205.3 MB) – 3,649,827 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a812c85de3edaeb4eda06fd9e7e4f28<br>SHA1: 78ee12ecb04944fdf9d3d71363d0d43c4276d1da<br>SHA256: ec17d8b7248233ac38611091ab01781e165ce048aef9f48211e3f8296c559afe</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>186.3 MiB (195.4 MB) – 3,649,827 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7921137be736d733357810148c45f68b<br>SHA1: 9d1c7a6a76e52c84338243c4c9cfe2407eaa6a96<br>SHA256: 976850da6fedd56cdcbc053579ad297d05f69d4b83223a196f35cf99a06da83c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>187.8 MiB (197.0 MB) – 3,649,827 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bfcefd3e01a4136cf4f5abefbc514f7<br>SHA1: 855e5b9481ab6642b9c3e7618cbc48f9ee26a152<br>SHA256: adfe464195dade637d7e6b86036cf98623addec8e28b1f1e9e56c9ed825eb225</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>236.6 MiB (248.1 MB) – 3,649,827 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3c8961d2d4b54de068d3efeea7a5966<br>SHA1: c85fe1abe170b9c12d2edcbf83684e56ac03bd49<br>SHA256: 939a3313c5eaa48f01d474d4192b05374fc70a5fc5d3f6372fa25bf5c61da6df</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>185.7 MiB (194.7 MB) – 3,649,827 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f80c8da07a451b20e304d7a9fd641bb8<br>SHA1: 70c0eaf0225928687a6ca391f8b65bf65b9c564c<br>SHA256: dc434a416c7d24d3849b7fce672e7a07b8571299f6427564433fbd1d2a2e4355</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.2 MiB (246.6 MB) – 3,649,827 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4957f7e3a185f782ec154722f1d35fee<br>SHA1: 2defb99814922931cc14aa9d6f9478adad32e829<br>SHA256: 2a5d621345b9ebce03d47390105c66c8fcbec2a26277c10f2c17f07191d74a61</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>200.4 MiB (210.1 MB) – 3,649,827 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c160510e80bbcfd42380219017565e0<br>SHA1: 7124600bdecd2155dfbf98ab4aa9b955a6a12fa1<br>SHA256: b5d9f0844e7019cc8a137f57cee50031e047fa4649f15643ee737d19fdc0b8c0</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>201.2 MiB (211.0 MB) – 2,112,307 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6be799655636f1c1b8a94b70e6f8d064<br>SHA1: 409224899c9bbb5314345546a8c300053fa6562a<br>SHA256: d29f0c4db35c73c3f3d6206a2ed690485fdf80310fce75be97e7b72dd9124d83</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>204.5 MiB (214.4 MB) – 2,112,307 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6cf079c8b94ed6ce891adb8b842f3593<br>SHA1: 0217ab8bc8e48fec89b3c94ad95fe8a3e1f45a74<br>SHA256: 6a120dc482bdbd6ff820a62c7d8b7d410a85b0b453132ee07d0aa21092a246b5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>198.6 MiB (208.2 MB) – 2,112,307 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f71450cacb44da4ebb97ac7967dc646<br>SHA1: 04ef09348056884bafe4ec3f0f87275200ba68aa<br>SHA256: 14bdc975b61f464bbce02b020ec4ebc1ef6265ce1581966b080d0f719c4fbc0b</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>199.0 MiB (208.7 MB) – 2,112,307 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65b0f039df06206425d29adff07ea894<br>SHA1: 905594ffe7e0753c915a4253e1bc516767e13f23<br>SHA256: 6f8defe212109729dd7d87e4c12c395edaefba95e2ed9620948c1be8818777bb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>221.1 MiB (231.9 MB) – 2,112,307 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b4802c651468c1bf09f79c840815005<br>SHA1: d42e88cf2913ed77e5b5ef22f0947a121394e9fc<br>SHA256: c0e15bb64355e0d012b8085df342ba329d76701ebe173f6e4523ad01ed937d1e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>198.6 MiB (208.2 MB) – 2,112,307 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 884bced2abeaddf62a6eb3112d12d118<br>SHA1: 5a30da1d2b099854dd53a8792ca530a2278e5e23<br>SHA256: 8edfadb7a73a1c3cb73d1de4d0f97e585676e1509ecdb3db94f24b726f0cc9f1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>224.0 MiB (234.9 MB) – 2,112,307 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9aedefa5ac894f6b91fb842054fff33<br>SHA1: 82a739517c1453684fd9ffbba255e8104dd4e73e<br>SHA256: b1a6a5d77faf561f5aeed4e53e854a65c02dfb13df323cfc3047deda1bdc7ba5</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>206.0 MiB (216.0 MB) – 2,112,307 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f2f52f94cf0105e2f6133617bd927c2<br>SHA1: da7a0c1656e19035814344809afed5460d707535<br>SHA256: 5869bb33863243b62aee79a88460001747e807f5c5446e5d1fe2a9d278cfc89a</pre></details></small> |


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
