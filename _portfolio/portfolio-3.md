---
title: "Networks and Security Project"
excerpt: "This is our (made together with Yves van Haaren) implementation of the bTCP protocol posed in the course Networks and Security at Radboud University. Grade: X.X <br/><img src='/images/500x300.png'>"
collection: portfolio
---

The project in short
----
The task was to implement a reliable datatransfer protocol (RDP) build upon the UDP protocol immitating the TCP protocol (bTCP is short for basic-TCP). We were provided with a working UDP protocol (called the lossy layer) and a simple interface acting as the application layer. We were tasked with implementing sockets. 

Key parts of our implementation
----
1. We had to implement a working handshake. The sockets followed a finite state machine, which we used to guide the sockets through this process. We had to exchange sequence numbers, window sizes and protocol types. As the application layer and the network layer run on different threads we also had to take that into account.

2. When the handshake is completed, meaning the sockets were in-sync and ready to transfer data, we had to implement a protocol ensure the data transfer was reliable. We fully implemented GBN (Go-Back-N) and (almost completely) SR (Selective Repeat). We implemented a proper OO structure to facilitate multiple protocols and expanded the provided command-line UI to support this extra feature.

3. We also had to merge the server socket and client socket into a so-called hybrid socket. This socket can now act as either a server (data-receiver) or a client (data-sender).

Key skill learned/used in this project
----
- Incorperating a finite state machine into the core of an implementation
- Construction proper and more elaborate OO structures/patterns
- Working with multiple threads and provide thread-safe code
- Working with more rudimentary networking modules in Python
