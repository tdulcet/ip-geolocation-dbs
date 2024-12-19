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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-12-19<br>IPv6: 2024-12-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.911MiB (6.198MB) – 295,954 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 18f706d7570984a29f9a2c2f223d9174<br>SHA1: beedda37e7f6a729824adc871bd8517cc7604e1f<br>SHA256: 44760420a205ca8946459e34bbcac8914f586e9df25b971d6ea88ae1ab53dcd4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.64MiB (12.20MB) – 176,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f466605b6af5ff3ae16cec67e2b1939f<br>SHA1: 454cb4137e320abc6185db9cd4dd05b1e08823e2<br>SHA256: 36493d126bb34f61be2deea5e1935271a489452c4726fc7a35cd0555be1ff181</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-12-19<br>IPv6: 2024-12-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.269MiB (8.670MB) – 414,073 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d38a9afee925156fd0019af2e912786<br>SHA1: b2d247355ee2dc5f11719a0fe37ffa2c61ea8e36<br>SHA256: fae4747954ca4e89250338ce45677b9681cbf87ee8de5f166d1bcf9310e03822</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.951MiB (7.289MB) – 105,746 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1594ab099b3427553581caa43ba0ff0e<br>SHA1: 479ef9cd103764dc889f000b73c67b62d5c63e69<br>SHA256: 759ea9db718a91e96f5d031676000ccd92b6002399cf69b159199473bc563f56</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-12-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>13.21MiB (13.85MB) – 661,346 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8beb1bcaa3879bd2578b76d6f03a932f<br>SHA1: bb3aa1b7c73556bc0bf351f11e379e288e694910<br>SHA256: 76319dcfb8e3e9fb28ec8a8073a3fff0dd189bbfd15f96cabb8e238c6efdaadd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>82.34MiB (86.34MB) – 1,251,260 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6eaec312d898e4f47c540794937baba<br>SHA1: 4bb4123c2b36fc7c55635e84b0a6c0e65d109b68<br>SHA256: 6e8c15a5f4dd40e44dad30c67241f99fae78b442e62141520f743cd5a35e7ea1</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.156MiB (7.503MB) – 359,168 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4fa1848a017a51ce167e1b45ef180e0<br>SHA1: d025902fca69db441cbc83871eb99ffd4b92c75e<br>SHA256: f02df1b7ee71bf749e1e43de462a3f6c365d9ed6e72e1d5c6faa86f25acb568c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.24MiB (17.03MB) – 246,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fee62599a38c614b43a277a08de845d7<br>SHA1: f6f5eddc6f61250f0fef53e42d76288b85a9971b<br>SHA256: 258dacce2a418e7297db10bd484df83410a61ac130bc1a5820b6fb0c0c58cb70</pre></details></small> |
| | | Full Location | Monthly<br>2024-12-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.6MiB (199.9MB) – 3,333,541 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f97a8dfa3d2efa2169aa49e5067082d<br>SHA1: 69f6046d5bebaecbd09f512a07ad0279a8bad58f<br>SHA256: 193177f00477af08b776744f0aa5ea8ffe08fe54bbe785733206c3c6f5ea0b02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>381.5MiB (400.0MB) – 3,700,914 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60c57063e8597965c85a15738ce2271e<br>SHA1: e6cfa1c20dff9df4b9dedd101304ed4939827a3f<br>SHA256: f48cf620380d7f79c9d8d05702be678101a193a90ef351c28ff300bad2cb1942</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-12-19<br>IPv6: 2024-12-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.918MiB (5.157MB) – 246,132 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77ef7e16cf2b6bbbd422ba2a934ef7df<br>SHA1: e1f77a047f5dba3e4ae075464e3761268e84b7fd<br>SHA256: 8dcac1f1779ff26fe9a26934fc72b4c423e9a2f1252d99e1436206cc2bf9f63c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.70MiB (19.61MB) – 284,192 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dce3866a2d21db59b0445d7ab2b5439f<br>SHA1: 62737a727dab8fc70aa7a79a6b203bedd659ee5b<br>SHA256: 2bc4972b559cd83a749cdf69acfcc9f7e1e9b63db44e48dc0e635dc639b29822</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-12-19<br>IPv6: 2024-12-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>167.6MiB (175.8MB) – 2,906,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1918be02cf5e40016993945dcdf9fe2<br>SHA1: 26d9a8404ce0b330647e6b9dec8e0dc1f37c9773<br>SHA256: beead4d706ffee13660a84a3a4fa8d161b26172c66d7d783002d7e5e9a446e97</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>223.8MiB (234.6MB) – 2,165,543 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58aa852f4471f22d59a91349fedddaa7<br>SHA1: 58ed488a65f8f18956e7b32e6e9c4c95283bd843<br>SHA256: eff43d3a7756d1032e8d1b53d8fc159639852e5511ede4f1a0b4456657557bb8</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-12-17<br>IPv6: 2024-12-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>10.09MiB (10.58MB) – 505,255 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a679f7889252a1dec56f9151d92423c<br>SHA1: 11b5ad3b1a35bd1a869dc69fece99ab5c3b9f647<br>SHA256: 0fa70f6c5bbbc7f3b91d2845159d219faa3a340862f329d418edafd6519af544</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.57MiB (33.11MB) – 479,819 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2d8affbbb3fd87a92b8557bc095162e8<br>SHA1: b9f0d74c3d47cb58677040af6a5e08e6609f6000<br>SHA256: 68c403daa3513a58045e66b1eab9b0d8d6be9b943dadcd52b248d8af285e5888</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-12-17<br>IPv6: 2024-12-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>158.1MiB (165.8MB) – 3,127,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0979dfe1a76090e7a5311061fd78b7a6<br>SHA1: 2ab4c768a288f28f5400f0216ff59c9795bc31f2<br>SHA256: f88763f420207861f732104848ab5505eb99f90dace8a146d3c6ec8b46be7c0b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>168.0MiB (176.2MB) – 3,127,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 72db2ea29235d6b95e4aac9a6c636164<br>SHA1: 69d9880ac3ced4b10f26117c9a70efdbc6eb2a7d<br>SHA256: aa58c008a7e3b4faebbd1ff53a80ec8f93da432d5e4bb5f6df7b8d7165a55a16</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>157.2MiB (164.8MB) – 3,127,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3c19dd478d1161bf0e7e4861d2bc1b27<br>SHA1: ab8ee21ed24da5a17fd4f31d121479f2ac57beee<br>SHA256: 2da8a6e64d14a7e558c14f1eb18a7c73c551224da36eef640617d745527f8df9</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>159.4MiB (167.1MB) – 3,127,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16da5b857dbf91111f8fd3d9b0a75ef3<br>SHA1: e99e0bf17af78b16daa0ebd690e63efdbd7c396f<br>SHA256: 891b41e5359ca432f129b8bd808a5d358bd8666ff0134dabd3bf2a9bb436276f</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>200.4MiB (210.2MB) – 3,127,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a49838410ddb31ecd95b7aee9dff529<br>SHA1: 5b344a14c82525847c476ef5186e980d95728ebf<br>SHA256: 193534c884d89b48837a488fe0b5a01639beb5b1e3cd06be31f76cfeeaaf7d60</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>157.3MiB (164.9MB) – 3,127,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e37048aa1365032d9e11919da0ee592<br>SHA1: babb643b6321741a338eb7209496536dfb4efdb8<br>SHA256: 284a72b0fdae2653e3746d7ac21c921a27472748aa5b5c6be848b514c47ff112</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>194.8MiB (204.2MB) – 3,127,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f56f9974a25215d81d981f102abaee3f<br>SHA1: 4fa3bc7256f4cfd1680549ac2ac26a58de52ddd5<br>SHA256: 851ec82a9849d01e72ff0395914e66722081cf25e7501dc9287d7494127269fe</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>164.0MiB (172.0MB) – 3,127,231 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c23baf7f990dd0dbfc19693fcee68e8d<br>SHA1: f7e22f6f293318b9b10a6428352c6f81050b44dd<br>SHA256: 0b2b285ef9a94158a8a08ae6f5545ea8b8be2785e534f58c6669c18241d9b850</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,717,803 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00ad98fe6bb103c6e921434d4c05b6f9<br>SHA1: 00a19b4787b77c1439654781ba412920c37e168e<br>SHA256: 85e4dd210cf8ed6b681fe8556424231e3603f609718bf639815f6487a6406990</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>164.7MiB (172.7MB) – 1,717,803 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ee8aa532f520a2846bc4772e8c53a2b<br>SHA1: 0b228a6e93467407c1c6f0f9dba26324b5c3151c<br>SHA256: 0c9ec68cfc1b4bef6a1ac9a233443d5e5cb72de227b992699d2a19bf185ea4dd</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>159.2MiB (167.0MB) – 1,717,803 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08abc59256ecab1994e69bef98e2af90<br>SHA1: d8af9fa667d6f69b2affc2cc746fa0827e8197d3<br>SHA256: 8791c08ca8ea30d23d81f9105705459dd2871fddb3a71b229c94b35e6692fb13</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>159.6MiB (167.3MB) – 1,717,803 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb1df6328cc784bfbd541585d7bee01b<br>SHA1: 2f306a5abf0690291b4c421d64b06c895760d19a<br>SHA256: 82e9d0c68c469754f885757de7e05d8ab034393adfd32321f83b62912f08c632</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>175.3MiB (183.8MB) – 1,717,803 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d086c3e4b6922e6e9aebf390c890848e<br>SHA1: 9c8cbb6dabfde38a120c66a3d7e70710a1031860<br>SHA256: 42c63f0b7b0d1276c81f82904eef3b7aad1bf636ceddfd886f753df9c245920e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>159.1MiB (166.8MB) – 1,717,803 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02f11be38fd34142269dedcc1ac072b9<br>SHA1: c7049cfc6ee0f994a81a435969ba53675eb335b1<br>SHA256: 1d014eb7c17f0a8915d7d392b767b5da02c8c812ffcb1fc17437b9d10634bbdb</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>176.8MiB (185.3MB) – 1,717,803 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df7b71f3c089317e0787cac6aac39365<br>SHA1: 3a50a74d1e10dca50e7fc412d1337b2222c8601d<br>SHA256: dd67c983e2bc38e8ddd3ebb9c0cc33816a43af55d25fcdf47193816dccda5672</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>162.6MiB (170.5MB) – 1,717,803 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7eadcf86a96675efb2d5a0c1cfef18bc<br>SHA1: bd08fceff355a9ff2abf43825281dd80efac4eed<br>SHA256: 9cfc79458e2ef38d1e94d369ddde51c220c4490850eb681a11ce24ea7ce81643</pre></details></small> |


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
