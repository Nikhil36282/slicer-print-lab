---
name: bambu-a1-print-quality
description: Prepare and refine complex 3D models for good quality printing on the user's Bambu Lab A1 in Bambu Studio, including orientation, supports, slicing, and saved 3MF projects. Use for new model preparation or troubleshooting an A1 print.
---

# Bambu A1 Print Quality

Work with the user to produce a reviewable Bambu Studio project that balances appearance, stability, strength, support removal, and print time. Prioritize good surface quality and reliable printing unless the user specifies another objective. Explain meaningful tradeoffs. Treat settings as a reasoned starting point, then refine from physical print results; do not promise a globally optimal or guaranteed successful print.

## User context and scope

- The user's usual printer is a Bambu Lab A1. Their previous project used a 0.4 mm nozzle, Generic PLA, and Textured PEI. These are prior context, not proof of the installed nozzle or loaded spool for the next print.
- Inspect the current project and confirm material when the actual spool is unknown. Ask only for missing facts that change the decision: decorative versus functional use, important visible faces, material, physical nozzle, target size, fits, and time constraints. Progress on independent inspection while waiting.
- A request to prepare a model authorizes inspection, reversible slicer edits, slicing, and saving a new local project copy. Preserve the original. Starting a physical print or sending a job to the printer requires a specific user instruction; preparation alone does not authorize it.
- Read the available computer-use skill and its referenced guidance before Windows automation. Use its supported runtime and observe/action/refresh workflow. Discover Bambu Studio from returned app/window objects. Do not reuse UI coordinates, indexes, screenshot IDs, or field mappings from an earlier project.
- If desktop activity interrupts input, refresh and retry only after re-observing. If the user stops computer use, stop. When input activity repeatedly prevents work, report what is already applied and what remains; do not silently overwrite the user's concurrent changes.

## Inspect the model before changing settings

Identify the intended model and plate; an open project may contain several unrelated parts. Read dimensions, object overrides, printer/nozzle/plate/filament profiles, process preset, and existing supports. A screenshot alone does not establish manifoldness, fit tolerances, or actual bed contact.

Inspect the geometry for small bed contact, tall narrow sections, boots/hands/weapons, thin walls, downward surfaces, bridges, enclosed cavities, assembly pegs, sockets, and faces that must remain clean. Look for floating geometry, non-manifold warnings, missing surfaces, and disconnected shells. Repair a copy when appropriate; do not merge intentionally separate assembly parts indiscriminately.

For a complicated model, compare the current orientation with plausible alternatives. Decide based on visible-face quality, support scars, support access for removal, bed contact, print height, layer-direction strength, and fit surfaces. Auto-orientation is a candidate to inspect, not an answer to accept blindly. Use a suitable flat face on the bed when available. Confirm the first layer in the sliced preview rather than inferring bed contact from the perspective view.

For tall parts on the A1's moving bed, account for leverage and shaking: a wider footprint, adequate brim/support anchoring, and restrained outer-wall and acceleration settings may matter more than infill. If splitting or cutting would materially improve the print, show the rationale and preserve a copy; ask before altering important assembly geometry or adding connectors when the intended design is unclear.

## Choose settings for the current part

Start from a compatible manufacturer process and filament preset. Retain calibrated temperature, cooling, flow, and retraction unless evidence justifies a change. Verify current official documentation or installed tooltips when parameter behavior or compatibility is uncertain. Do not apply PLA temperatures or support gaps to another material by analogy.

For a decorative PLA figure with a confirmed 0.4 mm nozzle, these are useful initial ranges, not universal defaults:

| Decision | Initial candidate | Adaptation |
|---|---|---|
| Layer height | 0.12–0.16 mm | Favor 0.12 for fabric/face detail; check time and feature size. Variable height can help curved surfaces. |
| Walls | 3 | Increase for functional loads or vulnerable connectors; check tiny features in preview. |
| Infill | 10–15% | Choose gyroid when useful; existing suitable infill need not be changed. Functional parts require load-based choices. |
| Top/bottom shells | Start with compatible preset | Check actual shell thickness as layer height changes, not only layer count. |
| Brim | Outer brim, 8–10 mm for small-footprint tall parts | Wide stable parts may need little or none. Check brim gap and removal around sockets. |
| Support | Tree auto for scattered sculptural overhangs | Normal/snug support can suit broad flat undersides. Compare removal and scarring. |
| Same-material PLA support top gap | Around 0.20 mm | Balance removal against underside finish and effective layer spacing. Never use this automatically for dedicated interface materials. |
| Top support interface | 2–3 layers | Confirm interfaces actually generate under the intended surfaces. |

