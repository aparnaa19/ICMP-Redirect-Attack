# ICMP Redirect Attack & MITM Lab 

This project demonstrates an ICMP Redirect Attack where the attacker convinces a victim to change its routing table, redirecting traffic through a malicious router. It also performs a man-in-the-middle (MITM) attack by altering TCP payloads using Scapy.

## 🔍 Objective
- Understand how ICMP Redirect messages manipulate routing behavior
- Use Docker-based containers to simulate a routed network
- Launch ICMP redirect attacks to reroute victim traffic
- Perform MITM attacks on redirected traffic
- Modify TCP packets in transit using Python and Scapy

## 🧰 Tools Used
- Docker (SEED Ubuntu 20.04 VM)
- Scapy (Python)
- Netcat (TCP testing)
- Traceroute and IP routing tools
- Wireshark (optional for packet verification)

## 📌 Key Attack Scenarios
- **ICMP Redirect Spoofing:** Sent forged ICMP messages to route traffic through malicious router
- **Routing Table Manipulation:** Used `ip route` and `traceroute` to verify rerouting
- **MITM TCP Interception:** Intercepted and modified TCP messages (e.g., replaced "APARNA" with "AAAAAA")
- **Packet Filtering:** Used MAC address filtering for targeted packet manipulation

## 🛡️ Key Observations
- Traceroute showed victim traffic rerouted through attacker
- Modified TCP payloads confirmed via netcat session
- System configurations like `send_redirects` and `ip_forwarding` influenced success



## 🔗 References
- [SEED Labs - ICMP Redirect Attack](https://seedsecuritylabs.org/Labs_20.04/Networking/ICMP_Redirect/)
- [Scapy Documentation](https://scapy.readthedocs.io/)
