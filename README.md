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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-07-26<br>IPv6: 2026-07-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.423 MiB (5.687 MB) – 271,410 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eef1c08aaf25a4007f24b24ee0269213<br>SHA1: 9246dac1e6bd391ea04400e2f87f7af2149f9553<br>SHA256: 6891443647b0f8769fd17b19e311d036fff2ece40199f1d0fd8a0ed4e1fec7e2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.83 MiB (17.65 MB) – 255,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f29a29a0fda18f3d4062351346683ccf<br>SHA1: baa2ed61bab237dd9a3cdca1c7d52cc3cd897fc0<br>SHA256: 2311795d435cf4679d811a9da78c663ab104c73694512f67fb9987f9b858739d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-07-27<br>IPv6: 2026-07-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.032 MiB (9.471 MB) – 452,214 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6dc0e372a2e8e6975e85fa8bb30ee902<br>SHA1: 3bb846f385d6cc7ccf387ab12ab2503e0a152321<br>SHA256: c15f78cfcbb0462e7edcbc203a514db41002080f63a72cc93bf00e4d4ac2da8d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.955 MiB (8.342 MB) – 121,007 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d12f88b0beb265283a527276f977a2d9<br>SHA1: 925a6d87baed967deecd6e9676e610e60ec2d2ce<br>SHA256: c4d475078dc36bd2e0cf8153e65f40f394fb20ab48484544be17f7511b5e4a05</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-07-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.13 MiB (12.72 MB) – 607,374 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ecd240bdf7027681bdc28f6bc4be950<br>SHA1: a1510ca3b752be0242462d89a255586795e891ef<br>SHA256: a8061823486070f0c9fb743a2e28d4dc38313b1fe857af599266b1f069437da2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>42.25 MiB (44.30 MB) – 641,997 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4a660d636eeaa2d8eeae3373007234c<br>SHA1: d5b1ef10111579d25cc14437754b9da25f7a4db1<br>SHA256: 1324dc37567b389bdc6e06e7f1a858beca6d601c1162faebeb141df6c46cec3c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.078 MiB (7.422 MB) – 354,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ec835290735187164b1f2f622ad9c0<br>SHA1: 10464ef5eb489f4745096b1c71046b06409244b5<br>SHA256: 6bc4af63c1e15b4d99d5b9dd9cddeb67bbf2eafc2529ba5d9ec4525e0fe7964c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.51 MiB (23.60 MB) – 342,046 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569d0c6b66a745289f0e152318090f38<br>SHA1: baf1ef75355d41d9bc4380f97ed3b085db479655<br>SHA256: 8940a06c7f9a27f129048c5a7a0b1579b368020d88f2d2efe0fc813b6d2f97e4</pre></details></small> |
| | | Full Location | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.3 MiB (219.4 MB) – 3,666,805 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b729ab459cc2b765b3b4ea035f481b<br>SHA1: 1496af12b72ee784e304cd84eb7335c826bc3906<br>SHA256: 69fc5ebf5414a7a939fc25a35f3128451cf340211ae51ab9f82d53a331d8ca03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.3 MiB (473.3 MB) – 4,386,528 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f197b2ebcfed77f9adc3310fc7b6020<br>SHA1: 24b1454a40fdda39f37fa9367a6a6a5a88d3be33<br>SHA256: 0160ad6b5bca3517eb65f79d6db1f9e373eeb34cfccbf189a588bb330d17af06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.670 MiB (5.946 MB) – 283,812 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96cb0452e66db1c3a35242fa031ebe0f<br>SHA1: 28fae5a412332f0cedc711132a0dd6f337488ec4<br>SHA256: 2785f482dbf1f2dcb1bd3a9f253c708b1fa5f86773908ef7a2f2bb16c0dd1ff4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.24 MiB (23.32 MB) – 337,921 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1683effffd067b4fddf82095f002903<br>SHA1: 82f6a3b239649f9e8af05d58b628eeed874ad7cd<br>SHA256: a51cfe2b60d111ec234510abdd73583f12186f7fc35e3decd80fd4ef4b5ea654</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1 MiB (178.4 MB) – 2,944,788 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52717d3cc345c65ab5cb86167d9b2112<br>SHA1: 0ad1bd8bf0bdf711f51a9a37bb75090cbf4ffc84<br>SHA256: c92293057f12c2c364411c35a02de2cb229e7a21791a1bfd25cab2ba6beac1cc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>298.9 MiB (313.4 MB) – 2,896,639 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23b3d9e4addd1683ed707d17a98a0e22<br>SHA1: 572b0633e6453018a04db4c06504726ffcbeadba<br>SHA256: ba14acc8e2fc9ac380640ba99de27ab073d603598996f6737853e5a1ca4a8a13</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-07-24<br>IPv6: 2026-07-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.26 MiB (11.80 MB) – 563,667 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f860b5c5de8e8476b430f900a09295c0<br>SHA1: 84421c95eed58bb078605d940865f4a39a6232ca<br>SHA256: 91c2ab4234bdcca1fd933c9388931b0405a0db2f3337708e184cc4e9d5f3bf51</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>36.06 MiB (37.81 MB) – 547,985 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 741e1b51a2c29277bddbc1b90f304735<br>SHA1: 9fc3f44f3adbaf0fcf03b0b5a754881f0b74fd74<br>SHA256: 5b6e1de5b0f833aa36943f1fa3a34cafb051e3481169bf52dfed7e929a6e141b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-07-24<br>IPv6: 2026-07-24 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>193.7 MiB (203.1 MB) – 3,770,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ebc408a8eacccf17ba86b3ef7ba38aa9<br>SHA1: 1a0e7d6947c315d46fec53786bee7de7a1af8ffb<br>SHA256: 30536167111a7551ff2065367cc81a86267153fe306e79f923ff3ce4f56b90e9</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>202.8 MiB (212.6 MB) – 3,770,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3391f9fbf1c2edbcfd08c17845b619c4<br>SHA1: 3a84668f5c2943b36a21114418955f17b1b4199a<br>SHA256: be98571ddd09dc0b9a155070db5ec62f748575de3ce361e298bb9d358b464091</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>192.9 MiB (202.3 MB) – 3,770,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a1d87e957284dd45672705f73e26f16<br>SHA1: 866151262ef141c2838f2421e7b16035c47a2560<br>SHA256: 97af76cb729c112c6f2785fd46b7eb71e51eae877841c79320b53fda6591ae22</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>194.7 MiB (204.1 MB) – 3,770,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 317bd3326b32f995b11e7c0c551ac529<br>SHA1: 8ebc3cdc7ab32d8068f259f3a2b85e46ecebb709<br>SHA256: 9f79a6a1738a496a057f5ed64416f423ea7d65c280cd5a523720f7c79463a33c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>245.3 MiB (257.2 MB) – 3,770,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b1932c3b288c78cf6c75a5cae147779<br>SHA1: b5d7173550b31055fbcc2ebab5c69302c1caaaa5<br>SHA256: 692bc15c56969b44b82282041771328bedf8580dea69f00f0ab6d86327ef4363</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>192.1 MiB (201.4 MB) – 3,770,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91254bdc185ee4c50a11ccd5b0e5806e<br>SHA1: 72c506dcfb1a131f34e499c5116720afbe197cca<br>SHA256: a98130a6520dd9bfd1301243903ad84ef6f62868b0984910862b74bb75f4e2d8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.2 MiB (246.7 MB) – 3,770,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c29aa5f29a4b17e106e7bf2417126d2d<br>SHA1: e1dd33e2c3d8e4ddd409348d9ff8111ce25ec634<br>SHA256: 2d70f7de47dee919866da53267edc0ede0201c651f06e34aa18820729d5db5c8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>197.9 MiB (207.5 MB) – 3,770,257 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7a882568e9a29d434768b519e405c7a<br>SHA1: b76626a9c166bd324bd9458d0817181044cd5db0<br>SHA256: 9cd7736cddea538d61f54e65f1b8d98822d97f6a5c8077b6d0afc55b3fa58242</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>198.4 MiB (208.1 MB) – 2,080,681 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d45dd0dd245eaffaa0762f69d927a5a<br>SHA1: 0bc60345c0d0f3aba6897f1d3f2585b386759a09<br>SHA256: ebb42629dc5785d85279bdc7530a2a00f10aa01b775d8ade5c36f78ba8c902d6</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>201.7 MiB (211.5 MB) – 2,080,681 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee85194875293479480f4a038457650e<br>SHA1: 9cb38ec76be7c19a7b0d00402ae8d193bf1f9230<br>SHA256: 9a62c88fe0f1e5d164ac940ba0f21e7a59430aadc5e10b121a0ac3b8c5d9ed14</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>195.9 MiB (205.4 MB) – 2,080,681 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3787e7a590cad26ee79a264074c3d5a<br>SHA1: 77e6afb53e672de56d820a826c7088bffb2b6960<br>SHA256: 90ccac7a52c68df84b11fffd534abebdaf67489d06c5b4823fd1dbff8aa9ac28</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.4 MiB (205.9 MB) – 2,080,681 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08a4be325e2584a7b6d6de86219cef88<br>SHA1: 68690b03b0d6faa9f2f01fd872bfe0a49312f54d<br>SHA256: da0d3449d4a92faf602cbcf146511665f7a0e2313eba9cfed0d81bf010566c51</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>218.5 MiB (229.1 MB) – 2,080,681 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 483e9bf75455fdf7ec249cb902180c75<br>SHA1: 3f0703a078f35f8bfb94eeb4ace3af0cf0584a29<br>SHA256: c5c1dcd306405a548be510aa331c454a83317ee2d92263f5ed0acf08c22294fe</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>195.7 MiB (205.2 MB) – 2,080,681 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b48ef946756273d39c41750dc6a7173<br>SHA1: 1dccee348e897b6ca6cacbcb2e0ff4f8819c5f0c<br>SHA256: 157073d39c3498a0cf61aa0fe508c8bed038253b63f39b51fc5fbf14a9cf2659</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>217.1 MiB (227.6 MB) – 2,080,681 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72ad270ef9665b809e0cf7ccbd3bb2bd<br>SHA1: 96f29f1f33171d31692341f273ebee472043bc53<br>SHA256: d9903b74f897a551cb0ed1f4d79627d41ff32a9435b26740bbd68b4beb0082ba</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>198.5 MiB (208.2 MB) – 2,080,681 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd9374085b5f4bc62a6a196a7e02973c<br>SHA1: e3b42d43c5d5561f6cce54db9ddd88d1991162e1<br>SHA256: 93c907b218037006a82b2ec3b0e6c3311b965f31a4725159bd59162faf15066f</pre></details></small> |


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
