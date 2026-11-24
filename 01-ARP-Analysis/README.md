# Experiment 01: ARP Analysis

## 1. Objective
To understand how the Address Resolution Protocol (ARP) maps an IPv4 address to a MAC address within a local network.

## 2. Tools Used
- Cisco Packet Tracer
- Simulation Mode
- Command Prompt (PC terminal)

## 3. Network Setup
The experiment used a simulated LAN containing:
- One router
- One switch
- Three PCs
- One server

The devices were connected through the switch.

## 4. Procedure
1. Switched Cisco Packet Tracer to Simulation Mode.
2. Selected ARP as the protocol filter.
3. Generated traffic by pinging the server from PC2.
4. Inspected the ARP request and reply packets.
5. Used 'arp -a' on PC2 to verify the resolved address.

## 5. Observations

**ARP Request**
- Source IP: 192.168.10.11
- Destination IP: 192.168.10.20
- Destination MAC: FFFF.FFFF.FFFF (broadcast)
- ARP opcode: 0x0001 (request)
- Target MAC: 0000.0000.0000

**ARP Reply**
- Source IP: 192.168.10.20
- Destination IP: 192.168.10.11
- Source MAC: 0060.70B4.A157
- Destination MAC: 0040.0B6D.2E7D

## 6. Result
PC2 successfully resolved the server's IPv4 address to its MAC address. The ARP request was broadcast across the local network, and the server responded with an ARP reply.

## 7. Key Learning
ARP helps devices communicate within a local network by discovering the MAC address associated with a known IPv4 address.
