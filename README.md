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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-11-23<br>IPv6: 2023-11-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>3.196MiB (3.351MB) – 135,473 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d555f6190e4b265d51a5714b7bcf5f9b<br>SHA1: a57d48754ca36ed34d63878ef7285616f909d651<br>SHA256: ef47411c98ff44c51a91cadcf3d0dbe8cb695081422b0f0065da65c0b56e35af</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.332MiB (6.639MB) – 81,964 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14f732081abe94bdc6f3c61a33c807a3<br>SHA1: 27758f7a1fed89b5424502e426f8631df2e5c01b<br>SHA256: bcab2fee5b91c05cfa0729ecabd4c1b83a4c507a04d24c13e68b41975aa0e413</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-11-23<br>IPv6: 2023-11-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.669MiB (10.14MB) – 410,695 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2950c463005c41bf05b2066f1fd4a13e<br>SHA1: 5b0941d7dfdaa000c20e3ad65bce54ad27af6eb8<br>SHA256: 936790a6f7e5f184993ac453ef44b5398490e7b9017053639877417a58245be4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.053MiB (8.444MB) – 104,347 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8d6a0d17c19d3640280986396c0a84e<br>SHA1: bcd53782f7ac102d489f70cf5328db4b07eee523<br>SHA256: fe82b61de60bc404468c5275844d74e6216fbf1a81f850c90e15f15671758c25</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-11-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.87MiB (20.84MB) – 843,679 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4824cc6419ccf88208fdf718a7fca18<br>SHA1: 987835d7b3544fe6f07ce7352bb95201745e5c82<br>SHA256: c8751b1b896ae78365e9a7cf37aad90e17ff8402376a12eb662384e078ba57ff</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>125.6MiB (131.7MB) – 1,626,322 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88485340d25f11846d46d6530ae7a806<br>SHA1: 72b46f5141fe05bcc8346d1784e16b772373b0e9<br>SHA256: 897f52952120d08252460653780ac783bc6830595ce5e5f471858d7b460bd339</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.260MiB (7.613MB) – 309,964 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d7fc3106cf6c65db7d44df8b4fb1d16<br>SHA1: 6ec97588db0af32a305835217289c32883d23f64<br>SHA256: 9bc7152bcf323316fc78e69cfa190cbddf22834208f48cee2e624c18150c9478</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.63MiB (26.88MB) – 331,798 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 264a68f442d85aea134072d7bca0f4fe<br>SHA1: 65171ab00588cb7f2ae029d9345b44cccc888d24<br>SHA256: f76d40c34e6881d9cf3d98b34ced8105e9bd9efbb3f55e2bc224ece181569030</pre></details></small> |
| | | Full Location | Monthly<br>2023-11-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>186.8MiB (195.9MB) – 3,075,320 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96e5fc94ee00f3349281d3d79c8e3e83<br>SHA1: cf6b55598525f02890d9596fefd546190401adc9<br>SHA256: 5dfdabdba40afb770f6ff5afcc35db6136e9e28182bd6b3fd23b3c203dca5d1f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.3MiB (303.3MB) – 2,504,397 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bcf1dc4f4611d3e39906c6048aa8fc<br>SHA1: 2cd36733f3043bb3d9985d20fa8416a68b122e30<br>SHA256: e3d5ccb9e02dd929dc48ad40f82d484f9ffe60f9098c5a3ac296e33c5b9c2a9e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-11-23<br>IPv6: 2023-11-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.446MiB (5.711MB) – 232,323 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f7d79b6a3ef8bc35c3c8381e7c028<br>SHA1: cbc8e9cbd5c151f0cdb02a21e5e6fe9d8b662cc8<br>SHA256: 9f3976e09ec875d7e97185503221656e80f41f531e268da1bbf874127de2583e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.41MiB (20.36MB) – 251,316 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9df2ea3be7027267ebb1947b4220cc4b<br>SHA1: e94b6a993297b5dff456113130c22e323534e39e<br>SHA256: 44458ed651d7b4bd99ad73459d500395c410da1b2fce9fbb2c4e5ce318c4bcf9</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-11-23<br>IPv6: 2023-11-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.3MiB (180.7MB) – 2,814,468 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25688ced507227d7990066c41a0d58d6<br>SHA1: 28da5022ff88d543bba4e15cc01b703781801bba<br>SHA256: cf219cb6d358d6e4df364a87f28817e4aaf8322370b86495ef74cc1941c73f5d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>171.4MiB (179.7MB) – 1,495,017 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6d4ab0c657ede6538d2756cef356f5f<br>SHA1: c2865c0d416ae7143165db8aca21627725b4b45c<br>SHA256: 66022701ed347d75f4f400e76024ae545696e742e4c0fd30bedf981c262b318b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-11-21<br>IPv6: 2023-11-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.62MiB (11.14MB) – 453,446 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a327fc20086d782e18d38e31225ba9d<br>SHA1: e3f33348ce425317fdf1f4ea648e1d74e6cf92c0<br>SHA256: e72e7b564e35bd1df0c93ad103b5d564ee867bfc3371ca66354df98c6b6c2750</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.35MiB (23.44MB) – 289,329 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 026013cc20b22406a69e78d4c953df80<br>SHA1: e4eadb37e0a00ce6628a7b8a24c3f4bd58ebeee0<br>SHA256: 478eb0155f0054728dacdaf196d987d00c753de223d7b002a5d8e64f9d4f1d3e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-11-21<br>IPv6: 2023-11-21 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>163.3MiB (171.3MB) – 3,238,258 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d6027186ebd2b406de7831c0ea2b8f7<br>SHA1: aa8c08ec2022df28b55f51925a22f124ca3dd2c7<br>SHA256: e0a07db115802d0887443dac481bb79fcb525414af87990e592ee485e4799334</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>189.1MiB (198.2MB) – 3,238,258 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4ebb7db8cb4d3371bccbe6ab69a57bf<br>SHA1: 8b5a256425e0356a05e8bbada4584f2ec05000fd<br>SHA256: e0887b7b225f9f0ac5480be8940273106f4b0a100b5e602efa40816e54ec0a33</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>167.5MiB (175.6MB) – 3,238,258 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe5c8b86c23b3f8ba5765945d05fe114<br>SHA1: d32f51038737a60eac07934b175c3fb6f07c9fbc<br>SHA256: 566b65ceb599d511a0a547b924ccf7380ec825dfb86b9266f2e3aeee47f94e6f</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>173.6MiB (182.1MB) – 3,238,258 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b195423ba82a75441a9dfdd1e25f7929<br>SHA1: 56366061a184a110fb0804bb03eacfc8742f1963<br>SHA256: c5762ebb8c016f9d6309df9420a28cc29c3b341798c0fa29b30c2e9ba4dcc3d5</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>198.3MiB (207.9MB) – 3,238,258 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c082ca9eb78065ac482e800a9ab15d3<br>SHA1: 4614449dfd6f26df1de38441c0aff8f548546185<br>SHA256: 305a20be0058afc1a896f7a3bd4fffc740f0897fd7b5753444c705c8ad31dd1f</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>162.5MiB (170.4MB) – 3,238,258 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5ad98176de039ba90b7ca963ca43120<br>SHA1: 7bb11639d85afc6d55f4509ce66438bdc366e2bc<br>SHA256: 23e7031668bb60963b5833d42dc01a0bd2f757ccf3e17398a9cd21cad8e375e2</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>199.9MiB (209.6MB) – 3,238,258 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82457f5702ea7bbbb28bf52cfcb8e714<br>SHA1: 504a7792eccd97c1420fe0668078bbdc59939d1d<br>SHA256: 341f30f1be74c7c8cfda4928d011367fbd6ff93501a132dd93cf9597fc69ec78</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>169.5MiB (177.7MB) – 3,238,258 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a0d16af9b2f78d2ff0f33b467abbc3f<br>SHA1: 3a99e22bd9dd177c8ec22e01e60a9b8346714bc4<br>SHA256: cc28b07e3d1ff1e7551ff21d68e4e1271f5280924ac28a1ac0f7d1429a636a9f</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>124.4MiB (130.5MB) – 1,237,238 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b2bca67d0bb2af5c02468abe26d204<br>SHA1: 756d5d1551f47b45d534dded8a60370b5b83cca8<br>SHA256: 05d0fabc387c6d4cc3d83539640eb855c6672a74152e7b011737380ad2e9cddf</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.4MiB (138.9MB) – 1,237,238 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eee0d1ffd6b2ffb92638093bef4e7e03<br>SHA1: f09437b29f64ef258b60bfc0ade0eb6b6a31b6e3<br>SHA256: cdf465ba941f9fe557fff1bdf98ccd95507f1bb912c55de42e59b97ddac7451e</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>126.7MiB (132.9MB) – 1,237,238 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e900750bc9d7b5537d3458f5ad21098<br>SHA1: 21ae5a214659836ef68ad9b9822dcfd917c7a1bc<br>SHA256: d7f1ba02435d7072fadad861fd30bb5f352dbcebda7de01b8ce4190d7093b498</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>127.9MiB (134.1MB) – 1,237,238 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84d5586f37b77133649ec87e85e711b7<br>SHA1: b0fff507f579910935b9808c2b13cdaa6de7955e<br>SHA256: 3b4274001b6a550075652bca144b5baa160f953b6f7bdacc7b867bec9fe3da18</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>135.5MiB (142.1MB) – 1,237,238 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b7fa6df00d97bac7b15e98660eaab96<br>SHA1: 9ee29f93e64db85cac3f0c5b6bc4d61d0ca34038<br>SHA256: 0e1ad21156e2eaea60b3e1df37606f92a6ca11eff3910bebbf23cb80102fadd0</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>125.6MiB (131.7MB) – 1,237,238 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 314ce9d80035d9b7c81219dedf22756e<br>SHA1: d4171d42486f3f209327cc14810caa4160804a63<br>SHA256: 911376904ffc0e1ed40eeb490c3433ede74f910ef9c7428c115b16414f73c176</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.2MiB (142.8MB) – 1,237,238 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04f42c9065c873f61aa573c1a31c7e20<br>SHA1: ef766b59cbf4b314afae33de9386d4ec2bd7bb7d<br>SHA256: 8ecf2ca74f4298d9cda9a91a7251c3629c8905ecd6f4a190ebf1d4506e69f9b0</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>128.4MiB (134.7MB) – 1,237,238 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79e4dea7a3af65d788893d2133b39772<br>SHA1: 420c3abf9af3568ce11ac37d5d1b47451b8e8bdc<br>SHA256: b3cf8af12d99bee0586c479b6400ac0327a162fc668ea9df35d54add9033f3ff</pre></details></small> |


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
