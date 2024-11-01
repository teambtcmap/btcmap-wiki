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
  "result": [
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

## get_element

- token
- id

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "get_element", "params": {"password": "xxx", "id": "node:12141608846"}, "id": 1}' https://api.btcmap.org/rpc
```

## set_element_tag

- token
- name
- value

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "set_element_tag", "params": {"password": "xxx", "id": "node:12141608846", "name": "foo", "value": "bar"}, "id": 1}' https://api.btcmap.org/rpc
```

## remove_element_tag

- token
- id
- tag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "remove_element_tag", "params": {"password": "xxx", "id": "node:12141608846", "tag": "foo"}, "id": 1}' https://api.btcmap.org/rpc
```

## boost_element

- token
- id
- days

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "boost_element", "params": {"password": "xxx", "id": "node:12141608846", "days": 7}, "id": 1}' https://api.btcmap.org/rpc
```

## add_element_comment

- token
- id
- comment

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "add_element_comment", "params": {"password": "xxx", "id": "node:12141608846", "comment": "test comment"}, "id": 1}' https://api.btcmap.org/rpc
```

<!-- ## generateelementissues -->

# Areas

## add_area

- token
- tags

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "add_area", "params": {"password": "xxx", "tags": {"url_alias": "test-area", "geo_json": {"type":"Point","coordinates":[0,0]}}}, "id": 1}' https://api.btcmap.org/rpc
```

## get_area

- token
- id

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "get_area", "params": {"password": "xxx", "id": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```

## set_area_tag

- token
- id
- name
- value

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "set_area_tag", "params": {"password": "xxx", "id": "test-area", "name": "foo", "value": "bar"}, "id": 1}' https://api.btcmap.org/rpc
```

## remove_area_tag

- token
- id
- tag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "remove_area_tag", "params": {"password": "xxx", "id": "test-area", "tag": "foo"}, "id": 1}' https://api.btcmap.org/rpc
```

## get_trending_countries

- token
- period_start
- period_end

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "get_trending_countries", "params": {"password": "xxx", "period_start": "2024-01-01", "period_end": "2024-02-01"}, "id": 1}' https://api.btcmap.org/rpc
```

## get_trending_communities

- token
- period_start
- period_end

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "get_trending_communities", "params": {"password": "xxx", "period_start": "2024-01-01", "period_end": "2024-02-01"}, "id": 1}' https://api.btcmap.org/rpc
```

## remove_area

- token
- id

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "remove_area", "params": {"password": "xxx", "id": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```
