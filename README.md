[![CI](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml/badge.svg)](https://github.com/tdulcet/ip-geolocation-dbs/actions/workflows/ci.yml)
[![pipeline status](https://gitlab.com/tdulcet/ip-geolocation-dbs/badges/main/pipeline.svg)](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/commits/main)

# IP Geolocation Databases

IPv4 and IPv6 Geolocation databases that automatically update daily.

Copyright © 2021 Teal Dulcet

Preprocessed free [IPv4](https://en.wikipedia.org/wiki/IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6) [Geolocation](https://en.wikipedia.org/wiki/Internet_geolocation) databases in [CSV format](https://en.wikipedia.org/wiki/Comma-separated_values) that are automatically updated daily. Includes both country only and full location (state/providence/region and city) databases. Based on the [ip-location-db](https://github.com/sapics/ip-location-db) repository, whose update scripts were [not open source](https://github.com/sapics/ip-location-db/issues/7). The scripts used by this repository are 100% open source.

All databases are provided uncompressed and in a consistent CSV format with minimal quoting. Localized versions are available. The databases are designed so that applications can directly download them, without developers needing to release an entire software update. This allows users to enjoy much more frequent updates and thus more accurate geolocation information.

❤️ Please visit [tealdulcet.com](https://www.tealdulcet.com/) to support this project and my other software development.

The databases are hosted [on GitLab](https://gitlab.com/tdulcet/ip-geolocation-dbs) because it has no maximum file size, just a [5 GiB repository size limit](https://en.wikipedia.org/w/index.php?title=GitLab&oldid=1104375442#Repository_size_limits) (previously 10 GiB). In contrast, GitHub has a [100 MiB file size limit](https://docs.github.com/en/github/managing-large-files/working-with-large-files/conditions-for-large-files). Commits older than two weeks (previously one month) are automatically squashed to keep the repository size under that limit. Please see the [CHANGELOG](CHANGELOG.md) for the full history. The databases are now updated [on GitHub](https://github.com/tdulcet/ip-geolocation-dbs) as it has no limit for CI minutes for public repositories. In contrast, GitLab has a [400 CI minutes/month limit](https://about.gitlab.com/blog/2020/09/01/ci-minutes-update-free-users/).

## Database comparison
Scroll right to see all the files »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-05-13<br>IPv6: 2023-05-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>6.136MiB (6.435MB) – 261,547 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4c4ff5e8629f79ffd206ce6f5719b15c<br>SHA1: 226ff076be47ee93de0c3104501ef42cbfac3827<br>SHA256: 87d7a98ef38fa83a7948e67dab81b2bd540dfa831616b6fdf6b1604bc7ec84c5</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.491MiB (6.806MB) – 84,024 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c76b60e4d58a6a9435ccc2a2e3975c08<br>SHA1: b3c49eeb013d07fe9b8c55fc414281a07f1e3dbc<br>SHA256: b55a21fe07cc80853a84d41ea6b23a60d0c3ee940267c3443a3210533b4ebdd0</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-05-13<br>IPv6: 2023-05-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.452MiB (9.911MB) – 401,500 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aeceb5b1eae0d6b415c68e67b80f7008<br>SHA1: c7a29df8a7371325ad11d25fcc3ca4166524b63f<br>SHA256: 8bb2dfbe940d2a061e4e8eda88b0314e6dd0f258b71329c1442496791f5d5874</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.542MiB (7.908MB) – 97,729 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0f0d986f6bd669b74c95c45c02dd1fc5<br>SHA1: bbd11327eac51c4ee5fa7ae4fd776592faf634ab<br>SHA256: f08fc8b1351f6ce779bda4176be2c472728c1ab70faa6aeffbb7cecf0dfa598e</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-05-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>13.68MiB (14.34MB) – 583,653 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3fe970f854c82ef5568aa78dc45cb8c7<br>SHA1: eb343a08f3ce153407c8ff8512f606237d48bf77<br>SHA256: 0634f14e78318d0599605c349f1895bdd784f74f30e16162ef9d3579cfb29fc8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>28.19MiB (29.56MB) – 364,967 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d4096eaa763becbd19bd1c7cd00e0f65<br>SHA1: c1c9d12c56573e66753786482d33fb4f6a27cf2a<br>SHA256: 0fbf81aafc64aea128e3b51b42293b41c6be217394bcb8463b078a3cdfe34604</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.198MiB (7.547MB) – 308,140 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 00b451f6412173581a7ba389f444f7b8<br>SHA1: 3581ae37ad536ccfc344035fac8da366e6f2a1c3<br>SHA256: 2632d03fe402810c0a5cd21cb01657e4bce6686f9a35a911a634e00376fe4fc8</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.40MiB (26.64MB) – 328,845 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6bb8a68614ae30eed99e534875572642<br>SHA1: 0ee22a19afac3f9a7cbd864af67674fe9cfc6161<br>SHA256: 7d06dc68c40737d45ad6dc84897a8b7371ad05211dc7716db73e16c197236656</pre></details></small> |
| | | Full Location | Monthly<br>2023-05-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>194.0MiB (203.4MB) – 3,206,976 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4ab320aa3a48e3e999f3451fbc5a2da8<br>SHA1: 0edbe11a0f197414c336d93dce71b581d19cd274<br>SHA256: e618d8745b11f6aff0dcb8f824c7f141c7fe734243d064f5f1fd7a093e46c571</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>365.9MiB (383.7MB) – 3,189,651 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c56df0a8c49cfc4fafc1dd0e0ea9177e<br>SHA1: 5e57dbd6ea1ad42ff4e411c9606c8f23cb91e70c<br>SHA256: 78e7ce4abf723db571f358a92321ca5b197405f36485132b7deb8c48d31a8d5b</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-05-13<br>IPv6: 2023-05-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.555MiB (5.825MB) – 236,860 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed3a236afb3c81be58fd9e618311f040<br>SHA1: c2f909455631207019aaab2b2e46e900ebf570dc<br>SHA256: e9f4b3ba35664fef476b681b4bf974f40a7c2605e7528a86ad8bd7ec533ad95b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>27.56MiB (28.90MB) – 491,350 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 24b4cca038e3d4dcc0f42da6244a3a35<br>SHA1: 2621cb133d2002e631b0adbef75d4ea6e931756d<br>SHA256: cc4498b24a37bbe633f6502d077cf044fd12484833daf07542118c9c7c386bc1</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-05-13<br>IPv6: 2023-05-13 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>192.8MiB (202.2MB) – 3,146,282 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88c13dfb1a052516749e7ea3a9487650<br>SHA1: 2e306a30fccb8fc193e5dd6bca9c2dc9b66b74eb<br>SHA256: eb792a298ee49d197c826b29bf481ad1c08529aa3138b1265dc37736edb20adb</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.6MiB (400.1MB) – 4,518,262 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7fdf49f6825c8d2c6839dbb6a75d33b8<br>SHA1: b3e158802b17935c7869bba17ff348eb8c749c91<br>SHA256: 5b247134a6e2438ebad87181e14b376f714b23fa9c8ca69d358366ad0778806a</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-05-11<br>IPv6: 2023-05-11 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.694MiB (10.16MB) – 413,287 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ae5c7c9e8c923f87e7ab167c006d79b<br>SHA1: 0575f3f384c7ec94ffd175d574a99a9718299c7c<br>SHA256: 3211bbeea560bbc502e38391fa3a078762ab73e5c595056e0c8dbfc7294cb9c3</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.20MiB (22.23MB) – 274,445 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fc037c7b34fd886781e84ef3810d542f<br>SHA1: da1a32ac1359ea6cc2de3980a7c7a6761dcfee38<br>SHA256: e49b2078bb9024b26ef8b1f22d0a4bf8312fef6482583b6f422717ebf87957d9</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-05-11<br>IPv6: 2023-05-11 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>193.2MiB (202.5MB) – 3,842,182 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: af194026326db0ad2b1fca7720b644fa<br>SHA1: 70dd16569249d76974ceb899433f8a764c51348e<br>SHA256: 3f67241dd2c4829b2cbbee2cc3c22268ac93af4f0bcdf9684b6ce31130861918</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>226.4MiB (237.4MB) – 3,842,182 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2130fc248333cc0551f0149939db247d<br>SHA1: 2e8046279f4804d561237473170ff7906f71b58c<br>SHA256: e4de50d48975cf93cb19dc0f653e9ae856b81216603ff02c0b0cd8a763e1c2bb</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>199.9MiB (209.6MB) – 3,842,182 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 747c997fbd37374d433e5f5f411dc382<br>SHA1: c75e70b3e23110a93c0491ccd1133abf4892bf55<br>SHA256: 05c554e56ab7ac60dd5d84f72e8e5e76344a74819c3b1bd6d1913c92a24df4ea</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>207.2MiB (217.3MB) – 3,842,182 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: aa8d1678f8fb398f4e59516fdbb9fb5e<br>SHA1: ba6d0994225f99e31429c7f27c040327388ea85a<br>SHA256: 11148f8a2a8f3ca01fa51c39dc6a5698da2e2a5d1931e8332617de970ad01760</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>243.2MiB (255.0MB) – 3,842,182 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6448b7a684924320b813352cd797604a<br>SHA1: 18c1d71e554ab00f78d235c79cd4e156e910d787<br>SHA256: 8ed1c2bd37b0e16c04088e15e53ee36c0bb93bbe1c5676858262317e4024b0b6</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>194.5MiB (204.0MB) – 3,842,182 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d657d0d3550bb57ffe3ddfbcbd0a9486<br>SHA1: d44d3bdacea33ec9a3dfb040f183b057cca5d8c6<br>SHA256: 6430967e96214ab9df40edcbe1c4ebcae84b495dc2527848e4f3d53247a4124f</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>243.9MiB (255.8MB) – 3,842,182 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9cdbdb4bf7d2994bba99485ca0b99259<br>SHA1: 419dcb6f391cbc0e3840226053828cb62e278e86<br>SHA256: e59b2ea685bec38ac6597b710e3e4cd589ad653badef0e1652231bddacf0ff4e</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>206.9MiB (217.0MB) – 3,842,182 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3f74da38b9211ec6ed3addda99bbf2e5<br>SHA1: fb1a3d1950f8c118b6d00521eb376097aad35673<br>SHA256: 8a822475e1843fc0664809ccd77172951d3b4c0447fb81f483f815f118f74684</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>128.8MiB (135.1MB) – 1,283,698 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 455889fefc2232217a2c242fe1c780d8<br>SHA1: 75a6c0ee3483cbf267172aefd5578bd60ccb91c6<br>SHA256: a7ab104a370b0f122df5e783ff61a739b0616fc492ce33250a8fdf0797dbb798</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>137.0MiB (143.6MB) – 1,283,698 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9171e50c59487caa821b86eeef775277<br>SHA1: 8498a2261ecc5514c26c240a39f3c0cde04cc312<br>SHA256: 6671027fa6c8802f45627b5af1485a3e4e87795f265a36b710763e07680c5ed9</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.0MiB (137.4MB) – 1,283,698 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c4f51f2e3ace8f0a289bb325d46ad0f1<br>SHA1: 0b31c2033a30fcb00b6e9e7d545cb1645c097214<br>SHA256: 083fe144d147c94cb3c9064257a38aa199f82a9cc77f4294734aa8f62a75b437</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>132.9MiB (139.4MB) – 1,283,698 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 855d9f071291262f9662e20fa74eb302<br>SHA1: 80de50ea55a7c878e64687b315df55460738deda<br>SHA256: 0620e65e05481a2fac73a37ed75276d374fd924020eecea36f399261a743f1d0</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>140.7MiB (147.5MB) – 1,283,698 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4842f93e26f73c6a0b6302f7918af6f7<br>SHA1: c9f3110a16976e98d25dc48015a900b4470c883f<br>SHA256: b015e6fd91301e244ef8ea6bedf894b9bfef1e8c70bbc306b4a8273ea04fb424</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>130.1MiB (136.4MB) – 1,283,698 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e7f0a31583710de179e6cc74666ee54a<br>SHA1: b674f3396920505aaf4bfec0abdf4723f3099e12<br>SHA256: b7c9976fa623d428d17a72d078637f408ed7153c5713cac7eb2fba42b131b18f</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>141.3MiB (148.2MB) – 1,283,698 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7875fd6c7775da69a66192cb66bc7c83<br>SHA1: 2c70c4f3697517bc26445327e8479c8a11f40c99<br>SHA256: e1fde2d14cfda9d4f90b2a0b0902a8239e9a1afdac03cb6ede5e293ae4ab2e92</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>133.2MiB (139.6MB) – 1,283,698 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b2956785dbda4c7c788461d7bdf070fd<br>SHA1: 6c5acfb5ad07176eee769ead4dfa1e622cf5a14b<br>SHA256: 5771dfd7f6c0165d731a776672d9c5282d16ce6ff79f251a490075ccd8ee533f</pre></details></small> |


## Databases

### GeoFeed + WHOIS + ASN database
Uses the [ip-location-db GeoFeed + Whois + ASN](https://github.com/sapics/ip-location-db#asn-database-update-daily) database. It is created by merging the five [Regional Internet Registries](https://en.wikipedia.org/wiki/Regional_Internet_registry) (RIRs) ([AFRINIC](https://afrinic.net), [APNIC](https://www.apnic.net), [ARIN](https://www.arin.net), [LACNIC](https://www.lacnic.net), [RIPE NCC](https://www.ripe.net)) IP-ASN, WHOIS and [OpenGeoFeed](https://opengeofeed.org/) databases. Licensed [Public Domain](https://creativecommons.org/publicdomain/zero/1.0/deed) (CC0 1.0).

##### CSV format
`ip_range_start,ip_range_end,country_code`

### iptoasn.com database
Uses the [iptoasn.com](https://iptoasn.com/) database. Licensed [Public Domain Dedication](https://opendatacommons.org/licenses/pddl/1-0/) (PDDL v1.0). If you need hourly updates, you can use the source databases which are in [TSV](https://en.wikipedia.org/wiki/Tab-separated_values) format with [gzip](https://en.wikipedia.org/wiki/Gzip) compression.

##### CSV format
`ip_range_start,ip_range_end,country_code`

### IPinfo.io database
Uses the [IPinfo.io](https://ipinfo.io/products/free-ip-database) database. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IPinfo:
```html
<p>IP address data powered by <a href="https://ipinfo.io">IPinfo</a></p>
```

##### CSV format
`ip_range_start,ip_range_end,country_code`

### DB-IP Lite databases
Uses the [DB-IP Lite](https://db-ip.com/db/lite.php) databases. Licensed [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), so users must attribute it to DB-IP:
```html
<a href='https://db-ip.com/'>IP Geolocation by DB-IP</a>
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

### GeoLite2 databases
Uses the [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) databases. Licensed under the [GeoLite2 end-user license agreement](https://www.maxmind.com/en/geolite2/eula) (EULA), similar to the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to MaxMind:
```html
This product includes GeoLite2 data created by MaxMind, available from
<a href="https://www.maxmind.com">https://www.maxmind.com</a>.
```
Localized versions of the Full location databases are available. See the filenames in the table above for the supported locales.

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence_2,state/providence_1,city,latitude,longitude`

Note that `country_code`, `state/providence_2`, `state/providence_1` and `city` are blank for some rows.

### IP2Location LITE databases
Uses the [IP2Location LITE](https://lite.ip2location.com/ip2location-lite) databases. Licensed [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0), so users must attribute it to IP2Location:
```html
This site or product includes IP2Location LITE data available from <a href="https://lite.ip2location.com">https://lite.ip2location.com</a>.
```

##### Country CSV format
`ip_range_start,ip_range_end,country_code`

##### Full location CSV format
`ip_range_start,ip_range_end,country_code,state/providence,city,latitude,longitude`

Note that `state/providence` and `city` are blank for some rows.

## CSV format

See above for the specific format of each database.

### IP address ranges
`ip_range_start` and `ip_range_end` is an IP address range.
- IPv4: `16777216,16777471,AU` means that the IP addresses between `1.0.0.0` and `1.0.0.255` inclusive are in Australia 🇦🇺 (`AU` country code). `16777216` is the decimal format of the IP address `1.0.0.0`. The numbers are 32-bit unsigned integers.
- IPv6: `42540528726795050063891204319802818560,42540528806023212578155541913346768895,JP` means that the IP addresses between `2001:200::` and `2001:200:ffff:ffff:ffff:ffff:ffff:ffff` inclusive are in Japan 🇯🇵 (`JP` country code). `42540528726795050063891204319802818560` is the decimal format of the IP address `2001:200::`. The numbers are 128-bit unsigned integers.

### Country code
`country_code` is the two-letter code defined in [ISO 3166-1 alpha-2](https://wikipedia.org/wiki/ISO_3166-1_alpha-2).

## Contributing

Merge requests welcome! Ideas for contributions:

* Improve the performance of the update scripts.
* Reduce the size of the databases.
	* Convert the databases to [TSV format](https://en.wikipedia.org/wiki/Tab-separated_values) to eliminate quoting.
	* Store the IP addresses in hex format.
* Provide localized versions of the IP2Location databases using their separate [Region Multilingual](https://www.ip2location.com/free/region-multilingual) and [City Multilingual](https://www.ip2location.com/free/city-multilingual) Databases.
* Add more databases.
