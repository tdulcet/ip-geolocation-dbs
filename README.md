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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-08-29<br>IPv6: 2024-08-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.756MiB (4.987MB) – 238,085 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b122b8eda63daa876df66a85800e3fe7<br>SHA1: e03aacaca21c0f5ea3d8515d3f59deab8f909cde<br>SHA256: f2b6b204aa17ba1363f9c3f8aa42d6c9181158778106073e614c6342c51b34ef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.827MiB (6.110MB) – 88,555 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a947130b5ad2518882c78d164cb47490<br>SHA1: eda943715cb85b7800889c6bed482fc4f1b139ae<br>SHA256: 2de58fd7e625b29339f393ff946a92f2dbd9da7b9ae13bc9fe7b7148fa70b7da</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-08-29<br>IPv6: 2024-08-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.147MiB (8.543MB) – 407,985 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c0fc19f973bcd25f13cfa639ca401ac<br>SHA1: 0a81be5e1bb7804d65772e9cca11345ca906df3c<br>SHA256: adcd8ad5edd391a7bce828a0981130bfac5848b8c246e74dd253fa1de57f53f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.687MiB (7.012MB) – 101,742 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c1045a8b542cac7d78a36912793cf8f<br>SHA1: 1df423748139a50e21fdad021cc87c96b6c72ec0<br>SHA256: 6a0f8affbf5c86f4807fc26405e19e27b14a7e95b5f2b83e8f5bb170be8633b0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-08-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.03MiB (17.86MB) – 851,887 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59728a92b477558a9214cfcd982dbc1e<br>SHA1: fe3dd8b7763bb8328f5923c1319f26eae82f7406<br>SHA256: 106ad3b0da4f2107afc7bda2f4cc55d396aeb4d76bfe46a76ef6c89e80e8e9b8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>78.12MiB (81.91MB) – 1,187,114 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 325e547827db30029f12e31dff032236<br>SHA1: bd44791371e37df09198ddde17566000904097fa<br>SHA256: b61215599493cae74f3c63d5eaed2257b19ed298a8423ea300091af95d1344d2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.930MiB (7.266MB) – 348,283 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0fbc41bc5bb2b90a8e0d5e5ce544a9e<br>SHA1: 1e8f1c989a09bda0597a4fd20bb1baf0e1ac7146<br>SHA256: 5ca608bc0834afa2ddcddbc57debfbc70f177637b74991fa1f5eac6b4004250c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.13MiB (17.96MB) – 260,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d830eaf780889ad98001bab48d5aa45<br>SHA1: b197b3368dda5c090062b0f952b463dcc36089a0<br>SHA256: c9b5f78bc10fd064cbc6e77285c497db8377b1d955acc23e6e6498b158cf6e7a</pre></details></small> |
| | | Full Location | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.4MiB (195.5MB) – 3,254,855 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a701f04a73cc8f80f1d62d7d31565c1<br>SHA1: c08290366ff76b789e82bc1d59e49f3a8b096083<br>SHA256: 05ad2982bf2f1253f055b5d985d376d16bb31cace83cb242d464f0595b931ab4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>351.7MiB (368.8MB) – 3,417,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e978ebf3bde1f974ba0a4b6532bcd5<br>SHA1: ce0a2c31a0c136ca457da29799b4d9d902203525<br>SHA256: 04b7870a00431ac40aa31592ac986f30dc8fcd0035a95ab9beee69df67b812b1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-08-29<br>IPv6: 2024-08-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.983MB) – 237,847 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a19f3b324b30f1b8e58614ced6c3eb<br>SHA1: 0ae869a9dcd1e992112ca1f19381c40b51f06f2b<br>SHA256: 16ded9b540a430569f72a4e9231fd255fdabd1dda07b4b19d35f69b1de8705a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.46MiB (19.36MB) – 280,554 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48429e636d89243b95e58e224ddcab83<br>SHA1: 62476d74b99370f1cf7032a405e741d78678dfbd<br>SHA256: 0cf7afea40b0dab546ce14724386b222921daeee0d831eecb913854ed7bdc0f0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-08-29<br>IPv6: 2024-08-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.1MiB (180.4MB) – 2,980,631 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b3e4b34496e91b79950bfd2ba90c64e<br>SHA1: 65cd184136a3ebc843b8b661eb3d7e435d8e169b<br>SHA256: 8fe209a185d5393cb91b8ddc3d044e30a9bbb3dfd9681ecce9b281cc7e030387</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,986,964 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf91d149bffc17e272f874de287e1a0<br>SHA1: d7fda16f424fa431e16b71116da2588052e905e8<br>SHA256: 28d426aa8fadf9fdb6308784807383ed47871f07d6c9d66d67e14bc55327d0c1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-08-27<br>IPv6: 2024-08-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.785MiB (10.26MB) – 490,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eff5bbdb447417192ba7903ef765ec0<br>SHA1: f2b0c58bce8ba03d671bc5f568359d91289292b7<br>SHA256: efc9f397946db91a848f8d877cf9089a9b236deab2fd44b3622aa623cc692e94</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>30.27MiB (31.74MB) – 460,035 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea9d5d8d272af9db716c735292e8a8e8<br>SHA1: b79e4981aafa6367215bb4294c5be79c9f162a88<br>SHA256: 489f92ae76255b32d433802210b04c3db83e4e95dd5bdcb9d3231977f897d75a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-08-27<br>IPv6: 2024-08-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.8MiB (126.7MB) – 2,416,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7305f29526576069bb5263f1baa0a8e9<br>SHA1: 8c78a72b17caefd045f5b975d2a39677b0f7686d<br>SHA256: 1cf9ebdec99ef2e5cdc5acd004ce552a5267f3d88efb777257816ccb3110dd71</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.6MiB (135.9MB) – 2,416,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c89e3839717d9d24e380fd66b8e6fabc<br>SHA1: 304a2f714a6c1461151144e265bebee506c8e0f3<br>SHA256: 9ffeb51c9bec4b1c6680390d87ad5807ee9758951dd374611b19142915cc12db</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.3MiB (126.2MB) – 2,416,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e5f00a0ad2a693ab0da6ae07e91e184<br>SHA1: 4d86bb67d9ec5c0648e9e456292a0dbf32e764fe<br>SHA256: e6cafa3e3d7b1e262d013415f599e3c3e36301d8c1f2475dd54393d048951478</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.8MiB (128.7MB) – 2,416,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85b5fdc1ccd14686dd8aa9962a245300<br>SHA1: 0c1b067e70fe674c5668b4c658926b6d45141588<br>SHA256: a6ef0bc67d848348a6d4ab8cabe0249e89f8a5b5bc5a3ce35719c361f624921a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.2MiB (157.5MB) – 2,416,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a952205c31d59c6cc49526ed59e6765d<br>SHA1: 24903e26589d82e6edb207d8ea06a53f75967dc2<br>SHA256: 4f62cad4893bf97f0fa35a71367e2a453a7c390a9be5a76334fb2e13e5ea9f5a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.6MiB (125.4MB) – 2,416,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5edfc8504efccb12d19200a4f8b3fc8d<br>SHA1: bf24d252767ab16c66a8bd671dcd15c9d8a39bb3<br>SHA256: ffcdf5eb9bd001437fafbdfefdade374502bcc839bd73c1bf9ba43dc4bccef67</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.9MiB (154.0MB) – 2,416,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77418efcb1d3ae1674276ee2ca049583<br>SHA1: b3817957a65fd2b7b2a5f5f2f415d0cfb3bdd0e9<br>SHA256: bb958158f481dc11debe9714631e0b7b74af0879d455e37258bf84b303a244c3</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.2MiB (129.1MB) – 2,416,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a52f3b3516be41fdea5361144b5a93bd<br>SHA1: 181f6557fe9a9d32455fcae2f2e91d2644ce0c85<br>SHA256: 27ff2a130c6d0b1f8f6a658c081f4eb8e1734dc206cecb38fa65eca3e0d78807</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>150.8MiB (158.2MB) – 1,617,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228eb2519f3cb9ec61ffa09b79f809b<br>SHA1: 9cb7e70a34005123843b657e150865b7159eb346<br>SHA256: f0c3e11baa51128549f0fbbcc0c5e1b4268ebec190bd77f3b18293b6888ff1ac</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>155.1MiB (162.7MB) – 1,617,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 215064c85b883749b0e992af036d04f3<br>SHA1: 881a0b82806008fb84bad173cdbdd9b7d575695e<br>SHA256: 65d497edb2a2c6452cda0374d2ef80cd04aa01a3af387f3a2e8c4d3806d9c7a9</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>149.3MiB (156.5MB) – 1,617,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5180ad8cbea6542b55c2a8bf02f26254<br>SHA1: 173f0de9aa993080b12d8127cfdf745763504d5c<br>SHA256: 6ac374b61fb9d71227ae1df99cf976e569929b14aab30673a6f9805e82f93927</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>149.5MiB (156.8MB) – 1,617,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 941a49dcef810ff2b52b72b44c0a6fa5<br>SHA1: 1fa4adf964961f0f3d34c7409a6a9157b1904fd5<br>SHA256: d6672c461ecd3e6fe6e809b4e76cf621a1d76cd190a42f160d9e83b9b6aabdf1</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>163.6MiB (171.6MB) – 1,617,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd3c17e8673b10f2f4a0dad160fef33d<br>SHA1: fefa7ee9332b6a581f4cd3fd10b3ef34436fe558<br>SHA256: 9491c54290d8e20ec6690a44077e6cef9972e099717d462e66e296182c427bda</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>149.1MiB (156.3MB) – 1,617,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f783fbb0bcfa66e5e3df2ca54f5422a6<br>SHA1: 2f6dc55473061d5e900044b20dc62625d73f8f48<br>SHA256: 2321700ca8f7c1cff2dca043af60f127fad7b184b8e11b3c7423f974eb636ea1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>166.7MiB (174.8MB) – 1,617,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4bf4fe8ca6cff5b5dd6d37385b333cb8<br>SHA1: 7ef67a68324b91e7fbfc6d10df16a6b5a41f39e0<br>SHA256: c5d7d6cd68eef3d28cc30b6ced69a38693bac8f51af0d22b55b9a8ef32c01ea7</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>153.9MiB (161.4MB) – 1,617,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd3cd116ba06eb1e4a97eced8486bbac<br>SHA1: dd6435cd74b9bbcb4b8d9a709a342d829b4fc25a<br>SHA256: 659e700953c526b45e14c27c307bcca4e5a3b20b401928c886cfadd688d0e70d</pre></details></small> |


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
