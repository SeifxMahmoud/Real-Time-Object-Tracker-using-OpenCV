
# Demo: Untitled - Google Chrome - 23 July 2025 - Watch Video

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/184b9010f8ad4f4481f090085230cc0f?sid=08d38458-84c6-430e-ab92-f303f634ac7a" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>


# Real-Time-Object-Tracker-using-OpenCV

## 🛠️ Implementation Details

This project uses OpenCV’s **CSRT tracker**, a robust object tracking algorithm designed for high accuracy.

1. **Capture Stream**: The program opens the default webcam using `cv2.VideoCapture(0)`.
2. **Frame Read & ROI Selection**: The first frame is extracted, then the user selects an object using `cv2.selectROI`, which pauses and allows mouse selection.
3. **Tracker Initialization**: `cv2.TrackerCSRT_create()` creates a CSRT tracker, which is initialized with the user-defined bounding box.
4. **Tracking Loop**:
   - Frames are captured in real-time.
   - The tracker updates the bounding box location each frame.
   - A rectangle is drawn on the tracked object, and the frame rate is computed using `cv2.getTickCount()`.
5. **Exit Condition**: Pressing the `ESC` key ends the tracking session and releases resources.

The tracker does not perform object detection—it only tracks the object selected in the first frame.

## Project Structure
object-tracker/
├── object_tracker.ipynb     
├── demo.mp4                
├── requirements.txt      
└── README.md      
