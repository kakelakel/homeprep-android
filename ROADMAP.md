# HomePrep Android Roadmap

HomePrep Android is the mobile client for the HomePrep ecosystem. It will connect to a user-controlled HomePrep Server and follow the server's public API and sync contract.

This roadmap is directional and may change as HomePrep Server matures.

## Permanent product principle

**Your preparedness. Your server. Your data.**

Core private household preparedness data will not require centralized HomePrep-operated storage.

The Android app is a client of infrastructure selected and controlled by the user. Future optional hosted services may exist, but self-hosted operation must remain supported and first-class.

> **Convenience may be centralized. Ownership must not be.**

See [DATA-OWNERSHIP.md](DATA-OWNERSHIP.md).

## Dependency

Android development intentionally follows HomePrep Server rather than running ahead of it. The app should not invent protocol, sync or authentication behaviour that the server has not standardized.

## Phase 1 — Client foundation

- Choose the Android application stack and minimum supported Android version.
- Establish project structure, CI and release signing approach.
- Define secure local storage for server credentials/tokens.
- Implement server URL configuration and connectivity checks.
- Implement the first API client generated or aligned from the HomePrep Server contract.
- Make server identity visible in the client from the beginning.

## Phase 2 — Pairing and authentication

- Pair a device with HomePrep Server using a short-lived token.
- Prefer QR-based onboarding where practical.
- Store per-device credentials securely.
- Support logout/revoke/re-pair flows.
- Display server identity and connection status clearly.
- Require no central HomePrep account for self-hosted pairing.

## Phase 3 — Read-only HomePrep client

- Household readiness overview.
- Inventory list/details.
- Containers.
- Assets.
- Tasks.
- Plans.
- Targets.
- Shopping List.
- Sync/connection status.

This phase proves the full Server → Android data path before write operations are enabled broadly.

## Phase 4 — Everyday workflows

- Add and edit Inventory.
- Complete Tasks and recurring checks.
- Mark Assets and Containers checked.
- Work with Shopping List entries.
- Confirm/review Plan checklist items.
- Update Targets where supported.

## Phase 5 — Resilience and offline behaviour

- Local cache for useful read access during temporary network loss.
- Clear stale/offline indicators.
- Queue safe offline operations where the sync contract supports them.
- Conflict presentation when an automatic resolution would be unsafe or confusing.
- Keep offline storage understandable and subordinate to the user's selected server rather than becoming an opaque second data silo.

## Phase 6 — Mobile-native features

- Optional notifications driven by HomePrep Server capabilities.
- Camera/image workflows only after the shared media/privacy model is ready.
- Barcode/QR-assisted workflows where useful.
- Home-screen shortcuts/widgets if they add practical value.

## Phase 7 — Polish and broader release

- Accessibility review.
- Localization.
- Battery/network efficiency.
- Tablet/layout support where useful.
- Production release process and store distribution decisions.

## Non-negotiable client constraints

- No mandatory HomePrep-operated cloud account.
- No mandatory central HomePrep data store.
- No hidden redirection of private household data to HomePrep infrastructure.
- No mandatory telemetry for core operation.
- Self-hosted local-network use must remain possible.
- The user must be able to identify which server the app is connected to.

## Non-goals for the first releases

- Maintaining a separate mobile-only HomePrep database model.
- Building social/community or messaging features into the preparedness client.
- Hiding sync/server status from the user.

## Related projects

- [`kakelakel/homeprep-server`](https://github.com/kakelakel/homeprep-server) — server/API dependency
- [`kakelakel/homeprep`](https://github.com/kakelakel/homeprep) — Home Assistant client/integration
