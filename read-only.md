---
icon: lock
label: Read-only guarantee
order: 50
---

# Read-only guarantee

The viewer displays your **real** Behavior Tree asset, not a copy. It is therefore built so it can
never modify it:

- the graph editor is created read-only, and node and pin widgets refuse drag, drop, double-click
  and connection edits;
- decorator/service drag-drop is cancelled before any drop is delivered;
- Delete, Backspace, Ctrl+X and Alt+click are swallowed while the cursor is over the graph;
- any modification that still slips through is reverted;
- the asset's `bEditable` flag and its nodes' read-only flags are never touched, so opening the same
  tree in the normal Behavior Tree editor afterwards behaves exactly as before.

Your Behavior Tree assets are never dirtied and never need saving because you looked at them. An
automation test (`BTGraphViewer.ReadOnly.NoAssetMutation`) enforces this.

## Automation tests

Run from the editor console:

```
Automation RunTests BTGraphViewer
```

or via *Tools → Test Automation*, category `BTGraphViewer`.
