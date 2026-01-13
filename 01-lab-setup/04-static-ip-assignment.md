# Static IP Assignment

This section documents how static IP addresses were manually configured using nmcli.

## Why Static IPs
- Necessary for targeting and packet analysis during attacks.

## Step-by-Step Configuration

### 1. Configure Static IP (Kali Linux - Attacker)

sudo nmcli con show\
sudo nmcli con mod "connection-name" ipv4.method manual ipv4.addresses 192.168.100.10/24\
sudo nmcli con up "connection-name"

Screenshot:- https://github.com/GorvBjaj/network-analysis-lab/blob/a382e25c176f5435b3ab67d2150cf40767eb896a/screenshots/kali-linux-static-ip-assignment.png


### 2. Configure Static IP (Ubuntu - Victim)

sudo nmcli con show\
sudo nmcli con mod "connection-name" ipv4.method manual ipv4.addresses 192.168.100.20/24\
sudo nmcli con up "connection-name"

Screenshot:- https://github.com/GorvBjaj/network-analysis-lab/blob/50418365964f7ca3880f1ad4e44e13c3cfeb9685/screenshots/02-ubuntu-static-ip-assignment.png



