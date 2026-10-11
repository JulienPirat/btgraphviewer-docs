---
icon: ai-model
label: AI / MCP Toolset
order: 55
---

# AI / MCP Toolset

The plugin registers a **native Unreal Toolset**, so any AI client wired into Unreal's Toolset
Registry (the engine's MCP server, or the in-editor AI assistant) can drive the viewer directly.
Your AI client lists it as `BTGraphViewerToolset` among the available toolsets.

Every call drives the same viewer window a human uses. There is no parallel code path, and all of it
stays read-only with respect to your assets.

!!!info Optional
The toolset lives in its own module (`BTGraphViewerAI`) and the viewer has no dependency on it. If
you never enable AI tooling, nothing changes.
!!!

Typical loop: `LoadCapture` → `SelectAgent` → `SetFrame` → `GetViewerState`. That is enough for an
assistant to walk a capture and explain why an agent did what it did.

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

!!!info Capture à produire : `bgv_ai_session`
**À montrer :** Un assistant qui parcourt une capture : LoadCapture, SelectAgent, SetFrame, GetViewerState.

**Mise en place :** Demande à l'assistant d'expliquer pourquoi un agent a fait quelque chose dans une capture. Laisse-le appeler les outils.

**Cadrage :** La conversation avec les appels d'outils visibles, et la fenêtre du viewer si ça rentre.
!!!

