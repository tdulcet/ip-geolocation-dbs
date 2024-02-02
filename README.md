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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-02-02<br>IPv6: 2024-02-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.796MiB (5.028MB) – 240,075 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5efa01ddea8fca1dc6ef002157e09623<br>SHA1: 950aa581950c5cf29ddee37f0ef64e554a60a7a8<br>SHA256: e6e9497bd765c72a17e5b11569b5fc1f757ea26060317272df60a42ed4f58dff</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.599MiB (5.871MB) – 85,081 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0ee359cf43bddfa7be546ae0be1d006b<br>SHA1: 407698d258b76172575557b70d2232b5e6a56619<br>SHA256: 03b3a8bb739a252c1039f051abc09f0e1971a259e8a58645f6dfffb36f8965c4</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-02-02<br>IPv6: 2024-02-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.252MiB (8.653MB) – 413,226 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b0e2bcc5d49da0e68ff48f2294e6112<br>SHA1: 2c7e8efaa11059ed93e167f02c2c771c1ebe7b9d<br>SHA256: f796810de5e043a64a37aee18edebbf1b247398859d0f4aedbea0c4797e8a6dc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.935MiB (7.272MB) – 105,503 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 512ba5e49da68a457eadb06b88661b9d<br>SHA1: 3a9a1860626f635d9733c0fa61cb9e8d6b15380f<br>SHA256: 87641c620e765d3310737b15b645b15b583748d392f4df4ad538b3153d388f84</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-02-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.09MiB (17.92MB) – 855,570 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c5a21d2ea179f2c93fa2d9e655b327c8<br>SHA1: 289cb84cccd5f2fa444d525f84da73ea4a9cfb36<br>SHA256: ed0406ceb8606fe68386438cbad5872f84af8819a1484e8771cf10dd114b071e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>52.40MiB (54.95MB) – 796,332 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 163b1eb8ef80b03da19172d93fcfa097<br>SHA1: 04a52720e6ec930e0b883445b85a03f94476771b<br>SHA256: c22cbfe7da7eaf719829cdd015e971fd23fd97e1edf9122a5cf6d387b3b18326</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.429MiB (6.741MB) – 322,238 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b58dc67267f460ea3cf5cad59cd04fb2<br>SHA1: d7cd4a637354f5a5c457e96633e1f5c9cc5c059c<br>SHA256: 55313849f9b0eeefb503ca58aa485ebe95d325c7771a4b2e5e9def19ee8aa2f6</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.67MiB (19.57MB) – 283,667 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7b73dc10990e7bef8c444f1cde6991f<br>SHA1: 07ae49b41bae3e257ad578c4bf31ee8040ccf1fa<br>SHA256: 7ea6211e834aaf328302ede30e6777fc4f71afb40ab1238cf0af2be151b5b248</pre></details></small> |
| | | Full Location | Monthly<br>2024-02-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>179.7MiB (188.5MB) – 3,143,531 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4796f68669fd62ff1776c3d247e13dff<br>SHA1: 8d63c70c0bd62e8829cfbd2dfba8d6b8e6c77fd0<br>SHA256: 04e5000cfd1d52386cf975f825886bb214085c10b75c2568efa51ce70fb6c3df</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>291.6MiB (305.8MB) – 2,831,720 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 657b58a340f82d12479e96ce7f695a45<br>SHA1: 1b9c4719ee91d1e9da68e6f0dd1529e893bf9777<br>SHA256: fbe98efa467387f6ceb69603459abde1562d03903aa05b063edc68d9aa4e87d0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-02-02<br>IPv6: 2024-02-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.640MiB (4.865MB) – 232,256 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60fec6f73486236c8d0d94598e079d6f<br>SHA1: 7f19645a2e7ae1f5579b6769363477a0ec58e5f6<br>SHA256: 7f7145aa700bc6d9b86d8e430377fb6751efd3a786e0455999aabe3401d275c5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.20MiB (18.04MB) – 261,405 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: beffcbfb309d78e440632bc98d2414ab<br>SHA1: dd35b8eae3704db42b162d88359698a1eaa070fa<br>SHA256: e646910999630fd6ef2510fb099cf8164d7433a42c1c9eb89f25eda20a88083e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-02-02<br>IPv6: 2024-02-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>168.9MiB (177.1MB) – 2,925,251 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 434c9a2a5a5c869e663a7e206ad5962c<br>SHA1: f2e0c48f3ecc7d10f4697a8c5c698e1979b08714<br>SHA256: 8d5321147896799a07280f735aae4be97a74bdd31110778527dc8f4b77485f61</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>166.3MiB (174.4MB) – 1,611,498 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f5657561eababf9a2a95782c6828fe7<br>SHA1: 2ad191a63a7542567f5b0cb618832a78ac2b69af<br>SHA256: 0da501537b4c33714df4de1f0432d13330a9317c16e783a1cdd1ccdee93a4052</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-01-30<br>IPv6: 2024-01-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.400MiB (9.857MB) – 470,898 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d41f525e80e69b75b57f35005e341cd1<br>SHA1: b75e8b1f94545bebfe8e5be4849c4cf170440b55<br>SHA256: 4c7c8196f3945f17c156d1c7af4413bb0a7535cbed92cf05195aae56faae387d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.52MiB (19.42MB) – 281,470 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 80ff9108c13ee3b4ad961b144c68cebb<br>SHA1: e1e4ba0a82cb7e23c6af0a413111c842e7acc6fc<br>SHA256: 1486868334098feb8f4197ffa22fda3111bea5d879e6b0eff6732dc80a031da8</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-01-30<br>IPv6: 2024-01-30 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>159.0MiB (166.8MB) – 3,378,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8c85a4f5d47637e9d4a4da24e511d950<br>SHA1: d15d9a961f9247ca34252f4e0b0dde099d3b2507<br>SHA256: 4fcd4b9834e6ee241c545d78790d84485b155463da26345b8c1da321f3a70182</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.2MiB (194.2MB) – 3,378,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27877375c57316fdb1e44595cba84405<br>SHA1: f957426967d175db1dacbaeb27b28294bd2721ba<br>SHA256: 5040708e1b420f1fe659e0df258c968bb5ebf79d77f727e495c05240a31f402d</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>163.2MiB (171.1MB) – 3,378,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 650bb5a044eda1a7ff2c96c977423063<br>SHA1: 185c093f466338ed18a338f3f4f67e90cdd42882<br>SHA256: 55eab1cd00b2995b47360dcc0fce12f72401f35cec1e8919a672a5ffc8aa94be</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>169.5MiB (177.8MB) – 3,378,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b275588ca34a9920cc077e4a9c495cad<br>SHA1: a6c08abe7a37cae1ea5022fc6a9497bb4f281dd2<br>SHA256: a84a72c246279e5c5b3710c3c77bf3de29226a5841995cb5af2ae650804188ab</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>198.1MiB (207.7MB) – 3,378,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cdd49aa877baacde358f57544d11a560<br>SHA1: f4e0c2425a4024044ba0136767997c654a7179ca<br>SHA256: 74d8a99e165908ce25c667fdd98b15c96d198939d73b6c5441392659bf587743</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>157.8MiB (165.5MB) – 3,378,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bbf64dacadbcc0ddda05f640e817eaa8<br>SHA1: 810660f5fa98d837b56d55c1aa4c15ef592f3f36<br>SHA256: 6721bfeba4d7fcc611722767c59f3d27dcc1dbf6f719bacc90da5df9e94f1079</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>197.5MiB (207.1MB) – 3,378,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 919518aa6738d60d399c82b3da7b0d38<br>SHA1: 57cfad54a6aea36701e9d5b5d9a124e62d5997ab<br>SHA256: 877f6557f078f80ae244d8a5b2e37d3884cfc3986422204739279061430f18c3</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>166.8MiB (175.0MB) – 3,378,831 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ef4f8fad174d43cb0cc4309998545b48<br>SHA1: 3fff56485d170049ff719c8496875edd4eafe4d5<br>SHA256: cc4374b8ff86b9fbd94f985ad295ef1e88e0a88c9ba502ef43b0e473b8199a2a</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>100.7MiB (105.6MB) – 1,126,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36450124c30fac59469372222dabb366<br>SHA1: c0c8e8f4b8de08a9f6820fa10a3d8c0f82a56989<br>SHA256: 2df12beecd7efe2dcc5b9f9310378364aa4e9da209e83328b328add9dd1269b1</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>108.2MiB (113.4MB) – 1,126,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8bd479ffef47b1a0f3e3ad4d15a00241<br>SHA1: 4be9466f514846b921fcad9bc86100fcb5c49e75<br>SHA256: ead3ce5283c52983c9abbf40c9e154b1a8a4e931201674dd6c962c9cb2f87e76</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>102.9MiB (107.9MB) – 1,126,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ce18ff3f17fab6c8e6d11c0e81ac4eed<br>SHA1: d433fb39afa8ba1ec8f75de749ac5959c5638c62<br>SHA256: 94a2c944facd74be549c01ed408d25bf63021acf22eb519a027e851c325b7c6c</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>103.7MiB (108.8MB) – 1,126,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb3a8ff3c6fab69b2518c2e9c1a51f73<br>SHA1: 31696fe50581a0783d350783e5e753d4a0b35ad6<br>SHA256: c0eb08181a64517b1f5f49a1346cf4c525a7412e64db678878bca076a5d07fab</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>111.5MiB (116.9MB) – 1,126,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44b5a8866870d45d0738b515a5245a97<br>SHA1: 5922f95d95c168cb035845a802ddd99f7f07bbb7<br>SHA256: ee152c0c3373bc2109aee702aba342ac795e33b1adcecf6b1c320026dec6980b</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>101.8MiB (106.8MB) – 1,126,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba6862746f6ebec4caae69f08470ff64<br>SHA1: 70e05d5a3781524eaf007d85ba1f1a1ee154bd94<br>SHA256: 0bf687e771c7ceaff1dfdb36023a314708ec0d339069f0a19a6500dca0bf0435</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>111.8MiB (117.2MB) – 1,126,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65e84661b9ecaeeb2d8418e5d39d9fbb<br>SHA1: d4847db146ed0c1006292449fe927907adacc01a<br>SHA256: 3dafe2a5c5d78145b893e365c5d2408a1356f87e4a8cf6105935e1eb7d899299</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>104.7MiB (109.8MB) – 1,126,070 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b414b99fc38440ca4a89353bec188a8b<br>SHA1: 71d8dfddbf843a074cb9e583b6ada2e50e669970<br>SHA256: 7c2af6179e4ce4846675a711717b3e84d24f2c9438f7b5a189345001705a9762</pre></details></small> |


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
