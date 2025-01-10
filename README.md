# Radar PPI Images Dataset

This repository contains a synthetic dataset of radar Plan Position Indicator (PPI) images and metadata generated as part of our [Radar Simulation Project](https://github.com/MYAzrak/RadarSimulation). The dataset is designed to help users train deep learning models for vessel detection without the need to generate their own dataset from the simulation environment.

## Project Context

This dataset is a crucial component of our [Radar Simulation Project](https://github.com/MYAzrak/RadarSimulation), which aims to enhance maritime surveillance using a simulated radar network integrated with deep learning. The dataset includes radar PPI images along with essential metadata required for training, testing, and evaluating deep learning models such as YOLO and CenterNet.

## Dataset Contents

The dataset is organized into JSON files, each containing:

### 1. Radar PPI Images

- Represented as 2D arrays where each cell stores intensity values based on azimuth and distance.
- These images provide the primary data for vessel detection tasks.

### 2. Metadata

- **Radar ID**: A unique identifier for the radar in the simulation.
- **Timestamp:** The time at which the radar scan was captured.
- **Ship Data**: Ground truth ship locations with bounding boxes.
- **Radar Position**: The coordinates of the radar in the simulation environment.
- **Max Range**: The maximum detection range of the radar.

### JSON Structure Example

```json
{
    "id": 2,
    "timestamp": 1731172429,
    "range": 5000.0,
    "PPI": [
        [0.0, 0.0, 0.0, 0.0, 11.0, 31.0, 131.0, 191.0, ...]
    ],
    "ships": [
        {"Id": -3234, "Azimuth": 10.5, "Distance": 4304.67334, "Bounds": "0 4304.673 10.5 264.1514 242.2614"}
    ],
    "radarLocation": {
        "x": -0.105,
        "y": 100.2,
        "z": -912.826
    }
}
```

### Visualization

- The dataset includes Cartesian and polar representations of PPI images for intuitive understanding and debugging. An example of each is shown below.

![RadarPPIVisualization](https://github.com/user-attachments/assets/3b453fc4-25a9-491d-9fd9-759309b15ba6)

## Dataset Access

- To acquire the whole dataset, download it from "Full Dataset" release or you can get a small sample through cloning this repository.

```bash
git clone https://github.com/MYAzrak/RadarPPIImagesDataset.git
```

## About the Data

The data in this repository was generated using a simulation system that mimics real-world radar operations. Each radar simulation captures vessels in various environmental conditions, including dynamic weather, procedural terrain, and vessel movements. The data is transmitted in real-time from the simulation to onboard software and visualization platforms.

**Key Features:**

- **Scalable**: The dataset can be extended or modified based on simulation parameters.
- **Flexible**: Supports multiple deep learning frameworks and architectures.

## Acknowledgments

This dataset is part of the [Radar Simulation Project](https://github.com/MYAzrak/RadarSimulation) developed by:

- [arcarum](https://github.com/arcarum).
- [Yousif Alhosani](https://github.com/yal77).
- [Mohammad Yaser Azrak](https://github.com/MYAzrak).
- [Ibrahim Baig](https://github.com/darkwing-30).

For more details about the main project, refer to the [Radar Simulation Repository](https://github.com/MYAzrak/RadarSimulation).
