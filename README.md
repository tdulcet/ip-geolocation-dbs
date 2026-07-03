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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-07-02<br>IPv6: 2026-07-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.382 MiB (5.643 MB) – 269,313 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 560e5f4283fae8304e33b3f33cf533fd<br>SHA1: 4ae19ce36067d955f96eb63a165fd77578c5af3e<br>SHA256: 38edf8404f620c9a071d6d8b2c77977e346cf8f8a5b2618df00c8edb43739a2e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.74 MiB (17.55 MB) – 254,406 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f76436280bb8ee34d79456988e515381<br>SHA1: 85821ddad40152d20b5d9dbbcedea6830fc45f73<br>SHA256: df22a367696664e57936a74a4dc8045a0329a9d9c0dc0624285802fb9c767b46</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-07-03<br>IPv6: 2026-07-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.026 MiB (9.464 MB) – 451,917 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32cfc09ab27283485bd13520b1af8a59<br>SHA1: 858a201325c17ce9f9bcaea4b3898972f37cff85<br>SHA256: 6780739c78ff4726ab73b78ecad2ca8a80b1a1743102f725a9d326dc91225e05</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.915 MiB (8.300 MB) – 120,399 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a232103ca0e4ac09afb44705b8804d1<br>SHA1: fd2a62f149293aee2dfb91cab9b55cf75f949a05<br>SHA256: 2089e31a76123a8d7c4f3c5507b4e1cd16522fc9516d7a20e1872cb689521d0c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-07-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.30 MiB (12.90 MB) – 615,914 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d95965d978bb695efc53aae226ceebd7<br>SHA1: 17f4f3220cc9da0d0229ecab2516d6bf3a73a1ab<br>SHA256: 42f1595faa48c256c753dfdec1fb6bcb07e1cb42e66e1c127f72130f09b51476</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>42.12 MiB (44.16 MB) – 640,042 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a52f289087b4ea59c8bceaa4c03fc359<br>SHA1: 828ab53beff815e5a72e54d0e62d09d7fed8d879<br>SHA256: 108fc0e15b26bb8a9b9ff56a74dc636cfb4fd5fc39a77a3e020f1f7036469394</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.078 MiB (7.422 MB) – 354,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ec835290735187164b1f2f622ad9c0<br>SHA1: 10464ef5eb489f4745096b1c71046b06409244b5<br>SHA256: 6bc4af63c1e15b4d99d5b9dd9cddeb67bbf2eafc2529ba5d9ec4525e0fe7964c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.51 MiB (23.60 MB) – 342,046 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569d0c6b66a745289f0e152318090f38<br>SHA1: baf1ef75355d41d9bc4380f97ed3b085db479655<br>SHA256: 8940a06c7f9a27f129048c5a7a0b1579b368020d88f2d2efe0fc813b6d2f97e4</pre></details></small> |
| | | Full Location | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.3 MiB (219.4 MB) – 3,666,805 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b729ab459cc2b765b3b4ea035f481b<br>SHA1: 1496af12b72ee784e304cd84eb7335c826bc3906<br>SHA256: 69fc5ebf5414a7a939fc25a35f3128451cf340211ae51ab9f82d53a331d8ca03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.3 MiB (473.3 MB) – 4,386,528 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f197b2ebcfed77f9adc3310fc7b6020<br>SHA1: 24b1454a40fdda39f37fa9367a6a6a5a88d3be33<br>SHA256: 0160ad6b5bca3517eb65f79d6db1f9e373eeb34cfccbf189a588bb330d17af06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.663 MiB (5.938 MB) – 283,439 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5e0b2b6a8aeacf3ff5598adb8880765<br>SHA1: 8804233331909b27cede1b5b43c2f97e3e0fa7fb<br>SHA256: b76b958024d8951ae29a80cf988f69d1e662dcc0bea8d923f50bdc702ec7cf2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.09 MiB (23.16 MB) – 335,708 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a285d07eeae37dd9fc478666744fc01a<br>SHA1: 088c9efb11f726ab15157c87e8ea1f653a7ad960<br>SHA256: 276a36ba7f5863bec8cfdfc9f38541e0dfacd40d41312852daaca8be67b6585a</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.4 MiB (176.6 MB) – 2,914,372 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77a6d0d39cccc6773bd841068fea21aa<br>SHA1: 2b573d6c293a367a2052b0737018f62a9b4b74c1<br>SHA256: 63c79df13cea9f7d90cb141a952a0ec792fe5f5c39e6a4cb98f1caae5055b951</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>295.0 MiB (309.3 MB) – 2,857,634 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78f9a0f50b954077a7222ec29768405c<br>SHA1: e7cf8076d18ce13f2ca1ddb68037263adaac2c3f<br>SHA256: 8eb07f6e7f6d570b63e6735ef434d9dbfc7a394946b35bb3ecbb67d2c31d9863</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.42 MiB (11.97 MB) – 571,770 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e32ae1d5dfa081a57bcf2919c867a7a0<br>SHA1: 54de9e9e90846925f805a099e43b1fe5e2915489<br>SHA256: e15e2f603ad71441a0a7155153123ca8887a1aff93aa9223627249e3ffb441ee</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>36.99 MiB (38.78 MB) – 562,094 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd7e551977e4363abd269cdea1242e3e<br>SHA1: 2a5b042bc075532120444a50093dc9bed11dd932<br>SHA256: bb883059a05167a6c300df0fb40ad5e545bca523c09603b08476c03c4ad57ab4</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-06-30<br>IPv6: 2026-06-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>192.3 MiB (201.6 MB) – 3,750,616 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0d6e36978ebc5a2fc8c5fd2752974eb<br>SHA1: 0675734fd69fbe7ea33929f3d20ce52d9587e630<br>SHA256: bc3e12d4000c94633ee4eae83422d12f28e029ab1c4da801efb35276a9602ecc</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>201.5 MiB (211.3 MB) – 3,750,616 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fd5008140808790137f6b984562612f<br>SHA1: fa8081214736e7dfd85b0777fe62d5899ebbb90d<br>SHA256: 694441d378e00b10c73ee841c85e6ef797fffaa032118d88d108b5082bda559a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>191.5 MiB (200.9 MB) – 3,750,616 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2176794b8e2f2bfb36895c4ccfbfb49c<br>SHA1: a1efb75e7009d194326f0d56b11f45491c89f147<br>SHA256: d53a4bee799128be55ae0ad0cdf88dd9767019d6e68e0a64c35501cb6f21b76f</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>193.2 MiB (202.6 MB) – 3,750,616 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d7296b949d133a3929b2033743ffd26a<br>SHA1: b6012930529975ecc3bd25a92d4ca327e757f307<br>SHA256: 53f23f226df19a570140ceecdcc5b5dd27153c83731bc66e86ece58909c6c875</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>243.7 MiB (255.5 MB) – 3,750,616 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74b414f8d79b1d90a9ee7e843340b206<br>SHA1: daf2f9a28e62722a8ae5a7d072c1137b829b26de<br>SHA256: 17801780e3e2a470a775c14bfaf4e4707f34fe7f92a62235247360801f01de70</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>190.8 MiB (200.1 MB) – 3,750,616 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cf8c65ff603f17c2c275899c0273cfc8<br>SHA1: 69985bea23d4380994cd94c2fe26087e46b0ac2f<br>SHA256: 7c964b45cf659c24b958e04536fe58e3c0c9ce85fd7c23678ff9834260ea9e58</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>233.8 MiB (245.2 MB) – 3,750,616 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d16ca55872f451d036ce1fada3fe74c1<br>SHA1: 7fe94cc235355997bed781dacd3f3e83fdc90d57<br>SHA256: 4eb81c7153ee36883338971e4e1cdca80fe43aa6d3c1f25178fa7d37f713da6c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>196.7 MiB (206.3 MB) – 3,750,616 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56b29702baa8f8dbad72b9d141c1e3b4<br>SHA1: 86184db091ebddbac118770d164b9d8633bd43b6<br>SHA256: c541a735042ef2e2ca92ef8b72c41d41eb8101abbbca7276d4b80a65cd4e9002</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>195.9 MiB (205.4 MB) – 2,057,116 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56bc428d6a86a74304169948953f9d0c<br>SHA1: fc744cc5689433a09f04961372f3e53c05340b2f<br>SHA256: 63f8752bb78b72df1a3e1d16fce7ec024a6b4ad18fa80af1405bb229d6680ecd</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>199.4 MiB (209.1 MB) – 2,057,116 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f403e00a5b847e0bfcc2624f58584abc<br>SHA1: 080b96fbda4d61c4be2215449ed5ff63e7a8ade6<br>SHA256: 8085a4cacca614ea6a7f5592bb067596cd31c9187e0121497b09f56e8adaeeb1</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>193.7 MiB (203.1 MB) – 2,057,116 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b140cdd9fd6528f51fe142c872361074<br>SHA1: 82fb4a09953d4c77d5013a368a6863745dd446e5<br>SHA256: 3c6ecca3bfb25f22dc1c383a208565368206286ce661d4925956676ac46ee553</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>194.1 MiB (203.6 MB) – 2,057,116 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e4254f9732b6158fc97ac3f179f1fac<br>SHA1: 99ebbc615e1227d07bdb26ca6f7412a9eb026f1b<br>SHA256: e14bc41c53361cfdb452b8f5d9b4508f0262f9ef26afc2a65580888a47ad184e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>216.0 MiB (226.5 MB) – 2,057,116 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8f1dfec7076dd704ce6ca808c983076<br>SHA1: 6a15f6bc119b51b1018b9962c71ec5ae66f82d71<br>SHA256: b4b5d23c2c6feb2610b390da4dcda37be04792b8a328e2c373609a047e82fd6b</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>193.7 MiB (203.1 MB) – 2,057,116 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7995015936ecb87cad7647302b01f4f<br>SHA1: 872c2fc770390271e55d620f5775e3b6d5f76567<br>SHA256: cf67700a649a7788ded7fcdab8f508494101f283d4a6ef38f1e01774706e338c</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>214.5 MiB (224.9 MB) – 2,057,116 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 663c6046f263db08338f8d257818e0b3<br>SHA1: 1581c9f062e025b00df211ae838e984865045256<br>SHA256: a0696058612b011f712b1e0712349c746365090a8fa88f852797b2de073fc20c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>196.3 MiB (205.8 MB) – 2,057,116 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 831a99e09fd855ef833f21457c381b6a<br>SHA1: 2f8c2789c83420603067dc7c56df1d44fceddb49<br>SHA256: 984b7fc0e7f0d420a9dc8f1a667e9b01d7a667d532e309fbd94eb1b202de6017</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
