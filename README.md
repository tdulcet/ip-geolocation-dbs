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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-05-22<br>IPv6: 2025-05-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.240MiB (6.544MB) – 312,498 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91ea3925dd59eb7dfeacc691865ff606<br>SHA1: 746008480c58878e87d9b6fa21c54ce52bd8a846<br>SHA256: 7cf6a40d66c81b4d08798500081f65ae8d4407f7eedf08b414eb88da85494349</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.23MiB (12.83MB) – 185,898 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b593c4fede9eaa5c2a8f4060569ed44c<br>SHA1: 2e3883849a28365b04317ffe7e0a86386cb7747d<br>SHA256: a86f5102c9c175822cc1a23881812e99a7358ea24740b9f9caa038400e28f4d4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-05-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.90MiB (13.53MB) – 645,706 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a57e7d2cc83a201cda3044e119397d48<br>SHA1: 1bec44de414f3589313053465ffeedb39ddf1344<br>SHA256: c3456f760aac6f97f2f600334040c3312408c20bdcb1d587fc63a2654eb9e62a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>100.6MiB (105.5MB) – 1,529,205 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2387b4fcdcf658d216f9602de5eef74a<br>SHA1: b7b88108b0241542e46e46c8ef1ff5666f39f06b<br>SHA256: 9e0c38b5001d8479f0210d99f274288d5a5497a1bc17fba36b777c3767b61a9c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.057MiB (7.400MB) – 354,084 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29dc016a76e5d1ce86f281b6be610e8f<br>SHA1: 91c6b4652acafb63416678a1a40d09acb733d81e<br>SHA256: 8c2e1dc4bcb582e63e3cf9a404cef7bbda49da95853a250d12f056cd6e928998</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.75MiB (18.61MB) – 269,749 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3faba08113ae8afbe0f9aeb0c0bc4db1<br>SHA1: baf9d49de9c133023e8e928090c9f50a291301bc<br>SHA256: 126f6ef6cfb9616fb3631b757bf8a7746130d673be4019cc177df52967b9cdf0</pre></details></small> |
| | | Full Location | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.7MiB (197.9MB) – 3,293,979 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc252212886dac7c40089289aaf5a71<br>SHA1: 67fd9db8ecf45ba433418c2361c87e2627dc8c3e<br>SHA256: 6fe5f2b32b1d809aac5a716539f4708f61c901ddad9c02b4ab613c7e262ccd06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.5MiB (412.6MB) – 3,819,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14c6250f6e4e959f775581c56c6b0abc<br>SHA1: 77ffea96762cadecd4cdca9183084900fec55cb2<br>SHA256: 1bc149f9307004c4ad7c60c0f1a25333a23792c5d431b1b374511792cbfab474</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-05-22<br>IPv6: 2025-05-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.968MiB (5.209MB) – 248,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d089ecb129beaeaf2a0c4ac1427eaf6<br>SHA1: 3b494cee2f0d5a67c96e8fd9ac320d9451b36a7f<br>SHA256: cd40baf1649b683953823e24dacd7a02626143eb798e879807a24d509beef71e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.24MiB (22.27MB) – 322,743 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beb56e4b585711434b2fde993d168a9c<br>SHA1: 55d2015800e048a7089193a246f2d5b1249d4440<br>SHA256: 9d5dd5a77dc590c2642e0f671432b7bf9450c4d0347d15a7d904c0c0b55c8ba0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-05-22<br>IPv6: 2025-05-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,019,379 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a68d931a9c3aafbbfc0ff557db9889f<br>SHA1: d3c7b6a63aa399a3a3bca849a9160e65422ac12b<br>SHA256: a6f47823a7140f643c6df5dbe10363559d6998953d47e61148fa9ce21dbf44bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>244.6MiB (256.4MB) – 2,371,820 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db0839b0b336b2cf8a46e6bd46836924<br>SHA1: fe99a8305efd24139243b32063ad92bc72cf9fc3<br>SHA256: c7e0b4a9c07317086b1a652dca4b3928e1bcaab9d1faa273e38c74a68ee151bd</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-05-20<br>IPv6: 2025-05-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.81MiB (12.38MB) – 591,321 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2c33265f44c88abedab4a0851b0b3b5c<br>SHA1: 6c92933a0ad04e1e7e55b1eb55424912ecf24587<br>SHA256: 36e1106b3dee00a9d88c8b39ea7a006766738e8748533c0c6eaa5ce5291f86ec</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.28MiB (42.24MB) – 612,151 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c8bda662c1bc8ef469b50f39d4a021b<br>SHA1: 7af45c1d81d39852a953f5fe428b5a6284765e37<br>SHA256: 5ab3792f6f40620aa5eecb3e4420cbe29d934342946e641be46c3365045e5cbb</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-05-20<br>IPv6: 2025-05-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.3MiB (179.6MB) – 3,379,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ebf033d39a39b4a695de569346341181<br>SHA1: 071e26528b32f08a84f83dc3271a65b059149dc7<br>SHA256: 94efd28ecdbe3c727f3b296a06d8d2ba1d6c787d9134d5ecc48b4d1a806f335b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.1MiB (190.9MB) – 3,379,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afcca26a7d0dc5bfc3c020a5c279fb5e<br>SHA1: 49b1cd273fc036bd403e6653b4815e113a0c08f1<br>SHA256: d578728b89d7b6d68a0810c36bec1b8e041350299409ad99f440ffa7fca87de3</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.4MiB (178.7MB) – 3,379,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6ae3a57eaa7e076fa8d48867f47eb30<br>SHA1: fd59458fe810d1e16d0a0043d7cb1c8062586203<br>SHA256: e3fce6572eb758b08da8b0268cff78ff24075150c65d9d4d109d885030235737</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.0MiB (181.4MB) – 3,379,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd55d8bca38bd775b6713f0774827db8<br>SHA1: 6af14d3dad33bda17ee1b5440ae3f9bdabde8fb0<br>SHA256: d5c47fdd149b1942ff8918e9418368e3ad9d15b7d2898dbc360a5d0bfacce170</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>216.8MiB (227.3MB) – 3,379,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63fd8e723fe7fd0e4cb880973d2f862f<br>SHA1: bc282f0cdd5d94cb1404f447a759e8ee4825f78c<br>SHA256: 6e8b66e6ead9be48a1fea94bf8a32fbbd984b163032bc914423619fc82463aeb</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.1MiB (178.3MB) – 3,379,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efb09d6c866a7a270768d2590e6fcd0a<br>SHA1: cd08afa09447eba7257ad56d77d6ef849726af04<br>SHA256: 93a590ae705123ab5ca835871de2a5c5ad37d2f737ff3fd0c6642c8b6289398f</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>210.7MiB (220.9MB) – 3,379,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d49f1d44d5d5a8c5f201d70184c2576<br>SHA1: 56e306a93a4523011d907b35c7c66e57bd8d63cb<br>SHA256: 3c9fb9b5c56b78b8a24efe53283ef06d099774463d6acb6b00e2f531c0be3ada</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.2MiB (185.8MB) – 3,379,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 202f110eba689857dbc2cf58da8cb4ce<br>SHA1: d3a9512080270550003cf1555adf5f1235ad2085<br>SHA256: f741c276047b5b5731c33a97bdd95f63d67939c1ef6f5434d91375379c27358e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>175.5MiB (184.0MB) – 1,863,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa455364c31baa1564024dc1b80323ea<br>SHA1: 7495320d7e647133c489aa43d188e40a2e24e7c7<br>SHA256: 387b0f7fc7c90e95087cd516b61f48ea8f2114d3f8cdc27db7aa676d5f99d220</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>179.5MiB (188.2MB) – 1,863,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e1fbdea39f3daec0a6b128cdd151445<br>SHA1: 5406787c76821b73a544ae6113a29bbd3458303e<br>SHA256: 93cde0f9d2a24ebb6b0c4d394cbcdf3c254faabd3a9511a0e4488e5359c1e834</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>173.7MiB (182.1MB) – 1,863,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76dd5e3040625570e24ab9b1710cf79c<br>SHA1: 0d462e895706ebc1eb882f5802d2d6ab4172cb5a<br>SHA256: cba8a8afc99bc71d4a90d2550ba416779df71a3a19aba99e903bbbcfe33de9e5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.9MiB (182.4MB) – 1,863,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1dac3a9a38b809a8ce7c0f14ab243f0c<br>SHA1: cfaa4e8192533a00d1d4815509470f3a99da9e94<br>SHA256: 87ee34668307e0c7897109c5b06bf475d2af3d64b46544322b7cfda15564f053</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>192.2MiB (201.5MB) – 1,863,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4527a626d4cdfd785cb16ad3648465ad<br>SHA1: bb783ce882def052ecf953e19fd435a07f384ac0<br>SHA256: dafd45f818e3b163fdb56c4aa4c1955e6535a8ae670c044017ad738a376dff22</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>173.4MiB (181.8MB) – 1,863,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 623e75c5b002b70e73d8b797f8825c0f<br>SHA1: a9fd8cf16149ff2d929f2642f7199eb98c483081<br>SHA256: b036b49dfe5150521e8f3cb568b174bb5f1be70b0816cb03721db37068a6de41</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>193.2MiB (202.5MB) – 1,863,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a318dea01a2a0fb8569f77285668ec2<br>SHA1: 1a8695307c0392b0ae7a18892563366b7d4a9dac<br>SHA256: ee7c1695891bf163476e1a73dd6cc25cd565ff3e727481564300b8f041506e70</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>177.2MiB (185.8MB) – 1,863,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9c3e747e45a78fe78d9c61802de882e<br>SHA1: 1bbc3c1c0bcfbdd0c3efeb8ac3ee8678154e5aed<br>SHA256: eb3def48c1e74f18de4fc64418e24df2b15883aea101f9cf67de6068f5120f92</pre></details></small> |


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
