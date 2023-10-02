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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-10-02<br>IPv6: 2023-10-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.615MiB (5.888MB) – 239,177 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c2b276ea5a6c4264df28a0a4b47bac7<br>SHA1: c615d1f23d612e1a3fc499b477060e708c1725a6<br>SHA256: 09aa65fbe65d06f947a01b4926f3e93f5013c1db70b741a507097d3874f13c31</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.259MiB (6.563MB) – 81,019 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a35be2a44590dc26fb6ba82cdd94ac01<br>SHA1: c02faf39196d19d136ed6de3ec3031b46e03dadb<br>SHA256: 5cb0ad90d2beb980d0afc2836faa9ec2abd5eb5ceae088b302c53ae61972b86f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-10-02<br>IPv6: 2023-10-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.587MiB (10.05MB) – 407,217 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ec1ece7c0ad1c4362f352f3c2d97b217<br>SHA1: f1bf877595f4d410d254f6b3edd96bb74104a602<br>SHA256: 2ff4757fb6697e3ab7d1c4cd75ff64f34ea389ffae014e03d63956dc53c3d63b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.017MiB (8.406MB) – 103,879 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f330073ab05205229d39edd986975b82<br>SHA1: 18710de5b3065035033bc57e231bba36a28f1867<br>SHA256: 8137dfebc70040eb493ecd7680ccd9181d703430fae41c4bca98f04a6d63af57</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-10-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.60MiB (16.35MB) – 664,961 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34d66c4608a11151f0c07effb2cd09b7<br>SHA1: 65021131a4163e7fafe1cdf53880078aea1baba5<br>SHA256: a1e78bbcf3c499ed5580e44781981307a2b018fcf8c62fc50e1da6a2522f2bfd</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>36.25MiB (38.01MB) – 469,316 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1370b5d4d34e2b678fdbd0b03bc6943<br>SHA1: 8d8bbd466ae696bc528c958b63709481bd7c8359<br>SHA256: 03965b163cdc194a5705d019bbb5061dc9ebcd0681fb6b98809e27707d250112</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.207MiB (7.557MB) – 307,820 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ff8d81d8ce4efd3476359318175af0<br>SHA1: d105d1c4490b536a83d0461759256799109a17cc<br>SHA256: 4cb45f08b0bbd6d6c4fb204e776835b939ac663761aea652d12ae2ab20494228</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.54MiB (27.83MB) – 343,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3256ab7e4df24ca9917bf92c70b9ce1<br>SHA1: 832b96b707911579f91d2a42cc84b0766c5db738<br>SHA256: fdb03997e4b7c1a6bdffa274673b7756d8dbfb2ede55f1186b3957ade7042544</pre></details></small> |
| | | Full Location | Monthly<br>2023-10-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>184.9MiB (193.9MB) – 3,048,591 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed65f47a5f866d476bde81f05015d0ad<br>SHA1: b0ef2e2cdf8875da35c99816df76f9fa88d3de9e<br>SHA256: 5bca8efa9618ae69c9fe4228342c0ec4bfb4d581ca0766a3a8e45978d1fe7875</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>269.4MiB (282.5MB) – 2,345,213 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f854d9364b9ab55744dfdc557c9f9f6<br>SHA1: f419e9a0b9db7b3c78b5c98927c74c8427f3fcd0<br>SHA256: 3d1595b762a094dfd2f9ac1525dcc77a67ac87dec747f420b0fa63ac4fe51cbb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-10-02<br>IPv6: 2023-10-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.547MiB (5.816MB) – 236,500 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4857bb88f1e540efdbadfb3e56c208c8<br>SHA1: 0190e03fc0543a58ca868f0f36a92556049db942<br>SHA256: 44b7a5f1e09f7ad797ea8511ecfc8ddada844067bdff82f4255273d85906d172</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>19.24MiB (20.18MB) – 249,120 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5105fe9bbe5d0ddc9bf8995e1cd8fdca<br>SHA1: 48b9366c0983f8d70d79ad112999057d17d64829<br>SHA256: c10da1d1999f1867044c9753957966c4989400bf25df0e7fb02c524b43dc90fb</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-10-02<br>IPv6: 2023-10-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>171.6MiB (179.9MB) – 2,803,356 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4abca24edbdd7d97ffaa621ecb9327a9<br>SHA1: 97c24a0d18b54cd8d2692e708765b79162107242<br>SHA256: 903407a226a3eb479f2165ba004762c64c3a41dd5a9c0d515be1353f99e5796a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>166.3MiB (174.4MB) – 1,448,721 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d928761a3b79f2ef6c55ec6d4dd813e<br>SHA1: e7de15f34cace41d4332e3d59c8ffe729fc2f8ec<br>SHA256: 613e34be98c76eab733c9982022bfa16a5d1ab57fd73444f0d6e8a2ef59ae567</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-09-29<br>IPv6: 2023-09-29 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.15MiB (10.65MB) – 433,307 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca3d749789782498cdc1137ba74f7e71<br>SHA1: eadd9f68eec153133ea63968e5d6165c0b0bd934<br>SHA256: ad34bd565097a0abb353f0730bb3f8a6dfddd3bb54a4944493bd393fbf3f4a58</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.20MiB (23.28MB) – 287,453 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d5a361c71b4fa01f781a6e000bd8305<br>SHA1: 464ef72644b0850d03e7d777767a819535c1cadd<br>SHA256: 128a90db9ed3cbcbc768f506ec717e608f3a8cef0cd45698eb77db300e1fa93d</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-09-29<br>IPv6: 2023-09-29 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.2MiB (199.4MB) – 3,794,818 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1241379b1cd2c509dcfa82cf2085ed79<br>SHA1: 74bdc6591bee71ccb9b95d65feb73041f1342799<br>SHA256: fb7db6c1530bfbde3f38db794ad4e97a67a0aff12c313155a25bf9031206ba97</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.5MiB (233.3MB) – 3,794,818 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98528c2a68081392c57b74f19752b210<br>SHA1: fb8aa93e1642c6415d88b5e167736a56b244092b<br>SHA256: b6767d4c5f1895ae2b46c116b67a2b88692957ee0a846a6362e25ce22a7b2f23</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.3MiB (206.9MB) – 3,794,818 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1916f82d45d3cc2cc6f7ad3ea2e2180<br>SHA1: 2a2869401010aafa0c4c0abb4d277e9f070b2df8<br>SHA256: da5d08e245e539031da06b7fa8997b602121ff2c04c25bda4f5ad8009da9e4dd</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.6MiB (213.5MB) – 3,794,818 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bec054338bda353853ea840337c7350c<br>SHA1: d79ace7f0faf7656e011d82f557160a81655679a<br>SHA256: 9ead2f599dc586505cfd1e9fd2a2a6c0122e8d9c85feaa7890823e05c3a15c57</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.3MiB (250.9MB) – 3,794,818 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcaef38f4121f9c4a0dcc47ae3b8f670<br>SHA1: b53a93b4b3637fcd4e9eb49c80821bc747de0383<br>SHA256: 908c876375e7dcef5dc44e39580fd11d4cbde1de25b2c0aab0973350549b1024</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.6MiB (200.9MB) – 3,794,818 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a43e37247f9216b68df0b136874da6c<br>SHA1: e132a202a88367ddb2677ce286ad6429aa35605f<br>SHA256: 9fc63e2a88090498f780288e15256a47ca7ae72c05c0be4cc712ee6500e812ef</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.0MiB (250.6MB) – 3,794,818 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7caed017f7b5df40d9fd06f71c1b629<br>SHA1: b65f4cbfedddd6d2faab9eaf707b5ab949584322<br>SHA256: 7537c865ecb56e9d31d167ee92173e77af44bc266289d98585431c4cd1c3cb06</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.8MiB (213.7MB) – 3,794,818 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a97918f443a646ea998e1498afe5ae8<br>SHA1: a32077f694a0e3ee85de3057780aece828242035<br>SHA256: 0de47eae0fb87a2aab711a83eb28f535fdb064212ee4618fc4eaa15d043e02c8</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>132.7MiB (139.2MB) – 1,323,278 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6b78cdb65133b1672cd77c670626573<br>SHA1: a3ca6ad3683c4f23a885611464ea4b78fa463a02<br>SHA256: 5c92f0b1ee650c250878da6c97f378b73447658593e51f6ea0aeffee38bd4deb</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>141.2MiB (148.1MB) – 1,323,278 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: edf87e7a7bfa5c936114f8d870a10beb<br>SHA1: eaf48fe124aca80b47fbfba25ee935cbbdd15c21<br>SHA256: cd1aa9b8461cd83eb0bc05c08ad24e747377d8af8a767fa5fd5f12be2d059923</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>135.2MiB (141.8MB) – 1,323,278 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90043bf3bec544fa9ed977e3db1ecf67<br>SHA1: be53a071f507b0eb6acf3fb5568ceb72922cf776<br>SHA256: 0d48bf4d7945189618e08fa3bb448bdc082994cb931f14e9c97bbeeea27cc6ba</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>137.1MiB (143.8MB) – 1,323,278 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2930b73e20bd5074c9c5a67c95faf71<br>SHA1: 7be0960c9a4b1ee228da990bb3d2ac20045ebeee<br>SHA256: d455823e0ce68ccdc4fca1adc50e6f232e06467851696a5f6d608fb00098f60b</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>145.2MiB (152.3MB) – 1,323,278 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 333f6749a63b0807b9d0854c1c442f2f<br>SHA1: 25aab244cef8398dc4ea7dca957914dcf3535c02<br>SHA256: e8f830fc2cc744dc794e3bc9ac4fc212e92b644c8f7d60c941ede61f094e6c00</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>134.2MiB (140.7MB) – 1,323,278 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ac8adf7b80649a4c926e8684e073632<br>SHA1: 4fab4baa70598ec5d132685852a827112f093a10<br>SHA256: 4c34616042fe5ebf3d1e21b93906828eb0f2639205407ab32c09f9f7bf749287</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>145.8MiB (152.8MB) – 1,323,278 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c30bcaf7f1dec8ab2da30b4c7f56bc2c<br>SHA1: 6150a75367bb7fbe867d6f82b4431ae09a37047f<br>SHA256: dab43dc16557cb39ddc36d0931b79e50f332e116f1fea97fca9db405ecc66e3b</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>137.5MiB (144.2MB) – 1,323,278 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fc4b79ac871cd288664d165a85979bc<br>SHA1: 55d55caf7c3b336bed2db447ebacc30274a94007<br>SHA256: bb0a8c71cb55338e023bd3e870a5c993545ab8576a99e3e6c17bce2d2390b4e3</pre></details></small> |


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
