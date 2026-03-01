# Hand Gesture Mouse Controller 🖱️🖐️

A Python application that uses webcam hand tracking to control the PC's mouse cursor and perform clicks and scrolling actions using specific hand gestures. The project utilizes MediaPipe Tasks Vision for robust hand landmark detection and PyAutoGUI for simulating mouse actions.

## ✨ Features

- **🖱️ Cursor Movement**: Move the mouse cursor smoothly by pointing your index finger.
- **👆 Left Click**: Pinch your thumb and index finger together.
- **✌️ Right Click**: Pinch your thumb and middle finger together.
- **📜 Scrolling**: Keep your index and middle fingers up (others down) and move your hand up/down or left/right to scroll.
- **🛑 Failsafe Disabled**: PyAutoGUI failsafe is disabled for uninterrupted control.

## 🛠️ Requirements

- Python 3.x
- OpenCV (`cv2`)
- MediaPipe (`mediapipe`)
- PyAutoGUI (`pyautogui`)

## 🚀 Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/fortune-ninja2/controlling-pc-as-mouse-input-using-hand-gesture.git
   cd controlling-pc-as-mouse-input-using-hand-gesture
   ```

2. **Install the required dependencies:**
   It is recommended to use a virtual environment.
   ```bash
   pip install opencv-python mediapipe pyautogui
   ```

3. **Required Assets:**
   Ensure the `hand_landmarker.task` file (MediaPipe Hand Landmarker model) is present in the project directory.

4. **Run the script:**
   ```bash
   python main.py
   ```

5. **Exit:** Press the `Esc` key to exit the application. 

## 📝 How It Works

1. The script captures video from your webcam.
2. MediaPipe Handlandmarker detects your hand and extracts 21 3D landmarks.
3. Depending on the distance between specific landmarks (e.g., thumb tip and index tip), the application interprets the gesture (like a pinch).
4. `pyautogui` is then called to execute the corresponding mouse action (move, click, scroll). 
