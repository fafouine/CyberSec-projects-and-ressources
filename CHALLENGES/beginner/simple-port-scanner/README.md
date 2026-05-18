# Simple Port Scanner

**Difficulty:** Beginner  
**Time Estimate:** 4-5 hours  
**Languages:** Python, C++, Go  
**Topics:** Network scanning, TCP/IP, asynchronous programming, socket programming

## Challenge Description

Build a TCP port scanner that can identify open, closed, and filtered ports on a target host. This is a fundamental tool in network reconnaissance and security testing. Your implementation should handle multiple ports efficiently using asynchronous operations.

## Learning Objectives

- [ ] Understand TCP/IP socket programming fundamentals
- [ ] Implement port scanning with timeout handling
- [ ] Use asynchronous operations to scan multiple ports efficiently
- [ ] Parse command-line arguments for target host and port ranges
- [ ] Interpret and display scan results clearly

## Requirements

### Functional Requirements
- Accept a target hostname/IP as input
- Accept a port range (start:end) or specific ports
- Attempt connection to each port with a configurable timeout (default 1 second)
- Classify ports as: OPEN, CLOSED, or FILTERED
- Display results in a clear, organized format
- Handle both IPv4 and IPv6 addresses
- Support scanning common ports (top 100, 1000, etc.)

### Non-Functional Requirements
- Performance: Scan 1000 ports in under 30 seconds
- Reliability: Handle network errors gracefully
- Security: Sanitize input, handle timeouts
- User Experience: Clear progress indication for large scans

## Acceptance Criteria

- [ ] Scanner accepts command-line arguments for host and port range
- [ ] Successfully identifies open ports on localhost
- [ ] Correctly reports closed/filtered ports
- [ ] Completes 1000-port scan in reasonable time (<60s)
- [ ] Handles invalid hosts/ports without crashing
- [ ] Results are sortable and clearly formatted
- [ ] Code is well-documented and follows best practices

## Getting Started

### Option 1: Build from Scratch
1. Research socket programming in your chosen language
2. Create a basic connection attempt function
3. Implement port iteration logic
4. Add timeout and error handling
5. Implement asynchronous/threaded scanning
6. Format and display results

### Option 2: Use Starter Code
```bash
cd starter_code
# Follow the README.md in starter_code/
```

### Option 3: Learn from Solution
```bash
cd solution
# Review the reference implementations
```

## Tips & Hints

- **Sockets 101:** A connection to a port succeeds if it's OPEN, times out if FILTERED, or refused if CLOSED
- **Performance:** Use threading (Python) or async (Go/Rust) to scan multiple ports simultaneously
- **Common ports:** 80 (HTTP), 443 (HTTPS), 22 (SSH), 3306 (MySQL), 5432 (PostgreSQL)
- **Tool comparison:** Compare your results with `nmap` or `netcat` (nc)
- **Pitfall:** Don't forget to close sockets or handle exceptions properly

## Testing Your Solution

```bash
# Scan localhost for common ports
python port_scanner.py localhost 1-1000

# Scan specific host
python port_scanner.py 192.168.1.1 80,443,22

# Compare with nmap (if installed)
nmap -p 1-1000 localhost
```

## Further Learning

- **Related challenge:** [Network Traffic Analyzer](../network-traffic-analyzer/)
- **Security concept:** Port scanning for reconnaissance
- **Next challenge:** [DNS Lookup CLI Tool](../dns-lookup/)
- **Tool:** Study `nmap` source code for advanced techniques

## Rubric

| Criteria | Points | Notes |
|----------|--------|-------|
| Functionality | 40% | All requirements met, handles edge cases |
| Performance | 20% | Efficient scanning with async/threads |
| Code Quality | 20% | Clean, readable, well-documented |
| User Experience | 10% | Clear output, helpful messages |
| Documentation | 10% | Comments explain complex logic |

---

[Back to Challenge List](../../README.md)
