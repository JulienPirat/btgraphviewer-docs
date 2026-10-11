---
icon: history
label: Changelog
order: 10
---

# Changelog

## 1.1.0

### Added

- The viewer is now drivable from an AI assistant through Unreal's **native Toolset Registry**,
  which backs the engine's MCP server and the in-editor AI assistant. Seven tools (`OpenViewer`,
  `LoadCapture`, `ListAgents`, `SelectAgent`, `SetFrame`, `GetFrameInfo`, `GetViewerState`) are
  exposed as `BTGraphViewerToolset`, in a separate optional module (`BTGraphViewerAI`).
- The viewer can now be opened from inside the engine's Visual Logger window:
  **Window → BT Graph Viewer**. It can be docked next to the timeline and log list. The standalone
  tab is unchanged, and both can be open at once.
- Details tab values can be copied with **right-click → Copy**.

### Changed

- New plugin icon.

### Fixed

- Settings saved during a session could not be read back in that same session.
- Picking a missing file, or a file that is not a Visual Logger capture, no longer paints the Output
  Log red.
- Closing the viewer left the Behavior Tree graph registered on the read-only node factory, so the
  normal Behavior Tree editor rendered that tree with read-only nodes afterwards.
- Saving a capture no longer reports success on a write failure, and a truncated file from a failed
  save is deleted.
- `GetViewerState` and the **T** dump now agree with the graph on whether ROOT is active.

## 1.0.0

First public release. Unreal Engine 5.8.

- Replay Behavior Tree execution from Visual Logger data: record live, or open any `.bvlog`.
- Frame-accurate timeline scrubbing with per-frame node highlighting on the real BT graph.
- Per-agent Blackboard view at the selected frame, searchable.
- Agent list with class filter and name search.
- Execution-index badges, decorator/service display toggles, and full color/font customization.
- Optional Gameplay Debugger sync.
- Plain-text frame dump (**T**) with clipboard copy.
- Strictly read-only: displayed Behavior Tree assets are never modified or dirtied.
