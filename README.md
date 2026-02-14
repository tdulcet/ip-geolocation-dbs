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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.454MiB (6.767MB) – 323,165 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65bf8c37d9359f16cc32ccc68257ff33<br>SHA1: 2937c6b8c4af5068e0b0e7db1223c7a19fef5078<br>SHA256: 34162f3f0cca2cdb54b5e003d65167260168dc26814744d118a3cbfc98a86719</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.24MiB (15.98MB) – 231,551 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6921d2123ea67edbd1d8d5cabedb8d49<br>SHA1: 02e1bf1ddd0bc05ec6ca873e56bf75984386747a<br>SHA256: 786557ed9e0a1cc0d9fb664c2ff81617faf25d63f94ac28f8d342c95751256c5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.784MiB (9.210MB) – 439,820 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4592fdbb2895a38eb64cf359d9849eea<br>SHA1: 724437088310013d82527e84e9e4513f35106976<br>SHA256: c393ceba8a7612b7507a31426312af09c94d8c447742742ec0145fb0187766e0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.616MiB (7.986MB) – 115,854 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6544cf8667bf0f94348a9c732596042a<br>SHA1: d78af94e5b58862cdc2bd7cdde05dd2c1f869ddf<br>SHA256: 9f97c153d181164558766b56a91b5033efcf91474c9bd695658ccfb7545d46f4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.19MiB (12.78MB) – 610,051 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6e567050e1d8aad1fe3c4e6fcc3fdf8<br>SHA1: 70ab7ef295a5d2f6a245183a240c8b9916e78272<br>SHA256: 7f380f5b77f4350a52bc21ce6b5472d18c84f22a5a636b31474720a5465d0756</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>97.91MiB (102.7MB) – 1,487,889 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2f9aaa2739ac332dd9924b6ff033aab<br>SHA1: 28bd06bfd91ab752a80d4f4b71bd817d61a37605<br>SHA256: 5fde1ec80b9c94569f5c537f908eabebdc78f0dd4994cffe28fb0138af9a2c3b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.768MiB (7.097MB) – 339,077 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0181205d24255559b4c2a13fdb0c95<br>SHA1: 77c5ed2ef6799485a1ff6d1bd9aa3aef442555aa<br>SHA256: f1a904010b8cf3e5db4f0ddc1b0fed4c77f852aa52effac37a04697ddb879a37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.90MiB (16.67MB) – 241,625 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f8f77acea5ee52ad5d81c9f3883d7a<br>SHA1: d3a894c2e7503a5fe5168eef49e53379425930d2<br>SHA256: 80ee4bf63ff4562160eda9ba68902de89a9e28a828c048003fd188647039bf1f</pre></details></small> |
| | | Full Location | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,746,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48770c63478550e9d616b0e8f11eb35f<br>SHA1: d754e9f10a536891a6f76b212ce1527fccbb205a<br>SHA256: 3abef96589717a094c9384cc0d2e88d16dcc6c1771a5eb42954efe056fe2caf0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>452.5MiB (474.4MB) – 4,397,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d15359a3c2245bffe65895c5939244<br>SHA1: a5622976378fbaa83dd68ce8bf186161f41252b1<br>SHA256: 3c33680bdbdc577647e1e500060fa0db02dc2af50f79e20bb78a7ae7ca1b33bb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.379MiB (5.641MB) – 269,229 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8df1f43c6aabf7404b9835918b8fde47<br>SHA1: 601b465ff0736111423be419aac3f6d5972b42f4<br>SHA256: 80bbfe7421ce68520f39ab366b0fc481427602add22c34ee6881ec43a96b1488</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.19MiB (23.27MB) – 337,206 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48696b7a642ffca450b564a365389e84<br>SHA1: 2da10da7971a84e435865041021aedd433c35db5<br>SHA256: 360124b18db3ea1ff8adc37d7d8c7432d236ac9d3e5c9f77123d8069ac8cd7ff</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.6MiB (179.9MB) – 2,969,494 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5343189d8e7d3b6229056c21a834739<br>SHA1: 8489f2c88b7fa2b7726299d47a687a5af88b7259<br>SHA256: 5f47bc0d8ce6968a1388a93536b1e895b0ddb335cd76007a7b142ca0fa206970</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.6MiB (307.9MB) – 2,846,346 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c67fa86a08014c894bae1e43237dbf3a<br>SHA1: 1bfac6af73658923732d9bf178d37d1b4cf1e23d<br>SHA256: f5b735e687c937676bc7cd2a6d383e598ea54e61f46b9863d97f53062b1634de</pre></details></small> |
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
