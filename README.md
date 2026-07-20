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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-07-19<br>IPv6: 2026-07-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.403 MiB (5.665 MB) – 270,389 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 12ae20a3e6c2a76f189524a3924d8ca2<br>SHA1: 0888f4266cd3d33c9cb041c4daf852d299d5ea6f<br>SHA256: 8c82bb3094604d9fbfbda6a6e6b74f9b86909d4bad14fc977d68fcbdeae06627</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.79 MiB (17.61 MB) – 255,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3ca52c86c5d4eab880c8c9466438f72<br>SHA1: 17ddc645da9352bdef833e66a8df2146637a8ac7<br>SHA256: 5047e037ee717d5359913a64f93d33852aa0a3b82b6423118ca7fb015a4db41d</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-07-20<br>IPv6: 2026-07-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.018 MiB (9.456 MB) – 451,511 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa53e196d16630296e2f60d6ab61b002<br>SHA1: 6d436fab416ba3fabb76ac7f7d15e3d0d4d3ac46<br>SHA256: c300ce7311a9bdcd4494d0e21d39e09e7239cc412760b9d8be3c7b6baf8e72d8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.946 MiB (8.332 MB) – 120,864 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1154b1a7d9ea828f7c0dd425e4c3985d<br>SHA1: 300d0959de30929e1b714ebba3d30167f6cecc26<br>SHA256: 0320d45757f8aeba13612cdd7487102e25e1f72904ec86d22785e0c0a0dba901</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-07-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.16 MiB (12.75 MB) – 608,813 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c07cceca3f776f09e42b261c7bcc775<br>SHA1: 67732d5414d0553d375bb41e0f40bf6ccbed8b74<br>SHA256: d48e88f659cb8dbc390b8c2a38a1cb13b549b6c11060d581f61e2867563a974c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>41.91 MiB (43.95 MB) – 636,887 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 155703c91d966b16ba06a695e472d3ae<br>SHA1: 1d8441bb506ce7a29d692377cfa0fbfb0d158799<br>SHA256: 19bfc6a8db3c5077f57d970f1b5178694fae61ce53dc502ea2ae65d738cf6a6d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.078 MiB (7.422 MB) – 354,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ec835290735187164b1f2f622ad9c0<br>SHA1: 10464ef5eb489f4745096b1c71046b06409244b5<br>SHA256: 6bc4af63c1e15b4d99d5b9dd9cddeb67bbf2eafc2529ba5d9ec4525e0fe7964c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.51 MiB (23.60 MB) – 342,046 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569d0c6b66a745289f0e152318090f38<br>SHA1: baf1ef75355d41d9bc4380f97ed3b085db479655<br>SHA256: 8940a06c7f9a27f129048c5a7a0b1579b368020d88f2d2efe0fc813b6d2f97e4</pre></details></small> |
| | | Full Location | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.3 MiB (219.4 MB) – 3,666,805 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b729ab459cc2b765b3b4ea035f481b<br>SHA1: 1496af12b72ee784e304cd84eb7335c826bc3906<br>SHA256: 69fc5ebf5414a7a939fc25a35f3128451cf340211ae51ab9f82d53a331d8ca03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.3 MiB (473.3 MB) – 4,386,528 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f197b2ebcfed77f9adc3310fc7b6020<br>SHA1: 24b1454a40fdda39f37fa9367a6a6a5a88d3be33<br>SHA256: 0160ad6b5bca3517eb65f79d6db1f9e373eeb34cfccbf189a588bb330d17af06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.670 MiB (5.946 MB) – 283,812 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96cb0452e66db1c3a35242fa031ebe0f<br>SHA1: 28fae5a412332f0cedc711132a0dd6f337488ec4<br>SHA256: 2785f482dbf1f2dcb1bd3a9f253c708b1fa5f86773908ef7a2f2bb16c0dd1ff4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.24 MiB (23.32 MB) – 337,921 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1683effffd067b4fddf82095f002903<br>SHA1: 82f6a3b239649f9e8af05d58b628eeed874ad7cd<br>SHA256: a51cfe2b60d111ec234510abdd73583f12186f7fc35e3decd80fd4ef4b5ea654</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1 MiB (178.4 MB) – 2,944,788 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52717d3cc345c65ab5cb86167d9b2112<br>SHA1: 0ad1bd8bf0bdf711f51a9a37bb75090cbf4ffc84<br>SHA256: c92293057f12c2c364411c35a02de2cb229e7a21791a1bfd25cab2ba6beac1cc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>298.9 MiB (313.4 MB) – 2,896,639 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23b3d9e4addd1683ed707d17a98a0e22<br>SHA1: 572b0633e6453018a04db4c06504726ffcbeadba<br>SHA256: ba14acc8e2fc9ac380640ba99de27ab073d603598996f6737853e5a1ca4a8a13</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-07-17<br>IPv6: 2026-07-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.27 MiB (11.82 MB) – 564,268 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b02b8339b95ed8c0de4dfbd1a8cab36e<br>SHA1: c318419a7529751ed214b518c35bde456dd2347a<br>SHA256: 106a269025f03581441b1cb1e122525569d7beaedac8f9cea1a750557fa8d815</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>36.69 MiB (38.48 MB) – 557,627 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9946f059f1de1761b074a6aef20ab0fa<br>SHA1: 06a2ddf594bb20f4ca9a8d966967a1a0aa037aa8<br>SHA256: 401e0d5df2b0f53a04ef47cae851f31557a24d53817cb0aa78bac0ca9fd4f930</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-07-17<br>IPv6: 2026-07-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>193.2 MiB (202.6 MB) – 3,761,027 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fdbb0fcb0091cf42de4169bac21c0263<br>SHA1: c651a45ddebeda46a7772d45846a716850e308d4<br>SHA256: 317e30af89bbebe1099738ac5269ab572d79a25f9a9b3f642569e02125d0a6fe</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>202.2 MiB (212.0 MB) – 3,761,027 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35f0dc0be1f48768c6bc2542802ca20a<br>SHA1: 094f6f7f027995fc881007f2544c86fa4f11d52f<br>SHA256: e2a21803b7c80eb2f6e998e16c63b757d2d5e070534f4ddbd3b6e93789e76d81</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>192.4 MiB (201.7 MB) – 3,761,027 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0061bde0154e795820747d11757db845<br>SHA1: 3f144bcc068a726d2fb8be0ddfaf8d6ad95c6066<br>SHA256: 9e5e11d2326aab393a8c76cc8dad11bafed084af44673c650fd3143c632e3369</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>194.1 MiB (203.5 MB) – 3,761,027 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 757b0db9bea0b395d8d03e6b87b6337e<br>SHA1: cb65efb36e701a403d4c7451a6c28ba3e53fc945<br>SHA256: 4408bd275a408805555e5e7f428987d79f4803df3ef885edb5d3843d41620799</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>244.6 MiB (256.5 MB) – 3,761,027 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc26c0dfe5c00ba0aeb95c1784335688<br>SHA1: ce8e7e09d928a346de54d949fa1b8b103092b111<br>SHA256: 548f75b5b15191b8cd066714af2f9a7429cb98a256c2d735d6cbdd60170a8697</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.6 MiB (200.9 MB) – 3,761,027 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d53adfc2621ad548e26646e28fdac940<br>SHA1: b775b294cac860a655c6366e3b574a98c1c0038c<br>SHA256: 8aff5c2230bca744ff2696631a1022550743e0df530aa761fcbed03220962324</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.6 MiB (246.0 MB) – 3,761,027 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7dbe545a9fc01fd08314ca2af04f79f<br>SHA1: d62a5773b732a3a01b1c26688e839a39d173bac7<br>SHA256: 3c3fc7b7a2c83cadb16ca04e5c99add1ef193a8024f741678d9b00ff811480fe</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>197.4 MiB (207.0 MB) – 3,761,027 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81df3f6a3926bb0a4429914a846e27ab<br>SHA1: 2843e3839742960053596acaa3b8d5f584cf7b54<br>SHA256: 0d4162f80f71f9f1354a23da3ae949968e68844e916674b9d78e6172c564f1a8</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>197.5 MiB (207.0 MB) – 2,069,556 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae5a664f6cc86282e0f3393e2a167beb<br>SHA1: 21138c0aa76958775f21f70ccb2ce8cb812f5e56<br>SHA256: 47d3ba45d2b396d600d4254dbccc0028c05e771f7da4ddf6b43e56cba360728e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>200.6 MiB (210.4 MB) – 2,069,556 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64d9982e409076798ff4c00c540659be<br>SHA1: f4b15c518eda961c391142ceaee0041799289abd<br>SHA256: 67a0c4e229631fc19d426a8806afe213a6333c8f76cdfb66a62fdf64a56303b9</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>194.9 MiB (204.4 MB) – 2,069,556 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d04afcdc9769332ae54a8c665053b7d<br>SHA1: d9eafa3bbcd1a5e37cd70479e555849585ac3a93<br>SHA256: 24cb313fa637655bc6758ffa20986a1d27e151bbe5229424097f77f7225e13a0</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>195.4 MiB (204.9 MB) – 2,069,556 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce38891bd98c3dee218efa859b588372<br>SHA1: 51d9215696a10e2b5260242be6e52a67dddfd06d<br>SHA256: 64185a6820e988ad95c0d5f5dc6a6e90c26d696e1ea1b332700faa7674dd8fa5</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>217.4 MiB (228.0 MB) – 2,069,556 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91ceb79b30f3adafa16bcdfa17a14337<br>SHA1: 0b33df0b359d2e36af05e9b6c2271d3357ba39e6<br>SHA256: 61243c4c1e9f3a0146fd400a36337e018ec2cfdc23d18ea1667582e2f294304c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>194.7 MiB (204.1 MB) – 2,069,556 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cea0263f828ff34069d47a6ac6e67183<br>SHA1: f671c2e1c8a2f31012dd0ecebf34fe569d512de0<br>SHA256: fb1c32fe359ede9773442417928a3b58a7be82a58256c2952ed5753988229795</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>215.8 MiB (226.2 MB) – 2,069,556 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ab47e948ad10e42005bb06cafbe8d43<br>SHA1: 1228c9ec6724cfe58ed5ede00f6e5de850e70ea8<br>SHA256: caa4308c88da7b55eabea62951848336b292fe887871f6dbc99afbbc758972cf</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>197.4 MiB (206.9 MB) – 2,069,556 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b154fb64cd421ccfd7496a39cebded7<br>SHA1: 3680da08fa43aeeeab3051155d80e7a47de7a762<br>SHA256: 3cc40bc4633b23a4940e460c6d3c16c79df2349ad869959b35d103905590b1bd</pre></details></small> |


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
