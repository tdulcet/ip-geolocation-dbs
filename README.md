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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-02-25<br>IPv6: 2026-02-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.301MiB (4.510MB) – 215,134 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9bce8f7f16a8f6b6a236af36ab99491<br>SHA1: 03945302b794d01fd0bd9c2e6da66c788b88309b<br>SHA256: 515890d3c8a7ef6e21bd0c8731b8032b7b0acd2bba5e938b1ecadbe7d89d82e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>3.699MiB (3.879MB) – 56,217 rows – 235 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6fe29b98461c42168800f1d1d238dc4f<br>SHA1: a0f125ebd1688f4166304e0f8869e669f73a8bfd<br>SHA256: c2829cd091a83a4b9cb39da39a4780f9efe9aff41376ae0c40cca5b75a965e17</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-02-25<br>IPv6: 2026-02-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.790MiB (9.217MB) – 440,136 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed184fb0fc8de695309d88ad0794c346<br>SHA1: 681d6c3f45cd0edb9a835474bdeabd602e1fdeb8<br>SHA256: 0956c411afa035da5f3ef064056a37310087aa132813b14dce9873d10439c18f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.628MiB (7.999MB) – 116,042 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: de2d4d3e5d4eb22dd997c440ad9325f5<br>SHA1: 533f1eacd6fee3a9a3e93828fbb4f47b6baaa123<br>SHA256: c774a38e8ddccf05f2adacb5c9d7785239e3614314eafc2a22e229aa19741de4</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-02-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.14MiB (12.73MB) – 607,751 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d021f0d620b03945a14d8eb0b9f36ab7<br>SHA1: a1a2bcc9ac7dff34bb74cf7f29019d38e20db738<br>SHA256: 067e00efc5ad2becdf0ff6bf5724bca591a9b2f2bb0b84f40fb98748efc4f694</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>124.3MiB (130.3MB) – 1,888,797 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a14db9308a0b9b1333afb90cabdff797<br>SHA1: 2bca7d63e0a16909c0d788b0d17b44d4b22f1bff<br>SHA256: 06662c4cb5595c8e0dd68c1345aa124754aa3c955ea7193ddd46ceee5589b4b5</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.768MiB (7.097MB) – 339,077 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dd0181205d24255559b4c2a13fdb0c95<br>SHA1: 77c5ed2ef6799485a1ff6d1bd9aa3aef442555aa<br>SHA256: f1a904010b8cf3e5db4f0ddc1b0fed4c77f852aa52effac37a04697ddb879a37</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.90MiB (16.67MB) – 241,625 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24f8f77acea5ee52ad5d81c9f3883d7a<br>SHA1: d3a894c2e7503a5fe5168eef49e53379425930d2<br>SHA256: 80ee4bf63ff4562160eda9ba68902de89a9e28a828c048003fd188647039bf1f</pre></details></small> |
| | | Full Location | Monthly<br>2026-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>213.7MiB (224.1MB) – 3,746,829 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48770c63478550e9d616b0e8f11eb35f<br>SHA1: d754e9f10a536891a6f76b212ce1527fccbb205a<br>SHA256: 3abef96589717a094c9384cc0d2e88d16dcc6c1771a5eb42954efe056fe2caf0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>452.5MiB (474.4MB) – 4,397,969 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72d15359a3c2245bffe65895c5939244<br>SHA1: a5622976378fbaa83dd68ce8bf186161f41252b1<br>SHA256: 3c33680bdbdc577647e1e500060fa0db02dc2af50f79e20bb78a7ae7ca1b33bb</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.362MiB (5.623MB) – 268,369 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4330c0bbff3419f12c7f73fddf1cf704<br>SHA1: b4df563510fe7f5fc4e1d278ea041c62c7bdca5b<br>SHA256: e91c6b0f644a92d45674456c276b13846b9893bbf0eb311dae698ed2f3d44d57</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.43MiB (23.52MB) – 340,836 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a2d9ae09529fd0059afa4956f1793e0<br>SHA1: fdd2b4377c51cd148c50a2369808306b7c9e9c10<br>SHA256: aa8f17dc70c0dab48cba63b84addf77a95f2d154825fa5a1cc5a78e9b68ebfd6</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-02-14<br>IPv6: 2026-02-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.7MiB (183.1MB) – 3,022,797 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63a84f26611e75064d6ca0974428a919<br>SHA1: 8280052bb209735824b9571ba8e1d3219f239f41<br>SHA256: cb6a41dd6ecfae830dbf227d07287c122fd823f9a56e968851d364746039495e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.5MiB (307.8MB) – 2,844,839 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a06e5ce285e86fe3c964abd92c36fbf4<br>SHA1: d5da4217a5c723981f96fe1b85823103e5248e1b<br>SHA256: d40b02049ece0c3e7ec8afcbbbece0eda05c646fb3a3a4719bd5bbcc13b321b3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-02-24<br>IPv6: 2026-02-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.06MiB (12.64MB) – 603,561 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ffd493b2a4006c46a67f5c7bdbe06d2<br>SHA1: acdd4db97b4ce7483f5bdf453c728cbf64fe909d<br>SHA256: af4dade8c37262b80de36b3e08304e458a8fcb57c83f2bb4beb9e6f13528a78c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.58MiB (44.65MB) – 647,074 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b04381d2efa59c649b72f44e4fc03b5<br>SHA1: d1f2b9cbcca18164afae84826fc0e3d39a830c0b<br>SHA256: 6e923f1cd9fbb0765607cd938de11f9eeb08bf24e6ed2abefbca6ec608e0ba71</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-02-24<br>IPv6: 2026-02-24 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>180.4MiB (189.1MB) – 3,563,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e8d02d656dff8cf04fbb2543e4b38d9c<br>SHA1: 259710280ead7a655db56c3048ab21209ffa8578<br>SHA256: 5260c75669d807d7f8c4acf20124c801f0d80d0fa049585f60bae2ff7ad0adfb</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>191.5MiB (200.8MB) – 3,563,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d60d7f6ab5c9002f7d9ed66ecbd42744<br>SHA1: 2d587ee1ad3ddd8b968454605578dd78330280a1<br>SHA256: aa4debbf488997df86fabed61d25eb130191fdd4c4aefab444323b04e38b2788</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>179.5MiB (188.2MB) – 3,563,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65cb537e1ba02ab881f51869a98ce352<br>SHA1: b7afb79eb39b494fd897a5401f0adff4fee1ff01<br>SHA256: 88857f38a9f095df68e7ac8b53cbcc06cc6db1e210ecf9285088c39481542d01</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>182.4MiB (191.3MB) – 3,563,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2fa1600ceee5c51f5848d356eaabe3b3<br>SHA1: 3d3902424a05f4dc607f442b6109b92e9d6e7dcd<br>SHA256: 8dc28184c2621f1dad6ed4f0f10e5e0ea8b890f14d703f40bd3d30432dcf11fe</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>227.5MiB (238.6MB) – 3,563,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9af33bd082350a2ae5975438f090409<br>SHA1: 7e9db630e18168cb157f9ca5b4faf09bb2d9ee06<br>SHA256: 5e57959ef674cd45349687b03d63ff843ed305661b2c16c3adb103714cae4480</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>179.0MiB (187.7MB) – 3,563,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f801550eb371ccf84772e418a82f725<br>SHA1: ee1e4f92c78673f03104b615cd27f6fc23af88a0<br>SHA256: fcfb7724db2f44702d9dd80b057556d7400e4b65d9ee95829e00c9745431dd8b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>221.6MiB (232.4MB) – 3,563,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d777d5d41e95e3df8e8a53d1267a4a9<br>SHA1: f9e93a4e85683dbaf551b48e8483e93388d38bc1<br>SHA256: 36e94e87f7d90515242fe8f2afd98fd9c24daf3f01fae120a760f8ed47c3461c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>186.5MiB (195.6MB) – 3,563,140 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4fb946212002b8836c97f195609fe4dd<br>SHA1: 2345d82726f79f2a418d777f0963deb795c37348<br>SHA256: 190bd856e2aab3d0da3a336639e3a685822ce917645de755de6c955c9373ec9c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>189.2MiB (198.4MB) – 1,993,191 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 318fbbc72465e13d171b2dee89b5f1c6<br>SHA1: e51a2f30c66363ae449552cb059a540910bda3f4<br>SHA256: a6385c9574ab2eb1ae37710d5e0e29ba95a1612ffe0879a88554e5f9f81bb7e6</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>193.4MiB (202.8MB) – 1,993,191 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58287465a4cb3f84b665f8bba6628ff4<br>SHA1: 5734d3b1c7681d9196d4a490fa04c170d8898174<br>SHA256: 187104bf3654fd5da329f92aef8e7949b12606e8849b5acf9559056a87fbaa10</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>186.9MiB (196.0MB) – 1,993,191 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 836c5c5731507494fef53cf2f4c18964<br>SHA1: 414a85777921a5c7b6e4a425824bcc3fc584a145<br>SHA256: 4db989979a317f3670727d92fb64ae7f213c004d108abee45159898d2173da01</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>187.6MiB (196.7MB) – 1,993,191 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35ac33f1c78ab9ee7fe326fd30f62a0e<br>SHA1: 7d5eaf16f0c9d85d728febe51f7c9b283708a300<br>SHA256: 2d4c184ade656e763575ad900ae9fc3126ce76829addbac77b63be9d834e5303</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>208.0MiB (218.1MB) – 1,993,191 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e747e1b5a20da7432a4390f8117c7465<br>SHA1: 4d237945ade2c78f85548bd4c3cba55dc446e7f6<br>SHA256: bc9d5e6e218fb5142200979f9c81eae34b693ba240db9c7bc32ea3fdf0029d16</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>186.5MiB (195.5MB) – 1,993,191 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8d6167fe58d5e15b970343d90f90923<br>SHA1: 44c2b808efcc3d0536c00c7987c00f2673d23424<br>SHA256: 39fe4fe57c09ac45da1ebcafc106bbaedb8fb3784e3419e6891ea24125ef8aa2</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>207.6MiB (217.7MB) – 1,993,191 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a8fd76ccf9b80db5e32a629f3104b97c<br>SHA1: 2ac71469e34a58f3d5b25a4f9f48374b0965bcd4<br>SHA256: 7f15385df528b0fa8bae691f8d393c9d32fc70a7ee66d7fdd38efb1a049083d4</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>190.0MiB (199.3MB) – 1,993,191 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58bef7d6ab8d93afd6e8539870895374<br>SHA1: 87144ddc0c4d01eef53670f574cfae85424cd68e<br>SHA256: b23c70a97366a9b3d67bfbe5a6e7245dfc633d3b4b3bbac4c25f0de2eacb5378</pre></details></small> |


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
