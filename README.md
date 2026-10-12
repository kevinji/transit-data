# transit-data
Raw transit data files and generated Vega-Lite JSON files parsed from the raw files.

## Sources and licenses

The data in this repository is not covered by a single license. Files in `original/` are
downloaded from each transit agency and remain subject to that agency's terms. Files in
`generated/` are derived from `original/` (e.g. monthly averages computed from station-level or
daily data) and are subject to the same terms as the data they are derived from.

| Directory | Source | Terms |
| --- | --- | --- |
| `bart/` | [BART ridership reports](https://www.bart.gov/about/reports/ridership) | [Creative Commons Attribution License](https://opendefinition.org/licenses/cc-by/). The data has been modified. |
| `sfmta/` | [SFMTA ridership dashboard](https://transtat.sfmta.com/t/public/views/Goal2Dashboards/RidershipTable) | No license specified. |
| `mta/` | [MTA open data](https://www.mta.info/open-data) via [NY Open Data](https://data.ny.gov/) | [OPEN-NY Terms of Use](https://data.ny.gov/d/77gx-ii52) |

The MTA data combines the daily ridership dataset
([MTA Daily Ridership and Traffic: Beginning 2020](https://data.ny.gov/d/sayj-mze2)) with the hourly
station-level datasets
([MTA Subway Hourly Ridership: 2017-2019](https://data.ny.gov/d/t69i-h2me),
[2020-2024](https://data.ny.gov/d/wujg-7c2s)) for days before March 2020.
