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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-07-05<br>IPv6: 2024-07-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.740MiB (4.970MB) – 237,284 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97574419a3d4f5ffde8d8c5468ced3e9<br>SHA1: f6f777a037849823dcf338c8af6b193448233db4<br>SHA256: 68c347f26483503a233db3a7265d912f344a7a0d6fa6dde7ec28f55f87fa821b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.535MiB (6.852MB) – 99,305 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1897f9adaf1abb5319f681f46171f76<br>SHA1: 5cbea122cce78c56ed7fffaad97b0241bc4c8995<br>SHA256: 567134f38c11c7d73c0d4398496b4550621df81073625338c225e830ee066810</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-07-05<br>IPv6: 2024-07-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.098MiB (8.491MB) – 405,532 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f5fc98dd1954d7b76fa301aa671f131<br>SHA1: 66854cbe2399cbd49cb89e30fdc58c30de6a2304<br>SHA256: 73bde491e1f4402ee07f3c4abacbc77a6d18ab88c7e60f1b6617d4dcb381059d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.494MiB (6.810MB) – 98,809 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60edd127f2d2dc06b53ea698d2711fca<br>SHA1: 1fbed4adde7f528739c5cf19c66c1ad442c44d42<br>SHA256: 0aa28eba6b6057a12ab3d97ad038e63dc28d42d41d3eb63a012c268d39639f1c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-07-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.20MiB (18.03MB) – 860,400 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 650651eeec2fc014e28a6295e3ecf594<br>SHA1: 71ce6ec8fce976e8291a283e77faccbc88f602a4<br>SHA256: b37d576079022eb8f88307845d61ecc88bfae3adf8dd3de67442310632aa03de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>73.60MiB (77.17MB) – 1,118,476 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 801d8ee0241add29d25e0e8e769bb69c<br>SHA1: f313034624d357533315f9ff2e1650355ad642f3<br>SHA256: bb6ea1e5c5c762320ae18e4ca671bdeedc3ffe91dcd2d9018c4d4e37b98bac05</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.909MiB (7.244MB) – 347,080 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cc33d54c3bf6b9175e0b145f7c4118<br>SHA1: a3816e7df4ffb8f7c8a3e26e9ecc5b337da78413<br>SHA256: cacc1ada016c1e717e0b0224945498ec7c02f45e18e6ccc3f699cf925eb98541</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.77MiB (16.53MB) – 239,599 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d8002e2bd70b383a55c26aa6c39879<br>SHA1: 2e8b5538dfa991864d56253287cfea899c731ec6<br>SHA256: 417be26de93d6c5b8d2da113e60494952f0235ed696211cedbd93a8683cecbc7</pre></details></small> |
| | | Full Location | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,260,981 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1931ab257b12ab9982e2e837f7a344a<br>SHA1: 265a511f4b4152bd6a0cba4302e7e551263bf78e<br>SHA256: af747f9dd2423c564835352c37e87e14cf8cec475eff93b3c6b458b8ad3a8e43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>339.4MiB (355.9MB) – 3,295,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3cd81e94c6b15797cf1a60147cbd224<br>SHA1: f49f6c791890b20c1ca8c05135f5558493b09356<br>SHA256: b412df8ef796f81fa4522b3051247207cb9af864a32937188218b559f4a52daf</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-07-05<br>IPv6: 2024-07-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.882MiB (5.119MB) – 244,344 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f71b297b6d31124fb4d85a0573420148<br>SHA1: c19cd0e022cce41cdad248812b6ed96ce01f3d96<br>SHA256: 4f6fdac09cbc5c0e25e4305fde012ad03b4b27ba701095ec557f2c1ed1c594bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.18MiB (19.07MB) – 276,325 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 455753ce19833b0e8aa5a719617562cf<br>SHA1: b7cdef244498f6ea069a0523ddc0f9997aed06ad<br>SHA256: 7da4ff6463125871ea8fa12c1e2c0bb4c82cbd5eb13603b15bb06a6c12f21dbb</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-07-05<br>IPv6: 2024-07-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.9MiB (180.3MB) – 2,978,355 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec317919e654aaf26ba2956cba42987<br>SHA1: 5a1d6e846a17d001ab2649860d9e68064c6a788d<br>SHA256: 5099491c3b03773fa74caf9833a9dbb55e732c359aa505587dcd7b44b8c904e3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>200.7MiB (210.5MB) – 1,942,692 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 038ee21bebef5c2336a17368fd32209f<br>SHA1: a21d0b165419264ad815c5d369b16dde7b1ffe6c<br>SHA256: 7d3aaf19058abf9358cba535f4f8cc3c6475d21045808f084c2bc63c0857a3df</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-07-02<br>IPv6: 2024-07-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.862MiB (10.34MB) – 494,043 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 634fea4866d8dbbd14b254b686304006<br>SHA1: 7ce6a09382fee1100e1f686a186a4edb9aa90058<br>SHA256: d4948b7274cd1e885014ecb0818343ee09315e61d21b5d397a1f5b9205ec8b1e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.68MiB (20.64MB) – 299,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 486dd2b6d9a1d02d208ab87364ff7d7b<br>SHA1: 9b8cd98949200ae3a1e47c8095b8a55701798ffe<br>SHA256: 35eeef3fa9196b10a5ce6e8ccf72958db9e929a4a8348ff26dca1e2481d9593f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-07-02<br>IPv6: 2024-07-02 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>119.3MiB (125.1MB) – 2,392,542 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6362008e868fdc93198f2fcb1b2eaa6<br>SHA1: 27e8a1aec21528920e147c7ebabe5d6226525d9a<br>SHA256: d8c3de92309fd339181e84ba2ebf084c10d8053fa0f26408139037b8cf2158f7</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>128.2MiB (134.4MB) – 2,392,542 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca2bad5e7b0ef66bc209e0e19c79da52<br>SHA1: ccac811d2ac27305092892a7c849daaa5e84dcfc<br>SHA256: 466573a3c0ad800752a22ec1d550ff8b38d4d9b9dba655f7d245632854c2106c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>119.1MiB (124.9MB) – 2,392,542 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c03bda66199036c1d78378e9ac1b1efc<br>SHA1: 7df54679afc48e06f1a80ba04aa2fe03cef93e80<br>SHA256: 7308e14a6e29b2faf1dda4ce716ecef0b9a76fd8dfe01ab74be758939e1e52e3</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>121.6MiB (127.5MB) – 2,392,542 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41bcc89154d562de6946acc701a21bf9<br>SHA1: ee244e586ab70ffd17ecbc8d5b60842b67071e9b<br>SHA256: 8bb468fb9f6e2efd50f1bedfd51988cebc90c0fb099444ad10cda399e59441ab</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>148.7MiB (155.9MB) – 2,392,542 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b1486b4b65c41f0b93129accd38344d<br>SHA1: 4bc29daeff16e5c2f032d830c42f7b7661977d7f<br>SHA256: 3b1d27e864286433acdb7ab22926f489c38d99ff38374f2e686b316a5a7724b5</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>118.4MiB (124.1MB) – 2,392,542 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20a54a16d01e47c89161ba0165357530<br>SHA1: a468d0cda883765f5b7fcf85ab714a3cc9b8d6c0<br>SHA256: 351fd4c1d74773a751c3c62b60ab700ab9fa67f44dfa12a4f6b312837611b836</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>145.1MiB (152.1MB) – 2,392,542 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb998e7f7b3d43011a76087e6f8cf2ff<br>SHA1: 1efbe8202378eaa42f1f2482d03e5457f1d47a70<br>SHA256: 4bf0d5013a29369f8c0892d778790ffa0942fb3c83fea31c3d1afc8ea19d3045</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>121.8MiB (127.7MB) – 2,392,542 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5285a2c690cb378e3243f39b3d2b8572<br>SHA1: a406cd07b09273a1b51225a77e08e496aa018ca6<br>SHA256: a13f7723bbd2eddb056cb654fba50da276ac0e0deea616f512b661e3b9e3a9ff</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>110.3MiB (115.7MB) – 1,189,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30ba2ac567f1a1d3be86a032bb633eb6<br>SHA1: 45bfc5977d40a0c28c49bf6196fb09de09f65047<br>SHA256: 23d0c8ebf666cf3e76f5784711714ead89bea301c682af069fb28db0150ee959</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>114.1MiB (119.7MB) – 1,189,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d2d8beb3133ac214b570f6149183622<br>SHA1: a1092bdfddfc6aca5b68b36d444bc3ca36584278<br>SHA256: a23fc0773acf1b3419a42e90f804a6baeecf3f3cbc2445d0dd37a2b793c22f51</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>110.5MiB (115.9MB) – 1,189,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c0d8c846cd8cfe9e9dd649a82a17970<br>SHA1: dd1b26cbf0d1b725507904d838ba94a532e62924<br>SHA256: fe0c3b6bc5f78e358ee37a1b062d93604850bcd66ab60efdc5030d5b00b96ffb</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>111.0MiB (116.4MB) – 1,189,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06354cb1fbb1b60335981b8cbcd6e7d6<br>SHA1: 131fc9c114122027a4b5f8d1f8fcf6e7bd089404<br>SHA256: 42c9ec3cd87286d7b92d1eb7712a22920c3e42357f23b6af0eee857421e1d2b2</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>121.5MiB (127.4MB) – 1,189,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c44a53d4213fb5b2c3f8eb8661755d82<br>SHA1: ddd3bae5ad33e5d82bdcc5b27c5f545961727c84<br>SHA256: 5e3b5d550b05a22a60457a9af1e5bfaf9e7e497bdb0455c08b40e4b7520fc86a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>110.2MiB (115.6MB) – 1,189,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7adbdb1fbc84ed9c7a27d5b1bda1350b<br>SHA1: 5985d651806b452738338bed348f7f5a44351d7a<br>SHA256: 73ffb4db9446be6cc6292cb9dd69b64257ddea49b95e27eb4c888ad0051387e1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>120.8MiB (126.7MB) – 1,189,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88336846617c25f333ab8b0d3283290a<br>SHA1: 4a083b7c1b4163b8142a47f8e81578c7c031d618<br>SHA256: d536c8a981f66f643af3a5bafcefaa606fbb3436cf968c110b2e4f99ace8192c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>112.2MiB (117.6MB) – 1,189,038 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 379c1292141b678c088900ef5962368c<br>SHA1: 12932af5c92493a52ab22763af8dcb5b67781fb0<br>SHA256: ae1f4e62c6e7786fabbac3dfb5fff66497ed3979d03480c76af99933b9c05d8a</pre></details></small> |


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
