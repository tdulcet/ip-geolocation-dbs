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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-04-16<br>IPv6: 2024-04-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.826MiB (5.061MB) – 241,615 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e9354ccbe869748ddbb809a765d606ce<br>SHA1: f97638fd2d0b1ab979bd4569754fe5593d78b391<br>SHA256: 7805e06ece5e75317b125e9e66d4715d740bbad94641e44e159fbc5847604ad1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.155MiB (6.454MB) – 93,531 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48d001a43ab1a135ba94b224992028d2<br>SHA1: 912936af2a4e5914a4e37f6da4c00e215d23ea4c<br>SHA256: 719e318964c0a91365da37c1d748d84670caa00dde67f163075e1113eb9ffb7b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-04-16<br>IPv6: 2024-04-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.238MiB (8.638MB) – 412,548 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83a036a6e71fd21a79ec290e57b5ff4c<br>SHA1: b67809f3bee18c2e42bad91b57d3ec4cb48dd0a3<br>SHA256: 84430fc3f62c57c58c90dc1c4ee53c690caf54bc247c3335932d930a636e9504</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.183MiB (7.532MB) – 109,280 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3f1deb3bda2e16f427527b69f195154<br>SHA1: 2031a7cfb2d6d1a172648c4f93b8b23f21caea89<br>SHA256: 6977d5df0b5066d17b137f8969f35731f2af3d7e8f1c3df13d3b6391f07c597b</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-04-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.95MiB (18.82MB) – 898,577 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21485e709319e0783652a16f9e4b63b5<br>SHA1: e15a5fbdc45f93cd589f3546bedc6ebbfa904163<br>SHA256: 5d82299faef876f24f6fb078ed477850d26fae79c0bb69680c906ab83be54832</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>74.37MiB (77.98MB) – 1,130,140 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bad88e217c14a86783a5ad21ba691ef6<br>SHA1: 8c12709284e8ab9afbddcf022a0647c69b1f214f<br>SHA256: aa020e61e756ac7ae37145d2efc0bd0cd76d11c6162c0d37d673700b8e05439f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.603MiB (6.924MB) – 331,502 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed612f6829372d96d1503867a952099<br>SHA1: d545a9307049b4d56f79cfc1544864fa920d1b6b<br>SHA256: 91dde8f7a7970c4c1b8054b947e0cca9ae1b8735bdd19fe420e6e491a7427366</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.03MiB (18.91MB) – 274,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b254c68dde265fc8d6412499c6db3dd7<br>SHA1: 2cbecfceb25b68f5f0f9889993e2f4931f5e18dd<br>SHA256: e4727e6d32df38a7582a7b9172ee67820f196bd746046a5050cd654393436920</pre></details></small> |
| | | Full Location | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.8MiB (189.6MB) – 3,159,870 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e335ee8885a5e6286297a9c06a48db0a<br>SHA1: 9b10ee274410a884c26ab662fbabb41f315616a5<br>SHA256: fc15b0d16ccdb65b6da2de506405d685d02531ce5571558ba78ed3e9110dcbbe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>322.9MiB (338.6MB) – 3,132,412 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eb566a7a93d1e35f303a2978c1da77b<br>SHA1: 78d75aa920c86cb0b75dff47ca09bb4f55bb6fd9<br>SHA256: f95d154f7a461a32269f564496c943eb8cb5e61df0269c831e76ea2f52896979</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-04-16<br>IPv6: 2024-04-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.897MiB (5.134MB) – 245,145 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86953d84c1cd0d89d0994ab1cd100b39<br>SHA1: d3303729b5fdd4e92be0090d728786a641d6bdf4<br>SHA256: 9503103e96fef9a268f0d6e3e3e189c3c227ba6a962256a4be433fec98dd6295</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.43MiB (18.28MB) – 264,858 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dee1827a7716642179bea6a3edb75c4<br>SHA1: 6d32a09ab10cd650c38bb65962cded09532e32f0<br>SHA256: d1b625011cb76995dc6c5895dea53ec54db80bd372c0878631cf89b1e7957469</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-04-16<br>IPv6: 2024-04-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.5MiB (178.8MB) – 2,955,821 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 100c457dda8054191dec8cb248ef7116<br>SHA1: 5997f43cfa17dfe7406c1480e1305b0ee4d7d2b8<br>SHA256: 2e80f7bb769fbecd8a09c918b55397ec9abeb21f176c73e5c23ca937d52e974b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,714,136 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09506237fd701236f9a08be9c399f75a<br>SHA1: 012fc8437c33186fadb2add162e68a946c843774<br>SHA256: b25eb4c33c6657facc2a0eab8012f99200c9aa7dcbc9eb0f151bcbda5e02cae0</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-04-12<br>IPv6: 2024-04-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.687MiB (10.16MB) – 485,323 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 90deb3f270192944c54e97b56c7d060c<br>SHA1: a5b5af1573f573b7e57bc5dcd3bbf6da90b19fc8<br>SHA256: 59bb62964254ed8a31e1d342c11108c1b09e2fe8043a873f0770371bb436be29</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.56MiB (19.46MB) – 282,092 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 745da3c1b2a9c5795b9031c04525068d<br>SHA1: c9fb27203cf2a147e48eb36f69e9ae38635cea89<br>SHA256: e386534360d4c109160dca1db200cc99bfcce5ef57de5a1598a82dc0053b937f</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-04-12<br>IPv6: 2024-04-12 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>130.5MiB (136.8MB) – 2,606,401 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef0a3a0cd5976dd9eb8d3e188864f9c4<br>SHA1: f83735a5b7de5633762551c513b738a794a85cb6<br>SHA256: 2c947e0f29104100a584fcc4cc4aecc1bc182dfd77e80775b09e011c23c5dcf7</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>140.6MiB (147.4MB) – 2,606,401 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d162b26ee7f132b12d0d091c72577292<br>SHA1: e87e0437d0315eed30437dc3194e238e5f230a19<br>SHA256: b8b4cccfcd642612fb5dc6bb1244a86778d34f36961bf1fb0da28a9af1d88e99</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>130.3MiB (136.6MB) – 2,606,401 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de88b2263c7a5a8f7a9d675815547e20<br>SHA1: 8f148f1c6025973087b14a90a22388fb1af3aae4<br>SHA256: 9e8a14a24a8ccfc10e1dfcb56f12a15a9f454327e00254b1091670c50de178ed</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>133.0MiB (139.4MB) – 2,606,401 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39623678fd52534d040b0d89d6043f17<br>SHA1: 069fae86cd7a13d216194f4568a83fa39bff3ae1<br>SHA256: 7b931aaca76337751bc9062b957103f5e566b8431400cc6b9bacf9b01f671455</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>162.6MiB (170.5MB) – 2,606,401 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9b57a77f97f537f233d9730b15cbd4f4<br>SHA1: 7c7cbb8c06699cd4b70207e59a679d113d143665<br>SHA256: badece465747fb446efcb5a893f86052d021b8a6215c224bb22d146d0d77a833</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>129.2MiB (135.4MB) – 2,606,401 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7474a1c8e55d3c3dd089d08575f405a6<br>SHA1: df69c6af4ecebc8d0fd2db26ec7655009d8da5be<br>SHA256: df6a3b1685f53d7019f43d5e57b3a562005653e54b5d353a99afde1b7610b639</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>158.7MiB (166.4MB) – 2,606,401 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ecc5581ffe93895503a35a7a648430a9<br>SHA1: ebc85cd4ba2a6fdedcaf2b14a06671380138560a<br>SHA256: 64e0cf85c699a8b5142061e13b6c119e12d8bd4764acc3266f3fb97f71d4b82d</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>133.0MiB (139.5MB) – 2,606,401 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18f7ef0fa591c1b9fbdb7c3c9c9a5cd1<br>SHA1: 9acc6fd94345f71e20d7bc9f4748b8d918051a1e<br>SHA256: 708b92b95802d38e7de45192f8c8c4fc7daabda3e0230aa1fc45e61bab24a6bf</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>112.0MiB (117.5MB) – 1,204,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e1dda2a291bc2dff0716db31e4a265e<br>SHA1: bec91697883f8db659c23a1c447d5f1096fae0e4<br>SHA256: b02b7fb7e1a948983937b999627230c35f2b31d19ba7bb13c7a3bc361202cd9d</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>115.9MiB (121.5MB) – 1,204,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db2034cfcfd4fd15e722d05fad75827b<br>SHA1: 5eb005e6844997f01d652e15bdae1f77c29f6ac0<br>SHA256: f4121ee25289b0df81fe55476fdf1310fba7436191de458de201ea0d82e948ff</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.3MiB (117.8MB) – 1,204,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ccf0768c19d9bb4f8e7ec14e0c3358e<br>SHA1: ba98634b27293d51e58c5e39c5c90fc42f7a7e54<br>SHA256: b98424e33993c678c7eac923bfef5f3e5b0ae16f2999ef12a9bad7973a0ec828</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>112.8MiB (118.3MB) – 1,204,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4b8cd4d4cd1e674681384f55c98c92b<br>SHA1: 1a613f3e9353dee82764ba81c5809edc6617ef76<br>SHA256: d0bf5aef61c7798e3aecd1092c6f92b3a160e9b7c950dad7c94df0a1475277d8</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>123.5MiB (129.5MB) – 1,204,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e45681536ef0991f5622c215a55cb34<br>SHA1: 7a7236a4ffcb2d32afacc915c51b25f480a59e7d<br>SHA256: 33c948896d01cfdd2b54deccdd1989b8f9439deb024ef06f7f1143361ecb76e5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>112.0MiB (117.4MB) – 1,204,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4f19bbd75740bf054612efe894e99386<br>SHA1: 8ba549ed858af5afb4e7eae87cd7f7606c0eea5f<br>SHA256: 125bdaf7cf6beabf4b133df307c075d3aa8025d2e9049cd79d852e7f828a521f</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>122.8MiB (128.8MB) – 1,204,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac06e11bf18f7c00ae668275fcac5820<br>SHA1: edf52da7fb2840ed65547ce7cbcd1ef02a883f01<br>SHA256: eee0399a49d05a2d23c0a7d170e423dc2d48fda2a538604f74d48089e60952d0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>113.7MiB (119.2MB) – 1,204,825 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 70aebac9c451bd92f5cea26ecac333bc<br>SHA1: cba81fbcdeb5a3b794d38c9bbfc90fc53c0cf400<br>SHA256: 39738f76d63e19fd8e9187dd7fbe866e35cc4b186567ece5c454b7948290923c</pre></details></small> |


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
