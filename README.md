# color_detection
this is to detect a particular color in an image or video
this is also my beginner project for computer vision engineer.

Explanation of util.py
The util.py script defines the get_limits function, which calculates the HSV (Hue, Saturation, Value) color range for a given BGR (Blue, Green, Red) color. This range is crucial for detecting specific colors in an image or video.

Key Features:
Libraries Used: Utilizes numpy for array manipulation and cv2 (OpenCV) for image processing.
BGR to HSV Conversion: Converts BGR to HSV using cv2.cvtColor for better color segmentation.
Hue Extraction: Extracts the hue value from the HSV color.
Red Hue Handling: Special cases for red hue wrap-around in the HSV scale.
Returning Limits: Provides lower and upper HSV limits for the input BGR color.
Explanation of color_detection.py
The color_detection.py script captures live video from the webcam, detects a specific color (yellow), and highlights it with a bounding box in the video stream.

Key Features:
Libraries Used: Uses OpenCV for video processing, PIL for image manipulation, and get_limits from util.py.
Target Color: Defines yellow in BGR format [0, 255, 255].
Video Stream Setup: Initializes video capture with OpenCV.
Frame Processing:
Captures and converts frames to HSV.
Computes HSV limits for yellow using get_limits.
Mask Creation: Generates a binary mask to highlight yellow pixels.
Bounding Box Detection: Uses PIL's getbbox to find and draw bounding boxes around detected areas.
Display and Exit: Shows the mask and original frame with bounding boxes until 'q' is pressed to exit.

