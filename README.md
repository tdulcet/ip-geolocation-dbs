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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-07-30<br>IPv6: 2023-07-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.682MiB (5.958MB) – 242,054 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0969aec2a8fee3ca58969f23bcf0578b<br>SHA1: 4f43366e295ff9b74bf3e8da490945497e00ef94<br>SHA256: 31a9d8c65eb6a96d932322b42d7a589a0ba8635bc90a43beb5215814e01f02fb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.571MiB (6.890MB) – 85,062 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f36da82b1953b085fb5a0395ff25e7f4<br>SHA1: 8278e5e3cbba0634e8c4bc4c55427bb341d6e314<br>SHA256: 6c1e6d174b594eae3bbe719c55c1bda5caad483bf30b274662e18eaa827912a0</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-07-30<br>IPv6: 2023-07-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.534MiB (9.997MB) – 404,964 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f50c4a692ea2eed6c3322d807f0c9ed<br>SHA1: 19d11a0b8b0184c2eab2cb66702c354cc7f0df7a<br>SHA256: 60f4ad5d5345e778532ead47187af5925cb64eb7569a18563f465e75337a165b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.667MiB (8.040MB) – 99,353 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 664a70bd187e90c185c2cb56977cbf05<br>SHA1: 779c81e5388293dfa3c0e4cb017d4582fb5bde7d<br>SHA256: a35552ab42b18148e4f227e2e50a090aba33fb7e55b41e1f971f6ef69e7fda01</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-07-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.69MiB (15.40MB) – 626,331 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae95fc896f99baa6df4fcb7ea6efa75a<br>SHA1: 64f0fd84a09c61796ad00fc8660590b85ee1a8d4<br>SHA256: c2c53572312d08a34394db3498f3b3655cef47ac2794d1c321ffc0b781ae3b11</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>35.96MiB (37.71MB) – 465,507 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 808d36fbcf6287c99dc85a0f34829e34<br>SHA1: b3c6154e19d6e427b2b0c0a1a8cb4ac949f597be<br>SHA256: 2901944a8397ee190f8a74da918f07d714926554c45b9b6e0e4c0b246b82a7f1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.175MiB (7.523MB) – 307,076 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f151f7f54b095b5ffda5d94059bb3dce<br>SHA1: f80142665d03d0371f800c5f959cf629ca3d8a10<br>SHA256: b490b03da5e813361b0ca08dd8f825c5991c8d4f9e21568776e4edd93746282a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.39MiB (25.58MB) – 315,780 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ccafe342cd0f83d168aa17033cc052e<br>SHA1: 18929b5d0a7ce12d7f3357fae4e283e3dd102ad6<br>SHA256: 55c042d3051eabf81b139c750768903bc3e9d8314dc416dc8b9ed715765677c2</pre></details></small> |
| | | Full Location | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,182,050 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3425f6eec44d17e75a144956ca9bedc4<br>SHA1: a6ae6d14f8e9a5705bee763c64c2bea6c879b127<br>SHA256: 9a1cffd22df1d59c077b7123b734f643ddf57a71c4d928ee793715e78400597a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.0MiB (303.0MB) – 2,522,649 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac831cafe688be22a072e63aeca50a09<br>SHA1: 8b579d16247db56f0e752f9c5566007ecce7b3c3<br>SHA256: f693430db94cf07b4b01343ab0d2e4ab2f16501d77f433b222ab16b8f015dcf2</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-07-30<br>IPv6: 2023-07-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-07-30<br>IPv6: 2023-07-30 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-07-27<br>IPv6: 2023-07-27 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.07MiB (10.56MB) – 429,503 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9ba7de2828df32afe2470aa4180d159<br>SHA1: a1de6965bfd71c894df74b116938ab4e93830dbd<br>SHA256: 1fb393a6f47ceb6bd0bb165892839cbea5ff853b633293852d45ece8465df2ab</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.52MiB (22.57MB) – 278,622 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d27a1a4ee0d7f2199ef56e37c4dbf86<br>SHA1: 21e0141a4cac1a6625dd4401c7f1ff736ecba650<br>SHA256: e023bd3ccbdd36d981dc6a553bf3aba80b38d6bd98aa4bd102c27adc3cf464c6</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-07-27<br>IPv6: 2023-07-27 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>187.8MiB (196.9MB) – 3,748,112 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4aae61c08c2cd88e34f25a1451e567ab<br>SHA1: 19ff2c5b6598e77c24fba54bc7048f1c0ff87526<br>SHA256: d9f8f1d6d65523715427f57342966a22cf5339ec03b0f04556071d3f680eb0a0</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>219.7MiB (230.3MB) – 3,748,112 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1de0f0d9abbf968df72a1c098b5634af<br>SHA1: 3f3af3fd9c2983da28edbc603a7d0c2b9fe4b407<br>SHA256: 90e56ca5640ab9b4f290440a58682d46f185fcb37a6abbb4c072ae8f3c2ecc58</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>194.5MiB (204.0MB) – 3,748,112 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65b903febf63f7b5783089bb4ab63bf5<br>SHA1: 3f71be09366a571137d9ef995524b54437118ca5<br>SHA256: d7dbecf8ba37b4652446cb3b334a27f5b79c7e0be6276ebd59d31432c194270a</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>201.2MiB (211.0MB) – 3,748,112 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa6ee4a0a6a35275994cf32604e8f065<br>SHA1: daf32971e8a14c33ad196d8f8593193cb1c52eb2<br>SHA256: 65899fd7ed52655ba51d91e04aa966e3b551321e4e05eef42577f17c3eb7d1fb</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>236.5MiB (248.0MB) – 3,748,112 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47ff0efead16e230213d23a99a043d97<br>SHA1: ffd6e65a72689169358e9d661e3bf1b032ae2a25<br>SHA256: 4289e7548bd88eec3e56b62c7e8801209d60488e5fad7b8690a0dcb31a5a3e8b</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>189.1MiB (198.3MB) – 3,748,112 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89de8487b975e4a0f30d2b4ab2953658<br>SHA1: ef2f3120686d507d7328996505debe362c17b279<br>SHA256: 9b20db05e7f83eb04440ab6b08b929f6b28963576c12a0770de1407dde8dc16b</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>236.5MiB (247.9MB) – 3,748,112 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eed06219e2f10e9ba775f9885402d1ea<br>SHA1: 33ee453ee04d9359fba46d3abc338a1d2bbee82f<br>SHA256: 5b41f97283304e53cb5dd19b54db21d985e6accfce234167fbb9757c251234cf</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>201.4MiB (211.2MB) – 3,748,112 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 786d13635c95132afca588fbc4bb84a4<br>SHA1: e5e198c905d3e4619f7a24afa19a1c1cb5bfe723<br>SHA256: 7de834cd33f3c9abfa828d3b01c9d6d18f4a0c955e7fa9ea6a516d4268e76420</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>127.9MiB (134.1MB) – 1,277,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfe95b7967ed1a080aa6137ce2b9ba72<br>SHA1: c71338a709190b17608631ae90ddacf2cff78880<br>SHA256: 68e52ad95dc8833836fa4974f68fd906597bad00342f2db0b71f9e15f928bcb3</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.2MiB (142.9MB) – 1,277,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27f175e4145242381e222d27c18bbb72<br>SHA1: add1b45897a8e277da12ea198547433ddf29b002<br>SHA256: f4558b5f5a5e4e29bb30a5f2c4c4f832d63169474f485b9b1917b1f86188d924</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.3MiB (136.7MB) – 1,277,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 87ea5e35f54b536e06b451efd58941ec<br>SHA1: 53c97673a531bbe7f26ae15d922ea062adc25d82<br>SHA256: 13f3403f80774637f2ae5592eccf66fe6c603479da8c5a5a41f4dffc77bf9161</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.1MiB (138.6MB) – 1,277,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1db9f5090f4b39d7dd824807f1649b93<br>SHA1: fb9f1fc192755fe89688c4e40782f389ecbb05f7<br>SHA256: e3d423562b9cfd3bae2b0be9a63a9897dbec49bc71d9dd77953166a782bfe8d9</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>140.0MiB (146.8MB) – 1,277,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f709d85cbdd31923a7fa2afdbda58471<br>SHA1: affb418a7c786ac7477fa180bbd5abca14eeaaec<br>SHA256: da3c5939a2f8404319ad184773581f1273094f8d829e7849f3ebf5e681c8c447</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.3MiB (135.6MB) – 1,277,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c24aed7969b915978daaacc3b9912294<br>SHA1: 998c4e94061d15bb6874b69c9f1a6c26c050aed6<br>SHA256: 5e345f40115ce1a935acd630baf352887ff8029b42529a5ea630f34a0686ac6c</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.5MiB (147.4MB) – 1,277,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c649d1c50d7fca32c605a12de07e4a51<br>SHA1: 696098632613ca93cfe771453edb3ad8736f7902<br>SHA256: 3d2604114b201c4335e8cce768d1d67c53204e098fd2ad36ca0eccba093b9bd5</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.4MiB (138.8MB) – 1,277,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8dc90d41fa745106ceae0a6c645889c1<br>SHA1: cfb20aca88fdbc0bdad92446fd45db0b2c2fe0cd<br>SHA256: 8b1ad4191fd013a758b52529633cee531aa4f94292ecf5ffa74fffb46c85ed17</pre></details></small> |


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
