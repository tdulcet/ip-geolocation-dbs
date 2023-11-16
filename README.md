[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases are scheduled to change from CSV to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than two days (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-11-16<br>IPv6: 2023-11-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.600MiB (5.872MB) – 238,523 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d4c58494561feb77fcb26a349dea272<br>SHA1: 549a10d6d07327e833ec0c3e32f37d5dad7981d9<br>SHA256: dea8cd73100e7135c22c1532a19a726e6f76c6b26b80e869af6be0fbaca42440</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.298MiB (6.604MB) – 81,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d4ccaa8846f1901dd15e831e1f4eea6<br>SHA1: 02be90623ee60df0caacc7d84eca2cce506459be<br>SHA256: 77af0f53a14a30af429ce9c9aff319d64b4a72266e4c8fa1eb4da58ea500b983</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-11-16<br>IPv6: 2023-11-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.625MiB (10.09MB) – 408,811 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18d64b79dc8259886812762145441b65<br>SHA1: 5d2548d573cc5ed663881a3b05f1da1ffb36b26b<br>SHA256: 33f193d3c016e39000d1b2da46ca9abac40befe6c2053c77abadd840bfa6eaec</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.103MiB (8.497MB) – 104,995 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a952171df665a5d02e8ec5994d6037e1<br>SHA1: b0979812b2188629f31bba62cb13d258040f4177<br>SHA256: c2f223937cb543cdd60b1eac02176cc28b42d8dc54235427500f06b033d15101</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-11-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>20.17MiB (21.15MB) – 856,797 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce9c00dffd321117e843a91674ccca2a<br>SHA1: cd60f1f6962cb17b235c531e636e3eb49ab4d4b1<br>SHA256: 17a5fc7b3f76821d01bcd98864ddd2d3e3eb988df9260895465c0bf277adce1c</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>39.80MiB (41.74MB) – 515,263 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b845ee89e1ebfe7fe3711e47fd9d6af5<br>SHA1: da054a7f9316b0378a8d31d36b1f1629044ca006<br>SHA256: 056631b0d201314e82a546b0dc23deb597e89739b3ae23a44af3f790d5733022</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.260MiB (7.613MB) – 309,964 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7fc3106cf6c65db7d44df8b4fb1d16<br>SHA1: 6ec97588db0af32a305835217289c32883d23f64<br>SHA256: 9bc7152bcf323316fc78e69cfa190cbddf22834208f48cee2e624c18150c9478</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.63MiB (26.88MB) – 331,798 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264a68f442d85aea134072d7bca0f4fe<br>SHA1: 65171ab00588cb7f2ae029d9345b44cccc888d24<br>SHA256: f76d40c34e6881d9cf3d98b34ced8105e9bd9efbb3f55e2bc224ece181569030</pre></details></small> |
| | | Full Location | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>186.8MiB (195.9MB) – 3,075,320 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96e5fc94ee00f3349281d3d79c8e3e83<br>SHA1: cf6b55598525f02890d9596fefd546190401adc9<br>SHA256: 5dfdabdba40afb770f6ff5afcc35db6136e9e28182bd6b3fd23b3c203dca5d1f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.3MiB (303.3MB) – 2,504,397 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bcf1dc4f4611d3e39906c6048aa8fc<br>SHA1: 2cd36733f3043bb3d9985d20fa8416a68b122e30<br>SHA256: e3d5ccb9e02dd929dc48ad40f82d484f9ffe60f9098c5a3ac296e33c5b9c2a9e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-11-16<br>IPv6: 2023-11-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.446MiB (5.711MB) – 232,323 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f7d79b6a3ef8bc35c3c8381e7c028<br>SHA1: cbc8e9cbd5c151f0cdb02a21e5e6fe9d8b662cc8<br>SHA256: 9f3976e09ec875d7e97185503221656e80f41f531e268da1bbf874127de2583e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.41MiB (20.36MB) – 251,316 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df2ea3be7027267ebb1947b4220cc4b<br>SHA1: e94b6a993297b5dff456113130c22e323534e39e<br>SHA256: 44458ed651d7b4bd99ad73459d500395c410da1b2fce9fbb2c4e5ce318c4bcf9</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-11-16<br>IPv6: 2023-11-16 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.3MiB (180.7MB) – 2,814,468 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25688ced507227d7990066c41a0d58d6<br>SHA1: 28da5022ff88d543bba4e15cc01b703781801bba<br>SHA256: cf219cb6d358d6e4df364a87f28817e4aaf8322370b86495ef74cc1941c73f5d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>171.4MiB (179.7MB) – 1,495,017 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d4ab0c657ede6538d2756cef356f5f<br>SHA1: c2865c0d416ae7143165db8aca21627725b4b45c<br>SHA256: 66022701ed347d75f4f400e76024ae545696e742e4c0fd30bedf981c262b318b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-11-15<br>IPv6: 2023-11-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.62MiB (11.14MB) – 453,463 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbd47709e48cd1d110ea208809b49437<br>SHA1: 19752605dd6e8b5e2abefc64f4fb892be222d1a1<br>SHA256: 7247412894de9f55d64462ba3fcde6bc7b26e10227f19d9a1f4cf725b33680a6</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.46MiB (23.55MB) – 290,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c75622070de96ad9ef2a804205d822c2<br>SHA1: 435e40b515f375005e09bcad44c0c52f9c144e56<br>SHA256: dd377abfaf01d3ad2f818e939fe7ce6b3d30c3715b9c996c534ed77a7092db91</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-11-15<br>IPv6: 2023-11-15 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>160.6MiB (168.4MB) – 3,183,537 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54617d3eff44d836e71811387fac6c34<br>SHA1: 6713b91876a43b1405ed5da66f9e204b178462b1<br>SHA256: d48bedbf8688be46580dbb0516c52215cb17659679991832e5298c97efb16d39</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>185.6MiB (194.7MB) – 3,183,537 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bc35f84e22099e93dadece38c4f7b4b<br>SHA1: 8e18ec81d7aa8387e4c9098546f613cc78690e15<br>SHA256: a5ce58a9719fe9064b57892c754afccd703d8150348ff42bc9f18fb2b8cd90d0</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>164.6MiB (172.6MB) – 3,183,537 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16ea90a8f0815c0cd722f7d809552145<br>SHA1: 6ae2ca346a22f41542488fd2e119e63a861a1548<br>SHA256: a3b782fbd4f21abdb475e301edc2ec5fe7f591c473cddc70fdf0d2ed649de1d0</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>170.6MiB (178.9MB) – 3,183,537 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 13ef7624071e9c7adae88a9d03c43923<br>SHA1: c8a3256f84e3525a42150ad7eb91624568120878<br>SHA256: 4ed23fb344b6e568f6b758110ff75955becea0daf397e59e117beaf14e9d5ac4</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>194.8MiB (204.2MB) – 3,183,537 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffcb51d86abacdbad828e134f48f12f0<br>SHA1: 4539dfba6c6fb859dfdef9d195cf0358bb4c4e1f<br>SHA256: 121021d9401fb61ef317e5617a1faa5c60511562ca29cffedb33977b3ba9654e</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>159.6MiB (167.4MB) – 3,183,537 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8ee42a0513ab2b8bed75b4ab81f331b<br>SHA1: ff0860c9f26349f7b6c7c5022d66be690e15430c<br>SHA256: 001e9efe1584653dcc44668d737616893a4a3b60fb32cb2d0b7b5ed00f5ab9dd</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>196.3MiB (205.9MB) – 3,183,537 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c52b3589782590deffaf55ba793d8315<br>SHA1: 86500e85a4d0b1dedc0eb5bbf3551f75c8f6ad0c<br>SHA256: e252a0ec35757fd7283729df2e83f7b04bd8e4030e356c78a2e131b0521a7b80</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>166.5MiB (174.6MB) – 3,183,537 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c5bd3f920b2e6234e02a55fca58b8bc<br>SHA1: dd79e06d08d66800c2e7650169e8c91389188f29<br>SHA256: 169530ed3db827ecad459e7b688308ae0fbb8703263f9c1f78e33b66db4cb1bb</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>124.6MiB (130.7MB) – 1,239,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b4790cb73b0353b6def89a687552c9<br>SHA1: 2064af3086c2e835dfba3e4a1f28432f84822d39<br>SHA256: 1747c06c118c4e5480120ab6bd400712b96241c5b6f850d6424cfcaa208876bc</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.6MiB (139.1MB) – 1,239,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3fba7fb62a8df7725c8707008ffc8a09<br>SHA1: 6575d578129e1b8cab3aeb4a7ca7f708e2a6880f<br>SHA256: ee82015cb9bdaaba2e1a502ba15ad8631de787bb5d48acea62c179bfbd95263c</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>126.9MiB (133.1MB) – 1,239,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14fc53994b3dd11794482f840ed2fe78<br>SHA1: 03b582e251590c5ebe8b043083d2a7bbc02ea9bb<br>SHA256: 4538eae5baffc09fd7870a45ade47145cc60364da98dd9da06deab07dcfd286f</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.0MiB (134.3MB) – 1,239,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b10d9ee11338de67895fd97c12b3eaa2<br>SHA1: a244f1d305556c78ed22958ccdb40899d25649f6<br>SHA256: 329cdcd09573612fc1c8f2ca473829eed0ad5f226527ffc2e299139c66f0550f</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>135.7MiB (142.3MB) – 1,239,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd6e94cf385950ceac43d75160f532e1<br>SHA1: eb9e6a64992509d2fa2a430fb987cf1248fed8b5<br>SHA256: 10fb5f79fa30f7f12ff3742adaeea0ff00e2d5a1fecc57a4044c0a3e7e33a558</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>125.8MiB (131.9MB) – 1,239,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ad347d88b3555c2f932bb90d9dc91e<br>SHA1: f9e2ef4677bee450bffe6348c6babb996acb9cdd<br>SHA256: 8829b9e5024cc2c138f1609cfed651b0ec5b66fc9ddef33c2be1a32c83bc044c</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.3MiB (142.9MB) – 1,239,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92d187db2b61f0bdcfceac1bd527990d<br>SHA1: 8388f442a57939e319835a6f5efc3657131273b0<br>SHA256: 5c14a1502672bfe1b12e414ea3bc6ee76cac23c8feea5f88dfd48d6f5222fe5a</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>128.6MiB (134.9MB) – 1,239,224 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 196195dc98d6966cc483d3ba670e889c<br>SHA1: 83f33fbe5b7b02f0709a1250b2a5901149bf3bf2<br>SHA256: 77c2f3ddaa02dc3538f00ac01f9bc388ec6d9ca65fd29f78f85b5f360ff65264</pre></details></small> |


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
	* Store the IP addresses in hexadecimal format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
