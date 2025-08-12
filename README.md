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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-08-12<br>IPv6: 2025-08-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.175MiB (6.475MB) – 309,207 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 217f606394b8bcd9d0f84a0360b6d845<br>SHA1: cd408e37a4a167073359bec099b466747bae3f78<br>SHA256: 28ae582dd401984a05ef2c866664d27286b3f3d6d6e989651158591b12e6d243</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.14MiB (10.63MB) – 154,079 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf95063dcc6056a614da401d068f46a<br>SHA1: f7603609170d2827b043c17e3c70a3191260c759<br>SHA256: 1ea29d6aad2cd2f85dca98659e3eb4d3f3c22f04b9eb6237c4a7db52c1e00858</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-08-12<br>IPv6: 2025-08-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.583MiB (9.000MB) – 429,780 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bcbeb956798c3cd8ad819695de4479f<br>SHA1: d22ff8f50f3b1e684f3b4f64b68e855668735158<br>SHA256: a7fa8500a6cbfbeff137972701dfa50e7d07406d855df90482385b9485f7cd9f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.213MiB (7.564MB) – 109,739 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41d5c9563e2a96782b44f59cc9e9c526<br>SHA1: 78b54dd2baa0a33c795fbd18b17bbf55729019e3<br>SHA256: 62c4f26d9e1438902b17ae6e5944819c968a0cfa0017557faddecc44b293bca9</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-08-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.89MiB (12.47MB) – 595,222 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05523a7c669c951d0929e603a3d662a3<br>SHA1: 5bc9e21eacbf28f40912223b0c6ab9bb22f226bf<br>SHA256: 0e4dfb9e18b4fdcebfcc5ba1bd0cd7e621cc9ea674c85085946294af07379063</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>92.73MiB (97.23MB) – 1,409,159 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d9a81e4b8b623d0031c2c7eb270189c<br>SHA1: 4928781831ff2f761d4461610ecba3a9e3c84513<br>SHA256: 17be0ac6f1dea378b78896e82c76903d8328087eca157469ac1f8dd2a3c7cd22</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.840MiB (7.173MB) – 342,618 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fced5df941addb9056b94a0f6f68597<br>SHA1: de47b1f9ba9f0ffbb556398c71c34fbf530591e4<br>SHA256: db6544ac94d1d22426f86a2b1b3d5b70f2d1b38ecd54fa536f817c5e106d4055</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.11MiB (16.89MB) – 244,855 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f879c057a5e3c7efdb9494722cfb973e<br>SHA1: 2a0586c6bd247669bc87d96e3dab86aee5e3a9ec<br>SHA256: 648aa19d3202320593d396fb44d416960c2d602a521000ac2510160c5d272d14</pre></details></small> |
| | | Full Location | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (216.9MB) – 3,615,295 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84dbaf75b3817fac2d522b918bcc3861<br>SHA1: 9b4ee36fa0923a2f68da4704164feac99f7551ba<br>SHA256: 43bd2f31f3e4f69856dfa6208d46d73b0063c028474adf986db93aef2740a7da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>447.1MiB (468.8MB) – 4,343,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4cfa7e8b0505f21943fa43a915ea9be<br>SHA1: dcb876a3bb589b77672f628a8ae019d6011d447b<br>SHA256: d3f883acce4ef8ed03ae21f30d09b7ca51f895f0830643368c5767a3642faf6c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-12<br>IPv6: 2025-08-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.131MiB (5.380MB) – 256,801 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9f69423f74c7fb611e703eb5df570e9<br>SHA1: d5c029138726289aa8aff0d0ab03087e9ba010ec<br>SHA256: f7842a20f323a1395403bc87af35ef4235bc460dcf668edb7acad3b821fc73c0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.04MiB (23.11MB) – 334,963 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52015cf9a3ea306d1a9fe3ecf0adf6a7<br>SHA1: 7d8bb22c7adf95d07d5aaf3c474fdea8627c9987<br>SHA256: ef4eecb2abf7a207bd40b7f8532e17068fe109151a9901a6e401ed4949741f34</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-12<br>IPv6: 2025-08-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.3MiB (176.5MB) – 2,918,477 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e4d7c4d02eb20701ff7c26df7649eba<br>SHA1: 76c5013213f9c230f5fcb8e671385089541eaa33<br>SHA256: b6482cf9e14d0817cbfb806f67cfaea075d7e21dd6830c40ba5b433beb4a0a2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>280.3MiB (293.9MB) – 2,716,703 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 530b128ef3618aa972c06ebc3ef103ef<br>SHA1: ed0c3e1480b41c2de1a0587230d714aa7706d394<br>SHA256: 8f4b13c4f9e83f5e801b3e6baba7a2ae6665e1bbd683cb7252f177828f5b6cc8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-08-08<br>IPv6: 2025-08-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.37MiB (12.97MB) – 619,093 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23a80eb4be7c0a96701c90544fb53f4a<br>SHA1: db95f4efdec0055d2a47b996026612b94c909b57<br>SHA256: 7d5f28570d9866dbe6824cae71aa5ff955070e083929b47e97d5b523e1b79ec5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.97MiB (42.96MB) – 622,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52632e6315e251640f2bd29cd72b2187<br>SHA1: e6f34a87977efb603e4ed3ebd32653d732914721<br>SHA256: 0e3a7a9fd50d8756096b4299e51ae79b1adc8503f6b94a32d54be98e5949e4bb</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-08-08<br>IPv6: 2025-08-08 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.1MiB (181.5MB) – 3,411,862 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89081fd24adb01a4154845cc8b14f47f<br>SHA1: 920b02abadc78bb61ba3a85e946297df81fef9c6<br>SHA256: 39b9f8c6761b8c8ea73b9d540b600f2e80fe5d068b625f792243a84589510e4c</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.9MiB (192.8MB) – 3,411,862 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41d80f13120ac87933d15ca7391d5a54<br>SHA1: 57e7148ba15a95e135c4e364e66c09050f6a6171<br>SHA256: 9d5793a0ed6ba7dfc36fa1d143543d1e85a38afa9c7c4ee18aa451329deab23c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.2MiB (180.6MB) – 3,411,862 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: abf2ca673e9a15b700119d9576399c30<br>SHA1: 1d88145b552ecac742f79bc02ce6f848d7629c79<br>SHA256: 173506b686ebd1575984b23b6aa3b640e012071ae3688bcfd7a901a2a9ff806f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>174.9MiB (183.4MB) – 3,411,862 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b60e4cb8750550fbb2f11a4b88b3b384<br>SHA1: cb0e334332ca1d2b412bd5c33a96b07334a33647<br>SHA256: 36bca0f99969dcae9a59229755427d6ccdc549a297c48721b371ebd7f459a5be</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.3MiB (230.0MB) – 3,411,862 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36a339c022b4d24173a36cd7f5e10d38<br>SHA1: df5b3b94aa7048f9696459abc64a7b2de52b2429<br>SHA256: 64e1737f6088b737196c697602d18bd882280733caa228e16d3b3d8fa438451a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.9MiB (180.2MB) – 3,411,862 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57225d0008cc2a97608a2a15aebbb41b<br>SHA1: cd20aa7e167c9a8f21f6e2a5d0e250eb0aab460f<br>SHA256: 66e1b305db5a53fd89c29d2ea33286dfb995ea40475c57ab7c41ad2f1e093ad2</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.1MiB (223.4MB) – 3,411,862 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e799bbe35157f03cab76a40956f9754a<br>SHA1: c126a8f7c53d8f252029087aae24d9327929fede<br>SHA256: a8e0eca540dc56da05c9452464cb12d1ed0091b7269624deb040a519aa70008d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.1MiB (187.8MB) – 3,411,862 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 263610af5297a6d0586da4086808a45d<br>SHA1: bdb44313b410f510f73d9618d83e64d34ecdb1eb<br>SHA256: 910f247ee1498dc8014f1e0214bb2f252a1035f2e31e64a4b1d52bb84eaf766f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>168.2MiB (176.4MB) – 1,785,117 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50cb8e64d87cff7b05f5dfc712e70de2<br>SHA1: 5b6120f581f673f54aef5109ee2d90c332d86d61<br>SHA256: e1c22dd94f02faf28568dceaef7a30b18f65e0b695d8a275d0f663d2a61d60a6</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>171.9MiB (180.2MB) – 1,785,117 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37ca992566e6bd6974ae0f61e67d949d<br>SHA1: 66491a0c4851a011988555304b58a1b23110c1fa<br>SHA256: 08ceeda4b26e863bc26f8648d6091f3e2e163fe5fa1f659705982d20b52253ab</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>166.4MiB (174.4MB) – 1,785,117 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46d5037518ee2ef56405b36f18116001<br>SHA1: 3f2ee057928bad9f16c5075d2201866bc269dc1f<br>SHA256: 2010d71068cee1643e6057c81fbf93d2367d3e91af004eb9095a1b37a93aef51</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>166.5MiB (174.6MB) – 1,785,117 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48da44f6818da86a462668343ef417d3<br>SHA1: 0a069e4aae4a929f3cb655c50102af68377a9446<br>SHA256: d0979cc16a5f630e3281efd16e239d03567bf83589bf4d2bcb72b280ec95bb5f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>184.3MiB (193.2MB) – 1,785,117 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4cbee3e202fb70e336f97d794cce6c65<br>SHA1: d211a9bfba4945e79af24b8380927a2b47914696<br>SHA256: d65d6103603d860283bacdf1807a633a5a4720ddc9eafe3480ff749130c972f4</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>166.1MiB (174.2MB) – 1,785,117 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7bcc8154d4313f3490e318e18228920e<br>SHA1: 5c4953e34b20cd3b8da0fe3c1f8f4c6a52fff67d<br>SHA256: b2234949c7f73401e67d2d5d44dc5a932a33321985520926310cd56aada81ba7</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>185.2MiB (194.2MB) – 1,785,117 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb8b2105407d5f56cec3defe9ca98d57<br>SHA1: fae02fb8877a3f490ffbf2e8767467439a8c28bc<br>SHA256: f4c990dc5e887f0310d5fb948c8a9722fbca39ad386c8a9f538cb2bd0d7e4e00</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>170.2MiB (178.4MB) – 1,785,117 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2230750e17d9d5534f39c10f86386e40<br>SHA1: bb136073f7b748fdb4325a59c8013a74b18ffb51<br>SHA256: a0220613573508c7ff2e92bbaa3bf5ad672015ed0f0adf545a737a9f21ccb4d1</pre></details></small> |


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
