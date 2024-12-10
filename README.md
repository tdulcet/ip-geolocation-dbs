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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-12-10<br>IPv6: 2024-12-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.899MiB (6.185MB) – 295,360 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e214a7ed1b1c6432d61f753ed464a2ff<br>SHA1: fe3e4a4f0005f716fdbf761db63ba345aa9e4cc9<br>SHA256: 0d14da3d9f0222b28a9fcb9d39803ac3d5fae9327ad88d6ec40ce641e4cf0e76</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.52MiB (12.08MB) – 175,026 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75f47e4230257d64633b636167b49da1<br>SHA1: 4fd4f34b358fa40ed9976b01ff87bc3fcb527810<br>SHA256: 2eba40d9bf15a366b59f2bfc6ca2ca178f99e56234058ea1228ba2d9d5a7357d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-12-10<br>IPv6: 2024-12-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.251MiB (8.652MB) – 413,191 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b618ab8cf8cbd237f125979994d293fb<br>SHA1: ef2fbe2d38b287c704826fb032c648e2d6d60749<br>SHA256: 4d9c38ef267f6804a9772062e6113182013df27a753cea31013458f6cb8e342f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.940MiB (7.278MB) – 105,586 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 339b0da389052a273a9352f7ae64c45b<br>SHA1: 13b35762a919f6ba69a03f3cdf16b9045fe22450<br>SHA256: 5c3b9aac4aede0ae0a8cd89bee1ab4a8ac853be0f81a4386d8e8231951a26caf</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-12-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.71MiB (18.57MB) – 886,077 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cae3138ce676a7c9e5bcde4739e67497<br>SHA1: 067b994535cb75aaacb0f58078de3b98b8021f38<br>SHA256: 43742a0c0fd8b07ea04c8f782072b88d2f59905b93c7494829a4667d31484945</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>86.06MiB (90.24MB) – 1,307,880 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81e03d1590bb50fc0a988e97f2836e8c<br>SHA1: cc64e675d05681d4f1e3b823e636ada5b74ca2da<br>SHA256: 83f832165ac187ab21b8a7dac8fe9fd0f823ea023379718e65de71a467be601c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.156MiB (7.503MB) – 359,168 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4fa1848a017a51ce167e1b45ef180e0<br>SHA1: d025902fca69db441cbc83871eb99ffd4b92c75e<br>SHA256: f02df1b7ee71bf749e1e43de462a3f6c365d9ed6e72e1d5c6faa86f25acb568c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.24MiB (17.03MB) – 246,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fee62599a38c614b43a277a08de845d7<br>SHA1: f6f5eddc6f61250f0fef53e42d76288b85a9971b<br>SHA256: 258dacce2a418e7297db10bd484df83410a61ac130bc1a5820b6fb0c0c58cb70</pre></details></small> |
| | | Full Location | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.6MiB (199.9MB) – 3,333,541 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f97a8dfa3d2efa2169aa49e5067082d<br>SHA1: 69f6046d5bebaecbd09f512a07ad0279a8bad58f<br>SHA256: 193177f00477af08b776744f0aa5ea8ffe08fe54bbe785733206c3c6f5ea0b02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>381.5MiB (400.0MB) – 3,700,914 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60c57063e8597965c85a15738ce2271e<br>SHA1: e6cfa1c20dff9df4b9dedd101304ed4939827a3f<br>SHA256: f48cf620380d7f79c9d8d05702be678101a193a90ef351c28ff300bad2cb1942</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-12-10<br>IPv6: 2024-12-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.918MiB (5.157MB) – 246,132 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ef7e16cf2b6bbbd422ba2a934ef7df<br>SHA1: e1f77a047f5dba3e4ae075464e3761268e84b7fd<br>SHA256: 8dcac1f1779ff26fe9a26934fc72b4c423e9a2f1252d99e1436206cc2bf9f63c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.70MiB (19.61MB) – 284,192 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dce3866a2d21db59b0445d7ab2b5439f<br>SHA1: 62737a727dab8fc70aa7a79a6b203bedd659ee5b<br>SHA256: 2bc4972b559cd83a749cdf69acfcc9f7e1e9b63db44e48dc0e635dc639b29822</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-12-10<br>IPv6: 2024-12-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>167.6MiB (175.8MB) – 2,906,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1918be02cf5e40016993945dcdf9fe2<br>SHA1: 26d9a8404ce0b330647e6b9dec8e0dc1f37c9773<br>SHA256: beead4d706ffee13660a84a3a4fa8d161b26172c66d7d783002d7e5e9a446e97</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>223.8MiB (234.6MB) – 2,165,543 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58aa852f4471f22d59a91349fedddaa7<br>SHA1: 58ed488a65f8f18956e7b32e6e9c4c95283bd843<br>SHA256: eff43d3a7756d1032e8d1b53d8fc159639852e5511ede4f1a0b4456657557bb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-12-06<br>IPv6: 2024-12-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.03MiB (10.52MB) – 502,509 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b38b0e51376e3c05ef990aea9c4f728<br>SHA1: 868c2b859c1393173ca71473b4a701727cc60497<br>SHA256: 2fb8a8d9e41f2aad7555df93c52738e078b09fe66c8e124221321cd821ec4ebf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.58MiB (34.16MB) – 495,080 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea0df056d5e24ec3a4730056f6e85ba9<br>SHA1: 24f0ec6fdf334da15990554f8dddf868638ea1a2<br>SHA256: a80c20cbf89f6cbc8aa95a2a07ca6c4bb615af5f7633023f6d8d510705c06948</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-12-06<br>IPv6: 2024-12-06 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>164.2MiB (172.2MB) – 3,245,307 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66d646f1e4eea27cc2769199609e2253<br>SHA1: 480f62eeab9bd802288fb23708beafa6b019615c<br>SHA256: 83027301407ca172ce464da925148708d06b7a99e67dc3988238c872266a633d</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>174.7MiB (183.2MB) – 3,245,307 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9dd933ca7a30d9573622a1640b399ed1<br>SHA1: 17211ad135798510ba7ee9256f7aba363f7e1c8a<br>SHA256: ed5d4f971a12faf9d488b884797894df16bd51dc760e0cfd7ae79f5ecadbd8ec</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.2MiB (171.1MB) – 3,245,307 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7bf14f05b29454eb12f3ce87082b9ff<br>SHA1: 3828744e6b73e13cf751fd46c8ca94a7ae170f69<br>SHA256: 03acc15c28c7a94852203a4a77abe866449d40f2725988befbfe406947ef68e2</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>165.6MiB (173.6MB) – 3,245,307 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e62f9af4879e272bb2bf881e4106e82<br>SHA1: c8efbb794e1948326335c031f6509217b82ade04<br>SHA256: 79aceb84ce52b64aed8c518a7e842396fc4ccb25f8388179feca5e14f5a3e926</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>208.2MiB (218.3MB) – 3,245,307 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bdad68fa98250b53b5eeb2e87c45b801<br>SHA1: d4e79934d58e30ef529685d88f54438ff73b9937<br>SHA256: 5e91d921a3204c38d1b8faf02397d7e21c361fd09a683d9754652229f544d380</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>163.2MiB (171.2MB) – 3,245,307 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93530cdcac86cc4fdf3f8819aa3ada8e<br>SHA1: 3530dcd5de83c8b788714a6becc8c7b63c7ab2b9<br>SHA256: 5bb9ad3bc803f1cbc98fa2ae3180a96f3a2404808ad2f9783369c2974a3ab237</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>202.3MiB (212.1MB) – 3,245,307 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec4513a399e276a5a213041d203b9716<br>SHA1: 345edf231c666a7ec1511d218328625d600603b9<br>SHA256: d664eb9dccab8dfe5f5039a49c91f59f21bd4575e54cd88edee6e7e78cb94f17</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.3MiB (178.6MB) – 3,245,307 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cdf7f16cb8b3f8d18931be00c811b38<br>SHA1: 5174ad15dd38b18f705eed6fb5e450d96d4e96e9<br>SHA256: 68ea9d98aa69deca70d06fd88493f2fdb72f981e96f9544701ea2e54ba0c89ce</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>152.3MiB (159.7MB) – 1,630,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1dddf77c077027e481d9619ef5e4b9c1<br>SHA1: af10f9bd37707714a615f24ff13456fb8db295c1<br>SHA256: 5d2c4261435d8a253b840a01679d9e1fefc8d8c27f3144363403f13b6137ed1a</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>155.4MiB (163.0MB) – 1,630,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c5ef9a39420e78bccc57a76867144cf<br>SHA1: 3225629d252f429140bfb4129bd286c331884369<br>SHA256: d35eb47d25b3c54e0a4b3f2132281a99e69048d26734c03d091e2e3825f2347c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>150.6MiB (157.9MB) – 1,630,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f93a3a5113aee63b9fab667c22297e83<br>SHA1: c4a98044708791fae17b0fdf2d161207163bea8e<br>SHA256: 694df5c6e746c4e4b570cded6164329c12caf42832563df2a735b73582340da6</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>150.7MiB (158.0MB) – 1,630,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c001d4d5c607f3abb0e43d0a02fc7644<br>SHA1: 2149b8022713dbb768687fd2cd61fa34d0b36e7c<br>SHA256: b58aa786c2557b4ea9ae01949dbc04c233f40e5d6bbb6c2d65ffdd69b9b42db5</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>165.1MiB (173.1MB) – 1,630,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 955f198c48edcf4e77f2a9019e20106c<br>SHA1: 5c99026731915c41741710e5f816b7b2a8e0b802<br>SHA256: cf8887fb0bd85cdbbce03de1b299622fe891b2650d52e4ee2a82666261cd85ef</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>150.4MiB (157.7MB) – 1,630,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04b0c5ef1de8d3beba19aad3aff45ece<br>SHA1: f1333abbdef4b36f6bd673e4a836e9e3b1579d1b<br>SHA256: b5754c0b71b2d8bef1a815d8b74f75fbed20d2aa4de461103f32b124f15d50f6</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>166.5MiB (174.6MB) – 1,630,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51c0a6338f5a5082b0516c8e270d5800<br>SHA1: a068ed6800355d3e95c55162c11a5dbfc84618ce<br>SHA256: 6ca122f86955059682935476a6acc18ca36926eea66a1f8d92f9816f63ec5437</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>153.7MiB (161.2MB) – 1,630,571 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be9982a2b6060aff073dcf7a16b9eaae<br>SHA1: d6ab797b2d545b2ddc0e38e4873559fc466873c2<br>SHA256: f03bd9ee4073cc177ca4db65857a6d9df132c6f964a67b021800c194e1cd32c5</pre></details></small> |


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
