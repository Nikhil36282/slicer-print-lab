# From model to a useful print record

Use this shared workflow with the current slicer and printer. The existing Codex skill is specific to Bambu Studio and the A1; add separate skills for other tools as they are tested.

## Understand the part

Confirm the physical nozzle, material, size, and plate. Identify visible faces, assembly fits, thin details, and any mechanical loads. Inspect the geometry and slicer warnings before choosing a process.

## Choose an orientation

Compare bed contact, height, support scars, support removal, and layer-direction strength. For an A1, tall parts with small footprints deserve particular attention to stability. Preserve the original project before changing orientation or geometry.

## Tune from a compatible preset

Choose detail and shell thickness for the part. Add supports where they are needed and accessible. Set adhesion for the footprint. Retain calibrated filament settings unless a specific problem calls for a change. For the A1 in Bambu Studio, see the [skill](../skills/bambu-a1-print-quality/SKILL.md) for decision criteria and candidate PLA settings.

## Review speeds and support stability

Record current support, interface, overhang, small-perimeter and outer-wall speeds, plus acceleration and object overrides. A fine layer preset does not establish suitable speeds for fragile supports. Inspect both Line Type and Speed previews at critical layers. Check anchoring, wobble and potential nozzle collisions alongside speed.

For a risky long print, save a baseline and use a small representative trial where practical. Change a targeted group of settings and record the time tradeoff. Live slowdown affects the whole running print; changing slicer settings requires a new slice.

## Inspect the slice

Check the first layer, support bases, critical overhangs, interfaces, thin features, connectors, and trapped support. Read the actual time/material estimate. Confirm settings are saved and object overrides do not defeat intended changes.

## Print and observe

Start printing only after a specific instruction from the user. Record the real result: adhesion, surface detail, support removal, damage, fit, actual time, and any failure height. Use a small representative trial when it can save a long repeat print.

## Improve one decision at a time

Diagnose from evidence, change the relevant settings, and compare similar trials. A successful physical result becomes a print-verified record. An unchanged slice does not add evidence.

Commit messages can be simple:

```text
docs: record figure preparation and support decisions
results: confirm figure print and add removal observations
settings: improve support release after figure trial
resources: add an official guide with a usage note
skill: incorporate a confirmed support stability improvement
```
