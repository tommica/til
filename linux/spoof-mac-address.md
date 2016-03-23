# Spoof MAC address

Local to remote

```bash
# Get your IP
ifconfig

# Ping the network
ping x.x.x.255

# Find the MAC address
arp -a

# Change MAC address
sudo ifonfig en1 lladdr ma:cg:oe:sh:er:e0

# Disconnect and reconnect
```
