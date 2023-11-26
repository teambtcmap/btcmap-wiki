# Reports

## Endpoint

[https://api.btcmap.org/v2/reports](https://api.btcmap.org/v2/reports)

## Optional arguments

- `updated_since` - ISO 8601 date
- `limit` - 32-bit integer

## Data

The `reports` endpoint contains an array of report objects. Each report covers a time period of 24 hours. The latest report is updated every 10 minutes and historical reports are immutable. Reports for the entire BTC Map dataset will have an `area_id` of an empty string `""`. [Area](areas.html) specific reports will have a value in this field.

## Example

```json
{
  "id": 48,
  "area_id": "",
  "date": "2022-11-12",
  "tags": {
    "legacy_elements": 6528,
    "outdated_elements": 6952,
    "total_elements": 8623,
    "total_elements_lightning": 1483,
    "total_elements_lightning_contactless": 257,
    "total_elements_onchain": 1444,
    "up_to_date_elements": 1671
  },
  "created_at": "2022-11-12T00:01:39Z",
  "updated_at": "2022-11-12T00:01:39Z",
  "deleted_at": ""
}
```

## Additional endpoints and queries

- Return only one report using the ID:
  [https://api.btcmap.org/v2/reports/28](https://api.btcmap.org/v2/reports/28)

- Return only reports updated after a set date: [https://api.btcmap.org/v2/reports?updated_since=2022-10-11T00:00:00.000Z](https://api.btcmap.org/v2/reports?updated_since=2022-10-11T00:00:00.000Z)
