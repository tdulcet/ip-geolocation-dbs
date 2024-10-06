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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-10-06<br>IPv6: 2024-10-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.900MiB (6.186MB) – 295,402 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7bfc56d7055146bf2e5d1d423f6538b9<br>SHA1: 211ab835ef0c984f973fc66076621316c75347bd<br>SHA256: d3de82d862363822865a5ec64a21db25bf0d59ed18357229e6f288946813ec36</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.40MiB (11.95MB) – 173,249 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7259a6f2c7a9ddf727851da8d8ac5c0f<br>SHA1: 9e75bffe8d93020b228ece424d6d18996da7d3c5<br>SHA256: 1b5911cf2439964ac37e4b74fdbf053283771f7080101e2887ea4dc9a95f4732</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-10-06<br>IPv6: 2024-10-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.174MiB (8.571MB) – 409,321 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f4e6488642100751242a9640035e642f<br>SHA1: bc265ee7c427403195e52e8ee6f263411f7ebddb<br>SHA256: 1fab378037972b8f0cc4b075e8603e9acab122e699a557eb62ee8d80bc54db45</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.917MiB (7.253MB) – 105,235 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 895325126d9e57b4f342b04c6b2c3e0c<br>SHA1: 1b6a02c2f12f887d2587c87cdc2d3ed9297c61bb<br>SHA256: 7efaafa87b51877d085a3ae36e7051b803834db4fa83dc6f1a39a94c587113a7</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-10-05 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.79MiB (17.61MB) – 840,017 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56e67a59e2757db028c4eb8673467d59<br>SHA1: 8539be405e55785364bbf2b59d4f3679e9fb196a<br>SHA256: 65c90b766f4973a1a590312e8579f440559a81867963386461586fc014290393</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>66.13MiB (69.34MB) – 1,004,890 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06985670ffa5c3df8006f69f6df938db<br>SHA1: b0f0455fef91c0df724613d16d82d85c1ab2fe42<br>SHA256: ed063c66c9a3a95dadeb224047068e4a0dbfa224e1c54104a9f800f11b72623f</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.939MiB (7.276MB) – 348,549 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1934c9e84da4a70171fa8a58df792d1<br>SHA1: a9efc628d84ddb0c5ec270a44c413d6e2e413eac<br>SHA256: 8974ef5ef8832adde54bf8eff5b734fbc419e040b6a1ba06eee6302c327937de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.54MiB (17.35MB) – 251,406 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccee8212e47dad6f6d37a7875599a267<br>SHA1: f12a6f633e3f93b21d90f94868a5dce0099a8f68<br>SHA256: fe5508fad3836313166aa43d498d12d6277cae16fef7835d5e92fdcd53bb2de4</pre></details></small> |
| | | Full Location | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.4MiB (197.5MB) – 3,289,697 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a0426270d27872fad498a291900b10d<br>SHA1: 4f4a7ccb4910df8d359d2ad76a1bd80c4be37d61<br>SHA256: 6869bc8bd2854724fd6be12e1a0efa4bf028d598fe1d116783216884c78d9f3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>362.7MiB (380.3MB) – 3,515,904 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b742d904c555f3e530341708e40522<br>SHA1: e367baa432e03a59b81c286e5f9bfaeeb0617eec<br>SHA256: f946dbe0156a23fd65f4c67f8c95dfc19e8984bc7f84d8323fc5c478da017055</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-10-06<br>IPv6: 2024-10-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-10-06<br>IPv6: 2024-10-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-10-04<br>IPv6: 2024-10-04 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.819MiB (10.30MB) – 491,882 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cee94f95862ca4894d0fc41a091557e6<br>SHA1: b924f2fb947e812044e6d0cae02b6c74fa5d832b<br>SHA256: 49c5e1a2947357f84f345dc600b4ad53a95d820d7816d8e108dda4e32111dfa1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.25MiB (32.77MB) – 474,949 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e321d51af1a8008667cd7ff8ea70589a<br>SHA1: 34a106a74b18800a01b98eae4e3aee6cce218895<br>SHA256: 409ec61daf8bab2eb262d1a0b91a2c3c4eae3065b54d08079e1bea0960f01cb2</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-10-04<br>IPv6: 2024-10-04 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>170.8MiB (179.1MB) – 3,373,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 28795f5faa786b2f00b794014c48a08a<br>SHA1: 52ef51800923e085a1330ae08e7a4badcfb12d12<br>SHA256: b2f5a4312975c9c24eebc4794f1ade6e612db01595b47d1240c7cb7d643649dd</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.5MiB (191.4MB) – 3,373,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f405c841fc6bede06d4c5336f11076a2<br>SHA1: 4df8755f704bef516bbcd1c61c1e43782daea0d5<br>SHA256: 68d8af8c1be1ce5c6ab117d899770647ac7bd0912641321348965d15b04d6d38</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>169.7MiB (178.0MB) – 3,373,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc033c38cade0b63006b85fa2f7c38ab<br>SHA1: 89c9f2e4a8b16244a530d81953a26dd8aa573e68<br>SHA256: 6aeb3453087c2f9a0d34ad107b3faa3340ffdcdbf4c5f1209f2f7280d0c8d1f7</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>172.4MiB (180.8MB) – 3,373,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aec591704a8f7b11912cdbc69fc7e001<br>SHA1: b14a700e2d1421ebeeec1cb687c61f852b4d6bd5<br>SHA256: e229983b7983130299e3e9b2cf4f4d28fa985dc31ae53c6456c763436f0272d1</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>216.6MiB (227.1MB) – 3,373,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80782cfd137b9db367322c3b49558674<br>SHA1: 68d45ca7b5428e4a38b45e0099dbaede8bf70e84<br>SHA256: 0eedfc30bb23c66b2b9242e0e505b3d6f81716eeb116081dfc1ff19ddd0fe2bf</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>169.7MiB (177.9MB) – 3,373,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75771c78673ecdd73c5492c4abcd4fcb<br>SHA1: 94bd62a9b54ec6ef9ee3e604b5d1dd63955ba412<br>SHA256: 131991633d405d01726948e612c736bd9373de63830ba107534018164d35f63e</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>210.3MiB (220.6MB) – 3,373,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d3510a7314bb634342eeca83c94ed12<br>SHA1: a584ed2a3ce4687725f9c1bb0a16bd9cfcc84e13<br>SHA256: 9eb4723bc94eb77a71c00598badc9981151e4638b22df976009bd9187c57bb47</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>176.9MiB (185.5MB) – 3,373,308 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca8885931129091abe5365d731e77001<br>SHA1: 373eba4f3811c32b616ce5b6c10350dbd923e6de<br>SHA256: e73c8f9d76eba4e6257a2f7fb0bc8fd125f827cae0c1b13bf7dc62444da33f70</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>148.9MiB (156.2MB) – 1,593,593 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ad05250dabdb5b306d13d148b6815e87<br>SHA1: 58373d31c4d98f1981f50a1f57240f76f4ea718d<br>SHA256: 586dfc093e5779173a8872252d3420d4159ac4de558c3e25e625f8b830e517fb</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>152.3MiB (159.7MB) – 1,593,593 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d7bb2a4cec633be008ed90d9a581afc<br>SHA1: e74aad842d144914268dd2faa44cd18875411ad3<br>SHA256: 03d5e1d7e1e28c1ed365ad5226d11395cfcd79a76614cf206ab4a69edd7bc1ec</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>147.2MiB (154.4MB) – 1,593,593 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47cdade70c3ce1046729aa845b4b82f0<br>SHA1: 65155a6714fe9c261351696d5199f97c1aefc3dd<br>SHA256: c39f61412a23540538687bf001917e436aa313a480ac0b4afe5ae35fb32678c2</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>147.4MiB (154.6MB) – 1,593,593 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf396efad1a3dbcaba48d7a3acc3f052<br>SHA1: b0446f96a0c26b8f23c1e8aff03f8b31ba9567b7<br>SHA256: 90b19f47aaebd8e970e460289294225e6f51263914d92b642821ab8a48cc10a5</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>161.6MiB (169.5MB) – 1,593,593 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 47cde20564b1f21a7d33295ec7e24b18<br>SHA1: aa26ecae0574e19f033d738453087728a765241d<br>SHA256: bd9ff1ce24952004ac71b2696fc8a5bfa14a8e61efd191c451de0993bc88207f</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>147.1MiB (154.3MB) – 1,593,593 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba562b672b3e93fe3901f532e81f9eb4<br>SHA1: ca5f5d6215432cea1587ac3ef8e1b0dbe7172c42<br>SHA256: 2e32b536d33f6184e97e233b9162790a923237244a638dc0bf5dc3f2f2a976f5</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>163.0MiB (170.9MB) – 1,593,593 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 577cf431d9fbce44c7ac1e60ad944759<br>SHA1: 3ba522f7e0d7142ead834e449bd420813a67a10c<br>SHA256: 6cde9307971da633c1f6d20fa75045da1155199c241170a1a5d3f2df3ddcc667</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>150.4MiB (157.7MB) – 1,593,593 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6afddb6aed17d32e10dd81200d87d834<br>SHA1: 9667f93052b960af00e0a3f04206be3d08e380c2<br>SHA256: 4e6d82d3fd191fcad129140dd87b9d484216e68b2682ea15682c5f49de711e04</pre></details></small> |


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
