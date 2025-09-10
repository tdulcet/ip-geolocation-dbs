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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-09-10<br>IPv6: 2025-09-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.219MiB (6.521MB) – 311,390 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32d9b4f6b4316ce229d7791d9edf931c<br>SHA1: 3a7938df53c208c8bf02fb0783a57cb1e887ff61<br>SHA256: 888f60fef2b546bfd4199dc051eae4ccc98509fdf6c0ebc4e82dcdc7b32b490e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.733MiB (7.060MB) – 102,324 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1bbd34e4f7013aff7e53026dcf83eee6<br>SHA1: c015c49be37559e7f589f57fed3272f1037f8972<br>SHA256: 9be4c2c4064177dc32b17dc36968dd1a4549eacd074bc2043d4a4678544c368c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-09-10<br>IPv6: 2025-09-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.622MiB (9.040MB) – 431,713 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78fd17cb4526bfea444948d3c2d723c7<br>SHA1: fb6b8a82067177dfe4fd456cc73b70f6c970a496<br>SHA256: 538bde1adfaa26904bae745a541f2c70930711861599fc80fd9281122425e37b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.229MiB (7.580MB) – 109,966 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43dfb1d9b7830bb287ff8ec4fdd6df9c<br>SHA1: deac836f1d685fa63db82db1b856909e84e225c8<br>SHA256: 4c54fa32cf2ae658452546730e339277141a269594c7dae0465bd7530920487b</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-09-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.09MiB (12.68MB) – 605,444 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e94ef570982f355968bbec10b327bb6<br>SHA1: b4ec3c5df30b4ba932482ca17641d14ae08194c1<br>SHA256: 3a8b367f5f5fce951a38789cffdafcc698b975f73474394576c45e355a84220c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>84.08MiB (88.17MB) – 1,277,769 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7af8a7afabe4328dc6a6ef6e1a7a1007<br>SHA1: 45d40eee5775879e9be4abf7ef8a63dfe22f776a<br>SHA256: 3f953912b73c88d8f1958de4807c901b5a153e499c5933dd3944a4619b177700</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.825MiB (7.157MB) – 341,824 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dae1f431e9d10a462dae84888365884<br>SHA1: c0cc78c9aa347b8d712850c57537fc0dc50f1dfd<br>SHA256: 3f57c286e145770c2ac0d5d3c14088a919db312a222bfef2cb85941399367b2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.93MB) – 245,375 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f7e3a8bff7f09ee7cfd621ef044564b<br>SHA1: feacd88a985ae6ef5d668ffcf375eefeed7948b4<br>SHA256: f554d05a841ea0162859a713eecebb3fb0dc814ea2d39b91150dd45627c31fed</pre></details></small> |
| | | Full Location | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (217.0MB) – 3,624,799 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7154efa553f5c77576cadbc5c42ec9c<br>SHA1: b63ba0a183e94bf6cd1aa8a15db942b52d55841e<br>SHA256: 00286d8f1fc1f8f801a25f123213615fc637aa494c49fb2537047bdab4b1aaed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>448.8MiB (470.6MB) – 4,362,462 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7375867bcf97ba785ec1fa3d092fb0ae<br>SHA1: 37a209470da0930c2308178d77c0c1cac376d849<br>SHA256: df10547da1aed72a27d58d5fbd860b66dc9bfc40df34c5dcca2b7da7fdf24ca0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-31<br>IPv6: 2025-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.161MiB (5.411MB) – 258,293 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95e8b98e399c9546eaa6913fe2309444<br>SHA1: 0729ec1700dd66e64d570295b605e265006a8972<br>SHA256: 7d5dd78fa0ac37316f479796659a319cb718b97cbcb6c276973e7a032a890aef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.45MiB (23.54MB) – 341,108 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ad0b9a6c005823c4054d4b7a7068006<br>SHA1: d04e0abccf0a13ec34ae27abfb08f929300b492f<br>SHA256: efdc13094674341ad2839eabd8b24cf19df12257e0c4a225196d48da8fbdf5e5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-31<br>IPv6: 2025-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.3MiB (177.5MB) – 2,934,344 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a60715c570305e0c75fe4faffb43ea0e<br>SHA1: 38b00b51abf99d675c6f578f3ddc6f1291989577<br>SHA256: 7b15658d15a2ea684f5136cc6b604a1305ba55f348332e98ac74007149eed726</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.0MiB (302.0MB) – 2,790,254 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ada012e83fb4d38f27d1fccd53c7b18<br>SHA1: da0592788b35abae1df0d9ced713b009ce8207e4<br>SHA256: 3a2da4e80c031ab64e77dcf65f18ecdb563e48d709a708d499e3751fd70be31e</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-09-09<br>IPv6: 2025-09-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.55MiB (13.16MB) – 628,081 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b55bada302077f78ef87cff8cec643c<br>SHA1: e817b3fef45660e8ddd11010b3b488ade7ce21fb<br>SHA256: 2205f44ad3ff8caf973c75729042ca091832aeb3450938ab70c2ec8ae678af07</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.97MiB (45.05MB) – 652,966 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a91295d51635c19f6bc4537b6d6b7e25<br>SHA1: 0547e0c65b1eacea147e48b32f072535791b47d9<br>SHA256: 11674db1f85c2409c1a1bf58f7b4c7f0a3c206cc75ffac784a982a154497063b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-09-09<br>IPv6: 2025-09-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>175.2MiB (183.7MB) – 3,451,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8b9db7037dc9a0cc6ce3fe229719666<br>SHA1: 5438d22f97c6c78006162dbca53535734f9dc494<br>SHA256: 4f88f21585cb6374490811732088775279f761328f0654e0e8e9d4a69b400d3b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>186.0MiB (195.1MB) – 3,451,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e09c606ce95f14c297f189786b17a33e<br>SHA1: 2199954d0330d0440840b31d2237a3678cbf0be6<br>SHA256: c83f89c5181967db02035dd0e0d1ac33a4b97a4bf633b3d28b648130b8636aec</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>174.2MiB (182.6MB) – 3,451,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b735c033af8f175947913ccfcf11100<br>SHA1: 72fbffa310cd181a95a2c4efe8ba6365713534f8<br>SHA256: 05f2937a12c0ab5363b9b3f510c7ec8a01ce57d6e781d5ff509fdb0e5bbd57de</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,451,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 230469da3413ecf34b61eca26a259dc8<br>SHA1: 4a77e1c78422865bf3db883814488ac02972d346<br>SHA256: 30c0799c2761c26045957296e93fb27e0d44a9746cb8ef04c640e00a584660ef</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>221.9MiB (232.6MB) – 3,451,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd2e17f7387275410d8ada575783b78e<br>SHA1: 0cfdb7ab3c1fb5ac996fe66bbbd0bd9c01fb7ccd<br>SHA256: 76953dcd2d2a6f19de767fe2dda0ba381cd51f40a6db27c546c54283bd97cbee</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>173.8MiB (182.3MB) – 3,451,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db7ffc439bda17084f7f2d8e35b63a68<br>SHA1: 47a804bdbc028b536d35dd8b854b83ed5928a4f1<br>SHA256: 8df3981ce018f47b322f2dd58275e5625105d29e1fe9d4efa2a3ee5f0dc66a3a</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>215.5MiB (225.9MB) – 3,451,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edd7a4fe0c16e9a5a8c50673be7d85a8<br>SHA1: 58173949587951ffcc89082b5802be3f883cb71c<br>SHA256: f3988d7f775839cc293a147d9e6a7c1e868b8d5a88aa900575e397ab79749531</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>181.2MiB (190.0MB) – 3,451,446 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fd100cd7c7d37be2d0b6f9637685a7b0<br>SHA1: a2cf6de783373833cc0dc35e6c1af1cc61fb01e2<br>SHA256: 606bb29572159e08ab97bf0315f1b4bad6210966450420dc8f5e210ce24f8452</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>177.2MiB (185.8MB) – 1,879,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a15b2744d4e3fb67c691a198342ba044<br>SHA1: 952af29b8852495cfbe04da0f18ff05957fa29b4<br>SHA256: 625c74a4357d9b8555eccd71ce49d09d9d585a623fc1a4f7a03c0111818da34c</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>181.4MiB (190.2MB) – 1,879,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23d302fa9d0d4069cbed2ee643ce4fc3<br>SHA1: 94368b52ad2810f195d54a5a362d7a749d9ffd63<br>SHA256: d5260ac13da3f8c4536266c08136530f3b3c803288dd44e1c3893c8fb78e3913</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>175.3MiB (183.8MB) – 1,879,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e13651a8586bda863f739811d73307d<br>SHA1: 7f8a476aa14e13409de01b04b8fdfde3ccfcdd06<br>SHA256: 099c7ab29f3a7cb3832fc4eb8582475878ba33b46dc105504d0e77d2c9ced3c6</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>175.6MiB (184.1MB) – 1,879,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8e9c40041d3d0715ebba46f8a6b1c67<br>SHA1: 6547bd07dc30e02055e8635a771677442971e0d5<br>SHA256: a51e68561d338105eea2459f1a7dd69173a3df5a34cdbe6eadb9b21ca300bac4</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>194.6MiB (204.1MB) – 1,879,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1b96f72a077361482460799c6c6f62a<br>SHA1: 1093212cf48e7c5e1ec31021a1e65b8882ab4655<br>SHA256: ff1b06f254cc0dbf4ebf7d9a966a36e2ceac13371da63edea8c682254f3a2968</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>175.1MiB (183.6MB) – 1,879,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c481cf85ae06d796298162e5094c1cd1<br>SHA1: e918a7f65fdfcbad09fd4a8586c0abf0f9ead553<br>SHA256: 08bd39dccf550945a3fde2a1d8ffa1d61391f0c84f625f61f75351bdd5c7f860</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>195.4MiB (204.9MB) – 1,879,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 423ddbcd49c5aa24c6e8e0ab191275b3<br>SHA1: 52b33d4210897b5f2adc075768221bea5186fd7f<br>SHA256: 38b0c70896c2c1c1eaef14556610fd6f2285ae82e29bac48caaaafbec089a179</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>179.2MiB (187.9MB) – 1,879,499 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab1df27501d42214a730105ff6db8805<br>SHA1: 7a074075d300e52fe357693a113ca07dc410d7a2<br>SHA256: ff77bddc6cc6e50e80141d975d11448bbc01d77a130b8ab1d05a2742df7dd506</pre></details></small> |


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
