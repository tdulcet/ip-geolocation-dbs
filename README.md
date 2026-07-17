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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-07-16<br>IPv6: 2026-07-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.398 MiB (5.660 MB) – 270,142 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a6c098a90a51e383a5a3621635cebc0<br>SHA1: debf2b95100e5f61f2d56272a3bf1744a62d1f44<br>SHA256: 59cd839663656e33b311fd036ec4154548d4323ab18e23eefdd7f5ef17e78f7a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.79 MiB (17.61 MB) – 255,157 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1f6055bdd35df10bb0f36fc6faafee2<br>SHA1: 8b50d9c1dd3a23f50c77af38ca71d148a8d92921<br>SHA256: ff448c093609333b8cfb2ca0fa821f89122371ceb307e0e03c242e71c47d73b8</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-07-17<br>IPv6: 2026-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.019 MiB (9.457 MB) – 451,577 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0b682f324ba9815f4157f7b53c2cd5f<br>SHA1: f37d41ff862128cc9b864b771bc437700bddc56b<br>SHA256: 8c995f7e41b4488ce0889295441edd94b1760a0f3b75d3f210cd27c4fedb9e5f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.942 MiB (8.328 MB) – 120,807 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7bc126558bb0d50a873e6d0ac8081c99<br>SHA1: ed17c2670f1d8a3a3dd6cc40fd7e50b86ef046cc<br>SHA256: d991388a4bd19026843737fd3ea9cf11249c472a7035c1d3217a9d40d22aa254</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.25 MiB (12.84 MB) – 613,138 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf3068ed91881cb7326bc57b8ab98ae5<br>SHA1: be2165d8943664960435219278f7b536d28aa99c<br>SHA256: da6ecb6cdafc629404f70fdd80ca09f3f3ad3bc33b1e1ff9a448fe9eb37dbeea</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>41.60 MiB (43.62 MB) – 632,244 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2222ba66330d0ace8ab94fc7fc6e6c7<br>SHA1: 5aed7f87d31595f41cfc841c27f815b4f42c13a0<br>SHA256: ff42a9f2f9a850024235eef87ffa2ed0907361e043fa2298768de4431d36b0e6</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.078 MiB (7.422 MB) – 354,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ec835290735187164b1f2f622ad9c0<br>SHA1: 10464ef5eb489f4745096b1c71046b06409244b5<br>SHA256: 6bc4af63c1e15b4d99d5b9dd9cddeb67bbf2eafc2529ba5d9ec4525e0fe7964c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.51 MiB (23.60 MB) – 342,046 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569d0c6b66a745289f0e152318090f38<br>SHA1: baf1ef75355d41d9bc4380f97ed3b085db479655<br>SHA256: 8940a06c7f9a27f129048c5a7a0b1579b368020d88f2d2efe0fc813b6d2f97e4</pre></details></small> |
| | | Full Location | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.3 MiB (219.4 MB) – 3,666,805 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b729ab459cc2b765b3b4ea035f481b<br>SHA1: 1496af12b72ee784e304cd84eb7335c826bc3906<br>SHA256: 69fc5ebf5414a7a939fc25a35f3128451cf340211ae51ab9f82d53a331d8ca03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.3 MiB (473.3 MB) – 4,386,528 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f197b2ebcfed77f9adc3310fc7b6020<br>SHA1: 24b1454a40fdda39f37fa9367a6a6a5a88d3be33<br>SHA256: 0160ad6b5bca3517eb65f79d6db1f9e373eeb34cfccbf189a588bb330d17af06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.670 MiB (5.946 MB) – 283,812 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96cb0452e66db1c3a35242fa031ebe0f<br>SHA1: 28fae5a412332f0cedc711132a0dd6f337488ec4<br>SHA256: 2785f482dbf1f2dcb1bd3a9f253c708b1fa5f86773908ef7a2f2bb16c0dd1ff4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.24 MiB (23.32 MB) – 337,921 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1683effffd067b4fddf82095f002903<br>SHA1: 82f6a3b239649f9e8af05d58b628eeed874ad7cd<br>SHA256: a51cfe2b60d111ec234510abdd73583f12186f7fc35e3decd80fd4ef4b5ea654</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1 MiB (178.4 MB) – 2,944,788 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52717d3cc345c65ab5cb86167d9b2112<br>SHA1: 0ad1bd8bf0bdf711f51a9a37bb75090cbf4ffc84<br>SHA256: c92293057f12c2c364411c35a02de2cb229e7a21791a1bfd25cab2ba6beac1cc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>298.9 MiB (313.4 MB) – 2,896,639 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23b3d9e4addd1683ed707d17a98a0e22<br>SHA1: 572b0633e6453018a04db4c06504726ffcbeadba<br>SHA256: ba14acc8e2fc9ac380640ba99de27ab073d603598996f6737853e5a1ca4a8a13</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.26 MiB (11.81 MB) – 563,730 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f96f9361790b2caf5185ba5a869dad3d<br>SHA1: 27c3f98c90c3d628794925a265100c22fb401f16<br>SHA256: 178e7c6272fc5bd92b3f38b1a1c444d23cd8fad7dbf54db030d2827ac8866e06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>36.71 MiB (38.49 MB) – 557,898 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a205ea3bf6408a0424aab0c5a7054830<br>SHA1: 7c394936905cfc8e4d153398b7d1cc3008435b63<br>SHA256: 047902c0d9de5540213330c591df133955b8c83510bd681b112b9a2f4c936bf5</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>192.9 MiB (202.3 MB) – 3,755,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c87ed4f0a48c8990a346e0a1ec56fd38<br>SHA1: 69d196f0a945b524763dfc44e56d31bf45c67034<br>SHA256: 3232f756e1b86dfb89e1a9a1c83898318a9349f289f890512fe02b10c77f6f96</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>201.9 MiB (211.7 MB) – 3,755,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a77469d67169daf40ac2aff1fa887831<br>SHA1: 9729a82c1ac8d103a2cc330f790e84c9c5b2e0b7<br>SHA256: 68849871adab47f304fdd0bfbae2caad2401eca297bd45559db2478b52880d3d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>192.1 MiB (201.4 MB) – 3,755,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53c014f6388ea14c100e259811cb9ce9<br>SHA1: 644963dd99afa0870aaf861e97bdc6956aff7f83<br>SHA256: 6431c6c033dcc4f2a8ac90036d867998230be5fe74924352c33d6aa9ac639a44</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>193.8 MiB (203.2 MB) – 3,755,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e01bfd569181c78da85775e15d86de68<br>SHA1: c302f248c74c561b53cccb6a4e1056f246d5f0b9<br>SHA256: 8fe10e942397ef13f15b9cbfd6e015712419b2722e78809c19cefea3fb52f507</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.3 MiB (256.2 MB) – 3,755,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08a2a6979e36beed1df6306ef5e01b6d<br>SHA1: 368a4373c0d200e37f0aa407fb62560274daf8c1<br>SHA256: e0f6c70fcb385772ce1543631c243cfcb7dc9748881bde4343e07e0e82977e29</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.3 MiB (200.6 MB) – 3,755,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c918b6b8b2045f91667d6acb1294bbc<br>SHA1: 607c46bb9027c49a26c0b6fb1b59508deea907b4<br>SHA256: 9cab5e6e9fa7a208398b9a2df9325db73f63fe7139d748e7c6a1c360cfe0ec61</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.3 MiB (245.7 MB) – 3,755,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27067f1f2f178a57f8480a1f6d6786ed<br>SHA1: 5456b05c207ce1344afc0bff5ec83082f47049b6<br>SHA256: 386a8e5f28db057fe9d82f9521284803baffb5c1dd1e8d45395473418927de8f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>197.1 MiB (206.7 MB) – 3,755,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6ce3bf469d35f85823d726baa5dec29<br>SHA1: 1224e9df09e26ae5ee86463f91b7f1f7af0c3fd1<br>SHA256: 0172fadc07280ae9074ebbc5422cb456fa4eac16851bb45f5433e5d8432987ac</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>197.2 MiB (206.8 MB) – 2,066,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0710fcf4fb91999e6bcdaf3ceb58dd9<br>SHA1: b7912a10f3f5dbfc9882fb723f532d328408f1ec<br>SHA256: cf67903908b7b58a9497260662cb04a5bc0e1f43a81a2e2fd7c7b856ad9ae647</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>200.3 MiB (210.1 MB) – 2,066,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0be4e8010e9291ea0806e15840348bac<br>SHA1: 9f527cdf287386d7b005156f9c8fa582f4d00db5<br>SHA256: 9eb0ebfd1eadbfe9b0d9df6ab21fed100b7b04f79534781033012b2b7765d64d</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>194.6 MiB (204.1 MB) – 2,066,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4cde428255d22edcbc14be8aec07e68<br>SHA1: 25dc06931e0a7a4e1f332874b4e16da2d2ffa470<br>SHA256: 3ad46857a4f77bb35f2447b8df5dc2f67e170c32e638ae37a773737012b1eefd</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>195.1 MiB (204.6 MB) – 2,066,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8dee0db5e32ceb0a5f1ca5382b73559<br>SHA1: a4c87471d463c5b6af690f96d751595817ab8870<br>SHA256: b12e11fb15d8f9a800b343ddac58dbf0ce7c6245923dc3a9efe6eb60a480e54c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>217.2 MiB (227.7 MB) – 2,066,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 418f308a842738f15518ee1cd1d10970<br>SHA1: f2209a598f5806e73ba60ca3b874d904d8dd93f5<br>SHA256: 96eb7f1f351840246f8793f5d50470b03c615a74639b84b9ac1b90a0f4d28130</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>194.4 MiB (203.9 MB) – 2,066,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0141e0fb57b06cc7d00ef2a9a7ca71ee<br>SHA1: 2b6f3fcd84a2bbf94a77c43c9bb5d7b2cd73e638<br>SHA256: e257274ebce3ceba3332e8ac9b621295953139c01c3116de2e776d241cc16039</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>215.5 MiB (226.0 MB) – 2,066,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c5dc5f4f84344f17114b512768e3561<br>SHA1: 7442281506c072e031d64c091595ce3a6a3b4af4<br>SHA256: f4274987b631d28c2a16f070272c97c0c6aa4e3a1e52aaff0e87e87b327707db</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>197.1 MiB (206.7 MB) – 2,066,350 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb16508465096114313190ad63361965<br>SHA1: 10168811319059ae36c18f26159beab4470b1029<br>SHA256: bdf9fa896100bb10a8ecb8c186587864f75ca328b792ddd00e90b5e658bff0b2</pre></details></small> |


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
