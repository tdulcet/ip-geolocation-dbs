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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.710 MiB (5.988 MB) – 285,807 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77051750650afceb5a3341917ceec781<br>SHA1: ccb3db74fd770dc4b2d80e633f9c3a469d059300<br>SHA256: 14af249c6843e18044f0159cb585390fb33e3f4eda4d7f3620a69e9a7f9f0190</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.56 MiB (18.41 MB) – 266,873 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e75e6d2f8323528849cc290bf6d1dc1f<br>SHA1: bf07aab77e3ce0f6228e5a683fc4990c34f402f0<br>SHA256: 21147e4b430a95dc09bf7d14a8454c77327a5f490e8729062034a8bc4c97d34c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-31<br>IPv6: 2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.180 MiB (9.626 MB) – 459,683 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b8f981310436e632d67e831bad0178<br>SHA1: 65b8453f348d9353d8a413db5980d6c7d73bf248<br>SHA256: 4bd58ea5b2f1d01e0f5f84383240355551e05b5de3e55d6753a16299102c7ca2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.106 MiB (8.500 MB) – 123,296 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb44b1028de3b2c03df07f460ea24465<br>SHA1: a772025087cc70c34af2829b69e5c7c2e12ebdb2<br>SHA256: aa999829b5dbdb1db5a23758c01a4928dd9d0643ff2e4bb63ed3e2f846ac0e99</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.44 MiB (13.05 MB) – 623,022 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34c571e226525312767b3deef1fd1eff<br>SHA1: 69fdc49923aa3c34b8d30d298c792ec1e3cc1e60<br>SHA256: fe6596bbc1c383e32240ec2a26c31c2e5db5c673b2b4d5f2b3205dfde4e8ab8d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>85.52 MiB (89.68 MB) – 1,299,678 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f0e851a5d7131f910a36d892ceb9a72<br>SHA1: a1d9514f2706fef37e76bd5182233a6b9d33daa8<br>SHA256: 9c32f3f1a97d23e8da95c65cda43fd3d882d322b6ea8eeb8dc380d01c923ba69</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.818 MiB (6.101 MB) – 291,264 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eac94e3e3ab719ab78593afa964f45da<br>SHA1: af19435e4e57c25937afe53d6fba292805882dbe<br>SHA256: 9f6a222c0122eb47e34ee42c495df4f17830c0ee40f4a9921b8535690d3270fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.44 MiB (24.57 MB) – 356,148 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ce580593be34cc4df87bfe5bc81e9b4<br>SHA1: 7a4ab5ae6144faf1b72fae6b2c3be92bb30697c0<br>SHA256: adebdde6726b52568b80d2b7d08b6598f6ecc66c089d6ef69e629573f008cb40</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.7 MiB (179.0 MB) – 2,951,725 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68b1b79e84df6b26076250d820ea0b18<br>SHA1: dda1c9fc8b5b7c2a62cf7a72bf999fc82e55255b<br>SHA256: e664ee3e96917e7ba878660728524375c22f39e4e3aee5f4eda024aeac6910dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,535 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fa4ebcfb46463ed745e92304c503838<br>SHA1: df8c366979b5a5c5a906cf825f26a8437c8d2081<br>SHA256: d04f2b9be41819f8c7cc2d6f4075f927287880b221d8d14a85195ba76acecbb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-30<br>IPv6: 2026-10-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.29 MiB (11.84 MB) – 565,442 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bac0df30c82408acb34ecb47e4fddcd<br>SHA1: 4d15ecb965cede6b4f6c40319af977a31a5514bc<br>SHA256: 2be7788fd1872cd627fea14fc8fd5bd94d7008c4e89f95227ea666a8817e8717</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.79 MiB (34.39 MB) – 498,343 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5238f5bfbb7f29923483fa5a345de094<br>SHA1: 07c50f22d019ef17acbb71f6ab34ab84550f93a9<br>SHA256: 2dfed78af005f7d29fef3b268e8ea2de99d5c28713c2de8338a837e185db40ac</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-30<br>IPv6: 2026-10-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>188.1 MiB (197.2 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94efa7fe7cca6656cc5d15fcbab7ce65<br>SHA1: 7b67b511ee3159f1898176044487b0779f6ab499<br>SHA256: 522ddf6ca7ca3cdcf81b5bd130d561ed9a8cb7d761c3d8577b98daedf9a5342e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>196.7 MiB (206.3 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 926b081348ca9f9ccb3c48897470bb2d<br>SHA1: a35de7f07eeebf05968832a47ba6612456f52fbf<br>SHA256: bec5fdf0bd5bc87d689672086004ac3b57e92b6ec5ccba8c8737d79309e7d0a6</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>187.1 MiB (196.2 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8914fbf4e18827f1f7a556b60932d9f5<br>SHA1: 09857368081dc0abacc908a6a9b42c9375d53503<br>SHA256: 94b1e6b5ffc663a109fb6bb5f11a1697b715de3c8103432686818b73e1cf6d53</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>188.7 MiB (197.9 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8007937400b05a1ad4737e5243b4ce2<br>SHA1: e36749f4772b9f779c82414e1782256b6dbda73b<br>SHA256: 9411bd9a106ba884c3c82af7ce415e8f049443ba2e07b892d612c46727203057</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>237.8 MiB (249.3 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e206c9cb4a9130ced5ea574bfc464f8<br>SHA1: c7d3311f38aaec964f992a7c3cc047688e20de89<br>SHA256: 073c80c14b28530cfd7df3e8b659dd4c76ec1c8f7d4f6547fc75f87b37a3c844</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.6 MiB (195.7 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c17f7c1ae6d41ff77ff4b9de5b7daa8<br>SHA1: 1300cb8e7f406370ddfb489535dba9142967a875<br>SHA256: 7244c0dc25bcdfe93228384a6ecbbf592e4fb55acc49d77fd251c7d889be6b38</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.3 MiB (246.7 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3671fa6b427585a84297ecc656cb3650<br>SHA1: cc87bb6c04c019e185cf1a7f9258262b9522fa96<br>SHA256: 9190a1531dcd3e5477f28cc5e2ef404914e70c2ded1a45e4c2e5cf4971ae6c36</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>192.4 MiB (201.7 MB) – 3,667,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e426307d2f2ee99ff71333ad9690c89<br>SHA1: 4f039a54b788fb00ba012d60c79159e892ba74cb<br>SHA256: 73c2fdd97b41aaf366dbc8f498460f753f51c321acc264b8d813527477f8c0f4</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.5 MiB (209.2 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a58a984bc62aa2389e1d4b4e50c968c7<br>SHA1: b4f80673d30b41b4991deeb7e146cdc334694e8f<br>SHA256: bdd7c9378b7ace18e0c931df3bc01faccef6289692cd8e702438fdba4949d897</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.8 MiB (212.7 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38f51318f7860a76cef157e4e908af12<br>SHA1: ea30b83dad68f8d63703de9272eb85f6eb965046<br>SHA256: b35cb808a1feaf9c8b0e4e1e472e2d569b690d63140b86b4bde6b1f9436a93dd</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f839252958a56f0564a87e4c2be426c<br>SHA1: 69f0bdbed0ae7651dfd491ec0147bd0d9b0b7c9e<br>SHA256: 6075c44cf5c062fbec03bd649f33403dd220e4bdaca720efe795001a4e78edba</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.4 MiB (207.0 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f711d4675567bcc9c5cefe1e6e1cea02<br>SHA1: 88ab2072cb7110f5a43b79a08cbd627a1deff1b5<br>SHA256: 3ccdf7a4f2118b07627a697acd0c046f0f0bebfaecbd1978674670568d2efb9f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.5 MiB (230.1 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c02bee173afc7a153598bd86f3585c57<br>SHA1: 63ac70901cb0bfb09539216b6ce292914aac58c7<br>SHA256: 3f79108192ff9c8a397f89626e6579ffae6163d2e9fb9075e159b971e4a08271</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.9 MiB (206.4 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba6fdcca211de06e09b9bdfe4a84e3ce<br>SHA1: 8b597ea024755aa6c5c44da606e0f5112a5953dd<br>SHA256: 8d310d4fc794455bc5fd005c0ab70085510028aa4d4d32f4f02480cce9780938</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.9 MiB (232.6 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e68ce272a9a0fd0844d7fab1cd971aee<br>SHA1: f7a77565a94bdb6ef279b332a5a8d047a228cbfa<br>SHA256: 8175ecfa43d4ba782a594408e5a6b44384f8cfd95b7904490812368c2b9f9be1</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.9 MiB (209.6 MB) – 2,091,341 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23e5a0ad75bbaa93d22358f3c390b95<br>SHA1: 855a88ef3169cdc5faf814ec09cf8a8d4d211862<br>SHA256: e35ce7d4e6a33c39380eac9032702a9425cbaea64b853c390b29269b20bccf22</pre></details></small> |


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
