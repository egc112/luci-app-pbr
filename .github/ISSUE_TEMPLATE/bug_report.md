---
name: Bug report
about: Report a bug in the LuCI front-end for pbr
title: "[luci-app-pbr] "
labels: bug
assignees: stangri

---

**Is this a LuCI bug or a service bug?**

LuCI is just the web UI; the actual work is done by the [pbr](https://github.com/stangri/pbr) service. Quick triage:

- Page won't render / a control does nothing / Save & Apply produces a JS error → **LuCI bug**, file here.
- After Save & Apply, `uci show pbr` shows the wrong values → **LuCI bug**, file here.
- Settings save correctly (you can verify with `uci show pbr` after Save & Apply) but the service still misbehaves → **service bug**, please file at [stangri/pbr](https://github.com/stangri/pbr/issues) and include the diagnostics from that repo's bug template (or the output of `service pbr support`).

**Describe the bug**

What you saw in the UI.

**To reproduce**

1.
2.

**Versions**

- OpenWrt: (`ubus call system board`)
- `luci-app-pbr`: (`apk list -I luci-app-pbr` or `opkg list-installed | grep luci-app-pbr`)
- `pbr`: (same, for the underlying package)
- Browser:

**Browser console output**

Open browser dev tools (F12) → Console tab. Paste any errors that appear when you reproduce the bug.

**Screenshot**

If applicable.
