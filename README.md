
![example-virtual-driving-instructor-fullstack](https://github.com/user-attachments/assets/d98acaec-bce4-4061-a9fc-c4351e0767ba)

# Virtual Driving Instructor

Planned project start: 2026/06/01 
Planned project completion: 2027/03/01

**Virtual Driving Instructor** is an AI-driven application that analyzes live video from your phone’s camera in real time to help drivers stay safe, maintain good driving habits, and comply with local traffic rules. It does **not** take control of the vehicle—it only informs the driver about potential hazards.
Place a phone attached to the windshield - with the screen facing the driver having a working front and rear camera, and the screen constantly on.

A mobile app streams camera frames to a web dashboard, which provides a detailed trip summary and safety feedback.
Also, you can track everything in the web app, for example, on a second device.

## 🔑 Key Features

1. **Pedestrian & Cyclist Detection**  
   - Real-time object detection e.g., speeding scooter towards the vehicle, visual and audio alerts.

2. **Driving Style Analysis**  
   - Identification of harsh accelerations and hard braking using built-in phone sensors (accelerometer/GPS).  
   - Recognition of aggressive maneuvers (sudden lane changes, sharp turns).  

3. **Local Traffic Rule Compliance**  
   - Load country-specific rule sets (e.g. PL, PT, DE, USA) from YAML/JSON.  
    - Enforcing behavior at pedestrian crossings (e.g., “must stop” before a pedestrian crossing in Poland - when a pedestrian is about to enter the crosswalk. This is not mandatory in Portugal at this time).  
   - Monitor speed limits and overtaking rules based on GPS speed.

4. **Driver Fatigue & Distraction Monitoring**  
   - Track eye movements and head position using Mediapipe or dlib - by front camera.  
   - Issue rest reminders after extended driving sessions.

5. **Detection of lack of focus **  
   - Warns the driver when he or she is driving forward in the car, and for an extended period of time is looking, for example, into the side window (Potentially driving into the rear of another vehicle, etc...).
  
6. **Lane Departure Warning**  
   - Lane segmentation and tracking of vehicle position in the lane.  Assesses whether the driver is deviating from the lane trajectory.
   - Alert when drifting toward lane markings without signaling.

7. **Collision Warning & Prediction**  
   - Calculate collision risk by analyzing object trajectories.  
   - Introduces very simple and inductive audio and on-screen messages with no distractions colission alerts

8. **Automatic Records**  
   - Automatic registration of clips of dangerous behavior of traffic participants
  
## 🛠️ Technologies (suggested by ChatGPT)

- **Mobile App (iOS/Android)**  
  - **Framework**: React Native or/and Flutter  
  - **Camera Access**: Expo Camera / Native APIs  
  - **Sensors**: Accelerometer, GPS (via expo-sensors or native modules)  
  - **Networking**: WebSocket / REST API client (Axios, Fetch)

- **Web Dashboard (Passenger View)**  
  - **Framework**: React + Next.js  
  - **Real-Time Communication**: WebSocket or Server-Sent Events  

- **Backend (Python)**  
  - **Framework**: FastAPI or Flask  
  - **Streaming**: WebSocket endpoint for video frames and alerts  
  - **Computer Vision**: OpenCV, Mediapipe  
  - **Deep Learning**: PyTorch or TensorFlow  
  - **Configuration**: PyYAML or JSON

---
  
     
