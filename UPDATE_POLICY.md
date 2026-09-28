# Public Site Update Policy

This repository is the public-facing summary for KimKong / Buddy Agent K. Product implementation and release evidence remain authoritative in the private product repository.

## Source of truth

For KimKong iOS status, verify the following in `buddy-agent-k/buddy` before changing public release copy:

1. `apps/react-pocket/app/app.json` — current source version/build.
2. `apps/react-pocket/release/ios/build-history.md` — TestFlight, App Store review, release evidence, and manual verification boundaries.
3. Current harness / canonical release plan — near-term planned work.

Do not infer App Store release completion from a merged PR, build number, TestFlight upload, or App Store review submission alone.

## Public status labels

Use these meanings consistently:

- **Released / 출시** — confirmed publicly available App Store version only.
- **In Review / 심사 중** — submitted to App Store review but not confirmed released.
- **TestFlight / 테스트 중** — distributed for testing but not a public App Store release.
- **Planned / 계획** — documented future work; never present it as an available feature.

## When this site must be updated

Update the public site when any of these happens:

1. A new App Store version is confirmed released.
2. A release candidate materially changes the user-visible product direction.
3. A major capability is added or removed (for example companion tools, voice, widgets, supported platforms).
4. Privacy, support, model/license notices, or external-service boundaries change.
5. The canonical near-term roadmap changes enough that the public Journey page would become misleading.

A build-number-only change with no user-visible significance does not require a public-site update. The Journey page is milestone-based, not a build-by-build changelog.

## What to update

- `index.html`: current public product positioning and major available/current-development capabilities.
- `journey/index.html`: milestone-based product history and clearly labeled roadmap. Do not add one timeline item per build.
- `privacy/`, `support/`, `notices/`: update whenever their underlying policy or legal/technical facts change.
- `README.md`: keep the source-of-truth and update-policy pointers current.

## Guardrails

- Never advertise an unimplemented feature as available.
- Keep Voice, Widget, iPad/Mac expansion, and other future capabilities under **Planned** until their release evidence exists.
- Do not publish private build IDs, archive paths, device IDs, credentials, private conversation text, or internal-only diagnostics.
- Summarize meaningful user-facing changes; do not mirror the full internal build log.
- If repository evidence and App Store Connect disagree, treat release status as unverified until manually confirmed.

## Current baseline

As of 2026-09-28:

- Current public App Store release: **KimKong 1.0.3**.
- Public Journey history is organized by product milestones rather than internal build numbers.
- Next documented work includes Tool Discovery, Voice UX (STT + TTS), Local Capability Bridge v1 PoC, and regression/integration validation.
