---
icon: command-palette
label: Navigation & Shortcuts
order: 75
---

# Navigation & Shortcuts

| Action | How |
|---|---|
| Open the viewer | **Ctrl + Shift + B** |
| Scrub the timeline | Click or drag on the timeline |
| Step one frame | **←** / **→** |
| Zoom the timeline | **Ctrl** + mouse wheel over the timeline |
| Pan the timeline | Right-click and drag on the timeline |
| Search frames | **Ctrl + F** (see [Search](search.md)) |
| Plain-text dump of the current frame | **T** (with the viewer focused) |
| Copy a Details value | Right-click → **Copy** |

## The text dump

Press **T** to open a plain-text dump of the current frame: active execution indices, Blackboard
contents, and the full node ↔ execution-index mapping. A *Copy to Clipboard* button is provided,
which is usually what you want for a bug report.

![The debug dump window](static/images/bgv_debug_dump.png)

!!! info GIF à produire : `bgv_timeline_scrub`
**À montrer :** Le graphe qui s'allume pendant que le curseur de la timeline se déplace.

**Mise en place :** Charge une capture avec un arbre à plusieurs branches. Enregistre l'écran pendant que tu fais glisser le curseur sur 6 à 10 frames.

**Cadrage :** Le graphe et la timeline ensemble. Moins de 10 secondes et moins de 3 Mo.
!!!

