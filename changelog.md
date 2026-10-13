# Changelog

## 1.0.0

First release. Unreal Engine 5.8.

- Replay Behavior Tree execution from Visual Logger data: record live, or open any `.bvlog`.
- Frame-accurate timeline scrubbing with per-frame node highlighting on the real Behavior Tree graph.
- Per-agent Blackboard view at the selected frame, searchable.
- Agent list with class filter and name search.
- Open the viewer as a standalone tab or from inside the Visual Logger window (**Window → BT Graph Viewer**), where it can be docked next to the timeline and log list.
- Optional [Gameplay Debugger sync](gameplay-debugger-sync.md).
- Plain-text frame dump (**T**) with clipboard copy.
- Details tab values can be copied with **right-click → Copy**.
- Drivable from an AI assistant through Unreal's native Toolset Registry: seven tools (`OpenViewer`, `LoadCapture`, `ListAgents`, `SelectAgent`, `SetFrame`, `GetFrameInfo`, `GetViewerState`) exposed as `BTGraphViewerToolset`, in a separate optional module. See [AI / MCP Toolset](ai-toolset.md).
- Strictly read-only: displayed Behavior Tree assets are never modified or dirtied.
