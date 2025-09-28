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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-09-28<br>IPv6: 2025-09-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.297MiB (6.603MB) – 315,290 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6df0ddf023e9f1e5c0a72ddd0995aaf<br>SHA1: 405f4fa89a63d77f0664ab470d62bd3506c613c1<br>SHA256: 91a3e85a4be847c9ab18d693e7dedd398b84f6f6433a4e3bc746ff9c834d76ce</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.90MiB (11.43MB) – 165,686 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f82f500d83e90b5767b0ce737687e52<br>SHA1: 9dd793b1a97b7e44ee493f0c11125e7526cc230b<br>SHA256: d5395e1cc7084a0024e5933f13842c918a14893398859453ad32924db694a02a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-09-28<br>IPv6: 2025-09-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.653MiB (9.073MB) – 433,274 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa305dcc5334055522b3a4dbe04bc9ce<br>SHA1: 64b8a10092a17bcb2d30cf5d14ffda52e73828b2<br>SHA256: 9c87d974820e1680e773d11106b5d4b9dd3b6736899d2defc51f5a7a4bb473d5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.317MiB (7.673MB) – 111,311 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 459257c91f7284b39aa525ced9a51060<br>SHA1: 15937b949ae8657bc0b1e54e3768300865d05e77<br>SHA256: 9931923508bc0b3b1e25f16eadad69371f65bf6f1029f3186da8154d696671c8</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-09-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.27MiB (12.87MB) – 614,291 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e6ff03a0957627e3953f35dabc35e4b<br>SHA1: 6730c804559bc8f3010690439ce09173a701edd2<br>SHA256: b1f95964d5f51d6fe82de6263a50208ad791c2b5c8de2d02ed44ec6be6ba4034</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>83.38MiB (87.43MB) – 1,267,129 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3912f4aa7deb0b4fe1f0249ae5b8160b<br>SHA1: 2b8fdd8948b71d635e16fbe83b390d324b5a68d1<br>SHA256: 2107c91cbff3df2dab91a91657847dce517badc6e41ce7383b53e60aa8de9082</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.825MiB (7.157MB) – 341,824 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dae1f431e9d10a462dae84888365884<br>SHA1: c0cc78c9aa347b8d712850c57537fc0dc50f1dfd<br>SHA256: 3f57c286e145770c2ac0d5d3c14088a919db312a222bfef2cb85941399367b2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.93MB) – 245,375 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f7e3a8bff7f09ee7cfd621ef044564b<br>SHA1: feacd88a985ae6ef5d668ffcf375eefeed7948b4<br>SHA256: f554d05a841ea0162859a713eecebb3fb0dc814ea2d39b91150dd45627c31fed</pre></details></small> |
| | | Full Location | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (217.0MB) – 3,624,799 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7154efa553f5c77576cadbc5c42ec9c<br>SHA1: b63ba0a183e94bf6cd1aa8a15db942b52d55841e<br>SHA256: 00286d8f1fc1f8f801a25f123213615fc637aa494c49fb2537047bdab4b1aaed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>448.8MiB (470.6MB) – 4,362,462 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7375867bcf97ba785ec1fa3d092fb0ae<br>SHA1: 37a209470da0930c2308178d77c0c1cac376d849<br>SHA256: df10547da1aed72a27d58d5fbd860b66dc9bfc40df34c5dcca2b7da7fdf24ca0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.185MiB (5.437MB) – 259,491 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50d719d1853e86e8da56334658c35eba<br>SHA1: f811bb310275e7b7653fa90e869cf112fe526acc<br>SHA256: bcbf902929f7d249538703a8dbbcc64d8fae4900531479cf0e3063367391f946</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.57MiB (23.67MB) – 343,010 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff677ddad3772ab36197d2ef84bf42e7<br>SHA1: 8be3a4e0ee14af3d087f70294904f7aa883b6743<br>SHA256: 0f288add4994bc16d4d6387a5818de57f3def88cb259fb8fe4a8f6b507e4c820</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.4MB) – 2,949,463 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ec6ef92605faf0c8ed3176f371a4f89<br>SHA1: cd21e0629e442168ad794701d10639489e2d7e3c<br>SHA256: 3470fc0e8a3432aae0bb7caf8d995d20c8043b2486e3fbc23fd209fe4a11d530</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.9MiB (308.1MB) – 2,846,052 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8446667c1feaa357c25104ee40c7db47<br>SHA1: 1631c4d82f37dbaa7ece00c99dde97aa5483e6ea<br>SHA256: a265bc2be67ada5c65a6d3631fcbea01cc1272b1b51f27002bc5f3bffbf061ed</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-09-26<br>IPv6: 2025-09-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.71MiB (13.33MB) – 636,277 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75351c748333b8dc11c45c3480314677<br>SHA1: 026bd8e3bfe599042d90c29d54ac652b431a4851<br>SHA256: 47c0d55bc67507c5f4f03a4bdb1c0bce8289fba4b9e840836b14184a8cdd0ed8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.05MiB (45.14MB) – 654,253 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6436ac1e401b26e364b488a0cf26a97<br>SHA1: b13b5dc818a65c2fdcf4faae95d5f192aa5e7da5<br>SHA256: ad7041468e688304d8eac4539147debd933c624c04e3ae4e6e1c81dee6cd7977</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-09-26<br>IPv6: 2025-09-26 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>176.0MiB (184.6MB) – 3,468,635 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9dd46da17bc055d44dca6e4f8f49f6d0<br>SHA1: f9f2353e16dc5b7d78e1d77b83d917f38362fc04<br>SHA256: f73b65ef6b3079897649aa2495b6562e4ca00e7f6f21335bd78380ac541640ba</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>187.1MiB (196.2MB) – 3,468,635 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c2fb479c57c94faa6b1e1f323bfac22<br>SHA1: ee5f4b686587c4eda5aa31223707a99516dc5db2<br>SHA256: 875d63c3fad9651d7142c624194510c12070ae88f0216ef5b0c3290d8882624c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>175.0MiB (183.5MB) – 3,468,635 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31f51472f32ad530d23304befb500d41<br>SHA1: a291812126c72bf52614a2ddf8d14f448ee3494d<br>SHA256: 389ed2f048c851aa7ffbc2830c63c10a30762287d9d542a814c080a33403c56c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>177.8MiB (186.5MB) – 3,468,635 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1abdd7ab1f715faabab8ff1d0766065<br>SHA1: a05583c58f8ac4c50a4d814e70cbdcfd7f178f32<br>SHA256: 570e5136231e2278c724b1cf423679473008b7ba574d9dbc236a4711bd9316dc</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>223.0MiB (233.9MB) – 3,468,635 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2dbc00f2f90674b54e914c98ded19013<br>SHA1: 125dfb899bc8955dff8eec9b4e3fe0a2d4ace00d<br>SHA256: e652466e4ab0e8428bf104776e5ce63cf485ada15b1b85f920805a0c41885d6c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>174.7MiB (183.2MB) – 3,468,635 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26159065d39ac956a23090c13bf7212f<br>SHA1: 94f890dc78fe7633bf2eff9fb1b1996fca80f5d5<br>SHA256: 917da1c6506e3d1e37b47bea8d6e39b4b66dcdca815de086fa64c85cffa38f20</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>216.7MiB (227.3MB) – 3,468,635 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d583995bc7fa9d96ef9b011fd93c347c<br>SHA1: f78f6b172ce5eca71993e4df26db3c7801c4cc2e<br>SHA256: 06d97ad61540c2f3a21b1ab9e29c6f0abd77eccd0d2435aa0666d19898f4fea2</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>182.0MiB (190.9MB) – 3,468,635 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65fbae1f8821fdecb58f174b1067c931<br>SHA1: e7548949c2dd2f2719da4c6f751de3f008c92ffb<br>SHA256: b31ddb4fbca67fc6918066226b5162d23dbeaa754156269b33f7aa33aab5adfc</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>178.0MiB (186.7MB) – 1,887,810 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efbe28300ec0318b6b53f3d558379400<br>SHA1: 3fb016ac847546faccc0107d4cb62f4cbad7d3c7<br>SHA256: 9def257ea7dc80807971206728c70f5d17aa9f8e49e8247174ebd8073f96a9f2</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.2MiB (191.1MB) – 1,887,810 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bae5bab209bd2c6edf85cb3366e063f<br>SHA1: 03d45bdfeb6f802ac7356fdd4050e85dbfdbd3fa<br>SHA256: b5339bfe456ffb1c734625a4563ae71059fe44f70dbc1ad69d071813140113b5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.1MiB (184.7MB) – 1,887,810 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c694498debbf911153e6529aba714c05<br>SHA1: a789c74e1c6ca7aa4c81bcf2e9f74e59e82bb7f2<br>SHA256: a3abcfbd99dcdb56e31a4964383d1e32f4677940e128dc4f26f809552c967938</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>176.4MiB (185.0MB) – 1,887,810 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 731e0515ec8b5256037597f884fa607f<br>SHA1: 8fbb1b9f4aafcda073ee16ae4f5b5b19862fd449<br>SHA256: cd83c18400a16372a6796b8ea497f5b733ae0f75d74865ea99461afc0e3d3d4e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.5MiB (205.0MB) – 1,887,810 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e42a079d2c78b203d4b9a514bd9c868d<br>SHA1: 288e9200b763345a2b9388943d181291228fdc14<br>SHA256: 48e9b3179690921ac42fda5779223eb27066405b5f454735d304e0a7239d0571</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>175.9MiB (184.5MB) – 1,887,810 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d07538a22e6d9937a1215fcce8e89c08<br>SHA1: 05f680f35381d801b47c7fe8438d608e11fdc92b<br>SHA256: ec96867f341d25b55646ea9bc3103bad91c88ad03a9e7565a03a4768327e3276</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.3MiB (205.9MB) – 1,887,810 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd25d733588e41268d8b4f9cc99775a1<br>SHA1: b39120bf74581d4025491e9c30b586c969f5025c<br>SHA256: 77cee3ad329f79c5d6844044f0a33c9fdb1122321da44e63125f379f7814138e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>180.1MiB (188.8MB) – 1,887,810 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdbb3000e493ee50c2f0a076742a4226<br>SHA1: bf05035cc5fda1e9bd64702393d794ab05f5bc0f<br>SHA256: 0f38cd889e70c78988cedbf99417dfec3832faaa877944007e4d3a65953b70e5</pre></details></small> |


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
