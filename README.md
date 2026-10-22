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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-22<br>IPv6: 2026-10-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.669 MiB (5.945 MB) – 283,743 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25e2322fa52759122537f3a41bf1ad9d<br>SHA1: d163fe738ee922731e2b9c89e082b4ad3b753f57<br>SHA256: 0052d2592cf83111b6c9b29eb52c8994cd7c53090cfb30fb9f1a7eda1dda53f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.51 MiB (18.36 MB) – 266,046 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f50352e64dac605b6e4a86690cffb57<br>SHA1: d06c2d96a6eb23bd4dfd0de6c65b8141a7964add<br>SHA256: 440185b5dd2c3ace794a816a1c64ed133d32cc270597130937d201ad552fe15a</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-22<br>IPv6: 2026-10-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.172 MiB (9.617 MB) – 459,265 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b89112afe9db073310328a6d462164f2<br>SHA1: 30d33294b067dfbf51cdfbee223ff86f845a4be7<br>SHA256: ea9c142af32f1af14d5a0e398f538de86be317b09713f00294c916d0cfc0ec1c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.066 MiB (8.458 MB) – 122,697 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b257e9b5935e027ffcfba0bd68164c2<br>SHA1: 3cd6eecf49922ee3725d3f65784b3d8220e11f3a<br>SHA256: 28589dfdc188ba958b062f3d50253e1b437db2102f9a0188777d36335bb9b4e6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.41 MiB (13.01 MB) – 621,129 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05e07235e0101ab53d257af2a4f94102<br>SHA1: a66c1f41d8306ad364d9298a1db8821e3b4d3a7c<br>SHA256: 91ec676b13737b74b2d3def251e429e3279e076edc0d6ca84c07e66611ffd9dd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>81.41 MiB (85.36 MB) – 1,237,137 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1b6cd3e9612b8c41f2e5a7665bdac12<br>SHA1: 0fca48d81dc3bd43b386d9af4e74a9da60e67dce<br>SHA256: 4609190c4ee5cd91625c525b8fad3f0fc32cc31c9173dfc31d9db74a2ddb7464</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.818 MiB (6.101 MB) – 291,264 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eac94e3e3ab719ab78593afa964f45da<br>SHA1: af19435e4e57c25937afe53d6fba292805882dbe<br>SHA256: 9f6a222c0122eb47e34ee42c495df4f17830c0ee40f4a9921b8535690d3270fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>23.44 MiB (24.57 MB) – 356,148 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ce580593be34cc4df87bfe5bc81e9b4<br>SHA1: 7a4ab5ae6144faf1b72fae6b2c3be92bb30697c0<br>SHA256: adebdde6726b52568b80d2b7d08b6598f6ecc66c089d6ef69e629573f008cb40</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-10-14<br>IPv6: 2026-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.7 MiB (179.0 MB) – 2,951,725 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68b1b79e84df6b26076250d820ea0b18<br>SHA1: dda1c9fc8b5b7c2a62cf7a72bf999fc82e55255b<br>SHA256: e664ee3e96917e7ba878660728524375c22f39e4e3aee5f4eda024aeac6910dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>306.4 MiB (321.3 MB) – 2,967,535 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0fa4ebcfb46463ed745e92304c503838<br>SHA1: df8c366979b5a5c5a906cf825f26a8437c8d2081<br>SHA256: d04f2b9be41819f8c7cc2d6f4075f927287880b221d8d14a85195ba76acecbb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-20<br>IPv6: 2026-10-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.28 MiB (11.83 MB) – 564,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fba0afd918140ce68a481f8c8b42e5b<br>SHA1: 9c42a026d8392f19b169072f46c2d4a3d5e9e6ee<br>SHA256: 835125e4362a0728676792407eba0206bc7916332cc05c1e6f19ccdb37e14946</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>32.89 MiB (34.48 MB) – 499,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0d3c118d8d3427882ea2de328273c1f<br>SHA1: 1467944acde565961da5cd53f06fff582ccba6fc<br>SHA256: 3c783addbd98131f3c160a8ecb8795d555ee715a371456a2f413295ffee170ff</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-20<br>IPv6: 2026-10-20 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>188.1 MiB (197.2 MB) – 3,666,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0f1ed41a68091f4cf6f04d642b75773<br>SHA1: 0644056a403513c766294229afe1958007bbe829<br>SHA256: c5eb3155ee679636b2888a9d5695861cfaa8352a6ae675469d8816d459483ad1</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>196.8 MiB (206.3 MB) – 3,666,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01a17126b6e3999202276dbfe41dd8c5<br>SHA1: 1dc2f2458dbb9ae07d0d8a36700639e30e87eec7<br>SHA256: 490dd5d40914bb83055d162790b8bb5f2d67a210a4d4c6d78cc3be3e3caefb4b</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>187.1 MiB (196.2 MB) – 3,666,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6ab103c65fdc117b77558b2b2b570ed<br>SHA1: 6e8adc41257caa5c4d9d6755d027c3c4d483fc4e<br>SHA256: 07ab36d3dd81bc33a88d9dd6f1b1901336e6abc75b92ed044130749ac64e3532</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>188.7 MiB (197.9 MB) – 3,666,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 546f35f3c63099cb0a554e33f565337d<br>SHA1: 9582fbe42e63fed08968aa0f899016b18f30ae65<br>SHA256: 27a484b3f4c24a46a791678c7357fad3dd2dcee0277d0c67531ef850da96053d</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>237.8 MiB (249.4 MB) – 3,666,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99c333dd687ac9ac39fd01b8929b43b6<br>SHA1: f499d947dcf11313dac73a17f0cecf75f7fe06ae<br>SHA256: 6af26e08a1764ebf13dd18b6809513e26d40d79ac27fe1bca267ff0c65d1ffc0</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.6 MiB (195.7 MB) – 3,666,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 261ab05de90430f71f2191842385fe81<br>SHA1: 5eaa39dc8330b356c268b7cf086777d4d8d76baa<br>SHA256: 36a078a7471148162acb2208cf0deb37cc6e25cd942f13ffaef4bc62611a411f</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.3 MiB (246.8 MB) – 3,666,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52f577689715b005d2f5f352ba91729a<br>SHA1: fc2191e456c9339b7a6f58fda3c7a7ca8079cd27<br>SHA256: 2a03efabb243bb95fa41831ceed382aa2cd8bc9f39726b9350c0483f9fba62c8</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>192.4 MiB (201.7 MB) – 3,666,888 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ecb368797f9788df6650b0f1796f813<br>SHA1: e53b6e20f90164f35a629edd215a160c4b1538f4<br>SHA256: 6c4b1be35a2d2036eecd09ad8356587e52b18f9eced78f9b6b4d000a8257c7a8</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>199.1 MiB (208.7 MB) – 2,085,455 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48419fedb2e604c96fc48e793ce208df<br>SHA1: 2b51ea6186416d5e9df5a70322ab619d088122f3<br>SHA256: 9059b045c5e521c77bed282c03bdc729775696f4f8a9f6d09d54ba25bb20e380</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.4 MiB (212.2 MB) – 2,085,455 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c52286fa14cea3ec034087147c63c2e<br>SHA1: dc8c2f82a02f662636fdd7d25e877e07f3f28292<br>SHA256: 980f3b17879c7661ed5e7c263bbe792602dd5e8e22292bb38332c8d674fb5c54</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.4 MiB (206.0 MB) – 2,085,455 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3da4ca10ec1d5071545274f5af7d338a<br>SHA1: bc78621c13b98695b8e0673af1cc02f3ee1496c7<br>SHA256: e17798740672afdfba7d00900842f526b6976374e34ee8f846de52b531f61a15</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.9 MiB (206.5 MB) – 2,085,455 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 89be3f21c67e41d99c2d96420bde7847<br>SHA1: b485f010ec8a2b565f67ee8e975adbbcd6424d23<br>SHA256: 65ef112df815d8d16066e09eb2a56c53ef964034f85742187751f46f8a42edc8</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>219.0 MiB (229.7 MB) – 2,085,455 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9613822e5798f3ae3bea6b2cf23613ae<br>SHA1: 435c6f12b5b8af5fd3b9ac9aea8073ad5c731d5f<br>SHA256: 1084763aef4d0d427c59fa0fbb8d92a669e366034bd54faf52616b86c2717eeb</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.4 MiB (205.9 MB) – 2,085,455 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56573d9fe7634cc1982521e41db90ddb<br>SHA1: 7ef80eebca096cca2fc970925f0595de8656630c<br>SHA256: 1a09559709966bd9fe55dff6a0c00dbff1d7ad44293c97067e69eb4bc4463897</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>221.4 MiB (232.2 MB) – 2,085,455 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38f60d471ffec5b9bfaef308ee74bec1<br>SHA1: 8836851ac017f4344271b6c03b2e0a81bebc63b2<br>SHA256: 8df9d6360f65274279a8af61b072f5484ddb87d2295531373e7c00d1744ed013</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.4 MiB (209.1 MB) – 2,085,455 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a7791f1d5adc2feba92c9730317d5cf<br>SHA1: 1ff7f6184c64f228896039148016bb383d10bdb1<br>SHA256: dd5f8423ff9f777f21bc0016953fca4cdcc397837379131053743b1b1eefda4c</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
