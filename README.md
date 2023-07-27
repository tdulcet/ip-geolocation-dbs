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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-07-27<br>IPv6: 2023-07-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.675MiB (5.950MB) – 241,781 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39074f3f30f4c0c6abdbb63d8b39301e<br>SHA1: 955529c8eb4420325f0f150883bb8c6a290b084d<br>SHA256: daa32c3335d519119e0a751b11823af81dab4c162514e88069c825cd43b9b6a1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.560MiB (6.879MB) – 84,921 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b887dc6978136389da61e78a8481affa<br>SHA1: 875d6f88b7e6bc555586e85cdc9991e5b6d33011<br>SHA256: 722f8188db543360e9b36e17aca9f143c5839ef6d3cfe014948742fa759ee63c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-07-27<br>IPv6: 2023-07-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.533MiB (9.996MB) – 404,929 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 520016798331749882a1d82cf14f86d5<br>SHA1: 2882af515fac28c2d18fb99b0c89f0a127d1ee81<br>SHA256: 598a4ec3e3afe7fbf0a4a34bd87e27da7862075e7a0c6265cd0ae2aa30fcb3f5</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.657MiB (8.029MB) – 99,222 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef1dc01432975040ecf1be11e3790b83<br>SHA1: d1c9655ac478b9f26e778bd7ec8af72234715f19<br>SHA256: 9ac48cadd661c95179548ad49a5f694893c9542b75dbba942221b74ef8771fb7</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-07-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.59MiB (15.30MB) – 622,366 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af1b50dad4c22bfebfff375225549d80<br>SHA1: f6b7ef8a0fc8e1d231e5f70ad7884b574a7f04ac<br>SHA256: 8efbe2ddc2cc580731a870f6abdf59ae2387ae3d0ec8f89a14d551c7ddaaa806</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>35.01MiB (36.71MB) – 453,188 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5aaab7aa4694740b05f0e338e64b56b7<br>SHA1: 4eec25eada8aa13ca6c894b5ce15dd98fbbedc0c<br>SHA256: 90efbd51ee83c9e295f8afd45bb52b9dee00857c569343b162de31ec0a61130d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.175MiB (7.523MB) – 307,076 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f151f7f54b095b5ffda5d94059bb3dce<br>SHA1: f80142665d03d0371f800c5f959cf629ca3d8a10<br>SHA256: b490b03da5e813361b0ca08dd8f825c5991c8d4f9e21568776e4edd93746282a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.39MiB (25.58MB) – 315,780 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ccafe342cd0f83d168aa17033cc052e<br>SHA1: 18929b5d0a7ce12d7f3357fae4e283e3dd102ad6<br>SHA256: 55c042d3051eabf81b139c750768903bc3e9d8314dc416dc8b9ed715765677c2</pre></details></small> |
| | | Full Location | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,182,050 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3425f6eec44d17e75a144956ca9bedc4<br>SHA1: a6ae6d14f8e9a5705bee763c64c2bea6c879b127<br>SHA256: 9a1cffd22df1d59c077b7123b734f643ddf57a71c4d928ee793715e78400597a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.0MiB (303.0MB) – 2,522,649 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac831cafe688be22a072e63aeca50a09<br>SHA1: 8b579d16247db56f0e752f9c5566007ecce7b3c3<br>SHA256: f693430db94cf07b4b01343ab0d2e4ab2f16501d77f433b222ab16b8f015dcf2</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-07-27<br>IPv6: 2023-07-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-07-27<br>IPv6: 2023-07-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-07-26<br>IPv6: 2023-07-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.07MiB (10.56MB) – 429,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb1fc78cd66dbba18f7f86c8e12fcae9<br>SHA1: cd2cd6108c294c5199fef2833843c4b2691ead46<br>SHA256: 96234ecec55294bd549ff6d46b7ebad8ae1e124366c0a657e708d82e7da8c876</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.49MiB (22.53MB) – 278,198 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93ef58867dfeed894945cbec5d3d07a3<br>SHA1: 64ca65c9e8b034ccc83b1996ddb63219a312c915<br>SHA256: 8781f5f128ad9d3d4ee264fd83780982bb56b1d0f81e58cff98a39e457637755</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-07-26<br>IPv6: 2023-07-26 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>187.8MiB (196.9MB) – 3,747,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7207e688988f39e5b438f20ed987e48<br>SHA1: df791213e6666670051ba4bcfe0fffd9e2e49061<br>SHA256: 133367b789bfd510dd89f447b6fe505f0538b9f2660c5390ded76035566d22df</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>219.6MiB (230.3MB) – 3,747,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 576127b3a9b6dfb6b0ce9167299f64a8<br>SHA1: 58a9eccbe9f014ba974efbd4e4fb1204330eb71a<br>SHA256: 44baeb1d6b2f0f0803431ee792bd39631dc1c117a326e8178f533c4ac510371c</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>194.5MiB (203.9MB) – 3,747,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9fc548e69ee0ca166faff2a8df0ad029<br>SHA1: 7103b8fd55a747cb24deb2322794367c9ec265d8<br>SHA256: 9f97569a9e20e3faf1a4edafad5c8f5b1d51746a888f3d2c88f9c8e43c2272ea</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>201.2MiB (211.0MB) – 3,747,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e70739697a9adfa524ea61115f5a58e<br>SHA1: 1e3b87e37a9d30e2d87109bdbc3d5ada4b07a4f5<br>SHA256: 24052f9077a38f88cd8c48cad2a8c985fa9866e6cefe50060b958f82f781d155</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>236.4MiB (247.9MB) – 3,747,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90d91239283d0064213fc1c5a6882e04<br>SHA1: 445b93816efe098cc956817a8ecb25b932c2f5fa<br>SHA256: bb57cddebfe973d4df1834803631ad344b4ebb0319ef3985e67553d4b25393a9</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>189.1MiB (198.3MB) – 3,747,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21ff79e17bae8766fd1e721b0a3f906e<br>SHA1: e6b36f40267aca4167bcb95c820274e78c63e13a<br>SHA256: 7f6f4498e6d262b9814f7f55a7beb4f08dc261c3d59237ef5cef3c5a529b9cbc</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>236.4MiB (247.9MB) – 3,747,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c95078a863fd23680aefc745afa4af55<br>SHA1: 705f3b1ff35a67e0b053452a62212e38f94a4a8c<br>SHA256: 916e7afff8f72e073da6cf30b7276882342bff0a47088387d4c04df52e976bae</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>201.4MiB (211.1MB) – 3,747,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29b131d024cb3fce0860e3a8003b18e0<br>SHA1: d8d2668d008b60d197ab65235364d6dc8a12942e<br>SHA256: 89201de917fa93258255f4e5c14b9352807d88a98e7a0c7a5ef182bc8ac78d03</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>127.9MiB (134.1MB) – 1,276,464 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d9a5e716752bab07931e9ed5802f7c0<br>SHA1: f21d23f1b78a98e975599fd70ad32d09e5f44bac<br>SHA256: 4a382c2959486970fdbd2562520ee45bd1e064ec71762f345084f7a4ea118ccc</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.2MiB (142.8MB) – 1,276,464 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7fe2c7a993eef1e87b8c199b06e96a0<br>SHA1: 4cce44e1355a16e048ddd6356014ac60547a6636<br>SHA256: 25b4b958a8704bdb2aaa3fa40b1d7f329e1ccb01c6a3bf5be5431612c0e4971a</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.3MiB (136.6MB) – 1,276,464 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62fdca7f8b74add4cee73cc9bc0c50ec<br>SHA1: 1e977d0718057aae94db08f87c6eba93e7810acd<br>SHA256: 6f74660ff5388ae52c9c749d214ce9186649c8cbae979068a7093633892886fc</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.1MiB (138.5MB) – 1,276,464 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8600315aa6781f99962c38d2b96ac27<br>SHA1: 04d4b9fd91afa62009aae87ceef77430678058e4<br>SHA256: 97409db7fa030bb7354ba42f2495a23a84ae8c55337a5a8bd37ce792f8093ae9</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.9MiB (146.7MB) – 1,276,464 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e687869d03c5db287eed551c24490525<br>SHA1: f524ab7057c6e32297482c238167870aea4d32e8<br>SHA256: f7d1a1773a0a0d4fa7ba1ce98e41fe29d59fd700051b5bbab657a42fe8506dd7</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.2MiB (135.5MB) – 1,276,464 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b1f5aed17ebcc99323f2c66cdc9c382<br>SHA1: 566a6e2a90e9e984f09d42a7adb29e2f1fc6c3e9<br>SHA256: f46000473de51d64f5265d6a793142c323e8be5be69f3c25f06179e15f59bf78</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.5MiB (147.3MB) – 1,276,464 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dad6beda28cfbd36d0abe69c3cc9e4d4<br>SHA1: a176b305bcbb8f8fb20a12121b305dd887f567a7<br>SHA256: 8ece06f6672fdc3aff574466b5fe38736a0a4d1cf41a7d4d74d3ddbe7d1489e1</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.3MiB (138.7MB) – 1,276,464 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 643078b81d18ea21ad1f25c54fd38e14<br>SHA1: 20a8869b794ccea2bb311ad6055032822a545161<br>SHA256: 49f70d8af3b5cae576f54ec0a57bd9c4a40ad6fbbd1900a26d43be71bae11253</pre></details></small> |


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
