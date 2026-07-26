# AI-Driven Congestion Prediction for 6G IoT Networks


## Key Contributions

* Designed an AI-driven Anticipatory Congestion Control Framework (ACCF) for 6G IoT backhaul networks.
* Implemented congestion prediction using a Multi-Layer Perceptron (MLP) model.
* Integrated Software Defined Networking (SDN) telemetry for proactive traffic management.
* Developed a simulation environment for evaluating congestion scenarios.
* Demonstrated significant latency reduction through predictive congestion control.

## ACCF Architecture

The Anticipatory Congestion Control Framework (ACCF) consists of three interconnected planes:

* Data Plane: IoT sensors, gNodeB, OVS switch, and MEC server.
* Control Plane: SDN controller collecting flow statistics.
* Intelligence Plane: MLP classifier predicting congestion and triggering throttle decisions.

![ACCF Architecture](assets/accf-architecture.png)

## Workflow

1. IoT sensors generate telemetry traffic.
2. Traffic is forwarded through the gNodeB and OVS switch.
3. The SDN controller collects flow statistics from the network.
4. The telemetry agent extracts relevant congestion features.
5. The MLP classifier predicts whether congestion is likely to occur.
6. Based on the prediction, the controller decides to maintain normal operation or throttle traffic.
7. The decision helps prevent queue overflow and reduces network latency.

## Project Structure

```text
AI-Driven-Congestion-Prediction-6G-IoT/
│
├── assets/
│   └── accf-architecture.png
│
├── dataset/
│   └── congestion_dataset.csv
│
├── src/
│   ├── 6G_Backhaul.py
│   ├── ai_telemetry.py
│   └── train_ann.py
│
├── results/
│   └── congestion_graph.png
│
├── research-paper/
│   └── 6G_PROJECT_RESEARCH_PAPER.pdf
│
└── README.md
```

## Features

* Congestion prediction using MLP
* Real-time telemetry analysis
* SDN-based congestion management
* Dataset generation and training pipeline
* Performance visualization

## Technologies Used

* Python
* Scikit-Learn
* Mininet-WiFi
* Open vSwitch
* Software Defined Networking (SDN)
* Multi-Layer Perceptron (MLP)

## Results

- Achieved 97% congestion prediction accuracy.
- Reduced average latency through proactive congestion control.
- Reduced maximum latency during high-traffic scenarios.
- Eliminated packet loss under tested congestion conditions.
- Enabled predictive traffic management using SDN and Machine Learning.

## Research Paper

This project is based on the research paper:

**AI-Driven Anticipatory Congestion Prediction Framework for 6G IoT Backhaul Networks**

The proposed ACCF framework combines SDN telemetry, machine learning-based congestion prediction, and proactive traffic control to reduce latency and prevent congestion in 6G IoT backhaul networks.

The complete paper is available in:

`research-paper/6G_PROJECT_RESEARCH_PAPER.pdf`

## Performance Evaluation

| Metric              | Traditional Drop-Tail | ACCF     |
| ------------------- | --------------------- | -------- |
| Average Latency     | 33.28 ms              | 18.61 ms |
| Maximum Latency     | 44.87 ms              | 23.06 ms |
| Packet Loss         | Present               | Zero     |
| Prediction Accuracy | -                     | 97%      |

### Key Outcomes

* Achieved 97% congestion prediction accuracy.
* Reduced average latency by approximately 44%.
* Reduced maximum latency by approximately 49%.
* Eliminated packet loss during congestion scenarios.
* Enabled proactive congestion mitigation using SDN and Machine Learning.

## Future Work

* Integrate real-time telemetry collection from IoT devices.
* Deploy the MLP model as a live congestion prediction service.
* Extend the framework for larger 6G edge networks.
* Compare MLP performance with Random Forest and XGBoost models.
* Implement adaptive bandwidth allocation based on predictions.
* Evaluate performance under varying traffic loads and latency conditions.

## Author

**Vinayak Khandelwal**
Netaji Subhas University of Technology (NSUT), Delhi
