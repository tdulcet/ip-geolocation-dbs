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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-09-03<br>IPv6: 2025-09-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.223MiB (6.526MB) – 311,627 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19af64c34ed3a5d08ecdf9702eda5efe<br>SHA1: ef45f35844e274c69deeeabbf6ba203b1b2ba1de<br>SHA256: 3913faf18e5b1b52ef466a7d136af2459f2c021a272143fd8441f50d5b1dac20</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.80MiB (11.33MB) – 164,169 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 160d2b75765f98d490c6ec1f7a51285a<br>SHA1: 8162a7e703026ed5f6d081afca688a65b74c04b2<br>SHA256: 36c691b7e1423b416613c311d39638d07f6428f6aa79f1e45575038d22a83f3b</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-09-03<br>IPv6: 2025-09-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.618MiB (9.036MB) – 431,531 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 541574fb1e6cb26eec97af75baa4e805<br>SHA1: 3d0358825264f4aa1101437d4c01f977fc05e3b6<br>SHA256: 2089275695c81b9267f5cc83a2263a07b1d9a14376ef487700d39e347807a6f2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.179MiB (7.528MB) – 109,217 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09642e28cbcd76ec85fcf6a48100a4dd<br>SHA1: 2361a143df518008dc20dd522867aeeda500f060<br>SHA256: 00b0e1e36e82dddd921bd87338819aea10f3be4c7153d24c60c35d0443de0526</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-09-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>11.97MiB (12.55MB) – 599,257 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 79364a490d796bf7c6987b53c8a235c7<br>SHA1: 9cd3e1627f5c46129d7cec6b2e6900d18a5268aa<br>SHA256: 1be7b0c1a93993e428ff6d272fd029e11964b287808c717d42e4b9563e3cf054</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>87.78MiB (92.04MB) – 1,333,922 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbc79f00013258eaccb40950b0ffa2a3<br>SHA1: 6e83975e70e7ac3329d77a3f4aea4f11abeb3fae<br>SHA256: 26cc5559f55723bb2bf456b6869fc8a7da4eb909d9911f4d686a4011ac5b8817</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.825MiB (7.157MB) – 341,824 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dae1f431e9d10a462dae84888365884<br>SHA1: c0cc78c9aa347b8d712850c57537fc0dc50f1dfd<br>SHA256: 3f57c286e145770c2ac0d5d3c14088a919db312a222bfef2cb85941399367b2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.93MB) – 245,375 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f7e3a8bff7f09ee7cfd621ef044564b<br>SHA1: feacd88a985ae6ef5d668ffcf375eefeed7948b4<br>SHA256: f554d05a841ea0162859a713eecebb3fb0dc814ea2d39b91150dd45627c31fed</pre></details></small> |
| | | Full Location | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (217.0MB) – 3,624,799 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7154efa553f5c77576cadbc5c42ec9c<br>SHA1: b63ba0a183e94bf6cd1aa8a15db942b52d55841e<br>SHA256: 00286d8f1fc1f8f801a25f123213615fc637aa494c49fb2537047bdab4b1aaed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>448.8MiB (470.6MB) – 4,362,462 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7375867bcf97ba785ec1fa3d092fb0ae<br>SHA1: 37a209470da0930c2308178d77c0c1cac376d849<br>SHA256: df10547da1aed72a27d58d5fbd860b66dc9bfc40df34c5dcca2b7da7fdf24ca0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-08-31<br>IPv6: 2025-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.161MiB (5.411MB) – 258,293 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95e8b98e399c9546eaa6913fe2309444<br>SHA1: 0729ec1700dd66e64d570295b605e265006a8972<br>SHA256: 7d5dd78fa0ac37316f479796659a319cb718b97cbcb6c276973e7a032a890aef</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.45MiB (23.54MB) – 341,108 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ad0b9a6c005823c4054d4b7a7068006<br>SHA1: d04e0abccf0a13ec34ae27abfb08f929300b492f<br>SHA256: efdc13094674341ad2839eabd8b24cf19df12257e0c4a225196d48da8fbdf5e5</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-08-31<br>IPv6: 2025-08-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>169.3MiB (177.5MB) – 2,934,344 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a60715c570305e0c75fe4faffb43ea0e<br>SHA1: 38b00b51abf99d675c6f578f3ddc6f1291989577<br>SHA256: 7b15658d15a2ea684f5136cc6b604a1305ba55f348332e98ac74007149eed726</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>288.0MiB (302.0MB) – 2,790,254 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ada012e83fb4d38f27d1fccd53c7b18<br>SHA1: da0592788b35abae1df0d9ced713b009ce8207e4<br>SHA256: 3a2da4e80c031ab64e77dcf65f18ecdb563e48d709a708d499e3751fd70be31e</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-09-02<br>IPv6: 2025-09-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.50MiB (13.11MB) – 625,899 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cabebd66dffc705f66e304c62522702f<br>SHA1: d09b5c03c766f0242ad3b7e19ebc70e8fa27e3a5<br>SHA256: 5a979c65e01acc0e43a704dcbf9a3bda5714593508d14fe2ad90a9b13d5609fd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>42.52MiB (44.59MB) – 646,192 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 30cd517920e15fc774cca108968860cd<br>SHA1: dd34de4c41bb74d53afa77b3b8d014f55a95b6a8<br>SHA256: e79f5aaa4e84a2350a91ecbfc73e49a50faec00b402b7d1e5f45c6dc11306460</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-09-02<br>IPv6: 2025-09-02 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>174.1MiB (182.6MB) – 3,432,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95d27d53483885bc317e9e9606b6a91a<br>SHA1: 8fd5bc038271b6d70ef7919eb9bb3396ba665c2b<br>SHA256: 741923a0aca29bb3b94084ddefdfc4f5f9993448160de5fed0342198f70bd4fe</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>185.0MiB (194.0MB) – 3,432,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b072b986317652af3d6aa3cc1c17b94<br>SHA1: fb02e4dcf4218668d7ba3dc1384cdba6acef31e2<br>SHA256: f22e91157c11b2ed31d3ac69defcb23b6a6d30d4f2ac3376c697ba86ada71ba1</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>173.2MiB (181.6MB) – 3,432,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c9ca913196462e30843c3a422096b70d<br>SHA1: 6b7675a0496856fa856f7d7eba34880d701d8b18<br>SHA256: 967df7e9ba496a3b69ed6850ee140a2464e459d860932b4c0b4ab47677b97961</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>175.9MiB (184.4MB) – 3,432,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f755f970d7c37de2b26d1ecb5574f2c<br>SHA1: 4da6ac6ee736a3599548d70eb7d1e006ba5ae2ce<br>SHA256: 4bc2d3e129ddb82b7507e1c2acc7aa83bcc8e1109cfb159853c61cde620b1277</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>220.6MiB (231.3MB) – 3,432,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 523396ba10b29cf4533b8edad150fa9c<br>SHA1: e00b3d514e27a1a82e4c310cffdf1cd8f21b33f0<br>SHA256: d4778912678767ac168e5e1abfea84b2cc15e49c1c503254c6f4a52600de557b</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>172.9MiB (181.3MB) – 3,432,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eee5311191df5603cfc7705ed32f6c54<br>SHA1: ccb1fd892cd5b71be2a50772434d94d7b8c4c0cc<br>SHA256: c66ee2114773d28482a7d9e478af663acb6f4c493ad4c82bde65b4713473b360</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>214.3MiB (224.7MB) – 3,432,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d9947e6d006650313a75b20ce311fe77<br>SHA1: 3b2b56d3cae52ba1dfd7840a2bbff5601493e25c<br>SHA256: 4eb033966fab51a07c80e4de457bf40738753060a84e0c548fd3462437f4d3be</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>180.1MiB (188.8MB) – 3,432,179 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 82c05550411c90655feba7c0f4115c4b<br>SHA1: 6bee87dc60bd5e96abe57dd1ae76ebdcf08f9810<br>SHA256: d636997d7430c24c35af17bbc084649a9667cda79b1ab11ce106b54bd210619e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>170.7MiB (179.0MB) – 1,812,582 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d715a0bb22ac653131c9070361e08d35<br>SHA1: 9d82558fd4eecd3fb858ba03d72fc4eb3d822299<br>SHA256: 034ed10ef48cd49352d14d8084de0e1469182d4f5ebbbe2b308d4db49e614203</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>174.4MiB (182.9MB) – 1,812,582 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5456dec9f61f89da7f535526d3bdfb93<br>SHA1: 84d03fa48c14d178e1e25cdb2a8e9c32c81cffd3<br>SHA256: 152ca174d6949950de24edac357e44aee1d88a49b1c626298f253fecd7cb3b8a</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>169.0MiB (177.2MB) – 1,812,582 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2b0f63939bf329dd3eb6abc0c839a20<br>SHA1: 40ac54a9f39f3add5fe5cef3639528e8bb8b3867<br>SHA256: 4a0dda9cb34a24118d3acf4304a0d9dd124698ca78037047a03ce719f98ed493</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>169.2MiB (177.5MB) – 1,812,582 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 307b356add95b701b47914bac64d3e70<br>SHA1: 4f3e57c3ea03fa75de4a4fd52da69643e6ec6bca<br>SHA256: 1f2a1dafacb3d0e9313691f5c44c30281c4af04461521161c9e8a780ce18d3f3</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>187.3MiB (196.4MB) – 1,812,582 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9119b7ab02a11b3e9238894f2b73b671<br>SHA1: 77222387f4da5ef5d3c387c81dae47116fcc6f3b<br>SHA256: 5903eefb727274c87e47d85daa5c98836253e8cd53f757907bf0d048af9da16f</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>168.8MiB (177.0MB) – 1,812,582 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4b7e368b66a186c1e520e1cdf683d099<br>SHA1: e2b16228b618a7772875fb7f41efac406f5bd0ca<br>SHA256: 312bda5f29a50c681f4ea264ed25f664920ed3ee4ca34485b0e862d4c6bc87de</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>187.8MiB (196.9MB) – 1,812,582 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64de11ec2d68dee91d757cbf0eddd657<br>SHA1: 184c88ab4d4067ef0fc767aec32a7fa3086a39c8<br>SHA256: a4a3759c6d77ce8db16c6a7d4d2f186fe744f866e4e63779f76191887b3fb165</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>172.6MiB (181.0MB) – 1,812,582 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 616474da57de09b1f1a49a3245166fcd<br>SHA1: 381110ce8d1f27480b1b825b8791998931d38f32<br>SHA256: 2eece01efe7a7633adb4517653c4fbe3719f2f4e92c209f5e971eb2b5d68810f</pre></details></small> |


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
