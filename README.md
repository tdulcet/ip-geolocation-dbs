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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-09-08<br>IPv6: 2023-09-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.639MiB (5.913MB) – 240,222 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5da062772b176a74dfe02d5edc83f9df<br>SHA1: 85665cacc872a2268943c538e1eb2a2353f3c77e<br>SHA256: a53df8cb8a7b0993ece2c63e1f81c45002e760dec33e17adf838f7abff004274</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.100MiB (6.397MB) – 78,972 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c8125b7b0bef6f8735d5d6ec413785b<br>SHA1: d81ceac00aa455f0bd0d2e858edd5eb45e5bb942<br>SHA256: e35a3afb63607d3931c95660ab87451e4508f1d02073c7788bacd803da404240</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-09-08<br>IPv6: 2023-09-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.558MiB (10.02MB) – 405,970 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6516f81e50a8394f374aef04d25dc668<br>SHA1: b66dc86dc150fad36eebacd38e613b147c5fcd64<br>SHA256: 57ee7ad81f377c7adb9fe1bc51c75a43fff1ba6340b7774af21bc09a4aa8ebb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.795MiB (8.174MB) – 101,007 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b63ff5e2337bf693a450b60866a22f9a<br>SHA1: d03f81c1a55093feaee04ac36499c13fc790055f<br>SHA256: 1f79c30a33f6ed1bcd264f99e65d8fc9827d5a602c26132f8c81a1996aa6bc47</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-09-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.27MiB (16.01MB) – 650,726 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1782f1648e0f31a996e14f4695670a8e<br>SHA1: 647c2aac203b6a27b2668919b310e8e79addbfa0<br>SHA256: 779e10cf82a2ad1f70646c2094f884c1839ab0d029e004780d4ddaa64fe2226e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>38.76MiB (40.65MB) – 501,800 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e9c2c381569d65bd25b69efcfd0ecca<br>SHA1: 71f4913534c570dadf7da93f2a3457bfff8b0366<br>SHA256: ebbc11b350b73f68c0146918ccc1a3e8bd6b4098d6eebbc33aa9423db10bdae2</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.416MiB (7.776MB) – 317,712 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8af33754952bca633e2643d56b9b3556<br>SHA1: 635e2f9c397074c2d69ffb9220affbfd86ec55f6<br>SHA256: 3ebea563a71e9352b6b395144accf2da57a57d06e4f59e570f279b0f7dd0b26d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.32MiB (27.60MB) – 340,762 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eabb53c9e90baf81be978b9f452f9fcf<br>SHA1: 926f5a148ab14f14ab51042d5e540547e30fdc1f<br>SHA256: 1fc208ccb6c914cdec8d9914c6bbc9c49c7d9cc9dfb2403391c007a74eb2b066</pre></details></small> |
| | | Full Location | Monthly<br>2023-09-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>190.1MiB (199.4MB) – 3,137,207 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2af38dd10686ebd6a86c594c3c4a2080<br>SHA1: 65277ab4aa4e2343a37d4407ef75cd7b9577ce09<br>SHA256: 30a72428cfaf99539c901922da1a549a4e9635f9cd813dc24c43dff6412dd165</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>281.2MiB (294.8MB) – 2,444,157 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03a9ee13cf7bef9c5c8c0f0940f7d68d<br>SHA1: 76dd4832de692a91cac900713620ea3132b3d208<br>SHA256: f8c720b6ce16ea0971582e27752eb16eb5bb69ed472ed8330ee45a84bc6666c0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-09-08<br>IPv6: 2023-09-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.512MiB (5.780MB) – 235,008 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f5b6633d21428ca1b77b02bd93ccf8b<br>SHA1: 52d80d0117cb022e501c545e2ce94f0292f49302<br>SHA256: b7ec29dd99ff8c1b7df35a0e90a87fb1ac93c22dfd85334670687358c1b14288</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.53MiB (19.43MB) – 239,903 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0828735b19358ff575bc94aeb9fd5e5d<br>SHA1: 89731a1b44a22cddc2b7f5cd9cee902f9ea0134b<br>SHA256: 32050d76fcd8c0b1edb50d74e670dcdd6ec2c415a0c478c78b5b036bbb262e48</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-09-08<br>IPv6: 2023-09-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>186.0MiB (195.0MB) – 3,035,503 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25939bb2ee9379027c7ed8b48c581ef9<br>SHA1: 0cc26f98398ad29837f913a430a0614477064fba<br>SHA256: a228f642ae927e8d72503c3daf7971e53068c745a86162a71f7c0ee85e3fcacc</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>161.5MiB (169.3MB) – 1,407,049 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9148267828dd02b4a07b8d71be61e05<br>SHA1: 3385387c9e1e91d9a4fefb58750dbd3ecf5b473f<br>SHA256: 84af78d046b164d3df6de0dbc9ec0d4555678bffc281df97f9793acfc4c09d03</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-09-07<br>IPv6: 2023-09-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.18MiB (10.67MB) – 434,132 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 138edd94548c1c60184dd16052f47b40<br>SHA1: 3fb50514b9c2619aa9841cf4ce3aa0425469ac4f<br>SHA256: d5e95b1bb56356352820c84f2ec67655ac0e03bc8cdcb2baa0372243dc396f13</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.73MiB (23.84MB) – 294,294 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f19e22551ec6938e5ddd3e227224c19e<br>SHA1: c6d8d992ffe5f1ce6e2779782e6599616599b9d1<br>SHA256: de8956f91efd6b3fd0dfaae26d079443981934e88e1d2726d6c0de965e971454</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-09-07<br>IPv6: 2023-09-07 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>189.4MiB (198.6MB) – 3,778,074 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fdbfbe40ece1329d5922d6eb6afc64c0<br>SHA1: a80a39059166ed953f515b060e2acdce246d1070<br>SHA256: 9b24dae9747a0499a77d8fe148a1fd0f1ec05f6b9556d52a196076b0ad0f8a7c</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>221.5MiB (232.2MB) – 3,778,074 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77330c438d15a0b5624ee0a2f3098a1d<br>SHA1: 59f391d1e24dfd83191e144c0e091d0106c9cc4a<br>SHA256: 5c0386f70192017ad6a3c9d84869e7c1c8625f957c92fc2e72590dfc447ac18c</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>196.4MiB (206.0MB) – 3,778,074 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ce38cf5d60338bf9f9fbe59a6ef7bd4<br>SHA1: 7ecffbcb9e01f5730c522d8ea06cecb72c0e2794<br>SHA256: 0864b694d46ec8ab4b2d8c4b3b5c08a2f9e24d7e4e1096b965cbc0814dda6d13</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.7MiB (212.6MB) – 3,778,074 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4aad338d06f994bc01a1bf3fd11324aa<br>SHA1: dedd63404f5f1a23f2ee56dc47acd91096769f72<br>SHA256: 352ed86e508b92eb38713182873c415bd60e1ffd8f826d1d8978009545091336</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>238.6MiB (250.2MB) – 3,778,074 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3341ed37b01de16999091f2c24b018f1<br>SHA1: a67e39ed9aacb04ca607ad13f78b371e874fbc60<br>SHA256: bb8a0fcc833c905a2edfbc027430bd3b0284ea5e072962fe62aca300fbb5e549</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.8MiB (200.1MB) – 3,778,074 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e8ff23bd8891c2622407071ded9c060<br>SHA1: 6c1cc2e911d15448ff155660853c2f3d5bf6ccda<br>SHA256: 28986f8ec579439ab1ffba57f502b1503ee61c8cb6314d758f7ebc5f99fc877b</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.2MiB (249.7MB) – 3,778,074 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff623be426cebfb90569bf355de2795a<br>SHA1: 6611b67b32ff7fa6c17b6fb7226da765bab74072<br>SHA256: 364a84bbed8bfcda93a2e2e0cf5dffaa1d8346b6ffe415fab987f80db60add37</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>203.0MiB (212.9MB) – 3,778,074 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eef996e3be767ee936459372724d721b<br>SHA1: e0a48652c1e0f816b476e0aedc845b4da730bd50<br>SHA256: 9567c9769e49e5d9306b9ef348284cdf528ee903c80321965850c7fdbf12b462</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>130.5MiB (136.9MB) – 1,301,716 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6cc27c15b1046a95baa6c18412d7e90e<br>SHA1: 29320d476989b2ac18efe47bd1060918d373ed2a<br>SHA256: 00fd940f492d9fe2dc46a3669f43459f8d5f65bec1d52fab7f48d28d1da27e9d</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>138.9MiB (145.6MB) – 1,301,716 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3b1557c90ff85dc4cf1a7d60747e7a4<br>SHA1: 07553c9a2701c2e085eab7528da79e94547e3769<br>SHA256: afc6b28b41db7b89b33aa3ad150bb4ee7a9c5aaa0ed45dfb71a5fe0ea7134b32</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>132.9MiB (139.4MB) – 1,301,716 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5baf55af74414ffe1df69cb8d9234b37<br>SHA1: 216d7b0fc8e463019f2c87073cdd71d1e27dd06c<br>SHA256: 8a3438ddc3984bc9ab0f601b4d82be8fbc5fdf674b148608d3b1f8e19abe91b4</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>134.8MiB (141.4MB) – 1,301,716 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 26d4c45f8923450fcff24127656b1948<br>SHA1: d6c139bc6163db1313be2a44e32a894445f37930<br>SHA256: 1099ecc7293fa4a5a46726bc53407f64ea801a9f830eab0b4d0dbc430ca725ee</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>142.8MiB (149.7MB) – 1,301,716 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1889465a5fe422bbff83f950e190c3ae<br>SHA1: 37e7e6f6483b14744906f62e4bacd4c3f68b4e67<br>SHA256: 01e080d9da577f4c02b81fed02783e55f9c44f34052fdfdf3ca10118c6594de3</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>131.9MiB (138.3MB) – 1,301,716 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db815d03ef5b8fd5f6455eb229dae1dd<br>SHA1: a0ad0439525ebbeb58d17e3ebb02879cb51d3545<br>SHA256: d9f4cac298557cdc44c4954e6053ecd33d8de62331b0ade9be5c8febac7f1e24</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>143.3MiB (150.3MB) – 1,301,716 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 255be94c2fd5cded37e8938edfc426e9<br>SHA1: cf00320413c9ae20b437a7a51fb548875896db61<br>SHA256: aada42c17d3b2330854a4d72163401e710946147f7d224f1db93aeeab2aa681f</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>135.2MiB (141.8MB) – 1,301,716 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6b628342738b24dadd88b06a59d9701<br>SHA1: a66f73f2c6d454fbded2f12021b6710394b75e48<br>SHA256: 3a506c3d25914ddd3937ee2917ca18d427d4e0de48ca23a4797a61a9342b1715</pre></details></small> |


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
