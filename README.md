[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases are scheduled to change from CSV to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than one day (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-12-29<br>IPv6: 2023-12-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.606MiB (5.878MB) – 238,763 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 008b90fe6e7016f5f894a0f34d352045<br>SHA1: b573d14025cd5fa4c4cc4adf9a75684a96a13465<br>SHA256: 07ae1e0247f1b87df47147357adbeaafb9fcbb1a269401c93ee062265cb173a6</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.372MiB (6.682MB) – 82,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fb7a5c683bd10c539b67d8d1ae104f8<br>SHA1: 9b3b1f536b0308d221899e00378dc0834a4d51f5<br>SHA256: edcd3af43919d2d5512995718a1f67d2a2dafc0af6e164ac7bee78a7989f0153</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-12-29<br>IPv6: 2023-12-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.722MiB (10.19MB) – 412,940 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15c4409dbdbdd92004416d899f5b41f2<br>SHA1: adcedb83517f1d670296213f712c1e9ba57a9755<br>SHA256: 5b7d09df86dedcdffe7c075ff63d18bfca5bf3ee59c7edeba599d9c3792dcdd3</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.099MiB (8.492MB) – 104,941 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 932a28548e8c818a0d89458b3b314a18<br>SHA1: 35c9c08419f49f57918484a880d356b3a46b08ae<br>SHA256: af8938bac1697a78436b7d9307234d81e6ec8b531f577342e65250c12ca3a27b</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-12-22 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>21.47MiB (22.51MB) – 912,531 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a300ff77934b7044128e9e3d0cda3c0<br>SHA1: 62b2513e142deb3d2728d0f3aa50b0968cf46dc0<br>SHA256: 0cc2224ff9e1f16358462772a12116eebb6404b4cc982a88a96fe728a3aef76f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 2,090,652 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 778937c5b9624aa9c6606e1b1bf40e51<br>SHA1: a5593a83d5aa682e4f9221c8ea17018105df1686<br>SHA256: 879856b4bee7da9503cadab9623a8a691a677881719bd4cc299aa3f3b87b2a33</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.227MiB (7.578MB) – 308,674 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7862828d186c4a916870bf5ee5c2dbf<br>SHA1: b2d61949f9d4cdf20a7bbe7858ca457da6437400<br>SHA256: cf718693f02d6570f872d99279b6729e48674fdf9a0ad17b2b5bd3a3004e7feb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.88MiB (26.09MB) – 322,049 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf9a945a8ed9ee1ba2168317dbed510<br>SHA1: 5488b48f6e283b58e14057f8bcc69c7a60073e80<br>SHA256: e724c992a57d034ab069e985589127206d0519f5cb5070ef4d8bc04d59937e7e</pre></details></small> |
| | | Full Location | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>188.3MiB (197.4MB) – 3,100,304 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e98adbd1d81ad4e7676a5bc97c6062eb<br>SHA1: 83a91e8b43cbdbea769542d684e8a2b61d6cbcb4<br>SHA256: 07faf7b0b69afe9bdfb83c30bf26ed6a6bc739fc4122230461107e862ca8202a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.3MiB (310.7MB) – 2,579,379 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b45c72d3f47f242ccb1124627ab028<br>SHA1: 46f55d20900ce13c49f5881ad197bc7a0d54d072<br>SHA256: cade24018cccb007f481018f12d82b3268ea4089c4223c710ce4213be2f799e1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-12-29<br>IPv6: 2023-12-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.426MiB (5.689MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f1168f938cf9939a4db2627ea0d3aab<br>SHA1: 3d4f791a4ef9f8391ba4970939c4681bb739baf9<br>SHA256: 0be742468ea1b736effb939648093be1986202293187170826d147402251e44a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>20.07MiB (21.05MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a23a416cd5ce5dc03b9cbe11228f3a3<br>SHA1: 765e389ced957809c29feb7d42217e0e3eee8df8<br>SHA256: 73bc73bae2b14496056b243da3b2e2638e3246fb911159cadd9be315d7fb59f6</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-12-29<br>IPv6: 2023-12-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>178.9MiB (187.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88dc7b190a561ded04490bc5546295d6<br>SHA1: fbca2a42d89544e9dfd8835511d5852f986e439a<br>SHA256: 7a5ab9f0e69bf6ae1b57fc9778a0d5f844624e9fab7242c30f1a4845342848a9</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>179.0MiB (187.7MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6f4b0298a0cfd2f8debb7ac65c9ae35<br>SHA1: da1eb06030ca04ae9e61aa7723f34727d9474af2<br>SHA256: 6cc5ef9a70e83e77fdf8ef506194884f379b8a96081ddf2650b8b7dc2787f773</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-12-22<br>IPv6: 2023-12-22 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.81MiB (11.34MB) – 461,376 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca5eaa034d38e32afa8d66467314a6f<br>SHA1: 25352e73ccd14563a222952f332be62d683c41bc<br>SHA256: 2f57a4f4d9e23002af4a5a51ff90c88999c1f83a9b4ec94671818a73c7c62ec0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.51MiB (23.60MB) – 291,409 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1a70c649f421de15476818a379dad82<br>SHA1: f72f0f1f88cf0cd6854cd785919929acacaa1061<br>SHA256: 282ed6fbafb00a39da6d7ed62e54177d77327e87a1e34f2e4b0a8fb4599119b4</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-12-22<br>IPv6: 2023-12-22 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>177.6MiB (186.2MB) – 3,524,882 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28f1c05779ce2e5e507b031c4e22425d<br>SHA1: a1bdc69ea129301535115f9664adf9598e6a57ae<br>SHA256: dd34d98b278e0306db6ed7d90fa274a335cf75a489836812c19c01a8217d7d0f</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>206.1MiB (216.1MB) – 3,524,882 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b98284fed550a14c1ae14330ddce532<br>SHA1: 847050ce4022ce6e53f42386b792a2ae1b09093d<br>SHA256: 99a45dad91f1add093a4fba9b35bc4580095289c1e2d1529d7351d7ec35a5fd4</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>182.8MiB (191.6MB) – 3,524,882 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9028255d1b65f344f01c7cc7c197a8e<br>SHA1: db6abc1412618b03d150d04ad929337324d6c32b<br>SHA256: eee148e871e2becd6b275f74f270889f4099494e9a439687043cf1f4bd496738</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>189.2MiB (198.4MB) – 3,524,882 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a92d1f2d0f3fd79d9f65af859c4d64b<br>SHA1: 6ee4e15d294b9a48a48d8b55c49fb0df49394671<br>SHA256: e0e54321d68f36676768157349ac817efec0034f417288f009a9a2d1ec851736</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>218.2MiB (228.8MB) – 3,524,882 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 043821a6acd08bfebe24c2014d4e8084<br>SHA1: b881b4701cdf9fd54265d5b609e870c1cf943c26<br>SHA256: e0e3e817983d3c25c7521d3af45c7e4d17723be7ff2cb4381214fcf79610e5cd</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>177.5MiB (186.1MB) – 3,524,882 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f559a2506b4b0533d2fb9900dd5b533<br>SHA1: d8cbfdddad786f926375dd21f2c0cfbb3f343762<br>SHA256: 9b127f4bceef2ffd056096f98bf5d68e4d5fa6c6667f6d26d0fe120fdefe529b</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>219.4MiB (230.0MB) – 3,524,882 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f9b0b1f7fd05fbbf365cf3cce319668<br>SHA1: 43ea594bc5cbda9e70b84a600cf456385e26a952<br>SHA256: 1b61db4b0ea079d23e0da2ec8b0b0634d9c5a804bdca674b33373c0b906ddb37</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>185.8MiB (194.8MB) – 3,524,882 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5d1273cc07c22bd8b26db162efb17f7<br>SHA1: 429ed53634fefa69fc81b343ccaf062aacdc08e5<br>SHA256: e0b8f6e86a93ef6c3ec19279165ad44ad6660fbe827264ba4a39ff04b8418760</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>123.2MiB (129.2MB) – 1,223,502 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9faa482a5f05500b7e74f696f0f03b9a<br>SHA1: e770f2e6ed159a2cf77820e7eafb11a76859a576<br>SHA256: b6029c5eef9d2a07ef4cd93e9c7c061237a7768051316f48022231bf82beefe7</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>131.1MiB (137.4MB) – 1,223,502 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97facfbd0730dacab159d3d74ed36bc2<br>SHA1: c6cbc5c01493f3ddbdee7a8c279785b92d9a41ff<br>SHA256: 784af202846b8aee32e6331d2f5056834667c3575b4aab051bc0b8e10a5403c2</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>125.5MiB (131.6MB) – 1,223,502 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b46daec4465bb25ece5a914f4188b7d<br>SHA1: 2512bcfd88d64af86f9a744d7f4051ed13e4f93b<br>SHA256: af1ee9f644ee52532768fe62aa735b6b8133f3f5d9513c45e9cf91aac7b03bc0</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.6MiB (132.7MB) – 1,223,502 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9680a39ee2a61d217c133388697a06e7<br>SHA1: cb94e386763e433fe2025482d4258be555ff9a11<br>SHA256: a485f9170f301d7c96f3ae2b457b908b3fe8abdb1bb5eb56aa18ed8a058f6d12</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>134.4MiB (141.0MB) – 1,223,502 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edbb3c9c89f8e9c3d4fc4cadc00fe8bb<br>SHA1: 386d7e224a2d2b1bdd16fda52217b05b966edf23<br>SHA256: 9a71707b7c708fd98845677841b73e48d90969b81ceb2ad0d577d1c1a76cd5c0</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>124.4MiB (130.4MB) – 1,223,502 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8816dc5939739e71453d73e6d623792a<br>SHA1: a8d52540b0ed50bf86f030edc5ef39dec3d24975<br>SHA256: 55d1fcefce5ab00b0a886456ab4d863c86ed45fd327d95eaf9012443b3d224fd</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.9MiB (141.5MB) – 1,223,502 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8dd13be017158d28ca7643c2d58aaeaf<br>SHA1: bdcaaa8e464a78df31fce104def8c11c545cabd8<br>SHA256: 51f821f98c034c3526ee33a61a4f956b2ceadc72b975e6c1711196de8646ead7</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>127.0MiB (133.2MB) – 1,223,502 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f6b70d420f4ac487efeadff4d239a62<br>SHA1: b4cb0751d6980ab011efc3dab92c44310b09f0c8<br>SHA256: 3163f1bed28e46aeb9b8862860fa4870e0789272382dafdcbc7b3b271fa0e4d8</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hexadecimal format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
