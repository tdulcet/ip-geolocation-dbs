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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-11-02<br>IPv6: 2024-11-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.854MiB (6.138MB) – 293,110 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 20dd8c03524af20b165613c47a8e7862<br>SHA1: 7de57375866fabd1327b8ad31963b59d6da57ce4<br>SHA256: 3cadd5ff4ef53c6e7f67882e8a8274c271160668cb19370f35cc899a2b3863d2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.046MiB (6.340MB) – 91,886 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2aaf813a2f2c4c4ab3807dc26cbc9e1<br>SHA1: 580bb5c430db18374519d495b9e318b1009fa270<br>SHA256: faa581228df8743865c55ec470b4696bff33edc6b9b6ad52624758ad9f21f7c1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-11-02<br>IPv6: 2024-11-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.231MiB (8.631MB) – 412,181 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 117e61fa3f7a86e4e3f9a2e04727e6c6<br>SHA1: d1e780cea8663617bdd6eec9a55fba3057585d2d<br>SHA256: d8d4d5423ccf635e577dea65eba48c2af09c3e01c9f2b44fc77209e172c0ce68</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.835MiB (7.167MB) – 103,989 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 298ba29ef41d9b646d07c6ae746bbe92<br>SHA1: f4734f579224dc8b52421f76fa053628835902dd<br>SHA256: 57c0b7f8cf3d1e0e6f34e39714dcd16cd6405af06d53a1f0684d7a59c175ca7f</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.82MiB (17.64MB) – 841,433 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19904353e10538514c9794cb3cc42484<br>SHA1: dcd3a9fa772f33aee99094d883ea78b4b65542f3<br>SHA256: f55ea09ba380e1aa247f7d8f4dc04557e32c7f80c3f26a0af8b58ca4672a4cc3</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>69.99MiB (73.39MB) – 1,063,639 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd39059fb29839a4abc569ca36a5499a<br>SHA1: 66b92b6f955413c6c6fdf8b5d23f9fe948a093db<br>SHA256: 8365294c760e94f05fe217d076c662b4460807248855f1c9bcee809c428c9628</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.056MiB (7.399MB) – 354,248 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d0746f47a1225271996460705211255<br>SHA1: a42a4bf19e2ebf577c82e10d3834e8df68696682<br>SHA256: 436aea2efe6e1523eea5e9ba484e5efba050d65a52ade285c3f9c0212c5ed301</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.43MiB (17.22MB) – 249,619 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efdc8aeb0b5fac8527fcc97613b42d4a<br>SHA1: 05d5c2e0b0a85115285dfae791b3139e2b9eab7f<br>SHA256: 45657f0c603e4d28c566dd5f9da450499802a059e8c1ff77082c945045a71fa7</pre></details></small> |
| | | Full Location | Monthly<br>2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>190.2MiB (199.4MB) – 3,323,413 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e766d2e8e0a2969d4ff92cf52388660e<br>SHA1: 38d95ed8fc01158d0f5ec9aa8f3bb385ef86d3d9<br>SHA256: 7656a9190b90023870afbde735c05ae68168d21190941a5da2be92e18c8b89a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>369.3MiB (387.2MB) – 3,583,553 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23856f8e31b066ac2b1f256c563a9300<br>SHA1: 4ffab13a7c3069f5a314ea0ee72c222a02103120<br>SHA256: 9d6307032c82257b206c839119decab677631aaf7e5d3138ed4b92f8cf07acc1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-11-02<br>IPv6: 2024-11-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.921MiB (5.160MB) – 246,296 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 40e580b10d9fe17a204d4682e8caec62<br>SHA1: 86c3da422b58cf1b996348924dc8256bc7f8c0df<br>SHA256: 32168c3110bd3fb45b79eed0642def8db10a273ed5096e224c2de29a05e02fca</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>19.04MiB (19.97MB) – 289,357 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f83651873d1db0d8addc8985566a84fc<br>SHA1: acbfe44dbde35a4fdbd66b655d20885747b3b874<br>SHA256: d240a5da5dd52cc7a57780fad1a11415b8e2130d68731c1182f1798b90e567f5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-11-02<br>IPv6: 2024-11-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.6MiB (182.0MB) – 3,006,530 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3205f79a16c843aace3d3a8e3aec5334<br>SHA1: 8987d05a3901bd7ec7439251708d0c2228642999<br>SHA256: 807a107f4be6c9d0eaa439b6e63f93c3067bae3d0b264ed83a142d3318442718</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>215.9MiB (226.4MB) – 2,089,755 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e072b36b8644392e07bc9ec16c01aa89<br>SHA1: 4145eaccf7a8ff6d0571c6ac031eefdf75dee798<br>SHA256: 575d88a498458f0cac331d823e497dff499178b951353e2f6594814450a3a71b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-11-01<br>IPv6: 2024-11-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.940MiB (10.42MB) – 497,914 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3fbc308cc649ed140021e3a6b73faeb5<br>SHA1: e4363bf44882f4db8be8487f365e8f5c7e7e9d10<br>SHA256: c4e2fa69d67e0add00630be6b5d327520585910dea988bedaff86f8e0c74c6dd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.98MiB (33.53MB) – 485,986 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d2140ad5357d78933818fe5b571a1db<br>SHA1: e4528c8236b6ebd71bb5de21bc867251d18de715<br>SHA256: 94765100b768e9947949829f0a116825014b3a1f78f7420bdfd8d339c2756074</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-11-01<br>IPv6: 2024-11-01 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.2MiB (180.5MB) – 3,398,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 727b7658f1b7b0ce3f02bbeb566a7c47<br>SHA1: 8489a951fc5152b7984c58392ce37decc8457d0e<br>SHA256: 19e5379b6a6f137b2a570c95817d88bde7a889eec1c3c97904a3786fc6ff5d47</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>184.0MiB (192.9MB) – 3,398,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5b79d0a3e4c01763d4b5c7365bf3c483<br>SHA1: ac18a42644f6646794e2c02d4413c07bdc76d061<br>SHA256: 6e87051a4bc8afd5786ce7e48699daf1fa985e396b9d912a3046cabca7a8ff89</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>171.1MiB (179.4MB) – 3,398,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: abdc82d7b12c8aa1b0308849cad5d888<br>SHA1: 93fec65c998c729324b8cc359a9cb53870e061b8<br>SHA256: c15eb0f7733158bb5ba22cdf1206ce5a9ff994c73d9c88ff2b75996c6502a72e</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.8MiB (182.2MB) – 3,398,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d6c453f040221cb0973a35f7c564875<br>SHA1: 152cf6dbf257856ccc3934686933fc163ef80069<br>SHA256: d8a7d57aa78f7935d804c4cf86f1cf7172321b980c623507a5c80e352bddacd2</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.4MiB (229.0MB) – 3,398,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35e94074e258e23df0d7ecf4d8f9fa2f<br>SHA1: 6c60e0a40254e6a153cb95e2a22398909a676280<br>SHA256: c230f7da38f7d50cf253b5884252ed43ea68d5c9025601a3703bd5eaa0403e90</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>171.0MiB (179.3MB) – 3,398,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c9a149e26c128d76f211526952389d2<br>SHA1: 56700229856451c7efba96576d1136b55ed5a220<br>SHA256: bf5ea334a4ae8a61951e7baf81096e17ae4b2e1af0bc9a9a14927639464eabf4</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>212.1MiB (222.5MB) – 3,398,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57e2d355dc0b84af4ec73a84a8b51050<br>SHA1: 6a97078fca571c7bbcd90e7580895d0e5a518b94<br>SHA256: 87d83d624b71632fce2a9376e456f245d1a9e5d8a09183077cf51c7e9b9364ee</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.3MiB (187.0MB) – 3,398,854 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e07c131cfce98d5b00baf95e06b4400<br>SHA1: 38165ba460be6b73a449774e37b9cd32a5f387ae<br>SHA256: 79407f57aaa572c79fa711ac42c6f46a7ddd8256d415ed730c72ec9eb171b31b</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>154.0MiB (161.5MB) – 1,614,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 038c5bdfc34de706ea4c715ad5cd480e<br>SHA1: da20e462ee6dd4a8ea8c9c3db3aaf4a180536dfe<br>SHA256: f5b7909f317134c1cca75e92c09d2d191e01b4cfd211442059731278051916d7</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>156.2MiB (163.8MB) – 1,614,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc29e23e1c2599acaac45ebf6c2f2a95<br>SHA1: b4bf2cc7618ac6d581d6667d6f05d4754f0e9bc0<br>SHA256: fec39a2d367e087725f49defa1916f7cd3474d5430b2cca3e9ae682a3a929bf4</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>150.6MiB (157.9MB) – 1,614,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d34d98b11ad391f4a3c77caa9226d2d1<br>SHA1: 487c227de83ccdf3def97825de82e102e5d0e65a<br>SHA256: 0d368a8fce4cd6e5b3cd1ae2864b142da81b158fcdd99bc9615e160929151dce</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>150.9MiB (158.2MB) – 1,614,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5085a3885e028e4f375becb69f7d2351<br>SHA1: 4229bc1fecb3efd6260926ea25980d99042c135d<br>SHA256: e269def5666d72752ab2438aa297ca8610bc7b3c93c45d8132afc4f8d8685593</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>167.4MiB (175.5MB) – 1,614,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06ffbdcef5fe0cbfabc22b63b8c986ec<br>SHA1: 366f344b070a7157cab7d47a80684ced5152cf48<br>SHA256: 1fd261ea55173ccf8547cf59979448bc3376b2b1b66a7d7afce19c174603d9b4</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>150.7MiB (158.0MB) – 1,614,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 977542fb649e5391bd9841f1e38b9dad<br>SHA1: f19fc74cdc182920512da6d503b38152bd18373d<br>SHA256: 0da17f277979a757d84709edbd6d10944e0442cd817b59e2ac907771a2f81e3f</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>169.1MiB (177.3MB) – 1,614,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57cc19d58bac30c671fb393045bc85be<br>SHA1: 07049ad5965d8be8bdc8e3f52b6f991cc2dda572<br>SHA256: ee4f53addfbf893757c1c63423c5cfb0c9bbb2ab06a0bbffd112d1e1ec6efc1c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>154.8MiB (162.3MB) – 1,614,903 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a29cd3979b2e3d94aadf4a745136520<br>SHA1: eb5c939401a46a918492da9d67230a9815f18da0<br>SHA256: 20da494e74c599c6a922e512403d5d18fcc640b513d432274e185a6a8e7b40c5</pre></details></small> |


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
