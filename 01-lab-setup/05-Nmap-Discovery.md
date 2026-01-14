# Connection Verification
This section verifies that both virtual machines are connected to the same isolated network.\
Also both machines should be kept on simultaneously.
## Verification Steps

### 1. Check IP Address
- On both machines:\
`ip -4 addr show`

- Ensure both IPs are in the same subnet.

### 2. Nmap Discovery on Kali
- On Kali Linux Terminal Use this Command:\
`Sudo nmap -sn 192.168.56.10/24`\
(Your ip with subnet)

Screenshot: https://github.com/GorvBjaj/network-analysis-lab/blob/a25ee79837fb4ce145c7018e638c9af03c4375e7/screenshots/03-nmap-discovery.png

## Another method: ICMP protocol

### 3. Ping Test
- From Kali Linux:\
`ping 192.168.56.20`

- From Ubuntu:\
`ping 192.168.56.10`

### 4. Result
- Successful ICMP replies confirmed connectivity.
- Both machines could communicate only within the internal network.

Screenshot: https://github.com/GorvBjaj/network-analysis-lab/blob/baf6f671db0c20d8c3fbb6f7609d382cad7a6dea/screenshots/04-ICMP-test.png
