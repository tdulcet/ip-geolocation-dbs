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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-06-24<br>IPv6: 2026-06-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.379 MiB (5.640 MB) – 269,186 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 422e44a2fd70608031682ef2e8e4fa63<br>SHA1: 6b056a96748aca826b82e126a74b182d0527450b<br>SHA256: e330d92622cb1b068efd3c6008b7e27e85d01ce5dcc0122ed806f5f87c64c59a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.66 MiB (17.47 MB) – 253,153 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79d7133f9452ebe727f117ace0dee798<br>SHA1: 61ac643e5a84648bc2d432fd07072b50bb1d055a<br>SHA256: 1f57668beed94c9809e6b5879211badd9cf18b28b68a62b90954453f9047bb7b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-06-25<br>IPv6: 2026-06-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.989 MiB (9.425 MB) – 450,070 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7666e802b1e2a2c8a038de3cbaa56bd9<br>SHA1: 58100fdfef240479f634d58e413bbbb159e004ac<br>SHA256: a63211aa002a4c8ec7b273bcc21672d68936d77bd019854919866a1cb59b1c1e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.868 MiB (8.250 MB) – 119,679 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5668372d0b1f6e677a077e456d02a3e1<br>SHA1: 2b99cc3a27add7b63df424cb1719a465a08dede4<br>SHA256: 127f9cc9a2b32bc5005d2b3d908363428ce0d0415f49bf46bfed19e22b1e86f4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-06-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.31 MiB (12.91 MB) – 616,446 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a1b2090ff12d5a0a5b1b88ab9f7372f<br>SHA1: 2639f162ac2256cda29cb9beaeb055e6d606fb0a<br>SHA256: e887368f4ed8547c93a5c28a2c8fe7389205d737ed481043f4731952883210f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>42.09 MiB (44.13 MB) – 639,636 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6cca847913b591b8559c581356e3f48<br>SHA1: 34fd462bef1b55e01a1e316b4cbc878236868a99<br>SHA256: 67d9b886dce51a7b0a62915cd0cbc36cbacc525a9df7f274b8e15fefdf992036</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.102 MiB (7.447 MB) – 355,800 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9779b594fc4d7c5fedd39074456964b0<br>SHA1: f1857d5d01ebf3fffd9827c74bc65345e8916bf3<br>SHA256: e5a4bdfa0635b5b15ba6de9b49d90e62fdc6d79622966eb6537f28dac53b051c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.76 MiB (23.87 MB) – 345,871 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 497c17574013e7a97b85c3096a788e65<br>SHA1: ce6db4fa8555a208ce550a745e54626c76a15fe4<br>SHA256: d54904ffc2bbe63f286e6ab4f05a06d3b13ca72a6eaacc9fc485461fb377cd7e</pre></details></small> |
| | | Full Location | Monthly<br>2026-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.9 MiB (220.1 MB) – 3,678,369 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4771d4369237ec9c638b9e8d923d601f<br>SHA1: 78f138eefe0b10273a8276b9f040541938bdea50<br>SHA256: 7ec412bdf605a24ab29a226dda6484d376455e55822c57e601ff87151af7af62</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.1 MiB (473.0 MB) – 4,394,152 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8837bf0f7e2750e7ba4668512a3d7db<br>SHA1: d4dd5a772d18e489ebc3f56bb07f38de2356a4d1<br>SHA256: e5a86e86fbf963ded29ad111b47f71ebb826213e62860792a6eefd696415ae18</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-06-14<br>IPv6: 2026-06-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.523 MiB (5.791 MB) – 276,445 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbbd1728d91c2745210523a6529fdc9a<br>SHA1: 428e628787b425155adbfbda44a3c9411948ff05<br>SHA256: c4d05bb79508d6b8868e55e4dc13787882c726e9f81fc664788da2a2c54284e1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.01 MiB (23.08 MB) – 334,542 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3be936503a0ec98674cc818ddc466d88<br>SHA1: afb165445966f5013414caadd96e12242e208087<br>SHA256: 2bae14aa887830b648b4459a61049b1827d63d888be282525131d2b2ceae63d5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-06-14<br>IPv6: 2026-06-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.9 MiB (175.0 MB) – 2,888,841 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a54972a25283423152f1f5299bac8bd0<br>SHA1: 29508df74e7357541d9e0b46c0d0d9d4505b128e<br>SHA256: fbe8a8513442902221aefb078c32661bf1902a31fcce1dfa4590453640b602a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.0 MiB (307.3 MB) – 2,839,959 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5361417d086b848e71911e01cd058944<br>SHA1: e777a708d40fce9b09bdb1567f279dc2ffee2115<br>SHA256: 3aad3927d0c56daa68cdd500e638d15cd6f73a8eed65b8919b663ed157a67a4d</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-06-23<br>IPv6: 2026-06-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.64 MiB (12.21 MB) – 582,958 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5117504d634680a6f6f716b8ed65e6ed<br>SHA1: a24f35468621a06e04e6cc9ddd3e9058c68729c4<br>SHA256: 486a87fa6bd8aecafed1de4c85e7a18cae44480a334dd3a02e29bda2de27cba1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>38.25 MiB (40.11 MB) – 581,285 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5de468e16b560513197ac70502348de6<br>SHA1: 18e01074d98364465d3d0167c0470b1074494846<br>SHA256: 874f2c08c0fcd69f1b1bf52f6558cd644ec0c2f2307ca879711b097ff4a5c4bc</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-06-23<br>IPv6: 2026-06-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>193.7 MiB (203.1 MB) – 3,776,018 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9184b34b625ed01f26dfdcae8a640715<br>SHA1: 26c9364e7d36d3bbfd4e71fc7e1ee39cd3197d4f<br>SHA256: e652d94c59820800dfba7f4b3402f4587009e61cb7cfecaba5ea1ffff797cc24</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>203.1 MiB (212.9 MB) – 3,776,018 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43077a43442c5f922bdd70fd9a917507<br>SHA1: 7c8928491b8a696a8922bd5ef9ee4fd229d5f020<br>SHA256: 3068a6a03bde0da3d6415078d5018ca50da5453cef56375b2a7fcf0ffe65ace3</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>193.0 MiB (202.3 MB) – 3,776,018 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89ed5498f811bd6885a715f692a10316<br>SHA1: fefeaf9c6f5a9186972020a277c0a05aaea8340e<br>SHA256: 241fcf604127ed36b4d357a998c758a6a5ca0545a5b1be57dae5939bd3f39cc9</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>194.7 MiB (204.1 MB) – 3,776,018 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28d0b3edcc8f18c0b2576eb613466362<br>SHA1: 9a2afb28b2d5ebbbc8783e72f7f2a0740fc6c680<br>SHA256: 5cec01043f270223ddf3968f9199d392ae1d08bbb72fb777600508e26e042879</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>245.6 MiB (257.5 MB) – 3,776,018 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3570c57c37e37f5095e9b72d8f5e742f<br>SHA1: feebfc864c5aa1352863def9db03a792f1d7f4e7<br>SHA256: 06d53492b37cfc89eb2b5988b99221870705ab15070917ae113d1effa54f6741</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>192.2 MiB (201.6 MB) – 3,776,018 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1286783fbc490d211bd3e24cf552a25b<br>SHA1: 00db88d0726afc2260c4d50e7f6c7ce78cedc28a<br>SHA256: 073185853ba6e96e4cd52b7f0b0fa0095dd9e1dd41f79bd85cb80c47c75e9a67</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.6 MiB (247.1 MB) – 3,776,018 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08f70dab8de48993e820d3a111101ebe<br>SHA1: 1d0125f384d3eab453c72371c6d930cc049dd333<br>SHA256: 544134b55091f965a518ae670b6528543477df977d94c618ade7184002c1cb48</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>198.1 MiB (207.8 MB) – 3,776,018 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f202e540fecee800648bc612f6401d20<br>SHA1: fe3c3898eefa5aac439e7d2603ce33d896ea42d4<br>SHA256: 25e4b4d294197a80fa5f0d255c007d1dcfecbb0b4eeafe04bee5fecc11fd0a1f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>198.9 MiB (208.5 MB) – 2,087,181 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d25af9ef72c82a316b0f504501a1b00<br>SHA1: 446921710fff0af6678e0b5a1f70f99ddeb43b5e<br>SHA256: 8cb94480f56958ac9604b9ab8d65effad22985cd9ee8a0c9bb03143cda75cc39</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.5 MiB (212.3 MB) – 2,087,181 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96f79cd7569959d470daaf3e80107c53<br>SHA1: 244eb4cdfc23e53be4b835b39ec03ff0d1fe6545<br>SHA256: 447466718a5e8981e5a353d193689a634ce55a4d68a8852b4de8a79f9fe788c0</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.6 MiB (206.2 MB) – 2,087,181 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4c0002c47e05f204da1cab6e12e739e<br>SHA1: 0b439e5a8e27b6c7fc4f6fb73836e2a67d6a97fc<br>SHA256: 77882ba095b5c18c86e3a57104ef5037a323d59f33bbbea525904bfb91ebc0e5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>197.1 MiB (206.7 MB) – 2,087,181 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 582cf135a1a2a559b345358f2579b523<br>SHA1: c2092b2856cd53e99b24da104106a86326391ae8<br>SHA256: 50c98c4c1d30523a31a6131bb63adbede82c18738fa2d4aba3c6e7f9480daa5d</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.5 MiB (230.1 MB) – 2,087,181 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed110f4efa80c80bb4bf1333dfd28ee1<br>SHA1: 59292f6d78a9d23078f5f181b56c6f30b84d6eee<br>SHA256: d048e7485fb4e4e20a29e9472697daf63cbe886e4c231f497bb01aae5b5d2908</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.7 MiB (206.2 MB) – 2,087,181 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efec3ccecf1d4a0acf44bb761f360202<br>SHA1: 653ed5b5acf5b4af2a7b928949c1788a49b4eb8f<br>SHA256: f98e264f1b3397ec2a4209ffe9cf8a66c21190837d7b1d53ce11686c4b667d70</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>217.8 MiB (228.4 MB) – 2,087,181 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9517ae6b5bcaacb6b79be6a59f5e645e<br>SHA1: f4654a8fa55040e6478f557f852b26a5c18ad65b<br>SHA256: 52930e9bc0674f5d62761181d6cedd99b44a3f7c97b09b4f6b948be862f53e96</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.3 MiB (208.9 MB) – 2,087,181 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50ca693886d20b5879e444e2708d0065<br>SHA1: 0122cf3363032fb054e3b7106aa7719329bc0175<br>SHA256: 563510bd1e3d2d0237a09424cfebd8837e468f1ca8b76c546cec07f8c474c3ff</pre></details></small> |


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
