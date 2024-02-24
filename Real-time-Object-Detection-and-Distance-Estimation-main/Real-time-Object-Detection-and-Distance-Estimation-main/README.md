# Real-time-Object-Detection-and-Distance-Estimation
Developed real-time object detection system using YOLOv3, estimating distances to detected objects based on known dimensions. Applied OpenCV for webcam feed processing, warning of objects within set proximity. Demonstrates proficiency in computer vision, deep learning, and real-time application development.

#Algorithm
Certainly! Here's an algorithmic representation of the above code:

**Algorithm for Real-time Object Detection and Distance Estimation:**

1. **Initialization:**
   - Set camera properties such as focal length, known object width, maximum distance, and minimum distance warning.
   - Load YOLOv3 weights and configuration.
   - Load COCO class names.
   - Get the output layer names from the YOLOv3 network.
   - Initialize the webcam.

2. **Distance Calculation Function:**
   - Define a function `calculate_distance` that takes the object width (`w`) as input.
   - Calculate the distance using the formula: `distance = (KNOWN_OBJECT_WIDTH * FOCAL_LENGTH) / object_width`.
   - Return the calculated distance.

3. **Obstacle Detection Function:**
   - Define a function `detect_obstacle` that takes the bounding box coordinates (`x, y, w, h`) as input.
   - Calculate the obstacle position (`obstacle_x`, `obstacle_y`) and distance using the `calculate_distance` function.
   - Display the obstacle distance on the bounding box.
   - Generate a warning if the obstacle is within the minimum distance.

4. **Main Loop for Object Detection:**
   - Enter a continuous loop for capturing frames from the webcam.
   - Perform YOLOv3 object detection on each frame.
   - Process the detected objects, store their information, and filter out low-confidence detections.
   - Apply non-maximum suppression to eliminate overlapping bounding boxes.
   - Draw bounding boxes, labels, and confidence scores on the frame.
   - Call the `detect_obstacle` function for each detected object to display distance information and warnings.
   - Display the updated frame in real-time.

5. **User Interaction:**
   - Allow the user to exit the application by pressing the 'q' key.
   - Release the camera and close windows when the loop is terminated.

6. **Conclusion:**
   - The algorithm continuously performs real-time object detection using YOLOv3, calculates distances, and provides warnings based on user-defined parameters.
   - The system displays the processed frames with bounding boxes, labels, and distance information.

This algorithm outlines the key steps and functions involved in the real-time object detection and distance estimation project.

Link to downlaod weights file : https://github.com/patrick013/Object-Detection---Yolov3/blob/master/model/yolov3.weights
