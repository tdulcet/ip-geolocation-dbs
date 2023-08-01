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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-08-01<br>IPv6: 2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.672MiB (5.948MB) – 241,638 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b7e4c977330165d35d16dfde8f1b6ae<br>SHA1: fdf15c0845113e0d592d22ba51d263cdb93d7853<br>SHA256: 18659c947628112e32d0fade835636ecf154222460e6604fe7bf68a92eecfa90</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.573MiB (6.892MB) – 85,090 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e024a246dc5d671e11b4dae0d98bf62<br>SHA1: 93b4fdad24614012937411123a989c3cdbd4b607<br>SHA256: 230e6ec5dbe13729eb28748d33da3589a663664dc87e993772a331dcc21141e0</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-08-01<br>IPv6: 2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.541MiB (10.00MB) – 405,247 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae93b4a238695e2285622152c4126f40<br>SHA1: 9b0fc002b3239a9622e18938bd371d67acdf21a8<br>SHA256: 882ab8d7f59fe3a9ff779642bd6a30cf0b21716be1a06a4fc6211c66c3307a86</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.675MiB (8.048MB) – 99,459 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e63d73b11495baaa1ce2404e0eecd98<br>SHA1: 3a7847813a01e5203fa8e2969137cf2cb8d0cc00<br>SHA256: 57ca90c513f4f90df9c5e8ac10a8281f4ac9ac4b17b05cd1bbdc404d1cf2f2a1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.65MiB (15.36MB) – 624,555 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3701e29007663229ea3890419c63540<br>SHA1: ed94f8d83536afd28b7a077b56ee5801caef93f7<br>SHA256: 29e573eb9cafd6c065843c2c4c9ab71fc61abcca9c3cb9f62756d553b5226404</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>36.25MiB (38.01MB) – 469,289 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 534d9531432e0833397c1d9a906e7b5b<br>SHA1: 15fc1b7a72584eef1cc0449722ab7eb0ce42d39c<br>SHA256: dda2fb94cdc3d04b9bff92e26c525a255c9a5b1e4fe839fa2b5c5ab3e58ade83</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.354MiB (7.711MB) – 314,876 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca76b98b742610e14368fd012848c6e<br>SHA1: 5a246f7aa51c885d4dc479284c99db5643e6770f<br>SHA256: e98c856388c6a61108e688ede0fd4bb7b818be019a620f09abfa12f09f9d4af0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.39MiB (27.67MB) – 341,571 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956b52205bafb278c0610cfec5e8e6f3<br>SHA1: 6e3ecda1bff92e53f23bf2ef3885149bc6312eff<br>SHA256: 0edd51b1478170d678f6905901a1c6a3ac7486a66f8672ee06079354a8c40436</pre></details></small> |
| | | Full Location | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.0MiB (201.3MB) – 3,170,913 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e50f1d7e16995e4854b0f105bd6c8b2b<br>SHA1: 1dcbe021497af64af841ae21163751821541e06e<br>SHA256: fa28f36a198a238e8f503e858e7561b54fb9c909d90276f58d195afea9f75250</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.8MiB (311.2MB) – 2,579,615 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bac2a6b630483711e47113caedf6461c<br>SHA1: 234b956c8061d27a07de03503b53aafee1dae740<br>SHA256: 67b384e2ddde5241f818748e689acf0bf9c436ed15bc23bd12c76eb991bd4fa3</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-08-01<br>IPv6: 2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-08-01<br>IPv6: 2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-07-31<br>IPv6: 2023-07-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.38MiB (10.89MB) – 443,050 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c77646518ffcb94379df1c3137b0350d<br>SHA1: 31740c34b4e5b19cd14a9c5c2032ecfc22e5ae32<br>SHA256: 5c5fb1d39fa4839107b6698202a0c9d84882702abe6306512f4a0fec49a8c5ca</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.80MiB (23.91MB) – 295,165 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 904a71e3325a820ee2fad37273d86ef5<br>SHA1: 61160b9327ce3d817f7db365b70875f3c33ec983<br>SHA256: 2494d570b8981e3192b3d0ceb61703f63429749fc4f20975a64b3fb2484cfba4</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-07-31<br>IPv6: 2023-07-31 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>184.6MiB (193.5MB) – 3,685,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 183ba0c17a5784faaadb292b744d1780<br>SHA1: dcec5b8bb04cee7d60ca4681714eb6e45382d5a6<br>SHA256: 91d71a5d6827f2493ebdfacfac34b80229a87e611bc9daee107d01e7109ae347</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>215.7MiB (226.2MB) – 3,685,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5d3a55a22e1d82a45bf241c27314d58<br>SHA1: 3ea39f906763265590ef0230cc5d4418a4d5becd<br>SHA256: bbedc4d37824728a7e6092abe7fa952f53a8ce1e6330e3553c913c42a3b4b6f7</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>191.2MiB (200.5MB) – 3,685,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2fa494cec25349228521580fff03e25<br>SHA1: 304655f02658cdc2a8904b0ae8303178f9a132c4<br>SHA256: d66084a2a340e9c4a78254e7ae985f079f95b90caa903fcb5024ad25c305bfe0</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>197.7MiB (207.3MB) – 3,685,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46c4e6d15e04ffc6d5e8d9658cdd9586<br>SHA1: 52aeee8a7252417b84f4d18c7288b0b24d6b0399<br>SHA256: 983668b5520db62f6e8a8ef15a996e68e5af65a988914678a0a45fe2dcfef3e2</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>232.6MiB (243.9MB) – 3,685,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6349652ef3cf4fe77a036dddc25dc391<br>SHA1: 4e1b3c2a566e30ef081b58dce6e54c301a89061d<br>SHA256: 48ac757513cc08561f2f92d939fd50d40075c133b4fb9790b2c165f7ea392132</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,685,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 842df731a0ed022614c3ef83a3542508<br>SHA1: e029d6a5480d351255e0b77e79445abdfe0befd5<br>SHA256: 462ae74d3fab77bedad45a58eec7644a9023f43a9fd0723e48bf93fef78e4ada</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>232.5MiB (243.8MB) – 3,685,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a947ba5cf074b1a79061c9aff95f91d8<br>SHA1: b8278659652db4d75c57f386a5bda4a7225d2572<br>SHA256: cea394f95d27ca42d8c0ab5d226ccc078a1da7d6c5ad8a9c4b7649fb6d1b7ab9</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>198.0MiB (207.7MB) – 3,685,489 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da77e517275bbd80f8d144598885096a<br>SHA1: fc3318fd99fb854a12fea594aba65640b9ab75e8<br>SHA256: 30f54842d8d31b8c26cf1155c1d939369c0582736d2b7bb99940cda9bf721e5f</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>124.1MiB (130.1MB) – 1,239,319 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be6503042583bc624a62482d09f45706<br>SHA1: d9563a97a0267bc7e4d07f385dbd17c7fcb3c3ac<br>SHA256: 40aa8bc0390fa7fa84677ced197e2a3c25b6e91fb22971e420323af1e3a45736</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>132.1MiB (138.6MB) – 1,239,319 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5cc2b00633c908b04ce2f05e81d510c9<br>SHA1: ea8ad5aa1a89a5bbeb74566965b3d1f0b6afa5e2<br>SHA256: ff32bd7bc2c168cdb7351c01b8f61ba80f26146e11c605d7f12a835877921c39</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>126.4MiB (132.5MB) – 1,239,319 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70a52aaf62a8439b41069d536e0829af<br>SHA1: e031f8e5151a3a19d8a9214bbd476da611b14fa8<br>SHA256: 5afe8c03a0f7532f8b9043e376689d4f5496bd7936fb6c8dc04d8ea975b42523</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>128.3MiB (134.5MB) – 1,239,319 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04d1a652e7991febf059a890d6bee94a<br>SHA1: 678e9927b25d819b491851b3ea972ec2b5e6c106<br>SHA256: 55bbafe74857064fa06115bfaac63cd81165599909382a4f58d827277f66642c</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>135.8MiB (142.4MB) – 1,239,319 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b06a76d07d3d8c55d46a0f9feeae1151<br>SHA1: 3f08637765c822a11151c4e909cf881fa73c3646<br>SHA256: 33dd48a6b8d1cc9c04b6763d35c7f5301967ccb8e9953fc6062a519dfe5a18b2</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>125.4MiB (131.5MB) – 1,239,319 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf3522cfc035ae27316e933afe45526c<br>SHA1: 9e1a2b85081dcced50ac8127e19127d422f146fe<br>SHA256: 3bfcee11783428622661853607ab449efb03fe9a2f9740e15ca6874a8526bfba</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>136.4MiB (143.1MB) – 1,239,319 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609a12fbe31f1e1473a072b60c954374<br>SHA1: edf922a3fb9ef22a8576f43ad23228a6774f6794<br>SHA256: 8f8a280f2c013c461ad5b2c212b0bc6618337a403bf3fe3e1c702013b855c68f</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>128.6MiB (134.8MB) – 1,239,319 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20fda25afee5cd3bee9b00e9438c22b3<br>SHA1: 51d8b04ef52b03b8a3741e67d8b1f22f092fe81d<br>SHA256: 5fb4779dce7919dfaed18b25048ff40280916d6c241d34212b9bb98f35ad59e1</pre></details></small> |


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
