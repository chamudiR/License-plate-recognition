# License plate recognition

This project implements a License Plate Recognition (LPR) system using YOLOv8 on a Raspberry Pi. The system detects license plates in images or video streams and extracts relevant information for further processing.

Features

 - Real-time License Plate Detection: Utilizes YOLOv8 for object detection.

 - Optimized for Raspberry Pi: Designed to run efficiently on low-power hardware.

 - Custom Model Support: Supports loading pre-trained or custom-trained YOLOv8 models.

 - Easy Integration: Outputs detected license plates for use in other applications.

Installation

Prerequisites

Ensure you have the following installed on your Raspberry Pi:

 - Raspberry Pi OS (latest version recommended)

 - Python 3.11 or later

 - pip and venv for virtual environments

##Setup Instructions

Clone the Repository:
`git clone https://github.com/your-repo/lpr-yolo.git`
`cd lpr-yolo`

Create and Activate a Virtual Environment:
`python3 -m venv my_env`
source my_env/bin/activate  # On Windows, use `my_env\Scripts\activate`

Install Dependencies:
`pip install -r requirements.txt`

Download YOLOv8 Model Weights:
`wget https://github.com/ultralytics/assets/releases/download/v8.0.0/yolov8n.pt`

Run the License Plate Recognition Script:
`python main.py`

##Common Issues and Fixes

ModuleNotFoundError: No module named 'sort'

Install the required package:
`pip install filterpy`

_pickle.UnpicklingError: Weights only load failed
Ensure that your YOLO model weights are correctly downloaded and valid.
Try re-downloading the model:

`rm yolov8n.pt`
`wget https://github.com/ultralytics/assets/releases/download/v8.0.0/yolov8n.pt`

Slow Performance on Raspberry Pi
- Ensure no unnecessary background processes are running.
- Optimize the script by reducing input resolution.
- Consider using a Raspberry Pi-compatible accelerator like Coral TPU.
 
