---
name: Bug
about: A defect that made the system behave incorrectly — in a user story, a feature,
  or on its own.
title: "[Bug] "
labels: ''
type: Bug
assignees: ''

---

<!-- Sections marked (Optional) can be deleted when you have nothing for them. Keep every other section, even if brief — the tooling checks they are there.
     This is the org base. Product repositories (cubecos, cubecmp, …) carry a tailored copy whose Environment rows fit the product; the section skeleton is the same. -->

## Description

> A clear and concise description of what the bug is.

Insert content here.

## Version

<!-- Product and the build you saw it on. Build / commit is optional — add it when you have it. -->

- **Product:** e.g. CMP 2.1.1 · COS 3.2.0 · VDI x.y · DPX x.y
- **Build / commit (optional):** e.g. `CUBE_3.1.20_20261007-0229_30d2b166` · portal `2.1.1-53ac5b18b` · `<repo>` `develop` @ `59f8a48a`

## Environment

<!-- Where it was seen and how to get in, one row each; `—` for a row that does not apply.
     Passwords: test accounts only; for anything real, name where the credential is kept instead. -->

| | |
| :-- | :-- |
| **Where** | e.g. testbed `cn13` (`10.231.0.13`) · `https://10.32.42.100/portal/` · CI run |
| **Access** | e.g. project `qatest0914`, account `user3` (affected) / `u2` (works), password `<test>` or "QA vault → cc1" |
| **Component** | e.g. `core/modules/config_kapacitor.cpp` · `portal-api` credential · `cube-cos-ui` node details → GPU Resources |
| **Relevant config** | e.g. Helm `credential.smtp` unset · driver `580.105.06`, kernel `6.12.110` · 3 control + 2 compute |

## How to Reproduce

> For UI bugs, the click path; for backend / API / CLI bugs, the command, API call or code path.

1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

## Expected behavior

> A clear and concise description of what you expected to happen.

Insert content here.

## Root Cause (Optional)

> Skip this if you have not investigated — triage fills it in. If you have traced it:
> the file / function / line, the mechanism, and how you confirmed it (log excerpt,
> code snippet, reproduction).

## Suggested Fix (Optional)

> A concrete fix in mind, even a one-liner.

## Screenshots (Optional)

> If applicable, add screenshots to help explain your problem.

## Additional Context (Optional)

> Anything else: supporting logs, related issues, the device for a browser bug
> (OS, browser, version).

## QA Verification

> How QA verifies this issue is actually fixed — write **checkable claims**: the exact
> command or click path plus the expected outcome. "Verify it works" is not a checkable
> claim. These claims are what the Qase test suite is generated from, so write them for a
> reader who has not seen the code.

| # | Command / steps | Expected outcome |
|---|---|---|
| 1 | `...` | `...` |

- [ ] **QA Status declared at Done** — when this issue reaches `Done`, set the board's
      `QA Status` field to `Not needed` or `Ready to QA`. Never leave it empty on a Done
      ticket; `In QA` / `Verified` are QA's own transitions.

## Output artifacts (Definition of Done)

> Beyond code, docs, and config changes, completing this issue must also deliver:

- [ ] **Handbook knowledge update** — land the durable, team-readable knowledge from this
      work into the bigstack-handbook kb (`kb/<product>/…`) via
      `/bigstack-core:save-to-handbook` (Topic / Runbook / Known-issue / ADR as fits).
      Diagnosed or fixed a failure? Ship the scenario sidecar (`<note>.scenario.yaml`)
      beside the note. Nothing durable to land? Write `N/A (<reason>)` on this line.
