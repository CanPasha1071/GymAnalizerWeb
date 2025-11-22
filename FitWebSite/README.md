AI Fitness Trainer Pro 🏋️‍♂️
A real-time, web-based personal trainer application that uses Computer Vision (TensorFlow.js) to analyze your exercise form, count repetitions, and track movement tempo directly in your browser.

No server upload required. All processing happens locally on your device for maximum privacy.

🌟 Key Features
Real-Time Pose Detection: Uses the MoveNet model to track body keypoints (shoulders, elbows, hips, knees, ankles).

Smart Rep Counting: Counts repetitions only when the full range of motion is achieved.

Tempo Analysis: Monitors the eccentric phase (lowering phase) of your movement.

Too Fast: Warns you to slow down.

Perfect: Green indicator for ideal muscle tension.

Isometric Hold Enforcement: Forces you to pause at the most difficult part of the movement (e.g., bottom of a squat) for 1.5 seconds to ensure quality reps.

Audio Feedback: Provides Text-to-Speech (TTS) voice guidance ("Go lower", "Hold", "Up", "1", "2"...).

System Logs: Displays a terminal-like log of your last rep's performance (Time under tension & quality).

Safe Start: The application launches in a "Paused" state, allowing you to position your camera before the workout begins.

Workout Summary: Displays total stats when you finish the session.

🛠️ Exercises Supported
You can switch between exercises using the dropdown menu:

Squat: Tracks hip depth and knee stability. Requires a 1.5s hold at the bottom.

Push-up: Tracks chest depth using elbow angles. Requires a hold at the bottom.

Dumbbell Curl: Tracks arm extension and flexion. Monitors the speed of lowering the weight.

🚀 How to Run
Since this project is a single HTML file containing all logic, it is very easy to run.

Method 1: Visual Studio Code (Recommended)
Open the folder containing the .html file in VS Code.

Install the Live Server extension.

Right-click the HTML file and select "Open with Live Server".

The app will open in your default browser (Chrome/Edge recommended).

Method 2: Direct Open
Simply double-click the .html file.

Note: Some browsers may block camera access via file:// protocol due to security policies. If the camera doesn't open, use Method 1.

📸 Usage Instructions
Permissions: Allow camera access when prompted.

Camera Position:

Place your device on a stable surface (floor or table).

Crucial: Stand sideways (side profile) to the camera. The AI needs to see the angle of your limbs (e.g., angle between hip, knee, and ankle).

Ensure your whole body is in the frame.

Start: Click the "SYSTEM START" button to load the AI model.

Begin Workout: Click "START WORKOUT" on the overlay screen once you are in position.

Feedback: Listen to the voice commands and watch the screen.

Orange Text: You are lowering the weight/body (Eccentric).

Blue Text: Hold the position (Isometric).

Green Text: Push up/Lift (Concentric).

⚙️ Technical Stack
HTML5 & CSS3: UI and layout.

JavaScript (ES6+): Core logic.

TensorFlow.js: Machine learning backbone.

MoveNet (SinglePose Lightning): A fast, accurate pose detection model optimized for web browsers.

Web Speech API: For Text-to-Speech audio feedback.

⚠️ Troubleshooting
Camera not working: Ensure you are using HTTPS or localhost (127.0.0.1). Check browser permissions.

Reps not counting:

Make sure you are facing the camera from the side.

Ensure you are going deep enough (e.g., Squat below 90 degrees).

Wait for the "Hold" command before coming up.

Voice not working: Check your device volume. Browsers require user interaction (clicking the Start button) before allowing audio to play.

🔒 Privacy
This application is client-side only. Your video feed is processed strictly within your browser's memory. No video data is ever sent to a server or stored.