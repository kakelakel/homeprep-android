# HomePrep Android

**Your preparedness. Your server. Your data.**

HomePrep Android is the planned mobile client for the HomePrep ecosystem.

The app is intended to connect to a user's own **HomePrep Server** rather than depend on a central HomePrep cloud account.

HomePrep Android is currently in the planning/bootstrap phase. No production app is available yet.

## A permanent data-ownership commitment

HomePrep Android will not require centralized HomePrep-operated storage for core private household preparedness data.

The normal architecture is deliberately simple: **the server belongs to the user; the app is a client.**

Self-hosted support is not intended as a temporary bridge to a mandatory cloud product. Future optional hosted services may exist, but they must remain optional and must not remove the user's ability to use HomePrep with infrastructure they control.

> **Convenience may be centralized. Ownership must not be.**

Read the full client commitment in [DATA-OWNERSHIP.md](DATA-OWNERSHIP.md).

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

The connected server should always be visible to the user. HomePrep Android should not silently redirect household preparedness data to HomePrep-operated infrastructure.

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

HomePrep does not plan to require a central relay or HomePrep cloud service for core use. Remote connectivity may initially rely on a secure endpoint configured by the server owner, such as VPN or HTTPS reverse proxy access.

Local-network-only operation should remain possible for users who intentionally do not want their preparedness system reachable from the public internet.

## Privacy-oriented client behaviour

The Android client should:

- use secure OS-backed storage for device credentials
- clearly identify the connected HomePrep Server
- make sync/offline state visible
- minimize locally cached data to what is useful for the app
- avoid mandatory telemetry for core operation
- never require a HomePrep account merely to connect to a self-hosted server

## Relationship to other repositories

- [`kakelakel/homeprep`](https://github.com/kakelakel/homeprep) — Home Assistant integration
- [`kakelakel/homeprep-server`](https://github.com/kakelakel/homeprep-server) — self-hosted server, API and web application
- [`kakelakel/homeprep-android`](https://github.com/kakelakel/homeprep-android) — Android client

The Android app will deliberately follow the server API contract instead of inventing a separate mobile data model.

## Current status

The repository exists now so the Android product track has its own roadmap and history, but implementation should wait until the first HomePrep Server API and pairing model are stable enough to build against.

See [ROADMAP.md](ROADMAP.md), [DATA-OWNERSHIP.md](DATA-OWNERSHIP.md) and [CHANGELOG.md](CHANGELOG.md).

## License

HomePrep Android is released under the license included in this repository. See [LICENSE](LICENSE).
