Gesture-Controlled RC Car 

A real-time gesture-controlled robotic car built using a Raspberry Pi and a Bluetooth-enabled wristband. This project interprets hand and arm movements via sensor data (accelerometer, gyroscope) and translates them into directional commands to control the car (forward, backward, left, right, stop).

Features
- Real-time motion recognition via Python on Raspberry Pi
- Gesture thresholds tuned using time-series analysis
- Data collection and visualization using PostgreSQL, Excel, Tableau
- Achieved ~85% gesture recognition accuracy in live trials
- Latency optimized to <150 ms and false triggers reduced by 40%

Tech Stack
| Component     | Tools Used                             |
|---------------|----------------------------------------|
| Programming   | Python, SQL                            |
| Hardware      | Raspberry Pi, Bluetooth wristband      |
| Sensors       | Accelerometer, Gyroscope (XYZ axes)    |
| Data Analysis | Excel, Tableau, PostgreSQL             |
| Visualization | Tableau dashboards                     |
| Communication | Bluetooth (Serial)                     |

Data Analysis
Collected over 15 gesture trials for each of the five main movements:
- **Forward**
- **Backward**
- **Left**
- **Right**
- **Resting (Idle)**

Data was logged with:
- Timestamp
- Sensor Type (Accel, Gyro)
- Axis values (X, Y, Z)
- Movement Label
- Trial Number

Visualized in Tableau to:
- Identify noise and inconsistent readings
- Compare gestures by axis trends
- Tune thresholds to distinguish between deliberate and accidental motions

Key Visuals (Tableau)
- Line graphs of AccelZ, GyroY, GyroZ over time
- Box-and-whisker plots comparing gesture variability
- Interactive dashboard to explore trial data by movement and sensor type

- Link for all the data visualizations: https://public.tableau.com/app/profile/christopher.seo/viz/data_17518578820300/DataVisualization15Trials

Results
- Optimized gesture logic using threshold filtering
- 85% recognition accuracy
- False positives reduced by 40%
- Average latency below 150 ms

CapstoneData/
├── Scripts/
│ ├── gen_synthetic.py # Generates synthetic gesture data
│ └── visualize_gestures.py # Plots graphs from dataset
├── Data/
│ └── gesture_data.csv # Main dataset used in project
├── Outputs/
│ └── Graphs, charts, exports from Tableau or Python
└── Tableau_Dashboard.twb # Final interactive dashboard

Getting Started
1. Run `gen_synthetic.py` to generate gesture data (or use your real sensor data)
2. Use `visualize_gestures.py` to preview trends and validate movement thresholds
3. Load `gesture_data.csv` into Tableau or Excel to explore
4. Modify `gesture_logic.py` on the Pi to fine-tune control logic for your car

Lessons Learned
- Importance of consistent gesture execution for data labeling
- How to clean and interpret noisy sensor data
- Real-time system integration between hardware and data analytics

Contact
Feel free to reach out with questions, feedback, or collaborations!

