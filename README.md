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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-11-27<br>IPv6: 2026-11-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.823 MiB (6.106 MB) – 291,434 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d54f498bd80525137024f591d13714a<br>SHA1: b3beb7a28a3676ddeac2e774ee2a2fd4d14d8165<br>SHA256: a42cf5da95fd9461b7fb525c60c5a1b0a7eb19ac38824a10aae39ff32963c4da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>18.16 MiB (19.04 MB) – 276,012 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: faa2aa211a90035cdc779da36609701b<br>SHA1: 1bc4dec2bc6dbb109f4a27b003b51cc9e908045c<br>SHA256: 2e038d595710edca4acaf2099a35aa21b895f2f8eecafb66b8474af1e686b748</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-11-01<br>IPv6: 2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.186 MiB (9.632 MB) – 459,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84167ee008949c7e879c18eaa6df481d<br>SHA1: e998f760da828517741b8a57f76ceac532d2afea<br>SHA256: 03cc8544ec1d65aa3d43c09d4f8db8b5471fb5a48eb435c2e8626cb2c202790e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.883 MiB (8.266 MB) – 119,798 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93720f717969024f48fd382cad72f274<br>SHA1: 5173d179b24a928fce65b1c5c1194626035a37ab<br>SHA256: 645dfd169109e1cda747277411d71f68ca9d428d01b715756c1925f6ae7473f0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-11-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.98 MiB (13.61 MB) – 649,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 239fbc62b5b6437ebc7179363292c415<br>SHA1: 7b3d8f256b29b2201e4a28343c504c8fc313b438<br>SHA256: 3376b71432527374dafb14c60ed9b02f08d6d17bb3d2872807f6fd644aa14ea1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>41.32 MiB (43.33 MB) – 627,913 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6c76889788e28eec23407653b4b37ff<br>SHA1: 6f5b5211dab8443fde9f6c9f0374aeab267d2d10<br>SHA256: 8cdb3ff8ad2772b73b231cada9012b85eb6a976a9c641e8abeee98987d184e43</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.244 MiB (7.596 MB) – 362,984 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1896a3d70d9c776ebbbc51174d2dff7a<br>SHA1: 6b153e2b071d13e45ab9795a9d41e7fcbf0b910a<br>SHA256: fb52bd209b940b70d4fa6772242238a7238e3fdf267f7232a326a283a172da63</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>24.33 MiB (25.52 MB) – 369,794 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90147b4da0ef46e810078a3ca7e5aa0b<br>SHA1: 9df64ba895edf447da29fd2c604e9ff223a49471<br>SHA256: d30738d906d231b000d8994f7a07aee2550e5ba72a4d6ed8b60712ef87862557</pre></details></small> |
| | | Full Location | Monthly<br>2026-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>205.3 MiB (215.2 MB) – 3,598,802 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a48535424fbcaaabbc7dfc056e39f5a3<br>SHA1: 4394336d775415fe1a653bacbda7921ede4fd2c4<br>SHA256: a320a6ae6f82cb61d2d9b36a2baf9ed6a69c127627aabc98a1c598893700a202</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>430.4 MiB (451.3 MB) – 4,178,996 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b774537c14ceaf921dbde58aa6fb3f09<br>SHA1: 7695b1a6e7b8783b8331d8935d87fb6691eb8b0f<br>SHA256: cee773355d5c7bcb515c4efd0abc0daeb0b545de5e714601f54daa4c6c03e77c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-11-14<br>IPv6: 2026-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.657 MiB (5.932 MB) – 283,201 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f559d3d04d0b023ee00044c37313155f<br>SHA1: f2851744febf1ec81c0fb7678ea93c854509da1f<br>SHA256: 9f2d57ba5bd15600148ec8af11bb5d1c73c5df8d92d43a7b8a2f04b570234a71</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>25.36 MiB (26.59 MB) – 385,339 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdf132961e4276d4847e99f3e8a11394<br>SHA1: d6d8d534b0c26e7d9435a5baf39b738f96ae35b9<br>SHA256: 5d4536a256517e52942cc5cbdae8d65712adad9f30f5d40bc77a31a922337bbd</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-11-14<br>IPv6: 2026-11-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.3 MiB (176.5 MB) – 2,912,900 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 172467e52d3011a3e293a609cebc0b99<br>SHA1: 0d251ec08fa282eabfa086b49c7435c45f6ba71f<br>SHA256: c92d9b5f9f80250491431f7cc1993e1e07425841790dab124810a2868f53ee98</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>318.0 MiB (333.5 MB) – 3,079,222 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71bfec8cda51cd5a447bb2f7d9a32287<br>SHA1: 1e76c265df3cb7a6db6a8e501ddd8bd0fbbc498b<br>SHA256: 71ad483d60ebeb8e24249a5f0ca2595d67654b77b66044c6d204581783aa8d62</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-11-24<br>IPv6: 2026-11-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.46 MiB (12.02 MB) – 573,842 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82fa4b41a07b36915ffdbbeb0cd0c625<br>SHA1: 1bfedfdb1fa10d45da4c87f75246a92648e7587a<br>SHA256: bb56fc59479e7f23662f0adb2069b2485834263d929c81446b2a77bafd89e05f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.95 MiB (34.55 MB) – 500,773 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd0a3b8ee4c0551fc9fdbc729541f642<br>SHA1: c79845febfbfe3b19712a361e439fad7a77c7ca6<br>SHA256: 314d234afb0f5609a5bfc23b17f8deddd3c724d31f4e9cbcca2319fa08e5f87c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-11-24<br>IPv6: 2026-11-24 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>186.3 MiB (195.3 MB) – 3,650,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 496bf5a6f48a3ef2264ebe5e686e323b<br>SHA1: 3b9807348e09b28722074cd838cab98bbe650a21<br>SHA256: 13bd94176b885beefe248f424328b213fe68605f6ddff5f84059776d76357ad8</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>194.7 MiB (204.1 MB) – 3,650,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b69def66d890035b15e0ec10ff2ef5ea<br>SHA1: d5158c43211050a31e87b7e84977d2fab4b49279<br>SHA256: d747a21670a6abe6b66cc6a1a84f9adf690dcb2f2114b382233bd2a9fbb79be6</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>185.4 MiB (194.4 MB) – 3,650,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e96998c2e80e3ed1e7d55e272963e66b<br>SHA1: be025c253940858cb79fb2df0a333dbbba779afb<br>SHA256: 5bc6e1d0582ee539c01ac77d13e09ca7bf2e5b7976d576799a52ae76db2e468c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>186.9 MiB (196.0 MB) – 3,650,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: caa9ad6eb7fa4d30eaafcb41d1827c88<br>SHA1: a8195b9172acaf4903e9c6fa6c34e37174957f53<br>SHA256: 283f1d336d2eac375148e89b27e37941b70c5e521a04ed534a186de8eeb9be0f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>234.6 MiB (246.0 MB) – 3,650,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66a9cc822b296564a4060dcf3bad42c4<br>SHA1: f1a4d33cd5297160f11bb56ccf68cc055e0ce9f9<br>SHA256: 09f36ffd0fe9b19c345692d589868d503452f133633c3326ddcb6f29edb48a88</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>184.8 MiB (193.7 MB) – 3,650,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ded6864df881a7bb1c242a9c11b702f<br>SHA1: 088d404a742bdecfffc48a217aaaef14faa67a2a<br>SHA256: ebaf6aa7b6e61049a615f1b58924488bb1c016ad93e7db54b655c7b50d4142c0</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>233.3 MiB (244.6 MB) – 3,650,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 386b5a53cfb957712bc22d7765790a60<br>SHA1: 033a81d9b71d46278a436ddb43f89f7a9d0f3b0a<br>SHA256: 12bee74f706449ef1c9021a48d92db41e288a02abadf4becfb0cf07696f25e67</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>199.1 MiB (208.8 MB) – 3,650,212 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f4920152be8d996517e84ae344b035e<br>SHA1: 4a33ec8d66cb06720c2986b08266bda1ae51a246<br>SHA256: 319d85114b3d35251939d3db0ad77d6106e9527dc9a11b148b67a696e40ddf5b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>193.9 MiB (203.3 MB) – 2,045,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c359068372fc1a63cbd0e755f5e97a67<br>SHA1: ea6e29e335bc14f6cebc4d094b757b3c2d245824<br>SHA256: 9620a3b1954faf575ae3a8f83d8f91da2ae1c2211553a72629a3660b53cf65b7</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>196.9 MiB (206.4 MB) – 2,045,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d3995a0f1e9dfec5eb140559cf1181d<br>SHA1: 4d4d8fbdea60350aba7e400975f6a274521eaa7e<br>SHA256: 00de4a48f89f240db1c59f1cf57dc14f294fd146c2d27fb8895f6b62226a4c61</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>191.5 MiB (200.8 MB) – 2,045,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7220a49c44113d3d15ad15ee095aefd4<br>SHA1: 6c8a54137b308d4531cc83f979acc2852f6213ec<br>SHA256: d40692dc71690599f82b0ebce3ec0e13d106155bee0eb158fa6161f824cb9766</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>191.9 MiB (201.2 MB) – 2,045,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c445014af0dc0d755eea610bc075fcd<br>SHA1: 10526f1424ed13527d7775fa8007e4d43e77a1e9<br>SHA256: 8d9bf480bf9034d5687322e6ea842c5bfdbfe5c4210186b326b5156da8e86d02</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>211.8 MiB (222.1 MB) – 2,045,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7910c368db00246744cacd31d97c8bf6<br>SHA1: 812db7b7870a9d46822b37f26b52d80ff1848de3<br>SHA256: 560b1b5a88ee4ace0419252b4150c3cdd08b4c5bb3c6653d2939e1fa4ec6e496</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>191.3 MiB (200.6 MB) – 2,045,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b588290143359eee2e253ac67e233ac3<br>SHA1: 232a2ddb53e6ae14671f924fa5c7f5ba8a8e82e0<br>SHA256: 8f41c8736f943a0d649c5d683742db3aaa380e63f43725ba20248a21dc4948f9</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>214.6 MiB (225.0 MB) – 2,045,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22751a5d91fcb8ec237d607c7b8deaf4<br>SHA1: 9787b71b166d2e38343e258caf33879fce6523e1<br>SHA256: 4b208135e76e26633b58b4358cee62ecaf28f6a3567cb88ed74534f65cf13010</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>197.8 MiB (207.4 MB) – 2,045,206 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: faa8449e91dec898815e14bf7d80474b<br>SHA1: 1f9eb25b5e3416b5957f63c5cbdaecc434f1f1ca<br>SHA256: 89cd97a55d8f884916301b373eca03281b6adb46c59a608e36e2b0c2bf075b72</pre></details></small> |


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
