# Security Onion Configuration

## Version
- **Security Onion Version:** 2.4.20
- **Installation Type:** Standalone Installation

## Hardware
- **Operating System:** Oracle Linux 9 (64 bit)
- **Hard Drive:** 1.5 TB
- **CPUs:** 8
- **Memory:** 20 GB
- **Network Interface Cards:** 2
  - One for Management (Web UI)
  - One for Monitoring (traffic from the lab to be monitored)

![hardware](images/hardware.png)

## Networking

### Management Interface
- Used to access the Web UI and the console via VMware ESXi
- Assigns an IP address to the virtual machine and the ESXi interface

![man_switch](images/man_switch.png)

### Monitoring Interface
- Used to ingest all traffic that is mirrored by the physical switch
- Does not assign an IP address
- Operates in Promiscuous Mode to capture all the traffic it sees on the network

![mon_switch](images/mon_switch.png)

## Access

### Student Account
- Allows the user to perform analyses

### Admin Account
- Allows the user to make any necessary changes via the web interface

## Integrations
- **Threat Intelligence:** AbuseCH
  - More than 100 observables are imported an hour

## Physical Hardware Configurations
### Server

This is the server that is hosting security onion through a local instance of VMware ESXi.

![server](images/server.jpeg)

### Lab Switch

This directs the flow of traffic into and out of the network.

![switch](images/switch.jpeg)

### NIC Teaming Switch

Due to the lack of a NIC Teaming feature on the main switch, I had to use another switch the duplicate incoming traffic to two outgoing ethernet ports.

![nic_team_switch](images/nic_team_switch.jpeg)

### Network Adapters

Both network adapters are sending duplicate traffic to security onion. VMware ESXi is configured to treat these as one adapter through NIC Teaming to reduce throughput problems.

![adapters](images/adapters.jpeg)