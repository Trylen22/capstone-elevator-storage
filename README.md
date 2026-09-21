# JetMax elevator storage demo

Standalone, dependency-free concept animation. `index.html` is the black pseudo-3D variant with orbit, elevation and overhead views. `original.html` preserves the original flat illustration. This is illustrative geometry, not a dimensioned or validated hardware design.

## Geometry and rendering

The 3D variant uses native WebGL depth testing, fixed-length two-link inverse kinematics, a rear lift mast, and distinct approach/lift/transfer/lower/retract stages. Arm dimensions are illustrative, not JetMax manufacturer specifications.

Regression checks: `NODE_PATH=/path/to/playwright/node_modules node tests/geometry.cjs` (Chrome at `/usr/bin/google-chrome`). Screenshots are written to `/tmp/elevator-tests/`. Tests sample 5,766 poses across storage/retrieval and all three levels, checking link lengths, arm/deck and arm/shelf clearance, stowed travel, and attachment of carried boxes. These checks do not constitute hardware collision or safety validation.
