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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-17<br>IPv6: 2026-10-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.655 MiB (5.930 MB) – 283,057 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d374b587d3cf299755d425707e93a723<br>SHA1: eba4a9b75661da4a4a1235df8529102349f77394<br>SHA256: 471d4ca8e8651b9770c128ee064e540b7bf892029d1debabb387e844cd94723a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.50 MiB (18.35 MB) – 265,950 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32c03d2a8a3b81e4a18c9edcb8dbb1fb<br>SHA1: f351cca723c3a24558951319a13462f7c13fe042<br>SHA256: 88cff94411534905c607da396034cd57a5ba3b85a83c55b97277cf84cf33559c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-18<br>IPv6: 2026-10-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.164 MiB (9.609 MB) – 458,884 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956a6c7c7ff70de55e34b0963f926f78<br>SHA1: bc0174274aff6358ed0e6387c144e33c85cfc8a9<br>SHA256: c88ee5a3c0f07ef7df5c8853888d0df1f8296d4027e6fa3d8bbf3dd6fcc2ffc6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.136 MiB (8.531 MB) – 123,751 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6d7ae183db837dbd50fa712328382e9<br>SHA1: 1bd26b85c885e0a79ee7939cc266e848c4c3b929<br>SHA256: 31d56295710f45d690093b31cd5ecedc6f1cc5f75c887f6eb95f036d7d0d7037</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.34 MiB (12.94 MB) – 617,985 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b49411f4f4a44f01189c19e0de983eb<br>SHA1: e617f58aa0bc08b190fddb7f9de834a25af77222<br>SHA256: 2a345789cc8ec6ddd36dd1bddcedb64707090ff5127a3d58b13c011ef2cad026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>76.73 MiB (80.46 MB) – 1,166,034 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a13d148e4d6fd4caf1547cec2d6b77e<br>SHA1: 18fa4d60d973b0808d984e4e99bd10eea56f9bc4<br>SHA256: 8d86654af553b668229e81f54fcf8f1dece9f80ab3149771e2160d0e53c3dd28</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.818 MiB (6.101 MB) – 291,264 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eac94e3e3ab719ab78593afa964f45da<br>SHA1: af19435e4e57c25937afe53d6fba292805882dbe<br>SHA256: 9f6a222c0122eb47e34ee42c495df4f17830c0ee40f4a9921b8535690d3270fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.44 MiB (24.57 MB) – 356,148 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ce580593be34cc4df87bfe5bc81e9b4<br>SHA1: 7a4ab5ae6144faf1b72fae6b2c3be92bb30697c0<br>SHA256: adebdde6726b52568b80d2b7d08b6598f6ecc66c089d6ef69e629573f008cb40</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.7 MiB (179.0 MB) – 2,951,725 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68b1b79e84df6b26076250d820ea0b18<br>SHA1: dda1c9fc8b5b7c2a62cf7a72bf999fc82e55255b<br>SHA256: e664ee3e96917e7ba878660728524375c22f39e4e3aee5f4eda024aeac6910dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,535 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fa4ebcfb46463ed745e92304c503838<br>SHA1: df8c366979b5a5c5a906cf825f26a8437c8d2081<br>SHA256: d04f2b9be41819f8c7cc2d6f4075f927287880b221d8d14a85195ba76acecbb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-16<br>IPv6: 2026-10-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.28 MiB (11.83 MB) – 564,751 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16b91423948def3d142feeae2b8ee5d3<br>SHA1: 4ebb0270a016de8858292d54717e8aa160cb478e<br>SHA256: d95cae8e4eba80f26fb86f3af272716c527f5ec3699f42769878d352c5bb5143</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.92 MiB (34.52 MB) – 500,243 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10cb71bb088267447c77540ac47b7163<br>SHA1: 575cc432814a7f829605741d5c9154e2d3a2e86d<br>SHA256: f9fd673d84477497d796538f926f02e68d241184d823a969c2b1276b0202c461</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-16<br>IPv6: 2026-10-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>188.4 MiB (197.6 MB) – 3,673,335 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbeca4861b7efc516cb19840a2f552e8<br>SHA1: 787ec31a3a5bcdd9696eb67aef816f9f5278f6c0<br>SHA256: aae9c4a01ab6807a9619e61ad895d2e3455c08a7c26d034b2b0e3cc840639486</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>197.1 MiB (206.7 MB) – 3,673,335 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 954f12e51e8ca558c9c821179aad080b<br>SHA1: 31c170f8c4c38e9dd36a62e6986b519c982a162f<br>SHA256: c86c1e1118f402db54f7b3870af0082d82615dfb11c76d17ebfc100b93c541cb</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>187.5 MiB (196.6 MB) – 3,673,335 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc0ddda722e783fc8e4c6d79effe2fd3<br>SHA1: f7a45bee753726d918beded06eb7e03120c722f4<br>SHA256: 15e5fb56cedb5f64b83e91abd9efb070f82b3da97c295d11ab67b09858cb10da</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>189.1 MiB (198.2 MB) – 3,673,335 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5796cf52ca2d9ee0d609a78e7c9ba5f1<br>SHA1: d537f65ad84c2cc992dd0a11652e916d90261e55<br>SHA256: fa7add4fa02cab5a7270b17734593007d7f612eb4c172e17e8a3ede0a80bc200</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>238.2 MiB (249.8 MB) – 3,673,335 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 484397e9abb2459bba1fbd679d57cdca<br>SHA1: 7f610f46d5ab51f1c21a9526a3cd68c8b1e9e7df<br>SHA256: f0f6cfb6950d183803063cfea67d98d1f83bafbf74a6ae4a86f9feb1a529e592</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.9 MiB (196.0 MB) – 3,673,335 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67b7d61dd275c3f959348632a7a7a051<br>SHA1: b939362a18b38d1ec27bf958937aad57994a3c24<br>SHA256: 2f999cdc3085d97de5044acee83762f1ef496e92bc2210a95af7116f149c02b3</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.8 MiB (247.3 MB) – 3,673,335 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 916ceb9cee18f5177a8068ad21d7d142<br>SHA1: 768ea7698ac0fd545c3ab89b4a844f1c39e7a7be<br>SHA256: fab561f804492b3f0d7b164579b3b5a797f53abdc8a6bc6aeaaf140f377b0b6e</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>192.6 MiB (202.0 MB) – 3,673,335 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c170211812ab7af0b4481749ee93181<br>SHA1: 74db1359cc8fc516bdbd71ac9b84083aa5a6a815<br>SHA256: 30b8139c0bc44cf792cfd94984ff38de775a95f542f80d3ff6884dade817049c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.6 MiB (209.3 MB) – 2,090,886 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 411d0d90ae31c0e4d760a38139ec7ffb<br>SHA1: b3570fa9902a7a3d07fc72cd6b6743b51afd930f<br>SHA256: 367195a21c45eff17ba01d123cf9a464d7df863d8e239f1aa7400cf04e5fa7fe</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.9 MiB (212.8 MB) – 2,090,886 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 160d2b4e23d8068da8a7e72857fe5f7e<br>SHA1: 28d9c6add9d63559330b27a7101e7462e9f2975f<br>SHA256: 0bd5923dc42e64ab11018c803464c6378561aa872e84fa277af980720e44bad9</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>197.0 MiB (206.5 MB) – 2,090,886 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf59a0af3371c54391a89ea545953ab<br>SHA1: f2736b2cec2ea67898c4f1ef1de114ded02532f8<br>SHA256: 99a2cc8dc71b9c2b05fb1ac74e5c433f89dedaf7b9a1ad79544f0ea37d744cd9</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.4 MiB (207.0 MB) – 2,090,886 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdf0b4c40f39fb2592b3468d8dd2d7d5<br>SHA1: 96287145de2387c2603fdb233d82616d376d81e5<br>SHA256: c69bee774db1c52f57fade3dc845ef8e458750debe29b6d41bd80abf2a3c6a46</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.6 MiB (230.3 MB) – 2,090,886 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a41537f094b41315bc7d5cf891a47623<br>SHA1: eea6cae0759c1fee72746cd16c69688b97715919<br>SHA256: 97cf05862d3b18de7193a6e929df1fe4d92dcaab002fac26293a8338cc88aa2d</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 2,090,886 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31ed61efc6c10c03236da2f66bd99c2d<br>SHA1: 7846b68ab76a3db3adac16f55c9aabd870ef7095<br>SHA256: a9389936156e2ed34088fa26c37329b956d649f48d4f0c03763102f68f808c6b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>222.1 MiB (232.9 MB) – 2,090,886 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e150cb77ee0ed25460e1538b09404b10<br>SHA1: b98dc6e38e82e51232aabd411f31469091bf4042<br>SHA256: 57a3966ae954e354fd0d1f608fd5b2e7dadf8888816de22965333b36333aa453</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>200.0 MiB (209.7 MB) – 2,090,886 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26a5bafc6ffc0a14fbb7a39120517db2<br>SHA1: fee65a6889a39e964b6c05e0fd8394a754c15dc7<br>SHA256: 20d3038e058731dbac5b6abff4d9ee4f5b84e7e9f29eb07310159458fca37861</pre></details></small> |


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
