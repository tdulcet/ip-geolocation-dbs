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
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-07-21<br>IPv6: 2023-07-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.531MiB (9.994MB) – 404,813 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9cb82cba5f90d864e467bd01f4322c84<br>SHA1: 5e11f98d2bc221c35453a79fe427df12c8e6ca9b<br>SHA256: 49ca84ebb6304e06f17b32062821fb5970dc0f39589aafa4aed1d3b3f1ab9422</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.635MiB (8.006MB) – 98,932 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e707287c3e05fcc701f72eff11be6eb<br>SHA1: 9ce0c39cba0edac3af47323b321ca4f9a1f291b0<br>SHA256: 00e899e27916720c5adf5b86a57b868a40fcc2223dec3fdd2e5f69036c47ec90</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-07-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.84MiB (15.56MB) – 633,241 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05d84526d354ece9ba960f6078cb8ab9<br>SHA1: 985548cfd805452fec98b7af9a0d948794cdcf31<br>SHA256: d48dc99fd7a82e30a19f90297a491b4675fe16f95e6fbba7afc8c31a9699ccc4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>63.59MiB (66.68MB) – 823,261 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42a66ce18050baa684a31e5cf2a6bdcf<br>SHA1: b908df516290f8df4c29b844c638456084b849e2<br>SHA256: 4ef245124c47dc99cc4226221f35186112e5293e3cf1a77388cdc3bf59fa9442</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.175MiB (7.523MB) – 307,076 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f151f7f54b095b5ffda5d94059bb3dce<br>SHA1: f80142665d03d0371f800c5f959cf629ca3d8a10<br>SHA256: b490b03da5e813361b0ca08dd8f825c5991c8d4f9e21568776e4edd93746282a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.39MiB (25.58MB) – 315,780 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ccafe342cd0f83d168aa17033cc052e<br>SHA1: 18929b5d0a7ce12d7f3357fae4e283e3dd102ad6<br>SHA256: 55c042d3051eabf81b139c750768903bc3e9d8314dc416dc8b9ed715765677c2</pre></details></small> |
| | | Full Location | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,182,050 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3425f6eec44d17e75a144956ca9bedc4<br>SHA1: a6ae6d14f8e9a5705bee763c64c2bea6c879b127<br>SHA256: 9a1cffd22df1d59c077b7123b734f643ddf57a71c4d928ee793715e78400597a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.0MiB (303.0MB) – 2,522,649 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac831cafe688be22a072e63aeca50a09<br>SHA1: 8b579d16247db56f0e752f9c5566007ecce7b3c3<br>SHA256: f693430db94cf07b4b01343ab0d2e4ab2f16501d77f433b222ab16b8f015dcf2</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-07-21<br>IPv6: 2023-07-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.467MiB (5.733MB) – 233,097 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fc8c718d8feb7df8afa7d211f053a94<br>SHA1: 36955dd6964f821a52e81e89b2aa2887ede87495<br>SHA256: 45a077cdafe9583102dee0244b694ec37c2e2a100eb480cf38ead3ee27fa51ad</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.85MiB (19.77MB) – 244,067 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57f190f14205ab2a6ea50128828dfa4e<br>SHA1: 9b00da4018ca80cdfc00506c828656799e087bd9<br>SHA256: 777c9c19e77916f147a488a4466aa59abbc4ab78e4784096a9964c54d90e2873</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-07-21<br>IPv6: 2023-07-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.4MiB (194.5MB) – 3,026,483 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bfb5ebda6a60ba155dbc514ae5db8ce6<br>SHA1: f423db3848511c5d299d1a8ef8206f5ac8bba372<br>SHA256: d62364cc5398cecd98452f5aa163c03394685d54749bf9d63a8f7524e705e673</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.9MiB (165.6MB) – 1,377,625 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f393f5fa1f352e785171758aa858311d<br>SHA1: 21aab039729c6bbc79cad8f9e99dd5f77b33a2ef<br>SHA256: 21be1860661b20efe51c8abc66990ed7b1faa80fcd7a6c633847794d128e8648</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-07-17<br>IPv6: 2023-07-17 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.35MiB (10.85MB) – 441,576 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7959b5ed6594fc1c363c2af510b79fd2<br>SHA1: f9dce10778a6878cc55b27324b3f7609f2077668<br>SHA256: 13a0d4fe02d12a8591632efc390d6e10627f5cf6d1d54c11c4d8789c03738780</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.99MiB (23.06MB) – 284,684 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2186f2727dfbb333fa7d121287c81f7<br>SHA1: f606caf0bd6206180f47738b2d1f5b06f0949121<br>SHA256: 5a97f23ff13fdf5c9ac29dd8063420d29b3314f2f34c427fd437f21778258ccb</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-07-17<br>IPv6: 2023-07-17 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.5MiB (198.7MB) – 3,779,324 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd873259b2819ac23651d4165be858a1<br>SHA1: 8ec7cfc3bd44592cd85d60218813769feb3ea24a<br>SHA256: b78fea8cd3a10385bc2a61a3021881ac69b0acb3c3f463631d7d259ed66b2e39</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.6MiB (232.4MB) – 3,779,324 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbd86b0e31c959c79df807b5c3c76830<br>SHA1: d575c4fba6ee0e530c1b21ffcc9984bdfe3ca551<br>SHA256: 2aa2b909b9712596d61d0e52953339397f2df06248042940fbf0d740614d55cc</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.3MiB (205.8MB) – 3,779,324 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f50208066cbe32a113d5fae804dc654<br>SHA1: d26cd6d52cc4dbe77ea89b6d13f0e1f15b88bdd5<br>SHA256: f5bfcb60e858cb4612c9059e4912d247a2321eabb7b2d851f315d94c6012e0c4</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.0MiB (212.9MB) – 3,779,324 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5fcbebb5fe3e067f201f301263ac46d<br>SHA1: 2656f33531df2708bf8e1a61afb686d5a3b91199<br>SHA256: ee69ac2f60c5f43b4b08833900013f612ec4d3e58133888c99ff0054c34d4d29</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.6MiB (250.2MB) – 3,779,324 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a25bf656642ed99e7e67b73b97785393<br>SHA1: 25ed3646c7952b5cd4615f5736ba8b80bc213181<br>SHA256: 878624d154a9399e19f9a93750483101ebf2db08afefa80e9e5ce0d97bf93650</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.8MiB (200.1MB) – 3,779,324 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 117818cfe59d6c230b2f0d7a497c92c5<br>SHA1: 84171eaad737e5ad243ba8f9a2db3b8056f90451<br>SHA256: e5b57fb4fcdc0e0adaabd2d7bda1d7956c3b425b80bd1cfa3822e1cce2d9a6f6</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.6MiB (250.2MB) – 3,779,324 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbdc23066b605e9612b746cc76f0e304<br>SHA1: 7953f2eb2c5796d339b3cc1f5a2e3de2694122e5<br>SHA256: c8208cb836c3bdf6e9ba390c8ab308fa7662cafef23aeac0bb643db47e57cbbb</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.2MiB (213.1MB) – 3,779,324 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1961c57383cdffa23b5c61e927618a31<br>SHA1: a222094b71133574663ea6ca1bbc092534531857<br>SHA256: 00b797a6290e07a08c4548b29a29cc98049b0198683697ec9f52e97fb9707fa7</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.3MiB (134.5MB) – 1,280,578 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d16a1e94fa5dd09f76ca9b4e15333181<br>SHA1: 53420b2b95754e8ea61eab8bc77e3e6bdcc0cc17<br>SHA256: df2cfc52d49958c0ecb129dce51770b797de141ba7bc53e690e27520651b9f41</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.6MiB (143.3MB) – 1,280,578 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c88c4ad6103fd03e14347610dbd56edb<br>SHA1: 47ed5e07f761da133c50544f34fd260ec68839b7<br>SHA256: 1072b0f637776560f73dabf1cd20ad9eb3663b322423da4a3b92cc5e48b0274f</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.7MiB (137.0MB) – 1,280,578 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95db63b16208a477a215d2233d84b549<br>SHA1: 968ef3c3c6b7938e15222d19aa37bcd149569ad4<br>SHA256: 2afef687f69bbb6276548d5b0f61eb538f1dcea923f5219c5b9618836f3a120c</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.6MiB (139.0MB) – 1,280,578 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bae8e2eac766ff4678e6b0135c98430e<br>SHA1: c06138d7e1efc3405a0f1ce3dcb87561172eddac<br>SHA256: f5c8e73015399dedab6203d362ba562ae399696ed474b2f46256129f06a02531</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>140.4MiB (147.2MB) – 1,280,578 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d68fe16af48654ff43684f1cc3e38db6<br>SHA1: 2eee6b6cbc371bef2e79aa308298e08f523b055c<br>SHA256: f0edd35fb3c6add0d80d51f36140815da4b8181d08df83b2bfa07be258975906</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.7MiB (136.0MB) – 1,280,578 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50179cfd49a2e764ff338068c6baffd9<br>SHA1: 33eef3437f561089f5552a2ca90492204a253810<br>SHA256: cde8c30d4831b9492f5465e67a805a693d4a99c7694ec572f5618c0746c676a4</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.9MiB (147.8MB) – 1,280,578 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cd7ac6819fb6679acb0c0a23e3b5c47<br>SHA1: b34428ef18d400b4f37010ed2082351b7c15c7ce<br>SHA256: d4c45fea495310790ec210e8b917d3d65578e9d3656599f3842282c37a601264</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.8MiB (139.2MB) – 1,280,578 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05820a1e20c829b4adfe2a9c380d5f69<br>SHA1: 00c614991cc971fcc2bd49d788b91ad3b6da4f82<br>SHA256: b04568712f0485cd6915c4fe204886e97d34b46ca4f748963eaeda31aee1b29c</pre></details></small> |


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
