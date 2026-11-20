# A handoff that survives another developer

Use this as a content contract, not a demand for seven separate files. A small component can keep most of it in one handoff note.

| Item | Required evidence | Common failure |
|---|---|---|
| Reference observations | Source identifier and visible region/time | Guessing the original tool or code |
| Adaptation decisions | What changed and why it serves this product | Copying the screenshot despite incompatible content |
| Design tokens | Named values used by the implementation | A token JSON that disagrees with CSS |
| Interaction states | Trigger, response, data effect, recovery | A beautiful button that does nothing |
| Asset manifest | Local paths, origin, redistribution status | A ZIP that still needs a private absolute path |
| Integration boundary | Mock/local/remote status, inputs and events | “Saved” with no persistence or acknowledgement |
| Verification | Viewport, action, observation, remaining gap | “Tested” with no record of what was exercised |

## Example state table

| State | Trigger | Visible result | Data effect |
|---|---|---|---|
| Unselected | Initial load/reset | Preview plus an available choose action | No selection |
| Selected | Activate choose | Button and status identify selection | Local in-memory selection |
| Different finish | Select a finish | Preview and selected finish update together | No server write |
| Reduced motion | OS/browser preference | Tilt and animated sheen are suppressed | Same selection behavior |

Do not add artificial errors to a demo with no network request. If integration is requested later, extend the contract around the actual failure modes.

## Minimal final handoff

1. How to start and the single action to try.
2. Which reference features were observed, inferred, and adapted.
3. Token and asset locations.
4. State table and integration seam.
5. What was verified, and what remains unverified.

For an offline claim, test with network access blocked. For an accessibility claim, distinguish keyboard and contrast checks from a full accessibility audit.
