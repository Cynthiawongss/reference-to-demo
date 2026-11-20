# Prism Pass · synthetic design study

## Request

Create a collectible pass selection for a fictional design fair. Use the supplied original SVG as the visual reference. Preserve a strong diagonal light motif while making the card readable and usable on a phone. Provide two finishes and a reversible local selection. No account, checkout, storage, or network call is needed.

## Evidence and adaptation

| Type | Reference | Decision |
|---|---|---|
| Observed | `reference.svg`, central diagonal bands | Keep a diagonal light motif |
| Observed | `reference.svg`, large pass name and bottom serial | Keep two levels of typography |
| Inferred | Static SVG cannot demonstrate motion | Pointer tilt is our optional interpretation, not a claim about source behavior |
| Adapted | Reference contains only one blue finish | Add violet as a second explicit option |
| Adapted | Reference text is part of SVG | Rebuild labels as accessible HTML text |
| Adapted | Reference has no interaction controls | Put finish and choose/reset controls beside the card, with a live status |

## Acceptable result

- Both finishes update the card without losing selection state.
- Select/reset works by keyboard and touch; focus is visible.
- Selection is labelled local and resets on reload.
- Reduced motion suppresses pointer tilt without removing any action.
- All assets must work offline.

Open `index.html` directly. Read `handoff.md` for the integration boundary. The example is deliberately small enough to understand without a build system.
