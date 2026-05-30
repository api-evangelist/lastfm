# Last.fm (lastfm)

Last.fm is the long-running music recommendation, scrobbling, and music-data service operated by CBS Interactive. Its Web Services 2.0 API (the AudioScrobbler API at `ws.audioscrobbler.com/2.0/`) exposes catalog data (artists, albums, tracks, tags), charts, geo-listening data, user listening history, and the Scrobbling 2.0 write surface.

Every operation is dispatched through a single endpoint via the `method` parameter (e.g. `method=user.getRecentTracks`). Authentication uses an API key for reads and a signed (`api_sig`) session-key flow for writes. The API is free for non-commercial use; commercial use requires a separate agreement via `partners@last.fm`.

**APIs.yml:** [apis.yml](apis.yml)

## Type

- **x-type:** company
- **x-tier:** 3 (bulk-registered from public-apis, then enriched)
- **source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) — category: Music

## APIs

### Last.fm Web Services 2.0

- **Documentation:** https://www.last.fm/api
- **Base URL:** `https://ws.audioscrobbler.com/2.0`
- **Auth:** `api_key` (reads) + `sk` session key + `api_sig` MD5 signature (writes)
- **Formats:** XML (default), JSON (`format=json`)
- **Packages:** Album, Artist, Auth, Chart, Geo, Library, Tag, Track, User
- **OpenAPI:** [openapi/lastfm-openapi-original.yml](openapi/lastfm-openapi-original.yml)

## Artifacts

| Type | Path |
|---|---|
| OpenAPI | [openapi/lastfm-openapi-original.yml](openapi/lastfm-openapi-original.yml) |
| Spectral Rules | [rules/lastfm-rules.yml](rules/lastfm-rules.yml) |
| JSON Schemas | [json-schema/](json-schema/) (album, artist, track, tag, user) |
| JSON Structure | [json-structure/](json-structure/) (album, artist, track) |
| JSON-LD Context | [json-ld/lastfm-context.jsonld](json-ld/lastfm-context.jsonld) |
| Vocabulary | [vocabulary/lastfm-vocabulary.yml](vocabulary/lastfm-vocabulary.yml) |
| Examples | [examples/](examples/) (album, artist, track, chart, recent tracks, scrobble) |
| Plans / Pricing | [plans/lastfm-plans-pricing.yml](plans/lastfm-plans-pricing.yml) |
| Rate Limits | [rate-limits/lastfm-rate-limits.yml](rate-limits/lastfm-rate-limits.yml) |

## Naftiko Capabilities

Per-package capabilities (one per Last.fm method package):

- [capabilities/lastfm-album.yaml](capabilities/lastfm-album.yaml)
- [capabilities/lastfm-artist.yaml](capabilities/lastfm-artist.yaml)
- [capabilities/lastfm-auth.yaml](capabilities/lastfm-auth.yaml)
- [capabilities/lastfm-chart.yaml](capabilities/lastfm-chart.yaml)
- [capabilities/lastfm-geo.yaml](capabilities/lastfm-geo.yaml)
- [capabilities/lastfm-library.yaml](capabilities/lastfm-library.yaml)
- [capabilities/lastfm-tag.yaml](capabilities/lastfm-tag.yaml)
- [capabilities/lastfm-track.yaml](capabilities/lastfm-track.yaml)
- [capabilities/lastfm-user.yaml](capabilities/lastfm-user.yaml)

Cross-package workflow capabilities:

- [capabilities/music-discovery.yaml](capabilities/music-discovery.yaml) — search → similar artists → top tags → tag-pivot → geo lens
- [capabilities/music-scrobbling.yaml](capabilities/music-scrobbling.yaml) — mobile session → now playing → scrobble → love

## Community SDKs

A vibrant community library ecosystem covers Last.fm in JavaScript, TypeScript, Python, PHP, Ruby, .NET (Inflatable.Lastfm), Dart, Elixir, Haskell, Common Lisp, and Java/Spring Social. See `common` SDK entries in [apis.yml](apis.yml).

## MCP Servers

- [ScrobblerContext](https://github.com/tfmart/ScrobblerContext) — Swift Last.fm MCP server with search/library/scrobble tools
- [lastfm-mcp](https://github.com/rianvdm/lastfm-mcp) — Cloudflare Workers Last.fm MCP server with OAuth 2.0

## Notes

- Single dispatch endpoint pattern — all methods are `package.methodName` selected via the `method` parameter
- Free non-commercial tier; commercial use requires an agreement (`partners@last.fm`)
- Documented rate guidance: ~5 req/sec per originating IP; scrobble batches capped at 50/request
- Reasonable Usage Cap: 100 MB stored Last.fm Data per integration
- "powered by AudioScrobbler" attribution required on consuming surfaces

## Tags

Music, Audio, Scrobbling, Recommendations, Charts, Public APIs, AudioScrobbler

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## Maintainers

- **Kin Lane** — kin@apievangelist.com
