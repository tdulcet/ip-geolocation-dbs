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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-09-08<br>IPv6: 2025-09-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.218MiB (6.520MB) – 311,365 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0c93c262a8b916a49a49dd384343c4d<br>SHA1: 612813104f2da415030ff8d1ae80068521bc8017<br>SHA256: 83e160c20be4b8ddc38a17bb10d03e4ab1f434917b2776713b58c9b602d24001</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.731MiB (7.058MB) – 102,296 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c740ac73f8168cea9606bd1bb2e4422f<br>SHA1: 3a1261ec53d0061d2b7bf3c769892951e63f34ac<br>SHA256: 88266bd67bd351c44465510fed4a8101b327b960bad98b03a6392d9632616ab2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-09-08<br>IPv6: 2025-09-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.618MiB (9.037MB) – 431,541 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01f1cc81652e9cb037352026ca0ca1fa<br>SHA1: 6c40b6f69e6983e220eee066a332c13f9d6002fc<br>SHA256: b64b48b89bdab2e84f0395bddde1d30477b3cc65a56a08b7847afa6365b4bdce</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.205MiB (7.555MB) – 109,609 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4894fef161e8a28b115e6a64b95f2b39<br>SHA1: f8ad1e72256f5325053fed7567827659b68dbdda<br>SHA256: 24b528e22e22628b331ed4a5eae92e25f507f36836da22923e08e16c17ceabe7</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-09-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.09MiB (12.68MB) – 605,405 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d93b547ff5e807d79e5ae723b788b72<br>SHA1: c923217b7e2d5cdbaf8a4ff2f206025cea53c560<br>SHA256: 2e35245044b2c1e47ffb733565d4143526526ae67485facb3dc143e31fa88de8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>84.05MiB (88.13MB) – 1,277,266 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1d87da45ff69fdec3912f80359d3ad3<br>SHA1: b0332b22706001becb683147b60d6fda80406e84<br>SHA256: ce14b7e9d82807c4cb8452cb969ca18ffa7d51dd1f558ad4b39670dc969eacd2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.825MiB (7.157MB) – 341,824 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dae1f431e9d10a462dae84888365884<br>SHA1: c0cc78c9aa347b8d712850c57537fc0dc50f1dfd<br>SHA256: 3f57c286e145770c2ac0d5d3c14088a919db312a222bfef2cb85941399367b2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.93MB) – 245,375 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f7e3a8bff7f09ee7cfd621ef044564b<br>SHA1: feacd88a985ae6ef5d668ffcf375eefeed7948b4<br>SHA256: f554d05a841ea0162859a713eecebb3fb0dc814ea2d39b91150dd45627c31fed</pre></details></small> |
| | | Full Location | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (217.0MB) – 3,624,799 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7154efa553f5c77576cadbc5c42ec9c<br>SHA1: b63ba0a183e94bf6cd1aa8a15db942b52d55841e<br>SHA256: 00286d8f1fc1f8f801a25f123213615fc637aa494c49fb2537047bdab4b1aaed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>448.8MiB (470.6MB) – 4,362,462 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7375867bcf97ba785ec1fa3d092fb0ae<br>SHA1: 37a209470da0930c2308178d77c0c1cac376d849<br>SHA256: df10547da1aed72a27d58d5fbd860b66dc9bfc40df34c5dcca2b7da7fdf24ca0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-31<br>IPv6: 2025-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.161MiB (5.411MB) – 258,293 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95e8b98e399c9546eaa6913fe2309444<br>SHA1: 0729ec1700dd66e64d570295b605e265006a8972<br>SHA256: 7d5dd78fa0ac37316f479796659a319cb718b97cbcb6c276973e7a032a890aef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.45MiB (23.54MB) – 341,108 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ad0b9a6c005823c4054d4b7a7068006<br>SHA1: d04e0abccf0a13ec34ae27abfb08f929300b492f<br>SHA256: efdc13094674341ad2839eabd8b24cf19df12257e0c4a225196d48da8fbdf5e5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-31<br>IPv6: 2025-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.3MiB (177.5MB) – 2,934,344 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a60715c570305e0c75fe4faffb43ea0e<br>SHA1: 38b00b51abf99d675c6f578f3ddc6f1291989577<br>SHA256: 7b15658d15a2ea684f5136cc6b604a1305ba55f348332e98ac74007149eed726</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.0MiB (302.0MB) – 2,790,254 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ada012e83fb4d38f27d1fccd53c7b18<br>SHA1: da0592788b35abae1df0d9ced713b009ce8207e4<br>SHA256: 3a2da4e80c031ab64e77dcf65f18ecdb563e48d709a708d499e3751fd70be31e</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-09-05<br>IPv6: 2025-09-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.53MiB (13.14MB) – 627,324 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: def4e139671475acfd8b638152537523<br>SHA1: 798139befd5a1cb826a599960bc0cc96f67e3a9d<br>SHA256: dd2ef27cf698c68b51bfe83a03e3bfcf8c3877ed4f1d25a55fbc40e87729b128</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.12MiB (45.21MB) – 655,263 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef47507457b7d368184fcdd6c5cdc26a<br>SHA1: 44d58cd713b1440b408772babe2a1efad5ca0858<br>SHA256: 57b7641577565dc835c8843e6efd2fff43adc8832a30085d2b94e92e46ebceb1</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-09-05<br>IPv6: 2025-09-05 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,435,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 992096c9251ad52285dff03c1b21f1ca<br>SHA1: ee4c2aae1cf5cc51093c123f339e729f39d476b4<br>SHA256: 106e6a621d626cb7d2989bd0948dadb3553ec2855a3c208eae1b01cb001699a0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.1MiB (194.0MB) – 3,435,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22bb0a6597c2bb1c593152ffccf8a34d<br>SHA1: ea679cdfd1e80cbbef99a9b60b8b45755687234e<br>SHA256: 6ed9d97e513cde23384849c33c303d30e1e3df21c343d20ccd3dc0bd60e27211</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>173.3MiB (181.8MB) – 3,435,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eebeb895a2641308da33ecac2ea441d0<br>SHA1: 57b7051ddd80cf699af6e06c01d6e2e802470706<br>SHA256: d7be890ad1554d3d6c7d5d4bce47cfae2805518815243a14ebc4cc3c98ce13ec</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>176.0MiB (184.5MB) – 3,435,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26c336d2922dba2aa07d263b32b903ba<br>SHA1: 66b9e848091247440b8754ee1370d2ffddf94da9<br>SHA256: 944c9fc4b12dcb6c1741aa1eee31888fe5b01bbe859a83d48c335d271ad1be82</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.7MiB (231.5MB) – 3,435,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a0c1391b75701337c1e67d8e73d5bd1<br>SHA1: 2fe3980903c79b40ce9451c60800c08f04cc2403<br>SHA256: 5f258d4036dbe82114d0985b5407b5b137b39b58e53442d83eed02f45df594e4</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>173.0MiB (181.4MB) – 3,435,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4da3ada42bcedcacd727798cb2b5a1e<br>SHA1: 066bb58c8f6190148cd3bd6e0f5092c7510ce4d1<br>SHA256: 66aded05af7c94cb4c566993e592c2833e70c0604c365ba3fbe8557b93db4dc8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>214.4MiB (224.8MB) – 3,435,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27a0a7a90cb9fd04146d599e07daebd8<br>SHA1: fd1dc1edb832e0b87d5e0a93dc818536227c736b<br>SHA256: d171df00f1b8d060edf42058da1c529db31551610e9efe6ad77ee8c93861a9e8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>180.3MiB (189.0MB) – 3,435,336 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 043af74beb245ef3f1cd0c587e6e64e6<br>SHA1: 71567d561117db547131d2e29295bc151d120d22<br>SHA256: 6140875c7e40d5d4f4bf2439b9baad3ac029e62502dbd54f588aec68c4449b28</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>173.2MiB (181.6MB) – 1,835,844 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3d7ab8d492a1c81d104e9a5f86ae206<br>SHA1: f66cf22a75e4a800cecbef6dc6e211fb10139cf4<br>SHA256: 52201182284197c69b9299d644dab69e2a38aebfaf277941b706bd18429718ef</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>176.8MiB (185.4MB) – 1,835,844 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7e47ab6a276590d5537a037c3894e56<br>SHA1: e9d7cfe30b1e9466b0a0d368e9b24d60d5882e7e<br>SHA256: d75900548246cc0974eb373e6a0583978f681ab7d872e1f0f6ff67861ef51491</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>171.3MiB (179.6MB) – 1,835,844 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea6bd1e50ced964dfd882087d52f52ba<br>SHA1: 12d16b15cfe1333bbd2db29e1ed3e011507beb4f<br>SHA256: 2050051c85943b8fc9b57086e9e3ba4d949db60d10c48953d336a4bfe04c5ac3</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>171.4MiB (179.8MB) – 1,835,844 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85aca661c83c685ca235296ffd32a85d<br>SHA1: be400b648a853df4860a8301e88b0328ac56e02c<br>SHA256: f6eb19cc3d59e7a0d64ee2fb75f86076fbc463bc561f8df217295e783679c537</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>189.9MiB (199.1MB) – 1,835,844 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 246bdd82a2e2d1ed40d6399e3a9c2d04<br>SHA1: 7e0c04a4cc4568c8631002867e43fb76c2ffe122<br>SHA256: 6e20a3add0392c75255cecf9312f94544b0b52d59532ed504f18bdbb4f455c06</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>171.1MiB (179.4MB) – 1,835,844 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa2da08337e149e8dd071bfc3060eb18<br>SHA1: 54a4600f0b675ce03a78bc3bbb9c9d50ac50a5df<br>SHA256: 3b81ebdafb5a5b2851ec5d71ef6bb9f2a7b86962e76218fd0f1fc89962e73f87</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>190.7MiB (199.9MB) – 1,835,844 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 417b0989e29ba032b6b9af703c6089ff<br>SHA1: 417ddb9f9ef2af77810fd580b18c0409c8cec0a5<br>SHA256: 534eec002f33ce20d9e5347ade93a154a71aaf88063b4e33d3bc056d610a3dc4</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>175.1MiB (183.6MB) – 1,835,844 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0dab6a48f99fec8faa5673fc02cfbfe<br>SHA1: 0bd562a829a154abc9859b2ca1deef07c7d58b08<br>SHA256: 39b825feb7a2e3625d8f97856e605399136fea0583490823339f1f49f918fd54</pre></details></small> |


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
