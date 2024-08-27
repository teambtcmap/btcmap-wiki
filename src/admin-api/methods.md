# Areas

## createarea

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "createarea", "params": {"token": "xxx", "tags": {"url_alias": "test-area", "geo_json": {"type":"Point","coordinates":[0,0]}}}, "id": 1}' https://api.btcmap.org/rpc
```

## getarea

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "getarea", "params": {"token": "xxx", "area_id_or_alias": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```

## setareatag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "setareatag", "params": {"token": "xxx", "area_id_or_alias": "test-area", "tag_name": "foo", "tag_value": "bar"}, "id": 1}' https://api.btcmap.org/rpc
```

## removeareatag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "removeareatag", "params": {"token": "xxx", "area_id_or_alias": "test-area", "tag_name": "foo"}, "id": 1}' https://api.btcmap.org/rpc
```

## removearea

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "removearea", "params": {"token": "xxx", "area_id_or_alias": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```
