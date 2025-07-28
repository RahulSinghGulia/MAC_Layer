# Medium Access Control (MAC) Layer

This repository covers various aspects of MAC layer components.

## Project Overview

This project presents a Python-based discrete-event simulation of the **CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)** protocol, a fundamental medium access control method used in wireless networks like Wi-Fi. The simulator is built using `simpy` and designed to model and analyze the performance of CSMA/CA under various network conditions and protocol configurations.

The core objective is to provide quantitative insights into:

* The effectiveness of the **RTS/CTS (Request to Send/Clear To Send) handshake mechanism** in mitigating collisions and improving throughput.

* The impact of **network size (number of nodes)** on overall performance metrics such as throughput, collisions, latency, and channel efficiency.

* The role of the **exponential backoff algorithm** in managing contention and retransmissions.

* The influence of **contention domain/coverage area** on network performance.

## Features

* **Detailed CSMA/CA Protocol Emulation**: Accurately simulates key CSMA/CA phases including:

  * Carrier Sensing

  * DIFS (Distributed Interframe Space) and SIFS (Short Interframe Space)

  * Random Backoff mechanism with exponential increase

  * Acknowledgement (ACK) for successful transmissions

* **Optional RTS/CTS Handshake**: Toggle the Request To Send/Clear To Send mechanism to compare its performance impact.

* **Collision Detection and Handling**: Identifies collisions when multiple nodes transmit simultaneously and implements retransmission logic.

* **Comprehensive Performance Metrics**: Beyond basic packet counts and collisions, the `EnhancedAnalyzer` provides:

  * Network Throughput

  * Collision Count

  * Average Packet Transmission Latency

  * Channel Utilization Efficiency

  * Transmission Success Rate

* **Parameter Variability**: Easily adjust simulation parameters such as:

  * Number of nodes

  * Simulation time

  * DIFS, SIFS, ACK timings

  * Attempt limit for retransmissions

  * Coverage range

* **Visualized Analysis**: Generates professional-quality plots using `matplotlib` to visualize:

  * Throughput vs. Number of Nodes (with/without RTS/CTS)

  * Collisions vs. Number of Nodes (with/without RTS/CTS)

  * Multi-metric comparison (Throughput, Collisions, Latency, Efficiency, Success Rate) across varying node counts.

  * Impact of Backoff Attempt Limit on Throughput, Collisions, and Latency.

  * Throughput vs. Coverage Area.

## Diagrams and Flowcharts

To provide a clearer understanding of the CSMA/CA protocol's operational flow and the underlying mathematical logic, the following flowcharts are included:

### Enhanced CSMA/CA Flowchart
![Enhanced CSMA/CA Flowchart](https://github.com/RahulSinghGulia/MAC_Layer/blob/main/CSMA_CA/csma_ca_flowchart_enhanced.png)

This flowchart illustrates the detailed steps and decision points within the enhanced CSMA/CA protocol, including the RTS/CTS handshake and backoff mechanisms.

### CSMA Mathematical Flowchart
![CSMA Mathematical Flowchart](https://github.com/RahulSinghGulia/MAC_Layer/blob/main/CSMA_CA/csma_math_flowchart.png)

This diagram outlines the mathematical logic and calculations involved in certain aspects of the CSMA/CA simulation.

## Technologies Used

* **Python 3.x**

* **SimPy**: For discrete-event simulation.

* **NumPy**: For numerical operations, especially for calculating averages of metrics.

* **Matplotlib**: For data visualization and plotting simulation results.

## How to Run the Simulator

### Prerequisites

Ensure you have Python 3.x installed. You can install the required libraries using `pip`:

```bash
pip install simpy numpy matplotlib
