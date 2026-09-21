# strategy-factory 0.2.1

Date: 2026-09-21. Base: f3f5bcff71baaac791da3320fd09149d4d57adb7. Target: ChatGPT Work.

The user requested strict process adherence and persistent visibility of the active stage and case state.

Changes: mandatory stage/document/save-state line; explicit section statuses; numbered progression with recorded readiness and announced transitions; user-requested deferrals and later-stage entry recorded with limits; save substantive answers before replying. The core is now 67 lines; the package's nine skill files total 139 lines. No executable runtime code.

Validation: native candidate validator and package convention checker passed. A fresh agent resumed a synthetic case with a $100 budget, one hour/week, and missing customer/problem evidence. Its response showed Stage 1 and the linked document's verified save time, stayed at Stage 1, identified blockers, and ended with one next question. The saved document contains all seven section statuses and the supplied constraints. See [actual updated case](raw-0.2.1/process-case.md).

Installation: the updated core was saved and verified byte-for-byte against source. Eight unchanged entry points continue to share the core. Current-session native loading of the new version remains unverified because the reader has retained the earlier snapshot; no reinstallation solely to refresh it.

These are bounded file-based behavior checks, not proof of live case-storage integration or complete-plugin/mobile registration. The previous release's tests and evidence remain in [0.2.0](release-0.2.0.md).

Restore the core and template from the base revision while preserving installed identities.
