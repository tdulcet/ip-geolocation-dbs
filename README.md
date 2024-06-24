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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-06-24<br>IPv6: 2024-06-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.735MiB (4.965MB) – 237,021 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 197c5c3eaa1afed2aed0352ac607add7<br>SHA1: ec97659b16a9ffcc8ec0aac9e6a941195f7ca68b<br>SHA256: cc374d8b24b58c953ce190935f00cd59a8906e7253861734abf5e9174241937f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.495MiB (6.811MB) – 98,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 494f2a4bf524c237c7b2d3610a2d323c<br>SHA1: 9fcf3264cac1a81160a1d24766eabfb8589d41a7<br>SHA256: f4478fadbbefde17172b91ec2f1b3c89c805552bdcbef12d145f26d2e23c67c9</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-06-24<br>IPv6: 2024-06-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.090MiB (8.482MB) – 405,121 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68412a8a0a0f0099ed2f76f8d863e1a8<br>SHA1: 7c89851a82ba79c36565fea55b9afd0c711a2fdd<br>SHA256: 27fab7b4ab7080eed319490b4aee8baca498bbdbdf90f116296a8efaf44d9a05</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.457MiB (6.771MB) – 98,244 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82c95783545d3c4bb61eeb590bc70717<br>SHA1: 7c5ee0ab11107bd6e4d56c13db7b3b0c3a55a3c9<br>SHA256: f34bd56361a3f8d2822fcfa4c9f04732225de042bf21b8fad54426cf262f55b1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-06-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.59MiB (18.45MB) – 880,313 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f03ce6b787c2d6f2c5e2b732bf2c010c<br>SHA1: ef874892051aec13f0ffd58ee8b3665f2d862cfb<br>SHA256: f67e7c2315058a37e606e6dc1f4ee9b937287d8f83eed364766ec7014d417ca9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>77.19MiB (80.94MB) – 1,173,077 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99122e2bba5d01b004397db461a3404e<br>SHA1: 968d0fe58d6f151697326472ce920bf939212221<br>SHA256: 0f0e7f490e6d90bf7da91b81df1d096b661fe55d3b6622a9ec2c9c17f0af1004</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.920MiB (7.257MB) – 347,790 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228d49dd4c10c1d4778473109614f06<br>SHA1: 84aeb9072586fe27e7a2fd0cdc62b4421b417010<br>SHA256: becc801a5b95a0c7e6dea789881460b3cce70a60f8b941077db5db9f24f332a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.87MiB (16.64MB) – 241,164 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77063c075f456a1e11f7a52af24ac9ce<br>SHA1: c787ab002266a3398026d5342c963fd1ea59f3b4<br>SHA256: 72503d5df7ba2b39c61d7f574dd167649fdff103e81019ba98b18c192a045f0b</pre></details></small> |
| | | Full Location | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.7MiB (195.7MB) – 3,261,621 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d700e342b096e0b5285fb98e7ea719e<br>SHA1: 95986a4433c4d6be7ba8f0d38d9ac62adeb2d962<br>SHA256: 48ea78edb396cd5b834f2a55d80909bfe196c2ba8756c47776a331bc1537686c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>341.2MiB (357.7MB) – 3,305,843 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8cd42e639e764b6915b74d34e29681e<br>SHA1: 59487357d7497ea585a66be963038da0bd3d8c79<br>SHA256: 093ad3c5b00a0620dd5ab55a96d31fdbde283e096d5d86611cf2e0af2cb6f688</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-06-24<br>IPv6: 2024-06-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.893MiB (5.131MB) – 244,932 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffde7736a4dce2d1dc8a9bbdbbed74a5<br>SHA1: b43b198dcef1ba6df65e58c1860df753727d07a0<br>SHA256: 8724d93cfde83ae2b1ecc823b3e74fd2991e6b70f24b1547c184c710023795dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.66MiB (18.52MB) – 268,413 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0affbc6694e8124ef8380a96f029473c<br>SHA1: ee3211b937aab5e966a663960fff6c4ebac1172f<br>SHA256: 1ab2b436fcbc1c46882e731a91c9c9ace7151e260ba27191c665827291450dad</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-06-24<br>IPv6: 2024-06-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.2MiB (179.5MB) – 2,966,969 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23fb370ce2d6e35cc080047ec96854e<br>SHA1: 6375dc2f3658701b80ddbbb07172e7979cfd3c60<br>SHA256: d5616074b0d3213fccda295fa79eab456cf538541040ad6d2b330f9b8e18e286</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>192.6MiB (201.9MB) – 1,864,338 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c773064f37ebb2a011fd7af63e5eb82<br>SHA1: 2b1c4e83df9f45b9539528f8dc4a01a661ce71e9<br>SHA256: a4a6a481f67fa24ccffea017ecff51d398b6046177a33e77ad479f97889e8457</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-06-21<br>IPv6: 2024-06-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.848MiB (10.33MB) – 493,331 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 176dc608b804a772be1a54f329be4504<br>SHA1: de1e4c34f4026de43260bcf1c404913d41a79b4b<br>SHA256: 30a4cbaaa59f84ddbc88d5e87032f8ab8533324e3b885b27079fde5e839b1fed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.33MiB (20.27MB) – 293,765 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aafd291af939bb3e632405fc422e0aef<br>SHA1: a12cb60a1b2b6345073b94f08c6f9d8ef65e1b21<br>SHA256: 3e1147ba34e243b966b6d5572af3dd1a98cea55ac1649902c8de33ae8db8321b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-06-21<br>IPv6: 2024-06-21 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>119.8MiB (125.6MB) – 2,397,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45cc27490fcf6e0d8dccb1872a02ceff<br>SHA1: 00bca558629d3100d5593f5018db812daabb4048<br>SHA256: 0583a9fb3b4c1583327b4d80a398519899a5b9a2fd6d1327be9e3a88ab5e7943</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>128.8MiB (135.0MB) – 2,397,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fec98ab1514cdf73d6df8daa0b2f81d8<br>SHA1: dea29699f6b0d9a9b0b4a71ad07286b7e6435252<br>SHA256: 5e1229904171155043df0056623e7c81ae4e9db86c0ba9dab20904d16cf30c13</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>119.6MiB (125.4MB) – 2,397,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ebfeb6e25d00d0b8500e796ed4c142ed<br>SHA1: d33e036e7b15c94265b2678f04c7ed0ae21b97d9<br>SHA256: 6a524fce3b15c1e79e10cc589c0eba88e5f13edafab6fcbb23ee96a85f01accd</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.0MiB (128.0MB) – 2,397,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a805942aa3191cb3d27da9966790fa2<br>SHA1: d4bb560e16676bfa5395ee6f4d1b6375cbca8244<br>SHA256: 1e3959576b5eab375ef816533e4f40b15967e801452c5ad16886023a1128330e</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>149.4MiB (156.7MB) – 2,397,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f067b9866aa105e2db19c331419600d7<br>SHA1: b8f2e2929b6baedfed7cef7db70aa709e51df8dd<br>SHA256: 77b9b8b12c8db22f2c7e720f4caeb83f2e4e5da66b8aadea0b2d763eb71cc1ff</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>118.8MiB (124.6MB) – 2,397,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b5dd23903f67ba3863a59d711322174<br>SHA1: ace42b0e7cedf2c8cfc0e7ab21f1cf73ebb68729<br>SHA256: 2135b53608cc251badfaf63ef2043b0c3cd374fd7193e68043f84f601dee76a9</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>145.8MiB (152.8MB) – 2,397,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98c7b6cd973d80c681bc83b640415de6<br>SHA1: f70f6806dac2b3c4402d582ec8f0b3c8a2b1dd59<br>SHA256: b53400c216efa1dfd61cc3e290b0c70f9c27f1e6a3177528dedba497827ed890</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>122.2MiB (128.2MB) – 2,397,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca7982b462db0a04532349b944531cc9<br>SHA1: f68fe7cba2b288862f62d099e49d059e486ab0c1<br>SHA256: 894c07fed07f8169086b89a387d2faa7d70e1e155063456c34feda30187dcfb6</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>116.5MiB (122.1MB) – 1,252,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d6a3c6d21d11bb841a6371aaa5ddf0d<br>SHA1: 35ea3bf02d29a6b3abb0302968b2d6125c4b8a9d<br>SHA256: 75dedb8d918cfed35fcd49f2b2882f287755366945c71d786a3522651f64ba7b</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>120.5MiB (126.3MB) – 1,252,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e987efdd6c6cbbc81a2838a5f72f1ab<br>SHA1: 430a02b8e74c6b72f7f84e14dc622056e61404c3<br>SHA256: 91946082b7e70f213edbd9581d24926d5ca0eac12d2f8f67123c63c304077c20</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>116.8MiB (122.4MB) – 1,252,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75ebecec3d8f0a5e920e500a293212ff<br>SHA1: 35b10fd80d0acc649003e92f79514c3787d8f657<br>SHA256: 67eb3aadb0f0d63d15c642784268c611ec2cd4014e731335f7974d27f4c54e63</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>117.2MiB (122.9MB) – 1,252,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52f39e8d034f7a4acbe8b0d84a161b9a<br>SHA1: 30588187ae1dcb0b927526250517340dee2c8547<br>SHA256: 63c89c6ae149d9ab562776564ebbbe5f4a95325fa37d36dba18cc3c43ead407a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>128.4MiB (134.6MB) – 1,252,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92da72a1671444f21298d200739b8be2<br>SHA1: a6bc00e262a331647ef75fb159ddcdbed91264e3<br>SHA256: 27b50c2266143245ccc1737d309cf795c551294ffd0128df83faecb3afcc09ce</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>116.3MiB (122.0MB) – 1,252,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44a006facb002280fa396c710cc6a473<br>SHA1: 58ce2bc93a7b030424cf46560e2032911a026448<br>SHA256: 1d8cb12a2d326f29b50722f6046a01ab6949c4dddc401cdfc53e4ceb0934f46c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>127.6MiB (133.8MB) – 1,252,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c9ceea12682affd1ad273164a2a0ff0<br>SHA1: cc3032efb28009af2ced89bc575d1df81e372e24<br>SHA256: ccadcd94567b0f0831b71833cdaf88b0110b1abfa92deae598705a9e67afd555</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>118.3MiB (124.0MB) – 1,252,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd72a820ab563f1c303db18875359772<br>SHA1: bc93e62a0ed75d650c8d8c34d237ec783d0d7fb7<br>SHA256: 7fb94daca317526a489d4e3dae5c94108d08a5648135395c6d09c87f1df6a285</pre></details></small> |


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
