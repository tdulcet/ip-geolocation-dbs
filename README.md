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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-07-26<br>IPv6: 2023-07-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.671MiB (5.947MB) – 241,632 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f578e9b70d55d748c2606c0f652920a3<br>SHA1: a54f7af5c7ff399ca79b339db974b3781a8c7492<br>SHA256: c3cc0546090817ae4796e8bf3fa77df1c994afc4faf8bb486a8d3f225028d782</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.552MiB (6.870MB) – 84,820 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16ed5ecf83372bb108a044f65e959fdf<br>SHA1: ad7f543304a00be6fb13802ac804f1ebc802262f<br>SHA256: 7be2b4d28b3075d8d2c045fc5f880fef4921f3b99d1fe83685a56a3ade0561e6</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-07-26<br>IPv6: 2023-07-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.534MiB (9.997MB) – 404,959 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78244f9095c723e4fd62518f2142912d<br>SHA1: 0537efb9cf7d2e2cd865c525a9ab011012760252<br>SHA256: 9a0d5a4e9d67e5e7a75df8b421d28f37d38fc7b865828692f7dcef73be729b9e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.654MiB (8.026MB) – 99,181 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0339db03fee3fdc14f2dcdee96320aa<br>SHA1: 3bcb209ba385b3fea33ffd92ba638496840078c7<br>SHA256: d043932df8d1f0759c446985ddcd17ff2bc08bc6a9a6fa6dc3f32933919bd524</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-07-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.52MiB (15.22MB) – 619,224 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6bb88c4a0d137ce0770ea4a080b8cec<br>SHA1: 734fcc1fa26c38d0ca6b1bc2532239b28d8c904a<br>SHA256: 70e543df7ca993003a58d2387ee06d55209c00a568ba82a391f2365e5acb8475</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>34.86MiB (36.55MB) – 451,275 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1f29ce049f8f666e149c000a5eab9ae<br>SHA1: 273c00c3a02937fc2fa3bbb443143fa1fe1c465c<br>SHA256: 9803c9c67f011310b0e4c2719a59c11ad11dd4c651980958b14945875f4dbd67</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.175MiB (7.523MB) – 307,076 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f151f7f54b095b5ffda5d94059bb3dce<br>SHA1: f80142665d03d0371f800c5f959cf629ca3d8a10<br>SHA256: b490b03da5e813361b0ca08dd8f825c5991c8d4f9e21568776e4edd93746282a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.39MiB (25.58MB) – 315,780 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ccafe342cd0f83d168aa17033cc052e<br>SHA1: 18929b5d0a7ce12d7f3357fae4e283e3dd102ad6<br>SHA256: 55c042d3051eabf81b139c750768903bc3e9d8314dc416dc8b9ed715765677c2</pre></details></small> |
| | | Full Location | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,182,050 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3425f6eec44d17e75a144956ca9bedc4<br>SHA1: a6ae6d14f8e9a5705bee763c64c2bea6c879b127<br>SHA256: 9a1cffd22df1d59c077b7123b734f643ddf57a71c4d928ee793715e78400597a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.0MiB (303.0MB) – 2,522,649 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac831cafe688be22a072e63aeca50a09<br>SHA1: 8b579d16247db56f0e752f9c5566007ecce7b3c3<br>SHA256: f693430db94cf07b4b01343ab0d2e4ab2f16501d77f433b222ab16b8f015dcf2</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-07-26<br>IPv6: 2023-07-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-07-26<br>IPv6: 2023-07-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-07-21<br>IPv6: 2023-07-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.36MiB (10.86MB) – 442,121 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d3e0283491067a204abd55cf003611e<br>SHA1: 2a66f88c889e22c5bacb0386b3c37ab8bc82354f<br>SHA256: 1f869f52190db4be6130518c8e9c47c1e46dc25f22692b6d7d06db7c27c1e16b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.96MiB (23.03MB) – 284,270 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed7b068d5cbbfc1e2e4ee8a078111440<br>SHA1: ab27af9cb48020fbb6646a5db7d2ab70c1585d99<br>SHA256: 2376ea9cecaa5b566f9fe93443260bcc3130bc87b72db50c37489efd84b145a3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-07-21<br>IPv6: 2023-07-21 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.4MiB (198.6MB) – 3,777,451 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4390832477c88c31fe30b8d5cf2b4bae<br>SHA1: 394419c8f25217fa14deb310258646761c639499<br>SHA256: e8bbe3bbe8de4655283bed4af46b6faf7ab4d7a71721567a8f6a664bdf641a31</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.5MiB (232.3MB) – 3,777,451 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2aac19fa7216f000ace51f36ecda23e<br>SHA1: abb53f86007c9b966916457a4cb7da641b4eca77<br>SHA256: 952b0269361f3b9bac47f6beadb55466835f5937e63189d9e9694db01f8d07d7</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.2MiB (205.7MB) – 3,777,451 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb4782e07c2cf2d4b3f1105508f8710d<br>SHA1: 8c991b8e133ee471d8a472af877a3abbac9fe636<br>SHA256: 17739090b5ad911b3066f6183490f306e4cb9aff31166602505391363a90f6f0</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.9MiB (212.8MB) – 3,777,451 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ddcf3ace9286f1d615f5b2c2cd4f34<br>SHA1: 7180885c67bc0ad74b12662aacabdd0763eae17f<br>SHA256: 35db71a1b44f250333ea82e55ec1587f010ca724049458afedfb793ab302e0fc</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.5MiB (250.1MB) – 3,777,451 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 137c3e8b680453b5456c20cbba14a41c<br>SHA1: dda1a3b25b4534efc5730ce3eadcb4fa42a46733<br>SHA256: 62c9d4dc5065bc78e0beb6c77e84d8a8b37c16aee8626206a8bd6a9a0d643b17</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.8MiB (200.0MB) – 3,777,451 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 395a1bbb366b1c20d0a9aff9abe60d50<br>SHA1: 727edb568046e9a242c40761853627a34ac1c864<br>SHA256: d35cc01e878f7525dc4d3cad1acc48f2a16d1b0d5f03bc569960ffd04a745f22</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.5MiB (250.1MB) – 3,777,451 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52fda7b985e45cfa3fa32ff998f905ef<br>SHA1: e3fd2d7f9c8b80496fb261788504e7ac0fa422ad<br>SHA256: 951dc982926c70c3eb1b2ac0e6e681b923f9543bb5bb2d9fb232618acd2c8e0e</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.1MiB (213.0MB) – 3,777,451 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32b2214ae759a0e836d2471484a54cce<br>SHA1: 923bf6de02915776f364184be17ed3dcf71d9087<br>SHA256: c8b123413cf1403af24b007a2eb82821c6191d4df6754708cd3d0cc30aa0d5f6</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.3MiB (134.5MB) – 1,280,595 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18081a3b759d8eec4217d7e1f278129b<br>SHA1: 90d550b7243cff7499997ff1738ac6734b68607c<br>SHA256: 7aa32a18c8818f8cc081ceb00231ed4c013f382cae0c3951a780c2ab2fe21fb0</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.7MiB (143.3MB) – 1,280,595 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f342173c2b4205ed836a4e7d0c38ca31<br>SHA1: 8ae51a4c1f3333005a60fed772778d5f7c239e4d<br>SHA256: 960db8ed2c0094b7a44e97797a685971a4d475c2463abec986895f99d9c9d0f4</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.7MiB (137.0MB) – 1,280,595 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d340d29ae0635322b932c7df08c7e5ec<br>SHA1: b63990e5aeaeb432be90c8166cffa508404e96a3<br>SHA256: 4c19ae2d6bbe4c6a727057d33db7d049f176c0b4145caef1f1b1d041aea39036</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.6MiB (139.0MB) – 1,280,595 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d55f6f5b349484303226c750793cbf5<br>SHA1: 783bcadc21459b2a5bfc9bf3d459df26cf68864c<br>SHA256: eee7fdba0fc50e7e32460b32c3b5203d5758ae97d18633632337470fae83cb22</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>140.4MiB (147.2MB) – 1,280,595 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1af06bbea0032999316e49eed56fec48<br>SHA1: 8b1a35291c7bdf536a31f26ace4c8ef02024c982<br>SHA256: 1441939d32a36f588d7e15a1df8ed5210e5bc3acccd1b655c91ae209cbe219ac</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.7MiB (136.0MB) – 1,280,595 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0b2aac7eff044d5804aa2ab5ad5a1ec<br>SHA1: d29c363fdf960c8fc3e2251747ea186e18a68827<br>SHA256: a647735cb8a18b8d46d4bdc1abb111872e7c1c2b8a685482b5c26bed8db65673</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>141.0MiB (147.8MB) – 1,280,595 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd6f84f7bc1a5e781b703df22bfcfc80<br>SHA1: c4be49c597b9738465433ec1cc81ca75cd4f6534<br>SHA256: b040dc854c73a7f12f12319f0808f94a0b4d06498e7e3996e4fe1428f98cf8c4</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.8MiB (139.2MB) – 1,280,595 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d1a45ad55541a6e80a711bdbaeef03e<br>SHA1: fc4e93561a2c9205e5d9bdd4601f0113e5c28de2<br>SHA256: 177557b2bb1b803b5b7406763512a81a40009e2b88f7bc1457b3b0ef55158e12</pre></details></small> |


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
