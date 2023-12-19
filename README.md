[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

> [!NOTE]
> On January 1, 2024, the databases are scheduled to change from CSV to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) and the IP addresses from decimal to hexadecimal format to reduce their size.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because while it now has a [100 MiB file size limit](https://docs.gitlab.com/ee/user/free_push_limit.html) for regular files, it has no maximum file size for Git Large File Storage (LFS) files, just a [10 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) and [strict bandwidth limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage) on Git LFS files. Commits older than one day (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-12-19<br>IPv6: 2023-12-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.603MiB (5.876MB) – 238,673 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d0085c7553381c2260c3538e073e10f<br>SHA1: 773e424605c0eb2de1a5e82b195f033e3d7d863e<br>SHA256: 22f1bd5a597d280138761ec29ae5c32289b956f640374702701508da9c46b9d0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.329MiB (6.636MB) – 81,927 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 243c2f619e5d5fd0644250985e6ae3fd<br>SHA1: 5d95375ce0eece2b626f106e7b681274109f3e49<br>SHA256: 5664fcde24c1fcd96b2a7bb638d92ff5f1215209531cc097dc44049a705c4e15</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-12-19<br>IPv6: 2023-12-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.715MiB (10.19MB) – 412,648 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f5e3fdf5a0561af85fd5b34c563e599<br>SHA1: aaedd44c22a184277733ebb93443f8cdcf8a59ab<br>SHA256: c86b8221dd48e83f18202b5e2045387b4145b6014c01d89198aded12d4eaad21</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.076MiB (8.468MB) – 104,641 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b62ffe73055d5c7a2e28e5ccf773aae<br>SHA1: 66042351f8faea00851b177daa0e48506a21eb2c<br>SHA256: bf4449f71c8c63a4a5e7b6a9b1d0999fc49ed523fdd3c5a3b0c8b0b3b215d4e6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-12-18 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>21.68MiB (22.73MB) – 921,177 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10393c0f6bd372320a5b5e02960a078d<br>SHA1: db8c5dbcde15846982c2377c58005c8cd1d7afd9<br>SHA256: 092d7f817f4e932f41af480790845db65d8746f31936dba0e12e27f8d5182d6e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>167.3MiB (175.4MB) – 2,165,964 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a5ec220e39554b1a37b7fdbfc2c12ed<br>SHA1: 2afae626882a7720be1ab58d8590c33896acf1d8<br>SHA256: 6e2ac8f426024ac62183fee82c36ed7ddd6cf8f0b6b932e3cb06f03467a1863a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.227MiB (7.578MB) – 308,674 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7862828d186c4a916870bf5ee5c2dbf<br>SHA1: b2d61949f9d4cdf20a7bbe7858ca457da6437400<br>SHA256: cf718693f02d6570f872d99279b6729e48674fdf9a0ad17b2b5bd3a3004e7feb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.88MiB (26.09MB) – 322,049 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acf9a945a8ed9ee1ba2168317dbed510<br>SHA1: 5488b48f6e283b58e14057f8bcc69c7a60073e80<br>SHA256: e724c992a57d034ab069e985589127206d0519f5cb5070ef4d8bc04d59937e7e</pre></details></small> |
| | | Full Location | Monthly<br>2023-12-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>188.3MiB (197.4MB) – 3,100,304 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e98adbd1d81ad4e7676a5bc97c6062eb<br>SHA1: 83a91e8b43cbdbea769542d684e8a2b61d6cbcb4<br>SHA256: 07faf7b0b69afe9bdfb83c30bf26ed6a6bc739fc4122230461107e862ca8202a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.3MiB (310.7MB) – 2,579,379 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b45c72d3f47f242ccb1124627ab028<br>SHA1: 46f55d20900ce13c49f5881ad197bc7a0d54d072<br>SHA256: cade24018cccb007f481018f12d82b3268ea4089c4223c710ce4213be2f799e1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-12-19<br>IPv6: 2023-12-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.454MiB (5.719MB) – 232,687 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7477aa0dc6695ad8d9200f94b8afd3c9<br>SHA1: 34d4e346c0da88e6d4f5988e17842c38d421b8b3<br>SHA256: 46a50da207a830584042870aa5b87c2dace68a946829e6fae37461d5b3427d52</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.74MiB (20.69MB) – 255,480 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efa7b87bcf99ba42fef37332f83b9e16<br>SHA1: dc9a17b5c1ee4e438d266c97c5aacd40da6bd740<br>SHA256: 24e3b2a9267c9b1de9614d05ec54385e3a732757a59c19eb3287899959cf7932</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-12-19<br>IPv6: 2023-12-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>172.2MiB (180.6MB) – 2,812,463 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4dbcfaaf8038ec905802f3bb4b98e60<br>SHA1: bb90c332e6a73443b2c214fd4c7c111fb053492c<br>SHA256: 1a5d0936e7c432fb29ae976e5de47f83fbae93c0e2d594781ab883143984266e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>176.6MiB (185.2MB) – 1,539,981 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa785991c752e8ca7a545029b778d706<br>SHA1: 641faab98a0a64a049fa166c4e4cee2698daa00d<br>SHA256: 7dec5cceb89309fb14723f22484df38d79bcc79adcd23394d5ce983d4a58e8f5</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-12-15<br>IPv6: 2023-12-15 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.80MiB (11.33MB) – 460,948 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23c230efe4476ddb9f047fba912d13ec<br>SHA1: 6cb22bc3fbf04579666cae6a1bd0b9d6cd4ddc1f<br>SHA256: 185b9dc9e4113cffb490c6006e02aebda2bc0bf3885268bc615cc85069a010ab</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.51MiB (23.61MB) – 291,465 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d8a3aee0f766dc438ce3fb042b5d205<br>SHA1: ce34a8569fe45fdd2b237e32effc6c2025b2b7f6<br>SHA256: fcb97d181cde9f100ba65a0fa295b691e9e95f04ce8c856e09f4574b18c05968</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-12-15<br>IPv6: 2023-12-15 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>176.7MiB (185.3MB) – 3,506,460 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffba5518a0eab9fec50fb22c374c9db8<br>SHA1: 40a0239ce1eb7c00e3504cc816335850809fbba9<br>SHA256: eab3827459ae6c5688afe292ecbde61ab35768b8e889a2d97ee1f1cefee25765</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>205.0MiB (215.0MB) – 3,506,460 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b01a6b5c730049a610773c6d56b134e6<br>SHA1: 6e47840045feec1aac270d42ae83182096cf5102<br>SHA256: 6eed2537a1246d2c64d8a0c149b7a6db5f33dc8b16f38d5d5feb52c316d7190c</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>181.8MiB (190.6MB) – 3,506,460 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ed56109620632d4a7b24743ca2d132f<br>SHA1: 5d71d17997d06c84144d110f20dff5a1eec699c0<br>SHA256: 1be6ee276eda8dfb58c814e9bca884744815c6388ff63d989bec87c47fce3720</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>188.2MiB (197.4MB) – 3,506,460 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4389f940ba7eb435fc379b91e3a69435<br>SHA1: 71ccb99f689d29fee3eabd6be9aef11efd6e42c9<br>SHA256: dda70cb489185a266a31b44e4eec4325607996075f94bacd395ef29508c97f4e</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>217.0MiB (227.6MB) – 3,506,460 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66e73fe9e690a883c10b0d2cbd866774<br>SHA1: 827825b415dd0a048801d6e864cb61e5708f8278<br>SHA256: a2c84d84a83bfab66b0259ae882791a38ba0e01a34891fe5a52b3b4279af135d</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>176.5MiB (185.1MB) – 3,506,460 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e614f122490a2284357d645e1959417<br>SHA1: efaeab6ef13dcde29a2a21a26ba57de5b94b3160<br>SHA256: 24af0a437ab46fb2b6a85bb3c95d150c87287284e361d754671a07869fcf7d03</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>218.1MiB (228.7MB) – 3,506,460 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2569a604c1f86947beee8dfd68ab4bb8<br>SHA1: 37318aa3edf366162c2e6f9a45e33ac08859d888<br>SHA256: 2f940550ef641b908eb4da0ece326ffaae92a41625c2c5dbe0926e46f494d830</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>184.7MiB (193.7MB) – 3,506,460 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: acacdea60064116f02f9678a24457a6d<br>SHA1: fa457f679f207d0b2ff69a9a299514787502ce2f<br>SHA256: 584fd74d1784aac052c020a928b2f777ef5a5333f2300ebfc109aff750b12f8d</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>123.2MiB (129.2MB) – 1,223,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6519a8d84c504a65ddc7bad4426acf07<br>SHA1: 29c720d86700941668ddb074b9b5864b84c61cbe<br>SHA256: eda38b75cca90dc65011e32884dc84b40b4832eacefe2f1ee16281079bbc4f5c</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>131.1MiB (137.5MB) – 1,223,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65a37aa450e68dd18ff53909e0b63036<br>SHA1: 39914fef18b39e0dd37336760700caec969761e5<br>SHA256: a6fd6fa415d0825fa9a559805f92189c0ca2143c03b74f6d6e3e4b134823087a</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>125.5MiB (131.6MB) – 1,223,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc07b3fbe4228e0ace863356e015c7cf<br>SHA1: b091faefd1b26cc25ec2ab14db43412e55e39de2<br>SHA256: c93e8f71acf4fb665002bf27ea89d806ee1473c71c0e34efbc10defc5533781c</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.7MiB (132.8MB) – 1,223,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a56832becbafdf3d389aba6203676824<br>SHA1: 9cdf85d6d140984878b938542704f0f642456381<br>SHA256: e1f047441246c4e90f80ae631a64f5737fa9c060c36fa047434e61863a5b0ee8</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>134.5MiB (141.0MB) – 1,223,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58c39e602abd5380a376a3e03a5fb090<br>SHA1: 1b7c3dda19c5e17035791ec1803308b478cdf3df<br>SHA256: cc5cc588a4f62d9a776f44df70029ea2dc70418369aff0ee8ebc997c4dabecb2</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>124.4MiB (130.5MB) – 1,223,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66809d0f079efbebe6dc07f0f046ab52<br>SHA1: ac67d8881a47c1ce68f665a6163ffa0f294bda73<br>SHA256: c029ea7c66f678f32822438b3c92ce3672dff41a207ad645f3a19295c2457355</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>135.0MiB (141.5MB) – 1,223,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14670fa89fdce65f59a359a7cddbd8a3<br>SHA1: ab04d76f7b3b88865cdb04c14fe03ca50876e8b8<br>SHA256: 1a038546ec3ba638d33956d4e7ba1bfa978c6494a11e9e6a75b53473b2ece328</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>127.1MiB (133.3MB) – 1,223,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54a03b4e47d6b10ce88d1b7d6da2e289<br>SHA1: b2bc25fde9c8b324b48c17dbd6e1fbea99a0a67b<br>SHA256: 38a0a9742861ee747e7c526f5f694b28a62fd1f1d68acb2fe957d3477a4c6259</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hexadecimal format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
