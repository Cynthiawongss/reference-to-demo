---
name: reference-to-demo
description: Turn a visual reference into an interactive demo adapted to an existing product, with traceable design decisions, working states, and a usable developer handoff. Use for reference-led UI prototyping or refining a referenced component; do not expand a small visual edit into a full product redesign.
---

# Reference to Demo

Make the useful qualities of a reference work in the user's product. Preserve the requested scope, product vocabulary, business rules, and any preferred implementation. Use the user's language for deliverables.

## 1. Establish what to carry over

Inspect the reference and destination product. If an image, video, URL, or project is unavailable, identify the gap without describing unseen material. Ask only when it prevents a useful next step; otherwise state the assumption and build the smallest requested slice.

| Evidence | Record | Example |
|---|---|---|
| Observed | Source and image region or timestamp | Diagonal bands behind a large pass title |
| Inferred | A plausible mechanism, explicitly a hypothesis | CSS gradients could recreate the surface |
| Adapted | A change and the product reason | HTML labels replace text baked into an image |

A screenshot establishes appearance, not hidden states or original source code. Extract relationships such as hierarchy, contrast, material, and rhythm before copying colors. Reuse the destination's tokens and components. If none exist, define only the tokens the demo needs.

## 2. Define the interaction before styling it

For each relevant action, specify **trigger → visible response → data effect → recovery**. Add states because the behavior needs them, not because a template lists them.

| Behavior | Required distinction |
|---|---|
| Preview or select | Local choice does not mean saved or purchased |
| Remote submission | Pending, success, failure and retry reflect the actual request |
| Disabled action | Explain the business restriction |
| Decorative motion | The same action remains available by keyboard and touch |

If the user asks only for analysis or a wireframe, stop at that deliverable. If building is requested, use the existing stack where practical; standalone HTML is an option for a small portable demo. Use local assets when available and permitted, or identify an original substitute. Do not add a backend to demonstrate a local selection.

## 3. Implement one coherent version

Keep tokens, displayed content, and interaction states consistent. Label mock data and simulated responses. A control should affect the intended state and provide visible feedback; avoid controls that only look interactive.

Motion must preserve readable text, visible keyboard focus, touch access, and reduced-motion behavior. No essential action may depend on hover, pointer precision, or an animation finishing. Preserve the user's accepted direction when revising; change only the requested dimensions and their necessary consequences.

## 4. Verify the journey and the rendered result

Run the core action, a reversal or correction, keyboard access, and relevant wide/narrow layouts. Check real request paths only where integrated. For a selection demo, test selecting, changing an option, clearing selection, and reloading so local persistence is not misrepresented.

Inspect rendered states separately from code and behavior. Compare hierarchy, silhouette, surface, and response to the reference; explain intentional adaptations. Report viewport, action, observed result, and remaining gap. Do not invent fidelity scores or claim visual review without opening the rendered output. An offline claim needs a network-blocked run.

## 5. Hand off at the requested scale

For a full handoff, read [handoff-contract.md](references/handoff-contract.md). Include runnable source, required assets, start instructions, tokens, state behavior, integration boundaries, and verification evidence. A small edit may need only changed files and a short note.

Identify editable source versus generated output, and local/mock/remote behavior versus the next integration step. The recipient should be able to reproduce the core action and tell what was checked. Building a demo does not by itself authorize publishing or changing live backend behavior.

See [Prism Pass](examples/prism-pass/brief.md): an original event-pass design with two finishes, local selection, and a documented integration event.
