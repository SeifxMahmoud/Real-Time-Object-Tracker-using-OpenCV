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
