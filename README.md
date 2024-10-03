Indian Currency Detection & Transaction Flow Tracker

A YOLOv8-based model to detect Indian currency and track real-time transaction flow (money in/out of pocket) via live video.


Features

Real-time detection of Indian currency denominations.

Track money transactions.

Supports webcam and video input.


Installation

Clone the repository


Usage

Run with your custom best.pt model:

python detect.py --weights /path/to/your/best.pt --source 0


Run with a video file:

python detect.py --weights /path/to/your/best.pt --source /path/to/video.mp4


Adjust configurations (confidence, IOU):

python detect.py --weights /path/to/your/best.pt --source 0 --conf 0.5 --iou 0.45


Training

To retrain the model with your own dataset, ensure the dataset is configured in data.yaml and run:

yolo task=detect mode=train data=/path/to/data.yaml epochs=100 imgsz=640

Results

Outputs (detected currency, transaction events) are saved in /runs/detect/.
