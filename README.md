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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-08-02<br>IPv6: 2025-08-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.147MiB (6.446MB) – 307,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ea9cea158e3bcbce167cc697521d36c<br>SHA1: d5ddbce634fa2e810c6181dc84af4e04e8f93af1<br>SHA256: 26c63ae14698802f042e38db45cb150fae3a7789500093df2fe6232e87e1209f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.13MiB (10.62MB) – 153,950 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80b99e1331c91fa4b7c3baba429a81be<br>SHA1: f60da0a2fe237bef96ebf9a592d05301e819402c<br>SHA256: 2db6efd980a9a28c1d8a6e792dcdb575ea33073904c35ea1abd7c117345117d4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-07-28<br>IPv6: 2025-07-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.553MiB (8.968MB) – 428,134 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b89aaa6860f40cde6ac2a4bdc97a45e<br>SHA1: dceebe5c47d6e84897ebc9fdf73fc53dbba308ee<br>SHA256: 77349eb3a20eba876c905d55245e65c82cb819c07d81bab823d67e9c3268b39b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.325MiB (7.680MB) – 111,424 rows – 226 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9a71834d9384d8cbc6a6e989859bcc0<br>SHA1: f293f7f62c2330f21db33787f023894ce82ba2d5<br>SHA256: 3b2a170af800dbda3611d6309b30ba03052da609109d1899330d743c86fd34a8</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-08-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.93MiB (12.51MB) – 597,151 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82630d477d44a94b96fcffe47af294c9<br>SHA1: a0f132547d0a9119b000ec100daf97bc82220c55<br>SHA256: f79180e846ba04f22ada79e77ee3b3330df7a3d5f2157719178ee09f02847e76</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>91.64MiB (96.09MB) – 1,392,656 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c30c72241e982b61be3baa6352ce4a8<br>SHA1: f5aac5b7b9297120fe68cf62144ba6d8e9fc6f3e<br>SHA256: 95c78212b041fe9e325467675bbaa09bfecd71528ca9c07d762f3f0a842ee4d5</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.840MiB (7.173MB) – 342,618 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fced5df941addb9056b94a0f6f68597<br>SHA1: de47b1f9ba9f0ffbb556398c71c34fbf530591e4<br>SHA256: db6544ac94d1d22426f86a2b1b3d5b70f2d1b38ecd54fa536f817c5e106d4055</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.11MiB (16.89MB) – 244,855 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f879c057a5e3c7efdb9494722cfb973e<br>SHA1: 2a0586c6bd247669bc87d96e3dab86aee5e3a9ec<br>SHA256: 648aa19d3202320593d396fb44d416960c2d602a521000ac2510160c5d272d14</pre></details></small> |
| | | Full Location | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (216.9MB) – 3,615,295 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84dbaf75b3817fac2d522b918bcc3861<br>SHA1: 9b4ee36fa0923a2f68da4704164feac99f7551ba<br>SHA256: 43bd2f31f3e4f69856dfa6208d46d73b0063c028474adf986db93aef2740a7da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>447.1MiB (468.8MB) – 4,343,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4cfa7e8b0505f21943fa43a915ea9be<br>SHA1: dcb876a3bb589b77672f628a8ae019d6011d447b<br>SHA256: d3f883acce4ef8ed03ae21f30d09b7ca51f895f0830643368c5767a3642faf6c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-02<br>IPv6: 2025-08-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.131MiB (5.380MB) – 256,801 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9f69423f74c7fb611e703eb5df570e9<br>SHA1: d5c029138726289aa8aff0d0ab03087e9ba010ec<br>SHA256: f7842a20f323a1395403bc87af35ef4235bc460dcf668edb7acad3b821fc73c0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.04MiB (23.11MB) – 334,963 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52015cf9a3ea306d1a9fe3ecf0adf6a7<br>SHA1: 7d8bb22c7adf95d07d5aaf3c474fdea8627c9987<br>SHA256: ef4eecb2abf7a207bd40b7f8532e17068fe109151a9901a6e401ed4949741f34</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-02<br>IPv6: 2025-08-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.3MiB (176.5MB) – 2,918,477 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e4d7c4d02eb20701ff7c26df7649eba<br>SHA1: 76c5013213f9c230f5fcb8e671385089541eaa33<br>SHA256: b6482cf9e14d0817cbfb806f67cfaea075d7e21dd6830c40ba5b433beb4a0a2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>280.3MiB (293.9MB) – 2,716,703 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 530b128ef3618aa972c06ebc3ef103ef<br>SHA1: ed0c3e1480b41c2de1a0587230d714aa7706d394<br>SHA256: 8f4b13c4f9e83f5e801b3e6baba7a2ae6665e1bbd683cb7252f177828f5b6cc8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-08-01<br>IPv6: 2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.34MiB (12.94MB) – 617,809 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77867d843637f6db78a3eb8a99c7a6c4<br>SHA1: 046b9aa711cf8cd347e42197b0d7f60943a19e6a<br>SHA256: a1693de86d9cc0da9df5ea0f9d1ad16c4f2b05fbb2f163ff0de38c69fabb8c24</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.49MiB (43.50MB) – 630,472 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 564b6ff41397e83364f296c375f940ee<br>SHA1: 255930e2f109a79b1f73094869b0cdd1af4023ec<br>SHA256: c98f2e1aabea2527c88ef26296dc160a4dda8c8edfc9bb40611ee014d78459f6</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-08-01<br>IPv6: 2025-08-01 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.3MiB (181.7MB) – 3,414,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30ee100c3e00d2544b53168abbf94030<br>SHA1: 6c7deaacc9c34254fe50141582c999e6a80fdd2e<br>SHA256: 389be59ecfa631cdf711933ff571573a5c61d91622f8e00935e047e4b99d260a</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.0MiB (193.0MB) – 3,414,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17540827593849766d38b002aaf2e48d<br>SHA1: b8a093e9d1db731275d4e608aeaddfb90d60d92a<br>SHA256: cd10ba1a96b96eb39ca1d0f85abc7767a01dc6e8e45bfacaa28724e46ddc311c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.4MiB (180.7MB) – 3,414,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ac8f14784ccbb9fc2ae04d169c618d5<br>SHA1: 80ab4f7caff7e654104645ec16513c7f72536741<br>SHA256: ca5369ebf9df1f93a4704acaece44f52571e49d255b979a0a18e6a41b4a101f8</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.0MiB (183.5MB) – 3,414,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce75224cd49af2f4c6d501330d9a71cb<br>SHA1: b388000704eb44dcc881fbbb1fe68999773bc361<br>SHA256: 6483c457738b5158a3c4550dd03c3d95e8dd1c9687259adbbfa7e74d9e773d08</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.4MiB (230.1MB) – 3,414,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2af9c7c09355e6753ce20da768b16a8<br>SHA1: a2dc4a0c81be28d15774ae8b62cb5fa5af04a85e<br>SHA256: c2b073b27a01550f6ec93bd4ff4c776d94fe2fb970d496c101eba7c2aa129e40</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.0MiB (180.3MB) – 3,414,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b9f528343c21c9bac8acf63f68e9f7e<br>SHA1: cf99eb5abf7ee2cc4e86033ec8da9a5aece092af<br>SHA256: 4f2a735d6fcd0648d18d1384531e841524485f9a29d7c8441eca9c2d3f7ce11f</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.2MiB (223.6MB) – 3,414,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f87fa01bbd6d91f9279c450b0dc45a32<br>SHA1: c7e6599c140c5caede185751f72c0bfe09aaefeb<br>SHA256: 459174293016668f1df1350b38036d566c02d60cc79fd14cb8fa59bfd47f9879</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.2MiB (187.9MB) – 3,414,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78f7390b541b37b184deaac8b8d959d2<br>SHA1: 7123a06d0b9de2465ce8a245242ec63fee057a8f<br>SHA256: 16a67a88ac22aa3766ece7e2ef72057786b9a028e9900bf04a6c6567e63146ec</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>167.1MiB (175.2MB) – 1,773,882 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 210fe57f4dbf030cf5c230596c9e9dd9<br>SHA1: 9749852c27ac54604c3b38d085a2629055fa3d62<br>SHA256: 85d9284b7eed0384c184e9bb0e4b320e0176441c90916173e6ff117db8f30bb6</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>170.7MiB (179.0MB) – 1,773,882 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4feef1d060b719ffd260478bc367b2aa<br>SHA1: 94eb23eaca16c1dfd5452e868fbd01521e716997<br>SHA256: 2a55e7e1e50e81b11c8fecaff7ea96fd481ae2641c4b01a2ffe694abaad3e313</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>165.1MiB (173.2MB) – 1,773,882 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f33eb47c62ae90ea9dbdf6e1fbc4e31d<br>SHA1: 8f9fa84d33c990f0ac915383e4a05c5a33f9b6e9<br>SHA256: 67f4d742bbb56efd00f26d98e02ca07cc5b9c266c1f915589c3db1128b42c7e3</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>165.3MiB (173.4MB) – 1,773,882 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26271fa7e939a6a4da6f355379d46139<br>SHA1: 9e75f2f5ff5c1819f153835156c01061cb2a7d85<br>SHA256: a2da46f2bd4f33dac55d184fba64080aa29572e89d304dd2a581114b1a9d35a4</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>183.0MiB (191.9MB) – 1,773,882 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a70aa24622c34c725f4c022791691e0<br>SHA1: a43c4d76f2df80b7db6468ce0deb726d2544807b<br>SHA256: acb3e9211d68ea6abe87d5cd163ca4fbe2541edb208016c1e39c0b22d49aa595</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>165.0MiB (173.0MB) – 1,773,882 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8991781d88c85271b264ca1588738a80<br>SHA1: 75f431b9defa64706d694c2a19cd803e82e74836<br>SHA256: ffba812a443cbc79b91eeef2dfb763ca15dac2a413cfe38ead930aea8bafbbc4</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>183.9MiB (192.8MB) – 1,773,882 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3626ed4cc099faf7ed5a0fe8b31a9a5<br>SHA1: 292d105c459411cea83071b4c05c7d5948168bdb<br>SHA256: fa00bf559797ce13f33f2b951a68a6af56dc7039873c0c8e88fe3b801c685bb8</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>169.0MiB (177.2MB) – 1,773,882 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ae54144dbaa49b069b9d34dd721fe83<br>SHA1: 27683d5fd15164b96c79cebdc72dd526c7800c1b<br>SHA256: 4b488fef14fbc0c2c9e644a8efab46f4b8400c0e58ed85d31a8f5dc1b3c11daf</pre></details></small> |


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
