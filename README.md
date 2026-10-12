# transit-data
Transit ridership data downloaded from transit agencies, and the chart data generated from it.

- `original/`: files as downloaded from each agency.
- `processed/`: intermediate data computed from the downloads, where a step in between is useful.
- `generated/`: monthly average weekday ridership for each system, which the charts read.

## Related repositories

- [transit-charts](https://github.com/kevinji/transit-charts): The [transitcharts.com](https://transitcharts.com) website, which charts the generated data.
- [transit-parser](https://github.com/kevinji/transit-parser): Scripts that download ridership data from transit agencies and generate the data for the charts.

## Sources and licenses

The data in this repository is not covered by a single license. Files in `original/` are
downloaded from each transit agency and remain subject to that agency's terms. Files in
`processed/` and `generated/` are derived from them (e.g. monthly averages computed from
station-level or daily data) and are subject to the same terms as the data they are derived from.

| Directory | Source | Terms |
| --- | --- | --- |
| `bart/` | [BART ridership reports](https://www.bart.gov/about/reports/ridership) | [Creative Commons Attribution License](https://opendefinition.org/licenses/cc-by/). The data has been modified. |
| `sfmta/` | [SFMTA ridership dashboard](https://transtat.sfmta.com/t/public/views/Goal2Dashboards/RidershipTable) | No license specified. |
| `mta/` | [MTA open data](https://www.mta.info/open-data) via [NY Open Data](https://data.ny.gov/) | [OPEN-NY Terms of Use](https://data.ny.gov/d/77gx-ii52) |
| `wmata/` | [WMATA Metrorail ridership summary](https://www.wmata.com/about/open-data-hub/ridership-data/metrorail-ridership-summary.html) | No license specified. |
| `sound-transit/` | [Sound Transit ridership tracker](https://www.soundtransit.org/ride-with-us/system-performance-tracker/ridership) | No license specified. |

The MTA data combines the daily ridership dataset
([MTA Daily Ridership and Traffic: Beginning 2020](https://data.ny.gov/d/sayj-mze2)) with the hourly
station-level datasets
([MTA Subway Hourly Ridership: 2017-2019](https://data.ny.gov/d/t69i-h2me),
[2020-2024](https://data.ny.gov/d/wujg-7c2s)) for days before March 2020. Days before February
2017 are estimated from turnstile entry counters
([MTA Subway Turnstile Usage Data: 2014](https://data.ny.gov/d/i55r-43gk),
[2015](https://data.ny.gov/d/ug6q-shqc), [2016](https://data.ny.gov/d/ekwu-khcy),
[2017](https://data.ny.gov/d/v5y5-mwpb)). The turnstile readings are too large to keep, so only
the daily entries estimated from them are saved, in `processed/mta/`.

The Sound Transit data is queried from the Power BI report behind the ridership tracker. It covers
all Sound Transit modes from 2019, and only Link light rail is charted.
