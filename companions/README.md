# Optional companion source

`investigate-prior-art/` preserves the existing standalone prior-art skill from `phinneywood/chatgpt-plugins@ab571a5c74d481a1efe4bd6e585d6f022ae87f01`, with its MIT license. The main Strategy Factory package remains Apache-2.0.

## Compatibility gate

The preserved companion delegates to section 2 of an older installed `strategy-factory` coordinator and explicitly says not to run every stage. This repository's current 0.3.0 coordinator delegates Stage 2 to `evidence-and-alternatives`, which requires a completed Stage 1 case. Those contracts differ.

The companion is intentionally staged outside `skills/` so it does not enter the current eight-skill plugin package. Before activation or replacing its source pointer, adapt it to the current standalone-research contract, test standalone research and gated-case routing, and verify the installed identity. Keep the old installed skill and source available while this gate remains unresolved.

This change saves the source beside its project; it does not claim a compatible bundled or installed upgrade.
