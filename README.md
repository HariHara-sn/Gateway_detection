# Gate Surveillance Object Classification using OpenCV and YOLO on Raspberry Pi 
## Overview:
#### This project utilizes OpenCV and the YOLO (You Only Look Once) object detection architecture to classify and monitor objects passing through a gate using recorded video footage. The implementation is optimized for deployment on a Raspberry Pi, making it suitable for real-time video processing applications such as security monitoring and traffic management

## Installation:
### To run the Python code, make sure Python is installed and import the required libraries:
- Numpy
- Opencv
  
## Execution:
Run the program with the following command:
```bash
object_classification.py
```
## Functionality

1. **Initialize YOLO Network**: Load pre-trained YOLOv4 model weights and configuration for object detection using OpenCV’s DNN module.

2. **Video Capture**: Read frames sequentially from a recorded video file.

3. **Object Detection**: Utilize the YOLO network to detect objects in the video frames.

4. **Display Results**: Draw bounding boxes and labels on the original frame, displaying the processed frame in a GUI window using OpenCV.

## Algorithm Steps:

1. **Initialize YOLO Network**: Load the pre-trained YOLOv4 model weights and configuration using OpenCV’s DNN module, tailored to detect objects defined in the COCO dataset.

2. **Video Capture**: Open a video file and read frames sequentially.

3. **Pre-processing**:
   - Convert frames into a blob format to be compatible with the neural network input requirements (normalization, resizing, and channel swapping).

4. **Object Detection**:
   - Pass the blob through the network and retrieve the output predictions from the output layers.
   - Decode the predictions to extract bounding box coordinates, confidence scores, and class IDs for detected objects.

5. **Display Results**:
   - Draw bounding boxes and labels on the original frame.
   - Display the processed frame in a GUI window using OpenCV.

6. **Cleanup**: Release video capture and destroy all OpenCV windows once the script execution is halted.

### Note

- Ensure the correct paths to YOLO weights, configuration files, and video files are provided.
- The algorithm's performance may vary based on the Raspberry Pi model and resources available. Consider using lighter object detection models for improved performance on resource-constrained devices.

## Links:
  ### Download YOLO Weights and Configuration Files
- [Weights ](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4.weights)
- [Config File ](https://github.com/AlexeyAB/darknet/blob/master/cfg/yolov4.cfg)
- [COCO Names File ](https://github.com/pjreddie/darknet/blob/master/data/coco.names)
