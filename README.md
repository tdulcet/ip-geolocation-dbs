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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-05-31<br>IPv6: 2025-05-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.257MiB (6.561MB) – 313,343 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1df2c39b6d6f87ec558616dfa73ad0d4<br>SHA1: ba21270d30c2cd57835471b801f4f09fa0812868<br>SHA256: 125e27dd4c0049121d3c3c2573ab20e6f6547613e21cc25f47a79e32376e5dfd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.26MiB (12.86MB) – 186,376 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 55b5b14120e5bc5a405296a0241df52c<br>SHA1: ce7719da047128ce21186b2fbbd609fec2b23d5b<br>SHA256: 0c055063c48122d28b319349bc540b5741acf898125a4f9a195dd3bbaad30e29</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-05-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.88MiB (13.51MB) – 644,838 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52001ec39e32fe34af8bf5f5c49c16ed<br>SHA1: a7b703a7bd266f1d433b4d25e65246dac51ea5d1<br>SHA256: 31e10d1b7d83bf65a0a6ad8a1e463826f48f768597aeaf46c1d97fd842e6cb95</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>98.13MiB (102.9MB) – 1,491,322 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3620475801a103edbf1c52a3c44b4137<br>SHA1: e7890689c4e5e2f8586293b9ad75b8d045468a59<br>SHA256: 2e01d2e9cbb3d926af78597f3c832d7ac3e07bb0d80c306b832acf12d91d667e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.057MiB (7.400MB) – 354,084 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29dc016a76e5d1ce86f281b6be610e8f<br>SHA1: 91c6b4652acafb63416678a1a40d09acb733d81e<br>SHA256: 8c2e1dc4bcb582e63e3cf9a404cef7bbda49da95853a250d12f056cd6e928998</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.75MiB (18.61MB) – 269,749 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3faba08113ae8afbe0f9aeb0c0bc4db1<br>SHA1: baf9d49de9c133023e8e928090c9f50a291301bc<br>SHA256: 126f6ef6cfb9616fb3631b757bf8a7746130d673be4019cc177df52967b9cdf0</pre></details></small> |
| | | Full Location | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.7MiB (197.9MB) – 3,293,979 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc252212886dac7c40089289aaf5a71<br>SHA1: 67fd9db8ecf45ba433418c2361c87e2627dc8c3e<br>SHA256: 6fe5f2b32b1d809aac5a716539f4708f61c901ddad9c02b4ab613c7e262ccd06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.5MiB (412.6MB) – 3,819,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14c6250f6e4e959f775581c56c6b0abc<br>SHA1: 77ffea96762cadecd4cdca9183084900fec55cb2<br>SHA256: 1bc149f9307004c4ad7c60c0f1a25333a23792c5d431b1b374511792cbfab474</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-05-31<br>IPv6: 2025-05-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.968MiB (5.209MB) – 248,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d089ecb129beaeaf2a0c4ac1427eaf6<br>SHA1: 3b494cee2f0d5a67c96e8fd9ac320d9451b36a7f<br>SHA256: cd40baf1649b683953823e24dacd7a02626143eb798e879807a24d509beef71e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.24MiB (22.27MB) – 322,743 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beb56e4b585711434b2fde993d168a9c<br>SHA1: 55d2015800e048a7089193a246f2d5b1249d4440<br>SHA256: 9d5dd5a77dc590c2642e0f671432b7bf9450c4d0347d15a7d904c0c0b55c8ba0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-05-31<br>IPv6: 2025-05-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,019,379 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a68d931a9c3aafbbfc0ff557db9889f<br>SHA1: d3c7b6a63aa399a3a3bca849a9160e65422ac12b<br>SHA256: a6f47823a7140f643c6df5dbe10363559d6998953d47e61148fa9ce21dbf44bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>244.6MiB (256.4MB) – 2,371,820 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db0839b0b336b2cf8a46e6bd46836924<br>SHA1: fe99a8305efd24139243b32063ad92bc72cf9fc3<br>SHA256: c7e0b4a9c07317086b1a652dca4b3928e1bcaab9d1faa273e38c74a68ee151bd</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-05-30<br>IPv6: 2025-05-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.91MiB (12.48MB) – 596,068 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c70a9121b62848f78c188d4518c5bbea<br>SHA1: 4248e418915199225cf0605dad8e18f5226ad9ea<br>SHA256: 3fa9a9022fe956cc85041934e96f29a88de0135dab7b53aed35a228c40440af9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.68MiB (42.65MB) – 618,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26f094e07e93b5f0dd41bdc197728e2d<br>SHA1: ab01322a23bfca27e8298a266f9eb68d3c9673da<br>SHA256: 09135653aebc777c0e0fe758c0498b56e4c777f56450b78dd81a9aa06e45a272</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-05-30<br>IPv6: 2025-05-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.1MiB (180.4MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec8c380f0bb9d9a5a9df1a1656d12909<br>SHA1: e49abed65d5686f50a4690535554bc3c106afd3e<br>SHA256: 09ffd7c64f9322d09cef37db31720d0359a57f9c520d0207ec8ae721bd528e41</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.9MiB (191.8MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e54adc160e27c57e0681e8edb14b2611<br>SHA1: 2be26e21011de5e241b7d9d069f467ebc48deea0<br>SHA256: 9a3b728598118194641eca69375e5ec1c56c02baced442ed26aff3ecd2c76c55</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>171.3MiB (179.6MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d975b556d13cd6f30371004bd50a0e97<br>SHA1: 672ee5e17d95a2e7759db9ff5b6b788a71a79d80<br>SHA256: 7b550b09daef994865de9ded2988bbb8685b6c398a3abc20de0cb68523a34402</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ac4bdb8d7e03018f65fae8ac00a0e9b<br>SHA1: cfafda6745f9a0bbb0e028dac6278d0894f52b92<br>SHA256: cefe3c4a9f362f800b6cb41d3b809d0b1c467f8b9c2f2f42c43f54d6892d53ea</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.8MiB (228.4MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67dbbc7775ab424339c8bea59c30e70c<br>SHA1: bcab2b3e8d739a942f4c74c07cb98060eb41780d<br>SHA256: 5b8daf8293a764e4e39e33fcf71b1a09bd31f95763ba605b243c3fd92094d309</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.9MiB (179.2MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c24d3ae69a8e20ddaca17b43231cc5b8<br>SHA1: f39e39e8c9c750a93546ecd1fda61694eb3b2d46<br>SHA256: 9d49c912292edc866e2a4a66aa030831f1b9cae53a4d887db0b3a693e2f48c2b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.6MiB (221.9MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf3bbbd5afc31fc3539579ee922256fe<br>SHA1: 968417c9d2a08367880eb89cec5424da59a50e91<br>SHA256: b3b41faee721f206978ef6d4bd85f7402ed54b4d132269f061eae1a1db3976c1</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.1MiB (186.7MB) – 3,395,372 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5a4d078c50f53421ad27bdddf569491<br>SHA1: 6f9ebbfd3df09400494e0b84e4183e8881c4842d<br>SHA256: 99fe222524141845b1d1044f957c452c838f36437c44260453825c83f85f32df</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>175.1MiB (183.6MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32c2ed691bc9169ae014b8fc9dd86313<br>SHA1: 4b069eb66bf31d66c444c514f86e1e692717a023<br>SHA256: b418313c5f07b6415d7f8ca4da8e59d0428f354f82e7e30eaf0494ca4b70344f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>179.0MiB (187.7MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25ba6b014f5190f1d9b38ae3f4810707<br>SHA1: 848de216ca055e32c8224fc473ab1e49a620e0de<br>SHA256: 35c934f1146f11b062c41a8879afc90848f2ac8249af66f9ed7a91c3d39f8ceb</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>173.3MiB (181.7MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9773b212f3ed70cef0173bcafa63dda3<br>SHA1: 7b1537f6ef01a8d115647f49ee8d01c810297cb2<br>SHA256: 3c471ae7bb78884a31beef3750e38a810ea9da3b8e29d8a8e42d291b9cbe1af1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.5MiB (181.9MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63182c214fbb0daf49c574493c5d3e66<br>SHA1: 06b01ce9877510b98f960684bed99bfd5f3bfe5e<br>SHA256: bd26f8730807e4b82c811026672bc35269b381a1cd62734d683817add0a7bcbf</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>191.7MiB (201.0MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97269922f2a231889fca4cb7433e2c51<br>SHA1: c1c1c0232735d2b5d3760117cb2899b91ed45d34<br>SHA256: c1776814f12a725334da7049057871858eb83c87b3cf1baac85b2b2a338bfbe0</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>173.0MiB (181.4MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf2c28397a5672784cd887128a2f7e19<br>SHA1: 55f49a9e42231063ca1a7b8373267c6223609dd4<br>SHA256: 98939cc079cecb280b09cb4448f5c0ed3135771b4de574144f0a55c9961f5a21</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>192.6MiB (202.0MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec9b47d9c303460924151ec0a39cdb63<br>SHA1: 8ca056e2b6fc1a335168a36df009bde1bea932ff<br>SHA256: d57e193b0779e70123bee36147ae2cf80c6de53b08bc1ab59cb7492e5739908d</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>176.9MiB (185.4MB) – 1,860,034 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1042618f8a21b1b4d7f58075cc514af5<br>SHA1: e23328876c74eb40028ec5e82f1022e1d83a3380<br>SHA256: cac5dd9725be13c3c214b85955147bff4bf6c0d5f6df4f6389073b4496a9bc0d</pre></details></small> |


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
