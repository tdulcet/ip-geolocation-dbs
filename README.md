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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-10-26<br>IPv6: 2025-10-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.312MiB (5.570MB) – 266,088 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d582b3f47395d8176ec33b3b1bc043e<br>SHA1: 83c86196c8ecfa2f358388861062f2fa9358affa<br>SHA256: d57f990082de7cc5a8db4a3f52c1655f7ff7370bc901b4b8bfde0f70b3cf921c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.810MiB (7.141MB) – 103,491 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fe879134acdf453586a7672893dd675<br>SHA1: 1c9023d21458adec16f577781a5bea17b04ab185<br>SHA256: cebf14f0838716dba593ebcae3ec659ad68e0ceb94f13bfdcb2c3813ece4cb1f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-10-26<br>IPv6: 2025-10-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.725MiB (9.149MB) – 436,884 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 792a9e8254dd2d6ccfadb5fe77263532<br>SHA1: bd110866492bbf16b82485170a19f6cae1e473f1<br>SHA256: 521160b2bfd9dbb835d83a9d64b5ce69b9b679504b22283f82eea2b77297fe6e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.445MiB (7.807MB) – 113,257 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46ce4e06a5ea1a6d7a2d7bcf12607a69<br>SHA1: e2b9142d7e092f79caee4af3154aaf7d4a6b5b68<br>SHA256: 314e9dc070092077bd2958209ede3320c82d9f9f651838c86b897751f7cf9288</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-10-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.30MiB (12.90MB) – 615,967 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 262941578fb82a5ce1687a0687b39f38<br>SHA1: 2098781e157e2f42fbad1982844f8e3235412345<br>SHA256: 5dfa322653877b48711a9707b66a4ede77993a1ab1a6e2c11d882fb53e84f129</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>54.96MiB (57.63MB) – 835,244 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 705f8c4383ff8723bab6e94bd7110e29<br>SHA1: 17373c3311c49baffa14b6c45d8657088bba7c74<br>SHA256: ff9decf38621ba742078a2d76f34efadf7149be3c996bfcba4667716700ab685</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.915MiB (7.251MB) – 346,209 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e6d674990e0f107fbd088e17b77f819<br>SHA1: e21f5ede55e9a68287555b79c322fd01792544ff<br>SHA256: ee56d76f9c227d305e7f5b79e40e5d3a11d30d9b4b4a21b0a814bc5fc6ccab58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.87MiB (17.69MB) – 256,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf6418c75d48ec2ce4a2a1c5d27690ea<br>SHA1: 9b685f6a9fe8620ee6003242f3c5acf610337b72<br>SHA256: e1a598f6d63830a2bae69310a4cc6608adaede1395648f0431135c9239a1caec</pre></details></small> |
| | | Full Location | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.3MiB (220.5MB) – 3,682,011 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42145ba207725adfe20cd9225ad15164<br>SHA1: 1d40332c6092241cca96d8e93cd7fb5c58e051bd<br>SHA256: c60c91128d39be7572205c3f816d9173c65edc218778bf32f3d1094e958cfd2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>464.6MiB (487.1MB) – 4,514,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f22f776ceeb745f6db78a0eef703371<br>SHA1: 30ac2eb9a7fa4373473059683b5de9079a24fedb<br>SHA256: de1e8fbe3abd61a6d689615765352368449ce489b189853826fcfeeff7321137</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.151MiB (5.401MB) – 257,820 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8f9908959f108cbfadfc9e7ab6b5884<br>SHA1: 972f263b1d19a67871258f42188f94e931d59854<br>SHA256: 975f5d9342bd724b46443117938bdbe68a26f1a6a67fbe877c780fa1f2a80930</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.32MiB (23.40MB) – 339,151 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 899eeee26f538ee8debffc108e588d79<br>SHA1: 0d77580077bcc05fd3f417a87c32cb013c8833c7<br>SHA256: 113b63ab10291245788982a1804bdc42917c5ba1431bd06f83e8db90d898c105</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,996 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f1a80c418d402b73fffc10b5e33b367<br>SHA1: 477f8a255df756d19d1c4c62f148143d63c6cca2<br>SHA256: 1e61d957caf16f9e8b581bb50ee239a27b4df55d443d3189a6df269d1e4a412e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>286.6MiB (300.6MB) – 2,780,123 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e193b09ce3e796f7ff230a3153398e6e<br>SHA1: 9fb3a062296faffa1023004232fb6fc559be1308<br>SHA256: 65b454a0db4cc428574b15646da49862ae8240441885272744911821e2cca9e3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-10-24<br>IPv6: 2025-10-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.93MiB (13.56MB) – 647,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b3c51dbde46367df229e50ebc84822c<br>SHA1: 6379200fbc3c8c1bc8c78abe5a4d1b8747f30fd5<br>SHA256: 7b54330938cbe0a082134c9f8dd232ade747f6bb49d337cdeec9a119a14495b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.39MiB (45.50MB) – 659,381 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdaa09ae5d2fef3cfb8cfaa3c3779442<br>SHA1: abb298856378abbb9e5ff8d4d63703057019a998<br>SHA256: d66c059b512337c9d40ccfb54d6fb693b9613c01bfb7dfe70e5aee746f9b5f91</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-10-24<br>IPv6: 2025-10-24 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,523,450 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 192cf15e52dc84b1d80bb547f40d0f66<br>SHA1: 58cd7c0d476ac3713339c4dd09a5adbacc68945a<br>SHA256: 10e8141aeeb92bdadee89d72f616c32ebe7a6e1ec89ddcd4ddba841430200ce6</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.3MiB (199.6MB) – 3,523,450 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5aa8dced81967b18696b9d4cb206237<br>SHA1: 382875b3aa565f45ea64bfb1fef3b5fdcd535b27<br>SHA256: 6cccec3ecb3db0bbb7bdbdbe6df02521e56fbf917e835549c1f2205589b6a087</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.0MiB (186.7MB) – 3,523,450 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbfee62e8b8c4ee5c4952f6e9249f40e<br>SHA1: d21bdcd3790f603a923c9ca77da751d2f95341d2<br>SHA256: 85de2c5a71a880db8d18396cab5f050e85eb17aae6c9a968f5b2d71f0016c8da</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.9MiB (189.7MB) – 3,523,450 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26fc81391ba9a0f59dd701a0d16e6172<br>SHA1: 8c5fa70eb0c3541e159249e710ebb71013e601ea<br>SHA256: e3d34e76c6741422b04b846eee65b09d9713827a1406e0b969b76623fbbf60cb</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>226.6MiB (237.7MB) – 3,523,450 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 022889d679d361217fc3e7f1d62830cf<br>SHA1: f575ba2cc521aa2068c5222a6c1a24f47d5314fc<br>SHA256: b672d311d3be5442895a91f68317d74e42ef57459564adf476bd7b772ab9c2cd</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.6MiB (186.3MB) – 3,523,450 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1b47d934ba35b9db92583020df6f272<br>SHA1: 35dc4d08776b932c89608d1cea15760c57635013<br>SHA256: db782d143f9188ea2e09030c58925bf5baeba591d58b6eb11017cda5083e0eec</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.3MiB (231.0MB) – 3,523,450 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e594ee54d34f767cda0b799dbdabf0db<br>SHA1: 2e9d6767e4ec1c9c6c8bc2c8c9c5778708818fd7<br>SHA256: e52c62681fb7741f2425bdca68393b8fc2d9e48e7110001fbdfde23708335775</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.9MiB (193.9MB) – 3,523,450 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36b69d378c460ab0736ee3484aa88c75<br>SHA1: b33285f26581c200ca9305436fbcd7d5d5bc9a09<br>SHA256: 8be83b700ab804a595fe53ec4e5e144bb7ba2068819c49b2d40ba16a5574de26</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>186.3MiB (195.4MB) – 1,963,577 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 594cec3f7f9480331600dee955b72592<br>SHA1: 71b31141d1e5d78fd363b5255eb14276567a5519<br>SHA256: bcef689245d75ce7d0cab20fd97d884ea2a40c3406acfa331ae670f0cb33fdfb</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>190.7MiB (200.0MB) – 1,963,577 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7a2d274f75503f2d3f79b7f2d722e18<br>SHA1: 5e2f74ff4d7d015924471316dd40d4d3cf6740a5<br>SHA256: b1a75e1223647ba142361942705bcb7dc5907856c3ea7486dd3374e59f1dd074</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.1MiB (193.0MB) – 1,963,577 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b24cb0927bb97d082d945738c12b5fc1<br>SHA1: 335aaef37ae5d8ffbcafd0fc0d7128b7f6154120<br>SHA256: 648038cc8762980307e4b9396b13660986210617488bc2e9b854eb47277dcc6c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>184.8MiB (193.8MB) – 1,963,577 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9bf5c8841d5adb2c9831a55d50b59b4<br>SHA1: 0e674aa548a8fe63f3cdcad666b6de7cc5178dcd<br>SHA256: 87a041c9480686c08800084eb3ec6720834d904749a4c999421a5b7c5af7025a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>204.7MiB (214.6MB) – 1,963,577 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a899e4264074bc5fc5a82ed98d610cb<br>SHA1: 39f19d6742b8610066ca98f5a8b0b503b017d4de<br>SHA256: d3c11358b3cdcdf09efe9491b5415f4c61410308e64b92e40ba00484642c413d</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>183.7MiB (192.6MB) – 1,963,577 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3497c114f8bf512d93d9c0bfcf17284<br>SHA1: 4d04d23a7c43be7d122518bd90be6bec3495aa6a<br>SHA256: b7463e9c8d620eb0435c8f1a730c5f9373b11016efaa8b07c30f3d815cbaa007</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>204.7MiB (214.6MB) – 1,963,577 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fbd55ec81dd2ca77061445e888b2ba4<br>SHA1: 2488efdb67ef2c59f4af087555aaa7ff0b57e662<br>SHA256: a5c92590d1ae9d5da6f29227ac451c56cf922e179e8a9aeca5b88aa4a3cf4f74</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>187.2MiB (196.3MB) – 1,963,577 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4dafa18ad9139c10ea08ed3d4eefc472<br>SHA1: 4239149cd89b9e73edf630d82b981a87466e7aac<br>SHA256: ae87dd4f224177a568af6c00a1fca45285d7d6299e1a237cdeb5c21ca4999a66</pre></details></small> |


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
