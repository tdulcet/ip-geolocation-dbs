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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.453MiB (6.766MB) – 323,135 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c3ef6c2f9753e4257a3c65f9f0dc98d<br>SHA1: bcdc1951277f6a80e9a24f2f7665b9823f417171<br>SHA256: 28602a5e1689d2e7ce92bf21adae7efe238f3a982c35545786246b5d4ec7da44</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.15MiB (15.88MB) – 230,182 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1000d6ed970ec0420044c8ff46c255af<br>SHA1: 756791c4217514f849ec8e800b0eca905d4c1228<br>SHA256: abcb1074b36a16368da99577c9f2057126c33dd6ac30bcd08129eaf0e4783e16</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.203MiB (9.650MB) – 460,772 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28cca8aa7177738c332338c5e6be3efa<br>SHA1: 491e39d6631fd07900fcdc119b624048e7ca583d<br>SHA256: 21896e116329c5e7f035dbfb145aa3c0235fdb431606e3d8bbed63722dfede51</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.526MiB (7.892MB) – 114,488 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be52f611e5a82e67b3dd7568034fdae9<br>SHA1: aa94a6a18eeaf36209b8b8de86b0d5cd47b123bc<br>SHA256: 88de889620b363208741d6fa5acd32ef0ab2347756f0d38437315cd2b1ac5eaa</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.37MiB (12.97MB) – 619,131 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 029bff4c0d89b4ec33e2e6f8f2488979<br>SHA1: acd77e47baf50b79de2febf8829bda1735ae4aed<br>SHA256: 4aee0bb6afd82cc3ef529651e9dc2e8d43ce401ef3bcbfb1da66783aebb31e3d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>64.37MiB (67.49MB) – 978,180 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3a67486070d0e609ef34e9ee8289715<br>SHA1: f826d0211ba6e1032f8040ec91ff6f6db3c56cf5<br>SHA256: 34ff5b5bbed69039abdb3dc885a6ec850c9db7bbb844dc917512d2ac9c8f4f7e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.843MiB (7.176MB) – 342,905 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7f0c42b88b3ee5ac2070e71f756f963<br>SHA1: 4416542c9574226ce202070dc48ca08edc6fab0d<br>SHA256: 5393382f53c552965d88b65e40e02f63c643f2379a931aaecef8209586b9ced2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.52MiB (17.32MB) – 251,059 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232548602865156556e4ff9d7db331da<br>SHA1: 61d1e0b2cefeca101ea9e8530969dab152188ab6<br>SHA256: b004edb93559a31ded3baa727a5d781edbe90c29420b4d5691f44e917e83bdb0</pre></details></small> |
| | | Full Location | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.7MiB (223.1MB) – 3,730,744 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42e04cdc8d81a8ce6b440accea48b373<br>SHA1: 9c414f68d243d9ebdc8b7c65e081580b035b663c<br>SHA256: 5274313529b847bd8629fb44b41144c683552f55760a830f535892f20b8e46db</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>457.0MiB (479.2MB) – 4,442,155 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56e8f0cd6817f6807824ced45628cb9<br>SHA1: 316812aba9e80b97b08bfca58defd796b628d008<br>SHA256: 44317ed175935104135d379f2a9918ca97141e9bf034ee1bca6cdf894093d72c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-08<br>IPv6: 2026-01-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.331MiB (5.590MB) – 266,810 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6936075ec427c7ed70a3d342b2e63912<br>SHA1: c7fae99a3a0567ed7445644b86a01fbef762ef6b<br>SHA256: 88ae548c41c1713b32260bdf14c95996bb2d7387a44e2bfd64ceb76fb873f61a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.53MiB (22.58MB) – 327,213 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27348409796721908a924318dcfc1b14<br>SHA1: f2aab8fb5a03f1d5d37b344e4c71e1277dc90aa7<br>SHA256: f0b5c009770b082f8e457f65291614d6cf88661b7518fcad74bac3f296014c2e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-08<br>IPv6: 2026-01-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0MiB (179.3MB) – 2,958,239 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49e99e9bd1ec9e6374170f539a275d4a<br>SHA1: a346ea441ddc4850ec1942528df68a32230e83a8<br>SHA256: 9a2330d68bf4d693241559bf46574fce71265babed257de579a39326314704da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>284.4MiB (298.2MB) – 2,756,871 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4043b07a9b191aa81c8428790ea89b1b<br>SHA1: f2e22768f73813f9e8b3d567b96e9129fb4a8790<br>SHA256: 8566a2873416028bfa9a7719f3649be95b44f46de14bcd84a0dae66027a203af</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-01-13<br>IPv6: 2026-01-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.13MiB (12.72MB) – 607,171 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fec9b73935d2bc294d9f06bcac889708<br>SHA1: cd288f4e8dd451c35167a3051b045877d6f35b7d<br>SHA256: 8e50ddfa9bad026b5535678ae6582abb4774d97e663ce7b72cbd7a69f6489dfb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.47MiB (44.53MB) – 645,352 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6a1ae582de899ee900b179c118ce2d0<br>SHA1: 98f57ecef1c937fbbba91249ac160948e2893da3<br>SHA256: 902d52b8cebd8b56fe5aa0fbdb83ea0d7744ec450e003d8df55294494715b28b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-01-13<br>IPv6: 2026-01-13 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.0MiB (186.6MB) – 3,514,865 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dbbf3b7b13356469ecd3188c2410abe<br>SHA1: 7459037bd6f511ec7f107d2dbb61350b43a0f9f1<br>SHA256: 52821dd4941475050c62519ac675a831ffc80a712f12023e6d275cf55b86daec</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.1MiB (198.2MB) – 3,514,865 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07f25c2ebceb4beaf4ad9616233663b1<br>SHA1: 570532726851a0d59b2887dcee2767d98c7d8051<br>SHA256: 4ddc1c08e1c2d96b38ddd69e452c7b834924f51334f482068e3d81a4eb122f34</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,514,865 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: febdb6be959cfca35ce8222ad9926e40<br>SHA1: 48cd80bf4651b8e585d8094e16edadf253270982<br>SHA256: 07e6ff2557442a9feb7ebe473c9eff7cfa11b84a34f5bad85d1e13c27636a601</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>179.9MiB (188.7MB) – 3,514,865 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5edb193582d56dc8757fcf9b8546b37<br>SHA1: c1e8e5e93ee2e0752a2985644e16ca262791fe81<br>SHA256: 0282ba2bc1c9609464dee5442cf4f99aef2da15d95445b900b32ecde7014c228</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.9MiB (235.8MB) – 3,514,865 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4a81b74c5b3449ba0ff57a5a9b311e1<br>SHA1: 49996e3a4a8cc06bd6ab08fcd34c3c6c9e256555<br>SHA256: b2a7ba50501db83c60f8162fce1403f38e0f8ad142b22dbaa30045a09e487302</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.6MiB (185.2MB) – 3,514,865 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b45ff55196024be3698a78a24b549c9<br>SHA1: 2da7c03d28856a7b07b5b7f6bea01e2926f446fd<br>SHA256: da1bda9ffe428b96fbdf5c2e8f46cf66df1069c37737b294a0c931238b9a52d8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>218.9MiB (229.5MB) – 3,514,865 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c28d1983771cf1e304fa2f6a14e1f1a<br>SHA1: 4b4cff679007843b07f9ac804b5c6a72d8d93e51<br>SHA256: ec53af1d737726f314a5ed1cdf847a9e582b93ff36930e125f8c662fa744e495</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.8MiB (192.7MB) – 3,514,865 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 815e75b76c9ec82bff8ee4b9c623fad7<br>SHA1: 25a2a5314c32997a13659450475d00ba8dacc5bb<br>SHA256: d21773d58dcf7462a4080c3863aa85aa005d9fb3d3ef137825104dd82c51c561</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>188.7MiB (197.9MB) – 1,986,131 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94c7cd0bd94ccb07a8eb3a2ca9d12ec6<br>SHA1: 3fbdbeed9feaf43d4720786b0f01ed9d1f41761f<br>SHA256: fee295a9fedaec7e83bbff87ce3d8db0d7f0f2e54746a0c9e7a02a9a3d672860</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>193.2MiB (202.6MB) – 1,986,131 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b77d6a069cbc4d2fe7062c7f1051d95<br>SHA1: 7f54ffaeb08865e7a404f51b4d59dcd32271861f<br>SHA256: 43ec45eabe67b19e709aa927f12531d89de48e2c68b584b03956e13757d6ed13</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>186.5MiB (195.6MB) – 1,986,131 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7eb8fccc0005fd7de7e73fc9b3c41465<br>SHA1: 037c82b188bb75fce0ee68fe7b576e7106f74cbb<br>SHA256: 8a09de9d0d50b6176b6e5d202ec258dd1e1342e53b7a3555e130f10d9f02fd49</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>187.2MiB (196.3MB) – 1,986,131 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61f19f4e8ca5afdf0db3c042653f8674<br>SHA1: 846edea3cab00ba45a7ecb03cb881cb5f24879f8<br>SHA256: a814449b0620959726e6765b1e4a8961f8968d6932b932d811b9b4546f14b1f1</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>207.5MiB (217.6MB) – 1,986,131 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5abd6498126d87807b24a58d3cb5a7a<br>SHA1: 85d0e823d114e31bb32e03f341f9762dbf28b27a<br>SHA256: a626a3adde62caa2af933d5f8de76e06bd8d31cb96e2a98218f60775ae47319e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>186.3MiB (195.3MB) – 1,986,131 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b54692b6851f6523becba49db19be6ea<br>SHA1: 43b9281ddfbca15f01e46eda6c9bda947508f5bc<br>SHA256: ce8c3bfeb835a2f3f2fdcc93af15a27e2049ea7321456e50a1edaf14ef2eab65</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>207.6MiB (217.6MB) – 1,986,131 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78187f8c455e6b9e5a78cf8893682983<br>SHA1: 530026dac9d593eeba4cde11286f433da9f8070e<br>SHA256: 72fcc085920ae665d52d2ab9bf1aabe61abb0b76816e69efc11702d1291b56e0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>189.8MiB (199.0MB) – 1,986,131 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 405f5fa1a96872e43257a201e8635ac7<br>SHA1: 88b51eeda422efcf098d00ac046c3b67ccf06631<br>SHA256: e9561a6f76afe0823ddb7227856347ffc1cd1a786d502ef082b9618cc7da1ac6</pre></details></small> |


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
