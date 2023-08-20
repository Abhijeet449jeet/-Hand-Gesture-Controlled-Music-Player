# -Hand-Gesture-Controlled-Music-Player
and gesture-controlled music player project that detects gestures and triggers sounds based on those gestures

This code is a Python script that utilizes the Mediapipe and OpenCV libraries to create a hand gesture-controlled music player. The script captures the video from the webcam, detects hand landmarks and gestures using the Mediapipe library, and triggers different sounds based on the gestures detected by the hand.

**Libraries Used:**

- `mediapipe`: A library developed by Google that provides tools for building applications that can perceive human hands, face, and body movements in real-time.
- `cv2` (OpenCV): A popular computer vision library used for image and video analysis.
- `numpy`: A library for numerical computations.
- `uuid`: A library for generating universally unique identifiers.
- `os`: A library for interacting with the operating system.

**Functionality:**

1. The script starts by importing the required libraries and setting up the initial configuration.

2. It initializes the audio playback system using `mixer` from `pygame` and loads sound files for different beats (e.g., `beat.wav`, `hihat_closed.wav`, `hihat_opened.wav`).

3. The script sets up Mediapipe for hand detection and gesture recognition by creating instances of `mp_drawing` and `mp_hands`.

4. Inside the main loop, the script captures the video frames from the webcam, applies image processing, and performs hand gesture recognition.

5. The script detects hand landmarks and draws connections between them using `mp_drawing`.

6. Depending on the position of specific hand landmarks, the script triggers different sound effects. These gestures are used to control the music playback, such as beats and hihat sounds.

7. The script also includes logic to prevent continuous sound playback and resets the "just_played" flags when the hand landmark positions change.

8. The processed image with drawn landmarks and connections is displayed using OpenCV's `imshow`.

9. The loop continues until the user presses the 'q' key, at which point the webcam capture is released and the OpenCV windows are closed.

**Usage:**

1. The script uses the webcam to capture hand gestures in real-time.
2. When certain hand gestures are detected (such as raising a specific finger), corresponding sounds are played using the `pygame` mixer.

**Note:**

This code represents a simple hand gesture-controlled music player project that detects gestures and triggers sounds based on those gestures. It does not provide a full-fledged music player with advanced features. Additionally, this code assumes that you have the necessary sound files (`beat.wav`, `hihat_closed.wav`, `hihat_opened.wav`) present in the same directory as the script.

To use this code, you'll need to have the required libraries (`mediapipe`, `cv2`, `numpy`, `uuid`, `os`, `pydub`, `pygame`) installed in your Python environment. You'll also need to have a working webcam to capture video input.

Remember that this code is a simplified example, and real-world applications may require more robust error handling, user interfaces, and additional features.
