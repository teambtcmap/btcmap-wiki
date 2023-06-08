# Areas

## Endpoint

[https://api.btcmap.org/v2/areas](https://api.btcmap.org/v2/areas)

## Optional arguments

- `updated_since` - ISO 8601 date
- `limit` - 32-bit integer

## Data

The `areas` endpoint contains an array of area objects. An area can be any geographic area like a country, town, island etc. An area can also be a community like Bitcoin Island Philippines for example. These areas are manually added by BTC Map. Currently the primary purpose is to promote local bitcoin communities to take ownership of their bitcoin mapping data by managing it themselves, which will help drive adoption.

Polygon data can be found for areas in the [GeoJSON](https://geojson.org/) format.

## Example

```json
{
  "id": "bitcoin-island-philippines",
  "tags": {
    "name": "Bitcoin Island Philippines",
    "type": "community",
    "continent": "asia",
    "population": "37802",
    "population:date": "2020-01-01",
    "geo_json": "<GeoJSON Polygon or MultiPolyon>",
    "contact:discord": "https://discord.gg/YAZjxHysQD",
    "contact:twitter": "https://twitter.com/BitcoinIslandPH",
    "contact:website": "https://pouch.ph/bitcoinisland",
    "icon:square": "https://btcmap.org/images/communities/bitcoin-island-philippines.jpg"
  },
  "created_at": "2022-10-15T04:12:56Z",
  "updated_at": "2022-10-19T20:40:21Z",
  "deleted_at": ""
}
```

## Additional endpoints and queries

- Return only one area using the ID:
  [https://api.btcmap.org/v2/areas/bitcoin-island-philippines](https://api.btcmap.org/v2/areas/bitcoin-island-philippines)

- Return only areas updated after a set date: [https://api.btcmap.org/v2/areas?updated_since=2022-10-11](https://api.btcmap.org/v2/areas?updated_since=2022-10-11)

## Communities

Community organizations with a medium or large amount of local bitcoin communities that are interested in joining BTC Map can reach out to a core team member to help facilitate a bulk upload of the data. Below describes the schema needed for each community and provides example values. Note that some fields are required and some are optional. Optional fields can be excluded from the dataset.

### Example JSON

```json
{
  "id": "bitcoin-ekasi", // should be all lowercase and spaces separated by `-` characters
  "tags": {
    "type": "community", // will always be `community`
    "name": "Bitcoin Ekasi",
    "continent": "africa", // can be one of the following options: `africa` `asia` `europe` `north-america` `oceania` `south-america`
    "icon:square": "https://btcmap.org/images/communities/bitcoin-ekasi.jpg",
    "contact:email": "hermann.unravelsurftravel@gmail.com", // can be any of the following options: `website` `email` `nostr` `twitter` `meetup` `eventbrite` `telegram` `discord` `youtube` `github` `reddit` `instagram` `whatsapp` `facebook` `linkedin` (at least one tag is required, new contact types can be requested)
    "contact:twitter": "https://twitter.com/BitcoinEkasi",
    "contact:website": "https://bitcoinekasi.com/",
    "tips:lightning_address": "example@getalby.com", // optional - can be a lightning address/lnurlp or a URL to a tip page using the `tip:url` format
    "organization": "african-bitcoiners",
    "language": "en", // optional
    "geo_json": "<GeoJSON Polygon or MultiPolyon>",
    "population": "2100", // optional
    "population:date": "2023-01-21" // optional
  }
}
```

### Notes

- GeoJSON can be created by following this [guide](../general/geojson-areas.html) or by using another method.
- For community icon images please provide a zip file of all the assets and naming each file using the community `id` (webp, png, svg, or jpg format).
