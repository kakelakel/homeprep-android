# HomePrep Android Data Ownership

## Your preparedness. Your server. Your data.

HomePrep Android is designed as a client of infrastructure controlled by the user.

The app will not require a centralized HomePrep-operated database for core household preparedness data. Its normal architecture is to connect to the user's own HomePrep Server.

## Permanent project commitment

Core private household preparedness data will **not require centralized HomePrep-operated storage**.

A future optional managed HomePrep service may exist, but self-hosted operation must remain supported. HomePrep Android must not intentionally force users into a centrally hosted data model in order to access the core preparedness features.

## Client behaviour

HomePrep Android should:

- clearly show which HomePrep Server it is connected to
- store only the local credentials/cache needed for the app to function
- use secure device credential storage
- support local-network and user-controlled remote endpoints
- make sync and connection state visible
- avoid hidden redirection of household data to HomePrep-operated infrastructure
- avoid mandatory telemetry for core operation

## Offline data

Useful local caching may be added for resilience and offline use, but the app is not intended to become an opaque second source of truth. Offline behaviour should follow the server synchronization contract and make stale or unsynchronized data clear to the user.

## Project rule

> Convenience may be centralized. Ownership must not be.

See the HomePrep Server [data ownership policy](https://github.com/kakelakel/homeprep-server/blob/main/DATA-OWNERSHIP.md) for the broader infrastructure commitment.
