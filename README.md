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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-07-31<br>IPv6: 2024-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.754MiB (4.985MB) – 238,009 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69e3297a22cbaeba30863ea9aa1ebd73<br>SHA1: 6d48eaf2fb4cadfaa14a7b5f34d216a43e9518f2<br>SHA256: 0346ca2a3e9684ea66c7ee4f88a1eb54ba55521eeb90d6bd077e94ee02cc5a51</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.770MiB (6.050MB) – 87,685 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9951c919ef65f1fe12c06e8b1d458c1<br>SHA1: ea240ce680f03e7158e5c30d8de932e29b37e611<br>SHA256: 12ecb9bbdf45ffc914599cb3f54c9aeb4db1951c336779b884e3318a483b4f89</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-07-31<br>IPv6: 2024-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.115MiB (8.509MB) – 406,375 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b59719791b53dbd12700cac0b1fd3ddf<br>SHA1: 763851e9d27be23edde763d468b817180aa29811<br>SHA256: fd9981957141f218d82aaaa9a9abb1602d06e369faf7818c18c468778c54295a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.615MiB (6.936MB) – 100,639 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6db554ef4e59b2b6dbb49d59f117fc22<br>SHA1: a46d6debdcbb2dff6af5bd2688cc582747b52e59<br>SHA256: 16b3065c1a8ee9342c76f8a009876b8f949ef26123aff7c9b10991fa30f29647</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-07-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.55MiB (18.40MB) – 877,860 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f1afeeb73f8bec4789f012f30ba35e1<br>SHA1: 134d1c6d671ac599f2af6994645d668dd4a7d5ab<br>SHA256: fdacf009b0714e0c5ef6ce9c49648ca95b44de1e7d19a765e100c379adaf51e6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>73.48MiB (77.05MB) – 1,116,702 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 635d3241d084c80ea4ec8b057425e4f1<br>SHA1: 6f795337fd71c2c469084052acf07ba1c6dea67d<br>SHA256: 525b98330b04d8c79a31333bdd11ddfc08d83bacc521265f197b07df40dc1a63</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.909MiB (7.244MB) – 347,080 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cc33d54c3bf6b9175e0b145f7c4118<br>SHA1: a3816e7df4ffb8f7c8a3e26e9ecc5b337da78413<br>SHA256: cacc1ada016c1e717e0b0224945498ec7c02f45e18e6ccc3f699cf925eb98541</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.77MiB (16.53MB) – 239,599 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d8002e2bd70b383a55c26aa6c39879<br>SHA1: 2e8b5538dfa991864d56253287cfea899c731ec6<br>SHA256: 417be26de93d6c5b8d2da113e60494952f0235ed696211cedbd93a8683cecbc7</pre></details></small> |
| | | Full Location | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,260,981 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1931ab257b12ab9982e2e837f7a344a<br>SHA1: 265a511f4b4152bd6a0cba4302e7e551263bf78e<br>SHA256: af747f9dd2423c564835352c37e87e14cf8cec475eff93b3c6b458b8ad3a8e43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>339.4MiB (355.9MB) – 3,295,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3cd81e94c6b15797cf1a60147cbd224<br>SHA1: f49f6c791890b20c1ca8c05135f5558493b09356<br>SHA256: b412df8ef796f81fa4522b3051247207cb9af864a32937188218b559f4a52daf</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-07-31<br>IPv6: 2024-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.983MB) – 237,847 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a19f3b324b30f1b8e58614ced6c3eb<br>SHA1: 0ae869a9dcd1e992112ca1f19381c40b51f06f2b<br>SHA256: 16ded9b540a430569f72a4e9231fd255fdabd1dda07b4b19d35f69b1de8705a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.46MiB (19.36MB) – 280,554 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48429e636d89243b95e58e224ddcab83<br>SHA1: 62476d74b99370f1cf7032a405e741d78678dfbd<br>SHA256: 0cf7afea40b0dab546ce14724386b222921daeee0d831eecb913854ed7bdc0f0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-07-31<br>IPv6: 2024-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.1MiB (180.4MB) – 2,980,631 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b3e4b34496e91b79950bfd2ba90c64e<br>SHA1: 65cd184136a3ebc843b8b661eb3d7e435d8e169b<br>SHA256: 8fe209a185d5393cb91b8ddc3d044e30a9bbb3dfd9681ecce9b281cc7e030387</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,986,964 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf91d149bffc17e272f874de287e1a0<br>SHA1: d7fda16f424fa431e16b71116da2588052e905e8<br>SHA256: 28d426aa8fadf9fdb6308784807383ed47871f07d6c9d66d67e14bc55327d0c1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-07-30<br>IPv6: 2024-07-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.882MiB (10.36MB) – 495,007 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b25fce70a01532d248b9da4d46fba47<br>SHA1: 207d107046137b8a3230cf0a519700a7b929dd63<br>SHA256: 51c473ea84b095e585c055c628be820280d881785957886c5c9a797336ffa193</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>20.60MiB (21.60MB) – 313,099 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0387d5e2660678f520a826bf710c6ed3<br>SHA1: ec5f9bdb66ba1ce2ee8949c3038273c3710b6766<br>SHA256: c1b12874b61131b3acabc8b1afcc1d0c76071119658ccd36546b52d0ae9f3c63</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-07-30<br>IPv6: 2024-07-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>119.9MiB (125.7MB) – 2,402,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 162d35ab072d4caf574ac0c800471eea<br>SHA1: 740ee16c6bf8151b5fa98461b1cf515ec74e29f5<br>SHA256: 8b7923b84cf026c762a5195587ab52106f5d56d5bb350b476ddd21e2cde3c601</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>128.8MiB (135.1MB) – 2,402,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd1d6f0f635d2e9903fff0cd63d696f4<br>SHA1: d65aa8c40301ded0c3af054eacf61a4492738cc9<br>SHA256: 4ac730c39126f1c8c22320fb0f1b66719c068145d0b9d471816ecf5a92491d35</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>119.7MiB (125.5MB) – 2,402,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1303a874db39290a38b3f2b34c91d4c1<br>SHA1: da47d08fa4a8ddf7d4540efe9bf25e11c6c19971<br>SHA256: 6391334f15509bd2e1969cfc653d804ff79b695fe04f9e57029292dd01cb75eb</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.1MiB (128.1MB) – 2,402,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86814ff96c0635d64c8f184edf9f9fff<br>SHA1: ab3dd942f643327b57295045f7a16091fe0fc9b8<br>SHA256: 3abcd39410f16d92c82af24f67578716918c9f5bc66196ab3702ff7f918facef</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>149.4MiB (156.7MB) – 2,402,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e81f5ea7cc5cab11864268241cfe33d<br>SHA1: a6464b56353734059c6eda956d6b2b4e2503a239<br>SHA256: e74812c59bb82c35aeb17b98a03752b5c33cb21093dd9fdd5bdbe654758d6848</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>118.9MiB (124.7MB) – 2,402,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ca58c91aef5a5525ea33a547ced65c9<br>SHA1: 392ed828cd972f4bd8043cdc9d27c39f93a26100<br>SHA256: 98ef59dc71b1962b7b0741b872606afb39e2099f6bd4d8004e2635347ca161ac</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>145.8MiB (152.8MB) – 2,402,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f256c7e02ce7429834f74f3bb6fcc53<br>SHA1: 89f05b8ad254948adeb3963b5f7d3fee950a51e6<br>SHA256: 272fb834d17688960399d90e6e2c21cdf1552bbee4856195fa5a71599e5d4511</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>122.3MiB (128.2MB) – 2,402,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51b11016abcfa3caa65d0ec3d2b9cb34<br>SHA1: bf9dc09df933ac3b4eaa251fe236b7422e7a39e4<br>SHA256: ae56ebdabf78cbc234ec489c477f6c7b6b289ce8fcc020dd129fd75fa9fe44bc</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>111.9MiB (117.4MB) – 1,204,849 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9dc86199062fb1f79e21f4b2b556c793<br>SHA1: 444b9b40af88595582ea2278bb695d3ffbec1f87<br>SHA256: 2e73d193cfc05e8f39d3f78bbe615f22f0caff0f4ea8d45c0b3aeb075628e881</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>115.9MiB (121.5MB) – 1,204,849 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ffafc0ebc0894bb16d84c3766c2f038<br>SHA1: 01574be02701961e669c386419e7e53f3bfbc016<br>SHA256: 81c3f2b6bf723302e540a54d5a6c8b3eeb9fc663ff01969621c481f89b0fdc2c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.2MiB (117.7MB) – 1,204,849 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dff51271cac9957838cb162c1ce09499<br>SHA1: a153a8c2293a78ec870ca701a79092bd090167fc<br>SHA256: a46733eeb3dcfe1f84d5b6562ae12fdeb6f57cc61fbe345a5d570415a27c888b</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>112.7MiB (118.1MB) – 1,204,849 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8ecb75893ee3bf0073abdcc7801c7f6<br>SHA1: dafbe5113968f3c81ae9a0ba6049b81837259789<br>SHA256: 1df40da5961776c95c69c9ebac8ddf0adfb6f7926bd40e98c6709e46844a50cb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>123.6MiB (129.6MB) – 1,204,849 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3951e0781ee83f51107f8fc682dacfa0<br>SHA1: 9dbe0cc7ff836df1f8884b7679d9580fd7901ab3<br>SHA256: ae914de63a012624979cf5b453fd768f003308a44ac6df013e5d9e533e893bbe</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>111.8MiB (117.3MB) – 1,204,849 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8167bf7b73c5068fefd87d6dbb1ab6a4<br>SHA1: 18ee8718a06af7188a8e7af23b6b217a4117e6ae<br>SHA256: 44e4c5fb6d35d3f38a99f656abd0931510e989960b7e87f2528540a5888d3b5b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>122.7MiB (128.7MB) – 1,204,849 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9e3609d7a453b773c6845d074a21611<br>SHA1: e87fad99c3d5f59ffc7c12c6f4ce57256a139dc9<br>SHA256: 2fed731f89fd65d4505021397f6e043e71a9cebdcdc3d0b399ccbe4f5a08e761</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>113.7MiB (119.2MB) – 1,204,849 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc36e8e35eb37bf5c54ce1d44e2623c0<br>SHA1: 8080f8d3b6e0440d3cc9d459b92a1d9b84637c1f<br>SHA256: ae852a3f099b05f65306e8825e1c49173ae72bf4a1bdc65c8c3900cbdbfb0e2d</pre></details></small> |


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
