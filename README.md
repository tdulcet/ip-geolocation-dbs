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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-11-05<br>IPv6: 2025-11-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.318MiB (5.576MB) – 266,389 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb869070df27fa8adca7274755855e7d<br>SHA1: 8dfadc692bf150be6a105d97748a8360334ab9ae<br>SHA256: 115e54ae28bcb159a15650d899e526950c11ddd4aaa30e8c5003bf7f8ed071b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.840MiB (7.173MB) – 103,953 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d8b296cf7de6679a1e1044ab025688b<br>SHA1: 75e3b54553984d9ecc88440f45e8887de2f4731f<br>SHA256: 2e9f277771b2e6bf886b3416884b1c413ddac1afcc7fdf9b59e33d53ba0b3c5e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-11-05<br>IPv6: 2025-11-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.708MiB (9.131MB) – 436,045 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b39f865a673113775c4c66223e58735<br>SHA1: 060261fd361710edfde0d1e46e444f204761af19<br>SHA256: 6e54fb85d194ef7ea6cce44d9ea093425400311b95d5e4bc4b1f59570efbac47</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.482MiB (7.845MB) – 113,810 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40040fe70099f3db720961435eaa2ac7<br>SHA1: 62081ac510dafdced88dfbf4430b3d3aab23d1ff<br>SHA256: 6fcdaede44fb275c4dfc7c151b083affc481be81c6eef09ad115e7bd3f4c6806</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-11-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.20MiB (12.79MB) – 610,697 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f28331ff0d81a9569f3afc3aeeaa367e<br>SHA1: f32c2d4beee9107bd52abd5ab06e4f762d808096<br>SHA256: 8999a44add3255e7c55b33b11a9c1377c5aafc6e5751dfaf053d0fbebc89a566</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>58.73MiB (61.59MB) – 892,538 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdb081af74e95e2b12d15f438d4f8673<br>SHA1: b3d455c81be01d2d6a1ed4beceb0ad2e7a508319<br>SHA256: 63a99121d9b976e59b1df14b58e1f5df925d0e1d95f61088e2dd423e11ca6ce2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.010MiB (7.351MB) – 351,015 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b145553d436fa9927d6cee221444f00<br>SHA1: 843b7bc7470f77f7a70889bca7f0073e810cf0c3<br>SHA256: a8d289151b074c668255eb1d321a0c2c24a2aeb5d42f6061a293505dba1162ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.94MB) – 245,486 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e455a11648304abcd99f5c6bb19d7c56<br>SHA1: c3ea6f03fa4fee059c88a1910284305da803f248<br>SHA256: 8f4586e376e7d38e45f03f638da9bba2d90a84820ec5114e2ce10da9e7b87624</pre></details></small> |
| | | Full Location | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,722,991 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8adb14693f593577d9641386622862f<br>SHA1: 4789a341532d78da8e6b9fd9df61010466508387<br>SHA256: 18d6fa0beb7252dcb6684069fa602d39f95517dc0b4ee10bc0092ef22f72d867</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.7MiB (473.7MB) – 4,393,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fe48bb05d21d396bfad13d9ca53f98<br>SHA1: e1c547a5ade8b7c473d8429a89dbbb42b7a679a1<br>SHA256: 0b7ad446a98640e9d471aa376d976a1b332132350201538914192826c2ba532d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.163MiB (5.414MB) – 258,420 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71af8f36a1397b54f07095e46ae8647f<br>SHA1: 4e7eea5925834f1ff4f956802d8305814f9d5f71<br>SHA256: d19b4141eb99c7f37b587dd2ce5a4dc9b0a4369860115050ed1938a6d4e42eae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.52MiB (23.61MB) – 342,190 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2d25b5f83304f5ab3963662d1d82459<br>SHA1: bb6059c49131cbfda3baf36ae84efd715bf63f7e<br>SHA256: d8aa367d610898959d5d76a083e838cdbb5319f8a54b6a6b269f0bc3dd7d4e3e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.6MiB (181.0MB) – 2,992,474 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8caf582afb85da7035ab080370960f1d<br>SHA1: da00b833f91f14149ca4e947ed9c030f7c66ece6<br>SHA256: a7b0f18c2da024f4ae25e028eb1834d611e0f6a4c58fc63ec6db40af5830bdb9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>292.6MiB (306.8MB) – 2,836,100 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc6b2a9b8fe3ed4d35e4b406d54dc4ed<br>SHA1: 40a84eef0f2ea3d6ea0fbc3a2c011d0993367c32<br>SHA256: 5b38c04d1cbde28d1234ab83322bf6d65bf2c6fd480c757260db36e3be83f37f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-11-04<br>IPv6: 2025-11-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>13.07MiB (13.70MB) – 654,081 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47271849395276ac845e496fea8701f6<br>SHA1: 91fa933a454c92a50c534bd32dd5c7d43aa89651<br>SHA256: 5bbcbd9c5589db5d22616ebf47a5a4b6957455120274a336a2a7d93525379ef4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>44.21MiB (46.36MB) – 671,845 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9c3838a280cbc302a3012fe2f9b1e44<br>SHA1: dea2d5d742366b6c1dcaa015f8247d47eecb5c5e<br>SHA256: 94978fbf60229d5f27ffa3eae259125396c41914d35d3e20cc40b8ea2bfd9723</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-11-04<br>IPv6: 2025-11-04 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>179.7MiB (188.4MB) – 3,541,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bee255f094d454f01c1c4acbae014ebc<br>SHA1: 5a0b73a523b4d42f36f316f78230b183309ed9b2<br>SHA256: 2ce0c9e2b3deebb9ed4fdafb082e5febb2eba4f584606c0071c48084743209ba</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>191.1MiB (200.3MB) – 3,541,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ed904137b316042e8a101cde7c1c736<br>SHA1: 4b0dc24f56301b548a34ffede8462cf3a9db8b9b<br>SHA256: b04c8c681ac053759268344b12926a547d74e3ad1a64adbbfdb3e023cffbe1c5</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.7MiB (187.4MB) – 3,541,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1c7a050f78ab22601d83da2ce6d977a<br>SHA1: a3a8cdc0bfd1577a46109f057c0488898630581d<br>SHA256: 569649ddf871155db0c7ca6ffb4c9e16c124cb8e01962fbe0d120a1804689ad8</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>181.6MiB (190.4MB) – 3,541,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6a6e1883d95125aba18237edd6dc62d<br>SHA1: 81017a0547af249a8814a3462dbd6e52437c0c09<br>SHA256: 286629f826eba0a95faf85711e18a34e243454f02781055bf8e63fd1e09497ed</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.4MiB (238.5MB) – 3,541,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0397bf5061375f066df0c8e435f591f<br>SHA1: e33e306a488fd8f74ba39dd672db30cd1f37236a<br>SHA256: 686cacde6c8cc5dcdb7ec6365f5cc4f532bb70aad42e0b62e02ca4bb273deb2b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>178.4MiB (187.0MB) – 3,541,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 562e9d5718d0114d0898a935066f10b3<br>SHA1: c1eea72832b8fc6cc873210558b3668ad3919f7a<br>SHA256: 26df1ac88f05d5c1a8341c4a9b6d808f97a56d53a1ea855eaeb9c8ecfab409b8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>221.1MiB (231.9MB) – 3,541,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca2a09138485d6a9a7a46bdc358030ab<br>SHA1: d6704d1ea4397b21a49f06d5e4693af877b24253<br>SHA256: 47dec88bc2de3d9f2c52ed1049169761bdacd6e414063dcf54aa2b5fa165981b</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>185.7MiB (194.7MB) – 3,541,679 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43911012c3dc7eef0d65ffb20961f230<br>SHA1: 9ffd3b74603ff3d492d479d668dcb4cdc55822f3<br>SHA256: 2670f578cf00e04c0d7de72859bc46a9c92185b4a02d1d137affa07459cf7b1c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>184.2MiB (193.2MB) – 1,943,254 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c18b9422b00fd26c3ccd994f5603b88e<br>SHA1: 3939f6cb964b551c233ebaa9c99c7eef8635b2e2<br>SHA256: eb019932182bf87137f7b191aefa48c28b33caff83756197992d086c7f1bf4a0</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>188.4MiB (197.6MB) – 1,943,254 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9be98ba8ef1b63657d3f342f67d62d1<br>SHA1: 0e41ed3ecfb971817f6cac181d25479ddcca4888<br>SHA256: 314b7f6848352fcea7ad6664e6cfa03b74c53539b0da956c9217668a2f4be893</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>182.0MiB (190.8MB) – 1,943,254 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64577c430e312bcfa191a83f4a503c5b<br>SHA1: ec2abce06345e33e2f466b0186da05c31069588a<br>SHA256: af5e7c38319eb4dbfe5bd1c56cbba57c083d8e95551e1b825ed20a6379a6d2c9</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>182.7MiB (191.6MB) – 1,943,254 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a27f9a239423da6671336e11e23a8d66<br>SHA1: 0d7ca703fe581ba6cb3027ad9136a3bc425a821f<br>SHA256: a7642a9ab80d6c05b72ca734677527d0961c79b728e8824f4b5bb7039aec5831</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>202.2MiB (212.1MB) – 1,943,254 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f57182de11a9382dbe92b040a3868489<br>SHA1: ab67ecc9f41e6ad1633ab4097400f712cee0ad5a<br>SHA256: c4b0437cb6f0d1d6293f417d9112a8228c3e23d981fe12bd22d3e9ad61e8b565</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>181.6MiB (190.5MB) – 1,943,254 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f9f416237382b516aa71e83a2204b11<br>SHA1: a87a1a35faaad70cf579b3dacb5480413e55ef56<br>SHA256: b8f634bac61727af881c57e01a7ea0b6e37d32cb988463dfed2c6d94383d4554</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>202.3MiB (212.1MB) – 1,943,254 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a01265f68e236444c679f3fc394341a<br>SHA1: defd6004d0aa505dd8c40dce34b1f5741f618abb<br>SHA256: 466ffbbfe048456487d9e54ac8b8c42e3ce0dc99958e36c02bb7aa8be3e7337c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>185.0MiB (194.0MB) – 1,943,254 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8cfaa0961f72bf1af352386827a12283<br>SHA1: 6241ae40d301e03493c8ffba390751d75f5667b9<br>SHA256: c07740cfa36ad5ab6cfc8ed08d27f53ff743a37c25e5fd5f18e5964f5edfb927</pre></details></small> |


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
