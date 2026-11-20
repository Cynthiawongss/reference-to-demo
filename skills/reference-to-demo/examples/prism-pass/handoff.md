# Prism Pass handoff

Open `index.html` in a modern browser. No build, CDN, external font, storage, or server is needed. Select a finish, choose the card, change its finish, then reset.

## Source and integration

`index.html` is editable source. `reference.svg` is an original synthetic reference; CSS gradients are an interpretation, not a recovered source technique. `design-tokens.json` records the token values used by this example. All sample assets were created for this repository.

The HTML exposes a `pass-change` CustomEvent on `document`, with `{finish, selected}` in `detail`. An integrating application may listen to that event and handle persistence according to its own API. The demo itself performs no save. State is in memory and resets on reload.

| Action/state | Expected result |
|---|---|
| Initial | Blue finish; no selection |
| Violet radio | Violet appearance; selected state unchanged |
| Choose | Local selection message; button disabled until reset |
| Change finish after choosing | Selection message follows the chosen finish; one event emitted |
| Reset | Selection cleared, chosen finish retained, focus returns to choose |
| Keyboard | Native radios and buttons support tab/arrow/space/enter; focus visible |
| Pointer movement | Decorative tilt, capped at six degrees |
| Reduced motion | No tilt or transition; choose/reset still works |
| Reload | No selection; default blue finish |

The generated sample sends no analytics or telemetry. This is a component study, not a complete product. See the repository validation report for observed checks; this table describes intended behavior.
