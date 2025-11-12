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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-11-12<br>IPv6: 2025-11-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.522MiB (6.839MB) – 326,564 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0d883515e5c8b4b3163f1199f54b51a<br>SHA1: fb853bd424e69b8031f0798467fa9f8fe3a429bb<br>SHA256: d2a6d43c7a62a34e1fad82d927c37f14f3aa3dd71b842bf4413e41640eab442f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.33MiB (10.84MB) – 157,056 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39a1dccd5bc8b1bb0c5dba4d327a90fc<br>SHA1: e438037f6272c978089fb97d2e2f41c1d9d1a226<br>SHA256: 6bca6ca8949baa64140b1c7c9934f1425275975b7c6ee0f0de529bdebb1f487a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-11-12<br>IPv6: 2025-11-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.708MiB (9.131MB) – 436,028 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9c5a65e28a3f4b6a06a1f4f88616f16<br>SHA1: 59b8de49ad085f7f5ab3a405e15dc651c8fb5e1e<br>SHA256: 1047c4bc5fd666c4f3f9cbf4f83f03d0823985a5982d376593eeb33fab980db9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.482MiB (7.845MB) – 113,810 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 782c1201e08beb85dabffed0980f3ae4<br>SHA1: 1d2e2e310c32befcbad6469cca1b142fefc0e0ca<br>SHA256: a5e1b1888666918dca958ab4e0db2eefb4c03c93c2cfd220b6754b45690bd984</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-11-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.36MiB (12.96MB) – 618,857 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb1e35664541d627715d72ba353d0294<br>SHA1: 1cbe9f6cbfed9d9ad40d36f739a64d11fe25ee5b<br>SHA256: ad918397a58a35d78354c46a3903dcdda81972190861ffff42259d173b3dda0a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>65.92MiB (69.12MB) – 1,001,700 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14ac7a1f3a3064a26384d8695052608c<br>SHA1: 2638a41ed142f4d6c4303582a4fb133e16556423<br>SHA256: 30c9f0b55f0bb679618536b23772244d9421a40fa9e7a6a1c9bd62bececdac27</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.010MiB (7.351MB) – 351,015 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b145553d436fa9927d6cee221444f00<br>SHA1: 843b7bc7470f77f7a70889bca7f0073e810cf0c3<br>SHA256: a8d289151b074c668255eb1d321a0c2c24a2aeb5d42f6061a293505dba1162ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.94MB) – 245,486 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e455a11648304abcd99f5c6bb19d7c56<br>SHA1: c3ea6f03fa4fee059c88a1910284305da803f248<br>SHA256: 8f4586e376e7d38e45f03f638da9bba2d90a84820ec5114e2ce10da9e7b87624</pre></details></small> |
| | | Full Location | Monthly<br>2025-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.6MiB (222.9MB) – 3,722,991 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8adb14693f593577d9641386622862f<br>SHA1: 4789a341532d78da8e6b9fd9df61010466508387<br>SHA256: 18d6fa0beb7252dcb6684069fa602d39f95517dc0b4ee10bc0092ef22f72d867</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.7MiB (473.7MB) – 4,393,722 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fe48bb05d21d396bfad13d9ca53f98<br>SHA1: e1c547a5ade8b7c473d8429a89dbbb42b7a679a1<br>SHA256: 0b7ad446a98640e9d471aa376d976a1b332132350201538914192826c2ba532d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.163MiB (5.414MB) – 258,420 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71af8f36a1397b54f07095e46ae8647f<br>SHA1: 4e7eea5925834f1ff4f956802d8305814f9d5f71<br>SHA256: d19b4141eb99c7f37b587dd2ce5a4dc9b0a4369860115050ed1938a6d4e42eae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.52MiB (23.61MB) – 342,190 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2d25b5f83304f5ab3963662d1d82459<br>SHA1: bb6059c49131cbfda3baf36ae84efd715bf63f7e<br>SHA256: d8aa367d610898959d5d76a083e838cdbb5319f8a54b6a6b269f0bc3dd7d4e3e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-10-31<br>IPv6: 2025-10-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.6MiB (181.0MB) – 2,992,474 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8caf582afb85da7035ab080370960f1d<br>SHA1: da00b833f91f14149ca4e947ed9c030f7c66ece6<br>SHA256: a7b0f18c2da024f4ae25e028eb1834d611e0f6a4c58fc63ec6db40af5830bdb9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>292.6MiB (306.8MB) – 2,836,100 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc6b2a9b8fe3ed4d35e4b406d54dc4ed<br>SHA1: 40a84eef0f2ea3d6ea0fbc3a2c011d0993367c32<br>SHA256: 5b38c04d1cbde28d1234ab83322bf6d65bf2c6fd480c757260db36e3be83f37f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-11-11<br>IPv6: 2025-11-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.49MiB (13.10MB) – 625,102 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 964f2fb5c6e698fd45ea26d05c42e64d<br>SHA1: 0fb7c840829314304808411f6b6076f8e57e1b36<br>SHA256: f5c2d91757eb6396f4f554f144c665f68494c0e11dd51233eef3efcd719cae56</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.40MiB (45.50MB) – 659,485 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd83cdebe3ea3f5e1fe3f9cb8d416b74<br>SHA1: bc14a69cb70990aac81d6cbc557e1fa2be25d9db<br>SHA256: cf81dcb8390c0722cd001c13189bff51a42a76fe2d9a38d3f9529b6d0ff333bd</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-11-11<br>IPv6: 2025-11-11 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>180.7MiB (189.5MB) – 3,565,965 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6357d25eafc9d1d0dba64ac294a0cf3d<br>SHA1: 512061549c889064dfaa65e28d28a87f5d970ebc<br>SHA256: fb3908e45f6b689cf91c4f56cafe463d3ce8d2c04a9c35f76686ea028b5001cc</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>192.1MiB (201.4MB) – 3,565,965 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d341ab715f3ffa4f21f812b8a5e4a970<br>SHA1: ac019b1d4e22f3238fc81f3413203c70c92424fb<br>SHA256: 1361d390634477e4755686c5e6a731cc66e75c781e1316ca7151a183791552da</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>179.8MiB (188.5MB) – 3,565,965 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9638c0b8eb6f19fcf56e194e9110915d<br>SHA1: a7091c88148594d78facebac3248daafa5bd1721<br>SHA256: e4ddce9edf93aefdc89e9ec100db2eb52adc3a2c1da47109e9f1417518d731f1</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>182.6MiB (191.5MB) – 3,565,965 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39bb7a9d7981421209553f41badd60ff<br>SHA1: 9663d0b216422fcfe1b89af308cf11252f297dff<br>SHA256: 9b6b7bf6c0059878b169f5a4337dc159c38bfd8fcba142d579be2e757203aca3</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>228.5MiB (239.6MB) – 3,565,965 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 856317f09527ab5218b90f66fec0a7c8<br>SHA1: f1348719423689a7be94da1ab7b7ea8581976767<br>SHA256: 9c427442b946bb3ad5a7a046807c07a75e9fc4bb6c5ea43409f3fb44547a75a3</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>179.4MiB (188.1MB) – 3,565,965 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1caf140699adadee002922e03f290d4<br>SHA1: 52917dea5518d837c41b76f8bfc026d28fc05f75<br>SHA256: 5bd75413bc10df1c2c3a53346140fed5cc741d82d4a294db5b28a4c260c54f82</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>222.2MiB (233.0MB) – 3,565,965 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a4f544f4c34dbce7e5961c42d35cbe1<br>SHA1: 8c452b058624d0efed5b5f620ed9ee76baa03e5d<br>SHA256: 9ae4de58bb25fed498b2b13faa7ce605f4c36ad0a1a3f13c0e8cf917a5c2c058</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>186.7MiB (195.8MB) – 3,565,965 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3dd01fd9534354289840d79df498ac8<br>SHA1: e499a3dfafad88b21bec0f48cca49b73530399b2<br>SHA256: fb8805b6097be6f61bed800b24804837f0ced61f22647c7e45e95c2d4a878d91</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>188.9MiB (198.1MB) – 1,992,796 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 737335e41061ce2ba43354186d1cc1c1<br>SHA1: f4e7d1a55819a6c3111e7f7107ed92eef01c3429<br>SHA256: 01e796ccb3ded1632adc9337c88af9e05d2556b7478b28accf9640e0ab42d2ae</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>193.4MiB (202.8MB) – 1,992,796 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f2f885750f8cc666109d84371fc0804<br>SHA1: 5ef8dc303e5debccb8599172d8aa24f7f72bc61e<br>SHA256: 605124ebca2e0d69748132ddefb88305230979914655cc93cc3aaf9954fcec43</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>186.7MiB (195.8MB) – 1,992,796 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33afb6faf7dc0ef0c3b4fdcec42319e5<br>SHA1: 6729d789f07407d22c284334f6d0a8b34e808574<br>SHA256: 1b5f857a927a3532c5169c28664777c1fcbaefbeb1afeb766b2852f461cdff72</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>187.5MiB (196.6MB) – 1,992,796 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70019341bad2c355d8be2f554a81afdc<br>SHA1: 7b375c0a6e571269a31fc48310b44be59fcb564a<br>SHA256: ca66e6c98421bb228c70fadbe56d366e85232c179cd0d1ceace9a81d526d6c3d</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>207.8MiB (217.9MB) – 1,992,796 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33c29e4fee700e146e5edd3860cba449<br>SHA1: 458335209bb30de72ffd28caecc56df77b73f200<br>SHA256: 4e3b2ef977d5e791e8e1b121bb2933205275a7957aa785fbd77c20ed2ae299e0</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>186.4MiB (195.4MB) – 1,992,796 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96ede318f52406c9a82020553b4f5208<br>SHA1: f4c8010003abf40d04b4f70ac8659cba66cb79c2<br>SHA256: 05103d4abe9b2252d8a8e16004887273c185afb89be2cef951135842fe806b57</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>207.6MiB (217.7MB) – 1,992,796 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0610bdf2dc47baa047a9e42e168f4501<br>SHA1: 564ad6fcd32b71ded07e58365bdb68fd89dc1d7e<br>SHA256: 42cc0efbcea0c7c1326ae7ce2187da06a7b09e8f6c9a0279a2c5d5960b56a587</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>190.0MiB (199.2MB) – 1,992,796 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6fb7e98683ca8f8e6bb6b9d5332190f<br>SHA1: 7c96a7e528aa23ae3242e5a8aae3ae8257eae714<br>SHA256: c7eca5484dfcda81cdfe462f94cd9daa506ef7d13640447bdbddf4d486dc5d3a</pre></details></small> |


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
