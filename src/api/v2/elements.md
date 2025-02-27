# Elements

## Endpoint

[https://api.btcmap.org/v2/elements](https://api.btcmap.org/v2/elements)

## Optional arguments

- `updated_since` - ISO 8601 date
- `limit` - 32-bit integer

## Data

The `elements` endpoint contains an array of location objects pulled from OpenStreetMap. These locations are filtered from the complete OSM dataset by looking for one of the following tags:

- `currency:XBT=yes`
- `payment:bitcoin=yes`

More information about these tags and other bitcoin specific tags can be found in our data [Wiki](../general/tagging-instructions.html#tagging-guidance).

Reference to the OSM Wiki about elements can be found [here](https://wiki.openstreetmap.org/wiki/Elements). An element can contain many different tags which provide information about a given location. Reference to the OSM Wiki about tags can be found [here](https://wiki.openstreetmap.org/wiki/Tags).

## Example

The `osm_json` key contains all of the information from OSM. The top level `tags` key contains BTC Map information which can include boosts, merchant lightning payment information, and other data.

```json
{
  "id": "node:9985802993",
  "osm_json": {
    "changeset": 127516569,
    "id": 9985802993,
    "lat": 53.4423766,
    "lon": -2.2775673,
    "tags": {
      "addr:city": "Manchester",
      "addr:housenumber": "585A",
      "addr:postcode": "M21 9AF",
      "addr:street": "Wilbraham Road",
      "currency:GBP": "yes",
      "currency:XBT": "yes",
      "currency:others": "no",
      "description": "Inexpensive traditional barbers, no appointment needed.",
      "name": "RJ's",
      "opening_hours": "Mo-Sa 09:00-17:00",
      "payment:lightning": "yes",
      "payment:lightning_contactless": "yes",
      "payment:onchain": "yes",
      "phone": "+44 7812 919857",
      "shop": "hairdresser",
      "survey:date": "2022-10-14"
    },
    "timestamp": "2022-10-14T10:27:01Z",
    "type": "node",
    "uid": 16971158,
    "user": "nathan_day",
    "version": 11
  },
  "tags": {
    "category": "other",
    "icon:android": "content_cut",
    "issues": [
      { "description": "Out of date", "severity": 3382, "type": "out_of_date" }
    ]
  },
  "created_at": "2022-09-25T08:45:08Z",
  "updated_at": "2022-11-02T10:16:37Z",
  "deleted_at": ""
}
```

## Additional endpoints and queries

- Return only one element using the ID:
  [https://api.btcmap.org/v2/elements/node:9985802993](https://api.btcmap.org/v2/elements/node:9985802993)

- Return only elements updated after a set date: [https://api.btcmap.org/v2/elements?updated_since=2022-10-11T00:00:00.000Z](https://api.btcmap.org/v2/elements?updated_since=2022-10-11T00:00:00.000Z)
