# Real-Time-Fall-Detection

## System Overview
This repository contains code for a comprehensive fall detection system that uses a webcam feed to monitor and identify fall events in real-time. Leveraging deep learning models, the system processes each frame of the video to detect human poses and accurately determine if a person has fallen. When a fall is detected, the system triggers an alert using Twilio, a cloud communications platform that enables programmable voice and messaging services.

The code is built around the [YOLOv7-POSE] (https://github.com/WongKinYiu/yolov7/tree/pose "YOLOv7-POSE") model, a  object detection framework that is capable of accurately detecting human keypoints and understanding human postures. By analyzing the positions and movements of different body parts, the model can determine whether a fall has occurred with high accuracy. Once a fall is detected, the system captures the video segment leading up to the event, saves it for review, and overlays visual alerts on the video feed to highlight the detected fall.

## Requirements

- Python 3.x
- OpenCV
- PyTorch
- Twilio
- TQDM
- NumPy
- YOLOv7 pre-trained model weights

## Results


| Accuracy  | Precision | Recall | F1 score |
| ------------- | ------------- | ------------- | ------------- |
|  81.18%  | 83.27% | 83.58%  | 83.42%  |

The performance metrics of the fall detection model were evaluated on a test dataset. These results indicate that the model performs reasonably well in detecting falls with high precision and recall rates.

## How To Use
- Clone this repository into your drive
- Install all the requirements with `pip install -r requirements.txt`
- Configure your Twilio account: Replace account_sid, auth_token, to, and from_ with your Twilio credentials and phone numbers in the make_twilio_call function.
- Run `main.py` file.




