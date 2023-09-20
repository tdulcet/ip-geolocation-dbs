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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-09-20<br>IPv6: 2023-09-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.617MiB (5.890MB) – 239,304 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8517d5b20644c5462c0cf529b1f9ff76<br>SHA1: 99d32df76f61a7fe4d23d18a243f92df3c28870a<br>SHA256: e96df6f12d9ca8878562417edbda7336f2469b8491897bd21da3a3d01fdae59d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.188MiB (6.488MB) – 80,103 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66bd71d8b75508ba05523441fad3da7c<br>SHA1: c35fc9152681e8dad719ff717b85ffe3159f87a8<br>SHA256: a8fc1e7b1e057f571feac08ffb913dbb0b19c3517761e439d1bf1ff08471ac66</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-09-20<br>IPv6: 2023-09-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.576MiB (10.04MB) – 406,767 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 910f0de2d77551bff4971f6d932a896d<br>SHA1: 5fe0d74e46551f061e2d9cd3573c5068d5d0767c<br>SHA256: 8d8ff70f3dfbc2473fadf7830ee968c88f4ab8d22e4765f8ab777898f5c4d0eb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.854MiB (8.235MB) – 101,769 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff60b9bdb7737d52995b9ef4ee4c8e81<br>SHA1: 969454043af4794e100feeed5d58e481d10465c7<br>SHA256: 93039def211dd6d932ce5c016e0c0e1f2c2842c6a651e79c4b5b8adc31921512</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-09-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.94MiB (15.67MB) – 637,013 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c810ae15fddfd243c2040a96e413a0ed<br>SHA1: f8f324b45ca8c43cec47b69e20b175c8644e4e60<br>SHA256: 7230dcae36f643f3f90a27040dec49210568645c4ace1dc31872aca1f9a37696</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>47.24MiB (49.53MB) – 611,495 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33e72e27b09d19309967f52b3cd06e86<br>SHA1: adf4b1f2a2056311774ce06b6aafc5f15d740d6d<br>SHA256: efdef19217fe6b11605a1df0fc1f65c835d596bb0461e2f58e03373da6bcfd9b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.416MiB (7.776MB) – 317,712 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8af33754952bca633e2643d56b9b3556<br>SHA1: 635e2f9c397074c2d69ffb9220affbfd86ec55f6<br>SHA256: 3ebea563a71e9352b6b395144accf2da57a57d06e4f59e570f279b0f7dd0b26d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.32MiB (27.60MB) – 340,762 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eabb53c9e90baf81be978b9f452f9fcf<br>SHA1: 926f5a148ab14f14ab51042d5e540547e30fdc1f<br>SHA256: 1fc208ccb6c914cdec8d9914c6bbc9c49c7d9cc9dfb2403391c007a74eb2b066</pre></details></small> |
| | | Full Location | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>190.1MiB (199.4MB) – 3,137,207 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2af38dd10686ebd6a86c594c3c4a2080<br>SHA1: 65277ab4aa4e2343a37d4407ef75cd7b9577ce09<br>SHA256: 30a72428cfaf99539c901922da1a549a4e9635f9cd813dc24c43dff6412dd165</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>281.2MiB (294.8MB) – 2,444,157 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03a9ee13cf7bef9c5c8c0f0940f7d68d<br>SHA1: 76dd4832de692a91cac900713620ea3132b3d208<br>SHA256: f8c720b6ce16ea0971582e27752eb16eb5bb69ed472ed8330ee45a84bc6666c0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-09-20<br>IPv6: 2023-09-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.512MiB (5.780MB) – 235,008 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f5b6633d21428ca1b77b02bd93ccf8b<br>SHA1: 52d80d0117cb022e501c545e2ce94f0292f49302<br>SHA256: b7ec29dd99ff8c1b7df35a0e90a87fb1ac93c22dfd85334670687358c1b14288</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.53MiB (19.43MB) – 239,903 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0828735b19358ff575bc94aeb9fd5e5d<br>SHA1: 89731a1b44a22cddc2b7f5cd9cee902f9ea0134b<br>SHA256: 32050d76fcd8c0b1edb50d74e670dcdd6ec2c415a0c478c78b5b036bbb262e48</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-09-20<br>IPv6: 2023-09-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,035,503 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25939bb2ee9379027c7ed8b48c581ef9<br>SHA1: 0cc26f98398ad29837f913a430a0614477064fba<br>SHA256: a228f642ae927e8d72503c3daf7971e53068c745a86162a71f7c0ee85e3fcacc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 1,407,049 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9148267828dd02b4a07b8d71be61e05<br>SHA1: 3385387c9e1e91d9a4fefb58750dbd3ecf5b473f<br>SHA256: 84af78d046b164d3df6de0dbc9ec0d4555678bffc281df97f9793acfc4c09d03</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-09-18<br>IPv6: 2023-09-18 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.51MiB (11.02MB) – 448,385 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0b9a2fe8bdb566b9247873547bab0a39<br>SHA1: 67c45ac8923feb05b803f38c33c1d47ac509aaf6<br>SHA256: 3aa8fb9932a44f0928d92cfc421fe96cdee9402e9997bb88c66d87d9ed567bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.77MiB (23.87MB) – 294,729 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ae34a5577e20ab648eca3f0140c3123<br>SHA1: f51d279b174a4d06f221350b6b5b428715465619<br>SHA256: 5634f024b27922ecdc1342eeddbba0fc2133ae658251ea41b574083fcb46d614</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-09-18<br>IPv6: 2023-09-18 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>191.4MiB (200.7MB) – 3,818,449 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aca25e91b1c5d314c0832a1ffa71b0d1<br>SHA1: ce5bda1236c8e40a5f53947d38bbe40c35ffa6ec<br>SHA256: bb6a237b9fbe5982f1c1a3159e3a139d0c56eee4c7ed4ec6356a20b5bbef73f6</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>223.8MiB (234.7MB) – 3,818,449 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fba258ede4bfb30b6ca530e211a369bd<br>SHA1: 71f7e6e4748815051d30647f61efe32d177760ee<br>SHA256: 139a5c7097b5b60959d9cf72e7fc78f8e1ad3827b8739c06105f322f924af9f8</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>198.5MiB (208.1MB) – 3,818,449 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 926d85ea469af7d8c54a2cd0083dc347<br>SHA1: b82603a81f7706194021bb33ca5031a5756bd81c<br>SHA256: 141689db1ba4d1595ffe138576d28eb1be1d1ea7700348ca2d0267cd95c34530</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>204.9MiB (214.8MB) – 3,818,449 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4cddb4c88cfd237cb4ddb2513111e64<br>SHA1: 20da8a738f15abf564980093dc8cef2613de4d29<br>SHA256: a83970d58d4c44a899bd682b820fb6ecf91e4c1eee986783491815de42dea110</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>240.8MiB (252.5MB) – 3,818,449 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5326adaf7e5645efb62542075410f769<br>SHA1: 46bd5d84edef6c79a5e97c46cb9d138da5aa7c14<br>SHA256: c22c10dfa187749794c17929d56127beb0b7d4c1329bc60c094cf5f8cc13e578</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,818,449 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91490e89f621e5c4579c267d45f85326<br>SHA1: dd4cec0e684e80ab17ef651c40ee2cb2bf3e14ca<br>SHA256: 761b9b33e28f9e5d3b2d6c57082c4cd1cdfe995877adf6b242beb78eac20bdc0</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.5MiB (252.2MB) – 3,818,449 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4582be149cdd725d3369b372719283b7<br>SHA1: 8d95d78fd3daa55b90bb1c64acf4126741333b3b<br>SHA256: 1b9353975e7420f0462771918927ad83085a5a166b881ec1736d82676dc982f0</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>205.0MiB (215.0MB) – 3,818,449 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ea0491b96d52f06563fb2bdc2415b74<br>SHA1: 78a7e85206475432a155b8f7b650743bdd9f7915<br>SHA256: 5cc7fa184171223a49e417be49ff1e9f5e54e80bfd8c1b42f7f5d70eaadafe5a</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>133.1MiB (139.6MB) – 1,327,556 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27473d03f851a1fb287f44b0d8d19f51<br>SHA1: 4f3cc851170b641d3d85f0a73d4e69740a760ac1<br>SHA256: f9bf36f3946b281f53b47a6ed56593e4c58362f24c5767c4dcd568a9f5d2105a</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>141.6MiB (148.5MB) – 1,327,556 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4cbfe398a6eff6262ebb7681304d6d8b<br>SHA1: d7c03527e417fc399cf26fda168891a04b6b06ee<br>SHA256: a8bfe5b484a44df8904d6e1786f5977cf2b18f34f1621a4a5008de5facf9a312</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>135.7MiB (142.2MB) – 1,327,556 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77fc44eb50b2d0bfb99043a49e866f94<br>SHA1: d607a57de20e265f87f5a642def8637689607945<br>SHA256: 332bb6c31fe235c97a1c4dbc348935dc0761f8786999e12616750cd66dbe0a81</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>137.5MiB (144.2MB) – 1,327,556 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10ca0adae11c426375e868cf86173111<br>SHA1: 39cc96b3dcc40c0774cd6c7b349a4901c373bec4<br>SHA256: 7b45cfcec573661faa9e687ffe8d26b3f718f8f69460a6c177ec6aaec80e6052</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>145.7MiB (152.7MB) – 1,327,556 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc6e4061b382ca259527b432ded9114f<br>SHA1: 2d95e252605d08b847633e39e3f271f739367418<br>SHA256: 59aabb20c35d241bc93a1c6e6f73186071f636f5cd1f2bbbecf2acfbd305fce3</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>134.5MiB (141.1MB) – 1,327,556 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85a982b46665ae683afd464677078a48<br>SHA1: 2201239e5bd4fecbcd4eabc64bfa803d6b0784bc<br>SHA256: bc3c7d3a7f69ce9e2dd8be2d80345606a8415f8da1ce825bbaee017b8c938e2f</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>146.2MiB (153.3MB) – 1,327,556 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4327508ecfd1605299dd907584a5c403<br>SHA1: b89bab261a8cd5608fcb1977a7242e63306f76d1<br>SHA256: 3d46c49b5b25bb327a41242eb187bb12f9799cdd8dfa673ebb3696a40f7fce1a</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>137.9MiB (144.6MB) – 1,327,556 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3fc8fd8981f963513d45aa756c46af51<br>SHA1: c2c980d40ab4e6b5bdcf27011d8fdfd5e1ceeec7<br>SHA256: a7b859aedc1fe95dffda347fa447a52227593cac7b9ef50873bc981748930b89</pre></details></small> |


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
