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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-11-13<br>IPv6: 2024-11-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.895MiB (6.182MB) – 295,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2b305e386035a1bb39976714b64259f<br>SHA1: efe63c480bce856c8c08a6074f747302c69297b4<br>SHA256: 3c260e7b9d170151289499b06f609735819a35cde50128e6e15240ccb8ce3ef4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.53MiB (12.09MB) – 175,183 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 488e2229315e1e170242fa96b82828eb<br>SHA1: ed12ee9994f17855c7465306820cd19fa0da1d65<br>SHA256: 0557b11a7d55eff4c285045ff0f7a5aa6792ad60ffceb649e98efc5980dcea5e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-11-13<br>IPv6: 2024-11-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.234MiB (8.634MB) – 412,343 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e41f0e193f96495dfc7d1dbfa52fe5f<br>SHA1: 525a9353b5b92ac7031f2be3696d0c707dc4a37b<br>SHA256: b7a3ae5df8dcd8f64b241ba91ed50d13f4c8b59bbc8dd63da93717be22e26ab6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.854MiB (7.187MB) – 104,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 402402741c845905b7b160e2ccd05460<br>SHA1: 897f5002bac44bc54f93ab69eea1ac1c2ea06934<br>SHA256: 08cd794479448327955596d6aff3b748f20584baeced26887fa0023aefd5e340</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-11-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.06MiB (17.88MB) – 853,279 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1939874b20664cdfde18914ab986266<br>SHA1: a292058cdb6e953ac73a1b55dfe13e2d1c1c2270<br>SHA256: f9efabc16db4333127561b30c51be257646d0eea221177ce5c30c7b6b187d1b6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>71.93MiB (75.42MB) – 1,093,104 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad188747d67162ed26baec8ea8263b07<br>SHA1: ec39ac2135cc9dbe9b02880559f35e1bc2ac427a<br>SHA256: a62df1aa561f2ed8df89c8afeb5a6e9d3387a28f25bb68cfb4941f2ce9f7a585</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.056MiB (7.399MB) – 354,248 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d0746f47a1225271996460705211255<br>SHA1: a42a4bf19e2ebf577c82e10d3834e8df68696682<br>SHA256: 436aea2efe6e1523eea5e9ba484e5efba050d65a52ade285c3f9c0212c5ed301</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.43MiB (17.22MB) – 249,619 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efdc8aeb0b5fac8527fcc97613b42d4a<br>SHA1: 05d5c2e0b0a85115285dfae791b3139e2b9eab7f<br>SHA256: 45657f0c603e4d28c566dd5f9da450499802a059e8c1ff77082c945045a71fa7</pre></details></small> |
| | | Full Location | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.2MiB (199.4MB) – 3,323,413 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e766d2e8e0a2969d4ff92cf52388660e<br>SHA1: 38d95ed8fc01158d0f5ec9aa8f3bb385ef86d3d9<br>SHA256: 7656a9190b90023870afbde735c05ae68168d21190941a5da2be92e18c8b89a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>369.3MiB (387.2MB) – 3,583,553 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23856f8e31b066ac2b1f256c563a9300<br>SHA1: 4ffab13a7c3069f5a314ea0ee72c222a02103120<br>SHA256: 9d6307032c82257b206c839119decab677631aaf7e5d3138ed4b92f8cf07acc1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-11-13<br>IPv6: 2024-11-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.921MiB (5.160MB) – 246,296 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40e580b10d9fe17a204d4682e8caec62<br>SHA1: 86c3da422b58cf1b996348924dc8256bc7f8c0df<br>SHA256: 32168c3110bd3fb45b79eed0642def8db10a273ed5096e224c2de29a05e02fca</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.04MiB (19.97MB) – 289,357 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f83651873d1db0d8addc8985566a84fc<br>SHA1: acbfe44dbde35a4fdbd66b655d20885747b3b874<br>SHA256: d240a5da5dd52cc7a57780fad1a11415b8e2130d68731c1182f1798b90e567f5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-11-13<br>IPv6: 2024-11-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.6MiB (182.0MB) – 3,006,530 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3205f79a16c843aace3d3a8e3aec5334<br>SHA1: 8987d05a3901bd7ec7439251708d0c2228642999<br>SHA256: 807a107f4be6c9d0eaa439b6e63f93c3067bae3d0b264ed83a142d3318442718</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>215.9MiB (226.4MB) – 2,089,755 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e072b36b8644392e07bc9ec16c01aa89<br>SHA1: 4145eaccf7a8ff6d0571c6ac031eefdf75dee798<br>SHA256: 575d88a498458f0cac331d823e497dff499178b951353e2f6594814450a3a71b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-11-12<br>IPv6: 2024-11-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.990MiB (10.47MB) – 500,390 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17b5e35f38138362d0cdf38bd3f003e4<br>SHA1: 591c5c4b654aec11df62b0e1a5225c6d55b050db<br>SHA256: 21e7752a5299137d9e4d95132db423c195fc9d8c45fb74b0194a9c98f40b78c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.16MiB (33.72MB) – 488,673 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 305d56622533aeb450c232ebc4627ab6<br>SHA1: f37c7fc8aca106d8d32fb2c806d9e20f742435af<br>SHA256: eac76473bf2ea15f03303c3dd623141d5121a7aae892d9af1d8e533674224144</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-11-12<br>IPv6: 2024-11-12 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>164.3MiB (172.3MB) – 3,244,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e841a00d66ddbffd7799f964b90d3576<br>SHA1: 5d948cf7f22369f3b23c487b87672cc9c90b0b36<br>SHA256: f4a20cc216feb1927f42294ed6e036079851021900bfcac6984f5073bb51d28e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>174.8MiB (183.3MB) – 3,244,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94658cb7ef2eab55d049b16202ed1fc4<br>SHA1: b7383b0ecbe3b64e5685b3f5316cb4552f078e84<br>SHA256: 8fc0e780af1a42d587370ec139c25e7ab243007a23f49cceaab21593cfd7135b</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.2MiB (171.1MB) – 3,244,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e01646f0b106e0c1588586fe1f76815<br>SHA1: 0d5f1d0d6592942cf73c894a6f771a8a64aca7f2<br>SHA256: 636061f30c9150922c0e542ce58776a4d9e51b5d8866edf5f3ae4cfb114f8526</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>165.7MiB (173.7MB) – 3,244,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c8e38fa1101c6ed9850f4aa0307477f<br>SHA1: 48d4f890d7050be17ec1c917b9daa848b45a1612<br>SHA256: b4aa477a5d675ed4a7727aaa4812a2a0778ea56d0fdfe92d70abbc119b6bce0f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>208.3MiB (218.5MB) – 3,244,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db840d8b8449a857ec509fa21aa546c9<br>SHA1: 8aed67a075bb6d7cc9dcdbe909c9b21580e8e021<br>SHA256: d6501804d167b9fd3379047103f151006571723c8419a54c5868afcfc7835f12</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>163.3MiB (171.2MB) – 3,244,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 284199974eac0e6d23bd3fd0b87faf7a<br>SHA1: 14636bf3c5ddbe45642e5a13a463689b61bd367b<br>SHA256: 4dcc5eadce411d4477fdfb2d70e96bf4728b3f9cabd74dc744f9004b42866037</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>202.5MiB (212.3MB) – 3,244,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5654640aa193a71a8d169f541b71e04f<br>SHA1: f198092993d3fec0641bcd1792814e0fd7652c9c<br>SHA256: f96ff9c45eefc5a48166ce5235692f819f37f27368c72d9608e5982d336379ee</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.3MiB (178.6MB) – 3,244,794 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c52adca13f1c7cef58d11a068b09594<br>SHA1: d6edf49f344834c00d1db8ce6d23c73e39191f0f<br>SHA256: 74237efa1a68a152ee8d3d9dea965388330cfed685246ec56611b5a01bb683e0</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>157.3MiB (164.9MB) – 1,678,984 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbb388ccb65cadfc62639da37c283078<br>SHA1: 892408545751ef0b1fdc4b22a7d32b6f8c310a9c<br>SHA256: 000c7079f3c1cfe89622857769b217aff11e20fd5220328d635eb19d7290bd94</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>160.6MiB (168.4MB) – 1,678,984 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7424ec607da10880d79bc8caebe29563<br>SHA1: ff667d974c3930fb2babd64bd78db6e801df9649<br>SHA256: 515192340b954d4d5a1b29054cdb7282ff8ab6db7e0403eb8e2c1f1758013ce3</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.5MiB (163.0MB) – 1,678,984 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f278533e01e16c2fbd677d65ee7473d<br>SHA1: 809c8debcd5a002141510c2bff727a4ee17b9841<br>SHA256: bf1e0bc124cf3cb28b49b1c9182a2dae1253b07c16edbc3045c34b440fab3937</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>155.7MiB (163.3MB) – 1,678,984 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb11fc6eebe85a3b1c597f3424b7a905<br>SHA1: 2f0bf2859f5e55f31649bf154e87e337d49e9d8d<br>SHA256: db7d273078bf69e6d361a2fda26dfbb0834fa8cf8b5bc15622a911008cc39303</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>170.8MiB (179.1MB) – 1,678,984 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f4955ebcc8f88899cdc6a08e6ad6550<br>SHA1: 0efbc08edd7fd089f55f154d6b075943cd8e5be8<br>SHA256: 506fdf4039f788cf96691305bd9cd5fa44400eabb6d0c0d6b7b43adc7764601c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>155.3MiB (162.8MB) – 1,678,984 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2582f03d8f927a2c45d0b556269e58fc<br>SHA1: dbba2c24d74f6da2e73e11eeeef81848c21d7d6d<br>SHA256: 9b79a19904f65cafc6250815659817b012df11e56582e6b941570fd32bfbe310</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>172.1MiB (180.5MB) – 1,678,984 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01e86cbfa5fc3e40cb9bd3edd439d547<br>SHA1: 7a8ad045751797c57b9bb93020cfe87a12cd3855<br>SHA256: e099752bfb332e271b0bb67b1c92c4b124d2b0e9dd80eefe66c5b5f48aa6c7f0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>158.6MiB (166.3MB) – 1,678,984 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f5aa05154ee1e1f7cb2187aae42dcb4<br>SHA1: 6f83ac26706484ee20f92c60ef013c3efc3333b3<br>SHA256: 8605cfa1d14d96e061744be05fa6b592fb51eaeaf83a1ebd49743145163279ae</pre></details></small> |


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
