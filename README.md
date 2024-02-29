# multiple_color_detection
![image](https://github.com/JohnPaulPrabhu/multiple_color_detection/assets/26264448/6492ad3f-9894-4c6a-ab42-6663b1b2217d)

This Python script leverages OpenCV to detect and identify multiple colors (red, green, and blue) in a video stream in real-time. It employs color masking, contour analysis, and refinements to enhance detection accuracy.

## Technical Details:

### 1. Library:
1. OpenCV (cv2)
2. Numpy
### 2. Color Detection:
1. Converts video frames from BGR format to HSV, which separates color information from luminance, making color detection more robust under varying lighting conditions.
2. Defines accurate color ranges for red, green, and blue in HSV space based on empirical values or experimentation.
3. Applies cv2.inRange to create binary masks for each color, isolating color-specific pixels.
### 3. Noise Reduction and Contour Detection:
1. Uses morphological operations (dilation) to refine mask borders, improve object shape, and reduce noise sensitivity.
2. Employs cv2.findContours to identify object shapes within each color mask.
3. Filters contours based on a minimum area threshold to eliminate noise and focus on relevant objects.
### 4. Bounding Box and Label Drawing:
1. Draws bounding boxes around detected color objects using cv2.rectangle for visual identification.
2. Superimposes color labels ("Red Colour", "Green Colour", "Blue Colour") on top of bounding boxes using cv2.putText for clarity.

## Steps:
1. Replace "bgr.mp4" in the script with the path to your video file.
2. Install OpenCV using pip install opencv-python.
3. Run the script using a command prompt or terminal (e.g., python multiple_color_detection.py).
4. Press 'q' on the keyboard to exit the program.

## Further Enhancements:
1. Additional Color Detection: Define color ranges and incorporate logic to detect more colors beyond red, green, and blue.
2. Adaptive Thresholding: Implement techniques like adaptive thresholding to address lighting variations dynamically.
3. Object Tracking: Explore object tracking algorithms to track the movement of color objects in subsequent video frames.
