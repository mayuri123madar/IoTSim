IoTSim – IoT Network Simulator
An event-driven, web-based IoT network simulation platform designed to model device communication, network performance, energy consumption, and protocol behaviour.

IoTSim allows users to define IoT networks through Python-based simulation scripts, execute simulations through a web interface, and analyze the resulting network behaviour.

Overview
IoTSim provides a simulation environment for understanding how IoT devices communicate and how network conditions affect their performance and energy consumption.

The application uses an event-driven simulation engine to model network activity and presents simulation results through visual representations and analytical outputs.

Key Features
Network Simulation: Define IoT devices, connections, and communication traffic.
Event-Driven Engine: Model packet generation, transmission, reception, retries, and packet drops.
Protocol Modelling: Support for multiple wired and wireless communication protocols.
Energy Analysis: Track transmission, reception, idle, and sleep energy consumption.
Battery Monitoring: Model battery depletion and node failure.
Network Routing: Simulate traffic rerouting when alternative paths are available.
Protocol Recommendations: Compare candidate protocols using simulation results.
Network Management: Save, load, list, and delete network configurations.
Simulation Traces: Generate and manage trace files.
Visual Analytics: View network topology and simulation-related information.
Technology Stack
Technology	Purpose
Python	Backend and simulation logic
Flask	Web application framework
JavaScript	Frontend interactions
HTML5	Application structure
CSS3	User interface styling
JSON	Network configuration and data exchange
pytest	Automated testing
Project Architecture
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
│
├── saved_networks/
│
├── requirements.txt
├── protocol_parameters.json
│
├── test_engine.py
├── test_protocols.py
├── test_sandbox.py
├── test_hand_calculations.py
└── test_chatbot.py
Installation
1. Clone the repository
git clone https://github.com/mayuri123madar/IoTSim.git
cd IoTSim
2. Create a virtual environment
python -m venv venv
Activate it:

Windows

venv\Scripts\activate
Linux / macOS

source venv/bin/activate
3. Install dependencies
pip install -r requirements.txt
4. Start the application
python app.py
Open your browser and navigate to:

http://127.0.0.1:5000
Testing
Run the automated test suite using:

python -m pytest
Run individual test modules:

python -m pytest test_engine.py
python -m pytest test_protocols.py
python -m pytest test_sandbox.py
python -m pytest test_hand_calculations.py
Simulation and Analysis
The application exposes simulation functionality through its Flask backend.

The primary simulation endpoint is:

POST /simulate
Other application endpoints support network management, trace management, and protocol recommendations.

Simulation scripts should follow the scripting interface supported by the application. The standalone examples in the repository should not be assumed to be directly executable through the web editor.

Modelling Assumptions and Limitations
IoTSim is a software-based simulation environment, not a physical IoT deployment.

Some radio and hardware parameters are model assumptions. The simulation does not currently represent every real-world networking effect, such as MAC-layer collisions and interference between nodes.

Simulation results should therefore be interpreted as model-based estimates rather than guaranteed real-world measurements.

The script execution sandbox uses process and resource restrictions but is not equivalent to hardened container isolation.

Future Scope
More detailed network behaviour modelling.
Improved protocol evaluation.
Expanded simulation scenarios.
Additional network performance metrics.
Enhanced visualization and reporting.
Further validation against real-world measurements.
Repository
GitHub: https://github.com/mayuri123madar/IoTSim

IoTSim – Simulating Networks. Understanding Performance. Optimizing Connectivity.
