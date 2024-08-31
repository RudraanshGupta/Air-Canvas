# Air-Canvas
Welcome to Air-Canvas, an innovative computer vision project built with OpenCV!

Imagine being able to draw in mid-air simply by waving your finger. With Air-Canvas, this becomes a reality. This project leverages the power of computer vision to track the motion of a colored marker at the tip of your finger and translate it into drawings on a virtual canvas.

I use Python for this project due to its rich set of libraries and straightforward syntax, but the techniques we cover can be applied in any language that supports OpenCV.

The core of Air-Canvas is color detection and tracking. By identifying a specific color marker, I create a mask to isolate the marker’s movement and then enhance this mask using morphological operations: erosion, to clean up noise, and dilation, to restore the mask's shape. I also utilize MediaPipe for efficient hand tracking, enhancing the accuracy of our finger motion detection.

# Algorithm

1. **Capture and Preprocess Frames**:
   - Begin by continuously capturing frames from the webcam.
   - Convert the frames to the HSV color space for better color detection.
2. **Setup the Drawing Canvas**:
   - Prepare the canvas frame.
   - Add interactive ink buttons on the canvas for color selection.
3. **Configure Color Tracking**:
   - Adjust the MediaPipe initialization to detect only one hand.
4. **Contour Detection and Tracking**:
   - Pass the RGB frame to the MediaPipe hand detector to detect landmarks.
   - Extract the forefinger coordinates and store them in an array for tracking.
5. **Draw on Frames and Canvas**:
   - Render the stored coordinates on both the live video feed and the drawing canvas.
   - This creates a visual representation of the user's movements.
6. **Display and Update**:
   - Continuously update and draw the points stored in the array on the frames and canvas.
   - Allow the user to interact and draw using hand gestures.

# Requirements

1. **Python 3**
2. **NumPy**
3. **OpenCV**
Make sure these dependencies are installed on your system.

![Air_canvas_demo](https://github.com/user-attachments/assets/1d7011e6-f953-4040-9f23-efd1b60b0939)


