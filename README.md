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
