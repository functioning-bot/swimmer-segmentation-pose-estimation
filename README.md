# Swimmer Segmentation and Pose Estimation using SAM and YOLO

This project focuses on detecting and analyzing swimmers in video footage using modern computer vision techniques. It combines YOLOv8 for object detection, the Segment Anything Model (SAM) for precise segmentation, and MediaPipe Pose for keypoint estimation. The goal is to develop a system that works reliably in real-world swimming environments, despite challenges like splashing, underwater distortion, and unusual body orientations.

We developed this project as part of an academic exploration into aquatic motion analysis, with a focus on performance tracking and biomechanics research.

## What It Does

- Detects swimmers in video frames using YOLOv8
- Segments swimmers from the pool background using SAM
- Estimates body joint keypoints using MediaPipe Pose
- Outputs segmented video and annotated pose frames for further analysis

## Why Swimmer Pose Estimation?

Analyzing swimming technique can help improve performance, reduce drag, and avoid injury. However, traditional pose estimation tools struggle in aquatic settings due to water interference, variable lighting, and non-standard body positions.

This project aims to provide a more adaptable, computer vision–based solution for swimmer analysis using publicly available models and open-source tools.

## How It Works

The system runs in two main phases:

### 1. Segmentation Phase

- YOLOv8 is used to identify bounding boxes around swimmers in each video frame.
- SAM takes those bounding boxes and produces detailed masks to isolate the swimmer from the background.
- The result is a video showing only the swimmer, with distractions removed.

### 2. Pose Estimation Phase

- The segmented video is processed using MediaPipe Pose, which detects key body joints.
- Each frame is saved with visual annotations showing estimated pose landmarks.
- The resulting data can be used for performance evaluation and technique feedback.

## Components Used

- YOLOv8 from Ultralytics  
- Segment Anything Model (SAM) from Meta AI  
- MediaPipe Pose by Google  
- Python 3  
- OpenCV, NumPy, PyTorch  

## Folder Structure

- `scripts/`: Python scripts for segmentation and pose estimation  
- `models/`: Pretrained weights for YOLOv8 and SAM  
- `input/`: Raw input videos  
- `output/`: Segmented videos and pose-annotated frames  
- `results/`: Sample output data and evaluation results  
- `utils/`: Helper functions for video processing  

## Sample Results

- Segmentation accuracy was around 90%  
- Pose estimation accuracy was approximately 20%, limited by swimmer orientation and water interference  

We also provide:

- A Google Colab notebook for running the pipeline  
- A YouTube demo video of the system  
- A Google Drive folder with result examples  

## Future Ideas

- Improve pose estimation for underwater environments through model fine-tuning  
- Add orientation correction for horizontally positioned swimmers  
- Collect and annotate a larger, swimmer-specific dataset  
- Build a live dashboard for real-time visual feedback  
- Enhance the segmentation model to deal better with splashes and bubbles  

