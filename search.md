---
icon: search
label: Search
order: 78
---

# Search

The Search tab finds every frame of an agent where a condition is true, so you can jump straight to
the moment you care about instead of scrubbing.

Press **Ctrl + F** with the viewer focused to open it.

## Conditions

| Condition | Matches a frame when |
|---|---|
| **Blackboard Key = Value** | The Blackboard key has exactly that value on that frame |
| **Node Reached** | A node whose description contains your pick was active on that frame |

For **Node Reached**, you choose the node from a list built from the selected agent's own recorded
data, so you can only pick a node that exists in that capture.

An empty key or node never matches anything, so a half-filled condition does not flood the list.

## Results

Every matching frame is listed with its frame number and time.

- **Hover** a row to preview it without moving the timeline.
- **Click or double-click** a row to jump to that frame.
- **Multi-select** rows to see them marked on the timeline, in the *Timeline Multi Select Color*
  (see [Settings](settings.md)).

## Searching all agents

**See all agents** runs the same condition on every recorded agent and lists how many frames matched
for each. Double-click an agent to open a new Search tab pinned to that agent, with the same
condition.

The Ctrl + F tab follows whichever agent is selected. A tab opened by drilling down stays on its own
agent, so the original search is never disturbed. You can have several Search tabs open at once.

!!! info Capture à produire : `bgv_search_tab`
**À montrer :** L'onglet Search avec une condition Blackboard et quelques résultats.

**Mise en place :** Appuie sur Ctrl+F. Choisis Blackboard Key = Value, saisis une vraie clé et une vraie valeur de ta capture pour avoir 3 à 6 lignes.

**Cadrage :** L'onglet Search, avec la timeline visible en dessous pour voir les frames trouvées.
!!!

!!! info Capture à produire : `bgv_search_all_agents`
**À montrer :** La vue "See all agents" avec un nombre de correspondances par agent.

**Mise en place :** Même condition que ci-dessus, puis clique sur See all agents. Utilise une capture avec plusieurs agents.

**Cadrage :** L'onglet Search seul.
!!!

