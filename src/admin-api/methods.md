# General

## search

- token
- query

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "search", "params": {"password": "xxx", "query": "query", "id": 1}' https://api.btcmap.org/rpc
```
Example response to a `berlin` query param :

```json
{
"id": 1,
"jsonrpc": "2.0",
"result":[
  {
  "id": 155,
  "name": "Bitcoin Berlin El Salvador",
  "type": "area"
  },
  {
  "id": 54,
  "name": "Berlin 2140",
  "type": "area"
  },
  {
  "id": 257,
  "name": "Einundzwanzig Berlin",
  "type": "area"
  },
  {
  "id": 77,
  "name": "Bitcoin Berlin El Salvador",
  "type": "area"
  }
]
}
```

# Elements

## getelement

- token
- id

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "get_element", "params": {"password": "xxx", "id": "node:12141608846"}, "id": 1}' https://api.btcmap.org/rpc
```

## setelementtag

- token
- name
- value

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "set_element-tag", "params": {"password": "xxx", "id": "node:12141608846", "name": "foo", "value": "bar"}, "id": 1}' https://api.btcmap.org/rpc
```

## removeelementtag

- token
- id
- tag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "remove-element_tag", "params": {"password": "xxx", "id": "node:12141608846", "tag": "foo"}, "id": 1}' https://api.btcmap.org/rpc
```

## boostelement

- token
- id
- days

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "boost_element", "params": {"password": "xxx", "id": "node:12141608846", "days": 7}, "id": 1}' https://api.btcmap.org/rpc
```

## addelementcomment

- token
- id
- comment

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "add_element_comment", "params": {"password": "xxx", "id": "node:12141608846", "comment": "test comment"}, "id": 1}' https://api.btcmap.org/rpc
```

<!-- ## generateelementissues -->

# Areas

## addarea

- token
- tags

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "add_area", "params": {"password": "xxx", "tags": {"url_alias": "test-area", "geo_json": {"type":"Point","coordinates":[0,0]}}}, "id": 1}' https://api.btcmap.org/rpc
```

## getarea

- token
- id

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "get_area", "params": {"password": "xxx", "id": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```

## setareatag

- token
- id
- name
- value

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "set_area_tag", "params": {"password": "xxx", "id": "test-area", "name": "foo", "value": "bar"}, "id": 1}' https://api.btcmap.org/rpc
```

## removeareatag

- token
- id
- tag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "remove_area_tag", "params": {"password": "xxx", "id": "test-area", "tag": "foo"}, "id": 1}' https://api.btcmap.org/rpc
```

## gettrendingcountries

- token
- period_start
- period_end

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "get_trending_countries", "params": {"password": "xxx", "period_start": "2024-01-01", "period_end": "2024-02-01"}, "id": 1}' https://api.btcmap.org/rpc
```

## gettrendingcommunities

- token
- period_start
- period_end

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "get_trending_communities", "params": {"password": "xxx", "period_start": "2024-01-01", "period_end": "2024-02-01"}, "id": 1}' https://api.btcmap.org/rpc
```

## removearea

- token
- id

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "remove_area", "params": {"password": "xxx", "id": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```
