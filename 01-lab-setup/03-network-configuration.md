# Network Configuration

This section documents how the virtual machines were isolated into a private network.

## Step-by-Step Configuration

1. Powered off both virtual machines.
2. Open settings -> expert -> network.
3. Disconnected the NAT network adapter.
4. Selected "Internal Network" as the network adapter type.
5. Assigned both VMs to the same internal network name.
6. Started both virtual machines.

## Purpose
- Ensure complete isolation from the host and internet.
- Allow communication only between Kali Linux and Ubuntu.
- External network access was fully restricted.
