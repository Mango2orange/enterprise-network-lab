# Enterprise Network Lab

## 📌 Overview

This project demonstrates a basic enterprise network setup including VLANs, inter-VLAN routing, DHCP, and ACL configuration.

## 🧰 Tools Used

* Cisco Packet Tracer / GNS3

## 🗺️ Network Topology

(Add your topology diagram image here)

## ⚙️ Configuration

### VLAN Configuration

```
vlan 10
name SALES
vlan 20
name IT
```

### Inter-VLAN Routing

```
interface g0/1.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
```

## 🔐 ACL Example

```
access-list 100 deny ip 192.168.10.0 0.0.0.255 any
access-list 100 permit ip any any
```

## 📊 Results

* Devices in different VLANs can communicate via router
* ACL successfully blocks restricted traffic

## 📚 Key Learnings

* VLAN segmentation improves security
* Routing enables communication between networks




enterprise-network-lab/
│── README.md
│── configs/
│    ├── router.txt
│    ├── switch.txt
│── diagrams/
│    ├── topology.png
│── screenshots/
│    ├── dhcp-working.png
│    ├── vlan-test.png
















## 🚀 Project Highlights
- Implemented VLAN segmentation for 3 departments
- Configured Router-on-a-Stick for inter-VLAN routing
- Enabled DHCP for automatic IP assignment
- Applied ACL for network security

## 🔍 Troubleshooting
- Fixed trunk misconfiguration issue
- Resolved DHCP pool mismatch
