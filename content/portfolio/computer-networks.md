+++
categories = ["networks"]
coders = []
date = 2025-04-12T23:00:00Z
description = "Hands-on implementation of real-world network protocols and transport mechanisms in C"
image = "https://ik.imagekit.io/ys4gkaixy/network-svgrepo-com-2.svg?updatedAt=1744745337992"
title = "Computer Networks Projects"
weight=3
type = "post"
[[tech]]
name = "Socket Programming"
url = "https://en.wikipedia.org/wiki/Berkeley_sockets"
[[tech]]
name = "HTTP"
url = "https://developer.mozilla.org/en-US/docs/Web/HTTP"
[[tech]]
name = "SMTP"
url = "https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol"
[[tech]]
name = "Go-Back-N"
url = "https://en.wikipedia.org/wiki/Go-Back-N_ARQ"
[[tech]]
name = "Stop-and-Wait"
url = "https://en.wikipedia.org/wiki/Stop-and-wait_ARQ"
[[tech]]
name = "Multithreading"
url = "https://en.wikipedia.org/wiki/Multithreading_(computer_architecture)"
+++

This multi-part project series was developed over the span of a graduate-level Computer Networks course. Each module focused on implementing key components of real-world networking, including application-level protocols and custom transport-layer mechanisms. All implementations were written in C using low-level socket programming.

---

## Project Modules

### HTTP Client & Server
Built a fully functional HTTP client and server pair, supporting basic GET/POST requests and response parsing. This helped explore how web browsers and servers communicate.

### SMTP Mail Agent
Simulated an SMTP-based mail delivery system that constructs and sends raw email messages using socket-level commands. Provided insight into how email infrastructure works behind the scenes.

### Reliable Data Transfer Protocols

- **Stop-and-Wait Protocol**: Designed a protocol to send data one packet at a time with acknowledgments and retransmissions to ensure reliability.
- **Go-Back-N Protocol**: Implemented a sliding window mechanism to improve throughput by sending multiple packets before needing an acknowledgment.
- **Threaded Go-Back-N**: Enhanced the Go-Back-N protocol using multithreading to support concurrent data transfer and reception.

---

## Impact

By implementing these protocols from scratch, this project suite offered deep insights into how the internet and data communication systems operate. It strengthened concepts such as reliability, flow control, concurrency, and packet loss handling—all critical in systems and backend development.

---

## Technologies Used

- **C Language**: For performance and low-level memory control.
- **POSIX Sockets**: Direct control of network communication.
- **Custom Protocol Design**: Simulated behavior of core internet mechanisms.
- **Multithreading**: Applied to increase efficiency in data transmission.

> This project collection was completed as part of academic coursework and is hosted in a private repository, available upon request.

![Networks Project Demo](/images/acquire_game.gif)

GIF created with [LiceCap](http://www.cockos.com/licecap/).
