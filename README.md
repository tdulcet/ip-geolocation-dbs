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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-02-20<br>IPv6: 2024-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.808MiB (5.041MB) – 240,688 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fad24a0762a5aa264e75c1fb3a40362c<br>SHA1: ee6e0bdad03e041d3431704aa65603c509b8d6c9<br>SHA256: 51d52a2365ec7d7022bd359169c3936e268f78943391db515add8cce2d327869</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.663MiB (5.938MB) – 86,065 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9c89e0b42751fc3f2aa55e29e3ef130<br>SHA1: 541f82f17f1563a5c36c946f58ea13bd32c5c995<br>SHA256: bf865c4c5de441b5101225a568c7d58df6c7118ec896ca2061ba75cf2c4b964c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-02-20<br>IPv6: 2024-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.191MiB (8.589MB) – 410,199 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1195ea7a51e02923c5a736a79062c186<br>SHA1: 30ef3375b03870346a8d21542aa96b124e81e3a2<br>SHA256: d5d84385a1244b00e690aa06897cd21a4e7589eadd91978ed32da522927d4a17</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.989MiB (7.329MB) – 106,326 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14eebc288e3010f0641b5043d87c33aa<br>SHA1: b269337a9706332618e0a2efa0e986c2405ffc0d<br>SHA256: a82118a7b05c7df7a1d35a9efa2c32f03b54dda6cd20704c2fbb51d6bc6e41b6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.83MiB (17.65MB) – 842,673 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55fd0eae19989df27dc5ea5c447a574f<br>SHA1: cecb5f5163e2abe659d48d1aaa5aaf47dee8e7ab<br>SHA256: 77cd15e53d0e12303f0b874f9f45d8d8487419ee19cf67b1ba51dde43fcfb845</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>53.70MiB (56.31MB) – 816,017 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40f5adcd824db3086d19e3c6cb6b13c2<br>SHA1: a0064cd68599a6905626cccc57a8dc0ce9133488<br>SHA256: 5abf6aa5879195476b673e1919dca660e83c4d059affa222618bc9e30bb9e44a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 322,238 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58dc67267f460ea3cf5cad59cd04fb2<br>SHA1: d7cd4a637354f5a5c457e96633e1f5c9cc5c059c<br>SHA256: 55313849f9b0eeefb503ca58aa485ebe95d325c7771a4b2e5e9def19ee8aa2f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.67MiB (19.57MB) – 283,667 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b73dc10990e7bef8c444f1cde6991f<br>SHA1: 07ae49b41bae3e257ad578c4bf31ee8040ccf1fa<br>SHA256: 7ea6211e834aaf328302ede30e6777fc4f71afb40ab1238cf0af2be151b5b248</pre></details></small> |
| | | Full Location | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>179.7MiB (188.5MB) – 3,143,531 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4796f68669fd62ff1776c3d247e13dff<br>SHA1: 8d63c70c0bd62e8829cfbd2dfba8d6b8e6c77fd0<br>SHA256: 04e5000cfd1d52386cf975f825886bb214085c10b75c2568efa51ce70fb6c3df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>291.6MiB (305.8MB) – 2,831,720 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 657b58a340f82d12479e96ce7f695a45<br>SHA1: 1b9c4719ee91d1e9da68e6f0dd1529e893bf9777<br>SHA256: fbe98efa467387f6ceb69603459abde1562d03903aa05b063edc68d9aa4e87d0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-02-20<br>IPv6: 2024-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.640MiB (4.865MB) – 232,256 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fec6f73486236c8d0d94598e079d6f<br>SHA1: 7f19645a2e7ae1f5579b6769363477a0ec58e5f6<br>SHA256: 7f7145aa700bc6d9b86d8e430377fb6751efd3a786e0455999aabe3401d275c5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-02-20<br>IPv6: 2024-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.9MiB (177.1MB) – 2,925,251 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434c9a2a5a5c869e663a7e206ad5962c<br>SHA1: f2e0c48f3ecc7d10f4697a8c5c698e1979b08714<br>SHA256: 8d5321147896799a07280f735aae4be97a74bdd31110778527dc8f4b77485f61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-02-16<br>IPv6: 2024-02-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.362MiB (9.817MB) – 468,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c0e2f9fa7051e43a489ae8ef8b30a2a<br>SHA1: 41540af7827853fdaa39f2338376169e18d5a26f<br>SHA256: 7ec868fb063641e1f1792187f8a112b11d82382755e5307ea819f3c033b60116</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.59MiB (19.50MB) – 282,541 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c84be43c1e8d107ffc87b3f826f87eaa<br>SHA1: 50dd11c8aab7dc409d6de3404b271519d2d0f70a<br>SHA256: f0dac142c485ee212938916dc81c7b75e0dfe05e2759a0102f3fa1a3a7b8e14e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-02-16<br>IPv6: 2024-02-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>159.4MiB (167.1MB) – 3,386,950 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83ff525ff4ce77adef5e08865fa4c660<br>SHA1: c0f2b502f82e895cfd63ad939f28e3d47a1e43ac<br>SHA256: 5052d5c330972b46850580a5ba68dc31957692029de5429d20ddb0d8a610c356</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.7MiB (194.7MB) – 3,386,950 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c21334fa7ab892930bfe8508f3a53dd3<br>SHA1: 05ff2cea137ad353362d0c24785e2537e248f055<br>SHA256: 6935b139b022d28301d75bc86bd2f4564fca11adfeb5a27e6bdfd2e5f3dbc375</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.6MiB (171.5MB) – 3,386,950 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2288dd2dd80ccdd06824de54547be8f0<br>SHA1: ae5b494b92f00dc79a7c1e5f789bcebb2919c512<br>SHA256: a550a23ec666dc4c027e6da2bd53cb89df3c53c0e2e5c6fc8957d360957bde56</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>170.0MiB (178.2MB) – 3,386,950 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6ffdfa2516615bcf9a8f07ae0e79fdd<br>SHA1: 84a230fa701bf4a59c58d007c6b1fc152a6c0f9c<br>SHA256: f37890a6bef925d49e32dfb04f46baf39ea57acb2b915d4cc3439c0b2a9a0661</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>198.5MiB (208.2MB) – 3,386,950 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a94959fda0ffaf1fbd350b37f96774d<br>SHA1: 6caefb6255187784ac9cfb232209026f7fb17090<br>SHA256: 42824dee63f621a7a2d88b515059196dac2f903260046a0ffdce1daf898a643e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>158.2MiB (165.8MB) – 3,386,950 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721de00ce7215e2473a1349e8ccf9d2b<br>SHA1: 79eec9581ad12cbc9179f7a8171eafd8d6279909<br>SHA256: 83dba24502b130ba473351ad5d8ed8192f380b2b0d24dc34624edea3cbd99c3c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>197.9MiB (207.5MB) – 3,386,950 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecf2c8d05985f184a2c983a4f960c75d<br>SHA1: 6c4d8024f7f06aef98aba04040aef24d6d95210e<br>SHA256: 3aeb8f3ac17369a2373fa972b9ae7fd9a37bd350cfd8256bb81115e503e396db</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>167.2MiB (175.4MB) – 3,386,950 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8aeed594a7191128a6b3e293f3f4d403<br>SHA1: 40c7aeb60c5d21dfea7b721a97e648f5b7a66bdb<br>SHA256: 6e95d900f029b02ca2584cafe8862a1304587675dfdf25f22883926e83e7249b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>106.6MiB (111.8MB) – 1,190,916 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b69db0da6c84205a7350f02e8db79fe6<br>SHA1: 36911ec43cbd78ba5460674a41eac94626f9f118<br>SHA256: 566cb875a93fae286e90f0c979477ac53937523340be1cd41b574f85d98c8f6b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>114.5MiB (120.0MB) – 1,190,916 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38dd98edc145b75734375c7a58658b08<br>SHA1: 9310d21936f8fc908e0f984ce38eaa38e673c627<br>SHA256: a0e6fcf134d3105487180208c6aa6cb233915a92696e8a14f3258ea9bbfdffd6</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>109.0MiB (114.3MB) – 1,190,916 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd9a0c43318b37aba3a3c25007036075<br>SHA1: 7ab801a5e896f4b69046d344f1983f5c8b9172a9<br>SHA256: 3cb6a11d6bbcd188c7302bd27436576dd24499b921e6b4e040d58f28374f09ef</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>109.8MiB (115.2MB) – 1,190,916 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c568a8b4d87dc9c310ce46034984cebf<br>SHA1: c7cbebecd0879ca6f1c392939eeebdcf36f6dc20<br>SHA256: 73768caee717e711b428d8cf6f143b093600034b6a48a70c367798e8ea229e34</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>118.1MiB (123.8MB) – 1,190,916 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9453165714943e68eedeb6d3272a4815<br>SHA1: c84a34f3f17f4dffa0876010ace87a3f383759df<br>SHA256: 08e31d529725dcec05d77db99e608742dacd84e36ff706a80fd91cbb3d331096</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>107.8MiB (113.0MB) – 1,190,916 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb0e5b9334de58aab92633f1e4da2e48<br>SHA1: e90df34f3e46a76cc41dd03a13dc265c8d9d5300<br>SHA256: 85da2cdc4a41b58d21c7e7dd3574f807f8dddbbbf92e76903782f4a2bc747f9d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>118.4MiB (124.2MB) – 1,190,916 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc65253006b299d5882796387630174c<br>SHA1: 5cfb763732fae3c81b415650264cd8ea8b7165dd<br>SHA256: b9252c77930e2b9f49fbcd39a80e0f93e1af79ed04c2f9cbbe968be1295621a4</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>110.7MiB (116.0MB) – 1,190,916 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6324921a504b77cda2f51c0dc7c81856<br>SHA1: 0b1f5eb433dfb99a90fa6ae377cf20936c89e829<br>SHA256: b9aee46993cd66331c29eda1b428938fdb9c4abd50501ea2b07522028dd244be</pre></details></small> |


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
