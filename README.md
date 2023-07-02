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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-07-02<br>IPv6: 2023-07-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.654MiB (5.929MB) – 240,920 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c12a23add8b40b13c342c3db8ee04da9<br>SHA1: 1555dff0aeb3fb61fe2d285a2de017366d2f3900<br>SHA256: 2333cd884902fcad5eb8d6e45b34ff34a47efe52486a08920fedac51808351c3</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.538MiB (6.856MB) – 84,643 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60984d559839cbf4b4fb86eb6214a7ca<br>SHA1: 6cc8c010f8bfabebf836f0592a447c6373391370<br>SHA256: faaefe884cb2d6a7dc1f232958b5d8d6ba9bfc6e42132ffbbcd31508be3a784a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-07-02<br>IPv6: 2023-07-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.488MiB (9.949MB) – 402,982 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df5c5a66b982c2491c0ee095e70dcbfd<br>SHA1: 1b1fa9cdc6fbe319ec69bba3f37332402e7a4504<br>SHA256: b8a2d4d8e7ab8a9c91e7e54c83f8dff4f422965145d17ca0a861450aa392c094</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.690MiB (8.064MB) – 99,653 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f9458eeb8681e49c3b2a63361d4f034<br>SHA1: 750972b3acc79f5c352ac2f32ec2178091ceb99c<br>SHA256: 42d63e34b068e4d7e81adb04e8866a51462f223d73bea26c73bc89dcd14a31d4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-07-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.51MiB (15.21MB) – 618,671 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 050b41a943629040facd22ed68fbfe5b<br>SHA1: 07f13f26aec5debc18386fbc163bb693bffab321<br>SHA256: 9ec3a03a2ec9b6cb94571d4c51d11879ae3936f3b2caa7ad9d88f9ba1189b393</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>25.22MiB (26.45MB) – 326,529 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a91516ee166dae1135c0fa8c35bc86eb<br>SHA1: 6a7ddce4c3dfc77567ea7fb1a4c2077cd8db73b0<br>SHA256: 6d9339d4623e7f1c75f6efcdb03b6024583561ebed0d5e5030dd5eeeb903a85b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.175MiB (7.523MB) – 307,076 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f151f7f54b095b5ffda5d94059bb3dce<br>SHA1: f80142665d03d0371f800c5f959cf629ca3d8a10<br>SHA256: b490b03da5e813361b0ca08dd8f825c5991c8d4f9e21568776e4edd93746282a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.39MiB (25.58MB) – 315,780 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ccafe342cd0f83d168aa17033cc052e<br>SHA1: 18929b5d0a7ce12d7f3357fae4e283e3dd102ad6<br>SHA256: 55c042d3051eabf81b139c750768903bc3e9d8314dc416dc8b9ed715765677c2</pre></details></small> |
| | | Full Location | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,182,050 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3425f6eec44d17e75a144956ca9bedc4<br>SHA1: a6ae6d14f8e9a5705bee763c64c2bea6c879b127<br>SHA256: 9a1cffd22df1d59c077b7123b734f643ddf57a71c4d928ee793715e78400597a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.0MiB (303.0MB) – 2,522,649 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac831cafe688be22a072e63aeca50a09<br>SHA1: 8b579d16247db56f0e752f9c5566007ecce7b3c3<br>SHA256: f693430db94cf07b4b01343ab0d2e4ab2f16501d77f433b222ab16b8f015dcf2</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-07-02<br>IPv6: 2023-07-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.439MiB (5.703MB) – 231,694 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0c4b81d24e29c6c73a6447059b20636<br>SHA1: 8c76ee0b559d70f6fb1acd4406663f06134b6562<br>SHA256: 132f535a3ece4d3c3eee807f18a6479238a090f60d2375c45d04d0e9b1d54afd</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>25.54MiB (26.79MB) – 462,259 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54639a0ea6642d34e91a8bfc1f2f8de1<br>SHA1: 352c556d23cba7adc88d266664397c34b7c73c9e<br>SHA256: 4eba6d756556213ffc49d306a9a146dd09448886b41fa238940e45c7db63131d</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-07-02<br>IPv6: 2023-07-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.7MiB (194.7MB) – 3,029,753 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6201ead3742759699a0624ca3fc1c3ef<br>SHA1: 9dd3f205e5b188f0c5ed8580ed5e732b6e3b134c<br>SHA256: 872e6b858799dcebe7280dae761e05a39f5cd67a958e0654aa28af381083e9c9</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>370.4MiB (388.4MB) – 4,379,832 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dcbbe797aa6b8b6fcadd64bb630ca41<br>SHA1: e880cf9d2c8fc14c77d2fb7716316d2d48902524<br>SHA256: 6d0ee8670108278c36af8f99e6df137911e37fc66cc5f29f0907c5582080fc3f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-06-29<br>IPv6: 2023-06-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.854MiB (10.33MB) – 420,185 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd3ee0dee324faf4794d91c07baed42c<br>SHA1: a02a8daab87259301d75c30e8d2851e7f6c1d947<br>SHA256: 61dbd7c9f9fce8cbcc7bab52b5132f807184d6555ea505cba884803ac04364b3</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.63MiB (22.68MB) – 280,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85daf77900355ef605cf6aca0630a353<br>SHA1: 5c68b4ee0d93761a814a178e0417a75aa41372bd<br>SHA256: 14d62d33d702624872c86f151023927b36bf4e3d45669ea40e85ea000f2f540d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-06-29<br>IPv6: 2023-06-29 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>188.8MiB (197.9MB) – 3,760,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16681d88e62117737c346c6005084b6f<br>SHA1: 077e849e729a7028c670e1e10775b24453f8af73<br>SHA256: b6a63567898bc4454b6000ced076455c736be4063f28b6411d730991b4090780</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.0MiB (231.7MB) – 3,760,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 173ecd3efae1bdde6652b58072708fe1<br>SHA1: 2b70236d119529efb79c463d3e48e2308fdfae77<br>SHA256: b52cbaf5e26cada3349b310cc2f22218a17adc625397ad40160bd340c277ea91</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.5MiB (205.0MB) – 3,760,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15b33aced03d29e9ac5c9725ba636a17<br>SHA1: 538ad9b995ff93e3e62bf5fbdb6198689ddeada9<br>SHA256: 60538c6eebe7c4b794ebdb41d5a1b14abcb7e708f72123d4c9005c360af43fd4</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.4MiB (212.3MB) – 3,760,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2232221d40f3a501d4334a6950ec3400<br>SHA1: cc9f5091a0447fee8a10d4a8c525cbdc82d6366b<br>SHA256: 1d6f8f6631429980138362b05143bfe63a434b2d8652a855e439397f60f3c30c</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>237.9MiB (249.4MB) – 3,760,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 249770d4d84ea2042adbb1ca9e75d1d7<br>SHA1: e1d9393de8112197011a23126f72d29fdcc126e3<br>SHA256: 2f68f1447b7003bf865fef516ccc4260960b6309bde0d9ca967e1ea10304c3fb</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.3MiB (199.5MB) – 3,760,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3073e60ab8b00727c52013d4e14efcf<br>SHA1: d5d409313b17c90c72c1f0f7b82c5c24fb2d520a<br>SHA256: fd02c0a389cd140b9b7bff838166173478e2fc4a911a336cf38cbe1dfb0c0a56</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.2MiB (249.8MB) – 3,760,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e04a05d0c50ef9270202dbd8fbfffb67<br>SHA1: 32ce2aeb5fb4f6d80a29ad778bda9ce30bb9e74f<br>SHA256: d6c57ec4a2975fe410e7a81e54877721c499c310b18b27c4d9b6a0317071f843</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.4MiB (212.3MB) – 3,760,527 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1983f9a047f93e0a731858194a357c77<br>SHA1: c6854260cbd57c907da4dc42ebc56b8871b56fb9<br>SHA256: 879a741071fbd0907735d22ec076789467f2bbbd8c8c6306aedfde2f9c790059</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.7MiB (131.8MB) – 1,255,423 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3cafcdc8871bb66c06b9384ad09ce8b3<br>SHA1: b30fefaf9de1452ed424d00ff731eb4416194c53<br>SHA256: 6a15441666ee7ac1633ad006edada3920ce49a98192065e318aa93c4be1a892d</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>133.7MiB (140.2MB) – 1,255,423 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77c34f3b1b5cc76b8602dffa04198956<br>SHA1: 89d0d5bd038cca5a1d3f1c53b2b55ecb215afac6<br>SHA256: 10b737b67aac1952eaf8dbe516df2a684ac9330ec578b57ad52b3e1b85bca8f2</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.9MiB (134.1MB) – 1,255,423 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb2c1a7baf13aca098b35cb93714cc78<br>SHA1: 139cb86b84d8721e374e58034473292fbb083593<br>SHA256: 201dc6be8a48a179c866c70906495a8b3970af24cd7ea65125804e70a3fca561</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>129.7MiB (136.0MB) – 1,255,423 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82d410c519287d4ca67f97e8eeff5d50<br>SHA1: fce32eadcb783b694f821f409397169804c627bf<br>SHA256: 499e93d92cb93d6cc0094eec924e588a4904925153a896564ccbbcfb35f732aa</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>137.2MiB (143.9MB) – 1,255,423 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e7dde10f25c520b69ef56edcbd844d7<br>SHA1: b731f46a6c8981359f389453c18cea7978a55a9a<br>SHA256: 676dd453ff2f52af80aa2cab93913f236ff2357cb3c9c6d61f19e77540dd6b16</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>127.0MiB (133.2MB) – 1,255,423 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54674b03603576a071bbbe286b171d44<br>SHA1: 31e03a929b0f81cc39a7b753ab11b13b94447cda<br>SHA256: 9f5f9d3e5d721081a466d0eacaa065325841f483b959126eeecb7c076db4cb89</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>137.7MiB (144.3MB) – 1,255,423 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 547ca0b93bad68bcdb0a9647a64e189f<br>SHA1: 12113f03a07557eac9cc97af9bcac18ca0288ace<br>SHA256: 3b36432c76ac500ef1ff546ee1cc69e5354fb91271fda4e2354dfb1091355727</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>129.9MiB (136.2MB) – 1,255,423 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 285993e101e61b021743b89d34bc2953<br>SHA1: 825ca90abb77fd8f519291d48da7300b8c608f45<br>SHA256: 3caf60ca07aa343ddfdb02739d6f887ba21f514f775ecb94194c3fd94e76c0a4</pre></details></small> |


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
