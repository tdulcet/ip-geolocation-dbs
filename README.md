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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-11-27<br>IPv6: 2024-11-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.843MiB (6.127MB) – 292,579 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f57a450a0381dc64b60697c520bf285f<br>SHA1: 1e2cf72987e5a18ffed370c3013a22e70015aed1<br>SHA256: 321dbe106dfef809d3e0e53f6b07631e1594fd96a36598cf280ef634d40db21c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.55MiB (12.11MB) – 175,480 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a351e3ba136d68ba1008fc348e06745<br>SHA1: d431fc2628d5845486cf4f8859eb363fe06259d3<br>SHA256: ce4e3388915016c6cf45bb10160d687be74df4c99d5d896940159ed40876f7e9</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-11-27<br>IPv6: 2024-11-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.251MiB (8.652MB) – 413,205 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97c50bca5b3a5f98f63649f6409f357f<br>SHA1: 4ddb6f23fff5bf8744d4dd5550fa12103235900d<br>SHA256: 5b0e234a5b120b84103a7489a710224fce8b2b169e11f5ff3e435b9944ebdae1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.915MiB (7.250MB) – 105,192 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a063d9d5d91d0d2d2e1a0bf444e53884<br>SHA1: 60cbff4d44efd31a0fcda3d7b4282a59a61d5771<br>SHA256: 48c1cf097870587b67ab325047aa21e2b34fd2e7c988c86abf554fcad5d2ab3f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-11-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.41MiB (18.26MB) – 871,252 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d51f99067a9e54518e6c7984a49c75bc<br>SHA1: 7e8d9012b1ebff0bfda8b2658f45d0a488ecadd8<br>SHA256: 287c454a78d5702601c6f07f5904edb45048f06f5bdd760ef3773cca023456d1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>79.82MiB (83.70MB) – 1,212,990 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2d68e95c880418dd7d74002da2f1cc9<br>SHA1: 400b748d2ff2f4e684421df15f033c9ae492af9f<br>SHA256: c4415a55de8b2abfb5793f61ede90467f115f1ba7c1448d553026d6e456d22cd</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.056MiB (7.399MB) – 354,248 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d0746f47a1225271996460705211255<br>SHA1: a42a4bf19e2ebf577c82e10d3834e8df68696682<br>SHA256: 436aea2efe6e1523eea5e9ba484e5efba050d65a52ade285c3f9c0212c5ed301</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.43MiB (17.22MB) – 249,619 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efdc8aeb0b5fac8527fcc97613b42d4a<br>SHA1: 05d5c2e0b0a85115285dfae791b3139e2b9eab7f<br>SHA256: 45657f0c603e4d28c566dd5f9da450499802a059e8c1ff77082c945045a71fa7</pre></details></small> |
| | | Full Location | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.2MiB (199.4MB) – 3,323,413 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e766d2e8e0a2969d4ff92cf52388660e<br>SHA1: 38d95ed8fc01158d0f5ec9aa8f3bb385ef86d3d9<br>SHA256: 7656a9190b90023870afbde735c05ae68168d21190941a5da2be92e18c8b89a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>369.3MiB (387.2MB) – 3,583,553 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23856f8e31b066ac2b1f256c563a9300<br>SHA1: 4ffab13a7c3069f5a314ea0ee72c222a02103120<br>SHA256: 9d6307032c82257b206c839119decab677631aaf7e5d3138ed4b92f8cf07acc1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-11-27<br>IPv6: 2024-11-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.926MiB (5.165MB) – 246,523 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b65d4763afb899ebad44d8601c4a4990<br>SHA1: 8bd20289ad5b22362c490ef2ad87bb040144c58e<br>SHA256: f7aebea3b623de1bee2349bcc7ee3f82183617838781052edfcba6d52b007268</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.15MiB (19.04MB) – 275,881 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f11ddd1e6ba253a1dcb084442e38371<br>SHA1: daa137a952d33b33ca13482857f06e22c04e4de3<br>SHA256: 3c06071a088143b211f2daf1ee846920b62170ed33e0bcfb866ca24d62f88932</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-11-27<br>IPv6: 2024-11-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,018,795 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8a4e6340df7e6348b98025cba6c876a<br>SHA1: f5e6d82e8c5aa0282f73a857b7aa0817b689bdb1<br>SHA256: 42764697d53f138d6988d09099fd34cd0215bdc2ae86ce1f0ef8181c4a0bf79e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>222.0MiB (232.7MB) – 2,147,643 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a3ad0ce3e97d8698462c6efbd0b983<br>SHA1: 39b2430a2a62e400d659a0218fda59402e4382ee<br>SHA256: 979307d692a1cc91c6c103a0f51cdf68654c3ff286af4df15fe284354e67234f</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-11-26<br>IPv6: 2024-11-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.03MiB (10.52MB) – 502,619 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a7372297cc58a79fbd9b573ca3226b4<br>SHA1: 67a4df319880a17ef3621357d5bdf30d00baf631<br>SHA256: 24a5d5d72ebf0577ce3def73b0f513840475d183532cafbde109b75beff9d08c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.26MiB (33.83MB) – 490,302 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dcca8a0e536e156e7997e84018750f1f<br>SHA1: e1045f20a611133be6f9712b61804d007011ee8c<br>SHA256: e4dc0732da1f5b77a1400aa71078b4d32bb6279ddf95dd38798a2f885531a544</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-11-26<br>IPv6: 2024-11-26 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>164.6MiB (172.6MB) – 3,250,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e542aa41fcf61684dda18722b54aad46<br>SHA1: 9615f7ba9ce67eb1354c1f22e38dcb4008494160<br>SHA256: 67934fd3d92289688ed637846232a7164deb4f031daa27bcb5c5fbb30df84f22</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>175.1MiB (183.6MB) – 3,250,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f9cfc06cc43d00ecde3bd10905e7e99<br>SHA1: e3a8a77500e74da51b3efcc080a21fd14f5ebac2<br>SHA256: 0eb8ab0f338c68da951697bb4f9217961716777a118d6693c51d01f86c117500</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.5MiB (171.4MB) – 3,250,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44f230b10a3e0ff52b43769e660026dd<br>SHA1: 863b088b84d1c69dc6877f8f349fa95bdd408d0b<br>SHA256: 0d6a523b39ab22be01c9f3bf7fa622fa6323efe1e2d522b9c59c3df0ccf3feb3</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>165.9MiB (174.0MB) – 3,250,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68f9f0e75090308f4c3ef12246c3eb97<br>SHA1: a93d89c371ea2683859706d498e2cb6f61763c3d<br>SHA256: c1c896d54bad1e80b25e0c7530cff4c72d0cf4d0818d3337cddf9758292d9ed9</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>208.6MiB (218.7MB) – 3,250,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f919fd515a5a2b3292f016a75e351fb8<br>SHA1: 8cce9b13c4350f023ec6f9bb42567642dd3c7c63<br>SHA256: 82a0aa84373c3ba2609c4914d2db7806764a0a800fec349d72c9af3266d909ce</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>163.5MiB (171.5MB) – 3,250,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 943a7ed1423b7521d8a49c2513f680b1<br>SHA1: afc181926c4752b9119f16ceba59e8e5b729b1c6<br>SHA256: bdd3b057b25cdc6fcc59fe117665bc828deef529c9ce8f9f975a4f9153cbe6d0</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>202.7MiB (212.5MB) – 3,250,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 313a877e03edc096db5af206bddac801<br>SHA1: 575c72cc209f287239dcaa9a1cf63c52ee12b9f5<br>SHA256: 4972153016e76fca806314b143f9b6ec22750c9f967edd6b33d54133cfe86785</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.6MiB (178.9MB) – 3,250,601 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91b79fbff459c143851d9ac624c8387d<br>SHA1: 5eeb9cc4f39fa7ed37f1fdff5989bb61927887d7<br>SHA256: ffd4f2bb287cac89481c7d19cdc3250b2bf15a1c715560d5d6b633a1493b4b1c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>157.7MiB (165.3MB) – 1,683,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0701ef5c712b01e1aea7effb7e94a0<br>SHA1: 8963df06acd566b0c2ea2a7808a8bf61c82430ef<br>SHA256: 1c240c324ceea182bea811059a611b5d06153f1a997e9d7787eb712378c4b511</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>161.0MiB (168.8MB) – 1,683,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b54b0d4f2c4d108e19570b7fcafdb79<br>SHA1: 6aaf7ba6ea3dc48c32e5bb0c655800916710eac8<br>SHA256: b37172558d0dbc284d7ac05a662349aa3562b8acb79c7b13c86c1ec9c76b1b59</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.9MiB (163.5MB) – 1,683,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 982254fa93f777a64ff4fa772313dcf1<br>SHA1: c7367df5780714e3f018da5167d3e7c73086f0b2<br>SHA256: 0e51ed3598f9c425e0433a90b6e59351d605d57b65b742b251064ddeb69d90df</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>156.1MiB (163.7MB) – 1,683,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10005a6c69f7025465f2c28eecb79dc5<br>SHA1: d2f8f6caba7d56c4f6eb9e3319d9b23a088632ae<br>SHA256: 5399ed578cfb0e64d37cfc976ec515de989dba245258e65f602c3568504cce26</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>171.2MiB (179.5MB) – 1,683,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ce9b5ea21320c8f894adc09ddf56623<br>SHA1: 5930f428730329764a962c5e2f318e823da4dd35<br>SHA256: f14dcf962425cd877d092e33f2977d7ed6fda8d44294467848c9ed2758b8028a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>155.7MiB (163.3MB) – 1,683,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c16afb0e00f2dbafb9c55f7612756a37<br>SHA1: 7e3e7a8c40dfd04d0583157569f4cf3b3c05467d<br>SHA256: 8031158a100c2dff864f4165e413d9a22b1b2d7ee83a29eba2070e8f593a9153</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>172.5MiB (180.9MB) – 1,683,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8735b381b559b68aa69302168b021472<br>SHA1: 57a6cb3edc6eb1ad12c8a585e7a480de5a6ba546<br>SHA256: a9e24f548e50e98decdb4e8fb9c3e233f515a0e60cddc4f052603a1355fe8383</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>159.0MiB (166.8MB) – 1,683,697 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 15a829f53bb15bc0e24d613cd3602e8a<br>SHA1: fbd4c3f0f0686efe5bbbbb7e49f93cd3f227365f<br>SHA256: 1788bf8cb8612d6dbd3ccd66e9890af3b2bba4ab60a7c716de9dcc25cb1027b9</pre></details></small> |


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
