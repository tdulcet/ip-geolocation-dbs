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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-10-05<br>IPv6: 2025-10-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.310MiB (6.617MB) – 315,981 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d843780c77e97211bcfcd302aa54071a<br>SHA1: a17a3925f207e59d26b3885cc1fe9462e82e5135<br>SHA256: 754462b8556f2f403711e2cc5d95bc9cee573d4df6ae729cd86bd75d1f389b64</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.93MiB (11.46MB) – 166,057 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 134c0e15cd113dc3ebe8d38c1c593f70<br>SHA1: 1d004be12d74f477bfd94c964a85b314f42c469f<br>SHA256: 73e4d2bb1f0e01a22d8ab04507d7128904f4877eb477ad2aef15caf663875366</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-10-05<br>IPv6: 2025-10-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.667MiB (9.088MB) – 433,955 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36fae7d5e3ec9da75d1c30ba1cd5e9d5<br>SHA1: fbe05850e890f57a8177a596bf3615035b204a1b<br>SHA256: 463ca425e69b5bdffc0236b1bbd7f422d755bd8e920869b73f7506ef00928a40</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.351MiB (7.708MB) – 111,819 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26a15aa6f5c4a17c153ae7802666547e<br>SHA1: 2226c9c1cebc21a7a42b5dbe434c576e1d0abcf0<br>SHA256: 0a9316094cbc48f072f320faabaccf6056a2b767c9ea0f0705adad81f1435348</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-10-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.30MiB (12.90MB) – 615,793 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27a9c9da3df55c98197ffa1dd7ab19ee<br>SHA1: 7dade1f8f510c5c87f7fd9a688c9488904fa8a61<br>SHA256: 7899812f97ebaa76f49a73751a3dd67106e78a4d886a539982fabb246c70e75f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>83.77MiB (87.84MB) – 1,273,035 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c1619815e8d1c5ee10684cdc47bbf69<br>SHA1: aa8b3c02890c28f87832bf07cdefb5c16046aa5c<br>SHA256: 108ff5f4578804061ccdb801877621ca5d6db98b4440739294a426dc3002f217</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.915MiB (7.251MB) – 346,209 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e6d674990e0f107fbd088e17b77f819<br>SHA1: e21f5ede55e9a68287555b79c322fd01792544ff<br>SHA256: ee56d76f9c227d305e7f5b79e40e5d3a11d30d9b4b4a21b0a814bc5fc6ccab58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.87MiB (17.69MB) – 256,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf6418c75d48ec2ce4a2a1c5d27690ea<br>SHA1: 9b685f6a9fe8620ee6003242f3c5acf610337b72<br>SHA256: e1a598f6d63830a2bae69310a4cc6608adaede1395648f0431135c9239a1caec</pre></details></small> |
| | | Full Location | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.3MiB (220.5MB) – 3,682,011 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42145ba207725adfe20cd9225ad15164<br>SHA1: 1d40332c6092241cca96d8e93cd7fb5c58e051bd<br>SHA256: c60c91128d39be7572205c3f816d9173c65edc218778bf32f3d1094e958cfd2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>464.6MiB (487.1MB) – 4,514,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f22f776ceeb745f6db78a0eef703371<br>SHA1: 30ac2eb9a7fa4373473059683b5de9079a24fedb<br>SHA256: de1e8fbe3abd61a6d689615765352368449ce489b189853826fcfeeff7321137</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.161MiB (5.412MB) – 258,309 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f26d4302c7fd76db0d0260380f6bd166<br>SHA1: af4522cf5b0da7a4f55fdb43eafd9203505afe55<br>SHA256: ccd12d01d176de876028be848cfde48c9259fe6937a9d2b5860504143663fae5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.39MiB (23.48MB) – 340,241 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6eda0fd5aedd731b1e43a4c8d35f5168<br>SHA1: 6cc4cc30710f6cbe42343b9494b486362bce385e<br>SHA256: 7cebccd5d4724480dfa8ce7feb46df8346a377c9663e9c706a42f95c27d002e4</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.6MiB (178.9MB) – 2,958,155 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe165abca69867578e8e23a850e260e3<br>SHA1: 28aa8e4206a34c7c19baa2c8dad557e3e7e29980<br>SHA256: 395f8c3845977ec0aa9aeb6377d2342a1e06c37721d3b8e06ec2ffe85d3cc7e8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>294.2MiB (308.5MB) – 2,849,176 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84c795dd4c828d0cd8fd981934d68c7e<br>SHA1: 2745be7c734086c09f40f1d7190fb4ec6cb937f0<br>SHA256: 7db0021ec3c03e994dd396ac728595c5a9f0c6bc1180ba247056935d66e38a9b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-10-03<br>IPv6: 2025-10-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.74MiB (13.36MB) – 637,671 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c83a3383a2bbe2ab99fe63f53f82bdf8<br>SHA1: b41a2de061016a0d7c0aafbdafdbea4fb690bb89<br>SHA256: d567fc171ec4c3e9b7053caf7f6ec4d81c95851cd4494b91a67cf66853db3c72</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.29MiB (45.39MB) – 657,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04fbcbcfe4ebb022f0c182b534cde325<br>SHA1: 81575097f54edd643e3df84fbc601d29ab0c145e<br>SHA256: bf0a761d185b403d4895b13afce395e0fa408376ae4b2ae297e1cc6cce437adb</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-10-03<br>IPv6: 2025-10-03 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>175.8MiB (184.3MB) – 3,464,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68088e21930f2b4455d99605b97f47ae<br>SHA1: 23581bcda89375aecd24995168693e431d6d520c<br>SHA256: 9291d9b1c08a8e97f2ba3d4134bff91aee14f7a5b01c324aaab8f0d678ee385e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>186.8MiB (195.9MB) – 3,464,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df6b26402e0bb78ac27ead9f89a18db7<br>SHA1: 0ec8677be72072eb4ba48dcf905dbb528dbad0b3<br>SHA256: 8cab4643357e49276996e9fabeea6099e4c1e0d01ff4d5432cac4f14e973db00</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>174.8MiB (183.3MB) – 3,464,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34d1b4d3c0da9306e91f80299a502d09<br>SHA1: a5d234b99c046275c6577cd7975851317ab92eae<br>SHA256: 1273125ad86e5b9f20286de3e283f96b25a215e70354ddabb1735d018de4f18d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>177.6MiB (186.2MB) – 3,464,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a82ed3d903c058c0a6851381cdc75cba<br>SHA1: bdd2a63688365b8764177ff1236b00b1c4c42d23<br>SHA256: 11c24bc86ab069b799c319d9351b6dfa405f2810b702b09c308b1caae11bafd6</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>222.7MiB (233.5MB) – 3,464,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d7bf65e28817128182b938ba21e2345<br>SHA1: 41ed125ab47b37c7cf2fe9a220efd7e02ee33535<br>SHA256: 46a9826bf1595c779545c2e8555c346e58a893e6f898ae55f97d1aa020a44f53</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>174.5MiB (183.0MB) – 3,464,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87d22ea44b34e4914bf07754e45c16c5<br>SHA1: 1f004eaf9a61062289fac1fb1e7824761527a58a<br>SHA256: 25e3c7f1ce75e10d8a534c2a49092764ea33da3d06cefb073d7d2333b4af3ce0</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>216.4MiB (226.9MB) – 3,464,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82b5550b4740f6227759c05a55db603e<br>SHA1: 490eacf1d1669d3c9c7fc26fc44a1881431fcd32<br>SHA256: c61024a38d5552550150c5c57f63507b756bfe45885d2cb41d5d34a27b19888e</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>181.8MiB (190.6MB) – 3,464,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c05bea70b4a536e706fe88d82ffcefe<br>SHA1: 10990ef06715fd4bf45ee545edab566430163b8e<br>SHA256: a76ad3821f2b9befba12faede499ad1de330a35fa6a2adeaaff91d46298a86fd</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>175.3MiB (183.8MB) – 1,860,566 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14adfb40df95fe766e50a6831d022141<br>SHA1: 82671229c711ca8752ea182d7e5c3a36a98ae03c<br>SHA256: 77690b3183bc66d5610c34c4eb956f9c6ad666824082f2dd76b69f92dd258acd</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>179.2MiB (187.9MB) – 1,860,566 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81407f722930bd0835b6e12eb104f072<br>SHA1: 5460599eadd5c7c18087b93bf646750fb7f7b054<br>SHA256: 012632f4e313c5d0b53295dd8484b62a731aa72146095b40d804e899d86407b9</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>173.3MiB (181.7MB) – 1,860,566 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 314322e42639ada5df92e903c5cb1c85<br>SHA1: 4d4609cf5a96362936fce4caede08143f4c5d1b4<br>SHA256: 1614563b4b183397dd9ad6aee01c8eccef5644e5de9c927075fbef53210424bd</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.6MiB (182.0MB) – 1,860,566 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fa5db4090d3fca1fa271fc8b9cef213<br>SHA1: 2ab9dcd5dd44f456c317ee5cad8e1498ca920104<br>SHA256: d0b3c7808bc6ee3e798bc58afa98bbdb56da83c59cc84db51d44cd61591903eb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>192.2MiB (201.5MB) – 1,860,566 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b99fda18963406ec8ab4be5b8d41eeb3<br>SHA1: d2ab78d202b4a0d2ff42cb1e9c41618667470d07<br>SHA256: a6cc1c8d0a33c488002ec6777ec00a9dd5ecbb206118429ddeeb683e0b8481c5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>173.1MiB (181.5MB) – 1,860,566 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0b5e8250c256af8b2bf344ddb7ee282<br>SHA1: 8f3129f8920722cfd7d21fd05846619adb3bb305<br>SHA256: dbb08340a77a9e5ba72558cae3697a9de0189b072d2b72a7eef8323f262782f7</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>193.1MiB (202.5MB) – 1,860,566 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb270d6cccf3e00e19937f7c87b2e34e<br>SHA1: f369249f45ef243baf111467e39ddb8ae9293f84<br>SHA256: 858d37034f82b27bb8d7299d653a1fc3c427cec44f080eadbf31089a7ad78081</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>177.3MiB (185.9MB) – 1,860,566 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e90dcc95dd05e937dad3e1cc6bafc4d2<br>SHA1: 75a4473d0a16f9fbc274afef56b7ae3e9310ad00<br>SHA256: 85c4caa3b5e22df4cc91dff2357a66d7747ff8b2967eed036e105899da3b1927</pre></details></small> |


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
