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

## **Project Modules**

### **HTTP Client & Server Implementation**

- **Objective:** Implement an HTTP client and HTTP server to simulate web communication, focusing on the underlying TCP communication layer.
  
**Key Features:**
- Built an **HTTP server** to handle client connections and respond with appropriate data using the HTTP protocol.
- Developed a **HTTP client** capable of establishing TCP connections, sending fixed-size HTTP GET requests, and processing server responses.
- **Skills Gained:** HTTP protocol, TCP socket programming, client-server architecture.

---

### **SMTP Agent Implementation**

- **Objective:** Develop a SMTP agent to simulate email communication using the Simple Mail Transfer Protocol (SMTP)

**Key Features:**
- Built an **SMTP** client to establish connections with a remote server and perform a full email transaction using commands such as HELO, MAIL FROM, RCPT TO, DATA, and QUIT.
- Supported basic **SMTP command handling** and protocol-compliant request-response interactions.
- **Skills Gained** SMTP protocol, email systems, socket programming.

---

### **Reliable UDP & RUDP Handshake**

- **Objective:** Design and implement a custom reliable transport protocol (RUDP) over UDP, featuring a 3-way handshake for connection establishment.

**Key Features:**
- Created, bound, and listened to sockets using low-level UDP functions (sendto, recvfrom) for bidirectional communication.
- Implemented a **3-way handshake** mechanism to simulate reliable connections over UDP:
    - **Client side**: Initiates connection, waits 20ms for a response, and sends an acknowledgment upon successful receipt.
    - **Server side**: Listens for incoming packets, validates them, and responds with an acknowledgment.
- Ensured message delivery despite UDP's lack of built-in reliability.
- **Skills Gained**: UDP socket programming, custom transport protocol design, connection management.
---

### **Stop-and-Wait Protocol**

- **Objective:**  Implement the **Stop-and-Wait** protocol to ensure reliable data transmission by requiring acknowledgment of each packet before sending the next.
  
**Key Features:**
- Developed single-packet transmission logic with support for retransmission upon timeout or incorrect acknowledgment.
- Integrated timeout management for detecting lost or delayed packets.
- **Sender Side:** Sent packets with a custom structure, tracked sequence numbers, and handled retransmissions on timeout or invalid acknowledgments.
- **Receiver Side:** Received packets, validated sequence numbers, and acknowledged only the last valid packet received.
- **Skills Gained:** Reliable data transfer, packet acknowledgment mechanisms, timeout and retransmission logic.

---

### **Go-Back-N Protocol**

- **Objective:** Extend the **Stop-and-Wait** protocol to **Go-Back-N**, allowing multiple packets to be in transit before acknowledgments are received, improving throughput.
  
**Key Features:**
- Implemented a **packet queue (ring buffer)** to manage multiple in-flight packets within a defined window size.
- Utilized a **background worker thread** for sending, tracking, and retransmitting packets as needed.
- **Sender Side:** Constructed and enqueued packets, transmitted all unsent packets in the window, awaited acknowledgments, and removed acknowledged packets; on timeout, retransmitted the entire window.
- **Receiver Side:** Processed incoming packets, tracked sequence numbers, and acknowledged the last valid packet received.
- **Skills Gained:** Multi-threaded programming, window-based flow control, Go-Back-N reliability algorithm.

---

Through implementing protocols such as **RUDP**, **Stop-and-Wait**, and **Go-Back-N**, these projects provided hands-on experience with core networking concepts, including **socket programming**, **reliability**, and **flow control**. Building each component from the ground up deepened my understanding of how data is transmitted over the internet and reinforced essential principles like **concurrency**, **packet loss handling**, and **network resilience**—skills highly relevant to systems and backend development.

---

## **Technologies Used**

- **C Language:** Provided low-level memory and system control for efficient protocol implementation.
- **POSIX Sockets:** Enabled direct manipulation of TCP/UDP connections for building custom communication protocols.
- **Custom Protocol Design:** Emulated core internet mechanisms such as handshakes, acknowledgments, and flow control.
- **Multithreading:** Applied to increase efficiency in data transmission.

> This project collection was completed as part of academic coursework and is hosted in a private repository, available upon request.