[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than five days (previously ~one month~ two weeks) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-11-10<br>IPv6: 2023-11-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.594MiB (5.866MB) – 238,306 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fb7d198360232da37b96de334cdfd76<br>SHA1: 4d047addbbeae13de797008e7061b3ca4dffb58e<br>SHA256: 3ddb7ee560dfa6ad250ebe6a728e9215962d4be448214e687e40c14d6b3a49be</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.267MiB (6.572MB) – 81,132 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b53d1d292bc7db463bcb773c5bb60f0a<br>SHA1: 8e0ef2347ff1ff3113f2371b85be8591b8344076<br>SHA256: 38f2d69ad516679ffaca90cfdfa08344a651f2d7307cf19df1baaccd1905e4cb</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-11-10<br>IPv6: 2023-11-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.640MiB (10.11MB) – 409,461 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2561f2e7d14e4585bf5193a526c98ff<br>SHA1: a136eedbf7b349f4c14cf19bb4e81f7b118ebbe5<br>SHA256: 4a5dd4ff01471bd26d1f5b63469364774889f2d9afb2fe727afadc571b0692fe</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.083MiB (8.476MB) – 104,738 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0965a09a91d62f0f026cf305eaef53a9<br>SHA1: f45a6b156230b9eda2b2b4d6b739d977f0c30d5b<br>SHA256: e61815936a3650e74ff0c5b1f26bde4bbb91aa7a2e2043efbb8f56998c24bc8b</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-11-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.30MiB (20.24MB) – 820,185 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e12008206a9b480298b76e851c71e03<br>SHA1: efcb6bfe9d475b68ad8e8bec0531a2d4f47f86b9<br>SHA256: 41e9a94be29d3e65a9597952a1e434914ca6f41b8173bb44c3e0c37f1bb9ea8c</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>40.19MiB (42.14MB) – 520,225 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74c7ab53babd2bce1090a6045644b22f<br>SHA1: 155e15b22ff4e9ee29ad0bd7dedcb43aa93ae827<br>SHA256: b82a4125542c911f438be298b9a74fd928ca233b27d0263d79472a92129edd2d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.260MiB (7.613MB) – 309,964 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7fc3106cf6c65db7d44df8b4fb1d16<br>SHA1: 6ec97588db0af32a305835217289c32883d23f64<br>SHA256: 9bc7152bcf323316fc78e69cfa190cbddf22834208f48cee2e624c18150c9478</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.63MiB (26.88MB) – 331,798 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264a68f442d85aea134072d7bca0f4fe<br>SHA1: 65171ab00588cb7f2ae029d9345b44cccc888d24<br>SHA256: f76d40c34e6881d9cf3d98b34ced8105e9bd9efbb3f55e2bc224ece181569030</pre></details></small> |
| | | Full Location | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>186.8MiB (195.9MB) – 3,075,320 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96e5fc94ee00f3349281d3d79c8e3e83<br>SHA1: cf6b55598525f02890d9596fefd546190401adc9<br>SHA256: 5dfdabdba40afb770f6ff5afcc35db6136e9e28182bd6b3fd23b3c203dca5d1f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.3MiB (303.3MB) – 2,504,397 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bcf1dc4f4611d3e39906c6048aa8fc<br>SHA1: 2cd36733f3043bb3d9985d20fa8416a68b122e30<br>SHA256: e3d5ccb9e02dd929dc48ad40f82d484f9ffe60f9098c5a3ac296e33c5b9c2a9e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-11-10<br>IPv6: 2023-11-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.446MiB (5.711MB) – 232,323 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f7d79b6a3ef8bc35c3c8381e7c028<br>SHA1: cbc8e9cbd5c151f0cdb02a21e5e6fe9d8b662cc8<br>SHA256: 9f3976e09ec875d7e97185503221656e80f41f531e268da1bbf874127de2583e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.41MiB (20.36MB) – 251,316 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df2ea3be7027267ebb1947b4220cc4b<br>SHA1: e94b6a993297b5dff456113130c22e323534e39e<br>SHA256: 44458ed651d7b4bd99ad73459d500395c410da1b2fce9fbb2c4e5ce318c4bcf9</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-11-10<br>IPv6: 2023-11-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.3MiB (180.7MB) – 2,814,468 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25688ced507227d7990066c41a0d58d6<br>SHA1: 28da5022ff88d543bba4e15cc01b703781801bba<br>SHA256: cf219cb6d358d6e4df364a87f28817e4aaf8322370b86495ef74cc1941c73f5d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>171.4MiB (179.7MB) – 1,495,017 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d4ab0c657ede6538d2756cef356f5f<br>SHA1: c2865c0d416ae7143165db8aca21627725b4b45c<br>SHA256: 66022701ed347d75f4f400e76024ae545696e742e4c0fd30bedf981c262b318b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-11-07<br>IPv6: 2023-11-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.78MiB (11.30MB) – 460,038 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9134ebaa8bf6a4de192911080380b1ed<br>SHA1: c947a3086f2ce7b082298c18e324534e2c597684<br>SHA256: 89ea655914e1f728a1611139ea6e8e2ddfef9b24893d5f898eb3a66ceba0e363</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>23.09MiB (24.22MB) – 298,975 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7770c4e022ff14298e2a7886c650d276<br>SHA1: c0ea1a8b7577c00ce53454803301d6eae46fd33d<br>SHA256: 2c15ea279e3c46d258c1e95509ff161039c8a2a4369a5fb95c300aa807f87740</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-11-07<br>IPv6: 2023-11-07 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>160.7MiB (168.5MB) – 3,184,245 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91a59492427e176b0884cd1bf7884791<br>SHA1: c21aa3dd3d25b843fa1556570af599a3ca7393f3<br>SHA256: 3a26b2d028536c6edb4522dd466df505dd17689c2815568b14ded4caca7c0d4a</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>185.6MiB (194.7MB) – 3,184,245 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b622a8bf245fca119a0265578cf0f3a3<br>SHA1: e132bb6a19ee13723feb17728e31896e2189da43<br>SHA256: 1276f30109f2c13e79bb38f328dda4c051b16affd1fefda8ea76979073e1fb67</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>164.7MiB (172.7MB) – 3,184,245 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ecac03f7fe2bdf2e012ffdac7c92fb1<br>SHA1: 9faa07b6a542595bf7c2a38f30ef41c691e0f467<br>SHA256: 7cc257572cad8c53cd10d58e19fda7897ee53ac6d9c487d8db9ed861f762298c</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>170.7MiB (179.0MB) – 3,184,245 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa4f5ab868fc7df8a485b20cd68c7555<br>SHA1: 02ce10b4d6cbc41962b6f23664f564b956644a6a<br>SHA256: 8b24f35b4d3cb60501368a82045d66e691dd7370f7af4678555a69c08c1d23eb</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>194.8MiB (204.3MB) – 3,184,245 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10ed99a125b85efd868bbc153ed0dc05<br>SHA1: 18844b5d42ea7ab9d5e468402d67913abae55f1c<br>SHA256: d26e42087afff2b9716e3ce93dd0f62b14c845258d96ff86d809da38251b19c0</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>159.7MiB (167.4MB) – 3,184,245 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a6753a95ec54e8f6efc4039c6f827d2<br>SHA1: 981c64269893ee7d6db1020e72fc2c0ee1c9839e<br>SHA256: 45882d47595775cb18c022e186d0bd9064132378bb57f070e1e2b4cff14acd2f</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>196.4MiB (205.9MB) – 3,184,245 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a27ab28496157dfad2a041296fdfb07c<br>SHA1: 2f35cfd60e2d0d43f703c62faa8cb178708bc67a<br>SHA256: 71923af7a27048bcf15097176340e0ef7a8bcc05176958f64140b77445360b8b</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>166.5MiB (174.6MB) – 3,184,245 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4de6e423a0f968f14dd00e049b094bdb<br>SHA1: e7408716bb56323b656394b7196b491397f4503c<br>SHA256: 4cb00cf61d7b12441239995f497a27b3ec10f64dd0b816858870902ce33f5e6e</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.1MiB (131.1MB) – 1,241,545 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4242a5719c67722566c5bf7b73d68de<br>SHA1: a6e126e5a321bb23a6e6cd71de84c740a72798fe<br>SHA256: c21f84b6213eca74c20e55a73b300adb464bc4bf79d273ff554de45157ce4413</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.8MiB (139.3MB) – 1,241,545 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 692900c6f686fb3391021a3b2a38cd67<br>SHA1: 80045d4c02cf0c8615f9fbdfc69bdf1de26154de<br>SHA256: 63e4192c4514451d953106a00f91b81ffa779446f37b5edc88fbd2676b3fa0fd</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.0MiB (133.2MB) – 1,241,545 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f3e84c8cb20e18c26dc292684a95a15<br>SHA1: ba559168e101068b474df8d0efcfc73790f3282b<br>SHA256: c8b712f18d6108aa3220d48537081e0a4e65ede12cd599071b650cc834157dcb</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.8MiB (135.0MB) – 1,241,545 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f15bb8b8a75f71b5050842ee55b8a6f<br>SHA1: 3fbdc7ff0371a75fd73251d556e2dc22f691a464<br>SHA256: 3c85be326015708b62a799222823f7b607d78c67e12d3a7d080c64d58b7a20bc</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>136.4MiB (143.1MB) – 1,241,545 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e08984e2ea072a3aaaa099206dbef601<br>SHA1: 8776c1a78cdf7634d3d6b19c0f14ebc8fc8266dd<br>SHA256: c0a01cd2b4eff48603ca1da067b7a0109b976fb94257415bf38ed8bf44463250</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>125.9MiB (132.1MB) – 1,241,545 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4c0344ba2b0216d24902662ef758015<br>SHA1: 1bbb1c08b79e947f757c3d1efe1b1b67b6800f97<br>SHA256: b3f42ab8f80ea71372760e315d172c587563c459d0539ee83705af401e765ced</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.8MiB (143.4MB) – 1,241,545 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 382c05a9b25a3c7e6b67cf3c844fadce<br>SHA1: 598710941fc81043641b37e4b00f16940ed60eb5<br>SHA256: bf5e16ace3605f4b38e027d73b5e9e40db574145efac2e2060b6387cefc2d2e6</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>129.0MiB (135.3MB) – 1,241,545 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e16fbfc5119c9939b4beb730d32e4fe6<br>SHA1: 48fc78e5788fd362aa14439cb90f55df92ba03c3<br>SHA256: 9b66acf38ff065e574f2bc9b859fa38fa3e7a3b50247c349175377b0fa015183</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hex format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
