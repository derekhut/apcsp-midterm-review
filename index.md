# 2025-2026 SCLS APCSP REVIEW MATERIALS

**Last Updated:** November 13, 2025

---

## Table of Contents

### [BIG IDEA: DATA](#big-idea-data)
- [Number Systems](#number-systems)
- [Bits and Bytes](#bits-and-bytes)
- [Calculations with Bits](#calculations-with-bits)
- [Analog vs. Digital Data](#analog-vs-digital-data)
- [Data Abstraction](#data-abstraction)
- [Data Compression](#data-compression)
  - [Lossless Compression](#lossless-data-compression)
  - [Lossy Compression](#lossy-data-compression)

### [BIG IDEA: COMPUTER SYSTEMS AND NETWORKS](#big-idea-computer-systems-and-networks)
- [The Internet](#the-internet)
- [Computing Components](#computing-components)
- [Packets and Routing](#how-data-travels-packets-and-routing)
- [Network Performance Metrics](#network-performance-metrics)
- [Internet Protocols](#internet-protocols)
  - [TCP/IP](#tcpip-transmission-control-protocol--internet-protocol)
  - [UDP](#udp-user-datagram-protocol)
  - [HTTP](#http-hypertext-transfer-protocol)
- [Network Design Principles](#network-design-principles)

### [THE DIGITAL DIVIDE](#the-digital-divide)
- [Factors That Influence the Digital Divide](#factors-that-influence-the-digital-divide)
- [Harmful Impacts](#harmful-impacts-of-the-digital-divide)
- [Reducing the Digital Divide](#reducing-the-digital-divide)

### [QUICK REFERENCE](#quick-reference)

---

# BIG IDEA: DATA

## Fundamental Concepts

**Data:** A collection of facts

**Number base:** The number of digits or digit combinations that a system uses to represent values

---

## Number Systems

### Decimal System (Base 10)
- Uses combinations of 0-9 to represent values
- Example: The number 5,729

| Power of 10 | 10³ | 10² | 10¹ | 10⁰ |
|-------------|-----|-----|-----|-----|
| Value represented (base 10) | 1000 | 100 | 10 | 1 |
| Amount of value | 5 | 7 | 2 | 9 |

### Binary System (Base 2)
- Only uses combinations of 0 and 1
- Example: The number 5 in binary is 101

| Power of 2 | 2³ | 2² | 2¹ | 2⁰ |
|------------|----|----|----|----|
| Value represented (base 10) | 8 | 4 | 2 | 1 |
| Amount of value | 0 | 1 | 0 | 1 |

The 1s signify which place values to add. In this case: 4 + 1 = 5

---

## Bits and Bytes

**Bit (Binary Digit):** The smallest unit of information stored or manipulated on a computer
- Represented as 0 or 1
- Basic building blocks of storage (like amino acids for proteins)
- Can represent: False/True, Off/On, No/Yes

**Byte:** A group of 8 bits
- 8 bits = 2⁸ = 256 unique combinations (values 0-255)
- Example: Color representation
  - Black = 0, White = 1
  - RGB color: [255, 255, 255] in decimal
  - Or: [11111111, 11111111, 11111111] in binary (3 bytes of data)

---

## Calculations with Bits

### To calculate the largest value with **n bits:**
**Formula:** 2ⁿ - 1

**Example:** What's the largest value you can represent with 8 bits?
- 2⁸ - 1 = 256 - 1 = **255**

**Example:** What's the largest value you can represent with 7 bits?
- 2⁷ - 1 = 128 - 1 = **127**

### To calculate the total number of unique values:
**Formula:** 2ⁿ

**Example:** How many different values can 8 bits represent?
- 2⁸ = **256** (representing values 0-255)

---

## Analog vs. Digital Data

### Analog Data
- Data that is measured **continuously**
- Changes very smoothly over time
- Examples: Volume of music, position of a runner, temperature throughout the day
- As time changes, data is being recorded constantly without breaks

### Digital Data
- Data represented in a **finite set of discrete values**
- Must be formatted as specific, distinct values
- Example: A YouTube video shows you've watched "10 minutes" (not 10.4387392 minutes)

### From Analog to Digital: Sampling

**Sampling:** Recording an analog signal at regular discrete moments and converting them to digital signals that can be stored on digital media

To store or process analog data digitally, we use sampling - recording values at regular intervals rather than continuously.

**Real-world example:**
- **Digital:** Watching a video on YouTube - you can see the exact duration (10:00)
- **Analog:** Watching a live game at a venue - it flows continuously with no discrete time markers

---

## Data Abstraction

**Data Abstraction:** Filtering out specific details to focus on the information needed to process the data

- Digital data is a simplified representation that leaves out extra details
- Example: Storing a date as "11/13/2025" instead of recording every millisecond
- Using digital data to approximate real-world analog data is considered an abstraction
- We accept this loss of precision for practical storage and processing

---

## DATA COMPRESSION

File types like MP3, MP4, and JPG all use data compression. Without it, a 3-minute song would be over 100MB!

**Data Compression:** A set of steps for packing data into a smaller space while allowing the original data to be accessed

### Key Concepts
- **Two-way process:** Compress data into a smaller package OR decompress back to original form
- **Useful for:** Saving disk space and reducing bandwidth
- **How it works:** Deals with strings of bytes and compresses them into smaller sets
- **Goal:** Condense large files by removing redundancy while retaining essential information

### Compression Process
1. **Encoding algorithm:** Takes a message or image and generates a compressed representation
2. **Decoding algorithm:** Reconstructs the original message (or an approximation)

### Compression Effectiveness Depends On:
1. The amount of **redundancy** or repeated information in the file
2. The **compression method** used

---

## Types of Compression

### Run-Length Encoding (Example)
Works by replacing repeating data with a count and the value

**Example:** `FFFFFIIIIIIVVVVVVVEEEE` becomes `5F6I7V4E`

---

### LOSSLESS DATA COMPRESSION

**Definition:** Reduces file size without sacrificing ANY original data

**Characteristics:**
- Can reconstruct the original message **exactly** from the compressed version
- Packs data so the compressed file can be decompressed with perfect accuracy
- Very important for programs where even small changes could make them unusable

**Used mainly for:** Text files, executable programs, documents

**Examples:**
- Run-length encoding
- ZIP files
- PNG images

---

### LOSSY DATA COMPRESSION

**Definition:** Sacrifices some data to achieve greater compression

**Characteristics:**
- Can only reconstruct an **approximation** of the original message
- Achieves high degrees of compression, resulting in much smaller files
- Some original pixels, sound waves, or video frames are removed **FOREVER**
- Loss of quality/detail in exchange for smaller file size

**Used mainly for:** Images, audio, and video

**Examples:**
- Converting color images to grayscale
- Lowering image resolution
- Reducing audio quality
- JPEG images
- MP3 audio
- MP4 video

---

## Important Principles

✓ **Fewer bits does not necessarily mean less information**

✓ **The amount of size reduction depends on:**
  - The amount of redundancy in the original data
  - The compression algorithm applied

✓ **Trade-off:** Amount of compression ⬆️ → Size of resulting file ⬇️

✓ **Choice matters:** Use lossless when you need perfect accuracy; use lossy when file size is more important than perfect quality

# BIG IDEA: COMPUTER SYSTEMS AND NETWORKS

## Fundamental Concepts

### The Internet
**Internet:** A computer network consisting of interconnected networks that use standardized, **open (non-proprietary)** communication protocols

**Key characteristics:**
- **Open network:** Any computing device can join as long as it follows the rules (protocols)
- Connects multiple computer networks together
- Uses standardized protocols that anyone can implement

---

## Computing Components

### Computing Device
A physical machine that can run a program
- Examples: computers, smartphones, tablets, servers, IoT devices

### Computing Network
A group of computing devices that can share data with each other

### Computing System
A group of computing devices and programs working together for a common purpose

---

## How Data Travels: Packets and Routing

When you send or receive data from the internet, the data is often too large to send all at once, so it's broken up into **packets**.

### Packets
**Packet:** A small unit of data sent over a network

**Structure of a packet:**
- **Data section:** Contains a portion of the information you want to send
- **Header:** Contains metadata (data about data) including:
  - Where the packet is from (source address)
  - Where it's going (destination address)
  - How it should be reassembled
  - Sequence number

### Routing
**Path:** A sequence of connected computing devices (called **routers**) that packets travel through

**Routing:** The process of finding a path for packets to travel from source to destination

**Important note:** Packets can arrive at their destination in order OR out of order! The receiving device must reassemble them correctly.

---

## Network Performance Metrics

### Bandwidth
**Bandwidth:** The maximum amount of data that can be transmitted over a network connection in a given amount of time

- Measured in **bits per second (bps)** or **megabits per second (Mbps)**
- Think of it as the "width of the pipe" - how much data can flow through at once
- Higher bandwidth = more data can be transferred simultaneously

### Latency
**Latency:** The time delay between when data is sent and when it is received

- Measured in **milliseconds (ms)**
- Think of it as "how long it takes" for data to travel
- Lower latency = faster response time
- Affected by: distance, number of routers, network congestion

---

## Internet Protocols

In order for computing devices to communicate with each other over the internet, they all must use the same protocols!

**Protocol:** A standard set of rules that everyone agrees to follow
- Protocols are **open** or **non-proprietary** (anyone can use them)

---

### TCP/IP (Transmission Control Protocol / Internet Protocol)

The foundational protocol suite of the internet

#### TCP (Transmission Control Protocol)
- Governs how packets are **created and reassembled**
- Provides **reliable, ordered, and error-checked** delivery of data packets
- Packets MAY arrive out of order, but TCP ensures they are reassembled correctly
- If packets are lost, TCP requests re-delivery

#### IP (Internet Protocol)
- Moves packets to their destinations
- Dictates how devices are given addresses for communication

**IP Address:** A unique numerical label assigned to each device on a network

---

### IP Address Versions

#### IPv4 (Internet Protocol version 4)
- **Format:** Four numbers separated by periods
- **Example:** 74.125.20.113
- **Range:** Each number ranges from 0-255
- **Total addresses:** 2^32 ≈ 4.3 billion possible addresses
- **Problem:** We're running out of IPv4 addresses!

#### ⭐ IPv6 (Internet Protocol version 6)
- **Format:** Eight groups of hexadecimal numbers separated by colons
- **Example:** 2001:0db8:0000:0042:0000:8a2e:0370:7334
- **Total addresses:** 2^128 ≈ 340 undecillion possible addresses
- **Benefit:** Provides vastly more addresses to accommodate growing internet devices

---

### UDP (User Datagram Protocol)

An alternative to TCP that prioritizes speed over reliability

**Characteristics:**
- Does **NOT** guarantee delivery or order of packets
- Does **NOT** include error-checking (unlike TCP)
- Eliminates the overhead of TCP's reliability features
- Delivers a faster stream of information

**Use cases:**
- Live video streaming
- Online gaming
- Voice over IP (VoIP)
- Situations where speed matters more than perfect accuracy

---

### HTTP (Hypertext Transfer Protocol)

**HTTP:** The protocol that controls how web page data is transmitted

- Enables communication between web browsers and web servers
- Used specifically for the **World Wide Web**

---

## The World Wide Web (WWW)

**World Wide Web:** A system of linked web pages, programs, and files that is accessible via the internet

**Important distinction:**
- **TCP, IP, and UDP:** Used to transmit data over a variety of networks (the entire internet)
- **HTTP:** Used specifically to transmit data over the **World Wide Web**

🌟 **Don't confuse them:** The World Wide Web is just one service that runs ON the internet!

---

## Network Design Principles

### Scalability
**Scalability:** The capacity for a system to change in size and scale to meet new demands

- A scalable system can grow to accommodate more users, devices, or data
- Important for long-term viability of networks

---

### Fault Tolerance 🔥

**Fault Tolerance:** The ability of a system to continue functioning properly even when one or more parts fail

#### Redundancy
**Redundancy:** The inclusion of extra components that can be used if other components fail

- Multiple paths for data to travel
- Backup servers
- Duplicate hardware components

**Example:** If one router fails, packets can be rerouted through other routers

---

### Benefits of Fault Tolerance

✅ **Reduces hardware malfunctions** - Issues with physical computer components don't bring down the entire system

✅ **Protects against cyber attacks** - Deliberate attempts by individuals to gain unauthorized access have less impact

✅ **Increases system reliability** - The system is less likely to completely fail

✅ **Prevents complete shutdowns** - Critical services can continue operating

✅ **Mitigates DDoS attacks** - A Distributed Denial of Service (DDoS) attack occurs when a server or network is overwhelmed with a flood of traffic, causing it to slow down or crash. With redundant servers or network connections, you can route around the attack and continue operating.

✅ **Easier system expansion** - Adding new components is simpler when the system is designed with redundancy

---

### Disadvantages of Fault Tolerance

❌ **Requires more resources** - Need duplicate or backup systems

❌ **Expensive** - Higher costs for materials, setup, and ongoing maintenance

❌ **Complexity** - More components mean more potential points of management

---

## Key Takeaways

- The internet is a network of networks using open, standardized protocols
- Data travels in packets with headers containing routing information
- TCP provides reliable delivery; UDP provides faster delivery
- IPv6 solves the address shortage problem of IPv4
- HTTP is for the World Wide Web specifically
- Fault tolerance and scalability are essential design principles for reliable networks

# THE DIGITAL DIVIDE

## What is the Digital Divide?

**Digital Divide:** The gap between those who have access to technology and the internet and those who don't

This divide creates inequalities in opportunities, resources, and participation in modern society.

---

## Factors That Influence the Digital Divide

### 1. Demographics
- **Age:** Younger people are generally more comfortable with technology and more likely to use it regularly
- **Education level:** People with higher levels of education tend to use the internet more frequently and effectively

### 2. Socioeconomic Status
- **Income:** People with higher incomes are more likely to be able to purchase and maintain technology
- **Cost barriers:** Devices, internet service, and maintenance can be expensive

### 3. Geographic Location
- **Urban vs. Rural:** Some areas have better internet infrastructure and access than others
- **Infrastructure:** Rural and remote areas often lack high-speed internet access
- **International differences:** Developed countries generally have better internet access than developing countries

---

## Harmful Impacts of the Digital Divide

### Educational Opportunities
**Example:** During the 2020 COVID-19 pandemic, many schools across the US shifted to virtual learning systems. Students without stable internet connections or access to devices suffered educationally, falling behind their peers who had reliable technology access.

**Other impacts:**
- Limited access to online educational resources
- Inability to complete digital assignments
- Reduced digital literacy skills

### Employment Opportunities
**Impacts:**
- Those without internet access may be at a disadvantage when finding and applying for jobs (most applications are online)
- Unable to access remote work opportunities
- Limited ability to develop digital skills required for modern jobs
- Difficulty accessing professional development resources

### Civic Participation
- Reduced ability to access government services online
- Limited participation in digital democratic processes
- Difficulty staying informed about current events

### Social Connection
- Reduced ability to maintain relationships through digital communication
- Limited access to online communities and support networks

---

## Reducing the Digital Divide

### Educational Initiatives
**Digital Literacy Programs:** Programs that teach people how to use the internet, computers, and digital tools effectively
- Organizations can release educational resources to help people navigate technology
- Libraries and community centers can offer free training

### Infrastructure Investment
- Local and national governments can fund businesses and projects that provide internet access to underserved areas
- Subsidies for internet service in low-income areas
- Public Wi-Fi in community spaces

### Device Access Programs
- Providing low-cost or free devices to students and families in need
- Device lending programs through schools and libraries

### Policy Solutions
- Net neutrality protections
- Universal broadband initiatives
- Affordable internet programs

---

# QUICK REFERENCE

## Essential Formulas

### Bit Calculations
| Formula | Purpose | Example |
|---------|---------|---------|
| **2ⁿ - 1** | Largest value with n bits | 8 bits: 2⁸ - 1 = **255** |
| **2ⁿ** | Total unique values with n bits | 8 bits: 2⁸ = **256** values (0-255) |

### IPv4 vs IPv6
| Version | Format | Total Addresses | Example |
|---------|--------|-----------------|---------|
| **IPv4** | Four decimal numbers (0-255) | 2³² ≈ 4.3 billion | 74.125.20.113 |
| **IPv6** | Eight hexadecimal groups | 2¹²⁸ ≈ 340 undecillion | 2001:0db8:0000:0042:0000:8a2e:0370:7334 |

---

## Key Definitions at a Glance

### Data & Representation
- **Bit:** Smallest unit of data (0 or 1)
- **Byte:** 8 bits = 256 possible values
- **Analog Data:** Continuous measurement over time
- **Digital Data:** Discrete, finite set of values
- **Sampling:** Converting analog signals to digital at regular intervals
- **Data Abstraction:** Filtering details to focus on needed information

### Compression
| Type | Data Loss | Use Cases | Examples |
|------|-----------|-----------|----------|
| **Lossless** | None | Text, programs, exact data | ZIP, PNG |
| **Lossy** | Some (permanent) | Media files, file size priority | JPEG, MP3, MP4 |

### Network Fundamentals
- **Internet:** Interconnected networks using open, standardized protocols
- **Packet:** Small unit of data with header (metadata) and data section
- **Routing:** Finding a path for packets from source to destination
- **Bandwidth:** Maximum data transmitted per time unit (bps/Mbps)
- **Latency:** Time delay between sending and receiving data (ms)
- **Protocol:** Standard set of rules for communication

### Protocols Comparison
| Protocol | Reliability | Speed | Error Checking | Use Cases |
|----------|-------------|-------|----------------|-----------|
| **TCP** | High (guaranteed delivery) | Slower | Yes | Web browsing, file transfers, email |
| **UDP** | Low (no guarantee) | Faster | No | Streaming, gaming, VoIP |
| **HTTP** | N/A | N/A | N/A | World Wide Web communication |

### Network Design
- **Scalability:** Ability to grow and meet new demands
- **Fault Tolerance:** Continue functioning when parts fail
- **Redundancy:** Extra components as backup

### Digital Divide
- **Definition:** Gap between those with and without technology access
- **Key Factors:** Demographics (age, education), socioeconomic status (income), geographic location (urban vs rural)
- **Impact Areas:** Education, employment, civic participation, social connection

---

## Practice Questions

### Data Section

**Q1:** How many unique values can you represent with 6 bits?
<details>
<summary>Click for answer</summary>

**Answer:** 2⁶ = **64 unique values** (representing 0 through 63)
</details>

**Q2:** What is the largest value you can represent with 10 bits?
<details>
<summary>Click for answer</summary>

**Answer:** 2¹⁰ - 1 = 1024 - 1 = **1023**
</details>

**Q3:** Is a temperature sensor reading analog or digital data? Why?
<details>
<summary>Click for answer</summary>

**Answer:** **Analog data** - Temperature changes continuously over time. However, when stored in a computer, it must be sampled at regular intervals and converted to digital data.
</details>

**Q4:** Should you use lossless or lossy compression for a medical X-ray image? Why?
<details>
<summary>Click for answer</summary>

**Answer:** **Lossless compression** - Medical images require perfect accuracy for diagnosis. Any loss of detail could lead to misdiagnosis or missed conditions.
</details>

**Q5:** Convert binary 1101 to decimal.
<details>
<summary>Click for answer</summary>

**Answer:**
- 1×2³ + 1×2² + 0×2¹ + 1×2⁰
- = 8 + 4 + 0 + 1
- = **13**
</details>

---

### Computer Systems and Networks Section

**Q6:** What are the two main components of a packet?
<details>
<summary>Click for answer</summary>

**Answer:**
1. **Header** - Contains metadata (source address, destination address, sequence number, reassembly info)
2. **Data section** - Contains the actual information being sent
</details>

**Q7:** Can packets arrive out of order? How are they reassembled?
<details>
<summary>Click for answer</summary>

**Answer:** **Yes**, packets can arrive out of order. TCP (Transmission Control Protocol) uses sequence numbers in the packet headers to reassemble them in the correct order at the destination.
</details>

**Q8:** When would you choose UDP over TCP?
<details>
<summary>Click for answer</summary>

**Answer:** Choose UDP when **speed is more important than perfect accuracy**:
- Live video streaming
- Online gaming
- Voice over IP (VoIP)
- Real-time applications where occasional data loss is acceptable
</details>

**Q9:** Your home has 200 Mbps bandwidth but you experience lag when video calling. What's likely the issue?
<details>
<summary>Click for answer</summary>

**Answer:** The issue is likely **high latency**, not bandwidth. Latency (delay) affects real-time communication more than bandwidth. Distance, router hops, or network congestion could be causing the lag.
</details>

**Q10:** How does redundancy improve fault tolerance?
<details>
<summary>Click for answer</summary>

**Answer:** Redundancy provides **backup components and alternate paths**. If one component fails (router, server, connection), traffic can automatically reroute through redundant systems, preventing complete system failure.
</details>

---

### Digital Divide Section

**Q11:** Name three factors that contribute to the digital divide.
<details>
<summary>Click for answer</summary>

**Answer:**
1. **Demographics** - Age and education level affect technology adoption
2. **Socioeconomic status** - Income affects ability to purchase devices and internet service
3. **Geographic location** - Rural areas often lack infrastructure for high-speed internet
</details>

**Q12:** How did the 2020 COVID-19 pandemic highlight the digital divide in education?
<details>
<summary>Click for answer</summary>

**Answer:** When schools shifted to virtual learning, students without stable internet or devices fell behind peers with reliable technology access. This created significant educational inequalities based on digital access.
</details>

**Q13:** Suggest two ways to reduce the digital divide.
<details>
<summary>Click for answer</summary>

**Answer:** (Any two of these)
- **Digital literacy programs** - Free training at libraries/community centers
- **Infrastructure investment** - Government funding for underserved areas
- **Device access programs** - Low-cost or free devices for students in need
- **Policy solutions** - Net neutrality, universal broadband initiatives, affordable internet programs
</details>

---

## Study Tips

1. **Focus on formulas:** Memorize 2ⁿ and 2ⁿ - 1 - they appear frequently
2. **Know the differences:** TCP vs UDP, Lossless vs Lossy, IPv4 vs IPv6, Analog vs Digital
3. **Understand real-world applications:** Connect concepts to everyday technology use
4. **Practice conversions:** Binary to decimal and vice versa
5. **Think about trade-offs:** Compression vs quality, Speed vs reliability, Cost vs redundancy
