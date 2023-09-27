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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-09-27<br>IPv6: 2023-09-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.615MiB (5.887MB) – 239,180 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4b52a566ba2654785275ed255fcb6de<br>SHA1: 1c98d7047b5716092f2f5f3915c24231a3a78e2a<br>SHA256: 233fc9c813bf33eab689362bc5e6829e1f77f20fac38394d5b21659ece1def5d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.239MiB (6.542MB) – 80,765 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 920b04d4650a17cbafb11c60a89a8af1<br>SHA1: 5d6e51aa140b3f1823b38459268137731d9cb5fb<br>SHA256: da7fef143657eef30a99f44a7a33771f7cefa377cd07852c251839af4d9219e1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-09-27<br>IPv6: 2023-09-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.602MiB (10.07MB) – 407,839 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5dc5bb77c9df0ec36862cc5627954f3<br>SHA1: 350722642df081632caaf4f7e876eb64bcc8a14d<br>SHA256: a2344286fb03b82a9797db418d41f378ed04eccd47d2eaf119e8508393459db0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>8.483MiB (8.895MB) – 109,912 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df9afb7fcdd4a40a61fdc03e77b29c6a<br>SHA1: 1478dcf61251bfeac94003ad67b0ab5225649614<br>SHA256: 675a54e6ad28bbb481b84e33a934ff896dbaca2264de7e4dda4ff28f2f967dfd</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-09-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.55MiB (16.30MB) – 662,815 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f05a60058df7e7e5dd6f38b47ddb2fe<br>SHA1: cdc51928c2aa0e63a64c5232be219cd14ba1da4d<br>SHA256: 6b159b14162639f00b97eb914513fc34d03720f20a4150f9c9b4aa96f5ca362d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>45.54MiB (47.75MB) – 589,565 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e5482d5f6e730e2d6daae2b320c051f<br>SHA1: 9dd0e4c1add41b4ba19bc7e9c9abea8c65844239<br>SHA256: 89d8ad8239ccb29985fc8d1b8b36d0cc9474f4bc03b3c989f953bb6a9e312f72</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.416MiB (7.776MB) – 317,712 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8af33754952bca633e2643d56b9b3556<br>SHA1: 635e2f9c397074c2d69ffb9220affbfd86ec55f6<br>SHA256: 3ebea563a71e9352b6b395144accf2da57a57d06e4f59e570f279b0f7dd0b26d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.32MiB (27.60MB) – 340,762 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eabb53c9e90baf81be978b9f452f9fcf<br>SHA1: 926f5a148ab14f14ab51042d5e540547e30fdc1f<br>SHA256: 1fc208ccb6c914cdec8d9914c6bbc9c49c7d9cc9dfb2403391c007a74eb2b066</pre></details></small> |
| | | Full Location | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>190.1MiB (199.4MB) – 3,137,207 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2af38dd10686ebd6a86c594c3c4a2080<br>SHA1: 65277ab4aa4e2343a37d4407ef75cd7b9577ce09<br>SHA256: 30a72428cfaf99539c901922da1a549a4e9635f9cd813dc24c43dff6412dd165</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>281.2MiB (294.8MB) – 2,444,157 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03a9ee13cf7bef9c5c8c0f0940f7d68d<br>SHA1: 76dd4832de692a91cac900713620ea3132b3d208<br>SHA256: f8c720b6ce16ea0971582e27752eb16eb5bb69ed472ed8330ee45a84bc6666c0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-09-27<br>IPv6: 2023-09-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.512MiB (5.780MB) – 235,008 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f5b6633d21428ca1b77b02bd93ccf8b<br>SHA1: 52d80d0117cb022e501c545e2ce94f0292f49302<br>SHA256: b7ec29dd99ff8c1b7df35a0e90a87fb1ac93c22dfd85334670687358c1b14288</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.53MiB (19.43MB) – 239,903 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0828735b19358ff575bc94aeb9fd5e5d<br>SHA1: 89731a1b44a22cddc2b7f5cd9cee902f9ea0134b<br>SHA256: 32050d76fcd8c0b1edb50d74e670dcdd6ec2c415a0c478c78b5b036bbb262e48</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-09-27<br>IPv6: 2023-09-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,035,503 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25939bb2ee9379027c7ed8b48c581ef9<br>SHA1: 0cc26f98398ad29837f913a430a0614477064fba<br>SHA256: a228f642ae927e8d72503c3daf7971e53068c745a86162a71f7c0ee85e3fcacc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 1,407,049 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9148267828dd02b4a07b8d71be61e05<br>SHA1: 3385387c9e1e91d9a4fefb58750dbd3ecf5b473f<br>SHA256: 84af78d046b164d3df6de0dbc9ec0d4555678bffc281df97f9793acfc4c09d03</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-09-25<br>IPv6: 2023-09-25 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.27MiB (10.77MB) – 438,288 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 112dd5af643f33b27e55be87baef2aaa<br>SHA1: 87505787c27b3ebd6b2495fb28f8c5a04c22f59d<br>SHA256: eac56ad3c21788b663e03d344be563feae358cc247d6543658607a6ba2bed6d4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.56MiB (23.65MB) – 292,019 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bee2014c428d8abd7855e94adaed7984<br>SHA1: 4ac1078947fb9ca9618e29e4c2ba851ab51a992d<br>SHA256: 84775b6a1ed3cabfb4e42b1adc463d74f9aeb0d24941814d7e9efe1e66a239e3</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-09-25<br>IPv6: 2023-09-25 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.2MiB (199.5MB) – 3,796,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99651776ea85c0c9e188482dfbbf71c1<br>SHA1: e20fd7bb7f44909c8884e84cae896a52085ecffc<br>SHA256: 10d4f837ab7335e5d9eb2cab76ffd0738212ba4e1013420dcdf4852ff062d0ce</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>222.5MiB (233.3MB) – 3,796,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38b169c46a89c0bc254b83dd8790c188<br>SHA1: 8b7435d93d92bc92aa11ccc9aedf2db83c027c4f<br>SHA256: bf9c2d2600555f8c20346410eb63e3d6b728205212da19258005b603fb018c26</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.3MiB (206.9MB) – 3,796,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25691d6732fea82aa878eabbe6787251<br>SHA1: 3306ff9a81ceb6d6e9912629e686b578ab7f685b<br>SHA256: f8853198fa288450c00d562bd033fc6416ca986dc5ec299aee67b8d959687c07</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.6MiB (213.5MB) – 3,796,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34935b39826a3e27ea136842ea0125d0<br>SHA1: 56e9477cd9a82a4a2dd7c986a43bf16b37429568<br>SHA256: 1f5374b363ba68b75a9f034af960fb0da9370d0ae343a823f49170d07a3fb4b0</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>239.3MiB (250.9MB) – 3,796,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9395c08f34b176f1f188b9e7bc19d841<br>SHA1: ae5db299d0755b29592f8f9acfee87236878ce77<br>SHA256: 1b02d0c109a934056cd7556735a70a0f0acd7556a8c7fa59ec179ae3e2f1cc9a</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.6MiB (200.9MB) – 3,796,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 69bd56bcd57b56a45413687cfd9042b0<br>SHA1: d56182eec7481a07a566744ef4797140df6e22cd<br>SHA256: 612848e59b5a8acd61ddcc62037908bfdd5ce2562962cbbea42b0922152eac19</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.0MiB (250.6MB) – 3,796,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f72165839ae1fd165bbd1329cf30f183<br>SHA1: f9bf9a4b441a4a67225da1849acbf0daea008491<br>SHA256: 66b4a7882c7c4584b0815fb46774b76da03c2dedacdc89df47934c7597e43c18</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.8MiB (213.7MB) – 3,796,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab45b6d518edefeb0c7066405bb29db1<br>SHA1: 3847f7a8a3595850a06961493990ba01096dd791<br>SHA256: c9af5a9782906233f0c0da7b959c64118808683749b92cf2b1a7d2ba970aec21</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>133.2MiB (139.7MB) – 1,328,148 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65c3c78686167deae05e61b16cd68f98<br>SHA1: 2119347b771e1a197135b01559363c4622cc707d<br>SHA256: 3605a5f8a9f17cd6e5083fbf8a5359012ff4371d69c6b68a09a141efe76aed83</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>141.7MiB (148.6MB) – 1,328,148 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afa746868544a80da27d38a7a146638f<br>SHA1: 5776966a7a92aa7f78e667dfe2b36bb074de5b0c<br>SHA256: ec1a38456a211ec433e9c4665be327163d6c0f364feae6c0cfd9b9cc76aa0903</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>135.7MiB (142.3MB) – 1,328,148 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 78a9ceff159330b725313f8bf7fa41cc<br>SHA1: 806e5f9e838339d9519de25f3829d7c066315170<br>SHA256: a8a099be7e29f0163db982975f37ef5cbf45fc0f63bf5c117c45316c077537d2</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>137.6MiB (144.3MB) – 1,328,148 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f64b25303c8e470c90b9524d2944f61<br>SHA1: 2fd2e546f080031c30126a4bce275add2b749f88<br>SHA256: 4b798eceb64a1ec461a69d175eb7d177087d258bc6642c7fdd1d4c01b97b82d9</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>145.8MiB (152.8MB) – 1,328,148 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80ca91ade493e3cd212fc381e9199d65<br>SHA1: 75523f375af2ce162c79ca39896dc7e2e23ea28e<br>SHA256: 066e630f5260b0becc08333dff324bc661030b6c241736b73d21a2a7d954cd6a</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>134.6MiB (141.2MB) – 1,328,148 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b43b00747a21bcaf4b942e84c7353f2<br>SHA1: 0ae82423d29fcea277b4fff18849044b14e96a9a<br>SHA256: a3a194602d9612a2f65e27eb5c6e09843b6f48f2dc3187053b612fa910cca108</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>146.3MiB (153.4MB) – 1,328,148 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a971859fcad01ec6d243cd2d5ab2804c<br>SHA1: e06216dc33e90a1b88c838a50c09cb1703085656<br>SHA256: 850a3795ea693dda67b3598fac81b4802d2da675be5c1ea77139c745285e86f7</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>138.0MiB (144.7MB) – 1,328,148 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44a44ca118540c46bfcb24f6f3bf9734<br>SHA1: 418621941ba9868f4f813b367ef81e8223b94a28<br>SHA256: 1b33869b56cd9b38951d7f876a146a31ee0975209f5bd199de23c36a21529d08</pre></details></small> |


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
