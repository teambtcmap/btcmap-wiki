# Areas

## createarea

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "createarea", "params": {"token": "xxx", "tags": {"url_alias": "test-area", "geo_json": {"type":"Point","coordinates":[0,0]}}}, "id": 1}' https://api.btcmap.org/rpc
```

## getarea

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "getarea", "params": {"token": "xxx", "id": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```

## setareatag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "setareatag", "params": {"token": "xxx", "id": "test-area", "name": "foo", "value": "bar"}, "id": 1}' https://api.btcmap.org/rpc
```

## removeareatag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "removeareatag", "params": {"token": "xxx", "id": "test-area", "tag": "foo"}, "id": 1}' https://api.btcmap.org/rpc
```

## removearea

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "removearea", "params": {"token": "xxx", "id": "test-area"}, "id": 1}' https://api.btcmap.org/rpc
```

# Elements

## getelement

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "getelement", "params": {"token": "xxx", "id": "node:12141608846"}, "id": 1}' https://api.btcmap.org/rpc
```

## setelementtag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "setelementtag", "params": {"token": "xxx", "id": "node:12141608846", "name": "foo", "value": "bar"}, "id": 1}' https://api.btcmap.org/rpc
```

## removeelementtag

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "removeelementtag", "params": {"token": "xxx", "id": "node:12141608846", "tag": "foo"}, "id": 1}' https://api.btcmap.org/rpc
```

## boostelement

```bash
curl --data-binary '{"jsonrpc": "2.0", "method": "boostelement", "params": {"token": "xxx", "id": "node:12141608846", "days": 7}, "id": 1}' https://api.btcmap.org/rpc
```
