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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-03-05<br>IPv6: 2026-03-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.426MiB (6.738MB) – 321,768 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61253d2e054b00b4970c1dae372e8d01<br>SHA1: 7d1c4a3003dd1eabbaf0088d5e0fe86d6e3f6fbe<br>SHA256: c6f65c7380e496def0aa5a8e2d303b4eb1f137cb23eaff329788a8c7b7d823dd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.15MiB (15.88MB) – 230,155 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 279e9d3533a27c9c664e89c8d0099ad0<br>SHA1: bbebea2223539233d194505753ad2172a638208f<br>SHA256: c888007a747bc88673d1f1fb3fbe19c87d8dbf99c40203320c760676f20078a6</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-03-05<br>IPv6: 2026-03-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.789MiB (9.216MB) – 440,065 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dc0e7501bbfa20e99079460735be1bf<br>SHA1: 81d735138acfcdd0aa570efc1201079faf6e0801<br>SHA256: 0d69185c0ae6560ad23da9f4a67da4dd77f732db05d8992e47699a561a9bbad3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.649MiB (8.021MB) – 116,357 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9965e08736af32493cdf272e25c611ba<br>SHA1: fe013a1bad3524a71b7eb2ee37d0aaf82731a39c<br>SHA256: a5fe61c75739d27884b1c3278c80037e9bb714d1dea246b578ad07087a71d468</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-03-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.35MiB (12.95MB) – 618,088 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aeedd2307003220ec3963fa6b41b27c4<br>SHA1: 9446599dcf09029123c521664ffc585c3742b0b2<br>SHA256: a1d76290bea1dd5796045e2420966ab4dd6dc3ef18a226400883fecb546206ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>112.7MiB (118.2MB) – 1,712,831 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d515bb7bf9300ca5e8fd8b8ee293bacf<br>SHA1: 2892c853455a7d4c82a17a01a054ce033e69238e<br>SHA256: 4ced799a36d275aed8288a473adf654d6b99a2e812ecbf35b0c5af15bfb979df</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.906MiB (7.241MB) – 345,970 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be67480ebe04792eaa1e993732e26bbc<br>SHA1: b9c086649cbd7a697ce8b1a6f1200cf343683838<br>SHA256: 97e3ba0306a918694a1abd35fb0fbe18e3275c023a00d3f378bb52d0381e6ca4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.48MiB (17.29MB) – 250,508 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 614f4ebb16bfdb3cd44828a77fb774d9<br>SHA1: be56f3e3114c6c18c1b7e097bb867772c72bf90a<br>SHA256: babfcc027ee9656b7ebe280a391c73174b4990721bda2e7c584c23450f4c5452</pre></details></small> |
| | | Full Location | Monthly<br>2026-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>212.5MiB (222.8MB) – 3,723,444 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d34e3013a398743fdc3bdbd816dba48<br>SHA1: 4f4868afd37a86dcd98f0ff21e863db08c4c69b8<br>SHA256: d805d064a2ceaeb75e8ee847780d1dcf8f54852ffa98bc007b0894fd1c1d24d0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>446.9MiB (468.6MB) – 4,345,257 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b0322dcdc11f95be5a5b01f4221151<br>SHA1: 5bcecfc1d1a51db165a9a209bc8f4b9a5e7e1bda<br>SHA256: 9a67a943e4fadd058173607911c45bce627c5fbebc2abef2f229894d2e8fc57d</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>6.241MiB (6.544MB) – 314,588 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55b7e48f1421f550d07e7c9cd5a0c7e6<br>SHA1: 5829ad0a8b167bd9c3f282bdb56fc9da0cde4f4f<br>SHA256: b661ed747da0e7db38a9a7ca6e153e650ab993d9eb063344338112bed6c3748c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.43MiB (23.52MB) – 340,813 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22be91078ff2881cce88f5313d02663c<br>SHA1: e9ff49d744cc908134d45f03c6a3fd6f3c96ddc9<br>SHA256: 54e30994ac133e20300ece1b194f449e99133ba86186c397266c617d7c1351ee</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-02-28<br>IPv6: 2026-02-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>175.6MiB (184.1MB) – 3,034,529 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a603fd61b83f3b01a6bd0fab4efb56b<br>SHA1: 549a8cf265cbaab5a3fac95599e772935530b533<br>SHA256: be491b62db5ba103e1882a77b8bec049946bc21467308bed51465880485d27df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.0MiB (305.1MB) – 2,821,922 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca035a43d11f3bbee80eee6143bd368b<br>SHA1: 76e4190ec1692c0d53dce534df44d5a0aa79d017<br>SHA256: e42b6b838e8a46bbdf531ffa62fc7a715422c417ce4d9dde2b90659fc71da684</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-03-03<br>IPv6: 2026-03-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.97MiB (12.55MB) – 599,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8762c8c984458bdf14a9f01a2ba7d83b<br>SHA1: b3c935e783c2f523c9d73acc8faa2762fa91bfb2<br>SHA256: 68a649edddca520029052dce2b0667c16af3f9d9bea5107f99ef20972d7854d5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>41.78MiB (43.81MB) – 634,881 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e044f4536ab1157b6d56c4e4d142d6bc<br>SHA1: 790485f84d101c2124f69fbf3d1bf4aae9f5aa1a<br>SHA256: 0cadf912e1ddab5e5b88a6a760dc92cd13c2f93992f5990255a564f21897749c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-03-03<br>IPv6: 2026-03-03 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.1MiB (186.8MB) – 3,519,953 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad78abe9b3915af9c8809aae9f7687f1<br>SHA1: 6fa9a7967588c2ed2629401427bef25e0aa9c50e<br>SHA256: 3fb109b139317bc089609007412846b584f8f01cde0e16595be33235eb6d1622</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.0MiB (198.2MB) – 3,519,953 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4796ce9f8879a07943f0dd2c3fef738<br>SHA1: 5b8537464679b25cc7e5e3cd6ea1307172fee3ed<br>SHA256: 896b19ccf5ce095f84cadb8c7380cf4f50cdd75272b5d55d9aa39877350d5ecd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.3MiB (185.9MB) – 3,519,953 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b860982291707a186e495d0d3976fe06<br>SHA1: 729b7bf6df22664a441357ceef49c22c0ebd415d<br>SHA256: ffb4792f62e82c8f585735876487266f1fc24b18311fca6dfc927f3e40100c35</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.1MiB (188.9MB) – 3,519,953 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3bcc59bec71cea93359d14788d1a88f1<br>SHA1: 288a83ba36afac03175876c6a63ab98a6b5dedeb<br>SHA256: 653abac14a77354a0424556e239a4c270f06567757691d3b039468bd65581b2f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.5MiB (235.4MB) – 3,519,953 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22ff240055b8f9ca5e55961e356e10b0<br>SHA1: 63a236e408f2014a5986ce0f4f5d0955aa2254cb<br>SHA256: 39a2c1dfc8ed88cdb6239dd2cc1ac64090ed61cb373c1ac9972d3224d26b7020</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,519,953 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 337ee8c8c69dc3bbc6b930f3e347ac46<br>SHA1: 700f058bdbc8cc3a78837d55957ed08b4197af06<br>SHA256: 7b979b51f0bbcf330e5c2737ab1eb362dd57c89a562005436b15a9d0f32b293b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>218.7MiB (229.3MB) – 3,519,953 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c522cc449279a3279e6d7b9150fb9e4d<br>SHA1: 310646ee59bb77c44f802db803bc6d7fd6eee571<br>SHA256: cde988f1a4917dc572349d0ca5c3efd2c3a22f30f9ca0f1cedb50a61a18f01e4</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.1MiB (193.1MB) – 3,519,953 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 155755f2ad9a01f6c13486a790dfef13<br>SHA1: 7ae978114a1c1473f870f47f93c29ef675eb8570<br>SHA256: 93520181010757ffe167fe6c23338b996af9ad6aa6620b5bb2a7c62d8dbc5058</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>184.8MiB (193.8MB) – 1,948,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 719c4b118a7e4cf936702c8a85aebb14<br>SHA1: 2600be657e5e74a5f1aebd770df0dc406c2c986d<br>SHA256: 638df7c353866d8a0479310a69698cbbb5fdd436819be81fd232922e519dbeed</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>188.8MiB (198.0MB) – 1,948,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1759a1633ecdf02d64a669c4a5370470<br>SHA1: e147a733de6603031c48048fa2cc8038df70fa53<br>SHA256: 01926974075aaa5cc65bf6e93a052a1d5a38be283015ed1eeb74a29b3f44e393</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>182.5MiB (191.4MB) – 1,948,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 779dcb9c4acc1de214f429d5d9feb580<br>SHA1: 728c2bbda31e2ab9c450a666fcc03840e00a920c<br>SHA256: 353cc3ef0440e4f9c02027a9a76c4b851cf7f1f0260c71e9734d425393cff143</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>183.2MiB (192.1MB) – 1,948,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06b2c48b06c351aacee4908652ae96b6<br>SHA1: eb4707080f59c7eb659576faca871b4b8a405d91<br>SHA256: 45a7368ea9bcd8fc03f1524b1f2b3d22aa0318da5c6941b1b87f69d34d8dd986</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>202.8MiB (212.6MB) – 1,948,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc1bf55e6703616984035f48c44bfe21<br>SHA1: cc8321099ad6a72115f68a5b80d4a19263732991<br>SHA256: adcf8fcc5344d84bae87f85f9ae0c7310e5ff43c05eeff1932880b444b75bab5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>182.1MiB (190.9MB) – 1,948,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46b3bdd98614d4912d8155b635ae8767<br>SHA1: 07834dbfbc947968a72a5a32b7777148e3d6ba0d<br>SHA256: 0f57f42b2013d56694d7874bf12a41dba637b33210be6d300db2fe1485704522</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>202.6MiB (212.4MB) – 1,948,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 044c3ba71159119041b01444a04fb29d<br>SHA1: fe60133f9e0e98dc0dd502dad5390122a3715283<br>SHA256: 9907c782207b466a92524eba48b27a9adc25cf4e275f588e29600af4d3c4b8e7</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>185.5MiB (194.5MB) – 1,948,288 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5e1e7321f4a7f1f75b09eaa5b870ff2e<br>SHA1: 08edb404d5b419898635fbcb52c22507204d0a7f<br>SHA256: 673ed43ca1269839b877cef3b4308c97e55077bf032314cbea410d7491934929</pre></details></small> |


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
