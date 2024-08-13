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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-08-13<br>IPv6: 2024-08-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.764MiB (4.996MB) – 238,501 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0e8f9f80e3f6bcaee5df9716a4e4eeba<br>SHA1: 1cbf162fec51b1aafe7f0a80c1151c3e92858b0e<br>SHA256: 19e5e1f97d7e65563d19692507eee6c81137f1b3542450dccdf3fdd76844399a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.782MiB (6.063MB) – 87,871 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 83516b3bea21bb84d0c47aece9db3611<br>SHA1: 70cd1c2ba5ea85d7503c5445853f49590c02f566<br>SHA256: b24eed6fc866028ba2bf1860574b7e5719a2b31ab30837daabb6609203635b48</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-08-13<br>IPv6: 2024-08-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.124MiB (8.518MB) – 406,824 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 43425757e7606269d516d23b7e29ffda<br>SHA1: 64a10056d87b95113208ab68391494c8e3de737f<br>SHA256: f72dccf8f9cd31b1c4bcb5b707090090f52e5ef97cd123b124b347f305b8d400</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.633MiB (6.955MB) – 100,909 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36674a77453b624c9b5860031a5aa154<br>SHA1: 0ba23857f5451f94e8aa3feefef66a565d62288f<br>SHA256: 6ae501b21d8b661917b088fe62052d887e48b9ef088399b9b814caee88d982c0</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-08-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.96MiB (17.79MB) – 848,576 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7545163e37091464fbb782119465015c<br>SHA1: e5a8acfa08c25a1b199f7357dc6cd81a6179848f<br>SHA256: 44cc28e51e8f8f0dba131161c20cf3f63635300b59d07a62114ef6f9579bd14b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>77.80MiB (81.58MB) – 1,182,342 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 746c02b3175efb1fe17f9b30166f1090<br>SHA1: a93ac27d5173239e642a93f995dacc8833c243ba<br>SHA256: 780412a2417d3c1b57dbdcb2e156a0aa6a0e6aa080392066a29db6340fdde4d4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.930MiB (7.266MB) – 348,283 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0fbc41bc5bb2b90a8e0d5e5ce544a9e<br>SHA1: 1e8f1c989a09bda0597a4fd20bb1baf0e1ac7146<br>SHA256: 5ca608bc0834afa2ddcddbc57debfbc70f177637b74991fa1f5eac6b4004250c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.13MiB (17.96MB) – 260,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d830eaf780889ad98001bab48d5aa45<br>SHA1: b197b3368dda5c090062b0f952b463dcc36089a0<br>SHA256: c9b5f78bc10fd064cbc6e77285c497db8377b1d955acc23e6e6498b158cf6e7a</pre></details></small> |
| | | Full Location | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.4MiB (195.5MB) – 3,254,855 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a701f04a73cc8f80f1d62d7d31565c1<br>SHA1: c08290366ff76b789e82bc1d59e49f3a8b096083<br>SHA256: 05ad2982bf2f1253f055b5d985d376d16bb31cace83cb242d464f0595b931ab4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>351.7MiB (368.8MB) – 3,417,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e978ebf3bde1f974ba0a4b6532bcd5<br>SHA1: ce0a2c31a0c136ca457da29799b4d9d902203525<br>SHA256: 04b7870a00431ac40aa31592ac986f30dc8fcd0035a95ab9beee69df67b812b1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-08-13<br>IPv6: 2024-08-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.983MB) – 237,847 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a19f3b324b30f1b8e58614ced6c3eb<br>SHA1: 0ae869a9dcd1e992112ca1f19381c40b51f06f2b<br>SHA256: 16ded9b540a430569f72a4e9231fd255fdabd1dda07b4b19d35f69b1de8705a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.46MiB (19.36MB) – 280,554 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48429e636d89243b95e58e224ddcab83<br>SHA1: 62476d74b99370f1cf7032a405e741d78678dfbd<br>SHA256: 0cf7afea40b0dab546ce14724386b222921daeee0d831eecb913854ed7bdc0f0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-08-13<br>IPv6: 2024-08-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.1MiB (180.4MB) – 2,980,631 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b3e4b34496e91b79950bfd2ba90c64e<br>SHA1: 65cd184136a3ebc843b8b661eb3d7e435d8e169b<br>SHA256: 8fe209a185d5393cb91b8ddc3d044e30a9bbb3dfd9681ecce9b281cc7e030387</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,986,964 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf91d149bffc17e272f874de287e1a0<br>SHA1: d7fda16f424fa431e16b71116da2588052e905e8<br>SHA256: 28d426aa8fadf9fdb6308784807383ed47871f07d6c9d66d67e14bc55327d0c1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-08-09<br>IPv6: 2024-08-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.881MiB (10.36MB) – 494,969 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f293a36852e82d64a4d52150a6be2c98<br>SHA1: e8f84003e06119c01b430fbe8e03f7d37b1b65d7<br>SHA256: 4e53aac3344d8efed7f53083a6673a2ba4648351b15cb80ae4e8e368b9edb80e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>25.66MiB (26.90MB) – 389,885 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5d014248d17cbb4a44409e6675fdca83<br>SHA1: c9bbaa288e212f15e7646867ea12e3b10ae743fb<br>SHA256: 0980cad41fe0f1555cfacffa4136e5ca3b53d5e3e177b2b6145eb94dc9d5c325</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-08-09<br>IPv6: 2024-08-09 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.8MiB (126.7MB) – 2,419,578 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aea890bfc79cb12cf79acaf9722e5b92<br>SHA1: 5f2208d768f1c05198cd5dd02eb9eb00b4b87261<br>SHA256: f2301f2379b69c31cbb112f3f5e094c670f3e1778e4451c7052a295783483ebd</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.8MiB (136.1MB) – 2,419,578 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a58659787e1beaeadb44053ab4f6ae93<br>SHA1: d17ea98ac08960f9d72ed78ea4d46576c04636c8<br>SHA256: a725b4b93584238f308a075df68604863704184f19a86a4d576e13aa96fed1dc</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.6MiB (126.4MB) – 2,419,578 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56acc649c5d01cbc912c0a50752ff1fd<br>SHA1: 217380dff819bd26f846587f821f15dab420ab23<br>SHA256: 15fe8277f4bdc667884017b628271739479604d56d47b74b9adb62350664f105</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>123.0MiB (129.0MB) – 2,419,578 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c210f3921707d30259a01e96b1bdf86<br>SHA1: 1c14f42a9ab8bdcb15f49faf3eccb8d9c48ca1df<br>SHA256: db7480643cfaeb20e5fb27a553c529993a9b635921e6aac8b1bec9cab603ac23</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.6MiB (157.9MB) – 2,419,578 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4675e42ec894ca42e43cdbdd37ee2c1<br>SHA1: 7d5483be3a9a2549d17456e6828cdcd91b248b8c<br>SHA256: 567096301c1bb2215e5229090f02a515738b3bb996c70f7191ba68b808a2edb4</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.8MiB (125.6MB) – 2,419,578 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e5e679efaef7b511904fc68a7473674b<br>SHA1: e7144f0f43be2ece390c0eb52693714d188c274c<br>SHA256: b792d751c5f7f905c8cbc918ac63b91c7b30584516e1961b7a2748e3c11b7630</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.9MiB (154.0MB) – 2,419,578 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30874fbb6fe29a39e73d6526cec13bf3<br>SHA1: c88e65fa70bbad1ec14cc82747b1d4d76b6bf8d9<br>SHA256: 7a091afd48ed5f0cc6655c7d57a8968d5b039ce124e2c62cd08b64fd6526ad68</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.2MiB (129.2MB) – 2,419,578 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc641e39a7dad56ff1690f61ceafb0d1<br>SHA1: ba2e6b14becc6b90cc6f78f37eae76d7c73c7c4d<br>SHA256: 3cd5d1a94cf4f3ae064aba1149dbe236c852af72949e2e2a6f868e2df87ae6d9</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>125.7MiB (131.9MB) – 1,361,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0df12854a6dc20440586c8f7a57b721e<br>SHA1: 98796a585442ddab148f988942e8fdb80e5241b3<br>SHA256: 9a91f52615f7f702fde156d4c9184188b39c1618646cdf520d1e71b1169d2e0f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>129.9MiB (136.2MB) – 1,361,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53446a30454963abbe78ff79e0d8a3f3<br>SHA1: efed031ab43e2b8e8d8b72fda299febfd4dceb44<br>SHA256: f809aaa08e760c52c501204f48e8e571a292009361becd057b6575354377f4c1</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>126.1MiB (132.2MB) – 1,361,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ed456e2591f1f7228d3aa0d7d0bc353<br>SHA1: 43ef81ff92ef2dfb8c490a69645b1d0b629cb01b<br>SHA256: 1fa20431d7edc1e0bdddeede32fd6c4103c4cd3cca38e05c3a263c4dfd7863ee</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>126.6MiB (132.7MB) – 1,361,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7903614ce8eed6ec88ad69452d619331<br>SHA1: 8ed60c3749dde0602860d2b351e3def5d39b8abd<br>SHA256: a6305b9c4bd606957b252f3c5fa89a8d18812da0b88f877f4a074c69ad75438e</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>138.2MiB (144.9MB) – 1,361,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 04523646f148588b51500ce2891463b3<br>SHA1: 0687f33b1de3f5c1eec91ed2ae8650f37f3d9f2f<br>SHA256: 3475feb0cf675ea18eef76c406f6579883273ef2618e874624445fbaeee3cfe5</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>125.7MiB (131.8MB) – 1,361,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4e8e39c20ed2bc4d30d99d41a806f40<br>SHA1: 6559b3c9332ea8611f5dbe589718b83dbdcf3ac3<br>SHA256: c97f38f52b0a8d10e6870b12d27de70dd1ba550184bd40a1c365c51669f69ce7</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>137.2MiB (143.9MB) – 1,361,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c789ecaac113a8ea631a54a4e1100ae5<br>SHA1: 2a4ff46a413e95b8d8a5399b4405a2b97baa94a2<br>SHA256: 1e1bcdd9d5619531fadb12d16e263270c6b11609d6d893c5ea8cec2aa5dbda35</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>127.7MiB (133.9MB) – 1,361,745 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50d4319205090b1138d62fdab8e0dc1f<br>SHA1: b159e313b95faab927b9dba63863c06da6b64f26<br>SHA256: e1f2b9f6ae2dcfdf282f703a92608da15975463c67eb3007ad9d1d4ad39229b6</pre></details></small> |


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
