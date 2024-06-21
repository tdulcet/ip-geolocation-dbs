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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-06-21<br>IPv6: 2024-06-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.736MiB (4.966MB) – 237,098 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ce9a4f00129832a003f2ccf1c7534a1<br>SHA1: b9194fd76e1a2f0dfb67ebc501d917828fdc0e36<br>SHA256: c7704fef34961e8b3ca25950ba22db0e3e8a9167c3f5558aeccbb89453030bcd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.489MiB (6.804MB) – 98,610 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42699390ad2ce3e49c705240acc82f69<br>SHA1: 4f0d99591fa7b671bf18aea7100e3a69211cfe34<br>SHA256: ad854f356a1968a7b923d5000d97d0821669511a7d172841f004c4f1b6352570</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-06-21<br>IPv6: 2024-06-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.095MiB (8.488MB) – 405,395 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c682419911bc0b2c50c7eb15f339f2e0<br>SHA1: bef4c8ac2beaf1ce1cd8694588a4a5ea69c44dec<br>SHA256: 1979e612da1ac345856818f90f9f2fff073d5ffdc9cd223f10e91d0c215b14f0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.429MiB (6.742MB) – 97,821 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e557ee50e169b4b0a7394a2e2a04b91b<br>SHA1: 24328d402379d4c2eedcdfb8456e731bfb9523df<br>SHA256: ed879cfa12bd81366716560769428a03250ac78929bce925076fd2bdf5dfd6d4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-06-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.59MiB (18.44MB) – 880,207 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c9b40ea81f3c739be7b7e04b35230c1<br>SHA1: 33f020733c4d30f34c3828f22ee75d663a80bdb1<br>SHA256: 11e7004646df9b9d3facac8c0e2b576d3152794f2eda45ecdca6e16d97aa2573</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>76.93MiB (80.67MB) – 1,169,143 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1facb814257c386997193f8f6d7cf07<br>SHA1: 9b173937d0918d76da1a96939abbbf3d00e5cdb4<br>SHA256: ddeceea0dd893eae67483271164cb55e03ba0dd16e05c278d7b38ea4c65bfb2d</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.920MiB (7.257MB) – 347,790 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228d49dd4c10c1d4778473109614f06<br>SHA1: 84aeb9072586fe27e7a2fd0cdc62b4421b417010<br>SHA256: becc801a5b95a0c7e6dea789881460b3cce70a60f8b941077db5db9f24f332a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.87MiB (16.64MB) – 241,164 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77063c075f456a1e11f7a52af24ac9ce<br>SHA1: c787ab002266a3398026d5342c963fd1ea59f3b4<br>SHA256: 72503d5df7ba2b39c61d7f574dd167649fdff103e81019ba98b18c192a045f0b</pre></details></small> |
| | | Full Location | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.7MiB (195.7MB) – 3,261,621 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d700e342b096e0b5285fb98e7ea719e<br>SHA1: 95986a4433c4d6be7ba8f0d38d9ac62adeb2d962<br>SHA256: 48ea78edb396cd5b834f2a55d80909bfe196c2ba8756c47776a331bc1537686c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>341.2MiB (357.7MB) – 3,305,843 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8cd42e639e764b6915b74d34e29681e<br>SHA1: 59487357d7497ea585a66be963038da0bd3d8c79<br>SHA256: 093ad3c5b00a0620dd5ab55a96d31fdbde283e096d5d86611cf2e0af2cb6f688</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-06-21<br>IPv6: 2024-06-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.893MiB (5.131MB) – 244,932 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffde7736a4dce2d1dc8a9bbdbbed74a5<br>SHA1: b43b198dcef1ba6df65e58c1860df753727d07a0<br>SHA256: 8724d93cfde83ae2b1ecc823b3e74fd2991e6b70f24b1547c184c710023795dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.66MiB (18.52MB) – 268,413 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0affbc6694e8124ef8380a96f029473c<br>SHA1: ee3211b937aab5e966a663960fff6c4ebac1172f<br>SHA256: 1ab2b436fcbc1c46882e731a91c9c9ace7151e260ba27191c665827291450dad</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-06-21<br>IPv6: 2024-06-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.2MiB (179.5MB) – 2,966,969 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23fb370ce2d6e35cc080047ec96854e<br>SHA1: 6375dc2f3658701b80ddbbb07172e7979cfd3c60<br>SHA256: d5616074b0d3213fccda295fa79eab456cf538541040ad6d2b330f9b8e18e286</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>192.6MiB (201.9MB) – 1,864,338 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c773064f37ebb2a011fd7af63e5eb82<br>SHA1: 2b1c4e83df9f45b9539528f8dc4a01a661ce71e9<br>SHA256: a4a6a481f67fa24ccffea017ecff51d398b6046177a33e77ad479f97889e8457</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-06-18<br>IPv6: 2024-06-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.854MiB (10.33MB) – 493,646 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8839f6c2709395d266749a37b599332<br>SHA1: 435bea83a06dba0d127324b73fc84638061999f6<br>SHA256: 6e997612af2c71983ffea36c88739faac0ce5c245b27f7bbd1cc3fdadbab5ce1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.33MiB (20.27MB) – 293,775 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 687865441875431cf683ea880769a39b<br>SHA1: 10f87600c48e2908d330a2355a67a61b53e9dfb8<br>SHA256: 3dcc47604e6146605bde9b7569843d5673427001ab9bc29bdfb8c96f0f5564a1</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-06-18<br>IPv6: 2024-06-18 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>119.8MiB (125.6MB) – 2,397,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06790f5ef0e7532ca1acb47d6f9975c8<br>SHA1: 83038bf58e9b7920966687333607950559dbac37<br>SHA256: 052d98a74d93dca8d1c2aa10d10cb4256dc423c46a51373abc13499b07bf51b6</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>128.8MiB (135.0MB) – 2,397,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31088f63bd7f8399c4257e0284cc185a<br>SHA1: 4214a29ac4ef77490b33d2dd0d6b67e587477e88<br>SHA256: 103b0f0c4050a94a5d0791ce4b6d6f513f75b7db63f73a78e5115fbd1018bd0a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>119.6MiB (125.4MB) – 2,397,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6bf70d557b7b6adac9336f81b37a499<br>SHA1: 092ff713c99f4445c284e6d53424d6cf9ff63808<br>SHA256: a6eeb7b8fe2f1ebd4d8fac6222309a1c638c53d7ea88079f279b833bc5aa8279</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.0MiB (128.0MB) – 2,397,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79739889817b3ea01fa53a6b3e365bd9<br>SHA1: 3c19b4f689f71ebbea4316295c65b5a95877c3b1<br>SHA256: 9e1a7687bc3333562e348e21226162a7fe47e38be7f1a08fba75472b7d4db937</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>149.4MiB (156.7MB) – 2,397,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c18e6caa8a1a9f3f7a042596208a1ee4<br>SHA1: ccb61c3dd709c08d4e08a2d61a6fb9f0b341ccca<br>SHA256: 192ae1206b90a5d67d37ecaa573b28f33ffa4ed4a2f2d80a679ba85ea0645907</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>118.8MiB (124.6MB) – 2,397,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbaa0d70df587d789586bab973c0c652<br>SHA1: b1e945dd347504926a9383e127c0bd758ee5d8ac<br>SHA256: 5f06bb4efc53d51a40dd58cfa0d0a04b5102a4d28685e6d2754756a0960ac899</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>145.8MiB (152.8MB) – 2,397,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8c5a2bee6bd45502e9453a354f9f916<br>SHA1: 708a4686635eab9e2213ef822e844bf33adf6af2<br>SHA256: cb541b324f6d15bd094099fb1789e7257b90c849fdf72c0af79de6937c2fd0b1</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>122.2MiB (128.2MB) – 2,397,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5932a28a48fe4fdf812dbbca1e84bb7a<br>SHA1: fe575fbcb899acce9d8ecf239ede35bffafd1ad0<br>SHA256: f76b95483a7e40fd39dc4064b95ebfa307666789e0057a79a70fbfd1e16d30f9</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>116.4MiB (122.0MB) – 1,251,503 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9a0fe13b931ae045b65dbe05d6077e0<br>SHA1: 5a4dabcbdd102c8a0e3cd1a4d6800ac158e97b08<br>SHA256: 58db9910936a19c18a6cecc077b92172482a3fc50d28cade7384d600c18709d6</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>120.4MiB (126.3MB) – 1,251,503 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81f7bc52553e4967e1b0173583fd0cee<br>SHA1: 322ab357c200772efc482ff4529f62ad66ae2d22<br>SHA256: 1ebef3546e55b80be184c003f1e7f5b2799c33fb1157b717fa6b32775797b233</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>116.7MiB (122.3MB) – 1,251,503 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 282d8715186917ae214b0dac6a657075<br>SHA1: d19c6dba7b086c95ad88c0a7131eced90fadd28e<br>SHA256: ebdd52bdfba32927a39200e3a87347096e0396d0207fa9056bd0be68712eb4e1</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>117.1MiB (122.8MB) – 1,251,503 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02bff630926b5dbad4b45ac4b9da1fe0<br>SHA1: 1fb13e4fd9092939b31b595e07e1f291d061730a<br>SHA256: ab60dd89625837f21e1f519293ba571a693581f3052f93e00332993b88c57dfc</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>128.3MiB (134.6MB) – 1,251,503 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 129e2e57629d3c11ba3c6c83a2c3ba0d<br>SHA1: 286df083927e2bbb400927fbb03c5bf111a42ac2<br>SHA256: 0454d32d6be309417aa8e94affda04907c7f9c995650891c9cd142c443da5473</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>116.3MiB (121.9MB) – 1,251,503 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05c6a2763282664521c3afec8664e05b<br>SHA1: 8382192b1ae2ee06fdc5a2bb377e97e7c3cfaef0<br>SHA256: 75045642d4fd0937988a93898fb29215e13c5bf3ce271dfdfe406c411a42061f</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>127.5MiB (133.7MB) – 1,251,503 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ebee55536e83b8dab23a0daef8ed5e97<br>SHA1: a252f7b0b971cf65992d38e07c075221c89e13a7<br>SHA256: 97a722be97a92d46bde06633118fb3aacec78a22174b41f72a6d9a2278920270</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>118.2MiB (124.0MB) – 1,251,503 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93623d478cdbe385acd3159389b900c3<br>SHA1: 45b8c8319123328cd64391068aaaf69c3b4d9384<br>SHA256: d2b5f3349250a13d65481395a08dcf230e8fa07c80dac755c2ebbf97faf9ac96</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
