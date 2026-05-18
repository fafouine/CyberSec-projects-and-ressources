# DNS Lookup CLI Tool

**Difficulty:** Beginner  
**Time Estimate:** 4-6 hours  
**Languages:** Python, Go, C++  
**Topics:** DNS protocol, network queries, WHOIS lookups, domain reconnaissance

## Challenge Description

Build a DNS lookup tool that queries DNS records for domain names and performs WHOIS lookups. This is essential for domain reconnaissance and network troubleshooting. Your tool should support multiple record types and provide comprehensive domain information.

## Learning Objectives

- [ ] Understand DNS protocol and record types (A, MX, CNAME, NS, TXT, SOA)
- [ ] Implement DNS queries using system libraries or DNS APIs
- [ ] Parse and display DNS responses
- [ ] Implement WHOIS lookups for domain information
- [ ] Handle DNS errors and timeouts gracefully

## Requirements

### Functional Requirements
- Query DNS records: A, AAAA, MX, CNAME, NS, TXT, SOA, SPF
- Resolve domain names to IP addresses
- Support reverse DNS lookups
- Perform WHOIS lookups (registrar, registration date, owner info)
- Accept domain as command-line argument
- Support multiple queries in one run
- Display results in organized format
- Handle both IPv4 and IPv6

### Non-Functional Requirements
- Performance: Resolve domain in <2 seconds
- Reliability: Handle invalid domains gracefully
- Timeout: Set reasonable timeouts for DNS queries

## Acceptance Criteria

- [ ] Performs A record lookup and returns IP address
- [ ] Queries MX records and returns mail servers
- [ ] Handles CNAME records correctly
- [ ] Returns NS records (nameservers)
- [ ] Retrieves WHOIS information (registrar, dates, registrant)
- [ ] Performs reverse DNS lookups (IP to domain)
- [ ] Times out gracefully on unresponsive DNS
- [ ] Clear error messages for invalid domains
- [ ] Well-documented code with examples

## Getting Started

### Option 1: Build from Scratch
1. Research DNS protocol basics
2. Choose DNS library for your language
3. Implement basic domain-to-IP lookup
4. Add support for other record types
5. Implement WHOIS lookups
6. Add reverse DNS
7. Format and display results

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

## DNS Record Types Reference

- **A**: IPv4 address
- **AAAA**: IPv6 address
- **CNAME**: Canonical name (alias)
- **MX**: Mail exchange servers
- **NS**: Nameservers
- **TXT**: Text records (SPF, DKIM, etc.)
- **SOA**: Start of authority
- **PTR**: Pointer record (reverse DNS)

## Tips & Hints

- **Library choices:**
  - Python: `dnspython`, `socket.gethostbyname()`
  - Go: `net.LookupHost()`, `net.LookupMX()`
  - C++: `getaddrinfo()`, or use external library
- **WHOIS:** Use system `whois` command or parse responses
- **Error handling:** Distinguish between "not found" and "lookup failed"
- **Common test domains:** google.com, github.com, example.com
- **Reverse DNS trick:** Try `nslookup` or `host` command to understand output

## Testing Your Solution

```bash
# Basic A record lookup
python dns_lookup.py google.com

# Query specific record type
python dns_lookup.py -t MX google.com

# WHOIS lookup
python dns_lookup.py -w google.com

# Reverse DNS
python dns_lookup.py -r 8.8.8.8

# Compare with system tools
dig google.com
nslookup google.com
whois google.com
```

## Further Learning

- **Related challenge:** [Simple Port Scanner](../simple-port-scanner/)
- **Advanced:** DNS poisoning, DNS tunneling
- **Security:** DNSSEC and DNS validation
- **Next challenge:** [Network Traffic Analyzer](../network-traffic-analyzer/)

## Extensions

- [ ] Cache DNS results
- [ ] Resolve all record types with single query
- [ ] Implement DNS over HTTPS (DoH)
- [ ] Detect DNS anomalies
- [ ] Build DNS zone transfer detector

## Rubric

| Criteria | Points | Notes |
|----------|--------|-------|
| Functionality | 40% | All record types work, WHOIS included |
| Accuracy | 20% | Correct DNS/WHOIS information |
| Error Handling | 20% | Graceful failures, clear messages |
| Code Quality | 10% | Clean, readable code |
| Documentation | 10% | Good examples and explanations |

---

[Back to Challenge List](../../README.md)
