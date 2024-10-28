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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-10-28<br>IPv6: 2024-10-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.876MiB (6.161MB) – 294,198 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0dfbd5d1ad91eb8dfcc076c8d099b68<br>SHA1: 560d2855d04e4b22fac9f14e234b43e20a5831e3<br>SHA256: ecad400593958a87cdd46ec60330793a19e1f92110cee62d39b0841717fe7dd0</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.46MiB (12.01MB) – 174,122 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63fdab7b0722ceb0c676bc4481986d38<br>SHA1: 802d406c316914a16cadf936b2f03ceb03c24278<br>SHA256: 4ca1e91802ae0ddc270bf5e3050ab3a291e386e09115fc1fdda5103c16b58c6e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-10-28<br>IPv6: 2024-10-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.223MiB (8.623MB) – 411,808 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4550403da417b59d848de6f5bf535546<br>SHA1: 1b7639b7fcf4d103e7d4aca0c95be7cf90fdaa2f<br>SHA256: c82f39601ef23ed06cde43b2bd4991746e380262087d60ddb0f486f3d52be1d8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.771MiB (7.100MB) – 103,014 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f0b1392aa02e0328f1ae1d75e925694<br>SHA1: 247c9d683ebaa0cf9d2726f58241359fd0740694<br>SHA256: 5b93927a97f0607874a9885c3b9567507d3947d6642cdb2c2fd17144dc504c46</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-10-27 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.95MiB (17.77MB) – 847,925 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b5e7868dd1feae528789e8a57322bd8<br>SHA1: 745a3f1eade1b23fd107ae99f4f505baba417191<br>SHA256: 1bf401de3cc74f3fe1b2570cb15be331716d4261dfa57ccf9718cf126465fadb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>68.09MiB (71.40MB) – 1,034,769 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00c488044957c2283d225e436ff0eda1<br>SHA1: 98d099a7346bf08796d961a1834e2aab86d3b97c<br>SHA256: 1103192a2486720f4e0a330cbbeff84159a873164946e82de6f0b0ba85f52337</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.939MiB (7.276MB) – 348,549 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1934c9e84da4a70171fa8a58df792d1<br>SHA1: a9efc628d84ddb0c5ec270a44c413d6e2e413eac<br>SHA256: 8974ef5ef8832adde54bf8eff5b734fbc419e040b6a1ba06eee6302c327937de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.54MiB (17.35MB) – 251,406 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccee8212e47dad6f6d37a7875599a267<br>SHA1: f12a6f633e3f93b21d90f94868a5dce0099a8f68<br>SHA256: fe5508fad3836313166aa43d498d12d6277cae16fef7835d5e92fdcd53bb2de4</pre></details></small> |
| | | Full Location | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.4MiB (197.5MB) – 3,289,697 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a0426270d27872fad498a291900b10d<br>SHA1: 4f4a7ccb4910df8d359d2ad76a1bd80c4be37d61<br>SHA256: 6869bc8bd2854724fd6be12e1a0efa4bf028d598fe1d116783216884c78d9f3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>362.7MiB (380.3MB) – 3,515,904 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b742d904c555f3e530341708e40522<br>SHA1: e367baa432e03a59b81c286e5f9bfaeeb0617eec<br>SHA256: f946dbe0156a23fd65f4c67f8c95dfc19e8984bc7f84d8323fc5c478da017055</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-10-28<br>IPv6: 2024-10-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-10-28<br>IPv6: 2024-10-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-10-25<br>IPv6: 2024-10-25 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.913MiB (10.39MB) – 496,563 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 446a99993468996e6398d9854b4e7aaf<br>SHA1: 4255e3ce40b0de50c25508ce11a6ef4cdc5fff9e<br>SHA256: 55ba6bae9a0fff293a626503825c63afee410615fd3773c2d68251264db1dea9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.34MiB (32.86MB) – 476,260 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f2770f75a78dd5674b14614eb5b70f6b<br>SHA1: f8b9bb4c3411743a7c7131dd17b77739bbe7ac8d<br>SHA256: e2663339ad3f3294dc7d733b5a53497f7b63688fd48fd8d5b9026b50b9f34b47</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-10-25<br>IPv6: 2024-10-25 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>121.9MiB (127.8MB) – 2,434,011 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dc2c7a3abaa3d9493c9e0ac9ee63a708<br>SHA1: 23be0c55b29e120fb54a911ec614b8b694050d83<br>SHA256: b9ddecb23588a696111d34accd9ed7ac57daa025a1c976f60437b28e6068870e</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>130.8MiB (137.2MB) – 2,434,011 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 558dc021e616fc3b9e4df2c069f6c0b4<br>SHA1: 0b9a56ddba39fcf1ff6a26b12b3a2a441362516d<br>SHA256: e1ae29b764ce16a196d8197a20c42eda3744f47dfd92d6b8393a7063db58b22d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>121.4MiB (127.3MB) – 2,434,011 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e87d9b9a48696545c6c06e9b6953208<br>SHA1: fea6f6343f5da19c991568f18021953cdb14ba26<br>SHA256: 1e53a80a1b925cde19737893a710dd3b14cffa3782f2ee76d331f4dd7ff30eca</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>123.8MiB (129.8MB) – 2,434,011 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 59aba2a400b0d86ff589a8bbbcc5eb0e<br>SHA1: 09651cf27244b620d552d0335b6f4292cd33439e<br>SHA256: 4dfe41f1f20c8488f9aaeadf7914db6464aed4e3e746b1c74dbb462afeadf679</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>151.7MiB (159.0MB) – 2,434,011 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0218646d94b2079bed3e525626ab560<br>SHA1: 6d29a3b351bbbf3dbec4f8e1ba4c1f14e921eb81<br>SHA256: bad283f4acc1969b309c4801166428bbcee1e083e0f0edab033af02321f6fd44</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>120.6MiB (126.4MB) – 2,434,011 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e5d761cd053e1f79ca6f080d04a872e<br>SHA1: edbe1b77ccdf90cc91f2c5d08a186d83f9ff5e1b<br>SHA256: 1992f57b10ec5af2e5212f3c705b6f02b1fba6bb74043242569f0dc924d820e5</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>148.2MiB (155.4MB) – 2,434,011 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a47cc6712d5b7402f10d9ca54476ccd0<br>SHA1: b3b15b6c9ffb0f7f2207319707cf9a86b8b78310<br>SHA256: 15f597075b98aac48a54f21f93f03ddbd9f961664759e93abc88cbcfc1531552</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>124.2MiB (130.2MB) – 2,434,011 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b106ad1f91d094acf7d3fde1101fa8ed<br>SHA1: 741b1a81942371db9bd87b5151efa379c7325def<br>SHA256: 02bc75a150416b00fddf59b6ac1ca5eb21b08aae5bd11324772432a55cdaa6b7</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>158.4MiB (166.1MB) – 1,667,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aca7a8e4debfe701049a0c094a326513<br>SHA1: 170dac84f07518a1f4d2be2ae859e26d8d4639f8<br>SHA256: 7745b9c52ac0522de18408573f43a10823ed620af020af3457c536ba1982d27a</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>161.1MiB (168.9MB) – 1,667,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6ca579582e6c4283006b314d62a588a8<br>SHA1: 19c3fcee8ebe970fa4f40ba069fadb6ed5829ef6<br>SHA256: bb346cca6f125d4df668c0365e4bf0fcedf6bda1853a8ab66ce710a0620317e1</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>155.0MiB (162.6MB) – 1,667,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 861545867e5fe5bb7203c2771692840c<br>SHA1: 10358cedbc9a468767d5e91d88f7d013684d2a40<br>SHA256: d79ac587ea9e512a06f82614556b566324912ee79579fefdf10fa1a5e54dd7b8</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>155.2MiB (162.8MB) – 1,667,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 814003cb57d85526fe48bd3c74200ba6<br>SHA1: 4d0d01cac7f94c2bd11ecb19017155c321a2fff4<br>SHA256: 54ea689910d0b80cab4f2205a34ca8d934c8882e1804665c645821fa036cec8c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>171.2MiB (179.5MB) – 1,667,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 74da6b4bbe857428985d797cd075423d<br>SHA1: e5d420f61d6450dfd9ad6353a6f193d99821d4ba<br>SHA256: 2712b195ba1d77a341a25dccc6f92871f454f8a76b7cbeff11359e67cec42a84</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>155.0MiB (162.5MB) – 1,667,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a30246dd6da4b1d5cb3b2cd166e5e54b<br>SHA1: 0600883ebf3052df4b6280dfe67fe596ff8dcf38<br>SHA256: 89fe39caef30c7ecd33a84f064fd1b7e809b2b5c57cf71a8291a34feff169363</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>174.4MiB (182.9MB) – 1,667,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2505f1a512c81215dc317c46796f62c<br>SHA1: 61198316f658c45666f7f165e6b125555781e14c<br>SHA256: 09030b2674f009c23ee72e37af02bc74ac906a573a42ecb352684653c5f41d46</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>159.1MiB (166.8MB) – 1,667,227 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c40f3ffb195c84a6c45d72a8b33b8db8<br>SHA1: fdc7d9c456e592ac5b962cf6c6486507b86a7911<br>SHA256: c1b5e99c700d8b2455b55cc3c2b63f8accbf331f029ffc4dc80130c80a3827fb</pre></details></small> |


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
