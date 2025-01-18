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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-01-18<br>IPv6: 2025-01-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.005MiB (6.297MB) – 300,657 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfad317721a85f1ed47b3700067f1645<br>SHA1: 765874b8930167e5cb992309775e098aeba58072<br>SHA256: c035ddb8242c11939bf19d8e84c198c37d28f66c21225daf8a2562831d4fc25f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.72MiB (12.29MB) – 178,054 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4a36ea520075dc64b7fe7da6e096d51<br>SHA1: cc3476c9f33162ac17d4df1e8fca21f242417206<br>SHA256: a56d1180286979b5db8cc5c76916fe41e4aa3fe52e0a66114075c749b89f7c05</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-01-18<br>IPv6: 2025-01-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.298MiB (8.701MB) – 415,551 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 37b1df5c9b0a45b93bb48a0881228498<br>SHA1: 68f5c9a9d04c39baf733b370b39cef905c803589<br>SHA256: caebd6270417ae988fbb3a2237c542a2d27db57091f5fe0536ffb26c845c1b1e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.992MiB (7.331MB) – 106,364 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96dd915b5a4cc19570edc8722a6c1ffb<br>SHA1: 919855281cfea362dbecb203386b9d4cbeb5b60f<br>SHA256: c89d7b72a6b3fb35d8f9bf6d1cce2738a6c482209a0824bc378e1de6fb315949</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-01-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.49MiB (13.10MB) – 625,547 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31dd9f8613dca0b96bfb47ea387e8491<br>SHA1: 251b4c62fae729ded2a279a2e8a3e6473f312c5d<br>SHA256: e3e39218cc62b998f42af189924a0678b61bdd6d01152e3e3e66833209959394</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>77.80MiB (81.58MB) – 1,182,255 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2aa1b4bc3452a2bedf5a1b9b09a7845f<br>SHA1: 07adc226acd13c3b6d639187e8eeb50bf5b76f69<br>SHA256: a82fc857a505a4622a3b1ca661138d87012f42a594d514fad0e5850182125b5e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.285MB) – 348,457 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83bc658c1ea05ee0c1dd67b508e416c8<br>SHA1: 70aa579150d7be548067432da89e0057b10e615d<br>SHA256: 636b0495d96e6e73c2fd6a2d599b3713d050acf8c2bc75556af8ad5d0fb3f95d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.36MiB (16.10MB) – 233,400 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea165adc6016bf7241db413dadd9d616<br>SHA1: c2e689ee2f5aa199cdf34e7bb0a4facf213548c1<br>SHA256: 40a1cbecef33f526b989ce930aa6fc2a0952064828188fe18df5b777d10b8d72</pre></details></small> |
| | | Full Location | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>187.6MiB (196.7MB) – 3,275,051 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ca665aabf2aee0b7c39b4545a5f75e<br>SHA1: 027d0a8a8014da5f6fc12e62c926c6933687bbf0<br>SHA256: 249e041ad20b36d2aebf8acd5c4d86a5f88957c86f3a7137f906df3200c6f623</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>347.2MiB (364.1MB) – 3,369,294 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb9eca947a082a3f2644b8c6907a6194<br>SHA1: 6d3040b4badad6d8c3e74a1fc773d997d8a618af<br>SHA256: 4d20b8e6b46f24b32ed9d99c2e5316f3c7e940a92aafbfdc42bea1eb6751282e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-01-18<br>IPv6: 2025-01-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.096MiB (5.343MB) – 255,041 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 385e7d39a49da4f7b26b8ca022e788dd<br>SHA1: 7bfbc318f06616719765ecf95f9c600ee41826cd<br>SHA256: bc2cb4bb17afe8e3962b87a8deb428f68ff7083def1f45c295c77d61751a71c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.13MiB (19.01MB) – 275,512 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3010eb9cc5eb5d69c08e40e6ada6b77<br>SHA1: b14d2ac80fc5b7043024cae2173668671a286f87<br>SHA256: cbf1a41317aa32c82f0ad9508afdfa47f673246f62711d998001fdfe0a7f5b17</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-01-18<br>IPv6: 2025-01-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.4MiB (185.0MB) – 3,056,590 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a976173ff14b69a2f374b84348a7b747<br>SHA1: ffcd6b20ec9ef8f0b9dc4f4c901e9fbf0f87075d<br>SHA256: b58bb3a37215ab1b1889208c52164428b5c56380cff711b82b6e54e5febfc1e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>226.7MiB (237.7MB) – 2,193,791 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fbc49d9a6e454cea9f8835d6e2277f3<br>SHA1: 9bfe0073a0141bc90622c08c9161a7283d562072<br>SHA256: 451e6a13f9d9293ed3e076c9bca96a945e2b1e2fd52e8171481f1a31a9e2be46</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-01-17<br>IPv6: 2025-01-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.16MiB (10.66MB) – 509,065 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0520edc5cda685f4682af506dfbfcd22<br>SHA1: 7c7dd31cbce66d12f53f40d2e5328bf51a934bba<br>SHA256: b4c94a64dd59a79c898cceecea17cd46544e2aac8c8f2949ba7ff68d5e3b9ab4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.44MiB (32.96MB) – 477,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc55426c53bd20663767c007ec94569c<br>SHA1: 9a14a5ddd848592cba20c85c932e4f94e060e747<br>SHA256: a6e843cd7f8424fd89d4030e33869e2c2eb2cef12026f0c622acde66d308872c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-01-17<br>IPv6: 2025-01-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.4MiB (173.5MB) – 3,272,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99904181c92a53c66f5c454f2e4c2c7e<br>SHA1: c9b38055fdbc1d11ecf951b1a33d2c03dc998ab6<br>SHA256: 3aabe858d74c69848c9e527b698954bebe896184597225c822ec3a9656ca0efe</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>176.2MiB (184.7MB) – 3,272,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dd5a6284da70bf59409a389041752dc<br>SHA1: 05618553d6282e7bc522872ff90baa2819ac1951<br>SHA256: ab61fcb269da7db24dd47c53483296e375a437353d3c14984323bfd3c652ce0f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.4MiB (172.4MB) – 3,272,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24a6e7970307ae82c941918d66322ffb<br>SHA1: bf5a9dfb90715f10ed685e7bd393084df4c3b66a<br>SHA256: c307e175d7bbab524dea08979e87936bca01c4cc58c4086902a6a8f27460d0c0</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.8MiB (174.9MB) – 3,272,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f48cafb96c9df3fdfd3144cea5c39e92<br>SHA1: d0e578164f3b8a17d23d02d17da7d999f8d6f370<br>SHA256: 6b5ae13e9f171da8dee57c39f352593f9a0915b54d598c64876b0d9da82974c0</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.8MiB (220.0MB) – 3,272,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4755167754e2f27f21d8974e50dfcda<br>SHA1: 41207d55b203e21adf005f2f2b75480a9bc50471<br>SHA256: 11750d74be009309cae1fa85cd5b08b488bdaa796513507846c531ef8fb70067</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.4MiB (172.4MB) – 3,272,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97fcd43e4cd72603c3a72a94c43ddafd<br>SHA1: c577442525dc300e3c68bbfaacf06bf358a8136d<br>SHA256: 649304b636a9b2fee1fa9e65d80e3f708a830381c759fabbd2d349d75fa74fe2</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.7MiB (213.6MB) – 3,272,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d83fa554901c4c911bb5b863533f470f<br>SHA1: 47060db2037640aa8c76806c546cec8c0562509e<br>SHA256: 33ec290a006828265b484bf4c18a7a611bd47a319a09b4a40bd36c45136ec4c3</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.5MiB (179.8MB) – 3,272,164 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecff0ce24cdd16b34a3a6a6842fd60ec<br>SHA1: b6edce5cb58115dc8e8205b9f4062d641d0dd420<br>SHA256: 4603d58b2a129a3d14731bbfa7c08d11b41337c1e19159463547feb6f3647901</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>162.4MiB (170.2MB) – 1,729,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23bacb862888a21bb15b9c7c9dbd656d<br>SHA1: ac2122a7ec077e37e1c203a2e821160bf191151f<br>SHA256: 6c9b549bc4479419d2ff4048eafbfd046d45e0752e0c2e8afed00b929f636841</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>165.9MiB (173.9MB) – 1,729,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae2fdb14db656f937d75231b66c24ad9<br>SHA1: be9bace7aa0313983d47ea78ba5186eede9c4cd0<br>SHA256: 067a1bdc29288560f6ff47e4dbb7ee2ab0c35a8b96120570a47ad2d3930635ac</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>160.5MiB (168.3MB) – 1,729,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ce63d83fe267fbce8c90318c4018cac<br>SHA1: 9b15dac1a6bded4b56749238e0c7bf96499b7489<br>SHA256: 1a0fdbf6100ecd2dd0224ac14654302a4cfcd550994e2b938435bbfce801a501</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>160.8MiB (168.7MB) – 1,729,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9860c96516e9754debff27d22065c44f<br>SHA1: 16dc410c963144aa08e4a2cc26a58351a3eb7c13<br>SHA256: 3c64f926dba7a7a4e47536720f75c9573164db071df038424db81c2d44bbc3a2</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>177.0MiB (185.6MB) – 1,729,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d65bca2c0b6374eb28216d73e2d71e4a<br>SHA1: 7e5a5c20dd7c56d5ddd2f81c6a1d75835c477022<br>SHA256: 6167b910eb6a6fd3ca28cafc0ce7189e72b17003148aec001d2b03fea3898cca</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>160.4MiB (168.2MB) – 1,729,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a8e23e9c92a6471bc24c681bd80217<br>SHA1: 7eb0116d9879e240ad6b04c8414fe93f3237270f<br>SHA256: fc8a25037058ef00ceef1fae246c926cba5e9903ced6ceccd2598b305a3e4811</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>178.3MiB (186.9MB) – 1,729,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2f52fa76ce668e33ada40f9698e42a9<br>SHA1: 26fb1b8a89fe2a834fc765d7f08d022b7472a870<br>SHA256: b2159feed6cced30a5f8956309e5742cf4599715f972a2733d2358435c9c0dea</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>164.1MiB (172.1MB) – 1,729,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aeaa214f9b4b4fc56861502481ee8b15<br>SHA1: 3d0cb507ec556a3b243949d433b6f1ce75acbb8f<br>SHA256: 36a55d5bd9d755906f89bd25ddb7911a781d2e75c570b2fabf2f3cf4221f7ccb</pre></details></small> |


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
