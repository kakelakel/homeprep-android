# HomePrep Android

HomePrep Android is the planned mobile client for the HomePrep ecosystem.

The app is intended to connect to a user's own **HomePrep Server** rather than depend on a central HomePrep cloud account.

HomePrep Android is currently in the planning/bootstrap phase. No production app is available yet.

## Product direction

The Android app should make HomePrep practical away from the Home Assistant dashboard while preserving the same local-first, user-controlled data model.

The intended model is:

```text
HomePrep Android
      |
      | HTTPS / API
      v
HomePrep Server
      |
      +-- Home Assistant integration
      +-- HomePrep Web
```

The server belongs to the user. The app is a client.

## Planned capabilities

The first useful Android version is expected to focus on:

- connecting to an existing HomePrep Server
- secure client/device pairing
- household readiness overview
- Inventory
- Containers
- Assets
- Tasks and recurring checks
- Plans
- Targets
- Shopping List
- useful offline/cache behaviour where practical
- clear sync state and connection diagnostics

## Pairing concept

The preferred onboarding direction is a simple pairing flow from HomePrep Server or Home Assistant, for example by scanning a QR code containing a temporary pairing token and server information.

The exact security and pairing contract will be defined in HomePrep Server before app implementation is locked down.

## Network model

HomePrep Android should support servers on the user's local network and user-controlled remote access.

HomePrep does not currently plan to require a central relay or HomePrep cloud service. Remote connectivity may initially rely on a secure endpoint configured by the server owner, such as VPN or HTTPS reverse proxy access.

## Relationship to other repositories

- [`kakelakel/homeprep`](https://github.com/kakelakel/homeprep) — Home Assistant integration
- [`kakelakel/homeprep-server`](https://github.com/kakelakel/homeprep-server) — self-hosted server, API and web application
- [`kakelakel/homeprep-android`](https://github.com/kakelakel/homeprep-android) — Android client

The Android app will deliberately follow the server API contract instead of inventing a separate mobile data model.

## Current status

The repository exists now so the Android product track has its own roadmap and history, but implementation should wait until the first HomePrep Server API and pairing model are stable enough to build against.

See [ROADMAP.md](ROADMAP.md) and [CHANGELOG.md](CHANGELOG.md).

## License

HomePrep Android is released under the license included in this repository. See [LICENSE](LICENSE).
