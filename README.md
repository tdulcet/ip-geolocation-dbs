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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-01-24<br>IPv6: 2026-01-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.411MiB (6.722MB) – 321,018 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 783130108deb157128f4af9808fae32e<br>SHA1: ed5a1258335a34b92a0537fb3b87a443549c0450<br>SHA256: eef6e2f24f808f906d5cb52ef40d679dcf20d63ee4d2249a48c34afbab562f02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.53MiB (11.04MB) – 159,970 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec132722f673ec264726f9c01b3d5535<br>SHA1: 7c2fc15b535cb81f2f09dfd00ce23d08ed61009c<br>SHA256: 170507664a1bb49bbd75a55bc10bc451321a85e8ce65eda94a9319719fed5749</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-01-24<br>IPv6: 2026-01-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.209MiB (9.657MB) – 461,059 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ae44765c838bf02aafa7831be26f841<br>SHA1: 43452d93c413d3120dea9b4ab95b02f0363bb836<br>SHA256: fd04a24714c4b9a1fb94e9f91bf13cf2bbc5871d7309fe1a528588b140ab302f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.549MiB (7.915MB) – 114,831 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3dafbe3a79f086dd930d137e9499256<br>SHA1: c9d676ada26eeb0a25da0127d7897a7171323449<br>SHA256: a17905e36b432a5467c1ce599b59842e481fac21d7338553e412e72fe54d8eed</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-01-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.08MiB (12.67MB) – 604,854 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70902a9aa1ad9cf82d9e7594b3eae806<br>SHA1: 83b1bede31a5fd8e88c700d230aece70d8bf218b<br>SHA256: cf5aa94e39b3c9015a31b843c6405b5eb12a0179e4459dc4e6fefedb27bfcb5f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>53.28MiB (55.86MB) – 809,630 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4b7fa71d3bbab9fb01d976f890f8267<br>SHA1: 74533b458d8b28735e471f99d9948ae47cffeee6<br>SHA256: 2408e28a1d84be172ed0e3d242b539578b463493b4f776d39fc7484dd02ad2b9</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.843MiB (7.176MB) – 342,905 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7f0c42b88b3ee5ac2070e71f756f963<br>SHA1: 4416542c9574226ce202070dc48ca08edc6fab0d<br>SHA256: 5393382f53c552965d88b65e40e02f63c643f2379a931aaecef8209586b9ced2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.52MiB (17.32MB) – 251,059 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232548602865156556e4ff9d7db331da<br>SHA1: 61d1e0b2cefeca101ea9e8530969dab152188ab6<br>SHA256: b004edb93559a31ded3baa727a5d781edbe90c29420b4d5691f44e917e83bdb0</pre></details></small> |
| | | Full Location | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.7MiB (223.1MB) – 3,730,744 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42e04cdc8d81a8ce6b440accea48b373<br>SHA1: 9c414f68d243d9ebdc8b7c65e081580b035b663c<br>SHA256: 5274313529b847bd8629fb44b41144c683552f55760a830f535892f20b8e46db</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>457.0MiB (479.2MB) – 4,442,155 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56e8f0cd6817f6807824ced45628cb9<br>SHA1: 316812aba9e80b97b08bfca58defd796b628d008<br>SHA256: 44317ed175935104135d379f2a9918ca97141e9bf034ee1bca6cdf894093d72c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.345MiB (5.605MB) – 267,509 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0604e023f5c6722d46ef6793af281ce<br>SHA1: 3eb54f1eebcd039df05135ab29260e09bdd4fefd<br>SHA256: 3c8d20a60ea0af489cb12852284187081cd8541958eecf909e2f4c90e9f0555f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.02MiB (23.09MB) – 334,578 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d24f67bbedc322d93d7843237e6d08bc<br>SHA1: fdf5e7611f467995a14f85f97c32c055b05d983f<br>SHA256: 122f2768c962576ccb07d18b092f50799b7b9ea494a23db97a4bb4754c05e303</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-14<br>IPv6: 2026-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9MiB (179.2MB) – 2,956,256 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7eebf486d9c42702ac790a4ac4e81b3e<br>SHA1: 110fe57678506100a087eda5e8cea65a848958d0<br>SHA256: 80471fedc344947500ec0408ae5d771afe66c98c0ba3989ad3f556cb157c73ed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.9MiB (302.9MB) – 2,799,002 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4bc462fd69a5966f640f89baf03f95e<br>SHA1: 51eb98defa6d6bc9f2d654be1fc3e566c1803852<br>SHA256: 122e835b4e22ab281b426d9e1eff933fe165e08f77812b4b427e046722b296da</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-01-23<br>IPv6: 2026-01-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.12MiB (12.71MB) – 606,715 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c58cd5801f24465b845c0ed201c76aaa<br>SHA1: 3b066f55d19f8da6596257054d94a52604c55e51<br>SHA256: 29eba5a44bfd2cd3297f5cb26255dfbc0cc227b0aaf34ba8feb042b50ce08857</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.76MiB (44.84MB) – 649,805 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c101f8c236c12ad169f3b6bb74be618e<br>SHA1: 482cb5abbcc7415f346c8ba7fdb4fcee5fe25801<br>SHA256: 40fa218a2b8842237d905b125c5a364009569ebf68ca636703b5b1f1bc05c672</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-01-23<br>IPv6: 2026-01-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.2MiB (186.8MB) – 3,519,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56c4253a50e216fb2d2cf452dd125140<br>SHA1: 7e8a77e503e9193a2d488c88cb673048a1ebb217<br>SHA256: 6f41e8aa7da263dce58960bb60a3c331be56bbf18031a20236ca66fd3e672c65</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.2MiB (198.4MB) – 3,519,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c68798b7e17d2763487a2ac51933ce5<br>SHA1: 9267d1838b60b0c53d42eed33ba3b59bd28cf699<br>SHA256: 413fbfe72cf52237018e924888875c1a2371c2d5abae762f3bb7384874baea8f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.3MiB (185.9MB) – 3,519,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31e22bdc7a9d4f0976f13716d658c988<br>SHA1: 909090fb4e80b70b697f0d6b3d66ec10fb1296ed<br>SHA256: f5e94709f9eb983107a455e586afa92421bd073961ee25a043bd91a2161dfd50</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.1MiB (188.9MB) – 3,519,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 126a0d3ef680bac8e6fbcd62128def31<br>SHA1: e6af89c3e330f16a9778b16799cb41e1e97d627e<br>SHA256: bc7d70b5fec95b90a8f42c35e283116c83b6bbeeef6fba9718bafaa7118e9c60</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.1MiB (236.1MB) – 3,519,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4c6f7d9425685c6b950df542d42a1d0<br>SHA1: aedbc0a16e4bc546bcbf7b823b4a07b8b93eac26<br>SHA256: 6448838064dc22e1f3f5211958709eed12394270f6588ac34a445566ea60f30e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,519,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1a04591a297d45253fd97671314e90d<br>SHA1: 70512d141eed02e13c4b15883fdcf081d04cdb49<br>SHA256: 119b1ba46b331af810c54461e02354e381572b47eb1f1be0d19e6903647e0fe8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.1MiB (229.7MB) – 3,519,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89582ee082a8492f2b4f7d3330da8a2c<br>SHA1: c3779411a2a3aba1910f4c9b10cf3e3b720fc884<br>SHA256: 3fb1782473aea00e4672ae196a09dc117dfc0c7359adf999fb7b8e3ed5f7653d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.0MiB (192.9MB) – 3,519,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 885a0b34b0212d5e1311684398ea84b7<br>SHA1: f59e7f6559b5d70c81e11a015b319e0ce2b82a06<br>SHA256: 820cb6e193fbcbb8aa3c83aa10087011cdaf6378d05adf5ab630f46879285a69</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>185.5MiB (194.5MB) – 1,957,545 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b8839110e9fb31941e68d7d87c02e75<br>SHA1: 362fd49a45680b3ece00b248da1e117d26dcd63b<br>SHA256: 849a8ccd1d8636d3aa75fa2822295583ebe0af15cb608b2c9b62741b16b55875</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>189.7MiB (199.0MB) – 1,957,545 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d097c006f55d4811e45653989653786f<br>SHA1: 9550dea90c104475ffe3461bfd38ce6b91726323<br>SHA256: 33100ac695046cc3d030dd204de3850fdb907bce954923c7922c99fda7702f77</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>183.3MiB (192.2MB) – 1,957,545 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31c905f8fd37b85ad07fef834c2060a8<br>SHA1: 4e551e7a2dcd4f65450c71b1e72dfb8e09da8fe6<br>SHA256: 1deea2f008f520308ff24a9c9e4dc92c7fe27250198333232bf7067227dea755</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>184.0MiB (193.0MB) – 1,957,545 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 413c9f73dfb92da92fe958ff1168e318<br>SHA1: fa398c386d907479ce270729fa274f15d221d2e9<br>SHA256: e518aa8321c943f510a00e9a74f96b425577293bac74eb0c7cb56c50c663014d</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>203.7MiB (213.6MB) – 1,957,545 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da4ba6686bcf452fa7108e9d8221d283<br>SHA1: 2ec90da775474bbc827674c2f92c8b5d656cbb78<br>SHA256: 935fdc34770c441c7a274df7305355db3c4795b5dde0f5cea20afa082a47fe69</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>182.9MiB (191.8MB) – 1,957,545 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3903700e5ab664faf792ba594592a55f<br>SHA1: e991c0d44bb1a157a34102a95422d7f39e6bb21e<br>SHA256: e9e330f57d7ffcea8c67257ca664022ea18aa15eca4ee6b52dae7c2adefc7246</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>203.7MiB (213.6MB) – 1,957,545 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3737e51685388a04c728243797e91de<br>SHA1: 0cb370b888fac164b7b34f28cd8f7c3ca9c5de87<br>SHA256: 62226f9673400466962ab4cfa4ce59bdd15cabcf3cfe11968f12d78dd5960496</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>186.5MiB (195.6MB) – 1,957,545 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6e00519dbcdc216a6869b39ff706c7e<br>SHA1: 15e9a2d1cfa4e49aad32ce2b63a680936ccb9c1d<br>SHA256: 3683674c5836fd2ac76994b10117d12aac685ecc20c88640633152f6b9192f6c</pre></details></small> |


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
