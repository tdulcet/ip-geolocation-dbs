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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-08-03<br>IPv6: 2026-08-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.391 MiB (5.653 MB) – 269,789 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6858cb073a137866ec422863484f70d<br>SHA1: c6f47708377394b29214d256bd58ebf1896e10b3<br>SHA256: 81be75396538f9622825daaebfc73c1a1876647444671ef9220436828cbe597b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.72 MiB (17.53 MB) – 254,044 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 635b4919b0cb2cffd1821e1fbc68db99<br>SHA1: fefb9d4eade0d855122e9d7322ba628a7348de49<br>SHA256: 282d330bace182899c493c702e6d9371f8a78b290a19c7fec9455236c9447478</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-08-04<br>IPv6: 2026-08-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.033 MiB (9.472 MB) – 452,290 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c941e75cc999b0d702781e453645cc52<br>SHA1: 876926c41f54f9285c2eb0f63899cb3d25ca1a65<br>SHA256: 5214e00f26154581170cb18041b6d1ea189b7cc22d414905dd1217c4dac15d60</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.959 MiB (8.346 MB) – 121,065 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20cdd90a1f95af4d297f48eba31be9c4<br>SHA1: a67c20d772434ac7efeedbc4e4d4867e7300d184<br>SHA256: 0059f2b0b9763edc517f24aba21071d33c9e12d1a44f077d63e3cf5c4aa19bc6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-08-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.25 MiB (12.85 MB) – 613,360 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 011e7a5dbbcce354f64ea398785c5ab2<br>SHA1: 4232706cbd31713840cd419048ca0b8e63bac657<br>SHA256: a0804e7c99a9d04fd058589b14103c4815e6d883c992f49362b8d07a357440ee</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>54.91 MiB (57.58 MB) – 834,505 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 889d388d937b83a8601f25cb9fe054a1<br>SHA1: 5a4156b4f1c8d1434ba113137f0e56113be53776<br>SHA256: 38df46f757ab3df728aa31aa3587fa7fd7b26b78de5f924528d0fa394743dfff</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.149 MiB (7.496 MB) – 358,140 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d3e21d2da14fe2fa0da1db2f6424311<br>SHA1: f274f58aadcfa3311603218b88e8b24a01671e36<br>SHA256: f62294be209c966f38eb82e27717bc64116462241210756e85c31429048d1f96</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.92 MiB (24.03 MB) – 348,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60cc96dd0eef36fef003b9981e7aa19c<br>SHA1: 077fc11bdf3b1a16ed5a8e22cb9889e86b007cf5<br>SHA256: da4f32fc9e285ea393eb3d4fec4fb4a153874623b14fc77373e8f448758ac135</pre></details></small> |
| | | Full Location | Monthly<br>2026-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>208.4 MiB (218.6 MB) – 3,652,137 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68a79460a812a271884a0a50858ee1f8<br>SHA1: e1cb26165f0fc2b394c3f08d99642d1e5a3e653e<br>SHA256: f40963b044ff4637dff7dd3608244f6e065cc97e9bb7262d5fea4abeed6cf026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>440.2 MiB (461.6 MB) – 4,274,498 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e9801b97694446ef740a7093d24488<br>SHA1: c8e28d1130d3667d5b313b6e468c5d9d69ffb027<br>SHA256: 88971b264e462d0a2d37d85f793d5e488192b4d883a1ad0142a7c28d9a60af96</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.729 MiB (6.007 MB) – 286,747 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ce5cc1653ddb65db06474bab749714a<br>SHA1: 4cc40ea81eba37e4bdc9ce61fe9ce058d0c49372<br>SHA256: d3b805b3c0b083f2ac8b16100752f8ea3eeb8e224cf00f594602330d36cefcb4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.35 MiB (23.43 MB) – 339,594 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 518560be8d49e16a3856c31b0d0bd875<br>SHA1: b1f9595b2778075c3ff384176d6845d15decf465<br>SHA256: 5d25d7d5e32cc9f7b89b03e674eb90f100272a7f4bcd26c78e8a2b2c41efb36b</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.3 MiB (178.6 MB) – 2,947,098 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b12349e01828d4a4bac50e8c858fd50<br>SHA1: e99752a712b42043ecd9c65d3e9651264ae608de<br>SHA256: 3d436dcbd07ba02c6c6fac1fe6d1baa7bca22dd26ec4bd68d3029810ffe0e936</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>299.1 MiB (313.6 MB) – 2,898,359 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddbe75f08ad96059705bbdd5423bfa36<br>SHA1: abe287e78fb8e2391d170e4400975486e52fac90<br>SHA256: eef9c134b1787ced9b9492f2d3cf0bd3e4f7ddc7f71199e6c54374d9513c5083</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.24 MiB (11.79 MB) – 562,863 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2e477e533dcf86b166803c4aa79eb5f<br>SHA1: f0c9d7f3d2364a9964faae5848a1509429f25ff0<br>SHA256: 6a8fa22fafede42eb93d8d610d517c0d597b73cddd5c2b812b27eaaf3c37fc9f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>35.76 MiB (37.50 MB) – 543,473 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c00b72e9aac5ee4b295fceb29d27a99a<br>SHA1: 0dcc395636dd8bb8907df210f3c34fa41be36fd7<br>SHA256: 2d9d7f097ae45d3165523c43accaf5e0e8558a43b9c809488a384d448c64faf8</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>193.6 MiB (203.0 MB) – 3,768,236 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f22805287bfbe18c20db7cd4db2e5292<br>SHA1: 69b342d7c07bf904fc0714cbc79234864b2193ed<br>SHA256: 28fd4ec2cab0d7e7ef9914bcc8c49328dc11e144b106065e1ef95cd31d9570bc</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>202.6 MiB (212.5 MB) – 3,768,236 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7958ca60a61a8e23d58e7661c3a2b8ba<br>SHA1: 34da23d5a4c55b2f68d1e3bbd86dd81162db1dd3<br>SHA256: 01c0320bd2c2cd8253f696f8285f9098f1c0f186163ce2812577e127e238f9e7</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>192.8 MiB (202.1 MB) – 3,768,236 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8df64dd94ee9a3bb6c5c4423e09fa03<br>SHA1: e5263a0e0a68a37b29e17814fe1f0c705806a0a0<br>SHA256: dce0be823629beb2ade10e6f61dc4dd3c31a2d41d3a057e6e7ce1863bbb82e7d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>194.5 MiB (204.0 MB) – 3,768,236 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc745064ab17e7e4a9ab5b6ea294182d<br>SHA1: 65006d9cf7bcc43a16ce3d21706c57cc291d8387<br>SHA256: bb8726369f81dd509bd5d187d72c9125241904ad372178a2ee96c1100d837862</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>245.1 MiB (257.0 MB) – 3,768,236 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 244b1fde0c438bccfabc4cb2b637a510<br>SHA1: 0ea5b65621e74477a48b1154956ca79bdc4eb534<br>SHA256: 4383b06fc010463312e94731427a3596c7feb91d034c073c20f5ddaa39fd855e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.9 MiB (201.3 MB) – 3,768,236 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5bd82e0305232dbe09c6f4ae132f5e4<br>SHA1: 068a58da7bd98848c2416f71a05b27f656e44e6a<br>SHA256: c41f0890daa81ccc4ba135632e75be9915ae2ef0746018b96494aaa09e630c27</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.0 MiB (246.4 MB) – 3,768,236 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f8675e8d9fd90cfd2d9f317ca4e0ba9<br>SHA1: 09311d8e4d8453edaed9f5486945507235b5b22b<br>SHA256: 8f1e4b106e1e4449deaa9337624188cfe87b673798f951034894d31fa4c14c49</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>197.8 MiB (207.4 MB) – 3,768,236 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a78daebb1e01c02b794270bc559135da<br>SHA1: 436bc4ce6b7d6e6967748a1389192e63b0c25000<br>SHA256: c678a44c4efd1f555776ab931245a2c6048e4d93dc6eefb18e4b72ad8db6bdd8</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>198.0 MiB (207.7 MB) – 2,076,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 234820c7cc6152d71bea434c26766c3f<br>SHA1: 5cb8c52140a53170dc256670b9e467ac11425d9a<br>SHA256: 7205d85974745e9fbf9b44014d6479bc448fee99b1a000aa33f3e5148dfaa197</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>201.3 MiB (211.0 MB) – 2,076,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0062df10ab7732baa6f29dfa87f9834<br>SHA1: 3d84f40311d0978debdac9ef1118eca0cb4048b8<br>SHA256: 0b213134235106159ceed19cd393d907d0d45e54a792407d9fd3948f3fd89b5e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>195.5 MiB (205.0 MB) – 2,076,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b013f724977e1dc569d3d33674b025d3<br>SHA1: a54ef820da61817d88dc9132c5dfd48022ea9b33<br>SHA256: b7b91dd2daa3db8ee6e5ee594d768028b9704eec274a96033d5111d1e62d13a0</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.0 MiB (205.6 MB) – 2,076,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9977016884698da3f8a9d0da2e9c4b4<br>SHA1: b9f69684a00f9faefbd36b285f6af8cc234e75bd<br>SHA256: 6a11287c5620fea5b06291001a99e44c6630b37f84069ead1c5def69fc3c3516</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>218.1 MiB (228.6 MB) – 2,076,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90193bbdd1ca8c5f24cec67b128ded54<br>SHA1: 35d7f52f3691f0885b44954e484e2c921383ca61<br>SHA256: 56d067a38d68a48eb23d798b9a193942cf3c7bbe4fed3a97dc9d38d1ccf455fc</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>195.3 MiB (204.8 MB) – 2,076,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06742ab3ce22d40e6cda8f51a040e6a4<br>SHA1: 756536a04356e8a1636c3329cb4bf45afb9a4985<br>SHA256: 2e707e5a11bb6a73b5d6c0b52c0ee8517cd721c4d4dca900767191b38bfa1a24</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>216.6 MiB (227.1 MB) – 2,076,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1079471cbb6c5dcbe2278da947825fb<br>SHA1: 627d23148947135fc960be0da776293a5af84024<br>SHA256: c2356cd24b21d5d2c0665e87c5eb0d64dae5c298bb32cfedca880dc68d8b280b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>198.1 MiB (207.8 MB) – 2,076,737 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c124ae0f07fa1f6264fb83a6a87a47c1<br>SHA1: 66e3c23d9a85c9d7588b18226e70c9ef86ef1daa<br>SHA256: 97adc8d556c2a65f6eb642be728d6b7fbf999f9149ea44607f5c424518165f82</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
