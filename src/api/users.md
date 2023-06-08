# Users

## Endpoint

[https://api.btcmap.org/v2/users](https://api.btcmap.org/v2/users)

## Optional arguments

- `updated_since` - ISO 8601 date
- `limit` - 32-bit integer

## Data

The `users` endpoint contains an array of user objects pulled from OpenStreetMap profiles. It does not contain every OSM user. A new record gets added to this table when an [event](events.html) is created and the `users` table does not yet have the profile information associated with this event. Once a user record is included, any changes made to the OSM profile will sync with the `users` table once daily.

We have been encouraging users to include a lightning address or LNURL-pay string in their profile descriptions so this information can be used to send them lightning tips. More information on the implementation can be found [here](../general/lightning-tips.html).

Reference to the OSM Wiki about users can be found [here](https://wiki.openstreetmap.org/wiki/Web_front_end#Users).

## Example

The `osm_json` key contains all of the information from OSM.

```json
{
  "id": "17221642",
  "osm_json": {
    "account_created": "2022-09-24T01:06:05Z",
    "blocks": {
      "received": {
        "active": 0,
        "count": 0
      }
    },
    "changesets": {
      "count": 220
    },
    "contributor_terms": {
      "agreed": true
    },
    "description": "Lead on the ground of Bitcoin Island, Philippines.\r\nPowered by Pouch.ph",
    "display_name": "Bill on Bitcoin Island",
    "id": 17221642,
    "img": {
      "href": "https://www.openstreetmap.org/rails/active_storage/representations/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBeno1MXc9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--44266f623ba498d7db2aedf5321b5122087e5960/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJY0c1bkJqb0dSVlE2RkhKbGMybDZaVjkwYjE5c2FXMXBkRnNIYVdscGFRPT0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--c51edbffdce997b8125dbbed51b6988fec44e09d/Bitcoin%20Island%20Square%20BG%20Trans.png"
    },
    "roles": [],
    "traces": {
      "count": 0
    }
  },
  "created_at": "2022-10-13T05:33:47Z",
  "updated_at": "2022-10-20T01:24:01Z",
  "deleted_at": ""
}
```

## Additional endpoints and queries

- Return only one user using the ID:
  [https://api.btcmap.org/v2/users/16990757](https://api.btcmap.org/v2/users/16990757)

- Return only users updated after a set date: [https://api.btcmap.org/v2/users?updated_since=2022-10-11](https://api.btcmap.org/v2/users?updated_since=2022-10-11)
