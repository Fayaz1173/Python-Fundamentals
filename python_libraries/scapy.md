# Scapy

## 1. What is Scapy?

**Scapy** allows you to:

- Manually build packets (IP, TCP, UDP, ICMP, etc.)
- Send packets to targets
- Capture packets from the network
- Inspect and manipulate packet contents

It is commonly used for:

- Network testing
- Security research
- Packet crafting
- Debugging protocols

1. Creating a Simple ICMP (Ping) Packet

```python
from scapy.all import *

# Create an ICMP packet
packet = IP(dst="8.8.8.8") / ICMP()

# Show packet details
packet.show()

# Send packet and receive response
response = sr1(packet)

if response:
    response.show()
```

1. Sniff Network Traffic

```python
from scapy.all import *

def packet_callback(packet):
    print(packet.summary())

sniff(count=10, prn=packet_callback)
```
