# SOC Analyst Response – ARP Spoofing

This section outlines the actions taken from a SOC L1 perspective after detecting ARP spoofing activity.

## 1. Detection
- Identified abnormal ARP behavior through repeated gratuitous ARP packets.
- Observed duplicate IP–MAC mapping alerts in Wireshark.
- Noted unusually high frequency of ARP replies.

## 2. Validation
- Verified conflicting MAC addresses claiming the same IP.
- Confirmed unsolicited ARP replies without corresponding requests.
- Correlated observations with packet captures.

## 3. Classification
- Classified the activity as ARP spoofing / ARP cache poisoning.
- Assessed potential impact on local network communication.

## 4. Escalation
- Documented affected IP addresses and MAC addresses.
- Raised an incident ticket with packet evidence.
- Escalated to SOC L2 / Network team for mitigation and enforcement review.

## 5. Documentation
- Recorded timeline, indicators, and observed patterns.
- Attached PCAP files and screenshots as supporting evidence.
