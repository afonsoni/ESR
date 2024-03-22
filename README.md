# ESR
Network Services Engineering (Engenharia de Serviços em Rede)

## Over-the-Top Multimedia Delivery Service

### Overview

This project is a Java-based Over-the-Top (OTT) multimedia delivery service designed for efficient content delivery. It features a shared overlay network with a PIM-SM/Opt-In strategy, multicast at the application layer, and supports simultaneous streaming and watching by clients.

### Features

* **Multicast in the Application Layer:** Utilizes multicast at the application layer for efficient content delivery.
* **Simultaneous Streaming and Watching:** Clients can watch a stream and stream content simultaneously.
* **List Ongoing Streams:** Provides a feature to list all ongoing streams.
* **Recovery from Bad/Failed Nodes:** Implements a probing technique to recover from bad or failed nodes. Routes are altered if a neighbor does not respond within 10 seconds.

### Technical Details

* **Programming Language:** Java
* **Streaming Protocol:** RTP/UDP (for video and audio streams)
* **Control/Handshake Messages:** TCP (ensures reliable message delivery)

### Assignment Details

#### Motivation

In the rapidly evolving landscape of the Internet, there is a shift towards on-demand consumption of various content types in real-time. This project addresses the challenges posed to the underlying IP infrastructure by designing an Over-the-Top streaming service.

#### Objectives

Using the CORE emulator as the testing platform, the primary objectives include:

1. Designing a prototype for real-time audio/video/text delivery from a content server to multiple clients.
2. Selecting a Rendezvous Point (RP) responsible for content distribution.
3. Creating and optimizing a shared distribution tree for efficient content delivery.
4. Implementing strategies for constructing and organizing the application overlay, crucial for supporting quality of service.
5. Monitoring server conditions and dynamically selecting the most appropriate server for content distribution based on a calculated metric.

### Implementation Steps

#### Step 1: Preparation of Activities

* Choose a programming language (Java) for group compatibility.
* Set up a test topology using the CORE emulator.
* Decide on the transport protocol for the overlay (TCP/UDP).
* Implement a simple client/server using the chosen transport protocol.

#### Step 2: Overlay Topology Construction with Shared Tree

* Develop an application capable of full-duplex communication.
* Define a strategy for building the overlay network.

#### Step 3: Streaming Service

* Implement a basic client/server for streaming based on provided examples.
* Use a test video (e.g., movie.Mjpeg) for initial testing.

#### Step 4: Server Content Monitoring

* Establish a test message exchange between RP and Servers for real-time server condition updates.
* The establishment of the best paths are based only in the latency/rtt

#### Step 5: Data Delivery Flow Construction

* Implement a mechanism for clients to request content and receive it from the nearest node.
* Optimize data transmission to minimize network traffic and the number of content transfer flows.

### How to deploy the project

- Make your core network setup 
- Edit the xml config file and specify if each node is a client, RP or just a intermediate node
- Run `make` to deploy the project (*you have to do this in each node*)

---

### Credits: [Nelson Almeida](https://github.com/NelsonAlmeida-18)
