*This project has been created as part of the 42 curriculum by \[okorkech\].*

# NetPractice

## Description

NetPractice is a practical networking project designed to introduce the fundamentals of network architecture and IP addressing. The goal of this project is to successfully configure small-scale simulated networks to ensure seamless communication between specific hosts. By solving a series of increasingly complex puzzles, you gain hands-on experience in allocating IP addresses, calculating subnets, and establishing correct routing paths across various network topologies.

## Instructions

To launch and complete the NetPractice exercises, follow these steps:

**Running the Interface:**

1. Clone the repository to your local machine.

2. Launch the interactive training interface by executing the provided script in your terminal: `./run.sh` (or by opening the generated `index.html` file in your preferred web browser, depending on your local setup).

**Exporting Configurations:**
Once you successfully solve a level and the goal status shows as "OK", you must save your work. Click the "Get my config" (or equivalent download) button provided in the interface for that specific level. This will download a configuration file capturing your successful setup.

**Submission Requirements:**
For your final evaluation, you must submit exactly **10 exported configuration files** (one corresponding to each of the 10 levels). All 10 of these configuration files must be placed directly at the **root** of your Git repository prior to pushing your final commit.

## Resources

This project requires a solid understanding of fundamental networking concepts.

**Networking Concepts Studied:**

* **TCP/IP Addressing:** Understanding public vs. private IP ranges.

* **Subnet Masks:** Utilizing CIDR notation (e.g., `/24`, `/25`) to divide network blocks and prevent overlapping subnets.

* **Default Gateways:** Configuring "Gateway of Last Resort" routes (`0.0.0.0/0` or `default`) for upstream internet traffic.

* **Routers and Switches:** Understanding how switches handle local traffic and how routers bridge distinct subnets via "Next Hop" IP addresses.

* **Network Layer Models:** Understanding how network communication is structured (see schema below).

**OSI vs. TCP/IP Models Schema:**

| OSI Model (7 Layers) | TCP/IP Model (4 Layers) | Protocols / Data Unit | 
| ----- | ----- | ----- | 
| **7. Application** | **Application** | HTTP, DNS, DHCP, FTP (Data) | 
| **6. Presentation** | (Combines OSI 5, 6, & 7) | Encryption, Formatting | 
| **5. Session** |  | Session establishment | 
| **4. Transport** | **Transport** | TCP, UDP (Segments/Datagrams) | 
| **3. Network** | **Internet** | IP, ICMP, Routing (Packets) | 
| **2. Data Link** | **Network Access / Link** | MAC Addresses, Switches (Frames) | 
| **1. Physical** | (Combines OSI 1 & 2) | Cables, Hardware (Bits) | 

**References & Tutorials:**

* [NetworkChuck: You Suck at Subnetting (Playlist)](https://www.youtube.com/playlist?list=PLIhvC56v63IJVXv0GJcl9vO5Z6znCVb1P)

* [Jeremy's IT Lab - Free CCNA: IPv4 Addresses & Subnetting](https://www.youtube.com/watch?v=aHwAm8GYbn8)

* [Wikipedia: Classless Inter-Domain Routing (CIDR)](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)

* [Subnet Calculator](https://www.calculator.net/ip-subnet-calculator.html)

**AI Usage:**
Artificial Intelligence (Google Gemini) was utilized during the development of this project as an interactive study partner. AI was used specifically to clarify the theoretical differences between default routes and specific "Next Hop" routes, to understand the "Longest Prefix Match" algorithm, and to help diagnose the conceptual reasons behind overlapping subnet conflicts (such as slicing a `/24` into `/25` or `/26` subnets) in the more advanced routing levels. AI was not used to generate the final configuration files.