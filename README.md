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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-05-30<br>IPv6: 2025-05-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.258MiB (6.562MB) – 313,394 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9bc97ed7e7b0921bacdf5bedd5ca660a<br>SHA1: dbeb0c691f93597cc6e8028e96773fa825a67c0c<br>SHA256: 1e510c3cb053c2f6002704d005874a0623c2e682783d3c38c3fba5c0fb99ba9b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.26MiB (12.86MB) – 186,334 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f056ec8191fd67ddc5ea3cb9c417fb6<br>SHA1: b52eaf306ba145be16ab30009fac738fb228b71a<br>SHA256: 7e57c475ca8db70cc815382eb0fef768bc85610f2cefb8a92dcfe5fe561b50ff</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-05-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.93MiB (13.56MB) – 647,478 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 364f81feef6b45c515942e767975b720<br>SHA1: e2dbd5261c44904e61557c5baa9049b05d33b28a<br>SHA256: b94f02e234f67a65dd756867c2b4d71db85175fcbe1e54e9e9e6edbb2a3e9a1b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>97.60MiB (102.3MB) – 1,483,157 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3934178e11af5f87d9101d735bbcd8d<br>SHA1: 24e0c4d8825434aa3b5d9d42569b1bff02f0e2bf<br>SHA256: 005221ecab49314a434beabe68484a0cad51ad9fdf4831ec4352fa63b9d431fc</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.057MiB (7.400MB) – 354,084 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29dc016a76e5d1ce86f281b6be610e8f<br>SHA1: 91c6b4652acafb63416678a1a40d09acb733d81e<br>SHA256: 8c2e1dc4bcb582e63e3cf9a404cef7bbda49da95853a250d12f056cd6e928998</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.75MiB (18.61MB) – 269,749 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3faba08113ae8afbe0f9aeb0c0bc4db1<br>SHA1: baf9d49de9c133023e8e928090c9f50a291301bc<br>SHA256: 126f6ef6cfb9616fb3631b757bf8a7746130d673be4019cc177df52967b9cdf0</pre></details></small> |
| | | Full Location | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.7MiB (197.9MB) – 3,293,979 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc252212886dac7c40089289aaf5a71<br>SHA1: 67fd9db8ecf45ba433418c2361c87e2627dc8c3e<br>SHA256: 6fe5f2b32b1d809aac5a716539f4708f61c901ddad9c02b4ab613c7e262ccd06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.5MiB (412.6MB) – 3,819,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14c6250f6e4e959f775581c56c6b0abc<br>SHA1: 77ffea96762cadecd4cdca9183084900fec55cb2<br>SHA256: 1bc149f9307004c4ad7c60c0f1a25333a23792c5d431b1b374511792cbfab474</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-05-30<br>IPv6: 2025-05-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.968MiB (5.209MB) – 248,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d089ecb129beaeaf2a0c4ac1427eaf6<br>SHA1: 3b494cee2f0d5a67c96e8fd9ac320d9451b36a7f<br>SHA256: cd40baf1649b683953823e24dacd7a02626143eb798e879807a24d509beef71e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.24MiB (22.27MB) – 322,743 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beb56e4b585711434b2fde993d168a9c<br>SHA1: 55d2015800e048a7089193a246f2d5b1249d4440<br>SHA256: 9d5dd5a77dc590c2642e0f671432b7bf9450c4d0347d15a7d904c0c0b55c8ba0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-05-30<br>IPv6: 2025-05-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,019,379 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a68d931a9c3aafbbfc0ff557db9889f<br>SHA1: d3c7b6a63aa399a3a3bca849a9160e65422ac12b<br>SHA256: a6f47823a7140f643c6df5dbe10363559d6998953d47e61148fa9ce21dbf44bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>244.6MiB (256.4MB) – 2,371,820 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db0839b0b336b2cf8a46e6bd46836924<br>SHA1: fe99a8305efd24139243b32063ad92bc72cf9fc3<br>SHA256: c7e0b4a9c07317086b1a652dca4b3928e1bcaab9d1faa273e38c74a68ee151bd</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-05-28<br>IPv6: 2025-05-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.86MiB (12.44MB) – 593,911 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e0a60f7599b0db630def6dabcffef23<br>SHA1: f4b4369c607f704e2bb76d7e26e53ecad7abb787<br>SHA256: 872b25b50b152d0353257b669f284b906d0688fdaaee4844b7b6344fb1b616cc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.62MiB (42.60MB) – 617,348 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c444b415b4e2051bb4764f4950ae6084<br>SHA1: be2ccac5940c3a9ac42b5c806f3de17c44e040f3<br>SHA256: 7e0ba72dcadca812ba48a4539c21ff7b59b7339fb566b4b03646a2cc8ff2f9c9</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-05-28<br>IPv6: 2025-05-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.5MiB (179.9MB) – 3,384,210 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f6ecf413034e2414e10846520c0e69b<br>SHA1: ecb73845ab28cee624b098a212d5073212967c1c<br>SHA256: c7e959fb7a665cd77f2fe5295eff069fba60319d7075fc2ca80b77096ea61f7c</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.3MiB (191.1MB) – 3,384,210 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d20c5f09d16b693aebccc9b40409d00a<br>SHA1: 7c7fa0d97817bf195f1b82c1fadc91ff330d0837<br>SHA256: f5a361813656d895bedda9cb44489fa1320521159da5a02606014181e7f199da</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.7MiB (179.0MB) – 3,384,210 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8eb2632aa09428d59b1032551332205d<br>SHA1: aebed739e29ea806a72c7e23501fcec1670cee1b<br>SHA256: af8af5455254e5f32e115fb01685be313004eb8af7cc849cd3755bf26eb7ce6d</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.2MiB (181.6MB) – 3,384,210 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2341cf725890e0aa220cd1e6f086ac7<br>SHA1: 17dc605e3877645ad91e9a79bd25d040ebfd746c<br>SHA256: 7445f89ae4b702670545472ba259732a720feddf647f299cc3559a7467bbc6cb</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.1MiB (227.6MB) – 3,384,210 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0b17450c168927c0da7efd55162fd57<br>SHA1: 945a3ec873d0609900b373aac82ed3f168745e13<br>SHA256: 38841d8e22ff394c58e75272aae5ebf5943a4b703663e899ece50e01f8240079</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.3MiB (178.6MB) – 3,384,210 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f464800beab9eab6f7497f0a88e53ddf<br>SHA1: c27e27fdf2f44eacd8d6bfef0bea7fa6167d4778<br>SHA256: 0f0368f515abc91577be902e8fd7d6c6864f844ec3e67194a973a68da5311833</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>210.9MiB (221.1MB) – 3,384,210 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e50f05385324e10c6fb7eb71dcbcc66<br>SHA1: f3dd066bae63269105658dd26632be3c4debc8a4<br>SHA256: b6e6a5a31cc1297e95fce270c416f9667dda0771048e7abc76c0d8ee4a143e4c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.5MiB (186.1MB) – 3,384,210 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afd8a90b80e50586a9421c14ea21eca8<br>SHA1: 0ae115aae50760b36722082c75055266655b3000<br>SHA256: a9e8cd6a1980bd5d009b3df094f0482267406b1665ecc59deee9ce6cacbb23ea</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>174.9MiB (183.4MB) – 1,858,695 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1dc49aab09a98c2fdffcbc7c477b7e4<br>SHA1: 886414896f8cb30ac9dce9bae28585348b6a0428<br>SHA256: 8650ac92235af866987b3f9931c1042cdc4c477adb218e4bef4a8ae94707688f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>178.9MiB (187.6MB) – 1,858,695 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e3e3d575a382a658836b6ac1d668cb3<br>SHA1: 873e38e4a34aeedb871eaea2982189390ff71078<br>SHA256: e3149e71fe9156678350f8b4937c178dad6ab53d27e37e9bc0d1b20278585829</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>173.2MiB (181.6MB) – 1,858,695 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6b2a70c1dd9ea30c652f216d5f462d7<br>SHA1: 0d399c68af1b46e4529bd0b210cf8a2499370257<br>SHA256: c099bbda612b495214bd8e724ec92cd4e5804c8caea49b50ed8932fd69b81d34</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.4MiB (181.8MB) – 1,858,695 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db7c4fcf412dc8b13dc9f15e65aa1260<br>SHA1: 984b7394c630d2194813433de69600011909541e<br>SHA256: 492503a23fcb1460a54fe49edd7eb549a73fb0202ccdba750c3959242d37ad87</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>191.6MiB (200.9MB) – 1,858,695 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45c2b5309883205b10edabeede0c3da1<br>SHA1: 81512e860990cec8b590c1a71aa0a826dfb35e9a<br>SHA256: b59fc9c7fa5afe63c902b0b6a94fa589467c2115907e000816ca39f8d9b9ca69</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>172.8MiB (181.2MB) – 1,858,695 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe92f0b33a27dc151f29db5919f6cc4e<br>SHA1: 3caf77bbb7f9133b3a7b753a25ff727c41abea5e<br>SHA256: 9569287913f9511c9af64f15a339782950afa0e9ceb0eb54bdf5cbcb46b163f0</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>192.5MiB (201.9MB) – 1,858,695 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56040f196859c388b551594f1a41c610<br>SHA1: f9dd1316075aca50604200bf75c7db222c15df2e<br>SHA256: 3b2e55d2c089365b7dc4e08dfe0819909a7b7b074cb04329c907deefed4a2cef</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>176.7MiB (185.3MB) – 1,858,695 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61b504c34d57ff3659cd0e6592140c11<br>SHA1: 85589b69ae120c79472ba1889302374841597790<br>SHA256: fad9b30397ccee643afb1a89f91282da5c72988895e4fa1649153c8c635b12d1</pre></details></small> |


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
