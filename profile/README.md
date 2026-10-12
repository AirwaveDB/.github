# AirwaveDB

Open data for internet radio stations and streams.

AirwaveDB separates station identity and metadata from playable stream endpoints, then publishes generated formats for applications and data consumers.

## Repositories

- [`database`](https://github.com/AirwaveDB/database) — station metadata, countries, languages, categories, and source mappings
- [`streams`](https://github.com/AirwaveDB/streams) — direct stream endpoints and country M3U playlists
- [`api`](https://github.com/AirwaveDB/api) — generated JSON and NDJSON datasets
- [`checker`](https://github.com/AirwaveDB/checker) — independent stream availability checks
- [`website`](https://github.com/AirwaveDB/website) — station browser and player

## Data sources

The dataset is built from open radio directories and verified public stream lists. Source identifiers and provenance are retained so imported records can be traced back to their origin.

AirwaveDB lists third-party endpoints. It does not proxy or rebroadcast radio streams.