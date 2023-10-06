[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-10-06<br>IPv6: 2023-10-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.615MiB (5.888MB) – 239,193 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38d39ed0fe9b00fd59445085b9e61946<br>SHA1: d8620903601be957d192ea16883ddf6ce9d8c1d7<br>SHA256: 466dd7537960e5dd32817072ab9f72b55206ebcb44ccd43457ff2bdbad3814d5</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.283MiB (6.589MB) – 81,340 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac394ea28977db873aa14fee0e1c868b<br>SHA1: 7ccb83bc635f198cbe57636c11147d368ba0048a<br>SHA256: 13195e1400021ff463119fd40612fa8d654f6fbb487f0d42355fc5e717914bf0</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-10-06<br>IPv6: 2023-10-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.590MiB (10.06MB) – 407,346 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a6a6bda0880b6280834285709d63ebc<br>SHA1: 5547a5631e7eb39062abe1d534549c8d6e9193e8<br>SHA256: a96fa0fd46f959b96fc415980e4976d600d203b1e92fde798e17c9d903bcecee</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.043MiB (8.433MB) – 104,213 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c36ab991babacaf1f8c567a3c01d4f1<br>SHA1: 2a5006ce1bb226b71eeb3d178ded19dc7dfd1eed<br>SHA256: 6b09a416de6a07f30206087657ed4b9bbe7dd74ba72262e0bf327851461b23d3</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-10-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.58MiB (16.33MB) – 664,062 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14bef4544b92565733712a202ba2f291<br>SHA1: c40ccccccab6e99e11fe10b958babac730e02562<br>SHA256: f9969f08bfd786a29919ecd18c2875128ded6bc4b0ee10ca67b3094359002c24</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>40.52MiB (42.48MB) – 524,487 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65579e0dad8f36410acbe5ae62ba8989<br>SHA1: 64fea2b67730401f446992602088ae651148733a<br>SHA256: 2d16722aee42da4a8d685b966ce0500600622d64d7c393c5896af074695ada71</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.207MiB (7.557MB) – 307,820 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ff8d81d8ce4efd3476359318175af0<br>SHA1: d105d1c4490b536a83d0461759256799109a17cc<br>SHA256: 4cb45f08b0bbd6d6c4fb204e776835b939ac663761aea652d12ae2ab20494228</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.54MiB (27.83MB) – 343,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3256ab7e4df24ca9917bf92c70b9ce1<br>SHA1: 832b96b707911579f91d2a42cc84b0766c5db738<br>SHA256: fdb03997e4b7c1a6bdffa274673b7756d8dbfb2ede55f1186b3957ade7042544</pre></details></small> |
| | | Full Location | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>184.9MiB (193.9MB) – 3,048,591 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed65f47a5f866d476bde81f05015d0ad<br>SHA1: b0ef2e2cdf8875da35c99816df76f9fa88d3de9e<br>SHA256: 5bca8efa9618ae69c9fe4228342c0ec4bfb4d581ca0766a3a8e45978d1fe7875</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>269.4MiB (282.5MB) – 2,345,213 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f854d9364b9ab55744dfdc557c9f9f6<br>SHA1: f419e9a0b9db7b3c78b5c98927c74c8427f3fcd0<br>SHA256: 3d1595b762a094dfd2f9ac1525dcc77a67ac87dec747f420b0fa63ac4fe51cbb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-10-06<br>IPv6: 2023-10-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.547MiB (5.816MB) – 236,500 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4857bb88f1e540efdbadfb3e56c208c8<br>SHA1: 0190e03fc0543a58ca868f0f36a92556049db942<br>SHA256: 44b7a5f1e09f7ad797ea8511ecfc8ddada844067bdff82f4255273d85906d172</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.24MiB (20.18MB) – 249,120 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5105fe9bbe5d0ddc9bf8995e1cd8fdca<br>SHA1: 48b9366c0983f8d70d79ad112999057d17d64829<br>SHA256: c10da1d1999f1867044c9753957966c4989400bf25df0e7fb02c524b43dc90fb</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-10-06<br>IPv6: 2023-10-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>171.6MiB (179.9MB) – 2,803,356 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4abca24edbdd7d97ffaa621ecb9327a9<br>SHA1: 97c24a0d18b54cd8d2692e708765b79162107242<br>SHA256: 903407a226a3eb479f2165ba004762c64c3a41dd5a9c0d515be1353f99e5796a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>166.3MiB (174.4MB) – 1,448,721 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d928761a3b79f2ef6c55ec6d4dd813e<br>SHA1: e7de15f34cace41d4332e3d59c8ffe729fc2f8ec<br>SHA256: 613e34be98c76eab733c9982022bfa16a5d1ab57fd73444f0d6e8a2ef59ae567</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-10-05<br>IPv6: 2023-10-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.18MiB (10.68MB) – 434,458 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1989bef3cead626cc3164752796d9d82<br>SHA1: ba2e093ea9e2365ee2a004368bbf663e99723590<br>SHA256: fd9748bd25d1324d5f0bb40713323ef934dd108e3cd423ba0b08f1930c4acb17</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>19.08MiB (20.01MB) – 246,995 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db8351f00ba0297ba91db2615f227b14<br>SHA1: a1ed07a426fccfc3a17319c431a2baee664a58dd<br>SHA256: 87677ec473ab7081cf2449e6e25bb61af6036fa32b78374b37248842bf67f5c5</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-10-05<br>IPv6: 2023-10-05 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>187.1MiB (196.1MB) – 3,725,647 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b15c83578010722ad6fc4459854d434<br>SHA1: 3302c4876ca221fb79cbedd51823c13f83309f25<br>SHA256: 8b49532a0369d7ab7ffe11dc3634983cd787ae4f028242a5f09f83e79a0b0e4c</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>218.1MiB (228.7MB) – 3,725,647 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c318177fa92a99fa31662fba65ace50<br>SHA1: 58d2e187a58945eacb10b5a2bc1ccfc966a2397f<br>SHA256: 47b0b86b0f127eb3228861b7ed6dadc5e224b5cc1d0a5e1b737f864aebcf66ac</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>193.6MiB (203.0MB) – 3,725,647 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f29e04335998e52fbc143a6aa9a7699<br>SHA1: 7101ba845f2c49b27041c0815cd081eac8d74564<br>SHA256: b9f6010fd994d2a8b1952e3bfa8b403b7a4e7480d4b1e6c2a79279f56f51210f</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>199.8MiB (209.5MB) – 3,725,647 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9548bcc64b50682716152c66fd771b35<br>SHA1: 6a86a4e4ec7610e0eeae8853ebfbc664047873fe<br>SHA256: b9d1c7705ce969bd8ffec5d9b4f5c29fd7140a312959a11048ee59a810972629</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>235.1MiB (246.5MB) – 3,725,647 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7f601a037cb7a1695f768d9fb386248<br>SHA1: 50b3a9d67795aa30d5ec7663f2b6934742f18f15<br>SHA256: 5606b23235dcd984fb3d892aff0c799c84ac1ecba8cfa88ad503dd50e8958d68</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>188.1MiB (197.2MB) – 3,725,647 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 500237d16a962e10c072a6e7e34b8908<br>SHA1: 97c539b6fa7f8d873845ee38c960373f0e89a10b<br>SHA256: b716bd4bc0a0586cc6ec66d502bfb5a5c5ef304b73ea3af61f8e326fce31f239</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>234.6MiB (246.0MB) – 3,725,647 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a666f74a36168f9a31f9bd9a9a7f4e5a<br>SHA1: 4990a7c13b07cdac648168fb0e0af20e31e27105<br>SHA256: 46c7912f7f1a1a398fdf023f865b9b966f5b4a6cb9c282ea63b33bac6d81e081</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>200.1MiB (209.9MB) – 3,725,647 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37ef86aee713776209663ce9ffcd58b5<br>SHA1: fb3fdc2a6c685c1d49c67c0274d36709e8063638<br>SHA256: 19c6376f9091ea92825a4a3b20a21024b8d3f1f2d5c1a3440419a0eaeb2eb488</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>118.0MiB (123.8MB) – 1,173,403 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9443fe74886d634d880f9063462eed5a<br>SHA1: 616c71823f03df2d60f7b34945e10504ebe714c7<br>SHA256: cf9ef71551cc1f80d3d1d2b74b6fe010421d785022dcb2aa297481a29bed8f26</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>125.4MiB (131.5MB) – 1,173,403 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efd472cf7aa9ae4c6e4e7ccb364d995f<br>SHA1: 1daaf67a1e3516aa266a510fc565bfd38b044a0c<br>SHA256: 8df05db2c1bf6c6dd90044b51f0b95344d952f91f9b3721ada2e016a454ea141</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>120.0MiB (125.8MB) – 1,173,403 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb65ab38807be082d843c405ab38d5ca<br>SHA1: 86aaf1aee376ea552460f0189fc10abcc021201f<br>SHA256: 7708a38bfa911ac8acb62278aaa94c07e6ab42c61e5a26a71076a58fe97f470e</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>121.6MiB (127.5MB) – 1,173,403 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 588898393f966f9d2aef53bac424eb3e<br>SHA1: a79237589eb8b308d137b045b22d2bae73e95972<br>SHA256: 75cd610c1b4a735094579349668e3077343c22f931e6b2c66a9540480426d7a2</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>128.8MiB (135.1MB) – 1,173,403 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4de3fb1eafd862217e914be7b7a2767c<br>SHA1: 9725058edce0ce8b1033b45dc5d17c71a8355656<br>SHA256: 3166f7a146de5f00bfcbe86457536e483f5b8e8b13cb68cf5bf1aa0e88d3d285</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>119.0MiB (124.7MB) – 1,173,403 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c07ecb1a281d1cf84278f3a42c9a29d5<br>SHA1: e1642d096c372ee06f7c0e9864e8e69f73bb6295<br>SHA256: cfd63762b8f05992cdc8b11226004ee006d95a18a630c000bee481868c9db687</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>129.3MiB (135.6MB) – 1,173,403 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ebd8edf9c538a2644651429198dda915<br>SHA1: 101305040717acd7ed8e4639d5c5ebde57bd7df2<br>SHA256: 0ad784540edea0ba673880db47b4ca7ffa7b7ed3cdde5652557f2d736e0b6487</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>122.0MiB (127.9MB) – 1,173,403 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25823504df9b76178fece2b4cd667744<br>SHA1: b8507a3ac1fe2c31c3a79241f2ed9ed780864df2<br>SHA256: 031696e9fa2a5c343cd94851aca93dbfcd9d14852bc13b03da4250cab4d15e16</pre></details></small> |


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
