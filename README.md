[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases are scheduled to change from CSV to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than one day (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-12-07<br>IPv6: 2023-12-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.606MiB (5.878MB) – 238,788 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 951e08c47761616fa097f392f5740278<br>SHA1: 6ec52edb110570bec1f311bbc4e3cfdc3c8f4c3a<br>SHA256: b9b811005823e2fd0b086c179b9f8061c3ffe33af2e5b637deb3f8b1b2d72cb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.357MiB (6.665MB) – 82,288 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d656a3b82c91423bd8d060f7d7ee93f<br>SHA1: 181fc9a72e83a979004b8a9c85405dceed113467<br>SHA256: e506d3f263eeaef7721aba3cdb43f57601ade905da199fb88b72c1d0f51b0057</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-12-07<br>IPv6: 2023-12-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.707MiB (10.18MB) – 412,283 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ad7fd2f5bccf7827b79f59b3af7abb4<br>SHA1: 164b7f1b9f35890ed33e1ce33b9030f8b906d695<br>SHA256: abb6ba81f2c9a22d78d2b612570a2db1836da7ce629f3ea629c4459ba9eb30a0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.058MiB (8.449MB) – 104,411 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e831bc691f496d8a60fd94a9b95ad2e<br>SHA1: 312ba3e301cb3cef8d4524eb83adfc7371c52e3d<br>SHA256: 75356416e65af1f1c76de2e90e77741ad2ee0b0cbbed8e8217d24ce354f6a482</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-12-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>19.41MiB (20.35MB) – 824,302 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91dfa91fc10f0132c0e313d1c0d2e7bd<br>SHA1: 9d9c7990ccd14723a6473a1d21fd728a62c53cc6<br>SHA256: 4d68162ab49f89f9da6c098b83a41ef823bca4f053b43ba667ec8bb0b874f1c2</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>59.05MiB (61.92MB) – 764,470 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1996d49f25f8ea35128ce94967a1d42d<br>SHA1: 37adb9ef6c3addb4b2b7f2b2269a1b36770178d9<br>SHA256: 0e53aea60be2f8d1eae4cb557769c00127a82b93196853c8383cc5e440720e96</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.227MiB (7.578MB) – 308,674 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7862828d186c4a916870bf5ee5c2dbf<br>SHA1: b2d61949f9d4cdf20a7bbe7858ca457da6437400<br>SHA256: cf718693f02d6570f872d99279b6729e48674fdf9a0ad17b2b5bd3a3004e7feb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.88MiB (26.09MB) – 322,049 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf9a945a8ed9ee1ba2168317dbed510<br>SHA1: 5488b48f6e283b58e14057f8bcc69c7a60073e80<br>SHA256: e724c992a57d034ab069e985589127206d0519f5cb5070ef4d8bc04d59937e7e</pre></details></small> |
| | | Full Location | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>188.3MiB (197.4MB) – 3,100,304 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e98adbd1d81ad4e7676a5bc97c6062eb<br>SHA1: 83a91e8b43cbdbea769542d684e8a2b61d6cbcb4<br>SHA256: 07faf7b0b69afe9bdfb83c30bf26ed6a6bc739fc4122230461107e862ca8202a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.3MiB (310.7MB) – 2,579,379 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b45c72d3f47f242ccb1124627ab028<br>SHA1: 46f55d20900ce13c49f5881ad197bc7a0d54d072<br>SHA256: cade24018cccb007f481018f12d82b3268ea4089c4223c710ce4213be2f799e1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-12-07<br>IPv6: 2023-12-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.454MiB (5.719MB) – 232,687 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7477aa0dc6695ad8d9200f94b8afd3c9<br>SHA1: 34d4e346c0da88e6d4f5988e17842c38d421b8b3<br>SHA256: 46a50da207a830584042870aa5b87c2dace68a946829e6fae37461d5b3427d52</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.74MiB (20.69MB) – 255,480 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efa7b87bcf99ba42fef37332f83b9e16<br>SHA1: dc9a17b5c1ee4e438d266c97c5aacd40da6bd740<br>SHA256: 24e3b2a9267c9b1de9614d05ec54385e3a732757a59c19eb3287899959cf7932</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-12-07<br>IPv6: 2023-12-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.2MiB (180.6MB) – 2,812,463 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4dbcfaaf8038ec905802f3bb4b98e60<br>SHA1: bb90c332e6a73443b2c214fd4c7c111fb053492c<br>SHA256: 1a5d0936e7c432fb29ae976e5de47f83fbae93c0e2d594781ab883143984266e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>176.6MiB (185.2MB) – 1,539,981 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa785991c752e8ca7a545029b778d706<br>SHA1: 641faab98a0a64a049fa166c4e4cee2698daa00d<br>SHA256: 7dec5cceb89309fb14723f22484df38d79bcc79adcd23394d5ce983d4a58e8f5</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-12-05<br>IPv6: 2023-12-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.69MiB (11.21MB) – 456,075 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7eb7b8fa2431ec48b2ac55a353ccc9a<br>SHA1: e8ba8de4eabc081909603cdcaedc71aa1dce5b1d<br>SHA256: d1133d75e354d52df348318b456135f5a35ff9981a47455377668f4530581918</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.54MiB (23.64MB) – 291,816 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6146153a6bf429b6a7399e5f914f4400<br>SHA1: 2e33cd49d691a65438fe9fe85b0ac94f76832269<br>SHA256: 05c013ff1d783555b7ba986a9e0151aa0aa92f094431ca45ac0f0a430308751a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-12-05<br>IPv6: 2023-12-05 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>172.7MiB (181.1MB) – 3,420,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d08e82c31b92c39e171cceb6a6f6daf<br>SHA1: 04c5b77966cb3e391d21951259f58b16f31646c4<br>SHA256: 8b2c6d54dcc4e9e58ffb006a2722a2907615552c6d7ebff965b7219a3b7fd0e0</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>200.8MiB (210.6MB) – 3,420,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3f4f24d84a573efdb2429b6e8fff45b<br>SHA1: 6d40eeb9b8e2f19c3b89e20b453242eb0ec3008f<br>SHA256: 67604d98a69e4b502b171bfee271a3f9aaa8f44dfabd85bc818e11312f4abd67</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>177.6MiB (186.2MB) – 3,420,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6e5dc17ba5a1449ff43ad580fa62717<br>SHA1: bacfb7df73ab8c22c87a952f089e3ee80b83ce40<br>SHA256: 776b488926e073b7e1bf842fb119b11ffb2ccb74aa01ebba2381da20ebf9fe49</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>184.1MiB (193.0MB) – 3,420,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48a203057d7baf2ad8f0e5243b8ad5e6<br>SHA1: f6f89d3b23a8fe511998a35892242d15c13ee2ad<br>SHA256: af6978070716d511aa0958c1264b3363dcb216311351e396df8bd93bcd651db8</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>212.6MiB (222.9MB) – 3,420,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ed8b1c6e65fbab8b09a379eb09298b7<br>SHA1: fff6fbaea83cc5b74eebbea552dabe0958b01f67<br>SHA256: 20dbf2ecb4fce48fb1c19744bf5132a6793b6595d9636fce323d3f2891a0ed82</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>172.7MiB (181.1MB) – 3,420,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 874a356f20edcea8f5d46c46a6f0c512<br>SHA1: 0add22a6c5884b8459a7a7b62a4181f8816ce30f<br>SHA256: 8459d4d87134ec5a2886a93d73c04a4f3498770ea7389a3e8ab225c27151cad3</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>214.0MiB (224.4MB) – 3,420,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7610c8cb69f7fc81f8093b497db53c85<br>SHA1: 3a99821b877280798a86c8bf4866ed43f2569430<br>SHA256: 739053b1d1ab993f4980d5aed4a759eb11b9a9c848f6d11de5fc659e684d29ce</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>181.0MiB (189.8MB) – 3,420,087 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb6b14420c624d0208d20904430f136e<br>SHA1: 4ddf8af754819ea95cd519d67d9fdc348dccdf52<br>SHA256: b16cda6376498f9a772964e04e55ba33d8f6086ed95d7088244bb43473c7f821</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>120.5MiB (126.3MB) – 1,196,133 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3f018925b714a3528c47877ef583ae4<br>SHA1: b2add9f115b4a22d920cd07182a3574ee38347b9<br>SHA256: 7fadeb5de08b484a4d5aa0856b7b72dd41dae253e9770e69cb28934683e7f926</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>128.2MiB (134.5MB) – 1,196,133 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4dd2014ef3de4472efe8c79bada97125<br>SHA1: a9a390c25a9c82f3ff3221ade922127897609f38<br>SHA256: da3cbb40a0d2cb750c56e0a55a34ca6ca5abb7aaef7fe408092b614f5d67b4f1</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>122.7MiB (128.7MB) – 1,196,133 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7462909939a8cb8fea502f4cf60f56ac<br>SHA1: 5fe4402877e03dfe89b3e6414f2977fcc997bbed<br>SHA256: 3a8a8e107b58f07f390ac21371069bb249ac0f1517d98475f99a25fa939412ed</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>123.7MiB (129.7MB) – 1,196,133 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c83f7e93a26ba898709f59df6170096<br>SHA1: 75c136bd67e5dcda1eec43e48e79b157b760aa62<br>SHA256: 702eab203ddbdfb2faebe1d39553a37583627ab4ced59a2b74a428ac474b6e84</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>131.4MiB (137.7MB) – 1,196,133 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1d7c1bf62242c26a8f519b07aa69316<br>SHA1: ebb6fdb56a846e9178348c09094bcd77d21a5fbf<br>SHA256: 296ba5b919495e8bf703b240cec9eea7c0169e8429458d58146eca875a9b488a</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>121.6MiB (127.5MB) – 1,196,133 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07e3fe0fb4948cec28c3ea6cb0e27720<br>SHA1: 41a3b8eefaf90f89a2d1d1d4381c6e1031986897<br>SHA256: 6dbcbf17e1f3c610b948534d14569e52d103e79ae445e11f3b1cade467c49da7</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>132.1MiB (138.5MB) – 1,196,133 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc934c194dde8d2f9d4166d4be00d51d<br>SHA1: 60da8410c6ebfbc29257506d1113d356bc335703<br>SHA256: 49dac769e1fa06afe5d1aa27b164a8da0b34fc67e5f35844735008bcaf899dcd</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>124.3MiB (130.3MB) – 1,196,133 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04ac9d1e6c11d66bcd3868e1dcfa414e<br>SHA1: a284fd9f9c079e0e43aca73a9a9b2932ca4db8db<br>SHA256: 25f08b3678ff2f6fef570915b9617aa7d190ca7ded95972fc8e27bb7e51baf05</pre></details></small> |


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
	* Store the IP addresses in hexadecimal format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
