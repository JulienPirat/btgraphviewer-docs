---
icon: ai-model
label: AI / MCP Toolset
order: 55
---

# AI / MCP Toolset

BT Graph Viewer registers a **native Unreal Toolset**, so any AI client wired into Unreal's Toolset
Registry (the engine's [MCP server](https://dev.epicgames.com/documentation/unreal-engine/unreal-mcp-in-unreal-editor){target="blank"}) can drive the viewer directly. Your AI client
lists it as `BTGraphViewerToolset` among the available toolsets.

Every call drives the same viewer window a human uses. There is no parallel code path, and all of it
stays read-only with respect to your assets.

!!!info Nothing to set up
The toolset lives in the plugin's `BTGraphViewerAI` module and is available as soon as BT Graph
Viewer is enabled. If you never use AI tooling, nothing calls it and you can ignore this page.
!!!

## Requirements

| | |
|---|---|
| Plugins | **BT Graph Viewer**, which pulls in the engine's **Toolset Registry** |
| Engine | Unreal Engine 5.8 |
| Status | Toolset Registry is Experimental |

Toolset Registry ships with the engine but is disabled by default. BT Graph Viewer declares it as a
dependency, so Unreal enables it for you.

## Checking it is available

Enable BT Graph Viewer as usual (see [Getting Started](getting-started.md)) and restart the editor.
In **Edit → Plugins** you will find **Toolset Registry** enabled next to it, turned on for you.

From your AI client, `BTGraphViewerToolset` then shows up in `list_toolsets`.

Typical loop: `LoadCapture` → `SelectAgent` → `SetFrame` → `GetViewerState`. That is enough for an
assistant to walk a capture and explain why an agent did what it did.

<video src="../static/videos/bgv_ai_session.mp4" autoplay loop muted playsinline controls style="width:100%"></video>

## Tool list

### OpenViewer

Opens or focuses the viewer tab.

### LoadCapture

Loads a `.bvlog` and returns the agents it contains.

### ListAgents

Lists loaded agents (paginated).

### SelectAgent

Selects an agent, as clicking it would.

### SetFrame

Moves the timeline to a frame.

### GetFrameInfo

Reports where the timeline sits.

### GetViewerState

Full state: active nodes, Blackboard, and the node ↔ execution-index map.

