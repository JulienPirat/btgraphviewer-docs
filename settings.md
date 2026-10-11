---
icon: gear
label: Settings
order: 60
---

# Settings

Click **Settings** in the toolbar to open the settings window. Click it again to close it.

The window is the engine's standard property grid, so it has collapsible sections and a search box
at the top. Every change is **saved and applied immediately**: the graph and the timeline redraw as
soon as you edit a value. **Reset to Defaults** (top right of the window) restores everything.

Settings are grouped in three categories.

## Timeline

Colors used by the timeline bar at the bottom of the viewer.

| Setting | What it colors |
|---|---|
| Timeline Background | Background of the timeline bar |
| Timeline Snapshot Marker Color | One marker per captured frame. Defaults to the native Visual Logger marker color |
| Timeline Cursor Color | The cursor showing the frame currently displayed |
| Timeline Cursor Glow Color | The soft glow around the cursor |
| Timeline Multi Select Color | Frames multi-selected in a [Search](search.md) results list, mirrored onto the timeline |
| Timeline Tick Color | The vertical tick lines |
| Timeline Tick Label Color | The time labels next to the ticks |
| Timeline Info Text Color | The text in the timeline's info line |

## Blackboard

| Setting | What it colors |
|---|---|
| Blackboard Key Color | Key names in the Blackboard panel. Defaults to the native Visual Logger status view color |
| Blackboard Value Color | Values in the Blackboard panel |

## Behavior

| Setting | Default | What it does |
|---|---|---|
| Enable Graph Change Revert | On | Any graph modification (node move, connection, etc.) is automatically reverted, to keep the graph read-only. See [Read-only guarantee](read-only.md) |
| Sync With Gameplay Debugger | Off | The viewer follows the actor selected in the Gameplay Debugger. See [Gameplay Debugger sync](gameplay-debugger-sync.md) |
| Confirm Before Clear | On | The **Clear** button asks for confirmation before wiping captured or loaded data. There is no undo, so turn this off only if the prompt gets in your way |

!!! warning
Leave **Enable Graph Change Revert** on unless you have a reason not to. It is one of the layers that
keeps your Behavior Tree assets from being modified.
!!!

## Where settings are stored

Settings are stored per project in:

```
<YourProject>/Saved/Config/BTGraphViewerSettings.ini
```

Nothing is written inside the plugin folder, so engine-level installs (which are read-only) work.

![The Settings window with its three categories](static/images/bgv_settings_window.png)

!!! info Capture à produire : `bgv_settings_timeline`
**À montrer :** Le sélecteur de couleur d'Unreal ouvert pour changer une couleur de la timeline.

**Mise en place :**
1. Ouvre la fenêtre Settings (bouton Settings de la barre d'outils).
2. Dans la catégorie Timeline, clique sur le rectangle de couleur à droite de "Timeline Cursor Color". Une fenêtre avec une roue de couleurs s'ouvre.
3. Laisse-la ouverte et fais la capture.

**Cadrage :** La fenêtre Settings avec le sélecteur de couleur ouvert à côté, dans la même image.
!!!

