# BlazePose Demo

A simple demo of MediaPipe's BlazePose model for real-time human pose estimation.

## About BlazePose

BlazePose is a lightweight, real-time pose estimation model developed by Google's MediaPipe team. It detects 33 3D body landmarks on a person, enabling applications in fitness tracking, motion analysis, augmented reality, and more.

### How It Works

BlazePose uses a two-stage pipeline:

1. **Pose Detection**: A lightweight detector first identifies the presence of human bodies in the image and locates a few key landmarks (similar to MobileNetV2 architecture).

2. **Pose Landmark Tracking**: A more detailed model then tracks all 33 body landmarks in 3D space using the initial detection as a region of interest.

The model uses **GHUM** (a 3D human shape modeling pipeline) to estimate full 3D body pose, providing:

- **Normalized coordinates**: x, y in [0,1] range (image-relative), z as depth relative to hips
- **World coordinates**: Real-world 3D positions in meters with origin at hip center

### 33 Body Landmarks

BlazePose tracks the following 33 landmarks:

```
Face (11 landmarks):
  0: nose
  1-6: left/right eyes (inner, center, outer)
  7-8: left/right ears
  9-10: mouth (left/right corners)

Upper Body (12 landmarks):
  11-12: left/right shoulders
  13-14: left/right elbows
  15-16: left/right wrists
  17-18: left/right pinkies
  19-20: left/right index fingers
  21-22: left/right thumbs

Lower Body (10 landmarks):
  23-24: left/right hips
  25-26: left/right knees
  27-28: left/right ankles
  29-30: left/right heels
  31-32: left/right foot indexes
```

![BlazePose Landmark Topology](https://ai.google.dev/static/mediapipe/images/solutions/pose_landmarks_index.png)

_Image source: [MediaPipe Pose Documentation](https://ai.google.dev/edge/mediapipe/solutions/vision/pose_landmarker)_

## Getting Started

To get started with this project, follow these steps:

### 1. Install uv

This project uses `uv` for dependency management. For installation instructions, please refer to the [official uv documentation](https://docs.astral.sh/uv/getting-started/installation/).

### 2. Set up the Python Environment and Install Dependencies

Navigate to the project directory and create a virtual environment, then install the required dependencies:

```bash
uv sync
```

### 3. Download the BlazePose Model

The project requires the `pose_landmarker_heavy.task` model. Download it from the [MediaPipe models repository](https://developers.google.com/mediapipe/solutions/vision/pose_landmarker/index#models) and place it in the `models/` directory. Create the `models/` directory if it doesn't exist.

### 4. Run the Demo

To run the demo, open and execute the `main.ipynb` Jupyter notebook.
