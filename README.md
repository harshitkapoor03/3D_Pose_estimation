# 3D Pose Estimation for Sports Analysis

This project implements a computer vision system for tracking and identifying players in sports footage using 3D pose estimation and person re-identification (ReID). I developed this to explore how we can automatically analyze player movements and positions in team sports like basketball or soccer.

## How It Works

The system combines several computer vision techniques:

1. **Player Detection & Pose Estimation**  
   - Uses YOLO to detect players and estimate their 2D poses  
   - Extracts keypoints (joints) and bounding boxes  

2. **Person Re-Identification**  
   - Generates unique feature vectors for each player using FastReID  
   - Tracks players across frames using similarity matching  

3. **3D Reconstruction**  
   - Triangulates 3D positions from multiple camera views  
   - Applies smoothing to stabilize the 3D skeleton  
   - Validates identities using the ReID features  

## Key Features

- Multi-camera 3D pose estimation
- Player identification across different views
- Temporal smoothing for stable tracking
- Modular pipeline for sports analytics

## Technical Approach

### Pose Estimation
- YOLO-based detection for real-time performance
- Keypoint extraction for body pose analysis

### ReID System
1. Bounding box detection (YOLO)
2. Feature vector extraction (FastReID) 
3. Similarity matching (cosine/Euclidean distance)
4. Identity database management

### 3D Reconstruction
- Camera calibration (intrinsic/extrinsic params)
- Multi-view triangulation
- Weighted moving averages for smoothing
- ReID verification for consistency

## Getting Started

### Prerequisites
- Python 3.6+
- PyTorch
- OpenCV
- YOLOv5 or similar detection model

### Installation
```bash
git clone https://github.com/harshitkapoor03/3D_Pose_estimation.git
cd 3D_Pose_estimation
```

### Usage
Run the main notebook:
```bash
jupyter notebook final.ipynb
```

## Why This Matters

This technology can help:
- Automate sports analytics
- Provide real-time player tracking
- Enable new coaching tools
- Generate advanced statistics

## Current Limitations

- Requires calibrated multi-camera setup
- Challenging in crowded player situations
- Depends on good detection quality

## Future Improvements

I'm working on:
- Better ReID models for sports uniforms
- Real-time optimization
- 3D court/field modeling
- Team-specific analytics