Use the installed slicer's meaning of threshold angle; angle conventions differ between slicers. Inspect generated support instead of copying a remembered angle. Prefer build-plate-only supports when they reach all required regions; allow or paint supports originating on the model when necessary. Avoid support contact on visible faces and assembly fits where feasible. Check that support is accessible for removal from between limbs and inside cavities. Do not enable support for every slight overhang.

Retain normal printer speeds where suitable; selectively slow outer walls, small perimeters, overhangs, and tall fragile sections when needed. Treat glossy surface consistency, mechanical strength, and decorative detail as different objectives. A smaller nozzle may improve tiny features, but a software profile change is not a physical nozzle swap.

## Verify the slice and saved project

Commit edits by leaving the field before slicing. Confirm the intended value changed; accessibility field IDs/order can change between tabs and may be mislabeled. Refresh after each UI action. Inspect object overrides because global edits may not apply to every part.

Slice and allow the mesh/support calculation to finish. Give concise progress updates for long slices. If window capture fails, rediscover the target and recover using the computer-use guidance. Do not repeatedly slice an unchanged model without reason.

Inspect the preview in Line Type colors and at relevant layers:

- First layer: model contact, brim footprint, support bases, isolated islands, and plate boundaries.
- Critical overhangs: actual support branches and interfaces below them, bridges and their anchors, unsupported starts.
- Thin features and connectors: continuous toolpaths, sufficient walls, missing details, fit surfaces, and excessive seams.
- Support removal: avoid trapped support and check scars on priority faces.
- Stability and collision concerns: tall thin branches, weak support bases, abrupt starts, and unnecessary travel across fragile sections.

A support separation gap is intentional; supports need not visually touch the model in preview. Preview inspection is not a physical print test. Resolve slicer errors and material warnings that affect the result before calling it ready. Compare a second configuration only when there is a meaningful unresolved tradeoff.

Read time and filament estimates from the completed slice. Distinguish model time from total time and note material spent on supports. Check whether timelapse contributes substantial overhead; discuss disabling it when the user values shorter print time, rather than silently changing their preference.

Save a new descriptive .3mf project in the current workspace's user-facing output directory. Verify the file exists and, when feasible, read its embedded project settings to confirm the saved layer height, walls, infill, brim, support options, and material. This read-only check complements the UI preview; object overrides still need inspection. Do not claim a save succeeded from typing a filename alone.

Report the saved project link, key changes and rationale, slice estimates, verification limits, and whether a print was actually started. Keep Bambu Studio on the useful preview. Do not send the print as part of preparation.

## Improve from real print feedback

When the user brings a failed or imperfect print, identify the location, failure height, material, nozzle, plate condition, and relevant settings. Use photos or the model when available. Separate bed adhesion, wobble/collision, missing support, fused support, weak layer bonding, stringing, and geometry issues. Change the few parameters relevant to the evidence and propose a small representative trial when it saves a large repeat print.

For difficult assembly fits or uncertain support release, use a small cut test piece or coupon when useful. Log confirmed outcomes with the material, nozzle, scale, and geometry context only if the user asks to retain them. Update this skill from demonstrated results, not from assumptions or one unverified slice.

## Documentation when needed

Prefer installed Bambu Studio tooltips and official Bambu Lab documentation/source for current parameter behavior:

- https://wiki.bambulab.com/ — current printer, material, and slicer guidance.
- https://github.com/bambulab/BambuStudio — official source and release notes when behavior is unclear.
- https://help.prusa3d.com/article/failing-supports_1807 — general support stability principles; do not transfer slicer-specific angle conventions directly.
