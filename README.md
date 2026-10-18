# Connecting a Wired and Wireless LAN

**Cisco Packet Tracer | Networking Fundamentals (IT 341)**

## Overview

Completed a Cisco Packet Tracer lab connecting a wired and wireless local area network (LAN). The activity focused on selecting the appropriate physical media, linking routers, switches, a server, a cable modem, a wireless router, and end-user PCs, and verifying that devices could communicate across the network.

## Network Topology

![Completed Packet Tracer network topology](images/topology.png)

The completed topology includes a primary routed network, a network reached through a switch, and a home network with wired and wireless devices.

## Skills Practiced

- Connected networking devices with copper straight-through, copper crossover, coaxial, serial DCE, console, and multimode fiber-optic cables.
- Identified device ports and considered transmit/receive wiring and Auto-MDIX behavior when choosing Ethernet cables.
- Used a console connection to inspect a router through Cisco IOS.
- Tested IP connectivity with `ping` and verified HTTP access with a web browser.
- Compared logical and physical views of a network in Cisco Packet Tracer.

## Connectivity Verification

### Server connectivity

From the Family PC, I pinged the server at `10.0.0.254`. The ping succeeded with **0% packet loss**.

![Successful server ping](images/ping-server.png)

### Website access

I opened `http://netacad.pka` in the Packet Tracer web browser and confirmed the page loaded.

![Website accessed through Packet Tracer browser](images/web-access.png)

### Switch connectivity

From the Home PC, I tested connectivity to the switch at `172.16.0.2`. The first attempt received two of four replies; the second attempt received **four of four replies**.

![Switch ping results](images/ping-switch.png)

### Router interface status

Using the Configuration Terminal, I inspected Router0 with the Cisco IOS command:

```text
show ip interface brief
```

![Router interface status in Cisco IOS](images/router-interfaces.png)

## Lessons Learned

- **Straight-through vs. crossover:** The correct Ethernet cable depends on the interface transmit/receive wiring and whether Auto-MDIX is supported. This activity included a connection that required a crossover cable when Auto-MDIX was unavailable.
- **Console cables:** A console connection provides local device-management access; it is not an ordinary Ethernet network connection.
- **Fiber-optic cabling:** Multimode fiber can be used for shorter-distance network connections. Duplex fiber links commonly use separate transmit (TX) and receive (RX) strands.
- **Logical vs. physical topology:** Packet Tracer's logical view shows network connections; the physical view shows how equipment is arranged in racks and rooms.
- **Home vs. larger networks:** A home network generally has fewer devices and does not require the same rack infrastructure used in many network rooms.

## Tools

- Cisco Packet Tracer
- Cisco IOS command-line interface
- ICMP `ping`
- Packet Tracer web browser

---

*This README documents my hands-on work and observations from a networking lab. The original course activity and assignment materials are not included.*
