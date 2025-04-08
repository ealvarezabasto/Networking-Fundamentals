# OSI Model

## Layer 2

### NIC (Network Interface Card)
* Hardware component that enables a computer or device to connect to a network and communicate with other devices over that network, typically using Ethernet, Wi-Fi, or other network technologies

### MAC Address
* Every NIC has a unique MAC address that is hard coded by the hardware vendor
* By typing ***ipconfig/all*** (Windows) or ***ifconfig*** (Linux/MAC) in the command line, user finds **Physical Address** that is the MAC Address.

  ![image](https://github.com/user-attachments/assets/a778cd82-bb53-47c8-8d92-46929d0e6d71)

### Ethernet Frame: Sent from one Computer to another Computer through internet network
1) Payload: data (e.g., data being sent from one location to another, document being shared)
2) Destination MAC (machine here frame is going to)
3) Source MAC Address (machine where frame is coming from)

### Switch
* Device that connects multiple devices within a local area network (LAN)
* intelligently directs data only to the specific device that needs it, based on MAC address
* Have MAC Tables

## Layer 3

### Packet: Used to transmit informaiton across a network
1) Payload: data (e.g., actual data being transmitted)
2) Destination IP address
3) Source IP Address
