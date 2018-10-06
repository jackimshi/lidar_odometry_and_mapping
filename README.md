[![Build Status](https://travis-ci.org/fferroni/lidar_odometry_and_mapping.svg?branch=master)](https://travis-ci.org/fferroni/lidar_odometry_and_mapping)
[![BCH compliance](https://bettercodehub.com/edge/badge/fferroni/lidar_odometry_and_mapping?branch=master)](https://bettercodehub.com/)

## Description

The repository implements the LOAM algorithm by Zhang et al. (2014) for realtime odometry and mapping using raw LIDAR scans, as a standalone library.

![](docs/animation.gif)

## Dependencies

The repository is build using Bazel. It assumes local repositories for

- OpenCV
- PCL
- Eigen

Please change the locations if necessary in the WORKSPACE file.

On Ubuntu 16.04 dependencies can be fetched with:
```
sudo apt-get update && sudo apt-get install -y libopencv-dev libpcl-dev libeigen3-dev
```

To build:
```
bazel build //...
```

## To Do

- Add some unit / functional tests.
- Remove OpenCV and PCL dependencies, and use just Eigen for portability.
- Add visualization scripts.
- Run with 2-threads (one for odometry, the other for mapping).
