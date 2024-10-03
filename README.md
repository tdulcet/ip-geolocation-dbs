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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-10-03<br>IPv6: 2024-10-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.635MiB (5.909MB) – 282,142 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 763f9255eeae0848a29ae495ea6e4581<br>SHA1: 8530730ef87a560338b0985a480d961d1e3b02af<br>SHA256: 1a0cd488598623fef7fb2fb04641007637b05af44c9075a8cb6cbb06a0459af3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.97MiB (11.50MB) – 166,723 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 472eef5d6030e3a873ead3a3598a47f9<br>SHA1: d1ee6ad2b1a7c899257b6739a7b8b663388d0f52<br>SHA256: 76bf7d82390687e4de887f93707ad792cf8018a93cd2fe2821d1210bbcbb5b8f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-10-03<br>IPv6: 2024-10-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.177MiB (8.574MB) – 409,497 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45481500d4b08a619aa34d62b180ab5d<br>SHA1: 40af459724adb6e7fcc773259738eb285c7b9f57<br>SHA256: 69e57bbaacfc7158cec2285cd6a5ce0e9922d2245388b631cbe8ba224f164e0c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.909MiB (7.244MB) – 105,104 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f7670e3d70772fbe0925848bc91e74a<br>SHA1: 5ef123cb8df92a4978a7f85776c84aae9b52c9b5<br>SHA256: 704be6054d99d27ac402668819df92091092e1b7b3f5b8f1bda11d082551801d</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-10-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.79MiB (17.61MB) – 840,143 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d41764048c5739d420ee9c8337398c26<br>SHA1: ecceadfcf7900bf51d442231e61b519cae76e318<br>SHA256: 08998e1c85660fc26f29c4e8fd3d700e16e8a25678409dff33172d850cc44c8c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>65.33MiB (68.50MB) – 992,801 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8cb42e9e84957ea1360c9cd3d847c5c1<br>SHA1: ec9673140f2aeb66b26ab4f76f07612e39b20d0b<br>SHA256: e00c2a0ab83aece11e604da3594c74c254af0fc2bc0c28f568ec981ddf210375</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.939MiB (7.276MB) – 348,549 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1934c9e84da4a70171fa8a58df792d1<br>SHA1: a9efc628d84ddb0c5ec270a44c413d6e2e413eac<br>SHA256: 8974ef5ef8832adde54bf8eff5b734fbc419e040b6a1ba06eee6302c327937de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.54MiB (17.35MB) – 251,406 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccee8212e47dad6f6d37a7875599a267<br>SHA1: f12a6f633e3f93b21d90f94868a5dce0099a8f68<br>SHA256: fe5508fad3836313166aa43d498d12d6277cae16fef7835d5e92fdcd53bb2de4</pre></details></small> |
| | | Full Location | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.4MiB (197.5MB) – 3,289,697 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a0426270d27872fad498a291900b10d<br>SHA1: 4f4a7ccb4910df8d359d2ad76a1bd80c4be37d61<br>SHA256: 6869bc8bd2854724fd6be12e1a0efa4bf028d598fe1d116783216884c78d9f3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>362.7MiB (380.3MB) – 3,515,904 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b742d904c555f3e530341708e40522<br>SHA1: e367baa432e03a59b81c286e5f9bfaeeb0617eec<br>SHA256: f946dbe0156a23fd65f4c67f8c95dfc19e8984bc7f84d8323fc5c478da017055</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-10-03<br>IPv6: 2024-10-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-10-03<br>IPv6: 2024-10-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-10-01<br>IPv6: 2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.813MiB (10.29MB) – 491,568 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 677b2a505791ac63792e685d979e5fc4<br>SHA1: 4d91acdffae99cb0dfe756f68bd15f7f729e9a04<br>SHA256: aa5047c52d0e8ecc158e0ce9d6e7662f2a02d8a684c6757317d5740b9c638a2c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.18MiB (32.69MB) – 473,817 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0131ae718c767970c049c6cefe3be73<br>SHA1: c33bec2101bec3dc1a9b00f3af6da64a2e5c3fc1<br>SHA256: 75edd2c7f741675367237b4f34a71cf691ac5cf2ef598f16461ee1082f75e322</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-10-01<br>IPv6: 2024-10-01 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>170.2MiB (178.4MB) – 3,361,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4c5e7674f02f7166caf025bedc04598<br>SHA1: 9c2b266a81f934edfe3aae4fcab55649ee6c8281<br>SHA256: 9f280b56fefc8bb83bd506791af3224c48691663b6f09d39bcc01a1d0595a1cb</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>181.8MiB (190.6MB) – 3,361,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5eedd482ed20f8614ef58c83763d29a5<br>SHA1: ae15fe1bc63d1a1d89b0694b2469649cacff65ee<br>SHA256: b5e92653e27cbe2de639a248ad0e8450c686cbad854821d9409a53870bf23a96</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>169.1MiB (177.3MB) – 3,361,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ff09945f1826a2611ac13664b85aad1<br>SHA1: 9b17d2ae6dc27f435e48b94f91ea9288139d80a5<br>SHA256: f78b44b9d45871fc72f9d6f2cadf7e28eaf2e9449db2df5713ca2ed8ec98a66a</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>171.8MiB (180.1MB) – 3,361,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4407fddd3aea4449f7117a27ef0cafce<br>SHA1: f5d9f03d8df7a338aa477d06301ad8da4e73d948<br>SHA256: 62eeeb841cd1097d55585a0eaf8bf7a89f65ffec4e45dd698e0b16617c66e05f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>215.7MiB (226.2MB) – 3,361,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f87f4c3041abb4f33d1b86ced7756b14<br>SHA1: 8887054837b2910aedef7977266e67c5ed8feed2<br>SHA256: cac5f3b830c4c247d1d64a13769478baa1e6c5530a580be99d7eb94085967a00</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>169.0MiB (177.2MB) – 3,361,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21a019af53152e3b7a2a37e2cbb016a9<br>SHA1: 1e95678a905732aa65ca78102cf9615bfee5d416<br>SHA256: b694f0aeb829987602b1f5c7e073470707409a2309ae834ad12e73faa4ca9e40</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>209.5MiB (219.6MB) – 3,361,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2113d8d97c0a59157a3aea16b43e848e<br>SHA1: daa5d8dbbf77d69db31a98a242c1c778ee4d07d0<br>SHA256: 0423353f2e2cfbaf89c3dbe4021a63ad4a8b7d4f72ef11f8c6ecf1a9bf98c49a</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>176.1MiB (184.7MB) – 3,361,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64c98ab4ce661b2dc582547cf515c34d<br>SHA1: 1a3794b1a150e1f655cccfa4638878193c8fba7f<br>SHA256: 5ea4bbabf518b96877fe5345d58747b063e019d2cbfd769cdf28d1a4cc0421f2</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>148.9MiB (156.1MB) – 1,592,717 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9aa304f192c10b0ab392273c8fabffea<br>SHA1: bec6e85b287df08ba988d3d873dbeb851f730186<br>SHA256: 870b95a2c123df072348758b56c2a80acba6606af1d9e083673a083118e23e21</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>152.2MiB (159.6MB) – 1,592,717 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f2058547ddc60c42599d45da38cb700<br>SHA1: 58fce9f9d71a16f57b4971e9b8484d8dc1f75932<br>SHA256: 164f4d6f4d15ce8a650c1d36e78421b7e4e4e5f2fe10d2e050c906f05226912a</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>147.1MiB (154.3MB) – 1,592,717 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa95433177f89077aea96bc33fdc874d<br>SHA1: 7bbf410f5bb61aefd6b1484516e01a0c4d2cfbc4<br>SHA256: 630af7a2215f434054e93109dc7b73507fd57e3a751b2df4f79dc991502a74e5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>147.3MiB (154.5MB) – 1,592,717 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53f5d2ec2622b0f22fb3a2c6875a658c<br>SHA1: b4eb14ea1f30cc16fce0cce80fd31759cfd1ca84<br>SHA256: c68919d750f2ff03b25fe0dcbc973ae6e4d69c61d824c97c1046a66d667d6cc2</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>161.6MiB (169.4MB) – 1,592,717 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e912b33f51bc9f4b492d22bd5add412<br>SHA1: f6b53c1eaaa5349a3079fdd0e7ac7e7676185824<br>SHA256: fb70c65f0e4ad57b4a9e09759411f2c1e114760744e7e4aaa365819eeabde565</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>147.0MiB (154.2MB) – 1,592,717 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c81f4c5c29e64e19513cf52596f8408<br>SHA1: b28a23d9076b95485ca0b02bbfdd4d9ab3fc2a82<br>SHA256: ea0003eb6c14051db9e381951802958554a771bfa3a4f453c59f69c36d44e60e</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>162.9MiB (170.8MB) – 1,592,717 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c9ae1047bcd907ce0efb0d11b044ffb<br>SHA1: 3418f41903467d083f037087203cf2180e401221<br>SHA256: 4f28a5f8e70803ebf5b66e11a6e96ed42d98f1433cc269b7c6309639a837d9fd</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>150.4MiB (157.7MB) – 1,592,717 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7037ae92bd9a9d95bd33c0eb0734ca33<br>SHA1: a0768c954ed3741f69ff10e25a37405456cf74a3<br>SHA256: a62f99f960af776bf59a6b69cbd4026be22ea6eb7b2205b19d52b248793ee0da</pre></details></small> |


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
