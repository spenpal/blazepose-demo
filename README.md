# BlazePose Demo

A simple demo of MediaPipe's Blazepose model.

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
