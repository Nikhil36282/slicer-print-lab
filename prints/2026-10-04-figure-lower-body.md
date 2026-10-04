# Sculpted figure lower body · 2026-10-04

**Status: Slicer-verified; user-reported print failure — diagnosis pending.**

## Part and objective

A detailed lower-body figure section with clothing folds, boots, and assembly connectors. The objective was good decorative detail with reliable support and easier support removal. The model was kept in its existing orientation: lower connector toward the bed, boots upward.

The model source and redistribution rights were not established. Geometry, the source model, and the full 3MF are not included in this public repository.

## Observed project setup

| Item | Value |
|---|---|
| Printer profile | Bambu Lab A1 |
| Nozzle profile | 0.4 mm, standard flow |
| Filament profile | Generic PLA |
| Plate profile | Textured PEI |
| Process | 0.12 mm Fine @BBL A1, modified |
| Slicer version | Not recorded |
| Real filament brand/type | Not confirmed |
| Physical nozzle/plate | Not independently confirmed |

## Settings and decisions

| Setting | Saved value | Reason / context |
|---|---|---|
| Layer height | 0.12 mm | Retained the Fine preset for fabric detail |
| Wall loops | 3 | Increased from 2 for more robust shells |
| Infill | 15%, grid | Retained existing saved configuration |
| Brim | Outer only, 10 mm | Changed from auto for the small footprint |
| Supports | Tree auto | Retained existing support type |
| Threshold angle | 30° | Existing Bambu Studio setting; not a universal angle recommendation |
| Build plate only | Off | Supports were allowed to originate on the model |
| Top / bottom Z distance | 0.20 / 0.20 mm | Increased from 0.12 mm for support release |
| Top interface layers | 3 | Increased from 2 |

See the [settings snapshot](../settings/figure-lower-body-2026-10-04.json). It records selected settings, not every slicer parameter or a reusable importable preset.

## Verification and estimates

- Slicing completed without a visible error.
- Line Type preview showed support beneath boot overhangs and around the lower section.
- Saved project settings were read back to confirm layer height, wall count, infill, brim, top support gap, and interface layer count.
- First-layer footprint and connector fits were not separately documented at layer level. Verify these before treating this recipe as a benchmark.
- No physical print was started by the assistant, and no physical result was supplied.

| Estimate | Value |
|---|---|
| Model printing time | 11 h 9 min |
| Total time | 12 h 3 min |
| Model filament | 114.93 g |
| Support filament | 19.58 g |
| Total filament | 134.50 g |

The displayed total included preparation and timelapse overhead. Actual duration and filament use are pending.

## After the print

Record bed adhesion, any wobble or collision, support removal force, boot undersides, clothing detail, connector fit, actual time, and filament brand. Add photographs only after checking that they are suitable for public sharing. Update the evidence level after inspecting the result.

## User report and planned retry

The user reported that the active print appeared too fast and was failing in an area requiring support. No failure photo, failure height, actual speeds, or completed retry result has been supplied. Excessive speed is a hypothesis; support adhesion, wobble, nozzle contact, and unsupported geometry remain alternatives.

Review support and interface speeds separately from the model overhang speeds, then inspect support anchoring and critical layers. Preserve the original project and document a targeted slower trial. Suggested speed changes and Silent mode have not been verified as applied or successful. No successful physical print or confirmed fix is recorded.
