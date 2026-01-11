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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-01-11<br>IPv6: 2026-01-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.437MiB (6.749MB) – 322,310 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbb917bb3860c94f9e9b6a23bb7d4431<br>SHA1: 8cd3aed3c7ea044e4dd38558522b68438f63369a<br>SHA256: c3cb71c6ef56b28fd7cecb35a7c4af62f8cad8792f0bf4c07d78e08ab5ade7d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.13MiB (15.86MB) – 229,916 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a811721568eeb3714d04674aa7784bb5<br>SHA1: 41843b648bc3aaec2da3012d0431fcd3b528bc82<br>SHA256: 2effe23faae45cfa63859d2b06ff41dc31bddec3683786c339a141a69e5060cd</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-01-11<br>IPv6: 2026-01-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.194MiB (9.641MB) – 460,318 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f407b0f259156bf6bb18c6ff1e18c5f<br>SHA1: f5176cb9db1a2f78ba79afc2953f8a81aad48bf6<br>SHA256: 450c71d365823768dbea071c67943ad18f393046923fa68a224b3a141f152dd5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.529MiB (7.894MB) – 114,526 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f26335ad48117887ebde0b1194897b85<br>SHA1: 8c869dece2a0fa3ea77444fe77a601ad97f568cd<br>SHA256: dde1a2cb8c4cd7b78db8f1cb9e762baccf419a48752da4686f7f4ac7f6a789f1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-01-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.51MiB (13.12MB) – 626,252 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95a1ee4e3a620c8a9ebac985a893a93c<br>SHA1: 5d20059b91a9091917ab02ec9d4e07a7b90ca4c6<br>SHA256: 7fea7e6938d9d43d84d5429d74c81bf89c2b49a5b5b4148a5e053078e13da699</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>66.01MiB (69.21MB) – 1,003,101 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95df3f6d875741cba93e7076b43b0918<br>SHA1: 4257f60756efa8db6bee7fbc370a330d6db68f8f<br>SHA256: 672564cf5947aa103c39825d5fcaedbd49928c42cf37235bb01f17c7322d8706</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.843MiB (7.176MB) – 342,905 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7f0c42b88b3ee5ac2070e71f756f963<br>SHA1: 4416542c9574226ce202070dc48ca08edc6fab0d<br>SHA256: 5393382f53c552965d88b65e40e02f63c643f2379a931aaecef8209586b9ced2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.52MiB (17.32MB) – 251,059 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 232548602865156556e4ff9d7db331da<br>SHA1: 61d1e0b2cefeca101ea9e8530969dab152188ab6<br>SHA256: b004edb93559a31ded3baa727a5d781edbe90c29420b4d5691f44e917e83bdb0</pre></details></small> |
| | | Full Location | Monthly<br>2026-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.7MiB (223.1MB) – 3,730,744 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42e04cdc8d81a8ce6b440accea48b373<br>SHA1: 9c414f68d243d9ebdc8b7c65e081580b035b663c<br>SHA256: 5274313529b847bd8629fb44b41144c683552f55760a830f535892f20b8e46db</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>457.0MiB (479.2MB) – 4,442,155 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56e8f0cd6817f6807824ced45628cb9<br>SHA1: 316812aba9e80b97b08bfca58defd796b628d008<br>SHA256: 44317ed175935104135d379f2a9918ca97141e9bf034ee1bca6cdf894093d72c</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-01-08<br>IPv6: 2026-01-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.331MiB (5.590MB) – 266,810 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6936075ec427c7ed70a3d342b2e63912<br>SHA1: c7fae99a3a0567ed7445644b86a01fbef762ef6b<br>SHA256: 88ae548c41c1713b32260bdf14c95996bb2d7387a44e2bfd64ceb76fb873f61a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.53MiB (22.58MB) – 327,213 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27348409796721908a924318dcfc1b14<br>SHA1: f2aab8fb5a03f1d5d37b344e4c71e1277dc90aa7<br>SHA256: f0b5c009770b082f8e457f65291614d6cf88661b7518fcad74bac3f296014c2e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-01-08<br>IPv6: 2026-01-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0MiB (179.3MB) – 2,958,239 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49e99e9bd1ec9e6374170f539a275d4a<br>SHA1: a346ea441ddc4850ec1942528df68a32230e83a8<br>SHA256: 9a2330d68bf4d693241559bf46574fce71265babed257de579a39326314704da</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>284.4MiB (298.2MB) – 2,756,871 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4043b07a9b191aa81c8428790ea89b1b<br>SHA1: f2e22768f73813f9e8b3d567b96e9129fb4a8790<br>SHA256: 8566a2873416028bfa9a7719f3649be95b44f46de14bcd84a0dae66027a203af</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-01-09<br>IPv6: 2026-01-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.17MiB (12.76MB) – 609,351 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec5818fdd6c8017106602fd5b575aef7<br>SHA1: 52e82ea93372effbc8e161053d171ba7364297fe<br>SHA256: ebff2637929339a88e5bf56d56cd6e859d3c01654ca2eef9bbfcf0d11bdf6377</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.48MiB (44.55MB) – 645,630 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5553d66f8cd7ffbcbcbc6a7c1f357cda<br>SHA1: fdf9705e36849b8ef9206e4e30c0acc42624459e<br>SHA256: 529ab4879f8fe7d4f80e3369a1aa08b26beaf18d3ba5fa3a8d5d48521b127480</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-01-09<br>IPv6: 2026-01-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.0MiB (186.6MB) – 3,514,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6628f79a3ac0f75a59fac089ea2702a6<br>SHA1: 6381d1e012d1e0f222692d36ff13e3163f5dcd1b<br>SHA256: 0950c1039f3fbec60c39da5a5292e47244a02536da4a401adeb026a92a5591d2</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.0MiB (198.2MB) – 3,514,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d26a4defb3526ca577f171343c889e9f<br>SHA1: b93dfecb0fda7f32cc74264866f6395568664dcb<br>SHA256: 7049d528c8a7fb585a4cbca60a1c5d2e2779560f2196f9c96db6fbf02380ce60</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.0MiB (185.6MB) – 3,514,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b17b829a1ac19480e5b7a573496b98d<br>SHA1: 9b58672ba498e4c817b004368df409a45e7c32d4<br>SHA256: 2193c55218f7965a2d66fd610466c6fef6520699d0d312f8cee4e482e1a565f3</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>179.9MiB (188.7MB) – 3,514,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e2abd4ae066c855e07449855392997b<br>SHA1: 75e765e9fa282c3887dff1716a499fab67837586<br>SHA256: 5bf1e6d492a07d95e93f44701a44935ecca59228e74e33ed1906c63418c0c3ad</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.8MiB (235.8MB) – 3,514,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90e19e7612488ee99a033c1e453058dc<br>SHA1: 6032c31aa047a44994715cf80b4564b896699d3d<br>SHA256: 06157c00382b215e9989b8b70b2fb81c4abe3c12e39db9b03b41a1a9abac9ade</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.6MiB (185.2MB) – 3,514,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3003ff129787a08cde33ee5879d6b59<br>SHA1: a193b2f3e948356c5e30ad058addc55e0d63831a<br>SHA256: c3c25ef35869150efd5801861acad9ecb35c161d74d1a53da032dd23eabf6239</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>218.9MiB (229.5MB) – 3,514,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e447931db7271526ee081df23bc0bef9<br>SHA1: b6743c4edae2e5e61982884337e84cf8c6592df4<br>SHA256: 45e9c04c0d8a43c809128c75ecb71b1684e45d370874de7b35286d34bf988567</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.8MiB (192.7MB) – 3,514,579 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f907702198327404e4c2089d10aa9569<br>SHA1: be6a905312412900923c3be1f4413db4c84634a7<br>SHA256: 2edf2392152a29954f692a4142430fb303d8f450d161cb853d9ab50f20762c31</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>186.7MiB (195.8MB) – 1,968,105 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63e4744d1ba89cf57fd11f13f33a96e0<br>SHA1: 17681037dbb38fbefe2e64cce70ca22c893e263a<br>SHA256: a2105108279e66c971bf903d9f9ff4e4a07a6b7e0a16c807a4b5a20eade02edb</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>191.1MiB (200.3MB) – 1,968,105 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b048c98ca345334383f5be4a308e1fde<br>SHA1: fe9813b323a63f862ab625d2247141c40bffb037<br>SHA256: e41eab1c26738e426547f9fd327a51b6f49646ca99f69f94af27a5c2a17182b5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>184.4MiB (193.4MB) – 1,968,105 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69d6279f8fd0c80188ea6bf504309757<br>SHA1: 29aab03349ebccd264702e29134de9951f3abe18<br>SHA256: 4b3be74ae6f172d88fc471e01f97730e3b1e94939b8c7fd4dbad0f6c88656e75</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>185.3MiB (194.3MB) – 1,968,105 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6453086ced2446dfc70272ee3124e20<br>SHA1: ac5e84bfe7bac0ba40f1a9e6f7c2cad39c6dfb77<br>SHA256: 14e363215ee80eb90bb9b3f55e2f363e96811344e1102641717f01b6226b6a0c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,968,105 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 052fe32c19ab659a65e93746523b8c9d<br>SHA1: aeb5bc746b6131244bd642ccf0ffa6ea4c688a69<br>SHA256: 27371cf701d557719c64581bc3fb951ba37e861fcf760294343df4828f2b21e5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>184.1MiB (193.1MB) – 1,968,105 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1bd32c77a8b8dc5a095dbff05ebc67a9<br>SHA1: 4e53d93ceed51f5b95757ca635938c18ff2ce4e9<br>SHA256: fe4d5ba13fafc9878803917b864627669bd30c08b2f56cbd5112844c3da6b74e</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,968,105 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92de25e4df9856cdefb37fd14a1bbb57<br>SHA1: b4e6cc09570931d8810e085da7c341159569480b<br>SHA256: 4d4f70faf1931eb66448f5cfb8758ee9ea4e5367769079f0108cb22de64501f3</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>187.8MiB (196.9MB) – 1,968,105 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56172d59e64d2157fa2db87b81427098<br>SHA1: a6c2724b22608e8817dd0bbf00aba600d33e3753<br>SHA256: 5df70fd6332caaace0449d1c17abd2c01c1339c9680aeb259b5ee3399c2632f0</pre></details></small> |


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
