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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-07<br>IPv6: 2025-07-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.314MiB (6.621MB) – 316,197 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48c77fa27efd72d23175cd5e37e1b0e4<br>SHA1: f247c914418771a7780bb9a9d60b3067ad93746d<br>SHA256: 21349d55f35aeefba197aa6a9896353f3eb91901e32bfe40dfd0628cb17e52f3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.26MiB (12.86MB) – 186,370 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 506694a9bea118447dd4c32a492ba6a1<br>SHA1: 6e07edfc5d32188c7284bea45c2c547251321595<br>SHA256: 68fbdfd657c2877f5ba9cec4eb85e062a9691d4ac88eb555d1dc9ae2dd05cff3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.13MiB (12.72MB) – 607,069 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc854e4e4e9f23e69d497dd0d672b541<br>SHA1: 363fb5529dcfd997e12f5b0282f7716168980112<br>SHA256: 5c1a435eb8df375fb5d9c0124d950fc5a8bfbf25e8eb7eb28e3c32b254f9ded1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.89MiB (94.26MB) – 1,366,070 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcffee4e07aba7877fed00fc9d9b21d1<br>SHA1: 08212ccb75ac9b7b5d59a4f88bf2f250217af99f<br>SHA256: 00bcb219501fd35355aa950cd8e8ac38154c40d8c242cf65f764a7b76e580779</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-07<br>IPv6: 2025-07-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.057MiB (5.303MB) – 253,125 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95ffb525ccf7554fce3b883e3c3e03dc<br>SHA1: cfd2058bddb8335014ef0155af9287eb4eb032a5<br>SHA256: 7f2d0669907805f467ba557b3f8a89f0cc365fe47fd8d2d06b459ef043b58cac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.80MiB (22.86MB) – 331,362 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba9c525bb7d6b096e7d2a8892fad8109<br>SHA1: 51c5aa6639dc0b1ba9137e7681566659089d3e9d<br>SHA256: 055c98ab2c55b531af78c6adefcb75267c71f317deda1d0e11cd3a5379f8eb41</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-07<br>IPv6: 2025-07-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.1MiB (174.2MB) – 2,881,364 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 857f03de59f847ebc914de35a0261594<br>SHA1: a8eb10b3a834af6faabde77d1402f59045791a92<br>SHA256: 4de98758f7a7f36de44db1501aae76db758f5a29bc7d70a9c2dad3a025af32df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>269.8MiB (282.9MB) – 2,614,886 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cf5e97154e6ed02edf8b16bd1ea2891<br>SHA1: c33d58815af98fa41a92decd4ae34875ecc10ccb<br>SHA256: 89eb5c59f64873edf5e3369de45be94f934ea8219710777955f08a65ad9b49fa</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-04<br>IPv6: 2025-07-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.50MiB (13.11MB) – 625,654 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3be3d5f57327ad5c44bc24cdbe07954<br>SHA1: 06015643704eecd59066ef0048276bbedc0c6e69<br>SHA256: 13a9cf22f6516b95f5a0df937ad49b0fbfaa1e4243e26f3efa0e128e8b760a44</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.22MiB (45.32MB) – 656,778 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84b906f2ef7bdf5611965c62e3db4841<br>SHA1: ebf6301dc792d1297372614e3f302806fe464c2a<br>SHA256: 23e1ccc1d2d880884aa1949b10f3c8bd0c14c949317327018e85ddcefabc605b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-04<br>IPv6: 2025-07-04 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.1MiB (181.5MB) – 3,417,002 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c8e2c006cbe9621e0ab3a9822083de0<br>SHA1: 84338832065c4e3d57b07ab032927a13067af956<br>SHA256: 968b51ff76e02e3728f49268bb18e9a36d2476fe3cd6b1d052e52a674773d8be</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.9MiB (192.8MB) – 3,417,002 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 704d93c86e1127a7ff9295d2f6394a53<br>SHA1: dc674e55be8a01936d0c31f6d6504d3ac99ea1cc<br>SHA256: a975803cd3629c53bc1110aa1b3003afc7a808a4f29cd622cecc1cbb51cf9cd6</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.3MiB (180.7MB) – 3,417,002 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 162539eef31791cda34ef92a954bbb6c<br>SHA1: 06857457d53e62785c6a05245fa534940a15aa9c<br>SHA256: f73fe5da687d5953b1546bdabad2d9843ee3ab97bf6532daf472ab8d02fe48f5</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>174.8MiB (183.2MB) – 3,417,002 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb57fc2ce1aa9fae117c10bd6737fea9<br>SHA1: 3e566b21c69906aaee4d6aaf843aacd448c8dcd2<br>SHA256: c58a04b6eb3ad3483acf4ad189d69151bcb9959f5cc9a45fb2b33404952530a7</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.2MiB (229.9MB) – 3,417,002 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b3dc8ac64260d61d5213430c90dcbe3<br>SHA1: 3b6f5fe7152d74407dcdf6c99b928d96cd713ec5<br>SHA256: 06d566a35419854877bb12edd8308bc1bcc5fb1a97f249f3ba867941a2cbaf6e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.9MiB (180.2MB) – 3,417,002 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9bdaaa1a5e55a193c37bbbab31aa00c2<br>SHA1: d44dd9e673100a5c85043741a26d9d7e98de897c<br>SHA256: 3fc118cc367d91d924795c2bfe57ed0b329b498b79b5f6a9f43a48dea81a68b5</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.0MiB (223.3MB) – 3,417,002 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39af857c0f8eabcdcac3318655d937c0<br>SHA1: 7befd4b02e899d737b38cdc86ebf3506c6d4741b<br>SHA256: e74b78405eb7cdb5b6292f5d033eb073631102b78d571821acb95a29aa73a790</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.2MiB (187.9MB) – 3,417,002 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99b26f5d7c135f04ec00a2dad97de7e6<br>SHA1: 6d31becac7e56f4b71e3e7e5eac443a1cde444d3<br>SHA256: dc0985bffa9c8b5c033773a5b4a03698e873c8440621a727d4b9d5e89df37d52</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>176.1MiB (184.7MB) – 1,872,248 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0026b7880da7bfe2f8fc782fde561eaf<br>SHA1: 60913d8084f8f0d75e4b1b7ed8a79187f8eacbd0<br>SHA256: a6c2292e4f1346a01dfb873c419a91840f7e3346cc3ab81c542a42abed817d4a</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>180.1MiB (188.8MB) – 1,872,248 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 970a3513ebaf23d719fe2e7d99cf4cc2<br>SHA1: 46d07c1982b46d21f0163c4ea313bd6c04e9ea69<br>SHA256: 39360e5be66057a34b511ee629bf1827ebe377d27e0b0ce37542fe10d3528531</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>174.3MiB (182.7MB) – 1,872,248 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0aa5f37079bb9f20be43d48d12bc01df<br>SHA1: fef5561e2839944b0ad9416537618bfe45847fac<br>SHA256: 97dd646107b4316043a1bceb9126cc8ccf525d928e680d1885e85cf8c34268b9</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>174.5MiB (183.0MB) – 1,872,248 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85bf41a5f317a024d33f42973b78e653<br>SHA1: 318315f955a95beaa7cd741718c72161a2edfbce<br>SHA256: fa020bfa3f454ee352b53b5741574c9e78f82f2deea2d27dda9d1b93a41b2887</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>193.1MiB (202.5MB) – 1,872,248 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 246562aa86be247cfc0596feb25a7700<br>SHA1: f55e43eab7f8d172038d2dc8ffd46e3fc9594af3<br>SHA256: df09c33e0a0add9b81b8b0fca267f6c597b4446efa1ce0f5d80d79e7ec609edb</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>174.1MiB (182.5MB) – 1,872,248 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55b75dee1e9d289216086ef4ec9b43ca<br>SHA1: 41b9b8306e45eb5ace258e5f11489910cafa9c23<br>SHA256: 647ebd2dc836b67b47bb8f55ec83d33d97dfead0f36ae3dd97438ea022d67d35</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>193.9MiB (203.4MB) – 1,872,248 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d01134da41ca562d2ddd820c346a4515<br>SHA1: 1466d94902d77b2b5c7a021fcc8fffb53ca25fc2<br>SHA256: 0bd7bd6e213c89d83c45d1aefb2586273a44728af6c9cca06db7144cb1c19fc7</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>178.2MiB (186.8MB) – 1,872,248 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33c6a6cbce88ba78b98b7caea310c1eb<br>SHA1: 8d45bb062ca51d57ae80010be498ca53418db439<br>SHA256: 6b0cfd90c1875d5f18b6f13206138ce395ce93b159b9113401c814f9e4565c10</pre></details></small> |


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
