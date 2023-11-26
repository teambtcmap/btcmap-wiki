# Events

## Endpoint

[https://api.btcmap.org/v2/events](https://api.btcmap.org/v2/events)

## Optional arguments

- `updated_since` - ISO 8601 date
- `limit` - 32-bit integer

## Data

The `events` endpoint contains an array of event objects. A new record gets added to this table when an [element](elements.html) gets created, updated or deleted. Please note that when an element is created or deleted on BTC Map this does not necessarily mean the same event happened on OpenStreetMap. For example, if a `currency:XBT=yes` tag is removed on OSM - this element will be marked as deleted on BTC Map because it no longer accepts bitcoin. While on OSM the element still exists.

Another important note is that the `events` table does not contain a complete history of all events that happened on OSM. It only includes records since BTC Map has been operating.

Only events with a `deleted_at` value of an empty string `""` are valid events. Non-valid events should be filtered out.

## Example

```json
{
  "id": 500,
  "type": "delete",
  "element_id": "node:2879194870",
  "user_id": 16971158,
  "created_at": "2022-10-11T10:03:39.549906728Z",
  "updated_at": "2022-10-11T10:03:39.549906728Z",
  "deleted_at": ""
}
```

## Additional endpoints and queries

- Return only one event using the ID:
  [https://api.btcmap.org/v2/events/500](https://api.btcmap.org/v2/events/500)

- Return only events updated after a set date: [https://api.btcmap.org/v2/events?updated_since=2022-10-11T00:00:00.000Z](https://api.btcmap.org/v2/events?updated_since=2022-10-11T00:00:00.000Z)
