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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-08-20<br>IPv6: 2026-08-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.459 MiB (5.724 MB) – 273,201 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4131ed8dc4fe2af80ebca536253f29fa<br>SHA1: 6da02a1505f6b5e44763d81fef9038739bf2a59c<br>SHA256: 014fc0603adf6b604ebf0bc9724b4ec641dce2c73440d6b5bc07e49c3c2f74df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.55 MiB (17.35 MB) – 251,476 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a5cea9cff7bc9542e5aeeaecaa06cc<br>SHA1: e99d8b677d63e3ac3296cc352978ca94ff2cd02c<br>SHA256: 96e7e28446182007a3a9151bb8078528f21684a3ea812ffaf2209462cf3c14e8</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-08-21<br>IPv6: 2026-08-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.056 MiB (9.496 MB) – 453,435 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17a57b6374f4e68848e6f1ad53264c7f<br>SHA1: 9934f377ec102fce27c3d853eccd3df576c47551<br>SHA256: ce41466e45acb29609ce81283d5d8beba348570dae328ee7c358f4db0a5239e4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.008 MiB (8.397 MB) – 121,810 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b6c92ba2a91495227909b29e5b9c4a1<br>SHA1: afd835f009d8fb436ff76dce6df25e2a090a3489<br>SHA256: e8424e82f0f53eb6d0a11d21f057ab033f4ab40ee068a5de432dba7ce72384a1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-08-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.18 MiB (12.77 MB) – 609,769 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9d6ece479654213ee5a4ed3e2584d29<br>SHA1: aa2a4cc9d056736eae4a76552e444e69c5759b3a<br>SHA256: 29b133808c0f88cada43a592438ec2c6fe057822d1da232c34fca81dcb4f8468</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>49.59 MiB (52.00 MB) – 753,597 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cb6423266e02e20a29fbe557a1e9b92<br>SHA1: 249b8e43d7926d966addc0b876e1eaa324007c38<br>SHA256: 38cb914136f47e168953dd983e81d986cf9c4080e8adda2c3dba06485fa8444a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.149 MiB (7.496 MB) – 358,140 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d3e21d2da14fe2fa0da1db2f6424311<br>SHA1: f274f58aadcfa3311603218b88e8b24a01671e36<br>SHA256: f62294be209c966f38eb82e27717bc64116462241210756e85c31429048d1f96</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.92 MiB (24.03 MB) – 348,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60cc96dd0eef36fef003b9981e7aa19c<br>SHA1: 077fc11bdf3b1a16ed5a8e22cb9889e86b007cf5<br>SHA256: da4f32fc9e285ea393eb3d4fec4fb4a153874623b14fc77373e8f448758ac135</pre></details></small> |
| | | Full Location | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>208.4 MiB (218.6 MB) – 3,652,137 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68a79460a812a271884a0a50858ee1f8<br>SHA1: e1cb26165f0fc2b394c3f08d99642d1e5a3e653e<br>SHA256: f40963b044ff4637dff7dd3608244f6e065cc97e9bb7262d5fea4abeed6cf026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>440.2 MiB (461.6 MB) – 4,274,498 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e9801b97694446ef740a7093d24488<br>SHA1: c8e28d1130d3667d5b313b6e468c5d9d69ffb027<br>SHA256: 88971b264e462d0a2d37d85f793d5e488192b4d883a1ad0142a7c28d9a60af96</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.716 MiB (5.994 MB) – 286,131 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d282e141eb5464b8254973895dd4a19f<br>SHA1: 43ed365a77bcc1acf8efbfc3769c01a237bf775f<br>SHA256: 436d012d7deb50897534e496aeb1616f14ea008640929405f2664f5122ffbbe2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.50 MiB (23.60 MB) – 341,989 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51aa8116a79265830a4cc7cd4ef86053<br>SHA1: c18af12e87abaf09ccf88a3c0de5227c764e8a1e<br>SHA256: 374157270162797a62dd05862b45a4be9f350bd4c2e81ca0a48534910fb28817</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-08-14<br>IPv6: 2026-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9 MiB (179.2 MB) – 2,958,317 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90a7499b08d50db46b5cf9fb15cd346d<br>SHA1: c27a4fdfd31298e65e03fed44f2b36b4aba8504e<br>SHA256: 7e2727a2650e2ae9c6e50b6fbae1b77db0938c91593e6e1e1de5d7e195393e70</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>299.6 MiB (314.2 MB) – 2,903,507 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a92797de8e315b9794c5a75c021c7b8<br>SHA1: 3bad371e9bab711cade7d5e88cc542a34819152a<br>SHA256: 4479ccaf1ffb1b9388ae015e24ea8e3e1780c412777f1ee2b0a30bda83f5d0e9</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-08-18<br>IPv6: 2026-08-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.20 MiB (11.75 MB) – 560,962 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9e100038fc76d66bac0e291d7513306<br>SHA1: 5d1e8642c2f615e56e2bda6193457809dc27a3ac<br>SHA256: b243ccf7f4b5bb10526cf48bb4eac3b2375ee15935055ff8dd230ca1bdc31141</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>35.01 MiB (36.71 MB) – 532,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82601410c1444f56dd370491480bc500<br>SHA1: dcf79c38b22164548b37878a7f9f322c1b9dfd51<br>SHA256: 27443593ded9e611ef544f706c61999879af68dc2c235ae55184cb888fb81cc9</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-08-18<br>IPv6: 2026-08-18 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>190.1 MiB (199.3 MB) – 3,703,735 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16972c7a69d319b6858b2c8f762a6cdb<br>SHA1: c46d002536c3a412477e8002fc07a8f4e68d971d<br>SHA256: 4456ac82e3b9ffeaebc5d273947ccdcd224946d69378b07cab0470d683d9259c</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>199.0 MiB (208.7 MB) – 3,703,735 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ca1ee96a50bcccc7879f1992b4fbb20<br>SHA1: 5826114ff478f04c9dffed4136e94e82624849de<br>SHA256: 8fadd2575d5e47ffbff333573680e2fa3edc05ca6c2247f770afa5faf296f6b1</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>189.2 MiB (198.4 MB) – 3,703,735 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddd0cb3ca04b450323d141ac7e81a728<br>SHA1: ca5e7eec3e100050eaeaa461fce5a5e0a959115b<br>SHA256: 203d793d9df070d0439a66512f59396e14a7cef5a20af3b484e426ea7882de4f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>190.9 MiB (200.2 MB) – 3,703,735 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2c71e862b0d882469fffd3880691a42<br>SHA1: 95eec672410985a940e4145a86b071fa9aa90813<br>SHA256: a9a4e0db00445e681542f70400f775a6fbf188efeb3c2ae03fa46dfa66d1e6cf</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>240.7 MiB (252.4 MB) – 3,703,735 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b80fd956bbe0df0abd1ba32aefad8248<br>SHA1: dbb8eed5d4507114d04ebe1e4477c0745da18c9d<br>SHA256: bcd41784955e8795f5e2c89e429343398f3f69169cb23c5c65fd929d23a15477</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>188.6 MiB (197.7 MB) – 3,703,735 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ab7f06518782e565f6a0d4a78706a3e<br>SHA1: 766a7f8904c548da83be28b9835a934e3b5c67ba<br>SHA256: fa6ab0cd2413bf33f30b3ba388c47a74dcaf711fd51c93e604dc4be43e2969d0</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>230.8 MiB (242.0 MB) – 3,703,735 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9da839c50380fbe03223a46c3837af24<br>SHA1: 62020d154839b2391da957388733411a5253e323<br>SHA256: 02e7664c3150b86a0baaecf217c366ff622b1673c8dadf5cb4f072ca3afcf08e</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>194.2 MiB (203.7 MB) – 3,703,735 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 834038eb5f77b3dad37a75ba06fc7551<br>SHA1: 77c1d9681a7393cd36e0331e30c8a7e70a63cd26<br>SHA256: 7740f768f20fa1b1dc75bec542e21d252c2fe94dc34519dc1a53bb5b88525c10</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.1 MiB (208.8 MB) – 2,083,176 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ffb7252eab142251570a7f9087a4770<br>SHA1: 4c70e3db3ef685e67ec507b319c14984d55ebfa5<br>SHA256: 57fa592de1019b7f5181878824641269e435aa855b076c70d40051639a0aa074</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.3 MiB (212.2 MB) – 2,083,176 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54ebaeca10259e0b994c1a88657e2096<br>SHA1: bfeb55e3ee58219d12b77dec83fdbc5881141b41<br>SHA256: 508f1368fabfa2ab959eb81503c183a30e15ccb1fa5e80652ee94bd0b6836bea</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.5 MiB (206.0 MB) – 2,083,176 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4418f035031aa129f7d15c5e2441bd89<br>SHA1: eac4197dc2df79ad2424d2bd6ea7b1193b7a4de1<br>SHA256: df3d23d7709cb521a16e7f70d6d533c373ed72e98d98f8002a566d2786cb0936</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.9 MiB (206.4 MB) – 2,083,176 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5b73942e62aad183253a3fb99e00bfd<br>SHA1: 5433bd51d725d80fed5b5a722bc91c42155d5a12<br>SHA256: 534907cb82bee03f29f2ff9afbf47661d9cb54255266f0366affcb1c260db7da</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.5 MiB (230.2 MB) – 2,083,176 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5ebfb66e8f3d00c81d4ef1f5207487f<br>SHA1: 09ee738a9d97f23eeb0eb3a4e6fe64668ee90187<br>SHA256: 6d6b090c97899703bdc466b15f73decaedf2ed83e0dcaaaea6b9e7e7060211ec</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.4 MiB (206.0 MB) – 2,083,176 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5fdbeb66393351d0d476dc80db1f54c8<br>SHA1: e0be49b7681629bab8f601b5466f2e4772d1e7b8<br>SHA256: b7c47c659a098d07032ecf60f1ae251305022355a3fe90f1ecdf410a55fc7c87</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>217.7 MiB (228.3 MB) – 2,083,176 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9fbc8db4bf5da57d3b7171a482fcfa15<br>SHA1: 3866293ed5658fdda5e6e184ba172f96f48da2f9<br>SHA256: 992e6497c55654958e38cae6ab0dfd35989029304ca50ebc4c4de6e065ea6ab8</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.3 MiB (209.0 MB) – 2,083,176 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 738868aa62253b6702195917e2a40ac3<br>SHA1: efdf6eb699555463d830b77ad1dd041ed3f1b6a4<br>SHA256: 96cb6bce91be556c2c11d03539f95866d806fae3f094b11d58a71c0cbc7d8334</pre></details></small> |


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
