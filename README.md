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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-08-27<br>IPv6: 2024-08-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.758MiB (4.989MB) – 238,161 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32ab27bbdb15597bb6a7de033a2aa2e5<br>SHA1: 29e031ccb65e8b3af16796d1a13d6de0729841dc<br>SHA256: d10f92048c681d92d951657050c1a7e0fbb4780410e7690670f8b7cf126681de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.830MiB (6.114MB) – 88,604 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a35364dcd5cf86a212f910b1b616cb71<br>SHA1: a675d29be9f8d77d5aec514e727c119d2dbfd0f9<br>SHA256: 06aa55114b9d7b81eaeabd18f3b1c5c0a13d24f57e7dfeeadf7b68b5304d8411</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-08-27<br>IPv6: 2024-08-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.139MiB (8.534MB) – 407,572 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3a80d50eaf81306b678496c0ab75ea6<br>SHA1: 83d000717168605f394979089fb522be3ae923c0<br>SHA256: f610d018bfac809ebf3572bd01d2d4d898fbfd2392fe20c317e9a33b71de1c9f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.665MiB (6.989MB) – 101,404 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 853f53818597fad6c308922a24a78401<br>SHA1: 9c0f2b0013a8b419bbd02d5f824078d920627c91<br>SHA256: b0c570573e9e91b33e52ff9775c9454648e90ac0516f531bcfba23a31191a6c3</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-08-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.11MiB (17.94MB) – 855,745 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7cdac5364cad199bd860f8c050cdeeb9<br>SHA1: a913a57217fd768853aa60586344e9dc8383da25<br>SHA256: 460ef7cc46213897f790983e26b1191ec4bb34a47e5ee98878d5ec85431fd671</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>80.27MiB (84.17MB) – 1,219,857 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71f69ee3f2f7528663b3443ee8c5e3a3<br>SHA1: 7ca9db848aa7f59d07cc005ad45502ffdee7e9f5<br>SHA256: 22eb092c110ad2bfb4aceac48f770989c05a21bfedc44120557112b7e15e3d09</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.930MiB (7.266MB) – 348,283 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0fbc41bc5bb2b90a8e0d5e5ce544a9e<br>SHA1: 1e8f1c989a09bda0597a4fd20bb1baf0e1ac7146<br>SHA256: 5ca608bc0834afa2ddcddbc57debfbc70f177637b74991fa1f5eac6b4004250c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.13MiB (17.96MB) – 260,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d830eaf780889ad98001bab48d5aa45<br>SHA1: b197b3368dda5c090062b0f952b463dcc36089a0<br>SHA256: c9b5f78bc10fd064cbc6e77285c497db8377b1d955acc23e6e6498b158cf6e7a</pre></details></small> |
| | | Full Location | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.4MiB (195.5MB) – 3,254,855 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a701f04a73cc8f80f1d62d7d31565c1<br>SHA1: c08290366ff76b789e82bc1d59e49f3a8b096083<br>SHA256: 05ad2982bf2f1253f055b5d985d376d16bb31cace83cb242d464f0595b931ab4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>351.7MiB (368.8MB) – 3,417,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e978ebf3bde1f974ba0a4b6532bcd5<br>SHA1: ce0a2c31a0c136ca457da29799b4d9d902203525<br>SHA256: 04b7870a00431ac40aa31592ac986f30dc8fcd0035a95ab9beee69df67b812b1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-08-27<br>IPv6: 2024-08-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.983MB) – 237,847 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a19f3b324b30f1b8e58614ced6c3eb<br>SHA1: 0ae869a9dcd1e992112ca1f19381c40b51f06f2b<br>SHA256: 16ded9b540a430569f72a4e9231fd255fdabd1dda07b4b19d35f69b1de8705a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.46MiB (19.36MB) – 280,554 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48429e636d89243b95e58e224ddcab83<br>SHA1: 62476d74b99370f1cf7032a405e741d78678dfbd<br>SHA256: 0cf7afea40b0dab546ce14724386b222921daeee0d831eecb913854ed7bdc0f0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-08-27<br>IPv6: 2024-08-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.1MiB (180.4MB) – 2,980,631 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b3e4b34496e91b79950bfd2ba90c64e<br>SHA1: 65cd184136a3ebc843b8b661eb3d7e435d8e169b<br>SHA256: 8fe209a185d5393cb91b8ddc3d044e30a9bbb3dfd9681ecce9b281cc7e030387</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,986,964 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf91d149bffc17e272f874de287e1a0<br>SHA1: d7fda16f424fa431e16b71116da2588052e905e8<br>SHA256: 28d426aa8fadf9fdb6308784807383ed47871f07d6c9d66d67e14bc55327d0c1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-08-23<br>IPv6: 2024-08-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.756MiB (10.23MB) – 488,748 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a33008e27579e518bd083841d962b18<br>SHA1: f47acbbfb5266cb6c7a00ad1a8567e82b5b704f2<br>SHA256: 6e8051eeb78e6e1747133ec8ddc07ec9e6c6baa9bf1cac04a0ecefabb146a638</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.04MiB (31.50MB) – 456,491 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac09d40d164f80ff52cb0c41e7f7ad9f<br>SHA1: 40ed0fb1b0b74d9981d9c0101f748fe723a5a5f5<br>SHA256: dd08493a2be7c9262d6ee121c4cb176ab352e65730f9d0874144ae412fa937e4</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-08-23<br>IPv6: 2024-08-23 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.5MiB (126.3MB) – 2,408,617 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 286b158acdb45ae8a991ffa0293ce1b4<br>SHA1: dcd1b39866835637f5561998812b33fd2043cedc<br>SHA256: 806d44cd40fbab5bdfc69a30341c2642d00c64116253c32f681c118eea39ca1e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.2MiB (135.5MB) – 2,408,617 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6377b38d3c0621cf14e9043fb41b403b<br>SHA1: e9d2a75d17bda69570300be2a1b2f94a4e9d5910<br>SHA256: e47c52ea862d236d1f71c2e1ef0fc5e9a0470a90ed44fb50190b1b610f86d0c0</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.0MiB (125.8MB) – 2,408,617 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7404994cc9229d1b506f8f498d6baab<br>SHA1: 5a00a2c3c7b8df49e60bf7dc570804886771c753<br>SHA256: 18141d0cfc90937fcbd1cd3f74f7b2d5d14a0561cb5bcc1735fe78c140d496fc</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.4MiB (128.4MB) – 2,408,617 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6e14c5d1cc067cbb0ac6034f550dafb<br>SHA1: c18acf033700045314751b7de57ced9003ebf86a<br>SHA256: 5d35299e95701ef01f978523c120343fbac1306c14d3ae44958f5c68533c6360</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>149.8MiB (157.1MB) – 2,408,617 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14c9901571345fdb736be26c2425216d<br>SHA1: aae79e7288c773f76b8b84a9608bf4999c1a6849<br>SHA256: 8bdb4d395a04e727e4f481adc7d2bf8dbc3af62ab912cb57d3492c40c2ea94fc</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.2MiB (125.0MB) – 2,408,617 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 851bba0490e747c5d21005c803e1060e<br>SHA1: e9eb936802461b53dd926c5e871df5eb6d99d370<br>SHA256: ac5c5fe270b746969e09d6d37c03abf2cb56bc3ee37267f93d10a9531844dac2</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.5MiB (153.7MB) – 2,408,617 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ce9b2c65ad0ef24ee4578fb0d88613f<br>SHA1: cf4f532399b1c52fc3bccc7342f6bbb76fb80c94<br>SHA256: f1bf91edb770fc82c41003ca878353ba537c63de4ba3356118ae2cd2a559d584</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>122.8MiB (128.8MB) – 2,408,617 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f967f605e84243fafda6420bf0c5a19<br>SHA1: 2cc7ec78b9873f766e4a79cdb55315e889ea95c2<br>SHA256: 13401741b269a3bd3ee1b460a98a6122b63587590ccc5477586eb4ae14f1ea79</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>152.7MiB (160.1MB) – 1,635,873 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a62f5db943096c930e5e27414c23570<br>SHA1: e495bb86c1c3a3c210fdd120cb5e365052bb92d7<br>SHA256: 876d1eaf32feba2cb920a3a176591e8bc53331be2213a33ea2d9bf47c233d851</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>157.0MiB (164.6MB) – 1,635,873 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50a084b854ffe5fd4d186b3751057adc<br>SHA1: 7915c8ae3289e37719199d21d7168755721bc226<br>SHA256: 91e49c0413f651bea78976d9b529470e01cc2a1f962a4120c3c4457530d6f844</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>151.1MiB (158.4MB) – 1,635,873 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a7ea3fc001bcecc4c1425459cd138b7<br>SHA1: 8243eda3fc1bebbf7ce1ec2d2d3c98f1e446bbd0<br>SHA256: 734e6993660089b147f018af0b5a1a6919b110e8517250402a6addaa759cb880</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>151.4MiB (158.7MB) – 1,635,873 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6c6918898df3fda207ec83de08eb12a<br>SHA1: c87ad559d68fd27fbfd7ddcca8f8adf46ce8719f<br>SHA256: 10207b19f4c78760698b2368e1c9a602337f43cad315dd1c518f3b41798c8ff8</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>165.8MiB (173.8MB) – 1,635,873 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad5d6247178955f2d3070dc522ac36ac<br>SHA1: e2fffcfbeffe03e0665dc816573f5fc3526f894d<br>SHA256: be94be86f7cd4470ae6252c926b892c9e4c4924ff181a8c5bba59dbbc1f6de1e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>150.9MiB (158.2MB) – 1,635,873 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a550175192e160a99739d3c1472cdc03<br>SHA1: 54d8a6909627a380a275adfeb4052b559a65ba02<br>SHA256: 7b2ee0f440274ebae151a7f7f123cdaf291399075022a812e6696b6306403190</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>168.8MiB (177.0MB) – 1,635,873 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8140d434d2142c7ef3109bf576c9f1e<br>SHA1: ce830dd0ac4567fad613f98f121f160f4cb8a366<br>SHA256: a0a19ed7bec4ffa7ef26cbea1d797180b84955e8369111fea3b8837c5687bb63</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>155.7MiB (163.2MB) – 1,635,873 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb6e80bf76c4bca804b755dbeaa427dd<br>SHA1: e14e1fadc572df84980cbc57291e4b627925d9a6<br>SHA256: c5ba3e08ea638ece4b0fb463a60daf4adcd002b7aa8fe421b90c132464c2cde8</pre></details></small> |


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
