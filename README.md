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
Scroll right to see all the files »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-06-09<br>IPv6: 2023-06-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.860MiB (6.144MB) – 249,539 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c3fa12e3ee5087f406fdc8f7f615a73<br>SHA1: ca73495b7e187a0c0cca6fb4652dd19734494ee9<br>SHA256: 995e818c19bafefbe368f0b6b7e1018f7bec80c5a2a87b1d0bf1c233967c3b89</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.522MiB (6.839MB) – 84,430 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cfd11b435b50b85c832c13d4861acd01<br>SHA1: 8d812861b7ab7f48c1a06f83a150536ffa9b7db1<br>SHA256: d2bb855f1f42324f9de778f9a0935ef5d3cf93377e07a34bdb4dec3389e73779</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-06-09<br>IPv6: 2023-06-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.480MiB (9.940MB) – 402,640 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 095f9ae30c5ef7ce0139645cdb326992<br>SHA1: 6bd79b66701990b3155439a78a2c981e944b013b<br>SHA256: 73a0d81e382438008ea72ca767e1c2ebaa938d9d07e1e77e0d06d4fa6f798bb3</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.637MiB (8.008MB) – 98,966 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3d21948ac00eaa8d1b0c32145fcd18b<br>SHA1: e5d459b0d9fde144760167cdd233e0f74b085859<br>SHA256: 5fdc8649075a97cfe9e5d9e3cf7b01472efe2b1361e580588041a511da652927</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-06-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>17.22MiB (18.05MB) – 733,751 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d8b1201127f9e66eef92a15bb4d42323<br>SHA1: 6942108447d7afe1141ae97626a14af13df3494e<br>SHA256: 24eb79e9991830c8ed118a76fce4e2752f8fce3db2a524136b83341b3411bf1e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>23.20MiB (24.32MB) – 300,272 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2cf7fe6dc7ccd284590bf7819c447a3b<br>SHA1: 1f072fe996bc46fd6ec3103d871ecf1dd694e4a8<br>SHA256: 476826d1e6077082f963cfbe1f58531e3107d1c192c61c625ce831f75cb7b0b8</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.258MiB (7.611MB) – 310,670 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea16f2b91095213f9faf4261a5404be0<br>SHA1: c745544fc460b4fd9cb1ac68204736bcf9eabf79<br>SHA256: f0ea96ff5e89f5f267e07aa2f74df623e088bcb91f1df0d02845e1c412aeea46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.86MiB (27.12MB) – 334,770 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7634f17216ca6f115cf06e4df5e44bcb<br>SHA1: 60cbd088cb95f3f19ddbebb63ee62aa7d4d5943c<br>SHA256: c3c8f61cd5d80cb8dabda6b047d66bfd6d73c7d0d9eef7427890f9825a480636</pre></details></small> |
| | | Full Location | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,190,306 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f9e88d1ad989b6a665fbfd9d3b82b2<br>SHA1: e1ce63d9dae9f45709cd662cb78d5f323b9caca9<br>SHA256: ca5be0a45d234b5f3db9fd7993ca3b95fb26381d390a4e0d3e8111f2e7922199</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>351.1MiB (368.2MB) – 3,068,912 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4471e6e2accf2b2f3c070f5cb39ed63a<br>SHA1: 158105fcee685e8e94bbff314ca8be8e235b169b<br>SHA256: 82b7025d3a47fff4700bbb503d62d17692265f78fae12837a6995bed2c31d118</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-06-09<br>IPv6: 2023-06-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.582MiB (5.853MB) – 238,084 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1341c73b679015c1849651b02f8442<br>SHA1: 68ca29c935cf40cbfd663086deea4e61d8c8dc4f<br>SHA256: 4124a3662930f11954fa549834f6208912d91c3ddb53382a0c39cfaba1a71bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.40MiB (27.69MB) – 477,002 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2db255cf92eb5224035b1230f0efcc2b<br>SHA1: 4e4c6b67a3842bcdf119210a6676113f6543fa54<br>SHA256: c4335ed7e2c56df30bddbe55d518c81bb73286caae4ae123b4969eca63c72f25</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-06-09<br>IPv6: 2023-06-09 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,120,022 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1419e77505317334ccdf478ab7daef44<br>SHA1: 1d97a0ac2b0129e4e268083a3cbc23c627acabbe<br>SHA256: 35551439abd88f4346ee7c19bd2da4093eab3273897ca4f28e5cdb1e5d078ee1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.0MiB (399.5MB) – 4,504,439 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e04f9fe903ade529e55bb6b0d36ccdb<br>SHA1: 3f03d09739691bd6ada8c4ee23de98629caf20c3<br>SHA256: 5f023916ba65784e33d23b0934799adf20ae2b5448b40b7bd34e659f96864649</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-06-08<br>IPv6: 2023-06-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.751MiB (10.23MB) – 415,778 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48003e5137d179c30f0685be642411d1<br>SHA1: 88616e144455cf88228a61b0a4cef60cfb225fcb<br>SHA256: 402c692e28248596cc51502f9a28dc3d86274729825da9a8b3ec70a0d3eee706</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.17MiB (22.20MB) – 274,043 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ad65e617402f3d5fa30663c6437f641<br>SHA1: 9c944607b5905fca96ddee5d825b4a40c9789ba6<br>SHA256: f276b200e10d6188ad51210aab7221eee63122177d4a1a0008307bf35c3caa01</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-06-08<br>IPv6: 2023-06-08 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.2MiB (199.4MB) – 3,786,874 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af74562aa4b6bc237d1251a89fd48091<br>SHA1: 4811094a04e8b23b8186f0cad547ad9ea60c8167<br>SHA256: ab2bbed166d459754d73bc7f64969a7759c507e2956f3f59984b11592555bc84</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.8MiB (233.6MB) – 3,786,874 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 590af752a23b9f8ee6ad700ef3399c42<br>SHA1: 1ea55e234e103e88caecd87a2c123428bef13cca<br>SHA256: 849dbea14f6f79a1269ad98b39fb911c4075345dcbb441e42d3c6d0b28048eed</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.0MiB (206.6MB) – 3,786,874 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 208a32d5ebe74fef02ed7b7a8185605a<br>SHA1: 2c399cde76a76de6eb17c3d7fd1f8c6d6402404a<br>SHA256: 9eebffd8220efabc23b9a4aeba7dcb55fa4121ac1aeaf8b57b30c76ac4f8b634</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>204.0MiB (213.9MB) – 3,786,874 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5dab89bb2e625bb702e72c4df69f558d<br>SHA1: 786f8ffb531ae12b796485a0f8936339e8a9e011<br>SHA256: 7bb37b13d461d7b992ed6c668d84f3c32fd26be0c095461af2905a2d4761c497</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.8MiB (251.4MB) – 3,786,874 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 390225d1466e06278e55ab1a3e56db32<br>SHA1: 11b570bc773f0390eff7d449e9763334ce1e0be8<br>SHA256: dc86fd6146488c421408dd356ff4f93767b7f19f9c45129ceddbb2ca9e05f1fe</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.8MiB (201.1MB) – 3,786,874 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01b701bc8795fce6cdcb00827771cbf2<br>SHA1: 76b263d5433169b53bd218734c4e6baa2796784b<br>SHA256: 8234f302aef491c572775218af21bb352f1420f82d73d599df3c75d9cac337a3</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.3MiB (252.0MB) – 3,786,874 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ca31fe29ed73cab562e514b312b7c74<br>SHA1: 590e785b719c06f2b67c2c8400d27d9298724dee<br>SHA256: c0b647ee43f88cf146e891f01f403ec41b7578f97aa935505bdd0e70579f116a</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>204.1MiB (214.0MB) – 3,786,874 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0f70d624343b24cd53b53725af786c4<br>SHA1: 94db20f42fe13a60b25c85c23128d156fe7eb965<br>SHA256: 6f91af3a222bd95476ccddb06e282b0e0c0ec515c792f1b2606baca0b2c4ae2c</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.1MiB (131.2MB) – 1,248,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e9d51ad9fadad037489f5cafd4d00d0<br>SHA1: ec658daf38515ef4f692e43e15d5168eb616d602<br>SHA256: 2e1899264c402d1e2d4f80393ae6f17a18ab2da6f81f68c88144991a90bad596</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>133.1MiB (139.6MB) – 1,248,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a12e3065e0e31cb2e2f79d01f231057c<br>SHA1: 0ab812f1be2685df4d54020f7f7b00abc6f7f584<br>SHA256: 095d984cf365086de23bcc517222f4a711deeaa43e5ce253d203ec267e161d51</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.3MiB (133.5MB) – 1,248,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe346487156e444bca6e4dddf21b26e3<br>SHA1: 28be6caf58eb83b44572c1dd4dd3c4f4dac260c1<br>SHA256: 0ca424aa8ecde59547d461d40a80cd6af7b6d428d7cde48762ec666cf76c0efe</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>129.1MiB (135.4MB) – 1,248,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04a9e766319fd4b9e907054c87179f91<br>SHA1: 060da078d36cc90553d3b607777a56147636274c<br>SHA256: 54ca4b03325648d74799aafcba3b82d510d7b3a99db61164e954893b72c3912d</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>137.0MiB (143.6MB) – 1,248,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d086c6634c6f246cb3cccdb049e63373<br>SHA1: 1f710ad4f6a700a21fa1b9970628b7ee2af378e6<br>SHA256: 6bbb6330f34f07c03a49c1b2d48fe6ee2d075f5ded18c0165fed551d5ac00bd1</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>126.5MiB (132.6MB) – 1,248,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c6e0aed72779a9b59d3d03dd7f289cf<br>SHA1: e9ca097d00759816360fcdd48c93afe8e62dbb0c<br>SHA256: 08feb82227c80f3b0c7a07fc696da2001035507f4646c551cc764e78651cf989</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>137.3MiB (144.0MB) – 1,248,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a5dd7e4066dfe57f4ac8b620cc29090<br>SHA1: 0f0eedd8af2a0d17c3e9ff7514bcd76986b7274b<br>SHA256: 216faf831a3adb0cb1d131ee70c50dff79a2279a009aaebf11bb845f558cf344</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>129.5MiB (135.8MB) – 1,248,829 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97b39aeb2424efd1dd6b2fb097d24ae6<br>SHA1: adea363794df4fadcf32704c7f44fcf63112c25e<br>SHA256: 56638192dc4ecbf7ab23607c9ed7a37b6189943f518f37faaf242ded63097de9</pre></details></small> |


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
