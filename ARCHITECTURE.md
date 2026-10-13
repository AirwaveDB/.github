# AirwaveDB Architecture

AirwaveDB separates canonical data from generated consumer-facing output.

```text
external sources
      │
      ▼
  collector
      │
      ├──────────────┐
      ▼              ▼
  database         streams
  station data     playable endpoints
      │              │
      └──────┬───────┘
             ▼
            api
             │
        ┌────┴────┐
        ▼         ▼
     website    clients
```

## Repository responsibilities

| Repository | Responsibility | Canonical |
| --- | --- | --- |
| `database` | Station identity and normalized metadata | Yes |
| `streams` | Playable stream endpoints and stream metadata | Yes |
| `api` | Generated public JSON/NDJSON and HTTP routes | No |
| `checker` | Stream availability and validation | No |
| `website` | Human-facing browser/search/player UI | No |
| `collector` | Source ingestion and normalization | No |
| `.github` | Organization-wide documentation and community files | No |

## Data ownership

`database` answers **what station is this?**

Examples: station ID, name, country, language, category, network, homepage, favicon, aliases and source mappings.

`streams` answers **where can it be played?**

Examples: stream ID, station ID, URL, codec, bitrate, protocol, HLS flag and verification metadata.

`api` answers **how can consumers retrieve it?**

It is generated from `database` and `streams` and is not a source of truth. Generated API files should not be edited manually.

## Primary formats

Canonical station and stream data use JSON. The API publishes JSON and NDJSON. M3U files are compatibility outputs for playlist clients.

The repository boundaries are independent of the serialization format: JSON is used because AirwaveDB records contain arrays and structured fields that do not map cleanly to CSV.
