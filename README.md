[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-10-05<br>IPv6: 2023-10-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.615MiB (5.888MB) – 239,182 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e4b696400a0421970e97e3dff40706<br>SHA1: 0b55270f70c4714439c256e2151aa0de975f160d<br>SHA256: 09f03b99eff3bff495f7a6f900570a1ccb8eff1658cb75cdc8285d57fc379eca</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.278MiB (6.583MB) – 81,270 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f15f23d23d39c263569c52a3679eb41e<br>SHA1: c2a2add522ed470fda404c82a62b1fe37b58d4e7<br>SHA256: eeedc75d318eedca5b6df3fa809bf230d81f7a9a15df727382581b138cda18f9</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-10-05<br>IPv6: 2023-10-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.590MiB (10.06MB) – 407,313 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bde50f20c396fdd6844952efd5796ea6<br>SHA1: 17303cfd6abd189adf8b16c3f2350daf3b8a66ff<br>SHA256: ea50c0a8cafa8c0d218e78e552256d676a1a9ed4b292790d52993dbb61b0dc1a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.033MiB (8.423MB) – 104,086 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59c05f05e61655fe22628b4787fff077<br>SHA1: c3812bef3cdcf9cca9a84cd00cbda352871f8157<br>SHA256: 02f0e01321b568e9a2f56e9749e2442a687989691479c218146370ad5d4bb441</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-10-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.58MiB (16.33MB) – 664,062 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14bef4544b92565733712a202ba2f291<br>SHA1: c40ccccccab6e99e11fe10b958babac730e02562<br>SHA256: f9969f08bfd786a29919ecd18c2875128ded6bc4b0ee10ca67b3094359002c24</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>40.52MiB (42.48MB) – 524,487 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65579e0dad8f36410acbe5ae62ba8989<br>SHA1: 64fea2b67730401f446992602088ae651148733a<br>SHA256: 2d16722aee42da4a8d685b966ce0500600622d64d7c393c5896af074695ada71</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.207MiB (7.557MB) – 307,820 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ff8d81d8ce4efd3476359318175af0<br>SHA1: d105d1c4490b536a83d0461759256799109a17cc<br>SHA256: 4cb45f08b0bbd6d6c4fb204e776835b939ac663761aea652d12ae2ab20494228</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.54MiB (27.83MB) – 343,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3256ab7e4df24ca9917bf92c70b9ce1<br>SHA1: 832b96b707911579f91d2a42cc84b0766c5db738<br>SHA256: fdb03997e4b7c1a6bdffa274673b7756d8dbfb2ede55f1186b3957ade7042544</pre></details></small> |
| | | Full Location | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>184.9MiB (193.9MB) – 3,048,591 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed65f47a5f866d476bde81f05015d0ad<br>SHA1: b0ef2e2cdf8875da35c99816df76f9fa88d3de9e<br>SHA256: 5bca8efa9618ae69c9fe4228342c0ec4bfb4d581ca0766a3a8e45978d1fe7875</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>269.4MiB (282.5MB) – 2,345,213 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f854d9364b9ab55744dfdc557c9f9f6<br>SHA1: f419e9a0b9db7b3c78b5c98927c74c8427f3fcd0<br>SHA256: 3d1595b762a094dfd2f9ac1525dcc77a67ac87dec747f420b0fa63ac4fe51cbb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-10-05<br>IPv6: 2023-10-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.547MiB (5.816MB) – 236,500 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4857bb88f1e540efdbadfb3e56c208c8<br>SHA1: 0190e03fc0543a58ca868f0f36a92556049db942<br>SHA256: 44b7a5f1e09f7ad797ea8511ecfc8ddada844067bdff82f4255273d85906d172</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.24MiB (20.18MB) – 249,120 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5105fe9bbe5d0ddc9bf8995e1cd8fdca<br>SHA1: 48b9366c0983f8d70d79ad112999057d17d64829<br>SHA256: c10da1d1999f1867044c9753957966c4989400bf25df0e7fb02c524b43dc90fb</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-10-05<br>IPv6: 2023-10-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>171.6MiB (179.9MB) – 2,803,356 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4abca24edbdd7d97ffaa621ecb9327a9<br>SHA1: 97c24a0d18b54cd8d2692e708765b79162107242<br>SHA256: 903407a226a3eb479f2165ba004762c64c3a41dd5a9c0d515be1353f99e5796a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>166.3MiB (174.4MB) – 1,448,721 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d928761a3b79f2ef6c55ec6d4dd813e<br>SHA1: e7de15f34cace41d4332e3d59c8ffe729fc2f8ec<br>SHA256: 613e34be98c76eab733c9982022bfa16a5d1ab57fd73444f0d6e8a2ef59ae567</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-10-03<br>IPv6: 2023-10-03 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.33MiB (10.83MB) – 440,662 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dc1906a76fe772c519c8e2c6b517a05<br>SHA1: d272342147c18d3ddd0d5c5f743a79061148aabb<br>SHA256: 0327a1381dfd6b45783c16a24ad7133d5de3f9499dace4f8be57880b9f2d1612</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.61MiB (23.71MB) – 292,735 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d10f1758f01c6c8668a8ae8d6af65e90<br>SHA1: f1eb7506b79437cb59d8d82fed7967754fbb183a<br>SHA256: 18bc35f2478cbb046294c77be8d6ace66ce867a5e9a7bded9f6146d11b903266</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-10-03<br>IPv6: 2023-10-03 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>186.9MiB (196.0MB) – 3,732,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a7026dd2b43f37a54f89a8571c306ef<br>SHA1: 127587b7611774ba40f309ecbabf900b241996ef<br>SHA256: e2e570bca98e83eba056a88450e56e2baaff7f9ba824fea27e1ac1f835b77e55</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>218.5MiB (229.1MB) – 3,732,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a70ad21ce587374e3269f3f0af23d0eb<br>SHA1: 8b56ac5676cc1188a4aa6077b73a0419b941988e<br>SHA256: a164d38b04598ef60fb40ce8acf7fa57077f5e26aa967af2e93553fabb84d284</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>193.9MiB (203.3MB) – 3,732,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 291e62c649fded3b52b18674da0219fb<br>SHA1: 1675569e0df312784b7e7a6e6c165407573d4bce<br>SHA256: edcee600e5230930b45e0792d6712b239ae257e9e42d984aab2752ee62b90b5f</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>200.1MiB (209.8MB) – 3,732,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc20fe47f356a3d7a0695b68b37c582e<br>SHA1: 47721d5f973702b7df1f46bb323aa8a36b756e9c<br>SHA256: c624aac1f03c8df52beb72378dba8b1023449891a8e2e2dff44630a19a56b554</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>235.4MiB (246.8MB) – 3,732,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8aee9bf8b6398d5c3a56787a1ad38a98<br>SHA1: bbd37a2ceb8a2ff0ea64996b76339a02c053d0d3<br>SHA256: e8f74dfc99bd8ae4597132e9a588391068d71d204ec15b7bf742eecdb0e3244e</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>188.4MiB (197.6MB) – 3,732,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f187d68b42e45f919edc14a513802b32<br>SHA1: 058663c53ce9b1aac786087e61cc61c41ad3bc5c<br>SHA256: 199c0e3f6352abe72009f51456f7ad1e0d558a4d50e47cce57737b892c04869b</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>235.0MiB (246.4MB) – 3,732,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68b4ac17cb3309d32b9bed779ee1309a<br>SHA1: fecd843295feadcd85d604b5e0dbd7c9e83b2a87<br>SHA256: bfd2c6cdd7846350f35221e75e81b1f6af312686f306b7f73ce8b5d7f88767bc</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>200.5MiB (210.2MB) – 3,732,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f0d518bb8384cd8c3aa4ef4988ada24<br>SHA1: 87ddbedbe921cc1b9033f2e77353c5f2fc6053ea<br>SHA256: 3dbb1498bab2a51fc3bf6a02fd3daac0d9a98205d35d4258d651b6a2d3e878db</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>132.7MiB (139.1MB) – 1,321,966 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68812a4d53f77a7889aa646e1ad1a875<br>SHA1: dbfd38a78b3632425cd4a777958d107348276785<br>SHA256: a14b9467cec75164b5702b456348d04b5754aeb377f02fc079628486b3aa294a</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>141.1MiB (148.0MB) – 1,321,966 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfdf14da1f59b7d2e4c71e4c05a399f7<br>SHA1: 17f26db0eda996ee8bd28f82d53e8bba670f6fc0<br>SHA256: c44ba2c95e63f0f3bfac5ae2e5a7d3aed29b9b74bf0add31682471270a5ef775</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>135.2MiB (141.7MB) – 1,321,966 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b1c71d22921cbce879c0588cdc5de35<br>SHA1: 31403f35fe59aba40054943921da102e89bc45e0<br>SHA256: 8e7e9a2b94d130b22d051ae3a8d12437a19bb1addc6f13a3796548c2f505d7d7</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>137.0MiB (143.7MB) – 1,321,966 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0b0b44d8eed68f0b17350bbe010f3b4<br>SHA1: ce86dcf9639b92593aade3bf9e6f88b62d59db48<br>SHA256: 06b66cd08894f6424736db56545bac1f331ab6c42957752210d32f63b6d5b527</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>145.1MiB (152.2MB) – 1,321,966 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49e8e63fe3e970aab3927e4b2529820c<br>SHA1: f99314d59302dc548221c8264ac3c7ffa6c217dc<br>SHA256: eb6b29fa84033679461825478872693d3ce071ecd99a11b10cb7ff84b3edbb2b</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>134.1MiB (140.6MB) – 1,321,966 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a35a8d10002f2be8a2500fbf09ed41e0<br>SHA1: 4ebf71ed1a7d939f3995dc108c55d77ee577f4d6<br>SHA256: 27fc26072a76f7d24215cde61b387c77cea3250dc60c4979649d8c9ca8c306ac</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>145.6MiB (152.7MB) – 1,321,966 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7963c453436ccb07926ec926ade17992<br>SHA1: 9fddcfd2329d2c3025134112aa4179ee6a45238c<br>SHA256: aeda42d72bf5b59841b394fe8b7052e964de32cebd5e094f044f6ee7e5d2e735</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>137.4MiB (144.1MB) – 1,321,966 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: abf170d74c652a6cb4b4e1d3621589e5<br>SHA1: 91530da344761ab719d67e4c08a334ec129f755d<br>SHA256: bfe216de1ba1cf96575038e3e382e32de463d6d9814d452c4142f5ebe58ae4d2</pre></details></small> |


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
