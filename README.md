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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-06-26<br>IPv6: 2023-06-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.653MiB (5.927MB) – 240,851 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9bb2096352e670856220893d5f6bddd5<br>SHA1: 202e7947305dcb1bc5b4fe9a6c775ed67bf35d5e<br>SHA256: ee5c8d66e73c0e3d283a50d183fc8a9e5abc417a600a44d031f04ba33acee6ae</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.536MiB (6.854MB) – 84,617 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98d9aa9c1ea9a8a5f24b8f3cd572d043<br>SHA1: 9b2d3a964d1e9e49817f1305ec5f077ac87d803d<br>SHA256: 03f6e8407013de1a158b49c26f7d6bd32cae1e3abbc98e72fdb0eb6a6defe606</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-06-26<br>IPv6: 2023-06-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.487MiB (9.948MB) – 402,925 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 579295de33c0371215e21336596693db<br>SHA1: 0bbf8dff9b5c4adea1a64dd1fb2a5c2932de8829<br>SHA256: cbde411a0d4176b8f60fd85e6496916b0eafb74566abca8f01f613a9b4de8b7f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.676MiB (8.049MB) – 99,466 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0692ab50678259cdd3ae95deb45d2258<br>SHA1: b7aa790a4f607bbbc5f8ce82ea7aa5e2c1bb31af<br>SHA256: 49e05ed485d233853e1621ca2fbd751b7cb9fded0e8ca536aa535e70b80d2ef1</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-06-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.14MiB (14.83MB) – 603,013 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b59f236d8439ab6f0f50de88a1dfd277<br>SHA1: 5c10741e5c32b0289b80d994a034f0d57ae5e875<br>SHA256: 49723e9b1e13a24b44cf931f95871310345e8597524a3d42fa7d39e30193490f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>25.68MiB (26.93MB) – 332,478 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8cbbd79d23286a3f54384b19d411a59<br>SHA1: c00c4d06d1aac37bb243b46b50408d6746aef1e0<br>SHA256: 0431990f5092bb2f73e2bdc4e1ae5583fa31e8ab0b3c48c376dcab064d2e69a1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.258MiB (7.611MB) – 310,670 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea16f2b91095213f9faf4261a5404be0<br>SHA1: c745544fc460b4fd9cb1ac68204736bcf9eabf79<br>SHA256: f0ea96ff5e89f5f267e07aa2f74df623e088bcb91f1df0d02845e1c412aeea46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.86MiB (27.12MB) – 334,770 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7634f17216ca6f115cf06e4df5e44bcb<br>SHA1: 60cbd088cb95f3f19ddbebb63ee62aa7d4d5943c<br>SHA256: c3c8f61cd5d80cb8dabda6b047d66bfd6d73c7d0d9eef7427890f9825a480636</pre></details></small> |
| | | Full Location | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,190,306 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f9e88d1ad989b6a665fbfd9d3b82b2<br>SHA1: e1ce63d9dae9f45709cd662cb78d5f323b9caca9<br>SHA256: ca5be0a45d234b5f3db9fd7993ca3b95fb26381d390a4e0d3e8111f2e7922199</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>351.1MiB (368.2MB) – 3,068,912 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4471e6e2accf2b2f3c070f5cb39ed63a<br>SHA1: 158105fcee685e8e94bbff314ca8be8e235b169b<br>SHA256: 82b7025d3a47fff4700bbb503d62d17692265f78fae12837a6995bed2c31d118</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-06-26<br>IPv6: 2023-06-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.582MiB (5.853MB) – 238,084 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1341c73b679015c1849651b02f8442<br>SHA1: 68ca29c935cf40cbfd663086deea4e61d8c8dc4f<br>SHA256: 4124a3662930f11954fa549834f6208912d91c3ddb53382a0c39cfaba1a71bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.40MiB (27.69MB) – 477,002 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2db255cf92eb5224035b1230f0efcc2b<br>SHA1: 4e4c6b67a3842bcdf119210a6676113f6543fa54<br>SHA256: c4335ed7e2c56df30bddbe55d518c81bb73286caae4ae123b4969eca63c72f25</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-06-26<br>IPv6: 2023-06-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,120,022 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1419e77505317334ccdf478ab7daef44<br>SHA1: 1d97a0ac2b0129e4e268083a3cbc23c627acabbe<br>SHA256: 35551439abd88f4346ee7c19bd2da4093eab3273897ca4f28e5cdb1e5d078ee1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.0MiB (399.5MB) – 4,504,439 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e04f9fe903ade529e55bb6b0d36ccdb<br>SHA1: 3f03d09739691bd6ada8c4ee23de98629caf20c3<br>SHA256: 5f023916ba65784e33d23b0934799adf20ae2b5448b40b7bd34e659f96864649</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-06-22<br>IPv6: 2023-06-22 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.840MiB (10.32MB) – 419,562 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f18cb3a7100f628f83609d1ff3bea499<br>SHA1: bd68ae1342d8ce5fa876d4d40409815a2746eb53<br>SHA256: 19be8a94835e410558e66d6db36190f09124ec9c0d94ea27adb66f458463cbdc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>20.94MiB (21.96MB) – 271,103 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5da297b4fccd432573d027023f31acf3<br>SHA1: fcf92b791e8717b25bba2cae2158f72ff5ccc07c<br>SHA256: 3087fa6b41d9c71da24e3128892f06905be2bbfa5980538ac0451a8c07e2f141</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-06-22<br>IPv6: 2023-06-22 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>188.9MiB (198.1MB) – 3,763,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e8afcf02aacd985b6017b86065d7757<br>SHA1: cbb26ac60aa09a22c2978d197bf981ff66cbb18d<br>SHA256: 7daec5d203f62497792cb7c40fb8a151fe07905643d205d9555a0a1864300da2</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.1MiB (231.9MB) – 3,763,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56c56830679c2f16ed445810c6de0bde<br>SHA1: 543a0f86ab26fb708e1ab9d871a05b7b5e62de66<br>SHA256: 3eee200849c7d82d5b1c705e8e2cb827ee81fb3517ae9c1af25161076b3193c1</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.7MiB (205.2MB) – 3,763,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5dd0e4a2768190de2f5e14f3a1b8100<br>SHA1: e04dfd03a6177ec56da5a9eba331c59fee0c71b3<br>SHA256: de5fd212daa36c1dfd7b1972f89dfb2600ddc3760f905f62c45161bfb9eacf03</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.6MiB (212.5MB) – 3,763,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2373cf3ea3f9e74b82a80a93d4e3d3a<br>SHA1: fe0a4c094bd65c2c7a0e2cf4a5afaf604974c434<br>SHA256: 0802c57a97410016ac7b7124859a8e90e4e1847709ca81146c09f1674ad0b9da</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.0MiB (249.6MB) – 3,763,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffeb2639753101c895f26ce8e4496ac5<br>SHA1: cb08974d4d904f7cf15b5c00e046fcddc6cfa77f<br>SHA256: 3c8858757043fb9be5c26913d8df0396bfb1a2e09015e89d15246e62eefa0644</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.4MiB (199.7MB) – 3,763,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f183c2553f1335c0120a575212db150a<br>SHA1: 00e11b8af09602d0d89e50899fabb10c2362af07<br>SHA256: fe1ff8236a5666c66c959468a39bb69198f927edf34cd0c4af568a10b70e047f</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.4MiB (250.0MB) – 3,763,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7e3b6c836d9f0a1df84bc6d6356ef8b<br>SHA1: fe5f20023f4275a26720981ba2d0207982d3c427<br>SHA256: 5fd73b2db76e7fb4b83fef5f682bc146faeacb8f33dfd3ff84b1cf323f374c55</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.6MiB (212.4MB) – 3,763,248 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbc99692634b79cbcbe6f113c833e286<br>SHA1: 5b0de2176214d48c6dba36b27f155f964754fdf7<br>SHA256: 9c016f08887d82a41687b5bd9cc667d55222864c250802fd44213669de6b8ef3</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>126.8MiB (133.0MB) – 1,264,410 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a70463fe68f427119bdd2cb74c3fc9e6<br>SHA1: 1cebbcdbdd52ec3fdc51c5573d6dffa5dfaa7dc6<br>SHA256: c8cde3748ad59dec512aaa7a47faca3a3e9f6506738377d9a6797252fee249a8</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>134.9MiB (141.5MB) – 1,264,410 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1b79524e11d17a0a218fa9dc3da6eca<br>SHA1: 83bf66f44d7b62d22572fa534039ec675ae55f07<br>SHA256: 2d09116c9103c3c10c44dc1356e406ed36a66632a7cec577453bf6b39376f4bd</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>129.0MiB (135.3MB) – 1,264,410 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e40561bf06a3c197769b21a5d6f1de81<br>SHA1: f7e168e5eb3f9009ccbc266dc2b0ee962d9bbda3<br>SHA256: 156cc9f0326860ed4dca89435dd0b9ecd37bf0c4aa9b841321c8f0b64b847545</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>130.9MiB (137.2MB) – 1,264,410 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fcce27600e3adb7d84bbae1e014df5f8<br>SHA1: bfaef4b725b8e5ae842ee4da8e37a6845f94ad6b<br>SHA256: 113392497c5079a97a474c4a88b855b22d7066ba69bfaa8ca4f91b681c26b535</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>138.6MiB (145.3MB) – 1,264,410 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab9e87affea4f907db532564fcbf379f<br>SHA1: eb96f0895c40eaad8ddbe5858f4f867568c3a72c<br>SHA256: 74db0ceb9b2c3f1c7cc66938f272ffdb7ba64901e6cbd09bf18ccc076053ed77</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>128.1MiB (134.3MB) – 1,264,410 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c390cd41bdb93aa6fcadcd452a1abf5c<br>SHA1: fe18e87f652988d6600b6eb7936c4e7af515518e<br>SHA256: f06d888158b965b154e55fbe58677d4493319d282a14a7629710e484dc08bd4a</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>139.0MiB (145.8MB) – 1,264,410 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3758b68618c70720cfb1ffd591abe0a8<br>SHA1: 6c1ee2943f802e89de4d62ad0d56bf151820e2fa<br>SHA256: 577caa265bebad71d8351dd37836a0f6cb2a6ba64b40044dcade1e038386d5ea</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>131.1MiB (137.4MB) – 1,264,410 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e48e43ec5566eed4bdd8fbf8b29ab6e6<br>SHA1: 2d59e2ea5e05f0c4872e453b2c7ad595c23c5775<br>SHA256: 90bf1d8fdafdb300280eb96f51e78d75584eb8c0fc0c070d13d93126e0154bdb</pre></details></small> |


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
