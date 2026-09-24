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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-09-23<br>IPv6: 2026-09-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.553 MiB (5.822 MB) – 277,897 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f64828f8124cb6fd1b3dbfa350e22dca<br>SHA1: de41f7611a2a93ba99cc3da11b432b3b86cc9137<br>SHA256: c1cb03aaa474162b7d1fe7a5a66015a413bc0e264358526cb5daeb17ca5dc98f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.76 MiB (17.58 MB) – 254,748 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1d857ddbf98c89bd5208c197f61ada2<br>SHA1: 3c5eb7717c6715ab003a5b65a14b717b6ec418eb<br>SHA256: 865c3797be3008c36655196e3d1455b5219c40779c7a3ef77e49b9da1a0300ef</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-09-24<br>IPv6: 2026-09-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.139 MiB (9.583 MB) – 457,610 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c59b161e6cdb0aa1b9444e4e90af61fe<br>SHA1: 79b108c55f0564fa4899efcdf690659c6ece0b18<br>SHA256: 498799cb3d235b9178d0d7c12b2e66c9d8d78923c8a133300ef35934b78e438f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.066 MiB (8.458 MB) – 122,698 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7dbe402210cb7b5656484a4625a2878a<br>SHA1: aa6cd7b0452dee54a35d4f3ad4e189704b4988cd<br>SHA256: defb64d6a6094a846f5dd4086577123ca30f6881a4ee939f11e95fe4c3e8bf07</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-09-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.32 MiB (12.92 MB) – 616,976 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af6d4a92763a4c2971145022c36aeb66<br>SHA1: ab8e06e3536d104b26cbf1214a1fcfaf6657da81<br>SHA256: 5a2eb2910032142abbf827c546ae277856374318745459cb7126c465cd02d7e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>62.91 MiB (65.97 MB) – 956,094 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e690b67c72b89c8ed30ac6720f953d8a<br>SHA1: 4966c2c2620a723b32f89475fd8e72f73796a3f7<br>SHA256: 016ade621e418326e269edb88fddf542560e3d43bb48f6e6c907f150704fa779</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.133 MiB (7.479 MB) – 357,311 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0c47fd01af8b18cc1d5cf2004691771<br>SHA1: 6b08ac2e1f8b48e55e72f8ba6ea0079e50a1af12<br>SHA256: 63aa3454aeef9769e4f0d68b4b93b23a7d195199a50487f4db5d258d90f8b08e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>23.68 MiB (24.83 MB) – 359,841 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ed7b2550b03a35e3bcceffa4ff9516e<br>SHA1: 2f8880592eb4dfde0c92576fbc78417988b521fc<br>SHA256: ecd35f269cfec0024d6ea639910b54c657f3f1dc08ab339c3d0b0384ed3cb607</pre></details></small> |
| | | Full Location | Monthly<br>2026-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>204.7 MiB (214.7 MB) – 3,588,539 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 343b463b14a760e04ccbd188e88baa4d<br>SHA1: b7e446f674922e349cb17f01c859bc3bd62fd5e3<br>SHA256: ba1847bf8c90ff7f1ab0a19c20aae3512e9bf7a3f144673fad5d87dafbf7780a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.2 MiB (449.0 MB) – 4,160,441 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2542313832b0583d31e84cd0f9afbfe8<br>SHA1: f2d167034376bc0d28d3f5a38fe3c15945c4ba61<br>SHA256: 9c2aa7d6132f5be8f547273ac5e8f21c074f3d7a26b3f7795c642f4a3b6a9693</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-09-14<br>IPv6: 2026-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.761 MiB (6.040 MB) – 288,365 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6747ad281e6d203df87a7283739262e3<br>SHA1: 90c532db8f1cce14645149b8f5cc394de42a2c96<br>SHA256: 6a9d95b18e972f327a0f7a32b7b4d33f0e33eef14e127439bb12b976b30249fa</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.80 MiB (23.91 MB) – 346,477 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1bfa9fbed82c09b5db9b5982e8b6d9a<br>SHA1: 8ce51aafdc54a7b6766d611cfafb10502b38fca4<br>SHA256: 9bc47e288cb9732ba16dbdd489323efcc7ac2a64bf0d684bc731464539bd785e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-09-14<br>IPv6: 2026-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0 MiB (179.3 MB) – 2,957,517 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dab7122ae812dd44dc6c14b6519b1f5f<br>SHA1: 10115286d4268e45b97d687718e7f7a5030498c3<br>SHA256: 9fcf166e7c6b2ce4064e5878e3c5094a10efd8718e9f3a05b0ce3206d68189e2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>304.4 MiB (319.2 MB) – 2,948,617 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 802cd20efc7238eaddac6e73d1914581<br>SHA1: a16e3bf85f8d17952c77749f9a5547179a3e0bef<br>SHA256: 3bb02a5d77da37fb74e8ab2d2e8e28be7e39f3e0486c0af2178bdaa6b3ff86a6</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-09-22<br>IPv6: 2026-09-22 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.17 MiB (11.71 MB) – 559,255 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc5235f23be90991141696cea420e702<br>SHA1: c658a6bb8600c3bce8f9a1abec2bb13d16eb8dd4<br>SHA256: 556d94ed140a0a54933de906aea022e557fd3957ea37b2f5b91cf6cb809fff36</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>33.21 MiB (34.83 MB) – 504,750 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a11292f38d4283bdf1ac94fed303bc9<br>SHA1: 0278dca1bd3cc3124dafb72341eddb7dd587269d<br>SHA256: f2ac592b0f064039ab44fa492389b41bceac389d329f9e4d57bf967089eb44d9</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-09-22<br>IPv6: 2026-09-22 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>189.8 MiB (199.1 MB) – 3,700,188 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6349edbc3f86db88fb989300e0e311d<br>SHA1: f986efe1fabbdf5c987c4a40d455f82707034a78<br>SHA256: f41398fa1a2194be42bf707ff7abe29a45acb26a60e4c6f5879146313793b350</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>198.7 MiB (208.4 MB) – 3,700,188 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 12294b170a7e8761e488a816eb9c68c0<br>SHA1: 3e713de21132724ac6db1b43b2a694dddcb67517<br>SHA256: 3fcab832c829a0cc1ed4b1ca67936a9c4fe6e92408e9708a03943dfb1ea47278</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>188.8 MiB (198.0 MB) – 3,700,188 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bcc7e996588dd76c623682d8b81d1fb2<br>SHA1: e8a46ffa254651f7f203ca4bd60673c02a95fa09<br>SHA256: 098d2580fa8900f36a5b91242bfe136b07a2cb7765f48ffc59be910f72151f5e</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>190.5 MiB (199.7 MB) – 3,700,188 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e03ee0fdaea7af0350e9c369a1ae6f83<br>SHA1: 1d2e6b6ea63740baddfb42f365701c78a70ddad9<br>SHA256: 2c0051616586619d566fbf96e7be3c9bd525f7f082a767ebc1e17cf174d0a520</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>240.1 MiB (251.8 MB) – 3,700,188 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1cfd2504c9ac5dfd534944cd22adcff3<br>SHA1: c01e0b433962d46dd57403abc55d0041f2ca41e5<br>SHA256: a00cbb625d399b539f95420a86039813c01a5525d6192e789434ec8eed077549</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>188.4 MiB (197.5 MB) – 3,700,188 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 71b4e0b2a5d1e1d7ea23ea8ef0ee3e4f<br>SHA1: 48cc04cf9a55e7fb158db7744c78d0abef8ed3dc<br>SHA256: c1f233a5fa08e5c45b393a0eeeef033d350b419e2e7e5ddcbf6acdc559d30678</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>232.8 MiB (244.1 MB) – 3,700,188 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7994ea84cafd6edc047be2f762458c45<br>SHA1: 61026201c96d5169c330a699d9a5ae3140f792e5<br>SHA256: daf4d087526d9437baa24d222274a94bdf0da7702dce62a5b5e1dd35efd36ca2</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>194.0 MiB (203.4 MB) – 3,700,188 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0cd81c7b9a23d21d3bcad09728235c4<br>SHA1: b998311295e7e6482e164cb499370aa14bb2e08a<br>SHA256: 1badd231e183cb2d4f8e3b6b952aab323f049ea5e19c7db1d96f4a3138d934c9</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>198.8 MiB (208.4 MB) – 2,084,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d1f37c50252e22f896408a1ba8d4224<br>SHA1: 028dd6afc908118a29a5162a7b4fa6037b8fcf8e<br>SHA256: 2e7c745071c40f34d8461b8d60e6e55ff787677029530fd1a6388fc0d7609602</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>202.1 MiB (211.9 MB) – 2,084,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44d98227b5d9d9baf8f150271d465e01<br>SHA1: 4e46d094afd54dfa60d120fff9a3ea85e8c07d3f<br>SHA256: 604336967787d971fb99a25f9ab5c91e6145745a24e57524d8f0bb6b78c0f036</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>196.1 MiB (205.7 MB) – 2,084,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a65622260e07b44b439d21211081a1b2<br>SHA1: 9c6e3303edbae0678a066a063a6e33fb5c59601b<br>SHA256: 476581735a627fe8e7bad63cf27673bec511eb0b5f24a88c44e3a8bee68b34b2</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.7 MiB (206.2 MB) – 2,084,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 33d902ed50c8b9280a28aaadf7138a53<br>SHA1: 33bbbf6b6bc5ec2485cff832fd927dbee7f27f1d<br>SHA256: 4de1ac0de6a9b273907387cf9369d2c96088af10916da2ef6933e9b0abb9c795</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>218.9 MiB (229.6 MB) – 2,084,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c4b0604249a293d3af85576af01a45b<br>SHA1: 69a8da9d0cd33aedcf8b0f4369e67e8425be7e15<br>SHA256: 5077a27a332b2faf78f76de09b759c9bceec01a001b014276497a2070aa90b91</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>196.2 MiB (205.7 MB) – 2,084,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bea67938b3537023d116c5041a678902<br>SHA1: 919ee23f1d1b3a8f549b32cf0e8c14674d9711a1<br>SHA256: 209ec201e1f2598365313d188aa09addfc7cabbe18709a2971209802ba54f50a</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>218.4 MiB (229.0 MB) – 2,084,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: deb3923fe4d12b1a3f8b91e77b29e6a6<br>SHA1: 8f604b3e0a0505befe6bf98d859b4b7047b79ff6<br>SHA256: 6c8185349cfbb7e8e8c1eebd3b126cb32862b9dcb509a10b65dfed03cebd6804</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>199.1 MiB (208.7 MB) – 2,084,332 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a1b28806a01f56c8f54751145c1a54<br>SHA1: 1c1a5c6053067702d31dc1a90dd15ab9bcb83c21<br>SHA256: b1e28e42390b9e88fa6921453b7051bb78055e1f43d9e91c225bf14b12efd8a0</pre></details></small> |


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
