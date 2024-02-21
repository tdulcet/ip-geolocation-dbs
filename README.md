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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-02-21<br>IPv6: 2024-02-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.808MiB (5.042MB) – 240,698 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52578b9c7754d2e781375a39fb5791b6<br>SHA1: aefd570e55997dfe9a964a528cb1b74fe542b1bc<br>SHA256: fccb54ec8d699db4758ade81ce4683547828908baedc32d5c6fcefe940016ded</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.650MiB (5.924MB) – 85,861 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44d098802bf13a98bde33d9e42fc7175<br>SHA1: 420106b04d160ec773188083a2aa4012be0b6e65<br>SHA256: 928c8953f9c55d411db3e1ee7603a1cd5cebe1e32730e76d4a1bbbe13c7161e3</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-02-21<br>IPv6: 2024-02-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.193MiB (8.591MB) – 410,282 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0571a20cfd62ef46d2fcd489c8bf116<br>SHA1: 2af79bf9764a165901791679fb614e690afc8d4b<br>SHA256: 578cd34545af887f0dc883854ee6492c1ba2038a5671b0700fa255a1e82722b8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.987MiB (7.326MB) – 106,295 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6aea32487b8d008669a391689675fcf7<br>SHA1: 134a7b162f1872bf8f92cfee376b8249c22f05c0<br>SHA256: 24e4efb67b1d5f2b0118b4fe94b454f433d4cdff794418caa20ebf1267a48a0d</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-02-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.15MiB (17.98MB) – 858,611 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 345b63c43bb684a472227b25725dfbaf<br>SHA1: ca57eb877340935285cbbdba41d9d8aa869f318e<br>SHA256: 4d68cc72d11631140466ecb8d6fb31fbb4554424b05a0f230d9d55cbce6b26df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>53.07MiB (55.65MB) – 806,460 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33f56c13391aaca3c39bcda8c859d4b5<br>SHA1: 07a5dc484aab6b660bb85ff3c969b0669dfe39be<br>SHA256: 0df489f663076c5ca3dbae4d72f2e2c5fac44fb19fd19922fb49eb87aed6f8b3</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 322,238 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58dc67267f460ea3cf5cad59cd04fb2<br>SHA1: d7cd4a637354f5a5c457e96633e1f5c9cc5c059c<br>SHA256: 55313849f9b0eeefb503ca58aa485ebe95d325c7771a4b2e5e9def19ee8aa2f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.67MiB (19.57MB) – 283,667 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b73dc10990e7bef8c444f1cde6991f<br>SHA1: 07ae49b41bae3e257ad578c4bf31ee8040ccf1fa<br>SHA256: 7ea6211e834aaf328302ede30e6777fc4f71afb40ab1238cf0af2be151b5b248</pre></details></small> |
| | | Full Location | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>179.7MiB (188.5MB) – 3,143,531 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4796f68669fd62ff1776c3d247e13dff<br>SHA1: 8d63c70c0bd62e8829cfbd2dfba8d6b8e6c77fd0<br>SHA256: 04e5000cfd1d52386cf975f825886bb214085c10b75c2568efa51ce70fb6c3df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>291.6MiB (305.8MB) – 2,831,720 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 657b58a340f82d12479e96ce7f695a45<br>SHA1: 1b9c4719ee91d1e9da68e6f0dd1529e893bf9777<br>SHA256: fbe98efa467387f6ceb69603459abde1562d03903aa05b063edc68d9aa4e87d0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-02-21<br>IPv6: 2024-02-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.640MiB (4.865MB) – 232,256 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fec6f73486236c8d0d94598e079d6f<br>SHA1: 7f19645a2e7ae1f5579b6769363477a0ec58e5f6<br>SHA256: 7f7145aa700bc6d9b86d8e430377fb6751efd3a786e0455999aabe3401d275c5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-02-21<br>IPv6: 2024-02-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.9MiB (177.1MB) – 2,925,251 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434c9a2a5a5c869e663a7e206ad5962c<br>SHA1: f2e0c48f3ecc7d10f4697a8c5c698e1979b08714<br>SHA256: 8d5321147896799a07280f735aae4be97a74bdd31110778527dc8f4b77485f61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-02-20<br>IPv6: 2024-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.435MiB (9.893MB) – 472,628 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 994e949185d43585ad39c1d6de567c83<br>SHA1: 99f072e5269819925116b35ec03a8fa1e4cecfa0<br>SHA256: 2ccf54b9229687c7de919d6b7556a9db76619494be4625751472f7aedee5343d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.68MiB (20.63MB) – 299,025 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb1944754f7e93e84a4d31642d5341d8<br>SHA1: 1b75a97025ff2292a240892494742445e15554bb<br>SHA256: 286281f7bc690acf0509ccd34dd146a3d54b28d3a2859ea8c3595124fc67184d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-02-20<br>IPv6: 2024-02-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>148.1MiB (155.3MB) – 3,148,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1153ed12d1f718fbefeabf4fb0ca3b73<br>SHA1: 272c554f40e65953c431c232f8aad5f46235942d<br>SHA256: 0aecc0b6098b0553646ebda8e8abcbdda7674bba177d130e0b2947ba2feed41b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>171.9MiB (180.2MB) – 3,148,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16e8eeb0f086c4ae0651368f62bc81ed<br>SHA1: d13418d2bf8cdb68f7254c12ba10b96183cb45b5<br>SHA256: e1f725775feac80a24dcc027dfbf1a7d566026f923d739f843e11e779464d00e</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>152.0MiB (159.4MB) – 3,148,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5c63e6c9d31364ae035acf1d7f624c0<br>SHA1: ba8fa260e7b8ba0d592725c57bca74b4e3fd1434<br>SHA256: f0b6f5764a3517497faa9d3b1cf4a85c4dcd39d48a97f93efe1e15a1ab8f8945</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>157.8MiB (165.5MB) – 3,148,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 842a5a1c33103b2221456b29e5b586b7<br>SHA1: ab03e3ce683e4934b52744348f2b42c3eb95ba14<br>SHA256: 4b38f825f414de736dc15c5006de58d0416c32da9a2e61669a90e7fac4985ff8</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>184.6MiB (193.5MB) – 3,148,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfe7b49bb2601b630c74a92ff34a2034<br>SHA1: 632e682e63c4d86996a47c6eb0d7746acb70d659<br>SHA256: a14822eb47a463952bf9aeac4cf3a16631d61922a3ab87cff35126274bd6847a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>147.1MiB (154.3MB) – 3,148,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5da8e38652ae2443223e7e3ced684d6e<br>SHA1: 519c7ec31a184eef2fb4b95476775b6b41168125<br>SHA256: f3b3c0aa6d2d39d3ed68e25e41450321782cac779ebead3ab92cb819f34dfd14</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>183.9MiB (192.8MB) – 3,148,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f13c2471373176660765ec81cfbc5d1c<br>SHA1: a2afd21157ddb323f8c6a08bf62a40bafc6be818<br>SHA256: eaf8452133c5e76f9dadcc86f2c852514d725987397cae862f6e51a4992eccad</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>155.3MiB (162.9MB) – 3,148,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64ddb43b3b8c87c734d50961b4aa76a7<br>SHA1: 1bfe3eed94d9271a3d87c876b9dcaa072acf0787<br>SHA256: 01fdf8dce2c0e02b0d0395e5c64e87401954bba47bd9da10dc0b0bebfddd45ff</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>102.2MiB (107.2MB) – 1,136,624 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f84cdadd15430eeb069bf569728d07e5<br>SHA1: fddd5a992096190b49f6f7c6e6382001bfe16e23<br>SHA256: bcf4c0edfdf27372acb5423086075e858ceba3f2d14951839cdff4502fc15857</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>110.6MiB (116.0MB) – 1,136,624 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f897c259753668b4aeb9dd87c203ac56<br>SHA1: 349a5c9b8f2a5ee8e9609aee7c0e223fa16deb29<br>SHA256: 712daffcb3714678fcfda35d7c0416d535c2e15b9e763f8170acbc8492dc1bba</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>104.8MiB (109.9MB) – 1,136,624 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03b56551ae6e201100a2b7897d3c8c96<br>SHA1: 33fa1a9884808560e26a081e57b7feebdfe26602<br>SHA256: 028170c2fe1bd188ac8b10d51e7c8799707ca179ce832b1391442fd48acabada</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>105.6MiB (110.7MB) – 1,136,624 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 324b3a3441eacd4e1dc2681ec1e451b9<br>SHA1: 5fd47bb369c7cdb8749ff93b619c7b96fd83f880<br>SHA256: a041df7f1edc3a25e4f6124612c2d5edcf9b7cc51984c3481fc19ac97edea70f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>114.4MiB (120.0MB) – 1,136,624 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e5fb4db2de9d724f5ed0f1826aead9f<br>SHA1: 49c2b37acdf06691569a393e32b8f10b9868df68<br>SHA256: 0bb25e65252a15bac775f6817c3619c0db7cbb474441ac87600fe3f3aaf9644a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>103.7MiB (108.8MB) – 1,136,624 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6303dad32cf137063440fcf0860a79c0<br>SHA1: 5976d156e2d00afc78cc60d86d32757c8fa05e06<br>SHA256: a25621d505edab84d98b13f0323e1bedc1c7b8fd742d76b0e844b104258a0695</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>115.0MiB (120.6MB) – 1,136,624 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45fcde6b602aaed1e740f7a77c03aeba<br>SHA1: d8970fb48e32542bdf86536548ebc143e5c974f2<br>SHA256: f5daa92a37c0f1db5a0ac68dc178ba02a0183de63dea6af07393ba4568ace3a0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>107.0MiB (112.2MB) – 1,136,624 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73fb7172f1f6982ada997a48ad9198f2<br>SHA1: 771020388a40e48d0beae1ff4350c489c49b91cc<br>SHA256: f4211a95fd26f14387a9ae7bd479d3d769805c6af21be5922cac5b5b620e304c</pre></details></small> |


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
