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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-06<br>IPv6: 2026-10-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.613 MiB (5.885 MB) – 280,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08ee5dbef56c7735deb414af9ac77409<br>SHA1: 6e3b5efb818e64345481438614a19506f8d9aa14<br>SHA256: af4b348f10aaf98849d5607570c9b40f56d2153aed6741030a64a73bf09848b4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.30 MiB (18.14 MB) – 262,940 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1286f56490c454eafd8f10df8e362727<br>SHA1: fdef324dde1b3d88ec0bab0deaf21b454bb3d28d<br>SHA256: c58a320c36ba88a77601490b68397c078928ee46273c7671790f1cce0b494396</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-06<br>IPv6: 2026-10-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.164 MiB (9.609 MB) – 458,900 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9fcb61b4ec0763d25d452f8468fe675<br>SHA1: 541d1f8086d924b36e689d556d597c6b97f2049e<br>SHA256: 1fc92bdf63d586d7969414c66d91b1e3c21f23bb1a286b3f0e423354c104cb74</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.102 MiB (8.496 MB) – 123,241 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4762afc8bc5df818a8d130b0fdb8de92<br>SHA1: a1e9fe29b11553a63cfeb21b811db5e5421c8b85<br>SHA256: 62d9f03fc8ed3819113de25caa73ba37d45df5570d35871e192189d31989135f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.24 MiB (12.84 MB) – 613,023 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3cf7504517b9cdb391f6c366cdf711a1<br>SHA1: 36d3cbef95657c4a4ad39a8ccaf99707deb4b1c2<br>SHA256: 5844f102d883e27a921097d041674399df6d451bc0ae049a031b6bb1bac41913</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>62.75 MiB (65.80 MB) – 953,589 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c650abf4b43e14a24f5c0e8f04c5aca0<br>SHA1: b1715fc87a0b6a679c0627d7391124f0067a3b28<br>SHA256: 304eab5b5fed018a329468ab84f56c5547f3ff29fcabf4daef64ebaa8cc4fe9d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-09-30<br>IPv6: 2026-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.778 MiB (6.059 MB) – 289,240 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 037cbe9e49d48b0386b4034c7048c166<br>SHA1: 8c73a34d6c47e79b0badefc8537eed6ecf22a1ff<br>SHA256: ee638c1c30f847a38cdca18fb3e6e1a2eb2df7ad320e6337d67810c3bab16fb9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.89 MiB (24.00 MB) – 347,830 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4516b087eb6d889360de69e0e36656c<br>SHA1: a1976e56a08064be5a24f8e5c28ffb07262b4716<br>SHA256: 4e0d0b9bdcd967472b7f36cf1465613f3e2211b91a422044355cac7646b8c6b2</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-09-30<br>IPv6: 2026-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0 MiB (179.3 MB) – 2,956,846 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a313f9fc27ba37b673b099489446886a<br>SHA1: ece362877a757aed6d6ccdad1bf2fbcb4031e9f6<br>SHA256: d7ef0d3ca1e2b8198a0e007e322d5c964611e1ed6f900d9d2edeffda292f2aba</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>304.3 MiB (319.1 MB) – 2,947,358 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ef9a15cb810aba175baeb46886eec39<br>SHA1: a8a32cdd1c882bab942deeb72f2c8da534c8bfdb<br>SHA256: da31230883dbafd4f2ec3e54d86964a6ec028cfbcf767d5e30d1552eff280d33</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-02<br>IPv6: 2026-10-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.22 MiB (11.77 MB) – 561,958 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d2296595a7911c1d8c97bc6bb67d013<br>SHA1: 26d63fc573f53c508d64b98e3ce25a75ec6e065a<br>SHA256: e50d5f795996c19f487f7e9e7692b1059f2a036b106a9bc1abc5954d7a78dbe5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>33.15 MiB (34.76 MB) – 503,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80061a0f52852dc1cad002c61b53b7dd<br>SHA1: b7a52be07c470f0d307d55e0df5c72472fed66a3<br>SHA256: 4c812ccc4d374c47950052491481fdb10efc2586427b127e5f91faf2c38ba641</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-02<br>IPv6: 2026-10-02 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>187.0 MiB (196.1 MB) – 3,648,417 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b832afe7869dcedd9a8e5833d3d6074<br>SHA1: 26d7b46627151d201baa2fb1175a044a42c5fcfe<br>SHA256: 462b2eeea8f8aaae6dc72bb99d1b7956a42d434b6f208ea57022a9e110c557eb</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>195.7 MiB (205.2 MB) – 3,648,417 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21e462c43424fe56c22527479945a2bc<br>SHA1: dc42c36c4a7f1b202179cfd27dc5c7204ff882e3<br>SHA256: 37b3dc3a3eb6eee8ee18466792b0f39b8532b2d1bccd5965c168b9ff05e59848</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>186.0 MiB (195.1 MB) – 3,648,417 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88d56b2e0bab218d73b993963187a07a<br>SHA1: 3979f1e66b7ea3348da00a60ae5062432aa8ec5b<br>SHA256: a0797d7bc53daa613ac9cf702ccc20a536a9bfc57fca5d16358d4b22b434f27d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>187.6 MiB (196.7 MB) – 3,648,417 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf8e1c315ed153b93f28221662d4cf62<br>SHA1: ff5023a573591c3fbf7a7cb8f7708709ae2149d7<br>SHA256: 3da6f1ccbd073e0099f582e02667671af0d93ac8f3240dcd439a992533cd5f4f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>236.5 MiB (248.0 MB) – 3,648,417 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a21b63164188a0d5863c5c258a03d4d0<br>SHA1: 6821ed639a29e43bd01935ea3d482ede77f4645b<br>SHA256: 89b0b658aa7b6492772a7822627cd1ab19c39815af14b8b9caa2307ce6fa9e0e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>185.6 MiB (194.6 MB) – 3,648,417 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3bb8694bc0a8b31702c3e7d2ed19646<br>SHA1: 98ba31f542a7c41014aa20a62cf9606fa30a2f39<br>SHA256: 1e58777086925dcf6a02666d5fe8e7bea5be31f3088403be92d0a401b9fd23d2</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>229.3 MiB (240.4 MB) – 3,648,417 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbc6cf5e1fa999a4f259e2c1012f0820<br>SHA1: 53bca0750744594b690fa8edf3d49e9d7f1bc55b<br>SHA256: fcf4de5277613feed9c181b958082f0f1de10ad425959631238aabd9bef36c9a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>191.2 MiB (200.5 MB) – 3,648,417 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45d0779299894ec78518762fe3663bc5<br>SHA1: b1427e998bf15ebe68f3cecc40afb80862e40610<br>SHA256: f42c65e801a505b20cfc5da2feabdef5c8fb42ac00aabfaed893d8fa3ef0154f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>197.8 MiB (207.4 MB) – 2,074,645 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fec9e0571b490449fcc853ba634e242<br>SHA1: 220b7010435ae5ea77b85eb0d4a3c3dea5486744<br>SHA256: 0824c2b088f609e95332f3f03bb256587f8b4a3ef94845873d9cb58a520cf554</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>201.1 MiB (210.8 MB) – 2,074,645 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343f1765b0c34429e8799321d7bdbd0c<br>SHA1: 2f977f61dbee63a21c6dc365c8abf3fdb043c84c<br>SHA256: 5def181bb4e7e7f45b1d768e885aa65ff011f250f8b3ea2ff0e5cc317653962b</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>195.1 MiB (204.6 MB) – 2,074,645 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f498cbe60c3294e8369d910f2a00e5fd<br>SHA1: 9310f813f222c5a7441c47613af5904ede6c990e<br>SHA256: 034f3ca8b6d6dd52a20e0b6e50a31dcd7a1d736b5d268384feaf7a6ba5ae1891</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>195.7 MiB (205.2 MB) – 2,074,645 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe5e3f89f7bb29069dabad7468f6a97b<br>SHA1: ca59c6f6ca6b555b74abbcc404fbfe84e8981382<br>SHA256: af0ce787e97a752aaabc770a293ec2d4a54d7ba202845116204457658a2ee940</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>217.7 MiB (228.3 MB) – 2,074,645 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b327f358222c66fecaa2da0f3528e8a<br>SHA1: 057803f1d49a7ceda1636d93814c4d271f85b85f<br>SHA256: 9aa137bed6138a31cd0f3ae5331f936c900b5e8fdf9c2fed1cca93ceb88eee51</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>195.2 MiB (204.7 MB) – 2,074,645 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b57a086a8a02fd7c6074299c113416ea<br>SHA1: e746a96d0dd3dedb618ffff64e37f2626bd68d8f<br>SHA256: d96bbdf19e086064e1179b83a25544e6c06288f544457464c247fce1b6a4e285</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>217.2 MiB (227.8 MB) – 2,074,645 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5081d233a8ca4cb1e354b4ce3aae466a<br>SHA1: 6827dfd0f9ded332ab3fdfcfb89d248c2170f85e<br>SHA256: c738446b9ee9c1da3d16687ebd558b392eae3a1ac983e0dab9c109a1a9a2edf3</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>198.0 MiB (207.6 MB) – 2,074,645 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51a8f0a30389ca9b1adf48111bd3c992<br>SHA1: f2c13b3621b470852b24ae1db65031e43ac4465f<br>SHA256: 91d441a1cc766045fc32bb9543053d064d9bf2d4deb2291916056bb0e5f9084f</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
