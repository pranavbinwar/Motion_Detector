# Motion_Detector
This code is a Python script that uses the threading module to create a separate thread for playing an alarm sound while monitoring the video feed from a webcam. The script uses the OpenCV library (cv2) and the winsound module for sound playback.

Prerequisites
Before running this script, make sure you have the following installed:

Python 3.x
OpenCV (cv2)
imutils library
winsound library
You can install the required libraries using pip:

Copy code
pip install opencv-python imutils
Usage
Connect a webcam to your computer.

Run the script using the following command:

Copy code
python script.py
The webcam feed will be displayed in a new window titled "Cam".

Press the "t" key to toggle the alarm mode. In alarm mode, the script compares the current frame with the initial frame and detects motion. If motion is detected, an alarm counter is incremented. If the alarm counter exceeds a threshold value, an alarm sound is played.

Press the "q" key to quit the script.

Important Notes
Make sure you have the necessary permissions to access the webcam device.
Adjust the webcam resolution by modifying the cap.set function calls with your desired width and height values.
The script uses a grayscale image for motion detection. If you want to use color images, remove the line frame_bw = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY) and modify the subsequent code accordingly.
The script uses a Gaussian blur to reduce noise in the image. Adjust the (21, 21) and (5, 5) values in the cv2.GaussianBlur function calls if needed.
The alarm sound is played five times in a loop. You can modify the number of repetitions and the frequency/duration of the beep sound by changing the parameters in the winsound.Beep function call within the beep_alarm function.
Adjust the alarm counter threshold (if alarm_counter > 20) to change when the alarm is triggered.
License
This code is licensed under the MIT License. Feel free to modify and distribute it as needed.
