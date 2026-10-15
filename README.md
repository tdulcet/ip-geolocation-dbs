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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.639 MiB (5.913 MB) – 282,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a572e956f46c2838a51366575ab656a1<br>SHA1: 1e65a0d22b5d6a23d6de4531180aabd4cdc6a173<br>SHA256: 45b659b1a4743d6062c752a2af57b2da842bfb24ff4245fdce69585538a8fba3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.45 MiB (18.29 MB) – 265,135 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4033749281f7b8490d4f895a83be28dc<br>SHA1: 95c7ba1d0ea56cfd994e0c5c286eb977820eeb6f<br>SHA256: a3b54254fd2f510ec408f41af8e1c61e1edc9ccd0b9750c5987a8c512032800f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-15<br>IPv6: 2026-10-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.162 MiB (9.607 MB) – 458,773 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6b79439644addb83e7dd31ccc690073<br>SHA1: 564332c6f5d82a1eacdd18af3ef36a58d45e7986<br>SHA256: 3a9924f2dd87b1b047a8b63a5aec889f0d82f127ed5d0b27328ef5b20aae106d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.116 MiB (8.510 MB) – 123,452 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19a8fe688e39747d30707d98bb01c795<br>SHA1: a8e5e0199e54c3e3ba54eb50052baa3f57f711ca<br>SHA256: 9b993f3a02bab0c0b615b1910e1577e8a9adb9de9302f654cb028dc6f75882e5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.33 MiB (12.93 MB) – 617,264 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a31dde043483cfc15716bd3c1f1fe6b5<br>SHA1: 65cb94a4cf33283a524e50842ca2b034f02891fa<br>SHA256: e54f8fa4063c66b11018379a95db5b4af5820ab3ababb22aaf288c89ed033adf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>76.71 MiB (80.43 MB) – 1,165,712 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01d3746f507752c0aa1c62d851c57b05<br>SHA1: 66d3e13b078bd1784dfb5daf13a2131240e4e64e<br>SHA256: eacc38dd103d0e5ccd943c3af3ed1209edf86e8c07cad3278b2368b2a4a020fc</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.818 MiB (6.101 MB) – 291,264 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eac94e3e3ab719ab78593afa964f45da<br>SHA1: af19435e4e57c25937afe53d6fba292805882dbe<br>SHA256: 9f6a222c0122eb47e34ee42c495df4f17830c0ee40f4a9921b8535690d3270fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.44 MiB (24.57 MB) – 356,148 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ce580593be34cc4df87bfe5bc81e9b4<br>SHA1: 7a4ab5ae6144faf1b72fae6b2c3be92bb30697c0<br>SHA256: adebdde6726b52568b80d2b7d08b6598f6ecc66c089d6ef69e629573f008cb40</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.7 MiB (179.0 MB) – 2,951,725 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68b1b79e84df6b26076250d820ea0b18<br>SHA1: dda1c9fc8b5b7c2a62cf7a72bf999fc82e55255b<br>SHA256: e664ee3e96917e7ba878660728524375c22f39e4e3aee5f4eda024aeac6910dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,535 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fa4ebcfb46463ed745e92304c503838<br>SHA1: df8c366979b5a5c5a906cf825f26a8437c8d2081<br>SHA256: d04f2b9be41819f8c7cc2d6f4075f927287880b221d8d14a85195ba76acecbb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-13<br>IPv6: 2026-10-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.26 MiB (11.81 MB) – 564,026 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c6c1d887afed0ed306e3cd511294828<br>SHA1: 74277c7d2626170f41c0b6fee705d92d526aa66f<br>SHA256: c691ff13723d0e283e2e2f8b58401f890e1278e65ae5ac6addae83d27ed2733d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.96 MiB (34.56 MB) – 500,823 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8ec1babb0bf51bc151b92a07570b65e<br>SHA1: 2e90cf412808c735c0617dddf6a0590b944db794<br>SHA256: 0d2ff39882e30ec6bedba0daa257072f5d893151b1ca7029c83c75b1c11d15a1</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-13<br>IPv6: 2026-10-13 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>188.5 MiB (197.7 MB) – 3,674,871 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f114798ea6ceceb830b3896f7853b8a<br>SHA1: 0ecac5ef80e6cbc84aae2345f0a7735bc0272375<br>SHA256: dc7350206f2acc6722af1c71f3d05b525023411e2238f900447a7148bf66c25d</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>197.2 MiB (206.8 MB) – 3,674,871 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 941e7a61e10e58f006bca1dbddf6e156<br>SHA1: 0af753d7f67dcc8d1d9219ddcc31ec429f961f28<br>SHA256: dc6c453bc14de22e095655e3c8acb1257bfab1d5cea529e9bf1e9467cfdcdc65</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>187.5 MiB (196.6 MB) – 3,674,871 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cffc7de4964917b8632370ddb51b123<br>SHA1: c21f4abf8d5314f5dd91f759e67c945d7bcc2a56<br>SHA256: 9e43debea8eca1b6ae6da3f85ffb439e44caa7ab97dde79eecd641720234f149</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>189.1 MiB (198.3 MB) – 3,674,871 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba67bad39b50449e9c9539196db14a5b<br>SHA1: d583aed45ccb5a313a7e47f0f714edf513bc48a0<br>SHA256: a7c30b94de7df8448197cae1d9576cca94ec019c3e07fedeb8bb810a8f6479cf</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>238.3 MiB (249.9 MB) – 3,674,871 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 256b0e9a4552afb341fd30357043ba10<br>SHA1: 7362506d808497643b87ee9045db985a1f6ae060<br>SHA256: f245ecdf9e2c06a7304c9abe74bda0b168c1aa10eac7fc31d06c6dd8acf7064b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>187.0 MiB (196.1 MB) – 3,674,871 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aecbb4c2f932cc93792a644b6f9a0b3d<br>SHA1: 24dc5fc6cdae346ab761cd5677e8f391fb8b5f0a<br>SHA256: dec3df3aa10377416fcb5b5fbf4f8dec0a6e815845b6bec4aa97837db4bdb49d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>236.0 MiB (247.4 MB) – 3,674,871 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 265d2cf0504014f26807815980dc1920<br>SHA1: a1432033d2ef663c0a41e1c3753131219ef4f661<br>SHA256: 3dbf6fdb44316e3dc30d675e3f06a414743b9e8d4b79cbe166f3f736c45b90d3</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>192.7 MiB (202.1 MB) – 3,674,871 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22fc4e034815fa24a0645ae662e60792<br>SHA1: f7d04769143bdef7983f52c68f3338192c459eb8<br>SHA256: 5a4744bdf3510098e2158833bceb08b9996c3db4f42bfb2470091bb3fdea3b95</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.5 MiB (209.2 MB) – 2,089,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 12295a677b191c66b67b9c1e23501aaa<br>SHA1: c66ce422c98a142aaae0acb263bc4ce3740555dc<br>SHA256: b631e9841a8ef684bda24bcf62d97bb925b5fe73d8249a834d989ee532c80468</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.8 MiB (212.6 MB) – 2,089,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f013dc91a65652327078ed466d02300<br>SHA1: 72c837c3d9331b2d64e5baa63e5db20328486d49<br>SHA256: 564bac201b49f3d567d900633951a4d546391bfc0cf5ab43a780be1819dbb51f</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.8 MiB (206.4 MB) – 2,089,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: deb01dd1c92bdac8ad9f8c6f4eba500b<br>SHA1: 72b1dddf2c78dd4b4d95176c8a6ae618bc8c0f5e<br>SHA256: 50537fb7cac9c81b57f0d88fc2b3967484746e62abfe9d8b0c6f919af9ab3f7a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.3 MiB (206.9 MB) – 2,089,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b42286856325465855d95ee766cbee4c<br>SHA1: f3d97fa6042bae6306b1260a148f0a07de0d81d5<br>SHA256: e763f800f9209c5b0710c563f1670d9764e70a75ee825f86eebe3d8fe54a8cbb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.5 MiB (230.2 MB) – 2,089,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a5a59d67fee1caf31fe31e08c52b076<br>SHA1: b2dda89ed237cf5777df7beb1147c8160b439c31<br>SHA256: 727e88ad9df76bf4c62817a1482d40b9d0b5ec3501b80cbd624cc40eeafa194e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.8 MiB (206.4 MB) – 2,089,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d23d117aced2840b81dd6b2a406e922<br>SHA1: fe1c6d0dd0dbe727ca1b498fcdb24c19e2482734<br>SHA256: e937b5308f626005c510c8cb48eabbb78b8eb9f61f4ac3f7b999c84c1f728002</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.9 MiB (232.7 MB) – 2,089,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb74f0671e098c0fb0146f4097127445<br>SHA1: aa54cfeea9f7e051bcbe0b7067e8fef215cf7987<br>SHA256: eb23e8b6f1d3772bbee2e0f2deb82d49bc87e16823b9ef230ca7577e5a74cd83</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.8 MiB (209.6 MB) – 2,089,686 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed4bbd813033e680674379a088a30c0f<br>SHA1: 3c535c2c58c2eb835d96c59eea03f0bb064b9e76<br>SHA256: 6fa17b2dd801ac4cea6045f2341c51576d83c9cdd85034304d07db0e89c38624</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
