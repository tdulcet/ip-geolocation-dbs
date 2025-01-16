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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-01-16<br>IPv6: 2025-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.997MiB (6.288MB) – 300,262 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16969385b14decb73c72f7d347b84440<br>SHA1: 769a9fd717b2054d1d3c25ef4573f61cae1211fa<br>SHA256: bdb935f9bac761f0dab208e336a448b8296831e291e289b65a8575e10a4505f7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.76MiB (12.33MB) – 178,648 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 969233649da83e2c2b998d658fe1b68a<br>SHA1: 5db05524a2aa93841c42f32ae12f3993849d88d7<br>SHA256: 92621dd010fdab232f5c248f08d50b05a418a1acc45bf94ba8ad76fe319e747b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-01-16<br>IPv6: 2025-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.299MiB (8.702MB) – 415,570 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb57c67e76a52cbf3ff03dbfcc32d292<br>SHA1: 46dca3446e0ad088818f39961104a52cd05afb22<br>SHA256: 6b214ba6bc4ee0ba4d9cc5e1d7abb6704ab9c5916c3378f59caa6d50f92a2406</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.982MiB (7.321MB) – 106,218 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ff495cfa1672bd93af33348382e3d3e<br>SHA1: a839e633c5a2843a2e68a5d41195cff3ffd305a6<br>SHA256: 352a6c99e83ba978e75bfe0dd477e11ec6f7911a49a6ef58180fd1ecbed72653</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.49MiB (13.10MB) – 625,547 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31dd9f8613dca0b96bfb47ea387e8491<br>SHA1: 251b4c62fae729ded2a279a2e8a3e6473f312c5d<br>SHA256: e3e39218cc62b998f42af189924a0678b61bdd6d01152e3e3e66833209959394</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>77.80MiB (81.58MB) – 1,182,255 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2aa1b4bc3452a2bedf5a1b9b09a7845f<br>SHA1: 07adc226acd13c3b6d639187e8eeb50bf5b76f69<br>SHA256: a82fc857a505a4622a3b1ca661138d87012f42a594d514fad0e5850182125b5e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.285MB) – 348,457 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83bc658c1ea05ee0c1dd67b508e416c8<br>SHA1: 70aa579150d7be548067432da89e0057b10e615d<br>SHA256: 636b0495d96e6e73c2fd6a2d599b3713d050acf8c2bc75556af8ad5d0fb3f95d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.36MiB (16.10MB) – 233,400 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea165adc6016bf7241db413dadd9d616<br>SHA1: c2e689ee2f5aa199cdf34e7bb0a4facf213548c1<br>SHA256: 40a1cbecef33f526b989ce930aa6fc2a0952064828188fe18df5b777d10b8d72</pre></details></small> |
| | | Full Location | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>187.6MiB (196.7MB) – 3,275,051 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ca665aabf2aee0b7c39b4545a5f75e<br>SHA1: 027d0a8a8014da5f6fc12e62c926c6933687bbf0<br>SHA256: 249e041ad20b36d2aebf8acd5c4d86a5f88957c86f3a7137f906df3200c6f623</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>347.2MiB (364.1MB) – 3,369,294 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb9eca947a082a3f2644b8c6907a6194<br>SHA1: 6d3040b4badad6d8c3e74a1fc773d997d8a618af<br>SHA256: 4d20b8e6b46f24b32ed9d99c2e5316f3c7e940a92aafbfdc42bea1eb6751282e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-01-16<br>IPv6: 2025-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.096MiB (5.343MB) – 255,041 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 385e7d39a49da4f7b26b8ca022e788dd<br>SHA1: 7bfbc318f06616719765ecf95f9c600ee41826cd<br>SHA256: bc2cb4bb17afe8e3962b87a8deb428f68ff7083def1f45c295c77d61751a71c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.13MiB (19.01MB) – 275,512 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3010eb9cc5eb5d69c08e40e6ada6b77<br>SHA1: b14d2ac80fc5b7043024cae2173668671a286f87<br>SHA256: cbf1a41317aa32c82f0ad9508afdfa47f673246f62711d998001fdfe0a7f5b17</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-01-16<br>IPv6: 2025-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.4MiB (185.0MB) – 3,056,590 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a976173ff14b69a2f374b84348a7b747<br>SHA1: ffcd6b20ec9ef8f0b9dc4f4c901e9fbf0f87075d<br>SHA256: b58bb3a37215ab1b1889208c52164428b5c56380cff711b82b6e54e5febfc1e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>226.7MiB (237.7MB) – 2,193,791 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fbc49d9a6e454cea9f8835d6e2277f3<br>SHA1: 9bfe0073a0141bc90622c08c9161a7283d562072<br>SHA256: 451e6a13f9d9293ed3e076c9bca96a945e2b1e2fd52e8171481f1a31a9e2be46</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-01-14<br>IPv6: 2025-01-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.13MiB (10.63MB) – 507,555 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bf6778a074d6f5bf8202cdfba83c8e5<br>SHA1: 54bd9bb9fb8eb1dfc683c9880ccad8be6b80e16c<br>SHA256: d910731d2936985f96ebffefb2d6063e07cf3351321bca5ffead942ebb6e1fdf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.35MiB (32.87MB) – 476,425 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5ca9ef4d9e82f73829ffb2926bd3efd<br>SHA1: fe5a228e82728c7c10877cfdfb404851092855de<br>SHA256: 2f3d9a5653e9e43bfc67a7f3b1a8a8e673da864d4d9d56944989a0d5c16a22fc</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-01-14<br>IPv6: 2025-01-14 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.2MiB (173.3MB) – 3,268,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ff50a676191a42235fb2d08960d8f88<br>SHA1: bb409f599a6a656dfaa6c82bf1bcf52c41eda3e3<br>SHA256: ad9f62bd1020326e0fc8425c732165847d797be3700f7af95382b67673308045</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>176.0MiB (184.5MB) – 3,268,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 51e5324247c2346a8d2ba42e9ad72f6e<br>SHA1: 93a8e66a010e4a019338a3969c91043b66dd595d<br>SHA256: a0eebf02e21a83412c4ca46f08efdf633f6dbb9c711228a507d9da8de47eda9c</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.2MiB (172.2MB) – 3,268,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c89e67a4e169433dc17e97156c8c0363<br>SHA1: eb77ee06491d5b03ff718e6a6d70c166257860d4<br>SHA256: e7e64e9b8018d90023459ddc3bb5ce96245409b83c9ef7c804af76e3a2547b08</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.6MiB (174.7MB) – 3,268,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 104ca9d29a52d0a28f13e11ca0284228<br>SHA1: 32b966967cdcdd37cca2ec38a9deb7540e9045a9<br>SHA256: b9265d700481a5f4e7f3211ea6eb811b0670ad36ea9c2b1213fe27830134c788</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.5MiB (219.7MB) – 3,268,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c331e27dda67e469a94e6695da366500<br>SHA1: eeb32460f8766c984fc46265515307915dbba15b<br>SHA256: be5aa93779ef1b26344e675329a8c5578a8a334f10e16c7561424b20be4bf3fe</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.2MiB (172.2MB) – 3,268,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2d7105f66df479c5f920401439c9b01<br>SHA1: 13143396b9f6042a3569af04c67a467658040425<br>SHA256: 5074ce1dd09c3dc1042ac0b0c118f94291dba9ba173c357736b35187712ea29d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.5MiB (213.4MB) – 3,268,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a7a16d52efae07d7d934fed10ba3fe3<br>SHA1: c609d6885aa96bd21f89dd691223fbe62a70a1e3<br>SHA256: 929ca0f3ac2efa456edbf59807f3016267450feb4663c2b29f04a8ac19432198</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.3MiB (179.6MB) – 3,268,783 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6da2635ad0957d755fd6c4b1fe17d4bc<br>SHA1: aa5766a89ffb9750e67ec1eb8b107019d061b950<br>SHA256: 74e3d97a4b971ab01e129c6c7fd473962d60e1e722f5641971c86b38de153e03</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>162.3MiB (170.2MB) – 1,729,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f3cf1e51b1d9d8dfa3fdac35ab21975<br>SHA1: b7e70f6be1a6f12c6f65df1c59c9d425219f4203<br>SHA256: 205fbed0e5950ec078592dd9b7bf7ca5bd0d8d4308ba49645cecdbf53bcefd58</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>165.9MiB (173.9MB) – 1,729,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7be4a03ad6c0da8de5196098a961698<br>SHA1: 1ce732b89eb08563c92f0ad27ab4571f23a28991<br>SHA256: 94402b0887209a5cf890170933617dc23dda996951663ecf7e7f43fa75683096</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>160.5MiB (168.3MB) – 1,729,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23b5eabe28803be829eb16c987ef20c1<br>SHA1: 96b430b92efaadbda72321648cdb06c3ff97f090<br>SHA256: 751d7275a6ee37666c230c361eaa921745db066cbd416b6054477ce9d8cb9178</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>160.8MiB (168.6MB) – 1,729,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38170bc4c98ef297d542114f6ebc8266<br>SHA1: 3f2b78a848f52d17a945c2f6c0ac84051867e023<br>SHA256: 222aee1191fb8e392adda2e84ab458f4dd45e1dc9963003c985bc3f41ca49188</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>177.0MiB (185.6MB) – 1,729,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ee9939d76d73aa9b2e5db0e2a8e5c99<br>SHA1: 8d64c992717c7540cfe421f0e7311df432e88209<br>SHA256: 023a829ffb4be5bed712fb7859beaf511337a4cb610b4a6266e6a31f1cc77eac</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>160.4MiB (168.2MB) – 1,729,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89a0b4bad1798a4533fc7b2c243775f1<br>SHA1: bc163555f287f43340ab8f915671194afe34fb18<br>SHA256: af5236e27a793357adb997b1ee1603eba38db7d7fb291e8121f04452361a0020</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>178.2MiB (186.9MB) – 1,729,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99538f8b73d3d1a3b8a3537f73af1bb1<br>SHA1: ed885d5860ef617326f3be4f68c6c362be5e6c80<br>SHA256: 77e142af1d3bb0da78ac3b2941279f05ced04739a57113019ee96517ee279113</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>164.1MiB (172.1MB) – 1,729,688 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06c5aa6772009b5cdffb2f23d5515792<br>SHA1: 45c8b6060797b52aec12559440ed8fe831d2245d<br>SHA256: 5534442d8c08c8a91d86f6ede225212c0e4ec006d3b1a0af5dd1a83f54cc101d</pre></details></small> |


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
