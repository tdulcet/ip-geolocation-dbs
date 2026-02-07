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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-02-07<br>IPv6: 2026-02-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.439MiB (6.752MB) – 322,418 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c2cc06bde58b2b1fb3b1b1d6f587d9e<br>SHA1: f812f94252d4a05cd0373de6bafae404e6008cd1<br>SHA256: aac065524530b4ed07ffe5c994b39c3354b93c6afc89c55f4d45c650a6f5a416</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.18MiB (15.92MB) – 230,666 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b1af7c3cb6bd627b3c298c699353333<br>SHA1: ee50ebbac82ab809e88e0fbb2f9b8896ca1833cf<br>SHA256: c32daad9196d4241db7d5880a319792df6b79869b38e24bb4c4b71e899d8b9ad</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-02-07<br>IPv6: 2026-02-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.769MiB (9.195MB) – 439,110 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da7c614c298ca6006bb17caf182f108d<br>SHA1: e34a0e5d14afc5a15281ad883b186ae822f5d0e1<br>SHA256: bac5269bbbaf6aa6ab8a831fc232e4183408353df5a5c0c54b350f02c63c555b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.588MiB (7.956MB) – 115,423 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c05db826edb091579da0a182ba962a1e<br>SHA1: 41ab5cb884605d74b8c448c0939978eba0668dd2<br>SHA256: f3d981ff5eefbbdbed8f4301ad6a6633fa4e78f415bfe3581f72495f4dc82268</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-02-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.16MiB (12.75MB) – 608,791 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f6c2e71f1386efac16eab93cdcc4a5b<br>SHA1: 017674684d197f5b15b2f8c1e81d023986392fcb<br>SHA256: a10b686f352f662eaa3e73d2429dfbfcb02893efa36761a45b113becbc06d352</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>52.32MiB (54.86MB) – 795,039 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41790a9aafcb8c4f47ce6af4051aebe1<br>SHA1: cae96e360f5e5227fb58a413b17a9078e4fe40b5<br>SHA256: 7e3dd0faa6639714f28010ac84930a58acd81fd3dd1154a360deb35fb7bd4b16</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.768MiB (7.097MB) – 339,077 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0181205d24255559b4c2a13fdb0c95<br>SHA1: 77c5ed2ef6799485a1ff6d1bd9aa3aef442555aa<br>SHA256: f1a904010b8cf3e5db4f0ddc1b0fed4c77f852aa52effac37a04697ddb879a37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.90MiB (16.67MB) – 241,625 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f8f77acea5ee52ad5d81c9f3883d7a<br>SHA1: d3a894c2e7503a5fe5168eef49e53379425930d2<br>SHA256: 80ee4bf63ff4562160eda9ba68902de89a9e28a828c048003fd188647039bf1f</pre></details></small> |
| | | Full Location | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,746,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48770c63478550e9d616b0e8f11eb35f<br>SHA1: d754e9f10a536891a6f76b212ce1527fccbb205a<br>SHA256: 3abef96589717a094c9384cc0d2e88d16dcc6c1771a5eb42954efe056fe2caf0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>452.5MiB (474.4MB) – 4,397,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d15359a3c2245bffe65895c5939244<br>SHA1: a5622976378fbaa83dd68ce8bf186161f41252b1<br>SHA256: 3c33680bdbdc577647e1e500060fa0db02dc2af50f79e20bb78a7ae7ca1b33bb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.379MiB (5.641MB) – 269,229 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8df1f43c6aabf7404b9835918b8fde47<br>SHA1: 601b465ff0736111423be419aac3f6d5972b42f4<br>SHA256: 80bbfe7421ce68520f39ab366b0fc481427602add22c34ee6881ec43a96b1488</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.19MiB (23.27MB) – 337,206 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48696b7a642ffca450b564a365389e84<br>SHA1: 2da10da7971a84e435865041021aedd433c35db5<br>SHA256: 360124b18db3ea1ff8adc37d7d8c7432d236ac9d3e5c9f77123d8069ac8cd7ff</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.6MiB (179.9MB) – 2,969,494 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5343189d8e7d3b6229056c21a834739<br>SHA1: 8489f2c88b7fa2b7726299d47a687a5af88b7259<br>SHA256: 5f47bc0d8ce6968a1388a93536b1e895b0ddb335cd76007a7b142ca0fa206970</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.6MiB (307.9MB) – 2,846,346 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c67fa86a08014c894bae1e43237dbf3a<br>SHA1: 1bfac6af73658923732d9bf178d37d1b4cf1e23d<br>SHA256: f5b735e687c937676bc7cd2a6d383e598ea54e61f46b9863d97f53062b1634de</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-02-06<br>IPv6: 2026-02-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.05MiB (12.63MB) – 603,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83a16f24cd6a5a9b2353e1f3caf76103<br>SHA1: a6dbaf3b99e0f834460ff3c37a81f287a9ca08bd<br>SHA256: 2ab62b763752b55b3d2933599fa5e76bc560aec785d70e8f4d3572bf2469d3ac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.88MiB (44.96MB) – 651,581 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b0744224acb0c3ece674c2e7bd6759c<br>SHA1: 3ed7a47cbc815442d1d46d9d371df64c9f78780a<br>SHA256: 9ad3ff62ced18047d88997e3d11a3edd7375e5787ef291174ce11a972d0b54bf</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-02-06<br>IPv6: 2026-02-06 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>177.6MiB (186.2MB) – 3,512,199 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17ecf6d68e99b80bac1d4c311a6179ac<br>SHA1: 189a42fedc7ef8b4f2c08d2dd6f78639948263b5<br>SHA256: 028599a737c65105e08ad8d50b815e36e2dbf55e009354de624db4819aa22e57</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>188.5MiB (197.6MB) – 3,512,199 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21b25166b6dbdd4e3ba465fd4b525e0d<br>SHA1: 7b77cbf3677bf4d6b0e907f612dd0c32424b1ac4<br>SHA256: 4480263a7ab83d9eb0d8b9bdd8c628194a7947c5203131a29008c30cf8d77969</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>176.6MiB (185.2MB) – 3,512,199 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8b6a024e9642f8bcccf963110b6460d<br>SHA1: 325f0333e4e2efa7790b64a758450c4b8b607cd7<br>SHA256: c271f4715cf08ed6b7bd61258a1df07b162cb73c94e08f3d9f25b7888a95c46b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>179.5MiB (188.2MB) – 3,512,199 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1bcb75bb8d1b2bd0b01211bc4fa411ac<br>SHA1: c6218ebb069338efe6ebec90899d135269e11d46<br>SHA256: 46dbd11eb83c79b24b9798af155e01e704a9e527280a48a3bd79b9bf8f72a995</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.3MiB (235.2MB) – 3,512,199 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4d514bcbc90261413c2f5ff7ae011e1<br>SHA1: 3ca7a5d8e04a8d1892d4a92296ff3600cb80b323<br>SHA256: 4b6b066a54b6108a253dc461a09cb170cf42fdcf0ae4d5db112857d6195815b2</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.2MiB (184.8MB) – 3,512,199 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db941ec3596df1f214d1c0c1bf207b5c<br>SHA1: 1aaf049778a85b083461eccf6db97d780c500aed<br>SHA256: a19c69241a717059e7f855f3dc58ae3cb438301e55ab594cc06ea85ec505ac60</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>218.2MiB (228.8MB) – 3,512,199 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95dc49fd4a1ba4503282f962455706a4<br>SHA1: 8aa27486b03257aa4849c3877e75111a83534dbf<br>SHA256: e71ae6aeb3c76c7c73955cb1266f9dcf13cf4ae1dbeb9097afea6347f1a938c4</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.5MiB (192.5MB) – 3,512,199 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 161b01cf81ae03e6910c861f38e6f586<br>SHA1: 7ee188109439eaa2e783033e6a22b7fd7f00acd2<br>SHA256: e9665b06e071b5cadf54c230101eb911c5de3fcef2e177dcfbb8f3fc0cf6239a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>185.6MiB (194.6MB) – 1,958,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0123a67aba2be1c477ee6124149ade91<br>SHA1: f531e307bc6cf90685d51d5fced289febdc020ed<br>SHA256: 15117148aaa1af7e9dc35b95faf5c95291062063776d8476c0548e128fa3ee81</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>189.7MiB (198.9MB) – 1,958,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ab20b24489b1b424198bbd8a8fa1652<br>SHA1: ad195eefb47ed2350e4955c55ed41b63b35f2cc7<br>SHA256: 7e2c446ff95b0e52bfb076d1eac4b10165179882f231539e9a60baf846c8ab73</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>183.4MiB (192.3MB) – 1,958,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1bbb08bb6982d4bd2bf54613b9f090c8<br>SHA1: 48804e18c5caec7133b5958790a6dd4d251d571b<br>SHA256: 9b6b742d15341543a50e8693d4f22c4cad78301a8ea2ccc7fa9e2f48e56508a8</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>184.1MiB (193.0MB) – 1,958,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b5524d63787b7115f445fe3e4a5591b<br>SHA1: 96690c820b1cdd45b7dd9e921b70fd8a3a533101<br>SHA256: 33bab61ea10573124d98f129feedd92851db2eed85746184a177ca7385768691</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>203.6MiB (213.5MB) – 1,958,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18a65dd80f0dc9db919399f5ca8cbac1<br>SHA1: 1863c0e07303756c3673f310ebdf5b5187d86fb1<br>SHA256: 82f446ca045ad53ec84e9b8f68bc890dc756399acd7ae574efc5e9787560c0ef</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>183.0MiB (191.9MB) – 1,958,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad40350a58ca96075282710ba8f55e9a<br>SHA1: 02a941b4dc92da80d81d35d51dd837743f308e62<br>SHA256: 908c153fc4081f0d73f6cc34eabbf53856d3d96d729eed99d20997718921ba57</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>203.6MiB (213.5MB) – 1,958,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b6c7ebf9ca6fd106f31c0d4c3a5fcfb<br>SHA1: 90178885317f8b1e1128d154730ea193978480af<br>SHA256: e528865446208546444ff0ac638d9f73d75d345ef5547344586086b743a71189</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>186.5MiB (195.6MB) – 1,958,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92cc60737d1a03d71a44b27c8d5d842a<br>SHA1: 6d97c1555103bb672615f32c8f68ef19c6915492<br>SHA256: 4ed853ba6db37407d1c372f312f86c48b9bb2b6c1989730f058af6afaeb46c04</pre></details></small> |


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
