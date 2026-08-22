# Last.fm (lastfm)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
