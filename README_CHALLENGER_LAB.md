# SHINE Challenger Lab — independent updater channel

This branch is **only for the separately installed SHINE Challenger Lab** (`%LOCALAPPDATA%\SHINE-Challenger-Lab`, `Documents\SHINE Challenger Lab`).

- Manifest: https://raw.githubusercontent.com/artstageteam-droid/shine-releases/challenger-lab/latest.json
- The `main` branch remains Claude Stable and must never be changed by Lab work.
- The `chatgpt-beta` branch remains the original combined Studio Challenger beta and must not be overwritten by Lab work.
- As of 2026-11-12, `latest.json` still references **0.90.1**, solely because its SHA-matching ZIP was already verified. It does NOT certify newer Lab candidates or mean the current Lab is outdated.
- To publish a *new* Lab version, publish a complete `shine-X.Y.Z.zip` and verify its SHA-256, install/rollback, CI, and real-user MP4 A/B. **Only then** atomically update `latest.json` to advertise the new version. Never update the manifest first.
- Publishing a Lab candidate without the user's explicit video-quality approval is forbidden; passing CI alone is insufficient.
- The app uses the numeric `parse_version` comparator, so use numeric versions, not SemVer `-beta.N` suffixes.
- The updater is opt-in: the user explicitly clicks `Перевірити оновлення` / `Оновити`; it never silently applies an update.

Legacy Lab 0.90.2/0.90.3 were hardcoded to `chatgpt-beta/latest.json` and require a one-time transition to a version with the new feed (PR #33). Once migrated, future approved updates can arrive in-app without reinstalling.
