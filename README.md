# Sourccey Hardware

Open-source mechanical hardware files for a robot platform and matching teleoperator assembly.

Last Updated: 04/21/2026

## Overview
This repository contains CAD source files (`.step`) for two major systems:
- `Robot/`: robot body, arms, dome, holders, linear actuator parts, and accessories.
- `Teleoperator/`: teleoperator enclosure and arm/control components.

The files are organized as printable/manufacturable part-level CAD assets and are intended for review, iteration, and fabrication workflows.

## Repository Structure
```text
.
|-- Robot/
|   |-- Accessories/
|   |-- Arms/
|   |-- Base Plates/
|   |-- Dome/
|   |-- Holders and Brackets/
|   |-- Linear Actuator/
|   |-- Print Modifiers/
|   |-- Walls/
|   `-- Wheels/
|-- Teleoperator/
|-- .gitattributes
`-- README.md
```

## Git LFS
This repository uses Git LFS for large CAD assets.

### Install and initialize (Bash)
```bash
# Install (Windows)
winget install --id GitHub.GitLFS -e

# In repo
git lfs install
```

### Track CAD files with LFS
```bash
git lfs track "*.step" "*.stp" "*.stl" "*.zip" "*.pdf"
git add .gitattributes
git commit -m "Configure Git LFS tracking"
```

### Verify
```bash
git lfs ls-files
```

## Getting Started
1. Clone the repository.
2. Ensure Git LFS is installed and initialized (`git lfs install`).
3. Pull LFS objects:
   ```bash
   git lfs pull
   ```
4. Open `.step` files in your preferred CAD tool (for example: FreeCAD, Fusion 360, SolidWorks, Onshape import).

## Contributing
Contributions are welcome. Suggested workflow:
1. Create a feature branch.
2. Add or update CAD parts in the relevant subsystem folder.
3. Keep names descriptive and subsystem-scoped.
4. Commit and open a pull request describing intent, fit, and any print/manufacturing notes.

## Naming and Organization Guidelines
- Keep related parts grouped by subsystem directory.
- Prefer stable, descriptive filenames (avoid temporary suffixes like `final2` or `new`).
- When replacing a part, preserve path/filename when possible to reduce downstream breakage.

## Status
Active development. Geometry, fit, and part naming may change as the robot evolves.
