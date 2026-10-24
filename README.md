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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-24<br>IPv6: 2026-10-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.675 MiB (5.951 MB) – 284,051 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c026d32960dee3b068ca56cc0a6b412<br>SHA1: 02a921542ff2e712d6d13d023e2a2c07988a17e5<br>SHA256: 217310f821ebd2ed5da9ddb1a5914df4025aa32368dcd1f9ae5a3d97eb269662</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.51 MiB (18.36 MB) – 266,150 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b0ef1e0bac3a410b9909475c3298764<br>SHA1: 7d93dda66b16d4bba7fe1ba935c3b8d09576076a<br>SHA256: 503891f443f0e7fea2184194ed3a1be09a206f08183cd0d32f3808dfb98c477c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-24<br>IPv6: 2026-10-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.172 MiB (9.618 MB) – 459,289 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 662eb9538f10032a0d2dde26512a4d42<br>SHA1: be1ea210dcd5263bbb27423700407150e06e4f41<br>SHA256: e13d1bb5dc61bbd1c1fd9a108f5aa1e7fb8ea3e9104b453246f882ec435f5f5b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.073 MiB (8.465 MB) – 122,795 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cb8da904cb48f9cc4dcc203d00a4705<br>SHA1: 59a85d429757a943a3fc025dffcfca666f0158b9<br>SHA256: 7660363917f81ca0655575cf1231582a17f080ab0851546440f4d9e53724364f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.37 MiB (12.97 MB) – 619,135 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee91d79eb1de9156f08c8504a179e606<br>SHA1: e332591289faae8db8807f5dca6bb9b747367369<br>SHA256: cb9c2b91e9a25ca26d0edd2125b3440c0b698a8f8491117b99645efd19fe7e37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>81.26 MiB (85.20 MB) – 1,234,818 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67d63ec0985d8df2c1b38334a3a148fd<br>SHA1: 75434d891a520bc0bfa542882ed57728728671bf<br>SHA256: 930b2249f924b41cfc6bdfe6fc484198c9a1ec42ee5ee660fff15592e714f53f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.818 MiB (6.101 MB) – 291,264 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eac94e3e3ab719ab78593afa964f45da<br>SHA1: af19435e4e57c25937afe53d6fba292805882dbe<br>SHA256: 9f6a222c0122eb47e34ee42c495df4f17830c0ee40f4a9921b8535690d3270fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.44 MiB (24.57 MB) – 356,148 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ce580593be34cc4df87bfe5bc81e9b4<br>SHA1: 7a4ab5ae6144faf1b72fae6b2c3be92bb30697c0<br>SHA256: adebdde6726b52568b80d2b7d08b6598f6ecc66c089d6ef69e629573f008cb40</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.7 MiB (179.0 MB) – 2,951,725 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68b1b79e84df6b26076250d820ea0b18<br>SHA1: dda1c9fc8b5b7c2a62cf7a72bf999fc82e55255b<br>SHA256: e664ee3e96917e7ba878660728524375c22f39e4e3aee5f4eda024aeac6910dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,535 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fa4ebcfb46463ed745e92304c503838<br>SHA1: df8c366979b5a5c5a906cf825f26a8437c8d2081<br>SHA256: d04f2b9be41819f8c7cc2d6f4075f927287880b221d8d14a85195ba76acecbb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-23<br>IPv6: 2026-10-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.27 MiB (11.82 MB) – 564,196 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01d6c14aa4d7de4f6b5307be12b12cef<br>SHA1: 746e2fe40c567be6e0e630287c1ed28abb0b40a0<br>SHA256: 7c8db6a6430051847bef7e87a443ae7586b230613bfbce1ffc25831406fe259f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.86 MiB (34.45 MB) – 499,295 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba812159681852253dde9602cf510c93<br>SHA1: 00912bfb61c2a022bf3cc8283667d4b068d39f8c<br>SHA256: 02f8c11b93f7075a0c7b796e001337ff65415d58e538887d08c954608bcbec31</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-23<br>IPv6: 2026-10-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>188.2 MiB (197.4 MB) – 3,669,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 310b1ee9e555d070fbbf30cf71fd81d8<br>SHA1: b0046ef3c5c831257317f56759fd8f1f20d974c8<br>SHA256: 085d8b2f1704fde3ca9fb6157afb82a2e6e18ffbc060983259990271088d8bac</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 3,669,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab0850e8fc4423ed7670daddb5cb1557<br>SHA1: c9ca551f5d2486580fcae4101ee73ee04df76043<br>SHA256: 4709bbd1ad899dc24a8803814464a7fcacf15bb6acb8b30b07f0f96636146b77</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>187.2 MiB (196.3 MB) – 3,669,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82673ce3498160a886151ada7620f3e6<br>SHA1: d1d401068d69920dc9f568ae697644d8d96a1beb<br>SHA256: 6152ab07d1e890df44cabc0bc68750bbd796c3d01c5b6b14e4736825f3ac95ea</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>188.8 MiB (198.0 MB) – 3,669,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ea0ee4bd195409f17051a57ac30e99b<br>SHA1: 8a2685a1d214dc7fd00dab4baf6cd69a7671d6fd<br>SHA256: f3eeddc98b4ae22fe285c6021a1450305e4a449881b4d1d5c12451d880270fa7</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>238.0 MiB (249.5 MB) – 3,669,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17974a6e1778fd688fd8b256b199fc85<br>SHA1: 7812e9084b6b783409a1b6cf89974aba292ab1da<br>SHA256: d52aebe46d712b971e0fc3e4f5a386cf42b26e26af4b0dc93c134522e012ae0a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.7 MiB (195.8 MB) – 3,669,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f47bb393734cf90472d36cbcb27a97e<br>SHA1: dc3a7e0b53f2ab9c19e3bc71e7f57ab228b0472a<br>SHA256: 880a7ac43ffb8e9c270e023af2988eeacf1a223e2f8097d43000aec87a97ff76</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.5 MiB (246.9 MB) – 3,669,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d9e324798c9bd97648ea5fdd1040d4f<br>SHA1: 3b7ec28f2c377588e35577a88bcc4e1875d43b0e<br>SHA256: 92cb8baeebb792e978f5008e1517a73d02e53d3430716a4083f864262197dd44</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>192.5 MiB (201.9 MB) – 3,669,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a75cc7a5e2af24603aca9234d9c2ffb<br>SHA1: 92e57699adabc86b64de1f169ac7698e8f91ad13<br>SHA256: ef0e850670637e7621a4bfff00e705ed3b8e3378988e642d1d4d863569204bc0</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.1 MiB (208.8 MB) – 2,086,240 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f26ecd8b8e3089a5a11ffeb838de760c<br>SHA1: 9acbe4e70607fa8921ff4451e64d7797af450255<br>SHA256: deb77a40efc492c5406a956ee48352f2ae752b7c46d7015247a70c4f52a0a948</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.4 MiB (212.3 MB) – 2,086,240 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59e302e5b1de1f7ae5d63586bc7543de<br>SHA1: 4b8ad74deba6d16d86f21329d2535bdf1167f060<br>SHA256: 9bdf3d9ebe45f223f6094293b82d53be04e6677268841c36dd7831176dd00321</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.5 MiB (206.1 MB) – 2,086,240 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5563bc0aeb99ea3e98f492b2224b9ba<br>SHA1: 3875434593a49a3a5c0fd6f8adf741e108e27b75<br>SHA256: 03491ca3d97a84fa872fb6aa11c09ac29b1816c64531be94a676298e6e9c8d0a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.0 MiB (206.6 MB) – 2,086,240 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e60e94c3e763c8596f07a291e0cb2477<br>SHA1: d8ea34b8682ae1f1d1824576b27604c9b18f4d27<br>SHA256: 3d1e0023b675fc995ebf5924b1d9e3fc267fa949f8aa902ff59a5f7e7c1bd018</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.1 MiB (229.8 MB) – 2,086,240 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85d7d0a81d0db360d1f29dd512299f09<br>SHA1: 4e16a49417af579e65fd70a544867c591232884e<br>SHA256: 4f7717ad8a1b71ee22d0c5606c32316c098ddb062fd9467f67333aaa2576e7bb</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.5 MiB (206.0 MB) – 2,086,240 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7006e8a2805171ceced190a70f25919a<br>SHA1: f730a94b208dfa32605204fa5f902e7bdd0808b3<br>SHA256: 0635b66c4cb51384dbd760d6d45566866088a1ade1b7277c5aea072ccd572e0e</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.5 MiB (232.3 MB) – 2,086,240 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34f3b33f543ce9c1a8f3ce63b97d1ed1<br>SHA1: 748ecb6785a5211fe3c3be8214ef0c2bea147c7b<br>SHA256: 0c13a4d2b85b74be954e0898aec6edb634f49d7249c2294915fea7d9b4378f17</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.5 MiB (209.2 MB) – 2,086,240 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73df835a1e319b03f668114e206bcfef<br>SHA1: eaeffa83bce1205e4179e55b73ad57c2576fa177<br>SHA256: 10f3be48ddcca36c5c9232fb281dcc62fc2f81be60a91f8125348d6b8afe8c05</pre></details></small> |


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
