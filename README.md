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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-12-01<br>IPv6: 2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.890MiB (6.176MB) – 294,898 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b9add4b68265ee694aec0c572c42aae<br>SHA1: caf2dc12ef3064dbc851123f66e357fc4bfad322<br>SHA256: c70749ea710a422b8f1bd3ebd0570edda12481c88857201d606c6fb232389e5f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.47MiB (12.03MB) – 174,303 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab01cf3f8ee6485863e73007c1efccb8<br>SHA1: 2c1e6084b57f1bb3b4c3ed9917419c9263912aed<br>SHA256: d744a49e4459196ad991773fdf9111adc6b5ca020e8f48e7d49fe8e3f3c837d4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-12-01<br>IPv6: 2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.247MiB (8.647MB) – 412,978 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343bf70225f42d8ccc097b10b3210089<br>SHA1: 876e964d53efb755e72def88bbb66b9ff684dcd9<br>SHA256: c60cfec655e96e703973472764dbe4f8cd22c89f0f92f9b6ec3fd0f6493ab02b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.928MiB (7.264MB) – 105,396 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b1af02c25af5a9508a9d36a4e826a9<br>SHA1: c19b120e390c0695ec8aaed90ba6bab433ab495e<br>SHA256: 6cb2ef5e39053e815a061d116e4b6325d42558d3dce88dfb56dd479da7106d79</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.49MiB (18.34MB) – 874,945 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 307356ee6748a427d773d14973856717<br>SHA1: 3f4917ed78a32705eec209b183e0078ee9d30524<br>SHA256: 6dffe7345117cfbf2bb721420e1bd21aa9acd9d512bc972fce3bc81e900d0d1f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>76.03MiB (79.73MB) – 1,155,443 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 011ed9deac0e2573752116b765d01baa<br>SHA1: 63a8ea61fa8b61f1416744564ceed3e7af0772ae<br>SHA256: d6bbbd4d2dcd84984e96bf85e00f2eaf85ebcdb5637521a8536fb4f3296c72fa</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.156MiB (7.503MB) – 359,168 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4fa1848a017a51ce167e1b45ef180e0<br>SHA1: d025902fca69db441cbc83871eb99ffd4b92c75e<br>SHA256: f02df1b7ee71bf749e1e43de462a3f6c365d9ed6e72e1d5c6faa86f25acb568c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.24MiB (17.03MB) – 246,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fee62599a38c614b43a277a08de845d7<br>SHA1: f6f5eddc6f61250f0fef53e42d76288b85a9971b<br>SHA256: 258dacce2a418e7297db10bd484df83410a61ac130bc1a5820b6fb0c0c58cb70</pre></details></small> |
| | | Full Location | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.6MiB (199.9MB) – 3,333,541 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f97a8dfa3d2efa2169aa49e5067082d<br>SHA1: 69f6046d5bebaecbd09f512a07ad0279a8bad58f<br>SHA256: 193177f00477af08b776744f0aa5ea8ffe08fe54bbe785733206c3c6f5ea0b02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>381.5MiB (400.0MB) – 3,700,914 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60c57063e8597965c85a15738ce2271e<br>SHA1: e6cfa1c20dff9df4b9dedd101304ed4939827a3f<br>SHA256: f48cf620380d7f79c9d8d05702be678101a193a90ef351c28ff300bad2cb1942</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-12-01<br>IPv6: 2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.918MiB (5.157MB) – 246,132 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ef7e16cf2b6bbbd422ba2a934ef7df<br>SHA1: e1f77a047f5dba3e4ae075464e3761268e84b7fd<br>SHA256: 8dcac1f1779ff26fe9a26934fc72b4c423e9a2f1252d99e1436206cc2bf9f63c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.70MiB (19.61MB) – 284,192 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dce3866a2d21db59b0445d7ab2b5439f<br>SHA1: 62737a727dab8fc70aa7a79a6b203bedd659ee5b<br>SHA256: 2bc4972b559cd83a749cdf69acfcc9f7e1e9b63db44e48dc0e635dc639b29822</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-12-01<br>IPv6: 2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>167.6MiB (175.8MB) – 2,906,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1918be02cf5e40016993945dcdf9fe2<br>SHA1: 26d9a8404ce0b330647e6b9dec8e0dc1f37c9773<br>SHA256: beead4d706ffee13660a84a3a4fa8d161b26172c66d7d783002d7e5e9a446e97</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>223.8MiB (234.6MB) – 2,165,543 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58aa852f4471f22d59a91349fedddaa7<br>SHA1: 58ed488a65f8f18956e7b32e6e9c4c95283bd843<br>SHA256: eff43d3a7756d1032e8d1b53d8fc159639852e5511ede4f1a0b4456657557bb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-11-29<br>IPv6: 2024-11-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.04MiB (10.53MB) – 502,880 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ef7ae66c48061347284ea995d728fab<br>SHA1: 74b9c0bdffdd76136896db0e83e43b95edd3aabe<br>SHA256: b74a95b18754b4e2c1c0f8f0a73bfbf7d27e8f6848702bcfd77eb04b3290f09a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.39MiB (33.97MB) – 492,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b363465dbe4fd554913b44c275c246df<br>SHA1: 8b52eb0576d7e7adbab228d2d9876f8f8e545af0<br>SHA256: ab4ea95f292fb7bfc85272400d979a36d5f51e4926536fae6c395abc50c9e6a3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-11-29<br>IPv6: 2024-11-29 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>164.7MiB (172.7MB) – 3,253,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28dd789aaf71040724c11953adbfe76e<br>SHA1: 81d4b289f39056524cca5d0464dee10a4fb39f4b<br>SHA256: c8391aff52ae113eebf163136b8640254fc61da578f2d2bdf05225088dbc846b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>175.3MiB (183.8MB) – 3,253,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4aa5542d87dd4395f3c371da931f7dca<br>SHA1: 59bbf8414d608734401c91545b771bf9103b3c31<br>SHA256: 4485813d0264d0f4171348dfd10d56f4b79e9b4c7c807a27ddef45549eb017a2</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.6MiB (171.6MB) – 3,253,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0c7c5341717718561c032485f27f8ec<br>SHA1: 54735771bbc6fd860a2246952e40197062883f0c<br>SHA256: 04e0bfae8e6f37ea07b3d5a4fa4c6fdb377783985b764ad649d52810b776bb04</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.1MiB (174.1MB) – 3,253,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b29101c4f15fbaea664454e178d8cf1<br>SHA1: d3512e77b33889673b0d3c64e5d72b5824bcd125<br>SHA256: 982b6adfb3f8d0b227dbbe2ded48b45665947f2fde08d6c9d68f4aa64bad22c1</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>208.8MiB (218.9MB) – 3,253,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19818c1916cc8d0cf8aec4848481b976<br>SHA1: 5831ea36090ceacdae25d88c23e206f7d9cbafdd<br>SHA256: 8cd389c57120093364e11cdd127bf1f376aee1d8ee59920bdd3ea0ddcfdece97</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>163.7MiB (171.6MB) – 3,253,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9fc2e24880c85f1c17a7131c7d9034c8<br>SHA1: 9f7b3f592d584b3dad8b4322c22f8c06f8cf6bd1<br>SHA256: 8d543420b94d0b0caad3840593cbbc4b96fe54ca52bf35aff1defd78d319c443</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>202.9MiB (212.8MB) – 3,253,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 024cca2f046c0424a8d015645e39a968<br>SHA1: a3be15a3070454c6d398810c47e218f2ef5b6686<br>SHA256: a762f8a224800c3c118abb66c9f584df3b453fce2f2e80f78aa22c8f50b709d3</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.8MiB (179.1MB) – 3,253,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f83057bde7f826330cc56ee26892f8a<br>SHA1: 53b5fc2c67f77a2cb37cb6a6d469d559c595dd72<br>SHA256: b6ada731e679d61414ba9458c9162ee5c8ac3f9d6f20ff1c19265831c5933830</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>158.4MiB (166.1MB) – 1,691,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1bac223ceb895fb3ff2f001b912c3920<br>SHA1: 9c162532c23d3cbc58264cefce383933c6b49768<br>SHA256: f29d7b293128391758731c2f5f1c0322ef2a1531b97ad9dbd123325f6a81bbef</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>161.8MiB (169.7MB) – 1,691,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25ba05233fc4bcd1faae42efc89896fc<br>SHA1: 8396bf77c91a4888b15b0ccfa1f0240793bdfc42<br>SHA256: 5099e48d5ce680f1c988493fb3d0d396b4929ec3b9afa2fe4497a7a7af1b3598</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>156.7MiB (164.3MB) – 1,691,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78fe0ef1362a5fe8f603bd076ebd685b<br>SHA1: e2787584fb02b00c271703f5aa0d0610dc42f784<br>SHA256: e5d4ab855ff15930c6435213482e1ef538c345cabd5330e80f658cfc67dc6721</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>156.9MiB (164.5MB) – 1,691,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e99858ab5684528fa64187f0c7c681f6<br>SHA1: ec02ad1ca0d362a3f589d56e02ebc934e7d8ff17<br>SHA256: f344b6389bf52d363f6e729d6514d759fc6b4edb51e3eeb097ac9b91bca2fe78</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>172.1MiB (180.5MB) – 1,691,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a7b3c893533fe076421365972eca77f<br>SHA1: 7bd8ab1c286d22a829f9ca8d97e8e1fc73ca8786<br>SHA256: 7f6720cea643176dbbea319d9ba9a191021dde0a792187c266bf5d433978152f</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>156.5MiB (164.1MB) – 1,691,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b81bf4631edd300f312587856d41094c<br>SHA1: e77479fea66c15dc7e62f9f7eaa73e36447b60de<br>SHA256: 03c50025d8733256a584fc8e8bc6246dd191e1764e3aa7fbb24beee7e6026598</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>173.4MiB (181.8MB) – 1,691,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9d8329b8dc51e4313cf1a7d60403ede<br>SHA1: 594cf02bb547e297b35f995a5a64a1ba2d204ea8<br>SHA256: d3a3e69b036b182c462d873fa68c125a09425c9fde2b1346295fd1267506eb8d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>159.8MiB (167.6MB) – 1,691,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac9a2acf7ee643d28f09b5176e48b530<br>SHA1: 2b26eab482006dc73350f35243d7f3a8e7a302c8<br>SHA256: 851ba85bd663e9203a542bc080edc3afbfdbdf3cb9ce190180cb91b849acf1e6</pre></details></small> |


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
