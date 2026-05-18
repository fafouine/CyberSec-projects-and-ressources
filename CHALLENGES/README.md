# Cybersecurity Challenges

Hands-on challenges organized by difficulty level. Each challenge removes progress tracking and presents clear requirements for learners to solve independently.

## 📋 Challenge Structure

Each challenge includes:
- **README.md** - Challenge description, objectives, and requirements
- **REQUIREMENTS.md** - Detailed acceptance criteria
- **starter_code/** - Optional skeleton/template (if applicable)
- **solution/** - Reference implementation
- **.gitignore** - Excludes progress files

## 🟢 Beginner Challenges (22 total)

### Network & Security Fundamentals
1. [Simple Port Scanner](./beginner/simple-port-scanner/) - TCP port scanning basics
2. [DNS Lookup CLI Tool](./beginner/dns-lookup/) - DNS queries and WHOIS lookups
3. [Network Traffic Analyzer](./beginner/network-traffic-analyzer/) - Packet capture and analysis
4. [Ghost on the Wire](./beginner/ghost-on-wire/) - L2 attacks: MAC spoofing & ARP detection

### Cryptography & Encoding
5. [Caesar Cipher](./beginner/caesar-cipher/) - Classical encryption/decryption
6. [Base64 Encoder/Decoder](./beginner/base64-encoder-decoder/) - Multi-format encoding
7. [Hash Cracker](./beginner/hash-cracker/) - Dictionary and brute-force attacks

### Data & Forensics
8. [Metadata Scrubber Tool](./beginner/metadata-scrubber-tool/) - Remove EXIF and metadata
9. [Steganography Multi-Tool](./beginner/steganography-multi-tool/) - Hide data in images, audio, QR, PDFs

### System Security
10. [Keylogger](./beginner/keylogger/) - Capture keyboard events with timestamps
11. [Linux CIS Hardening Auditor](./beginner/linux-cis-hardening-auditor/) - CIS benchmark compliance
12. [Systemd Persistence Scanner](./beginner/systemd-persistence-scanner/) - Hunt Linux persistence
13. [Linux eBPF Security Tracer](./beginner/linux-ebpf-security-tracer/) - Real-time syscall tracing
14. [Firewall Rule Engine](./beginner/firewall-rule-engine/) - Parse and validate iptables/nftables

### Vulnerability & Threat Detection
15. [Simple Vulnerability Scanner](./beginner/simple-vulnerability-scanner/) - CVE database checking
16. [Canary Token Generator](./beginner/canary-token-generator/) - Self-hosted honeytokens
17. [SSH Brute Force Detector](./beginner/ssh-brute-force-detector/) - Monitor and block SSH attacks
18. [DNS Sinkhole](./beginner/dns-sinkhole/) - Pi-hole-style malware domain blocker
19. [Security News Scraper](./beginner/security-news-scraper/) - Aggregate cybersecurity news

### Advanced Concepts
20. [Simple C2 Beacon](./beginner/simple-c2-beacon/) - Command and Control beacon/server
21. [Trojan Application Builder](./beginner/trojan-application-builder/) - Educational malware lifecycle
22. [Phishing Domain Generator & Quishing Scanner](./beginner/phishing-domain-generator-quishing-scanner/) - Typosquat + QR phishing detection
23. [LLM Prompt Injection Firewall](./beginner/llm-prompt-injection-firewall/) - Detect prompt injection attacks

---

## 🟡 Intermediate Challenges (25 total)

### Security Operations
1. [Secrets Scanner](./intermediate/secrets-scanner/) - Scan code and git history for secrets
2. [DLP Scanner](./intermediate/dlp-scanner/) - Data Loss Prevention for files, DBs, traffic
3. [Docker Security Audit](./intermediate/docker-security-audit/) - CIS Docker Benchmark scanner
4. [Subdomain Takeover Scanner](./intermediate/subdomain-takeover-scanner/) - Detect dangling DNS records

### Vulnerability Assessment
5. [API Security Scanner](./intermediate/api-security-scanner/) - Enterprise API vulnerability scanner
6. [Binary Analysis Tool](./intermediate/binary-analysis-tool/) - Disassemble and analyze executables
7. [SBOM Generator & Vulnerability Matcher](./intermediate/sbom-generator-vulnerability-matcher/) - Software Bill of Materials with CVE matching
8. [GraphQL Security Tester](./intermediate/graphql-security-tester/) - Automated GraphQL vulnerability testing

### Network & Traffic Analysis
9. [Wireless Deauth Detector](./intermediate/wireless-deauth-detector/) - Monitor WiFi deauth attacks
10. [JA3/JA4 TLS Fingerprinting Tool](./intermediate/ja3-ja4-tls-fingerprinting/) - Fingerprint TLS clients
11. [DDoS Mitigation Tool](./intermediate/ddos-mitigation-tool/) - Detect traffic spikes

### Threat Intelligence & Analysis
12. [Payload Obfuscation Engine](./intermediate/payload-obfuscation-engine/) - Multi-layer obfuscation
13. [Supply Chain Attack Simulator](./intermediate/supply-chain-attack-simulator/) - Fake PyPI dependency confusion
14. [SIEM Dashboard](./intermediate/siem-dashboard/) - Log aggregation with correlation
15. [Token Abuse Playground](./intermediate/token-abuse-playground/) - 15+ token vulnerabilities

### Post-Exploitation
16. [Credential Enumeration](./intermediate/credential-enumeration/) - Post-exploitation credential collection
17. [Lua/Nginx Edge Backend](./intermediate/lua-nginx-edge-backend/) - Full CRUD backend via Lua
18. [Mobile App Security Analyzer](./intermediate/mobile-app-security-analyzer/) - Decompile and analyze apps

### Exploitation & Defense
19. [Race Condition Exploiter](./intermediate/race-condition-exploiter/) - TOCTOU attack & defense lab
20. [Credential Rotation Enforcer](./intermediate/credential-rotation-enforcer/) - Track credential rotation
21. [Chaos Engineering Security Tool](./intermediate/chaos-engineering-security-tool/) - Inject security failures
22. [Self-Hosted Shodan Clone](./intermediate/self-hosted-shodan-clone/) - Device search engine
23. [Privesc Playground](./intermediate/privesc-playground/) - 20+ privilege escalation paths

---

## 🔴 Advanced Challenges (25+ total)

### Offensive Security
1. [Exploit Development Framework](./advanced/exploit-development-framework/) - Modular exploitation framework
2. [Automated Penetration Testing](./advanced/automated-penetration-testing/) - Full pentest automation
3. [Advanced Persistent Threat Simulator](./advanced/advanced-persistent-threat-simulator/) - Multi-stage APT simulation
4. [Distributed Password Cracker](./advanced/distributed-password-cracker/) - GPU-accelerated cracking
5. [Network Covert Channel](./advanced/network-covert-channel/) - Data exfiltration techniques

### Defensive & Detection
6. [AI Threat Detection](./advanced/ai-threat-detection/) - ML-powered threat detection
7. [Malware Analysis Platform](./advanced/malware-analysis-platform/) - Automated sandbox analysis
8. [Kernel Rootkit Detection](./advanced/kernel-rootkit-detection/) - Detect kernel-level rootkits
9. [Zero Day Vulnerability Scanner](./advanced/zero-day-vulnerability-scanner/) - Coverage-guided fuzzing

### Architecture & Compliance
10. [Cloud Security Compliance Dashboard](./advanced/cloud-security-compliance-dashboard/) - Multi-cloud compliance
11. [Supply Chain Security Analyzer](./advanced/supply-chain-security-analyzer/) - Dependency vulnerability analysis
12. [Bug Bounty Platform](./advanced/bug-bounty-platform/) - Vulnerability disclosure platform

### Specialized Security
13. [Blockchain Smart Contract Auditor](./advanced/blockchain-smart-contract-auditor/) - Solidity vulnerability analysis
14. [Quantum Resistant Encryption](./advanced/quantum-resistant-encryption/) - Post-quantum cryptography
15. [Hardware Security Module Emulator](./advanced/hardware-security-module-emulator/) - Software HSM with PKCS#11
16. [Adversarial ML Attacker](./advanced/adversarial-ml-attacker/) - Generate adversarial examples

### Infrastructure & Monitoring
17. [API Rate Limiter](./advanced/api-rate-limiter/) - Distributed rate limiting middleware
18. [Encrypted Chat Application](./advanced/encrypted-p2p-chat/) - Real-time E2EE messaging
19. [Monitor the Situation Dashboard](./advanced/monitor-the-situation-dashboard/) - Cyber threat situational awareness
20. [Honeypot Network](./advanced/honeypot-network/) - Multi-service honeypot deployment
21. [Haskell Reverse Proxy](./advanced/haskell-reverse-proxy/) - Functional reverse proxy with middleware

---

## 🚀 Getting Started

1. **Choose a difficulty level** - Start with Beginner if you're new
2. **Pick a challenge** - Pick something that interests you
3. **Read the README** - Understand requirements and learning objectives
4. **Build your solution** - Code from scratch or use starter code
5. **Check the solution** - Compare with reference implementation
6. **Share your work** - Create a PR or share your approach

## 📚 Challenge Template

See [CHALLENGE_TEMPLATE.md](./CHALLENGE_TEMPLATE.md) to:
- Understand the challenge structure
- Create new challenges
- Follow naming conventions
- Use proper difficulty guidelines

## 💡 Tips

- **Start small** - Beginner challenges build foundational skills
- **Build progressively** - Intermediate builds on beginner concepts
- **Don't skip ahead** - Advanced requires significant experience
- **Read code carefully** - Solutions teach best practices and security patterns
- **Experiment** - Modify solutions, add features, break things safely

---

[Back to Main README](../README.md)
