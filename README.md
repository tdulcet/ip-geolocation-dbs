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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-09-04<br>IPv6: 2023-09-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.635MiB (5.909MB) – 240,077 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74558a9d79fcd1d9ecd8b0ae60626bce<br>SHA1: 28adb43d41b9f890f9181607c297953fb77435a2<br>SHA256: d17dfb9aaaced4270405c3e4306973a544b2a2266fba763422876d6013dc8181</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.667MiB (6.991MB) – 86,306 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2511e333cf078ba332cfd6dee1abbd9<br>SHA1: 9e4f7f64b18f0b53167eff12cc80d431a74e96da<br>SHA256: 4f2083640637518dcb6fabf8a619b1ece30702c654463bb734ef4f414ef79a97</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-09-04<br>IPv6: 2023-09-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.551MiB (10.01MB) – 405,689 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5889d02ea0c1ee2d71c185a328cb1dd5<br>SHA1: 61331bee7cd65365a033d85d8fc10d6b69f0904e<br>SHA256: 83ddae30610a238945f6c8ebb48d7371c55bcf81a4527d3c5161993570112dd4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.786MiB (8.164MB) – 100,891 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ab6598fc85b1051986550dda9e8744d3<br>SHA1: f3eba1d8f1442385494d219c1f09323b00181b31<br>SHA256: fa5464115a3abe6a070678993cec25d94372c8adf001871a84bd5e38896b1ef2</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-09-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.45MiB (16.21MB) – 659,316 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 32e479e192cfe49e60e77c95970164a7<br>SHA1: 785b8843cb717edd68f2104eca089e44197b5f49<br>SHA256: ce3d167ba2de7095747b918757b29a0ec0b3dffc9ddcff32d1260d8a0ddbd6ee</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>38.22MiB (40.08MB) – 494,809 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 609364427aab06bdd8d6a02756df2fe2<br>SHA1: 28796e5b5c91835a4faec58b7bb7a8b5abbe059b<br>SHA256: 34268db9ae99d737a277159f5e503aac4e2020ce4168ab5eef30d6e228ee9faf</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.416MiB (7.776MB) – 317,712 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8af33754952bca633e2643d56b9b3556<br>SHA1: 635e2f9c397074c2d69ffb9220affbfd86ec55f6<br>SHA256: 3ebea563a71e9352b6b395144accf2da57a57d06e4f59e570f279b0f7dd0b26d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.32MiB (27.60MB) – 340,762 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eabb53c9e90baf81be978b9f452f9fcf<br>SHA1: 926f5a148ab14f14ab51042d5e540547e30fdc1f<br>SHA256: 1fc208ccb6c914cdec8d9914c6bbc9c49c7d9cc9dfb2403391c007a74eb2b066</pre></details></small> |
| | | Full Location | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>190.1MiB (199.4MB) – 3,137,207 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2af38dd10686ebd6a86c594c3c4a2080<br>SHA1: 65277ab4aa4e2343a37d4407ef75cd7b9577ce09<br>SHA256: 30a72428cfaf99539c901922da1a549a4e9635f9cd813dc24c43dff6412dd165</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>281.2MiB (294.8MB) – 2,444,157 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03a9ee13cf7bef9c5c8c0f0940f7d68d<br>SHA1: 76dd4832de692a91cac900713620ea3132b3d208<br>SHA256: f8c720b6ce16ea0971582e27752eb16eb5bb69ed472ed8330ee45a84bc6666c0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-09-04<br>IPv6: 2023-09-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.512MiB (5.780MB) – 235,008 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f5b6633d21428ca1b77b02bd93ccf8b<br>SHA1: 52d80d0117cb022e501c545e2ce94f0292f49302<br>SHA256: b7ec29dd99ff8c1b7df35a0e90a87fb1ac93c22dfd85334670687358c1b14288</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.53MiB (19.43MB) – 239,903 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0828735b19358ff575bc94aeb9fd5e5d<br>SHA1: 89731a1b44a22cddc2b7f5cd9cee902f9ea0134b<br>SHA256: 32050d76fcd8c0b1edb50d74e670dcdd6ec2c415a0c478c78b5b036bbb262e48</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-09-04<br>IPv6: 2023-09-04 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,035,503 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25939bb2ee9379027c7ed8b48c581ef9<br>SHA1: 0cc26f98398ad29837f913a430a0614477064fba<br>SHA256: a228f642ae927e8d72503c3daf7971e53068c745a86162a71f7c0ee85e3fcacc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 1,407,049 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9148267828dd02b4a07b8d71be61e05<br>SHA1: 3385387c9e1e91d9a4fefb58750dbd3ecf5b473f<br>SHA256: 84af78d046b164d3df6de0dbc9ec0d4555678bffc281df97f9793acfc4c09d03</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-08-31<br>IPv6: 2023-08-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.18MiB (10.67MB) – 434,305 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34782e32a969c7c9a665cdf72ce04830<br>SHA1: 4a63374b2eb6fbb03fa662585ca9e3666f77aef0<br>SHA256: 28933eb6645b72f2fab7e7010d1b77e835a81dba75bb2dae723d8d1aa4a3daa1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.56MiB (23.66MB) – 292,091 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dbf3464fd3b8139d1e235fcd12e155c2<br>SHA1: 90a30da40cfb671b7ee379117893555f6ebc1dd6<br>SHA256: 3580308e37b2bbf1833f3e9348ce69e7134ddc070bfbdca219be7da8a2f84079</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-08-31<br>IPv6: 2023-08-31 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.6MiB (198.8MB) – 3,781,921 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 912ee2931aa641d45934dcbbbac0d716<br>SHA1: f9967a9c84a44ebbde50e060c79d4d6688284816<br>SHA256: 00b1d970bc4d881c14fafde4b343d7f39ba7c2aa57a604c19ad90f2407d7568b</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.7MiB (232.5MB) – 3,781,921 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6510bd63f1b1567b24883f35a39f4d42<br>SHA1: 40ed8c0e15000629a0b5145425f3c815a3f9815d<br>SHA256: f3fa3215691854bad4c4522b143366ad08a7b0c7c530e74205b2d5c6b2dfb2c5</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.6MiB (206.2MB) – 3,781,921 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4623ba4ded79f8580375e9bd360ea162<br>SHA1: 694668c380071ac3668f1e056fa64d7069b66cb0<br>SHA256: be6ecd647e803ffcab7fdb634ba1660a86bf14b7d392ffa9c23e4e7a71e9e016</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>203.0MiB (212.8MB) – 3,781,921 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dac3be2cd5d6faaf291fed96ef57cf0<br>SHA1: 71181bbc3af1f43c189f57e208e5bf3ea41aa317<br>SHA256: 58c75d5cc504e093886110bdbb9f2bcdaacfd3668e6d0c27d86785ba296ca223</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.6MiB (250.2MB) – 3,781,921 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59845528480792ca8f05dab6b2cbf371<br>SHA1: c36f8196f0a5a0ac1b16114f5c5dd0488c9e39d0<br>SHA256: 2b21b7b2ba5c11925aca7b8c46133e67443b09956bd29581d0854ee65f34e500</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.0MiB (200.3MB) – 3,781,921 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7b9e050b01795f73fadb5efa9093ba47<br>SHA1: 517b2bea255ed4abb737ea4f33676586d4736481<br>SHA256: 515802041972ad5aba3d31b2771eef6cea0407c63e93e113974f7b1b0e23e84a</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.3MiB (249.9MB) – 3,781,921 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3c0352eb05031d6eeae51b0a5a3ba76<br>SHA1: 5b6e4b0e0ef58cf5d30a51c6316c3cf7d981cd5a<br>SHA256: c02cfa58d6ca928565d45681355e11889ab52ee29127c1a6ad72caed3c4c837e</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.1MiB (213.0MB) – 3,781,921 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84c10555434a43f51c4bfbf926e6dcf0<br>SHA1: 3fc613ced37ceaaabb08a6a024323678e2c5e9f3<br>SHA256: 41849a242b320acb7994b8a19d0c5301e116ad42d7a442fbdaed187078f6f63c</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>129.7MiB (136.0MB) – 1,294,315 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90665759c49e7ba4543d4c3dd7d50182<br>SHA1: 6984eb26ba2a8e7b40d3196e6575724df83dc602<br>SHA256: 1e8278514639d170dfb28c088105907bd3f6112c40992cc14a66fe26133b47f7</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>138.0MiB (144.7MB) – 1,294,315 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fca50d48670df7fb5961b8f4de25623<br>SHA1: d36a35d86806044b09785a56901011af3fa011c1<br>SHA256: 0ee06f6f97635cd914bde26e34d930ec7b3d5668f93f6219f029f091c87d6455</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>132.2MiB (138.6MB) – 1,294,315 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6df685711a639115aa9ac346d65a60ff<br>SHA1: 14c7c481dbcbda7c6267a0cf90d74fb01acf3121<br>SHA256: 30fd222883a8caefc892582a310c4a46344026f5e6b21dc6d49ef7902bef797c</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>134.0MiB (140.5MB) – 1,294,315 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b852958396a7d1cb465fc6423c614e6f<br>SHA1: 61fb1ca60b048c6a134efb12b44ef5abff118d07<br>SHA256: bb93692ae55dc175180f0cd0901b6e2628f47e3676e1f986c0d6127eab8cbfbb</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>142.0MiB (148.9MB) – 1,294,315 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44ae7466832263dedc069183471e90a8<br>SHA1: ed40769747b739a2ee9a07c176e953c9e90c9374<br>SHA256: 1a09ce56872b573aa1d2b3f813689ce088da21d584f8becfb9f259d22659fc23</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>131.0MiB (137.4MB) – 1,294,315 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f00a86a1af54c90a2fee8af6153bfb07<br>SHA1: 40cdfcc69c1bf855074a0c28a302bc392f876576<br>SHA256: f7b7be4812210987135bed70e8c53ee6897ea251a98dd72bd2f03afda069bbe1</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>142.4MiB (149.3MB) – 1,294,315 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c18b9438d22c604655719c5b36c96e1<br>SHA1: 950097135cf049451abb0b5d29dd217cc841c473<br>SHA256: 45a0f42a89f33d87ab1f46e698210b4c006000e70122f2102a2ab5cda28cbaad</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>134.4MiB (140.9MB) – 1,294,315 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe44ec4ac9042d7875024fe7bc3e7faa<br>SHA1: 905f007707669f93c1dab49c9ce927f53ac6d7a2<br>SHA256: 42caa145e8eee43564e8d06799fd78b85ffce81499adfe38cdd8c5286f3002fa</pre></details></small> |


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
