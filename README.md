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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-08-11<br>IPv6: 2026-08-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.437 MiB (5.701 MB) – 272,094 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86927d21d4308aa1456565478c77a6b6<br>SHA1: 03c8686051bc8e59db5df4d030b6ebfa2efd51df<br>SHA256: 9aa7f4a12f0fda22477a8f5eebbeb4835e26a6329f7af02365843491eb4ecb01</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.77 MiB (17.58 MB) – 254,839 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa5f8f76664b41fd2aaacefafdd0d078<br>SHA1: 5eff5a018409f7cb19bc7f59fe32f20283ce0e0f<br>SHA256: 8fe802825ef5038d21027ef5f5bc5c62b96fe89a42c9688e70f0b5c6c67de39b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-08-12<br>IPv6: 2026-08-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.053 MiB (9.493 MB) – 453,292 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17027632634d3561cd2cecf0ec29c222<br>SHA1: e0b46a557707ed9471ab49d459aaff2fc70f5261<br>SHA256: 0888a76915f7d24e08c78e5f4ce2868f323cdbb4e556a61887d5a49cd2265ebe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.996 MiB (8.384 MB) – 121,620 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cfb53eabdfd65b9b471096fabb09918<br>SHA1: 4b4ba37308b362ae4bfbcf6efcd709a457e58b7e<br>SHA256: 442b53aaf7f426db6ed66902fbd714d262f0b2e618b6e67a3ce8274c73b42312</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-08-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.31 MiB (12.91 MB) – 616,346 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f114a6afc055ab33c12b2e944e8a5dd1<br>SHA1: 5b4c0bca2c8d6ff2040a91b129e451b4becfedde<br>SHA256: 9040b1772347ca71de3ada4252e19139e4817229ca03b4e713e96067308800b1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>66.57 MiB (69.81 MB) – 1,011,686 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d49c0f696bbbbc9b1b511643dba57fc<br>SHA1: 773f4028afba23e59a69772eadd53c1bf9b362b8<br>SHA256: 5fec78dfc946d8e617682a4803842ec9ff13a6066ac607b3bd04a9d7f5f941a7</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.149 MiB (7.496 MB) – 358,140 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d3e21d2da14fe2fa0da1db2f6424311<br>SHA1: f274f58aadcfa3311603218b88e8b24a01671e36<br>SHA256: f62294be209c966f38eb82e27717bc64116462241210756e85c31429048d1f96</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.92 MiB (24.03 MB) – 348,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60cc96dd0eef36fef003b9981e7aa19c<br>SHA1: 077fc11bdf3b1a16ed5a8e22cb9889e86b007cf5<br>SHA256: da4f32fc9e285ea393eb3d4fec4fb4a153874623b14fc77373e8f448758ac135</pre></details></small> |
| | | Full Location | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>208.4 MiB (218.6 MB) – 3,652,137 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68a79460a812a271884a0a50858ee1f8<br>SHA1: e1cb26165f0fc2b394c3f08d99642d1e5a3e653e<br>SHA256: f40963b044ff4637dff7dd3608244f6e065cc97e9bb7262d5fea4abeed6cf026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>440.2 MiB (461.6 MB) – 4,274,498 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e9801b97694446ef740a7093d24488<br>SHA1: c8e28d1130d3667d5b313b6e468c5d9d69ffb027<br>SHA256: 88971b264e462d0a2d37d85f793d5e488192b4d883a1ad0142a7c28d9a60af96</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.729 MiB (6.007 MB) – 286,747 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ce5cc1653ddb65db06474bab749714a<br>SHA1: 4cc40ea81eba37e4bdc9ce61fe9ce058d0c49372<br>SHA256: d3b805b3c0b083f2ac8b16100752f8ea3eeb8e224cf00f594602330d36cefcb4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.35 MiB (23.43 MB) – 339,594 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 518560be8d49e16a3856c31b0d0bd875<br>SHA1: b1f9595b2778075c3ff384176d6845d15decf465<br>SHA256: 5d25d7d5e32cc9f7b89b03e674eb90f100272a7f4bcd26c78e8a2b2c41efb36b</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.3 MiB (178.6 MB) – 2,947,098 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b12349e01828d4a4bac50e8c858fd50<br>SHA1: e99752a712b42043ecd9c65d3e9651264ae608de<br>SHA256: 3d436dcbd07ba02c6c6fac1fe6d1baa7bca22dd26ec4bd68d3029810ffe0e936</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>299.1 MiB (313.6 MB) – 2,898,359 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddbe75f08ad96059705bbdd5423bfa36<br>SHA1: abe287e78fb8e2391d170e4400975486e52fac90<br>SHA256: eef9c134b1787ced9b9492f2d3cf0bd3e4f7ddc7f71199e6c54374d9513c5083</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-08-11<br>IPv6: 2026-08-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.21 MiB (11.75 MB) – 561,282 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 943f518febee8cdfebb01398dc9a4c7e<br>SHA1: 1d96019c38ca70be8782afc04836e8c23c9aa748<br>SHA256: 227c2afebb8d8664fcc87eccf840d4e3b2b3236a63b7b83d13a2328dead532e4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>35.48 MiB (37.21 MB) – 539,215 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f98e3d89bfbd092ce5291f418a057f0d<br>SHA1: 7d6f07ab9b374be6ee230d4c69045328134eba65<br>SHA256: f2f3b7bca1d5131415f16871ff92de1fa2a658fe321ca99d57d7a06223d06cc0</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-08-11<br>IPv6: 2026-08-11 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>192.8 MiB (202.1 MB) – 3,754,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f595be408f116993ce7c37bf036d0c7<br>SHA1: a3ee0fceda6952032e9ea3dc4bc29a98aa83f6c9<br>SHA256: f6bb9b6a8adb14fbea43de16c57724ae28c684f495780710f96dcac9f580f776</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>201.9 MiB (211.7 MB) – 3,754,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97640752712aa9bf8ad92503a84e1344<br>SHA1: 64ecbb44d7d2d8f34943befdd0160da6b5c90c77<br>SHA256: b83aaaa5f090cad82e83c11c795f6dff9844cd3e94ddbb4ef553745456197615</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>191.9 MiB (201.2 MB) – 3,754,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: faf9af72fe987930ada60310b3082143<br>SHA1: 4b63c25d7e01dddf81ad89041f4de25c83538875<br>SHA256: 67dd87ad2df242eca51fe02c6f8bf038423b867e1f320a326663b085890911c0</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>193.7 MiB (203.1 MB) – 3,754,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d175b101d344b1cdbd3faacf0154e1e3<br>SHA1: 2a01ccca5ec2825741ac84b8dafe4afd2079dcd9<br>SHA256: 43777945b1317681888a3b9da0e8f8fdd820f49c909637de8fb36bffd12dad3c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.1 MiB (256.0 MB) – 3,754,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 062f463bcf55d00044757dd86f826db7<br>SHA1: c443caca4be274c633aeb6b18540224994986d33<br>SHA256: e8702a79f3d3ad387548f6468dd2727192e3c41371bff03a0731697b6342e245</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.2 MiB (200.5 MB) – 3,754,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35f532d7c5aeb7e5da05a8f4adfb9e84<br>SHA1: 4d5f864df8796964b2cbb63722e33958a93ea88c<br>SHA256: 07b254b5ed09444b4a17b6315d37541ec9e3cc94ff3b0603486e31982c571a19</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.1 MiB (245.4 MB) – 3,754,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2ca89c05f235f889effce58ca9141de<br>SHA1: 12d94b4bca20490e97977d9c3d9a10c3485d681b<br>SHA256: e72cc2ba5f78011d0ac2ac6eb518ca4cacdfbb989331ebbaec8389c297d1d3e9</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 3,754,589 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b1afd21162bdcda6344c0743cc2a033<br>SHA1: 34297ca9a0d7d54c39aceb97366e2e69ef7818b0<br>SHA256: 3fcd6794acde6cc0aed6d13d5b12220c1e3483ca40fd8ee7c7c130bdc2694f0d</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>197.7 MiB (207.3 MB) – 2,074,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fd20d2fbf6aba9d33b7fc3cc5d1bc6a<br>SHA1: 2e5e8ab384efc4b5f1acd596c2aba3cd619af0f4<br>SHA256: f2f6b86afcc605038687740be87a25a873690516448539bad275ef5b95b4f2c9</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>200.9 MiB (210.7 MB) – 2,074,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf5420765877d235a763170ca1602529<br>SHA1: 24bdb88e73965a35106f03ff160635e5a6746d63<br>SHA256: e02796fe308ea753e740d66a6cbad3b04b2a67e9d0b39300f8e477482d48749b</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>195.1 MiB (204.6 MB) – 2,074,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ff05ac612469ac439b93f1324608a39<br>SHA1: 22a886befbd96cdbde13c2b59e2026c617c7e5b9<br>SHA256: e348a1537cdf88abc5373e526507ac827f39ee29f57e2d4bb11a7b8d6fdda096</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>195.7 MiB (205.2 MB) – 2,074,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac2738c6c0eadcca22365074c095a4c5<br>SHA1: 888317b607cbd2424a938b819df79ba36e4232ff<br>SHA256: b3d1b238d323a75147c6a6bec2b927af43bd32801f6633b23b712ff7ca8236ae</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>217.9 MiB (228.4 MB) – 2,074,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f7f61bb41e5c5ed824b8a6c8a7c011a<br>SHA1: d811999caa3d1615da8c9e9db81fb271d751f9fb<br>SHA256: 7cd96b3d7d21a303bbacb07e3140876845c20ec0c07fd131b943bce97dcfb63a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>195.0 MiB (204.4 MB) – 2,074,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 566ac2184de6d71b336dd6e442e0b2a2<br>SHA1: d521cc4b8ce2d8857823e218bddfc34d18a5489d<br>SHA256: ea4979dcde6cba7da2e9b32862fe4db76e0d040a3072ec0222ce657ecc11ed7f</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>216.1 MiB (226.6 MB) – 2,074,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bf29169a90fd436dfe56639aa172c16<br>SHA1: c03f0678b0a4ba6f25fbc52e111c5bd3c53d24f5<br>SHA256: 8347ff97e324d00ca34af9616e47f62a32c60c24cbdb348bc69e10ddec60a979</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>197.8 MiB (207.4 MB) – 2,074,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8890458962f8c91b62a43d5835cb81b<br>SHA1: 574c82cef367624eb58ac54a7bca8bd3b19e8577<br>SHA256: 6f6f304b05aea4fec7a8f11fadcd5c1bf0a5ae00902063b3ee5b935f32234fad</pre></details></small> |


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
