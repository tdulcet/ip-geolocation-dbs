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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-02-17<br>IPv6: 2026-02-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.451MiB (6.764MB) – 323,025 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b85992c46c1bcdc78eac4e62e4dce6f<br>SHA1: 01f285cda6d56e1cbf546198b95295a42624e773<br>SHA256: 75299fb8bb6204301a548721e338a215775a384668392f2eb721c129efd2b2c3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.20MiB (15.94MB) – 230,998 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38540582f57791215fda51ef7f9d2718<br>SHA1: 83a4459a24cf38bfdbb81a15e53232d3fe3b0d05<br>SHA256: d7f44aeb28cbe5d89faaf0271e18970eff2dc2084be632dd4b9a01aa00293992</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-02-17<br>IPv6: 2026-02-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.785MiB (9.212MB) – 439,899 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0430c8cfc35965be5a64b118c4b8f096<br>SHA1: 03fbaf8f9eb4f6f10649faaf444eac0b880e255d<br>SHA256: 0a7cea708e720e782730fcf785a4d63fe1b20f9af78b7a75d603e6ed9aea5ef5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.609MiB (7.979MB) – 115,751 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7803cbf3ab5fa91d98974afe38c5ebc<br>SHA1: 429ea5f473364e2458e6d66c028a07383f766d83<br>SHA256: 1c5e6f3c80d095a0951a61c46e04263be7049bca391b7bfb0abf724a84f071e5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-02-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.18MiB (12.77MB) – 609,795 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6dcaa13ac17e061c3c73b764b08266e<br>SHA1: 7cc2c01c37a765db196da5b5c3429b05639373ad<br>SHA256: be1ad4d6626dc07459ea7f9caf489d57d70b706f8818d4e3ea94d7c8497bf485</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>97.84MiB (102.6MB) – 1,486,776 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff7117ea0e7d18fed8b237a8725d518b<br>SHA1: 65f4b4b0b63e300b2081d4fe50e6ef6e80fa6746<br>SHA256: 59390966476b61e579170c75b4b15bd9e0f634111b9655b6159b3a546a1c9d32</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.768MiB (7.097MB) – 339,077 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0181205d24255559b4c2a13fdb0c95<br>SHA1: 77c5ed2ef6799485a1ff6d1bd9aa3aef442555aa<br>SHA256: f1a904010b8cf3e5db4f0ddc1b0fed4c77f852aa52effac37a04697ddb879a37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.90MiB (16.67MB) – 241,625 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f8f77acea5ee52ad5d81c9f3883d7a<br>SHA1: d3a894c2e7503a5fe5168eef49e53379425930d2<br>SHA256: 80ee4bf63ff4562160eda9ba68902de89a9e28a828c048003fd188647039bf1f</pre></details></small> |
| | | Full Location | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,746,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48770c63478550e9d616b0e8f11eb35f<br>SHA1: d754e9f10a536891a6f76b212ce1527fccbb205a<br>SHA256: 3abef96589717a094c9384cc0d2e88d16dcc6c1771a5eb42954efe056fe2caf0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>452.5MiB (474.4MB) – 4,397,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d15359a3c2245bffe65895c5939244<br>SHA1: a5622976378fbaa83dd68ce8bf186161f41252b1<br>SHA256: 3c33680bdbdc577647e1e500060fa0db02dc2af50f79e20bb78a7ae7ca1b33bb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.362MiB (5.623MB) – 268,369 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4330c0bbff3419f12c7f73fddf1cf704<br>SHA1: b4df563510fe7f5fc4e1d278ea041c62c7bdca5b<br>SHA256: e91c6b0f644a92d45674456c276b13846b9893bbf0eb311dae698ed2f3d44d57</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.43MiB (23.52MB) – 340,836 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a2d9ae09529fd0059afa4956f1793e0<br>SHA1: fdd2b4377c51cd148c50a2369808306b7c9e9c10<br>SHA256: aa8f17dc70c0dab48cba63b84addf77a95f2d154825fa5a1cc5a78e9b68ebfd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.7MiB (183.1MB) – 3,022,797 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63a84f26611e75064d6ca0974428a919<br>SHA1: 8280052bb209735824b9571ba8e1d3219f239f41<br>SHA256: cb6a41dd6ecfae830dbf227d07287c122fd823f9a56e968851d364746039495e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.5MiB (307.8MB) – 2,844,839 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a06e5ce285e86fe3c964abd92c36fbf4<br>SHA1: d5da4217a5c723981f96fe1b85823103e5248e1b<br>SHA256: d40b02049ece0c3e7ec8afcbbbece0eda05c646fb3a3a4719bd5bbcc13b321b3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-02-13<br>IPv6: 2026-02-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.08MiB (12.67MB) – 604,769 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 247304c6267f9cd87002149124fe9107<br>SHA1: 04783a38c793ab79a537d43ad15efbb9b179e4fc<br>SHA256: e94891d2ee206197e5e453a9c9fdd601317eb578aeac7da6b8012c7b6f132400</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.17MiB (45.27MB) – 656,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4893d3ddba7c80496acb9cc4a57e3bb9<br>SHA1: ac9e3b9f7dfe0da745bf683ce24b70b9f2247e6d<br>SHA256: a6c5fd38fc27277c3f87b509f676718ebba58b7257cefab599dd29931bd6592c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-02-13<br>IPv6: 2026-02-13 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>129.2MiB (135.5MB) – 2,588,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66e5056b618d721ea392a42cf7bd9e33<br>SHA1: 455dd5da45a894ed0fcf52c34e0036a77f3a8534<br>SHA256: ce20fc90b1ec289dc7abcf711a3120e2b7be4fdbdeb658b6847063f94b274b1f</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>137.7MiB (144.4MB) – 2,588,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 574527d4476a2cd983b01cb5864b902c<br>SHA1: 64f9833f175b3430b5495cd81d29358fb7f0a62f<br>SHA256: 67007d6f70c963086d120e0dcff6a1c5da876a1a5b1f13d8f81305a4ee4f093b</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>128.8MiB (135.1MB) – 2,588,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39897fee7353c260011d11887121f869<br>SHA1: 4621cd13b0930f5a90a22fa45d25c143633fc9f2<br>SHA256: 4375dcc6c7271858ff74fd4962db137038158c5e7e030884bb2c1ebc10635208</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>131.4MiB (137.8MB) – 2,588,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 688a4e960e044042cd8ab3b714066cec<br>SHA1: 365dffc7107905d64591cbd123a21c74b344d112<br>SHA256: f27e41959ac1d793c20c2ed392027e9bee3c8df42840d8f2d31fc8adc838da5f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>160.0MiB (167.7MB) – 2,588,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae1acd67ff23e3a54bec9c1ec568a5ee<br>SHA1: 1b15bbe56de012d382ee13ddff896b74925ef464<br>SHA256: 25231fd1b23fc93bee522c8db3b52bf3cf7ebe60ec72a80f429faa33ba67477c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>127.8MiB (134.0MB) – 2,588,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3350de2f4326fc8d648d65a115df8601<br>SHA1: c2e1c5fea3356f3eceffc45e3452bcc2bb392fcb<br>SHA256: a8fa9c44f0a51d04994bebe10894c4ed209d0d3b30d53a7e3c66fad2b38213a9</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>156.7MiB (164.3MB) – 2,588,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa8a94106cf1df92df7af0cd0969b450<br>SHA1: d0e8b58f64d48c7a2c1cbd0a55e34b4edecad61c<br>SHA256: cf116eae1992652a0344132f682308ce6db1a2360fbda74b207f563ffdc9b997</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>131.4MiB (137.8MB) – 2,588,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 547cde4b5e24d15819699fd0fdcb6b63<br>SHA1: 6e3fa4dff997cdb61387e9f7853effdaaf422f23<br>SHA256: 4b270839a43ba011bfc563d135cbb8eb65a9786b7c32568d4c6444ba81240de5</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>186.8MiB (195.9MB) – 1,969,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c80fa92c99f018e3d1f0acbbb7c5afd<br>SHA1: 6622db95787be02177002e2eae144b47158e490a<br>SHA256: 8330ae4f5dea6380eb59883f527a58be635327aa46b8031559ce8d7e4013959d</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.0MiB (200.3MB) – 1,969,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e29f061b481eb9ac7301e18d2f1cd39<br>SHA1: 3c2fb02db20a90b968e5223a2f19a40b4830df75<br>SHA256: 0bb26018310fabad9fab51f325460e95b93d81ee834690f7fb78f7816eccd0ac</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.6MiB (193.5MB) – 1,969,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6446f0088f3d06d598fd8f6080b94369<br>SHA1: 8ac27588579ad96ef4968d7d4b7b60198be9da0a<br>SHA256: 91e3aeaec4031ef857e77e7a71f300cf3682ca8ffca0d255cfa531a2e007d204</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.2MiB (194.2MB) – 1,969,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed22265f38d9afa9347474aa5e24fbb<br>SHA1: e8638fb779f5fe04fb10278c3de1fe8b2fa0b90f<br>SHA256: 8fbfc08162da6072446c121b1c6705b1a676b7ce7c56a600bd17a8ace4ed545b</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.1MiB (215.1MB) – 1,969,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7caff8b990d5484668562fd1d90f201c<br>SHA1: e5b5ab76d55075bdcf879124a1cbedb7634a326d<br>SHA256: 7b5258a7fda76c00a6fddc16c59882c124050236425583be015ff53c66cde303</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.2MiB (193.1MB) – 1,969,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff79fab40c1e9a4b15a9cc8531bfb08c<br>SHA1: 5445c2d989964bfc424dcb44dec2100a9fe8694b<br>SHA256: 2aecd86a957a942d10bcbf353a1a5a8acd0413ab6157ddd4056e5125bd5ddc1d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>204.9MiB (214.9MB) – 1,969,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa36a70d49d07559342cebec18805fd8<br>SHA1: 5f03db5d06babec448f9d35c28c7aadf2142cf75<br>SHA256: 8947968c57f528eccd85f5e9e9a3fd0ac23b6cd5d27f384b3e3ec4a5d9cc3aa1</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>187.7MiB (196.8MB) – 1,969,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fc934e9b236801b40d4d2217f4bb90a<br>SHA1: 0486ec3e61e83e71342766fd885ca57215247318<br>SHA256: 071b2baf1f2a59190e3a815cd0b3d7eb680371be3bc9c6794ff588b6ff34e7cc</pre></details></small> |


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
