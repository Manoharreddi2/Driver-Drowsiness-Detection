This project is a real-time drowsiness detection system that uses computer vision to monitor the Eye Aspect Ratio (EAR) to detect signs of fatigue and alert the user with a sound if drowsiness is detected.

🧠 How It Works
Uses a webcam to continuously capture video frames.

Detects facial landmarks using dlib's 68-point facial landmark detector.

Calculates the Eye Aspect Ratio (EAR) for both eyes.

If the EAR is below a set threshold for a defined number of consecutive frames, an alert is triggered.

A sound is played using pygame.mixer to wake the user up.

🛠️ Requirements
Python 3.x

OpenCV

imutils

dlib

pygame

scipy

📦 Install Dependencies
bash
Copy
Edit
pip install opencv-python imutils dlib pygame scipy
Note: You need to install CMake and Visual Studio Build Tools for compiling dlib on Windows.

📁 Files
drowsiness_detection.py: Main detection script.

shape_predictor_68_face_landmarks.dat: Pre-trained facial landmark detector from dlib. Download here

music.wav: Sound file that plays when drowsiness is detected.

README.md: Project documentation.

▶️ How to Run
Download the required .dat file and place it in the same directory as your script.

Ensure your webcam is connected.

Run the script:

bash
Copy
Edit
python drowsiness_detection.py
Press q to exit the program.

⚙️ Parameters
thresh: EAR threshold to detect eye closure (default: 0.25)

frame_check: Number of consecutive frames the EAR must be below the threshold before triggering an alert (default: 20)

You can adjust these parameters based on your environment and camera setup.

📸 Output
Green contours around detected eyes.

Red alert messages when drowsiness is detected.

Alarm sound plays using music.wav.
