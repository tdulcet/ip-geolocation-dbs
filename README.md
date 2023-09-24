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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-09-24<br>IPv6: 2023-09-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.619MiB (5.892MB) – 239,381 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b02d1ebe0c46548f26b7dd404b9fdbd7<br>SHA1: b0d0760ff0e089e259f6ea6aded37185df629ef3<br>SHA256: 45b3a30b8962f0c75e691d0efa4adb98dde4e5b1796e43b79fd4f8739553c3ec</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.220MiB (6.522MB) – 80,523 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7f73e9664bbebfafb3f90e585128e37a<br>SHA1: 37d46c478543c154f576222c605650efc579c7c3<br>SHA256: 63f39c4e33fc4db9497cd0172bcd5d4ed5f5b84f5dc51a1e904ae6f29789f9ef</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-09-24<br>IPv6: 2023-09-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.598MiB (10.06MB) – 407,676 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee8a23f0161d3d82b931463985938b25<br>SHA1: 53eb97fb7fe91b31172e0adc8b1ae3bebe88cc30<br>SHA256: 4142964ccc6ec1cbafc14db8ae58acfb21706907e45c67c5be04f714d4b9e801</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.870MiB (8.252MB) – 101,972 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e4f25536c0da5ab0eacb372ca7bffc73<br>SHA1: 15abf46c333d83a3bebf529bd2f307ad0d19c84d<br>SHA256: 3e1fff5bbb5448f51325899088416554d2da3134b1bd5bc75293063bb4635863</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-09-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.94MiB (15.67MB) – 637,013 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c810ae15fddfd243c2040a96e413a0ed<br>SHA1: f8f324b45ca8c43cec47b69e20b175c8644e4e60<br>SHA256: 7230dcae36f643f3f90a27040dec49210568645c4ace1dc31872aca1f9a37696</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>47.24MiB (49.53MB) – 611,495 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33e72e27b09d19309967f52b3cd06e86<br>SHA1: adf4b1f2a2056311774ce06b6aafc5f15d740d6d<br>SHA256: efdef19217fe6b11605a1df0fc1f65c835d596bb0461e2f58e03373da6bcfd9b</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.416MiB (7.776MB) – 317,712 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8af33754952bca633e2643d56b9b3556<br>SHA1: 635e2f9c397074c2d69ffb9220affbfd86ec55f6<br>SHA256: 3ebea563a71e9352b6b395144accf2da57a57d06e4f59e570f279b0f7dd0b26d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.32MiB (27.60MB) – 340,762 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eabb53c9e90baf81be978b9f452f9fcf<br>SHA1: 926f5a148ab14f14ab51042d5e540547e30fdc1f<br>SHA256: 1fc208ccb6c914cdec8d9914c6bbc9c49c7d9cc9dfb2403391c007a74eb2b066</pre></details></small> |
| | | Full Location | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>190.1MiB (199.4MB) – 3,137,207 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2af38dd10686ebd6a86c594c3c4a2080<br>SHA1: 65277ab4aa4e2343a37d4407ef75cd7b9577ce09<br>SHA256: 30a72428cfaf99539c901922da1a549a4e9635f9cd813dc24c43dff6412dd165</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>281.2MiB (294.8MB) – 2,444,157 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03a9ee13cf7bef9c5c8c0f0940f7d68d<br>SHA1: 76dd4832de692a91cac900713620ea3132b3d208<br>SHA256: f8c720b6ce16ea0971582e27752eb16eb5bb69ed472ed8330ee45a84bc6666c0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-09-24<br>IPv6: 2023-09-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.512MiB (5.780MB) – 235,008 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f5b6633d21428ca1b77b02bd93ccf8b<br>SHA1: 52d80d0117cb022e501c545e2ce94f0292f49302<br>SHA256: b7ec29dd99ff8c1b7df35a0e90a87fb1ac93c22dfd85334670687358c1b14288</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.53MiB (19.43MB) – 239,903 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0828735b19358ff575bc94aeb9fd5e5d<br>SHA1: 89731a1b44a22cddc2b7f5cd9cee902f9ea0134b<br>SHA256: 32050d76fcd8c0b1edb50d74e670dcdd6ec2c415a0c478c78b5b036bbb262e48</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-09-24<br>IPv6: 2023-09-24 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,035,503 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25939bb2ee9379027c7ed8b48c581ef9<br>SHA1: 0cc26f98398ad29837f913a430a0614477064fba<br>SHA256: a228f642ae927e8d72503c3daf7971e53068c745a86162a71f7c0ee85e3fcacc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 1,407,049 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9148267828dd02b4a07b8d71be61e05<br>SHA1: 3385387c9e1e91d9a4fefb58750dbd3ecf5b473f<br>SHA256: 84af78d046b164d3df6de0dbc9ec0d4555678bffc281df97f9793acfc4c09d03</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-09-21<br>IPv6: 2023-09-21 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.20MiB (10.70MB) – 435,201 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d20b840cf2955583caef76a0bdfc4ed3<br>SHA1: 86fd45ba9341476c0df126f568951670e0836dc1<br>SHA256: 5abc36a70b937413b5c964e2f608da49419b79449534c7704eae7a49fe1bafa7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.41MiB (23.50MB) – 290,083 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e233581980221699963d5b996ff4802d<br>SHA1: 55c0cdc0cd0b520bbbb373e8a46079c254681914<br>SHA256: 4d970172b2426c3bf14c3798d2227bc77eceb953097d523319e2db4e6133ec27</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-09-21<br>IPv6: 2023-09-21 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.9MiB (200.2MB) – 3,809,106 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 156c9cd560650590e7385cb6341e4ebc<br>SHA1: ff4b973748828d376c427a2d2420629e4a8fb4ef<br>SHA256: 1753eb43fe61dad66de6c02003f02dc7c77e9344c91c99a32df6e85b0dca89e0</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>223.3MiB (234.2MB) – 3,809,106 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 001534fc803bde61a3076ca5e5434f0c<br>SHA1: 9b63883764209b32d3ec5366505c82f05aaeae58<br>SHA256: bcc3432fee045deccf40f6a8d81c14b4c05469cbcea1ee93075a8db16542538f</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>198.0MiB (207.6MB) – 3,809,106 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8280a16dd228a9de12c839deb4bdecd<br>SHA1: 392c28ab01e647959b6f7b25c903bd9de70758a1<br>SHA256: 4f0bc51f36e249510ef5814e7ca042c30abe84f3b465d1ebc15d57c623151e77</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>204.4MiB (214.3MB) – 3,809,106 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed7bac63317043b40e7b8396365216cc<br>SHA1: 85aafb311f665f20212a14c88fe338208c65913d<br>SHA256: 17061c799957a0c376b267cfff78d0d704b2dc982347b995d94c57154eccb1d2</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>240.3MiB (252.0MB) – 3,809,106 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d6ec22c7d353dc50932f09a11391b7<br>SHA1: 80e55ede1e48d542556924ee510d54ee7b0c0001<br>SHA256: 2cfa07c72f80107e960ab3e458e8159f731cb72a02fa8e290c0b38af5c932488</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>192.4MiB (201.7MB) – 3,809,106 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3035557b9803b936eb1a85c3d1ffdd19<br>SHA1: 2f60f2703682bf65e4cbac4693bfd6201f258585<br>SHA256: 96714f79812631f98c236ffc690dc63022c6bcd9a7f2e59cacaa391c61306ae1</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.0MiB (251.6MB) – 3,809,106 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04b1b9a6ba0fa89c54c709c05783be76<br>SHA1: 27bed3a9981ea84b293a1913465e650c3696318e<br>SHA256: 8c348296732185b25ea7b9b3a4b84696567d450d4c134094ef408266615e3de0</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>204.6MiB (214.5MB) – 3,809,106 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecd17f45d1063149713508feefee2b32<br>SHA1: e19de5a66e4cad94d50cbea064daebe74e25968c<br>SHA256: 3c3c10ed780a1a1cb05a5f3c930ab56d8db300931844d5f73168045862e673ab</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>132.8MiB (139.3MB) – 1,324,696 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02308e1948210a0782fae98effc31d8c<br>SHA1: 4129d60e05dcdfabdeff1abb3128c7c2cda4200c<br>SHA256: 3b92781c98e595b265c2ebc4198ab616be23f832d9b4990aac7b69b32df6e947</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>141.3MiB (148.2MB) – 1,324,696 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa8844a5ed01d07898e9dfddab806bd3<br>SHA1: e0d332ec21312d1a7f22270e9169a20b28a511b7<br>SHA256: 586be04b3ce4d5396ba48722f7dc9d43dd3eb2785da7bf343b6861d830a34e92</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>135.4MiB (141.9MB) – 1,324,696 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1b7503bcf59b397fcf9d43abf9eb11b<br>SHA1: 48eaff815dde23d7dec5d291b8b0d568e6c2b3bd<br>SHA256: 044b7b4763cdcaea4c3de80181d030a27578773d6df41cda8dfcba562a70e539</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>137.2MiB (143.9MB) – 1,324,696 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72684641533a4c6bf9096c263853be83<br>SHA1: 4662988ca943a946e95e2aa0bd97612f148249d5<br>SHA256: dfe2b1c87a4e5ded8555fa09b7e29dbfa6cc6588999d3ea3f4c69e1b1bd65b24</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>145.4MiB (152.4MB) – 1,324,696 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3fdfee22d79d37c2c544148322df79e<br>SHA1: 1dbad0fc0bd11c315d323cc54a9d75575012c643<br>SHA256: ee66cf1109ad36cc463ec59c8b19027b64d81ad9d4d6e1264f2bdecd1f6d8d05</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>134.3MiB (140.8MB) – 1,324,696 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87fb56685e2e384f66bf1b4e79a393cb<br>SHA1: 00f564cc13d3fc321d23ec3c4ddae1494153820e<br>SHA256: cac72a87776b66af2123d954e2b4adfdf5fe3a0d7822f9de74d567b5a6582035</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>145.9MiB (153.0MB) – 1,324,696 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3c0222747de8dd2ff30222b9420d1a4<br>SHA1: b79d9fcc948df53c0c41ba095343e36a00c05e42<br>SHA256: c2888c2edeb26f7219b417fd6f4ff92f3ee47a5c32683cd02238e65f649d1b87</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>137.6MiB (144.3MB) – 1,324,696 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a5c70e3f9d1fc61baa25bc67a9b971<br>SHA1: 6b00b2a068b88e395f76c03e90de5ed41cfeb4ee<br>SHA256: 6922f2d9a9dc3ae989604ba5d9dcc43a13e6f8e5585116f9bcf6dcb9a904e3ac</pre></details></small> |


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
