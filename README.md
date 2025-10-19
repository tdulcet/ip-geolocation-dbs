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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-10-19<br>IPv6: 2025-10-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.300MiB (5.557MB) – 265,496 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5093da1491cb1dfadd7ad08431f682d0<br>SHA1: d0d95c3c03944efd1acb11e05414193edf2f8e76<br>SHA256: 98e7774e7d128ba60b25b0d9363e74d41b6e9fead55ddb197b2935b3732a4d00</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.804MiB (7.134MB) – 103,393 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 08923ce050f77df16f43c79d073733c2<br>SHA1: 4f3369ab2417df4de09518caed522993fa9fb54b<br>SHA256: b8ef49d0c35d949180a9af07865f5f0209321cf787bca30c3624ced58c8d8ae1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-10-19<br>IPv6: 2025-10-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.709MiB (9.133MB) – 436,100 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b270b4828e469930f8005a10170977b6<br>SHA1: b774070987bda24fcaec91db82e221ca533775bc<br>SHA256: cfcade75e2629390d1f833f341e44f906a2b4052dffada9c6aea5560c5cbc5cd</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.408MiB (7.768MB) – 112,696 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 946189ababc91666902f3f4b2f99bff1<br>SHA1: 175ea0c73a6e85b1551ecbb71c6f8a8962f016f7<br>SHA256: 705b4c9c8062a6cc312bb952fd4b12896adbdb48da47c0c38e975a99bf3618d3</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-10-19 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.63MiB (13.24MB) – 632,272 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8da7f82876668366a8078a6741c6762f<br>SHA1: 67dfc225573da362b442199967395afe129de0a6<br>SHA256: 57e1663822495d2ced5b9f489727d5b4e737329ad48b7c041d6f51f17f3078e5</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>57.51MiB (60.30MB) – 873,931 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d2a5f04bfeb8c1406d2f07b0f3a9ea9d<br>SHA1: c09341d89e746b73552ec5b89fce2390565578e1<br>SHA256: b97e57f790a73a7f7efa88110c116247279cf51a291170388178ff6d48464760</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.915MiB (7.251MB) – 346,209 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1e6d674990e0f107fbd088e17b77f819<br>SHA1: e21f5ede55e9a68287555b79c322fd01792544ff<br>SHA256: ee56d76f9c227d305e7f5b79e40e5d3a11d30d9b4b4a21b0a814bc5fc6ccab58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.87MiB (17.69MB) – 256,387 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf6418c75d48ec2ce4a2a1c5d27690ea<br>SHA1: 9b685f6a9fe8620ee6003242f3c5acf610337b72<br>SHA256: e1a598f6d63830a2bae69310a4cc6608adaede1395648f0431135c9239a1caec</pre></details></small> |
| | | Full Location | Monthly<br>2025-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>210.3MiB (220.5MB) – 3,682,011 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42145ba207725adfe20cd9225ad15164<br>SHA1: 1d40332c6092241cca96d8e93cd7fb5c58e051bd<br>SHA256: c60c91128d39be7572205c3f816d9173c65edc218778bf32f3d1094e958cfd2b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>464.6MiB (487.1MB) – 4,514,867 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5f22f776ceeb745f6db78a0eef703371<br>SHA1: 30ac2eb9a7fa4373473059683b5de9079a24fedb<br>SHA256: de1e8fbe3abd61a6d689615765352368449ce489b189853826fcfeeff7321137</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.151MiB (5.401MB) – 257,820 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8f9908959f108cbfadfc9e7ab6b5884<br>SHA1: 972f263b1d19a67871258f42188f94e931d59854<br>SHA256: 975f5d9342bd724b46443117938bdbe68a26f1a6a67fbe877c780fa1f2a80930</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.32MiB (23.40MB) – 339,151 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 899eeee26f538ee8debffc108e588d79<br>SHA1: 0d77580077bcc05fd3f417a87c32cb013c8833c7<br>SHA256: 113b63ab10291245788982a1804bdc42917c5ba1431bd06f83e8db90d898c105</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-10-14<br>IPv6: 2025-10-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1MiB (178.3MB) – 2,948,996 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f1a80c418d402b73fffc10b5e33b367<br>SHA1: 477f8a255df756d19d1c4c62f148143d63c6cca2<br>SHA256: 1e61d957caf16f9e8b581bb50ee239a27b4df55d443d3189a6df269d1e4a412e</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>286.6MiB (300.6MB) – 2,780,123 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e193b09ce3e796f7ff230a3153398e6e<br>SHA1: 9fb3a062296faffa1023004232fb6fc559be1308<br>SHA256: 65b454a0db4cc428574b15646da49862ae8240441885272744911821e2cca9e3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-10-17<br>IPv6: 2025-10-17 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.91MiB (13.54MB) – 646,278 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e46ac480ec1d807159862bc822efb63a<br>SHA1: a5d04484ce28cc126833f4936c8bc16f58b3c223<br>SHA256: f9100894745aecfa72eed653a7f6c004d6831d2c57e4853d580983652b29b047</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.34MiB (45.44MB) – 658,572 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bdf35514164de4f01d4e15b69a1627e3<br>SHA1: 606f034ca61fd527b28705b7ffe2631dd209cacf<br>SHA256: f59528ee133bd238a00882f98631f452de85c9264b6eeeda24a57c803427096c</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-10-17<br>IPv6: 2025-10-17 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>177.4MiB (186.0MB) – 3,495,636 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b95639b20a0bfdb85a015e1e02dbba81<br>SHA1: 64aa94b0fd19b23cf9aa891f735fc95e26b218de<br>SHA256: 3e00033906ade3b96b855901e4597403103de902dba05cb1f39ef0624779f536</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>188.6MiB (197.8MB) – 3,495,636 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a67b43b37d8c4ddcfcba26159a7c90f4<br>SHA1: 433c74319e12224375c00701a5a9d1656a0ad25d<br>SHA256: ede51198ed3c4113ff0440b7a428e384a1fe427f6de97d8f34d3d6951012cdb0</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>176.4MiB (185.0MB) – 3,495,636 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb8cf5cf74101333a7a3c93126806f73<br>SHA1: ad12b7f407d857cb8f21e93d8765185b1fcd41cf<br>SHA256: 406c00827c2e58bfda08320d2a03d933be743d837fb5cf39660ddcca5de6f18b</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>179.2MiB (187.9MB) – 3,495,636 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9eb71a21afbbad491d83d4d433315930<br>SHA1: 92bbb91188f05a8bd92813add4a428c6c4ad1e4a<br>SHA256: a2f5391c0045c68f91abd9f8374f3860c890655d8527c2fe5dd56367f86e287a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>224.8MiB (235.8MB) – 3,495,636 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba1ea36dabfe7b638314abdb3b3a447e<br>SHA1: be44c7105e27607d0cb4555df746349d7e27c855<br>SHA256: 05a261368d9475fecb7dab108703dc1e130d91e7194291be7172b5a17198d6e9</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>176.1MiB (184.6MB) – 3,495,636 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e454295e10b715f5bbc3579508c08f9f<br>SHA1: 3895d9f87706198b68addff2d1da5d2b09cea1eb<br>SHA256: d362a20a7e0f263fec76e25321ebd874d738059b8e45c1f5ad6e30826205c086</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>218.5MiB (229.1MB) – 3,495,636 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9e98bc260f5a9376aeb407fcff3fd881<br>SHA1: 9d7c0b17b6b889581f3b56898746f3a045e00eca<br>SHA256: efc4042dd09540fd4ede93a653cf542e09976a75ae16f5700c752b6a862f0e32</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>183.4MiB (192.3MB) – 3,495,636 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a2300ad847a1679eb19723be7b753a2<br>SHA1: bc067a0a00d2ae5de1a1623d0f3d244485b43b9b<br>SHA256: d0a2b8c7a8c6c1bc11c86999dd27d9f9c9cd6b5448fc52cc25ae2e7da2453de7</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>179.7MiB (188.4MB) – 1,903,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94d2ee897da3f377ef538e9b4399cdd7<br>SHA1: fda5343d04becd395843a7643b18646865824a71<br>SHA256: 040b82899784a476f377254a42f25141b47ea8bdf41f5a77136c38b5c30c7f93</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>183.8MiB (192.7MB) – 1,903,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d52017be7ca57d8c0a1ce5c1adb5582<br>SHA1: 8612c704b124cbfda8a834fc6defa6a93d7a8990<br>SHA256: 2f412ccd3496f9a501234e3b3371056b95efa92ec33402097e3325e7959afb3e</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>177.7MiB (186.4MB) – 1,903,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57e8ce9e1ad6c28cfd2085c036bac727<br>SHA1: 8b07a09f56d14cd845a2337b2dc1fb7c3b4ff0cd<br>SHA256: 70a35cebc96260b54ab0afc9483477ece7c0a591907bc3e7f1850401d253f574</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>178.0MiB (186.7MB) – 1,903,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 77f38f7bb7d9e8f417d597f30de14b6d<br>SHA1: 15dae6a4dcd7809017ba70e4577e2cbca5a75a85<br>SHA256: ab01684d183917c9eb4037f12304a873133a4126c1f8cb5cc646a9628e9539a1</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>197.3MiB (206.9MB) – 1,903,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7b87001af292be8b4889d700acbd28d<br>SHA1: 548b4bd62d7e49cfc13443b9886376550b7b3ce1<br>SHA256: de3cbf46e284249b64f0ec30ec50c4ef4a2213f84f8d12128b5c8ca0d9e80c2b</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>177.5MiB (186.1MB) – 1,903,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b673b25426be9e5a590560eaa1990e2e<br>SHA1: 085d6a2d5d39b4b8a3653814a2bea0d979a3b6d3<br>SHA256: a53a234a950415b7a0f334e0ce5015ede2aae28025366b37d1b8131ffe741f9b</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>198.0MiB (207.6MB) – 1,903,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 17cb2d0b6ce62fb21d2264bab029e5f7<br>SHA1: 8640824afa473c4f10cf19825ace43aa2f849d91<br>SHA256: 36c787a692f8554bde485151f596f1841a908f2377bcea1c34928d708db58348</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>181.6MiB (190.4MB) – 1,903,847 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ba2d9a8fb121ce04b205ecee2245cd1f<br>SHA1: 0c6cc67ba90dba162dd6e1941e547bb914b23afa<br>SHA256: 36ae7873f794678cea3e57294c6314e1fa7500dcdb22ecb8710ef288704ff3ed</pre></details></small> |


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
