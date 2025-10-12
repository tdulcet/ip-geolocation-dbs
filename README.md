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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-10-12<br>IPv6: 2025-10-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.336MiB (6.643MB) – 317,240 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64ff4deb7f5becc9286dea99141a8676<br>SHA1: 58becfbe9e21356d9589e1e9a3167a2b2803ccf0<br>SHA256: de9b12ed49a267e35553c7d73e77d9a48d77d039789ddb4f9874c5252296adcb</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.94MiB (11.47MB) – 166,271 rows – 255 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 886a671b74a219cc0732c17b85ee106e<br>SHA1: d184e43599c1d1c168094f053b59659f1dbb3662<br>SHA256: 89607a3a9bd831f5f5e0744a9a07d218cc05b5e772a98fc4959e33f3e3e1655e</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-10-12<br>IPv6: 2025-10-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.695MiB (9.118MB) – 435,386 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57be1223d667245eae30cb7cb8805a58<br>SHA1: 12baf256a3f2ccbe203073289e254e620399c5ee<br>SHA256: 6456b5e42ea10929662a0a6c2afd312690ef1bb32d36a0571282f3d98b49d026</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.381MiB (7.739MB) – 112,282 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a7698ad95f3531c9d8ce07dd4c1786c9<br>SHA1: 7a6ff3bbda8340e133a8f3e76933bd01aeddc98b<br>SHA256: 3d3a155d91f72c1f24db052f1029e43f26dd323bb1271779d1651577de51885c</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-10-12 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.20MiB (12.79MB) – 610,612 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 571b8c26d154ca4ac0cdf392a9466536<br>SHA1: d5866152ab1671816b15df90492e413343c55436<br>SHA256: 1ed5e9c5b0bb3d3906ff6cbfef358adef04e8dc8b4b89c4c8fb827992cc4f63b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>70.85MiB (74.29MB) – 1,076,704 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbda1604c4eaecde40ba3a3aacbf9632<br>SHA1: 818bc776fc06607bb1cd6afa171356773e029a0d<br>SHA256: 7326662ce79677baaae9183921117e0a98f48bf25b83866ace71d05bd001e6d7</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.915MiB (7.251MB) – 346,209 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e6d674990e0f107fbd088e17b77f819<br>SHA1: e21f5ede55e9a68287555b79c322fd01792544ff<br>SHA256: ee56d76f9c227d305e7f5b79e40e5d3a11d30d9b4b4a21b0a814bc5fc6ccab58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.87MiB (17.69MB) – 256,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf6418c75d48ec2ce4a2a1c5d27690ea<br>SHA1: 9b685f6a9fe8620ee6003242f3c5acf610337b72<br>SHA256: e1a598f6d63830a2bae69310a4cc6608adaede1395648f0431135c9239a1caec</pre></details></small> |
| | | Full Location | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.3MiB (220.5MB) – 3,682,011 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42145ba207725adfe20cd9225ad15164<br>SHA1: 1d40332c6092241cca96d8e93cd7fb5c58e051bd<br>SHA256: c60c91128d39be7572205c3f816d9173c65edc218778bf32f3d1094e958cfd2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>464.6MiB (487.1MB) – 4,514,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f22f776ceeb745f6db78a0eef703371<br>SHA1: 30ac2eb9a7fa4373473059683b5de9079a24fedb<br>SHA256: de1e8fbe3abd61a6d689615765352368449ce489b189853826fcfeeff7321137</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.161MiB (5.412MB) – 258,309 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f26d4302c7fd76db0d0260380f6bd166<br>SHA1: af4522cf5b0da7a4f55fdb43eafd9203505afe55<br>SHA256: ccd12d01d176de876028be848cfde48c9259fe6937a9d2b5860504143663fae5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.39MiB (23.48MB) – 340,241 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6eda0fd5aedd731b1e43a4c8d35f5168<br>SHA1: 6cc4cc30710f6cbe42343b9494b486362bce385e<br>SHA256: 7cebccd5d4724480dfa8ce7feb46df8346a377c9663e9c706a42f95c27d002e4</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-09-30<br>IPv6: 2025-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.6MiB (178.9MB) – 2,958,155 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe165abca69867578e8e23a850e260e3<br>SHA1: 28aa8e4206a34c7c19baa2c8dad557e3e7e29980<br>SHA256: 395f8c3845977ec0aa9aeb6377d2342a1e06c37721d3b8e06ec2ffe85d3cc7e8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>294.2MiB (308.5MB) – 2,849,176 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 84c795dd4c828d0cd8fd981934d68c7e<br>SHA1: 2745be7c734086c09f40f1d7190fb4ec6cb937f0<br>SHA256: 7db0021ec3c03e994dd396ac728595c5a9f0c6bc1180ba247056935d66e38a9b</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-10-10<br>IPv6: 2025-10-10 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.84MiB (13.47MB) – 642,872 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d56133175a2887a507dfb0d45cb27fa7<br>SHA1: 90929fbfdd301fe8ca5c8dccd2e87881d997e939<br>SHA256: 42af161d2f3080dad3f1a6f83d619883de6101e0b4259996b9243266607d5c71</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.17MiB (45.27MB) – 656,101 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6ff82e51d68d2c97f535dc89cbb213a<br>SHA1: 8fdd96fbc4200053f6d54312abb66adce52ea77b<br>SHA256: fa0b6cdeb9b598217c442601fe29416b2041d606907463006980ff6556d9ec42</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-10-10<br>IPv6: 2025-10-10 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>176.8MiB (185.4MB) – 3,484,637 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9d249bd2faef4e540ce187c14ee17970<br>SHA1: 415d065b5cdbdf6a7c1064df747872c6119e0666<br>SHA256: f4a1c3dee8b498bca98ef2218d85ff6dca515eb04b4ae20a0b5c83c7473264d0</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>188.0MiB (197.1MB) – 3,484,637 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 545dd2b9d6a72b89b6e327d14eccf464<br>SHA1: bddcc02566b62bd2950593b7f57f411215bb5784<br>SHA256: da7b6f778d5255a5dbe957c13baebf1be83588482eb1c000cc95982bdba4e769</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>175.9MiB (184.4MB) – 3,484,637 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 60e0318f29cbdb0264b0fc2c44e008f9<br>SHA1: 7ec6a375dfc19e56250089bb0d59dc67be6b1f63<br>SHA256: 199c00834d6a176f1b994f2be1790c00c4cf24d7baf5bde52cf46b10c51768e1</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>178.7MiB (187.4MB) – 3,484,637 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 293e757d662564e98a0cf5b09819cc92<br>SHA1: 1c9b1c7328be66c9f7ed573669c1f3dcc289f857<br>SHA256: d329c7db76ede21e97f5aaeba17e33f9890136a11a966d9577353c11a8febd5a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.1MiB (235.0MB) – 3,484,637 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5468b190a4b4ce3161614d1f0925c713<br>SHA1: faa83ebb2f0f962d407fb3393b5b5fa222cf0118<br>SHA256: 11b45aaf6ecbd90ab243d73357010bf72127796ca868ed13b85541b48558f2b6</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>175.5MiB (184.0MB) – 3,484,637 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 56f0c19d25ee83651e154055738873e9<br>SHA1: 91878f1c55aaacf8194c8367ce573394b1118a67<br>SHA256: 167250892211e16259b2dc1a70234b31b6c87cdd04d7221c7c56e19d14c90211</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>217.8MiB (228.3MB) – 3,484,637 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 61788de35282dcc2a4daf8e4f4255c10<br>SHA1: f48ea27981a4fe0245ef60485bb660e9d2de2047<br>SHA256: 2d13e3f7ee082789320ce63ff16c952750daa2cb310f02b00357caa5369bb2b6</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>182.8MiB (191.7MB) – 3,484,637 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ea59503a92584bb67d4e2a0b4c76fa8<br>SHA1: 603f5943bd77ef112fc0fdf67dc156f98208c172<br>SHA256: b2e19e61c951ca7761e87e094937b6c38ce66830a9baa8583d9e3b9b3e9801a8</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>179.3MiB (188.0MB) – 1,900,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: be00b0f636d0ff6439c79dbaf3937f53<br>SHA1: 0ee20224f6619c581f95cde973b5b565fd9c7b2c<br>SHA256: 107c34a53b2c1a7461f315f2e1c1e85b4dca2391348efdb55101ccde14058ca6</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>183.3MiB (192.2MB) – 1,900,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 93116c5a5708a9eeb16e9d74d2da64a9<br>SHA1: ecfa1d358e0c3365cc7c17f033e872b6fbfe3614<br>SHA256: 831162d5f83fbb8ccf04402c81d8541e61ffbca58c6742e7ab1a638e61d2d118</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>177.3MiB (185.9MB) – 1,900,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c93e81b7b0a996a4a8606b7dd99ad981<br>SHA1: 4fe6d4f083173d25076287d7a2c3a57b62d0801d<br>SHA256: 6c8f03e35253e4a8e37772faa96653aa7c58ed0307c21638ef5b61d6999534c3</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>177.6MiB (186.3MB) – 1,900,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7ebd27af34533452f95e4d86d9c8b7f0<br>SHA1: bfa46fd34a1241c4762c1e5bf98bda706fd0a8e9<br>SHA256: fa34bfc2c709640855c0bffc788ec07649f4edc7a31fe26b2dc87fe0df13325c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>196.8MiB (206.4MB) – 1,900,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c3b298704c8bd7773b7a0e9e3eb793d1<br>SHA1: 6f79d718ff60d94099e292a230ebdbc5c8cfcf9b<br>SHA256: dc01e95de21c59ce8f45db8e53ec4e2103733320db67b428bd6a7331263f5e4c</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>177.1MiB (185.7MB) – 1,900,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af73a2fa97ba759a33111c155697b5b4<br>SHA1: a672b236fd5605ef2c569dec483d56b7d2095c31<br>SHA256: 948eff41060933632e4c3d6e7cfe90a6653179ad07ab73279e8784252483da88</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>197.5MiB (207.1MB) – 1,900,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb7000410b25551fdff09a330923ed36<br>SHA1: cf3977c17bf0f619f8d6887c5b2052a796e66c7c<br>SHA256: ea086d9d087b9730251dd44e1271dc43ec8cf81346aa4112e95977bedae4f6ad</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>181.2MiB (190.0MB) – 1,900,030 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e3562bfb2282c4c2d3dddb47ec2c0be6<br>SHA1: d6507debd12901ff80b00eef5d0d1c733a7ee702<br>SHA256: c3e50247cb87105a6ce657aad7cbabcbb18a6c126bbf3a622dd1ceecb67020fd</pre></details></small> |


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
