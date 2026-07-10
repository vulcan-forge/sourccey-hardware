# Sourccey Hardware

This repository contains CAD models for the Sourccey robot and teleoperator. The models are provided as STEP (`.step`) files for fabrication, prototyping, and 3D-print preparation.

Last updated: July 10, 2026

## Folder structure

```text
.
|-- Robot/
|   |-- Accessories/
|   |-- Arms/
|   |   |-- Gripper/
|   |   `-- Shoulder/
|   |-- Base Plates/
|   |   |-- Dome Level/
|   |   |-- Level 1/
|   |   |-- Level 2/
|   |   `-- Level 3/
|   |-- Dome/
|   |-- Holders and Brackets/
|   |-- Linear Actuator/
|   |-- Walls/
|   |   |-- Hinge Walls/
|   |   |-- Level 1/
|   |   |-- Level 2/
|   |   `-- Level 3/
|   `-- Wheels/
`-- Teleoperator/
```

The folder names describe the assembly or function of each part. Variants such as left/right, mirrored, or level-specific components are identified in the STEP filename.

## Loading STEP files into OrcaSlicer

STEP files are CAD exchange files, not preconfigured print files. Each part must be checked and prepared for the selected printer and material.

1. Open OrcaSlicer and select the printer and filament profile you intend to use.
2. Import a model with **File > Import** (or drag the `.step` file into the build plate). Browse to the relevant folder above and select the part.
3. Confirm the dimensions and units after import. The models are expected to be in millimeters; if the size is incorrect, check the import scale before continuing.
4. Use the orientation tools to place the most suitable face on the build plate. Add supports, a brim, or other adhesion aids when needed.
5. Review the preview after slicing. Check walls, holes, overhangs, and any separate bodies before exporting the G-code.

For an assembly, import the parts individually and arrange them on the build plate. Keep related parts in their original folders so the source files remain easy to identify. OrcaSlicer may convert STEP geometry during import; save a project file if you want to preserve the plate arrangement and slicer settings.

## Documentation

See the [Vulcan Robotics documentation](https://vulcanrobotics.ai/docs) for additional robot documentation and build information.

## Licensing

Unless stated otherwise in a subdirectory, this project is released under the [CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN-OHL-S-2.0)](LICENSE).
This license permits personal, educational, commercial, and manufacturing use. If you distribute a modified design or a product based on it, you must preserve the notices, make the corresponding source available, and license the modified covered source under CERN-OHL-S-2.0. Private modifications do not need to be published unless they are distributed.

Third-party symbols, footprints, models, and datasheets may have separate licenses. Preserve their notices and verify redistribution rights before committing them.

## Disclaimer

This hardware is provided without warranty. You are responsible for reviewing the design, complying with applicable laws and safety requirements, and validating any manufactured or modified hardware before use.
