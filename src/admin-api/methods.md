# Elements

## getelement

- token
- id

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "getelement", "params": {"password": "xxx", "id": "node:12141608846"}, "id": 1}' https://api.btcmap.org/rpc
```

## setelementtag

- token
- name
- value

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "setelementtag", "params": {"password": "xxx", "id": "node:12141608846", "name": "foo", "value": "bar"}, "id": 1}' https://api.btcmap.org/rpc
```

## removeelementtag

- token
- id
- tag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "removeelementtag", "params": {"password": "xxx", "id": "node:12141608846", "tag": "foo"}, "id": 1}' https://api.btcmap.org/rpc
```

## boostelement

- token
- id
- days

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "boostelement", "params": {"password": "xxx", "id": "node:12141608846", "days": 7}, "id": 1}' https://api.btcmap.org/rpc
```

## addelementcomment

- token
- id
- comment

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "addelementcomment", "params": {"password": "xxx", "id": "node:12141608846", "comment": "test comment"}, "id": 1}' https://api.btcmap.org/rpc
```

<!-- ## generateelementissues -->

# Areas

## addarea

- token
- tags

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "addarea", "params": {"password": "xxx", "tags": {"url_alias": "test-area", "geo_json": {"type":"Point","coordinates":[0,0]}}}, "id": 1}' https://api.btcmap.org/rpc
```

## getarea

- token
- id

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "getarea", "params": {"password": "xxx", "id": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```

## setareatag

- token
- id
- name
- value

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "setareatag", "params": {"password": "xxx", "id": "test-area", "name": "foo", "value": "bar"}, "id": 1}' https://api.btcmap.org/rpc
```

## removeareatag

- token
- id
- tag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "removeareatag", "params": {"password": "xxx", "id": "test-area", "tag": "foo"}, "id": 1}' https://api.btcmap.org/rpc
```

## gettrendingcountries

- token
- period_start
- period_end

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "gettrendingcountries", "params": {"password": "xxx", "period_start": "2024-01-01", "period_end": "2024-02-01"}, "id": 1}' https://api.btcmap.org/rpc
```

## gettrendingcommunities

- token
- period_start
- period_end

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "gettrendingcommunities", "params": {"password": "xxx", "period_start": "2024-01-01", "period_end": "2024-02-01"}, "id": 1}' https://api.btcmap.org/rpc
```

## removearea

- token
- id

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "removearea", "params": {"password": "xxx", "id": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```
