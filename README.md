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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-01-05<br>IPv6: 2024-01-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.771MiB (5.003MB) – 238,838 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 278891d75711543469b223362e870dc9<br>SHA1: 6f5f0fef0873217b5396d9799f6f7c9f62f5df07<br>SHA256: 7b7f8b23e5b04f9742d96d77d61a35d5d71df2ab490ae3b2d65d48f26d91b140</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.455MiB (5.720MB) – 82,898 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55b4ff8eca0f2cb9c0d814202aec041e<br>SHA1: 10589cc0400830346f11b6af9eddef68385d4316<br>SHA256: d5f3280addc8c0bbb1306677c00576142b6f41ca30a85aa9a904f808b4be0ce8</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-01-05<br>IPv6: 2024-01-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.245MiB (8.646MB) – 412,910 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df1932d3add057fc70727b138b067f42<br>SHA1: b46e0815dde1e31c3202ceca04042c2cdc566b8a<br>SHA256: 78ec9dbe1afc30dbc63fff2ef8e46fd46e6163e94783e96662ee15d15b2f6f3e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.884MiB (7.219MB) – 104,734 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d7662bf33b1f475efc0bb3f546df996<br>SHA1: 41bb0caf987a58e7cb6398b4f125d2c72267a593<br>SHA256: f765113f8e7412d23e3741f384180761831ed86961582e04b468c3e14d2c64ab</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-01-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.55MiB (17.36MB) – 828,671 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27889ac4e98e0fcb3a7a44a1fcd55021<br>SHA1: ae91c1756d0246e15a15bfaf931c01274e214795<br>SHA256: 2de91fd57f1b5a8f86619448c4585a16a5ad8f277a40f9d140192eee360053e4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>50.21MiB (52.65MB) – 763,030 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 933678adca039c871d82d4870ad1528c<br>SHA1: 6f5f8d1a198edb11598b26df90bbfb756ae58ab6<br>SHA256: 4b1c78760218147da7fff8da141cbbfaf7e8f3b719a2d8e928f8a3d3e2dfbb0c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.162MiB (6.461MB) – 308,408 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736158b820db1062b003cfce212076a4<br>SHA1: f3b03108eb0edf83c338abed05e010c2b0e9cde1<br>SHA256: 68e446a0380ab263a21743f68ab8aa6b249b213af0d6ffdac0780fe4912cb7c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>21.05MiB (22.08MB) – 319,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73819723f00de32c17c8aeca84d93383<br>SHA1: 71d954fffd9f9f5979ff89981fcfae6f73cadb05<br>SHA256: 1328a782f89b58d1f6fabcf3542ce4bb259d89c1f28a0cc70abfe70b5e573eea</pre></details></small> |
| | | Full Location | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,096,472 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b990a48af772fbc4cf7093aa51d35b4c<br>SHA1: 8ddfa8795c4c534c0bfd99b2472382b368d7fd5c<br>SHA256: 117938f84386f9ca627464e7c42856b6d9ff4f68bbcac12a393b73ea1ac0836f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>243.3MiB (255.2MB) – 2,358,639 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c61e48446e598bab5cfa16234f5f136<br>SHA1: c3373a6fe2e2f8e08a48274939c4b494fb99b5f1<br>SHA256: ff81c189923d299847f5b5e0e5c472fe10d836d11e24fa5379a2def67c998406</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-01-05<br>IPv6: 2024-01-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.626MiB (4.851MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24caac24a9c72bc3caa6451ceab08833<br>SHA1: aa114043e64d74ecd9e8ccd339b80c62d3fcbabb<br>SHA256: 6d48a0384e6e4d38820ac8d2936c12db7eb726dfe20c59600d4f14d173e3b15f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.10MiB (17.93MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fc970b50f7b01de0d0c6bd29224c13<br>SHA1: cb1fe32e67d0561cefef5f2908570ae3af446a24<br>SHA256: e0f36200f10f817a89b6cf80d8d459900c5428a669cc706af32d15b709a8b624</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-01-05<br>IPv6: 2024-01-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4MiB (176.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4104f39d8c379ec8967157286f495717<br>SHA1: 440c75c20491f104948897ce552c95510badba7d<br>SHA256: 6689c6e63153fcbdc00272e2ec6cf04f0c6877860b4a667b3972dfa08c898747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 142dfb0f4dc0ceb4f5a41b018ea53524<br>SHA1: 284b510184f46179e9e34f60dd0db14fc72f3e50<br>SHA256: c57159c9a8879702623a2ef4d0c2fad06d21e96f1836db2d3a09f9216aee1641</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-01-02<br>IPv6: 2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.262MiB (9.712MB) – 463,957 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ad80abfd3f2b59e2971fa6040ebc50e<br>SHA1: 0845b734ad732c985b9133ba20e58b1a336cef2f<br>SHA256: 23cf94cb2976ba18043688837726f7ea14eadf90385a099be939bc92de323e1e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>20.40MiB (21.39MB) – 309,973 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 021a3573afef1d4a51ab148c59d11aca<br>SHA1: 14c17434c68955df0ad454466b4050cc1e7fb939<br>SHA256: 3f2d079beedc1a970f02a52fe014df34bb177e4d813948cd070e5ba0432e221f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-01-02<br>IPv6: 2024-01-02 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>157.3MiB (165.0MB) – 3,353,243 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a90b1baa1737c4b6e035b227b5974e5b<br>SHA1: 2311eb664ada28cd34bd333a922ee8e4e7fa9100<br>SHA256: 7a3010cc5cb8ccb8d801dd7ed1f226262813a72f4218ef95847360918261156a</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.1MiB (193.1MB) – 3,353,243 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d67c428d8903123a62ab704db4137448<br>SHA1: c901cbf5157b6b08fe69c9afac8cdf56221cc905<br>SHA256: fafa483c7d8cf19e706d0a676447a5a85785ace057f8bc22b9c88ff84a7d29bb</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>162.0MiB (169.9MB) – 3,353,243 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ab17247c383a8279d9b76170e976a7<br>SHA1: d91ba16d6d233a94081aea17dd112092dcace743<br>SHA256: e0944a14d27c747aeba5f137ca609d096475532bc32aaf8e2bdf0f38ae3fe9e2</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>168.2MiB (176.4MB) – 3,353,243 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6f860a3b72e62242d7b7905a714ee49<br>SHA1: cad8fd3266277d54542d8c9758ceb7270c1eccc9<br>SHA256: 5624a6b641320c92e78ebfe090fdcfe2e65927b15893262933cf858af95f077e</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>195.1MiB (204.6MB) – 3,353,243 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0f320399980fe27e0004413bf1b4ead<br>SHA1: 8b44fff5b869f6278d6f2d2baec347d2e8d227b6<br>SHA256: ad921a0f23a69da366ad9cb42afef95cecc8c7f1c3b8f753dd593469903c9c6b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>156.9MiB (164.5MB) – 3,353,243 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09613d7bdd84cfc7190cac38e1d815b9<br>SHA1: 0ea49316029d1af76698aeabeb4523ff9b3bf165<br>SHA256: da46371b4ce8c7c931ca82c741fdc134f4029f5b23ba09700fe7d143631fbcec</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>196.4MiB (206.0MB) – 3,353,243 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6569173e6558aee39622a3350e259cf5<br>SHA1: 42adbc9e0c3c6e6906b1667ffdcad22e65338604<br>SHA256: 3d73964a69cc1ed1786302b2a90baebe6b2b2b2255d5d6e27dc1835910151f0c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>164.4MiB (172.4MB) – 3,353,243 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b8009985e4c0fccd11e36e91d38268c<br>SHA1: 7428c720261c7a93c1ee390064c8099d6067168c<br>SHA256: 0786cca6a90bfc59de7c75e0bce7b7d8479d8df696305e5c245328a07a42d679</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>105.3MiB (110.4MB) – 1,183,143 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 572265bf2b885459ad9f0536e8344d5c<br>SHA1: cfe375eb8544d7983a20b9e5f20c7da734add1e3<br>SHA256: 5e151d3182f7f8166560d4a9b283b33ffc40791a204229f35d8e6fc764ef882b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>112.9MiB (118.4MB) – 1,183,143 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b760408baace1770966bd072154d5ad<br>SHA1: 01e6f6befdea12a8acd369244bb0de43d7d42800<br>SHA256: 00195934d2913adaedf9e7f776a0a1c8bff4d832942ef5ab945ebed1eaddf0b0</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>107.5MiB (112.7MB) – 1,183,143 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20ebd7da596b00c147c756abfcb7c482<br>SHA1: cd39e406e4d6d0b1e3c9d19d42ebd3ca10fbbfdb<br>SHA256: 007f668fd85d7e0ff96350c63f6e20f8fe77f08a450c724ba95b567330f0855d</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>108.5MiB (113.8MB) – 1,183,143 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62b0d926ab3561b3476429df23a8c56f<br>SHA1: a7339b8aa749b76c7ee35d46a67b02aa8fcbc058<br>SHA256: 0aa88e13ecc6936b01c70532363f2a3a4a205f8126dda97c2b227528652743ac</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>116.0MiB (121.7MB) – 1,183,143 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcf59ca371e26e2745d798a713f6db11<br>SHA1: 519c2016fd8bea1fdffd3c37a1b112c587240e2c<br>SHA256: 7ab7cb9f53eba337c263eb63f6ec0f05bd614945202a57b19ea888dd767f4a96</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>106.5MiB (111.7MB) – 1,183,143 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c29fa1f5dbcf3780191fba9a872abb5a<br>SHA1: 299934488bbc56f4cf93e6c251280646517d7822<br>SHA256: 51a6cc49ef1f5464c469f337a55a5b9f4d4f641143d5c95b87e99bca3d41c3e5</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>116.6MiB (122.3MB) – 1,183,143 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e4df7b3ebe1085a1f186c13e5840443<br>SHA1: 062c79d99b9cf4fdeb30d366513ddb2e40abf1f3<br>SHA256: 8f8102db20f76631fcc9b0d4b0f377d07ed74e10fa40899b26333e8e46893e7b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>109.2MiB (114.5MB) – 1,183,143 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5d21650eca8fbbb97bb51ac8745246f<br>SHA1: 4e22dc6206874a8200af8b83dbad34899ce0b727<br>SHA256: 5f7abbcff751259413d6325466db23b8bdc96460e47ad23ceda85bc9bca03194</pre></details></small> |


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
