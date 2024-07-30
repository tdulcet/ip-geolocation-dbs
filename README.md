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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-07-30<br>IPv6: 2024-07-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.754MiB (4.985MB) – 238,001 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de718336c1f2f0fb90a140913acbec21<br>SHA1: 28460f17d8f2831df339db761a427a0e3b490b1b<br>SHA256: 8e5138a57ee718b08f63f4f83cfcce105e93e886dab9c2a4b0d694e1d33f8c1c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.766MiB (6.046MB) – 87,629 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc296d80d0d765e5ba19eb90c51034ce<br>SHA1: ace6ab121afc675d582976252cc791c01e040cd6<br>SHA256: b68bf7870021c8a1e794111b190412f9f7ca7a15584a5ea592e1c9eadba6a8e1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-07-30<br>IPv6: 2024-07-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.111MiB (8.505MB) – 406,187 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82c2655d58d25923b71f8373350c15a6<br>SHA1: 422b0f7257a2a3a638016f5587b7872821083403<br>SHA256: 22da4bd5882c3d140ed10cd3dd4322ee5a9724dac3e99399076099d3e4d10fad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.607MiB (6.928MB) – 100,521 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7c82784eb619b8afa0a3adbb0ac5d8d<br>SHA1: 052c40ed2f0e3de98a08ebcad0731ee89d6b7a99<br>SHA256: 7087ca983eea7ffde277488465dc90bf0aee359398ea10c088db15a8c5f60c75</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-07-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.55MiB (18.40MB) – 877,860 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f1afeeb73f8bec4789f012f30ba35e1<br>SHA1: 134d1c6d671ac599f2af6994645d668dd4a7d5ab<br>SHA256: fdacf009b0714e0c5ef6ce9c49648ca95b44de1e7d19a765e100c379adaf51e6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>73.48MiB (77.05MB) – 1,116,702 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 635d3241d084c80ea4ec8b057425e4f1<br>SHA1: 6f795337fd71c2c469084052acf07ba1c6dea67d<br>SHA256: 525b98330b04d8c79a31333bdd11ddfc08d83bacc521265f197b07df40dc1a63</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.909MiB (7.244MB) – 347,080 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cc33d54c3bf6b9175e0b145f7c4118<br>SHA1: a3816e7df4ffb8f7c8a3e26e9ecc5b337da78413<br>SHA256: cacc1ada016c1e717e0b0224945498ec7c02f45e18e6ccc3f699cf925eb98541</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.77MiB (16.53MB) – 239,599 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d8002e2bd70b383a55c26aa6c39879<br>SHA1: 2e8b5538dfa991864d56253287cfea899c731ec6<br>SHA256: 417be26de93d6c5b8d2da113e60494952f0235ed696211cedbd93a8683cecbc7</pre></details></small> |
| | | Full Location | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,260,981 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1931ab257b12ab9982e2e837f7a344a<br>SHA1: 265a511f4b4152bd6a0cba4302e7e551263bf78e<br>SHA256: af747f9dd2423c564835352c37e87e14cf8cec475eff93b3c6b458b8ad3a8e43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>339.4MiB (355.9MB) – 3,295,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3cd81e94c6b15797cf1a60147cbd224<br>SHA1: f49f6c791890b20c1ca8c05135f5558493b09356<br>SHA256: b412df8ef796f81fa4522b3051247207cb9af864a32937188218b559f4a52daf</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-07-30<br>IPv6: 2024-07-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.983MB) – 237,847 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a19f3b324b30f1b8e58614ced6c3eb<br>SHA1: 0ae869a9dcd1e992112ca1f19381c40b51f06f2b<br>SHA256: 16ded9b540a430569f72a4e9231fd255fdabd1dda07b4b19d35f69b1de8705a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.46MiB (19.36MB) – 280,554 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48429e636d89243b95e58e224ddcab83<br>SHA1: 62476d74b99370f1cf7032a405e741d78678dfbd<br>SHA256: 0cf7afea40b0dab546ce14724386b222921daeee0d831eecb913854ed7bdc0f0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-07-30<br>IPv6: 2024-07-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.1MiB (180.4MB) – 2,980,631 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b3e4b34496e91b79950bfd2ba90c64e<br>SHA1: 65cd184136a3ebc843b8b661eb3d7e435d8e169b<br>SHA256: 8fe209a185d5393cb91b8ddc3d044e30a9bbb3dfd9681ecce9b281cc7e030387</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,986,964 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf91d149bffc17e272f874de287e1a0<br>SHA1: d7fda16f424fa431e16b71116da2588052e905e8<br>SHA256: 28d426aa8fadf9fdb6308784807383ed47871f07d6c9d66d67e14bc55327d0c1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-07-26<br>IPv6: 2024-07-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.882MiB (10.36MB) – 495,052 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4ccd13aeb23f0619536980099eb7feb<br>SHA1: a2943def65fcfd2d5d442713e3c4fb0a271b1a7e<br>SHA256: 58a4c382003ebda1da0fadb1748be41a5d0b09b328f08bd08457efc38b664ddb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.57MiB (20.52MB) – 297,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f91acc93a30491c7ec385579b955e378<br>SHA1: 82aec91bc1f32e2ab8c0dedf514ef7eabf72ff2f<br>SHA256: 9f0c096d44d7f2e797c82974c64da6251f0fbf6428d2c0bede36f6e49fc44265</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-07-26<br>IPv6: 2024-07-26 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.7MiB (126.6MB) – 2,417,842 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da2b8a35d087482a879f3f807eee9c48<br>SHA1: a58ba097a8d13897c587656284dfa00ad938b265<br>SHA256: dee874f5b48753deaefde32e35813bef13ac1cd7252e1d0991b57ffaa9ddcbe4</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.7MiB (136.0MB) – 2,417,842 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 058657d49849a92c5b96932bb8466c3f<br>SHA1: 3be34aa5383ddd97180a020d2ba222660231ee3e<br>SHA256: 232993c8a5b567ef6d88d7085cb4a4637b653bedf4a8472ee293d467f6128fc5</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.5MiB (126.4MB) – 2,417,842 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e3ec1841c71555ef4ebdefc84ab3f2f<br>SHA1: 49d9586a8c89f23240f15bb316dac89c0632ea81<br>SHA256: bca526c78bfe3eccc8bd2d51495a57bed58d6afac538e6f56843e5a5d8008770</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>123.0MiB (128.9MB) – 2,417,842 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 328464a059eed4b2963d4d2105cec0f7<br>SHA1: 90f7c755b4cc86bac668dde1cd37badcd0dad680<br>SHA256: 95a98c7dede511ac47aa7cc93f986bda61b55c010be42456627f15b4b3198cd9</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.5MiB (157.8MB) – 2,417,842 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dca6b2a72987eaa8cd23952f32de1d8b<br>SHA1: 1f13b0f479b52b9ae03738fb22b46f2989a47053<br>SHA256: 679cde1d2c827de63eb9e1833dbf474f33f84d30bfbf88d6a4db930e4d7a3a00</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.7MiB (125.5MB) – 2,417,842 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f44c1682b8cd03b5cee9f2c4fa574686<br>SHA1: 8202e6e15f89fe1083d650c17447679ed0581616<br>SHA256: ba7904e58ca4d5fd03bf6ed876028ff1283bb34cb4487cb0e55d7f7da7c4e6b8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.8MiB (153.9MB) – 2,417,842 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a99c7b132f2d47567c8a7e87a4ce1fcb<br>SHA1: 87715770f0718b1b546c63283fcacf3cefd84212<br>SHA256: e33d27f3819eb71d2b8e7bb71a4e2f767a055e5b92e447b668f418243e4dde7b</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.2MiB (129.2MB) – 2,417,842 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d29d5e71d9983e9519699195898db8a9<br>SHA1: fe715e4e5db2ea3d3a63eadd12a38be64154b2ed<br>SHA256: 7566e0a3ca0f8e435a7fca7d195a7955df89b75c4489d4a47883433e451477d3</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>118.3MiB (124.0MB) – 1,273,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 597b4395c92c6b45ab87882c3c0986d3<br>SHA1: ebdbada8a915345e446c5ecaaa78302a306ecff5<br>SHA256: 0fea3cf74953555ef7dd36817e6516f18fc07fbe3b515ba265aaf0ae99ed3b5a</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>122.5MiB (128.4MB) – 1,273,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f3a35eca3ad63f583213f102b38b6dc<br>SHA1: e850f216bcf0a0322e4b011babac266be4c65e2d<br>SHA256: f211f52b6bcf1f8f7dd3b5d7ad7b6d90492be5212dc2287e61499208e6d0306c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>118.7MiB (124.4MB) – 1,273,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6088c2bb2af70f1ad5dd1cf1220bf71<br>SHA1: 200d2c9c3304811e7fb17648c722797efe2b8281<br>SHA256: 1bed8055acfc08d09acb609137bd718e1aa8a6fd7912e8172dbfbef7fb47a6a2</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>119.1MiB (124.9MB) – 1,273,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 205efcb69e69e88a01b79313777ef7bd<br>SHA1: 71dbd3d14cf102c59287adf78bf330e1da2b12b1<br>SHA256: 6ff0b39915cd0b8a96b9e0206b943189207636c9680cb4620d334995f644e4ce</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>130.6MiB (136.9MB) – 1,273,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e931ada25989a61414ff6919df5f66c9<br>SHA1: aaa1b80efc724096ea8bf78d157b19932b0055e0<br>SHA256: 34bcdf4726aeeb8fb44957ad69ac0f79370d532be4fb9f3d050c72726d37929a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>118.2MiB (124.0MB) – 1,273,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10086b03905bc7a0872ede3bd695b466<br>SHA1: c282658979c5e0f147d08ec3859865d167e840d0<br>SHA256: c1ee90013b14f9fbfeb5149ec63d56f38a3a06d754debf1538a43550834a0771</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>129.6MiB (135.9MB) – 1,273,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38e02e1ee94c1ad0625d33dfae892ead<br>SHA1: 8230ae018d22d57fe536a3f6c3d8e4b6ba3ba025<br>SHA256: ca5ca88966fd4850cc405770f58c3ef32836e1a356f0bc98cb894e61f6c40047</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>120.1MiB (126.0MB) – 1,273,333 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb441d67f27261547f4f9f1ab2d3f7aa<br>SHA1: a2dd62701d0c878d9783071187fa061616c3247b<br>SHA256: e84f8e9aa12ee43178dfa30d71c374b9ca1eec0373fc8296a61bb72441108251</pre></details></small> |


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
