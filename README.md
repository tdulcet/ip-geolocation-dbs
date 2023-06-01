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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-06-01<br>IPv6: 2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.823MiB (6.106MB) – 247,989 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8a8e81989020a6fb25b784dbf63a6aec<br>SHA1: 60312ef86abba7b3b8cf4bf1f0f30a19f334ef48<br>SHA256: e74692454da0d5aa697c56adf8487352442869053751421b59f54cbe6beddb6a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.535MiB (6.852MB) – 84,598 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f99043568574c142896f3ff140c572f<br>SHA1: c95659ee00f66bd392076a724a1a33cb5bc8f9e8<br>SHA256: 179f63a55f3a2a20a34634d1f8833bafc876419fc3b2bf10f27977fc70ff8777</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-06-01<br>IPv6: 2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.470MiB (9.930MB) – 402,219 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 069b903d13110d9647af3fbd2e75ce21<br>SHA1: 57d9c528d5abd4a32f551f249c618f96854b041a<br>SHA256: 61e1068a1e2f54e948dca156d59b8a38628b17e775816070132339c6dbe87f7b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.608MiB (7.977MB) – 98,584 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 838b859e947d40dd7545ec1fe2f288cf<br>SHA1: de77435d721b8eb364f5a988d8073532728d81c4<br>SHA256: 74bf21444110d22d03af58fdf129b55a2462ca3cc75d97dacb617e321627cafd</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.06MiB (14.74MB) – 601,195 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09427008fbaa47978c17f73816fa881f<br>SHA1: ae1097501172a1037e1871b76e9d3a7bca213c7d<br>SHA256: 0549271f471347fe3a2953cabf17fc784caa25ee479fe98fc2bdb5c54d6d81ee</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>23.45MiB (24.59MB) – 303,558 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e772735d91abbb3b11f2650f49e2db0f<br>SHA1: 508af908a32ddc36761896797bb6a8b56aca7a1f<br>SHA256: aee3289511ce003dfa15161fe96e0e4006b2e08baa10f22e7c5926a4e0ab0445</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.258MiB (7.611MB) – 310,670 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea16f2b91095213f9faf4261a5404be0<br>SHA1: c745544fc460b4fd9cb1ac68204736bcf9eabf79<br>SHA256: f0ea96ff5e89f5f267e07aa2f74df623e088bcb91f1df0d02845e1c412aeea46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.86MiB (27.12MB) – 334,770 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7634f17216ca6f115cf06e4df5e44bcb<br>SHA1: 60cbd088cb95f3f19ddbebb63ee62aa7d4d5943c<br>SHA256: c3c8f61cd5d80cb8dabda6b047d66bfd6d73c7d0d9eef7427890f9825a480636</pre></details></small> |
| | | Full Location | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,190,306 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f9e88d1ad989b6a665fbfd9d3b82b2<br>SHA1: e1ce63d9dae9f45709cd662cb78d5f323b9caca9<br>SHA256: ca5be0a45d234b5f3db9fd7993ca3b95fb26381d390a4e0d3e8111f2e7922199</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>351.1MiB (368.2MB) – 3,068,912 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4471e6e2accf2b2f3c070f5cb39ed63a<br>SHA1: 158105fcee685e8e94bbff314ca8be8e235b169b<br>SHA256: 82b7025d3a47fff4700bbb503d62d17692265f78fae12837a6995bed2c31d118</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-06-01<br>IPv6: 2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.582MiB (5.853MB) – 238,084 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1341c73b679015c1849651b02f8442<br>SHA1: 68ca29c935cf40cbfd663086deea4e61d8c8dc4f<br>SHA256: 4124a3662930f11954fa549834f6208912d91c3ddb53382a0c39cfaba1a71bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.40MiB (27.69MB) – 477,002 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2db255cf92eb5224035b1230f0efcc2b<br>SHA1: 4e4c6b67a3842bcdf119210a6676113f6543fa54<br>SHA256: c4335ed7e2c56df30bddbe55d518c81bb73286caae4ae123b4969eca63c72f25</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-06-01<br>IPv6: 2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,120,022 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1419e77505317334ccdf478ab7daef44<br>SHA1: 1d97a0ac2b0129e4e268083a3cbc23c627acabbe<br>SHA256: 35551439abd88f4346ee7c19bd2da4093eab3273897ca4f28e5cdb1e5d078ee1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.0MiB (399.5MB) – 4,504,439 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e04f9fe903ade529e55bb6b0d36ccdb<br>SHA1: 3f03d09739691bd6ada8c4ee23de98629caf20c3<br>SHA256: 5f023916ba65784e33d23b0934799adf20ae2b5448b40b7bd34e659f96864649</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-05-31<br>IPv6: 2023-05-31 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.708MiB (10.18MB) – 413,891 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3a17daa1307cd81f855dc14f3c4d07f<br>SHA1: 0c91b596481afade18f3a049d588b7927529798a<br>SHA256: bce2c2063357ba0ae8d00beb3d22483a257aa3979cbb6cd5630fe982a3cfaeab</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.10MiB (23.17MB) – 286,091 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6342a3f787aedc1d2d4564acb4f81727<br>SHA1: bd4c3dd89b7ee26133b13d2a9813ef4b201dcfa4<br>SHA256: 763802d288f517136b66ea91fe79aabfb35c293bd6dca121a26af7cf74e55aae</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-05-31<br>IPv6: 2023-05-31 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>188.5MiB (197.7MB) – 3,752,910 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6a9d3d67ffd62a0ea019f9dd2effe1b<br>SHA1: 8abf924fdb6a6f26c7f071ab2e92d6b5a4ef810c<br>SHA256: d72a02ee933f2e610fdc677a2d2a6c89c86b79178b6ca4bd034cacf801399ae4</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>220.8MiB (231.5MB) – 3,752,910 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a610b17d752177e3dee0710fc6d79b4<br>SHA1: cb694ac6fe29d40a5833140067aa855afde5bee2<br>SHA256: 747fb98e79de8567ff8551ecb8332149580e643a67f6f1dd10cfe03711ac286f</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.2MiB (204.7MB) – 3,752,910 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00891e070ab9aedb44be43146ddb92b6<br>SHA1: 54e665375db10d415b082d7fbb00c5af4bce285a<br>SHA256: 4f2f7450c02e1e2e71c219cbba3b656fb46d76b60a44f6279b606e555aed1c39</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.2MiB (212.0MB) – 3,752,910 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3aa45558cb32b3424a44a3c0f91e6c4d<br>SHA1: 742581be1da96ef74cbf6a11479c410a6cd7122b<br>SHA256: 50423b4cf807ec02fedfcfc00a949540a8e72a1e905996edac4ce8f884cda60b</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>237.4MiB (248.9MB) – 3,752,910 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02082e8919e150166b54e45f295b59b6<br>SHA1: 82e6d4417dbaaa26e58726cbaddfc8712450a3f6<br>SHA256: 5596e7c5ebddfeb39329876e8ea922eb92d1cc6807fdc647d1df33c6c43d2a81</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>189.9MiB (199.1MB) – 3,752,910 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9337f3f23c13cb782b289a5838b243c<br>SHA1: 0f8fcd9b94fbe1ecd7bd5c7a9950f2629bcb9952<br>SHA256: def09d57996ae7fd66370388a1964618ee8377cf1df7b36eb3fd17f543c0d767</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>237.9MiB (249.4MB) – 3,752,910 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04cb703e16a0805d13388cd5f9c75142<br>SHA1: 5dbd3ceaffcb80c5eaf7c2c36704a78257def090<br>SHA256: adca1fdeedc69b8b1a4da35785efd25ae3efc624d085259055c7beb6e2cce037</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.0MiB (211.9MB) – 3,752,910 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3c4517be1ca44cb4418d73f78556bb5<br>SHA1: aaf2b5846530cd0fa3cb14bc8cd5c107824fcf5f<br>SHA256: 70c3982a94784d282ed2d6c996f8b620398b5bfbbf47e89ddb2e1f44ff27c1d7</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.2MiB (128.2MB) – 1,219,774 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 134708253090e8d4096e19d3cd2d9999<br>SHA1: c1bdfc780fd1560c0b01a4ad7acd779447b20e73<br>SHA256: cc7e1b6efd9995b3e406b57bf35ff4b18113e7a9408919b6a888d23d7134a2f7</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>130.0MiB (136.3MB) – 1,219,774 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa2bab91a596ced614f1358bcb8026a7<br>SHA1: 37488fded96cf6ed54e916b122c82a41def2174b<br>SHA256: 192ba2b9d2fd438c8a28e99ed96aa9e368e6df4cdecdbbe9be6240dad7f60bd0</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>124.3MiB (130.4MB) – 1,219,774 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86e5bf540588623420406e4e4bc579a6<br>SHA1: 7609a777bffd5705a6bfda24e7105b883fd60f30<br>SHA256: 99b2fb7044cc963b536419a8b204c863b151f0f6ae95132661d3746e12a7162d</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.3MiB (132.4MB) – 1,219,774 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bdf4073a4cf63a8123fb442238207f4f<br>SHA1: 5cb9c4f14c1e3b1a995b3634e4f4ee919d5f183c<br>SHA256: a7511afb671f862f527a1f502faa202828adc62b3141dbb07a56b267cf3b0ed8</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>133.4MiB (139.9MB) – 1,219,774 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccccf58038a4a41d6f3c7a8931e8203d<br>SHA1: 99f27b7608b766ca55ecf5ed4b38a763e41bfdc2<br>SHA256: 13b1dcef935e3ac55f50a6008dd5ae6ec06f987d4b5bef747e3831b860d5a622</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>123.4MiB (129.4MB) – 1,219,774 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43c93ce3acce4fc9c5384ad450bfdc53<br>SHA1: 847a84c276eedc4075fe777991a07bf21d8268b7<br>SHA256: 3d8b82ca393e136687f3f4a6f4206b54d0724f0be407df9393d42b40319b2889</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.3MiB (140.8MB) – 1,219,774 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03efac05f508ef4e8610b5e5ff906749<br>SHA1: 0a1aabceecec239edbb0ae729e43ff02e07b52d8<br>SHA256: ccd55cc388381b516eee3fe4b786dfb7faa4e57a1f94ef6f00d2c0a81ccb69e1</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.4MiB (132.6MB) – 1,219,774 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c72d8a2b5bb1a3d99ab0bf9a261681d<br>SHA1: c08b316935d2c66a32af1705f2813d7745c2500a<br>SHA256: 57942322a1172af1f413f55723f056d987a3f61c569fba44f2c3f86d58a30f24</pre></details></small> |


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
