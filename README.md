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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-06-07<br>IPv6: 2023-06-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.858MiB (6.142MB) – 249,452 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f09e721808d6bbbd7f90011308aab55<br>SHA1: 6dd1186c1a11c809daa64dbe8c63fca1b508acef<br>SHA256: a1b8f512bf5a2e732c763759e5ac06fa55b076283b31b45c02f7a3658b41beb4</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.542MiB (6.859MB) – 84,684 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95d33ebb08ba32fabcdefa596575e9a1<br>SHA1: 94484ab7670ef5d1bfc48557068243e5081fd0d5<br>SHA256: 01d4e9b8437337c3c304ae823ee1d73734ab8d3258226958c5bb63a7ab411b82</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-06-07<br>IPv6: 2023-06-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.474MiB (9.935MB) – 402,407 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 97d167c360296d1d2a69e4a401b1e883<br>SHA1: a7094232a7ada68d90bcd72bb554f12ecd97674a<br>SHA256: 11163898de1ab25aee1d160b53ea72cdcded7f9298d49f0c12b43b7c461af81b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.626MiB (7.997MB) – 98,824 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: cbe1e0612537d76606113c4304a622b2<br>SHA1: 18611e4e6b40d6b8d807f29afe17d25321ac3325<br>SHA256: 344507fd4b451fbfd2af5041a25d10f9613c753505ab8d544f276599d51c5720</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-06-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>18.31MiB (19.20MB) – 781,420 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 6a7f45c6b61404977976315b01ff3627<br>SHA1: 310eaae0e8c49cccc4fdc14f4119f8b225028b77<br>SHA256: 631e451517d3ad42ab7f0c3bdac24577cb10f6d761336d2177938e8a39e18a23</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>23.29MiB (24.42MB) – 301,513 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 06eae8c94cba277a1474ab14c328500d<br>SHA1: 982b4b6c97c6438b0f59332fafe871451d820437<br>SHA256: 62d6cbe20ce06a373b85a6d1c636e791fb092a01714f243f79fed74ca8967c85</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.258MiB (7.611MB) – 310,670 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea16f2b91095213f9faf4261a5404be0<br>SHA1: c745544fc460b4fd9cb1ac68204736bcf9eabf79<br>SHA256: f0ea96ff5e89f5f267e07aa2f74df623e088bcb91f1df0d02845e1c412aeea46</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>25.86MiB (27.12MB) – 334,770 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7634f17216ca6f115cf06e4df5e44bcb<br>SHA1: 60cbd088cb95f3f19ddbebb63ee62aa7d4d5943c<br>SHA256: c3c8f61cd5d80cb8dabda6b047d66bfd6d73c7d0d9eef7427890f9825a480636</pre></details></small> |
| | | Full Location | Monthly<br>2023-06-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>193.0MiB (202.4MB) – 3,190,306 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 05f9e88d1ad989b6a665fbfd9d3b82b2<br>SHA1: e1ce63d9dae9f45709cd662cb78d5f323b9caca9<br>SHA256: ca5be0a45d234b5f3db9fd7993ca3b95fb26381d390a4e0d3e8111f2e7922199</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>351.1MiB (368.2MB) – 3,068,912 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 4471e6e2accf2b2f3c070f5cb39ed63a<br>SHA1: 158105fcee685e8e94bbff314ca8be8e235b169b<br>SHA256: 82b7025d3a47fff4700bbb503d62d17692265f78fae12837a6995bed2c31d118</pre></details></small> |
| [IP2Location LITE](#ip2location-lite-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Monthly<br>IPv4: 2023-06-07<br>IPv6: 2023-06-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv4.csv?inline=false)**<br>5.582MiB (5.853MB) – 238,084 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 5a1341c73b679015c1849651b02f8442<br>SHA1: 68ca29c935cf40cbfd663086deea4e61d8c8dc4f<br>SHA256: 4124a3662930f11954fa549834f6208912d91c3ddb53382a0c39cfaba1a71bb7</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-country/ipv6.csv?inline=false)**<br>26.40MiB (27.69MB) – 477,002 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2db255cf92eb5224035b1230f0efcc2b<br>SHA1: 4e4c6b67a3842bcdf119210a6676113f6543fa54<br>SHA256: c4335ed7e2c56df30bddbe55d518c81bb73286caae4ae123b4969eca63c72f25</pre></details></small> |
| | | Full Location | Monthly<br>IPv4: 2023-06-07<br>IPv6: 2023-06-07 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv4.csv?inline=false)**<br>191.3MiB (200.6MB) – 3,120,022 rows – 242 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1419e77505317334ccdf478ab7daef44<br>SHA1: 1d97a0ac2b0129e4e268083a3cbc23c627acabbe<br>SHA256: 35551439abd88f4346ee7c19bd2da4093eab3273897ca4f28e5cdb1e5d078ee1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ip2location-city/ipv6.csv?inline=false)**<br>381.0MiB (399.5MB) – 4,504,439 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7e04f9fe903ade529e55bb6b0d36ccdb<br>SHA1: 3f03d09739691bd6ada8c4ee23de98629caf20c3<br>SHA256: 5f023916ba65784e33d23b0934799adf20ae2b5448b40b7bd34e659f96864649</pre></details></small> |
| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-06-06<br>IPv6: 2023-06-06 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.720MiB (10.19MB) – 414,428 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2dce370e03366b07eb6ff49fbc7ec9ec<br>SHA1: 995e5edd8dadc8a41ea7c38f144baf7d2966cfdc<br>SHA256: 9bd3607aa47dba79ee85aedb6ebb796a1908fb88ad82ee7b97174e3d1e6b67fa</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>21.11MiB (22.14MB) – 273,312 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d895cb396c264e6bbc82569a4a0cd156<br>SHA1: 1567f9497dc56add77bb195a2f1d3a2c1fde6136<br>SHA256: 293a88810218ccbe3cb57e512e57752dc47278e539bb28b81776f5296dbebab6</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-06-06<br>IPv6: 2023-06-06 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>190.4MiB (199.6MB) – 3,789,076 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9c29b00c4b1d66f3b7e5f926e85ff675<br>SHA1: 7021d0eb4d29b9a53b2306d4b70bbd847c1e29e4<br>SHA256: 90ec1eb8c9c0d4e5d23d76a38cce417b101e7b60c6658c20687df4a56e441890</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>223.0MiB (233.8MB) – 3,789,076 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea6596ef30d94c91fce5f04cfecf823a<br>SHA1: d8aface6feb6495ffd05eb59590387a9ba6812f1<br>SHA256: 9826b5989064f82ea0921ce1dcdd8fe584e159d26f2b838cc3166e8a769216a0</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>197.1MiB (206.7MB) – 3,789,076 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9a3f0deb8a5304802729706801b4b753<br>SHA1: aee191f2c859b41e8b39797ab56e8022edf25c97<br>SHA256: 1a2e68c237ab530743bbfb8a6d16006d024bb2d9a14c5e3a16f0ee4565e30005</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>204.2MiB (214.1MB) – 3,789,076 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 95d92115cb1c5522e1bb0352a5700503<br>SHA1: b3daf18a6603ce52246fbaed387741ac3216f822<br>SHA256: 70f99c6d55b4a8ef770d8ca0fe7a4034616adb2bb55bc7240eafe9d4fff04821</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>240.0MiB (251.6MB) – 3,789,076 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f8ca50db88017e4b4007cdd18bee2e7b<br>SHA1: 9ed3883d0066c7b425f1b09af160d2eaf9503f3d<br>SHA256: d3c46bbd0c58c6200e6fd3b27c89e172f41eadb15fc37f6748eaca5857f4917b</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>191.9MiB (201.2MB) – 3,789,076 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 68b2dee494113ecc53a5e34d2721e861<br>SHA1: 799c5edb47c83cad8786af4557d0a3ed4bd5faad<br>SHA256: 7ffa8714d673e28281f9f54372f14477a16d43c89f07a29dfc0989dde454178f</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>240.5MiB (252.1MB) – 3,789,076 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 7271a5995653acb3b210fa8d633c1b21<br>SHA1: 5f23f9907ebdfa853a134d8596a54422afc5266e<br>SHA256: 5631cdba54de699e4cb86e9207d732df6ccd73ff81969ea0f94a5e2f0cfb16c3</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>204.2MiB (214.1MB) – 3,789,076 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2e05e64e848d58585fc2f618120e7129<br>SHA1: b0329290670cf7aa480b76615eef70fac3008a56<br>SHA256: 9c26918d59fae6c628808d605a651206c4f58919cfeea85cfbe5059286b44b69</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>125.0MiB (131.1MB) – 1,247,734 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c2f61d401a71a42006d5e7ef712250fa<br>SHA1: 10c759a8bdc1f6e6bc9b566aa5facd10b2701c35<br>SHA256: fb929e6806de4b915c1e76b927703939c76036e99f0b666586eb0f4e66293552</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>133.0MiB (139.5MB) – 1,247,734 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 39219c9cfec1e82d1fd4e52fda7ce9e0<br>SHA1: 82c5925b076723dba906fb471a77951c6ac98817<br>SHA256: 52f5eff331615eabd5d289463616f5baa6d28b014d1c389992064ac6ebbcc9a2</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>127.2MiB (133.4MB) – 1,247,734 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b608a85705b7753331fa0128aec8fc01<br>SHA1: e5dc3eb36b1b9072b8e96d67e1b5911bbf4dba24<br>SHA256: 57efa0b289e3b4e20a5af489a4f660a3d4a720642c869f532b7aaad3baee5a27</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>129.0MiB (135.3MB) – 1,247,734 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2684c19c258a150f7c6e4242d097bff6<br>SHA1: 0f2c96d289436f76b76b35255ad357f6ef89608a<br>SHA256: 9118e61bb73f40387540d60d68171ac22ab53e3b494e010aed64821f5e02a1cb</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>136.8MiB (143.5MB) – 1,247,734 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: a2607865f66397dfa4883b4162a01617<br>SHA1: 607399c4aa8dd55f32562aa7b0e6a120ef37b352<br>SHA256: d4ab4da71053b398662df768a55f0cd041f0f732360fbdf096f4ad6c5d97dc00</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>126.3MiB (132.5MB) – 1,247,734 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 41f5ebadc3e671b60b3b8aeac283580b<br>SHA1: 41e342b2677641a0d4f5fe6804645e9c0b0328a3<br>SHA256: 64f1e696ba2d61bceef9341b0ed37b2a04a8ef35848916fcf7f12a47b73be5a5</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>137.2MiB (143.9MB) – 1,247,734 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 871a20a8463123cbebeaec025c756a51<br>SHA1: 5d21db05119f0ebfd318ebf02ace8a73cddd2aac<br>SHA256: 8e51e90ac34946762a0ec73a76d95b0b9003d84e598dae476c670adae991848e</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>129.4MiB (135.7MB) – 1,247,734 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1ef755fd3d1259759b8a9e844e6c23c2<br>SHA1: 05265145e0dfb12007e4ec75e0d026ab12a50a2b<br>SHA256: f42308df728be2468e00d0e24df1545f7652ff1de3734809b3b855ce478fb21e</pre></details></small> |


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
