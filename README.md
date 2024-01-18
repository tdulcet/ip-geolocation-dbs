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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-01-18<br>IPv6: 2024-01-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.784MiB (5.017MB) – 239,519 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 052e7f37c898b2e2d50634cca70d7ba9<br>SHA1: ea6570f5d6a516b198c701411b5b597a969d4ede<br>SHA256: 564ac02bf2df733e2c0c19f9b1b77015ca37b97e03bb3f3a018f3b5160eb9c33</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.511MiB (5.779MB) – 83,756 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be96ab04b7350c31155961639a7ee67a<br>SHA1: 73b9782885dd333babea914bd60c93b11f45e22d<br>SHA256: 02bae7ae0e151cef1f28d9e116e4b007309aa20334f222b3a47282b0b3ababc4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-01-18<br>IPv6: 2024-01-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.222MiB (8.621MB) – 411,727 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 189fd538ff559f607e122190ef204cf2<br>SHA1: f0065b13fd6fe0186e21f066f63c063e01bc3091<br>SHA256: c2b73aaf06a7d77558ed5bd87a42dc96a83a533f78081f52a361a61a2c4c70d3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.913MiB (7.248MB) – 105,165 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3da9044b2b2d370669b8e8d5404ebd15<br>SHA1: c76775dc8b524b500b870ff66975199ace1ed8a7<br>SHA256: 2df614a487cc79ef7bd0f851b4d5dc636b6f83e2cc4efde06c1cd96854785702</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-01-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.88MiB (17.70MB) – 845,102 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eccbeef01c58641b08a84205c5c32863<br>SHA1: b79b6fa534eef3366436bbe93734bf53e57ad8fc<br>SHA256: e7be96eebb9b6ec3864009c027b39032de86b343bcaaf306a7134e83d1e47aaa</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>53.80MiB (56.41MB) – 817,529 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 692940bf4a0ba97cd3a83e4a5b5c2227<br>SHA1: c6cb6e26e6cf9a25901cf01762708f11c667e50e<br>SHA256: b75f95b75143f9f0711f2765f8e7d61181916f238da31e9f516b1a175164fc9d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.162MiB (6.461MB) – 308,408 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736158b820db1062b003cfce212076a4<br>SHA1: f3b03108eb0edf83c338abed05e010c2b0e9cde1<br>SHA256: 68e446a0380ab263a21743f68ab8aa6b249b213af0d6ffdac0780fe4912cb7c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>21.05MiB (22.08MB) – 319,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73819723f00de32c17c8aeca84d93383<br>SHA1: 71d954fffd9f9f5979ff89981fcfae6f73cadb05<br>SHA256: 1328a782f89b58d1f6fabcf3542ce4bb259d89c1f28a0cc70abfe70b5e573eea</pre></details></small> |
| | | Full Location | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,096,472 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b990a48af772fbc4cf7093aa51d35b4c<br>SHA1: 8ddfa8795c4c534c0bfd99b2472382b368d7fd5c<br>SHA256: 117938f84386f9ca627464e7c42856b6d9ff4f68bbcac12a393b73ea1ac0836f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>243.3MiB (255.2MB) – 2,358,639 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c61e48446e598bab5cfa16234f5f136<br>SHA1: c3373a6fe2e2f8e08a48274939c4b494fb99b5f1<br>SHA256: ff81c189923d299847f5b5e0e5c472fe10d836d11e24fa5379a2def67c998406</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-01-18<br>IPv6: 2024-01-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.626MiB (4.851MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24caac24a9c72bc3caa6451ceab08833<br>SHA1: aa114043e64d74ecd9e8ccd339b80c62d3fcbabb<br>SHA256: 6d48a0384e6e4d38820ac8d2936c12db7eb726dfe20c59600d4f14d173e3b15f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.10MiB (17.93MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fc970b50f7b01de0d0c6bd29224c13<br>SHA1: cb1fe32e67d0561cefef5f2908570ae3af446a24<br>SHA256: e0f36200f10f817a89b6cf80d8d459900c5428a669cc706af32d15b709a8b624</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-01-18<br>IPv6: 2024-01-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4MiB (176.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4104f39d8c379ec8967157286f495717<br>SHA1: 440c75c20491f104948897ce552c95510badba7d<br>SHA256: 6689c6e63153fcbdc00272e2ec6cf04f0c6877860b4a667b3972dfa08c898747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 142dfb0f4dc0ceb4f5a41b018ea53524<br>SHA1: 284b510184f46179e9e34f60dd0db14fc72f3e50<br>SHA256: c57159c9a8879702623a2ef4d0c2fad06d21e96f1836db2d3a09f9216aee1641</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-01-16<br>IPv6: 2024-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.357MiB (9.811MB) – 468,721 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0449670dadd71fd82b637ab0576b53d1<br>SHA1: b88211e72c86e21b6cf90704bb5c876fcd9d3acf<br>SHA256: e8a239b7cc991b35954f7a069ade72d0aa86d8555a1045d3442e76c89f1bdf14</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.25MiB (20.18MB) – 292,501 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b9adcb2f88c07473985869aa8946ba7<br>SHA1: 50b683cb46b306daa8c9fc95f58eb384c25f370a<br>SHA256: c704c89b7325571d96ad60a094e3ee629e68d49f42848394c5b4ffdf167ee287</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-01-16<br>IPv6: 2024-01-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>161.7MiB (169.5MB) – 3,442,944 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7db6a5efc2640ddb07b51dfcac817ea9<br>SHA1: 8ccc351eb39907230418d4fa462fc599bcb45d78<br>SHA256: 8d9edff3856caa64619772a56e328f4af03361e9a3fcc83e1ac4d0420694a0fb</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.4MiB (198.6MB) – 3,442,944 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae536edc1a820199a18eb1d04c815343<br>SHA1: 0a9518f54361d96080f05da17c9ab4a39fa54da9<br>SHA256: 4dcc3624cb24dc4e11480165112222d24fb25007ce85658d9ba05ce5f93901cd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>166.5MiB (174.6MB) – 3,442,944 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fde339da11e42fc0580d812a287477a<br>SHA1: 9fa66cd595bc03a4259bba2bba5686e61bdb7fbb<br>SHA256: 46d5b1a0076298a0f8a473c4f9e08ee568a330277c10752a2ba2cdbe030052c0</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,442,944 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6aadbbbdd613f71c35fb14c6259a6390<br>SHA1: f86b9eceb64b9dd10346eefe926f89d1174b3f8f<br>SHA256: a6e22f43ed1b8358ed1058e563b34d2b8eab719419e9dad747cd0df4161b28b0</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>202.3MiB (212.1MB) – 3,442,944 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9666be2a16cae9102573a944c2388ffd<br>SHA1: b8e5a0b47acf1654a2b48cca43d0fee092629d49<br>SHA256: 9dd71e2974a879bd80e7e7b5a4d008a27dface2ef580ef0ead1ad5540d70d820</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>161.2MiB (169.1MB) – 3,442,944 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83f3be197c2dd4824f84be75dd6bbd26<br>SHA1: 5e0d84c184725c476eeb1268d6a79e06cd26f0d7<br>SHA256: 55ea0c8397e039178fad04ab4e73c28cd1bdf2662d0c9756e336333ce8fbdee6</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>201.8MiB (211.6MB) – 3,442,944 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 500c79109d439d808a212c38451a6ca5<br>SHA1: a1ea31b72b97306830a1233f954da56dccab325c<br>SHA256: 30db5d487b7aec506277afd9ec677fe58b2d2104c01a86d4e443e7fffd7daebe</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.5MiB (178.8MB) – 3,442,944 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb5e4f89f5949a566ecc9ab0e9e60637<br>SHA1: 92b87446564bd18e68b2d20b6b7df71a36562399<br>SHA256: 1b3fba568ebf58f9763b9f8f4a73417df80fcf3e4760809ffa472d1948636a34</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>109.6MiB (114.9MB) – 1,227,792 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19f7c04123aa50e1c05b678c11efb0e6<br>SHA1: 344d91cc728238d00bbd993ad1b8aa4bde75bbf8<br>SHA256: aee77b38a48d71f3dac8dbb19f28443d4386a1e0e15bd54815c91b36d98cab67</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>117.7MiB (123.5MB) – 1,227,792 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ecdc54c900f52c18ad055aa0d0ace9a<br>SHA1: 64e3163da4dcc07925edb8d4c6d67b8105a41642<br>SHA256: 748f6e467d1fd484ae819e1e1b14317701932f3cfc8b930041b4cf869b04162d</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.0MiB (117.5MB) – 1,227,792 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b07e38a9002fec7b86a59794a925a1<br>SHA1: 75b0411f9622c42c63f1d3cd50883e270b178626<br>SHA256: 6bbd4556d13f215414a49801b5399e56d1e0de40dab160248e53ec972f30f7ef</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>113.1MiB (118.6MB) – 1,227,792 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6389866137a75e69491ce19a7c93568c<br>SHA1: 160b9109c5c0d59cf05fcd59b7c9fb984c2cbbc5<br>SHA256: 29ff8582b9a83e20b332d58809121e788ed9c81a19c0cb4bf63433f2e004902a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>121.4MiB (127.3MB) – 1,227,792 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b72abdb42cbe72e9adca0b652f26a66<br>SHA1: 088681078c0bfbda7aae0091d4014b18891fff30<br>SHA256: e551e3ce5616a4868da97fbb02ae2645fc3b4c79e9ccda12b1dbdfa91dba4b99</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>110.8MiB (116.2MB) – 1,227,792 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65f2ba448eef6486510d27c889510214<br>SHA1: 19e39c65431684426f2612427f0eb3e1c382d87e<br>SHA256: 027719db1dcc94c1463c7a8b69a4138e235ddac2a20ffc1347149c35d9f8ec36</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>121.6MiB (127.5MB) – 1,227,792 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f05bc3ba5a877838d4ccadeb1c8b783<br>SHA1: cc4b315e38589c9492c10839ef696d023aa4788f<br>SHA256: 3120a8d2219a15343af54d4691fd41f714cb3a1792b26b0f999df33026d9dacf</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>114.0MiB (119.5MB) – 1,227,792 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b96e08e081a34590396ef1266dc4627<br>SHA1: e7fa0ec64378da6f08e1965c3eff243b1d25093d<br>SHA256: 8304b381490dc018d6e95e1538f51c6be1685f5f52b744be87bad0ea63194c3b</pre></details></small> |


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
