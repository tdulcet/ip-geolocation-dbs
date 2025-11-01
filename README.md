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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-11-01<br>IPv6: 2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.316MiB (5.574MB) – 266,317 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32830e6f2b882cf880570007e809f5bb<br>SHA1: 1a22805e34676f973ddcca939fbd83cb363c104e<br>SHA256: fcc66c368c8ea87d87cbc5b69d4735cfb1f31733f565ae55b47c58ade3abf784</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.824MiB (7.155MB) – 103,696 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f08944a12d935c155e03ad21e83a9397<br>SHA1: 5202e0ce541d7d4e8f7d3f4c3a115f077680ad82<br>SHA256: f0ed0d0bc076ad3b96588b48f647273afef3e9c4dd111e35bb93e2c8feb2a40c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-11-01<br>IPv6: 2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.742MiB (9.167MB) – 437,746 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17e7671d1988bf3f4bd57298ff7fcde6<br>SHA1: f53d6ff0f51552c33bc5a7d178a4cb1db5dab552<br>SHA256: 43d7e5dd19c258d11bcc623dc0eea331e80fabfb5c2612ec6f16612668233d1e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.464MiB (7.827MB) – 113,549 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8ca63a572d5a1cbccaef2920d611ff6<br>SHA1: 887a0280d03f4ac9cbf9e0daa08056713ed1d3e9<br>SHA256: 738e16e3cf1e30a69e12ed0cd7faf3239f9cf3483fcd3ba698e6e1e504e52f99</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.24MiB (12.84MB) – 612,960 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23016bd9d78865bf37ac03609c4c2a68<br>SHA1: 050f8e6d140b87228bf26ef81c70a0d8de144f50<br>SHA256: 763a499cbb0cb3aeb19916751904775339e4fd6bf618910bb3d8f521494d4cc4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>71.52MiB (74.99MB) – 1,086,819 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ee682beb00c85b707d5c5cbd4b344fa<br>SHA1: 43a8c2b15c6598c03e73fe052dc433341c28ec3b<br>SHA256: d2ff7fe192a5750b128fb66b5d38fb92b196a3dcf7f6eecc50dcb2f2b6d28f6c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.010MiB (7.351MB) – 351,015 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b145553d436fa9927d6cee221444f00<br>SHA1: 843b7bc7470f77f7a70889bca7f0073e810cf0c3<br>SHA256: a8d289151b074c668255eb1d321a0c2c24a2aeb5d42f6061a293505dba1162ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.94MB) – 245,486 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e455a11648304abcd99f5c6bb19d7c56<br>SHA1: c3ea6f03fa4fee059c88a1910284305da803f248<br>SHA256: 8f4586e376e7d38e45f03f638da9bba2d90a84820ec5114e2ce10da9e7b87624</pre></details></small> |
| | | Full Location | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,722,991 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8adb14693f593577d9641386622862f<br>SHA1: 4789a341532d78da8e6b9fd9df61010466508387<br>SHA256: 18d6fa0beb7252dcb6684069fa602d39f95517dc0b4ee10bc0092ef22f72d867</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.7MiB (473.7MB) – 4,393,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fe48bb05d21d396bfad13d9ca53f98<br>SHA1: e1c547a5ade8b7c473d8429a89dbbb42b7a679a1<br>SHA256: 0b7ad446a98640e9d471aa376d976a1b332132350201538914192826c2ba532d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.163MiB (5.414MB) – 258,420 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71af8f36a1397b54f07095e46ae8647f<br>SHA1: 4e7eea5925834f1ff4f956802d8305814f9d5f71<br>SHA256: d19b4141eb99c7f37b587dd2ce5a4dc9b0a4369860115050ed1938a6d4e42eae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.52MiB (23.61MB) – 342,190 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2d25b5f83304f5ab3963662d1d82459<br>SHA1: bb6059c49131cbfda3baf36ae84efd715bf63f7e<br>SHA256: d8aa367d610898959d5d76a083e838cdbb5319f8a54b6a6b269f0bc3dd7d4e3e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.6MiB (181.0MB) – 2,992,474 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8caf582afb85da7035ab080370960f1d<br>SHA1: da00b833f91f14149ca4e947ed9c030f7c66ece6<br>SHA256: a7b0f18c2da024f4ae25e028eb1834d611e0f6a4c58fc63ec6db40af5830bdb9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>292.6MiB (306.8MB) – 2,836,100 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc6b2a9b8fe3ed4d35e4b406d54dc4ed<br>SHA1: 40a84eef0f2ea3d6ea0fbc3a2c011d0993367c32<br>SHA256: 5b38c04d1cbde28d1234ab83322bf6d65bf2c6fd480c757260db36e3be83f37f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.97MiB (13.60MB) – 649,317 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2969077f9451e4f6c8ddb4d0501d5e1d<br>SHA1: ffa46fa4c03cf7a46bccbec62a6efea4b4d7395a<br>SHA256: e653affb903b14517b2ba65f494abf13ae10ee72540380a12d8f60114d4bd7c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.40MiB (45.51MB) – 659,512 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c57f6e25487f65e89e1cabf83713f47<br>SHA1: bb520eb3cfd736ebf97d88db4a56eb101e791d34<br>SHA256: deb89d74faaa3518b6493543d5ada1f4586b8ba94bde8cda9378c7479889173a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.3MiB (188.0MB) – 3,530,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfe97f27ea1370cc58ebf0da110ba155<br>SHA1: 5f4eb26205b2e352b89013622e2caa182b65476b<br>SHA256: a883ffe664e92dc96bd0a902e830fe64f31e63b6c535bf90adcdc0b0ee1e9159</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.7MiB (200.0MB) – 3,530,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9de704d2f688abafc67594eaff793555<br>SHA1: b123f1090961c0d49d7fb0b93406569538a3b4a8<br>SHA256: 367fa27ac1051f124c77702203944c41d0a0b621e0b86f049ec63e15fbe22507</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.4MiB (187.0MB) – 3,530,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 327f8eab57960ac4d53335df17254a4b<br>SHA1: 545c542fc350846b94a5131e561d32e8f244de76<br>SHA256: 99ae3d5e6492cc17b083618061b970d56d06fa0f7e9c322db1a8db6f70893658</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.2MiB (190.1MB) – 3,530,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 636ee196da8dc2d90ee65d4a0f2b409c<br>SHA1: c9f3eebf61542fa7e5e04d4fef1e6f275e297bfc<br>SHA256: 80cc706211205236d01b5508c95e77375737c8873a1a34fcfe452f5829ea641a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.1MiB (238.1MB) – 3,530,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53266828ac7e4fedaee969a984fe9758<br>SHA1: 6365bf70c4cca8667346608d2522cc5bcdc80bcd<br>SHA256: d5b716d6e87cf991f48bee15fc6a2ff4a7a250b0ba90c41ed48d0076956afc0b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.0MiB (186.6MB) – 3,530,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbd1b6a78a6aeeaa634414c532617658<br>SHA1: 2ab36dedd29c9744f7acdb23307bceb8cacfef2e<br>SHA256: 656cc9aa84a60960361fb3dbf2dce88cdbbcfe4589d7abe6c4986f5755791962</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.8MiB (231.5MB) – 3,530,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a5ca093430b72d2d2569ba9cdb81401<br>SHA1: 5afec5de2e6f2dd927783a93b6b99397e43a35cd<br>SHA256: 47105501df76345664307f9d9f7817636418e5e86a3460c55cbb38fb3a1d42ec</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.3MiB (194.3MB) – 3,530,690 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59969650e60d96d0c4f00d9a1153264e<br>SHA1: 72cbd6ce1e3858735390c1d945aa06fc18636a97<br>SHA256: 697648f4c69a495dd65e506701b58f6c0af6eacf72b6b99223eb3226d4472a4d</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>185.2MiB (194.2MB) – 1,953,972 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc548a6457a782570ed167a73f63f7f6<br>SHA1: 3ba8c274cadfda55521fac7129b4559e1c13400c<br>SHA256: 9e8415fa4658912e03b1940beedf7a78aeb4c336c6f2ddb807379b60d45c559f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>189.6MiB (198.8MB) – 1,953,972 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34124ee40de06e6f490c4ec62a6d6456<br>SHA1: 1e864ae8bd44afb7bca8e54977cc2264adaa5c35<br>SHA256: 5c851cb148c81f5d8dfd945ef553a9baa96c1046d784c5967d491a7616789a36</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>182.9MiB (191.8MB) – 1,953,972 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ae7e433f02656d8e305d17089d248bb<br>SHA1: cff4cb13d66dc8ae13be31c12af8547cb3678973<br>SHA256: b6bf4a78acc426acb085a718012c0f6e3d123c5ec468e07ae0184bf1a764e73c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>183.7MiB (192.7MB) – 1,953,972 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba4e8c730ea10faebda745c2071c2c15<br>SHA1: 6d608dce8250e603d5a9d70c54ff2c01499184f9<br>SHA256: c7648eaefde4ad58f1275eb034d2493591e70cab8ee994e6e26e062bec88d6f9</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>203.3MiB (213.2MB) – 1,953,972 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30ef2a8463b92ff2dad1593fcff24390<br>SHA1: ed9e6344ea5e4e2daeabd0eb836fc8a45d073024<br>SHA256: 396519996df35b71802c118955d37761e668beb686bbfe38008b8c68cc7406ee</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>182.6MiB (191.5MB) – 1,953,972 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f9226726653dd458240bd18fde1e33e<br>SHA1: 0ceb6e18852ab1124a4a0f7c397cae6ad86d7b10<br>SHA256: 912d007b3b1abecac83467f9965c9a28a8f316199fbdb56c05f9257e03e1d8af</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>203.4MiB (213.2MB) – 1,953,972 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 337124f2256e3d59a99834f513bfc3ab<br>SHA1: d5a5c1dc00c1b3f72cd781332accf64843aa9928<br>SHA256: fb1315d63ab3ad7e6809e6321ec376b909e4ab13a3630b25cd138b6665b9fc6d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>186.2MiB (195.2MB) – 1,953,972 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e831d2a4a8bc7e27afd8ce8ddb78ae4f<br>SHA1: c9ef5c1529fbf8bba51ddf30474683d45656228a<br>SHA256: 6657a6deca5a8dcecc74fbac93778e36608f07d54bc6f448daf80bed4edb7330</pre></details></small> |


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
