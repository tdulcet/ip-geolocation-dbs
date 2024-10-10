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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-10-10<br>IPv6: 2024-10-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.875MiB (6.161MB) – 294,179 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e80483d0d9d42a9ddf7f2fff04d19867<br>SHA1: 314ca70f122df078752575ede8dea65d61a58633<br>SHA256: 1436e1f4ac5109e0518d10dfc723bf788d5212ae48cdc75d7343714510cf5032</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.58MiB (12.15MB) – 176,047 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fb9c12722c707ed75ee87ff86fafc83<br>SHA1: f89e7789e28122a019474ed685b6365edd358886<br>SHA256: 763f10bce10d618ca7757c59a20e598accbe1a57e7c8e4c70c35930a86ea247f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-10-10<br>IPv6: 2024-10-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.216MiB (8.615MB) – 411,426 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c6013a7a83c739592d90ea206f441d1<br>SHA1: 64846edd901ad2c6fc328a31aaf1c683d9e675da<br>SHA256: 114535c1667aaef8074cb6388adbbd0bc970946550f50552d62ed7ca557c7ad4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.790MiB (7.120MB) – 103,302 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c990d052b0da371d78d19a1a894d04b5<br>SHA1: 0c50dec144c653f02c9bf1ca67e87d3e54a819f6<br>SHA256: db357be2dd81c56a60af7e3ca627865009075110f9af77971009bba0f0215bd6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-10-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.75MiB (17.56MB) – 837,726 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ec7f844884c53683c45f4ed0d969d6b<br>SHA1: 36350dfc1638878a9408cad0496a03876b67d1a7<br>SHA256: ec5a4f75726dea0eb7b67a55759e8d8427be4eefd16c7edba18f8d2183a27af0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>66.70MiB (69.94MB) – 1,013,624 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19b5ffc16a7a08dc319be0124a159fe4<br>SHA1: 6c9ca3f305649c183dd267732691db86a5d24856<br>SHA256: dc3652e9db9edec88051ee8e679ca726943739e86d1d8c7665f5f9086593d929</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.939MiB (7.276MB) – 348,549 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1934c9e84da4a70171fa8a58df792d1<br>SHA1: a9efc628d84ddb0c5ec270a44c413d6e2e413eac<br>SHA256: 8974ef5ef8832adde54bf8eff5b734fbc419e040b6a1ba06eee6302c327937de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.54MiB (17.35MB) – 251,406 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccee8212e47dad6f6d37a7875599a267<br>SHA1: f12a6f633e3f93b21d90f94868a5dce0099a8f68<br>SHA256: fe5508fad3836313166aa43d498d12d6277cae16fef7835d5e92fdcd53bb2de4</pre></details></small> |
| | | Full Location | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.4MiB (197.5MB) – 3,289,697 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a0426270d27872fad498a291900b10d<br>SHA1: 4f4a7ccb4910df8d359d2ad76a1bd80c4be37d61<br>SHA256: 6869bc8bd2854724fd6be12e1a0efa4bf028d598fe1d116783216884c78d9f3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>362.7MiB (380.3MB) – 3,515,904 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b742d904c555f3e530341708e40522<br>SHA1: e367baa432e03a59b81c286e5f9bfaeeb0617eec<br>SHA256: f946dbe0156a23fd65f4c67f8c95dfc19e8984bc7f84d8323fc5c478da017055</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-10-10<br>IPv6: 2024-10-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-10-10<br>IPv6: 2024-10-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-10-08<br>IPv6: 2024-10-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.821MiB (10.30MB) – 491,954 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a82794d3b4fbd60cff4e2101a078105f<br>SHA1: 372a27930ddff7228add123d11f45f4697c96c06<br>SHA256: 2b149e2bbaf1f3bb3381ebb4120bc2151747f187f6b328b0cd81ac2bf40d36b1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.91MiB (32.41MB) – 469,732 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75a89576fd952c910a448cd194700c3b<br>SHA1: 7d58ec69efe213a178c7e56256a32203b8cd0c41<br>SHA256: bed5f5ac9fd4f700f70a81539a7dcaf8a1f5c3f1b38f986004fbe4efa74ec83b</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-10-08<br>IPv6: 2024-10-08 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.1MiB (180.5MB) – 3,395,891 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1984eec1bc11d33072f0d4ff2bae3198<br>SHA1: c2fa0352c159ead4efe0940d1c27bc9cd5149f7d<br>SHA256: 7732bb4f9d7403d104f3b9bac2453ee2fbaa97277bba840c987c73a5c56bed84</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.9MiB (192.9MB) – 3,395,891 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94d3c3df90255b608c6599c962f154b4<br>SHA1: 4d19aabba9e7b62e17aea951c01e278c77c5b2a4<br>SHA256: d345d88c465636b73e3d514378b6db272d75806788ee8ecb16ee3586f5c41269</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>171.0MiB (179.3MB) – 3,395,891 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 334ef37e6c52192aeaabea1b0856b2ce<br>SHA1: 87f5e38458c12aef73387b87e079b4b1cbcc1831<br>SHA256: 1e84d545111f475f5b97636d93c232c85f3cd8984cb952bb88ccd0feaf82234d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,395,891 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dea407d996d44754b8d4bebadd956ab4<br>SHA1: 087a4e13661f985764e4d5dbc18f747fc5c9314f<br>SHA256: 1f8bcc1a780f1fff1fd92673d7fd67aa165f8c4daf4ffb839f655837792d9b86</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.4MiB (229.0MB) – 3,395,891 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61cb57d7d3e2c989d32706f2f4ca6a86<br>SHA1: 0c7bee295c55e1f749adc2eae9e7d596623f995f<br>SHA256: f36b1ed983cac292e0c50dd6d308b42608e0de402e0af1f3d8e291d2b203392f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.0MiB (179.3MB) – 3,395,891 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e554e3ecd81ee02dbb14ccab554d1aa<br>SHA1: 8392d21263e5ff22e9477cd4c9e2c75bf275cce1<br>SHA256: f7533df2ec761a8a8fb33e208f7d001fdb8b2a612c961dda4665261ef2b30dc8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>212.1MiB (222.4MB) – 3,395,891 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a733c59cdce0d5ee562c938c50b1cf48<br>SHA1: 8766f3470ffed1ae8ddfa0a0053fd42410935a0c<br>SHA256: 0e64dd7de7265d1817060286c940ff7fb8930b2c5105a2a0f4bc1094b231c906</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.2MiB (186.9MB) – 3,395,891 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74976cbfb42a50908fa8c221125ef48c<br>SHA1: be74709abcaff856eb83dff18fbd3931aef47bce<br>SHA256: 807cbe5933b5f552501e7d86806e98f318f34622f4ff6b337e49e577c23040bf</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>158.0MiB (165.7MB) – 1,662,639 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f19e4d4b87cfe4eaf932730143b746e<br>SHA1: c497a4d281cfa449f66f236236b988cee6dc0819<br>SHA256: 286c652459bd2e5f99588181061d66443944eeed4a9951731724910c7bc2f625</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>160.6MiB (168.4MB) – 1,662,639 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f8aa724b67ab7230f6dc2b29053ff91<br>SHA1: 959c0d9d017235cd4ddfd0369fee4ce99950e98e<br>SHA256: 992c994037905d9cfa3251eaaa8ba9f8bafc5430209c3c7effedc5a0c08288d9</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>154.6MiB (162.1MB) – 1,662,639 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f7c77679a09f7622e8fa95ac3ab06af<br>SHA1: aca1320ba81315846db8ef72b46f75b0a279976f<br>SHA256: 430aecfc9e48292c684a042d907e7f21e98981412985ffbdf72af35214ebc52c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>154.8MiB (162.3MB) – 1,662,639 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc0d37bf950d2eda7156a8d35595c4ca<br>SHA1: 624430679ffc529785b69021fe6b7180029dacd6<br>SHA256: dbefd1f30d936b062f65b398a0da6c926c372952d6b52892180aadcae806261f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>170.7MiB (179.0MB) – 1,662,639 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 856a83b22ac09bb48e0533a7fa3dedb3<br>SHA1: ed6b8d2ef3dc543c3b106c5d1656c16b35c72d02<br>SHA256: 93fc9027b97623e45e2ada5044f08e661e81a93e669e977959b8b5a32d5e7472</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>154.6MiB (162.1MB) – 1,662,639 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33b0154ef4239645de6f99752f51821a<br>SHA1: 117f4c2864e6c8d31e7bc78a67e5d53bec11eaa6<br>SHA256: e7a0896020eedd630dbbb53c5349a17c38754d08f3afed71aed5e9a9f7419d01</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>173.9MiB (182.4MB) – 1,662,639 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d59027eb9405a9761af9e0b4ee08000<br>SHA1: 9f1b34c3f552abeeae492febd407982fc1df3f9f<br>SHA256: 46a76a562b15c027147705fa5beddb32f38dfaa0e72e33846f6139cd3070a96e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>158.7MiB (166.4MB) – 1,662,639 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2cf3e29d9cddcf99d4a1a4963ae5d2f2<br>SHA1: fd8e92e5d4389218f853a75b9e39895039478fd9<br>SHA256: 07cbb253f03f55e82aa7c7f331c03eefbacdf904a8fa3aa3f68bf13acafba9f2</pre></details></small> |


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
