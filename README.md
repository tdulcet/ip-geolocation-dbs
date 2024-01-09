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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-01-09<br>IPv6: 2024-01-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.772MiB (5.004MB) – 238,919 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e24dbdd9c9d8cdacba8353e22724bba<br>SHA1: 88944be7f5aa18800db5848274ddb70f6b3b2f03<br>SHA256: 17910141c0c1b59f4ba1d950af61d8c6555b75b3cfa6dd76905e3b465d99ef49</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.466MiB (5.732MB) – 83,069 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1753db926f5f5b4ed154a41536ab13cb<br>SHA1: b0819ec850fdb4638489ca6e97bcbf559a6cd6bf<br>SHA256: c93e71a42bde7c249285b32d0bf8b310dbf89ffb4bc71d2410c8c2d01290dabc</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-01-09<br>IPv6: 2024-01-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.243MiB (8.644MB) – 412,803 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 448e535137f4293bab496922ebbc7eb0<br>SHA1: 800be99b9923698251a69c7d287cdac92c010c59<br>SHA256: c64fd98e79ab7d4ca561a0253283d07e1f0ccee691719ca91646024924bd2f5e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.895MiB (7.230MB) – 104,894 rows – 226 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9908563f094f5e672ff311608514200c<br>SHA1: 7feffd7dff11e3c3e608bde7afcdd3b9e9906e61<br>SHA256: 5ff798a6b86b341f0e40a6aec1c3cf9c9060af6efbd0e9bb8815382d05bac722</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-01-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.73MiB (17.54MB) – 837,553 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 764b3db3bd4aca0ef9066c6523cb3193<br>SHA1: 859154fcd91332bfd95432933417cb8ad3610c5e<br>SHA256: 8977dbe895508f64e30ff1ee0849424a7213badcd82a827ad637ec5cc0713638</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>50.27MiB (52.71MB) – 763,909 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db73c0bd4f1e3ea6ed552341b87652a1<br>SHA1: 9f5f6d2bd1fae6a927c9b2b877b57d4222bca0cf<br>SHA256: 08c9a4347eeaa69ac11e1ca7824283f9bb3c2089162e6ed55b12a1f69c4339c0</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.162MiB (6.461MB) – 308,408 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736158b820db1062b003cfce212076a4<br>SHA1: f3b03108eb0edf83c338abed05e010c2b0e9cde1<br>SHA256: 68e446a0380ab263a21743f68ab8aa6b249b213af0d6ffdac0780fe4912cb7c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>21.05MiB (22.08MB) – 319,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73819723f00de32c17c8aeca84d93383<br>SHA1: 71d954fffd9f9f5979ff89981fcfae6f73cadb05<br>SHA256: 1328a782f89b58d1f6fabcf3542ce4bb259d89c1f28a0cc70abfe70b5e573eea</pre></details></small> |
| | | Full Location | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,096,472 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b990a48af772fbc4cf7093aa51d35b4c<br>SHA1: 8ddfa8795c4c534c0bfd99b2472382b368d7fd5c<br>SHA256: 117938f84386f9ca627464e7c42856b6d9ff4f68bbcac12a393b73ea1ac0836f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>243.3MiB (255.2MB) – 2,358,639 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c61e48446e598bab5cfa16234f5f136<br>SHA1: c3373a6fe2e2f8e08a48274939c4b494fb99b5f1<br>SHA256: ff81c189923d299847f5b5e0e5c472fe10d836d11e24fa5379a2def67c998406</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-01-09<br>IPv6: 2024-01-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.626MiB (4.851MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24caac24a9c72bc3caa6451ceab08833<br>SHA1: aa114043e64d74ecd9e8ccd339b80c62d3fcbabb<br>SHA256: 6d48a0384e6e4d38820ac8d2936c12db7eb726dfe20c59600d4f14d173e3b15f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.10MiB (17.93MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fc970b50f7b01de0d0c6bd29224c13<br>SHA1: cb1fe32e67d0561cefef5f2908570ae3af446a24<br>SHA256: e0f36200f10f817a89b6cf80d8d459900c5428a669cc706af32d15b709a8b624</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-01-09<br>IPv6: 2024-01-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4MiB (176.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4104f39d8c379ec8967157286f495717<br>SHA1: 440c75c20491f104948897ce552c95510badba7d<br>SHA256: 6689c6e63153fcbdc00272e2ec6cf04f0c6877860b4a667b3972dfa08c898747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 142dfb0f4dc0ceb4f5a41b018ea53524<br>SHA1: 284b510184f46179e9e34f60dd0db14fc72f3e50<br>SHA256: c57159c9a8879702623a2ef4d0c2fad06d21e96f1836db2d3a09f9216aee1641</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-01-05<br>IPv6: 2024-01-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.185MiB (9.631MB) – 460,118 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e0bfa1e2680407cac1bbd4d78a7534b<br>SHA1: 733c1a2d5689d7ea28db269577364658d31c2215<br>SHA256: dfd8732e1e80e2308986e604f2a85f1a388699905de233ad8aab03613c1ad7e6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>20.17MiB (21.15MB) – 306,550 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5eba152bc0ae719bbd2a37cd7ce08210<br>SHA1: 25d6338259675e94e579e07250b7e7918c6210e1<br>SHA256: 7c250407bbe61695e7fd0fec53817ef638d9d277df1d8c2b065df1463d446cd8</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-01-05<br>IPv6: 2024-01-05 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>157.3MiB (165.0MB) – 3,353,120 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: deb4feded02895f0633b186b81cc276b<br>SHA1: 2dd847146251492c47a9362fb9435ca267c14fbd<br>SHA256: 21c1e6f852ec370592fa488aca2a0f2aceb82195da32ceac135b233ad78df351</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.1MiB (193.1MB) – 3,353,120 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0832476a7cfba29d7d4b9e3de696016<br>SHA1: 7eb3236257dd70397b4b7171e65707aa92b8e609<br>SHA256: 118c32d5fbad6b2d1112ff8d01475d8847ae4ab51a4649b3cbc0144202e0793d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>162.0MiB (169.9MB) – 3,353,120 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b86d56ee7417ee63331a25d57751ff2<br>SHA1: 88e979036d3491b6f56babb98cd077b481936ee1<br>SHA256: 029dc2228a11f7d43fa309af869e3bbd2b81242604001d343837b5e6f97e9e17</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>168.2MiB (176.4MB) – 3,353,120 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1fa4116d962cc4505985fb9b17b6ab94<br>SHA1: fccb3b920ede99ef7f608ebafd011210b1829dcf<br>SHA256: b074f494354cadabcd46dea9f1e5a57d77abd985e7acd2fc0ac0136135c2abb7</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>195.1MiB (204.6MB) – 3,353,120 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccc4d20aefbec49290c4427d42760855<br>SHA1: c00b461a4116a163bff07fde9dca634f374ff920<br>SHA256: 054e5b07da8bff435723190e8f17b56b2772ecca3fa0cf972fa59ab23ffe9423</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>156.9MiB (164.6MB) – 3,353,120 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 828c0ee5eee3ed8690787f04ae4352db<br>SHA1: 8c4d59cdbdee291937d74e690d1d117a604ad6c9<br>SHA256: f6c0150ee8151f143ba226c40136a95c6407799f31ed56345dec40c9d0c3c44d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>196.4MiB (205.9MB) – 3,353,120 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 542df92f26e5b0d3dd5b2056fbedbd9f<br>SHA1: 97983666742f934bd46e920c9cb505cff425208a<br>SHA256: a82aec5fbb64438621691cfe52c803511ad2f9b98d021f91f368537c667f33c7</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>164.4MiB (172.4MB) – 3,353,120 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa52bb4cbde165f35945e822dce1359b<br>SHA1: 6617e791f3571b8338ca5bc0e82dd8e35deaaa13<br>SHA256: 969bd76c8c7586428bc6d2581ce614329e3d008c6fdc1437f678793bbb6ae46a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>105.0MiB (110.1MB) – 1,180,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cf11a21886ef5846b1371f6e73e89e0<br>SHA1: 92dc9c976804d4cf8f0fc26888643206c22e5d69<br>SHA256: 9aea0ff5a70090cbbd9dbaac991ba6981ed6efb675ad6e9addd1e99c5ef7df0e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>112.7MiB (118.2MB) – 1,180,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f65e4c66266168e7578ff4c0a1ed254<br>SHA1: 6370dea551acdd30f293320edf7e1de5b337aa61<br>SHA256: 492b173ba8528ce879c3a5d0ab28ee3af50e777b514937ad815ccffe2ba47cd7</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>107.3MiB (112.5MB) – 1,180,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b84b18c3715ec2d287b6473767c1e691<br>SHA1: cfc67491a6ab9ec6284cee71454cff8d1d5c2cee<br>SHA256: c4b4cd52c21837f904de3c3123bb5f88948e186d94b4f6c431248c44787c0d79</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>108.2MiB (113.5MB) – 1,180,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4128f74300b1ba1e2c7d52de8c5c5672<br>SHA1: 0c211bb07389446c5b9d317d8a83bbb79ce7bfcf<br>SHA256: 4d21bd267cad83711bdecd971a853feadd9b5a5f1a0dccdaa5a8a85121220466</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>115.8MiB (121.4MB) – 1,180,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d29906b6e2af18076711f5309a9583fb<br>SHA1: 299a467390d165266aeaa83ecba4914e5d6a7888<br>SHA256: a4ba551e61ee05617d77c48cb3cb484b233a0573da319fd092e5da0d305e338e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>106.3MiB (111.4MB) – 1,180,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2a02845b3a714b18f57fac67f29f714<br>SHA1: 11b7f118bdb01d768583b23b2a996c9eb0981f76<br>SHA256: 7f61c3e5f2d32d42f638a53fc49e86a20080dd3cc2495cbddfe5132322c1ab14</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>116.4MiB (122.0MB) – 1,180,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dcdffb4aafe9365ccdfa77186ac466cc<br>SHA1: d353f0890e32fc06c2440d954c63e52454ab1b84<br>SHA256: e3d065aeb74651c926e2c13a1c83dd2de74e144ad09a118b461cd95a73171141</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>108.9MiB (114.2MB) – 1,180,442 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edaecff4d29a432da8b7febbb0879917<br>SHA1: 964d0de8f423ed819c81e7abbf0493b73b14c216<br>SHA256: f0898217e4497ea3d64cb407a7ec7986e9d30bdacb1602104dd867a7ee6f0bd7</pre></details></small> |


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
