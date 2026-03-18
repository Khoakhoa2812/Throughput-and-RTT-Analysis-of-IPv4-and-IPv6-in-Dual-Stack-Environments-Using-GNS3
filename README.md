## Comparative Performance Analysis of IPv4 and IPv6 in Dual-Stack Environments

## 1. Project Overview

This project involves the design, simulation, and performance benchmarking of a Dual-Stack network architecture. The primary goal was to measure the impact of protocol overhead on **Throughput** and **Round Trip Time (RTT)** within a virtualized enterprise environment.

## 2. Methodology & Topology Design**

![Topology design](https://github.com/Khoakhoa2812/Throughput-and-RTT-Analysis-of-IPv4-and-IPv6-in-Dual-Stack-Environments-Using-GNS3/blob/main/images/Topology%20design.png)

**_Figure_**_: Network Topology Design_

*   **Virtualization Platform:** GNS3 (Graphical Network Simulator-3).
*   **Infrastructure:** Integrated **Cisco 7200 Series** routers running IOS with **Ubuntu Linux** end-hosts.
*   **Architecture:** Implemented a **Dual-Stack** model, allowing IPv4 and IPv6 to operate natively on the same physical (virtual) interfaces.

## 3. Configuration & Implementation**

![Router configuration](https://github.com/Khoakhoa2812/Throughput-and-RTT-Analysis-of-IPv4-and-IPv6-in-Dual-Stack-Environments-Using-GNS3/blob/main/images/Router%20configuration.png)

**_Figure_**_: Router configuration_

![Linux network configuration](https://github.com/Khoakhoa2812/Throughput-and-RTT-Analysis-of-IPv4-and-IPv6-in-Dual-Stack-Environments-Using-GNS3/blob/main/images/Linux%20network%20configuration.png)

**_Figure_**_: Linux network configuration_

*   **Addressing:** Configured IPv4 (Class C) and IPv6 (Global Unicast) addressing schemes across all interfaces.
*   **Routing Logic:** Established using OSPF Dynamic Routing to ensure the flexibility and automation in routing.
*   **Linux Administration:** Utilized the Ubuntu terminal to configure network interfaces (netplan or ifconfig) and verify connectivity.

## 4. Performance Testing & Results**

![Throughput comparison graph](https://github.com/Khoakhoa2812/Throughput-and-RTT-Analysis-of-IPv4-and-IPv6-in-Dual-Stack-Environments-Using-GNS3/blob/main/images/Throughput%20perfomance%20comparison%20graph.png)

**_Figure_**_: Wireshark Throughput comparison graph_

![RTT comparison graph](https://github.com/Khoakhoa2812/Throughput-and-RTT-Analysis-of-IPv4-and-IPv6-in-Dual-Stack-Environments-Using-GNS3/blob/main/images/RTT%20performance%20comparison%20graph.png)

**_Figure_**_: Wireshark Round-trip time comparison graph_

*   **Tooling:** Utilized **iPerf** for TCP/UDP throughput testing and **ICMP** for latency (RTT) measurement.
*   **Analysis:**
    *   **Throughput:** Identified that IPv4 achieved slightly higher throughput due to its smaller header (20 bytes) compared to IPv6 (40 bytes).
    *   **Round-trip time:** Observed consistent RTT performance across both protocols, confirming IPv6’s readiness for real-time applications despite the header size.
*   **Verification:** Used **Wireshark** to capture packets and inspect the differences in header structures and MTU behavior.

*   **Key Fidings:**
    *   IPv4 achieves slightly higher throughput in LAN due to smaller header size
    *   IPv6 demonstrates strong performance in simulated enterprise WAN scenarios
    *   IPv6 shows comparable RTT performance to IPv4

## 5. Technical Skills Demonstrated**

*   **Networking:** IPv4/IPv6 Dual-Stack, Routing, ICMP, TCP/UDP.
*   **Tools:** GNS3, Wireshark, iPerf, VMware.
*   **OS:** Cisco IOS, Linux (Ubuntu/Debian) CLI.
