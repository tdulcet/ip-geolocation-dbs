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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-08-16<br>IPv6: 2026-08-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.444 MiB (5.708 MB) – 272,425 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a90a786845d6ecd90b10c2629fcc3644<br>SHA1: 31b89ed5b511fcba45843aadfa78f61e9b4b371e<br>SHA256: fa164a04c9c62e3a4c6a1bf492e648fce6311729df771463a25d1f7aa68f6b53</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.54 MiB (17.34 MB) – 251,323 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d0adbf1619dfc43e3813c75848966f3<br>SHA1: 34281618e5dc02a3d8cf00ec2a01e870581ab04c<br>SHA256: a302002b753e30da92565c2d6f2eb921d7b6d573bc67a7a938e9fafd56efcbef</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-08-17<br>IPv6: 2026-08-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.055 MiB (9.495 MB) – 453,362 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d10507b71978944251395f81172e72d9<br>SHA1: 85b3bb590032b96dc80b8e0853439f94a8d74b0f<br>SHA256: 8e6ffeb4ba577643c03ea2bbc25c80f8889ddbb8cbb57c70e4efcab7653a0181</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.996 MiB (8.384 MB) – 121,628 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f279577350a9e1586e8ea70ab6718fc<br>SHA1: 8ac6ab8bcc18a6be2ca30c766bde11e4ece74538<br>SHA256: a002c4eb29c06e8b1cbfb581ecec46ecde07835b277aabce5c48115d9a5ee647</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-08-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.28 MiB (12.88 MB) – 614,813 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3571db85c78938994b829457da71df4<br>SHA1: 2d51989c333f4888eacd644db16b5add88db44e0<br>SHA256: 9cc7d3347781726d4a71f2e60429f950368c77e6f295c385b13a6e3a5ba84681</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>44.65 MiB (46.82 MB) – 678,501 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55f48fc6c8e26369a4c5aafd3922c3aa<br>SHA1: cdf36bb5f81ee0daa77e3455f64bcbfafc395652<br>SHA256: db33418607543024174986861d99fc94ea297c421c065064b50771d59a0cb347</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.149 MiB (7.496 MB) – 358,140 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d3e21d2da14fe2fa0da1db2f6424311<br>SHA1: f274f58aadcfa3311603218b88e8b24a01671e36<br>SHA256: f62294be209c966f38eb82e27717bc64116462241210756e85c31429048d1f96</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.92 MiB (24.03 MB) – 348,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60cc96dd0eef36fef003b9981e7aa19c<br>SHA1: 077fc11bdf3b1a16ed5a8e22cb9889e86b007cf5<br>SHA256: da4f32fc9e285ea393eb3d4fec4fb4a153874623b14fc77373e8f448758ac135</pre></details></small> |
| | | Full Location | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>208.4 MiB (218.6 MB) – 3,652,137 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68a79460a812a271884a0a50858ee1f8<br>SHA1: e1cb26165f0fc2b394c3f08d99642d1e5a3e653e<br>SHA256: f40963b044ff4637dff7dd3608244f6e065cc97e9bb7262d5fea4abeed6cf026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>440.2 MiB (461.6 MB) – 4,274,498 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e9801b97694446ef740a7093d24488<br>SHA1: c8e28d1130d3667d5b313b6e468c5d9d69ffb027<br>SHA256: 88971b264e462d0a2d37d85f793d5e488192b4d883a1ad0142a7c28d9a60af96</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.716 MiB (5.994 MB) – 286,131 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d282e141eb5464b8254973895dd4a19f<br>SHA1: 43ed365a77bcc1acf8efbfc3769c01a237bf775f<br>SHA256: 436d012d7deb50897534e496aeb1616f14ea008640929405f2664f5122ffbbe2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.50 MiB (23.60 MB) – 341,989 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51aa8116a79265830a4cc7cd4ef86053<br>SHA1: c18af12e87abaf09ccf88a3c0de5227c764e8a1e<br>SHA256: 374157270162797a62dd05862b45a4be9f350bd4c2e81ca0a48534910fb28817</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9 MiB (179.2 MB) – 2,958,317 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a7499b08d50db46b5cf9fb15cd346d<br>SHA1: c27a4fdfd31298e65e03fed44f2b36b4aba8504e<br>SHA256: 7e2727a2650e2ae9c6e50b6fbae1b77db0938c91593e6e1e1de5d7e195393e70</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>299.6 MiB (314.2 MB) – 2,903,507 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a92797de8e315b9794c5a75c021c7b8<br>SHA1: 3bad371e9bab711cade7d5e88cc542a34819152a<br>SHA256: 4479ccaf1ffb1b9388ae015e24ea8e3e1780c412777f1ee2b0a30bda83f5d0e9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.22 MiB (11.77 MB) – 561,809 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8bb866d18cfbdf7740ef1c576a6f1f6c<br>SHA1: 958be972cfe685e4a643e91f53f5b4e6e67f20fd<br>SHA256: c38a3d96a5313ee116e6b2a4aaeb34550c624814d21bf1d4415c6f9a1719066d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>35.53 MiB (37.25 MB) – 539,874 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90ef4e2914592dae896a0f8b929b810f<br>SHA1: f0ab70fa4c66eaf03879835bdba7487f00b23e49<br>SHA256: 2285e6fdb8ce87fb999341e6876cbb5c7a827d612f22cbf45b4b1f50348fba65</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>192.7 MiB (202.0 MB) – 3,752,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 380bff4f0c4adf65e14666026b5f646a<br>SHA1: a976c665e2a9ee81b6c1b4f69d9bbd3633add827<br>SHA256: ba59146ae35b7bf7ce0fc92574f9274b9bc6f33a2dddd032e4f94e125742d7e0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>201.8 MiB (211.6 MB) – 3,752,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9d459018cededce53543949dbfe6c40<br>SHA1: d0db246e302f9f7ef24f8df9d5c9bbcd3a99f6c3<br>SHA256: eef83b6ebaa2c446bab7d6c747e89ec6e7e476a321267bc45d63e5e2d46dcf87</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>191.8 MiB (201.2 MB) – 3,752,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f36a87ef69729efbda975a9f577846ba<br>SHA1: 5700a03941d4e5961cada0a7771c5b2c41ec389f<br>SHA256: 4a966b08d5170961cc36b88c2dd5f52fecaaac0088338fc032d5630fd43bfb93</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>193.6 MiB (203.0 MB) – 3,752,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aac34547c1cd3b4e6b1acb2ddf5dd929<br>SHA1: cbcf9b3a230c665622077b0bb61b57b03af3d8b5<br>SHA256: a8360c640a7e450b29cbd9bc6b006853282b022336a550988224b3d943d29a9b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.0 MiB (255.8 MB) – 3,752,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80a2693504c5b68cd1e81bbb054b77c4<br>SHA1: 7507cdda9422c1ad20a0c18c9486fdcd18f1e8e8<br>SHA256: 603004d1d84238298dfd58765e00c4601a75b0b421cd973a499cc3751dfc9b98</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.1 MiB (200.4 MB) – 3,752,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84f9c0698c07000235539cd1811710ce<br>SHA1: e7b1df065099fe1d7ac0a36e6699969861bc2bc9<br>SHA256: 113eb4f4edfaec3801c54f5784a949ca3f1904d221a76d0b2356686039395b1d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.0 MiB (245.3 MB) – 3,752,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd3b969449c559ce98ff279138aaeaf3<br>SHA1: 5a0c62b6b5e10c06028cccc0baeb3f7ae7a1159f<br>SHA256: ee2750044ad127a2a48074b98c0811f6f79b7a5adb940dddcca9f605d8d2a846</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>196.8 MiB (206.4 MB) – 3,752,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2109cb4c266126585a7dc01f4a98f9d<br>SHA1: cca2b2fabf45ef42bde6f6a3359f59f45099b12c<br>SHA256: 18fcbe54f2dfc72dc757b22802059ef2b3c7bb5a74b00e3181203552a22b98c3</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>198.0 MiB (207.7 MB) – 2,077,512 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 076285f5dfcd6de55814bbd467cd4e80<br>SHA1: feb262d8fa5b8527c99a18c8dd927dfa328a9e63<br>SHA256: 0417bce542c77dfbfcd1c00c5f899b4fe7114bccf50f11f995d439cdd5e35935</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>201.2 MiB (211.0 MB) – 2,077,512 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 543ec2b83ad02bb9235c99f0a0dacbac<br>SHA1: 8bb804540dc131b2940f71a7227bf17028b69d4b<br>SHA256: b2ebd9af463388611b567b9d5e669370cdad0c2d662f997d463d0738e6c69389</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>195.4 MiB (204.9 MB) – 2,077,512 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c70707d03acbdfcdfb685dd9689a408f<br>SHA1: 862787d752ac70ec8dbc4b1604ef7207d981117c<br>SHA256: 854abc2e1db25198d08d4e4bd43a5e1acd15c28489fd68e772b4fec20f3233e2</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.0 MiB (205.5 MB) – 2,077,512 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4352bd1ba1dfe90488efa3022498408<br>SHA1: 21de7c5db8c624565cd67c3feec2b06e30087c98<br>SHA256: 2193e19c7145490f55a3be577319d0fdce74e781e88823e830e3156eb062eef4</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>218.2 MiB (228.8 MB) – 2,077,512 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8edf867f04692a6e352bf099592b0485<br>SHA1: 4a29508ad1b04850a79fae6f7bcd6db7f5d59bbc<br>SHA256: 20538a7f2f1162d83138747afcf5fb80c71ca8f24d23ef3ecb895e6e1024205d</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>195.3 MiB (204.7 MB) – 2,077,512 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55e884808cda518df77512df5efb1f86<br>SHA1: c442bec49be271c605acac7505744c39346ec2c5<br>SHA256: f7ec3674ea2d75d45b51b8f7d45366eed01c3db9542bef269427df31a17eb57f</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>216.4 MiB (226.9 MB) – 2,077,512 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a6b83b84551aa5cd3bcaff6853c40e4<br>SHA1: c4d86f77af1eb85b017a95a818c91b974b427a0c<br>SHA256: 9d128560f5de99acf7ce786bfbd3a51a6c0eefbc326e01c834bb8e2832382cdd</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>198.1 MiB (207.8 MB) – 2,077,512 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea65e388a5f2c129c9d6b9270dba4024<br>SHA1: 15b7b9296a4469fe25093da41270eb38acedb6d5<br>SHA256: 31d0c48a02190782309ada337f91ad7cde27f5455a46b90c81d4678eadeecc09</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
