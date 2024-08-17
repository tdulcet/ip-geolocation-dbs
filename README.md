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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-08-17<br>IPv6: 2024-08-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.767MiB (4.999MB) – 238,654 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc1a82dbc38c3d5d4707e4a1611a3256<br>SHA1: 6c8b2c312ef173fa5a5e7c865da60bd31ceede8b<br>SHA256: 3b9e93283ab04552e647b3e44f71c607b0a73d45b05acaba0df17dead8697a17</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.799MiB (6.081MB) – 88,132 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e0ba1059e03ae193891e431ea5337f8<br>SHA1: 1f6d066316c807292ba2f09c93e1e88f132d35a5<br>SHA256: 97aa1a41c8ee61477ee01032a8fdb5d223ed3c768747d9b01e184fd3bef92d93</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-08-17<br>IPv6: 2024-08-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.134MiB (8.530MB) – 407,361 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 513bce948f677814ec42f630cc2f4d6d<br>SHA1: 58859925da2511d2c562eb1669d45cc084bb87fb<br>SHA256: 1693d1e2ec314881a939ec1d2e520d45bb7a3a5f3d1cccdae6bfc0cf27df4076</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.657MiB (6.980MB) – 101,275 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1951940a7f2a36c55c89f449c39bbe80<br>SHA1: 167e96f6ac34127b18d990a02e1adee966307de9<br>SHA256: 2050ab3afa0d4df21275800ad8c5847f644b367bf5864195e9c6e24b1993f55a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-08-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.96MiB (17.78MB) – 848,283 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d09115091cdf1aeb2b20f8f3d41bea23<br>SHA1: d015a52b91d9008c578f0d880873d9c860219c57<br>SHA256: a3cd080c7be904978b871b8027cb988329c9aecff15d9c2935e5b92fb838ff42</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>67.29MiB (70.55MB) – 1,022,534 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9c4ddfda7e55f62beeb598b69dfade8<br>SHA1: 48bb0ee468255ada16148118e710a945a99592f1<br>SHA256: 55c3ac2dd0ba5cabb47b5c41c6f161ee7103dcb5ee25554045e933bcd22534c1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.930MiB (7.266MB) – 348,283 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0fbc41bc5bb2b90a8e0d5e5ce544a9e<br>SHA1: 1e8f1c989a09bda0597a4fd20bb1baf0e1ac7146<br>SHA256: 5ca608bc0834afa2ddcddbc57debfbc70f177637b74991fa1f5eac6b4004250c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.13MiB (17.96MB) – 260,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d830eaf780889ad98001bab48d5aa45<br>SHA1: b197b3368dda5c090062b0f952b463dcc36089a0<br>SHA256: c9b5f78bc10fd064cbc6e77285c497db8377b1d955acc23e6e6498b158cf6e7a</pre></details></small> |
| | | Full Location | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.4MiB (195.5MB) – 3,254,855 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a701f04a73cc8f80f1d62d7d31565c1<br>SHA1: c08290366ff76b789e82bc1d59e49f3a8b096083<br>SHA256: 05ad2982bf2f1253f055b5d985d376d16bb31cace83cb242d464f0595b931ab4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>351.7MiB (368.8MB) – 3,417,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e978ebf3bde1f974ba0a4b6532bcd5<br>SHA1: ce0a2c31a0c136ca457da29799b4d9d902203525<br>SHA256: 04b7870a00431ac40aa31592ac986f30dc8fcd0035a95ab9beee69df67b812b1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-08-17<br>IPv6: 2024-08-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.983MB) – 237,847 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a19f3b324b30f1b8e58614ced6c3eb<br>SHA1: 0ae869a9dcd1e992112ca1f19381c40b51f06f2b<br>SHA256: 16ded9b540a430569f72a4e9231fd255fdabd1dda07b4b19d35f69b1de8705a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.46MiB (19.36MB) – 280,554 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48429e636d89243b95e58e224ddcab83<br>SHA1: 62476d74b99370f1cf7032a405e741d78678dfbd<br>SHA256: 0cf7afea40b0dab546ce14724386b222921daeee0d831eecb913854ed7bdc0f0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-08-17<br>IPv6: 2024-08-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.1MiB (180.4MB) – 2,980,631 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b3e4b34496e91b79950bfd2ba90c64e<br>SHA1: 65cd184136a3ebc843b8b661eb3d7e435d8e169b<br>SHA256: 8fe209a185d5393cb91b8ddc3d044e30a9bbb3dfd9681ecce9b281cc7e030387</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,986,964 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf91d149bffc17e272f874de287e1a0<br>SHA1: d7fda16f424fa431e16b71116da2588052e905e8<br>SHA256: 28d426aa8fadf9fdb6308784807383ed47871f07d6c9d66d67e14bc55327d0c1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-08-16<br>IPv6: 2024-08-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.898MiB (10.38MB) – 495,838 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31dc92be42e6eed912b891664e83c237<br>SHA1: 4b198eed7e1965a4df0588c49855a7b0cca42d1e<br>SHA256: e0ea4162ea02607c8d5a939e3a4f775c6e963cb1ad71e3578f077bb97474f36e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.02MiB (31.47MB) – 456,163 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19ea467d42adca9bfe56086ca46771b8<br>SHA1: 40dddf360c5aad38d926880704bab47e179e21c5<br>SHA256: 0e72738fdb081b2914f748d2fc1030501727c6dbbd09c7e03ed76f61d9efeb90</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-08-16<br>IPv6: 2024-08-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>121.7MiB (127.6MB) – 2,433,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31c669e8369f7d943fae5ea9b03ff343<br>SHA1: 1ac225ff5d04fa24b35317617aabbd14f439d4d1<br>SHA256: 139c1c540839cb8bf346833715d9e9fbd9139503e29921c5d77c60b9e1cdd56e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>130.5MiB (136.9MB) – 2,433,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8da7922b8209f67c126eac9b64814e24<br>SHA1: 7511c9da0484423194be3934b779c8d9944cfcf9<br>SHA256: 7d3c7e560e501ac689153a586d116e182a60304e8725c14b6d31c7ea59acd3f9</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>121.2MiB (127.1MB) – 2,433,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e81fcdabfe4232e192ae0ae6fe5aa386<br>SHA1: 6df25feb08826719ba0c2fc5e958b82689a812e1<br>SHA256: c6e1cea8db95771dce77dbe24feff1a72df77e2b8ccb55908a709a39c9969ae6</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>123.6MiB (129.6MB) – 2,433,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfc4e3f5d5e29487866a4ddd93a47209<br>SHA1: c947a1beec26daeaf676c399ab90459adfc6ec81<br>SHA256: dd4d8f2a2d7b03818733bc61be35592f2fcf35d96c6ef7cf8820f0860acc834f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>151.4MiB (158.7MB) – 2,433,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cba835c062507f82fe42f00879d48258<br>SHA1: 544d2d791b966f2dd8ff349f5081dd78da5a10a1<br>SHA256: dfd7d6d91229ceb35311742125ab93da76d77c32a07b3ab82f3b9721c5e72b93</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>120.5MiB (126.3MB) – 2,433,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 559124b280d66c184b1cd7f17afd80f0<br>SHA1: ec25331f921ae65d2cf7e04cf9e408db3b24e720<br>SHA256: 3ab877542c46b45056a95844382d5bbc88313e4dce78e43b935f9d373678e9a9</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>148.0MiB (155.2MB) – 2,433,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3becbf881ff050d1156d1f6a2b4f0e07<br>SHA1: e93a9655d8711b08ea3840e33c0602421e6edf5a<br>SHA256: dcfff4593b5547f34c0bf3f6a1bcedd4bb0c8aeac323d68749f117534e41738d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>124.1MiB (130.1MB) – 2,433,623 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30fcc2bb165448f129bb5a7611ec9aef<br>SHA1: 05a61f1952d6f4ec99569d4cd1ae400f1cae5436<br>SHA256: 6e77f17eb1d31536ec35e17ffe04e2e660ad0ea1f6ccf272c645ca52d6f07598</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>153.0MiB (160.4MB) – 1,638,552 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c835574aced45f552a4a3cfbf978c93<br>SHA1: 9233304c254696cd782b65c774fc3b27d5d32604<br>SHA256: 29d13cd33dc1e3d8d04c0e403637c6989dc9677cc31e848830adcbcc34cc72d9</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>157.3MiB (164.9MB) – 1,638,552 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 392ea4090d354263f94cd6d631ed7cc8<br>SHA1: ac9906888f6180855c9e8689ddcf1ab7fec6171e<br>SHA256: 5db54b7333432283deaaa9baa1d544208aa91740f1b4230bc30d088ee86777ae</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>151.4MiB (158.7MB) – 1,638,552 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1c9bb5424539fab7fe724fc26f4b16fb<br>SHA1: a8c0341bfc386c9bfc7a46f07eaf8868bd9ecc12<br>SHA256: c6072411254e77262a058cae74106f460bbba53db52cb8a31148fc3ed74433ed</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>151.7MiB (159.0MB) – 1,638,552 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e307f06a278ea040c235f72b2a7a2f2a<br>SHA1: 82890d1cb5312fb439645330931933facc0981fd<br>SHA256: 23ed0ce7672b456b7b4d5a471b95a453bad67a46bddb1dd3868e86f56bfd7e3a</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>166.1MiB (174.2MB) – 1,638,552 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3c17a711baa847d1791a361c1b5bf5d<br>SHA1: ca4f8cf74901bdd162c30077624ece4af8c8c681<br>SHA256: 2545344ebf416fe4206593ecfcd632767c5669870882e03b6414380e3a6eb5d1</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>151.2MiB (158.5MB) – 1,638,552 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3608beb61155f36bfb8103f868adaa9c<br>SHA1: 0d1320bbbeff1ae6aa204b2ab7e37045d6ed0684<br>SHA256: 623df4fa5f4ef9210fa93529043fa69c6ea4e06c51c563fbf521cfbb6c5c3273</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>169.1MiB (177.3MB) – 1,638,552 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 676d89d5662d35f0e353a3135c804bb2<br>SHA1: d4b2f3a74fe4113b32f44184f1946edec2248b36<br>SHA256: 8b5f31344b661c6b74389297d8f93e85c56ab2daa5eed3e6e4fc544c7497f42a</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>156.0MiB (163.6MB) – 1,638,552 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56b6a802807d0bdcb0f79acd96e52a12<br>SHA1: 0fc6344fb990ae3d3e8d18c3230918dd041e250e<br>SHA256: d0a9e266d74cb17fbe8e085bfded68197730988c4a649230fd7debc1ba81c741</pre></details></small> |


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
