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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-06-17<br>IPv6: 2025-06-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.195MiB (6.496MB) – 310,235 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50dcf7328d7a000426327918116dc696<br>SHA1: 11ac742f09997594816a46e2fcf3e13959739d57<br>SHA256: 43feb9976bc85c5dab71b6cad1d832c15cf29cd52e9e5d86593f1fe6a024b196</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.20MiB (12.79MB) – 185,356 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 075bea3416b4f7393750739d29446234<br>SHA1: c1f56906b75eb37d6b66154acdfda7cdf7dd89ea<br>SHA256: e5e65a04fdc7632f03db4b9600ee9c40e8ace37b595d61d441f0d30bc2e458d0</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-06-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.34MiB (12.94MB) – 617,853 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c92bb618e4891ec05512861b7ba3dad<br>SHA1: af947300ff5029069d51f3e957ff17d31b6ceaa4<br>SHA256: 4ad5dd2d860d09b22234014e837cbaf47abc95bb7803b1bdd414c33590f1cc86</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>64.36MiB (67.49MB) – 978,120 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ff6ef781f80190961e1256a0ced731a<br>SHA1: 529fb045eb709f200103b23c8a99929914584f1f<br>SHA256: de12e3d39cf7c111423c3cfb60b15bf585e378f733447d429d97cad07ca22272</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.020MiB (7.361MB) – 352,022 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5d6ce30939ecacab9e5fbbde143dd7a<br>SHA1: dbe45e91ef39b1de3ae5caecefe6dce72faff5e1<br>SHA256: 843f29bd3db6468809b0042da7a6b44aa5aa0f7b3378bce2344b427d7b8b2458</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.50MiB (17.30MB) – 250,746 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86b9bc39132e2d99653445ab24f13e89<br>SHA1: 04cafe97346c96dfaa2a0c192e271c1aa18bb99e<br>SHA256: d337bc1e4ec66010e25e0e0279f489bc7bb3f2218829c1b952e7b21620faf6b0</pre></details></small> |
| | | Full Location | Monthly<br>2025-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>189.6MiB (198.8MB) – 3,310,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1255823f4fa6d96cb2339938032ec17<br>SHA1: 7bcb7165d5248f918857090fad507b3b62aff99f<br>SHA256: f33143e90c472ffeaf3431c1f790ca9297c4fcb75c4f9b48690bbe6cb9d79c80</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>401.5MiB (421.0MB) – 3,898,653 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50981857bc3865133c307de9e8f457db<br>SHA1: 915f84f9ac8ac491a0dc82f8e1c8a8b51e82b9eb<br>SHA256: af893c4ae1cfc50fe6b043a92e1ececd960d30f00aa8a0067646fda960aa8ddc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-06-17<br>IPv6: 2025-06-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.060MiB (6.354MB) – 306,250 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66813478af08592fdfc48fd31bff150b<br>SHA1: 811a9109b04c7e248ec3039089a3534799a0b45e<br>SHA256: 7438026d984ce77dc6a3c83ea0623314e8e04ce52f031ecb819c2211c10dda60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.18MiB (22.21MB) – 321,882 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dc7e513e52e0755f6fdadbaacc17b5a<br>SHA1: c9ee76ff47638d91e8db56f68fe6b0d1ca2f6cef<br>SHA256: 35bfcec7d2598e67771e9d918023c4280f9109650acfb7bc6d7776c000fa7505</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-06-17<br>IPv6: 2025-06-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,073,788 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5842c1e89d9e6a7ace62a726c41126ac<br>SHA1: e3950375fff9f4e7a1b551e841a320f17e1763f3<br>SHA256: 136c0e48f44d563e0a01829656f7c14024757ccb342856959d0a6797ee9afb85</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>243.8MiB (255.7MB) – 2,366,384 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e93be5d64be521626b8e98eb9c04690<br>SHA1: 8491599042ab2c0661a6d9968a86b0de5322e2e2<br>SHA256: 699e1f5782b93d7acd864659595c72dc1e8bf20e3457b3d9fbe5503103a35841</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-06-16<br>IPv6: 2025-06-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.18MiB (12.77MB) – 609,788 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 296aecfef2ffa13ac69f291145f6986b<br>SHA1: f8a6643eeb2e73dd2a0536d32d18880cfe99672e<br>SHA256: 9f4c7f43248b281e35a5d21d90d3c437f09baaadea75e53c46e6044ffee6af73</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.57MiB (43.58MB) – 631,666 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9fb67be70747850af18ff1adda0a1aa<br>SHA1: e871858a5d642cd6a4a5729566eb44be78baf341<br>SHA256: 432398b19fb76ee8706ed53c9706136c83b9ad29aa7fb250baa014743be25ed3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-06-16<br>IPv6: 2025-06-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,410,756 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 187f96cb1e59d5c82b232ddd667d18ea<br>SHA1: 819ea6ae2d3cd865f21bd3032eaf5fe75a4a6e57<br>SHA256: 26d547511104f4f2ebf74ddb2044fb0bb6e871f52a84b6faa8d4991e3d7926d0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.8MiB (192.7MB) – 3,410,756 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d0a8bf82b05ec5be886ce16ed5e4b57<br>SHA1: aef5d8d31bbd5be108933552ce569f2a9d98f568<br>SHA256: 9e94ed27019cbb091ac72c98ab44f2516d42e1679b659ff3f959a5278bc6998f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>172.0MiB (180.4MB) – 3,410,756 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8885596d7bdf25c7401fe45cede67954<br>SHA1: f2745074cfc01bdc041f7963961bc9ec56173eca<br>SHA256: 7984df47dc6a4cca7b0d9057fb392c4f4f05d37f70052b0f28612841ba799b84</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>174.5MiB (183.0MB) – 3,410,756 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 444359ef36652690422d3e04a563c3af<br>SHA1: ae94b42a66050c0eb2c5ac7d6b4ca13717e310d7<br>SHA256: a011e522a1c287d59a5595fb6be9a03889d16491011081fb21094b59856db42e</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>219.0MiB (229.6MB) – 3,410,756 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94c565e013a5455cb58abd6577235eab<br>SHA1: c6ba65616f4d75e8f8e66d94fcb13287da41cb3f<br>SHA256: a5c713dc8ae1f7fbbd0c4c92d8258af58227488fb8061b2b12bcea33581017d5</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.6MiB (180.0MB) – 3,410,756 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 156c46e51ac88d107d4a80f24d18c6bc<br>SHA1: 453976d7835079c1182dbab9143eedd331ee57b9<br>SHA256: 3bad6b091b8dd9099423566e315c6c7741bb6d7570b3e22db5c1b34c20235dbe</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>212.7MiB (223.1MB) – 3,410,756 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e9b04d3944788f8fbbc123edf2c63ba<br>SHA1: 13379b710f9211f901a7c2a5bf348d58a853d326<br>SHA256: d107d1043f46e44f738c11c6d60cc4d2b5999bc3839384ef0291155ff6b0b677</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.9MiB (187.6MB) – 3,410,756 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7e820d789d9c0368986e3dbfa048593<br>SHA1: df30a20c105f127a0aa011be6ab15f32ad54a60c<br>SHA256: 5419feeffe752039d0b6754451ad221459a38a1e7b8031fa8757466e0733e99b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>177.5MiB (186.2MB) – 1,887,912 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d917418a159a03f0c0f084201b30d93b<br>SHA1: 5c4b7e5ce5fd16efd24619395001f426b9cbfe06<br>SHA256: d3c53e2dc0aaad1c8d4a10209d1477882e05ddab4ab133e52d925e2871228c4e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>181.7MiB (190.5MB) – 1,887,912 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42128004db66aa910dc549bb0e6543b5<br>SHA1: 479f286983a542d0ef9126d9e315ebe193ff5afe<br>SHA256: 22367cb7ed9a6a0d56ab8ec92ea8418f4648bbebc2f319d4455fdbf21a8175d6</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>175.9MiB (184.5MB) – 1,887,912 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1773b4742583ba5a56c9bf6ba538179c<br>SHA1: 23aed073be93cd7fc96c2e22f716fc5d83fcde82<br>SHA256: 69e3c654e616ccb8a5424f10d539a915f75f6edac27be34df299a727b977813c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>176.2MiB (184.8MB) – 1,887,912 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e9d9ab17cce4c3c2434577060cf7277<br>SHA1: a5e29dee58be4e0376a5ef2b7598dec2762f73bd<br>SHA256: 64a9458512fec951da367ea125fa04dc8455b22779286ad2f14e56970c5f6e05</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>194.9MiB (204.4MB) – 1,887,912 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef43112cefcfb4cd5e4a612f8328972a<br>SHA1: 247b5e66970bac9175fd285b6105af3782d15098<br>SHA256: 21d41b82d0b6e5230e0d1039311f662f9b194a7625602e0c23dad787f745c1f3</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>175.6MiB (184.1MB) – 1,887,912 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6a852034059c8b501a4ccefe3c12c9d<br>SHA1: a715ccc5dcc84370e3249317c4eb8059ff94b152<br>SHA256: d36f5dc51939b3dd7d6ce9f58c10dccfff717519d65028c76feb6e84e07aa73a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>195.4MiB (204.9MB) – 1,887,912 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92af5e59f691659b7de2f39133961d42<br>SHA1: 19e0c420d92fc791adeb180fefd342caf420e5bc<br>SHA256: 1459991c7f287f30f0d23802e4f4146599705567397e49e9abc5573af9aba81e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>179.5MiB (188.2MB) – 1,887,912 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 229126748c2aa0607672f31ad46ca087<br>SHA1: 0d4324ad5468144ac4f0c6b4daca16b06314410b<br>SHA256: 65d66f97df64c0be52f7cb59b06870771fa0a2e10ef3cd741d09caf7e4f98762</pre></details></small> |


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
