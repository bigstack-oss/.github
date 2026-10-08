# bigstack-oss/.github

The organisation's **default community health files**. GitHub serves what is in `.github/`
here to every `bigstack-oss` repository that has no file of its own:

| Path | Serves |
|---|---|
| `.github/ISSUE_TEMPLATE/` | the issue chooser — one template per ticket type of the [scrum-board ticket standard](https://github.com/bigstack-oss/bigstack-handbook/blob/develop/kb/bigstack/workflows/scrum-board-ticket-standard.md) (Epic, User Story, Feature, Task, Bug, Spike) plus the Support feature-request form and the security-report form |
| `.github/PULL_REQUEST_TEMPLATE.md` | the pull-request body: Summary · Closes · QA (`QA-Status:`) · Test evidence · Notes for the reviewer |
| `profile/README.md` | the organisation profile |

## Two tiers

**Tier 1 — the base, served from here.** Every repository without a tailored need gets this
set as is: libraries, tools, docs, the long tail. The five process templates (Epic, User Story,
Feature, Task, Spike) are the same everywhere by design — they are the standard's artifacts,
not a product's.

**Tier 2 — a product's own set.** A product repository (cubecos, cubecmp, lachesis, …) keeps a
local `.github/ISSUE_TEMPLATE/` and PR template: **this base plus its own `bug.md` and
`PULL_REQUEST_TEMPLATE.md`**. A COS bug names a build string, a topology and a component; a CMP
bug names a URL, a project and an account; cubecmp's PR template adds `QA-Verify:` for its
build bot. GitHub overrides issue templates *per directory*, so a tier-2 repo carries the whole
set locally — which is why the base must stay the skeleton of every local copy.

**What keeps tier 2 honest:** the *skeleton* is the contract — the `##` sections, the QA
Verification block on Story/Feature/Bug, the Output-artifacts checkbox on all. Rows, examples
and wording inside a section are the product's. `handbook templates check` compares a repo's
local set to this base by skeleton and flags drift, the way `handbook dod` flags a missing
note; `handbook ticket create` validates a body against the repo's own template first, then
this base — GitHub's own precedence.

## Changing a template

Open a PR against `develop`. Keep: the `type:` in every issue template's front matter (the
org issue type, not a label), the `## QA Verification` section on User Story / Feature / Bug,
and the `## Output artifacts (Definition of Done)` checkbox on all. Line endings are LF. A
skeleton change here is a change for every tier-2 copy — say so in the PR, and open the
follow-up PRs in the product repos.
