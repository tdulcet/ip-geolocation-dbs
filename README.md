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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-01-05<br>IPv6: 2026-01-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.437MiB (6.749MB) – 322,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbb917bb3860c94f9e9b6a23bb7d4431<br>SHA1: 8cd3aed3c7ea044e4dd38558522b68438f63369a<br>SHA256: c3cb71c6ef56b28fd7cecb35a7c4af62f8cad8792f0bf4c07d78e08ab5ade7d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.13MiB (15.86MB) – 229,916 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a811721568eeb3714d04674aa7784bb5<br>SHA1: 41843b648bc3aaec2da3012d0431fcd3b528bc82<br>SHA256: 2effe23faae45cfa63859d2b06ff41dc31bddec3683786c339a141a69e5060cd</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-01-05<br>IPv6: 2026-01-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.182MiB (9.628MB) – 459,701 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fa201d8bdba9fdbb967a6510f5fba8c<br>SHA1: bae620f75dbc4933b1478957c8863a37e764373e<br>SHA256: 50ea7260e762c61213c00bdc06ffbd65bc30be7e32f7af717ab79d7c12130913</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.513MiB (7.878MB) – 114,288 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a016dd8fdb1f73e7b1b82b6adde98ccd<br>SHA1: 9c41ca037ca247aa13d02f055b893e0dd5d29bae<br>SHA256: 4193a60abd3fbc0b02a92149cb43d735434cc96cb3c74fc79b510431be7bdf31</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-01-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.56MiB (13.17MB) – 628,919 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f816d9cf46e35539d88d2b6fe29573cf<br>SHA1: 183232a2ae199964a45f541d4129c7dc5eb1c561<br>SHA256: 9ccc35eee34cd424553888f18e469e50af715ce73d9dfd76ce2187bcf47229af</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>64.58MiB (67.72MB) – 981,470 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98abfe38493f092216acf6d405d7543c<br>SHA1: 0b2817bb746e153c60119653675e0270401e7526<br>SHA256: bde98f49229322b41f99a71dc1025c37e6bdb86d3075a476431e7483852f56ce</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.843MiB (7.176MB) – 342,905 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7f0c42b88b3ee5ac2070e71f756f963<br>SHA1: 4416542c9574226ce202070dc48ca08edc6fab0d<br>SHA256: 5393382f53c552965d88b65e40e02f63c643f2379a931aaecef8209586b9ced2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.52MiB (17.32MB) – 251,059 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232548602865156556e4ff9d7db331da<br>SHA1: 61d1e0b2cefeca101ea9e8530969dab152188ab6<br>SHA256: b004edb93559a31ded3baa727a5d781edbe90c29420b4d5691f44e917e83bdb0</pre></details></small> |
| | | Full Location | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.7MiB (223.1MB) – 3,730,744 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42e04cdc8d81a8ce6b440accea48b373<br>SHA1: 9c414f68d243d9ebdc8b7c65e081580b035b663c<br>SHA256: 5274313529b847bd8629fb44b41144c683552f55760a830f535892f20b8e46db</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>457.0MiB (479.2MB) – 4,442,155 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56e8f0cd6817f6807824ced45628cb9<br>SHA1: 316812aba9e80b97b08bfca58defd796b628d008<br>SHA256: 44317ed175935104135d379f2a9918ca97141e9bf034ee1bca6cdf894093d72c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-12-31<br>IPv6: 2025-12-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.249MiB (5.504MB) – 262,700 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1336d51547e70ff41f1e470101d76301<br>SHA1: dbc5c69176db1e71290241508d9bf23d3fbc7c99<br>SHA256: e1be0793199e009b2d581c68300def944a9534d67b3357dba466bbc4e29c4608</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.00MiB (23.07MB) – 334,332 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7de5c30d61a35275c4463ba1939d47a<br>SHA1: 187b58e38e8853be50cbc6bce0c609f30fbb700c<br>SHA256: 6dd9378a342492e7af6faaf3f48f8ef56f75a9870b6cd6cbbdcdff264db76afd</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-12-31<br>IPv6: 2025-12-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.7MiB (179.0MB) – 2,955,286 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb75d526f52d515d850e10a62f3ce7a1<br>SHA1: fc0b4e2c3eedc461e42d5fa445bfd64c25832111<br>SHA256: add4cb25ee97481f007b554ee596a004318bf30a9034a47e9fac209eb7947e29</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.3MiB (302.3MB) – 2,794,225 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfbae8186489381f9b07bacec41f902b<br>SHA1: ab0c06ba27f24066c49aa9282addd61ee7f70de4<br>SHA256: f67f46b0227237d8454f4b74ef88bd4742945b80e8efd3dfbd080bb0de4e5229</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-01-02<br>IPv6: 2026-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.21MiB (12.80MB) – 611,144 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1168655ad247a27a81cbf4919f3fb03e<br>SHA1: 8be7bbecbcf772334058e7c9173579ddde87cccc<br>SHA256: 858fa41bdb7b7e57e6bf75c7f95647c1658fea4e130df078d5393c965a38a4f0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.55MiB (44.62MB) – 646,615 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 519a9bd62ae41c7408fd2657aa828497<br>SHA1: 89586519606ef6248728675c120fcdb55d14976b<br>SHA256: ab8cac38fc1f19d8a0c0b03a00cec3f50c5ecf709167f62dd4fc2342bc4d5624</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-01-02<br>IPv6: 2026-01-02 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.2MiB (186.8MB) – 3,517,805 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5845de664713b2a7ae1d4822a052f777<br>SHA1: 88371f9a84cc3b2e489a754a074129c5c4c4ec4b<br>SHA256: f67ccfe35f88ed965da8ff56bc8e33372233eef68c74419249d441067cf1260c</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.2MiB (198.4MB) – 3,517,805 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a70087f4d967a6b8a1c99391edd5b0bb<br>SHA1: 8e0e897f066050a588a3980f713a60b67b1b4a46<br>SHA256: 5f1f17d7b8acf852252ce1800b8cc0363ab5f0295bdca97db6a7f08dc7a553f4</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,517,805 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15487fac9ab56ae19a8ac5306dc79732<br>SHA1: 62b4df6ef1d6c316595034d151739c3f9f460f94<br>SHA256: c268559c4e6aeea06e8cee084d35706cab8f6f5b6c10c8303166eb2ba99d2aff</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.1MiB (188.9MB) – 3,517,805 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afa431111513a92df9fa58311a69fd12<br>SHA1: 610c416e17c12cea2f111af7ec4c0bda46178568<br>SHA256: b900812fc3abcd33ebcfe84abaad79dd7c5366e5d13e3545c6c2504e36c07408</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.1MiB (236.0MB) – 3,517,805 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 189875a6cdbeb8906278f9fa388aae5e<br>SHA1: ea7c8c9e92c0bb1d5f9e5d28922a9e3884ccd82a<br>SHA256: 3e4f00ccea5947e333ce358d1c0183801eb54d2d64eb34a6ea1a5e4d59bcfe99</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,517,805 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c0c85798fb7c5a0ca3a09cc6d5d9a53<br>SHA1: 6dc1c76704469ec193d372b5a6b0a5b2ada719e9<br>SHA256: 914bc3ce09c3433c93c4e0575cc53cc381a564462657257994b40dec8484728d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.1MiB (229.7MB) – 3,517,805 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f230f1184f7f5a2e0607658b1c3bcd3f<br>SHA1: f6378fc64205e001fdeaf99d7502142c54307abd<br>SHA256: 8c668c4059c621255510c724dbf01cfa0d04fc2dd1705e85aa31473e80447eae</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.0MiB (192.9MB) – 3,517,805 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2f55d1b81ae99236c19c246a0fce97b<br>SHA1: 7c9d9e43f1be8a93a82928be8537066dca1270bd<br>SHA256: c71776c1a6b34b38f34254d2e9bba6e465d2e6df77540214dfda1331f583b430</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>183.8MiB (192.7MB) – 1,938,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b1cb0ae730ff0913c3b7ad7311ca3a6<br>SHA1: 08d404f0822ef4f382b41c0c56e096926b20cfeb<br>SHA256: ecee9a82f05b7f345b00044074cb1f1bfb1d94331709900b9dc342b972078b4f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>188.0MiB (197.1MB) – 1,938,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afee03218fe217a21e07126a25f43f07<br>SHA1: 81ed4a84fcf1f11f2a799c65642f8f83e98fc148<br>SHA256: 1faa29ef88e913c8510baecf1231039755205d717acf3bbc0446c8450d7dcdb0</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>181.5MiB (190.3MB) – 1,938,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c335f330161eb78c38b7a7d98798777d<br>SHA1: 4590144decda51770d7adac876ff5f621981fa37<br>SHA256: e33923cfa57eac4552e287b512b99b8b1144d3a4d9e1715db8f95c954348b4ba</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>182.3MiB (191.1MB) – 1,938,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00682ed740c48cd8c23c299ca6c530c3<br>SHA1: 97fed21fa9a0f9553804de40c93ea05f9a5836fb<br>SHA256: e495708bb20fb7a88fe79c84a393a9c84a28c0df86aa0fce8fbe276f206c5d6f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>201.7MiB (211.4MB) – 1,938,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71cda4618462adc6ed496d7436e4344c<br>SHA1: 10b37f7398790bb0f2728057be8264f539d005d4<br>SHA256: d61dd948315a4665bceb2c9dc6b5ffafc07f441770acae9a0a1f7b28a0b476ed</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>181.2MiB (190.0MB) – 1,938,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d96b809b87fce179321d74f8b836b<br>SHA1: f0e0832441eb1fb727d6306a70adb4d851890f81<br>SHA256: 882cac4ad5e18ec6abf1b68be1b61b117285dfb34c8041f25652eea0fbcf882a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>201.8MiB (211.6MB) – 1,938,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dcc2957174dc2a48fa43407df3ea32d<br>SHA1: d5a5bd795769dfbd6c1366b40e6ae9633c3a9fa5<br>SHA256: 539b43312fdb726446e31b884de8cfb99306e607082e1f04cfc36a51fd3ea409</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>184.8MiB (193.7MB) – 1,938,923 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e1001a0b8348bab83a2b6149a7cb7c3<br>SHA1: 3eb7bb6762c3a7f0af55414d3bf2a91047b2fcb6<br>SHA256: f600e626b4a74dabb066da0a24e24c5221d333771b63ac2bd2a1d56895f8eae5</pre></details></small> |


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
