                                                                        **Real-Time Object Detection with Jetson Nano and OpenCV**

This project demonstrates a real-time object detection system using the NVIDIA Jetson Nano, OpenCV, and Jetson Inference Library. The system captures live video frames from a camera, processes them using pre-trained deep learning models, and displays the detected objects in real time.

**Features:**

  Model Selection: Choose from multiple pre-trained object detection models:
  SSD-Mobilenet-v2: General-purpose object detection.
  PedNet: Pedestrian detection.
  SSD-Inception-v2: General-purpose detection with higher accuracy but heavier computation.
  MultiBox: Face detection.
  Real-Time Processing: Processes video streams in real-time, optimized for Jetson Nano's GPU.
  Customizable Detection Threshold: Set a confidence threshold to filter out low-confidence detections.
  Multithreaded Frame Capture: Efficiently captures frames using a separate thread to ensure smooth video processing.
  Bounding Box Visualization: Draws bounding boxes and labels with confidence scores around detected objects.
  
**Requirements:**

  Hardware
  NVIDIA Jetson Nano or any compatible Jetson device.
  USB Camera or any compatible camera module.
  Software
  Python 3.6+
  JetPack SDK (pre-installed on Jetson Nano).
  
**Required Python libraries:**
  OpenCV (cv2)
  NumPy (numpy)
  Jetson Inference (jetson.inference)
  Jetson Utils (jetson.utils)
  Installation
  
**Clone this repository:**

  git clone <repository-url>
  cd <repository-folder>
  
**Install required Python libraries:**

  sudo apt-get install python3-opencv
  pip3 install numpy

**Ensure the Jetson Inference Library is installed:**

  Follow the NVIDIA Jetson Inference Setup Guide.
  Connect your camera to the Jetson Nano.

**Run the script:**

  python3 object_detection.py

**Follow the prompts to select the detection model:**

  Enter 1 for SSD-Mobilenet-v2.
  Enter 2 for PedNet.
  Enter 3 for SSD-Inception-v2.
  Enter 4 for MultiBox.
  The program will start detecting objects and display the live video feed with bounding boxes and labels.

Press q to quit the program.

**How It Works**

  Frame Capture: A separate thread continuously captures frames from the camera for efficient processing.
  Model Initialization: The user selects a detection model from pre-trained options, loaded using the Jetson Inference Library.
  Object Detection: Each frame is processed by the selected model, detecting objects and identifying their class IDs and confidence scores.
  Visualization: The system overlays bounding boxes and labels on the detected objects in the video feed using OpenCV.
  Display Output: The processed frames are displayed in a real-time video window.

**Known Issues**

  Ensure the camera feed URL is correct when using an IP camera.
  Higher-resolution video or heavier models may cause lag; reduce the frame size or FPS to improve performance.

**Future Enhancements**

  Add support for custom-trained models.
  Implement a GUI for easier model selection.
Integrate additional post-processing features like tracking or counting.

Acknowledgments
NVIDIA Jetson Inference Library
OpenCV
Jetson Nano Developer Resources
