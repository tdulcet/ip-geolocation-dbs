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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-03-27<br>IPv6: 2024-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.818MiB (5.052MB) – 241,208 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 820a283e68b95ed4a6b53ebe57498dd5<br>SHA1: 4d550d9e20e6425eece3f22a1cd8f447b277cc7b<br>SHA256: c5a509a0e74c390f697bfea910c4d1f5fc1868be67a3ea1ac7edbbf2a0815be8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.083MiB (6.379MB) – 92,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d76aec304a8d19fa5ec83632252eea7<br>SHA1: 1eb172d670663fd9c3673a0d0724a58657d3f801<br>SHA256: 5de9ef5b6b13b4d5492f12db6f8c04cb5fdc486e31bdedb172dd8aadc5ed4d1a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-03-27<br>IPv6: 2024-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.212MiB (8.611MB) – 411,257 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42f5a485d05cfe6d78ccb6f6cb23ebee<br>SHA1: 6584e92023c5810d456d0ee835e71a7075709a21<br>SHA256: 4144ef211901943be219d943c7390d04c99ae5c4e95f908c0ba770ba0a233ba3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.076MiB (7.419MB) – 107,643 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31bbfde370ddf2176e0154efcb619556<br>SHA1: 7e7b96a0a157005ae87f7cda0294cc0c0725fd89<br>SHA256: 659f997e45810fbeefc41c6db48fd7aa17e93bb553f76990e8a0ab65cdc1dc26</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.93MiB (18.80MB) – 898,122 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba6b3c57263f5c1b3d5134f93d04ce5b<br>SHA1: 71831436824e341a71b582439e012c54cc25f0e1<br>SHA256: d2a818ccc31a7c727cb2098fce9f5d167f1f5a7aadf94acfea76ad7ce28d7d52</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>77.87MiB (81.65MB) – 1,183,365 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b351fb88e3f2bc003eb1fd27ff5c134<br>SHA1: a7036d2950c397f4468a30867922c763e3fd0935<br>SHA256: ac921334aee592e8e40dd21e7a9ebbf196cd5897658db7d2e6491126511d31f2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 322,326 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b232d78e18dacf266bba37244688a18f<br>SHA1: 2ea0bf2a68630d5c12c6fa1d18f2f3eb0845f297<br>SHA256: b9f2935f135d22119e5db5d8d8666980b07ac2e36359fd6dbdc9c26a8b3be2f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.03MB) – 275,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49241985f6153f5f100b60421257f25<br>SHA1: 51e0348aaa544a9b75aa17c9431f3745175c5c5f<br>SHA256: 3420806d6067a2579fe3eef92e4cd09b9b792cce9c418a3ca7f3c820f4edb887</pre></details></small> |
| | | Full Location | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,158,494 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd92465491c42b3844af48593793b1d0<br>SHA1: 53a3bac0d03e0e4bef95ad11b21c1a1e92eed9f8<br>SHA256: 6157eb8d8b93b5da65533893b6b1af8682e371476cd754957d56f3cfd1179aad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>307.8MiB (322.7MB) – 2,989,351 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a432fad1dde6398b8b6ee222abf32676<br>SHA1: 78d2ec063fa05a95bb17703a5111864cd91a5446<br>SHA256: 5974cc41b3872ea8fe373def59322db31b678ff8585a6e529b9737d648343c0d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-03-27<br>IPv6: 2024-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.826MiB (5.061MB) – 241,587 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53358947a90b798856b0f2491fbc6d2c<br>SHA1: 7c9c0c0ee1f075fe6d82ea2f7ca31f00a5b7ad18<br>SHA256: bf9da0021f243ed534ef8e2352a5fee71207c3b880a727cd5031b79c5c122185</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>16.63MiB (17.44MB) – 252,757 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05df7acc3edcfc49d6d0cc8e5b23185d<br>SHA1: de417cfa98cd08340a971a226b8075d8887c08b6<br>SHA256: e2904c3019400cf283bda389c8d7dc9f8c0b5dabc1bfd9dc40ea4326c79f404f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-03-27<br>IPv6: 2024-03-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.8MiB (179.1MB) – 2,959,758 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d837249426a59f38d52d9939db4c1a1e<br>SHA1: c71a37a88777bcc232ed0cec8b11f4b0b93ba955<br>SHA256: c25d6cf67e34fdd6f9b5042bffd4059449b156fc6b7bb6e3fd49ce1979642175</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>169.7MiB (178.0MB) – 1,642,006 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e91d25d35aa21837cbe8c01e725e1cb8<br>SHA1: b3aecd7e3f4493788fdc4c941a22f3f071cd5130<br>SHA256: fe72238b338f395cd55c98381ca41ebddfc893eb2bd92625551b9fe4d8d96a53</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-03-26<br>IPv6: 2024-03-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.642MiB (10.11MB) – 483,031 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c430975e3ca6750a7851cb388649921<br>SHA1: ac7fbbc5b239e3625f5e9d75040e7f845203df32<br>SHA256: f10979ef8b70d31b8194ddd2e9406407fcbb237e24ba0913d4fc911f7577b144</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.60MiB (19.50MB) – 282,675 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67e6b2df2b25ad1470f184570b75df6a<br>SHA1: a20aa3b2299e58c55ab9d9fd43b445f0094618e8<br>SHA256: d7d52092624239a23a71db583f2970b163acc96168f9114ec184cdba26cae4dd</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-03-26<br>IPv6: 2024-03-26 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>143.3MiB (150.2MB) – 2,876,363 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4218ae3db5d2b9824f7be30b20b6c386<br>SHA1: 43ba4c5e23bad3ac2c16791ab08df00fd4341e3e<br>SHA256: ac9088fc0083561dfeec465be1369c551880ce146c06cc42d58abc8cef6a9a31</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>156.0MiB (163.6MB) – 2,876,363 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a42e0885a47fa7b98e1d581cd706893d<br>SHA1: d78549923fd7def47ed6b89c83f297f5252c6352<br>SHA256: e771d7be7939fcac89e7be22f1beb163c212094633c9cd93256ad1ee3983ed60</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>142.9MiB (149.8MB) – 2,876,363 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8d506c58bc530397b2fbe0a35fa683c<br>SHA1: 90abee68519b38bb94abed0208893a4c0177d781<br>SHA256: e341e53d551f1ddf222989fa7b35c705b5427c5996ae82a818f643fb2e17b16d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>145.9MiB (153.0MB) – 2,876,363 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: baa9c18e438ba1c0130264bb06226de4<br>SHA1: 3a31727a5ec83864334db0b05cfaca9d6cb71309<br>SHA256: df5504ddcbe20347bb536b5d94de11d166a24e214d29fc943b5fa24d24a8eccc</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>178.4MiB (187.0MB) – 2,876,363 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ef60973c00ec30030b8bf5d0a554e67<br>SHA1: a4ce37b850cce79b4e856233bd3ef453243bfc7e<br>SHA256: ee31c0eb7f2e60e2b02a84c0e36dce1fd10f9c740daad07f76051302bbadb201</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>141.6MiB (148.5MB) – 2,876,363 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f55d93bd33fc787a2be8f489ea0a45ba<br>SHA1: 16d03ceffe2e7fac40295ac15bb99342bdf0f680<br>SHA256: 1436b6fc0e175120a661527a8740c301b0fcf6239bbe76395ea7f23a4cbe342e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>175.1MiB (183.6MB) – 2,876,363 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37fb72ea8259dacf2329e50bba9d3b17<br>SHA1: 1ebb514636125e1f8778c5b72160cf46ed7cc3d5<br>SHA256: daa4d58c5553a4b4089975e093d97bb7f289b07cf3d553f3a2ed420b520b69d5</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>146.6MiB (153.7MB) – 2,876,363 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a5adadbc8b62cd17ead17459e5cc49e<br>SHA1: 0f837a3c2959fee0db2f289e75740e1a9772b46a<br>SHA256: e87b40fbe67fbf411c656f60ce75651c87ca6a35c43bc71f861156de7f677895</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>112.6MiB (118.0MB) – 1,216,416 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0520b20bf889a166b824c36c2bd78cbf<br>SHA1: e7e38fce6c289e08c745287082f675fa2618b969<br>SHA256: 2543168de29d274359879fceec3799876e347504dc6e17fd469035109b503e07</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>117.0MiB (122.7MB) – 1,216,416 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c421f59d67a5696de8d073e3b9a2eb26<br>SHA1: 4eb40e5f553f7b69901165cadd20304510f6c26c<br>SHA256: 140ea15244ed716eb11a6c1a3d4e194e8f19183376d04273626cc06856967aec</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.6MiB (118.1MB) – 1,216,416 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 13184767ce32a8c648aad2fc988e7a2b<br>SHA1: 61337c53db568a3f252fc67b13c2c66ead7cecc8<br>SHA256: 9b70d1db62791069ea07c673a8ac97d2dd047a264d5d9a79b04f17fb7bc679b1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>113.2MiB (118.7MB) – 1,216,416 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 341277f3ef4847add51a66f7d0bb7161<br>SHA1: b9c650fd7c54c47de0ec862789b37736c475a0e9<br>SHA256: 1ad2ef9597219c7d1a2f6ca8b3244cc31c9b7434ed9eaefba047552f81b465e5</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>124.1MiB (130.1MB) – 1,216,416 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 584c9c34919044641130dda653375ff3<br>SHA1: ffa88d680b03f60b0435f109d69eca292d090ee4<br>SHA256: c0d1d5c5a7368d68ff547071fcd311780580ddc2e016da468b5575e26dc69945</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>112.4MiB (117.9MB) – 1,216,416 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4eef91eccb4d353caab1e2612857b29<br>SHA1: 3659bd26fad808f46f109d6dbd4d2cca928a8d1a<br>SHA256: 4bcfe9af8f39c4027fdb65aaa2eca07759251c25bcc53a23bf53ed14e5ad8794</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>123.6MiB (129.6MB) – 1,216,416 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5db6a52f614723ab77a401ce8a0f303<br>SHA1: f8a2eba7fa2c2c72b6203de590091f82d6929880<br>SHA256: e1a495f42c091f0c14fdbeff2a5dd3650dd7a35d5b73569ffcd904e86e0e2f57</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>114.6MiB (120.2MB) – 1,216,416 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06b47c93b47ee60f86b0eba130141691<br>SHA1: 91db668131f1df49aa7d259162c6e1dadf2d04d3<br>SHA256: fe8cb4ddf077371738b019ba62833d50d72c1dfa6dfcd77819b7e8a1d3f6c8b7</pre></details></small> |


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
