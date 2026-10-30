# Last.fm

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

Last.fm is the long-running music recommendation, scrobbling, and music-data service operated by CBS Interactive. Its Web Services 2.0 API (the AudioScrobbler API at ws.audioscrobbler.com/2.0/) exposes catalog data (artists, albums, tracks, tags), charts, geo-listening data, user listening history (recent tracks, top tracks/albums/artists, weekly charts), and the Scrobbling 2.0 write surface (track.scrobble, track.updateNowPlaying, track.love). Every operation is dispatched through a single endpoint via the `method` parameter (e.g. `method=user.getRecentTracks`). Authentication uses an API key for reads and a signed (`api_sig`) session-key flow for writes. The API is free for non-commercial use; commercial use requires a separate agreement via partners@last.fm.

**Areas:** Music · Audio · Scrobbling · Recommendations · Charts · Public APIs · AudioScrobbler

## Last.fm on APIs.io

Everything profiled for Last.fm is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/lastfm/](https://apis.io/providers/lastfm/)** — or go straight to one of the APIs or properties below.

### APIs (9)

- [Last.fm Album API](https://apis.io/apis/lastfm/lastfm-album-api/) — Album metadata, tagging, and search.
- [Last.fm Artist API](https://apis.io/apis/lastfm/lastfm-artist-api/) — Artist metadata, similarity, tagging, top albums/tracks, and search.
- [Last.fm Auth API](https://apis.io/apis/lastfm/lastfm-auth-api/) — Token, session, and mobile session acquisition for authenticated calls.
- [Last.fm Chart API](https://apis.io/apis/lastfm/lastfm-chart-api/) — Global top artists, tags, and tracks.
- [Last.fm Geo API](https://apis.io/apis/lastfm/lastfm-geo-api/) — Country-level top artists and tracks.
- [Last.fm Library API](https://apis.io/apis/lastfm/lastfm-library-api/) — A user's scrobbled artist library.
- [Last.fm Tag API](https://apis.io/apis/lastfm/lastfm-tag-api/) — Tag metadata, similar tags, top albums/artists/tracks, and chart history.
- [Last.fm Track API](https://apis.io/apis/lastfm/lastfm-track-api/) — Track metadata, scrobbling, love/unlove, tagging, search.
- [Last.fm User API](https://apis.io/apis/lastfm/lastfm-user-api/) — User profile, friends, listening history, top entities, and weekly charts.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (10)

Multi-step workflows that chain operations into a business task.

- [Last.fm Album Genre Profile](https://apis.io/arazzos/lastfm/lastfm-album-genre-profile-workflow/)
- [Last.fm Artist Discovery](https://apis.io/arazzos/lastfm/lastfm-artist-discovery-workflow/)
- [Last.fm Chart To Album Deep Dive](https://apis.io/arazzos/lastfm/lastfm-chart-to-album-workflow/)
- [Last.fm Genre Artist Explorer](https://apis.io/arazzos/lastfm/lastfm-genre-artist-explorer-workflow/)
- [Last.fm Geo Artist Spotlight](https://apis.io/arazzos/lastfm/lastfm-geo-artist-spotlight-workflow/)
- [Last.fm Loved Tracks Insight](https://apis.io/arazzos/lastfm/lastfm-loved-tracks-insight-workflow/)
- [Last.fm Now Playing Context](https://apis.io/arazzos/lastfm/lastfm-now-playing-context-workflow/)
- [Last.fm Tag To Track Deep Dive](https://apis.io/arazzos/lastfm/lastfm-tag-to-track-workflow/)
- [Last.fm Track Radio Seed](https://apis.io/arazzos/lastfm/lastfm-track-radio-workflow/)
- [Last.fm User Taste Profile](https://apis.io/arazzos/lastfm/lastfm-user-taste-profile-workflow/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Lastfm Agentic Access](https://apis.io/agentic-access/lastfm/lastfm-agentic-access/)

#### JSON Schema (8)

The data models the API reads and writes.

- [Artist](https://apis.io/schemas/lastfm/artist/)
- [Last.fm Album](https://apis.io/schemas/lastfm/lastfm-album/)
- [Last.fm Artist](https://apis.io/schemas/lastfm/lastfm-artist/)
- [Last.fm Tag](https://apis.io/schemas/lastfm/lastfm-tag/)
- [Last.fm Track](https://apis.io/schemas/lastfm/lastfm-track/)
- [Last.fm User](https://apis.io/schemas/lastfm/lastfm-user/)
- [Scrobble](https://apis.io/schemas/lastfm/scrobble/)
- [Track](https://apis.io/schemas/lastfm/track/)

#### JSON Structure (3)

Data models expressed in JSON Structure.

- [Lastfm Album Structure](https://apis.io/json-structure/lastfm/lastfm-album-structure/)
- [Lastfm Artist Structure](https://apis.io/json-structure/lastfm/lastfm-artist-structure/)
- [Lastfm Track Structure](https://apis.io/json-structure/lastfm/lastfm-track-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Lastfm Context](https://apis.io/jsonld/lastfm/lastfm-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Last.fm Music Vocabulary](https://apis.io/vocabularies/lastfm/lastfm-vocabulary/)

#### Examples (9)

Example requests and responses.

- [Artist Getinfo Response](https://apis.io/examples/lastfm/artist-getInfo-response/)
- [Lastfm Album Getinfo Example](https://apis.io/examples/lastfm/lastfm-album-getinfo-example/)
- [Lastfm Artist Getinfo Example](https://apis.io/examples/lastfm/lastfm-artist-getinfo-example/)
- [Lastfm Chart Gettopartists Example](https://apis.io/examples/lastfm/lastfm-chart-gettopartists-example/)
- [Lastfm Track Getinfo Example](https://apis.io/examples/lastfm/lastfm-track-getinfo-example/)
- [Lastfm Track Scrobble Example](https://apis.io/examples/lastfm/lastfm-track-scrobble-example/)
- [Lastfm User Getrecenttracks Example](https://apis.io/examples/lastfm/lastfm-user-getrecenttracks-example/)
- [Track Scrobble Request](https://apis.io/examples/lastfm/track-scrobble-request/)
- [User Getrecenttracks Response](https://apis.io/examples/lastfm/user-getRecentTracks-response/)

#### Collections (11)

Postman and Open Collection request collections.

- [Last.fm Web Services API (2.0) Album API](https://apis.io/collections/lastfm/open-lastfm-album-api/)
- [Last.fm Web Services API (2.0) Album Artist API](https://apis.io/collections/lastfm/open-lastfm-artist-api/)
- [Last.fm Web Services API (2.0) Album Auth API](https://apis.io/collections/lastfm/open-lastfm-auth-api/)
- [Last.fm Web Services API (2.0) Album Chart API](https://apis.io/collections/lastfm/open-lastfm-chart-api/)
- [Last.fm Web Services API (2.0) Album Geo API](https://apis.io/collections/lastfm/open-lastfm-geo-api/)
- [Last.fm Web Services API (2.0) Album Library API](https://apis.io/collections/lastfm/open-lastfm-library-api/)
- [Last.fm Web Services API (2.0) Album Tag API](https://apis.io/collections/lastfm/open-lastfm-tag-api/)
- [Last.fm Web Services API (2.0) Album Track API](https://apis.io/collections/lastfm/open-lastfm-track-api/)
- [Last.fm Web Services API (2.0) Album User API](https://apis.io/collections/lastfm/open-lastfm-user-api/)
- [Last.fm Album API](https://apis.io/collections/lastfm/postman-lastfm-album-api/)
- [Last.fm Web Services API (2.0)](https://apis.io/collections/lastfm/postman-lastfm-openapi-original/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Last.fm — jsonschema rules](https://apis.io/rules/lastfm/lastfm-jsonschema-spectral-rules/)
- [Last.fm API Rules](https://apis.io/rules/lastfm/lastfm-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Lastfm Authentication](https://apis.io/security/lastfm/lastfm-authentication/)
- [Lastfm Domain Security](https://apis.io/security/lastfm/lastfm-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Lastfm Plans Pricing](https://apis.io/plans/lastfm/lastfm-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Lastfm Rate Limits](https://apis.io/rate-limits/lastfm/lastfm-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Lastfm Finops](https://apis.io/finops/lastfm/lastfm-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.last.fm)
- [Documentation](https://www.last.fm/api)
- [Getting started](https://www.last.fm/api/intro)
- [API reference](https://www.last.fm/api/intro)
- [Support](https://support.last.fm)
- [Blog](https://www.last.fm/blog)
- [Terms of service](https://www.last.fm/api/tos)
- [Privacy policy](https://www.last.fm/legal/privacy)
- [GitHub](https://github.com/lastfm)
- [Status](https://x.com/lastfmstatus)

## API Evangelist rating

**Kin Score 54.2** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 62.7 |
| Contract governance | 27.3 |
| Operational transparency | 26.3 |
| Developer ergonomics | 72.6 |
| Access clarity | 50.0 |

**Agent readiness 23.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/lastfm/](https://apis.io/providers/lastfm/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Last.fm: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/lastfm/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
