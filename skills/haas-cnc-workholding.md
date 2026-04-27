---
name: haas-cnc-workholding
domain: CNC machining
description: |
  Plan CNC setups around restraint, datum strategy, and failure prevention,
  especially for awkward near-net AM parts and one-off R&D fixtures.
status: validated through daily Haas ST-20Y and VF-2 operation
canonical-location: tonykoop/cnc/skills/haas-cnc-workholding.md
also-referenced-from:
  - tonykoop/cnc/SKILLS.md
  - tonykoop/cnc/README.md
  - tonykoop/tensile-testing/README.md
provenance: |
  Derived from self-taught Haas operation at Uniformity Labs, including both
  successful setups and the failures that made the lessons memorable.
audience: human (machinists, manufacturing engineers) + agent
maintainer: Tony Koop
license: CC-BY 4.0
---

# Haas CNC Workholding

> *The first CNC question is not "what toolpath should I use?" It is "what does this part want to do when the cutter touches it, and what holds it against that?"*

## When to use this skill

Use this when:

- the part has limited flat references
- the part came off an AM build plate or other near-net process
- the setup is one-off or low-volume enough that fixture judgment matters more than fixture cost amortization

## Core method

1. Identify the cutting forces that will matter first: pull-out, roll, chatter, jaw slip, wall deflection.
2. Choose the primary restraint strategy before choosing the toolpath.
3. Define the datum surfaces you can trust today, not the ones the final drawing wishes the part already had.
4. Run the program in the air first and reduce feeds on the first real pass.
5. Inspect after the first meaningful cut, not just at the end.

## What this skill emphasizes

- Workholding failure is often more dangerous than programming failure.
- A boring stable setup beats a clever fragile setup.
- Near-net AM geometry changes the fixture problem because the part may not start with machinable datums.
- The setup sheet and notebook matter because tribal knowledge disappears quickly in low-operator environments.

## Failure modes I watch for

- Assuming jaw grip is enough without asking how the cutter will try to peel or rotate the part.
- Referencing off a rough AM surface as if it were already a finished datum.
- Skipping the air run because the CAM looked clean on screen.
- Optimizing feeds and speeds before the restraint strategy is trustworthy.

## Cross-references

- [`cnc/README.md`](../README.md)
- [`tensile-testing`](https://github.com/tonykoop/tensile-testing)
- [`metal-powder-flow-device`](https://github.com/tonykoop/metal-powder-flow-device)
