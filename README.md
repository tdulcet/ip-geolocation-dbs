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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-01-06<br>IPv6: 2025-01-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.966MiB (6.256MB) – 298,703 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da145d6c2803f98624c62dae71f2248e<br>SHA1: d7e2a6776331a565fa341e656344b9bb137f18cb<br>SHA256: 3b3b6a601bd8444a096c24fae6b579cafb201957f25c857ab9346f1858f57023</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.75MiB (12.32MB) – 178,526 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b454dbe2174f12abaddb30994c6b908c<br>SHA1: f25ee08dc17107129dd58ae7aa8dac8c264d460b<br>SHA256: 01a689b4c102c0eb8e51babee219bbdb0f696c87bea244b06d9eca9852cc32ec</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-01-06<br>IPv6: 2025-01-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.289MiB (8.692MB) – 415,103 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cad7a3909442d601d0181e05d184a824<br>SHA1: cc1522e0195ecc3c3123cccd25f1a686d08fd33b<br>SHA256: 55a515c0b8a6714fa3d6004eb97aa7921bc56b8f68537adbe639b55834e8f8ba</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.973MiB (7.312MB) – 106,087 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 686ae928839710f467fe6d159bb5cb72<br>SHA1: b8ca665f2080df8613f8d61680b349567c22e0fe<br>SHA256: 1990a792fba07a81cfbe564a35c10f14930108f04b0713b3b08b290d8ebca1c2</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-01-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.89MiB (14.57MB) – 695,419 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a4327f38fa40a692adcb6f71c27c27c<br>SHA1: ad04d511e8ae449999baaafd8cc523f0fa3a8c10<br>SHA256: d1dbff01bee8850fc2c3b746961ef3b9eb515c1c9317337faeb833f4a30dbd94</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>86.23MiB (90.42MB) – 1,310,486 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50552204037f474a03b9f9699e2a799a<br>SHA1: 48b3c29224e04472d317382220ee80c8e4af2ee8<br>SHA256: 014e93648d170fcbbc3f99c4b499bc02fedd2a0929d059ad450c5f631786b257</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.285MB) – 348,457 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83bc658c1ea05ee0c1dd67b508e416c8<br>SHA1: 70aa579150d7be548067432da89e0057b10e615d<br>SHA256: 636b0495d96e6e73c2fd6a2d599b3713d050acf8c2bc75556af8ad5d0fb3f95d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.36MiB (16.10MB) – 233,400 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea165adc6016bf7241db413dadd9d616<br>SHA1: c2e689ee2f5aa199cdf34e7bb0a4facf213548c1<br>SHA256: 40a1cbecef33f526b989ce930aa6fc2a0952064828188fe18df5b777d10b8d72</pre></details></small> |
| | | Full Location | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>187.6MiB (196.7MB) – 3,275,051 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ca665aabf2aee0b7c39b4545a5f75e<br>SHA1: 027d0a8a8014da5f6fc12e62c926c6933687bbf0<br>SHA256: 249e041ad20b36d2aebf8acd5c4d86a5f88957c86f3a7137f906df3200c6f623</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>347.2MiB (364.1MB) – 3,369,294 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb9eca947a082a3f2644b8c6907a6194<br>SHA1: 6d3040b4badad6d8c3e74a1fc773d997d8a618af<br>SHA256: 4d20b8e6b46f24b32ed9d99c2e5316f3c7e940a92aafbfdc42bea1eb6751282e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-01-06<br>IPv6: 2025-01-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.096MiB (5.343MB) – 255,041 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 385e7d39a49da4f7b26b8ca022e788dd<br>SHA1: 7bfbc318f06616719765ecf95f9c600ee41826cd<br>SHA256: bc2cb4bb17afe8e3962b87a8deb428f68ff7083def1f45c295c77d61751a71c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.13MiB (19.01MB) – 275,512 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3010eb9cc5eb5d69c08e40e6ada6b77<br>SHA1: b14d2ac80fc5b7043024cae2173668671a286f87<br>SHA256: cbf1a41317aa32c82f0ad9508afdfa47f673246f62711d998001fdfe0a7f5b17</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-01-06<br>IPv6: 2025-01-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.4MiB (185.0MB) – 3,056,590 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a976173ff14b69a2f374b84348a7b747<br>SHA1: ffcd6b20ec9ef8f0b9dc4f4c901e9fbf0f87075d<br>SHA256: b58bb3a37215ab1b1889208c52164428b5c56380cff711b82b6e54e5febfc1e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>226.7MiB (237.7MB) – 2,193,791 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fbc49d9a6e454cea9f8835d6e2277f3<br>SHA1: 9bfe0073a0141bc90622c08c9161a7283d562072<br>SHA256: 451e6a13f9d9293ed3e076c9bca96a945e2b1e2fd52e8171481f1a31a9e2be46</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-01-03<br>IPv6: 2025-01-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.12MiB (10.61MB) – 507,083 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb9a45b91617efc89dd055470aef35d4<br>SHA1: 4be5e3e9c859a13b8e74d3fb694ada03d755afb6<br>SHA256: 160d13e9c73eb554d389b982e39bd865a9711e7edc18524ddbca46b699d419c0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.28MiB (33.85MB) – 490,543 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf48fa43f758c69d6b8806c99215a93a<br>SHA1: 849805d327d662102e10e36d4b93c2690eed5232<br>SHA256: aa98c783062f632c882def689c449db86dfcd71767ed6ba2795981d311ce02aa</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-01-03<br>IPv6: 2025-01-03 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>157.7MiB (165.3MB) – 3,119,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67d38d18441a74deb823632b31a7a5c1<br>SHA1: 5461c713b2505e71988f7b4710ec305690e19232<br>SHA256: a64cfe4de63e72fee9e1beb4aa2e53387304830de2c66506e7e75d648088f7ee</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>167.5MiB (175.6MB) – 3,119,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92975004fd827256b3e18f319152827f<br>SHA1: 7a9b16747b10fb58c12e4d5689f380cf0b92727f<br>SHA256: 8a0515ae42d12c2acc96d6a89740ecebbde12bb1ba3a79154e8b9d294053006b</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>156.8MiB (164.4MB) – 3,119,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e706f018d2f5f5cc6531bec70941013<br>SHA1: b3b3d1725df8e9716133e4860f98a3e3d354a144<br>SHA256: ad6577328e77b3bf9da6e0a7f10ccfde92d09913abedf81acfb446e50eb6f470</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>158.9MiB (166.6MB) – 3,119,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a779874a99470e805bc899abeaee7a5d<br>SHA1: 99840e286bfce0bd34b5c1660852f07e2ef80d6e<br>SHA256: 475f7cdc773a8376626ee0ac1bcf072231c520dcdcc7ab6a8b059fb8c0b6832c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>199.9MiB (209.6MB) – 3,119,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44d90b300bacff7bc91ab3dbdea2954e<br>SHA1: 649410de46161b6d874b7393ed93e8bf6e59b668<br>SHA256: 1a35140e7a8a3c7d5726d90444060eadbf4bd944607ff7d5b149eea1cb8892e4</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>156.9MiB (164.5MB) – 3,119,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3503015937744330e7cf5db7675c89e5<br>SHA1: 0ea1c66d98fb3c09d901978ae32f78e06f4173f4<br>SHA256: 78425e7ade2fccff20df25a38bb98ac87507811903dfd4b938a70d22993aa9b1</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>194.2MiB (203.7MB) – 3,119,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19c986021049f088621eed47e1a8e867<br>SHA1: d7d9e936f1f2086590b48d843906bc95f563663a<br>SHA256: 601d97a9e5f7dd3db796eadb7b4475464bbc937ece88a1fb38bd06b0baf4b046</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>163.6MiB (171.5MB) – 3,119,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a48001bf10963768978e03803f8d25c<br>SHA1: 7bf4e20440bec76f0d30c1e60d60d2de80ad4f61<br>SHA256: 0adf70d53c71055649ff610eabcd30f5c5286375c7ce1a730f9219a0b340c7c6</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>153.0MiB (160.4MB) – 1,638,445 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96938f8f2265e5b0e8cd4a56de826b40<br>SHA1: ad2e3689810be8abff622dc112601fbc4e452256<br>SHA256: 1cc576090f188cc3218e621afa46ba8d8e42adc09f7e1f58ebc34419b2809113</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>156.2MiB (163.8MB) – 1,638,445 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6978a4ad14891d91347a07054b25d6a8<br>SHA1: 6ae249edc9806ded45370a21f5acf53addb64aef<br>SHA256: b49c769c3dbf999e22d346c7286e01e4f707939c85ce4c6f12cd6b6a080f2149</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>151.2MiB (158.5MB) – 1,638,445 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb9e506da0056e51b1bd11df70a178a2<br>SHA1: 3955424f0ce4450f7788d51ea608e897002e9c3d<br>SHA256: 72a9cc5bab3afa54b21b116154e3a8394161cfeb1716550c5363ed6c422bfbdc</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>151.4MiB (158.7MB) – 1,638,445 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca1711fa783af35d8afcb36745b0f0a7<br>SHA1: 8bbdd2c6cb7e5ef51c49bed68c74304b85fc59bc<br>SHA256: cc22abf10c95902fa5d27edd5d0cc6a2b9ca71f72137524a7ba765f03cba2181</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>165.7MiB (173.8MB) – 1,638,445 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4111a448cb41184445855b96986eee37<br>SHA1: 35cb6585dc19b6e22f6aa40668df4419969e0e06<br>SHA256: 6b28238602a913b238837787836c8b5b82d912985904553e60e221dd842b2219</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>151.1MiB (158.4MB) – 1,638,445 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23b05004ff76749ad17259a4bc135d22<br>SHA1: a9b85dce1ffd467e3a94fb0bd625d23805d7496a<br>SHA256: 603974488d5accdcd30c78f5862ae08a17a2a5c93d14dcfeea2055261cd220ce</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>167.5MiB (175.6MB) – 1,638,445 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3335d95b8ea0d1b42d9513a522d9126<br>SHA1: cea1c7e32c2c04793b447ddd60890b02a827ef59<br>SHA256: 27f5e63debf42cdc584d0cd3b418e351697930fb23b49d36275afe6cacf0c217</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>154.4MiB (161.9MB) – 1,638,445 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75eb889254b8e48ef3d766fa5c866a4a<br>SHA1: 51d24bc89ff1440d9aad2a51bfd5739d92f6e108<br>SHA256: baf86cc9810248ba7e58ed54bd5541dc2e31e9f3db94e67075a4e7c850da8206</pre></details></small> |


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
