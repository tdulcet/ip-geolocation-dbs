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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-10-24<br>IPv6: 2023-10-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.614MiB (5.887MB) – 239,141 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc8ec3c6380307ea1aa872c4b29fc7a0<br>SHA1: 54b6aa1450228898b133647a8864269c04643ab9<br>SHA256: 1fecd475891e097d9af38dce6ddb50a93f0511a2da4c5d4b3202ea6491cd3a04</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.368MiB (6.677MB) – 82,436 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36d9281205ec6fd9d8a6ac4a2d1e60a2<br>SHA1: 1e3236d12cc938afcb715f14fe5150fb13c2bb24<br>SHA256: 09117303350d588b9533b1b6fe0caba9e340ab3cf6eb91023d6d8bc4f0c9440c</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-10-24<br>IPv6: 2023-10-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.627MiB (10.09MB) – 408,922 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a110f4fb845f41eb92b3acf21593994a<br>SHA1: e18385eb1ef5697954ed27e8944d8e58da206201<br>SHA256: 604a32e3fb7ffd9c366460caf1885b4c7c13c500a476d1f33c530b639925b536</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.112MiB (8.506MB) – 105,107 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0659d1e45e2d8f20015e80bb675857f4<br>SHA1: e49598bf24d12ec664d890ee937d62e0940de56e<br>SHA256: ba7ec8e0b6149dc38a9dda655a1b47bf0ecffb443af3f5ab7bcb08151363024a</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-10-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>17.81MiB (18.68MB) – 758,424 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32b14ef528077dc013404f3c0b9362<br>SHA1: 21d84b481ae6276825310b0015652047ba8fe50f<br>SHA256: 61fc14d0430b805a1c6b8c9823c703191c6b8659add122f1081482b6e5cc72d8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>43.30MiB (45.40MB) – 560,497 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31a60733bb02d90941b76b8cff230884<br>SHA1: 94aac79c5d8c371f8755d7ed9f8a86de89bca621<br>SHA256: 2fb297bf2a25b8a7ce34b2e86f301abab8e3bb47d4aef751730a38fbd522811a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.207MiB (7.557MB) – 307,820 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ff8d81d8ce4efd3476359318175af0<br>SHA1: d105d1c4490b536a83d0461759256799109a17cc<br>SHA256: 4cb45f08b0bbd6d6c4fb204e776835b939ac663761aea652d12ae2ab20494228</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.54MiB (27.83MB) – 343,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3256ab7e4df24ca9917bf92c70b9ce1<br>SHA1: 832b96b707911579f91d2a42cc84b0766c5db738<br>SHA256: fdb03997e4b7c1a6bdffa274673b7756d8dbfb2ede55f1186b3957ade7042544</pre></details></small> |
| | | Full Location | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>184.9MiB (193.9MB) – 3,048,591 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed65f47a5f866d476bde81f05015d0ad<br>SHA1: b0ef2e2cdf8875da35c99816df76f9fa88d3de9e<br>SHA256: 5bca8efa9618ae69c9fe4228342c0ec4bfb4d581ca0766a3a8e45978d1fe7875</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>269.4MiB (282.5MB) – 2,345,213 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f854d9364b9ab55744dfdc557c9f9f6<br>SHA1: f419e9a0b9db7b3c78b5c98927c74c8427f3fcd0<br>SHA256: 3d1595b762a094dfd2f9ac1525dcc77a67ac87dec747f420b0fa63ac4fe51cbb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-10-24<br>IPv6: 2023-10-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.547MiB (5.816MB) – 236,500 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4857bb88f1e540efdbadfb3e56c208c8<br>SHA1: 0190e03fc0543a58ca868f0f36a92556049db942<br>SHA256: 44b7a5f1e09f7ad797ea8511ecfc8ddada844067bdff82f4255273d85906d172</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.24MiB (20.18MB) – 249,120 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5105fe9bbe5d0ddc9bf8995e1cd8fdca<br>SHA1: 48b9366c0983f8d70d79ad112999057d17d64829<br>SHA256: c10da1d1999f1867044c9753957966c4989400bf25df0e7fb02c524b43dc90fb</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-10-24<br>IPv6: 2023-10-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>171.6MiB (179.9MB) – 2,803,356 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4abca24edbdd7d97ffaa621ecb9327a9<br>SHA1: 97c24a0d18b54cd8d2692e708765b79162107242<br>SHA256: 903407a226a3eb479f2165ba004762c64c3a41dd5a9c0d515be1353f99e5796a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>166.3MiB (174.4MB) – 1,448,721 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d928761a3b79f2ef6c55ec6d4dd813e<br>SHA1: e7de15f34cace41d4332e3d59c8ffe729fc2f8ec<br>SHA256: 613e34be98c76eab733c9982022bfa16a5d1ab57fd73444f0d6e8a2ef59ae567</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-10-19<br>IPv6: 2023-10-19 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.50MiB (11.01MB) – 448,012 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4be894287c17a1edef2b4587f74006e<br>SHA1: 90525d02e8e6683b74ed41d5de6c5cb5d9cda69f<br>SHA256: f37019a94e43488014136e2b89e99501956b4ff277c0bc2414f5296ed912f2ec</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>18.61MiB (19.52MB) – 240,936 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cdd0920a3b1c9d83e163b05542a29de<br>SHA1: ac783f8ff45e7e859715d1bb485b34129e36664f<br>SHA256: 5fd45896a0ee1926cdc0e205edb220970770ef1071bf73a74c1f6d40b28e9a00</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-10-19<br>IPv6: 2023-10-19 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>196.6MiB (206.2MB) – 3,910,782 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47a558823947609599d8c44b5e17f430<br>SHA1: cdcae62d118c9fb2c850d861937da3ebe17b6254<br>SHA256: 5dc8e7d03da04c20d2ddc1d3d93acbeb92fae43ac897d7b68fcee47c6eeddb81</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>229.2MiB (240.3MB) – 3,910,782 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3228c706b7de601d508fd03b93bb2acf<br>SHA1: 83fd5d971c95454551a8198ef8979f9a6578ff6a<br>SHA256: 7435d1fbd6540beea6c0cb689037615249e5915b40ccd95cbee1c9dd7bc2047e</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>203.4MiB (213.3MB) – 3,910,782 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab4ad8671f32680044db534edabc1d96<br>SHA1: 8242a12a8439a8997f0990a43588171f32026ce0<br>SHA256: 923f415864180e8800d7fbe4b3b7d764cf0ea5abf37d3c85cd6db1e77b35a256</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>210.0MiB (220.2MB) – 3,910,782 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcdc5303f38236fd241844f5f5fef6d5<br>SHA1: 3bb92d56391b97f15cf6bb32419310a5a41cb563<br>SHA256: 76e7e07e0ee8ec8e3e4af6ef1fa0bbe0e011f7d578e272f3b40be6b91885e117</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>247.2MiB (259.2MB) – 3,910,782 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72eec574a16052ccab4b7cffdc99ce77<br>SHA1: ee05f152dff1e8ae3c504a7be9e5a20f18f76380<br>SHA256: f414f32232f1b377e2fe695ccb2aaf381ee1c160b0438e539499d491143afd35</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>197.7MiB (207.3MB) – 3,910,782 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99be8fc89045a5bdbb74a7821ce85b1c<br>SHA1: ecdb330a143b6202d88e9b50232af0417cfe3a33<br>SHA256: 3dac381acce3e76be4055f93d41d229b3d3662dd07274491f53bb751936f9cdb</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>246.8MiB (258.8MB) – 3,910,782 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1fb87f46216a1c27275696b70c0827a5<br>SHA1: 78a71bfa9f3b3ae26bad481cb19f261353aa5f92<br>SHA256: 661df08b68556bff3234adce65a3fc17e6e171990dcbbad014cf5d229cec7f54</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>210.1MiB (220.3MB) – 3,910,782 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83317deeb9a73381c222d4b7838b29dd<br>SHA1: 355cfae349773d41aba4f77d2615918634ea28bc<br>SHA256: 968147c931b184677cc5dd1ecd701e7fe1d03f1c07cd8f9f6128e17fe996c27b</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>121.5MiB (127.4MB) – 1,207,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aac46d66c8f47bb11b4bc5e1ba9492aa<br>SHA1: d10abccaaf0f090384f8ebc63c09e06a6e37650d<br>SHA256: 13fc12eb41611f576d2d159edbdc0eb0ede1becdecd84e5d35bced923666d708</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>129.0MiB (135.3MB) – 1,207,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc15acf36a6c72523561205447884229<br>SHA1: c5ebc68470375a7098106aee843cadf9d5b024fc<br>SHA256: fb1af6625028d3afe3823494102e737a533f44b75054e3a8bcdae19d86b1b172</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>123.4MiB (129.4MB) – 1,207,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b09991a61437066de90994dff2eb0d5<br>SHA1: e2338ef97168ccd517b19fa66f5291b528c5b86a<br>SHA256: c2f515ca49c1e7d3a8d4aafe87344a46a66c9bd84befd786d09e469a7ddff401</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>125.2MiB (131.2MB) – 1,207,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 675a9c042aa4b1e5a97bf6c0326f5fb5<br>SHA1: d34138ef56a131d177798cba2dd16823a5d81a2f<br>SHA256: 1432b310292f840adde75ac612711b1e79b7c81658f951c35771e1f36484fb15</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>132.7MiB (139.1MB) – 1,207,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f64911890b76b960e189e771601050cf<br>SHA1: f07209cd4b7cd30b9673c6422603eaac7a411dca<br>SHA256: e2cad5bf1d3839a7cfc6fb9ed771fac35639a4deedbe659b492fb109d5fbdac8</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>122.4MiB (128.3MB) – 1,207,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 547e78596ed8b1caabcb41ddd07aeff4<br>SHA1: fe6583242fe0f4757f4ede946c6ed14abe8371cf<br>SHA256: 13577e79fa0f122e6f7de24de649c93e5fc1fc3d6de7d8fea486fc54e2ecc720</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>133.0MiB (139.5MB) – 1,207,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4e8100b9178f3098d00a2821d3763b0f<br>SHA1: b7631d2237ba56eb683e4517c182f92815a79eeb<br>SHA256: 6f3094b1ecf11dbdf72851c5fe49109af665c82f5ef4febb2069c92a9cf5c533</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>125.5MiB (131.6MB) – 1,207,600 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab06b988b8ef6f0c26b3377d45638cf8<br>SHA1: ced8a73a694c09e9a490cc403a787b061d8e75cd<br>SHA256: ed79b5e9dbb2a2bb6d176339fac851649dae5b04713e80920743c657f6fc576c</pre></details></small> |


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
