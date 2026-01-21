# Traffic Analysis – ARP Spoofing

This section analyzes the ARP traffic captured during the spoofing attempt.

## Capture Overview
- Traffic was captured on the Ubuntu machine using Wireshark.
- Display filter used: `arp`

## Observed Indicators
- High volume of ARP Reply packets sent repeatedly.
- Unsolicited ARP replies (replies without matching requests).
- Same IP addresses advertised with conflicting MAC addresses.
- Wireshark warnings indicating “duplicate use of IP detected”.

## Key Evidence from Capture
- Multiple ARP replies claiming ownership of the same IPs.
- Frequent ARP announcements updating IP–MAC mappings.
- Broadcast ARP traffic consistent with cache poisoning behavior.

## Interpretation
- Conflicting IP–MAC mappings confirm ARP cache poisoning activity.
- Duplicate IP warnings indicate ARP inconsistency caused by spoofing.
- The traffic pattern matches known ARP spoofing signatures.

## SOC Perspective
- This behavior is a strong indicator of ARP spoofing or misconfiguration.
- Alerts are expected due to duplicate IP detection and gratuitous ARP bursts.
- The capture demonstrates successful generation and detection of malicious ARP behavior.

## Conclusion
The ARP traffic pattern and Wireshark warnings confirm an ARP spoofing attempt within the isolated lab environment.
