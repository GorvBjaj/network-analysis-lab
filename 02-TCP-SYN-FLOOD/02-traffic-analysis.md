# Traffic Analysis – TCP SYN Flood

This section analyzes the network traffic captured during the TCP SYN flood attack.

## Capture Overview
- Traffic was captured on the Ubuntu machine using Wireshark.
- The capture focused on inbound TCP traffic from the attacker.

## Packet Pattern Observed
- A large number of TCP packets with the SYN flag set.
- Very few or no corresponding ACK packets.
- Repeated SYN packets from the same source IP.
- Multiple half-open TCP connections.

## Wireshark Indicators
- TCP flags: SYN = 1, ACK = 0
- Repeated source IP: 192.168.56.10
- High packet rate within a short time window
- Wireshark warnings such as retransmissions

## Screenshot for TCP SYN packets:
- This is how TCP SYN Flood attack looks like in Wireshark.
https://github.com/GorvBjaj/network-analysis-lab/blob/0cc9a2d11d1033ee630ef8f41cda129d440b5355/screenshots/06-TCP-SYN-packets.png


## Screenshot for TCP ACK packet 
- Only sent by ubuntu(192.168.56.20) to kali linux but attacker doesnt send any ACK packets back to complete the connection




## Normal vs Attack Behavior

Normal TCP:
- SYN → SYN-ACK → ACK (connection completes)

Attack Traffic:
- SYN → SYN → SYN (no ACK completion)

## Conclusion
The observed packet behavior confirms a TCP SYN flood attack, where the attacker attempts to exhaust server resources by creating incomplete TCP connections.

## SOC Perspective
From a SOC standpoint, this pattern is a strong indicator of a denial-of-service attempt based on abnormal SYN traffic volume and incomplete TCP handshakes.
