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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-03-20<br>IPv6: 2025-03-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-20<br>IPv6: 2025-03-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.368MiB (8.775MB) – 419,040 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7210bd75d12259d5744348b189fde1c5<br>SHA1: aad2227f7e64f965f0928cce5b71908c1782f780<br>SHA256: 1470b98e82bedf7c6810eefd8bb94c491709a96ac91257b3401ea19973aab749</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.031MiB (7.373MB) – 106,967 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a1e04945b3d1b341ec19cb7a03664a3<br>SHA1: 7fb65111f0c68218caf817b1d95fc49062478fe8<br>SHA256: 571128bd32a21c385b21d0b30a9b2e3709ed7d3304e1080130f5d5c2f8652d60</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-03-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.67MiB (13.28MB) – 634,241 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf5ef40c4c216c88ae0a30ee1bc529b7<br>SHA1: cd85f717986f67038b443881ae899d341503fdea<br>SHA256: 2059f99eded450b662e3125c2dfe0e09bce36d61753f1b460cd48f7151162739</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>69.95MiB (73.35MB) – 1,062,974 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a809b67e1a31fdd8fc7d35629907831<br>SHA1: dfa65619bd769acf239f8728d0b8eecc713ac4f6<br>SHA256: e9dd3785ac6c617cb97cd04b3fae93c35a49ca11505512af29274b808201531c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.404MiB (7.764MB) – 372,055 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e5911df23fa4121906510a5a567b13<br>SHA1: 9325bb0b20fe7cf38b086bd997249c0ea0460073<br>SHA256: 388e526b141f72da365e6c1487008eaf5440f4e2a173bfada2766c55cb3eb316</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.53MiB (17.34MB) – 251,265 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609d7024eb89dc7bd684d0207b3733b9<br>SHA1: 956350aa870d6a38630af3f3a3b53278471d39bd<br>SHA256: 95146645c0293ed5818f1df79ae51e4c9c07a1f6c91ea0f9331b8da35b754bbe</pre></details></small> |
| | | Full Location | Monthly<br>2025-03-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.0MiB (200.3MB) – 3,335,187 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 533d87186c64f981273c433100841370<br>SHA1: 62922290000ef7c4549382119783c2045e4d1e6a<br>SHA256: 51718b9bcaef22b3bcf85a754a3a5fdd48d4a0efd9af8a4e3532e918a7368b41</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>388.5MiB (407.4MB) – 3,770,967 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a5296fc623ecf8f0caa811c6b1aa61<br>SHA1: a31112844edcf6b611b51dd56508b700f7dfd9d1<br>SHA256: 4018f4afbdecaeedf11e8e21fc7f50e5719bc241f3a50121788f441946a9b58f</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-03-20<br>IPv6: 2025-03-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.118MiB (5.367MB) – 256,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced96baa8d12dd7a7473b62ca04f3ec1<br>SHA1: f15aed8ee671e3e27c23c736e23edc25368ae1b8<br>SHA256: c034868fc655de42297d14220caccea0ab330ee13028773c38db7c6de47b21b0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,344 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18cef1451430608ae8ad70e0f4963dff<br>SHA1: 43bd5d1e9844ece7eae20604c4d83f7960da31a0<br>SHA256: fed2a958c9ff8365cbd35a38e1b062b5237d9c3576831c5f27705c77a13bbff3</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-03-20<br>IPv6: 2025-03-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,062,954 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1de2b09cb2477a5e3a644739a02d816<br>SHA1: 2ab572bf0cc2040a312448643055f2f718ca5ac5<br>SHA256: 1d66b45f20fdcc805cf1b87b04dc600ee7e3bcce4b90b5400d770f1ca47a3254</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>233.4MiB (244.7MB) – 2,257,726 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16d52faeae6d9b914518dee2695e772b<br>SHA1: ba805ee8a2f7aede9c579332c56ae8ddfc7f7251<br>SHA256: 87cd4c71031299fc55a0c464dac619478c748c283c398787e9e7547a3ae9b9e1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-03-18<br>IPv6: 2025-03-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.32MiB (11.87MB) – 566,742 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de707207eebc21f9417ad37e3008b6aa<br>SHA1: d59ec2795628a035846b47abc5f077544cd3c0c1<br>SHA256: 5a15bbb893b92c0d08aaf902288acbae037af53c08e61521123d4529428513bf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>38.39MiB (40.26MB) – 583,483 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec9e058a71ec118863bee88a85d2b5be<br>SHA1: 6c42dc94d8dd569e92d469ad389cba23dade74b7<br>SHA256: a495c08a29ca4db209aef5d09c2b5029b21e511f43c3d400ec3ac4cd959c1944</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-03-18<br>IPv6: 2025-03-18 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>168.1MiB (176.3MB) – 3,322,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b850b46df7e76afb40f0428a0a9c1c1<br>SHA1: 8703a32121defb5f0c8c92ecaa36ef8b74a4d522<br>SHA256: 2fde18fbd88b4895d5cb4ce4b42e8473e6e02f1ab453b9fed6a0af8c9425a9fd</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,322,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: caaa68f7b660588666c6504ae3e9d2a6<br>SHA1: d1aada8b0649ae013eab6fd7fe5ee273c7cc1144<br>SHA256: 7755712b193d9c353229bae4cd1fd6eb17cd4d69ae22ae55fd172477c66d6cbd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>167.0MiB (175.1MB) – 3,322,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f7318c315cc27d5888d8bd7ded5ce2c<br>SHA1: 672c3f390627c7045786372dad21197f31897b9f<br>SHA256: c02b5341e1f75be747efa1e5837df8b98a962a01286f0b98fc14f0a92007f9c3</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.4MiB (177.7MB) – 3,322,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3191d215bd3bf49d8c0d1b91059a6a66<br>SHA1: 675faa0b2412ad933f5715d72b7e7381b42301a8<br>SHA256: b6276bba31f44cbba278ae5ffdee71469d04ce037dad2b123a4687e78522b3b7</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>213.2MiB (223.6MB) – 3,322,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49facaa813e40c11ea5eedd73fb50fda<br>SHA1: 6518cebcf217019d1921068322ee3ab9373e5a75<br>SHA256: 9a7cc776adea20b2bd48f34ff26985a9737b9c947961162f9149147ab02c9420</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>167.0MiB (175.1MB) – 3,322,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d03cdb954da98de26be4c47e12e91419<br>SHA1: 5881070558770a2f0927e57bae6ec570cb9d888b<br>SHA256: b14936068992f4cd40ac0217dd2b810886bc70e739c18caa8f6c118cab3cf24f</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>207.1MiB (217.1MB) – 3,322,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f6e4541d32c12f8f2c975b7de59c8ca<br>SHA1: 378e225ce53adcaa4022db937cf007f86d8ceab7<br>SHA256: 1e1d643d1a0045c0eccf125ee9d92c88c5defdb080d7f20f9ca17935ee6052a9</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,322,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a055153dbc5c6670a0cd9a167dacb5dd<br>SHA1: 6baf163677388c338828e7308d0caf2e6830ada8<br>SHA256: 099fd41313ea1c70c9b1afb5de83222d68abfd99c651b2a6dd47ad50452eadf7</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>172.7MiB (181.1MB) – 1,835,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c589411498e62ffdd03d5be3ac636d81<br>SHA1: 7195542acdbaa9188d4063126f3d96d936c8db32<br>SHA256: 4bc8af1a56298ecd90f7ba5d9c5b430dd21ce0dfea8d6a21139f677e176c5e5a</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>176.5MiB (185.1MB) – 1,835,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a93cbcf934528d01eab85126080c3ff<br>SHA1: f38cabe10825c7a9e519cb6d29e7b65de09ccd30<br>SHA256: 0bdafb5c9bb2a01a2323ca3c0461882fb179a766cef5df9aa47dda83963f85c9</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>170.8MiB (179.1MB) – 1,835,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 885c972737a7d41d344c04c2ba8cb692<br>SHA1: 558f92ab2a2b63de122b405025b89edbd9c53c06<br>SHA256: bcad3fdd8c0a1f97560f9fe1b5a06795e416f6080d5857e0d3404671e67d05ed</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>171.2MiB (179.5MB) – 1,835,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9bd4c6a73a454541d821dea91f3e3f9<br>SHA1: 30f65c8b5d9f08f1ae44d25bc6af70c6191e2942<br>SHA256: 716e9236088a4d069b55e7009366fe493973e8253643cc53cee07f9c24868bea</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>189.1MiB (198.3MB) – 1,835,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 553f3843ee228443ce7db7d9abcaef2f<br>SHA1: 65ad884fdb548d238f0359e1d54c673352e717ca<br>SHA256: 79b0d06d1cc561000939135a6384274be1e82513d70d2b1b5961ce0d54b6cb74</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>170.7MiB (179.0MB) – 1,835,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f72babc1669f7e55d59303fb8b98e2cb<br>SHA1: a00157ed49ec3e4a7fcb1c20eb0f8000628b6e7e<br>SHA256: dedc4f2c50ea61042c74e104bf6cecd835be1e57346b1ca764f7c82665f26b6e</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>190.1MiB (199.3MB) – 1,835,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: da2443d5aef95b8dd81ce2c34c6b5dae<br>SHA1: 95dde019606ec9d4cb1b51865e505359a819187e<br>SHA256: 589bb4fc02eb0d4d7ed93bed738fb9244ec99b00c22c3510eaadeaab940ceb90</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>174.6MiB (183.1MB) – 1,835,851 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19c30151c00f1175d1f36278fd49bffc<br>SHA1: 6c4f45d0d0f669e85a54dc7faf62e4513c4dabc1<br>SHA256: dba8318a10ce144891688fabcc3069e1645002de4097dab4935c98990a95e0cc</pre></details></small> |


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
