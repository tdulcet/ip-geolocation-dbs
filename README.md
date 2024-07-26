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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-07-26<br>IPv6: 2024-07-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.982MB) – 237,870 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5195c3bb8b982810de6f6fc7a9c1071d<br>SHA1: 0545d07be80b4a2938bb068b660d18b59bd82270<br>SHA256: d7e326be26fe2343d3f85315b49fad49b0d2b1cdc4bb4ef1d7b3c0bf4b4f2b06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.759MiB (6.039MB) – 87,524 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6989f04b529b31308e90836f70b93ce<br>SHA1: 91df705507a60fb44cdba51a4b7dfb5d67b3f029<br>SHA256: b97a3eb4c0915931a87a0d251fb1ad31d99e9a18a5740325ceeedba7dc390b57</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-07-26<br>IPv6: 2024-07-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.111MiB (8.505MB) – 406,168 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 120ad6f0a135f4a387aebb31e428fc03<br>SHA1: 4b4b444e0a05c75cecd961adf26c0863b6cdc83b<br>SHA256: 6027e45339b045eb92d7c6b4e33fac1b8ab0fc942e21a3a461d91d4fbe776db4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.596MiB (6.917MB) – 100,358 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4298fc29e83cc9eb4a49cbe97e5f0e7d<br>SHA1: d1f60025701c14c01cd389b5cc482f69487a443f<br>SHA256: db56a763964b251be25d1d3785ec2484b43dd732baf1e3d44b00064d5021b835</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-07-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.43MiB (18.27MB) – 871,863 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4983658865f662dfb05c160690dc709<br>SHA1: ac11b0e65783f8c3b09d3e1b17596b584b1f4437<br>SHA256: 8054cd1992278e32840e61ca155c47569202e5e87a9d36d528d761a6c24867e5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>64.63MiB (67.77MB) – 982,242 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8bc4d74f03c090d1ae56f4ed67434997<br>SHA1: 618369d093ee0be6578ea58f2405a3a91ffd7e98<br>SHA256: 99d1f681284e0a6b0c09a09fb024410b583ebd28151ddda94c1735167247ef75</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.909MiB (7.244MB) – 347,080 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91cc33d54c3bf6b9175e0b145f7c4118<br>SHA1: a3816e7df4ffb8f7c8a3e26e9ecc5b337da78413<br>SHA256: cacc1ada016c1e717e0b0224945498ec7c02f45e18e6ccc3f699cf925eb98541</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.77MiB (16.53MB) – 239,599 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7d8002e2bd70b383a55c26aa6c39879<br>SHA1: 2e8b5538dfa991864d56253287cfea899c731ec6<br>SHA256: 417be26de93d6c5b8d2da113e60494952f0235ed696211cedbd93a8683cecbc7</pre></details></small> |
| | | Full Location | Monthly<br>2024-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,260,981 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1931ab257b12ab9982e2e837f7a344a<br>SHA1: 265a511f4b4152bd6a0cba4302e7e551263bf78e<br>SHA256: af747f9dd2423c564835352c37e87e14cf8cec475eff93b3c6b458b8ad3a8e43</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>339.4MiB (355.9MB) – 3,295,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3cd81e94c6b15797cf1a60147cbd224<br>SHA1: f49f6c791890b20c1ca8c05135f5558493b09356<br>SHA256: b412df8ef796f81fa4522b3051247207cb9af864a32937188218b559f4a52daf</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-07-26<br>IPv6: 2024-07-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.882MiB (5.119MB) – 244,344 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f71b297b6d31124fb4d85a0573420148<br>SHA1: c19cd0e022cce41cdad248812b6ed96ce01f3d96<br>SHA256: 4f6fdac09cbc5c0e25e4305fde012ad03b4b27ba701095ec557f2c1ed1c594bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.18MiB (19.07MB) – 276,325 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 455753ce19833b0e8aa5a719617562cf<br>SHA1: b7cdef244498f6ea069a0523ddc0f9997aed06ad<br>SHA256: 7da4ff6463125871ea8fa12c1e2c0bb4c82cbd5eb13603b15bb06a6c12f21dbb</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-07-26<br>IPv6: 2024-07-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.9MiB (180.3MB) – 2,978,355 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec317919e654aaf26ba2956cba42987<br>SHA1: 5a1d6e846a17d001ab2649860d9e68064c6a788d<br>SHA256: 5099491c3b03773fa74caf9833a9dbb55e732c359aa505587dcd7b44b8c904e3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>200.7MiB (210.5MB) – 1,942,692 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 038ee21bebef5c2336a17368fd32209f<br>SHA1: a21d0b165419264ad815c5d369b16dde7b1ffe6c<br>SHA256: 7d3aaf19058abf9358cba535f4f8cc3c6475d21045808f084c2bc63c0857a3df</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-07-23<br>IPv6: 2024-07-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.879MiB (10.36MB) – 494,890 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3daa918ef24735f2ec868e6d44038d35<br>SHA1: 7f8e0e31d6c6c74e94fc8392e0362c768c74dc85<br>SHA256: 64491d8ed4902aa1004824d1b48cd289a4807ec5a94d3f2570c23c8c10b05f49</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.56MiB (20.51MB) – 297,323 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e2397c0374de26db5ae261f222d8004<br>SHA1: 07696a04ee852483fe32dc37e16ca1ee285b8d5c<br>SHA256: e6a405dcfd8a97a6a8585f53650dcea72d91376d0288ad548f45942ce7d6526a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-07-23<br>IPv6: 2024-07-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.5MiB (126.4MB) – 2,414,091 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa0ad9d6c584c1ad3282020d3db328bc<br>SHA1: 39f67e4e7f47f318cf92130a4bef4f250641f316<br>SHA256: 932653062dc2d814f92b55422f808a72980b9a70e1260ac3fee593071fa27d42</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.5MiB (135.8MB) – 2,414,091 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42c664fdadeb8bc95009080aa61c6c2a<br>SHA1: e98e9c1af9cdc9fb9ea924582807e3023ac9b5a4<br>SHA256: 510224582bb2a65266548141f787a4fd18896fe71fa47d6f3b3665c8ba25dfd7</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.3MiB (126.2MB) – 2,414,091 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a6e450c5a64ee32b9d043424c72e135<br>SHA1: 8fb60d86f83df7db713ea6ec193c7f8395c607e6<br>SHA256: ff383211a2e89261342c6b1bb0fb35788c347301dc75f5a93815c1886a9d931d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.8MiB (128.7MB) – 2,414,091 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc74f3d5c753864a479ac11ac0cc471c<br>SHA1: 233b5ebd597ab40e6c4ab814d25127584d30d8fe<br>SHA256: fd0ce8cebe20f3ff677ea5ecc135a7a2a4f9b2988f037fff2fe52510d430adf3</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.2MiB (157.5MB) – 2,414,091 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 319a9a0a313a6eb8f1a080abe23d8e67<br>SHA1: efcee246d4d5ca70868515cdb37df24fc5acec3a<br>SHA256: 16245a0d94be3056031e266cde41db036b977c7f17e75c21cfdd5b975f087259</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.5MiB (125.3MB) – 2,414,091 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c4463012b9bae3a4d05a7d426a243ea<br>SHA1: 91cd70abe36f76d668bd59cbac527c470970c462<br>SHA256: d3aae670c26073a964968a66e772550a952a975b733143a7cb0b5e239ec4a181</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.6MiB (153.7MB) – 2,414,091 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 13ea5040fdc2f8a4fcf3a181478550a2<br>SHA1: 2b9383a267f75d9f687d84eb6c26394e9bb3c4ee<br>SHA256: fc12f7dc6163f02b275a7e8edadd6da1d12f7f4a3d90e71f2fdb5634da9faecc</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.0MiB (129.0MB) – 2,414,091 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2348dbdaeffc26d87ce4b072c7238005<br>SHA1: db6969a5f4ab805750259c6aa56996ba667e0c35<br>SHA256: 1eca70ef5b0310e6248b5f4a268b3afd0f0cb9a0ad23b2a45c3119e1d532d2e2</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>117.8MiB (123.6MB) – 1,268,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b3937b06461cc3683984a7767879f50<br>SHA1: f2929994a5834267511443caf635b5989592a23a<br>SHA256: d3e07d43e21d43f9ea563786b0cd079743476e94ae8fecee0e660b9a5dac7275</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>122.0MiB (127.9MB) – 1,268,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 357f3e3c2f6a2ad6ea83223c4b53b233<br>SHA1: 44c84a863fb6447ab6f6038a633c4a259e6ba091<br>SHA256: 30aa56e10f7f71eb49ca2bcce4a67fcafc1d2c80956aa9001ebd57b5e7442328</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>118.2MiB (124.0MB) – 1,268,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6549f25511535c0173d6132fc04b2b78<br>SHA1: 461c58f982e96553933c85adcf7cf2e718fb9a88<br>SHA256: 5a00acf78115f8f168328221799aabd08cba270675a567329b13c7b47174ca9c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>118.7MiB (124.4MB) – 1,268,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e9b5a77e8a67190f66b486482547fc3<br>SHA1: 2b03a5d3093cff397b486db4306751073131927d<br>SHA256: 457e897961f06a5c30916666ad44ba0b6089730dab89114784031d69bbb0e55f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>130.1MiB (136.4MB) – 1,268,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36e48431065e484ac2056646d81ea43a<br>SHA1: 8bf7f75963ae8335c0a9cb0705e43ae7ad89b0ae<br>SHA256: fe018555d39e18459dd89ede0362c529424d217713c31e79334c7badf141f7c2</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>117.8MiB (123.5MB) – 1,268,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01fc9e87e1f92ef23f5c6e7994f5ea39<br>SHA1: 93aad57d4f343aa17d4298b04f98c74c5838d5e0<br>SHA256: 7dcad49c04e72b377664ddc4e9598a0fbd5254b147e0b14f9ee3c176960b57b6</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>129.2MiB (135.4MB) – 1,268,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6896e2b0237cf39e6327ed2d9e1dbb0f<br>SHA1: feec48f381dd81f560fd0e0487f6a54678970518<br>SHA256: 6f626c5f8c4c97e15ab0a22885fb626c9f3ecad895e974c764a9770091dc9ae6</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>119.7MiB (125.5MB) – 1,268,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef8dcd42198173b8c0a46f5e366000cd<br>SHA1: 278c460c73799fc88c64931161aa3a472a5b32db<br>SHA256: e9309cd32fedab95212290dcecb9660cba7c32c0e40dcf62517f1ce71c029204</pre></details></small> |


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
