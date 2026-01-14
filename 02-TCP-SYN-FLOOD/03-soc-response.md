# SOC Analyst Response – TCP SYN Flood

This section outlines the actions taken from a SOC L1 perspective upon detecting a TCP SYN flood.\
After recieving an Alert for TCP-SYN-FLOODF attack these steps must be undertaken.

## 1. Validation
- Reviewed PCAP data to confirm abnormal TCP SYN traffic.
- Verified high SYN rate with missing ACK responses.

## 2. Classification
- Identified the activity as a TCP SYN flood attack.
- Assessed the number of affected hosts and impact scope.

## 3. Escalation
- Documented source IP address and target system.
- Raised an incident ticket with supporting evidence.
- Escalated the case to SOC L2 / Network team for mitigation.

## 4. Documentation
- Recorded timeline, indicators, and packet evidence.
- Attached PCAP files and screenshots for reference.
