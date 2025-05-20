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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-05-20<br>IPv6: 2025-05-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.233MiB (6.536MB) – 312,142 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd0bcd2b3d95fe25369a9760fb03f857<br>SHA1: aa6e66e4350864ae90986e88875a7c5f9e0f1383<br>SHA256: 1a63baa854e2a779e933ae1f7018545af2a73132946606cbd10139318d96edff</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.22MiB (12.81MB) – 185,715 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22b13a4a6efa29f63f091b16388948b6<br>SHA1: b1cdd084a631d935cbd8171e6f77bc9762d6beb4<br>SHA256: 03525bdf4606902fc1fcea098c75438331fc81206371f648830fdb3e2808f031</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-05-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.76MiB (13.38MB) – 638,637 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84a23a05293492d5fd79b3044229bb63<br>SHA1: 4eae177bbea7af8f4f92226b6ba668008ea70a34<br>SHA256: 80ac62eb81fc81570c006a712add23b2767414afcd57b02e7f6d17cd4b5663f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>102.2MiB (107.2MB) – 1,553,516 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 787b9251af7f62d950aa14bdb71a04c0<br>SHA1: 6ede2eadc92a3bc44f3bbdbffb050598b25c1071<br>SHA256: db93be69cbbeb43442d634471d60937bc0f3494225d90dd46e74e9d45478f6ff</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.057MiB (7.400MB) – 354,084 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29dc016a76e5d1ce86f281b6be610e8f<br>SHA1: 91c6b4652acafb63416678a1a40d09acb733d81e<br>SHA256: 8c2e1dc4bcb582e63e3cf9a404cef7bbda49da95853a250d12f056cd6e928998</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.75MiB (18.61MB) – 269,749 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3faba08113ae8afbe0f9aeb0c0bc4db1<br>SHA1: baf9d49de9c133023e8e928090c9f50a291301bc<br>SHA256: 126f6ef6cfb9616fb3631b757bf8a7746130d673be4019cc177df52967b9cdf0</pre></details></small> |
| | | Full Location | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.7MiB (197.9MB) – 3,293,979 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc252212886dac7c40089289aaf5a71<br>SHA1: 67fd9db8ecf45ba433418c2361c87e2627dc8c3e<br>SHA256: 6fe5f2b32b1d809aac5a716539f4708f61c901ddad9c02b4ab613c7e262ccd06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.5MiB (412.6MB) – 3,819,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14c6250f6e4e959f775581c56c6b0abc<br>SHA1: 77ffea96762cadecd4cdca9183084900fec55cb2<br>SHA256: 1bc149f9307004c4ad7c60c0f1a25333a23792c5d431b1b374511792cbfab474</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-05-20<br>IPv6: 2025-05-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.968MiB (5.209MB) – 248,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d089ecb129beaeaf2a0c4ac1427eaf6<br>SHA1: 3b494cee2f0d5a67c96e8fd9ac320d9451b36a7f<br>SHA256: cd40baf1649b683953823e24dacd7a02626143eb798e879807a24d509beef71e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.24MiB (22.27MB) – 322,743 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beb56e4b585711434b2fde993d168a9c<br>SHA1: 55d2015800e048a7089193a246f2d5b1249d4440<br>SHA256: 9d5dd5a77dc590c2642e0f671432b7bf9450c4d0347d15a7d904c0c0b55c8ba0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-05-20<br>IPv6: 2025-05-20 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,019,379 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a68d931a9c3aafbbfc0ff557db9889f<br>SHA1: d3c7b6a63aa399a3a3bca849a9160e65422ac12b<br>SHA256: a6f47823a7140f643c6df5dbe10363559d6998953d47e61148fa9ce21dbf44bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>244.6MiB (256.4MB) – 2,371,820 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db0839b0b336b2cf8a46e6bd46836924<br>SHA1: fe99a8305efd24139243b32063ad92bc72cf9fc3<br>SHA256: c7e0b4a9c07317086b1a652dca4b3928e1bcaab9d1faa273e38c74a68ee151bd</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-05-16<br>IPv6: 2025-05-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.79MiB (12.36MB) – 590,136 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dceb086eeffd58d748d981b64f638cad<br>SHA1: d58f6840a77c7708f108d3fc37f5218e2179c793<br>SHA256: 3633bb9b737793bd23f44ff41cf98c6c47bae87afa6b2aaba267bf5533d01f5b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.14MiB (42.09MB) – 609,982 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 891c155030798273de8f6c61e99aa515<br>SHA1: 5e03264c26c1d31b0378a656e35bea2de4a7d614<br>SHA256: 5a0fff631c657f0cb2cfd5dbf16f1a470bb8a825702096dd1bf0e6d8ae0a694c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-05-16<br>IPv6: 2025-05-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.4MiB (179.7MB) – 3,381,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 791df700ea42b6702c4dddb9a7aab951<br>SHA1: e2fd4485eccf82dc04a0d6b26a1f386a1b10fe6a<br>SHA256: e9b4d9ccf785bcf006bbe0ef6a9259812df2ded964c8070fca25bbff64a37d28</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.2MiB (191.1MB) – 3,381,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f349650b4b5e09e72ab224012bc954ea<br>SHA1: ad592b684d5ec0744b6efffc6bc5f2618e987cc8<br>SHA256: cb0b0fb20e4e43a22faaa6d2d5ea53b4ff56766c69c1dadcc4e336af89d52675</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.6MiB (178.9MB) – 3,381,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66aeade3f43fb365ca41a3c8a6758cbb<br>SHA1: ae21e656039298368383289b3f973eeecb8c8ec3<br>SHA256: d776c0f6a169efbed8457b5b7ca96bf536dfb2d8c730fccea476136e16671780</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.1MiB (181.5MB) – 3,381,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d6f153ac2c80a974a1fcc6d1d2dee6b6<br>SHA1: fd339dc830b8a1b627d91a786225c827f30da49d<br>SHA256: 9bc5c6ed6fc289a0e846df48e8ae51c61776a6276baefb9c74261e15401c6772</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.0MiB (227.5MB) – 3,381,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b5837019eca284d599ba2cb91bd486e<br>SHA1: a723782e2ddcca1c34967355060e3dd5f88d3f92<br>SHA256: 581e1a5047361c84434c245f00d19e62028f3a946408067807c362b0194b3109</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.2MiB (178.5MB) – 3,381,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 480062d14bbdb2c67a78cdba4af6ba1b<br>SHA1: cddd1fa541a6cceb9085d909ff6e32a8afe3cd28<br>SHA256: 4016aa0c51c58226a8dabda2b2e1ccd4e074f32f0f14958e77cf824f5327262c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>210.8MiB (221.1MB) – 3,381,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c275861da50556220408917cf6f68951<br>SHA1: 74323a0131bb21809112dd8f6bea763bdf4fe3f1<br>SHA256: fb2b3f5e72e6c6b8fdf4be02467645d2ba738158c9ae5641e9234bf36d097b3e</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.3MiB (186.0MB) – 3,381,777 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ea1317e98dde61f2679bad5ef4f933f<br>SHA1: 57c15773349adadd999239d018d10e08a7966b15<br>SHA256: 49cba0b2aab632c3bab4d74cbbeb41540c255fc7328a89837585679706db92d7</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>175.8MiB (184.3MB) – 1,867,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4b0bbd9c8270efe700f5b35065b8a8e<br>SHA1: a9d2d572fd44aa992b90df06f0510f8692333e85<br>SHA256: 01f621686e499980f585c00dbd4b9127fa8e032b26da751a3c08dea8397b18a8</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>179.8MiB (188.5MB) – 1,867,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a5d34317c4af3e9c87f1de7e037c49fd<br>SHA1: 448756bae01a0bd799351dfa9a605f8da88c2cd6<br>SHA256: e382c3eb9b780e55308c0d1717b74c7feaed95e54904ad9f7ef2dcbb494917eb</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>174.0MiB (182.4MB) – 1,867,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d8627c1e79397f13cf4547633b74018<br>SHA1: 618bf0d5920663d892e3e9aefb7f0fe759e8062f<br>SHA256: 41160ab64c599d983ab838578cb6d6b76de4a8fc8add4c69c64a29a56203dfea</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>174.3MiB (182.7MB) – 1,867,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca91f8b58167775648455d04eb282a79<br>SHA1: 0e2df4e3ca3a9e605432b21f47c806f4795ae5d5<br>SHA256: ba9d2fa77ac7ee715cb5fb1bc339c889d2de451cde9f9b7247d717bdb99347fc</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>192.5MiB (201.9MB) – 1,867,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0b161fcb856178b535f9c96fcd58451<br>SHA1: 5a6ceddb49880cd9d511a3c3e0f5e7a0c45546a7<br>SHA256: c3265ca5f2311a8eee77d1cd61fdcb0395fabacd2cf5cf6a8fac7f9121d94a57</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>173.7MiB (182.1MB) – 1,867,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aaadc1f73a525094fcc1ac96e75330c8<br>SHA1: 592db86cfc60daf93e997f6b6c8864b4130c9abe<br>SHA256: eb8381e159cec3cfff826620489c2afbba77949a09a5babbc88fca84a91ec6cc</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>193.4MiB (202.8MB) – 1,867,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d757396a48ad0db72c9e0b0a62467bf1<br>SHA1: 8103bf7d1e9b7b5f9ecbf636f7aefb892291152b<br>SHA256: 1049577aac7195b97c8f80e198db1dc23fec81d02c56b4bf5a9c32385c9d8322</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>177.5MiB (186.2MB) – 1,867,457 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5890e5945415c1ed5e7051bc70df551<br>SHA1: 0933282f54c06f0c0d094c5bbb10b5cd70da913e<br>SHA256: 5d3438de3cba94574e93751907ea08c2453cddbbb4e24b45c9d316ce6b5261be</pre></details></small> |


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
