[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than five days (previously ~one month~ two weeks) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-11-07<br>IPv6: 2023-11-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.593MiB (5.865MB) – 238,264 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d77ac2cf9d3c72cd80069614f12be5a<br>SHA1: 806c7fb6dfc539c1f672a1d01e44c1f03b0f5dd9<br>SHA256: 1e92fc5780e1bbe336a96080ab831359347073003a2242336ae2a677140bcffa</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.251MiB (6.554MB) – 80,916 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c9d9019872c9d99111b3a39130b9b10<br>SHA1: 08fdb7da9c919781df9053fd48589883658a0a30<br>SHA256: 18f38bb11822b20923a20f01464965b16ece1e6ccaa1881def8fb55f75f5ee7d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-11-07<br>IPv6: 2023-11-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.636MiB (10.10MB) – 409,297 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: baf48991d241385d947e9bbb15f76819<br>SHA1: 649f8a4bb9e14648afc60340370d0ddcd8bdd447<br>SHA256: 7e7c037bd12a6c022a679c8e30c1468041a394c86c46a361b9c2889f1396a567</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.056MiB (8.447MB) – 104,385 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a38b365005871cea8c41de1a5e462727<br>SHA1: 0b63721e2f7ccaddd9aef802ac0f02512f3889d5<br>SHA256: 5e41c92d5fd537c97c85029625b6bd0132940bfddb912499f89eb64ed2361254</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-11-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.22MiB (20.15MB) – 816,763 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e67d3d17a38a50e9d614d306842311d<br>SHA1: 2097cf72696c81eefd4bd30e9dd782c508d5b339<br>SHA256: 25fb16442df94a563d234935ab08019dfa4d7f0c7f3db86eaa2fccd51e308921</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>40.01MiB (41.95MB) – 517,899 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b8a0bc6d2e7138b344c170c4f2e9d69<br>SHA1: 6dfc9f9cd649fbd4b45be274a497e9e5e91d5ebd<br>SHA256: f28f120fd7e6430ed353600d95fdb873c859c93eb3610dba366b0cd7872b97fd</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.260MiB (7.613MB) – 309,964 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7fc3106cf6c65db7d44df8b4fb1d16<br>SHA1: 6ec97588db0af32a305835217289c32883d23f64<br>SHA256: 9bc7152bcf323316fc78e69cfa190cbddf22834208f48cee2e624c18150c9478</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.63MiB (26.88MB) – 331,798 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264a68f442d85aea134072d7bca0f4fe<br>SHA1: 65171ab00588cb7f2ae029d9345b44cccc888d24<br>SHA256: f76d40c34e6881d9cf3d98b34ced8105e9bd9efbb3f55e2bc224ece181569030</pre></details></small> |
| | | Full Location | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>186.8MiB (195.9MB) – 3,075,320 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96e5fc94ee00f3349281d3d79c8e3e83<br>SHA1: cf6b55598525f02890d9596fefd546190401adc9<br>SHA256: 5dfdabdba40afb770f6ff5afcc35db6136e9e28182bd6b3fd23b3c203dca5d1f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.3MiB (303.3MB) – 2,504,397 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bcf1dc4f4611d3e39906c6048aa8fc<br>SHA1: 2cd36733f3043bb3d9985d20fa8416a68b122e30<br>SHA256: e3d5ccb9e02dd929dc48ad40f82d484f9ffe60f9098c5a3ac296e33c5b9c2a9e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-11-07<br>IPv6: 2023-11-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.446MiB (5.711MB) – 232,323 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f7d79b6a3ef8bc35c3c8381e7c028<br>SHA1: cbc8e9cbd5c151f0cdb02a21e5e6fe9d8b662cc8<br>SHA256: 9f3976e09ec875d7e97185503221656e80f41f531e268da1bbf874127de2583e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.41MiB (20.36MB) – 251,316 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df2ea3be7027267ebb1947b4220cc4b<br>SHA1: e94b6a993297b5dff456113130c22e323534e39e<br>SHA256: 44458ed651d7b4bd99ad73459d500395c410da1b2fce9fbb2c4e5ce318c4bcf9</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-11-07<br>IPv6: 2023-11-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.3MiB (180.7MB) – 2,814,468 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25688ced507227d7990066c41a0d58d6<br>SHA1: 28da5022ff88d543bba4e15cc01b703781801bba<br>SHA256: cf219cb6d358d6e4df364a87f28817e4aaf8322370b86495ef74cc1941c73f5d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>171.4MiB (179.7MB) – 1,495,017 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d4ab0c657ede6538d2756cef356f5f<br>SHA1: c2865c0d416ae7143165db8aca21627725b4b45c<br>SHA256: 66022701ed347d75f4f400e76024ae545696e742e4c0fd30bedf981c262b318b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-11-03<br>IPv6: 2023-11-03 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.62MiB (11.13MB) – 453,325 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd0e10057967cd4c19b3e78599d0c31a<br>SHA1: b2f15b5a6601a7f17cb4903d4ffd33b101e04fa9<br>SHA256: d760f5a8b356b01d7032eb088eb6fadf1e863d017efe7c1862f66b75558c7ece</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.38MiB (23.46MB) – 289,674 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3c3cee14f300c2bd43db9df1aa54f09<br>SHA1: 824e0a953d56300fb268324218c49a5e4740b79d<br>SHA256: f045d3b3a10d6974eaf8b07d13c29ff71fc611c6a1cb9d3d207cdd8ecc162a43</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-11-03<br>IPv6: 2023-11-03 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>157.4MiB (165.0MB) – 3,122,649 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76c346baca060b652a49080815d0ff60<br>SHA1: ec34647d039a70ec653a17f66c4adffb20ea9622<br>SHA256: e2ff3c2f65cc840000f751aadbdb8ca4ae6c207091fcd0845416f9897009dfed</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>181.9MiB (190.7MB) – 3,122,649 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3aac187541bc4200d82c54f7271cd779<br>SHA1: e6aa6406c5929d0e2a5e6a0c8ade5478ec31ae31<br>SHA256: f2d3dedf0a665d25bc6a59e9c280c058d233ccffa747c671f1ebb0c10f69508f</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>161.3MiB (169.2MB) – 3,122,649 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8008c076bd399a0d14c3a0024d6ec34e<br>SHA1: a0d0ed0acfc06c95a954eb12986b362361fe1bce<br>SHA256: 7daa1c71b1148ec5db1357aa4d21a9f4ba470fb0ec7a1f44f7bde5de6891368c</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>167.2MiB (175.4MB) – 3,122,649 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb473fc6e4e254142618c9b938479ef0<br>SHA1: b15beb2e5da0110f75a376a3c88fadebfe697027<br>SHA256: 1fd9d3096e282a1c3c357b43c6fa255e22b6c9649dc40040ad01479450987317</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>190.6MiB (199.9MB) – 3,122,649 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b43decaaf28a8d71c1d16de923f44b8a<br>SHA1: 6c0777880cbb560b58f5853cf59ed09d30752678<br>SHA256: fe0ea9f00acce1112953168edfaca88d999bb8f6d66fbbed0fe1f70e216abae4</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>156.4MiB (164.0MB) – 3,122,649 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2dae8f6484a67a12a70c18b46762240<br>SHA1: 8630eff78cb80c5156830f969c4dde51fc54f2af<br>SHA256: d53a285d4a0ee2674ffab58732a5ff85245cef463906b2d2f85ebb20f9aec1d1</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>192.1MiB (201.5MB) – 3,122,649 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f10c240678dd6db9de961d6ce7a1b10<br>SHA1: d256d3cdc8fb058357f4a5bbc6e27f85fedb1e79<br>SHA256: 1edc415ec29dd70f2e6a8655ac881c11c6c42b123e78fefafd83d2450d51118e</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>163.0MiB (170.9MB) – 3,122,649 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: faad95e6eca23b80b9e0654e504979ee<br>SHA1: 8d5c3eea6e20e964ef2f71b3804181a18a1103c2<br>SHA256: 6a28c2b90a0b678764879ebfbcf7e5b202ccb40144fec84b1c0240a4c08a4e71</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>121.5MiB (127.4MB) – 1,206,717 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ef967cb75e2e958661089ec443523ba<br>SHA1: b731d6daf3835f1202bdc9467c6ab5fe63f8e6bd<br>SHA256: 132e2c1d21711595e1e121833893e8f346c2d2bbf9e23acc34cd98ff47dde37e</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>129.0MiB (135.2MB) – 1,206,717 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57b2562638b152c46cc84e004a3a9075<br>SHA1: dd6c900f9661ae94e4a8a772ec7d814b66690408<br>SHA256: b6273b9779896b32f9e396eae71a68949e8dbf7dbaf8861a4658a60c49d3ee2e</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>123.4MiB (129.4MB) – 1,206,717 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6580f494bb77d0ffca9ca265b6f0a80c<br>SHA1: 12752e9adf28cb9a174ecb743cecd12f37d67096<br>SHA256: 2182e5b4ee9be7c6c34d9e8c9e9510aa6aa17e267d415698eb2554866d2977f9</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>125.1MiB (131.1MB) – 1,206,717 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d4f4420fb12e15c3ec90c46d45d44fb<br>SHA1: 46c96b5a76a484bbdecc00fe90b2117ee8d1422b<br>SHA256: 6b69258e3f7433fc9f6f643cae5279f91dddcc6ea46e0239d2e71f142c910b1c</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>132.6MiB (139.1MB) – 1,206,717 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9d148e25912c86a1bfdec14aad4ebb9<br>SHA1: 2a3a6b2219c197f34dbdf1a463b246ffbe9cc2bd<br>SHA256: f9d50db5b0040c9f1e17719c69984f79ac0e56f9918edeb131729ed377d312d7</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>122.3MiB (128.3MB) – 1,206,717 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b151f18f98c67afd0488940b304f633<br>SHA1: f41ac36c67b81cbe8bb421d5a5dcb54e3fb58ee8<br>SHA256: b7ec804bf0d109bdb4a25140c6ece45ffb216f0d048bc3f06a1aecc3d2dd0975</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>132.9MiB (139.4MB) – 1,206,717 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dbef271528e82298ef79d4317a6f80d<br>SHA1: 2f526a227e0a6e19681099a416b221c2d95f043f<br>SHA256: 55bc61cbeb054060d457a1a8583aae095fdbc33aa1d43cc517733afff26d172e</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>125.4MiB (131.5MB) – 1,206,717 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b760b4ae5b4e61c6a78a72dd6be4a6f<br>SHA1: 84de0ef908b98a38cc3543f2769fc6fe9bf30560<br>SHA256: 24af3c8873bc860838c16c5241997fb3dfe7be6073079a4398f5d2d448f3d200</pre></details></small> |


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
	* Store the IP addresses in hex format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
