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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.251MiB (6.555MB) – 313,019 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ae724184614610f00d649089c181b95<br>SHA1: 5fbf89d6add0fcc6c22d3ce6e89be4d039c63282<br>SHA256: c08a65dc69c14ee5b8d5baf3954a80e44f319576cd3b49eef2c43dcd2901c52c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.85MiB (11.38MB) – 164,953 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21cd5d427a1ab91ab74899574e936023<br>SHA1: f06809b266f3460486ee839870a2bb178061a294<br>SHA256: dd91fc0703a268531cf747a4ecd8a5d2cb1e12c45d30939af5104940a08041f6</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.636MiB (9.055MB) – 432,415 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ef22bead8bdf654eebcb0c5a12311a5<br>SHA1: 4d3da5b5617ded9c23c40050e0f6c2140bbce32d<br>SHA256: 09fb7e5bc86df7a83bca3bc331c36428ad17d4c9aa704b3d7a6ae412ece4909b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.245MiB (7.597MB) – 110,215 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a1db80b53dc71b19fb665c61a41c5b3<br>SHA1: 0fde2c92ad8f6c3ea63134bc5fe440b268558e9f<br>SHA256: 4f1b90234fe3cace59f8e3bf9a3db0b2a76291efb50d965e5125b7ced15f607a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.15MiB (12.74MB) – 608,045 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 097a7f416b260b3730f18f77fe57ac3d<br>SHA1: 7de768c83089909f15f67f9490d38f863a42ce63<br>SHA256: f6145c109a297c3bcff05d979bfe71ffab34f792327362cf4e226d78eb4e0aff</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>86.12MiB (90.30MB) – 1,308,679 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0883c2297dfbbe5440eed68c49594ae<br>SHA1: 187456d8ce0adf4d913b5bd6d1b1a41f0a0f1571<br>SHA256: 047685af9954ff0f0176fd97cde1846018c96b34070294b0b8fb82c6d2325c22</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.825MiB (7.157MB) – 341,824 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dae1f431e9d10a462dae84888365884<br>SHA1: c0cc78c9aa347b8d712850c57537fc0dc50f1dfd<br>SHA256: 3f57c286e145770c2ac0d5d3c14088a919db312a222bfef2cb85941399367b2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.93MB) – 245,375 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f7e3a8bff7f09ee7cfd621ef044564b<br>SHA1: feacd88a985ae6ef5d668ffcf375eefeed7948b4<br>SHA256: f554d05a841ea0162859a713eecebb3fb0dc814ea2d39b91150dd45627c31fed</pre></details></small> |
| | | Full Location | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (217.0MB) – 3,624,799 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7154efa553f5c77576cadbc5c42ec9c<br>SHA1: b63ba0a183e94bf6cd1aa8a15db942b52d55841e<br>SHA256: 00286d8f1fc1f8f801a25f123213615fc637aa494c49fb2537047bdab4b1aaed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>448.8MiB (470.6MB) – 4,362,462 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7375867bcf97ba785ec1fa3d092fb0ae<br>SHA1: 37a209470da0930c2308178d77c0c1cac376d849<br>SHA256: df10547da1aed72a27d58d5fbd860b66dc9bfc40df34c5dcca2b7da7fdf24ca0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-31<br>IPv6: 2025-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.161MiB (5.411MB) – 258,293 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95e8b98e399c9546eaa6913fe2309444<br>SHA1: 0729ec1700dd66e64d570295b605e265006a8972<br>SHA256: 7d5dd78fa0ac37316f479796659a319cb718b97cbcb6c276973e7a032a890aef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.45MiB (23.54MB) – 341,108 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ad0b9a6c005823c4054d4b7a7068006<br>SHA1: d04e0abccf0a13ec34ae27abfb08f929300b492f<br>SHA256: efdc13094674341ad2839eabd8b24cf19df12257e0c4a225196d48da8fbdf5e5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-31<br>IPv6: 2025-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.3MiB (177.5MB) – 2,934,344 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a60715c570305e0c75fe4faffb43ea0e<br>SHA1: 38b00b51abf99d675c6f578f3ddc6f1291989577<br>SHA256: 7b15658d15a2ea684f5136cc6b604a1305ba55f348332e98ac74007149eed726</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.0MiB (302.0MB) – 2,790,254 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ada012e83fb4d38f27d1fccd53c7b18<br>SHA1: da0592788b35abae1df0d9ced713b009ce8207e4<br>SHA256: 3a2da4e80c031ab64e77dcf65f18ecdb563e48d709a708d499e3751fd70be31e</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-09-12<br>IPv6: 2025-09-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.57MiB (13.18MB) – 629,147 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cda9d59cc7cbb8471ed6e9e972dd3abb<br>SHA1: 48aa9971e0b224b100d035465cbc81e8c2377e42<br>SHA256: 2aa715fb73bbd7970ce29ee2e695fef118e891f66cb1c5baab5d69fb6efbc99c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.16MiB (45.25MB) – 655,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41f2395f4b340f154c37a063305889ba<br>SHA1: 373f1a2490a8d73b24411065a596333b8c58e450<br>SHA256: e2a4c0471e61252e519520ebcbd3f4da07434accfeea975e601c22a7a7fa0e20</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-09-12<br>IPv6: 2025-09-12 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>175.4MiB (183.9MB) – 3,454,634 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a510ae4ee2d31145912cbdddbe17ed26<br>SHA1: 8e825f656997b1707d0e016c32f5a8c71a1ba92c<br>SHA256: dca550c8d45c3ba44a06eb874eb3d864dc9295b58023e9642fe0b2eb463f3946</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>186.3MiB (195.3MB) – 3,454,634 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b70a79f1d600b34553ae80721a57234<br>SHA1: 16d6cc2fa85ed899724bfc144c88497cb5780226<br>SHA256: 6e9588d539e9d11d75d66697fabbb03f39c2b6002a7214fac651b434c432fea7</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>174.4MiB (182.8MB) – 3,454,634 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1c2efe3082ab84d2ede327d4065cc75<br>SHA1: 9a310fefd8e58ac93e52ef9b7e56f75707d8da56<br>SHA256: b462297b0875dbe10abd5ce0894132a6cdbad539c55dd8b725d535f377562edf</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,454,634 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f36ce2dcd24a51e089ae1c51d8a0dfdc<br>SHA1: a245aeba84fbeece55dbaf13907938c1d0325644<br>SHA256: 171a9c740acefff8a9d4d8a274bb8f43522362685f4cd4ee499012a029b72c03</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>222.2MiB (233.0MB) – 3,454,634 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f53a40357ed4057069d139f54c5f27be<br>SHA1: 8d39f2c23dd2b793cb5589de6f7a03e8ee9a9217<br>SHA256: 0177f7054908de16dfdbee624d8804c6bcfba70f1c236318e0e7ee0934a5c4ea</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>174.0MiB (182.5MB) – 3,454,634 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4192b92cc3c517ee4b38253ba109a92f<br>SHA1: de011005f018c5f6bca1a964e83a0813b593b767<br>SHA256: c571ccf2a1ea3e727ad73c0ecb0a5f764c48b17c3a3846f857aca4d7d5a5ef01</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>215.8MiB (226.3MB) – 3,454,634 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca34f3ffea5cf65bcf1e1ffe094be89f<br>SHA1: 588e0b8e6293ad7c874affad694271021d894477<br>SHA256: 251de3c448ee07125e75596514e70d04a6fe118279d07a6cc1900dcf1871d983</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>181.3MiB (190.1MB) – 3,454,634 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e87ae58f6abb7094283ee4097353d4e5<br>SHA1: bd61646e73c8344706f68ba08c87bde6af2f6114<br>SHA256: e4e2d0288cd950a4c52ef17f99d2c06b809d0893571312d6400d91854e83a15e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>177.5MiB (186.2MB) – 1,882,813 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82d72f42da1d49250c6823bc28ad8f05<br>SHA1: b0155c6d119f1e233d1b80c7685b8339cb3070d7<br>SHA256: 166791ec9fe5daf9c3362f0c918f213384c73d47705d85650df94805afde65ed</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>181.7MiB (190.5MB) – 1,882,813 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57e687327e85adb94339a7eb749fb79e<br>SHA1: a563a8f9a12e1a3e4382fcbd8aa8d75a4086d59d<br>SHA256: fb99555379cc741da483887c71d3599c7cf911f57eeda5cc976eae5573b51aa6</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>175.6MiB (184.1MB) – 1,882,813 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46be44bac0390e0e0c018da12c496759<br>SHA1: f5db83b7d38ae52e9139e1b8d3b962dfc3d3d379<br>SHA256: ee70102e3d2ef62e3dcb6665337e587399d3ec9f6fdf6c18e012bb515f900eae</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>175.9MiB (184.5MB) – 1,882,813 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce4958ab1f0b4bdc6ce9d9fc68a4049d<br>SHA1: cd54c6b0961fd42b401b3148e7bb0eb98a6d94d8<br>SHA256: 4c23f807a8f10f8d0321e4b6d7285f3eeb2af153579cee0e9ed5ae34b1e5bb51</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.0MiB (204.4MB) – 1,882,813 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39fc18eedb87f90368856184941d2c50<br>SHA1: 56628d25f3acbb80fa374cf15dca536301e05a66<br>SHA256: 0a2f76e27e74b6a12d158f8455bf8e5544e4d1c0f46fd112968c3d60432e3fe5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>175.4MiB (183.9MB) – 1,882,813 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fac8dab667ddb18416ee418a352d7b5a<br>SHA1: cdff5ab2cdb4ab006aed685fb412aa2f292d6206<br>SHA256: 5f8bcbc97e21f6a3f6a280689b8da602e333dccd55f61d484552cfe3c1c94990</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>195.7MiB (205.2MB) – 1,882,813 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56bb6bfc971518ff35f879bb45eba311<br>SHA1: 7df6f29e67662372472f76e2d820ed2b98a30399<br>SHA256: 422bd4f58c677ea760fa49be08020dc242afa6be1ddd097ee7c531a600675f86</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>179.5MiB (188.3MB) – 1,882,813 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5f8e2c27cedb04d2d15941711ebd648<br>SHA1: d2ea6b5fc6716d5177c4dfddef13570c2becd0f3<br>SHA256: 40613608a3276e6c53e9a7b8e6e545edc746ab47677a165d9312cb2b94f66888</pre></details></small> |


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
