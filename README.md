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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-08-15<br>IPv6: 2025-08-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.188MiB (6.488MB) – 309,828 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86070e19b8bfe9a7ccc659558daeb60e<br>SHA1: ef94fd95d5bc8885645193759880c6812da71aff<br>SHA256: 3372085956c9b2ac9659eef8a1f3f96683129d6eac622583caf5123eb5c30b3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.69MiB (11.21MB) – 162,442 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d52a6e3199f90083be3fdf520797c83c<br>SHA1: 79c5d330b6ec98fa01097d4911f6cc61480c004a<br>SHA256: 1dd3b313572be232d50282bc202990249bf4db3f1a0dd8f4a1d443177b4f5969</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-08-15<br>IPv6: 2025-08-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.594MiB (9.011MB) – 430,338 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57c12a2a836f8395270b000f87d5a0b5<br>SHA1: 390c3fdd69d54d9d4db6cfb43cf5968dd14724a6<br>SHA256: c791d17a25117eb09ec45500b155fed265429f66f00e29014b86756de81d7789</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.213MiB (7.563MB) – 109,730 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1dfd04d170a603ba62f62285305ad08e<br>SHA1: 43a65c9b7d789f32cc373a75409b63a7c70e781a<br>SHA256: 542cfd503ce4ce823ae82f573850f7ad0baebf4b4338a23dfafbee430106a9e4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-08-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.90MiB (12.48MB) – 595,898 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e37ac3b08a1bee893e243d8e9446162<br>SHA1: bc9fa7be0c8689c315638b2bf5ec9705065a4d0e<br>SHA256: fbf8bcdf7fca5a2fdbd2d3a69ecdee2d7f5fe0ec66a8cbe1084c4d6299901555</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>92.62MiB (97.12MB) – 1,407,493 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85ff98779ed50a8a492575ab65707d18<br>SHA1: 02f18f83a9af1f2844b850bba26fe2506ffc4eb1<br>SHA256: 756f83fced769028f52c81aeda7cd89c70e9c64fba5ecb461a042b5c18364e62</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.840MiB (7.173MB) – 342,618 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fced5df941addb9056b94a0f6f68597<br>SHA1: de47b1f9ba9f0ffbb556398c71c34fbf530591e4<br>SHA256: db6544ac94d1d22426f86a2b1b3d5b70f2d1b38ecd54fa536f817c5e106d4055</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.11MiB (16.89MB) – 244,855 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f879c057a5e3c7efdb9494722cfb973e<br>SHA1: 2a0586c6bd247669bc87d96e3dab86aee5e3a9ec<br>SHA256: 648aa19d3202320593d396fb44d416960c2d602a521000ac2510160c5d272d14</pre></details></small> |
| | | Full Location | Monthly<br>2025-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (216.9MB) – 3,615,295 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84dbaf75b3817fac2d522b918bcc3861<br>SHA1: 9b4ee36fa0923a2f68da4704164feac99f7551ba<br>SHA256: 43bd2f31f3e4f69856dfa6208d46d73b0063c028474adf986db93aef2740a7da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>447.1MiB (468.8MB) – 4,343,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4cfa7e8b0505f21943fa43a915ea9be<br>SHA1: dcb876a3bb589b77672f628a8ae019d6011d447b<br>SHA256: d3f883acce4ef8ed03ae21f30d09b7ca51f895f0830643368c5767a3642faf6c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-15<br>IPv6: 2025-08-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.152MiB (5.402MB) – 257,838 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07e653090dfd5d1c13121b162af09fab<br>SHA1: a808596024eb433213c8e90bc6277f5bb0611ced<br>SHA256: 6da92c7dd70266c69657400e1252ef514fc1e7028aa8a0e6bb3bb9294c78588f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.38MiB (23.46MB) – 340,069 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a95a5ab506163fb86cd3197ca9610e1<br>SHA1: a7fba9b72e8a271807218c6b426e547f46226c54<br>SHA256: d86789dca5ee5d16277ae57abc33199b0ea4a3b3fbd358a820c9a2d761c4edd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-15<br>IPv6: 2025-08-15 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,023 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ec0f30e04446d83c414d7ba54cd9da6<br>SHA1: 4440d7254688eef8397b92e3f583e9b9240fe63b<br>SHA256: 3eb81d283d8a85d9a1e21e2d775d4bef02c37fd3fddf7b3981fe5aef17ec27be</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>287.6MiB (301.5MB) – 2,785,870 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b12d395e9581ae946a39d0335c84cd65<br>SHA1: 66a2ff83b2e1cedccb7704236a41162bb2e963ac<br>SHA256: 8a594aae021dd354a93a799eaf42efd4fab365f15f15ca3401e4ee230579599b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-08-12<br>IPv6: 2025-08-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.39MiB (12.99MB) – 620,021 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8704ca5d1d4693be1c724088c481719<br>SHA1: faf3dc0d35c554fbf17242fbf100820a56d2e9b2<br>SHA256: f750463cecdcbf40acbf27b6b05b4866b4244521772ee48de757ff5ea0bf3e8e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.00MiB (42.99MB) – 623,019 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2cf33d1682aa7f5bee51137a53990718<br>SHA1: c95e0517c75679faea98c1cbdf93906ce70b5e95<br>SHA256: 7084a3a78471166057327b33545fe81f644ba61c7cef2b8b82fb1d2e0542b136</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-08-12<br>IPv6: 2025-08-12 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.7MiB (182.1MB) – 3,422,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc0efc6bbc5a70d460ec29f2dccac7c<br>SHA1: 4db98fbb31a2328f2c3e2df74c79cc764eee7d8b<br>SHA256: a618d37d89c7d0511e59f4465c0a780b43ca9c9b2b9909ea7f010d03351a6c68</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.5MiB (193.5MB) – 3,422,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1720466e7ddecb55d21e782683df447e<br>SHA1: ae7da7ec1b04634a218769f25e086449d1d6b591<br>SHA256: 1ebc94f2284e621639a8545f6be5c050d7ee6da3cfd0e2b252181ce4a26b6336</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.7MiB (181.1MB) – 3,422,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5170a8dcfaf3a31174ecfba5c7f57c3b<br>SHA1: 321978431b6a28f1170fde404cf55dfeeb81856c<br>SHA256: 0261d5197a9619303e9e25daa4a669eb5f9f2be8356830a6745f2c672c94cc66</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.5MiB (184.0MB) – 3,422,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51b8e560b2fe8017985430b090bb60a8<br>SHA1: 212e71f21fbdaac1a7ed237b5562b8588ebf6865<br>SHA256: bf8e4c6a9c4c06445cadda567c4d1f849ceb142914211049be7f86def08bf31b</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.1MiB (230.8MB) – 3,422,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 475a638416fc8d3dada5fbe809ebbc4d<br>SHA1: ce92949ceb84a03e420d21c3b0e68d1ea3ca3ee0<br>SHA256: 55ec641a32d246f8fe27a5d4d53ce026d681305ac638dc3492b0437a1c310d62</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.4MiB (180.8MB) – 3,422,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e07bd568f445b04a01e8c4dbf994e361<br>SHA1: 4afd04d60b3287ef186f8af6fafae19b4a97d37c<br>SHA256: ba6b8ec2d7be85c3ef9fd54676ab0b5214ed4d0b9fb2f335bd83e6dab7640a2a</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.8MiB (224.1MB) – 3,422,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc01451f13045a35a42471587c050067<br>SHA1: 6685590e0f20acb0d50d0cd4bc93e916f100ee8c<br>SHA256: d5869afbeaf87e861ff193a7c923dbe92d911b4d68aba2dc40b924a26911fbce</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.7MiB (188.4MB) – 3,422,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56d2dbfa3f8974c4bb7c13a30801912f<br>SHA1: b093ce77e5dad3ced4ac2279a4b54831a4415ef6<br>SHA256: 139006adda5467da7d74e597db01e21e0c2b9730a4035b022f075fd6fde7a68e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>171.2MiB (179.6MB) – 1,817,033 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 577bcb6368400bd7d5d23fb0fa6fea0f<br>SHA1: 1e8ed8b304e52cc16914d2eca29890f9f4f39a4b<br>SHA256: f36fd9bb230434430574e10337c1dc6ed9f3995181498ed07ecf32c5690eb019</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>175.0MiB (183.5MB) – 1,817,033 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87cd4228e11dccb645e175d2f61ac648<br>SHA1: b4d33cd55e6ba0bff17bdc424dcfd7cd25cf592c<br>SHA256: 81eed7f61e881d0363f31f0205d0528e353a43622802727dd63204c7c5eafada</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>169.4MiB (177.6MB) – 1,817,033 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8ecce845e01b25b54c6635df2b4318e<br>SHA1: 639522210d2243e5da852c63f8abe8d783fbb8c9<br>SHA256: bbafed2b692dd9127ffb0762a2f3f3b738d4110595d6a8e78ce1fcbcf8e30e32</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>169.6MiB (177.8MB) – 1,817,033 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14321bdbc3c74998061a0fd5c9f2959d<br>SHA1: 3d0e5a5b0523ea5684930b529b5cd68558dbe62a<br>SHA256: b3b28b758478288644b0107736441ca8f7a60a7aa40f5e6dd0eaef62909ed631</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>187.6MiB (196.7MB) – 1,817,033 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ced997e6f0a3cba0a0e9040b671ea4<br>SHA1: 9826ad9e7b175f809817c3e867f7fcfde577af5d<br>SHA256: 5e73f65e3498f2e5bb21f5d136a2983f86a52e810bb568431f9a4e5ec21795d7</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>169.1MiB (177.4MB) – 1,817,033 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a75d2aec2d267cc5b2729fe05600b5cc<br>SHA1: ce1e3995a2659064f446336cb5da24f137a70f5c<br>SHA256: 7f052d6e47926bde7a6bc5f71bd5650ab36c052b255dcb9c2ebd1bc57380051b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>188.5MiB (197.7MB) – 1,817,033 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c416b9a6e2236885ca276dfdf0a1ff86<br>SHA1: 2b7e865faf054ba42cf44903670bcf99424d272a<br>SHA256: 88602b058e8ac4a6554e3bab6e9eb59cfaeec18b1ff3ba688ea1bbe2dde14a1e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>173.1MiB (181.5MB) – 1,817,033 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 258520d8ca9b2824d3851b88fd18e93e<br>SHA1: da861c96c06d1786335734b5633c6b4e13854e05<br>SHA256: 4015554ee539b85390ae03b508b1a9b5b462c8ec6fa6cff60be085f6e2fd0a3c</pre></details></small> |


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
