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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-10-23<br>IPv6: 2024-10-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.843MiB (6.126MB) – 292,545 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf33c034300d04df41de571eb294940c<br>SHA1: 7f92a253b5e9bcb662a782a7965489663599c2ce<br>SHA256: 2983be4affe0d6291727d95405072a11d37ae25fad443bf813adb842dd93e23c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.44MiB (12.00MB) – 173,873 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20dd028d803b9c7bf1073c805ce797f8<br>SHA1: e11f2d28108f5c16052cdc3399caa11cfa9af4e7<br>SHA256: a0b66dc109afc7d74e1617396e11537b3e05d62afdc278704d177dbf178027cc</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-10-23<br>IPv6: 2024-10-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.220MiB (8.619MB) – 411,638 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e20672d6cde1c8ec81736f3198e21826<br>SHA1: f34e9097c7c602112284277545726a4e65822458<br>SHA256: 9177d226b454d26c3f8aacd0e3d9b3ea98b24d98bbbb2ddfe1356c22e108cb90</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.798MiB (7.128MB) – 103,425 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b07f7c79d64d478489920a742618cce1<br>SHA1: 71545f0bee282ba8db306ab6f7e20e934485b798<br>SHA256: 79318700423b47a1b42dee6eafb2dc5b05aed5b8561e696cfafdbd42b43d594a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-10-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.91MiB (17.73MB) – 845,811 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 001b32a929da8ed2531e027f490be541<br>SHA1: 11dcb077c51701e7f304d9b1082a8598d32c71dc<br>SHA256: b3c539081a3dbf1d3711aaf8424967c888073d2f0d48213bef80219c236e5c0e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>67.69MiB (70.97MB) – 1,028,612 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b1721b0e17756358d053941062d78f2<br>SHA1: 01fa1a376f6e116c527535aa12f69a3c4feb499c<br>SHA256: 227aedf621e38dd5f619ae6c81785bf443c0e22411e2e7577fc433d15a545a00</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.939MiB (7.276MB) – 348,549 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1934c9e84da4a70171fa8a58df792d1<br>SHA1: a9efc628d84ddb0c5ec270a44c413d6e2e413eac<br>SHA256: 8974ef5ef8832adde54bf8eff5b734fbc419e040b6a1ba06eee6302c327937de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.54MiB (17.35MB) – 251,406 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccee8212e47dad6f6d37a7875599a267<br>SHA1: f12a6f633e3f93b21d90f94868a5dce0099a8f68<br>SHA256: fe5508fad3836313166aa43d498d12d6277cae16fef7835d5e92fdcd53bb2de4</pre></details></small> |
| | | Full Location | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.4MiB (197.5MB) – 3,289,697 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a0426270d27872fad498a291900b10d<br>SHA1: 4f4a7ccb4910df8d359d2ad76a1bd80c4be37d61<br>SHA256: 6869bc8bd2854724fd6be12e1a0efa4bf028d598fe1d116783216884c78d9f3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>362.7MiB (380.3MB) – 3,515,904 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b742d904c555f3e530341708e40522<br>SHA1: e367baa432e03a59b81c286e5f9bfaeeb0617eec<br>SHA256: f946dbe0156a23fd65f4c67f8c95dfc19e8984bc7f84d8323fc5c478da017055</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-10-23<br>IPv6: 2024-10-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-10-23<br>IPv6: 2024-10-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-10-22<br>IPv6: 2024-10-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.900MiB (10.38MB) – 495,893 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 745d81a7e8e0c60eec8cde8d1b3010f0<br>SHA1: b4474d97af551fcc616966b0db52c348380497ca<br>SHA256: 0cc7e24eb5dac4048e3ddd8e57c998d84242ec7440e16e3a983a756f93ee6cd5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.33MiB (32.85MB) – 476,047 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c586c07a519e8b15201457ad57efe5ac<br>SHA1: 181d2165915612f5ae867ffb9cc7a12dad1e50b0<br>SHA256: d829a91b05dd9f31cac4994d1e5e7d2db3a138aaf4bf75179667d1b77b4c4f0f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-10-22<br>IPv6: 2024-10-22 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.1MiB (180.5MB) – 3,397,274 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d78889c6a4aa2a2151813fa02045bede<br>SHA1: af6dab76f80ec18ac70314a616dc1d2df25e81f5<br>SHA256: 6b5c3b08e4a5462dcb369bea974c048cfa3d0e0d86e86c006681a4e06011885b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.0MiB (192.9MB) – 3,397,274 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9065a70f5fb817f9dc88ecfd79e9da5a<br>SHA1: 1b530925cee8b5db177ef325cea3189510c6ff11<br>SHA256: dcacb88d59e697223b8eabb9326fe02528ef7a88ccdfd4ed55af89aac5762685</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>171.0MiB (179.3MB) – 3,397,274 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf64328d838d844908885eda66a9d4f9<br>SHA1: a7e36dcb30b7f8f33170bc0aeb90ba437cbf7d91<br>SHA256: 0ac9acd02d1e8a72bf3d23887dce7cafcf59603ab58eeddea6ab33cef4cc0899</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.7MiB (182.2MB) – 3,397,274 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9bfadcc6c3122863be9c213fe0aa7c7<br>SHA1: 9b6822b8eb36b1bb67f8c6c50fa1b3b3d3114117<br>SHA256: b99775874a7c4b9fc8c7708ab25830a3eec27c63d1b2f89c9789ad5a6d58d287</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.3MiB (229.0MB) – 3,397,274 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4546135b0c76d86fb8bfe393e0d833e0<br>SHA1: ee9f3f6dae404f33c351557cad64aaf25680c06f<br>SHA256: e3a01d59a5c598b2cfce8917a4526e87e2b415e3c6a9b68d6499511455da1408</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.9MiB (179.3MB) – 3,397,274 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b563a7fe8ff3188ecdab5f97052c7c9<br>SHA1: 04bbb89506fd539c88bfc132ac390628fd239aff<br>SHA256: 2b7a8a13fbef9647f99bad548011b040bfb85e034ea739385b53321b9429e0bd</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>212.1MiB (222.4MB) – 3,397,274 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1bbd1df6013e68d5c53f46e1fb49e8d2<br>SHA1: c69e743f339a2d807957854afd214e2724aa6d50<br>SHA256: 06313b1f6e74f9377eaa6effa8da31f74933cb61e5af79ed32f959f99089af70</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.3MiB (186.9MB) – 3,397,274 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72b84183ed27c27a4603c1ab2852bf4a<br>SHA1: 2681d091dc1b67f29e9349311cfe7083614d9e06<br>SHA256: eb35fb5dc13d683e58422d056a6c58ee5051237dede6c71eb86a39ecd405c7ce</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>158.4MiB (166.0MB) – 1,666,426 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0b4dcba0a9b88065f3bb8c84ea3fccc<br>SHA1: 75097a6c14931074bd6986bad3ba4167659a7ed6<br>SHA256: 8e6d6734ddd18e535e293c7ff7954c91d59d4ad50984fe2e9c504c4d60546c22</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>161.0MiB (168.8MB) – 1,666,426 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 133e7490ba0aaae4338c52fa8da3d1ca<br>SHA1: 06201a631dcbe29e50a563786185f152ab5de769<br>SHA256: 8e5d8fc38927bdd6e3e69c1973a6df9f6d05a5399ead71732ba0a66f2a4e2890</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.0MiB (162.5MB) – 1,666,426 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfb509aa183d3bff632180d5206cec30<br>SHA1: a5d83511d065183285468f914c6d81995375d10e<br>SHA256: df1890e479aa94ca27fc0d15e62ab6d68943b1747c16ebfd726f5df9ca9f687e</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>155.2MiB (162.7MB) – 1,666,426 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 182f6fdeaa8eb4a3b32f17853f990290<br>SHA1: fe4e178e4831e329b6fcbdcaed92a330e457e8e6<br>SHA256: 84469c8cff183a403a9df0bc7f92b97c52ee8a2dc70d5e73f62a77f015881e3e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>171.1MiB (179.4MB) – 1,666,426 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d34111a6cd0f4a1b67ea45c722161961<br>SHA1: 1534b9ef75ca8add2e3eb7d4b4c170820885d557<br>SHA256: d06c1db7245903398203cd7fb3ecf236fd06127d3714d84bb265b803d1430e15</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>154.9MiB (162.4MB) – 1,666,426 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4276849d202898dccb551da2e587afb0<br>SHA1: 9bda33d9ab4865be81794d308e3f9e1f57218809<br>SHA256: 7ca54d035795c80ebacb6b1d07b8c8c560ee9b2b67ff189ef4d8462532c734e7</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>174.3MiB (182.8MB) – 1,666,426 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bcccd6405692ea68df8be508cd5f9dc<br>SHA1: 7f4797e0e7cd34e58f358fd5ad48f0a2c162d135<br>SHA256: f8255c867be9e9c1a7061ee23d10f4ba74d2a2a124836ed9163cccd836c34be6</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>159.0MiB (166.8MB) – 1,666,426 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a38e73475a6e15a34bc35a13d42932f0<br>SHA1: cc1128e3fd8b85256d7e223047b041d2a584f61b<br>SHA256: 42e68e64d4cdd3b12f0710dcc7d76ec6c4fd5b4332efcf22334ebba43cf0abd8</pre></details></small> |


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
