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
| [server-country (GeoFeed + Whois + ASN)](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2026-10-07<br>IPv6: 2026-10-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.tsv?inline=false)**<br>5.617 MiB (5.890 MB) – 281,112 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f207db79590e6d44ad1a9bca197525f<br>SHA1: 35fe2f4fc188b5e2ba644085a7342d9f22408b3a<br>SHA256: 4cb203aac33857b06ad986fda935b7b63acb7f2daf49aa6a0608055c260439ea</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.tsv?inline=false)**<br>17.30 MiB (18.14 MB) – 262,943 rows – 253 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e2cc96e5cc7e272479717870a0bcdaea<br>SHA1: 21952e4517d6a2a715154d9a479d9e80396aabe5<br>SHA256: 0207bcbbb85e59bde93823e9a4d4734ec78fef5c8bcd3b063bd296d8a1a9ca30</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2026-10-07<br>IPv6: 2026-10-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.tsv?inline=false)**<br>9.167 MiB (9.612 MB) – 459,024 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 972eb09d3cf082599c935eaa2df498ed<br>SHA1: d5d0b322beba9723ffb9117fdb1c4790df3c7511<br>SHA256: 903378f6f46ee45e894886dfca764e4422ff5ddae4b1eb2567696b5a93fa79e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.tsv?inline=false)**<br>8.145 MiB (8.540 MB) – 123,888 rows – 224 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a449ea932b56ad8d130751d86296e17b<br>SHA1: e6d8df8edf70d149d8aeab6a7d3787a6eb90a52f<br>SHA256: a3543e08c12bbe4f2bf19a56bb5fd47baec9e2f5a9b3c019cc05208070aa0c78</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2026-10-07 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.tsv?inline=false)**<br>12.25 MiB (12.85 MB) – 613,400 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b9d6eacf55519500120c2538d2d40340<br>SHA1: 065f35ee2ff873f5e946c5ee32008a20684576b3<br>SHA256: 988c0467160fb4dc8d416b6ba1e5e46e954f6b1879ef7d6aebe790f2c03cae39</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.tsv?inline=false)**<br>68.95 MiB (72.30 MB) – 1,047,790 rows – 248 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b8229bb0e8b5203fca7a5697b67b9a90<br>SHA1: 3dda17b71ca19a14d5bb082287ded5782379538e<br>SHA256: fc23da1a5b79494512e4385092b3d7f2718f7b488453ea2bfe83f1f7fe0887a4</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.tsv?inline=false)**<br>7.229 MiB (7.580 MB) – 362,108 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 92dd1596197772bc7e5180c35bb7dffa<br>SHA1: e367ef2064c0c12041546a5d3ef137d9031a12ce<br>SHA256: defffa3d8a374d07ad385392431a0e20b416f182103de80384ff0506108c36cf</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.tsv?inline=false)**<br>22.95 MiB (24.06 MB) – 348,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41ba48a29d7b2cf09eb2bd7cbe97bc91<br>SHA1: 037fe7c0ad8d8c735107bcc10ed1bc2789811d11<br>SHA256: 9aa79d833336042f971645189d548d6987a76fcf56481cd36a1bc93112eae9b4</pre></details></small> |
| | | Full Location | Monthly<br>2026-10-01 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.tsv?inline=false)**<br>206.7 MiB (216.7 MB) – 3,620,420 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: dafce67d077f33b29b4ed338bf706905<br>SHA1: 775ec42a124043a9aca04895847dece2ec721392<br>SHA256: f480d10e41bff6914fd7e76f9266d934b24d96c07533f35d10e4da9d12ae44a1</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.tsv?inline=false)**<br>428.8 MiB (449.7 MB) – 4,166,426 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 57afc1fff84ae28415fd717bc57b0e0c<br>SHA1: 909cd98200266011f4f2b467440631251d395d83<br>SHA256: eacd7966858d7f911e5de27efe136d26f3e91123ae4564bb06bd3ef555ea61fc</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Bimonthly<br>IPv4: 2026-09-30<br>IPv6: 2026-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.tsv?inline=false)**<br>5.778 MiB (6.059 MB) – 289,240 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 037cbe9e49d48b0386b4034c7048c166<br>SHA1: 8c73a34d6c47e79b0badefc8537eed6ecf22a1ff<br>SHA256: ee638c1c30f847a38cdca18fb3e6e1a2eb2df7ad320e6337d67810c3bab16fb9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.tsv?inline=false)**<br>22.89 MiB (24.00 MB) – 347,830 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4516b087eb6d889360de69e0e36656c<br>SHA1: a1976e56a08064be5a24f8e5c28ffb07262b4716<br>SHA256: 4e0d0b9bdcd967472b7f36cf1465613f3e2211b91a422044355cac7646b8c6b2</pre></details></small> |
| | | Full Location | Bimonthly<br>IPv4: 2026-09-30<br>IPv6: 2026-09-30 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.tsv?inline=false)**<br>171.0 MiB (179.3 MB) – 2,956,846 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a313f9fc27ba37b673b099489446886a<br>SHA1: ece362877a757aed6d6ccdad1bf2fbcb4031e9f6<br>SHA256: d7ef0d3ca1e2b8198a0e007e322d5c964611e1ed6f900d9d2edeffda292f2aba</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.tsv?inline=false)**<br>304.3 MiB (319.1 MB) – 2,947,358 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ef9a15cb810aba175baeb46886eec39<br>SHA1: a8a32cdd1c882bab942deeb72f2c8da534c8bfdb<br>SHA256: da31230883dbafd4f2ec3e54d86964a6ec028cfbcf767d5e30d1552eff280d33</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2026-10-06<br>IPv6: 2026-10-06 | ⬇️ **[ipv4.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.tsv?inline=false)**<br>11.23 MiB (11.77 MB) – 562,267 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cc5b78325181fadfe6bc9426f2b2e4cb<br>SHA1: 7fbbc5b5f09ef25ac04a6b9a09f68d42115a6a4e<br>SHA256: eb54001b511f5d16fb346b900966545e43bb9a96e23bad6f50f8e0ba427e74e9</pre></details></small> | ⬇️ **[ipv6.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.tsv?inline=false)**<br>33.02 MiB (34.62 MB) – 501,738 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cacee1c1f295bf5bdb993b238635d1e8<br>SHA1: 7d5ccbdf327ec73ccbec1fbdb109d5ebcc2b3d75<br>SHA256: 4237c7a47ba5b6ba2e62d2e5ae40c906d0fbb550e35d9298c3074c7d90c6fe11</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2026-10-06<br>IPv6: 2026-10-06 | ⬇️ **[ipv4-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.tsv?inline=false)**<br>187.7 MiB (196.9 MB) – 3,659,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27e831b743dd798f5c8ec06ef0a1c411<br>SHA1: cb1372ea36374060d32e4e16e219a38cf7edf15c<br>SHA256: 6e6609239732a3b910bfaa9a6ca0874b5255a9fb7902a8820cad94c7ad624509</pre></details></small>⬇️ **[ipv4-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.tsv?inline=false)**<br>196.4 MiB (205.9 MB) – 3,659,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95d2a0a49ee27a2bc2adf198e2726750<br>SHA1: a043106dcda1f1c5476802c581c421afd03222d0<br>SHA256: 179fc5c3cc4706deb91292074bacbf26db0a72910aee13fa18bd5ae2496efb74</pre></details></small>⬇️ **[ipv4-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.tsv?inline=false)**<br>186.8 MiB (195.9 MB) – 3,659,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a6dcce093bdd44061c5109b8bc526c09<br>SHA1: 8e1b37b0b6a9cafe046cf1c33b7c68ac025f8a17<br>SHA256: 2cfa0784eddadff590586ea47c46c40f4e9a858059fa0495fea0ef1c3151bc54</pre></details></small>⬇️ **[ipv4-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.tsv?inline=false)**<br>188.4 MiB (197.5 MB) – 3,659,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2b47814ee03cd7cf1f1db78674d05c76<br>SHA1: 565d9d1e0e62fa7f117cf4e7219360b917d6d269<br>SHA256: 6731d6e7f9aaf2cb2db5d67aabc2b223b84aa42724ac97857b2b69c7d56f9665</pre></details></small>⬇️ **[ipv4-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.tsv?inline=false)**<br>237.4 MiB (248.9 MB) – 3,659,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa64ba847fb76344b88d9beb8250ae65<br>SHA1: 2303e71f868c4827eb025e663f432c98d2c2a739<br>SHA256: 2767ce9398fe405e4898d32897ea9b0586eac3dd2a2cb1a6482d10b8b5b9329f</pre></details></small>⬇️ **[ipv4-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.tsv?inline=false)**<br>186.3 MiB (195.3 MB) – 3,659,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ec91f3901270be41ae7f47ec715433a<br>SHA1: 2d0f64c02f1c558f658a5d281a505667beae2837<br>SHA256: 164d5e552bb50f0239aa60b063bd05d11b8f21f42db6d536aa37bb8c44c3a3c8</pre></details></small>⬇️ **[ipv4-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.tsv?inline=false)**<br>234.9 MiB (246.3 MB) – 3,659,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 50b923ee00260b755e31bfaa9d12c2bf<br>SHA1: d4f0c620875a4124fc2643ddb277cebc6f3406b6<br>SHA256: a46a09f6747e6474d3f1ad2ef4bf89ea3a9a140744d68f68cb8a0300921b9d45</pre></details></small>⬇️ **[ipv4-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.tsv?inline=false)**<br>192.0 MiB (201.3 MB) – 3,659,784 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 27e38728bcaa76e31f4b2e0de804eb00<br>SHA1: 4b0e3e6299f6ba0d4ddaccf9cc45bc3391fd80dd<br>SHA256: cc7d3edf2a58db90b761be75b1e3af7bd5e74f9353d9a323d482ba22270576be</pre></details></small> | ⬇️ **[ipv6-de.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.tsv?inline=false)**<br>198.5 MiB (208.1 MB) – 2,079,437 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9aebe115602c462c71c2025ae5eb9b93<br>SHA1: 1f8680234ad2aa24f8189864021e01fb6f9a32bd<br>SHA256: 58c1c7a159b34cd2cc369336558aa7070052351520e50eb302c9b0c50f4d4502</pre></details></small>⬇️ **[ipv6-en.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.tsv?inline=false)**<br>201.8 MiB (211.6 MB) – 2,079,437 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d218c2124e4b2e8d9a204a6e33232fe<br>SHA1: c73dd1eb8155fe4d202599819261d7c88441d0ca<br>SHA256: ffa80cb340968e0a92026106d08c297b7a80563a35a356850f3d60f278436f55</pre></details></small>⬇️ **[ipv6-es.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.tsv?inline=false)**<br>195.9 MiB (205.4 MB) – 2,079,437 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 03325001add341ae3db2eaa143222d8e<br>SHA1: a3a9b425a8fcc721170285b70b409c7819dd6829<br>SHA256: 49f95f4a2e03dba7e29370ef3fee92be0aef2f0fdb9e05273eaa22ef8030f747</pre></details></small>⬇️ **[ipv6-fr.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.tsv?inline=false)**<br>196.3 MiB (205.9 MB) – 2,079,437 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a4151f940c26975a06997563c8c6fb38<br>SHA1: 25999a7806cff2bb9a3634628169149d66f6b023<br>SHA256: a505f9acfd49df591242ac6546a1654c6603384a2ee090abd40999bb4f26ef25</pre></details></small>⬇️ **[ipv6-ja.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.tsv?inline=false)**<br>218.4 MiB (229.0 MB) – 2,079,437 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05a6ff73bba405145330c181d7e259a0<br>SHA1: f66fb28756023702b9acffbb9efe9fe8007345da<br>SHA256: 579072413ceea04b60b84ede0040c463955fa6ae9e4ba8ab4d167a18473381bd</pre></details></small>⬇️ **[ipv6-pt-BR.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.tsv?inline=false)**<br>195.8 MiB (205.3 MB) – 2,079,437 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 21af2dfb6927de00f102ffa4ce4de07b<br>SHA1: ebb909259bc2515e22fd5c41a9b126f21302e854<br>SHA256: 7ef8c27c9646f87fbcd1777c57769bc88cacd1a8a171d651ec19d2ba62bc034e</pre></details></small>⬇️ **[ipv6-ru.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.tsv?inline=false)**<br>220.8 MiB (231.5 MB) – 2,079,437 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cae7ee3e7b39bb834809d86ecfa8682d<br>SHA1: 82cd3067ddfb552a2b4be25e35ece9ca29ac2552<br>SHA256: a963d8a2dd01d1edf2222b33774ad80b3c0dd1757849b072341093f9ccc1b5c9</pre></details></small>⬇️ **[ipv6-zh-CN.tsv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.tsv?inline=false)**<br>198.8 MiB (208.5 MB) – 2,079,437 rows – 251 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 363297724639376e3c99139e3622f737<br>SHA1: 4f53f81e11e372bd58ca14a591fda4bbc7dc46d3<br>SHA256: 6ae5041784fa16360e6edc4f533d1705e4d2e60fa17e046fff53b8fd1959666e</pre></details></small> |


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
