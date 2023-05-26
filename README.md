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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-05-26<br>IPv6: 2023-05-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.836MiB (6.119MB) – 248,547 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecc96a84f82638c6373567aff3be4a50<br>SHA1: 62d42bc1e18f64c360168736556122f8e334a447<br>SHA256: f1d7f9de505b829b88a166f0014547564ac75f0b79b70355ef13f122bd404f41</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.522MiB (6.839MB) – 84,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd7ce6ad8e660dc9f251bcbf315d86fd<br>SHA1: c4a49b515a2d33714be77d949a7801136792b79a<br>SHA256: 5305a84e46a6199ded97a6900f27db55c75ba72a0dc4ba445100d36c69160f04</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-05-26<br>IPv6: 2023-05-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.466MiB (9.925MB) – 402,049 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82305140f84e2bd62789470b828a2339<br>SHA1: 5e1f213d0e5f8e9b670e68dd5d0d9ed303d0be5b<br>SHA256: 9fe6caf766480e9e62e20ee67adec769a4681a370a9b34b59eef9df8d24dab2d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.605MiB (7.974MB) – 98,548 rows – 221 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73bb1d1e03bccadaa04534edfc0de4e9<br>SHA1: e43111b79b97ea697937c68f842e6746e88dce9c<br>SHA256: 49524fe43647e2b9b6e04eef94c93c246b3193a2d529c73f484180ed9b9b2198</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-05-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.79MiB (14.46MB) – 589,678 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 089f9afb49bd273cf264b120221fca16<br>SHA1: 2a94b1eb601507b97795e166e2ba668ead121f5f<br>SHA256: 9b9b9d1753763b4a496f38df3f0ec6f7165dc565a55c346c0ecd56de7f17131d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>22.78MiB (23.88MB) – 294,854 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed4d35e0a67195a5e36bd45670c5c18b<br>SHA1: 6cb68ba41545191cebd11df41181da766c7fd717<br>SHA256: 569b2b081e12d9d8bad7aaacdde5019cfc9603f38550ec83ba55319bdcf0131a</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.198MiB (7.547MB) – 308,140 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00b451f6412173581a7ba389f444f7b8<br>SHA1: 3581ae37ad536ccfc344035fac8da366e6f2a1c3<br>SHA256: 2632d03fe402810c0a5cd21cb01657e4bce6686f9a35a911a634e00376fe4fc8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.40MiB (26.64MB) – 328,845 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bb8a68614ae30eed99e534875572642<br>SHA1: 0ee22a19afac3f9a7cbd864af67674fe9cfc6161<br>SHA256: 7d06dc68c40737d45ad6dc84897a8b7371ad05211dc7716db73e16c197236656</pre></details></small> |
| | | Full Location | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>194.0MiB (203.4MB) – 3,206,976 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ab320aa3a48e3e999f3451fbc5a2da8<br>SHA1: 0edbe11a0f197414c336d93dce71b581d19cd274<br>SHA256: e618d8745b11f6aff0dcb8f824c7f141c7fe734243d064f5f1fd7a093e46c571</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>365.9MiB (383.7MB) – 3,189,651 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c56df0a8c49cfc4fafc1dd0e0ea9177e<br>SHA1: 5e57dbd6ea1ad42ff4e411c9606c8f23cb91e70c<br>SHA256: 78e7ce4abf723db571f358a92321ca5b197405f36485132b7deb8c48d31a8d5b</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-05-26<br>IPv6: 2023-05-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.555MiB (5.825MB) – 236,860 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed3a236afb3c81be58fd9e618311f040<br>SHA1: c2f909455631207019aaab2b2e46e900ebf570dc<br>SHA256: e9f4b3ba35664fef476b681b4bf974f40a7c2605e7528a86ad8bd7ec533ad95b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.56MiB (28.90MB) – 491,350 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24b4cca038e3d4dcc0f42da6244a3a35<br>SHA1: 2621cb133d2002e631b0adbef75d4ea6e931756d<br>SHA256: cc4498b24a37bbe633f6502d077cf044fd12484833daf07542118c9c7c386bc1</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-05-26<br>IPv6: 2023-05-26 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,146,282 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88c13dfb1a052516749e7ea3a9487650<br>SHA1: 2e306a30fccb8fc193e5dd6bca9c2dc9b66b74eb<br>SHA256: eb792a298ee49d197c826b29bf481ad1c08529aa3138b1265dc37736edb20adb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.6MiB (400.1MB) – 4,518,262 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fdf49f6825c8d2c6839dbb6a75d33b8<br>SHA1: b3e158802b17935c7869bba17ff348eb8c749c91<br>SHA256: 5b247134a6e2438ebad87181e14b376f714b23fa9c8ca69d358366ad0778806a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-05-23<br>IPv6: 2023-05-23 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.723MiB (10.19MB) – 414,522 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cee048f49832f92edea44dfdca19bf18<br>SHA1: 30752fad112d4dd9fb4bbcc78ca0a03a1dbf91f1<br>SHA256: 45c8a266f8bb522e5ae49e23c23505ac86dbc70c794a021864ced4f6609e6f67</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.74MiB (22.80MB) – 281,452 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d4fe98eb1b2a86d130ada98162f4f7a<br>SHA1: 343b4958a3d29f3c08b7163f8b509e84e6f9843d<br>SHA256: 6e6c8139e128773863b09baccb4a648ce92cbfaa88dbe0f3e2a4dea98a318ac2</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-05-23<br>IPv6: 2023-05-23 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>192.1MiB (201.5MB) – 3,822,733 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01a0acb65162344ee4b6681ea99c0f98<br>SHA1: 355697e72e0b5b9a71433b6db9ac4ae8cf4da16a<br>SHA256: eb8d011a591854fefe6b3dcbcb4e1d7833358f47ce2b95e4845e0f97e3ebc7c6</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>225.2MiB (236.2MB) – 3,822,733 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecbe2e2f50ef2bf263561307f18cef71<br>SHA1: e9eb1ba2a9c1b7a394c4995c7b68804fa6b382ae<br>SHA256: 484fd6daae736b0f945b626055996eafcd7c6a5a6d9d64714a36d4c0cadeee51</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>198.9MiB (208.5MB) – 3,822,733 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9cd7c602c3255564b0bfe3df7dba3f3e<br>SHA1: 3270a64cc5b9afb39cad4f9adfc287609b914c7d<br>SHA256: 6d22f817daeb0624390d2af34ce2597206828b1bc4dd47ee85fbe9f6a2c3481b</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>206.1MiB (216.1MB) – 3,822,733 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: afd9fbe4305988b2621e688f55652af5<br>SHA1: 5b4768345be980e465fcb99aa0916d8ea397cd99<br>SHA256: 0b4643ed7c2fa878a833950e764b26a34aebc7fd8210d823acd1409cff9a3e6d</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>241.9MiB (253.6MB) – 3,822,733 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 810a2f6d9f3cd7588b5003acb2911d2b<br>SHA1: 5b77b98248a83a8b158347c2f949fba236dd52c8<br>SHA256: c090d25e3086303e5e6c5a140962c0b02fbfb13cbd6f97b38c640d0dc7ee6019</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>193.4MiB (202.8MB) – 3,822,733 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0fa1b8244f0efe0c8d3b0e62660d558<br>SHA1: fe165d6412bcbcaba7fc15a650c4221c75a843c7<br>SHA256: cdf4721a9bbe1bc4025c0abfda4a3115b3e518cbbe1127c05b7bebae565eab34</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>242.5MiB (254.2MB) – 3,822,733 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7ff0219f8f6485c30a501c4ffeea8a4<br>SHA1: 0770e02bcd8a7ea1cf18c5b60df24b13dad3ef76<br>SHA256: 35549489991914a521b15ba46dc5d1a79441fe5b4ea67efaa9de786457159e49</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>205.8MiB (215.8MB) – 3,822,733 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2938b909a6a2c2cfbcb2e5aa12b9e89<br>SHA1: a9db610169ceed84243154bf4c855cd90068eff4<br>SHA256: f89fd5249ac76530302a1f51d5948f0e52001c98ad3cc6e83924aeb7354fa3c1</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.3MiB (134.5MB) – 1,278,283 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc3c2bb9411b2c5350dc7f53a436167a<br>SHA1: 867576af2fde7239db8e30d74d272de04b2f98d6<br>SHA256: 2e6cd90ef4def99896fffcc2f24768de706532c3f6f238d6e6bb5dbd420e2a13</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>136.4MiB (143.0MB) – 1,278,283 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8408287999263b253be94a2cdc1f33e5<br>SHA1: caf40dc77900f6345d07560c74032d8383c5a5e3<br>SHA256: c423e8e54675329dab6405588dbb4da61689a8f56187811b7daaff102dfbc9a5</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>130.4MiB (136.7MB) – 1,278,283 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45c14942fda5b10dce90ffff0a9d87b7<br>SHA1: 25f8d2f04dfd8ef7548a0c7b89c28eda8e1221d2<br>SHA256: b519be57e8dbe19fe3a2a53948dba52b2aa5e3129d21c890104d70101ee86b70</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.3MiB (138.7MB) – 1,278,283 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9597ad11a6f5a94b562e6cb57b96c88<br>SHA1: 4d56e28af91609c621f97c368018121e9312650a<br>SHA256: e034e6f7d9454d360bbff8aa615c1f0a00b68f3286fb0f72e20ad3d81509f52c</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>139.9MiB (146.6MB) – 1,278,283 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31bad7ebbf98033dcd1ffbfa0844d793<br>SHA1: 36657bd3fd3316b68ff8db570987c48810e8657c<br>SHA256: afa1b6d9fbaea2ea294d7f9d28fe60a627b75ced9a26af359d7fd909970404ef</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>129.4MiB (135.7MB) – 1,278,283 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1823a7ef44cd0709ae25cb9ff29924d3<br>SHA1: e9fce563d56a50fc4cafefc61006645f5c9a956c<br>SHA256: 91d233e07dd3213e1dde70e531794dee09095b0ce9e42e09aef0af3320c08b7a</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>140.6MiB (147.4MB) – 1,278,283 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d5226408667c07d736bab3ae220cfad7<br>SHA1: f9ec7ae0d03d209fdb6ec075afdf1eb02e90baa7<br>SHA256: 792702141b863ffb37ef3c2eb2aed8fe4da57dd166af5f6a9ef717eccf3012fa</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>132.5MiB (138.9MB) – 1,278,283 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba6ad631c2ec4c3cba92c407039d9f37<br>SHA1: 990e2059489219b7e9ab0d7932c41b41e00982d0<br>SHA256: 471617b7d7749b4c7db56754feb142897001af22fe8e3f4dc4f08a021c883c72</pre></details></small> |


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
