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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-01-16<br>IPv6: 2024-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.782MiB (5.014MB) – 239,383 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5583a6f1e0cac198bb2eb50f4b3f6ebd<br>SHA1: 8b988097afee0434e06f785835d47a72bfe23d19<br>SHA256: c48e7e7feb62790c844ee1f820ab3da518cfc677999c749c40ac0f1b522a7340</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.500MiB (5.768MB) – 83,589 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ff90356004362aa8e18d83433cc8397<br>SHA1: 7b04f2c87f7ec72cf5eda6d71da7c6317aa050c2<br>SHA256: 54004515b8b7cf974092e7efd4e869a2e17140af76c2766272302ef16fbb387c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-01-16<br>IPv6: 2024-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.205MiB (8.603MB) – 410,869 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9d7630709f0bea344bbfd384d46ff5a<br>SHA1: 2250bc053074bdba85cb865f54902b9911f00e82<br>SHA256: 11bd856a4e8ef43df4c93bef662644d1b78d7232abf9931efd1a2405a0f9e3c0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.890MiB (7.225MB) – 104,823 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a08c3fbdb8eb9867dbc10e01be8e7e2<br>SHA1: 12c8e39e43cb6a638e39c9522cef3f54a203f237<br>SHA256: 204db79f9b543e9ecef2b0641f4f6b36f3c6f3fa8a9b4c5ec7660b06fb59d269</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.89MiB (17.71MB) – 846,069 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00f7a6dec63da273757097bbfeb8360c<br>SHA1: f5fe787822b262364735ff0db45c992b7a51a5e7<br>SHA256: fb6c5973c376b9cffc386e38161f293b7be78650561708374d92f9cf93f39096</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>49.74MiB (52.16MB) – 755,876 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4549a8b793c223f26841c1c4f454eb39<br>SHA1: 07ca2a24f8891b638f4d5fcc4d03ebd68d19f64a<br>SHA256: 3a3fd1f057c0b6662280f9d876397a5aae34a41cf832b64506b1ecbfd3284d34</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.162MiB (6.461MB) – 308,408 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 736158b820db1062b003cfce212076a4<br>SHA1: f3b03108eb0edf83c338abed05e010c2b0e9cde1<br>SHA256: 68e446a0380ab263a21743f68ab8aa6b249b213af0d6ffdac0780fe4912cb7c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>21.05MiB (22.08MB) – 319,959 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73819723f00de32c17c8aeca84d93383<br>SHA1: 71d954fffd9f9f5979ff89981fcfae6f73cadb05<br>SHA256: 1328a782f89b58d1f6fabcf3542ce4bb259d89c1f28a0cc70abfe70b5e573eea</pre></details></small> |
| | | Full Location | Monthly<br>2024-01-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,096,472 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b990a48af772fbc4cf7093aa51d35b4c<br>SHA1: 8ddfa8795c4c534c0bfd99b2472382b368d7fd5c<br>SHA256: 117938f84386f9ca627464e7c42856b6d9ff4f68bbcac12a393b73ea1ac0836f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>243.3MiB (255.2MB) – 2,358,639 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c61e48446e598bab5cfa16234f5f136<br>SHA1: c3373a6fe2e2f8e08a48274939c4b494fb99b5f1<br>SHA256: ff81c189923d299847f5b5e0e5c472fe10d836d11e24fa5379a2def67c998406</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-01-16<br>IPv6: 2024-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.626MiB (4.851MB) – 231,572 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24caac24a9c72bc3caa6451ceab08833<br>SHA1: aa114043e64d74ecd9e8ccd339b80c62d3fcbabb<br>SHA256: 6d48a0384e6e4d38820ac8d2936c12db7eb726dfe20c59600d4f14d173e3b15f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.10MiB (17.93MB) – 259,824 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23fc970b50f7b01de0d0c6bd29224c13<br>SHA1: cb1fe32e67d0561cefef5f2908570ae3af446a24<br>SHA256: e0f36200f10f817a89b6cf80d8d459900c5428a669cc706af32d15b709a8b624</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-01-16<br>IPv6: 2024-01-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4MiB (176.6MB) – 2,916,608 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4104f39d8c379ec8967157286f495717<br>SHA1: 440c75c20491f104948897ce552c95510badba7d<br>SHA256: 6689c6e63153fcbdc00272e2ec6cf04f0c6877860b4a667b3972dfa08c898747</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,560,460 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 142dfb0f4dc0ceb4f5a41b018ea53524<br>SHA1: 284b510184f46179e9e34f60dd0db14fc72f3e50<br>SHA256: c57159c9a8879702623a2ef4d0c2fad06d21e96f1836db2d3a09f9216aee1641</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-01-12<br>IPv6: 2024-01-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.198MiB (9.644MB) – 460,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e22860f663293b2beb43d7102fcd4cd8<br>SHA1: 1a9c82d254e2d90751fb55974c2603108906fc29<br>SHA256: bb79c5717f0351dbe602aa50554fa39a1c75b9e2f77edd9aa6c3f6efc94bc6fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.18MiB (20.11MB) – 291,500 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a7fa5e46f17dfb3b00853b65cf34642<br>SHA1: 101f5832d94290a616c74cbd3c944356c253aa81<br>SHA256: 08c4db3907aa59d4e35721bae3828aebf79bd9340e23dff1fc9b8243d6d49ec3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-01-12<br>IPv6: 2024-01-12 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>161.2MiB (169.0MB) – 3,434,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4314b692aef87592caef5657e0976d67<br>SHA1: c99de4ce4a2ccc424dbdfc57a1324a0ce946d7b8<br>SHA256: 2219aded4608d632029d982ea0d06df419c66eb02c5e8722fba52df6f1536c80</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>188.8MiB (198.0MB) – 3,434,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc6f4ed538c4bd8d3323bd1268a142f3<br>SHA1: 0334c30777b7ce4609f410d94dddab6c954d8513<br>SHA256: 48df27e557b73e1fa780da4b57bc3dcc113ffffa9971620d1edc3c1bb13fffd5</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>166.0MiB (174.1MB) – 3,434,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc801640dcff5244c6d1d0c017a4e112<br>SHA1: 4ef1dea3b89f7b24b499f4ff1f4cd150116beee6<br>SHA256: ea1de0634acb19b17e336d103e6d9de7391064c61f291c84960b2befb0a4037f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>172.4MiB (180.8MB) – 3,434,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7620cb2a1c81a336d154beb26bd08f71<br>SHA1: a3ab3d219cdfd04e2a2b59aa1154ed55d154b3a7<br>SHA256: 92c028a86b9558112a712693b97139718b6ebec664cbbba7dae5bd68c1ac412f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>201.8MiB (211.7MB) – 3,434,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c21013aa633e3920e601e3765abd076<br>SHA1: 97aa644cf88d859f2f5d4e2a1e43f41adb34dc42<br>SHA256: b567384696f6b67b6b8f60b08c8528bec854b799a4ccde71e1a731f9a595fc95</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>160.8MiB (168.6MB) – 3,434,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0db88fdbd1d8ec13de3aebf4e48c3758<br>SHA1: a1c5256b745d82f87af3469d129b976ea13687a0<br>SHA256: 75fa6883bfdb8196bfadb53a195e8c26dd9738205664e755c08011fc221ae7b0</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>201.4MiB (211.1MB) – 3,434,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db890ab4bfdeb6c5771d0306065bffb3<br>SHA1: 7823c14a50b2293ccea470e1a315dbc866bb8ceb<br>SHA256: d4d3d8aa4e5f36daca99241fda47291746b8a1d533620afb0ddf0562c5528b95</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>170.1MiB (178.4MB) – 3,434,292 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60172dbf1fad5df809be1d6e9eb693ef<br>SHA1: 55aa075dec9adba0033ad1bee70c527845fd2988<br>SHA256: a471bcc0e85d5afe43c4a990a90fa0eba2dc8558aa8336e2c5678c3e2a724c0b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>109.3MiB (114.6MB) – 1,224,427 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9391fcec801096fd50cd98f526b7b021<br>SHA1: 7b8633d27456017f93132febcca8a6a945cfd34a<br>SHA256: b5da82815f0a9b5d3dc6e089988dfe2099a0d9f26bb65c509927b112320fe1ba</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>117.4MiB (123.1MB) – 1,224,427 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7a5454db9704096b3a84942cf5eba19<br>SHA1: 8763f4425317bcab398880c7d052863b76d5a763<br>SHA256: 8f99be22966ba0737cd7cbecd9d237b1db3f6727142daa12edefc78ecac18f33</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>111.7MiB (117.1MB) – 1,224,427 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d50a9982da356e9536a39b30be2465f<br>SHA1: 7e89e39e76fa60d7f72a1fdcd7755f22b1096d27<br>SHA256: 7f1d993be4762fa4e6f927b0390df16d982262587e5a1dbed84bf5fbd9c789cc</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>112.7MiB (118.2MB) – 1,224,427 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5308973bb4f1472146126ab46b53a9d5<br>SHA1: 26cd749332673d8367bb6e8ff7cb563263619b87<br>SHA256: ebcca545f87831b7bdb24144efab9d160e635cc1edf3097a123ad25b4212dc4f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>121.0MiB (126.9MB) – 1,224,427 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05d82d003668b479f086df8cac1c1a87<br>SHA1: a85beb636a37f7d8aa158c9624cdf6229fdb9d7b<br>SHA256: c4c0844be49d5e540e2a0e7e3e465af1441c3d8d113157c782aed45a3858d035</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>110.5MiB (115.9MB) – 1,224,427 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 525959ed612bda40a5f8f9927777fb8e<br>SHA1: c376ae8accb39e6961c7e8910c2939d52900ea6f<br>SHA256: b1b9d4818d67c036ed7db2027f74f3bb47207aace21d7fd27c2b0dc4f39241cc</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>121.2MiB (127.1MB) – 1,224,427 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7105fccab400ebca6b38b57c159c1f8a<br>SHA1: 24ad5fb9e5622c13167c98927953198a1cec82cd<br>SHA256: bf6253ae62f0ae54ed7c955360d03e9610b4f9d66071c949a5efdebf1a6c173c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>113.7MiB (119.2MB) – 1,224,427 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be6a6de920dad8b26db50a7f6ed5cec4<br>SHA1: 69df59c49df81a06c3440b1c8ed398d08515054d<br>SHA256: 76f5b28ea2b2fc718f5421f2ba6772a741df374503009d77a9d2f556952481d1</pre></details></small> |


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
