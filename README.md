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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-10-30<br>IPv6: 2024-10-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.803MiB (6.085MB) – 290,582 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f939d56e7b55879b32364e48b494467b<br>SHA1: 162170729bd5e84a5762e941b6dace9e1ea85669<br>SHA256: 8d4e342a4d83c60cae6cd9da0013b48699b22793d7e6b0ca47a0e503b368e991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>11.40MiB (11.95MB) – 173,250 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e054a3b311f06e99559287600ad92635<br>SHA1: e4a7b8fa23f504441e635cf2ecf0c23fe2aebfaf<br>SHA256: 28ecc38589c3847e9fc25ddd2cf108f7313b3f701d80545356b501fe120090d0</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-10-30<br>IPv6: 2024-10-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.226MiB (8.626MB) – 411,945 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff9f59760cf502d1693d5fe0cf242c33<br>SHA1: 9c6701cfef9e85b07f8cc5d0b271ef807c63a617<br>SHA256: 63486afa8e9877499461a03d6f98848c1a19afab0d13fb5e22ebcf2b4e7c1d6a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.828MiB (7.160MB) – 103,884 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b9f813a424a1f85dce0ca6358cbd856<br>SHA1: 6d481707d363ec92a6306c71a62cef3d259a2398<br>SHA256: 30514253f3d908f302f8b1a0376b1454d034a5710a80873131203e1f3b7de8aa</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-10-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>16.91MiB (17.73MB) – 845,798 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fea476c7a6bea196242498ef99bd4186<br>SHA1: 353ec36e62808ee602e34474303abdb3a2dddf40<br>SHA256: e3b65391296e9f27e64780f7dcbe7478f307c367279594ba9bb1344f04eaf70c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>67.99MiB (71.29MB) – 1,033,187 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ee4263f127007633b52d77027fa79d25<br>SHA1: c5f956a9643d089c6acf3a4b897a9fbe2a8bc574<br>SHA256: 213e36da7f351c110d18898cfb78d714a0b622078d5dc8ac2cb033cbf34d5ce4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.939MiB (7.276MB) – 348,549 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1934c9e84da4a70171fa8a58df792d1<br>SHA1: a9efc628d84ddb0c5ec270a44c413d6e2e413eac<br>SHA256: 8974ef5ef8832adde54bf8eff5b734fbc419e040b6a1ba06eee6302c327937de</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>16.54MiB (17.35MB) – 251,406 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ccee8212e47dad6f6d37a7875599a267<br>SHA1: f12a6f633e3f93b21d90f94868a5dce0099a8f68<br>SHA256: fe5508fad3836313166aa43d498d12d6277cae16fef7835d5e92fdcd53bb2de4</pre></details></small> |
| | | Full Location | Monthly<br>2024-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>188.4MiB (197.5MB) – 3,289,697 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1a0426270d27872fad498a291900b10d<br>SHA1: 4f4a7ccb4910df8d359d2ad76a1bd80c4be37d61<br>SHA256: 6869bc8bd2854724fd6be12e1a0efa4bf028d598fe1d116783216884c78d9f3c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>362.7MiB (380.3MB) – 3,515,904 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42b742d904c555f3e530341708e40522<br>SHA1: e367baa432e03a59b81c286e5f9bfaeeb0617eec<br>SHA256: f946dbe0156a23fd65f4c67f8c95dfc19e8984bc7f84d8323fc5c478da017055</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-10-30<br>IPv6: 2024-10-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.914MiB (5.153MB) – 245,963 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c11e07b48c3ff9dc003d831e01610f2c<br>SHA1: 626451d497b3677a6bfd528418f851654f5aef2e<br>SHA256: 4bddc40271ade36b9b6ee8905c2498d63635103bc5427073914856909c60c6c8</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>18.50MiB (19.40MB) – 281,133 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fbf22f62873ba8e0b199f57ba0fbd5b5<br>SHA1: 6fa1f5458fa60dd5ffa9e15d6369f0ee131bd28f<br>SHA256: 4ec90b745fd6f1b914704f219238fc8220e392d78436d623668dd01a90435b1d</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-10-30<br>IPv6: 2024-10-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>173.2MiB (181.7MB) – 2,999,714 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3e32be3aa7ef828bdde4d0126a9b26f0<br>SHA1: 166a2c63410a55b3115f842abc7c2e112de2e8ef<br>SHA256: c5b955922ef4822687040c6bdb8e7a7de48824584987a72fca5bef6079264991</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>213.9MiB (224.3MB) – 2,070,664 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: feffb0e633ec66af369dc3d4b16ab946<br>SHA1: 913b66a8e900cedf8a3df05cf337628ff9133a86<br>SHA256: 70bed76e41e5f99b76ed015bc54962b0aef55a5a428a3b749b009e0b7410ece3</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-10-29<br>IPv6: 2024-10-29 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.927MiB (10.41MB) – 497,244 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 004076b70013179928673cfc0f180639<br>SHA1: 3f65772b215d00cccf8d86d0c78b0736c378b87a<br>SHA256: cec9464bd9bfa8b8ec4cfcea80895c44d8a8badc8541daf42fe28d578858b714</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>31.95MiB (33.50MB) – 485,550 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b00c0a43d4c0cdd77b87f48c0e925dd5<br>SHA1: 0823b4ae34779896afba0a03a110eb87f64305d2<br>SHA256: c6e00d97716481eb40243df7cd55913c5110646d4caef7cd2cca0ee84070a0a8</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-10-29<br>IPv6: 2024-10-29 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>172.0MiB (180.3MB) – 3,394,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53bad1006dbd97ce8beba5a6f7fe6689<br>SHA1: 4f5e4b4c24ef77c369c642f77f62a9729c627547<br>SHA256: 0e24e534f33c3928056897989d4ecca2e941cae4b0c40250ef81e76721e5095c</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>183.7MiB (192.7MB) – 3,394,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 465d03a36b03b9e4a665c55b1ecf08de<br>SHA1: 8c218956f25eef93f6cf89fbcfb9f187678b5230<br>SHA256: 75f142999c253961e55a1ba6cd89078ff0885b4c894103a72e57b078669b37a3</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>170.9MiB (179.2MB) – 3,394,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1fc90e39fc9bd50562b03edd6b95d83c<br>SHA1: 73778d15dd0b29c69fedadc4d94e1f806f42c6fd<br>SHA256: ac2d460b35bf28c2866a1bb9f2074bb5434705841415b53de07ffec5b1f3a489</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>173.6MiB (182.0MB) – 3,394,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d19f4606ab8e311dc31f750cefebe0d9<br>SHA1: e3acfc39ac553625ccc4dc5843d6604b972b0f8b<br>SHA256: 113cf54097436479d908a8cf703fd690b8c8f3564738f9c8f58510d20e129cf5</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>218.1MiB (228.7MB) – 3,394,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a1a3b20c63d9e71a3ab5974764410f66<br>SHA1: 08fb45392eeb5389fc303fb8bd12a8cd9849c113<br>SHA256: 028f2a451bab15771a5bfdd33fde9789e2a6c8ad6082d0af01a8ddf5835e18a7</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>170.8MiB (179.1MB) – 3,394,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a330f00a12be9b20a8ac319eadb3a38a<br>SHA1: 838dff7701af5dc751705587696984f906f06c1e<br>SHA256: d843de8e1c87b16cd007e22a642429f5c81e15723278aba12498ae239dab8409</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>211.9MiB (222.2MB) – 3,394,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 883920429bd04c1e237e6ec65ef3407b<br>SHA1: 704b75c7ec539c9bf825d90fe3977a386e092da7<br>SHA256: 0703d199b281fa53b794ebd420300caa3b404fbd59079e31a7c62a3d298cf318</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>178.1MiB (186.8MB) – 3,394,538 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: eb91a68cee1d23a2fd32b92d40982294<br>SHA1: 2cda09f5bbbf40c9592b6eaa629b6c46e4acf8e0<br>SHA256: 1b24f32636d0382dd88b536e1ccf91f94756aa31097eb2af4146ddbf3a39414e</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>154.1MiB (161.6MB) – 1,615,864 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ced3853c51199e00e1a980a880e46872<br>SHA1: 309234ae3cc82a763cac58c62a6f37cbd1dc9c02<br>SHA256: c8d54f1732360f15514c88b4a76753aed53aa3e0ce5ee6eb47e3bdbca798f83f</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>156.3MiB (163.9MB) – 1,615,864 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 73334a09099b64ba72318a61536042e4<br>SHA1: af2a86973039afdeab7f0d9d26009c1973d9ad9f<br>SHA256: 190e7b2522448c2ef931900cfd5e0a15ad0d905438008d504fe78f27618ef6d7</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>150.7MiB (158.0MB) – 1,615,864 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 859472a30a269d0179f16adf983a22ea<br>SHA1: d08960b9ec1bb5bf4bb5874425342010373f083a<br>SHA256: be111287b9ca013eadaaad1825353caef72538725483768170075079fcf3a65f</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>151.0MiB (158.3MB) – 1,615,864 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa12c6ee151510ca61fb9ec4f9c45184<br>SHA1: 361f9b9dd7d87cd7c8e3815f3c8d27904e057dba<br>SHA256: ff58d351db5d94aa0de8487c5e954d433a2be5c3ce574f518e98094472886ed9</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>167.4MiB (175.6MB) – 1,615,864 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2bc0354ce189443543cef34978f398ca<br>SHA1: e777ac6c8303ad84f720d2a6e6fe22ec21eb8462<br>SHA256: c0e0b12d5ebf30393817218aebf55f067032a34ac0174e72fcc05563ca1d90b1</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>150.7MiB (158.1MB) – 1,615,864 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 932469e02c55ba239ccdb73b2267ea15<br>SHA1: d8eb88553010b193d583d4349ac1e39906e80431<br>SHA256: 587bb933c1b83c002094d8ec6a5f61cfa15c346204c01eabb861e4a218734a48</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>169.1MiB (177.4MB) – 1,615,864 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 336f7b36000692ab56ab09a4991fd321<br>SHA1: cd8753c204f20cfdce709c3978282bd0a947fa03<br>SHA256: 9bf82c737f5733d097f52055a819885c5e1d8a424d4911c3739a4ac0acccca6c</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>154.9MiB (162.4MB) – 1,615,864 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3a8a366c4afa43f38728b7c341b66f50<br>SHA1: 5fdd9c689367472a6fb6c7febe39f8301255fea1<br>SHA256: 606ad44d7ad35449729ba8a7d3999f461eecf231c7a477bef1b93a754aa57624</pre></details></small> |


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
