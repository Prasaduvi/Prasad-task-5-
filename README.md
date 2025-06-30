# Objective
The primary objective of this task was to:
* Capture live network packets from an active interface.
* Identify basic network protocols and different types of traffic.
* Gain hands-on experience with Wireshark for packet analysis and protocol awareness.

# Tools Used
* Wireshark: A free and open-source packet analyzer.

# Task Steps Performed

1.  **Wireshark Installation:** Installed Wireshark on the system.
2.  **Network Interface Selection:** Initiated packet capture on the active Wi-Fi network interface.
3.  **Traffic Generation:**
    * Generated ICMP traffic by pinging `www.youtube.com`.
    * Generated HTTP/HTTPS (TLSv1.2) traffic by Browse various websites.
    * DNS queries were automatically generated during domain name resolution.
4.  **Capture and Filtering:** Allowed the capture to run for a sufficient period to gather diverse traffic. Applied various display filters within Wireshark (e.g., `icmp`, `dns`, `http`, `tcp`, `tls`) to isolate and identify specific protocol traffic.
5.  **Protocol Identification:** Identified and analyzed at least three distinct protocols, as detailed below.

# Findings and Protocol Analysis

During the packet capture and analysis, the following key protocols were identified:

 # 1. ICMP (Internet Control Message Protocol)
* **Observation:** Captured `Echo (ping) request` and `Echo (ping) reply` packets when `pinging www.youtube.com`.
* **Purpose:** Used for diagnostic or error-reporting functions. In this case, it verified connectivity to a remote host.
* **Screenshot:** `Screenshot (87).png`

# 2. DNS (Domain Name System)
* **Observation:** Numerous `Standard query` packets were observed, primarily from the local machine to the DNS server.
* **Purpose:** Essential for translating human-readable domain names (e.g., google.com) into machine-readable IP addresses.
* **Screenshot:** `Screenshot (89).png`

# 3. HTTP (Hypertext Transfer Protocol)
* **Observation:** Identified `GET` requests and `HTTP/1.1 200 OK` responses, indicating web page and resource retrieval.
* **Purpose:** The foundation of data communication for the World Wide Web, used for loading web pages.
* **Screenshot:** `Screenshot (88).png`

# 4. TCP (Transmission Control Protocol)
* **Observation:** Widely present as the transport layer for most application traffic (HTTP, TLSv1.2). Observed TCP three-way handshakes (`SYN`, `SYN, ACK`, `ACK`), `Application Data` segments, and some instances of `TCP Dup Ack` and `TCP Retransmission`.
* **Purpose:** Provides reliable, ordered, and error-checked delivery of a stream of octets between applications running on hosts communicating via an IP network.
* **Screenshot:** `Screenshot (84).png`, `Screenshot (85).png`, `Screenshot (93).png`

# 5. TLSv1.2 (Transport Layer Security Protocol version 1.2)
* **Observation:** Encrypted traffic labeled `Application Data` was frequently seen over TCP, along with `Encrypted Alert` messages.
* **Purpose:** Provides secure communication over a computer network, widely used for secure web Browse (HTTPS).
* **Screenshot:** `Screenshot (84).png`, `Screenshot (85).png`
