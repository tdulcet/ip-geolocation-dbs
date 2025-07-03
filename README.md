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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-03<br>IPv6: 2025-07-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.225MiB (6.528MB) – 311,765 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae6036ddcc9ba247b1628f3ee3cb77cb<br>SHA1: f30e8fb7af8b23109f28050aa4548f9cdb0fada6<br>SHA256: 18f783953367524d65a12de57fae23822d81e44f5e4baca44a97c51a9b431350</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.48MiB (13.08MB) – 189,584 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b7938f7ad1c2b61b1f8ba4593ea1cdb<br>SHA1: 02c2399a3ceecc202b74300a5d0210b130f6b939<br>SHA256: 9359c939fc1b90a0f6085b5a2b710ec6711989dc47a31c117199f158f8cf4bd1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.28MiB (12.87MB) – 614,619 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30b4bb04fd684ec3aefb31d3f58db500<br>SHA1: 7de3ed5a132c9c5d4d2b9802945ef7f300552f97<br>SHA256: b5a32909f9466e7ee03c47e9d19c277c795a90fc0b9ade667b01f68688fd46c0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.76MiB (94.12MB) – 1,364,094 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55711dce4c17c959adb038adac37b13f<br>SHA1: f0b035f66f91aac4b44fe8d8717fedb34caf5b25<br>SHA256: 262de65bb4ea48c41c18432cd60232a5d2114f5709b8f95e9862eea781611740</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-03<br>IPv6: 2025-07-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.057MiB (5.303MB) – 253,125 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95ffb525ccf7554fce3b883e3c3e03dc<br>SHA1: cfd2058bddb8335014ef0155af9287eb4eb032a5<br>SHA256: 7f2d0669907805f467ba557b3f8a89f0cc365fe47fd8d2d06b459ef043b58cac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.80MiB (22.86MB) – 331,362 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba9c525bb7d6b096e7d2a8892fad8109<br>SHA1: 51c5aa6639dc0b1ba9137e7681566659089d3e9d<br>SHA256: 055c98ab2c55b531af78c6adefcb75267c71f317deda1d0e11cd3a5379f8eb41</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-03<br>IPv6: 2025-07-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.1MiB (174.2MB) – 2,881,364 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 857f03de59f847ebc914de35a0261594<br>SHA1: a8eb10b3a834af6faabde77d1402f59045791a92<br>SHA256: 4de98758f7a7f36de44db1501aae76db758f5a29bc7d70a9c2dad3a025af32df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>269.8MiB (282.9MB) – 2,614,886 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cf5e97154e6ed02edf8b16bd1ea2891<br>SHA1: c33d58815af98fa41a92decd4ae34875ecc10ccb<br>SHA256: 89eb5c59f64873edf5e3369de45be94f934ea8219710777955f08a65ad9b49fa</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-01<br>IPv6: 2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.46MiB (13.06MB) – 623,624 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 565987db4e36cefc662f352a891f2b04<br>SHA1: 500e5f906db1518e6bfad1108df7485f3ab85c0e<br>SHA256: f8701ad4983c053616f733f891f7e3ba11851ad3f8fb7a8f7ed83553c24cb9e6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.54MiB (44.61MB) – 646,459 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c22d1aed8f8497ba8c293e31cd4f7ec0<br>SHA1: fbfd822ef5e680d27cd8f32bc94b32c382131f51<br>SHA256: 54ad29d0f9649c9aa0a6754209371ba2e26bf3dde7577cc2a3ac0d718ebf238c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-01<br>IPv6: 2025-07-01 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,413,977 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5cb0b0fcb1bf5bc41336e6762d4d7f6d<br>SHA1: 040a34364c989d903a5885a09bdc830bbdc83c61<br>SHA256: 9fba5b71456cde682c09fcd88df75c33fef0168878eb410a42ef62236f7d9381</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.7MiB (192.7MB) – 3,413,977 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04878c211fb604da82ae45ca6262cd27<br>SHA1: b27a2b128f821e34bf58ef912168ea9680082e72<br>SHA256: 51b88103d10df5017942b297a596843a668dbcd1da7de304b2f58caa70d99e07</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.1MiB (180.5MB) – 3,413,977 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0261f86876cf00334978640b0ee56e30<br>SHA1: b0e9d19a288aa5d8c8a790923b8770a00a075925<br>SHA256: 4a645f71671a419820d9e0875263ca285d40c71afb1a42c76353fea6a99c81ac</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>174.6MiB (183.1MB) – 3,413,977 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d99f497223bca9dbcc3b04ee6da21f6e<br>SHA1: 12a0adfb766c9c9190dfbfa25ce61b220d9a9a92<br>SHA256: 336dbd40d0b6a87f430dfc004a89c8ddcbe69fa22caf4c11c8adfe10b149f73f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.0MiB (229.7MB) – 3,413,977 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad0584938dc1e1fa07ca8ce9b0a48399<br>SHA1: 0ece1bc42119a6df2fcd6cb48e65cc38c8c39ceb<br>SHA256: b788bcddb9274cace8a702600a13838366b94bb9157d3df6be31f0d3e7bc21bb</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.7MiB (180.1MB) – 3,413,977 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a16895b74d469809d6fc187f693b64d3<br>SHA1: d95985d7d7a36b37ffadd120a33c71bb5df2c743<br>SHA256: 7978b0d71e4886321258c28b5f7be0e3df336d21fc66557cef80ccd01698df1e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>212.8MiB (223.1MB) – 3,413,977 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e1b3a5fd24012342181abdbd369a0ae<br>SHA1: 032cbf963e7bfbf1574c97c44197e46b7a71ae1d<br>SHA256: 4d1455b2cec1ad4cd669bcb8c4ee8cbd6c3e050d57e98f6afc29df4f1c739430</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,413,977 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b81a3636e01b80801cb16251a1feb10<br>SHA1: 6e615dced61ae597d105dc7a4da3dc44d03592cc<br>SHA256: b03a77d02f0bd8ca8e6963dacbe00fc15d327ea653db2eac41128ec01755e23d</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>174.1MiB (182.6MB) – 1,853,591 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c6aa16018fbc4bf3a6487841f42d057<br>SHA1: 666c6f47f74fb48b610990e8c49a32628afbaaeb<br>SHA256: 990f4bf76839d0bb76719a68da182be0103a7b5970a3c14f667bb4f257e4834e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>178.1MiB (186.8MB) – 1,853,591 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf9f2d603c6e373f4a709d78396fdc5<br>SHA1: 63129f1a82ee3e4541ca2e9c3f02fc432c80be19<br>SHA256: c4ef323b61c6cc0e9be8cc113dbf367e13e4dc5b609f776ef82f3d1922480a0f</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>172.5MiB (180.8MB) – 1,853,591 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96d82e2b56366ab4e143f65e6e6035b0<br>SHA1: 89b093b0c4689d9ce3ff60cb8dac480572ba7823<br>SHA256: 8a45b22e2bde63bf1472fe8d723b8c5b0686090e1fd184e834d2684a7cfd4867</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>172.7MiB (181.1MB) – 1,853,591 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6af70a40dc06592ad2f31b65e9f2c6a<br>SHA1: c2f2f63580a431501de55aed20f8e3ac778cd6d8<br>SHA256: 37a56f6869c4f64a90280a92a9c7a81356f04fe088d0a6302d2d912da664da92</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>191.0MiB (200.3MB) – 1,853,591 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3545bc992d0da102434eef9be39c1499<br>SHA1: 46acd9a6f5e76bcb5130570a1e62e16d90fa887f<br>SHA256: 46e61af70ea986ddfb6b91a7e7bb7f468dca1e398c99904b51814563ff7bc26e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>172.2MiB (180.6MB) – 1,853,591 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 670f436dddf8d6a268ca447dc16b4027<br>SHA1: e54861feb63fc8b16c940697ec57124d9bc550e6<br>SHA256: 6474f5a3416078d5878b6cb6cd4db9f61970572b85a1d043d54bb8154d0a0084</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>191.6MiB (200.9MB) – 1,853,591 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc3d1a2edd0d7fd93a192e83fa07dc96<br>SHA1: d1f2f59bee45e88f3666453a44c61c2106126fe9<br>SHA256: 781a36b59042592205033eb876bb0b4b1fba2785a53847376d8b3dbc0b42bb9b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>176.2MiB (184.7MB) – 1,853,591 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64f5bf6273857f19b1f16d3995ddefb5<br>SHA1: 0d32557d7dae7bf23b3220de41c2e00813597d91<br>SHA256: 65e159e442e5e9d5b4c59a2eb767d83b1cd1c3be31d6d0187c11e8dab6732c9a</pre></details></small> |


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
