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
| [GeoFeed + Whois + ASN](#geofeed-whois-asn-database) | 🅭🄍<br>CC0 1.0 | Country | Daily<br>IPv4: 2023-07-10<br>IPv6: 2023-07-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv4.csv?inline=false)**<br>5.663MiB (5.938MB) – 241,293 rows – 247 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: d83512dda318594008d6623d591f1a43<br>SHA1: e6e0ea5b54319558ab1b84441b904f414b1b47a5<br>SHA256: 4fe34799902e965f1b175444d1a301f424679f58008136351f5519cd0efe824b</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geo-whois-asn-country/ipv6.csv?inline=false)**<br>6.542MiB (6.860MB) – 84,687 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2baf9abcd7b4a7e95e1cccf1f7db8bd8<br>SHA1: c7fd7334f9ff0e62a05749af91f1877564daf47f<br>SHA256: f3f5463b16408552d92d534845e3b71350f879a99deee8c5b13e412950da6916</pre></details></small> |
| [iptoasn.com](#iptoasncom-database) | 🄍<br>PDDL v1.0 | Country | Daily<br>IPv4: 2023-07-10<br>IPv6: 2023-07-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv4.csv?inline=false)**<br>9.513MiB (9.975MB) – 404,062 rows – 240 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c08945e30615924691309f494c86f615<br>SHA1: 39d6fea9b0d2c84fb98492619f1948f70d1c9c6f<br>SHA256: adc72c5ecc1ddaed22676ce28a91c379923416164dfc4a264503768059b2e828</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/iptoasn-country/ipv6.csv?inline=false)**<br>7.711MiB (8.086MB) – 99,924 rows – 222 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ff0952605812d308d1fb13bbeec3c97f<br>SHA1: 90f942498ce4490f1840944bcd27d44f652c3bc2<br>SHA256: 5412eb4bb929bfcfb34f0efd3e9566087cfb01ed5b1eaa32df92013e3f81d610</pre></details></small> |
| [IPinfo.io](#ipinfoio-databases) | 🅭🅯🄎<br>CC BY-SA 4.0 | Country | Daily<br>2023-07-10 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv4.csv?inline=false)**<br>14.44MiB (15.15MB) – 615,660 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2cfb4968334ffe43017dde5d312493fb<br>SHA1: 353708035fa22c6f9e7f8018649d35a8066c6888<br>SHA256: 613b987eacab35b4632d20ad5dcbe90ef00f62d829a4f53a6bb58bb56068a5f1</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/ipinfo-country/ipv6.csv?inline=false)**<br>31.36MiB (32.88MB) – 405,965 rows – 243 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f6a21d8e3505da7cd08559dd29da8248<br>SHA1: cbf95e10c541afbeed0118868c603cebc92b4a6b<br>SHA256: 1c1f34f9f84066329e2068dae7b7b47fe999626e100c782ea2fe870facffd185</pre></details></small> |
| [DB-IP Lite](#db-ip-lite-databases) | 🅭🅯<br>CC BY 4.0 | Country | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv4.csv?inline=false)**<br>7.175MiB (7.523MB) – 307,076 rows – 245 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f151f7f54b095b5ffda5d94059bb3dce<br>SHA1: f80142665d03d0371f800c5f959cf629ca3d8a10<br>SHA256: b490b03da5e813361b0ca08dd8f825c5991c8d4f9e21568776e4edd93746282a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-country/ipv6.csv?inline=false)**<br>24.39MiB (25.58MB) – 315,780 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 2ccafe342cd0f83d168aa17033cc052e<br>SHA1: 18929b5d0a7ce12d7f3357fae4e283e3dd102ad6<br>SHA256: 55c042d3051eabf81b139c750768903bc3e9d8314dc416dc8b9ed715765677c2</pre></details></small> |
| | | Full Location | Monthly<br>2023-07-01 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv4.csv?inline=false)**<br>192.5MiB (201.8MB) – 3,182,050 rows – 244 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 3425f6eec44d17e75a144956ca9bedc4<br>SHA1: a6ae6d14f8e9a5705bee763c64c2bea6c879b127<br>SHA256: 9a1cffd22df1d59c077b7123b734f643ddf57a71c4d928ee793715e78400597a</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/dbip-city/ipv6.csv?inline=false)**<br>289.0MiB (303.0MB) – 2,522,649 rows – 249 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ac831cafe688be22a072e63aeca50a09<br>SHA1: 8b579d16247db56f0e752f9c5566007ecce7b3c3<br>SHA256: f693430db94cf07b4b01343ab0d2e4ab2f16501d77f433b222ab16b8f015dcf2</pre></details></small> |


| [GeoLite2](#geolite2-databases) | 🅯🄎<br>GeoLite2 EULA | Country | Weekly<br>IPv4: 2023-07-08<br>IPv6: 2023-07-08 | ⬇️ **[ipv4.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv4.csv?inline=false)**<br>9.894MiB (10.37MB) – 421,915 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: ea705d901dc6bf86114ca514710461a9<br>SHA1: 98fabc4ebb684ad3c04860bd5e7e5d7406e5fc7a<br>SHA256: 7d0c8d8d0ac9e884120ea8c469d7d1515c208fd89ab94dcdc4d4d33dd247253f</pre></details></small> | ⬇️ **[ipv6.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-country/ipv6.csv?inline=false)**<br>22.76MiB (23.87MB) – 294,684 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 818d5b86d0646965afe83b9fb484f138<br>SHA1: dae291376e762d3e70ad09d09980079d01658da1<br>SHA256: 6b5e7d789ee76c70dc9483af196d608d6a24b3a576507d85e461c8800ab46ff4</pre></details></small> |
| | | Full Location | Weekly<br>IPv4: 2023-07-08<br>IPv6: 2023-07-08 | ⬇️ **[ipv4-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-de.csv?inline=false)**<br>185.7MiB (194.7MB) – 3,700,837 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8d2c7da82b5b3813c9dafb5b7d42edde<br>SHA1: b379688d3affa7246634be7be9297264bf3daa99<br>SHA256: 982a84aee3d30cd65fd16d91c1592486b65abb32987152fda7b16bd87c3290b1</pre></details></small>⬇️ **[ipv4-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-en.csv?inline=false)**<br>217.2MiB (227.7MB) – 3,700,837 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 131ae3aef9d6eb93de1651c94a4e5377<br>SHA1: 23d4a7c9fc3f7501121dc5343c686bd50e2f0660<br>SHA256: 4a32930afa459bba44893714f88ba1100d749178daed40c923ea0e1cd9c64889</pre></details></small>⬇️ **[ipv4-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-es.csv?inline=false)**<br>192.4MiB (201.8MB) – 3,700,837 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 8ee9be5f4e22bbfc69dc7c41929a48bf<br>SHA1: 1d17b91b9b69462eacd6e3005674a33e53028fd1<br>SHA256: 155dcf406f3a4ab799c32e07a1da747dcbe2af9d174824a08ca4965037342ba9</pre></details></small>⬇️ **[ipv4-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-fr.csv?inline=false)**<br>199.1MiB (208.8MB) – 3,700,837 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 94680f1a7def72a8a58d8df3c2d8cb55<br>SHA1: 0e93672ab2531b609f5484f10ca00142212734e9<br>SHA256: e2d57beb2cb882086321393fce57077ba21d67a63358c26d73a5c0aaa2f659c5</pre></details></small>⬇️ **[ipv4-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ja.csv?inline=false)**<br>234.2MiB (245.6MB) – 3,700,837 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: f206fdc6f9b06d5a1b2efe3f7233ab65<br>SHA1: 34fc15d31522dfac10b6c8f1b130781b1550781b<br>SHA256: cc55ac8c019c2561768578956cb22cdaa9ee1dbafa551ba1d533468709b2ab64</pre></details></small>⬇️ **[ipv4-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-pt-BR.csv?inline=false)**<br>187.3MiB (196.4MB) – 3,700,837 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: e0b1a899434cff4afe448afb35c85164<br>SHA1: 2a51a329016cfc865077f91e25b9f770c4dee10a<br>SHA256: 49bc032f9510ab53f045d47face2c5a57c0c012d4aa60eae8af841e71405dea5</pre></details></small>⬇️ **[ipv4-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-ru.csv?inline=false)**<br>234.5MiB (245.8MB) – 3,700,837 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 1f54d762feab1493e1d4b685658f62cc<br>SHA1: 6fa197502719d23c16ff76f28a701df4e42ccb08<br>SHA256: ab0458670c274aee5176c9fe4e7f83f7ec36245e4c87dfc48c6615f2c4b89037</pre></details></small>⬇️ **[ipv4-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv4-zh-CN.csv?inline=false)**<br>199.3MiB (209.0MB) – 3,700,837 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 58c240184dd360ad30b5789fa8d9c552<br>SHA1: 9672471ecd2d32fa1116e1983db521c290297be0<br>SHA256: d35e7bea697118579310d63d8671ec48134e9df018bf6bfe02e8a3f1d62bf1e3</pre></details></small> | ⬇️ **[ipv6-de.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-de.csv?inline=false)**<br>122.4MiB (128.3MB) – 1,224,139 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c135c3c02973356665279093879e5ce2<br>SHA1: cc5545aa616486a633f05de08a9617ba95ea1488<br>SHA256: 26db60d6ac28fc21c7fd59828a7d09273a286050ce0fbf786f3fa1a044f75f4f</pre></details></small>⬇️ **[ipv6-en.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-en.csv?inline=false)**<br>130.0MiB (136.4MB) – 1,224,139 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b15774cad530e4fa4a231d9992477638<br>SHA1: 42716645003bd601aa519ab258a7ecc4664e7b1b<br>SHA256: 0b0e73c1c62fa1f50c295e3eb1ade62ad7a2466fe633925a4aa1c74b575f0a15</pre></details></small>⬇️ **[ipv6-es.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-es.csv?inline=false)**<br>124.5MiB (130.5MB) – 1,224,139 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 9184bebf28c4b5e9c01fbc0493c789ec<br>SHA1: f1bbbdc54cdf5ee2ae1f443d3bd02915140640b1<br>SHA256: 1767cb7dae8cffa04a5f3ec4ccee50362e5c723142ccf7c0d83558b5dfd51d62</pre></details></small>⬇️ **[ipv6-fr.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-fr.csv?inline=false)**<br>126.2MiB (132.4MB) – 1,224,139 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0c9c683963fc96c65905c1a5d8053fa<br>SHA1: 72025465ad58a10392a4b2255bf4d5a028073152<br>SHA256: 1202dbe4c8300a3feb7d652f640be158e6c5f1b5b2af04f7eda38f3e487fb593</pre></details></small>⬇️ **[ipv6-ja.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ja.csv?inline=false)**<br>133.6MiB (140.1MB) – 1,224,139 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 0d9974e2669a0736d96ae4e5494bb696<br>SHA1: 61b820fe4be45b7dac7e0721d4144507f21a25a8<br>SHA256: d3f1801b38aa0f694d5e94111bbde63be6e379452b95c916bd4977af5305ef39</pre></details></small>⬇️ **[ipv6-pt-BR.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-pt-BR.csv?inline=false)**<br>123.6MiB (129.6MB) – 1,224,139 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: c7f294f9e400eebd6b2cf3f426e4dc61<br>SHA1: 37c39154a8034f615de495113b72acddfc9cb5d0<br>SHA256: 6c9a34133756fbda293fcebca872fd55c0b908670edddf3a522230380bf9c239</pre></details></small>⬇️ **[ipv6-ru.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-ru.csv?inline=false)**<br>134.1MiB (140.7MB) – 1,224,139 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: b0ad3fdd571f535b87d663b41e9d09ef<br>SHA1: bd27b0063cd056a9621ceb326c938d860d6de8cf<br>SHA256: 0303f11e9845565172b59363969e88d9e4f39a34afa12f823af054ef0ba33766</pre></details></small>⬇️ **[ipv6-zh-CN.csv](https://gitlab.com/tdulcet/ip-geolocation-dbs/-/raw/main/geolite2-city/ipv6-zh-CN.csv?inline=false)**<br>126.6MiB (132.7MB) – 1,224,139 rows – 250 unique countries<br><small><details><summary>Checksums (click to show)</summary><pre>MD5: 02d1cdcfcfb80fa10a4207ad1e555716<br>SHA1: d967f0fb954af6a3321a37d1c939f29db57e2ef5<br>SHA256: c5441b61c48a9a554bdc624b15860b538cf380fdc0cf16ecf8af6995c551be97</pre></details></small> |


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
