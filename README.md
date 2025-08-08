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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-08-08<br>IPv6: 2025-08-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.165MiB (6.464MB) – 308,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6888c6e00ff2cd75562c56c1592c8d7<br>SHA1: bf9e22cfe838def4cb60e34a06222c40c2a12625<br>SHA256: 29b4291ee74d0cac097e3467ebe9ee9287ff528ee2afbf485cc5ccdcc19b6328</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.11MiB (10.60MB) – 153,589 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93b901dbe3c61086868c4c442e048998<br>SHA1: 734145779f12a4c6e5eea2e88c178794c97df22d<br>SHA256: 38bb04bf1da4b4f709dcc7db600e82292d815e3c670f7176d99c740fc285976d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-08-08<br>IPv6: 2025-08-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.573MiB (8.989MB) – 429,277 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9eac227f39408970ebbc362a2879eb45<br>SHA1: ac2d06c1cbf3d48b5538302470eda0470f152372<br>SHA256: a91da619c37613118922193a177b6f4b64aa58c29744f5bcc0ba5c4a2d9fa74c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.257MiB (7.610MB) – 110,408 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea0c637b02b510df92d451fc4edfdb80<br>SHA1: 6a85a3bd6e5bc90c0312a93fcf86b0beeb127119<br>SHA256: a7bb89b0b661ff3f04f20e67bfa5ed520d7cb69b8de6485968b243e60c3d785c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-08-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.95MiB (12.53MB) – 598,427 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 877c0f09e44bb8515c7eddde97a39849<br>SHA1: 5b3d2134ee6c67f442f08d241a10d6956068c075<br>SHA256: b056ccafdca9fbc4f8892f1104565710d4f2e394af1e1020a48c1df616775a8f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>93.20MiB (97.73MB) – 1,416,327 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56db3c362e84d6df40497662ef085dc7<br>SHA1: 8c403368761a18306a65574f68ea9f0ad43c2543<br>SHA256: 28c99c53a6e51eba62bfdf44d9ea4d93612a605eb2082a0b50c28741d75b1726</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.840MiB (7.173MB) – 342,618 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fced5df941addb9056b94a0f6f68597<br>SHA1: de47b1f9ba9f0ffbb556398c71c34fbf530591e4<br>SHA256: db6544ac94d1d22426f86a2b1b3d5b70f2d1b38ecd54fa536f817c5e106d4055</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.11MiB (16.89MB) – 244,855 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f879c057a5e3c7efdb9494722cfb973e<br>SHA1: 2a0586c6bd247669bc87d96e3dab86aee5e3a9ec<br>SHA256: 648aa19d3202320593d396fb44d416960c2d602a521000ac2510160c5d272d14</pre></details></small> |
| | | Full Location | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (216.9MB) – 3,615,295 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84dbaf75b3817fac2d522b918bcc3861<br>SHA1: 9b4ee36fa0923a2f68da4704164feac99f7551ba<br>SHA256: 43bd2f31f3e4f69856dfa6208d46d73b0063c028474adf986db93aef2740a7da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>447.1MiB (468.8MB) – 4,343,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4cfa7e8b0505f21943fa43a915ea9be<br>SHA1: dcb876a3bb589b77672f628a8ae019d6011d447b<br>SHA256: d3f883acce4ef8ed03ae21f30d09b7ca51f895f0830643368c5767a3642faf6c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-08<br>IPv6: 2025-08-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.131MiB (5.380MB) – 256,801 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9f69423f74c7fb611e703eb5df570e9<br>SHA1: d5c029138726289aa8aff0d0ab03087e9ba010ec<br>SHA256: f7842a20f323a1395403bc87af35ef4235bc460dcf668edb7acad3b821fc73c0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.04MiB (23.11MB) – 334,963 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52015cf9a3ea306d1a9fe3ecf0adf6a7<br>SHA1: 7d8bb22c7adf95d07d5aaf3c474fdea8627c9987<br>SHA256: ef4eecb2abf7a207bd40b7f8532e17068fe109151a9901a6e401ed4949741f34</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-08<br>IPv6: 2025-08-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.3MiB (176.5MB) – 2,918,477 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e4d7c4d02eb20701ff7c26df7649eba<br>SHA1: 76c5013213f9c230f5fcb8e671385089541eaa33<br>SHA256: b6482cf9e14d0817cbfb806f67cfaea075d7e21dd6830c40ba5b433beb4a0a2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>280.3MiB (293.9MB) – 2,716,703 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 530b128ef3618aa972c06ebc3ef103ef<br>SHA1: ed0c3e1480b41c2de1a0587230d714aa7706d394<br>SHA256: 8f4b13c4f9e83f5e801b3e6baba7a2ae6665e1bbd683cb7252f177828f5b6cc8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-08-05<br>IPv6: 2025-08-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.35MiB (12.95MB) – 618,163 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dbd32a37978b382cb4b9e7d42cd579f4<br>SHA1: 3a62ac727151301fc51cd68288bc83f9a9b66b67<br>SHA256: 5d82faf402f233a44d2306962f612ca84aa2844e886994cb1688e01b9a582747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.92MiB (42.91MB) – 621,868 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c22879575b4be29baba5212a400408b9<br>SHA1: c5991c5a620997477c72ff7440b6eb64a920d1fa<br>SHA256: 42c32c1a315ad8fbf9942f45efa825f16e3ad06913cb735fd510c288f46c131f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-08-05<br>IPv6: 2025-08-05 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.0MiB (181.4MB) – 3,409,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2292826d3c31bc911226e7ae943092a9<br>SHA1: 0517339e66e286e78528159a0fb1fbb14961ccd5<br>SHA256: dc224b333904b44d74b12baae7114fec3b9189f0a8acb713dc65740fbef67d05</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.8MiB (192.7MB) – 3,409,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45dcd8e40eed1d66a2874cd97eb7be66<br>SHA1: 8bebde87fce3cb036b3b4ca8965ab0b4ebda7aca<br>SHA256: bce4cca2a85946c3761ad2d208764238f7c9dfcbf10f3abc6439b4b11f34cdcb</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.1MiB (180.5MB) – 3,409,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 492a0f2d348ffbddbf5b2f3b17743438<br>SHA1: 3e9f81abe2afc8536b7968cb36bcac0b25cecf5a<br>SHA256: 67886a37936d82a603f90168fc2335e670654f95bd60cca3ad86033708b09098</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>174.8MiB (183.2MB) – 3,409,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9777a63c6e37b6fd90ea0626169c1bbb<br>SHA1: e539dc2eac4e6730c4e6073740beab82e4fcc789<br>SHA256: fdeb16978894d02b74dc111c1360c00c286a1cb6ce9fe13d7beedabc9fd9c67a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.2MiB (229.8MB) – 3,409,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6367462f02f77a1fbe84956cc49b37b9<br>SHA1: 6abc190c07a3cebfb3bbbace89b060d5a8b34dd4<br>SHA256: 87d5e96827c1e9d896f6415e7ac1588c73d022d3176f395b0339d850cb01be82</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.8MiB (180.1MB) – 3,409,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 610fc60e291d4d868072511fe6348b2c<br>SHA1: be6605ea70876507e402b9de4e157302d14b4bba<br>SHA256: d5619029b633be2dd5d2f1a0af110a968f36307f67bb5c4f2427c589a4cd341d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.0MiB (223.3MB) – 3,409,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91aadd001bb245699bb4005d80859a31<br>SHA1: 25c76abea1ebba487c5c6160394505a206a724ed<br>SHA256: d08de8e919b40477d99e4200d6e824383db9af15acc329e788592a13950a2b0d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,409,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 725a7c0ccd7032e2d570c13e0ba87b93<br>SHA1: c27c646fd29f1f0dec8281b86ce9ab417c0e2d19<br>SHA256: 22210020261e54844e6d6dfdce66c409d71e489ca74b215c98ffbf56470f8954</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>168.1MiB (176.3MB) – 1,783,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cc2118965528be8c0ffebe8c6fbe0fa<br>SHA1: 15fadf4b7b348fa9f605ddfcd7cfe8c60914ff67<br>SHA256: 403c87acb8b3f23b22ef8c37e4b90f805ae4238f64ad7ffc83f4e7f1eb8d2911</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>171.7MiB (180.1MB) – 1,783,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21d57829d2b2f30cc48bf32e56cebafa<br>SHA1: 8913a66190e194c95c10aad184e3f66a092aa3da<br>SHA256: 86a32f06caacb75a839183d3a533a5a79447e20f274b27b1761f0aaa2410b187</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>166.2MiB (174.3MB) – 1,783,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04e4c5ca0d7b5be1d5c8245e0b580457<br>SHA1: 4354fa82d2f41972441dc68dfa6a6b83ebfddc82<br>SHA256: 44d4eaaaba9d92253a556d21489289ffdca57414b3b768f7f1f385e129797ee3</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>166.4MiB (174.5MB) – 1,783,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb4855ffe2e5d5cb9b837da39d92bf0f<br>SHA1: e7826681bdd8effccc0166821514f5aaa6f23d78<br>SHA256: 8a753edc981465b610893d179f9c8a1d4b0f6c499cc034a3f19984e359cdaf77</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>184.1MiB (193.1MB) – 1,783,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f01c7964e30c868a9c579cf4dabe5e1<br>SHA1: 3bfac5cff4172f6b11ca38ab5af51896570ea1e7<br>SHA256: f8262a9940c0329538c8ec451278f46c7d83ca6de7da53fbf9204b974d516d74</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>166.0MiB (174.1MB) – 1,783,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39b940fbe0dbdc9ba9e971eb410b193b<br>SHA1: a1f8b59c5201768a70ff8159da7d7dfbe3cf54da<br>SHA256: 2a1dd2c197e468af467caf509ff86351d35eff55508761f538013f39c01df920</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>185.0MiB (194.0MB) – 1,783,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 234243ac538e29451cacd92dc836af90<br>SHA1: 5f200f82d0fafe4a87a21dfb2e8edb08f41d3bb3<br>SHA256: 862c6ca8f194dc7a1656ac62b02ed706c139bb04fe0aacba86e591d817ca6f66</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>170.0MiB (178.3MB) – 1,783,662 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46344b02e3940cfe5880b0f4dcbd19ff<br>SHA1: 19e1da0de2d47b33a60e204361a1dd9e0a03beb3<br>SHA256: 7c8e7c24630507d1b8688a2b8766a58dd668009c1efcfd8bfc1bb92b897c67e3</pre></details></small> |


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
