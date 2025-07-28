Medium Access Control (MAC) Layer

This repository covers various aspects of MAC layer components.
Project Overview

This project presents a Python-based discrete-event simulation of the CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance) protocol, a fundamental medium access control method used in wireless networks like Wi-Fi. The simulator is built using simpy and designed to model and analyze the performance of CSMA/CA under various network conditions and protocol configurations.

The core objective is to provide quantitative insights into:

    The effectiveness of the RTS/CTS (Request to Send/Clear to Send) handshake mechanism in mitigating collisions and improving throughput.

    The impact of network size (number of nodes) on overall performance metrics such as throughput, collisions, latency, and channel efficiency.

    The role of the exponential backoff algorithm in managing contention and retransmissions.

    The influence of contention domain/coverage area on network performance.

Features

    Detailed CSMA/CA Protocol Emulation: Accurately simulates key CSMA/CA phases including:

        Carrier Sensing

        DIFS (Distributed Interframe Space) and SIFS (Short Interframe Space)

        Random Backoff mechanism with exponential increase

        Acknowledgement (ACK) for successful transmissions

    Optional RTS/CTS Handshake: Toggle the Request To Send/Clear To Send mechanism to compare its performance impact.

    Collision Detection and Handling: Identifies collisions when multiple nodes transmit simultaneously and implements retransmission logic.

    Comprehensive Performance Metrics: Beyond basic packet counts and collisions, the EnhancedAnalyzer provides:

        Network Throughput

        Collision Count

        Average Packet Transmission Latency

        Channel Utilization Efficiency

        Transmission Success Rate

    Parameter Variability: Easily adjust simulation parameters such as:

        Number of nodes

        Simulation time

        DIFS, SIFS, ACK timings

        Attempt limit for retransmissions

        Coverage range

    Visualized Analysis: Generates professional-quality plots using matplotlib to visualize:

        Throughput vs. Number of Nodes (with/without RTS/CTS)

        Collisions vs. Number of Nodes (with/without RTS/CTS)

        Multi-metric comparison (Throughput, Collisions, Latency, Efficiency, Success Rate) across varying node counts.

        Impact of Backoff Attempt Limit on Throughput, Collisions, and Latency.

        Throughput vs. Coverage Area.

Technologies Used

    Python 3.x

    SimPy: For discrete-event simulation.

    NumPy: For numerical operations, especially for calculating averages of metrics.

    Matplotlib: For data visualization and plotting simulation results.

How to Run the Simulator
Prerequisites

Ensure you have Python 3.x installed. You can install the required libraries using pip:

pip install simpy numpy matplotlib

Execution

    Clone the repository (or save the code):
    Save the provided Python code as a .py file (e.g., csma_ca_sim.py).

    Run from your terminal:
    Navigate to the directory where you saved the file and execute:

    python csma_ca_sim.py

The script will first run a basic simulation, then proceed with comprehensive analyses, generating several plots that compare performance under different conditions. The plots will appear in separate windows and should be closed to proceed with the next analysis.
Key Insights and Achievements

This project successfully demonstrates a clear understanding of wireless network protocols and simulation methodologies. Through its analysis capabilities, it highlights:

    RTS/CTS Efficacy: The simulations generally show that RTS/CTS significantly reduces collisions in denser networks by effectively reserving the channel, leading to improved throughput, especially as the number of competing nodes increases.

    Network Scaling Challenges: As expected, an increase in the number of nodes leads to higher contention, which can result in increased collisions and latency, and potentially a decrease in per-node throughput without effective collision avoidance mechanisms.

    Adaptive Backoff: The analysis of the backoff attempt limit illustrates how the adaptive nature of CSMA/CA helps to manage contention, preventing network collapse under heavy load, though excessive limits can introduce unnecessary latency.

This project showcases strong analytical, programming, and data visualization skills, crucial for understanding and optimizing complex systems.
Contributing

Contributions are welcome! Feel free to fork the repository, make improvements, and submit pull requests.
License

This project is open-sourced under the MIT License.
