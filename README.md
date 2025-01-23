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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-01-23<br>IPv6: 2025-01-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.017MiB (6.309MB) – 301,263 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d7516a7f58dd930826b48834afbf25c<br>SHA1: 49ed81299ad30353d4054ba4ee6ddbf6833ae1ed<br>SHA256: 7c764b159bb6d83f8f6ecd3f571b0d4977098625fc9f13ce95eb6388f18096bf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.77MiB (12.34MB) – 178,877 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aaaaf9389e0ba26dba6cbae86924b2c6<br>SHA1: 9a5529503c1ea775e0cf0a7b735c57ea9c18bf9f<br>SHA256: 43a01f81cecfe2429c90aa04a68cd0b05f5f3e208a9ecbe16e0421275c4151ce</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-01-23<br>IPv6: 2025-01-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.331MiB (8.735MB) – 417,176 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14ecdae1d72487a9fda4ebd57e5595fe<br>SHA1: b6f0cd9f694b2ad3f76f6ed5917e5c71ef86b0e7<br>SHA256: 4fbe69ca5350ff39f8058f704b48b32d4a899c80ab5c846ea2f5612858d1ffd5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.094MiB (7.438MB) – 107,912 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b1298f49f2607d0131f4e21e85965d7<br>SHA1: 5fb921a4a49ebc663e8b498742a521d6994cbb03<br>SHA256: 06511ccbf3b1d2a59d1f1335e03039294c8a1867d5239c4486ba1ae6619b07b1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-01-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.46MiB (13.06MB) – 623,704 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4754dc053a12d36f1253755c730edebc<br>SHA1: cebe1b8128d1c1a390ae8e93c583f39eae6878a3<br>SHA256: ac5dd05751a859570f4fa241cffa6b545e8d657bcf82255c3332cec7c04085d9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>81.44MiB (85.39MB) – 1,237,586 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dcba6db3d6f232d3c69010787f2377db<br>SHA1: 8d7a70566676edd595ba5f2731702fa21a9499a9<br>SHA256: 96ba40c59841829cc22842f6870408deb49954d3309f66fcc80f34eb0e25cbf9</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.285MB) – 348,457 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83bc658c1ea05ee0c1dd67b508e416c8<br>SHA1: 70aa579150d7be548067432da89e0057b10e615d<br>SHA256: 636b0495d96e6e73c2fd6a2d599b3713d050acf8c2bc75556af8ad5d0fb3f95d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.36MiB (16.10MB) – 233,400 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea165adc6016bf7241db413dadd9d616<br>SHA1: c2e689ee2f5aa199cdf34e7bb0a4facf213548c1<br>SHA256: 40a1cbecef33f526b989ce930aa6fc2a0952064828188fe18df5b777d10b8d72</pre></details></small> |
| | | Full Location | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>187.6MiB (196.7MB) – 3,275,051 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ca665aabf2aee0b7c39b4545a5f75e<br>SHA1: 027d0a8a8014da5f6fc12e62c926c6933687bbf0<br>SHA256: 249e041ad20b36d2aebf8acd5c4d86a5f88957c86f3a7137f906df3200c6f623</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>347.2MiB (364.1MB) – 3,369,294 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb9eca947a082a3f2644b8c6907a6194<br>SHA1: 6d3040b4badad6d8c3e74a1fc773d997d8a618af<br>SHA256: 4d20b8e6b46f24b32ed9d99c2e5316f3c7e940a92aafbfdc42bea1eb6751282e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-01-23<br>IPv6: 2025-01-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.096MiB (5.343MB) – 255,041 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 385e7d39a49da4f7b26b8ca022e788dd<br>SHA1: 7bfbc318f06616719765ecf95f9c600ee41826cd<br>SHA256: bc2cb4bb17afe8e3962b87a8deb428f68ff7083def1f45c295c77d61751a71c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.13MiB (19.01MB) – 275,512 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3010eb9cc5eb5d69c08e40e6ada6b77<br>SHA1: b14d2ac80fc5b7043024cae2173668671a286f87<br>SHA256: cbf1a41317aa32c82f0ad9508afdfa47f673246f62711d998001fdfe0a7f5b17</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-01-23<br>IPv6: 2025-01-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.4MiB (185.0MB) – 3,056,590 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a976173ff14b69a2f374b84348a7b747<br>SHA1: ffcd6b20ec9ef8f0b9dc4f4c901e9fbf0f87075d<br>SHA256: b58bb3a37215ab1b1889208c52164428b5c56380cff711b82b6e54e5febfc1e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>226.7MiB (237.7MB) – 2,193,791 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fbc49d9a6e454cea9f8835d6e2277f3<br>SHA1: 9bfe0073a0141bc90622c08c9161a7283d562072<br>SHA256: 451e6a13f9d9293ed3e076c9bca96a945e2b1e2fd52e8171481f1a31a9e2be46</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-01-21<br>IPv6: 2025-01-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.17MiB (10.66MB) – 509,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 774d3ae09ac585298e7d4dd93ecd0140<br>SHA1: a37c549485773f696107ab280534b7f60f070711<br>SHA256: 5e5beb2153e46b5f778f78c902b9128af762e6c434fdf61663211989331c2eb1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.52MiB (33.05MB) – 478,955 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a7eb560bf83c4a40749d83bd71920c6<br>SHA1: 950dba6ab2517921fe8c7a2b646ef9efadd57f3d<br>SHA256: 657671258da3d2a1a4a212d2e6dd0e157187a10813c0e76fd8e465d7f689f6dd</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-01-21<br>IPv6: 2025-01-21 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.4MiB (173.4MB) – 3,270,676 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0abe3f972d48a3cc770fcbcc5a3e9f57<br>SHA1: a7ea3c4d68e5eb700675e76b404da2cc2e6dfa15<br>SHA256: 727eea0b1da4675bdbf8e28a36c408714d88d5286f3708fba2c64eb52e6b82c9</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>176.1MiB (184.6MB) – 3,270,676 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ac7f7bd57eca2750b5bd91647552ec1<br>SHA1: 5eee62837ba04a24fe165053d02dbb40856b0d62<br>SHA256: 224e4474f8a5a09a259c7261b115d56c06cfc919b5716e3042ad3f1c51fbae45</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.3MiB (172.3MB) – 3,270,676 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3a03eaaa217ceac9ea554168764e73e<br>SHA1: fb1d5cb12ad158ede2553caed7a7fb2123aea326<br>SHA256: bad06184021d3f8bbf64f2b4c24d5dabedb6ad5be6074e3a65d1234251374f9f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.8MiB (174.9MB) – 3,270,676 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c8853cdbc204b87804c95e2120c8e05<br>SHA1: 3638b9176732cabe4e4fb8b8a7160f5cc0a561d7<br>SHA256: 7b860c9b7d8197d6434e8ef52d0785b51ae6a19f8729144c6eb2e0b3ce6a16bd</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.7MiB (219.9MB) – 3,270,676 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46dce3a2037bd0426d476c5c99f44e7d<br>SHA1: e6b6b03c30e798c5bc16c5adfd81e11c9acd4c55<br>SHA256: c719e00c1a9c33ed9f3ba1e4c435d81891a4cf8a91757c54b104ab43b49141c1</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.4MiB (172.4MB) – 3,270,676 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1132177c77c47f449eea8fe09d21d886<br>SHA1: 12a245beb5750cbf6877b54849eceaba1f9e493b<br>SHA256: 16caf18141426221ed2ab197822318db2ff1bb2e536ef8d2c6d02c9472c7635a</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.6MiB (213.5MB) – 3,270,676 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c18d74683292c134ff6c8ca500f63de<br>SHA1: 4af074d3bbe0bf8768e84d35db74b0503d6b23fb<br>SHA256: 04117f2745304e721471732aae7e6b9a0ac74cec79d78ecaa97d4913da333518</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.5MiB (179.8MB) – 3,270,676 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df08a078312fe68c7929472803efa6cf<br>SHA1: 1ab78f04701ffd3d2c90b1bf2a2fd274fb1e0343<br>SHA256: dd9fb5d92ea9e94f67ee5cef1a4ddbca967be69e9b48636da756a16fc2a68665</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>162.4MiB (170.3MB) – 1,729,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2335d5015798029c55794a24d11701b<br>SHA1: 22cbbae39cab562b9be102b17cb5b22a60e5f63a<br>SHA256: 848802d3a93dd831a2e75b6a5b5a702055de08519bf35b5775a9e481b388490d</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>165.9MiB (174.0MB) – 1,729,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c34c7146639e550b262b205d35f82c88<br>SHA1: af61bf97f982c28fb36f6c84740684f6826a9eed<br>SHA256: 183973d4ebaf7cd5516607c62c8e261a2b18b7767f8560260417c48289b08dd3</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>160.5MiB (168.3MB) – 1,729,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f0f5d56dcbe867d0e6eacb46d785803<br>SHA1: b8d47a231c7aaa3c6c7659afcd5121d1ab619de1<br>SHA256: 9835ea2bf58d3b3cce6613d2ecb1ccda14189b8549ac79b079d8ce55f3bd7674</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>160.9MiB (168.7MB) – 1,729,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bed11cfe14e0efc118b71c03a186a94d<br>SHA1: b9824b281fb53d0d99e04122694c3aeaf17051a9<br>SHA256: 3bf2b9643b34a6bc145212425e7b5c906a7a94125ae25381652cb462a49e9fa2</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>177.1MiB (185.7MB) – 1,729,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c19cd4c3157a07f372f7cdaa6ca56f7<br>SHA1: 61bf1a21e067449c2339f37721e98c83f3dae305<br>SHA256: 13f3071bcc5552e56c68ce30c789a773106ab9881aed33f5e80b760c4d8ea675</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>160.5MiB (168.3MB) – 1,729,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42dd901104ff431ee92e99d249b1f2a1<br>SHA1: 103abeb834e86ec0a16319c60c9be75ff6008ac1<br>SHA256: bb1631c9487543ba373ec7a7433dc2dac19c7f5eb70a63af794c4aa8c8169b05</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>178.4MiB (187.0MB) – 1,729,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50e818e586ec1fbdbbc1174f84ff1de9<br>SHA1: 5a80716ab6419a263b74fdbbdf8a820aa183f7fc<br>SHA256: 9a856cf11de73748c021273c203068e1170ef123047e00c76d8a958dc356edd4</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>164.2MiB (172.2MB) – 1,729,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a28a6ca4c59f4d267263747c31fc8b9<br>SHA1: 50b60f18aadf0b079ef52769bab19e3d59a05585<br>SHA256: 459462f9d8f461ec26711f207de62511d9d5b1c12565b8d8ee42ce3d2ca97cab</pre></details></small> |


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
