# Network Topology Generation and Configuration Project  

## 📌 Project Information
- **Author:** Amit Kumar  
- **Date:** 18/08/2025  
- **Internship:** CISCO Virtual Internship 2025  
- **Domain:** Networking Essentials  

---

## 📖 Introduction  
This project aims to develop a tool for automatically generating a **hierarchical network topology** from router configuration files.  
It addresses key areas such as:  
- Network performance  
- Load management  
- Configuration validation  
- Network simulation  

---

## 🎯 Objectives  
- Create a hierarchical network topology based on router configurations  
- Validate network configurations and identify potential issues  
- Simulate network activities and test connectivity 


## 🖧 Network Design  

### Components  
- **Routers:** R1, R2, R3  
- **Switches:** Switch1, Switch2  
- **End Devices:** PC1, PC2, PC3, PC4, Server  

### Topology Diagram  

<img width="1364" height="737" alt="network topology diagram" src="https://github.com/user-attachments/assets/36f27d48-6832-4019-a5f8-2c45ae348379" />

---

## ⚙️ Configuration Details  

### Router Configurations  
#### Router R1
```bash
 enable
 configure terminal
 hostname R1
 interface g0/0
 ip address 192.168.1.1 255.255.255.0
 no shutdown
 interface g0/1
 ip address 192.168.2.1 255.255.255.0
```

#### Router R2
```bash
 enable
 configure terminal
 hostname R2
 interface g0/0
 ip address 192.168.1.2 255.255.255.0
 no shutdown
 exit
```

#### Router R3
```bash
enable
configure terminal
hostname R3
interface g0/0
 ip address 192.168.2.1 255.255.255.0
 no shutdown
exit
```

---

### Switch Configurations
#### Switch S1
```bash
 enable
 configure terminal
 hostname Switch1
 interface vlan 1
 ip address 192.168.1.10 255.255.255.0
 no shutdown
 interface range fa0/1 - 2
 switchport mode access
 switchport access vlan 10
 interface range fa0/3 - 4
 switchport mode access
 switchport access vlan 20
 exit
```

#### switch S2
```bash
 enable
 configure terminal
 hostname Switch2
 interface vlan 1
 ip address 192.168.2.10 255.255.255.0
 no shutdown
 interface range fa0/1 - 2
 switchport mode access
 switchport access vlan 10
 interface range fa0/3 - 4
 switchport mode access
 switchport access vlan 20
 exit
```

---
## End Device Configurations

#### PC1:   
```bash
IP 192.168.1.20,   Subnet Mask 255.255.255.0,   Gateway 192.168.1.1
```

#### PC2:   
```bash
IP 192.168.1.21,   Subnet Mask 255.255.255.0,   Gateway 192.168.1.1
```

#### PC3:   
```bash
IP 192.168.2.20,   Subnet Mask 255.255.255.0,   Gateway 192.168.2.1
```

#### PC4:  
```bash
IP 192.168.2.21,   Subnet Mask 255.255.255.0,   Gateway 192.168.2.1
```

#### Server:   
```bash
IP 192.168.2.30,   Subnet Mask 255.255.255.0,   Gateway 192.168.2.1
```

---

## 🔍 Testing Connectivity

### Ping Tests

**From PC1 → PC2**
```bash
ping 192.168.1.21
```
**From PC3 → Server**
```bash
ping 192.168.2.30
```

### Traceroute Test

**From PC3 → Server**
```bash
tracert 192.168.2.30
```

---

## ✅ Conclusion

The project successfully demonstrates:

Generating a hierarchical network topology

Validating configurations

Testing connectivity among devices

The configurations align with the project requirements, ensuring a functional and reliable network environment.

---

## 🚀 Future Enhancements

Automating configuration file parsing

Adding visualization tools for topology generation

Integrating network monitoring features








