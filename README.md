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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-08-14<br>IPv6: 2024-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.766MiB (4.998MB) – 238,607 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1525dc2054957e4e3f05d419c9b74a4<br>SHA1: 19cf8b8a650caa8661eaad173e9b2431934c7f4e<br>SHA256: 26641f04392f42f2d7eb1e9b2b2fdc829be9279f984ed541cd42495275d10bd5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>5.788MiB (6.069MB) – 87,962 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fb12db7991dd1b501070e3337524647e<br>SHA1: abdaea1af22afccf9fb981ec1e5c520cf8ed8a5c<br>SHA256: 8422793a6c17465e726c50cd2abb7d027d7f27e79608f9406def74ffc8c26ad2</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-08-14<br>IPv6: 2024-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.131MiB (8.526MB) – 407,192 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4319ac6b643461a57d089fde8d3d361d<br>SHA1: 8135246d91babc8059122e00d08ec4dc8a050762<br>SHA256: 14d259aaca365cd8646a5cc82adde24593b927be42e14f7d27a3baf65d76157a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.640MiB (6.963MB) – 101,026 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: efd0ef65e8d5eab381f5a522eeb38d7c<br>SHA1: 454ed5846d7e00dbfbcd0bab9e327a0b7e3a24f1<br>SHA256: cdda305b60b2bcb81b0c35553dc22b0a9cf2ee00282ff250d11c8558b31358f5</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-08-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.96MiB (17.79MB) – 848,576 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7545163e37091464fbb782119465015c<br>SHA1: e5a8acfa08c25a1b199f7357dc6cd81a6179848f<br>SHA256: 44cc28e51e8f8f0dba131161c20cf3f63635300b59d07a62114ef6f9579bd14b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>77.80MiB (81.58MB) – 1,182,342 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 746c02b3175efb1fe17f9b30166f1090<br>SHA1: a93ac27d5173239e642a93f995dacc8833c243ba<br>SHA256: 780412a2417d3c1b57dbdcb2e156a0aa6a0e6aa080392066a29db6340fdde4d4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.930MiB (7.266MB) – 348,283 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d0fbc41bc5bb2b90a8e0d5e5ce544a9e<br>SHA1: 1e8f1c989a09bda0597a4fd20bb1baf0e1ac7146<br>SHA256: 5ca608bc0834afa2ddcddbc57debfbc70f177637b74991fa1f5eac6b4004250c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>17.13MiB (17.96MB) – 260,326 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7d830eaf780889ad98001bab48d5aa45<br>SHA1: b197b3368dda5c090062b0f952b463dcc36089a0<br>SHA256: c9b5f78bc10fd064cbc6e77285c497db8377b1d955acc23e6e6498b158cf6e7a</pre></details></small> |
| | | Full Location | Monthly<br>2024-08-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>186.4MiB (195.5MB) – 3,254,855 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a701f04a73cc8f80f1d62d7d31565c1<br>SHA1: c08290366ff76b789e82bc1d59e49f3a8b096083<br>SHA256: 05ad2982bf2f1253f055b5d985d376d16bb31cace83cb242d464f0595b931ab4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>351.7MiB (368.8MB) – 3,417,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8e978ebf3bde1f974ba0a4b6532bcd5<br>SHA1: ce0a2c31a0c136ca457da29799b4d9d902203525<br>SHA256: 04b7870a00431ac40aa31592ac986f30dc8fcd0035a95ab9beee69df67b812b1</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-08-14<br>IPv6: 2024-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.752MiB (4.983MB) – 237,847 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41a19f3b324b30f1b8e58614ced6c3eb<br>SHA1: 0ae869a9dcd1e992112ca1f19381c40b51f06f2b<br>SHA256: 16ded9b540a430569f72a4e9231fd255fdabd1dda07b4b19d35f69b1de8705a5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.46MiB (19.36MB) – 280,554 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48429e636d89243b95e58e224ddcab83<br>SHA1: 62476d74b99370f1cf7032a405e741d78678dfbd<br>SHA256: 0cf7afea40b0dab546ce14724386b222921daeee0d831eecb913854ed7bdc0f0</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-08-14<br>IPv6: 2024-08-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>172.1MiB (180.4MB) – 2,980,631 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1b3e4b34496e91b79950bfd2ba90c64e<br>SHA1: 65cd184136a3ebc843b8b661eb3d7e435d8e169b<br>SHA256: 8fe209a185d5393cb91b8ddc3d044e30a9bbb3dfd9681ecce9b281cc7e030387</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>205.2MiB (215.2MB) – 1,986,964 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbf91d149bffc17e272f874de287e1a0<br>SHA1: d7fda16f424fa431e16b71116da2588052e905e8<br>SHA256: 28d426aa8fadf9fdb6308784807383ed47871f07d6c9d66d67e14bc55327d0c1</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-08-13<br>IPv6: 2024-08-13 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.886MiB (10.37MB) – 495,230 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 65d70023d7b2dcecbdb0121eb424861e<br>SHA1: f32b27ee85193494d44e26bd4c2e64aa41c04786<br>SHA256: 8963d7adfcc89807182ee979bc443dba7826c3929686ebddf608bb7dbf42ad36</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>29.95MiB (31.40MB) – 455,148 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0c6e322b21335f1c18d07858e289509c<br>SHA1: 0222e63db64fd2e8a15bbad66f788a7e48d4c6fc<br>SHA256: 48a2f8da520e656d3f95b5555f7a6c1c3d0a10fa75ff3aae1ef420d0d0a7a574</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-08-13<br>IPv6: 2024-08-13 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>121.7MiB (127.7MB) – 2,434,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 785918e73efb95ed7b41dc592fcae8ee<br>SHA1: a5986971eb74ff76d98843810559f5178d350293<br>SHA256: 7f36ac625c5afc1988fbe394c2abb980035d1d344611f1a7d8c6a35f4752f53d</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>130.6MiB (136.9MB) – 2,434,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9f1789c92874ad46b03a64271a94a06a<br>SHA1: 00b501ee6c1ec771b3284370da80ca29826258c1<br>SHA256: 0ceb408e7caa696d253d7d90b2d4ce69b9b6026aad5960e9abd0315652f166cb</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>121.2MiB (127.1MB) – 2,434,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f0a4ef40e45665b98addda6566d42707<br>SHA1: 6c0d63603948e43c85114322c68ca94a1dcc35e4<br>SHA256: 58718347ffe7724d5a227b1338fc3331326af52ad66745c8e0c4fc509400d542</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>123.7MiB (129.7MB) – 2,434,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f9826f78a9b64397a8262c07fcbaacb<br>SHA1: 0eb4e833d5449c41dd9494180ce11cfffcc7766d<br>SHA256: d474f147e103f1dc9d68bdd60182355929c8cb8ce9decf1265d8637508c2cd48</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>151.4MiB (158.8MB) – 2,434,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d09376bbaf616082ac1730ce32e71e0e<br>SHA1: 3b7f8b89955d26975ae6cf48de18bae7404e65b0<br>SHA256: 5c2201db2efad46e741db97dc3cdfc43c5b76411a0b55c95e16ef5e2f2fbc690</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>120.5MiB (126.4MB) – 2,434,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f7707690ecab40d4fdd8cc963e18b13<br>SHA1: 409154ac82738aff694a5ab2479ff92c1dd3a531<br>SHA256: 763cd5ff7c99cabf76aeb445915546069461821fc00cecd7548486c8318b26ed</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>148.1MiB (155.2MB) – 2,434,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4a24467a33252a55e5934dbd4cf29315<br>SHA1: 6decbe656ab97130c63fc98586c3283d645b45f9<br>SHA256: 6a18550afa5128665772149c991f89724bf115d56c57656424eb454bff07d925</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>124.1MiB (130.2MB) – 2,434,586 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ef6939d2da37b45bd891edf717ab073<br>SHA1: a33e91e00afa0fdaaa397b108f8955c2a14c88fd<br>SHA256: 9b1a8c2cbe1109fc69feafc80a6d1f24f2bde629c37f23f92247111a426a3308</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>152.8MiB (160.3MB) – 1,637,269 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1051d39feb3f5b3be7cb1b05cd907bde<br>SHA1: 6f28985a0079642e348233393ef39ff79cefdeca<br>SHA256: 7d6ed9062c2fe2075db42f1c20b2f2cac98e6d948fa2e729a140b9d11e1fcd7d</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>157.1MiB (164.8MB) – 1,637,269 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5391c329ee7643de4370ff8245a12479<br>SHA1: 874ec0b80f2a0a445f5f272567a9763c37694c0e<br>SHA256: 92f4714b866880e4e5c92c25d4ab858eccb67b97cd0bc939c90a5370d03fb01c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>151.3MiB (158.6MB) – 1,637,269 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64f71fff28288bc3a8264464098c47e0<br>SHA1: 670d98164e8a4b92874cc5564f81e811c94d4c3b<br>SHA256: 5f83d705bc254759aa7dcd609d0246037ee75c0a5b28d9f432f85bbf2e582c61</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>151.5MiB (158.9MB) – 1,637,269 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c91c5cc6eb0cd12988ab3d91731bdcb5<br>SHA1: 7ad05d1623799518a948e2053046bf73f95bc908<br>SHA256: 2bdd5abac6004c07694a2d2c4bc043536be0d5288cf0dd65eea76b1efc7eeb37</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>166.0MiB (174.0MB) – 1,637,269 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bfb5993849f38402c6f7f7c1de547c59<br>SHA1: 38e8c4a6d593a541f407b452e296be3e625b2d26<br>SHA256: 3c0dae054038bab3ea9591d1da61c5fd90a9d130b66403f16bfdca99c8f92e5e</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>151.1MiB (158.4MB) – 1,637,269 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8f146ec4f7b72554432d7cb89c7d9f86<br>SHA1: 201f0e9925de32ae2948ddd219cd50c07ad9f6f9<br>SHA256: 4bcc5787da401889bafad2852b6f33c4ab7ae0bc7692dee733f925f09d1bb41d</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>168.9MiB (177.1MB) – 1,637,269 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f5024a436810506073f816ef5ea02431<br>SHA1: 1905483beda49168e88e8b172c6f0e64b1f4b3fa<br>SHA256: 387aead9d07dfca0a3629e402d2b6d24d350050ce0d2e0d990111d10587ac685</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>155.9MiB (163.4MB) – 1,637,269 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7a25beacedca58d49e6aef5c204952c3<br>SHA1: c3d9a5f4031203a9268c542241e75e065a2ad658<br>SHA256: c11cb3e29f702c11bc2b372ae92948b8e098c785bd6787a90f596d0f20f7a9cf</pre></details></small> |


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
