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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2024-05-08<br>IPv6: 2024-05-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>4.840MiB (5.075MB) – 242,293 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97b52440becfbec57e897435107561b7<br>SHA1: 05a4269f104195a48b1df98cb11ac5124f462019<br>SHA256: 7ade1d52da3fa7555fb00d210ce91b063054b647ccd48da980494313f9a75044</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>6.268MiB (6.573MB) – 95,254 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 479c2277f5943febb5463720b4883373<br>SHA1: ee676ca7946fa9be47f3e5142e0469627a8065ed<br>SHA256: ddc64d314b402a6c09bb8a8d9aacf2e4b600188947334cc4fb86806339dab546</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2024-05-03<br>IPv6: 2024-05-03 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>7.489MiB (7.853MB) – 413,328 rows – 126 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f21d0b0177a675c8ff9d72f925f345b<br>SHA1: 4e21a81c048667ad55f5aefccf18ed7d0782abed<br>SHA256: b11173725d3c0b9f35905fa17f23705444d8602f8ecb7922eda9998447b0294a</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>6.222MiB (6.524MB) – 97,295 rows – 84 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 441d8d4ae682ca094e1c3b182659fe0a<br>SHA1: 68e3bdb66a9b94261e2977835f38399f61cd1c52<br>SHA256: a0b5b676a5b2a68993261e37216b04a94c164b544a65d6c6fbe4fdc0e8457292</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2024-05-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>18.79MiB (19.70MB) – 940,786 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 16435f6422c6c8660cb4acd0fb579c7c<br>SHA1: e494d6972aa524a256cee505044206209a300a62<br>SHA256: b8d3e991ecae45b1d131ced948a296e52576fc87e0ed7789708d4a1a30f9fa7f</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>79.83MiB (83.71MB) – 1,213,201 rows – 246 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7c815b7e21c9337d788bcbaaef43afce<br>SHA1: 889afb0a3a4e69f0b1d4702bfa6da50a432f665a<br>SHA256: ee6d95f2f1980e99c9b8cfb734eeccefc599078447381bd69dd782691a483001</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2024-05-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>6.812MiB (7.143MB) – 342,272 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b6a0dcf5757ea0e706a0c94568280620<br>SHA1: 03bfb92700023a7d01c587329c906e922cc5547c<br>SHA256: 0701b9503a19f2b5ef4f8f0658a2a534df0822bfbef51efb3a1bda57a55e3f99</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>19.66MiB (20.61MB) – 298,729 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2849001e67a02bd3a08a527da352e577<br>SHA1: 9f755c138f40a70c4ae69708dbdc5e8ef7f7767a<br>SHA256: 5130d7be5953b435bb330affb2fd878e7d5cf8b2c52a1d894258152ceabae370</pre></details></small> |
| | | Full Location | Monthly<br>2024-05-02 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>184.2MiB (193.2MB) – 3,220,410 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 370827b267c010e93a9e283b93c295b7<br>SHA1: dc5b7559d75d79ed88de26ae4281be2075f11796<br>SHA256: 540ecb934cca1d5d8c74a0a6af24ad0a1ff60fd114c0d10e34c816f2c71f0407</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>352.3MiB (369.5MB) – 3,417,644 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 390cb4649597293b6f658c2539043819<br>SHA1: 083b6f7c90866d15cb38d7c80161776a233b8efa<br>SHA256: 390822a76bd90dd6a9a255e68aad76890959f99892f2f5b9db086ce9aea01a06</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2024-05-08<br>IPv6: 2024-05-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>4.940MiB (5.180MB) – 247,251 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 01186f618906e8a86cb19644d41d20da<br>SHA1: deec7203d4d1b7d2f6e570d2f9b266e527f70d48<br>SHA256: fac2f5169a0d09163c490a15ed2baf33b320d045d4a322e303615ee1c529ed30</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>17.59MiB (18.44MB) – 267,259 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 22d3e3bcaa44ff5f7c9bba501be8f19d<br>SHA1: b8157b22815f05f6188687637be52c92d39ff65e<br>SHA256: 3fb81be267f86c69bb8805e4daa892738a3a76558767d4ef27bbf6f95a18210e</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2024-05-08<br>IPv6: 2024-05-08 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>170.9MiB (179.1MB) – 2,960,692 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 14506da570232614ab1a76e45735f421<br>SHA1: f139b51a9c5a9421c67b1965ac5401befe35b734<br>SHA256: c51306ec8cf048271b6a8e500f942292deda452f14197c48b83c1baab6ddfc01</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>183.1MiB (192.0MB) – 1,772,190 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8d155edcd26a365c0bb0cd5ec2bb347<br>SHA1: 940de771ad10e3cfcc813ce70bbc1ec58c7e922d<br>SHA256: e0b1c26467bacd38d3d9abf3057b61a9343e6a869d9ef21906a2030ef276cd49</pre></details></small> |


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
