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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-04-18<br>IPv6: 2024-04-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.828MiB (5.063MB) – 241,701 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eca79977f3f68fd411d289387bd1ba2<br>SHA1: 89b1d5980cdd2ebf90f62f83e18d4c2637f0594c<br>SHA256: 45252f8f7bbff03c2087d14c85a14d1e4c3d923f9c29c3b74344e9ec1eb4500c</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.169MiB (6.468MB) – 93,743 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86569e805ad9a2bd168d5e7ad16b0fe3<br>SHA1: f8b5f99c0c5678bce6b98c069650890125b441eb<br>SHA256: 0862ce50ba43398f6df4b30687f4cbfc26ee7d5959a4ef9d4a25b8943a0ce137</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-04-18<br>IPv6: 2024-04-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>8.235MiB (8.635MB) – 412,415 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff6a119f02ba74085c7cb7ee8dfd5684<br>SHA1: f8d803295fb9049bf64e6d362ad3e64107bc227b<br>SHA256: dc6fb65c458d43d74ce7dd8c0da7dc92141fc43f992d6917dfd6be7b1d908663</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>7.189MiB (7.539MB) – 109,370 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41aafa945b4db90f29f6efd5b01ec1b2<br>SHA1: 8052fd80e3bf64efb8814ac557d3a5a2abda1f0f<br>SHA256: 5f3235871dc43ebbab351dc3f9662de9fb9f45cc16139738223c551b7f4158c6</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-04-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>17.53MiB (18.38MB) – 877,676 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 950ab6cf8ce270856e2428b4ed0db18d<br>SHA1: 5f9652fc5909dbdc65d9b33c3076e570b73197e2<br>SHA256: 747daf82666f7b132cdc1b30945ee9b478d1ef086b674b3e7371fd3a5e3a5e9b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>75.27MiB (78.93MB) – 1,143,893 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 81a5050f92b1a0fc9c5f58f8a3d0f338<br>SHA1: 946ae9cb178c294758d638096cc8f8bfe1985b26<br>SHA256: a39edcf5defd2cf945334931e08a57096558b99663ce23809329bf5d5e6d3076</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.603MiB (6.924MB) – 331,502 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fed612f6829372d96d1503867a952099<br>SHA1: d545a9307049b4d56f79cfc1544864fa920d1b6b<br>SHA256: 91dde8f7a7970c4c1b8054b947e0cca9ae1b8735bdd19fe420e6e491a7427366</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>18.03MiB (18.91MB) – 274,058 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b254c68dde265fc8d6412499c6db3dd7<br>SHA1: 2cbecfceb25b68f5f0f9889993e2f4931f5e18dd<br>SHA256: e4727e6d32df38a7582a7b9172ee67820f196bd746046a5050cd654393436920</pre></details></small> |
| | | Full Location | Monthly<br>2024-04-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>180.8MiB (189.6MB) – 3,159,870 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e335ee8885a5e6286297a9c06a48db0a<br>SHA1: 9b10ee274410a884c26ab662fbabb41f315616a5<br>SHA256: fc15b0d16ccdb65b6da2de506405d685d02531ce5571558ba78ed3e9110dcbbe</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>322.9MiB (338.6MB) – 3,132,412 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0eb566a7a93d1e35f303a2978c1da77b<br>SHA1: 78d75aa920c86cb0b75dff47ca09bb4f55bb6fd9<br>SHA256: f95d154f7a461a32269f564496c943eb8cb5e61df0269c831e76ea2f52896979</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-04-18<br>IPv6: 2024-04-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.897MiB (5.134MB) – 245,145 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 86953d84c1cd0d89d0994ab1cd100b39<br>SHA1: d3303729b5fdd4e92be0090d728786a641d6bdf4<br>SHA256: 9503103e96fef9a268f0d6e3e3e189c3c227ba6a962256a4be433fec98dd6295</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.43MiB (18.28MB) – 264,858 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3dee1827a7716642179bea6a3edb75c4<br>SHA1: 6d32a09ab10cd650c38bb65962cded09532e32f0<br>SHA256: d1b625011cb76995dc6c5895dea53ec54db80bd372c0878631cf89b1e7957469</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-04-18<br>IPv6: 2024-04-18 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.5MiB (178.8MB) – 2,955,821 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 100c457dda8054191dec8cb248ef7116<br>SHA1: 5997f43cfa17dfe7406c1480e1305b0ee4d7d2b8<br>SHA256: 2e80f7bb769fbecd8a09c918b55397ec9abeb21f176c73e5c23ca937d52e974b</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>176.9MiB (185.5MB) – 1,714,136 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 09506237fd701236f9a08be9c399f75a<br>SHA1: 012fc8437c33186fadb2add162e68a946c843774<br>SHA256: b25eb4c33c6657facc2a0eab8012f99200c9aa7dcbc9eb0f151bcbda5e02cae0</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2024-04-16<br>IPv6: 2024-04-16 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>9.699MiB (10.17MB) – 485,932 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cb16db6cf73b806decc44e1ec3070d2b<br>SHA1: c1a03ae67a6e4665ee1149cb739fd134ba38b035<br>SHA256: fa1be03a55b5adcdd86df047441c484dbf5e23602ae1c9f916d364b246ba6374</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>18.57MiB (19.47MB) – 282,248 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b72b7527c48f730dacab4a76aa967fc5<br>SHA1: eb7d1ad23b3a629081a5672f00601c20d6419c97<br>SHA256: e431de90c0ddcc407720d1eb709dbfc0af8d544c815ad3132fe88e9d01d59483</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2024-04-16<br>IPv6: 2024-04-16 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>130.5MiB (136.9MB) – 2,607,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8e20ac79c27aca6d94d3ebd41bc5e44f<br>SHA1: 608cd68ebb50034a931a23180d89318ff5408a3d<br>SHA256: 1164d47eda3e0351c7358d0c8a68ab5a00f7db53880222aad8ad23ee53c2765b</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>140.7MiB (147.5MB) – 2,607,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ddb4bc087181ca79ce26378c7c6e3b09<br>SHA1: a7bd56e67fa06eeb3301ef9b968fb5b9ba13be00<br>SHA256: 2a548d0ca69126ce22cae2e4cb9065addc6597f40e9eea505346eab8527e2de2</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>130.3MiB (136.6MB) – 2,607,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6aeafff6c24b2164783841ba487a3c8f<br>SHA1: 7cf7143a8d584f99c63bdc07a26150a963065b42<br>SHA256: 00b84c97703393e1f45acfb1e4b0cd15d9258d419f1d825e5a91ed979b16f63c</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>133.0MiB (139.5MB) – 2,607,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 234231d73b33b0a120de23e6b7ca77bb<br>SHA1: b0a191fa610b479626386229f937378593ecb31b<br>SHA256: 93de75ec36c19649a0a07d0432b9626e67d18f49599e74d693f77a10e7bf3a64</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>162.6MiB (170.5MB) – 2,607,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6864884a2ad93b8f86fbbcc9eb7b6d02<br>SHA1: 823c82c2b6ffa61c0f6410b4c1f1334c848e41ac<br>SHA256: 2a8141c46d80c3dadafc5ac00397a01b36507882c1cc3c8f1a6b71ed8373b16f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>129.2MiB (135.5MB) – 2,607,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bc2cb93952c3f4e7953f53bd3d9aca7a<br>SHA1: 78c653cae3989599e82c53edc2aa945482787dd0<br>SHA256: ad050ca6f80c5b87d3d9c83e2280bbd34771862165a141cbde95c6ca61187e5b</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>158.8MiB (166.5MB) – 2,607,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbc07dd4ccfdf2571ccde42b402812a3<br>SHA1: fc2f5c43537aadec3d466a0ec9bbf27af33e01c6<br>SHA256: 71bb20d97a576a20e3b89e3c0917f07cd4abfe3577fbf9bbe93d944bcebb51a7</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>133.1MiB (139.6MB) – 2,607,359 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3b7377a706d85932652008cf956b2647<br>SHA1: f0695653d87d647a374bd4b3f9f78c2c8620cec8<br>SHA256: 297d953c75976f33de42835c75c2bb951cd83bf6af75f1549ad608af2f9dc800</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>112.5MiB (118.0MB) – 1,209,720 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 48ea7a0d6133320a4b2731ae517d18bd<br>SHA1: cb769b39fc99b58b4cd54810abf049f29a7dded0<br>SHA256: c1268356f3a310b7a57b96f699bc876719e30f7d0913ac991ea843e4a9a16e60</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>116.4MiB (122.0MB) – 1,209,720 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53b88a701c4bdd27865b117fe6b6fab2<br>SHA1: 1e6e1f8edf1d39b8b29a598db3523ed1348d24aa<br>SHA256: b32726e189796731339218dde419232a73ee9cac962c8a688843f01d65c05e94</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>112.8MiB (118.3MB) – 1,209,720 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3d584e67d5e812c8a171cd08870bbdd7<br>SHA1: b184a9850a07c0e1ec7d8b0331031d53c694f80e<br>SHA256: 32405de417d7f26876e704dbeda08a7397dec7bedc2ae993a35e56051dbcac5a</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>113.3MiB (118.8MB) – 1,209,720 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1162b2fba5e57272cd7ce09d65f0f604<br>SHA1: b05d95a2f3d6fcc4e9be95111c1c2e63782eecf4<br>SHA256: a888f5958b764ffafbf2e686fbfe18d99d58ea60d280ca9e5454045dd1a6123c</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>124.0MiB (130.0MB) – 1,209,720 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 11e30931a077ba42301405f9ab61a23e<br>SHA1: 0bae0b0c646e6f93e663c3180014eea76673fed6<br>SHA256: 2002fbd41bfc9f9d1951a2ee98362663cdb9bd7ec14ca8cc177ab58df17563b2</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>112.4MiB (117.9MB) – 1,209,720 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97d3c6cd240558234e85a94a9c0cae39<br>SHA1: 3c82327d8e24e5fce5eb8c3a4077b1fa3baa54c9<br>SHA256: 3e6c43fd85a89539a3af4554fa3b1c60a2cbe2df7c725cc5c11cce9e2e7800c5</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>123.3MiB (129.3MB) – 1,209,720 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00200622fd56b97668bb197325a3836b<br>SHA1: 89fda864c1c1338eeb0cfa399e8c84f435825819<br>SHA256: cc4e1a443d2952f8e7d93374ef6504dbe3964292fcf66ab0ce6c5a30c6264ab0</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>114.2MiB (119.7MB) – 1,209,720 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d419ee1c56a9b8e0bfa6eeb25b59d14b<br>SHA1: 40fcd1fa07c927538d9c635d3f5ea37393852eee<br>SHA256: 9be19b82dca417b3514f28e984e6a2e00d1c627fc196eeb5066cd471de7936b6</pre></details></small> |


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
