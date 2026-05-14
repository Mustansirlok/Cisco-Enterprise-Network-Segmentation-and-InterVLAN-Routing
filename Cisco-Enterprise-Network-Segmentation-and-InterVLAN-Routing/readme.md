# Cisco Enterprise Network Segmentation and Inter-VLAN Routing

## Project Overview

This project demonstrates the implementation of an enterprise-style network infrastructure using Cisco Packet Tracer. The network was designed to support VLAN segmentation, inter-VLAN communication, centralized VLAN management, and Layer 2 redundancy prevention using Cisco switching technologies.

The lab simulates a real-world multi-switch environment commonly used in enterprise campuses and data centre access networks.

---

## Technologies and Concepts Used

- Cisco Packet Tracer
- VLAN Configuration
- Inter-VLAN Routing
- Router-on-a-Stick (ROAS)
- Rapid PVST (RPVST)
- VTP (VLAN Trunking Protocol)
- Trunk Links
- PortFast
- Spanning Tree Root Bridge Configuration
- Cisco IOS CLI

---

## Network Features

### VLAN Segmentation
Configured multiple VLANs to logically separate network traffic and improve network management and security.

### Trunk Configuration
Established trunk links between switches to allow VLAN traffic across the enterprise network.

### Rapid PVST (RPVST)
Enabled Rapid Per-VLAN Spanning Tree Protocol on all switches to prevent Layer 2 loops and improve convergence time.

### Root Bridge Election
Configured:
- SW1 as Primary Root Bridge
- SW2 as Secondary Root Bridge

This ensures optimal traffic flow and STP stability.

### VTP Configuration
Configured:
- S1 as VTP Server
- Remaining switches as VTP Clients

This allows centralized VLAN management across the switching infrastructure.

### Router-on-a-Stick
Implemented inter-VLAN routing using router subinterfaces with 802.1Q encapsulation.

This allows devices in different VLANs to communicate successfully.

### PortFast
Enabled PortFast on access ports connected to end devices to reduce startup delay.

---

## Verification and Testing

The following verifications were successfully completed:

- VLAN creation and assignment
- Trunk link verification
- STP root bridge verification
- VTP synchronization
- Inter-VLAN communication testing
- Successful end-to-end ping connectivity

---

## Verification Commands Used

```bash
show vlan brief
show interfaces trunk
show spanning-tree
show vtp status
show ip interface brief
show running-config
ping [destination-ip]
