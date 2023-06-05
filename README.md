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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-06-05<br>IPv6: 2023-06-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.858MiB (6.142MB) – 249,452 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f09e721808d6bbbd7f90011308aab55<br>SHA1: 6dd1186c1a11c809daa64dbe8c63fca1b508acef<br>SHA256: a1b8f512bf5a2e732c763759e5ac06fa55b076283b31b45c02f7a3658b41beb4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.542MiB (6.859MB) – 84,684 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95d33ebb08ba32fabcdefa596575e9a1<br>SHA1: 94484ab7670ef5d1bfc48557068243e5081fd0d5<br>SHA256: 01d4e9b8437337c3c304ae823ee1d73734ab8d3258226958c5bb63a7ab411b82</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-06-05<br>IPv6: 2023-06-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.468MiB (9.928MB) – 402,142 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 19064f7a29537315eeb8d8a4bd144cbd<br>SHA1: 76e763337952333dd401d30a685ec31288e4e57a<br>SHA256: cbda2113fab7784f8aa680cacbeb4701efb6b60af6da0a0b9138c09a45a6926e</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.618MiB (7.988MB) – 98,714 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 380ce0226602c4759b0681b5a5c689fd<br>SHA1: f6dd2ac6b9962e1bc3a4aed555ff10ea98bef641<br>SHA256: 34f5a62849b82ad55e591cc5b1b1103581a4532fb98a826b49236d722aa3f0dc</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-06-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>18.29MiB (19.18MB) – 780,311 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 119bab4878461adff1ce9776874c1680<br>SHA1: 85e663475d6be4b2669e4db9663ae077783c57f9<br>SHA256: 12232a735c31721260ba65c09ed8a6bb4574a1daa3e39b4590a651d6bc0c11c7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>23.47MiB (24.61MB) – 303,801 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3333c1d1f610e06079b7754481d1795c<br>SHA1: 1310fe780837eb1cb27010e78b4ff26c13186e97<br>SHA256: 64b9214fb59d3e43f2f0db24cde9b6b69c834ed68ea33926c183d5f248960e54</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.258MiB (7.611MB) – 310,670 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea16f2b91095213f9faf4261a5404be0<br>SHA1: c745544fc460b4fd9cb1ac68204736bcf9eabf79<br>SHA256: f0ea96ff5e89f5f267e07aa2f74df623e088bcb91f1df0d02845e1c412aeea46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.86MiB (27.12MB) – 334,770 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7634f17216ca6f115cf06e4df5e44bcb<br>SHA1: 60cbd088cb95f3f19ddbebb63ee62aa7d4d5943c<br>SHA256: c3c8f61cd5d80cb8dabda6b047d66bfd6d73c7d0d9eef7427890f9825a480636</pre></details></small> |
| | | Full Location | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,190,306 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f9e88d1ad989b6a665fbfd9d3b82b2<br>SHA1: e1ce63d9dae9f45709cd662cb78d5f323b9caca9<br>SHA256: ca5be0a45d234b5f3db9fd7993ca3b95fb26381d390a4e0d3e8111f2e7922199</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>351.1MiB (368.2MB) – 3,068,912 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4471e6e2accf2b2f3c070f5cb39ed63a<br>SHA1: 158105fcee685e8e94bbff314ca8be8e235b169b<br>SHA256: 82b7025d3a47fff4700bbb503d62d17692265f78fae12837a6995bed2c31d118</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-06-05<br>IPv6: 2023-06-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.582MiB (5.853MB) – 238,084 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1341c73b679015c1849651b02f8442<br>SHA1: 68ca29c935cf40cbfd663086deea4e61d8c8dc4f<br>SHA256: 4124a3662930f11954fa549834f6208912d91c3ddb53382a0c39cfaba1a71bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.40MiB (27.69MB) – 477,002 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2db255cf92eb5224035b1230f0efcc2b<br>SHA1: 4e4c6b67a3842bcdf119210a6676113f6543fa54<br>SHA256: c4335ed7e2c56df30bddbe55d518c81bb73286caae4ae123b4969eca63c72f25</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-06-05<br>IPv6: 2023-06-05 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,120,022 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1419e77505317334ccdf478ab7daef44<br>SHA1: 1d97a0ac2b0129e4e268083a3cbc23c627acabbe<br>SHA256: 35551439abd88f4346ee7c19bd2da4093eab3273897ca4f28e5cdb1e5d078ee1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.0MiB (399.5MB) – 4,504,439 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e04f9fe903ade529e55bb6b0d36ccdb<br>SHA1: 3f03d09739691bd6ada8c4ee23de98629caf20c3<br>SHA256: 5f023916ba65784e33d23b0934799adf20ae2b5448b40b7bd34e659f96864649</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-06-02<br>IPv6: 2023-06-02 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.716MiB (10.19MB) – 414,229 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a0b76fe450e5617685cb964d192e634e<br>SHA1: 9e3b8ff4803dd1f5167d5351e8fb6396a6d987b8<br>SHA256: 668c845f759ef73296a70a78e18a958946023d55c08ff0eaa9b9fb0e1e226c3a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.15MiB (23.22MB) – 286,708 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 91f752574ce2c770b7b450896c763250<br>SHA1: b25818dd95fdecbc20fc46229040788099a5ec2a<br>SHA256: e3397d5d6c9ff898b66fe0d06296eb6bbcf309efb52c73a1afb76b461dc51b01</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-06-02<br>IPv6: 2023-06-02 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>188.6MiB (197.8MB) – 3,755,122 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c558057514e457537b7448cadbd135f8<br>SHA1: 58c990f02ef68744e4ea1d1df2773a984a074e63<br>SHA256: 0ad3a47185d0611457cbc31a5ede69a7026785778416ff388db083f6fff16944</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>220.9MiB (231.6MB) – 3,755,122 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3767cc1b5f404617095c55aa2b302475<br>SHA1: 4c1ce89ab991f16c008ac4df0ecbfb71d2ab04a4<br>SHA256: def2f2db87aedae76ac8a35e3f8ce0c4d0135648068c7a1ef40f6a3cffddb6b3</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>195.3MiB (204.8MB) – 3,755,122 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 754594cd71a712cdf52d8caf7e6de6dc<br>SHA1: 00384a57d63af6232ebd96da249ca13aaa1098ee<br>SHA256: cb48b56ebfeb560932d7b10fa15df56d45eb8ac6dab9e512fc41ecfc00649473</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>202.3MiB (212.1MB) – 3,755,122 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c1acdd4c6c08139d46d6917d3871d204<br>SHA1: 719c3411189319d6d16ac3e7cc8b6b4fa0378b01<br>SHA256: ea9cbc5e58348f0458a7a751cea9e423e8629784610b6abf0bd8889ad862a2fc</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>237.6MiB (249.1MB) – 3,755,122 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: fe3d09433cd3ee9f2be0ff4f9f5aff63<br>SHA1: b16ade8d910b95cdae54defaa95b173de6bb45bf<br>SHA256: 959d6e4d8a87cf2fe16fa81e564356a456f9bf6a82e752c3ea44132398688cc9</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>190.0MiB (199.2MB) – 3,755,122 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 969c5bcb90f9ab9bd9d5c39e89a93c6c<br>SHA1: 3ba306d59bc64edde382e2e089f0cdf942816b97<br>SHA256: c00789ee9ac9796c21ffdd53f0699998ddb4a8848ebf09bfff6072f1dca23679</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>238.0MiB (249.6MB) – 3,755,122 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7eae01b6fa90234a9d3aeb25db3b52d7<br>SHA1: 42d8b3b4b3f87f2285c08fda54213cd87c4fcab7<br>SHA256: 767119dcc2eb9b64d0484abea017c72ac5dc88db7d01e5fd629e74fca438fc07</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>202.2MiB (212.0MB) – 3,755,122 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a28a64ad6934a8285040b30c135aace8<br>SHA1: ac6f4adbc962e713b7e7da1662883e4e8d126454<br>SHA256: 8842478f1b763d8bf1a00ae6e5fe9d57bacb53f23b937cf197ba79a29c0345b4</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.4MiB (128.3MB) – 1,221,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 294c4029eb408a4b2b7ad090ba624255<br>SHA1: 81c1d1d6a671b15b74672266afad40f3d564f073<br>SHA256: a695f2763de1bd9b46522fac8c86401861451d5a9496a26566f2cabdf45d4a76</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>130.2MiB (136.5MB) – 1,221,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 34ce570eeaa4d33329e9a5221008dc56<br>SHA1: 175f8e8df851c5ee05aff67990acba0e76ed314e<br>SHA256: 9e50652354eb8b169dfd84f54cdb59243567db5f1ef1ca90bb95f56a9cd78880</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>124.5MiB (130.5MB) – 1,221,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41c9a71bf6c8dda83f6f12375b713aec<br>SHA1: d272c47209848bdd4975aabff97a04a5ae6c9ea4<br>SHA256: aaf41a3af888bd77ecb65c8200d0460aad16954b24f599b2b6c702f4b64b1753</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.4MiB (132.6MB) – 1,221,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ed64dd9e77a25bfccafcb59f258a71e5<br>SHA1: 2e2ebdf3ff0828bf0bec7a0721a640652ee46604<br>SHA256: 67adfa103198b71da16b6062208a5c1463124938a989052684e108ba5a02004a</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>133.6MiB (140.0MB) – 1,221,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9577fce5ab3ea2265c99fcbee81620c1<br>SHA1: b7c4cb4367484de97b4f9c0e1831bb1a280329de<br>SHA256: 7e616ad3c2daaa23f09624468a46e516ba7da8df47c38040b374757e999332ec</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>123.6MiB (129.6MB) – 1,221,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 64ec1f9605137158a704456362c48077<br>SHA1: 409d2af993088af8207bdd9154d255e80490d742<br>SHA256: 9cd045101fbf8a914c23c50942619b38818e38eba56dd6085698238424ed226c</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.4MiB (140.9MB) – 1,221,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 146c80d487946fa81ff841bf806edceb<br>SHA1: 3ba1906794d8446a14e899185816eb2c6e2cb6d3<br>SHA256: 6d917984d9b288b8ffac23752386fd78dffa2befcc689590cddd2a5d377ffe21</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.6MiB (132.7MB) – 1,221,180 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: df46aacd6ea73215e85409160b096db1<br>SHA1: d025cfb30fd4061886eca55371c99e951eb038bd<br>SHA256: 404ab944ddfb0b796b4d76986d98e0cb480fb1cf78333fae7eb1fea65c2a24a8</pre></details></small> |


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
