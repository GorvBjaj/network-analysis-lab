# Traffic Analysis – ARP Spoofing

This section documents the ARP traffic observed during the spoofing activity and how it was detected.

## Capture Overview
- Traffic captured on Ubuntu using Wireshark
- Display filter used: `arp`

## Repeated Observations
- Continuous ARP Reply packets at short intervals
- Unsolicited ARP replies (no preceding ARP requests)

## ARP Announcements (Gratuitous ARP)
- Frequent ARP announcements were observed meaning that particular ip device shouting thats me not him.
- These packets repeatedly broadcast IP–MAC mappings
- Used to overwrite or defend ARP cache entries

## Detection Indicators
- Wireshark warnings indicating “duplicate use of IP detected”
- Multiple MAC addresses claiming the same IP
- Abnormal volume of ARP replies compared to normal behavior

## Interpretation
- The packet patterns confirm ARP cache poisoning behavior
- Duplicate IP warnings indicate ARP inconsistency caused by spoofing
- Repeated ARP traffic is required to keep the poisoning active due to ARP cache expiration

## Related ARP Spoofing Scenario (Weak Networks)
- In networks without DHCP Snooping or DAI, an attacker may claim an unused IP address
- Such claims rely on unauthenticated ARP announcements
- This represents another ARP spoofing risk, separate from MITM attacks

Screenshot: 

## Conclusion
The observed ARP announcements, repeated poisoning attempts, and duplicate IP detections confirm ARP spoofing activity within the isolated lab.
