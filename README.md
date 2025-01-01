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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-01-01<br>IPv6: 2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.960MiB (6.249MB) – 298,393 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d2c79dec09329ee9b0b93328e7844ae<br>SHA1: dd7db916e163a864725ea869ed2a4b51c27a9b06<br>SHA256: e4c20f2617931d38aae14bb6e6e1b2f3ba5a9d130951f87e2390e8e5d27b55c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.63MiB (12.20MB) – 176,792 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f254e8f7a00e3420f95f30dd8825b519<br>SHA1: d0182b3c23f38a17187e1fae7d3906577ddf8b22<br>SHA256: b8b855267b22a0f890fb4d6863956ec16e5658e2acb8ca1ffc2ce7b7414eaec5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-01-01<br>IPv6: 2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.291MiB (8.694MB) – 415,197 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2d11d2b9e480892154b968666ad5412<br>SHA1: 538d0815f67fac8c02f142a3b1c31943be58add2<br>SHA256: afd4db5a2075909b67102b616cea9474a79cf0bf6649be38147ebdea8b4af328</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.979MiB (7.318MB) – 106,169 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 690ed854f07e9355a0aec5bc6f2a8284<br>SHA1: 6bd18b5905a3eff96a89fb4d7fdbd14913256088<br>SHA256: 2719442f069461bb0c71082a1dcc024a3b6a81e1eab2106502905eebf331a924</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.65MiB (14.32MB) – 683,492 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3e4e21949f41b8c6143f496a7395e32<br>SHA1: 18ba8df96bf0ef14e368adb4736a450732924cb0<br>SHA256: 77304f9fb84df0ed57f423aa3afb565a092bd28421f43ec9d86543c8deae732b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>80.50MiB (84.41MB) – 1,223,289 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 432cb790799ce5c2e4da24eb39b6b942<br>SHA1: 84d02ddd60d36cbab47f4461c9dbafadbd7b1714<br>SHA256: 7613b9c0d519c07978e5eb684a8fc649ff8a219d46628e664371bbb57805ca60</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.285MB) – 348,457 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83bc658c1ea05ee0c1dd67b508e416c8<br>SHA1: 70aa579150d7be548067432da89e0057b10e615d<br>SHA256: 636b0495d96e6e73c2fd6a2d599b3713d050acf8c2bc75556af8ad5d0fb3f95d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.36MiB (16.10MB) – 233,400 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea165adc6016bf7241db413dadd9d616<br>SHA1: c2e689ee2f5aa199cdf34e7bb0a4facf213548c1<br>SHA256: 40a1cbecef33f526b989ce930aa6fc2a0952064828188fe18df5b777d10b8d72</pre></details></small> |
| | | Full Location | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>187.6MiB (196.7MB) – 3,275,051 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ca665aabf2aee0b7c39b4545a5f75e<br>SHA1: 027d0a8a8014da5f6fc12e62c926c6933687bbf0<br>SHA256: 249e041ad20b36d2aebf8acd5c4d86a5f88957c86f3a7137f906df3200c6f623</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>347.2MiB (364.1MB) – 3,369,294 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb9eca947a082a3f2644b8c6907a6194<br>SHA1: 6d3040b4badad6d8c3e74a1fc773d997d8a618af<br>SHA256: 4d20b8e6b46f24b32ed9d99c2e5316f3c7e940a92aafbfdc42bea1eb6751282e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-01-01<br>IPv6: 2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.096MiB (5.343MB) – 255,041 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 385e7d39a49da4f7b26b8ca022e788dd<br>SHA1: 7bfbc318f06616719765ecf95f9c600ee41826cd<br>SHA256: bc2cb4bb17afe8e3962b87a8deb428f68ff7083def1f45c295c77d61751a71c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.13MiB (19.01MB) – 275,512 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3010eb9cc5eb5d69c08e40e6ada6b77<br>SHA1: b14d2ac80fc5b7043024cae2173668671a286f87<br>SHA256: cbf1a41317aa32c82f0ad9508afdfa47f673246f62711d998001fdfe0a7f5b17</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-01-01<br>IPv6: 2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.4MiB (185.0MB) – 3,056,590 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a976173ff14b69a2f374b84348a7b747<br>SHA1: ffcd6b20ec9ef8f0b9dc4f4c901e9fbf0f87075d<br>SHA256: b58bb3a37215ab1b1889208c52164428b5c56380cff711b82b6e54e5febfc1e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>226.7MiB (237.7MB) – 2,193,791 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fbc49d9a6e454cea9f8835d6e2277f3<br>SHA1: 9bfe0073a0141bc90622c08c9161a7283d562072<br>SHA256: 451e6a13f9d9293ed3e076c9bca96a945e2b1e2fd52e8171481f1a31a9e2be46</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-12-31<br>IPv6: 2024-12-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.12MiB (10.61MB) – 506,749 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2de82f25f66c0e88d417ce48c0eea769<br>SHA1: 998350c16a75b7b286b29e7f472c8972df2bb969<br>SHA256: d529c8557553976960aea1a033eb1bc23b460e1497a8993f62c21d2c72d2b92c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.17MiB (33.73MB) – 488,852 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6124608e446d6c04c7834034408aae2<br>SHA1: 3b726e416a0702af1fc715392e1dcaf7aafa7b17<br>SHA256: 1344e0e132a6931ad085291c11ad190fb04a0949c06f1c77db761a61e9c5b0d8</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-12-31<br>IPv6: 2024-12-31 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>157.6MiB (165.3MB) – 3,119,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0c4ee1ab9db3ff488ccd18329c688a6<br>SHA1: ddfb7bfc0ed75471c333263887d2fe06f4b147dd<br>SHA256: 32c7efec24e56aa58b937fcc2e8ed14a60905af8e9a13989bc771c54912407b2</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>167.5MiB (175.6MB) – 3,119,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: adb52451bbbebede7db7f515e1093e36<br>SHA1: 99b92ef445f207e6c16deebb8f6a589e15c5c96b<br>SHA256: 7dc4250ea1d78a0562c59be709c652711d4ba4400e9519381913b37c4684b14f</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>156.7MiB (164.3MB) – 3,119,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32eb12205a685b6a0c2d03722504087f<br>SHA1: 83e58e680a5722c28b94fe5d5157580fc0d72bf5<br>SHA256: 67999d47be67a95831744b03958e267d4b51db7e5021d3c40b7818f79defd563</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>158.9MiB (166.6MB) – 3,119,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4aec6f931562cb7d6e2f90a395dd638<br>SHA1: 07e9ba3b0e1e2095b1baa36f1fb6e8a903aec6e9<br>SHA256: 86282bc7d430ce371bcdaf5d5c868f521c931a6383dbab308344446945383eff</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>199.8MiB (209.5MB) – 3,119,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2de78907edd633c4c79bd8d6bdb2eb5<br>SHA1: 73ad832fd088c3bca9846962c782694d8a98be59<br>SHA256: d8903e16af1e8393fea47275c1e5cb5ddbbf626c47feccd09c987cb401e93003</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>156.8MiB (164.4MB) – 3,119,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6b1fb468765424f04faf6011e7bc8c3<br>SHA1: cd429b8531cde537b6fbcce2e40963b9a01a6b4a<br>SHA256: 71407f9e28cb7d7f780a3bf1aab866562e1cc1a6fafd7e7e831e8dbaaab1f38d</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>194.2MiB (203.6MB) – 3,119,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fa622a53f18155ed7d6f510206853f1<br>SHA1: 1c2e39f941175bb70c8b15510eec388afd1a3b3b<br>SHA256: 68636e767f8e4f285974a45be7b854d098b0d88662ffc3bb8eeb12130cd8811b</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>163.5MiB (171.5MB) – 3,119,005 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 437267b1c2a407bed123aca0aaf3aa06<br>SHA1: c83a4af083d68c0c017ada7261d460b6ce574ec8<br>SHA256: 4c194eafb12564293b7d00c850fc31c5bd6c5d3c630cba91072e0c4b944b485f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>152.7MiB (160.2MB) – 1,635,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d1ac2b3667fa1331a66c8bf2dce4b81c<br>SHA1: 6b496ad67be07bb01b37bf7cad1814c880ec5259<br>SHA256: f5170fa383ad968e38cacd08f3e3cbfbc6180225c5507671089e09139bcad4e9</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>155.9MiB (163.5MB) – 1,635,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49c725d882c4fbcd1a8e32cc0c2cc03b<br>SHA1: 8a509935e0792c0d47793f7d654a751200f1c083<br>SHA256: a4508b4d508e976d49f1b0a145bc1521c7ff5d8c7fd18d3c98c8e12423da17c5</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>150.9MiB (158.2MB) – 1,635,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df4cb9b1647d2a052a42dd347e3421ab<br>SHA1: 8a8f579fd788e465e022d58cf52233a0fc537d29<br>SHA256: 6a9eb9bda640f91ba9082c64ab53f68698e7ede9f626a371b4ebabf9ea5ee524</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>151.1MiB (158.4MB) – 1,635,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 203d65b9b967298e4d4955af41b284b6<br>SHA1: 1387fc2e1bdc041f696a3917731e7d6a21bb4e98<br>SHA256: 7c96e52aeb271f409a7a1eb64f23867874512d25206781fbcac6e76fe1d3974e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>165.5MiB (173.5MB) – 1,635,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1c59a3d4f6b61c62942f75783ca0af1<br>SHA1: 041a7c7bec040c5eb4391941edcb949fea9d6140<br>SHA256: 5d51a873f240551ec5ba8547b78fc8ade115128b030409f32b436e790f6ba83a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>150.8MiB (158.1MB) – 1,635,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6cde8e80249cbf85e6da66d1734ea3c9<br>SHA1: f47e849fb104684a84a90c92116b464c36002f5f<br>SHA256: 2895493b669bd5d75ec0c3f6957e971b90c496e22fe72cfb7aded3af587f71c9</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>167.2MiB (175.3MB) – 1,635,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e29da2c8339e4c057a2382c160865e1<br>SHA1: 42e9c1db3c15d7c2df67658045a5e462d258513c<br>SHA256: bd6ba9bd3a1e5232a12ad98359fd306e971657bec10d28b424c2dd840476e46f</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>154.2MiB (161.6MB) – 1,635,629 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59d20af437c58393171d9d30191c87ce<br>SHA1: bb9b2bfd3d4fb909048daae8357ca47d796fd23a<br>SHA256: bf1b6b8067a87591d3ca5754333d61501973f37cd4a2a08fc626c8bfaf036c66</pre></details></small> |


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
