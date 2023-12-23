# Visual Odometry

This repository includes a Python script, `main_vo_2.py`, that leverages the `visual_odometry.py` module for visual odometry using homography. The `visual_odometry.py` module introduces the VisualOdometry class, which implements functions for finding matches and computing relative transformations.

## Usage

Execute the visual odometry script using the following command:

python3 main_vo_2.py

# `visual_odometry.py` Module

## Functions

### `homogenized(x: np.ndarray) -> np.ndarray`

Converts a matrix representing coordinates (2D or 3D) into homogeneous form.

### `VisualOdometry(camera_intrinsic: List)`

Constructor for the VisualOdometry class, taking camera intrinsic parameters as input.

### `find_matches(incoming_frame: np.ndarray) -> List[cv2.DMatch]`

Finds matches between key points in the incoming frame and the source frame.

### `compute_relative_transform(matches: List[cv2.DMatch], update_src_frame: bool) -> Tuple[np.ndarray, np.ndarray]`

Computes the transformation mapping points from the source frame to the incoming frame.

### `run(incoming_frame: np.ndarray, update_src_frame: bool = False) -> np.ndarray`

Main function for visual odometry, computing the mapping from the first camera frame to the incoming frame.

## Prerequisites

- OpenCV
- NumPy

### Installation

```bash
pip install opencv-python numpy

