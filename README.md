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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-01-12<br>IPv6: 2025-01-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.990MiB (6.281MB) – 299,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5fd4a85146de1198fa9f670fd3222522<br>SHA1: ca6691e4dfa33d0f7b770638f3f239d45df46503<br>SHA256: 3bfe190d391c8344490aaabafb823f8b7cdb93378db62c3c908bde349a60fa06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.77MiB (12.34MB) – 178,905 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 46d4e676c1616d0649e991453b0fff8e<br>SHA1: d6694bddd36d826e8c0f3e76e702609bc588239f<br>SHA256: e10a9ee23a689dcfd0ffa1f7e94f1937895caeeba00634787cc1f83aa20573a5</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-01-12<br>IPv6: 2025-01-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.306MiB (8.709MB) – 415,912 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc16efe1a32ff43fb3740d7d9e9a829b<br>SHA1: 9295ea7b3facef6aa97211aade6e3262971fce13<br>SHA256: d9f198639f66ce72fb6ac35c8c1dfffe49331c5bdf6fc7af0689b711bc49a908</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.008MiB (7.349MB) – 106,618 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b378c68fb8d717ae651a08862c600fc<br>SHA1: e5ddd7225218d238e3df3e90d38c499e972c910b<br>SHA256: 37cc3432a67e72c32a0f172984aa8323b6753ab30da503052a22ec8f1b48b527</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-01-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.36MiB (12.96MB) – 618,624 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3f3d3e1d3bd217e8c8183f3eadd463a<br>SHA1: 070a1e1d993c28c9a0af925e9523282d527f92aa<br>SHA256: a28fcbb41e61e3e29c314de05113d20f257124a1d39647dc2480ca4a67787d08</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>85.15MiB (89.28MB) – 1,293,956 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db31480b42815f1240d11ec43358ff06<br>SHA1: 004ee03586fe57c4e1b8692c0d48c10fbc2ca6e9<br>SHA256: 83f55257b119aafde5668c3555e0eb515b536ad8165df18fe8284bf0613b5ec4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.948MiB (7.285MB) – 348,457 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83bc658c1ea05ee0c1dd67b508e416c8<br>SHA1: 70aa579150d7be548067432da89e0057b10e615d<br>SHA256: 636b0495d96e6e73c2fd6a2d599b3713d050acf8c2bc75556af8ad5d0fb3f95d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>15.36MiB (16.10MB) – 233,400 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea165adc6016bf7241db413dadd9d616<br>SHA1: c2e689ee2f5aa199cdf34e7bb0a4facf213548c1<br>SHA256: 40a1cbecef33f526b989ce930aa6fc2a0952064828188fe18df5b777d10b8d72</pre></details></small> |
| | | Full Location | Monthly<br>2025-01-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>187.6MiB (196.7MB) – 3,275,051 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45ca665aabf2aee0b7c39b4545a5f75e<br>SHA1: 027d0a8a8014da5f6fc12e62c926c6933687bbf0<br>SHA256: 249e041ad20b36d2aebf8acd5c4d86a5f88957c86f3a7137f906df3200c6f623</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>347.2MiB (364.1MB) – 3,369,294 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb9eca947a082a3f2644b8c6907a6194<br>SHA1: 6d3040b4badad6d8c3e74a1fc773d997d8a618af<br>SHA256: 4d20b8e6b46f24b32ed9d99c2e5316f3c7e940a92aafbfdc42bea1eb6751282e</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-01-12<br>IPv6: 2025-01-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.096MiB (5.343MB) – 255,041 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 385e7d39a49da4f7b26b8ca022e788dd<br>SHA1: 7bfbc318f06616719765ecf95f9c600ee41826cd<br>SHA256: bc2cb4bb17afe8e3962b87a8deb428f68ff7083def1f45c295c77d61751a71c1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.13MiB (19.01MB) – 275,512 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3010eb9cc5eb5d69c08e40e6ada6b77<br>SHA1: b14d2ac80fc5b7043024cae2173668671a286f87<br>SHA256: cbf1a41317aa32c82f0ad9508afdfa47f673246f62711d998001fdfe0a7f5b17</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-01-12<br>IPv6: 2025-01-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.4MiB (185.0MB) – 3,056,590 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a976173ff14b69a2f374b84348a7b747<br>SHA1: ffcd6b20ec9ef8f0b9dc4f4c901e9fbf0f87075d<br>SHA256: b58bb3a37215ab1b1889208c52164428b5c56380cff711b82b6e54e5febfc1e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>226.7MiB (237.7MB) – 2,193,791 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fbc49d9a6e454cea9f8835d6e2277f3<br>SHA1: 9bfe0073a0141bc90622c08c9161a7283d562072<br>SHA256: 451e6a13f9d9293ed3e076c9bca96a945e2b1e2fd52e8171481f1a31a9e2be46</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-01-11<br>IPv6: 2025-01-11 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.12MiB (10.61MB) – 507,031 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0485c79f9cfd348e01173588a80f93e4<br>SHA1: 8147d289085ccbf0450f199b3812645cbe4a5469<br>SHA256: 305aaf238f8182b1d050da356ffe98cedbc3a364a5c8ee153d8a5546313db243</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.53MiB (33.06MB) – 479,172 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 579e3913b1b6d81e4186fdcaa63089f2<br>SHA1: 72b1437c6217c79f1a3506d3f3136d46618ce8e0<br>SHA256: 8515e259c3fffd64c0e8fe74a410ff1ddc1337c6c42ed634c00e384aa2a3538e</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-01-11<br>IPv6: 2025-01-11 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.0MiB (173.0MB) – 3,264,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97ebdf6cd0f7f26875e3a603aeb3fa99<br>SHA1: e8f6b689bf56c50b202ec68361511fb154e05a8d<br>SHA256: 71c46c39b5183a38c95e0be6f22781505a8c1043314895480dd3cf343bfd6f6a</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>175.8MiB (184.3MB) – 3,264,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df271e1bd83c40c207341a0111e4673c<br>SHA1: c283b3b462035b2fee7bfe28410af50b5177efef<br>SHA256: b85b5b1ff03951a05c1cc80241621d265885843ac3fd778e41263d3be35b82bd</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.0MiB (172.0MB) – 3,264,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5db6f110eb958e33cdbe8ed73d729986<br>SHA1: 0b996db241f4c81ebe12dda3c4d5e1f6bc7da6ba<br>SHA256: d560ecec95630fc3367e863be8d890bf8bf3a16540813b35cb98de8ff883817b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.5MiB (174.6MB) – 3,264,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3bd2a1a7e8a57d659069a751f84b0daf<br>SHA1: 0687ee602570a0d55cba7362f304213656f3314a<br>SHA256: 28f17c4fb998e30629da36f348581476672489e478f9b4d70885d0d2c7a3c7f7</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.3MiB (219.4MB) – 3,264,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddef485516b2edc3a613c4c5164a2e03<br>SHA1: 638a4686ef7ba604052e0a91570f47e4a2558721<br>SHA256: 0eb1368606ec22f99f1ea5eec790c60e2dc2690e22cf833638940f6115572f5e</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.0MiB (172.0MB) – 3,264,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 38e3f0630773bcce366129a9a116d54e<br>SHA1: e6795a114fc4aee33b2601b029d05da555b36620<br>SHA256: 75bf108a1ca9b2e60a467545de1fec3ef2afc525f052e3a0b438560f6f3bf568</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.2MiB (213.1MB) – 3,264,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2434297298bea476633a6b0a1da6aa51<br>SHA1: 31708b798a11e95ba97588d1447f17e11a0e954f<br>SHA256: 39c4dbb19e2197bb1c79263e4414fd36ccfd30f078fb97a832079246c8962245</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.1MiB (179.4MB) – 3,264,691 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cd5b40dccfcd67189065b8296b105ac2<br>SHA1: 7888725b018238003434ded1b24f52358addb157<br>SHA256: bdd047a622739312721844df1d3f2364674e1db6b72af52ccaf1c36a46f54207</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>162.5MiB (170.4MB) – 1,731,008 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 523e9dc8cc0ba2f4bdbf74c38bd982c1<br>SHA1: 3f8d9a775e5d178bb33c15731c29472c1930223c<br>SHA256: e9c57f06fe91c18d4fa540a3b2782fa6bee4159a5a7aed848a7d76787039f9fb</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>166.0MiB (174.1MB) – 1,731,008 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f98c8a083c314f25f5ef02f349e1c51<br>SHA1: e80caf3053f9af232e09ba8871081805def4d30b<br>SHA256: 834e7288a6b8948f7d9f8d40e9aba43b2ff8bf6419072f85ba8157e26341b94b</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>160.6MiB (168.4MB) – 1,731,008 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7c5444907c868fa795fc316af952f3e<br>SHA1: 387bc389e34013a7b73944accdde9623695c4a2a<br>SHA256: 28057d2d8e39c22180aeb0e1d9b32058f3d85dcf38791b31c06cd0452424824d</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>161.0MiB (168.8MB) – 1,731,008 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dfbbe92a49f00695bfc0e5ab57e9ecea<br>SHA1: bc4cab1765a2e5f069eea5e8cf218dec269566c5<br>SHA256: 12ce5f065815f7928cf6bbab83bf1000855e563c08db7771b702e6b481753785</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>177.2MiB (185.8MB) – 1,731,008 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c500d65e5c195e8b0379f94736a3115<br>SHA1: dea9a7ebba853a8428e390bd566236eb3839121c<br>SHA256: df944e001117476acff61b7655f50d0a25f1796a13e99df9a3c3cd223f0fb8b4</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>160.5MiB (168.3MB) – 1,731,008 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf969961b3d231f3dd1b12235a355f4f<br>SHA1: f4518231b3ac25a1e70df845495b93987afc9be4<br>SHA256: bb857633187c942542dc7fdd5e6985a9ad9302dabf99d2dec9cc86632a06bc02</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>178.4MiB (187.1MB) – 1,731,008 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6001a1280935a238dd7ac9b28f393ba<br>SHA1: f4b350d4d87d50a7b9356708a75f140a7a55cc35<br>SHA256: 694c77849acf37b79cfb9e794d5a1111c5eaa44f1e8ea1d247f0ab460d0b8982</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>164.3MiB (172.2MB) – 1,731,008 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d1530904a6f19a8a4b5719cb0b88f8f<br>SHA1: 23af94d50fc264b4df60fdb49a9a4f572ff09d7d<br>SHA256: 3e0f34b70afc031b8eb15f49dd6d28948b019e04bdcfeda68c3a057ee5b5c595</pre></details></small> |


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
