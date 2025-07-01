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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-07-01<br>IPv6: 2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.225MiB (6.527MB) – 311,725 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3b9ad4f431782f883321b2462e7c540<br>SHA1: bed9520c28b099bc24bb842dbca7e5175b5e9a51<br>SHA256: 18163f705fe221766568eeeebe44a55f83718ce85a43b1bae6fec4be7dac42d5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.42MiB (13.02MB) – 188,759 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0a20e28f5635519905a2fe08f8cc048<br>SHA1: 5d884dab417938c198f3b68ef97f526420524bb2<br>SHA256: 0bac8d277b8ec8f48dc8b7e0492881855f028e15c95987031532ed685327290b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.28MiB (12.88MB) – 615,059 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e776f885c513e1d66b3cf7eb865ae83<br>SHA1: 1ec2ab46fff194f334de35c991eba3ac78850f8b<br>SHA256: da431bb91114642979827225ef0ef150a51cb34e2f3e430a74f69b1cd833a928</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>89.59MiB (93.94MB) – 1,361,508 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bc57464969862c5ea37ab1605325ac2<br>SHA1: 0a05d66ae4316d2583a552dade0368d25cd555ac<br>SHA256: 823ebba951bcb289d9f01b9d918a0d5d75b7316cfeac2126ec19ca79d9a18fd2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.936MiB (7.273MB) – 347,414 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c7d04c1b18093022e4d15fa13a3c793<br>SHA1: dff4668b90e9636e95d8d91ff5a0a5ef9d5a5138<br>SHA256: bb6417cdf168cf263192276c68d7f85bc709281ccbdd11c7d6ba1ea44867c631</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.19MiB (16.98MB) – 246,056 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07ba0d7228586a57128c0190c562a0b2<br>SHA1: eb3bd3cbe62f1d0f9297b597c839a74a4105bbb1<br>SHA256: b8a31ee890783e3b9d52b11a812428f9f2be236ecd040856f8782eed2451f3ac</pre></details></small> |
| | | Full Location | Monthly<br>2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,542,592 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec969a73671e8d644f7e1929154e221<br>SHA1: 57f8bee7c39ebea2c55845fddf09460d80963bff<br>SHA256: 523ca5cf6d43927bcdf8f0a9456d21d3d609e2054a0ab2c56a84b4c84e48b664</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>442.6MiB (464.1MB) – 4,301,032 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d63d081a66db1dd9fca73814d5662f<br>SHA1: 349e36d47acede517a0c291a40a9d636a8d85cc7<br>SHA256: 568f715ffd891dc642a79d89cb6270052c4d96e3cab597d73a50f1191484838e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-07-01<br>IPv6: 2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.057MiB (5.303MB) – 253,125 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95ffb525ccf7554fce3b883e3c3e03dc<br>SHA1: cfd2058bddb8335014ef0155af9287eb4eb032a5<br>SHA256: 7f2d0669907805f467ba557b3f8a89f0cc365fe47fd8d2d06b459ef043b58cac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.80MiB (22.86MB) – 331,362 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba9c525bb7d6b096e7d2a8892fad8109<br>SHA1: 51c5aa6639dc0b1ba9137e7681566659089d3e9d<br>SHA256: 055c98ab2c55b531af78c6adefcb75267c71f317deda1d0e11cd3a5379f8eb41</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-07-01<br>IPv6: 2025-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>166.1MiB (174.2MB) – 2,881,364 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 857f03de59f847ebc914de35a0261594<br>SHA1: a8eb10b3a834af6faabde77d1402f59045791a92<br>SHA256: 4de98758f7a7f36de44db1501aae76db758f5a29bc7d70a9c2dad3a025af32df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>269.8MiB (282.9MB) – 2,614,886 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0cf5e97154e6ed02edf8b16bd1ea2891<br>SHA1: c33d58815af98fa41a92decd4ae34875ecc10ccb<br>SHA256: 89eb5c59f64873edf5e3369de45be94f934ea8219710777955f08a65ad9b49fa</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-06-27<br>IPv6: 2025-06-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.41MiB (13.02MB) – 621,439 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4bebf2387fe02e352ee45cddaceb2b54<br>SHA1: 0c9a596ca50ec8ed6b666b2c448be9ac5b380098<br>SHA256: c6f1f13f82e6ab3f277eb6600b28f43b667475b171eb4b359afdd750d6bc580c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.96MiB (45.04MB) – 652,832 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 001ab7e5cac3d57823c51e85a8fe4a81<br>SHA1: d15dc09fcc40dbb5f008543f064d635d20a1e513<br>SHA256: 3a8f4058b16eb5a55cbf13371f5da43914d0fd938b222578fea536c858af986d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-06-27<br>IPv6: 2025-06-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>173.4MiB (181.8MB) – 3,421,356 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbf1c340d368f5766783447685930ba0<br>SHA1: 25877a4f927c5f43a1d18c3d4ad38eefbdb99d9e<br>SHA256: aad7a27f3220e6b7113040bdb197a12f3315913794d2b9939117a704ff7e0395</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.3MiB (193.2MB) – 3,421,356 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72e0b9e0fcbbcc2fe416d2cd1e5345f0<br>SHA1: 6d9351a81015089e32cfe19a0b4e1db6b93e7ae3<br>SHA256: 865cc471d65cb7dbe73ab727c110bf518b62cca48c241372b2529ab74e9158a5</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.6MiB (181.0MB) – 3,421,356 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4422b1f5e87beb4e24af24990e17eaca<br>SHA1: 8b7da9db56cb0703f9716b4a95aab2c46e80f301<br>SHA256: ae2db244b4a6ab4be57db8793a45e3be9f85f706aef51b4f42310334aad76d83</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.1MiB (183.6MB) – 3,421,356 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 783f90276746128274871c14705a8f40<br>SHA1: 4e81ff2ea402f0f2454899d88ba45bfd815c9122<br>SHA256: 8609948ea2eb624542dfc9b9c8f748e57a1e8f8ce28b64a1968ab41750a8e43a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.6MiB (230.3MB) – 3,421,356 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc094ac820088e9ab41776c1b28901b6<br>SHA1: b6ef4127297945a421c06fb81afa420497ee9ee3<br>SHA256: d031d902f38c4df2968dd74548882a501d85ef294adc28726a410024cd42306b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.1MiB (180.5MB) – 3,421,356 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7475f47d8626a67354920fdf5916fe79<br>SHA1: ad3a0295157529fd367fc75516a2f5c8587bb71e<br>SHA256: d5f2c6bfed46ad2bba61e33b0bace10a45cb2dc9998efdd20f34e9a8cb4aa9e3</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>213.4MiB (223.7MB) – 3,421,356 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 513da8bead5b305049729de84f448b5d<br>SHA1: 26f57ecd83e0e7d98b793c0919fd93a84df8d9d9<br>SHA256: 3311712a51a2ad37dbb861a6cab3cd0108fbfc9eb8bba7fe2d9b2b7974bec010</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>179.4MiB (188.1MB) – 3,421,356 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9bd3d7c057507d35803435c11011c483<br>SHA1: c6331db13767ad0ef62ae8e7d1e84327228a4c17<br>SHA256: ee526944e6e4aaf19fa2392319901171612751abfcd65b7a79a7a96c77256f0e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>180.5MiB (189.2MB) – 1,916,827 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 915b6b6ba6bb2d32cde6f3ca8718034a<br>SHA1: caedf4094f47192419bb8d1a4799107b7d34c04d<br>SHA256: 4a3d9d44a67aeca229319c21423cc8b84cd6054ce7cf062978ef29d2c0232429</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>184.6MiB (193.5MB) – 1,916,827 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbd2c7fa8cfc4728dbf7ba7da60b3012<br>SHA1: 1d12d6eac38416cf05c407d3c38c7409e05d55fd<br>SHA256: d6c81d369c146aec0fb647813ad67be80220993c73a688913274725f79653d69</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>178.6MiB (187.3MB) – 1,916,827 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7347fe5ba3f8357123a42769d3b6a63<br>SHA1: 3d157dac98979cb36f02f058c0f4ddf44f7026c0<br>SHA256: 67f9ec2a7a68229f6c24305b22e6333aa19457e783f4cae84de971ab28722a02</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>178.9MiB (187.6MB) – 1,916,827 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 077533ed587ef34f0a339602ee5eb0f6<br>SHA1: 3dae635ea628d1c4413bf147e7880284dab6725d<br>SHA256: 8dab77698dc63f0a459a92c9cb7a2ef7a0acd5b0af60b339269d56d7da335fe4</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>198.0MiB (207.7MB) – 1,916,827 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70993c022ae0b8bc0c08bb5b850cce45<br>SHA1: 19b0e81b74e6c478a4f417dbece16b25da6527a2<br>SHA256: deb7e6e77360bb61ea99cf9169fe0511547a5842bfa78235e7bf98e23612f51b</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>178.4MiB (187.0MB) – 1,916,827 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee3daf530c80f37534f3deb3ca8a62b3<br>SHA1: a2f8752764d73e1afb8068f67dc7b440bc6d9f00<br>SHA256: d24886c51acc5895ab22c175bc2438d7b7fd23b8675a14844f8e57a9e35ff054</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>198.8MiB (208.4MB) – 1,916,827 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8612290bae575c327f6037ca104f179<br>SHA1: ac466ffb2eab5281c904fdc10dbcb1ac071c8e0d<br>SHA256: 84cd4521f1cd812785677c2eab078d60508b72548c1828c3c82b1f1f49d46714</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>182.5MiB (191.3MB) – 1,916,827 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b009969314dc476ed3bf98c7b739e9f7<br>SHA1: 60b9db3c516415ab77552e0f34818a9c7efe9f5d<br>SHA256: d4f838f193be808eeee77a95f0f34ef5b240bcea216a1b572750cd309ba2f63f</pre></details></small> |


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
