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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-16<br>IPv6: 2025-07-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.335MiB (6.643MB) – 317,272 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24e7e97f6d8e741822c4db907cfc4ce8<br>SHA1: ea5689837ffae732e12aea5026a2c97221b185a4<br>SHA256: 7e71b90341c4bcbcabf99cdd42aee64d64cd137ff0e5b9c6a6917a11d756fdd3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.35MiB (12.95MB) – 187,618 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8fea928efb36cae7a568fcf6d250741<br>SHA1: 8b3c24e95e3bcf17ff8d59da3062958f9d7dc29e<br>SHA256: 55c651405f5822775f920f63c75a485e4c7768e56e81df73083ccb2f19583e60</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.82MiB (12.39MB) – 591,566 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b0c66a0870d7ede88edefd1df2619cd<br>SHA1: 5e88d92b90cabb58e712c90ccb3b5d399d3a626c<br>SHA256: b5275d7fd82242d827e45382a765c969a00ac97c391e8588b8e2c3ff79ff4de1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>83.77MiB (87.84MB) – 1,273,006 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 768bf6444c3919ad9dafe013ec1858a9<br>SHA1: f010ca47ed5ecae7629b9ccf6e3d44ff6a66cf05<br>SHA256: 82efa3e7224b12783275f8a8268b80fbca6f95f9c02ea5ef38d3b67b5dfd7b3d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-16<br>IPv6: 2025-07-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.068MiB (5.314MB) – 253,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ddf95be39b948ff8a1f5f72a989f3db<br>SHA1: 53e521e70cdc7bf139a71019e836b80590d710b8<br>SHA256: 50c6f2769387e3ee7cedf43b469b7ba544e29e43852d8c3fccd14dbf39e376a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.78MiB (22.84MB) – 330,989 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43bd9e1f0cc46c204def11cc25411429<br>SHA1: bb110aabf0613079fa6821963cb9072ee8a672f5<br>SHA256: ef3129675278c4750cafd639f31a9a899cbc6468108504cf55d1a6439f90199f</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-16<br>IPv6: 2025-07-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.2MiB (176.3MB) – 2,916,495 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec46eb0d6770f3a4934f80b9ba8b43ce<br>SHA1: f00f5138d48a37c35fcf9f170e21939324735351<br>SHA256: 16a49d4f2d09a24369e498fa18c855ad30e4610d4fb1424acea4ea9ccec6048c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>279.1MiB (292.7MB) – 2,704,923 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dac800448bd3a785c553531ef23da1b6<br>SHA1: aaef79ba06d4297b621a7688cc2224cb694528a0<br>SHA256: 6c59b673d7391b858e46d6527a0bce731c26713b44246050076e424d61a9f656</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-07-15<br>IPv6: 2025-07-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.55MiB (13.16MB) – 628,300 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11a40550b6b16e51a63f83b843050b7c<br>SHA1: 1651b9c9724ab0c5d0ac19de7fa4e914138a2ba8<br>SHA256: 2929e3c1e3d22316121e82c3b7a11c204b474fba23950e0e69283fe7d2d98eec</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.34MiB (44.40MB) – 643,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4771f75648ad84fae6ca616c1b4ca01d<br>SHA1: 76edd9482b6e0c145706018b4be2075dd99556af<br>SHA256: 54b5fe89a4576c1ad1afedfbdef47e67e6ac01e216297d671a9be97be37f914e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-07-15<br>IPv6: 2025-07-15 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.1MiB (182.6MB) – 3,433,928 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5bce5ba649db1065b5cb93337959062<br>SHA1: 675bb2f97671fec30a588080789f81ab89107417<br>SHA256: 6b2b5111fcb5bdc9b6abc08dad7d07fae7eb36762227aa554c25a5b6fadb5f5c</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.0MiB (194.0MB) – 3,433,928 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2c8bbe7a768643b96ed79541dff3083<br>SHA1: 6b2a4e8a2566e0962455e3c5666c84b44062e00d<br>SHA256: 72b2a61a315743d704272980b11e717934444599dd446af5e147a4aff2a73bef</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>173.3MiB (181.7MB) – 3,433,928 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54e5ab8971846309e4419c2b9d8bc0dc<br>SHA1: 3e7fb4378cfeda7d2d180b5f3a76f146c02a811f<br>SHA256: 5251585cba7331c14a932b60440e1f35fe524b91a9f428f2b5066e5ac4eb1df4</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.8MiB (184.3MB) – 3,433,928 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a68120242e739f9cb2652ae77eb20f8<br>SHA1: 7cbe1fd20746595728c1b01bc0e601385f6e3fb3<br>SHA256: 818a24d8ee9d44dddf985a1b54e28d7c0fe340ebf23f3e3c3fb0071fa1ef0185</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.4MiB (231.1MB) – 3,433,928 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a37532a317a42e22233851d51b6c0bcb<br>SHA1: 43cf52677f08d6a131a2c8a22e3daa5532a7e3e6<br>SHA256: bb756a5b989f868649d6c169d6d72db27b829ddc593c264502a1836f00bdfb7b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.8MiB (181.2MB) – 3,433,928 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b9d55028287e40ad057850d8698d831<br>SHA1: dd6a89a86cb2dad65209672889bb06d783e437a4<br>SHA256: d539b5eab74def036bef1aad3dc5de5321aa6efabd00ebf9fe9be14caef6c54b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>214.2MiB (224.6MB) – 3,433,928 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2879d6214035adfe969c1d4bf7459d73<br>SHA1: fbe31003db7f701d6117acf995473a536b928046<br>SHA256: cf0ef7162ea4922ea44e64d574f369df3e31354cade81bd267a79d3ed71fd59a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>180.1MiB (188.9MB) – 3,433,928 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61bc686d5ff01559f5f6d2c6ce002fa5<br>SHA1: de6949d6ce3112f69a776d7308f7fe1877071920<br>SHA256: 85e9e5986f87843ab33ffaa9a30a43da6aae4f7308aa47b0fff9531fc4a18154</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>178.4MiB (187.1MB) – 1,894,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b211a5f3b3f17843107fd99acb027f2<br>SHA1: c7c8e18acc5c0bf32ae1b5aa5d2c8975d737c9f4<br>SHA256: 8ac4079602cf1b7ea940992fcbfe634809ce7d8129fb9e17fc36713373706654</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.4MiB (191.2MB) – 1,894,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2629355ece0091c5f87177d1757f65bc<br>SHA1: 1bc22b533691bda73845e58156e386f216752bf6<br>SHA256: da5fbb8895306cb9e9be7bf3e704f64bdf2d0f8bc844a4968e1c9a55aea307eb</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>176.6MiB (185.2MB) – 1,894,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 610f9ff9cbd91c4c4fe26742b29ee5ab<br>SHA1: 631ea15017688285e1c25c9196d5d78f5393d2c6<br>SHA256: 3d927d7cd92e1df7335efa9d793e4e2ebb1ded6f745324240800f2695a0cfac9</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>176.8MiB (185.4MB) – 1,894,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a83788eb85bf2879c23be8b5f943f28<br>SHA1: 3d813742cb0e652988d298fee29d0e827ec6b3d4<br>SHA256: ecc899d824cf46512d9eb4e6929443ed87578152901f64af09edb591db49b3b1</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.6MiB (205.1MB) – 1,894,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19d2e38108c956903a666729723afcb6<br>SHA1: 49c72ea45b10e45319d63f5541e3488a0012c152<br>SHA256: 93cdefa1f79ff1118bb0f7a5aa3d2206368afbac4f940bbf174e07328185597c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>176.3MiB (184.9MB) – 1,894,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e6c2a3a8669c65eac496bb852f6abe1<br>SHA1: cb2adb42efe32d92372ae039f7367a0a1e655232<br>SHA256: e27fc093504ffe364bb2e5105a02c09eea0a518bfe4731c43295c3e65fa6b9f2</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.4MiB (205.9MB) – 1,894,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 879a0212f0cf725825a41c646347b386<br>SHA1: 5130184ecde571e325954ff9c77ef0b0dc1ce99c<br>SHA256: 67a17231d80522b596f459a3873ece6715bf47a69008883949edd9f2a9ecf00c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>180.4MiB (189.2MB) – 1,894,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dcbae30577c578fe075d33f241ad966<br>SHA1: 0b49280347ae208a232a0abca860f134a92968e8<br>SHA256: 9e5d27733131ea13fa06ed675c1a384175ab11e3e6c93da96ecb36e8d592e923</pre></details></small> |


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
