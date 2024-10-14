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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-10-14<br>IPv6: 2024-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.881MiB (6.167MB) – 294,481 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71d63b2173f20e63731d7a849867d072<br>SHA1: 87ef2d5ddb2fc136b19ece2314ea6ee4a1d6fa8d<br>SHA256: 43b06919237916acb533c796fa81987896d94070949432b5882ee609032adec0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.60MiB (12.16MB) – 176,277 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2e570a595a15bccf543b60b7e939c5a<br>SHA1: 4e360ad4b0e7b1b433eac8ca2f936a66f4c2b88f<br>SHA256: baad945faadd4df90774b0e9634d97d3f4ce896ae30d37451e0521284883fb0a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-10-14<br>IPv6: 2024-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.215MiB (8.614MB) – 411,385 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78557bf589bdee330e68a3f81dcaf051<br>SHA1: 6a7634d3de8c81eac2dc785d9693a3e287766a8c<br>SHA256: 54130df628d02db550cfb7e8f9954be20e9008d8ed656ce1ce72ec7caba1fe8c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.802MiB (7.132MB) – 103,482 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d8fd555286d0ad1d0e69d92affaabc8<br>SHA1: 18a853f89fae66dbe83911b6a1e00d125b53f12a<br>SHA256: 3357d78361d696c10a1c712545983ed8d0e929c2638fb896a85c9e4f8a3be029</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-10-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.72MiB (17.54MB) – 836,679 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 134291724898aba7cf7951f5484507ce<br>SHA1: c9333adc2017f2aa2a917bd2ca6b258d48bcbeff<br>SHA256: c2a002a66359678c6296132986cf3ac4f252be3d0baa08aad6441a966b7304ae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>62.25MiB (65.28MB) – 946,029 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e70858380c075bedfc3ea7487aac8b70<br>SHA1: b403d6578678f0e358b9b3e5d7bc7aede8bb294a<br>SHA256: da6cca067f5efb919eb2d0cde0d1cd654043570261a59d5d986dd5db9f28c874</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.939MiB (7.276MB) – 348,549 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1934c9e84da4a70171fa8a58df792d1<br>SHA1: a9efc628d84ddb0c5ec270a44c413d6e2e413eac<br>SHA256: 8974ef5ef8832adde54bf8eff5b734fbc419e040b6a1ba06eee6302c327937de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.54MiB (17.35MB) – 251,406 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccee8212e47dad6f6d37a7875599a267<br>SHA1: f12a6f633e3f93b21d90f94868a5dce0099a8f68<br>SHA256: fe5508fad3836313166aa43d498d12d6277cae16fef7835d5e92fdcd53bb2de4</pre></details></small> |
| | | Full Location | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.4MiB (197.5MB) – 3,289,697 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a0426270d27872fad498a291900b10d<br>SHA1: 4f4a7ccb4910df8d359d2ad76a1bd80c4be37d61<br>SHA256: 6869bc8bd2854724fd6be12e1a0efa4bf028d598fe1d116783216884c78d9f3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>362.7MiB (380.3MB) – 3,515,904 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b742d904c555f3e530341708e40522<br>SHA1: e367baa432e03a59b81c286e5f9bfaeeb0617eec<br>SHA256: f946dbe0156a23fd65f4c67f8c95dfc19e8984bc7f84d8323fc5c478da017055</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-10-14<br>IPv6: 2024-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-10-14<br>IPv6: 2024-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-10-11<br>IPv6: 2024-10-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.837MiB (10.31MB) – 492,762 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b5bccbd8ae43646f3034421d6507b92<br>SHA1: 7cbb87759fbdfc18ac7c9672e4ea69508679825c<br>SHA256: dae56167268345627d21d34de006e9a23f0b856ecfa76398df3870d919c1fe98</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.28MiB (32.80MB) – 475,369 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e37fad24d90afe20e1b058e435ec7704<br>SHA1: 843f51004bb1577ff51b270992ca5d2884d23569<br>SHA256: 3de52806f0248d37ca51d891c77e27fffacce2113bd86ad15d194860f4e4080f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-10-11<br>IPv6: 2024-10-11 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.1MiB (180.4MB) – 3,395,051 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27a3ec6ad8c4e637b12f6d4ed4aa7552<br>SHA1: 6ff4a87a720789a1c14f0273247c9fccc0bdbcc5<br>SHA256: 35896ae634e035f90f5138721334fb0bdfe2429fc88037f8602ea3e842c2a133</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.9MiB (192.8MB) – 3,395,051 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7ee5e4dd6e8f69631574ef697f4c8e6<br>SHA1: 6e2b5209ef81870ae10ce94d2ec9970c491e045d<br>SHA256: c1caeae806d7027d497440dc4693ee263909a6c416ab6ad6066522c9f328d19e</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>171.0MiB (179.3MB) – 3,395,051 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 635d9ef7ad622feb117f69f17b8a604e<br>SHA1: e966592a1f2fe9f84dee105d96fe65c1663e4886<br>SHA256: 60d20bb174e879b753338c558abbcd136ff6bca8c6e2d93db429880ff84f9069</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.7MiB (182.2MB) – 3,395,051 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b5f50204330fcdcdef67a65579f1feb<br>SHA1: f9a9f6a1782f1d05150c5e9f80ae2a5e47f9e80c<br>SHA256: a277948c597393b126763b7506c2ed6c26a431d022c47a148117debf4ac330a7</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.4MiB (229.0MB) – 3,395,051 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 802324f2d26d4ab1b96e57029eb46e64<br>SHA1: 1849656de481753abc175f91af4c2bba6c028424<br>SHA256: 1fb679ee49b6e1631266ab557235b213d03a74e9fb8839843b86cd6b1cb19f9e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.9MiB (179.2MB) – 3,395,051 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35a76ea264bd635cec3d3c9feb2ad300<br>SHA1: 26e04622ee6b58e88a58128d8f6c6f46e842d2a3<br>SHA256: 9f4a167a66bb37dcb39a41a57f71eae2959a70fbde448812e125973a1016b217</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>212.1MiB (222.4MB) – 3,395,051 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89a3cef564d21ac59395097e5ed48ea7<br>SHA1: 52876047d1ec962589b69b48dc01e9314290172e<br>SHA256: 2224dc756d60e4a17d99299f3a8718f861b90a3e99201133efd65fd2853069a6</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.2MiB (186.9MB) – 3,395,051 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51e91d57ed54c9254797123e9098a649<br>SHA1: 74d7f3840a9231fb0e13be5ff59f64a865907f06<br>SHA256: 649db197b9c90a550b9fa4f2315acb8aa784f1a291491256f107a793518a93ce</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>158.6MiB (166.3MB) – 1,668,146 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58a1d13414d7a93721190364407a81b1<br>SHA1: 539bea3bcdb120778bba6a5bdf323d91a5e71f89<br>SHA256: 32c1339df5114c6e2661301771ba5b3cb0e0dd6828dbfd1639dd5c05c1552238</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>161.2MiB (169.0MB) – 1,668,146 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fe65c06321275ab25ccdb6c913e8f7d<br>SHA1: d97a5fb7e0aa16e763823900ffd7096d0d7d5905<br>SHA256: 2d00d67c22476f1a00b283de86515aef9e19834c75e4eda468042c2e268fcc2a</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.2MiB (162.7MB) – 1,668,146 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e4d194c40e04786a7110ca00dba58c3<br>SHA1: b5ca1345cd8acfda36cc5d4353c04eba9fb18436<br>SHA256: 60dd247cf0b1b8d60a846bb5c0c94ddfff85272b5dd65c2599dd80a1fa5dedaa</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>155.3MiB (162.9MB) – 1,668,146 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e82ee7fb16b6f1deb96732c611413c55<br>SHA1: 73b93a60877933811b75ee4ea6287eb097a8096f<br>SHA256: 6cbb76685a2de8e3a255cede595c2f621a1a1549a69a2de528315c625d83d04b</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>171.3MiB (179.7MB) – 1,668,146 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d5ebb0c8b700efd173abff25ff2bdf6<br>SHA1: 94cd8bf2e60a6ca83ea4343ac73f6f1f259a485e<br>SHA256: adee1c311ff69190d600549deb4266c942677b3276e5d5a85384c44997b65a02</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>155.2MiB (162.7MB) – 1,668,146 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e763540d1e1a0755362aaebad8eefc80<br>SHA1: a4f5ab2491e4f3ea7117cf491811af61b7165ac9<br>SHA256: 3717ce8ddba6d47da1879493b19111944332cf41f4fd90f078899a38ac66bf39</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>174.6MiB (183.1MB) – 1,668,146 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5988bf9dd6b6b7b786d66960ad7019e0<br>SHA1: 5ca3001f260bc0764a351de51d5817e5bc0df161<br>SHA256: 7db44a8648a02987ae6ffe0910bd98867f701e686722526fba59e5a345d52a95</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>159.3MiB (167.0MB) – 1,668,146 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bdec43ebf3468d9cdf1e575c8a790a3e<br>SHA1: e065ca10cd9a9a1ed6118519629b37a8f52409e4<br>SHA256: ce5b2b176c43cc6ebdd1851035cfcd840a8639d52f1c05ef40d53969f7d1e7fe</pre></details></small> |


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
