+++
categories = ["networks"]
coders = []
date = 2025-04-12T23:00:00Z
description = "Hands-on implementation of real-world network protocols and transport mechanisms in C"
image = "https://ik.imagekit.io/ys4gkaixy/network-svgrepo-com-2.svg?updatedAt=1744745337992"
title = "Network Protocol Implementation"
weight=3
type = "post"
[[tech]]
name = "C"
url = "https://en.wikipedia.org/wiki/C_(programming_language)"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/C_Logo.png?updatedAt=1744511053296"

[[tech]]
name = "Socket Programming"
url = "https://en.wikipedia.org/wiki/Network_socket"
logo = "https://ik.imagekit.io/ys4gkaixy/ethernet-svgrepo-com.svg?updatedAt=1745338856328"
+++

This multi-part project series was developed over the span of a graduate-level Computer Networks course. Each module focused on implementing key components of real-world networking, including application-level protocols and custom transport-layer mechanisms. All implementations were written in C using low-level socket programming.

---

## Project Modules

### HTTP Client & Server Implementation

- **Objective:** Implement an HTTP client and HTTP server to simulate web communication, focusing on the underlying TCP communication layer.
  
**Key Features:**
- Developed a custom **HTTP server** to handle requests.
- Implemented client functionality to send **HTTP GET** requests and receive responses.
- **Technical Skills Gained:** HTTP protocol, socket programming, client-server model.

---

### SMTP Agent Implementation

- **Objective:** Build an SMTP agent to simulate email communication via the Simple Mail Transfer Protocol (SMTP).
  
**Key Features:**
- Implemented an **SMTP client** to send emails to a server.
- Supported basic **SMTP commands** and interaction.

**Technical Skills Gained:** SMTP protocol, email systems, socket communication.

**GitHub Repository:** [View Code](#)

---

### Reliable UDP & RUDP Handshake

- **Objective:** Implement a custom transport protocol over UDP, introducing reliable data transmission with a 3-way handshake mechanism for connection establishment.
  
**Key Features:**
- Built a **3-way handshake** for **RUDP** to establish reliable connections over UDP.
- Used **sendto** and **recvfrom** functions for communication between client and server.

**Technical Skills Gained:** Socket programming, custom protocol design, UDP handling.

**GitHub Repository:** [View Code](#)

---

### Stop-and-Wait Protocol

- **Objective:** Implement the **Stop-and-Wait** reliability technique where each packet is acknowledged before sending the next one.
  
**Key Features:**
- Implemented single packet transmission and retransmission on timeout or incorrect acknowledgment.
- Timeout management was built for retransmission.

**Technical Skills Gained:** Reliability techniques, packet acknowledgment, timeout handling.

**GitHub Repository:** [View Code](#)

---

### Go-Back-N Protocol

- **Objective:** Extend the **Stop-and-Wait** protocol to **Go-Back-N**, enabling multiple packets to be sent before acknowledgment is received.
  
**Key Features:**
- Introduced a **queue of packets** to handle multiple transmissions.
- Used a **background worker thread** for packet management and retransmission.

**Technical Skills Gained:** Multi-threading, window-based flow control, Go-Back-N algorithm.

**GitHub Repository:** [View Code](#)

---

### Data Packet Transmission Optimization

- **Objective:** Optimize data transmission protocols by exploring error handling, retransmission strategies, and performance improvements.
  
**Key Features:**
- Optimized packet transmission techniques to reduce delays.
- Introduced efficient **error correction mechanisms**.

**Technical Skills Gained:** Error correction, performance optimization, data integrity.

**GitHub Repository:** [View Code](#)

---

### Protocol Testing and Debugging

- **Objective:** Test and debug the reliability of the implemented protocols, ensuring robustness and fault tolerance under various network conditions.
  
**Key Features:**
- Developed a suite of test cases to evaluate **packet loss**, delays, and retransmissions.
- Used **network simulators** to mimic real-world conditions.

**Technical Skills Gained:** Testing methodologies, debugging, fault tolerance, network simulation.

**GitHub Repository:** [View Code](#)

---

### Conclusion

These projects allowed me to dive deep into network protocols, from building custom **RUDP** to exploring reliability techniques such as **Stop-and-Wait** and **Go-Back-N**. Each project built on the previous, expanding my understanding of **socket programming**, **multithreading**, and **network reliability**.

You can explore the full implementation of each of these projects on my GitHub, linked above.

---

## Impact

By implementing these protocols from scratch, this project suite offered deep insights into how the internet and data communication systems operate. It strengthened concepts such as **reliability**, **flow control**, **concurrency**, and **packet loss handling**—all critical in systems and backend development.

---

## Technologies Used

- **C Language:** For performance and low-level memory control.
- **POSIX Sockets:** Direct control of network communication.
- **Custom Protocol Design:** Simulated behavior of core internet mechanisms.
- **Multithreading:** Applied to increase efficiency in data transmission.

> This project collection was completed as part of academic coursework and is hosted in a private repository, available upon request.

![Networks Project Demo](/images/acquire_game.gif)

GIF created with [LiceCap](http://www.cockos.com/licecap/).