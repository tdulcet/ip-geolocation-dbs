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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-02-20<br>IPv6: 2026-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.457MiB (6.770MB) – 323,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a85456f993d326edfd4b3ef8b41f318<br>SHA1: 3d0b8c0aca9a178473e3e2702da232a6958b3222<br>SHA256: cf4ee3284287ed7fe9f1e0cf3cb45b3a2201328abbd79c1960a3171b21cf920a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.24MiB (15.98MB) – 231,615 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 129be68ae5557bc7c7a2ea2bdda1b58f<br>SHA1: e0d2793b10d38d636e4e97561de268d27c119cec<br>SHA256: 93f84fbccc7b08f291342f27b0608348b2e10a76d940228c9b9dca9a0d5532bc</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-02-20<br>IPv6: 2026-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.791MiB (9.218MB) – 440,172 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98d02ba4b80807136a2f4f526398e068<br>SHA1: db4a9a5c6d97ec4a5e98eab808c22c781708b90e<br>SHA256: 8d62fdb9e9ffedde1d930a1d941c9cc20e73fbc53c0ae799a42dc5fd68b7396c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.613MiB (7.983MB) – 115,804 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b26e44a4480fe197680a4c42760b31bd<br>SHA1: 9ace22ceed36fc184d7e1865796df209064ab874<br>SHA256: 740e54823261bfdece660780838df3a68cfce1163cead38842c6c7e6a2ee9c50</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-02-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.16MiB (12.75MB) – 608,647 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02f82fc8d6ce6a7380e8ecc70c327a1b<br>SHA1: b9cc209ed4bf8692480a0b360e0fb6a03649d39e<br>SHA256: 98ad3c47b25487980cb3f80d272d9b3ce3c9c2f5465f5fce5236ac60d4894bc0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>123.2MiB (129.2MB) – 1,871,889 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0e2946322f2c90d8c07757a1b72efad<br>SHA1: fa5c20a31de780b57f5f906c3e1c4dfd0384d9da<br>SHA256: 102ea58338445230760ab1226721892679dd907997804d047cf22b48ce8ab78f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.768MiB (7.097MB) – 339,077 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0181205d24255559b4c2a13fdb0c95<br>SHA1: 77c5ed2ef6799485a1ff6d1bd9aa3aef442555aa<br>SHA256: f1a904010b8cf3e5db4f0ddc1b0fed4c77f852aa52effac37a04697ddb879a37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.90MiB (16.67MB) – 241,625 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f8f77acea5ee52ad5d81c9f3883d7a<br>SHA1: d3a894c2e7503a5fe5168eef49e53379425930d2<br>SHA256: 80ee4bf63ff4562160eda9ba68902de89a9e28a828c048003fd188647039bf1f</pre></details></small> |
| | | Full Location | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,746,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48770c63478550e9d616b0e8f11eb35f<br>SHA1: d754e9f10a536891a6f76b212ce1527fccbb205a<br>SHA256: 3abef96589717a094c9384cc0d2e88d16dcc6c1771a5eb42954efe056fe2caf0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>452.5MiB (474.4MB) – 4,397,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d15359a3c2245bffe65895c5939244<br>SHA1: a5622976378fbaa83dd68ce8bf186161f41252b1<br>SHA256: 3c33680bdbdc577647e1e500060fa0db02dc2af50f79e20bb78a7ae7ca1b33bb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.362MiB (5.623MB) – 268,369 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4330c0bbff3419f12c7f73fddf1cf704<br>SHA1: b4df563510fe7f5fc4e1d278ea041c62c7bdca5b<br>SHA256: e91c6b0f644a92d45674456c276b13846b9893bbf0eb311dae698ed2f3d44d57</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.43MiB (23.52MB) – 340,836 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a2d9ae09529fd0059afa4956f1793e0<br>SHA1: fdd2b4377c51cd148c50a2369808306b7c9e9c10<br>SHA256: aa8f17dc70c0dab48cba63b84addf77a95f2d154825fa5a1cc5a78e9b68ebfd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.7MiB (183.1MB) – 3,022,797 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63a84f26611e75064d6ca0974428a919<br>SHA1: 8280052bb209735824b9571ba8e1d3219f239f41<br>SHA256: cb6a41dd6ecfae830dbf227d07287c122fd823f9a56e968851d364746039495e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.5MiB (307.8MB) – 2,844,839 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a06e5ce285e86fe3c964abd92c36fbf4<br>SHA1: d5da4217a5c723981f96fe1b85823103e5248e1b<br>SHA256: d40b02049ece0c3e7ec8afcbbbece0eda05c646fb3a3a4719bd5bbcc13b321b3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-02-17<br>IPv6: 2026-02-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.07MiB (12.66MB) – 604,234 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2092776425a55f20d9503e27c65a6d4<br>SHA1: e26bdc837752da309d6941fe95459610f26395c8<br>SHA256: 9e7ddd8a043438698396d5462269967d6a45327dcdd963d6206e20012144c4ff</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.97MiB (45.06MB) – 652,998 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1fcb89b73d057dded5758f56b80eee9e<br>SHA1: 1dc85c315f4391175ffd4bd9adeada0928af2478<br>SHA256: e9d1891f51373cb7caf65851665d2960655723f9cc6aa6cc180a97be80f51ef1</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-02-17<br>IPv6: 2026-02-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>129.3MiB (135.6MB) – 2,589,534 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f174f04d268beec4f2e9425f18ab58ff<br>SHA1: 1f20dfad43ef71051c7b68c435fefcea65ab9f39<br>SHA256: 6696f927b6153c1a237b97d39753119f642b86e5064862358d16d9fb8915ab4b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>137.7MiB (144.4MB) – 2,589,534 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2f98ab6fa8e784cbfb0c905a0c5bd28<br>SHA1: 913147993d8cdecee9bad7b9dc8b5dc3db780f34<br>SHA256: 9bebfb0de04e2a5ef924cf7d711635a00d00ff87c73cd0699bc0d7e2e2843485</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>128.9MiB (135.1MB) – 2,589,534 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f53e4780957865ef5622cbfcd466a10<br>SHA1: 5ef53f9b94959bb456174bc7ba19540a0a07e45e<br>SHA256: 4cc2e14fe3f71cd7cbca4adf58e7e1937f77963add658034577c52f6f65baa10</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>131.4MiB (137.8MB) – 2,589,534 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4aeae506d1f321819b99ca91f1b92c2a<br>SHA1: fe07c5afdcaf860c3b3b2a99b24870e25b76c8c0<br>SHA256: ab7904fcc3890248c99cc5d46b0e4351adaa1dc9d70c062e0cd7f9940b6685cb</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>160.0MiB (167.8MB) – 2,589,534 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44e70b5b96edc085308449e09905c132<br>SHA1: e311b159d9d78d9918ccaed094ff0985cab44428<br>SHA256: ffd05f29ebd24fe6f311170a12a199400faa69b6f0e4ebda1ccc29b43a169c67</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>127.8MiB (134.0MB) – 2,589,534 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee7fbc21d1f17a497bc9e09b03ae32f7<br>SHA1: 2281871429ebd7f535ae89221ff134b4a134bd7c<br>SHA256: 4fe796e12e0138d154803f9d6a661fbb75c507208d7c14c8d4f752ecf739a82f</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>156.7MiB (164.4MB) – 2,589,534 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77b9b5d968d6b64f88ff0b06e222c80d<br>SHA1: d4416b8f9d41b7d12544261a7aec7c6f798233d7<br>SHA256: b9d7115a49d1fc65d6937545c38a1121cbbcf2a19ab64911a8e38315336c939d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>131.5MiB (137.9MB) – 2,589,534 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05c95045d9f5b409b6b641ece818d5c2<br>SHA1: 51abb61c5b13224f725aa5881f4cbeaed03389a3<br>SHA256: 24092889076d69cefd061dd9507af47270f392119d6d5767cf725b6f112efa60</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.1MiB (196.1MB) – 1,971,498 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2560b86c8587a789a06df3ffa47a8f1<br>SHA1: f6acfc4408223df1a21ff5db0102a82cf9202364<br>SHA256: 82269e7f8864c91d60f0181c99fbd9b35de45da068e4bd6aa133a5999b15189a</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.2MiB (200.5MB) – 1,971,498 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ed4db4548c38e9a81919984e2b4b39d<br>SHA1: 6c4bd31f95e2cccea2c62760e2126a8fb004e857<br>SHA256: 0e393c5759b5a6c55931509dbf047b0e7b76403d840d94f390a79111c42ae401</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.8MiB (193.8MB) – 1,971,498 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb0d4ba0c2f5d64c295b4d4c67d6b3f5<br>SHA1: f0302cd99441f8c8e6108cdf320fc9e00cc2d862<br>SHA256: a4b910f68d119fe6283162df938a1b8ccda2c896151a872f57d7bb3ada199bd2</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.4MiB (194.4MB) – 1,971,498 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 225d4569ce3c6ddab4c9f748ccf88523<br>SHA1: cf171f5f2c62ebaad90ac3bc21b67fc9f83d4566<br>SHA256: 0bc6e9f60aa1ea519fa8cf938f6327cd9ccabe201fd4490406ad3aedf18da78e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.4MiB (215.4MB) – 1,971,498 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee77112152669bca8ef66d5d28d46c82<br>SHA1: 0b065bcd54358a70326a602e3e7771a1464417b8<br>SHA256: b12214232d8f718c7249f4b26521e6309d6d9e5bf337d8a791277a43439287a3</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.4MiB (193.3MB) – 1,971,498 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f58d86fb0a8a93790017375837d8576f<br>SHA1: 9f38f7911643a2d054d68952df7c3b4fa40f256e<br>SHA256: 9ea84b9754f2322e34d94538935b1aa047cffe1ef16c5d25cbdb9f6e32c0fbe4</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.2MiB (215.1MB) – 1,971,498 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72b9817a8912ac8a49ba6a08b1edbd20<br>SHA1: c9383d53342ed69c45947eae5f66c80044ba4b6e<br>SHA256: 1a7c466e6250005d77d0c1fd4f889214837b787ed3e7d38bbbc6fcdce437078b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>187.9MiB (197.0MB) – 1,971,498 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90fafc347185d65e8d54b05ec7c7779e<br>SHA1: 3394133f8d9091255190c5598e4b790657e70efe<br>SHA256: 7d936d8285c42a0249a1dd4cb90ce30bef9367367881db584969b92de1715ded</pre></details></small> |


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
