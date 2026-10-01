# Sourccey Mk.V URDF

Open `SourcceyMkV.urdf` with this directory as the model root. Mesh references
are relative to the URDF and use meters after the STL scale is applied.

Contents:
- `SourcceyMkV.urdf`: full robot links and joints.
- `meshes/`: visual and collision STL geometry from the full Fusion assembly.
- `joint_summary.csv`: all movable joint names, link pairs, axes, and limits.

The model has six revolute joints per arm, four continuous wheel joints, and
one prismatic shoulder lift actuator. Joint angles use radians and linear
travel uses meters. The left and right arm joint names have side prefixes.
Shoulder-lift limits are -120 to +120 degrees on the left and -120 to +110
degrees on the right, matching the working full-control scene.
Both full-assembly gripper joints range from -5 degrees closed to +60 degrees
open. These are geometric simulation stops; servo percent stops are configured
in the VR controller and depend on hardware calibration.
