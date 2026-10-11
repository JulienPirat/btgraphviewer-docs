---
icon: home
label: Home
order: 100
---

# Behavior Tree Graph Viewer

**Replay and inspect Behavior Tree execution after the fact.**

The default Behavior Tree debugger only tells you what an agent is doing *right now*. Behavior Tree Graph Viewer
works from Visual Logger data instead: record a session (or open a `.bvlog` someone else captured),
then scrub a timeline and watch the real Behavior Tree graph light up frame by frame, with that
agent's Blackboard next to it.

![BT Graph Viewer replaying a captured session](static/images/bgv_interface_overview.png)

Useful when the bug happened three minutes ago, on a machine that isn't yours.

| | |
|---|---|
| Engine | Unreal Engine 5.8 |
| Platforms | Editor-only |
| Project type | C++ or Blueprint, no code changes required |
