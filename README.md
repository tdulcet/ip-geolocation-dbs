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
Click link to view the [full table](README.md#database-comparison) with all the files or scroll right »

| Database | License | Type | Updated | Download IPv4 | Download IPv6 |
| --- | --- | --- | --- | --- | --- |
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-08-20<br>IPv6: 2023-08-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.635MiB (5.909MB) – 240,071 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fa84ae85dd3c7cae68e568b8d15787f5<br>SHA1: f79e675abaf182b0dc2e18131e188927304b7b0b<br>SHA256: a534762ec2c0b30d8f4a5fcf62cd262b266f7315e0a22d51c004411adb690871</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.632MiB (6.954MB) – 85,854 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6da3644375c6d57e0f06248fe37d5246<br>SHA1: 9649318cc4e0ba5468812da41f3a130b8e23bb6c<br>SHA256: e430500abb43ac1df5f4d1d7ef60de67b2a5e55e19d4605908aaf8ff1702ccd9</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-08-20<br>IPv6: 2023-08-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.545MiB (10.01MB) – 405,438 rows – 239 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6c0bf76a9eab3e91052cb6e106e650cc<br>SHA1: 16aee6d2f8db15b437cb625d63fae63333c63d5b<br>SHA256: 5f35523d7f96c89c2e737c5a5c60c7b038c0fe32869dbe3089ce2a1cd11c3b4d</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.740MiB (8.116MB) – 100,294 rows – 223 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a9092fe1579b5206a3543b63b58b7750<br>SHA1: 604eafd238ee86df64bddd6e8e1a4d25c19dff33<br>SHA256: e41f82eeec5a3e6fecf9728e1ca2af0540da828f475b6921cd941ab36ad8264e</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-08-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>15.21MiB (15.95MB) – 650,161 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 88db65992ad9e84d4bc89ba258a4a251<br>SHA1: 0a190709d0b8c36623a616d89ee66c5e60ce421b<br>SHA256: d8c6fb326dd3585a7270f4dfaacd2f4832cb1524d372a5bcdc04fdf70444aa86</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>33.05MiB (34.66MB) – 427,868 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3ee83e87f03de4e9116403b4f0a33e07<br>SHA1: 74f5dc04f2cdde527b24913bb9f04de6e4a6afc4<br>SHA256: 1bbf66bb86b8163a81ce2539826d1d4f69c7d0c5e9e6f64ce48f7c6add0dc506</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.354MiB (7.711MB) – 314,876 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ca76b98b742610e14368fd012848c6e<br>SHA1: 5a246f7aa51c885d4dc479284c99db5643e6770f<br>SHA256: e98c856388c6a61108e688ede0fd4bb7b818be019a620f09abfa12f09f9d4af0</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>26.39MiB (27.67MB) – 341,571 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 956b52205bafb278c0610cfec5e8e6f3<br>SHA1: 6e3ecda1bff92e53f23bf2ef3885149bc6312eff<br>SHA256: 0edd51b1478170d678f6905901a1c6a3ac7486a66f8672ee06079354a8c40436</pre></details></small> |
| | | Full Location | Monthly<br>2023-08-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.0MiB (201.3MB) – 3,170,913 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e50f1d7e16995e4854b0f105bd6c8b2b<br>SHA1: 1dcbe021497af64af841ae21163751821541e06e<br>SHA256: fa28f36a198a238e8f503e858e7561b54fb9c909d90276f58d195afea9f75250</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>296.8MiB (311.2MB) – 2,579,615 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bac2a6b630483711e47113caedf6461c<br>SHA1: 234b956c8061d27a07de03503b53aafee1dae740<br>SHA256: 67b384e2ddde5241f818748e689acf0bf9c436ed15bc23bd12c76eb991bd4fa3</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-08-20<br>IPv6: 2023-08-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.464MiB (5.730MB) – 232,983 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a108e1e4776e169b7a8ab8c17d0196c9<br>SHA1: ac50374d43d4f2eacb0dc0e8091d12198db0f810<br>SHA256: ed29e2492323a596f3447c1210a21bf79252743adee0ecde01ab65c831e402ce</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>18.48MiB (19.38MB) – 239,226 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5ee23fdc5ffd739f265aa51786817ac0<br>SHA1: 01741ad8bd3bd06bac109e33191a94e63160c0ba<br>SHA256: 3a9b3c3fbb2df2cea2f6861cc88f201703c4a7a17623ffc4a31f95236c941a21</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-08-20<br>IPv6: 2023-08-20 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>185.5MiB (194.5MB) – 3,026,941 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b3ad101145ae7532282cdb5d782ecb2e<br>SHA1: fdf6175b442adb8b67cf234f48e8b8c42b217e5d<br>SHA256: 8f189280a0da9ee9e8bf57768e2a567d7cb6dc73308f25ee42f535a6434d8849</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>157.4MiB (165.0MB) – 1,372,805 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 53d4e17c83be387c60dbc224cabd3063<br>SHA1: 29e2a05c7ffe924332b8f1db422ac45bf113c47f<br>SHA256: ad56e70598738e9c420c33d6ed68895c6e5b0c623ae1b3a191bf2ec9b10e9465</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-08-18<br>IPv6: 2023-08-18 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>10.19MiB (10.68MB) – 434,671 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6f841e4c06ba878711735e9fdd8eabe5<br>SHA1: 526163fd4767cdee7308ed956a73f02860b41f4a<br>SHA256: e4d656a99ce363c680a641f37938ad8c933fdb3ff684f21484327d873aab02f5</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.35MiB (23.44MB) – 289,373 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df543d8dfa91443505710a89774e739e<br>SHA1: 9020276b635647c36ead8c3bcda398886c22c809<br>SHA256: 1c87e3d3dd0691ce369ff0de3495b83988d58a1635d8a7d3ab1447a5099cc3a5</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-08-18<br>IPv6: 2023-08-18 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.7MiB (200.0MB) – 3,804,503 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6e5d5b9f24a0dd114ca3faa84f88c52f<br>SHA1: 9ca05c2784d8c8fc1ce744589347f80e32079363<br>SHA256: 159afcea8e12c12eb1e298dbb1a58acc60e502ff0f03e194e20c01a1774e714e</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>223.1MiB (234.0MB) – 3,804,503 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e94e8dff6f87f5e9df5c973771634ffe<br>SHA1: 276287e219bff18465eec1f8ac5ce7482d724d62<br>SHA256: 3f236825bfce15c43eaca31a7e429653274faea48145a3ea1a05768781cad234</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.7MiB (207.3MB) – 3,804,503 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 453d9a040ccef7fe309e5185e1d88041<br>SHA1: 5f30762364c6f357cb1110e90ee07f20ae5c0001<br>SHA256: b5059116a2bbdaffbbf647a610539784fbf6d7ccf533b75b7127cdab311cf519</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>204.2MiB (214.1MB) – 3,804,503 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cff0f1651e290c6fc49b1eea77b72990<br>SHA1: 0636013f641d2f2f3b35acd72e1e0aa15db75714<br>SHA256: bb480dc3261a9ae18186e60001c5b5b0af21d5d0f7799b8da36d3759a190c98f</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>240.1MiB (251.7MB) – 3,804,503 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9ceaa925e9ad2a990c059ba4889d1baf<br>SHA1: e28ecdbdd9f6de3420c800f4c45051125be644d2<br>SHA256: df543b3a2dabaccdc48d1d15caf15041861722939ba7dda18a651f5dfcfc9f2c</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>192.1MiB (201.4MB) – 3,804,503 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 035619787fcf0d2d996ee07b6e5b0155<br>SHA1: 7cfc200b4bf9779ddd7301baee79e4a3147668ae<br>SHA256: 5e005badccdcf1985181161ac900d89fd013633ffdb91b4daf1b7ade1bff6bf1</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>239.9MiB (251.6MB) – 3,804,503 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 591702a82aacb64d97ece31eaa55af41<br>SHA1: 7dd5cf4f9c368febbcc9df2c638c8ada5befb7f5<br>SHA256: fa222a8d3428d5b8e5d12571e3f7927fe3e4326c62715690a0b98d91350089f8</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>204.5MiB (214.4MB) – 3,804,503 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c0e7c323bfeb0f6f5d54461665f3f417<br>SHA1: d49bee8ee6490e2f046fa6fcd004b04610af8752<br>SHA256: ad5bd05f76428eaaa91bf9b44a97a40f5ee335ecb833905952fd249ca35fc610</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>129.1MiB (135.4MB) – 1,287,888 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d3c502caa04596be412860b48286b00<br>SHA1: 5a2f5e2dec978fb159b87f0d96233a0ad3e274e7<br>SHA256: 8f9373743a4ca40d6a4baaf72ef8b29f626f2a47a9cb1a22eaab839a9f90c13c</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>137.4MiB (144.1MB) – 1,287,888 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bf256bccb98de248af553e8be491f8cf<br>SHA1: 3cee1e1ebc8c3763e24db0b30b6acfbab6eaf2f4<br>SHA256: 47d5a9ead7b586a942da50ac07f23945e22aaabef28bd9aa7a2194785f7050ae</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>131.6MiB (138.0MB) – 1,287,888 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41485950fabf091a53172a166acf3a5f<br>SHA1: fa7717ad785b1bd7283ea2db525e1db524bfa23c<br>SHA256: 91fe648eba11a0090d62afcdac0e158ac7320138792766a406d1d01caa193908</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>133.4MiB (139.8MB) – 1,287,888 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: bd1a67131db6cebd94d2ce1d12a2fcb5<br>SHA1: efc2ecdd17da0261b37e02519729d51583f64236<br>SHA256: 55dd318d032d922059936b5d675a647306e15610cb08327b0e38159d65ac8f8f</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>141.2MiB (148.1MB) – 1,287,888 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 67d6df5ca812e0d2cd2c27a7847c0838<br>SHA1: df279c2ccc4b691c740692294543f39846a5ecdd<br>SHA256: b821fa195c40405e0287ae5759c2aec538aee330ddeb8dc428d45dc3bdbeac75</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>130.4MiB (136.7MB) – 1,287,888 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 85bc7175d778fc946fe21af6ef159fa0<br>SHA1: 367d023d6e76dd16984e1c0e02e5fafdf7e3ae85<br>SHA256: d35b8b2d0da9776ea5566959406272f211597a5d58c83cd46e8f78e40f70b1a4</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>141.7MiB (148.5MB) – 1,287,888 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8aad104d6ec1975297635d72966aa352<br>SHA1: 001817fdfc1dc5044ce1383c9795e9c0a12384c6<br>SHA256: 80853b28c1af85a000391712860120083b741f9fece05bed2d26008dfeba8fd1</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>133.7MiB (140.2MB) – 1,287,888 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f65feff9b2902ff488846f26beef0f45<br>SHA1: 0ad67df0019d71b1063aafbb94a3d3a15e391d2e<br>SHA256: db9c35552a7dcf4b67fcef2d8b36b2bc8e65149866b72b0eeb4e10d9e0e7219e</pre></details></small> |


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
