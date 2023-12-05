# NIC Teaming Procedure

Do not need to change ANYTHING inside of Security Onion.

Essentially, the throughput within the hardware and ESXi increases and delivers in the same way to Security Onion, the VMware ESXi Host.

## Steps: 

1. Power off the physical server, not the VMware ESXi Host

2. Install the additional Network Interface Card and connect to Switch via an additional Ethernet Port

    Will need to have Deep add the mirroring in Meraki

3. Power on the physical server

4. Cross your fingers that it can boot up

5. Go into VMware ESXi and Edit the Mon_Switch

6. Click Add Uplink and the new Physical NIC should be available

7. Go to Edit Settings then NIC Teaming settings

    1. Default for Load Balancing
        
    2. Default for Network Failover Detection

    3. Default for Notify Switches and Failback

8. Management Network might need to be restarted