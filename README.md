# Packet Sniffer - Task 1

A simple **Python Packet Sniffer** built using raw sockets on Linux.  
This program captures network packets at the Ethernet level and parses **IPv4**, **ICMP**, **TCP**, and **UDP** packets.


## Features

- Capture Ethernet frames
- Parse IPv4 packets
- Extract and display:
  - ICMP packet details
  - TCP segment details (ports, sequence, acknowledgement, flags)
  - UDP segment details
- Format multi-line packet data for readability


## Requirements

- Linux OS (AF_PACKET raw sockets are Linux-specific)
- Python 3
- Root privileges to capture packets (`sudo`)


## Usage

Run the sniffer:

```

sudo python3 task1.py

```

> Press `Ctrl + C` to stop the sniffer.


## Sample Output

Partial terminal output (first few packets):

```

Ethernet Frame:
- Destination: FF:FF:FF:FF:FF:FF, Source: 00:0C:29:3E:5B:1A, Protocol: 8
IPv4 Packet:
- Version: 4, Header Length: 20, TTL: 64
- Protocol: 6, Source: 192.168.1.2, Target: 192.168.1.1
TCP Segment:
- Source Port: 443, Destination Port: 53212, Sequence: 12345, Acknowledgement: 67890

```

> Full sample output can be saved in `sample_output.txt`.


## Notes

- The program runs in an **infinite loop** to continuously capture packets.  
- The sniffer **only works on Linux** because Windows does not support `AF_PACKET`.

---

## Author

**Sumayyah Siddique**
