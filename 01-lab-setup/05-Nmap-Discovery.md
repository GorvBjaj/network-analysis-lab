# Connection Verification
This section verifies that both virtual machines are connected to the same isolated network.
Also both machines should on simultaneously.
## Verification Steps

### 1. Check IP Address
On both machines:
ip -4 addr show

Ensure both IPs are in the same subnet.

### 2. Nmap Discovery on Kali

### 2. Ping Test
From Kali Linux:
ping 192.168.100.10

css
Copy code

From Ubuntu:
ping 192.168.100.20

markdown
Copy code

### 3. Result
- Successful ICMP replies confirmed connectivity.
- Both machines could communicate only within the internal network.

## Evidence
Screenshots and terminal outputs were captured for verification.
