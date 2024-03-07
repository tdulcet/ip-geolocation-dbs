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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-03-07<br>IPv6: 2024-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.805MiB (5.038MB) – 240,540 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36bf563f7bd667f00663b687a4df990a<br>SHA1: da2d5bf34bbb679e606d5355a7b50cd90e8a8615<br>SHA256: 4c40fd2cd238dd951d2793d5e2516d1f43df05e3dece97dba29bf804f70fb495</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.973MiB (6.263MB) – 90,775 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76be2e82c5726785216bed62728b4868<br>SHA1: 68fef587005a711a5e00563992ba8f9dc34931d2<br>SHA256: a5e5f074c5a3f16b413af1de91b41be7ad168c8f29afbce5af6dc44b75d33052</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-03-07<br>IPv6: 2024-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.197MiB (8.595MB) – 410,484 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3697891dcd67a5920bb12ad15bca35c4<br>SHA1: 5ea404e704c353ded4ec291b948d19fe621c68fb<br>SHA256: d0adbd9b0aa0bbe9ed47a09b05a3f53c365c639cc1aa90743929019a05e13539</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.036MiB (7.378MB) – 107,046 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 916e93cfdbb4919877b99ec8bfb4240d<br>SHA1: 3dd55923093cf7417ca9c082e9bad75051beae77<br>SHA256: 038dbc150a4ffe35930533dc9f6867fcbda73411d106eb196fa024185fdd5c9c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-03-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.47MiB (18.32MB) – 874,785 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63982dde957cabdca0fb02dbbcdd2278<br>SHA1: 05e8ced509df254dd329cdb07e17962fb7039794<br>SHA256: 0d9f893041d494585ec65ce9137893126cdbb9b2d63c7b67dc6a422e7f9c6821</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>57.95MiB (60.77MB) – 880,658 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35bfb835bf24b30aec8d887fbdb4f19f<br>SHA1: f4d1268bf210db9ca5c3b6e3794b5e897cc6e4a6<br>SHA256: 6041fbcabb0249eda6bd2c84b0b9b22aedf5a77dfb0bd55018f6169624ad4ca1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 322,326 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b232d78e18dacf266bba37244688a18f<br>SHA1: 2ea0bf2a68630d5c12c6fa1d18f2f3eb0845f297<br>SHA256: b9f2935f135d22119e5db5d8d8666980b07ac2e36359fd6dbdc9c26a8b3be2f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.03MB) – 275,831 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a49241985f6153f5f100b60421257f25<br>SHA1: 51e0348aaa544a9b75aa17c9431f3745175c5c5f<br>SHA256: 3420806d6067a2579fe3eef92e4cd09b9b792cce9c418a3ca7f3c820f4edb887</pre></details></small> |
| | | Full Location | Monthly<br>2024-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.6MiB (189.4MB) – 3,158,494 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd92465491c42b3844af48593793b1d0<br>SHA1: 53a3bac0d03e0e4bef95ad11b21c1a1e92eed9f8<br>SHA256: 6157eb8d8b93b5da65533893b6b1af8682e371476cd754957d56f3cfd1179aad</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>307.8MiB (322.7MB) – 2,989,351 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a432fad1dde6398b8b6ee222abf32676<br>SHA1: 78d2ec063fa05a95bb17703a5111864cd91a5446<br>SHA256: 5974cc41b3872ea8fe373def59322db31b678ff8585a6e529b9737d648343c0d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-03-07<br>IPv6: 2024-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.772MiB (5.004MB) – 238,843 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c15a8429d90e259b5d89e46f363cb94<br>SHA1: 11590e995ca6469691aed3ae703c69398c77a07d<br>SHA256: 36416d6d7e8c82177e05f1950529ec607ca389a020fb40fc49b45bdf0bcf638d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-03-07<br>IPv6: 2024-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.8MiB (178.1MB) – 2,942,325 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8bf036b2620260eba08c4b59f30ad2b5<br>SHA1: a99847ab6732f596cef7ddc2da1038c4ceb123c5<br>SHA256: a2351d207b79faebc18456f39c7c525677f4083269f536c4bf18267d2697cc0e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-03-05<br>IPv6: 2024-03-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.533MiB (9.996MB) – 477,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98c0fbd21ca5eaccc21752053abc5986<br>SHA1: 2cc3db6d36c516edc7c28c5aacb233468f7e4235<br>SHA256: 7de9666cbc4ad85563bcab91c4e6c1ed1aaa36abfd86ff0e4047d0c401bd626e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.28MiB (19.17MB) – 277,822 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93fb512a4b945de06fd719d66578cca5<br>SHA1: 3018822a2475c4a3215f0a1dd01d8b7678034e40<br>SHA256: fc2dded2e26bc47ce2a570e3034095bec3c7c01bece7960bc40ee574ee40fc75</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-03-05<br>IPv6: 2024-03-05 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>157.2MiB (164.8MB) – 3,338,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4515178d522853a8166a3b877a986253<br>SHA1: 5c51c0cefd15eb8e684b5be0112851f31952709c<br>SHA256: cf278cc2496d113cace8df6341363912141696562634ad871ceb7946cd1f6dfb</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.6MiB (191.5MB) – 3,338,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10f7e36bd5e5fd12882345c17c2d029a<br>SHA1: da4d9c6aa6e6d2c58d10676f4fe673a663aec3f9<br>SHA256: fc5124c93399c25793fa0dcf9567bfee9d140d0908261461ddd4dad2020a621e</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>161.4MiB (169.3MB) – 3,338,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b90f6ded41685d60b08e5e13af5ec263<br>SHA1: cd62a7c7c03839c0e0ccae14e6937d0be55b8f50<br>SHA256: 00580e3c0065d6923de1f4f5fddf159d707792df6f84b4f00626dd5fb94eadac</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>167.5MiB (175.7MB) – 3,338,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b72f763ce3100cd9c3d2780e538e6431<br>SHA1: b000f5852ef1cd7baa6dd31af08546a14e87d4f7<br>SHA256: 4e7754f2409a641f9588d619de90e59e16c229b348aeb4867481a95ef635ad55</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>195.8MiB (205.3MB) – 3,338,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d264ed31b0a3febdbdcb5e046dd07dbe<br>SHA1: b8441a4c400e91f127db8b019dafdec27b3c6d33<br>SHA256: a2cc42f04dc0963f6838390b543145ead9e273a0508bae2b4430d6344d01cb71</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>156.2MiB (163.8MB) – 3,338,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3fa6a439148c6a9c493a6761bf48649e<br>SHA1: 14e35badd60a191da6439dbadaf356168856f4fb<br>SHA256: 2d806be6a35f7321489e8c799bd36b337ea75f8dbce8838860d6d84232bfa54d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>195.2MiB (204.7MB) – 3,338,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1793f67caeabc38a831718e9d7e0e40f<br>SHA1: 54d9278005a912cfb71b847c2269b6e9b5b3bcb5<br>SHA256: bb11556fa8b12e6d0a91fa9d1e46ac4f1f6a1876a347fca58172f3472ca76d19</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>164.9MiB (172.9MB) – 3,338,727 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98f8e29d131ba58b205dbdf9dba522b6<br>SHA1: 0b5c99f4556618e0a4739c589715a412b6cee341<br>SHA256: 63d431dd3516698b99deb8434030ebd34c3c372e31e8076ef42e21d375f24bf0</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>103.8MiB (108.8MB) – 1,160,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c48311ae77cc8e2d781e63fdb11b1709<br>SHA1: e8cd5ff4c35ef7c52cc43136fb63592affef1faf<br>SHA256: a8693744e09dcc67b1b414d0ccc190cb39fcbff1dce0fb2d4fad470708b70055</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>111.2MiB (116.6MB) – 1,160,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4330ff931db056c18820730f6f256b0e<br>SHA1: 4acf0c94228031f75c2ee10a3f3a8e661161d802<br>SHA256: 2b71487e9f62bd43b73754a6d310e8b4998820db3804505f98027a187fedd998</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>105.8MiB (111.0MB) – 1,160,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85881eb53dbe26f29a7c31e8a434e47e<br>SHA1: e8b5c018f5cdb0c09e95eb9bfe2cf22d9c684e5d<br>SHA256: a7ef02144368e24b5aae119185b96c5d1e870fe95f7757def91c96245f1181a7</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>106.8MiB (112.0MB) – 1,160,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9454836ff2b6ff748dc4e8abcdbd34e<br>SHA1: 13dbda9f01a5348758bcd66de77dbc9793769486<br>SHA256: 6cab604456f06ca8aa3b83683369fca69987e05e65dc204e887bcdd2016eab0a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>114.6MiB (120.2MB) – 1,160,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e42ae3b3d3e3cd27e3dfd17092802773<br>SHA1: 4f776125873a3d682ad9b9745c7e364fbf2d2b01<br>SHA256: 935162ff61218158953aa7ec222584e4c109c31bc122a03d5298fa4ff10e5b54</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>104.9MiB (110.0MB) – 1,160,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f99bd696a4c53a85363dda384662e156<br>SHA1: b0129510a3b9f2cd479b6553e17e4983d84404ed<br>SHA256: 6f6c9ed2eacc3276a4bcb0ed0735a4e556c9fe211126fff4c1df603abc97bace</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>115.0MiB (120.5MB) – 1,160,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c39cba5125c4332e583c1b064870178<br>SHA1: 546ca004871f0c08c6c51c421fd0539c6f562e4f<br>SHA256: 6aa6de68fea05449d0059ceabdf42e971f7a96673bababd36741acb84fc2a356</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>107.7MiB (112.9MB) – 1,160,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae3aa9c38b135b90e62d17e7887d45d1<br>SHA1: 01b7eb49a3083c54f10fc420be15687f6fa417b9<br>SHA256: fc2f3d0dda7766db8a9b81bf172c575e6d14650aff0557a9c03eec2132998a2b</pre></details></small> |


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
