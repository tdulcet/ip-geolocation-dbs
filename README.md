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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-02-01<br>IPv6: 2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.418MiB (6.730MB) – 321,381 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 606d0374eb5680146040a0275b48fc82<br>SHA1: 1b26d4e3aee7585331c697416b6f12d66a61ba54<br>SHA256: 7a63ace9b826c78a38fa1506e0c86b49b2c741ebf74648934e3bffef7dc5c584</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.21MiB (15.95MB) – 231,118 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fcaee1d465436fadcf6dff479abb92a<br>SHA1: 266ef271a3882988a4b0963103ef3bb15c99b088<br>SHA256: aac3047788921b3e68387395eb2e98ffd78c2856fbf77d202c49a8780866a2ec</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-02-01<br>IPv6: 2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.763MiB (9.189MB) – 438,806 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e729720a7414640c968b53a6b748499f<br>SHA1: a229573406ff1fbdb1087d9cd7828ee0b35e5dc0<br>SHA256: 9931bdf2d944baa0f1c4afe5bac9de3680c1db4830e4fafc36c683f1d8461ee9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.574MiB (7.942MB) – 115,214 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b35553cfbb49dfd7a300bdbb16f994cd<br>SHA1: 3465655418782ffb18fb143e7449991170fe5193<br>SHA256: 57dd7c2100dd5665f9e4d6222a24487a58fb6aabe4ff0d9dfa15fcb3bf4fc3d2</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.06MiB (12.65MB) – 603,929 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb43cfb0cb26f86538b75dedada4c504<br>SHA1: e28fe6af5efe3edf1684ecc50f4907da689e3d96<br>SHA256: 3c8cdf875533f9005aa6815639c8aae8dd706ac921ed5996f7725cff32caf4f7</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>55.28MiB (57.97MB) – 840,080 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1422ffc05e10d86b4ea4701c9062d4c<br>SHA1: 30612e13fd6684246d85fe40c125f81aadfce86c<br>SHA256: 1b37700292c3129d0dfe698dd051944e82b7d949dbbdddd20ba191a88e4d20be</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.768MiB (7.097MB) – 339,077 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0181205d24255559b4c2a13fdb0c95<br>SHA1: 77c5ed2ef6799485a1ff6d1bd9aa3aef442555aa<br>SHA256: f1a904010b8cf3e5db4f0ddc1b0fed4c77f852aa52effac37a04697ddb879a37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.90MiB (16.67MB) – 241,625 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f8f77acea5ee52ad5d81c9f3883d7a<br>SHA1: d3a894c2e7503a5fe5168eef49e53379425930d2<br>SHA256: 80ee4bf63ff4562160eda9ba68902de89a9e28a828c048003fd188647039bf1f</pre></details></small> |
| | | Full Location | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,746,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48770c63478550e9d616b0e8f11eb35f<br>SHA1: d754e9f10a536891a6f76b212ce1527fccbb205a<br>SHA256: 3abef96589717a094c9384cc0d2e88d16dcc6c1771a5eb42954efe056fe2caf0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>452.5MiB (474.4MB) – 4,397,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d15359a3c2245bffe65895c5939244<br>SHA1: a5622976378fbaa83dd68ce8bf186161f41252b1<br>SHA256: 3c33680bdbdc577647e1e500060fa0db02dc2af50f79e20bb78a7ae7ca1b33bb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.379MiB (5.641MB) – 269,229 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8df1f43c6aabf7404b9835918b8fde47<br>SHA1: 601b465ff0736111423be419aac3f6d5972b42f4<br>SHA256: 80bbfe7421ce68520f39ab366b0fc481427602add22c34ee6881ec43a96b1488</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.19MiB (23.27MB) – 337,206 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48696b7a642ffca450b564a365389e84<br>SHA1: 2da10da7971a84e435865041021aedd433c35db5<br>SHA256: 360124b18db3ea1ff8adc37d7d8c7432d236ac9d3e5c9f77123d8069ac8cd7ff</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-31<br>IPv6: 2026-01-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.6MiB (179.9MB) – 2,969,494 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5343189d8e7d3b6229056c21a834739<br>SHA1: 8489f2c88b7fa2b7726299d47a687a5af88b7259<br>SHA256: 5f47bc0d8ce6968a1388a93536b1e895b0ddb335cd76007a7b142ca0fa206970</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.6MiB (307.9MB) – 2,846,346 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c67fa86a08014c894bae1e43237dbf3a<br>SHA1: 1bfac6af73658923732d9bf178d37d1b4cf1e23d<br>SHA256: f5b735e687c937676bc7cd2a6d383e598ea54e61f46b9863d97f53062b1634de</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-01-30<br>IPv6: 2026-01-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.12MiB (12.71MB) – 606,613 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f0b41c8c73f150a5d9757eb08d3cc3<br>SHA1: d95ecece4584ed5d79b844df5dc663e8999c0d80<br>SHA256: f79a6ca148bea56751954344aeb99eb8f842a13d8e0bf6ded99b02e19868913c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.88MiB (44.96MB) – 651,591 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdbb7eb4051ec402336113b3c73cfbe0<br>SHA1: ef6cd55ee5734bffa7273e0134b64af2d1a19b72<br>SHA256: c211d31c35f554bea3938a08d4904d4e225fca7222352abadc2d97f28441ee66</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-01-30<br>IPv6: 2026-01-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.9MiB (187.6MB) – 3,533,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89c10cd725c0dd612288e793effae31f<br>SHA1: 0d3e04452a725797d75ce44a91bf7954157470bf<br>SHA256: b8d9781df27ae024cd9fa9ef317b2bd81a5d1ce18b27cd9fd7d405e349bcbe94</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>190.0MiB (199.2MB) – 3,533,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01a61d27a600e8a50deca64462862780<br>SHA1: ba4c1108a0be8262ca2100326de5f44a713c5eae<br>SHA256: 2d14a03d625d3c0e0afbe1040bdf40482a7e2f0cd3353ef453476f198290e1cc</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>178.0MiB (186.6MB) – 3,533,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24e40f120d2bd2b8bb2d7cf9eaa33eda<br>SHA1: 718475f9ccf78500e54c8989aa5e4e84ef55406c<br>SHA256: 3fb97c10876ddb3f31c6a7e285e6485c813f4d814b5f1ba4a10878f30fe419f2</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.9MiB (189.7MB) – 3,533,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f180313dede00280fb3d4355e8c0aec<br>SHA1: cb1a72a99e4a0d7d3b20091dbb58ae7ffc456a8f<br>SHA256: e4b1f03ef93ce4b06fbc09b47fdd5d6fd8fbed5cedb528095df01daf7d8d8f01</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>226.0MiB (237.0MB) – 3,533,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b98c2f6ebc163893387a2ad62de4f2c9<br>SHA1: 4035b96c4141d981c39308f698ef83bc0fca2081<br>SHA256: 5d6f80d8251039099428e5daf5c1503598c47e2a6e01282f43dcb68eed1ef42e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.6MiB (186.2MB) – 3,533,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3fbed9ca086f680c6e697ab3abaa908<br>SHA1: ee5deee5ee3f8883b7c68b16b1fc52a4ed9ed27a<br>SHA256: 9b6e4e9a10137f751f35dc63362e5b57b45c195dcac72ca38c0d8ef60118bfbf</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>220.0MiB (230.6MB) – 3,533,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59f14b8f1be3c3f535960f33d576a755<br>SHA1: b6ee9c69887ab14d52f33bbbff0d88b5ffca9d2a<br>SHA256: a174863d969a87075553e73859b22d3be96f8bd3d7608230e3e7d699c6bde4e2</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.8MiB (193.8MB) – 3,533,659 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3b2bbc52ccbf60e4561db1ff4e4624f<br>SHA1: ac188d311ac187e09a63e3227067b9778cf4d1d7<br>SHA256: 034c2faddca7f79b8fad5c45b3e3c3eb4510bda7770f63a3c87e211be3e28bb8</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>187.1MiB (196.2MB) – 1,973,658 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91a722c8246cad541f55355965264ebc<br>SHA1: 6cc7de3f7a5a4499734651754ca8739b4a7a2120<br>SHA256: dc30bf891afa93871ae7b81386f265f0a5781cf6f660923f6b505a6e5361978e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.3MiB (200.6MB) – 1,973,658 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d66d361b11debedb8d0c627e7a85b4<br>SHA1: 90c0d27a9a0576251349457b9360c437758d84b5<br>SHA256: 31bd2b9f29fd38d099efa6b633e4ecd4ad8b3b3c8609b5126d18bf07e67a0146</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.9MiB (193.8MB) – 1,973,658 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86e05b691992beee5f1a08d2108b908b<br>SHA1: 3a2e048c802e8cb2d75cd6b447b940364ea28cab<br>SHA256: cb1fc7f3129e6b85c2b99b46b57963edd576204af387b9170adeab47355afde5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.6MiB (194.6MB) – 1,973,658 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5ae648308ed3de35e2eeed4886a0476<br>SHA1: deb22879d774d345826021783b6d4681a2d48c6e<br>SHA256: 7d5ed83f1b91224a8f6a3b437daa9f3e5fb5067966dafb9885d8f5d19618c22c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.5MiB (215.5MB) – 1,973,658 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 322ffcbcc769c6f12c1753b28c5fc830<br>SHA1: cdb9cdb4ed7728471072a4c7c659561eed028d58<br>SHA256: c0b26821250dfd8a1445ff13323f8cf3dcee4af35d4a2ae333ace675b2d1e2c6</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.5MiB (193.5MB) – 1,973,658 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd388e2cbfefa7c4d8eb0249be9b2636<br>SHA1: 69f0ea23c23ee821c897e1658c2969bb47176474<br>SHA256: 89dbfcf72410b31f55cfd320b2cd58e5d2ad8c33b1ff9321a980e3b828c318f5</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.5MiB (215.5MB) – 1,973,658 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 033f3c05c4536d65398c4aac6c87fb1c<br>SHA1: 5929db3fa73460149275e041eb1eb97302697e2e<br>SHA256: e0ca09e660147a903e63315f5941071a2b042559f905b80f173e54bd86b34872</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>188.1MiB (197.3MB) – 1,973,658 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8c22b83de41c2b0caaaf55828eee29d<br>SHA1: aad473b67d90eb235ad358a18a2f426126dd1407<br>SHA256: 24fac052e293b4b1d1f13d7631a1520fd373368de76585bdee8f1008f83912f3</pre></details></small> |


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
