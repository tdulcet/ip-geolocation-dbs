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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-05-28<br>IPv6: 2025-05-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.252MiB (6.555MB) – 313,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a04a69b2fd6007e251f284b9d074d5f<br>SHA1: e82eaa68cecc7ea720069f4fcb590b48798e6f22<br>SHA256: 68d693658a384d1bfe7849427592a5842c275874cfb43ef857bf415186ccfa02</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>12.26MiB (12.86MB) – 186,327 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77bb4c2a51e40e017b6918eb06f5fd49<br>SHA1: 3fb08dcbb96fc74028e5954f4da5fe2c6921139b<br>SHA256: 5cf1c0c975ad9b4f39610783846f63fe23e27d9c66fc9556d435a2c5d1e22688</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-03-31<br>IPv6: 2025-03-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.377MiB (8.783MB) – 419,446 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d798b44c14b430db2043586aa3329d47<br>SHA1: c0a54d184d183c6cba057c0d4b088de3b9dd4ba6<br>SHA256: 03207fa98a82c1c301e567744e30324019b947a50bf24c47099a8acc8e46f725</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.985MiB (7.325MB) – 106,270 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fe6de760c3995afb0cd08f53f853b42<br>SHA1: d6c9b8459fc61f0cfcc9d99b6affd9d3edde81cb<br>SHA256: b3f70cafa4168850b870bc2c4365b0666d73d81889e7dab9e74dbc7b7548a790</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-05-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.91MiB (13.53MB) – 646,039 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d900fe257debee28beeb91aa56ee9a97<br>SHA1: 540f89b0933c90f4ecd1bcb0a4d8686e260575f3<br>SHA256: 4533fe3ea03e8ba1762112d3ce5f5114bcdc6586ec40d3b07315f0947d491eb3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>97.71MiB (102.5MB) – 1,484,832 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2520f37ed4b5644ddd3234d9019383b<br>SHA1: 043332d78f7922c1b698771c14b2d87173977583<br>SHA256: 1c0e55d2ad0bb0dc333763c70ee0850916259ecd9dc50ae3a3c9a2272da7553e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.057MiB (7.400MB) – 354,084 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29dc016a76e5d1ce86f281b6be610e8f<br>SHA1: 91c6b4652acafb63416678a1a40d09acb733d81e<br>SHA256: 8c2e1dc4bcb582e63e3cf9a404cef7bbda49da95853a250d12f056cd6e928998</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.75MiB (18.61MB) – 269,749 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3faba08113ae8afbe0f9aeb0c0bc4db1<br>SHA1: baf9d49de9c133023e8e928090c9f50a291301bc<br>SHA256: 126f6ef6cfb9616fb3631b757bf8a7746130d673be4019cc177df52967b9cdf0</pre></details></small> |
| | | Full Location | Monthly<br>2025-05-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.7MiB (197.9MB) – 3,293,979 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddc252212886dac7c40089289aaf5a71<br>SHA1: 67fd9db8ecf45ba433418c2361c87e2627dc8c3e<br>SHA256: 6fe5f2b32b1d809aac5a716539f4708f61c901ddad9c02b4ab613c7e262ccd06</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>393.5MiB (412.6MB) – 3,819,767 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14c6250f6e4e959f775581c56c6b0abc<br>SHA1: 77ffea96762cadecd4cdca9183084900fec55cb2<br>SHA256: 1bc149f9307004c4ad7c60c0f1a25333a23792c5d431b1b374511792cbfab474</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-05-28<br>IPv6: 2025-05-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.968MiB (5.209MB) – 248,641 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d089ecb129beaeaf2a0c4ac1427eaf6<br>SHA1: 3b494cee2f0d5a67c96e8fd9ac320d9451b36a7f<br>SHA256: cd40baf1649b683953823e24dacd7a02626143eb798e879807a24d509beef71e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>21.24MiB (22.27MB) – 322,743 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beb56e4b585711434b2fde993d168a9c<br>SHA1: 55d2015800e048a7089193a246f2d5b1249d4440<br>SHA256: 9d5dd5a77dc590c2642e0f671432b7bf9450c4d0347d15a7d904c0c0b55c8ba0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-05-28<br>IPv6: 2025-05-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>174.3MiB (182.8MB) – 3,019,379 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a68d931a9c3aafbbfc0ff557db9889f<br>SHA1: d3c7b6a63aa399a3a3bca849a9160e65422ac12b<br>SHA256: a6f47823a7140f643c6df5dbe10363559d6998953d47e61148fa9ce21dbf44bc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>244.6MiB (256.4MB) – 2,371,820 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: db0839b0b336b2cf8a46e6bd46836924<br>SHA1: fe99a8305efd24139243b32063ad92bc72cf9fc3<br>SHA256: c7e0b4a9c07317086b1a652dca4b3928e1bcaab9d1faa273e38c74a68ee151bd</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-05-27<br>IPv6: 2025-05-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.86MiB (12.44MB) – 593,798 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 714417b21798ea22311758a659052f4b<br>SHA1: 63c243c1fa28fa89514a905697c100b28e7744e3<br>SHA256: f06b51d5f4aeb567dc1c614c08328c715dc9a40da74fc29bc25b9254421b0ba6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>40.60MiB (42.57MB) – 616,971 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4662c1ba880abc8b3001b3b5fa53277a<br>SHA1: 430d26eff24c60bfb37d7db75584e4bba8ef1dd1<br>SHA256: a1ef9676d1b7fe24459b1c461c8070c9213c6460d6c0034b61527aa4ed16eed8</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-05-27<br>IPv6: 2025-05-27 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>171.5MiB (179.8MB) – 3,383,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88c9b5251931616713615cf7c8c4f761<br>SHA1: 7b395b79e331c0e241ca3286730d03c3b6ed0f01<br>SHA256: d7968bd95bec4bbfd9d89bba23253ec132b720d6f4c9eaa306367042bdbd29ad</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>182.3MiB (191.1MB) – 3,383,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fdd769058d534b66c33555be46925b22<br>SHA1: 8e42342599c3d88fff0e9db9b75fb1c754d9693e<br>SHA256: ae7a4b0cba7261bd406939eedeccd860a6aba134bb9abc7543e4134c3d42fb70</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.7MiB (179.0MB) – 3,383,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dad5eb73ecc0637e86e2f2bccb311f8b<br>SHA1: 29f3e0dbb67e839f654d2b87f988efda11c1192e<br>SHA256: e974c9160aa4131e290bd533c2f9af55eef1493684d8a3cd3728fd7254662dfd</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.2MiB (181.6MB) – 3,383,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2a341b83366b5b69a7f3f679dc6d89e2<br>SHA1: e67838a9b2f2b949eadcbf15c043a3f59eafb031<br>SHA256: 89c9a1e8766d2e288a83c1d855b111a9ce726d48ed897dfa07bd4feec67989a6</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>217.0MiB (227.6MB) – 3,383,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 511c421bb531cbeb5f5291f4eafe8b7f<br>SHA1: b01400727ea25895320e14a85d04eb1440cc6755<br>SHA256: 7240209bbd0f88d82003af1810fd4d9d6fd0945d2b46e76a7d9a5f5a88e09dc2</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.3MiB (178.5MB) – 3,383,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a9ad0b7d535c792f1b78cd66d1e5db3<br>SHA1: 1d89c583f524b9d5d19cfc4731436514454bba1c<br>SHA256: 45b77ce305e014f6c1821c0409e882915fa8ff427bdfb669ac41f0ad5788bdd8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>210.9MiB (221.1MB) – 3,383,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ebe70e53bf7e0c10dc71a6b940c9f633<br>SHA1: de4f3d02f92bf03d4072a43ac1aceab7fff50830<br>SHA256: 6cb0a8b45f0558c1e21d5cabe23b3fe9408c1a5fc475a70d1e0d1bdc96ee3637</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>177.4MiB (186.1MB) – 3,383,766 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c154cbcc9d1dbca7eef04c63ccf15c4d<br>SHA1: fac28c018b790e6a54e93c9643f3756d0257f063<br>SHA256: db281df1114d1b73cb2b1e1ec038e64a467793ebe213e2cf21aa3c9ffb069e9f</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>174.9MiB (183.4MB) – 1,858,245 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c6adcea61b49a89eeb29ecb901e22318<br>SHA1: 765c28534044c904f5937820ce4bf27e7ed3c19c<br>SHA256: 79f3ec4e9f8bb34bb75166c4f4545c9887de0f107bd3aa9c7e7799079c857b03</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>178.8MiB (187.5MB) – 1,858,245 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7caba248ca40648ecee6509ab0a2fe33<br>SHA1: 1e25b1485f66e81958c83637898140b3c36dcdd6<br>SHA256: 75c8562ecaef6f36fbf6f31871faa87ae001ee604f26ef5abf10906014f4b043</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>173.1MiB (181.5MB) – 1,858,245 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a79484503cd00df0ec902ade86ed5e1<br>SHA1: 2d6b1af64b9ae80084e697d5def89e2c4afb5881<br>SHA256: e5ac0fa152df61805f123f19b787b6d01fead7c726af68f0cdc45d45c474bb51</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>173.3MiB (181.8MB) – 1,858,245 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b4f651fbe6ca725733be9f1b90aee6a0<br>SHA1: 5fcf30487c094eff09c4d7954f633835e6ec6b75<br>SHA256: be6e773afb84c7bfd6e776e60b5fd25f2e94fec46645425d372903785e5e42d1</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>191.5MiB (200.8MB) – 1,858,245 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 199872864b980e46734c4b3d32fe8308<br>SHA1: 60f98944d45dd32c55e941a8027d3b859500f120<br>SHA256: 06940e9a8b2ab52786de58031e61db8a24d67fa880513452be335194c8ac9257</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>172.8MiB (181.2MB) – 1,858,245 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 858e7825a80096795ab47f189ff618cc<br>SHA1: 694ad8158b505d097f8b0d5f8c7935b9a1eada22<br>SHA256: 1ba6b99f23678931453991da6fa7e5d71d3cd2f0cd12e9480e57abc8abdd8fd2</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>192.5MiB (201.8MB) – 1,858,245 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f55da34cde0b05b62d9f4c63953b08f<br>SHA1: 06ec2c39f55a00e29bcb935af6a5b19b878c3050<br>SHA256: afb6a529131dd7c04691ca9ba545e2240800e4aa8876a154a3ff2ad7bad69c2b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>176.7MiB (185.3MB) – 1,858,245 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24d2fe91f13a7265ec360408361d3e50<br>SHA1: cf67896e10a9c609e2702ae0969b37b2e1fdf8ad<br>SHA256: 720f5c2d44736ebd62ddcf8c0534d2ded776dea51aeabf440425be137668abe6</pre></details></small> |


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
