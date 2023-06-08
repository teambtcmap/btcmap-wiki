# Introduction

## Endpoints

- `/elements`
- `/events`
- `/users`
- `/areas`
- `/reports`

## Data source

Most of the data included in the BTC Map API comes from [OpenStreetMap](https://www.openstreetmap.org/) data.

For BTC Map data we try to follow the same naming convention of keys as the OSM dataset.

## Update interval

We sync with the OSM servers every **10 minutes** to provide up-to-date open mapping data that is specific to bitcoin for everyone.

## Standard keys

Every record in our tables will contain the following keys:

- `id`
- `created_at`
- `updated_at`
- `deleted_at`

You can link data from different tables together using the `id`.

Records are never removed, they only have the `deleted_at` field populated when they are deleted.

OpenStreetMap and BTC Map data contains many optional tags. It is good practice to check for the existence of a tag before referencing it to avoid `undefined` errors.

## Caching

Applications can create local caches of the data and stay in sync with the BTC Map API. If a new record ID appears and you do not have it in your cache, you can assume it is a creation. You can discard cached records that have been updated.

Caching the data will allow for many improvements in your application like the ability to work offline, decrease loading times, reduce data usage and more. You can also incrementally sync the data by only fetching the records you need since your last update, instead of asking for all of the records in every request.

## Status

You can check the status of the API and it's endpoints [here](https://stats.uptimerobot.com/7kgEVtzlV1). If you are experiencing any issues please reach out and let us know.
