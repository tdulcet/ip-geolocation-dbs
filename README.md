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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-02-24<br>IPv6: 2025-02-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.058MiB (6.352MB) – 303,309 rows – 252 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0827ba3ad57611056351bad0e831fa0b<br>SHA1: f325ea030c1366363b9d9fcb94aa9aa3a718622c<br>SHA256: 182199d7e91a0c4ce15a10a11856c559848f64b34fb0db07f434057be08a7027</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.82MiB (12.39MB) – 179,591 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 76a51399561c8a08af87eabf3436f6ec<br>SHA1: bc50c97ac7c2c19df8645613e6e342427fc51c38<br>SHA256: 1dfb0ce8bcfa5803befdb675c70b1a2edbb297799e0fa72488c83509d22511f7</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-02-24<br>IPv6: 2025-02-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.355MiB (8.761MB) – 418,402 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0d8758a1a984a372b2c652a19ab5d91<br>SHA1: e4c61dc4ce9d35a91ab1c19d855bda906f3728bb<br>SHA256: c341dcf04b9c0f1dabbd44015fc02be11760e85af458b40a26fb961be83ba334</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.945MiB (7.283MB) – 105,659 rows – 225 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b067fbb54a81586785df1eec59564680<br>SHA1: cdad72e22edff81b780bf0f6d4139f45c59d34b7<br>SHA256: bea278f016faa8321e6d0e89eefe3925f98b6aaa0af745ded6b16afd6698c0f2</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-02-23 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.49MiB (13.10MB) – 625,416 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc705a32dd589ce9b0e9e43ed065c2b0<br>SHA1: c6896fe93f1124d4592a589468e402f7cb277025<br>SHA256: 52472ffdd182857a093d84385dfb9314ef8ca7b9a549105eb949eba38f993351</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>73.93MiB (77.52MB) – 1,123,479 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f1336e339cd455dec50e1b6f6b7faa2<br>SHA1: 442c2cbd25888a2d01e3318c7580f6c9e2d562ce<br>SHA256: c076431f37122a01354f04eae012de215f5cf74e2617d10e36c5e67d0e0053f9</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.300MiB (7.655MB) – 366,133 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1883f9d3b66b213c9652b2754f1edf29<br>SHA1: eabd8daf3b6851fcbcdc502e271ee563eec33de9<br>SHA256: 48be6b4f7ce5d49e0aa80354a2b3fa8091ee7ee9484b2e9e86348dca5ad725ae</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.67MiB (17.48MB) – 253,386 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d55b4d9f7f247f6d719dfe6f22af97e<br>SHA1: e4000c982518636457b48c0db654339bbb107992<br>SHA256: 7e96626938329706c08fd7182845e644e7fc4ce49380ee1a2a98ba94e239a30c</pre></details></small> |
| | | Full Location | Monthly<br>2025-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>191.4MiB (200.7MB) – 3,348,947 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60485671c8df462635efe9a1ee688a7d<br>SHA1: 88209afd2bfcdb478271d4ffeece8c99574845b0<br>SHA256: fb480016b5d4f38aff4b0de3ca0ac0c3208eebccfe5e646d41fe4244daba799e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.8MiB (412.9MB) – 3,823,929 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b430dc9cb96e643623c473cf6e961f4<br>SHA1: 606c5485a9e97b4d4725ee4f6d1690f279e22e77<br>SHA256: 5ffa4c3b8b38e31395832d320455ced8ec5507fe92acd68682b97b3d566815a6</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-02-24<br>IPv6: 2025-02-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.106MiB (5.354MB) – 255,506 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80e1c64b5c125fb46702d19882d68845<br>SHA1: d20869dac975135625842bbcc7b817f2b47da8b2<br>SHA256: 399a14c794395d001176ed9793dc27f299e4ec2de8f90dfdedc07c6a433b0214</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.38MiB (19.27MB) – 279,282 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63b017b1edcd0613c72b27eb077caab5<br>SHA1: d04cfc8b0738a636a2e7787d56061329ecfc4174<br>SHA256: 75f4cef5e2d3c06892367ddaf51c9842b12960eb86547e026e2e127a0d551591</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-02-24<br>IPv6: 2025-02-24 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>176.3MiB (184.9MB) – 3,054,155 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b7e63fc3f917acbfd3385aa01ee6b4c9<br>SHA1: 32e4cd6190262bf917d8b7cf206924ffc9d12809<br>SHA256: 8ea4b66fa2628df42fdc49f527c411ef1916e77a858644aa2bd10598df1d2140</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>230.8MiB (242.0MB) – 2,233,220 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d3ee6ff5b739344f91652d949eaf994<br>SHA1: 2eb2eda60699cd7653ca6509c327cec4e486e798<br>SHA256: 5bb91a2e35c6d95f3c0a40e6551823c1ce8cafeda7cac1926bf871dadbb045a4</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-02-21<br>IPv6: 2025-02-21 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.992MiB (10.48MB) – 500,471 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 98fd1047336b0e8ff9351534b1563f95<br>SHA1: 206d1ab6e7b7924f3c9b3a76186bf8c3c201200c<br>SHA256: bf5d2332f8e273998b49f5713a3c7c942fff753d98a12a601354a69da6f647ac</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.40MiB (32.93MB) – 477,252 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c58c9ff2a3c03ce77ae31ca42499cb59<br>SHA1: 0084ad2e81827f242c0e79d1fdf9086278a3d203<br>SHA256: ac2039f447ffc81517e46d8521183d1cdfffa288fa6263504119dbdfe6a2eb8a</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-02-21<br>IPv6: 2025-02-21 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>165.4MiB (173.4MB) – 3,270,970 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 469a19fa6b2f5d098fa35ee8a50e5754<br>SHA1: f308083ee9213c312baa781029b30225a40786d3<br>SHA256: 2df1aed98f9d665e8a260c67dba527b16deab08b9f1898a24cf23d98e71d4ec7</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>176.2MiB (184.7MB) – 3,270,970 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce938f67ba522c980be45df4eb56aab3<br>SHA1: 7a08efd1a06ccdb7c12c716f378b50f7385b41f2<br>SHA256: f1796e540d9ef5970b78ce33b3b5aa8a00c7cd2385a24f0101bb7bf047ea28ff</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>164.4MiB (172.4MB) – 3,270,970 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 10ace2ad9e3dd587d97a7233618995f1<br>SHA1: 84fab210db3ddb0f46124c1c734ee2a43587a4a5<br>SHA256: 4e9178e4e3872caaedcffcd2ff44d5f7cfeafd65ce7f1930ad5911387b0a872b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>166.8MiB (175.0MB) – 3,270,970 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b917286385dbde6304cf27b0b1b3c6cc<br>SHA1: 350b4749991c448d9c8607f8b7ab18331c7a8817<br>SHA256: a49371e256b2d086305fec55395ebf9817cd856bc8f1985c864371892795113c</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>209.9MiB (220.1MB) – 3,270,970 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c20999895e74e02865a9b31a7902f4fc<br>SHA1: feaaff533214aa17daf0c0eb3ff314ef6c4aec4a<br>SHA256: 975b545c621b35803808bfc47603b8e3d2c5bb80b4dbae876ab2a88a995d15a9</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>164.5MiB (172.5MB) – 3,270,970 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93c3eefeee56255b3ff70ff0a2936c88<br>SHA1: d3823cf22ef1403494f06d142bcf554732b40719<br>SHA256: 4f9e2a96d28b80dedc3c0523a693f8a7e2c3bd31ee0f06a59be945c833e4a7bf</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>203.7MiB (213.6MB) – 3,270,970 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ae0bedfcd19fd8df81a8d85bb5ec58a4<br>SHA1: e8fdc776b1432a90aa261f424190031018fa07c7<br>SHA256: d76a84a71061ddfe3096379a0eadfebe41a08d32221eef64cb436c41b022fb5c</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>171.5MiB (179.8MB) – 3,270,970 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4c83a828792745c5f1ac0a44019710d<br>SHA1: 970c752beca2d9ae7d3bf185f389b071529ab7a2<br>SHA256: 50bbf92add79b699c1ca343845e977525907c3ad5967e2b353ec3c177c8441bb</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>162.3MiB (170.2MB) – 1,731,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbd4537e1ebd48a7d39bc4c46587cbb0<br>SHA1: 849c74d872134d8b4c29415e22d4ea0504dbd664<br>SHA256: e24b0b86f698e35200964c6ba6c1a43e027914f07f0234f375b0248486b1a9e8</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>165.9MiB (174.0MB) – 1,731,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ca9a550acfeba23806201216a7a2126e<br>SHA1: 7e1ac92fb52abe0a9d7b7ab16e8d05351a742a8e<br>SHA256: 6963f60ad4fe085253c3bebc036dc8ef17602010b331cd7250a4cb71d107da67</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>160.5MiB (168.3MB) – 1,731,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6d4e8ded2cf04d0d9d884519ee21f397<br>SHA1: a6d805425c5432a6ffed202a0ca0adaaec106574<br>SHA256: f1db612eaf1d1bc974ddbab49bbf11ba6e270fc711179aa9d5c1fea1315ef5f5</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>160.9MiB (168.7MB) – 1,731,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e20e21b379cd7ce444211a062b22dde<br>SHA1: 376210d83de0c57ccf17af2cc7bfc4de2b125b9e<br>SHA256: f39c4e1840dd0d1c2f50c304c34f804eda5b91cf9b20629c843a9180a6e3946f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,731,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 07afca1004e2d1b4ca4001ef5f415a23<br>SHA1: 1cdaf865997469a1cf3cb22fd33511e3cbb925e5<br>SHA256: 39df2a68ccfdf9bcb0ec5ed47e5a5ceace924cb9d6b5dad2eb4404775138897d</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>160.4MiB (168.2MB) – 1,731,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4d00945b29bb7a06d0c002bfefce5b1d<br>SHA1: 336b7929e638bd7ccb1aefb26e0b34203aebabf9<br>SHA256: aa48332eb5d4dd5ee1712dfd53eecb6a02b2b942c2542fc9a7c8a83332c01754</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>178.2MiB (186.9MB) – 1,731,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5c4a220142f4a5fd4e6b4a4006963dd3<br>SHA1: cefe9e26098749ec0ee9db69550084526734b048<br>SHA256: bf83a6e92eb280b163039e1581f8e91da0f0e500b58032f11cf897eed0362728</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>164.0MiB (172.0MB) – 1,731,048 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6cd6ab7fbe292e1106739e1d9a752f54<br>SHA1: 965c69bf9f80b4c4dd48c297244e2567c1742529<br>SHA256: 7f9ff9e40416ed07b664465b0405a0c1ec0ea9f04d5e6a092733882565d0e4a8</pre></details></small> |


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
