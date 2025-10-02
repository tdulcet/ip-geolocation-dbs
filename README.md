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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-10-02<br>IPv6: 2025-10-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.310MiB (6.616MB) – 315,939 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d2007544df68b4433bc5da88ececcca<br>SHA1: ab0a039676b638f8247474c15070f86b39e52f14<br>SHA256: 3431e516b2daef4750f27ed3057b6547f38502e73635c5cc24eb0b1e33eab17c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.91MiB (11.44MB) – 165,769 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cee0b360ff0d2f4ed09ebba33c75fe05<br>SHA1: 6d6b50968998fb4491406b5bfd87808c80f3743e<br>SHA256: 997352edf584b3a670ac4848744b3ee32b9aadb0684c92dac52dfd8df085db3d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-10-02<br>IPv6: 2025-10-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.670MiB (9.091MB) – 434,131 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae7300bd06314aba50dd86f0b539a731<br>SHA1: 2961126d9cdc7224b5305add678ef9fc428a6381<br>SHA256: 84003a635efe754b0258797fc56203a49cc36d94fc5a6db4319787d7c0a81232</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.349MiB (7.706MB) – 111,799 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 662c3d603983283fa1997d2a274cadad<br>SHA1: ab13e7e7a47275449be6233396697d971a727ee0<br>SHA256: b5928c845824be54a3594cbbe35874d3f83bed7906b7d37d73142e35c5e47d45</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-10-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.21MiB (12.81MB) – 611,444 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fac64048b832695dad01e9faf0f8b04c<br>SHA1: fc6646ec46925c5e760ab5f4cde487c23f0c152e<br>SHA256: 4520fe4209ba6eebca373b69d3e2e1cf8321d6e39892edf99b5b3d3659e654c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>83.65MiB (87.71MB) – 1,271,215 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d6b0d7101cb6830c4a1df4eeea51838<br>SHA1: a9dadeaec73f9df18a749c04fb5dd83d9ed4444d<br>SHA256: 872fe38607bbb65b27ae60ac9356f2d758b3d4af3f5a7d229893dbfa276f47a0</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.915MiB (7.251MB) – 346,209 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e6d674990e0f107fbd088e17b77f819<br>SHA1: e21f5ede55e9a68287555b79c322fd01792544ff<br>SHA256: ee56d76f9c227d305e7f5b79e40e5d3a11d30d9b4b4a21b0a814bc5fc6ccab58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.87MiB (17.69MB) – 256,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf6418c75d48ec2ce4a2a1c5d27690ea<br>SHA1: 9b685f6a9fe8620ee6003242f3c5acf610337b72<br>SHA256: e1a598f6d63830a2bae69310a4cc6608adaede1395648f0431135c9239a1caec</pre></details></small> |
| | | Full Location | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.3MiB (220.5MB) – 3,682,011 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42145ba207725adfe20cd9225ad15164<br>SHA1: 1d40332c6092241cca96d8e93cd7fb5c58e051bd<br>SHA256: c60c91128d39be7572205c3f816d9173c65edc218778bf32f3d1094e958cfd2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>464.6MiB (487.1MB) – 4,514,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f22f776ceeb745f6db78a0eef703371<br>SHA1: 30ac2eb9a7fa4373473059683b5de9079a24fedb<br>SHA256: de1e8fbe3abd61a6d689615765352368449ce489b189853826fcfeeff7321137</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.161MiB (5.412MB) – 258,309 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f26d4302c7fd76db0d0260380f6bd166<br>SHA1: af4522cf5b0da7a4f55fdb43eafd9203505afe55<br>SHA256: ccd12d01d176de876028be848cfde48c9259fe6937a9d2b5860504143663fae5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.39MiB (23.48MB) – 340,241 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6eda0fd5aedd731b1e43a4c8d35f5168<br>SHA1: 6cc4cc30710f6cbe42343b9494b486362bce385e<br>SHA256: 7cebccd5d4724480dfa8ce7feb46df8346a377c9663e9c706a42f95c27d002e4</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.6MiB (178.9MB) – 2,958,155 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe165abca69867578e8e23a850e260e3<br>SHA1: 28aa8e4206a34c7c19baa2c8dad557e3e7e29980<br>SHA256: 395f8c3845977ec0aa9aeb6377d2342a1e06c37721d3b8e06ec2ffe85d3cc7e8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>294.2MiB (308.5MB) – 2,849,176 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84c795dd4c828d0cd8fd981934d68c7e<br>SHA1: 2745be7c734086c09f40f1d7190fb4ec6cb937f0<br>SHA256: 7db0021ec3c03e994dd396ac728595c5a9f0c6bc1180ba247056935d66e38a9b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.72MiB (13.33MB) – 636,421 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c895b62b8bfbc82a859fd380f500117c<br>SHA1: 154de9ee7710de4d42046087a02008f4c938a42f<br>SHA256: a1b0cd0062fcf89535b5d135f8f2985a2b0786e9a99f62661c7b08e948e1b72e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.26MiB (45.36MB) – 657,358 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e86528309e9b98282db37714bb27b878<br>SHA1: 6cc170a4a621faed47337ecf27fd53c6e728ac51<br>SHA256: 1db4633b78b2b11b716ee2bdb5bcaa5535379361ed703369c3f10f480fba00a8</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>175.7MiB (184.3MB) – 3,463,432 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b16ff58e71a8c43d06cbc722ca73cb91<br>SHA1: e5d948715a5292d9e2d98de38bc02b0a65e1cd5f<br>SHA256: b00efe75103cecf655eb5d020d2c07ff226d93bbe18820656ac9048935717e87</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>186.7MiB (195.8MB) – 3,463,432 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ade8ee5e0376ee57671fe7cacce229b<br>SHA1: a5d5da462cbbfb093176d91da6d85739ecd0f166<br>SHA256: e84a7fb4e96b629e52f8b3621f4c6dd398f06c3534ccf50847893b929cc0cf6d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>174.7MiB (183.2MB) – 3,463,432 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 129efe073b22204eea8ba40ef6031554<br>SHA1: 1b9308db224e71b379884759eb6679fad9f6020c<br>SHA256: 8f025c1fb298f61586da25b2e4d47893476ab591fc90138b7162161cdd531e8a</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>177.5MiB (186.1MB) – 3,463,432 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b0b33cec177a3e39e7859a4d27fec03<br>SHA1: e2e74aa3c3f57fd34c57583f8035cb4eed8710dd<br>SHA256: e0a5face62951b66b3fef82802bff23f1881154a37de960cfc6666f31170ed03</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>222.6MiB (233.4MB) – 3,463,432 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbfd2d112d3d16241a047df5a6199e0a<br>SHA1: e099214fa5fe9c8cbdcfbf71791d4ad442771f38<br>SHA256: 6ebe9e6a57be4d96182705835d9967a1ba2adf35a8283e87d5568f3829ea25b9</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>174.4MiB (182.9MB) – 3,463,432 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85dbaf78147464db9aa6367c68961df1<br>SHA1: d88086ae22522b5a92b7bba7be6d1514a89a4894<br>SHA256: 32a7a3275a501a77dd2a51ad2016a09ffe58b81e80b58052c118db7fd9b3d095</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>216.3MiB (226.8MB) – 3,463,432 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b63dd2a9be780f52e7178d46de8da1f<br>SHA1: 66b9b6b0bbd69d3831faf063823166e5667ab472<br>SHA256: 31871c1cf00852810b0d1def8ade7c9c53bd637a506973545af1a15a50189e8d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>181.7MiB (190.5MB) – 3,463,432 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a407dfcb693f949625647a72bbbd62f2<br>SHA1: a514ccc72f8feab70d4335c9de5494dfd0d1d08a<br>SHA256: 15cf788d02ec9e392209427d3a92c815166b0a2bee9fa7efdad22678a26ece77</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>175.1MiB (183.6MB) – 1,859,337 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 898eaa96e37129c56bd3047aa11428d3<br>SHA1: a40d7c4a58c9e49a7ce571bc72616260ae5928ab<br>SHA256: a3a2f84d9818b47023eee8d5e69328cf2f25f73f71c76c6a381fb943531bb4aa</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>179.1MiB (187.8MB) – 1,859,337 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1cc30c7830570f770378c59e978da07<br>SHA1: e146b48f931b00f1b1f897166a656a0591cf2be6<br>SHA256: b4e06f7cb43e9be9795feea273d2ccfe3c4625d08641494aa784c0cdcfa90f40</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>173.2MiB (181.6MB) – 1,859,337 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d72561adfb7f870a7b0e6b88c65a7ded<br>SHA1: 8ca25cee7ff73fa3dd3667603b98a9c7826414a5<br>SHA256: 43a228be8972c05525170096156e873524babe1eb2c09f234696fe5412dfdcfb</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.4MiB (181.9MB) – 1,859,337 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98a3b3d9f00ec3f3b8fbb1dc934e7b6c<br>SHA1: f515853abb490949ea433ad2a3f583246b224d1d<br>SHA256: 19d3f93cadfa239361260e4c420a57d4636a6841ad00641472778415d3ea0460</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>192.1MiB (201.4MB) – 1,859,337 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b7988eb8a27054e1740e67828f868ea<br>SHA1: 4f9b287da13e6d870a17a7addde15a05eb7028be<br>SHA256: e3bb0dc448db5dd22a58838ea318e893afb5b21deb582fc429822079dcf494f5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>173.0MiB (181.4MB) – 1,859,337 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70c2875ac8c4bec9386a358e9f8912da<br>SHA1: 6d7aceb1b0845a3d90da9cfde4d9e5e3c4c9c30a<br>SHA256: b41fc0a7a45a67a6afb3fdf15eae5d330fc881ae58c7155d517c012bb760f811</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>192.9MiB (202.3MB) – 1,859,337 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a08a38964981ce4cec6be7400de98692<br>SHA1: c63b21723aa672da3abf25bfce0107a615278706<br>SHA256: 6a4d239c82019823059b5f6546cb9ab8e9fe846ea3c0ec50123c7a9895681161</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>177.2MiB (185.8MB) – 1,859,337 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 499a643d3d81d77db5aeb645f19423c4<br>SHA1: 07f68f2f3a37561807343a657510f27768275342<br>SHA256: cb5fa45ff9a4354f7bb517b06080fc890e3d4833fd332c7b12d7c086ae7fb698</pre></details></small> |


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
