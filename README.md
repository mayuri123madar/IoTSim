# IoTSim – IoT Network Simulator

IoTSim is a web-based Internet of Things (IoT) network simulation platform built using Python and Flask. It allows users to simulate IoT networks, study communication protocols, analyse energy consumption, and understand network performance through a visual interface.

The project aims to make IoT network concepts easier to understand through script-based simulation and performance analysis.

## Features

### 1. IoT Network Simulation
- Create and simulate IoT network scenarios.
- Execute simulation scripts through the web application.
- Observe communication between connected devices.
- Analyse packet transmission, delivery, loss, and retries.
- Study the impact of device failures and battery depletion.

### 2. Protocol Simulation
IoTSim supports simulation models for multiple communication protocols, including:

- Wi-Fi
- Bluetooth Low Energy (BLE)
- Zigbee
- LoRa
- MQTT
- CoAP
- I2C
- SPI
- UART
- CAN

### 3. Energy Consumption Analysis
- Estimate energy consumption of IoT devices.
- Analyse battery usage during simulation.
- Study the relationship between communication activity and energy consumption.
- Estimate network lifetime using the implemented energy model.

### 4. Network Performance Analysis
- Examine packet transmission and delivery.
- Analyse packet loss and retry behaviour.
- Study buffer overflow and device battery depletion.
- Observe how network performance changes under different conditions.

### 5. Protocol Recommendation
The recommendation engine evaluates supported protocol configurations using simulation results and ranks candidates based on network lifetime.

### 6. Network Management
- Save network configurations.
- Load previously saved networks.
- View saved network information.
- Delete saved networks.

## Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| Backend Framework | Flask |
| Frontend | HTML, CSS, JavaScript |
| Simulation Engine | Python |
| Data Visualisation | JavaScript-based charts |
| Testing | Pytest/unittest |
| Version Control | Git and GitHub |

## Project Structure

```text
IoTSim/
│
├── app.py
├── engine.py
├── protocols.py
├── iot_protocols.py
├── protocol_interface.py
├── energy_model.py
├── recommendation_engine.py
├── iot_framework.py
│
├── templates/
├── static/
├── saved_networks/
│
├── test_engine.py
├── test_protocols.py
├── test_sandbox.py
├── test_hand_calculations.py
├── test_chatbot.py
│
├── requirements.txt
├── MAJOR_PROJECT_README.md
├── PROTOCOL_DOCUMENTATION.md
└── README.md
```

## Installation and Setup

### Prerequisites

- Python 3.10 or later
- pip
- Git

### Step 1: Clone the Repository

```bash
git clone https://github.com/mayuri123madar/IoTSim.git
```

### Step 2: Navigate to the Project Directory

```bash
cd IoTSim
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Start the Application

```bash
python app.py
```

### Step 5: Open the Application

Open your browser and visit:

```text
http://127.0.0.1:5000
```

## Running Tests

Run the test suite from the project directory:

```bash
python -m pytest
```

To run individual test files:

```bash
python -m pytest test_engine.py
python -m pytest test_protocols.py
python -m pytest test_sandbox.py
python -m pytest test_hand_calculations.py
python -m pytest test_chatbot.py
```

## Main Application Endpoints

| Endpoint | Method | Purpose |
|---|---|---|
| `/simulate` | POST | Execute an IoT simulation |
| `/save_network` | POST | Save a network configuration |
| `/load_network` | POST | Load a saved network |
| `/list_networks` | GET | List saved networks |
| `/delete_network` | POST | Delete a saved network |
| `/recommend_by_simulation` | POST | Recommend protocols using simulation results |
| `/recommend_protocol` | POST | Get protocol recommendations |
| `/compare_protocols` | POST | Compare communication protocols |
| `/recommend_topology` | POST | Get network topology recommendations |

## Simulation and Modelling

IoTSim uses an event-driven simulation approach to represent the behaviour of IoT networks.

The simulation engine models activities such as:

- Device communication
- Packet generation and transmission
- Packet delivery and loss
- Retransmission attempts
- Buffer overflow
- Battery depletion
- Network lifetime

The application also provides different views to examine device behaviour, protocol performance, energy consumption, and data flow.

## Energy Model

The simulator uses the electrical energy relationship:

**Energy = Voltage × Current × Time**

Where:

- Energy is measured in joules.
- Voltage is measured in volts.
- Current is measured in amperes.
- Time is measured in seconds.

This relationship is used by the energy model to estimate device energy consumption.

## Security Considerations

The application includes script validation and sandbox execution mechanisms intended to restrict user-submitted simulation scripts.

These mechanisms should not be considered equivalent to operating-system-level or container-based isolation. Additional security hardening is recommended before deploying the application in an untrusted production environment.

## Current Limitations

- Protocol behaviour is represented using simplified simulation models.
- Radio interference and detailed MAC-layer collision behaviour are not fully modelled.
- Real physical IoT hardware is not connected to the simulator.
- Energy consumption depends on the assumptions and parameters implemented in the models.
- Simulation results are estimates and may differ from real-world device measurements.

## Future Enhancements

- More detailed protocol modelling.
- Improved network visualisation.
- Advanced energy optimisation.
- More realistic wireless communication modelling.
- Extended security isolation for user-submitted scripts.
- Integration with real-world IoT datasets.
- Additional simulation scenarios and performance metrics.

## Project Repository

GitHub: https://github.com/mayuri123madar/IoTSim

---

**IoTSim – Simulating IoT Networks, Understanding Communication, and Analysing Performance.**
