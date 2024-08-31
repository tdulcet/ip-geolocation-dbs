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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-08-31<br>IPv6: 2024-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.756MiB (4.987MB) – 238,056 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa11c5d2521f5926f7711d60cb669002<br>SHA1: b1194f47679bf07e01b17052eda11c3d98f11877<br>SHA256: a93ce6ca99365e2f8272f77addd82613a357b4288151176148bfc87ba2065199</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.833MiB (6.117MB) – 88,646 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fd398bb531115786c1e47b52a166477<br>SHA1: 620c99d9f6c7d4d56ac50872019673200d7e1264<br>SHA256: 3ea56723109753a1081f747b0ab43b4518c3e863e4ee533edc6bd7eae774ec82</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-08-31<br>IPv6: 2024-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.145MiB (8.541MB) – 407,910 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ac641d680c6c418fa00228667af6014<br>SHA1: 55d7ea500d6fba8bbf5c452f2d80c64fc3f61ac4<br>SHA256: 3c37eeabcbc880e0454243bf4bd42f94c8ba711cdb3eda915c021fdf96a3f969</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.690MiB (7.015MB) – 101,782 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c909cc64d147e7300e15fd1f9c7cf736<br>SHA1: 74b753afaed8851ce6ed606a1b2ccb22ff015195<br>SHA256: cc9f3775cf48fa8ea33514bf672852fb8f98af5c41cd832fcb47796e781769a4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.88MiB (17.70MB) – 844,811 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bad58b6230c8054554f541919a31921d<br>SHA1: b0ebb7164c525f1851d5635f6d9be1982765656e<br>SHA256: 74e9bde1f49aad8e084aaabf7fd1fbc95bc846deb5e52b606b77db55618c9768</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>73.90MiB (77.49MB) – 1,123,065 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09daff544afd489072d0bc4798161155<br>SHA1: c9f401cdbdbe60fd57bf13dca11f7c294c637eaf<br>SHA256: 8f9b2a68fb0f8b3ecf72c9162dd1220cf5b45f86d2066e622ad36633010f6d83</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.930MiB (7.266MB) – 348,283 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0fbc41bc5bb2b90a8e0d5e5ce544a9e<br>SHA1: 1e8f1c989a09bda0597a4fd20bb1baf0e1ac7146<br>SHA256: 5ca608bc0834afa2ddcddbc57debfbc70f177637b74991fa1f5eac6b4004250c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.13MiB (17.96MB) – 260,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d830eaf780889ad98001bab48d5aa45<br>SHA1: b197b3368dda5c090062b0f952b463dcc36089a0<br>SHA256: c9b5f78bc10fd064cbc6e77285c497db8377b1d955acc23e6e6498b158cf6e7a</pre></details></small> |
| | | Full Location | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.4MiB (195.5MB) – 3,254,855 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a701f04a73cc8f80f1d62d7d31565c1<br>SHA1: c08290366ff76b789e82bc1d59e49f3a8b096083<br>SHA256: 05ad2982bf2f1253f055b5d985d376d16bb31cace83cb242d464f0595b931ab4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>351.7MiB (368.8MB) – 3,417,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e978ebf3bde1f974ba0a4b6532bcd5<br>SHA1: ce0a2c31a0c136ca457da29799b4d9d902203525<br>SHA256: 04b7870a00431ac40aa31592ac986f30dc8fcd0035a95ab9beee69df67b812b1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-08-31<br>IPv6: 2024-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.942MiB (5.182MB) – 247,345 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75be5fd9df21ddbc1fdbffc757c5c88e<br>SHA1: 617600a865f99d7027bf00861f55ec2f8fd1574e<br>SHA256: c577e4648304b379620b9b9b1a7b46685fe2b5a3719de872d7565971b4f67dd3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.43MiB (19.32MB) – 280,024 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 529fb8698467082348344b270ff7cc32<br>SHA1: 5e3253c77897a6f1833518163500372c619862fd<br>SHA256: 9289075bcac9e9a959f8009c5eae593e88bd3925aa371f097f4b54c6bd5bb9ed</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-08-31<br>IPv6: 2024-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.5MiB (182.0MB) – 3,005,655 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50ec8daacd5cafd5b2765884871d9b09<br>SHA1: 889e86b248ea9a4741e8399a0e67d17ad637cc38<br>SHA256: 5909cda69b8afb1da39fd44d4e35827b08820512a824be3f438aeb08bfbe1c67</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>210.3MiB (220.5MB) – 2,035,716 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 221fa2afd3b2e737797b4dd7b49d116b<br>SHA1: 42a7d10f6dcb092f867344cabddb6856eda16b19<br>SHA256: 138f90080a7371e27aaa532721e6449e41511cbca7244a5e31fdcc4081b48129</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-08-30<br>IPv6: 2024-08-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.792MiB (10.27MB) – 490,527 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6d9dacca13cf541a4e1a1906d0e9181<br>SHA1: d4b4cdb215e81df273ac93e1eeb845391827cb01<br>SHA256: 93ba31fea2a3d47db7ec5072e2048a3b537e6f5693ef40073efbf1f784b6452e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.28MiB (31.75MB) – 460,214 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3503c0eb3509c0214ff3699ce71d1cd5<br>SHA1: 31b4877288843e0d64b4cb8de849fb994c29b3bb<br>SHA256: a9f587181c488de998fc428e4237de551c3125ce877665f79b9a7e3039dc3a6e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-08-30<br>IPv6: 2024-08-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.9MiB (126.7MB) – 2,417,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36c9ecc2b0bbb42a5438d4d2407c0494<br>SHA1: 94d2f84650e92013eb021dea9309d74d4387a734<br>SHA256: 15636892b7015fc8f7e0bfd16c2e4a2bf3106ebd36ad77a2ce1d6d1dfac86159</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.7MiB (136.0MB) – 2,417,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bb935317f81d9053b904f0142cadad6<br>SHA1: 8b29502e6c48ed5490a4210700133daaee31f162<br>SHA256: 5f86c170a6bdaa97783501f7ee648a01ebfeafc06468f3ddff6d98e4d20e7c4d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.4MiB (126.2MB) – 2,417,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 678ddf01578e3d8fc1afb76c22374b22<br>SHA1: 05628f6557c298026df858d4aa28544d89042e22<br>SHA256: 2ef3455ebbeca7e39cdb8abdffe87c97d36388272cd8ced7ef41d9be6023a5ae</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.8MiB (128.8MB) – 2,417,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be222f4b7fcd839b2e4782d2c804c947<br>SHA1: 850a71298bf7d73f219bfeb16d4cd5c67989d2a4<br>SHA256: 2ee8bd15d24a2098ded04df547549dd75ca8af6906a031c447d902f94b44d3d9</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.3MiB (157.6MB) – 2,417,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d165406d69824adc0ea262ef634ca27d<br>SHA1: a0953389cd79691ba1c155a1f46233cd516d3bc0<br>SHA256: 0250a3dc1175fac0ce0a7b119ef2aa64f06a00dc6693aa9d35565166723f12bf</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.6MiB (125.4MB) – 2,417,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e24a37c0a729d40e2b4f5606d7c2252<br>SHA1: 74823cce084d325f470a10b175a8a9a17fc5f85d<br>SHA256: 8ac7781f91e695df6e7711f83764da56321f999b295668ff2f44afb23fade462</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>147.0MiB (154.1MB) – 2,417,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d503669bbae3623dd4f3aaa61d0c45a<br>SHA1: 2b7fad39805e0d788b33c3958957000d0a6841f7<br>SHA256: d9a5c31d0484a1f5162867d2305d0b15adc7ce5d9bb6c109f654caa164bf98eb</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.2MiB (129.2MB) – 2,417,280 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f79184f8d280f86110c3d3ecd70495d9<br>SHA1: a731e6c54bdb0bf792ddfedb1f98d78bf7dcafef<br>SHA256: 6f6028a9761e257d26486b1c3875beae0bea1781202584d40f8d3c9206152205</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>150.9MiB (158.2MB) – 1,617,428 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9482c88b560e33979ef1851f7ae2e014<br>SHA1: c64c2330568af404ff7389f96c8a36cbbb9a8b9e<br>SHA256: 39cc2ccb9076bad3a94d04cfd3503e81320cbe401c4d63e047e0678ece289405</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>155.1MiB (162.7MB) – 1,617,428 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5666d7e1c91816eabf80cb12dec903f<br>SHA1: d0cf767a7dac20077d32cc26ae83b061934530be<br>SHA256: 0c36952a998782d799a680a179ee6ae91d28d12d09163142f573f760498955dd</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>149.3MiB (156.5MB) – 1,617,428 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d919217f677578860b9ae7e2ede60b20<br>SHA1: d17784e34ec0d510a388319be37ec0a39bb5e34c<br>SHA256: c25c2dfc552adadc3795d1c3387da6db11975721a8a9e54da84fb8094e80fe21</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>149.6MiB (156.8MB) – 1,617,428 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6c939d52c4ffa0793ef4039c11de4cc<br>SHA1: 7164ff8985f7a99159766ce31a783808be256e92<br>SHA256: 7ae91569fabca39cdf77cf00ec2a47a6877663cdb259c57bae150b3364f0e836</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>163.7MiB (171.6MB) – 1,617,428 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2cde4972ead1cdf71afbed6d8dcdd5c9<br>SHA1: fd7607f2c0717753fa04feb0cb7006bb9bb23aa7<br>SHA256: 7708c74abfb15d61507ba72b6ffa1310c260f6c97104a51ed0ac8ceec94203b5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>149.1MiB (156.4MB) – 1,617,428 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16ca574d1d1a4d71b9e7fa6acc1d4f96<br>SHA1: 43a62eb41308ee0cf494b65848a7c840311ec61b<br>SHA256: 535b2e344aaa44e5e5735c1f2b92fc7cb7c049844b2b620b91ff8d2220230a1b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>166.8MiB (174.9MB) – 1,617,428 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59ea47fca9e4cb5bbed6957792656b7f<br>SHA1: d0830ccbb53165b97e9c9e71280a0f33d033398e<br>SHA256: 93d1b3932eee595cf62200ddb5e419f0c80a642bd4c3f83fe793169f4a7c7c99</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>153.9MiB (161.4MB) – 1,617,428 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a98710192b763a603e6813cfe713dea1<br>SHA1: 54a9baaf30d64e7a2f3008631ab9b9c30b92ef27<br>SHA256: b5622257762bbb0bc24fffd0eae7ca71757f389932af10b9ba6f929ed0eb06c0</pre></details></small> |


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
