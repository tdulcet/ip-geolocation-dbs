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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-07-06<br>IPv6: 2026-07-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.375 MiB (5.636 MB) – 268,970 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62e713e7c03fe94c0aad4c63490cc8c9<br>SHA1: c5ad1288051c2401d3cec499ce4a0ec8dab58044<br>SHA256: 7bf2d0359f4315e76532ac534594d7cdb343c996c6d536d24356f09675019dc3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.72 MiB (17.54 MB) – 254,152 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 621b0f4bc026a149b496ae7d8fde4622<br>SHA1: 6e66d75c9ba50758cd5134e9df875a11e9f2e2e3<br>SHA256: b443c88771ebba77aad1f08b38b25f90d6317f514338c865644271bcc422d2be</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-07-07<br>IPv6: 2026-07-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.015 MiB (9.453 MB) – 451,395 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9c18302b7685f9c32c146757e1c574e<br>SHA1: 938a58adb1239b13150c15afa94dd3de92965200<br>SHA256: a26c212fb8267c66a329821c5062ff27ddaa47815f5edfc0bd46d36e182917e5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.919 MiB (8.303 MB) – 120,451 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 62f1f6401236232107da0f3cccf296ad<br>SHA1: 294eddc92b820514b5933bc5ac66f49a22da2282<br>SHA256: c96d6af4bce9d6e0ab50add73d356ea7a9d4b8b887792be02db0a5433418d46c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-07-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.53 MiB (13.14 MB) – 627,527 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d62d8163ac0c4880abece4a2571d5ad<br>SHA1: 1df4076e0488b1c13c6f4c94e9cc1b91da23a0eb<br>SHA256: c1c5b4e8f6119f9eaab31833798c8afd4249b812e08cc7bdf0e47402fa7422a8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>42.13 MiB (44.18 MB) – 640,218 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4240e1b88815cf40faa7b77ee0c5b46a<br>SHA1: f80005493a604b47f3726205f19dd761e10ab125<br>SHA256: 91e1ad838a43f1aa9e3d252cec81834a0dfc365a70cded29cea77bda354dd999</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.078 MiB (7.422 MB) – 354,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ec835290735187164b1f2f622ad9c0<br>SHA1: 10464ef5eb489f4745096b1c71046b06409244b5<br>SHA256: 6bc4af63c1e15b4d99d5b9dd9cddeb67bbf2eafc2529ba5d9ec4525e0fe7964c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.51 MiB (23.60 MB) – 342,046 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569d0c6b66a745289f0e152318090f38<br>SHA1: baf1ef75355d41d9bc4380f97ed3b085db479655<br>SHA256: 8940a06c7f9a27f129048c5a7a0b1579b368020d88f2d2efe0fc813b6d2f97e4</pre></details></small> |
| | | Full Location | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.3 MiB (219.4 MB) – 3,666,805 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b729ab459cc2b765b3b4ea035f481b<br>SHA1: 1496af12b72ee784e304cd84eb7335c826bc3906<br>SHA256: 69fc5ebf5414a7a939fc25a35f3128451cf340211ae51ab9f82d53a331d8ca03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.3 MiB (473.3 MB) – 4,386,528 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f197b2ebcfed77f9adc3310fc7b6020<br>SHA1: 24b1454a40fdda39f37fa9367a6a6a5a88d3be33<br>SHA256: 0160ad6b5bca3517eb65f79d6db1f9e373eeb34cfccbf189a588bb330d17af06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.663 MiB (5.938 MB) – 283,439 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5e0b2b6a8aeacf3ff5598adb8880765<br>SHA1: 8804233331909b27cede1b5b43c2f97e3e0fa7fb<br>SHA256: b76b958024d8951ae29a80cf988f69d1e662dcc0bea8d923f50bdc702ec7cf2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.09 MiB (23.16 MB) – 335,708 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a285d07eeae37dd9fc478666744fc01a<br>SHA1: 088c9efb11f726ab15157c87e8ea1f653a7ad960<br>SHA256: 276a36ba7f5863bec8cfdfc9f38541e0dfacd40d41312852daaca8be67b6585a</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4 MiB (176.6 MB) – 2,914,372 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77a6d0d39cccc6773bd841068fea21aa<br>SHA1: 2b573d6c293a367a2052b0737018f62a9b4b74c1<br>SHA256: 63c79df13cea9f7d90cb141a952a0ec792fe5f5c39e6a4cb98f1caae5055b951</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>295.0 MiB (309.3 MB) – 2,857,634 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78f9a0f50b954077a7222ec29768405c<br>SHA1: e7cf8076d18ce13f2ca1ddb68037263adaac2c3f<br>SHA256: 8eb07f6e7f6d570b63e6735ef434d9dbfc7a394946b35bb3ecbb67d2c31d9863</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-07-03<br>IPv6: 2026-07-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.42 MiB (11.98 MB) – 571,931 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad761f835e106b358c7f95930f60c548<br>SHA1: 3d569c1208ecc205cf8525239743e5b736c06b19<br>SHA256: 9e0b044e6fb5fe450899c9e91909a7149601d4f6be7eb0d239e1fd9ae1a7193d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>37.10 MiB (38.90 MB) – 563,781 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9a2b30200233a8a6d7eda98daa0629a<br>SHA1: 6a4a34f4cba12c56f17c3734238fe87ac9cca05b<br>SHA256: 77651927f41846cafd85e0b7dd487c1f7cf1c046f16f4619ea1bd50b2f12ac6c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-07-03<br>IPv6: 2026-07-03 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>192.5 MiB (201.8 MB) – 3,754,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c9b74733d0e08745a809f1bd0f8e5ec<br>SHA1: 68d6fb8e70eb357d57f71fb0fe9c3ace5c84f349<br>SHA256: 07569aa03831eaaf821d1d74e545c8487d7251811b7a63d69236b7e3133a1cd9</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>201.7 MiB (211.5 MB) – 3,754,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2909001c806acfbf235f719191d12647<br>SHA1: d4b0de23b04a50c4307d441bd369de81593dd40f<br>SHA256: ef9ca1a59a4c67ee533d333976ecb127bfbf45ea802e7b90bc5bc9a55dd1c88d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>191.8 MiB (201.1 MB) – 3,754,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01c0e5b29621d71b84b9075475de3b2a<br>SHA1: 4ce5cffa5381d3a5f172a64f56e8323b0639b4ae<br>SHA256: b404f425c0056bf4968e6db19266cb62a16e4c3abcd56798e8a762097feb1ed9</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>193.4 MiB (202.8 MB) – 3,754,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fc10d7b6fcf6b7509a63c933080cdd3<br>SHA1: e398e6ead2e53f57f59fe6657660e83c7d8dc9a3<br>SHA256: d4686b10ceadd95e479f8e140707e0b595c0047ae022d5cb9211699348a33bde</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.0 MiB (255.8 MB) – 3,754,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57d440b26965914952509ce6f4077982<br>SHA1: 8baeb94cf0627e6da319e4fb662f758bcd4d595a<br>SHA256: 2eddb0bec9e476376af5325bfd0db9a373340f0aefffa8be8b37337614692357</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.0 MiB (200.3 MB) – 3,754,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76458e5eec95dc55893a770537adcf96<br>SHA1: 0f3d8c678fb2cbaa5220a0c3bfbc77a62d1a9e6e<br>SHA256: 63507118af311fe7e8fe3ae47add7dda7b1582a194f4bf96bd060a53f6137876</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.1 MiB (245.4 MB) – 3,754,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85d6f78dbe44c3de37a4131fdbda0f78<br>SHA1: 47091451cdd07e3f2995a45f657dcd3e70bab23a<br>SHA256: 1a46137ddcec275928790ad7cc398e9f1378f74e6ddab7c70d2998b867b8f169</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 3,754,876 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3fa8aefd1327fe6510104a9944b1f0d<br>SHA1: 7cb2f54ac7d4bb583fe4b0eec686f512cf9580b8<br>SHA256: dedae350d08b68e0ec97386d16c1034c13b18f750e5f5305180959de5829cd49</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>196.4 MiB (205.9 MB) – 2,062,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ddc191a9ccb23744c6180070540596c<br>SHA1: 53b004af23aff4a09cd26a487240c41ea5d5e7c8<br>SHA256: 9c1e27b10180462e927a69a54e4e35f21da0166a70c68722bb6a1ac6b22e7807</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>199.9 MiB (209.6 MB) – 2,062,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cb59487433d0213dd1b2ba03eeb9355<br>SHA1: a8bb82c7021058bd1b57309e635d970b5932ad6b<br>SHA256: 2d8b6e4fc691606e1952099c46cee6affa0e1d76c039442522b5a00f588eb579</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>194.2 MiB (203.6 MB) – 2,062,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a091b197e09fefbd21a72b8fa947364<br>SHA1: 1716c449b94faccb72e5f7384f0abd302775f84a<br>SHA256: cc3520b762d68356235e721146a08d3619daeb2e203672a85624830409057711</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>194.6 MiB (204.1 MB) – 2,062,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acd99c0ca72d75c8cbef656f913b5c30<br>SHA1: de8c7d59f05086583ddfdefa637913e98d60f712<br>SHA256: cec641a3b452f3e245686330efb4cce1b43662d7b17309f7e58e41b793ecf542</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>216.5 MiB (227.0 MB) – 2,062,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fc26aafd059adda45ce8512fe4a6f0c<br>SHA1: c1bc8bb739882a4626bf02cd86e41713e4fa6fd1<br>SHA256: debca5008c7a00bf1d7d4546c67f711c717c8407535a5dfc74735da84564fb76</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>194.2 MiB (203.6 MB) – 2,062,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34eedea95c1f2325711eab971dbfbe7c<br>SHA1: f2cf0990d3256412096365cb2c1859027c005a49<br>SHA256: 4fbd99e42e6f78c4a3081f138f15d8a6c6841d1d7a925c9303a00e0a69e167cd</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>215.0 MiB (225.4 MB) – 2,062,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd913b11dd4c8a3062f676dc0d0bb8b3<br>SHA1: 71fceab362be3a4dcfb919213f960d6f21a365ae<br>SHA256: e1eb93e3e69f3a3ee8e36463c9eb9648e334d56a76371c6b47a3967744aa0d9d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>196.8 MiB (206.3 MB) – 2,062,391 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cae1f246a169dc46e39b48083fa9eed6<br>SHA1: 776abb1c464c47f9c0fd7e37029be483965f4bd3<br>SHA256: 25e9eb8bf2cc7fe81b7c1e342f85eedf0792ecde74b9f2932b28b1d06e4cfcf9</pre></details></small> |


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
