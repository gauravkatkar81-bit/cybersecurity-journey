# Module 5: Networking Fundamentals
**Path:** TryHackMe - Pre-Security
**Date Completed:** 28 October 2026
**Focus:** What is Networking, Intro to LAN, OSI Model (7 Layers), Packets & Frames, Expanding Your Network

---

## 📌 1. Key Concepts Learned
- **What is Networking:** The Internet, IP addresses, MAC addresses, and using `ping` (using ICMP packets to check connection performance).
- **Intro to LAN:** LAN (Local Area Network) topologies (Star, Bus, Ring/Token), switches, routers, subnetting, how ARP (Address Resolution Protocol) works, and DHCP (Dynamic Host Configuration Protocol).
- **OSI Model:** The 7 layers (Physical, Data Link, Network, Transport [TCP vs. UDP], Session, Presentation, Application).
- **Packets & Frames:** Packets, frames, the TCP 3-way handshake, TCP (Transmission Control Protocol), UDP (User Datagram Protocol), protocols, and ports.
- **Expanding Your Network:** Port forwarding, firewalls (Stateful and Stateless), VPNs (Virtual Private Network), and protocols like PPP, PPTP, and IPsec.

---

## 🧪 2. Hands-On Lab Walkthroughs & Exercises

### Lab 1: LAN & Topologies Overview
- **Tasks:** Learn about LAN topologies, advantages, disadvantages, and IP/subnet configuration concepts.
- **Action:**
  1. Reviewed different network topologies (Star, Bus, Ring) through interactive concept slides.
  2. Explored how switches and routers handle local traffic and how DHCP assigns IP addresses dynamically.
- **Key Takeaway:** Understanding how devices connect locally and why star topology is the most common today.

### Lab 2: OSI Model Layer Sorting Game
- **Tasks:** Practice matching protocols and networking devices to their correct OSI layers.
- **Action:**
  1. Played the interactive OSI layer sorting exercise on TryHackMe.
  2. Dragged and matched protocols (like HTTP, TCP, IP) and hardware (like switches and routers) to their respective layers (Layers 1 through 7).
- **Key Takeaway:** Memorizing how data flows down the 7 layers on the sender side and back up on the receiver side.

### Lab 3: Packet Simulation & Firewall Rules
- **Tasks:** Analyze packet flow between computers and block malicious traffic using firewall rules.
- **Action:**
  1. Observed simulated packet and frame transmissions between two computers.
  2. Tested sending multiple packets to check connection behavior.
  3. Configured basic firewall rules to stop unauthorized traffic and protect the system from getting attacked.
- **Key Takeaway:** Seeing how packets move across networks in real-time and how firewall rules filter traffic to secure a network.

---

## 🛠️ Commands & Tools Summary
| Tool / Concept | Function |
| :--- | :--- |
| **`ping`** | Network utility using ICMP to test connection reachability and latency |
| **ARP** | Protocol used to resolve an IP address to a physical MAC address on a LAN |
| **Firewall** | Security system (Stateful/Stateless) used to allow or block network traffic based on rules |
| **VPN** | Encrypted tunnel used to secure private network traffic over the public internet |
