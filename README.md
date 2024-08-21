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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-08-21<br>IPv6: 2024-08-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.769MiB (5.001MB) – 238,749 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3984bbd51c0bf61da2bca13f21cc028<br>SHA1: 6ae1b2a126162b97e7fd279c0164292f3d2fe75f<br>SHA256: 629c4fc45b218c621373ad04343733c2f050dc3d3b6b2fcb9106bb8c4a7f81ed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.812MiB (6.094MB) – 88,317 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2b37f76098140c9ff047a6b54616169<br>SHA1: b42748506b2c727abc2e2ef159cb202018095987<br>SHA256: 478ff974877fb844c60ed13595753f3aa8b960ef68b234f1af8a2a2278a4c733</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-08-21<br>IPv6: 2024-08-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.135MiB (8.530MB) – 407,401 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f13ac62d92fc148cae9d09b1a81f164<br>SHA1: a827472fd13e0395ad7d9fc8440e050ed868efec<br>SHA256: 79d89f318d485018def606f053a13dbfffbf159051631fc3526bc099b07e5739</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.644MiB (6.967MB) – 101,084 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9d88f25d7ab6f669dffdd62282e05a8<br>SHA1: 0070477101ac1ebd1c9dabd7bce0f2e8280863ee<br>SHA256: e789ebbf25aaaeea5a9bc93b0564d1c3d804943149c13fde24ffe19c55b81c2d</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-08-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.96MiB (17.78MB) – 848,283 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d09115091cdf1aeb2b20f8f3d41bea23<br>SHA1: d015a52b91d9008c578f0d880873d9c860219c57<br>SHA256: a3cd080c7be904978b871b8027cb988329c9aecff15d9c2935e5b92fb838ff42</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>67.29MiB (70.55MB) – 1,022,534 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9c4ddfda7e55f62beeb598b69dfade8<br>SHA1: 48bb0ee468255ada16148118e710a945a99592f1<br>SHA256: 55c3ac2dd0ba5cabb47b5c41c6f161ee7103dcb5ee25554045e933bcd22534c1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.930MiB (7.266MB) – 348,283 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0fbc41bc5bb2b90a8e0d5e5ce544a9e<br>SHA1: 1e8f1c989a09bda0597a4fd20bb1baf0e1ac7146<br>SHA256: 5ca608bc0834afa2ddcddbc57debfbc70f177637b74991fa1f5eac6b4004250c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.13MiB (17.96MB) – 260,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d830eaf780889ad98001bab48d5aa45<br>SHA1: b197b3368dda5c090062b0f952b463dcc36089a0<br>SHA256: c9b5f78bc10fd064cbc6e77285c497db8377b1d955acc23e6e6498b158cf6e7a</pre></details></small> |
| | | Full Location | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.4MiB (195.5MB) – 3,254,855 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a701f04a73cc8f80f1d62d7d31565c1<br>SHA1: c08290366ff76b789e82bc1d59e49f3a8b096083<br>SHA256: 05ad2982bf2f1253f055b5d985d376d16bb31cace83cb242d464f0595b931ab4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>351.7MiB (368.8MB) – 3,417,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e978ebf3bde1f974ba0a4b6532bcd5<br>SHA1: ce0a2c31a0c136ca457da29799b4d9d902203525<br>SHA256: 04b7870a00431ac40aa31592ac986f30dc8fcd0035a95ab9beee69df67b812b1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-08-21<br>IPv6: 2024-08-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.983MB) – 237,847 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a19f3b324b30f1b8e58614ced6c3eb<br>SHA1: 0ae869a9dcd1e992112ca1f19381c40b51f06f2b<br>SHA256: 16ded9b540a430569f72a4e9231fd255fdabd1dda07b4b19d35f69b1de8705a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.46MiB (19.36MB) – 280,554 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48429e636d89243b95e58e224ddcab83<br>SHA1: 62476d74b99370f1cf7032a405e741d78678dfbd<br>SHA256: 0cf7afea40b0dab546ce14724386b222921daeee0d831eecb913854ed7bdc0f0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-08-21<br>IPv6: 2024-08-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.1MiB (180.4MB) – 2,980,631 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b3e4b34496e91b79950bfd2ba90c64e<br>SHA1: 65cd184136a3ebc843b8b661eb3d7e435d8e169b<br>SHA256: 8fe209a185d5393cb91b8ddc3d044e30a9bbb3dfd9681ecce9b281cc7e030387</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,986,964 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf91d149bffc17e272f874de287e1a0<br>SHA1: d7fda16f424fa431e16b71116da2588052e905e8<br>SHA256: 28d426aa8fadf9fdb6308784807383ed47871f07d6c9d66d67e14bc55327d0c1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-08-20<br>IPv6: 2024-08-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.548MiB (10.01MB) – 478,345 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0c27ba732b687920d21018e3fb751fe<br>SHA1: 9e53ff482a4ab0aacab2456a3b978859a1e7c36d<br>SHA256: 605de127ecd9ad5f816a9b0f7c4eab5e1bb196f4ab6931481b022d10f06a03c3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.04MiB (31.50MB) – 456,560 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a626b4502f9c26a9eda842d669b84b91<br>SHA1: 01c52bc61c30962eae18dc77db2ef30af5147618<br>SHA256: 536675ab922b4f5b52eef4e7f8dc8ff9923da2b7ad53583cf97b4c0216ecfca5</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-08-20<br>IPv6: 2024-08-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>118.4MiB (124.2MB) – 2,374,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0891c1161cd16adac0b5c6ce145abf69<br>SHA1: b5e7824621e4c62a416c878cb540fe614deaf8a8<br>SHA256: 05cc383ab39de27a6f0d7d99051bd1f9e5c8f0e0a76dc78ed884a6b1512295c1</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>127.2MiB (133.3MB) – 2,374,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fba008c0c2bf4edf7c0610e7e0e32475<br>SHA1: e43d0401949525616e66243c6d3f8470d6cd0cc9<br>SHA256: b7ca9d33d2bb8b62d1fd1a2eb5dd4663c4be9e7a83028299e8841b2ed9cfdd7a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>118.0MiB (123.7MB) – 2,374,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db9e0b0b06850f92a98bb4c12e6707ff<br>SHA1: a97265a44630ad7750e70e32f2326cf92d8fc90b<br>SHA256: db2e8ba07c3072576e488d46d518853bf8ea09f24444bb5951e2364b1ec395ad</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>120.3MiB (126.1MB) – 2,374,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 457c036000cf0a8b77c95d92b16e2a56<br>SHA1: e4125d0f1dc930943410ba38a2b9838d30d07bc6<br>SHA256: cb207217dda563f4fb027e6ecce4f08520aceab264e1cf9205160a46c639f263</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>147.0MiB (154.2MB) – 2,374,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 692d42138e28dcc7fb7773fa8796d94c<br>SHA1: 7dfdf1a7514faf3ba5659356ca844467eac33f49<br>SHA256: 72675602c079b50e603f1fad0859899ca247f593d82cdd7b29c993ea8c28f851</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>117.2MiB (122.9MB) – 2,374,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74cd0272148c0a9457de8351ab034199<br>SHA1: e30c07d055574780a687c60a93b532439a7b3b6c<br>SHA256: 05c79a0d5b35ed64b180153dd52afc9cda2a49dbb19280757834b86dad90e790</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>144.1MiB (151.1MB) – 2,374,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 509a988afe8051eed99972f645cf0144<br>SHA1: 2b803f1121a5e7de4240314f3d6db8f69c795722<br>SHA256: fab4d71d3b7df3b3838850494b5529b6557175336057dfcaab6c3a4d55148aee</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>120.9MiB (126.7MB) – 2,374,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84e29cbdce24a8d452ea608e10fe8e03<br>SHA1: 42c9bee4cafc467005c5dd257187f256378c0e88<br>SHA256: 2d4d521d86da10c81d892cb6e444fc32019e2dff715b122ff5a9189ef4e99113</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>152.7MiB (160.1MB) – 1,635,869 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76d6b667b47c4210e6731d00fbe154e8<br>SHA1: 487a7fd0e0b4c37cce7a30a860203834b8312f4f<br>SHA256: b006ca618f1436cbe507dfe0e897290fd9319c2aa31dbfee03bf67473d6358fc</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>157.0MiB (164.6MB) – 1,635,869 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ca257bdc1c78fc2d0fc6bbb8924a79d<br>SHA1: cc29713b6910d97b0faad46578445b77b558f976<br>SHA256: 9451786b75fe3a4efde87f1b07db37572579480c5560cb8bd7b744e34b695cf5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>151.1MiB (158.5MB) – 1,635,869 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d375a9584e21d5d568e88935b22f4be8<br>SHA1: d17575a0b4e034135db75f257add20f8ac5bc6f8<br>SHA256: 50659e8d38f8fcf671c60f87a45f84098b6fac50b9f40149f0f9fd0b19857678</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>151.4MiB (158.8MB) – 1,635,869 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a840df4fb0683711457bffee967a884<br>SHA1: fb7239a09e5b56d1844ef51bcf05b57ddb3fcaa5<br>SHA256: 4932d3e47fc5e83e3680eb73b30154639165f23fbdf9e34979aabeabf73058e0</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>165.8MiB (173.8MB) – 1,635,869 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9cd7abe76d073c745d7b42b33dd0f30<br>SHA1: 952512be4eff006b9e0273433ab84f3270ea0c8a<br>SHA256: 1ea3ef31efc4aa398d38bc54bf84c190bda0a871d7c1dc551313a0e593754dc3</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>150.9MiB (158.2MB) – 1,635,869 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1356ed76467203288f9387f9243201ca<br>SHA1: 7163039b20319e1ab435cac5f1cd70349809c081<br>SHA256: c6b9e6b4b729eaa95dc11ac7597788d2bee8f84cfeafe6e33b5ef0671b413aee</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>168.8MiB (177.0MB) – 1,635,869 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f35be19e0ae306a457e46970ebedabd7<br>SHA1: 5650be56c87b56c858bca17cbaf9ba51335b5456<br>SHA256: d7593a0c455151866d856b1ca6d1de925245fb31d80c032076603ed16ebfcf12</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>155.7MiB (163.3MB) – 1,635,869 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: adeb30384096e9702e816c476ca94c9a<br>SHA1: 0415951be3ad9605159643b987bfef2268330484<br>SHA256: 10f2e300f8cd0199adb8e254b0bd334b16a4f9fa26bf12ea5919a5636e9525be</pre></details></small> |


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
