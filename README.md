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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-06-01<br>IPv6: 2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.852MiB (5.088MB) – 242,890 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e18888fa59a73d7f7b4708547f5081d<br>SHA1: 10ef30049ade6a54fd5020259e2e5ccaa1821819<br>SHA256: add10f4182d280545fe2c3449dcefe46c5c4932aae1b2b56f06c83634ea42d06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.403MiB (6.714MB) – 97,301 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5aadfd3c8bc1cfca1360d6d907d339c5<br>SHA1: 2705a800345902ed386d943be577f167789153de<br>SHA256: c33cbbc7920e178f76ceeb94dd09d546659aaf1c7f51a755187d2a60d57a4f33</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-06-01<br>IPv6: 2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.181MiB (8.578MB) – 409,689 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c77a702cd07c163980ffdd122e41031<br>SHA1: 7a1433b9e51f39ace80fb3003a904dc0d9ea372a<br>SHA256: 860eead29c2391f05ba91b4d4e59196d2565b842bc14189ed568b7a351545c5b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.397MiB (6.708MB) – 97,335 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd7b26197e00fe82c48566739f714202<br>SHA1: 5dd286157b4c2d55e88e177ac26b5077944d1439<br>SHA256: 2300258a616aae3b76231f03a20014ece059464b82ddf27d64392510ffad9181</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.63MiB (18.49MB) – 882,246 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f28d8346e7b5746e83f3649fb30061b6<br>SHA1: c7062188ccd8bd3333100f1ed5dd176633846182<br>SHA256: 851d7d2156d7c1bd4274a71e5e6e10c9bb3df463be54bbf0acc237af748fc13f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>76.83MiB (80.56MB) – 1,167,586 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28f32e6eb4598f25ef094d8134c44e92<br>SHA1: 5a615cec132a6055cf13860b60f657f8aab1affa<br>SHA256: 4308fd70eb56887ecf4b4b1d80d55095ea1cb5d1634efcd23526b5bc6a1ac3c8</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.920MiB (7.257MB) – 347,790 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f228d49dd4c10c1d4778473109614f06<br>SHA1: 84aeb9072586fe27e7a2fd0cdc62b4421b417010<br>SHA256: becc801a5b95a0c7e6dea789881460b3cce70a60f8b941077db5db9f24f332a2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.87MiB (16.64MB) – 241,164 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77063c075f456a1e11f7a52af24ac9ce<br>SHA1: c787ab002266a3398026d5342c963fd1ea59f3b4<br>SHA256: 72503d5df7ba2b39c61d7f574dd167649fdff103e81019ba98b18c192a045f0b</pre></details></small> |
| | | Full Location | Monthly<br>2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.7MiB (195.7MB) – 3,261,621 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d700e342b096e0b5285fb98e7ea719e<br>SHA1: 95986a4433c4d6be7ba8f0d38d9ac62adeb2d962<br>SHA256: 48ea78edb396cd5b834f2a55d80909bfe196c2ba8756c47776a331bc1537686c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>341.2MiB (357.7MB) – 3,305,843 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c8cd42e639e764b6915b74d34e29681e<br>SHA1: 59487357d7497ea585a66be963038da0bd3d8c79<br>SHA256: 093ad3c5b00a0620dd5ab55a96d31fdbde283e096d5d86611cf2e0af2cb6f688</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-06-01<br>IPv6: 2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.893MiB (5.131MB) – 244,932 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ffde7736a4dce2d1dc8a9bbdbbed74a5<br>SHA1: b43b198dcef1ba6df65e58c1860df753727d07a0<br>SHA256: 8724d93cfde83ae2b1ecc823b3e74fd2991e6b70f24b1547c184c710023795dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.66MiB (18.52MB) – 268,413 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0affbc6694e8124ef8380a96f029473c<br>SHA1: ee3211b937aab5e966a663960fff6c4ebac1172f<br>SHA256: 1ab2b436fcbc1c46882e731a91c9c9ace7151e260ba27191c665827291450dad</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-06-01<br>IPv6: 2024-06-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.2MiB (179.5MB) – 2,966,969 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a23fb370ce2d6e35cc080047ec96854e<br>SHA1: 6375dc2f3658701b80ddbbb07172e7979cfd3c60<br>SHA256: d5616074b0d3213fccda295fa79eab456cf538541040ad6d2b330f9b8e18e286</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>192.6MiB (201.9MB) – 1,864,338 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c773064f37ebb2a011fd7af63e5eb82<br>SHA1: 2b1c4e83df9f45b9539528f8dc4a01a661ce71e9<br>SHA256: a4a6a481f67fa24ccffea017ecff51d398b6046177a33e77ad479f97889e8457</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-05-31<br>IPv6: 2024-05-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.780MiB (10.25MB) – 489,913 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a9409f8206210e9bb70cb36ecd04237<br>SHA1: 9df1b5620a2ca974d5e7f7ac698505c51edd1e5d<br>SHA256: 212f7fcf4bc685aadb4e23b244ebd5cd989a68e208e6605a5b2d228c223628d3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>19.00MiB (19.92MB) – 288,715 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a65d01da0abbc3a9fd75ea0975b4cde<br>SHA1: 05cf751ea67f6e27dc1c1f5cd840933f1d982411<br>SHA256: 659797eb74ae1042577b6857bbaa783f7874aacfaf2f48e3bda1f0d82fb6827f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-05-31<br>IPv6: 2024-05-31 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>118.7MiB (124.5MB) – 2,376,235 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4995506b226f42d4c1772b345a4d69b3<br>SHA1: 6e54be8cfb008d95cd1c73ae7b4049b2ab44ddd3<br>SHA256: 08e7aaaaecdf0ab9b7ac53a9fd0577aced653b72c5d1022ab0d1a069dbe08088</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>127.6MiB (133.8MB) – 2,376,235 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 298a6cc5e642e3b0f58a5ac373672e50<br>SHA1: a3cbb05124dd1cf14bd70ea1cc8876c494c00526<br>SHA256: 1045c6858e1cebd6ac322d7c84e3f3f162a57b8dd3764114dcb667b98ed043fd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>118.5MiB (124.2MB) – 2,376,235 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f8c65f71ecd4a8e7475b47d8883d4c0<br>SHA1: c5a394f313cbc39de1d4245ab0867e7535ac2884<br>SHA256: fc30831bc96a1427f7b9f8f953e40d6b509f337702936d842ba2e9131905f8dc</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>121.0MiB (126.8MB) – 2,376,235 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5fd2abc824c0d83a23aa029caed9871b<br>SHA1: 9062e4d0f3c79911d075cbc2e51a10b53a9e3b7f<br>SHA256: f15cfa22aff0ee18b0c537fcb0517fbd7436c1a23e582e76faa17f7d2c9a713c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>148.1MiB (155.3MB) – 2,376,235 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e8f711cc99d04e224dc36d6768c304c<br>SHA1: e92de23b71e3f9c8ef7a8258350a9d913aafadea<br>SHA256: bf1621e7e657e3ea5569ea68ebba056c72e729999882d7d2b0bfd3fcee3e653c</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>117.7MiB (123.4MB) – 2,376,235 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b31274d98fef307f3c5f1250490d259<br>SHA1: 2a83c8588a670794eda3503dfd73a79322dcf082<br>SHA256: a5582821a2e245317a7fdb35c9ac26e571475106e77890a6ae47da27f0ad4b70</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>144.4MiB (151.4MB) – 2,376,235 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e062ac75be2d56d9b5e916484fbad41<br>SHA1: d184f307ac57d9207252dc7094c4f1d129f203a9<br>SHA256: c0cec85a1c3bc1632b9baa51b82bfd307765259a94e3cfcf746c2a027b5ecc1c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>121.2MiB (127.1MB) – 2,376,235 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a2c24a31a0f00fcb08e7af4f85bbe85<br>SHA1: ec386430f28c92e51815c28ce02befc39c99d481<br>SHA256: 69737170779ff98a3ef90fcc49d5844bce45cdab3b63ae6e360bc388cb2f33e9</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>110.4MiB (115.7MB) – 1,187,369 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4126a30659963e1d3153c71eaf3aee6<br>SHA1: 027b4e0e613213bfea25d7ca2d9ef99939c31409<br>SHA256: ee3ff934a2f4a7b166f6d53907efc238601c9c759f50626578e1a4e3f7e992c4</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>114.2MiB (119.8MB) – 1,187,369 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b50927f751a062c4a73c3122ef8c2de5<br>SHA1: a253df92780fa43e09981be32de6334fc47e51a8<br>SHA256: e4f32ed256809fc6bad57f5ffebe16e53d1b4fff06ed5aedd3e9db5930edeb4c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>110.7MiB (116.0MB) – 1,187,369 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ce1fb479f0b38213dae4bbe5ebc7227<br>SHA1: 15a15d7e421f00c7b9b9fe6af05b5efcbfdf7854<br>SHA256: e08d6818b21e34b517a89ddc6dd12e636cc674029fdc800415241087b69d3818</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>111.1MiB (116.5MB) – 1,187,369 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3439ffeb385312528e7aa4a87b4427f3<br>SHA1: c45a8be54083db667d8fa3ffa8e88206ccbd2027<br>SHA256: 951698cc813a047770896bf63109685f30a52a7f3805e3be0044767d7b622ee1</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>121.6MiB (127.6MB) – 1,187,369 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6ed28bc3ab14ba989390dc8a0d55e70<br>SHA1: e8a7dca9f9322525bed17b8ab0f467ffa51f112b<br>SHA256: 605b37688c876600b6c92ffa31ee826007dd916caeb96bc096f26f9237611343</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>110.3MiB (115.7MB) – 1,187,369 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8b1734a20cba0fecb36380cce4a40c80<br>SHA1: 8a27880635712426bed773e859a308352e8c808b<br>SHA256: 7acba049059c689bcd6964929672e105ebde581fe11c744bc348347d48790efa</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>120.9MiB (126.8MB) – 1,187,369 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6924937c1248589b4863ad48bd833420<br>SHA1: e21c6a81b120515adefe4edef0a96d39a860c266<br>SHA256: 76beb1bce922728c695dcbb0dbe90a342ac751481d316317b76b8700ce6e4814</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>112.0MiB (117.5MB) – 1,187,369 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe6703a2173d7127868192e6fac2f8e6<br>SHA1: f7a1969252efa08618cee180b175038126352020<br>SHA256: 72730eb5f3fff25658aafdf41f3b041d4d1d81cb757180b7609e5120c20ce6ce</pre></details></small> |


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
