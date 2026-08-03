# ros2_robot

WHEELTEC ROS 2 robot workspace baseline.

This repository was created from the complete workspace deployed on the robot at
`/home/wheeltec/wheeltec_ros2`. The initial baseline was captured on 2026-08-03
before subsequent development work.

## Repository contents

- `src/`: ROS 2 packages and required runtime assets.
- `msc/`: workspace runtime configuration supplied with the robot.
- `map_4911.pgm` and `map_4911.yaml`: map files present at the workspace root.

Generated colcon directories (`build/`, `install/`, and `log/`), Python caches,
runtime logs, and nested Git history from vendored packages are intentionally not
versioned. Large models, meshes, SDK binaries, maps, and recorded data are stored
with Git LFS.

## Clone and build

Install Git LFS before cloning:

```bash
sudo apt install git-lfs
git lfs install
git clone https://github.com/KoAoQ/ros2_robot.git
cd ros2_robot
colcon build --symlink-install
```

Source the workspace after a successful build:

```bash
source install/setup.bash
```

Hardware-specific dependencies, udev rules, ROS 2 Humble, and vendor SDK runtime
requirements still need to be installed on a new machine before all packages can
run.
