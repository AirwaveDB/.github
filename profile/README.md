# AirwaveDB

Open directory of internet radio stations and playable stream endpoints.

AirwaveDB collects station metadata, normalizes duplicate records, keeps playable stream URLs separately, and publishes the result as JSON, NDJSON, CSV, and M3U data.

## API

Public JSON data:

```text
https://raw.githubusercontent.com/AirwaveDB/api/main/v1
```

Examples:

```text
https://raw.githubusercontent.com/AirwaveDB/api/main/v1/index.json
https://raw.githubusercontent.com/AirwaveDB/api/main/v1/countries/jp.json
https://raw.githubusercontent.com/AirwaveDB/api/main/v1/stations.json
https://raw.githubusercontent.com/AirwaveDB/api/main/v1/streams.json
```

See [`AirwaveDB/api`](https://github.com/AirwaveDB/api) for the endpoint list and data model.

## Repositories

- [`api`](https://github.com/AirwaveDB/api) — public JSON and NDJSON endpoints
- [`database`](https://github.com/AirwaveDB/database) — canonical station metadata and source mappings
- [`streams`](https://github.com/AirwaveDB/streams) — playable stream endpoints and country M3U playlists
- [`checker`](https://github.com/AirwaveDB/checker) — independent stream availability checks
- [`website`](https://github.com/AirwaveDB/website) — station browser and player

## Data sources

The dataset is built from open radio directories and verified public stream lists. Source identifiers and provenance are retained so imported records can be traced back to their origin.

AirwaveDB lists third-party endpoints. It does not proxy or rebroadcast radio streams.