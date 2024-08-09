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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-08-09<br>IPv6: 2024-08-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.766MiB (4.998MB) – 238,614 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2247497e0a69fcb2cbbc197f2f615898<br>SHA1: 07809db5e62eb927e081778052c86cd09d4c4f70<br>SHA256: 3ccf7cc0fcd5c4aefc800bb1907f993703901502224faa0ca1e901613859938d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.779MiB (6.060MB) – 87,825 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e55790258cd708d97a8fcc7d96beb39e<br>SHA1: a29a9b780715b377d82dedfe3b4559b229f0d40a<br>SHA256: fe0777fda72d0e2e3bd40ae2ae933d94f16986da77542e41b167d307957fe576</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-08-09<br>IPv6: 2024-08-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.130MiB (8.525MB) – 407,151 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa6aeaa97e8365fcb9159154fdd4ba31<br>SHA1: 769665971cfdc3a1875ab5a9bc51650d1d980aa1<br>SHA256: c8655b52553c46b99a343d784063c0d76172cbfe6b5ebd1523e0f47f96343c9c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.621MiB (6.942MB) – 100,726 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 31bf2ddb930eef0a849ebba7803809a7<br>SHA1: 88ee667c0dfe07ca1ef02b7d11146716b82d2286<br>SHA256: 89c35bbb2c03c1d6ad19e4be86f6f02bfa680647464fd05ac13887fa1174c4c9</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-08-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.01MiB (17.84MB) – 851,121 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68f3b609ffe7dbedf6cea570c0c5cc62<br>SHA1: 75e21ebd098a5b0b9458d905850a488d04ff9df1<br>SHA256: 76c2487890efbb3ede0ee274b4ca880c6b98acaec454ae7ac96dc044fbc09cd5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>85.68MiB (89.85MB) – 1,302,104 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9fb33e1871d9863c9645dc7417f3cb5<br>SHA1: 2d17bcb397401a55d51dca87a85f4ab3377e69c6<br>SHA256: 6cb13183363039455115d989b328253625049410ef6c68c6821ae2ab73497e4e</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.930MiB (7.266MB) – 348,283 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0fbc41bc5bb2b90a8e0d5e5ce544a9e<br>SHA1: 1e8f1c989a09bda0597a4fd20bb1baf0e1ac7146<br>SHA256: 5ca608bc0834afa2ddcddbc57debfbc70f177637b74991fa1f5eac6b4004250c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.13MiB (17.96MB) – 260,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d830eaf780889ad98001bab48d5aa45<br>SHA1: b197b3368dda5c090062b0f952b463dcc36089a0<br>SHA256: c9b5f78bc10fd064cbc6e77285c497db8377b1d955acc23e6e6498b158cf6e7a</pre></details></small> |
| | | Full Location | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.4MiB (195.5MB) – 3,254,855 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a701f04a73cc8f80f1d62d7d31565c1<br>SHA1: c08290366ff76b789e82bc1d59e49f3a8b096083<br>SHA256: 05ad2982bf2f1253f055b5d985d376d16bb31cace83cb242d464f0595b931ab4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>351.7MiB (368.8MB) – 3,417,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e978ebf3bde1f974ba0a4b6532bcd5<br>SHA1: ce0a2c31a0c136ca457da29799b4d9d902203525<br>SHA256: 04b7870a00431ac40aa31592ac986f30dc8fcd0035a95ab9beee69df67b812b1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-08-09<br>IPv6: 2024-08-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.983MB) – 237,847 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a19f3b324b30f1b8e58614ced6c3eb<br>SHA1: 0ae869a9dcd1e992112ca1f19381c40b51f06f2b<br>SHA256: 16ded9b540a430569f72a4e9231fd255fdabd1dda07b4b19d35f69b1de8705a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.46MiB (19.36MB) – 280,554 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48429e636d89243b95e58e224ddcab83<br>SHA1: 62476d74b99370f1cf7032a405e741d78678dfbd<br>SHA256: 0cf7afea40b0dab546ce14724386b222921daeee0d831eecb913854ed7bdc0f0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-08-09<br>IPv6: 2024-08-09 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.1MiB (180.4MB) – 2,980,631 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b3e4b34496e91b79950bfd2ba90c64e<br>SHA1: 65cd184136a3ebc843b8b661eb3d7e435d8e169b<br>SHA256: 8fe209a185d5393cb91b8ddc3d044e30a9bbb3dfd9681ecce9b281cc7e030387</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,986,964 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf91d149bffc17e272f874de287e1a0<br>SHA1: d7fda16f424fa431e16b71116da2588052e905e8<br>SHA256: 28d426aa8fadf9fdb6308784807383ed47871f07d6c9d66d67e14bc55327d0c1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-08-06<br>IPv6: 2024-08-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.880MiB (10.36MB) – 494,929 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 49b558d77c72732d8d17e54b993c0cfe<br>SHA1: 78c8696b2efea59abb99516d4471581850e18dae<br>SHA256: 36682eb79ff481a0259303dc42f2ccdffae5b2bfc39774c5a0df26a956bfa64d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>25.63MiB (26.87MB) – 389,492 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e676fc0a2c3747b15b12f8ace0d2c6b6<br>SHA1: d3d45e561827a58c0cde1dc6dda159db85924a64<br>SHA256: e337087de06d5ca3b77aa8bf821be2bf5eb7444cb56e632b553533e0de3f87b2</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-08-06<br>IPv6: 2024-08-06 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>120.7MiB (126.6MB) – 2,417,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0633a3e6f27da7d9e68584818b533c7a<br>SHA1: 3e93e0e64f3cbdeed658c753781422faf45588f2<br>SHA256: 379686845dcbd84f2ef87d8ebc2df9187375120cb3c14ad59290a8c3e1cc8783</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>129.7MiB (136.0MB) – 2,417,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 99a7ed42445a3cda611783669e19eb69<br>SHA1: 3b2083c35a8cb3ddad4ab52012e7554cdc2d37e7<br>SHA256: fa52f436d48d1ce7c779a96957773ed2fb4ab0ae9e9efc486f223e0cb3b5e2ee</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>120.5MiB (126.3MB) – 2,417,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6b821cd5c8a1e41768ab66bcd7aad7e9<br>SHA1: a4a799af187f937655ab518bfd56fa66bb1db224<br>SHA256: d23f7189f3d48ed932dd2f865888f6f535892c720993f33588d4eff3aa030708</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>122.9MiB (128.9MB) – 2,417,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b068076f93e19061af747c9728eac034<br>SHA1: bfa18ac80f8a5355408881e6b3aa421dc869a5df<br>SHA256: be60768bf79969b4e87aea976a76d58a70b6945095adf18cbd177f5c08682784</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>150.5MiB (157.8MB) – 2,417,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1d0a9d91547b0f4c0fb5eb81cf9ac280<br>SHA1: 026e2dcaee3a3a6eef3ae0ea0c34bd78f4aa2fe4<br>SHA256: a3ad978d8bebb72d4c9f2103133e293ee59f1e3cc1b471de0c7134a7f3e7ef1a</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>119.7MiB (125.5MB) – 2,417,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5bd3d4ead6c215898e99ec1622ccfa1b<br>SHA1: 4f188c6a069f9293073e28d20525120283a49fd7<br>SHA256: 163c9c0421f13c4624a7c89afd767814212ffb9c496641e673514c82ea26a20c</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>146.8MiB (153.9MB) – 2,417,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95c6ae3200b093f4eb1736e901fe1707<br>SHA1: dee821d9e083f68902c1b32d20c30cb02ca0297e<br>SHA256: 6e953aa91004dae5814ee6dc4529bb00c61b8edc57bee2702af0af00d5ee378f</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>123.2MiB (129.1MB) – 2,417,808 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34d7dfc35ef1198ccba46d0f7d26f789<br>SHA1: f431f3a35e6821be9462fe9c0f22acfcb8da16e0<br>SHA256: d289daaec0a3d0ae52ee9b7e4ce0efd57afa21823fdaff325c96e6bff2a792fe</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>125.9MiB (132.1MB) – 1,363,938 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 25d94c9cc672ed408b295e9dd04ee1ba<br>SHA1: 5482dc7ba792a2ef4676474fd6ba0bca2e8fb7f2<br>SHA256: e0a7c8fa22cae033bae05ef0b78adf82d52f9eaaf91ae7a26d17c280f33e8b8e</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>130.1MiB (136.5MB) – 1,363,938 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2f53cb8ae8316c11705d4a05bf5396f1<br>SHA1: 1f5126e0a8221ca66af7806d59db154ded623ab2<br>SHA256: 43845076d760c239bf9094698108f6ab63b76e4f5a646bcb338575ef69f1227b</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>126.3MiB (132.4MB) – 1,363,938 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 36354110107685a140fd3d66dab1522c<br>SHA1: 2a2723b7c31ce36edb7d6af717f118c36c554778<br>SHA256: 6407000ff80759ee9196f66c83a0350c4ad9fb16f1f40bfc7fdb090aa31ecd69</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>126.8MiB (132.9MB) – 1,363,938 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79cfdc2ca00dffbd675c834a7abf925b<br>SHA1: 333e7d36d6ab1f6c36e2f2f0d684aa07d4943fc7<br>SHA256: 5daafdbd743f48169d8e1e44f657a2a9200ad90d75ca0db799ac86247bb0399f</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>138.4MiB (145.1MB) – 1,363,938 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 45296888220f1e6e07f6f75eabbe71fa<br>SHA1: 849bfeeba86f936624a92778dabdfa25f46d84cf<br>SHA256: 7882d43b7d417f6e8d5f3c19e9731f6d4c3556d7279f783f2f96c5c23dc94f51</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>125.9MiB (132.0MB) – 1,363,938 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02863d22fa221dbfd6f29d119b7de35f<br>SHA1: 62b9628cee38d2ea7742b51e8319569601bf9cd1<br>SHA256: 59346a450f9b3425d78fce178de94bc3f23d17d68d2f9c0fbb1d8b6026a7349e</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>137.4MiB (144.1MB) – 1,363,938 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 908b29647cb27b150c0a0b0ac96b6d7a<br>SHA1: 576f58d4bece7bcaadef126640de6e92e3866eb0<br>SHA256: 64d066e077d152e5e00775513d78e96bc71757d6f23fae9cc3af8676b3cc3f8c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>127.9MiB (134.1MB) – 1,363,938 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cacddc1361833b4475d557617b376511<br>SHA1: 3340d3ceaba2f4c370e772e103f055789451d919<br>SHA256: a9dee0f0dd83ed7bd7317273f9d83f002f707e4fc76d298d9ab69c0bc7eab269</pre></details></small> |


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
