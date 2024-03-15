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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-03-15<br>IPv6: 2024-03-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.812MiB (5.045MB) – 240,886 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5286d7bd04942e5d263d03dd3ecad45<br>SHA1: 744f508e096d346b01a1820450b5f74369112ffa<br>SHA256: 89404cf798a1d7dd791a2650c05a362dbb57f0d4635098338782edeef373678c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.026MiB (6.318MB) – 91,570 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d353adfc25aef9ec16b270225d6cda72<br>SHA1: 616e5784e61a51c58edbca5fce90d2ad722bd480<br>SHA256: 68c09ae8a24a83d82e47980354724269d6b41621169564658964134d2a0e31db</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-03-15<br>IPv6: 2024-03-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.208MiB (8.607MB) – 411,048 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11cc34ca0870d7d7e1a965118675cd19<br>SHA1: 3c2f56d4dce7e5bace494c29663d0072c535fd89<br>SHA256: 2394f3e5a95d0a1faea2fe66033d84f5c67fed6d03125ed4e6f10b8c95bc0863</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.087MiB (7.431MB) – 107,816 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 042cf3f396b0eb14581e1bd5fee5a33c<br>SHA1: b0cbac9f7d23f25ab735fce141f6e135b359a0be<br>SHA256: 0fc8227b894a69b54ffbc36abbac9185868bd5b24edb4cf5f0a749e67b8fd557</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-03-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.62MiB (18.47MB) – 881,930 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7644b024b1bd543e68d37200cfa4cd0<br>SHA1: a3c1579a4a427af3049f019805096a01d3b5e984<br>SHA256: a8cec31b092702c1fbbda7b5a1ca9635d8cd6e77eb457974090db146ceff2108</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.14MiB (77.75MB) – 1,126,761 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4e565722128ddfd424d0978cf2a0ad3<br>SHA1: dcd4a3941b8a2470bef0202bd6f8f561a625756a<br>SHA256: 143f293755ced2bf18fffcb37f413a5f536667b60b57d806f537ab4662203051</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 322,326 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b232d78e18dacf266bba37244688a18f<br>SHA1: 2ea0bf2a68630d5c12c6fa1d18f2f3eb0845f297<br>SHA256: b9f2935f135d22119e5db5d8d8666980b07ac2e36359fd6dbdc9c26a8b3be2f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.03MB) – 275,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49241985f6153f5f100b60421257f25<br>SHA1: 51e0348aaa544a9b75aa17c9431f3745175c5c5f<br>SHA256: 3420806d6067a2579fe3eef92e4cd09b9b792cce9c418a3ca7f3c820f4edb887</pre></details></small> |
| | | Full Location | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,158,494 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd92465491c42b3844af48593793b1d0<br>SHA1: 53a3bac0d03e0e4bef95ad11b21c1a1e92eed9f8<br>SHA256: 6157eb8d8b93b5da65533893b6b1af8682e371476cd754957d56f3cfd1179aad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>307.8MiB (322.7MB) – 2,989,351 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a432fad1dde6398b8b6ee222abf32676<br>SHA1: 78d2ec063fa05a95bb17703a5111864cd91a5446<br>SHA256: 5974cc41b3872ea8fe373def59322db31b678ff8585a6e529b9737d648343c0d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-03-15<br>IPv6: 2024-03-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.826MiB (5.061MB) – 241,587 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53358947a90b798856b0f2491fbc6d2c<br>SHA1: 7c9c0c0ee1f075fe6d82ea2f7ca31f00a5b7ad18<br>SHA256: bf9da0021f243ed534ef8e2352a5fee71207c3b880a727cd5031b79c5c122185</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>16.63MiB (17.44MB) – 252,757 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05df7acc3edcfc49d6d0cc8e5b23185d<br>SHA1: de417cfa98cd08340a971a226b8075d8887c08b6<br>SHA256: e2904c3019400cf283bda389c8d7dc9f8c0b5dabc1bfd9dc40ea4326c79f404f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-03-15<br>IPv6: 2024-03-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.8MiB (179.1MB) – 2,959,758 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d837249426a59f38d52d9939db4c1a1e<br>SHA1: c71a37a88777bcc232ed0cec8b11f4b0b93ba955<br>SHA256: c25d6cf67e34fdd6f9b5042bffd4059449b156fc6b7bb6e3fd49ce1979642175</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>169.7MiB (178.0MB) – 1,642,006 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e91d25d35aa21837cbe8c01e725e1cb8<br>SHA1: b3aecd7e3f4493788fdc4c941a22f3f071cd5130<br>SHA256: fe72238b338f395cd55c98381ca41ebddfc893eb2bd92625551b9fe4d8d96a53</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-03-12<br>IPv6: 2024-03-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.584MiB (10.05MB) – 480,112 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ae932e4c7d909c0b0d331e33fdcea96<br>SHA1: 20736b48476f7b95a5503536ac72875d07f91cb3<br>SHA256: 26a87632fe19ea16cc695e5df04b7914563405704e9ee40432fcf797e2b40734</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.00MiB (19.92MB) – 288,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8081bf9032dc946b1b8ac60fc04e7e75<br>SHA1: 2e56b1c07b0afeacae7e3f11289710985a583ffe<br>SHA256: e79e6b638ecc0cb8b1035a66008608a59ad7e10543a92608faa375b8bbedf401</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-03-12<br>IPv6: 2024-03-12 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>134.5MiB (141.1MB) – 2,872,492 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b5ac5523e3d9a58119bda5e095bc63e<br>SHA1: 42a2c7772ad353af2131f4b357f858fe8e475fb3<br>SHA256: 35560df76956d924388aabaafd73653638db57b320f09196cb701a0fdb7422ee</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>155.9MiB (163.4MB) – 2,872,492 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b52c0982072e9af8f4169715b2e95e91<br>SHA1: 262f4388aa91d3f86e6d2112eb6a580829590f25<br>SHA256: 929c422ad96f6acd77f1d0f7400da3c5aab36501b6f0c5893a583f1c6236b233</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>138.3MiB (145.0MB) – 2,872,492 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96598337babd93cbd7a0b0ae4891ced6<br>SHA1: e074228d0b87f6781a8530905ce7a136eb1f3952<br>SHA256: b4efaf5e8e4443cee0dff26f2960fb80c66b767e3db449a172c931d3a81c82c1</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>143.5MiB (150.4MB) – 2,872,492 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc8bfc685bff37c1374f669d7d483dd2<br>SHA1: 035007e7c4aa64c93dba99f5fd49fd38b0e761ea<br>SHA256: 94dedd07d38e600590bace9a159bf318a2bca108d0c1db0d003f89331ed6d161</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>167.8MiB (175.9MB) – 2,872,492 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 619012011de86f272b7cc09e0ca34d04<br>SHA1: 92af0328bce27368bdfd791f591522da4d64e8eb<br>SHA256: 20d3a78368653c4b23e757702e964e8116fa8f6302d8da36839fb61234319d77</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>134.2MiB (140.7MB) – 2,872,492 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64469eef704e478608004a9ec396ab17<br>SHA1: dc2a2c9fef07774f54080ff7568ba596e35718c1<br>SHA256: a80317291aace45e4198215b951c5665c1ff4717f6adc40d904c6e044722b5e0</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>167.2MiB (175.3MB) – 2,872,492 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 425b797c1e589300353052c6a3245e82<br>SHA1: abdb0a6ce4dc18d911efc4ff5a724e7d12967a26<br>SHA256: 4e807c09edc26c2536559db1636d9223031fc2e446e8627e1702b74aa272d768</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>141.3MiB (148.2MB) – 2,872,492 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae26916f75ad7428e0ff5d665d162530<br>SHA1: 08ef32861254a728452c08459632242e50f861e8<br>SHA256: 28cd90e57bea61f1597b5f06d8a15a9bca5f85ef925b493a6875302b3679e014</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>108.0MiB (113.3MB) – 1,205,384 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d1a671323402ea783e554cc1b9fd511<br>SHA1: fd191e72fbabff9c098074d37f948d0640156778<br>SHA256: 0163fe07b5c7d889e09f0cfe4fa942567e2021792364d03d4412e56fe168a04c</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>115.8MiB (121.5MB) – 1,205,384 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd7826dd50127ab6abe03c54fd156cef<br>SHA1: 24cc4c82dc8df1da868e6d2e3294c2316509e030<br>SHA256: 9c21dcb659b1103b98461cfa3a690dceb459418470fefcd8bc6eaffebc378142</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>110.2MiB (115.6MB) – 1,205,384 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cc68091be33f635d9a51d65c63545d6<br>SHA1: 14cb6142f0cea0c4d9a8eb2f7b324f40a9e8122a<br>SHA256: a00099f617bba4e9f0314189bc2c8c65e27f455eeba7aed3ffa4d6f7a9c99a5c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>111.3MiB (116.7MB) – 1,205,384 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 397d92cbf9a82f0b3ad9cb356895211b<br>SHA1: d1100b48ce3deeae3237e7716d57d63992fb56eb<br>SHA256: 079254c938e69af63b16868fece48ad06f470c16d062d87906e029736df688db</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>119.4MiB (125.2MB) – 1,205,384 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ace989667125d6df13899ed0917b1f8c<br>SHA1: ed62be1a4d175734bda0426ef8ee4b2a27161250<br>SHA256: b6bc68fcaa1a5a4acf8965e83437d1a4478fcb39f78a5cb3888b53330e0fb378</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>109.2MiB (114.5MB) – 1,205,384 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cedf6ef0a141b3eff3a095fa5125fd81<br>SHA1: d9bf7847684d794ad8603c294f8fbbfc37fe3aa9<br>SHA256: 6dc4da656b8908741f27bfcbd1f23454ea2a736b764b7378885eaf459e6b3bd6</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>119.7MiB (125.5MB) – 1,205,384 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3c7de415e8d63543c34608f738fdc1d<br>SHA1: 19949dcbbc4c59f9e1d340fb4855cd293ec9f9eb<br>SHA256: 0021cbd1c2624a0d10c33712796042e3573b6da34a1d8c060fab4a7fd3a47f03</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>112.1MiB (117.5MB) – 1,205,384 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9a65724d6068a2be2602c6f39a786cc<br>SHA1: bb1a2981b351abcf71e77ccbd07487ec371bcf75<br>SHA256: 4a94eb3aa733837868be5884e5c304ab05768f0b0c4cf0b8fe3c986bbc070223</pre></details></small> |


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
