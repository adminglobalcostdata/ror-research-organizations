# ROR Research Organizations: 146,716 institutions

[![Apify Actor](https://img.shields.io/badge/Apify-Actor-1f6feb)](https://apify.com/phonic_lily/ror-research-organizations) ![Licence](https://img.shields.io/badge/licence-CC0_1.0-blue) ![Records](https://img.shields.io/badge/records-146%2C716-green)

Search 146,716 research organizations from the ROR registry (v2.15, 2026-10-20): universities, hospitals, companies, funders. Country, city, coordinates, website, Wikidata/ISNI/GRID ids, founding year, status. Embedded data, no scraping, pay per record.

## What you get
- **146,716 records**, each carrying its own `license` and `attribution` fields, ready to republish with the required credit.
- A **100-record free sample** in this repository: [`sample.jsonl`](sample.jsonl) and [`sample.csv`](sample.csv) (opens as a table on GitHub).
- The **full dataset** as a filterable API (JSON, CSV, Excel), no scraping, no login: [ROR Research Organizations: 146,716 institutions on Apify](https://apify.com/phonic_lily/ror-research-organizations).

## One record
```json
{
  "ror_id": "03ebg0v16",
  "name": "Boys Town",
  "acronyms": null,
  "aliases": "Father Flanagan's Boys' Home; Girls and Boys Tow",
  "types": "nonprofit, funder",
  "status": "active",
  "established": 1917,
  "country_code": "US",
  "country_name": "United States",
  "subdivision": "Nebraska",
  "city": "Omaha",
  "lat": 41.25626
}
```

## Quick start
Python:
```python
from apify_client import ApifyClient
client = ApifyClient('<YOUR_APIFY_TOKEN>')
run = client.actor('phonic_lily/ror-research-organizations').call(run_input={'maxResults': 10})
for item in client.dataset(run['defaultDatasetId']).iterate_items():
    print(item)
```
Or from the command line:
```bash
curl -X POST 'https://api.apify.com/v2/acts/phonic_lily~ror-research-organizations/run-sync-get-dataset-items?token=<YOUR_APIFY_TOKEN>' \
  -H 'Content-Type: application/json' -d '{"maxResults": 10}'
```
Pricing is pay-per-record on Apify (see the Actor page); the sample here is free.

## Fields
| Field | Description |
|---|---|
| `ror_id` | ROR identifier (https://ror.org/<id>). |
| `name` | Display name. |
| `acronyms` | Acronyms, comma separated. |
| `aliases` | Other names and labels, semicolon separated. |
| `types` | Organization types, comma separated. |
| `status` | active, inactive or withdrawn. |
| `established` | Founding year, null if unknown. |
| `country_code` | ISO 3166-1 alpha-2 country code. |
| `country_name` | Country name. |
| `subdivision` | Country subdivision name. |
| `city` | City (GeoNames). |
| `lat` | Latitude, decimal degrees. |
| `lon` | Longitude, decimal degrees. |
| `geonames_id` | GeoNames id of the city. |
| `website` | Official website URL. |
| `wikipedia_url` | Wikipedia URL. |
| `wikidata_id` | Wikidata Q-identifier. |
| `isni` | ISNI identifier. |
| `grid_id` | Legacy GRID identifier. |
| `fundref_id` | Crossref Funder Registry identifier. |
| `domains` | Internet domains. |
| `parent_count` | Number of parent organizations. |
| `child_count` | Number of child organizations. |
| `last_modified` | Date of last modification in ROR (YYYY-MM-DD). |

## Data, licence and attribution
Research Organization Registry (ROR) data dump v2.15 published 2026-10-20 on Zenodo (https://zenodo.org/records/23500708), licence CC0 as stated in the Zenodo record metadata and on https://ror.org/about/ . Schema v2 JSON; one record per organization. Only organizations, no personal data. Null means the source gives no value; it is never 0.

**Licence:** CC0 1.0 (public domain dedication), ROR data

**Attribution:** Source: Research Organization Registry (ROR), https://ror.org, data release v2.15 (2026-10-20), CC0 1.0. No attribution is legally required; crediting ROR is appreciated.

Snapshot date: 2026-10. Empty values are `null`, never 0.

## Cite this dataset
GitHub's *Cite this repository* button reads [`CITATION.cff`](CITATION.cff).

## Feedback
Found an error or want a field added? Open an issue in this repository.
