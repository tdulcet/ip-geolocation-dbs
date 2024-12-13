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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-12-13<br>IPv6: 2024-12-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.905MiB (6.192MB) – 295,669 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1463553e7c4197b34237044b777e6f82<br>SHA1: afcfbc4b3a110089ae4cf18349372bb0dc2626a4<br>SHA256: b7f86abf216f366f4fcbc53f8ef114316c96ef0b476193b5d3ea169756c8109c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.53MiB (12.09MB) – 175,192 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8dc675cbb13a2a1856dce9b8d613ef54<br>SHA1: 6055c9507b33c5c6f40bc4e93d1c712b8b82e097<br>SHA256: da9df40bf9ff0fe10c3f5331e4f458aa4dd29d324f8ef055db22337faa8a0eaa</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-12-13<br>IPv6: 2024-12-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.266MiB (8.668MB) – 413,947 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f84ced2a75fa96be8c4639390ef6a9e7<br>SHA1: 2373637df65c0053b650be8e869fdf5639bef62d<br>SHA256: 758119d151a7072f56d0cabe2f93c8207f48534fcddcfe3e4e7ddb5fcb996367</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.937MiB (7.274MB) – 105,531 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 862cbac4d54e8e4ed098f8b95d7e6116<br>SHA1: 049e5826feabc60903dbed39a8f1c91912054937<br>SHA256: 3e3b46310e025a215467fddf13b096a7ddd82b867846bf5addb7f49b5c4ab16d</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-12-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>18.21MiB (19.10MB) – 911,194 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1187563870741c685daf052e135c53c<br>SHA1: ba8ba5ee86aa863162b2698a61c09df4a04fc9bf<br>SHA256: efac41c92e900d7bf423de0a36934f3ed0a314e1a60417d8b718dbc14f125af4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>81.77MiB (85.75MB) – 1,242,713 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9dbaba1b4f769ff9a213dfec9618254<br>SHA1: 5b0b0eaf1ef9ee791e2fde5dfe0a8b4427c88a77<br>SHA256: 2b0738c956b96d0e256592fe885703ee11c9c8afa7bd432371ebb89001a8e408</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.156MiB (7.503MB) – 359,168 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4fa1848a017a51ce167e1b45ef180e0<br>SHA1: d025902fca69db441cbc83871eb99ffd4b92c75e<br>SHA256: f02df1b7ee71bf749e1e43de462a3f6c365d9ed6e72e1d5c6faa86f25acb568c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.24MiB (17.03MB) – 246,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fee62599a38c614b43a277a08de845d7<br>SHA1: f6f5eddc6f61250f0fef53e42d76288b85a9971b<br>SHA256: 258dacce2a418e7297db10bd484df83410a61ac130bc1a5820b6fb0c0c58cb70</pre></details></small> |
| | | Full Location | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.6MiB (199.9MB) – 3,333,541 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f97a8dfa3d2efa2169aa49e5067082d<br>SHA1: 69f6046d5bebaecbd09f512a07ad0279a8bad58f<br>SHA256: 193177f00477af08b776744f0aa5ea8ffe08fe54bbe785733206c3c6f5ea0b02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>381.5MiB (400.0MB) – 3,700,914 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60c57063e8597965c85a15738ce2271e<br>SHA1: e6cfa1c20dff9df4b9dedd101304ed4939827a3f<br>SHA256: f48cf620380d7f79c9d8d05702be678101a193a90ef351c28ff300bad2cb1942</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-12-13<br>IPv6: 2024-12-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.918MiB (5.157MB) – 246,132 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ef7e16cf2b6bbbd422ba2a934ef7df<br>SHA1: e1f77a047f5dba3e4ae075464e3761268e84b7fd<br>SHA256: 8dcac1f1779ff26fe9a26934fc72b4c423e9a2f1252d99e1436206cc2bf9f63c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.70MiB (19.61MB) – 284,192 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dce3866a2d21db59b0445d7ab2b5439f<br>SHA1: 62737a727dab8fc70aa7a79a6b203bedd659ee5b<br>SHA256: 2bc4972b559cd83a749cdf69acfcc9f7e1e9b63db44e48dc0e635dc639b29822</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-12-13<br>IPv6: 2024-12-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>167.6MiB (175.8MB) – 2,906,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1918be02cf5e40016993945dcdf9fe2<br>SHA1: 26d9a8404ce0b330647e6b9dec8e0dc1f37c9773<br>SHA256: beead4d706ffee13660a84a3a4fa8d161b26172c66d7d783002d7e5e9a446e97</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>223.8MiB (234.6MB) – 2,165,543 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58aa852f4471f22d59a91349fedddaa7<br>SHA1: 58ed488a65f8f18956e7b32e6e9c4c95283bd843<br>SHA256: eff43d3a7756d1032e8d1b53d8fc159639852e5511ede4f1a0b4456657557bb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-12-10<br>IPv6: 2024-12-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.05MiB (10.53MB) – 503,247 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 896f571e7fa4c67b333007623b53ea82<br>SHA1: a1965222d20b12488c51c535f92676f379dbbec5<br>SHA256: 5eaf9351242b835edc41bd630f7f517d2a36a7aa7803eaf332944dcd1e10d190</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.55MiB (33.08MB) – 479,460 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e9bd277384f3ee29d1ba82efdec7531<br>SHA1: 28611bdec075c3247fa09576343c9e7afa7bce27<br>SHA256: 276605659f8b00f9c4e4642be8e3eb25957a8cf40637a3e873695551f03932df</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-12-10<br>IPv6: 2024-12-10 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.2MiB (173.2MB) – 3,263,158 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db0277ac344c10332b157b83605d254f<br>SHA1: a81f0f70789d7c8a9e773a755a92704bcf2b95e6<br>SHA256: 72642f3e33ed38867dac016e57a8d4e48a3b480ad59a001fbc77806cdcce243e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>175.9MiB (184.5MB) – 3,263,158 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54630a90a320752b6a62920ddf40e376<br>SHA1: 92eb4b88b73ff5648fd60ff08a9e3b7d82417332<br>SHA256: a9ce87949160e3fe1c7c03f3e7b810714cfa06d34c452d50a768a989c3ee98fa</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.2MiB (172.2MB) – 3,263,158 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8eff78f5b22f8c89ebf8d3e3c9b37962<br>SHA1: 022bbb1d88f5f7ad7467681bb3759fb7ebb52d09<br>SHA256: 886e2e6f6e92b2865f410c383f4881340ec4ae59e6ff170f9d57dc6ed9014256</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.6MiB (174.7MB) – 3,263,158 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 589db05c6015e090e6281b81a207ff3c<br>SHA1: a2bbe243aa319e264a6cc7e0e861ec6744c42c53<br>SHA256: a0232ead4b1997cd7ba81b96f8529cec9d84e4ba38642a7491ee7d3f57744f9c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.5MiB (219.7MB) – 3,263,158 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f4dff9157c3cc3bc51cc19a2d78330f<br>SHA1: 06dcab73d4bd0cf0413a7cf91d9f522e884bf0e2<br>SHA256: 01801bd3722ea980a6d2d0a91983306e5518065e1bb0b84d6da3c7085a5cfb61</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.2MiB (172.2MB) – 3,263,158 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4755ad10238a9b1dc0ada40177e87f1a<br>SHA1: 0e9a6b5aa9556f22fd96588141064f350b45c628<br>SHA256: 24b44b0d79751e81445f9974e3e8b7705fceca8817d8bb4da6b2bc33dcd4cfb2</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.5MiB (213.4MB) – 3,263,158 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1159c5485a58ab10d633ebcb9596f32f<br>SHA1: 5a84ae2e2538e9c372fab68ca34ea25f5bfc2bc0<br>SHA256: b6fad07c268796a0cfe34be1d4ae5ced397e3edf2663dc7984165d03ef3879d1</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.3MiB (179.6MB) – 3,263,158 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 861099206540430247d3642965c179a4<br>SHA1: 3434b16c353a2fa10e547f7a1b570c5b5360aa41<br>SHA256: 93d3345b9acfcfd5b4a35c18e9687e7d4f7eee359ff08324ee61d4e5baed4103</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>162.2MiB (170.1MB) – 1,730,187 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ba69ab95da865958eeb31fcd30021e5<br>SHA1: 36ca36a9a784af82362d18d110c03428537bd12e<br>SHA256: 12eae09e9dd1439e3600d67239d89569a8e94d1b2a23800893c252a56804e6df</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>165.8MiB (173.8MB) – 1,730,187 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19eba5ca4275451bffc7b34999be745c<br>SHA1: 5dad5ecca9cba6cf092370e8413e1cd3cc85b10e<br>SHA256: cfd6739d99434cbca5ca66e4a78513424dfdd8cd210ad89f8f706737e171524c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>160.4MiB (168.2MB) – 1,730,187 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a7fdd272e7498d5a1cbdb01fe54cf74<br>SHA1: 58cf88cbcd654d3a7f5d88c28969e6393f520316<br>SHA256: fd442ba19cd1d76ef063e8b9d8a81d5c24f3ec37bce1976f9b181de7625d9d9d</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>160.7MiB (168.5MB) – 1,730,187 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d7664ef61796cdfb094038703001d4e<br>SHA1: 72c86a8d44b58bb3393aa87d0932b06f59c7b3fb<br>SHA256: e6f7ff7c3460b6192be9c1585b70a15825767e39a4066aa378dc3089f3472681</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>176.5MiB (185.0MB) – 1,730,187 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2bfea0975150802d615274070b95957<br>SHA1: b35de2a0ecdca6beafd7a829389782d9ac136211<br>SHA256: 66e6d059bf525250fe949cc54916e0ec944474d7f6e35e40fa282325704ce7d3</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>160.2MiB (168.0MB) – 1,730,187 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 440dbe4ad67e41d51c18afe410eb7b56<br>SHA1: af27179b5e3d2b7b9d715cec3e41b7453bb8ab52<br>SHA256: 7c54816b12889f2da8e82bd245795f379c0e8afa7add24d20e16f9ebbef3ae86</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>177.7MiB (186.3MB) – 1,730,187 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6427f68cd3146f3f2926c69b3ec339b1<br>SHA1: d2290276400be325d160e02ed8241476e46aadee<br>SHA256: 6f32ccedfb669423cff28ade6c382360b76db2038aa0854e3d8cccda4c434186</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>163.7MiB (171.6MB) – 1,730,187 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6f313934a70080951dfddf705f67ad0<br>SHA1: 2371dd152f9e1fbd93c2481fb7933a3d3acd238a<br>SHA256: d04ff0ce657fc3590967ebd79dd14e69f46b16f6190eb2e48f11b4c0750f52fd</pre></details></small> |


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
