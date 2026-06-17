## Core Idea

The Internet can be described in two ways: as a **nuts-and-bolts hardware/software system**, and as an **infrastructure that provides services to distributed applications**.

---

## 1.1.1 – Nuts & Bolts Description

**Hosts / End Systems**

- The Internet interconnects billions of devices worldwide
- All devices (PCs, phones, TVs, cars, thermostats, watches, consoles…) are called **hosts** or **end systems**
- ~2/3 of the world's population are active mobile Internet users
- Term "computer network" is becoming outdated given nontraditional devices

**How Data Travels**

- End systems are connected via **communication links** and **packet switches**
- Link types (physical media): coaxial cable, copper wire, optical fiber, radio spectrum
- Each link transmits at a rate measured in **bits/second**
- Sending end system: segments data → adds **header bytes** to each segment → forms **packets**
- Packets are sent through the network → reassembled at destination

**Packet Switches**

- Takes a packet on an incoming link → forwards it on an outgoing link
- Two main types:
  - **Routers** → used in the network core
  - **Link-layer switches** → used in access networks
- Both forward packets toward their destination
- The path a packet takes = **route** or **path**

**Transportation Analogy**

- Packets = trucks
- Communication links = highways/roads
- Packet switches = intersections
- End systems = buildings

**ISPs (Internet Service Providers)**

- End systems access Internet through ISPs
- Types of ISPs:
  - Residential (cable, telephone companies)
  - Corporate
  - University
  - Public WiFi (airports, hotels, coffee shops)
  - Cellular data ISPs
- Each ISP is itself a network of packet switches and communication links
- Access types offered: cable modem, DSL, high-speed LAN, mobile wireless
- ISPs also connect content providers (servers) directly to the Internet
- ISPs are **tiered**: lower-tier ISPs connect through national/international **upper-tier ISPs**
- Upper-tier ISPs: high-speed routers + high-speed fiber-optic links
- Every ISP network is **managed independently**, runs **IP protocol**, follows naming/address conventions

**Protocols & Standards**

- Everything in the Internet runs protocols to control sending/receiving
- Two most important: **TCP** (Transmission Control Protocol) and **IP** (Internet Protocol)
- IP defines the **format of packets** sent/received among routers and end systems
- Together called **TCP/IP**
- Standards developed by **IETF** (Internet Engineering Task Force)
- IETF documents = **RFCs** (Requests for Comments)
- RFCs define protocols: TCP, IP, HTTP, SMTP
- Other standards bodies: **IEEE 802 LAN Standards Committee** (for network links)

---

## 1.1.2 – Services Description

**Internet as a Platform**

- Internet = infrastructure providing services to **distributed applications**
- Distributed apps: involve multiple end systems exchanging data
- Examples: email, web, messaging, maps, music/video streaming, social media, video conferencing, multiplayer games, location-based systems
- **Apps run on end systems** — NOT on packet switches in the network core
- Packet switches don't care about the application — they just forward data

**Socket Interface**

- How does a program on one end system send data to a program on another?
- Answer: **socket interface** — a set of rules a sending program must follow so the Internet delivers data to the destination program
- Postal analogy:
  - Letter = data
  - Envelope + address + stamp + mailbox = socket interface rules
  - Alice can't just drop a letter out the window — she must follow postal rules
  - Same for programs — must follow socket interface to send data
- Internet provides **multiple services** → when building an app you choose which service fits (details in Chapter 2)

---

## 1.1.3 – What Is a Protocol?

**Human Analogies**

_Asking for the time:_

- "Hi" → "Hi" → "What's the time?" → "2:00"
- A rude/no response = communication fails → no useful work done
- Specific messages + specific actions based on replies = protocol

_Classroom analogy:_

- Teacher: "Any questions?" → student raises hand → teacher says "Yes…" → student asks → teacher answers
- Same pattern: message → response → action

**Key Point:** If two people run **different protocols** (one has manners, one doesn't) → they **cannot interoperate** → no useful work done. Same in networking.

**Network Protocols**

- Same as human protocols but entities are **hardware or software components** (computers, routers, smartphones…)
- **All** Internet activity between 2+ remote entities is governed by a protocol
- Examples of protocols running right now:
  - Hardware protocols: control flow of bits between network interface cards
  - Congestion-control protocols: control packet transmission rate between sender/receiver
  - Router protocols: determine a packet's path from source to destination

**Web Request Example (protocol in action):**

1. Your computer sends a **connection request** to web server
2. Web server returns a **connection reply**
3. Your computer sends a **GET message** (name of the web page)
4. Web server returns the **web page**

**Official Definition:**

> A protocol defines the **format** and **order** of messages exchanged between two or more communicating entities, as well as the **actions taken** on transmission and/or receipt of a message or other event.

**Bottom line:** Mastering computer networking = understanding the **what, why, and how** of networking protocols.
