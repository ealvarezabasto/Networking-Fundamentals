# OSI Model

## Layer 1 - Physical Network (Ethernet Cable)
**Description:** Simplifies Networking concepts

## Layer 2 - Data Link (LAN

### NIC (Network Interface Card)
* Hardware component that enables a computer or device to connect to a network and communicate with other devices over that network, typically using Ethernet, Wi-Fi, or other network technologies
* NIC has a MAC Address hardcoded to it

### MAC Address
* Every NIC has a unique MAC address that is hard coded by the hardware vendor
* Computers in a local area network (LAN) communicate using MAC addresses.
* By typing ***ipconfig/all*** (Windows) or ***ifconfig*** (Linux/MAC) in the command line, user finds **Physical Address** that is the MAC Address.

  ![image](https://github.com/user-attachments/assets/a778cd82-bb53-47c8-8d92-46929d0e6d71)

### Ethernet Frame: Sent from one Computer to another Computer through internet network
1) Payload: data (e.g., data being sent from one location to another, document being shared)
2) Destination MAC (machine here frame is going to)
3) Source MAC Address (machine where frame is coming from)

### Physical Ethernet Switch
* Device that connects multiple devices within a local area network (LAN)
* intelligently directs data only to the specific device that needs it, based on MAC address
* Contains the MAC Tables that lists MAC Address and respective Port. Can have multiple MAC addresses for one Port. (e.g., MAC Address XX.XX.XX is associated with Port 1)

  <img width="422" alt="image" src="https://github.com/user-attachments/assets/25a19a68-bdae-4423-9a01-1d70f3b923f2" />

  ***screenshot from Introduction to Computer Networking Udemy Video***

### Types of Traffic in an Ethernet Network
#### Broadcast
* It typically occurs in Ethernet networks when the sender needs to learn the MAC address of the destination device by broadcasting an ARP (Address Resolution Protocol) request to the entire network, and once learned, future communication becomes unicast with the specific MAC address. 
* ARP (Address Resolution Protocol) Request: which IPs are associated with which MAC address
* To discover the MAC associated with an IP Address
* By typing ***arp -a*** (Windows) in the command line, user finds **ARP Table** for their computer. ARP Table: IP Address (Internet Address) and MAC Address (Physical Address) associated which each IP Address

#### Unknown Unicast:
* A destination MAC address is not recognized by the switch and is therefore sent out to all ports in the same VLAN except the source port, in order to discover the correct destination. 

**EXAMPLE:**
* Computer 1 (MAC 1) wants to connect with Computer 3 (MAC 3) so it sends data to its Switch 1.
* Switch 1 does not contain MAC 3 as part of it's MAC Table so it doesn't know which port MAC 3 is assocaited with.
* Switch 1 will flood a ping to all switches and ports around it to know where is the MAC 3 address that Computer 1 is looking for. It could be that MAC 3 is part of Switc 2 MAC Table.
* Once the MAC address is found, Switch 1 will update the MAC Table.

#### Multicast:
* Allows a single sender to transmit data to a select group of receivers.
* It uses a special Ethernet MAC address to identify the multicast group, and only devices belonging to that group process the data, reducing network traffic and conserving bandwidth. Multicast is commonly used for applications like video streaming or distributing data to multiple recipients efficiently.
**EXAMPLE:**
* Computer 1 needs to send data to Computer 2 (MAC 2) and Computer 4 (MAC 4), but not to Computer 3 (MAC 3).
* Multicast will forward data / traffic to Computer 2 / 4 but not to Computer 3.

## Layer 3 - Network (IP Addressing Information)

### Router
* Computer sends data to Router (Default Gateway). That Router is connected to a LAN

### IP Address
* No two computers in the same network have the same IP address. Unique IP Address per machine.

### Packet: Used to transmit information across a network
1) Payload: data (e.g., actual data being transmitted, video that I want to upload to YouTube)
2) Destination IP address
3) Source IP Address

## Layer 4 - Transport
* TCP (FTP, HTTP) / UDP Port (DNS, NTP)
* TCP Layer Protocol that is used by Port 80 (HTTP)

## Layer 5 - Session

## Layer 6 - Presentation

## Layer 7 - Application
* Examples: Email App, YouTube App
* * TCP (FTP, HTTP) / UDP Port (DNS, NTP)



