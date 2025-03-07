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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-03-07<br>IPv6: 2025-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-07<br>IPv6: 2025-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.367MiB (8.774MB) – 418,996 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96c27701e16fc7bcc4a749abe2937753<br>SHA1: acfc1df7f0bb64f56f855b1547e72dcf60d9caa7<br>SHA256: e9cfc5da032f61a5f2edb597f5c35afe780ae04858e5d943a2b49c470d71c05e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.986MiB (7.326MB) – 106,286 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a81a497c4eeb55b065e6ec5e8df6ed0f<br>SHA1: 54bfffab4ce4b11a448b9dd3fb98384fc45e70b0<br>SHA256: bb8e7aa2c3271d95bc597123677f3245441d94bd690e01d7227778ac1339e1ba</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.44MiB (14.09MB) – 672,909 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c377958478105a101c1ddde87a53d58f<br>SHA1: 9adb98546f3636fd3434372ec3682bd4f8c35437<br>SHA256: 1f742482549522aad46f6caef1ba5a12fc291a51da7e3688de11d33708d48fe5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>71.39MiB (74.86MB) – 1,084,905 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2d75981f63415c5e04ee54472efb09b<br>SHA1: d008c27e0420006acab8265a31d65a1a0bc72de8<br>SHA256: a9b274be3d330736b5487caad2d3d79094154600cfb9f858af8855c8901e515b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.404MiB (7.764MB) – 372,055 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e5911df23fa4121906510a5a567b13<br>SHA1: 9325bb0b20fe7cf38b086bd997249c0ea0460073<br>SHA256: 388e526b141f72da365e6c1487008eaf5440f4e2a173bfada2766c55cb3eb316</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.53MiB (17.34MB) – 251,265 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609d7024eb89dc7bd684d0207b3733b9<br>SHA1: 956350aa870d6a38630af3f3a3b53278471d39bd<br>SHA256: 95146645c0293ed5818f1df79ae51e4c9c07a1f6c91ea0f9331b8da35b754bbe</pre></details></small> |
| | | Full Location | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,335,187 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d87186c64f981273c433100841370<br>SHA1: 62922290000ef7c4549382119783c2045e4d1e6a<br>SHA256: 51718b9bcaef22b3bcf85a754a3a5fdd48d4a0efd9af8a4e3532e918a7368b41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>388.5MiB (407.4MB) – 3,770,967 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a5296fc623ecf8f0caa811c6b1aa61<br>SHA1: a31112844edcf6b611b51dd56508b700f7dfd9d1<br>SHA256: 4018f4afbdecaeedf11e8e21fc7f50e5719bc241f3a50121788f441946a9b58f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-03-07<br>IPv6: 2025-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.118MiB (5.367MB) – 256,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced96baa8d12dd7a7473b62ca04f3ec1<br>SHA1: f15aed8ee671e3e27c23c736e23edc25368ae1b8<br>SHA256: c034868fc655de42297d14220caccea0ab330ee13028773c38db7c6de47b21b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,344 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cef1451430608ae8ad70e0f4963dff<br>SHA1: 43bd5d1e9844ece7eae20604c4d83f7960da31a0<br>SHA256: fed2a958c9ff8365cbd35a38e1b062b5237d9c3576831c5f27705c77a13bbff3</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-03-07<br>IPv6: 2025-03-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,062,954 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1de2b09cb2477a5e3a644739a02d816<br>SHA1: 2ab572bf0cc2040a312448643055f2f718ca5ac5<br>SHA256: 1d66b45f20fdcc805cf1b87b04dc600ee7e3bcce4b90b5400d770f1ca47a3254</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>233.4MiB (244.7MB) – 2,257,726 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d52faeae6d9b914518dee2695e772b<br>SHA1: ba805ee8a2f7aede9c579332c56ae8ddfc7f7251<br>SHA256: 87cd4c71031299fc55a0c464dac619478c748c283c398787e9e7547a3ae9b9e1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-03-04<br>IPv6: 2025-03-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.16MiB (11.71MB) – 558,942 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d76287beda46a614b75cf5c53d54d93<br>SHA1: 8ea257107faf6ad8da9d829376242235090c2e31<br>SHA256: eb78dcbbb2f083b6a180d515ac24ab58bb6c45d224222cba8368a113b4d04ddd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>37.80MiB (39.63MB) – 574,398 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f85b9f87d1ce102eb609b93f24699be<br>SHA1: 4712fd3010a869c082c3eef313875d326ed5c362<br>SHA256: ce8c96bd07bd7b4ec12e836cc10fb7bc676cef49fc852ed2226b65e7de40d246</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-03-04<br>IPv6: 2025-03-04 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>166.5MiB (174.5MB) – 3,293,615 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4bf816f2f1b5668d2b6d7326a61a31d<br>SHA1: 03ad7899b45d57b7b1325352aafff7115f6de9f6<br>SHA256: 4cc9cc99d26c34fbe00e7c0c836c2bb87c17d7ee2a1cc0089be8327efe11d29e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>177.3MiB (185.9MB) – 3,293,615 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34a66aade66a1fa3da86ae283ce33e6e<br>SHA1: 1724f874e0fb610402944d24a672e59de190bfea<br>SHA256: 12010f7c7280452115bac6412e05167b108f053d45b30a5c774f46f8007bba94</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>165.4MiB (173.5MB) – 3,293,615 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 644da6ea8eab5ae5eb734b67646ac6a8<br>SHA1: 531a21e5abd7af6126b9cabc912e53418d585897<br>SHA256: 9d83a83c22f71ff829752d28bf1e6a00ebeb0f847923e2e06f32e574350078cf</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>167.8MiB (175.9MB) – 3,293,615 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0948c62a90d4515cea2df145f122c989<br>SHA1: 94b61e344ef4ca2f351c91f1ff20d558db63ea86<br>SHA256: 7f188bc322afd18be6266e384918ca4594cc90ece8f2ee7e7fbcf496b84a8b63</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>211.2MiB (221.4MB) – 3,293,615 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25f8dce86bd33287f908dc8e0f65b555<br>SHA1: 43009eb8a0760fa7f90920872941f7538743e1b5<br>SHA256: 468538c3591100d53d1ec2bf31f2273a41f712de0005189f71250c8a7d19df64</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>165.5MiB (173.5MB) – 3,293,615 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d41295ed057c6a68af7792908a2c2ea<br>SHA1: 927e72d416a40bb931f7d8c0c92524d77fd7bece<br>SHA256: a0a0d280292cf35bb78bb653b6588cafe81388b92ae409181ce2c0b827b04fe9</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>205.0MiB (214.9MB) – 3,293,615 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba4597ff8f23ee907bb1a02f23524a02<br>SHA1: 41fa4af13664437cb304b18996f6ecc8d467a2ad<br>SHA256: 9a1986ba8401d50dbe83b89778e9dac634d61548f7a77151237f523bd4e7793f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>172.7MiB (181.0MB) – 3,293,615 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f54e7d12db07f285bde76476c79d7260<br>SHA1: 07ff12b1287be1eb615b14b90cec66f3f78b1fa6<br>SHA256: beaf14cdb1fe1a27d542fa9a3c4297c17b407d761b44944aefa0d23075b2926f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>162.8MiB (170.7MB) – 1,738,649 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb6ad05d39fb4486d3a12f994a20fdd2<br>SHA1: 49873f3bbb566cf859be6c95d246f7559ff30bd8<br>SHA256: 9e5d8d5ba8c2820c9a423d1d0a29b56a35a3302fa9d2c35c1d14c5e77cd14ba0</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>166.6MiB (174.7MB) – 1,738,649 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f36b76b002923c695ac6e0959204a733<br>SHA1: ca5858fa1ac1d784418a79436b37512eb965c931<br>SHA256: 23606b0a2c976a328be8eacd7f380b30a7818faf1b2008a079210af02bdf98ac</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>161.0MiB (168.9MB) – 1,738,649 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a75bc7a584cd4259c11bbb31b12ba208<br>SHA1: 75d8b98a2f2293ad2215ccaf21759d41ff1debc2<br>SHA256: aefab6354ec817e8a2472ffa0120916b721700eb137232628d4b871e2de952a1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>161.4MiB (169.2MB) – 1,738,649 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2c990288e986c2e178203d7fbb5bb79<br>SHA1: 1810e06276d18ccd3c08c49f48c3a9765ab8d890<br>SHA256: 4dd07284c9c26f94df2cdddbc7b5590c23fe6ceb0882c321d40f1bec7b9453b6</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>177.8MiB (186.5MB) – 1,738,649 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d1af38b1d5461a3177842c09c9e77dd<br>SHA1: 35110eb7259ca54e95dc297eb31150ba6e4cd914<br>SHA256: 9621b81cf57a9d4d205cc16c3c2a7a586f1a5eb42c9ccc1960a5d2f45fafa1c0</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>161.0MiB (168.8MB) – 1,738,649 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 359bc5c61b32de3430a917001a1c0b98<br>SHA1: 9b89324aca9725623179643e4888055a40160b54<br>SHA256: f8f4f00824bb15675e97e9c3a58f9c867635e8dabffe72a6c2cad060e9ccde77</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>178.7MiB (187.4MB) – 1,738,649 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c35c82b0296c4dace9a47d1a4619b558<br>SHA1: e3800702a602abef90f19ea172fb4a74e34893a3<br>SHA256: d35667297036cb2e74d90d6e16318e242b585becc7dc46cc4b0b7f68fb415d0e</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>164.7MiB (172.7MB) – 1,738,649 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e55a69f4914c3a263ab32521ef0c815<br>SHA1: 14f156acd2c1e029da781332783b058628498b77<br>SHA256: 9ed64366c5c620d0ab3e106293fc90278afb03a4b83bb0efd4d62695604c7e17</pre></details></small> |


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
