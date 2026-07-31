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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-07-30<br>IPv6: 2026-07-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.431 MiB (5.695 MB) – 271,814 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3179b5c45330e37883ce1802db778e59<br>SHA1: 2f504432f495f7b17704e9dae4bea8b82b8acf56<br>SHA256: 13565e961227dbd86ca9bd8763ea929890b200ef733dd39937170a84a7d96e23</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>16.84 MiB (17.66 MB) – 255,977 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3657d8be57ce97599ce509eda3c32b1a<br>SHA1: 43024815316f0face5876bd26874db123f124dab<br>SHA256: bd6ffa13395b717348c3f61cf9015c1a85a67b7bc8c357f289b51c6b031e1c3f</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-07-31<br>IPv6: 2026-07-31 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.031 MiB (9.470 MB) – 452,187 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41963aef17cad38ea44360ba7d6abf8a<br>SHA1: 7938232f6348caa58205a2ba13915fbcefbf1c15<br>SHA256: eaebc38dc5d78c0bbe701cac48bd4c6c7bcf95cd600f4a8e76de6b2d80ac8410</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.967 MiB (8.354 MB) – 121,191 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af01a067d4ed3af662c1c5db065cfa88<br>SHA1: 8d0c37f06bf843c40e334f78b999a334a8ccd4e1<br>SHA256: 580bbe7ae0741f412b969bc68df9430e78b3d946e1d55f7c0e87c1ce6cf63eda</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-07-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.15 MiB (12.74 MB) – 608,382 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0384ee34b592047091a489bace159e9<br>SHA1: f0d92bdde7c6140e7dc114930dba91f29a2511ca<br>SHA256: f0c8fa914113aefef026924108027aa3311c4a20fda272d1616085adecf85598</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>42.31 MiB (44.37 MB) – 643,013 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 497e9ea68064d99e9479564288cdcd2f<br>SHA1: 1cc438adc27b6a35fe1a9fb834701f44599c28e8<br>SHA256: a422d8dbea3338307d9c97860eb96ab958e31fe45fe56b0a1c70488951d6f59c</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.078 MiB (7.422 MB) – 354,560 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f3ec835290735187164b1f2f622ad9c0<br>SHA1: 10464ef5eb489f4745096b1c71046b06409244b5<br>SHA256: 6bc4af63c1e15b4d99d5b9dd9cddeb67bbf2eafc2529ba5d9ec4525e0fe7964c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.51 MiB (23.60 MB) – 342,046 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 569d0c6b66a745289f0e152318090f38<br>SHA1: baf1ef75355d41d9bc4380f97ed3b085db479655<br>SHA256: 8940a06c7f9a27f129048c5a7a0b1579b368020d88f2d2efe0fc813b6d2f97e4</pre></details></small> |
| | | Full Location | Monthly<br>2026-07-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>209.3 MiB (219.4 MB) – 3,666,805 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f9b729ab459cc2b765b3b4ea035f481b<br>SHA1: 1496af12b72ee784e304cd84eb7335c826bc3906<br>SHA256: 69fc5ebf5414a7a939fc25a35f3128451cf340211ae51ab9f82d53a331d8ca03</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>451.3 MiB (473.3 MB) – 4,386,528 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f197b2ebcfed77f9adc3310fc7b6020<br>SHA1: 24b1454a40fdda39f37fa9367a6a6a5a88d3be33<br>SHA256: 0160ad6b5bca3517eb65f79d6db1f9e373eeb34cfccbf189a588bb330d17af06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.670 MiB (5.946 MB) – 283,812 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 96cb0452e66db1c3a35242fa031ebe0f<br>SHA1: 28fae5a412332f0cedc711132a0dd6f337488ec4<br>SHA256: 2785f482dbf1f2dcb1bd3a9f253c708b1fa5f86773908ef7a2f2bb16c0dd1ff4</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.24 MiB (23.32 MB) – 337,921 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b1683effffd067b4fddf82095f002903<br>SHA1: 82f6a3b239649f9e8af05d58b628eeed874ad7cd<br>SHA256: a51cfe2b60d111ec234510abdd73583f12186f7fc35e3decd80fd4ef4b5ea654</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-07-14<br>IPv6: 2026-07-14 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.1 MiB (178.4 MB) – 2,944,788 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 52717d3cc345c65ab5cb86167d9b2112<br>SHA1: 0ad1bd8bf0bdf711f51a9a37bb75090cbf4ffc84<br>SHA256: c92293057f12c2c364411c35a02de2cb229e7a21791a1bfd25cab2ba6beac1cc</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>298.9 MiB (313.4 MB) – 2,896,639 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 23b3d9e4addd1683ed707d17a98a0e22<br>SHA1: 572b0633e6453018a04db4c06504726ffcbeadba<br>SHA256: ba14acc8e2fc9ac380640ba99de27ab073d603598996f6737853e5a1ca4a8a13</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-07-28<br>IPv6: 2026-07-28 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.24 MiB (11.78 MB) – 562,685 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 074c439f907b992fea9743734ec28f53<br>SHA1: 68cbf665161fed697ad2ba52b3f856021e0e14a7<br>SHA256: f767db9a66d3d01f85d581218572ea51a0dc1b5f8149d7badb9e80aa24a3df07</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>35.83 MiB (37.57 MB) – 544,555 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea7a9dfebb1e9318ea666cc3056a896f<br>SHA1: 38156a066bf44b02723650c8940254c1a4e29c37<br>SHA256: b023c1d43d6752be5d4e2f0ccc4998bf385351af7ac37de8af66df7d36e4eb42</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-07-28<br>IPv6: 2026-07-28 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>193.6 MiB (203.0 MB) – 3,767,494 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 63cafb64ebd6c2b8386b94ca2711c444<br>SHA1: fbc34676f84de8104d2419af34d08e99c79dc6d5<br>SHA256: c276f8a97e478e64c613792ffcb0981284f03686f9afec3d1f28ab0a3bea8f27</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>202.6 MiB (212.4 MB) – 3,767,494 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86074d24be5a1caea924e66ee01d6506<br>SHA1: d0e33a803419164df65b820b3619c294cdf53c3b<br>SHA256: 303525822cab554fb2fbd817412313d77d1e26859be5a52fc735c065b6912d9a</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>192.7 MiB (202.1 MB) – 3,767,494 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa148415113f750fdd91beaef75c4805<br>SHA1: 27643c05df50bf2d7117cb115584c140a4daf24b<br>SHA256: 3f64b89e6a991ac9a3908ab1dbf28f12f49639268dc22b34c71130d7f866cdea</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>194.5 MiB (203.9 MB) – 3,767,494 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 66d523a97417c6065d8ef7fae2d912f5<br>SHA1: e2399891a736c8fed048a6ef2898328af7dcf591<br>SHA256: 53850e5aca090bfc3dda7f39ea52fd840c9863c000af6487c60189f399f2fae7</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>245.1 MiB (257.0 MB) – 3,767,494 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e81e3f846cd85e4da50a92901eb76441<br>SHA1: c02a48ebc3634f8a3874d8d3ecc4e559b2ee31d6<br>SHA256: fbd4cd64a064a035b3602e60d09d260c8199df0aa7c6df6f5a71ca74973009be</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>191.9 MiB (201.2 MB) – 3,767,494 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 44816be2ebc3762de3f8992f9408e6d0<br>SHA1: a572a6115acc8e5e7149322ddaf3c9d3d0e39e85<br>SHA256: 02b2cba946ef760cf3cc72f0b083d1aa53bb69613e7a682610604163c57004a9</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>235.0 MiB (246.4 MB) – 3,767,494 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8fea2929bf9669209e16899d0e6aeead<br>SHA1: 7726885b16d631b0859d21384eed45a29879069e<br>SHA256: 96401e0defe7c3a0f41263909edfa58e8393178f30bb135d727c4b70af9452b7</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>197.7 MiB (207.3 MB) – 3,767,494 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c99efe4aaff3c7f9ca55837140b42ff6<br>SHA1: 20853f3ac06f85aed704bc3660d2774836e198ec<br>SHA256: c6671120c204ac4957414504a3c50f2f7dbd3065a9a6fa567226af0745676f8c</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>197.9 MiB (207.5 MB) – 2,075,569 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a3a73fd1b6ab321467b95b6b662f763d<br>SHA1: a969c7d88275920d6551eff6024eea7bdbcfb5ec<br>SHA256: 8a60b200c7b18a97e913fe8a11ac32df72bbb34fd131bcb3393b330f3db0cca0</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>201.1 MiB (210.9 MB) – 2,075,569 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ba6d220963b5e83deb75ca7817ce8bc<br>SHA1: 0537a6fb116ea7b5c2a42f993e1ace04f6e494f5<br>SHA256: cce72db8260b6c9848d055145a1d4189303b6f06201c3432a20402976817a82c</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>195.4 MiB (204.9 MB) – 2,075,569 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ba7d5c76142142cda166c3c98d20f6a<br>SHA1: 06a8272fec8b1fd8c62e0a2c02af560c2e6f4433<br>SHA256: 258b4db17c86fb329dd14dd93da20d8aedf28e1406627c2c409bc43e8dc44cbd</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>195.9 MiB (205.4 MB) – 2,075,569 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e289c9fb41b3d47aaf0d0dfdd0d1d390<br>SHA1: e4123094705f7775530a610c00bdc3754ccd4fdc<br>SHA256: e8e0b30a009c0d335757e502ad83d99c691093ee206e5ca3b55743578348d664</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>217.9 MiB (228.5 MB) – 2,075,569 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b5fc11192601bfe513e58b15a22c2791<br>SHA1: 562e115a547b645f164b7ae9c601e893a6945be4<br>SHA256: 569fccd476f55c6a2d67f256fbd2bb665d8637f09fee8f3603cad8248031016a</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>195.2 MiB (204.6 MB) – 2,075,569 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b995567f5adc017f58cdee6cf7b18f59<br>SHA1: 6980271251c0c1946b6bf69191800d7c96ef5cf3<br>SHA256: b4c6bef9781228b119f22b5c7e11c7010e0f3ef8b8547065e733850e10e9c6bd</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>216.5 MiB (227.0 MB) – 2,075,569 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 42653c1589a254b8f93fc157bab05fff<br>SHA1: f0355919568a476a43d381803facbc200fbfcec1<br>SHA256: 8b1f26344dcf985537e68f42f9dcd847522c574edf5f04ff4d0beb8c610259e5</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>198.0 MiB (207.6 MB) – 2,075,569 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1eeb0a8a302cae0725b73da70f6a198c<br>SHA1: 06ccc829f098e729d50ed30ad59328bf007d48b4<br>SHA256: 59f8e3acd139acba2b4642863569644793ebc81ffdddbf4607c014c85141c1b7</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db server-country](https://github.com/sapics/ip-location-db/#original-databases-update-daily-free-for-commercial--personal-use-no-attribution-required) (GeoFeed + Whois + ASN) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

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
