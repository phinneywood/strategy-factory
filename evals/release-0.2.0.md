# strategy-factory 0.2.0

Date: 2026-09-21. Target: ChatGPT Work. Replaces methodology from source revision f35493127839651bc5a9032bfb3cf7f67d7bff8f.

## Changes

Rebuilt the complete method in a 59-line core. Eight 9-line stage entry points reuse it: 131 lines and 1,420 whitespace-delimited words across all nine SKILL.md files. Zero executable runtime code. The new writing entry point joins the eight existing installed identities.

Cases now have one persistent document with seven stage sections. Retain forecasts and authored prose, revise dependent sections, and distinguish recommendations from user decisions. Use named practitioner sources and clearly labeled adaptations; the package is not proven by those sources' reputations.

## Verification

| Gate | Result | Evidence and limit |
|---|---|---|
| Native candidate validation | Passed | All nine actual personal-skill candidates passed quick_validate.py. |
| Portable conventions | Passed | Plugin-factory validator returned ok:true, no errors; not full manifest-schema or security validation. |
| Persistence and source equality | Passed | All nine native instruction files saved and verified equal to this package; per-file hashes in raw-0.2.0/persistence.json. |
| Session discovery | Existing skills visible; new skill unavailable in this snapshot | Native read of the new writing entry point returned “skill package is not available”. |
| Native reader | Cached prior core | Native read returned the previous 40-line core after the new 59-line file was verified stored; no claim of current-session new-version loading. |
| New case behavior | Passed, bounded | Fresh agent read candidate; challenged assumed willingness to pay, asked one consequential question, created seven sections. First run overdeveloped later stages; added one brevity sentence and repeated in a fresh context. Final case: 606 words. |
| Resumption | Passed, bounded | Fresh agent updated supplied case after a pilot missed its adoption threshold. Original forecasts, threshold and author prose preserved exactly; recommendation and dependent claims updated. |
| Writing entry point | Passed, bounded | Fresh agent read bundled entry point and core, fulfilled explicit rewrite request in Assisted drafting mode, created no case. |
| Other hosts and complete-plugin registration | Unverified | No claim of ordinary Chat/iOS or marketplace registration. |

## Raw behavior evidence

All test cases are synthetic. No live customer research, outreach, production actions or external case storage were tested. Temporary case paths were explicitly supplied to the test agents.

- New-case prompt: Develop a neighborhood home-maintenance reminder service; assumed price $15/month because people forget maintenance; create the living case using only supplied information. [Actual document](raw-0.2.0/new-case.md).
- Resume input: intake triage assistant, 80% adoption and 400 hours/quarter forecast; expansion requires at least 70% adoption and no worsening errors; claimed $24,000 cash savings, no staffing reduction, $2,000 estimated operating cost. Author prose: “We should roll this out to all teams. The pilot proves we will save $24,000 every quarter. People want this because it makes work easier.” Update: 25% adoption, projected 100 hours/quarter release, unchanged errors, no comparison group; critique without rewriting. [Actual document](raw-0.2.0/resumed-case.md).
- [Writing request and response](raw-0.2.0/writing.md).

Actual file assertions verified exactly seven numbered sections in both cases; original resumption forecast and expansion threshold retained; author paragraph byte-for-byte unchanged; dependent revision markers present. Live case persistence unavailability and concurrent case edits remain untested behaviors. A transient save conflict during concurrent unrelated skill operations was recovered by staging and saving each operation separately; final equality checks passed.

## Dependencies and recovery

Stage entry points require the core to be readable. Research and durable case access come from the host. No server, database, model pinning or added connector.

Restore the previous skill contents from the base revision while retaining installed identities. Do not remove a skill to roll back its contents.

Invocation: @strategy-factory — develop an idea or resume its living document.
