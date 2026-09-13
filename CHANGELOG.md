# HomePrep Android Changelog

All notable project-level and user-facing changes to HomePrep Android will be documented here.

## Unreleased

### Added
- Initial HomePrep Android repository and product definition.
- Self-hosted server client direction with no required central HomePrep cloud account.
- Permanent data-ownership commitment documented in `DATA-OWNERSHIP.md`.
- Explicit rule that core private household preparedness data will not require centralized HomePrep-operated storage.
- Initial roadmap covering pairing, read-only validation, everyday workflows, offline behaviour and mobile-native features.

### Changed
- README and roadmap now require visible server identity, user-controlled endpoints, no mandatory telemetry for core operation and no hidden redirection of household data to HomePrep-operated infrastructure.

### Planned next
- Wait for the first stable HomePrep Server API/authentication contract.
- Choose the Android application stack.
- Bootstrap the app project and CI once the server contract is ready for client development.
