[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases
IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-10-11<br>IPv6: 2023-10-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.620MiB (5.892MB) – 239,373 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17b8ec60bc7daa141aec398b5e9a2985<br>SHA1: 4d318c76500b757c9b597a6185d1bbd207330498<br>SHA256: d26670bbf0cb04e85f8613e14b94a07fb328b05b9c4c63cfb146d827aecb5ba9</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.302MiB (6.608MB) – 81,580 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 557d0882b722800da65a6b28e75464f2<br>SHA1: d5ebdbab9725e2255f4b614abfa510b049c4af5a<br>SHA256: fab7d51a6c220a970703d4054b8731836448ad91b983b45c4be9791a50e6dae2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-10-11<br>IPv6: 2023-10-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.600MiB (10.07MB) – 407,729 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8355c35bb11c716961c756713bdcd47<br>SHA1: 8aa100a049a416f3fba7b944f485dad4a5a85b9b<br>SHA256: 2f10699f26d00a7050e0fa019999337fa2cd35708c8aaf7847a47e70b229f012</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.094MiB (8.487MB) – 104,879 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e039af5508f9ffd5c775bcd047566655<br>SHA1: bc28272fd39c8436b0d818cc4cad64b6e7fbeee5<br>SHA256: f1c312707da05f3efc9589d53bde15f8c1f82f3b8a444607d0434fd64a95de49</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-10-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>16.27MiB (17.06MB) – 693,863 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91c1288e0f98d4c4d97e46f647e26e55<br>SHA1: aaede043b38f76a255eb6380ed30554b5f037b50<br>SHA256: 0d2ef5e2fce76b2c868688098c24c9d48fdd4782a7f7eee5ff93895109fd30c8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>43.38MiB (45.49MB) – 561,552 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 330f45587cd0c2c021e45db6d5ca1ff3<br>SHA1: ba0fd2af01676c42bb7cc775a6640e970bc688df<br>SHA256: e60bfc9e46bfedd2936bddaf981d533087a27c219d276148d36f06a0f73a9166</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.207MiB (7.557MB) – 307,820 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ff8d81d8ce4efd3476359318175af0<br>SHA1: d105d1c4490b536a83d0461759256799109a17cc<br>SHA256: 4cb45f08b0bbd6d6c4fb204e776835b939ac663761aea652d12ae2ab20494228</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.54MiB (27.83MB) – 343,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3256ab7e4df24ca9917bf92c70b9ce1<br>SHA1: 832b96b707911579f91d2a42cc84b0766c5db738<br>SHA256: fdb03997e4b7c1a6bdffa274673b7756d8dbfb2ede55f1186b3957ade7042544</pre></details></small> |
| | | Full Location | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>184.9MiB (193.9MB) – 3,048,591 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed65f47a5f866d476bde81f05015d0ad<br>SHA1: b0ef2e2cdf8875da35c99816df76f9fa88d3de9e<br>SHA256: 5bca8efa9618ae69c9fe4228342c0ec4bfb4d581ca0766a3a8e45978d1fe7875</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>269.4MiB (282.5MB) – 2,345,213 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f854d9364b9ab55744dfdc557c9f9f6<br>SHA1: f419e9a0b9db7b3c78b5c98927c74c8427f3fcd0<br>SHA256: 3d1595b762a094dfd2f9ac1525dcc77a67ac87dec747f420b0fa63ac4fe51cbb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-10-11<br>IPv6: 2023-10-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.547MiB (5.816MB) – 236,500 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4857bb88f1e540efdbadfb3e56c208c8<br>SHA1: 0190e03fc0543a58ca868f0f36a92556049db942<br>SHA256: 44b7a5f1e09f7ad797ea8511ecfc8ddada844067bdff82f4255273d85906d172</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.24MiB (20.18MB) – 249,120 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5105fe9bbe5d0ddc9bf8995e1cd8fdca<br>SHA1: 48b9366c0983f8d70d79ad112999057d17d64829<br>SHA256: c10da1d1999f1867044c9753957966c4989400bf25df0e7fb02c524b43dc90fb</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-10-11<br>IPv6: 2023-10-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>171.6MiB (179.9MB) – 2,803,356 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4abca24edbdd7d97ffaa621ecb9327a9<br>SHA1: 97c24a0d18b54cd8d2692e708765b79162107242<br>SHA256: 903407a226a3eb479f2165ba004762c64c3a41dd5a9c0d515be1353f99e5796a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>166.3MiB (174.4MB) – 1,448,721 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d928761a3b79f2ef6c55ec6d4dd813e<br>SHA1: e7de15f34cace41d4332e3d59c8ffe729fc2f8ec<br>SHA256: 613e34be98c76eab733c9982022bfa16a5d1ab57fd73444f0d6e8a2ef59ae567</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-10-10<br>IPv6: 2023-10-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.34MiB (10.84MB) – 441,129 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4bcb5a3177e756f44ff60dab4658319c<br>SHA1: f8704fe7b19267f317a0ffbe76ad23a245f3e5e2<br>SHA256: 65de5505f79ec2029f94060938e1afb765c36ea98f5d3f4f116b433dfc3db6aa</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>19.46MiB (20.40MB) – 251,864 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff7962cff83ad5f10c7525077fafd9f5<br>SHA1: 405f5d24e253b2f828a050faacfe471f2f51cdfc<br>SHA256: a3754a202c423adaa2aef792cde281b34dbd16892c3e0c78f0140d6f136cbe71</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-10-10<br>IPv6: 2023-10-10 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>192.4MiB (201.7MB) – 3,828,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a516278328b45845f87650a3ce72750<br>SHA1: 0009370c99b6ed878c6730b0d1fbb2b3652ec385<br>SHA256: 208c1151683af13778f4df8fda84e36a444b92be949805f8154b9b46b1f38ade</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>224.4MiB (235.3MB) – 3,828,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4952c05fe8d38dcae4297ca246c67198<br>SHA1: ac012aa402c061bcca8f1aa4face3280f78cbf0f<br>SHA256: 8aa0e51f626268a67484cf500bc913a9a36f0702f9420bded408ebcdfbd7a098</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>199.0MiB (208.6MB) – 3,828,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9618c325cd2cf251694c19caf11719a5<br>SHA1: 632e732170d6c4dd89f9e24c7f72b2a8dd359015<br>SHA256: 9193f322d426182a21ca2870dd5c75be323492019dc15b534e184665932d698c</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>205.4MiB (215.4MB) – 3,828,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c971d01080af7290ea6414c05441f1c3<br>SHA1: fe3a8a7b9bb1852ea8fedecb12e4071ff62d7c89<br>SHA256: c12e99a95035e0bc3747fdacd70f3109eff9d1ee7c9c254dbebe40c88d061d9b</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>241.5MiB (253.2MB) – 3,828,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6831aa8daabd985934ebffb6c22c588<br>SHA1: 532eb671a063eb827573a82bf8ed733c0a4bfc72<br>SHA256: be3f9772336f12b9d36151e86f7efc45c784cff1284de36e183e084132dab0fd</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>193.4MiB (202.8MB) – 3,828,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30c7c4a9f05e87b2132b0a8a0757aee5<br>SHA1: 686feeb7bb97a7d2acaaebd480aedbc3979bf340<br>SHA256: c6eb9662ca4e3f4e8a72558d28b5f81031c50951d73d60e9b3f2c81ad78c43f5</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>241.1MiB (252.9MB) – 3,828,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 452eaa8f957159e708807ec42edd8cad<br>SHA1: 5cbb9a01a7291de76d28605d241e4b61b791dd66<br>SHA256: 2346742c943864929b9f8270f0806b16103d87f1107d455e34c09f637a05274a</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>205.6MiB (215.6MB) – 3,828,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6117e6c774a14374bd3dd03c735be845<br>SHA1: 92b7b07d3479b6bcd9547e52fd458ba255826e9d<br>SHA256: c6f18b714ad916e742a9b875910eecc6b10dff537ab9b2776b972762a15f8200</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>121.6MiB (127.5MB) – 1,208,380 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a80b8e00ec7368859b726c5c22ded022<br>SHA1: a94d8680512f08e54f003b7bbed4a49ecc2e76f7<br>SHA256: d3a61d72045642256f6b40399127063ef6cc0682631b9b04ea8c60f5b0a6e1ae</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>129.1MiB (135.4MB) – 1,208,380 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c95d5ba4fe49b04c861a0d0844b40be7<br>SHA1: 924003d390e22d6813f80c6f6f86c3b1b9c65f6b<br>SHA256: 1ea3f14dfe60ea9f245cd1f42a8401466f8c4b3076865c799528d8dec66c205a</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>123.5MiB (129.5MB) – 1,208,380 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d410eec9be43a956b5498f501f80de2<br>SHA1: 8af6e3050b755e11042a92577dee0f866614751a<br>SHA256: 8e6cf9482f8be4e200aab2c42d536e9dfe3c83d58288235e977582454e4379c4</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>125.2MiB (131.3MB) – 1,208,380 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a7678d7d3dacb96f9abb446f05b4c72<br>SHA1: 875f8a352c7bfb3d910b8101c9ee9bd828ebb376<br>SHA256: 2c3bd94bf41455fd19f58c408ea4bf74873ac000ebb726fa0834b906047c102b</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>132.6MiB (139.1MB) – 1,208,380 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f6cc9e514f84de37e397b8b042b1a64<br>SHA1: 1935b1750b716718f23d781ae23247566ee7a190<br>SHA256: f30efd40bf2ed6eb4639857fbd2cde299f1a8bda1b2ac728a16aabc8f88c9333</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>122.4MiB (128.4MB) – 1,208,380 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7dbca11e53d6a3ba6418c8ff3ca3b828<br>SHA1: a473a4324ef097f17ccf54789fd2d4581d811757<br>SHA256: 7a7cbc531ea0e26a7f25d46311f381e7991d8e0dc43e9941b65720727fee8dfe</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>133.1MiB (139.5MB) – 1,208,380 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ac7857dffa84370f33b6d64651864cc<br>SHA1: c5dcbd9541859e08a9ea6141b575d5383d61f288<br>SHA256: 3d4c56a62dbf217f29a6967bf50d38ac2bcafe6ad02e3e87d2544cbdd27b9ec9</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>125.5MiB (131.6MB) – 1,208,380 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3531698891741eb3e6920a199e972fcb<br>SHA1: 1b600f03fc966b7abde2f298feb4ed0ef9c8e107<br>SHA256: 4eadc5b457f50f20273b60be8574552868561267d4ed4678b3d6cf1419579321</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hex format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
