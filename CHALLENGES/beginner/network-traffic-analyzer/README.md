# Network Traffic Analyzer

**Difficulty:** Beginner  
**Time Estimate:** 8-12 hours  
**Languages:** Python, Go, C++  
**Topics:** Packet capture, protocol analysis, network monitoring, tcpdump/Wireshark

## Challenge Description

Build a network traffic analyzer that captures packets and displays protocol information (IP headers, TCP/UDP ports, DNS queries, HTTP requests). This is fundamental for network security analysis and troubleshooting.

## Learning Objectives

- [ ] Understand network protocols (IP, TCP, UDP, DNS, HTTP)
- [ ] Implement packet capture using system libraries
- [ ] Parse packet headers and extract information
- [ ] Filter packets by protocol or port
- [ ] Display traffic statistics
- [ ] Analyze network flows

## Requirements

### Functional Requirements
- Capture live network traffic
- Parse IP/TCP/UDP headers
- Extract DNS queries and responses
- Extract HTTP requests and responses
- Filter by protocol (TCP, UDP, DNS, HTTP)
- Filter by port or IP address
- Display traffic statistics
- Save capture to file (PCAP format)
- Read and analyze PCAP files

### Non-Functional Requirements
- Performance: Handle 1000+ packets/second
- Reliability: Don't drop packets
- Safety: Require elevated privileges appropriately

## Acceptance Criteria

- [ ] Captures network packets successfully
- [ ] Parses IP headers correctly
- [ ] Extracts TCP/UDP information
- [ ] Shows DNS queries and responses
- [ ] Displays HTTP request/response details
- [ ] Filtering works accurately
- [ ] Statistics are correct
- [ ] Can save/read PCAP files
- [ ] Code is well-documented

## Getting Started

### Option 1: Build from Scratch
1. Research packet capture libraries
2. Implement basic packet capture
3. Parse IP headers
4. Parse TCP/UDP headers
5. Extract application-layer data
6. Implement filtering
7. Add statistics
8. Implement PCAP I/O

### Option 2: Use Starter Code
```bash
cd starter_code
# Follow the README.md in starter_code/
```

### Option 3: Learn from Solution
```bash
cd solution
# Review reference implementations
```

## Libraries by Language

### Python
- **scapy:** Full-featured packet manipulation
- **dpkt:** Fast, lightweight packet parsing
- **pcapy:** Packet capture (wrapper around libpcap)

### Go
- **gopacket:** Comprehensive packet processing
- **raw-packet-capture:** Lower-level access

### C++
- **libpcap:** Standard packet capture library
- **libtins:** C++ wrapper around libpcap

## Protocol Headers (Simplified)

### IP Header
- Source/destination IP
- TTL (Time To Live)
- Protocol (TCP=6, UDP=17)

### TCP Header
- Source/destination port
- Sequence/acknowledgment numbers
- Flags (SYN, ACK, FIN, RST)

### UDP Header
- Source/destination port
- Length, checksum

### DNS (UDP port 53)
- Query/response
- Domain name, record type
- Answer section

## Tips & Hints

- **Privileges:** Packet capture requires root/administrator
- **Scapy trick:** Use `.show()` on packets for human-readable output
- **Filtering:** Implement both library-level and application-level filtering
- **Test traffic:** Use `curl`, `dig`, `ping` to generate test packets
- **Comparison:** Compare output with `tcpdump` or Wireshark
- **Storage:** PCAP format is standard; use libraries to read/write

## Testing Your Solution

```bash
# Capture traffic (requires sudo)
sudo python traffic_analyzer.py capture

# Capture for 30 seconds
sudo python traffic_analyzer.py capture --duration 30

# Filter by protocol
sudo python traffic_analyzer.py capture --protocol tcp

# Filter by port
sudo python traffic_analyzer.py capture --port 80

# Read PCAP file
python traffic_analyzer.py read -f capture.pcap

# Show statistics
python traffic_analyzer.py stats -f capture.pcap

# Compare with tcpdump
sudo tcpdump -w capture.pcap
python traffic_analyzer.py read -f capture.pcap
```

## Further Learning

- **Related challenge:** [Simple Port Scanner](../simple-port-scanner/)
- **Advanced:** Protocol dissection, flow analysis, anomaly detection
- **Real tools:** Study tcpdump, Wireshark, suricata
- **Security:** Intrusion detection, malware analysis

## Extensions

- [ ] Real-time protocol statistics
- [ ] Geolocation of IP addresses
- [ ] Malicious traffic detection
- [ ] Encrypted traffic identification (TLS)
- [ ] Web UI for traffic visualization

## Rubric

| Criteria | Points | Notes |
|----------|--------|-------|
| Packet Capture | 30% | Correctly captures packets |
| Parsing Accuracy | 30% | Headers parsed correctly |
| Filtering | 20% | Filters work as expected |
| Code Quality | 10% | Clean, readable code |
| Documentation | 10% | Good examples and explanations |

---

[Back to Challenge List](../../README.md)
