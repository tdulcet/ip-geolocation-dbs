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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-04-03<br>IPv6: 2024-04-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.808MiB (5.042MB) – 240,711 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b675bbf66405756a8b26711a5d64876<br>SHA1: 611be741bb71010c31ddc6641c3653d378cde219<br>SHA256: b42bcc3097377fb6c72671d83f9cfd83ee0ca9eaae50bcf0f8a0569e08b0fefd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.109MiB (6.406MB) – 92,837 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28b3f3a1b58b659bd598806e9dae8291<br>SHA1: a723c917119ae2774a2ead0d1906892009b2cbde<br>SHA256: a661a294e7b312e1c67b72c9517efd065a9e1a55a80c6d67790fda47182f92d6</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-04-03<br>IPv6: 2024-04-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.223MiB (8.623MB) – 411,801 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e92fbc7c4fab4701b87c112ed51d75d1<br>SHA1: ae3f20c691e0c1027d11910ce68c382ba4bb33df<br>SHA256: d0b29b383fa9615b8e443336f58ae26897f8075d62181aafc4866c285fc723dd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.106MiB (7.451MB) – 108,107 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9efdca72d02911334bab4b11de5c39b<br>SHA1: a2b0595dd4e2abc95c14a7fd71fb7f7f5b1cd383<br>SHA256: 0a4fe584d10f65e3029a871a52332255f45217adb2d9c8437d8107bb6b85c798</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-04-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.68MiB (18.54MB) – 885,076 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 464783d86cff24e400c13a9bde65dabf<br>SHA1: c8d0857da4d293aa59e33ec4dc67e9f74837d840<br>SHA256: ea0c0c2aced3a515f18c9ce7218b099536546e1f5cde8ace6fd45d3b209c9605</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>95.02MiB (99.63MB) – 1,443,950 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4cc406195e56481c280a20b40e15fe58<br>SHA1: 75da720bee1e28105e5a476706393235b1683ca8<br>SHA256: 21ba1b957f1e41908d197214b628173edbd1644649fd6a1059e5dbb2295239ac</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.603MiB (6.924MB) – 331,502 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed612f6829372d96d1503867a952099<br>SHA1: d545a9307049b4d56f79cfc1544864fa920d1b6b<br>SHA256: 91dde8f7a7970c4c1b8054b947e0cca9ae1b8735bdd19fe420e6e491a7427366</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.03MiB (18.91MB) – 274,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b254c68dde265fc8d6412499c6db3dd7<br>SHA1: 2cbecfceb25b68f5f0f9889993e2f4931f5e18dd<br>SHA256: e4727e6d32df38a7582a7b9172ee67820f196bd746046a5050cd654393436920</pre></details></small> |
| | | Full Location | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.8MiB (189.6MB) – 3,159,870 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e335ee8885a5e6286297a9c06a48db0a<br>SHA1: 9b10ee274410a884c26ab662fbabb41f315616a5<br>SHA256: fc15b0d16ccdb65b6da2de506405d685d02531ce5571558ba78ed3e9110dcbbe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>322.9MiB (338.6MB) – 3,132,412 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eb566a7a93d1e35f303a2978c1da77b<br>SHA1: 78d75aa920c86cb0b75dff47ca09bb4f55bb6fd9<br>SHA256: f95d154f7a461a32269f564496c943eb8cb5e61df0269c831e76ea2f52896979</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-04-03<br>IPv6: 2024-04-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.897MiB (5.134MB) – 245,145 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86953d84c1cd0d89d0994ab1cd100b39<br>SHA1: d3303729b5fdd4e92be0090d728786a641d6bdf4<br>SHA256: 9503103e96fef9a268f0d6e3e3e189c3c227ba6a962256a4be433fec98dd6295</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.43MiB (18.28MB) – 264,858 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dee1827a7716642179bea6a3edb75c4<br>SHA1: 6d32a09ab10cd650c38bb65962cded09532e32f0<br>SHA256: d1b625011cb76995dc6c5895dea53ec54db80bd372c0878631cf89b1e7957469</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-04-03<br>IPv6: 2024-04-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.5MiB (178.8MB) – 2,955,821 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 100c457dda8054191dec8cb248ef7116<br>SHA1: 5997f43cfa17dfe7406c1480e1305b0ee4d7d2b8<br>SHA256: 2e80f7bb769fbecd8a09c918b55397ec9abeb21f176c73e5c23ca937d52e974b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,714,136 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09506237fd701236f9a08be9c399f75a<br>SHA1: 012fc8437c33186fadb2add162e68a946c843774<br>SHA256: b25eb4c33c6657facc2a0eab8012f99200c9aa7dcbc9eb0f151bcbda5e02cae0</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-04-02<br>IPv6: 2024-04-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.660MiB (10.13MB) – 483,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3325ba1847e578f54fe947206231bb5b<br>SHA1: 989bd20e7e904411badea4ca23b15f497b3dcf67<br>SHA256: 1d990a0bc81a0887296e3eae8cc89843f70bfe29ba1025bd3523f535cff359bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.64MiB (20.59MB) – 298,445 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c3a71caa62dcaa9b1f168bd623d1703<br>SHA1: 7c8f769ce89a330c3a6a8c196f9e2f493d874c24<br>SHA256: a3c811304c06d578bea06bb46c7a475641fc85427c0ec64fe3c70219cdd7e2e4</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-04-02<br>IPv6: 2024-04-02 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>127.4MiB (133.6MB) – 2,567,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c13f47b42b2960f0e040a86f652f98f<br>SHA1: b886d31b83e670c125ff843cc5a143b8b4ee9523<br>SHA256: bd11d6f53024f02ad851f2f86bee713f11fd68636f56826b28537ac03b8c2f4b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>138.3MiB (145.0MB) – 2,567,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 332989b777e12493c4f8f095225c4017<br>SHA1: f1a50224a0b76d3f0924b47b874d27b1608ff910<br>SHA256: 5fda16046be3f3f1009bf1b2d067cbe76b42c265c47d9465ee14ea4d23aee5b4</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>127.0MiB (133.2MB) – 2,567,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c4de89197fa75a16cb952732441a5a5<br>SHA1: 93d8f293b0899c0420163ad9b22c9824c92fa47c<br>SHA256: fb174022227d68e9a2459e7540b1a1a7930e4a59eeb959ed74dba574aadcbf65</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>129.7MiB (136.0MB) – 2,567,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e51d1810cd6571868fe3a87c7e8270a<br>SHA1: 6cb276a483ed5f292b90a848a9850d334ab665e8<br>SHA256: 407ea58c6c226720ebd3c2a0a3bfede48bef3436ba9b39c1b87165d84519561c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>158.6MiB (166.3MB) – 2,567,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2484686b228325bc2d6e8d4f56ddb2df<br>SHA1: 465eaf213a493dec752063e9a4929fc246a44b54<br>SHA256: 64ee360df8a34dc6e63360383c4f08271ad121828538f0dcc18af3741290141c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>126.1MiB (132.2MB) – 2,567,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 921aa93061e6d7e4db99ddd7d9b65e0b<br>SHA1: f90d3db2e403f5dd6a66cea8ec47ed17ae53c5e5<br>SHA256: 163bd1fc38fed0c6a7807bf74e32af7f3084db78dd028ad7b087603259e50a49</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>155.5MiB (163.1MB) – 2,567,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 769d97f35af8a974940b9e67d26c0b15<br>SHA1: 578e89403f4c5344fc2ff5cc877d269db3895d16<br>SHA256: 0296376f83095bdeea766cfd568bda8ff2156e36ae026d7b47c0f612d402c490</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>130.5MiB (136.8MB) – 2,567,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9447a86981a9d282d483961465efe291<br>SHA1: 48a253a3b365e9fa36bab88d05ce9cedfca622be<br>SHA256: e67ceb9bb2e477119a7c8ae578d0fa96b161dd363bf5c94bdc9304d7ec918624</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>106.1MiB (111.3MB) – 1,150,820 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca15911d8d37d83c8fb79b4d834b2f25<br>SHA1: f502e085af08730aae04ca0816a590da4972974b<br>SHA256: f371d4b8a86a8ad4dfba7f55d31c37b70e38795cf38774fa8eefbd0793473573</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>110.4MiB (115.7MB) – 1,150,820 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d47f323d6699537008652753ab09c9f<br>SHA1: 1297f7ab01c514d85a8b2f39ac07ee27e2386e9a<br>SHA256: 8f9214cd8ac8fa079aa0ca9ab592a1d52e30f864711cb66ac4b2a1ab1e723bce</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>106.1MiB (111.3MB) – 1,150,820 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1d2e2e99c4aee9aa8d778e229aa02ff<br>SHA1: b7149f5c75f8acbde306d14c6a233f3f15f63ea0<br>SHA256: 4080a02296a568efc55d81cd301f1797bc0046bf0a35b5da23dd74caf9935df7</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>106.7MiB (111.9MB) – 1,150,820 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ff6fda14016b5f7ffeeabc03c9a0e8c<br>SHA1: 7ecde5d2fe52129738bb4c6838c4f73abc0b73c8<br>SHA256: ad259f453efb360ccc28272a42300a1480a643b8185a38ca5858c1646e81f289</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>116.5MiB (122.2MB) – 1,150,820 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65f14a1574e4daf3699395344f94ebb4<br>SHA1: 87191acd27da841a81c79f4f80a1ea2aaae54707<br>SHA256: a1893bead2ad743b91165517f2597501d971f0bcc46eda1ab404f8f3f7846ae7</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>106.0MiB (111.1MB) – 1,150,820 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 876e6f46be6e00a27dcd76c39e8b7710<br>SHA1: 4f1b4ed42f6207a5a6b1e1cfb46513f5c889e57f<br>SHA256: e4d3dd5cf516bf9c65ed2b824062812d8f675a2573ab5eb9eb7367f7dc04981b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>116.3MiB (121.9MB) – 1,150,820 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4cd3086bfe56cef1379b01795e3496e2<br>SHA1: 1db4f75d7c30543598d757d03440c371618f114b<br>SHA256: 69f1801416dd70f5f0f72cad62e5e19aa869213e854f943f245d328a87d40f89</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>108.0MiB (113.2MB) – 1,150,820 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e44a3a3f3b26c20a0d82d4c92603c94<br>SHA1: 38a01c066e7d84198cc5a69aac1f598604679c29<br>SHA256: d6efb37173b047b808d9ab4816e1385b63258161c3b3302f47d214c78481210a</pre></details></small> |


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
