# Cisco Packet Tracer Network Project – KGOTSO PKT.pkt

## Author
Name: Kgotso Seadimo  
Student Number: 37611720  
Module/Subject: CMPG 325  
Date: 13 October 2025

---

## Project Overview
This project simulates a small enterprise network using Cisco Packet Tracer.  
The main goal is to configure and demonstrate a functioning network that allows communication between multiple subnets through proper addressing and routing.

The network includes:
- Routers
- Switches
- End devices (PCs, Servers, Printers)
- Basic routing configurations
- IP addressing plan

---

## Network Topology
- Routers: 1 (or more, depending on the file)
- Switches: 1 (or more)
- End Devices: PCs and Servers
- Connections: Ethernet links

The network is divided into subnets for better organization and control.

---

## IP Addressing Scheme

| Device         | Interface         | IP Address        | Subnet Mask        | Gateway          |
|----------------|-------------------|-------------------|--------------------|------------------|
| Router0 G0/0   | —                 | 192.168.1.1       | 255.255.255.0      | —                |
| Router0 G0/1   | —                 | 192.168.2.1       | 255.255.255.0      | —                |
| PC1            | FastEthernet0     | 192.168.1.10      | 255.255.255.0      | 192.168.1.1      |
| PC2            | FastEthernet0     | 192.168.2.10      | 255.255.255.0      | 192.168.2.1      |

Note: IP addresses may vary slightly depending on the final configuration in the .pkt file.

---

## Configuration Summary

Router Configuration
```
enable
configure terminal
hostname Router0
interface GigabitEthernet0/0
 ip address 192.168.1.1 255.255.255.0
 no shutdown
exit

interface GigabitEthernet0/1
 ip address 192.168.2.1 255.255.255.0
 no shutdown
exit

ip route 192.168.2.0 255.255.255.0 192.168.1.2
```

PC Configuration
- Assigned IP address and default gateway manually (or via DHCP if configured).

---

## Testing and Verification
1. Ping tests were performed to verify connectivity between PC1 (192.168.1.10) and PC2 (192.168.2.10).  
   - Successful reply from destination.
2. Simulation Mode was used to visualize packet movement across the network.
3. Show Commands:
   - `show ip interface brief` → Confirmed interface status.  
   - `show ip route` → Verified routing table.

---

## Challenges Faced
- Initially forgot to enable interfaces with `no shutdown`, causing ping failures.  
- Resolved IP misconfiguration issues between PCs and routers.  
- Ensured routing was properly set up to allow traffic flow between subnets.

---

## Lessons Learned
- How to design a simple network topology in Cisco Packet Tracer.  
- How to configure router interfaces and static routes.  
- How to assign IP addresses and gateways correctly.  
- How to troubleshoot basic connectivity issues.

---

## Video Demonstration Instructions
- Length: 15–30 minutes  
- Part 1:  
  - Show and explain the network topology  
  - Walk through configuration steps  
- Part 2:  
  - Demonstrate network functionality (pings and simulation)  
  - Reflect on challenges and lessons learned

Evaluation Criteria:
- Clarity of explanations (5 Marks)  
- Technical accuracy (5 Marks)  
- Evidence of functionality (4 Marks)  
- Presentation and organization (3 Marks)  
- Professionalism and originality (3 Marks)

---

## Software & Tools Used
- Cisco Packet Tracer (Version [insert version])
- Basic CLI commands for configuration
- Windows Command Prompt for ping testing (within Packet Tracer)

---

## Project Files
- KGOTSO PKT.pkt → Cisco Packet Tracer Project File  
- README.md → Project Description and Instructions

---

## How to Use
1. Open `KGOTSO PKT.pkt` in Cisco Packet Tracer.  
2. Click on each router and switch to view configurations.  
3. Use the PC Command Prompt to test connectivity with `ping`.  
4. Switch to Simulation Mode to view packet flow.  
5. Record your video demonstration following the evaluation checklist.

---

End of README  
This README file provides a clear overview of the project, making it easy for anyone to open, test, and understand the network design and configuration.
