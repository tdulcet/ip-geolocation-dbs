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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-12-29<br>IPv6: 2025-12-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.430MiB (6.742MB) – 321,957 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 549a1c878e6a15df7b0b1ddc66a079af<br>SHA1: 72bf64e968127c4f2d51932646fabb38d5146a1d<br>SHA256: cfb1c3dd9cee84a2d566e249ec40589c14a70b9f7d1463023cf368d62a326348</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>15.15MiB (15.89MB) – 230,269 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 350ee2b9683bdfdb2d3ca6dd664428d4<br>SHA1: 3f1faf842a9150dca5846291a50da5592ea34878<br>SHA256: 0061650bcdd1ce8af78cbedd7c04a4c628215baa087b3917e9fc5c2ac2fd8cb7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-12-29<br>IPv6: 2025-12-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.184MiB (9.630MB) – 459,813 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9fd6425924bfe554ef8e87a9c587783d<br>SHA1: 8861477579ada30ab8e485288173abe3c2cc3ab5<br>SHA256: fd01dba80bd2533849eb89dec9478ca2ea472cb581f8a911a0b7050ee284ae0c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.498MiB (7.862MB) – 114,054 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7dbd926e147112b0ee220ea1eabe29e<br>SHA1: 2ba1c8ffc98f0fda48d31e03ec687edaae3b55ba<br>SHA256: 1d00409dc9b124ae1e04d73101bb0ede64a06c851c7454959cb829dac86bec91</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-12-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.46MiB (13.06MB) – 623,890 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5d79dd342c8473a89ec19f41eabc4b9<br>SHA1: bc823b7a38e4db473a52771a803efc05ce14e6fa<br>SHA256: d3ced4e0feec22832c3b56321c83f909a893e9433e8f45a74a02891903486f49</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>77.10MiB (80.85MB) – 1,171,733 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f3519b651c29cd03773db893836861c<br>SHA1: e79d6cfa120d8d41f1eec38f2bc7b4d3588e2c39<br>SHA256: 701d524b98f211186fc276faaca185d10f1524722f19493ef380dc4c1462ff32</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.286MB) – 348,136 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7e1cdc0f734432db063bc8ea17fe4ac<br>SHA1: 37f9e6c112306274cec40e193d1e3e569c64b3b2<br>SHA256: 742518e7640f170ed5d2a0d958f205c284fd65e6fd90134ef8d6439deb66baa9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.04MiB (16.82MB) – 243,745 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9a4942e90efa6668450bf8739e73630<br>SHA1: 8140c024fc4e57de5931427bca463f79a25acee0<br>SHA256: 25e47804b9ec05818a0640f0015ee2ceee04af5c18c8c6691df1a1a7ff24fad4</pre></details></small> |
| | | Full Location | Monthly<br>2025-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,748,051 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c39e4254afd397ecc092fa9b312dc177<br>SHA1: d08c9a3568d106245f5b948c13a1bcc47aef182c<br>SHA256: 33321706c4dff22486ff51602c7835792629103b1d2fbb2f2a4359946878f8f5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>454.6MiB (476.7MB) – 4,419,200 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 721d96d4249476809ae6caf6ab63732a<br>SHA1: ff95bbb13ec1774645bbcd94414a0919197819d0<br>SHA256: f5996fce2eea4831364047053cd636b4b0bc70543d854ca5c863b7abe0f99515</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.196MiB (5.448MB) – 260,054 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd1da47eecbcb1371255bdc50c718d77<br>SHA1: 750933e1de8cb3d548ac391160af871b871bed93<br>SHA256: 057d957bff860585d56f46ecfe886d386bfef914406c23dbc1816ac00ba37c62</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.00MiB (24.11MB) – 349,485 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78fac9141a055ba1200b9e4197d17a6d<br>SHA1: 2dad5e9fe9e6680a486b8de86a165bcc1d75629c<br>SHA256: 2f85601d58de0e24dd53e1f990a048c34f01bcf4433e39e78d3d87d89d39ae02</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-12-14<br>IPv6: 2025-12-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.5MB) – 2,947,207 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd8aac3eeb88b310fa305cd0935ecfd9<br>SHA1: c74492fae9ff6ac08a5c5dbc08bed733d3da06ea<br>SHA256: 1dcc9f177867a631fe4c98c83a10cdb7d7578efba05eb4d13a9d34ff00ead1c9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>291.3MiB (305.4MB) – 2,823,618 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf7686fea78936ceeebd798c0594060a<br>SHA1: 3bf18b3cb9ecb79d04eff383fce69df36bae3d51<br>SHA256: a5bbe43965014f4f35c9262bd8e7ae3e3dceb030619ee951589b718687fc8ec6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-12-26<br>IPv6: 2025-12-26 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.26MiB (12.85MB) – 613,513 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c0727563d3f31ca1fe2fd16b6ee3962<br>SHA1: 516fbd852fac8d941d9a75076ba0919343715c5b<br>SHA256: 1f6aa6fc5d27368017d7c5c904c39afa268129ed0d0fbfbba44927c3b8390e48</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.56MiB (44.62MB) – 646,715 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e6f59dfcf14a7aba02c7207e46fd5642<br>SHA1: 124610ad457fd6d82af087d1669c469763cc14c6<br>SHA256: 5b402dd5662cfddda24602c126f0d77685e19aca69795e1f3023fe9369feaace</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-12-26<br>IPv6: 2025-12-26 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>178.5MiB (187.1MB) – 3,522,453 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 077632c518af56d075a528c16ca634ea<br>SHA1: 027d4bdc8e3a88fa793c212993d18929bc259cc2<br>SHA256: 63d1c30218833550926b7c62a5eda1e886867cbadae17a4090cb70bb91b94a83</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>189.5MiB (198.7MB) – 3,522,453 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf424031e2b276afc62ce90c6f954daa<br>SHA1: 5cb5504eff3f2565c6d938c5396edd556a730529<br>SHA256: 3b8d9c74a6fd8dfe898c08e22c52db12d9d8cee9a3e73bf93b1e5156d24c28a4</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>177.5MiB (186.1MB) – 3,522,453 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 992be0c196515231573ecf27d22896ef<br>SHA1: 864ad8e3b88a30a5bee9885ba85daa5742a23812<br>SHA256: bf0a19061e3be779784d0496aa16f52cc15b11705a30841ff5f6eba81a462b32</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>180.4MiB (189.2MB) – 3,522,453 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18ce50f8edea0096fd98e86b2172f0bd<br>SHA1: 495f06835da8a44d02fc1d2f1a1f144ba518b9d5<br>SHA256: 52dcc162f2e7f0f79fdeface70f567504b7b218544e2f78c92ce9022e2acb1ed</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>225.4MiB (236.4MB) – 3,522,453 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6c27e97e30ee27a9bfcf64c39337caa<br>SHA1: 1528966b9078bbce078aef08fa94ca550cbf5a3d<br>SHA256: 3baef4119e84c7d781773d83333c4920a5a54490d41ef113627c0c7137cae17e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>177.1MiB (185.7MB) – 3,522,453 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4025378465585d7af7b97a28215fc6e8<br>SHA1: 208580ad91e95d15fc391d7eb18aab81f42e2ef0<br>SHA256: 682093858209b9a380cab2ca759b364707c9261027bf01b29de7f98741a78dfe</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>219.4MiB (230.0MB) – 3,522,453 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e29d277821adb7d7eb8aff0bef9c4dc2<br>SHA1: fe4c85237d24f0802a85cadf1f6ddf78208d6e37<br>SHA256: 417e9e3c7b683284a1bfa59df50a21b67b2da883add870d06561094ddf0e7f14</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>184.3MiB (193.2MB) – 3,522,453 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af29ebc4e9a93ae24891b3dda0184968<br>SHA1: 173a87ba099ebe9f94407ab747f4c0254a42c499<br>SHA256: 25f2362239f14b6ed4577bb0e50a72fc0ccd99bb131ebaebf460da363514ed04</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>183.7MiB (192.6MB) – 1,937,894 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb59e75498adfcd7983470c9ddd3e87b<br>SHA1: 7c2f4835d4b1dc32ca3211f0389100645b23d3a5<br>SHA256: 3e8da22d7f686a52f77fd1f2ee7983c1d12d8c5ab59483584888ddb73e8f0489</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>187.9MiB (197.1MB) – 1,937,894 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 54bbf5c2986c6df56da8b468f6eb826d<br>SHA1: 559fc69aae9fe77a16c26da6286728293cd0bfc9<br>SHA256: 7eb40084c3c66f39ed5df9f74bd2be0246f33162ea8caef1b70d4305d371644a</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>181.4MiB (190.3MB) – 1,937,894 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50f0a255743dd24ec33a6438396fcf65<br>SHA1: b1f1327485aa240a6ac63628850e8e9ae687a0d3<br>SHA256: 0d143b72aacece0c2fc9f9fdb142c4038353e6e9834664765b16fbc1e9492f89</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>182.2MiB (191.0MB) – 1,937,894 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 059334e7535e909edd297af442f6fddd<br>SHA1: 752363212155ce5224ca9706b3b53c7a53707c3e<br>SHA256: 9ad72259018c425cbeb5281b47ffde6d58c1eca645b52a05ca18bfe30ddf5eee</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>201.6MiB (211.4MB) – 1,937,894 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c723a6bcc78966aa55bce57d943b0b2<br>SHA1: 7afe6b674138ac00c3abead0eb34929d66ebe7ec<br>SHA256: b64c3f5b54ee5346ae8a1d41698d1f9d9b0257fa26d939459b7d707db3577a36</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>181.1MiB (189.9MB) – 1,937,894 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 190f56cf49570fa26c0199f0bd15610d<br>SHA1: 39d001f730f597b11d02a5b4cc9c3051c1f5a61b<br>SHA256: e68b7deebf4a710fc8f07c1fce4bb102eeb14528fd73188a9b02502a53b898d8</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>201.7MiB (211.5MB) – 1,937,894 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2f0c77f1237ff141f34ce31e1d0a632<br>SHA1: cc12c78382412d58faea67fb9763c9489868175d<br>SHA256: b103c90f25217f0832c41b613e69659ca16459981f97bfcead8e6313c2c28e6b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>184.7MiB (193.7MB) – 1,937,894 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9e01de3e4a8d68bc3e25657d48ad7d9<br>SHA1: 013a18c033b63a5aa8faf05e743f94701ba4f0fd<br>SHA256: 1ae503767f6d6c649929d8cbef81028ee1eb12d10b095714eccc2c55bde8bcbd</pre></details></small> |


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
