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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2025-09-18<br>IPv6: 2025-09-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>6.256MiB (6.560MB) – 313,263 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8c5420b3418b35b8501b630885590d6<br>SHA1: a33d3cc24f92f6b55bbbed36f8438ad94184f7f8<br>SHA256: fe17c4d426192a6bebe717a5f67be77af016a8f6d024b2ce15b48f0982936e15</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>10.87MiB (11.40MB) – 165,198 rows – 254 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 896e3b1e2aa7aed264850e94e29e6071<br>SHA1: 3ade936eb7243e67b907e3bb45e1fd8d96050899<br>SHA256: e203c2fcb3a07a76e5db469cb51d2bc5397ad3421054c0e6f83325b564c55fe1</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2025-09-18<br>IPv6: 2025-09-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.645MiB (9.065MB) – 432,898 rows – 241 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 35de31ef2c539a4a6f55346401f72c26<br>SHA1: fd4d8a988fe92916e3c0370bb29f51726b5a0d16<br>SHA256: 881ec405140d166fa5c1616cc9159af6494f7e156609832ceca66f17dc7ca5c2</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.273MiB (7.626MB) – 110,641 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bb49d30f7302284335785f0929156d3b<br>SHA1: 81e102a51d049573838f6d7e882a434fcecc08ce<br>SHA256: dea5f4a9743510573fe63b66c396eb783f4f78f66419daa1e87ec2f26cb46d20</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2025-09-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.20MiB (12.79MB) – 610,582 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d3b1b54210e29bd9def6542642a930a8<br>SHA1: 9856c88c9db510b524315ee60c2fe1433c366c2a<br>SHA256: 535e9e2128a184b362825ea87d84a3b963939efc468a38ce189193cd3ce785b4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>66.23MiB (69.44MB) – 1,006,443 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 843d792aaf3808cf7e3929b92e4f9805<br>SHA1: 636e5b726c40cd808b5c16d20af489c0fe896600<br>SHA256: fb32f522be1d159ba0be8d3547dbe4a9d947daf9e3aa98ed83f860c0c9a12773</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.825MiB (7.157MB) – 341,824 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dae1f431e9d10a462dae84888365884<br>SHA1: c0cc78c9aa347b8d712850c57537fc0dc50f1dfd<br>SHA256: 3f57c286e145770c2ac0d5d3c14088a919db312a222bfef2cb85941399367b2d</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.15MiB (16.93MB) – 245,375 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f7e3a8bff7f09ee7cfd621ef044564b<br>SHA1: feacd88a985ae6ef5d668ffcf375eefeed7948b4<br>SHA256: f554d05a841ea0162859a713eecebb3fb0dc814ea2d39b91150dd45627c31fed</pre></details></small> |
| | | Full Location | Monthly<br>2025-09-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.9MiB (217.0MB) – 3,624,799 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f7154efa553f5c77576cadbc5c42ec9c<br>SHA1: b63ba0a183e94bf6cd1aa8a15db942b52d55841e<br>SHA256: 00286d8f1fc1f8f801a25f123213615fc637aa494c49fb2537047bdab4b1aaed</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>448.8MiB (470.6MB) – 4,362,462 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7375867bcf97ba785ec1fa3d092fb0ae<br>SHA1: 37a209470da0930c2308178d77c0c1cac376d849<br>SHA256: df10547da1aed72a27d58d5fbd860b66dc9bfc40df34c5dcca2b7da7fdf24ca0</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.185MiB (5.437MB) – 259,491 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50d719d1853e86e8da56334658c35eba<br>SHA1: f811bb310275e7b7653fa90e869cf112fe526acc<br>SHA256: bcbf902929f7d249538703a8dbbcc64d8fae4900531479cf0e3063367391f946</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.57MiB (23.67MB) – 343,010 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff677ddad3772ab36197d2ef84bf42e7<br>SHA1: 8be3a4e0ee14af3d087f70294904f7aa883b6743<br>SHA256: 0f288add4994bc16d4d6387a5818de57f3def88cb259fb8fe4a8f6b507e4c820</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2025-09-14<br>IPv6: 2025-09-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.2MiB (178.4MB) – 2,949,463 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ec6ef92605faf0c8ed3176f371a4f89<br>SHA1: cd21e0629e442168ad794701d10639489e2d7e3c<br>SHA256: 3470fc0e8a3432aae0bb7caf8d995d20c8043b2486e3fbc23fd209fe4a11d530</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>293.9MiB (308.1MB) – 2,846,052 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8446667c1feaa357c25104ee40c7db47<br>SHA1: 1631c4d82f37dbaa7ece00c99dde97aa5483e6ea<br>SHA256: a265bc2be67ada5c65a6d3631fcbea01cc1272b1b51f27002bc5f3bffbf061ed</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2025-09-16<br>IPv6: 2025-09-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>12.66MiB (13.28MB) – 633,715 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0dd110e7e90a0f803d593e6a1760dc62<br>SHA1: 3b676bfc5531a2208b685f5c2b0dd2ed1fefbfa2<br>SHA256: 5e5b905d83a9954009f09e9c30ed573e7caaae0cc8b3a8834a50c66a77f52b58</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>43.26MiB (45.36MB) – 657,387 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a214e0f8cae5f19c4d33924aca4964d<br>SHA1: 10846f04ab5e211842eb91e6dda933557b8adf0b<br>SHA256: 4f4463d6ef8b5eda6cdc4692c6547d1c8539dcc42c3abb58b40aa141dbd62e62</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2025-09-16<br>IPv6: 2025-09-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>175.6MiB (184.1MB) – 3,459,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a3b2f50ffaa62381afb99a79d5a0b57<br>SHA1: 2d9483aaca2ae957cd638e2023f428341bb3d360<br>SHA256: 51c3f26e9e93960620b0ac2b1f94432e059ef69530513f15dbc04e38cb2c455f</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>186.6MiB (195.7MB) – 3,459,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 691eb1fda0450e5d2f8162d544dd1dd4<br>SHA1: 149e7280d74c56a7aa33eab48760b54ae265daf4<br>SHA256: f62429e8f8aaa42465630c6f70b5fb136067d80bf1ac08f91133ff1b840610c4</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>174.6MiB (183.1MB) – 3,459,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21d78d571634b9ea2de202a50116053c<br>SHA1: f0348773366e4b187cba48da79f7b3c5b993180c<br>SHA256: 828215a0e1a80b1dc0fa67ffbc05e0ad6089b3847ddf23c940c4f1ab6deb4a84</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>177.3MiB (185.9MB) – 3,459,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09c3bb8e091e21bebd437b8d5de152f0<br>SHA1: 19ce1d2afdba65ba6a3d09e7573b630ae679ffd7<br>SHA256: dc03c2db6d9d2795462afc2fef0008e404eb311ec148ca05a69847c90f99e13a</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>222.5MiB (233.3MB) – 3,459,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0a3c761cbf83cb019f37f995ac47d5ee<br>SHA1: fa6c94aeb742197d0ba00862f56ccac2a10ce731<br>SHA256: 8df3087927ae5da819d1790964ef588161ec95523fad96b7b2a488c4b4857967</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>174.3MiB (182.7MB) – 3,459,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23cdf7be3fb65adf339197e8ebd0bed0<br>SHA1: 7cf4edf7eb225476aded4034f167d3052230e346<br>SHA256: 7dcf33279674f321668a2d0d831f86b843684cc174cce0b8adfd43d380f61509</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>216.1MiB (226.6MB) – 3,459,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e1856720831b6e77e7923a5aa6f7ebd5<br>SHA1: 905916a119a649b105336e488af73d69c62f37da<br>SHA256: 80cda7924cc9a6bb6f7e5103dc1e2a5384aa74424e02d6b2be2c552eba4549f4</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>181.6MiB (190.4MB) – 3,459,587 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 29831798c393f69c3a05f2ce67cd02cf<br>SHA1: 8aaadd16ac33fa5a10e5207bd7985db0e0676928<br>SHA256: f61ed51e4328d839629757b9a673d25c508a33add00406397ce6684f76d05049</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>177.8MiB (186.4MB) – 1,885,409 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7486e80b0d1b47a590e6fac6d18b05d3<br>SHA1: cd6c9c738002273c42c3c206f365791f037fa6f5<br>SHA256: 0db8a49e649acba5b111e20d15055a98ba44f0b379e81400e5d2e731282df9c0</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>182.0MiB (190.8MB) – 1,885,409 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f1305e7d3380c71933bbe908a91644f6<br>SHA1: a58886bea3eca53fbcc7d814e2a530a6d277ca7c<br>SHA256: f19f7d5b4c954b9168ac6529424b8ad133683160b7333c7b78ad5fa2abc56341</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>175.8MiB (184.4MB) – 1,885,409 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 75ffc5d9e69beb35a3fa9461b236bf42<br>SHA1: da3b1d44aeab780c9b1d6e7d7d6319c188da4163<br>SHA256: 68608fee4913b4c9cfa4e3ab79f3175e7fa3f4602bc20450897c0b852ce6a1c6</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>176.1MiB (184.7MB) – 1,885,409 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ce3805c389f4b8f6e99699a05db654d<br>SHA1: f4ed3bee073e094a3c9367fe3bd30d3c2233dad4<br>SHA256: 941f6c9aeb3e7b537a68794d024f93d0b83dfcc50466a481df10bebe12e175eb</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>195.2MiB (204.7MB) – 1,885,409 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa66790aae3dd7ef8607282028d36986<br>SHA1: 182576e1d1b220315fdd6c706d211f7f2cd46297<br>SHA256: 60ab0d7231e198e70f895f0de5190324dcf3b05b02c94995e95b20b4a46e8678</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>175.6MiB (184.2MB) – 1,885,409 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 613b4b355cf43428ccd0ae5dbe29e1eb<br>SHA1: 09ed0ebdee9cbde6fcdd84aae0145ae86bad65c8<br>SHA256: b8f1874e90b9581f8c1ead81195fbf45204a3bd1d387717dd3cfdfbf238aa1b1</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>196.0MiB (205.5MB) – 1,885,409 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d29bad08c41eeb4fec7dae6a1e4beb6c<br>SHA1: 0be12291aa081c2d0b27a21d6b8445a466db34d0<br>SHA256: 550e69c44230caccdf87347805ec8fbe3b24358b13bc45031bb4a0a3e0b5cb4b</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>179.8MiB (188.5MB) – 1,885,409 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe4a5ef3cbf00ea3fcef8a546a99a2e6<br>SHA1: 9f0b12c291b57ba5a45f31dc138091f599f5e316<br>SHA256: acfa21fa4a95267a19be108e1ad2fed8be5eeb8d13aa52e6b8812e825992c66f</pre></details></small> |


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
