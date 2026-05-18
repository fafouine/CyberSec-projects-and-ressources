# Hash Cracker

**Difficulty:** Beginner  
**Time Estimate:** 4-6 hours  
**Languages:** Python, C++, Go  
**Topics:** Hashing, cryptanalysis, dictionary attacks, brute-force

## Challenge Description

Build a hash cracker that can identify common password hashes using dictionary attacks and brute-force methods. This tool is essential for penetration testing and demonstrates hash vulnerabilities.

## Learning Objectives

- [ ] Understand different hash algorithms (MD5, SHA1, SHA256)
- [ ] Implement dictionary-based cracking
- [ ] Implement brute-force cracking
- [ ] Optimize performance for hash comparison
- [ ] Identify hash types
- [ ] Handle different hash encodings (hex, base64)

## Requirements

### Functional Requirements
- Crack MD5, SHA1, SHA256 hashes
- Dictionary attack using common password lists
- Brute-force attack (customizable character set)
- Detect hash type automatically
- Show crack time and success rate
- Support rainbow table lookups
- Optimize performance with multithreading
- Display statistics

### Non-Functional Requirements
- Performance: Compute 1M hashes/second
- Reliability: Handle large dictionaries (1M+ words)
- Memory: Efficient memory usage

## Acceptance Criteria

- [ ] Cracks MD5 hashes correctly
- [ ] Cracks SHA1 hashes correctly
- [ ] Cracks SHA256 hashes correctly
- [ ] Dictionary attack finds common passwords
- [ ] Brute-force works for small passwords
- [ ] Performance >100k hashes/second
- [ ] Automatically detects hash type
- [ ] Shows progress and statistics
- [ ] Well-documented code

## Getting Started

### Option 1: Build from Scratch
1. Implement hash functions (MD5, SHA1, SHA256)
2. Create hash comparison logic
3. Load dictionary file
4. Implement dictionary attack
5. Implement brute-force
6. Add hash type detection
7. Optimize with threading/multiprocessing
8. Add statistics and reporting

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

## Hash Type Detection

- **32 chars (hex):** MD5
- **40 chars (hex):** SHA1
- **64 chars (hex):** SHA256
- **Prefixes:** `$1$` (MD5), `$5$` (SHA256), `$6$` (SHA512)

## Dictionary Sources

- **rockyou.txt:** Popular leaked passwords (14M passwords)
- **Common passwords:** top100.txt, top1000.txt
- **Language dictionaries:** word lists for brute-force

## Performance Optimization

- **Multithreading:** Parallel hash computation
- **GPU acceleration:** Use GPU for hash computation
- **Caching:** Cache computed hashes
- **Early exit:** Stop on first match

## Tips & Hints

- **Hash libraries:** Use built-in or external crypto libraries
- **Progress indicator:** Show percentage/speed for long operations
- **Dictionary order:** Most common passwords first (rockyou sorted)
- **Rainbow tables:** Pre-computed hash tables for quick lookup
- **Salted hashes:** Many systems use salted hashes (harder to crack)
- **Test data:** Generate test hashes for verification

## Testing Your Solution

```bash
# Generate test hashes
python hash_cracker.py generate -p "password123" -a md5
# Output: 482c811da5d5b4bc6d497ffa98491e38

# Crack hash with dictionary
python hash_cracker.py crack -H "482c811da5d5b4bc6d497ffa98491e38" -d rockyou.txt

# Brute-force 4-digit PIN
python hash_cracker.py brute -H "482c811da5d5b4bc6d497ffa98491e38" -l 4 -c "0123456789"

# Batch crack multiple hashes
python hash_cracker.py batch -f hashes.txt -d rockyou.txt
```

## Further Learning

- **Related challenge:** [Caesar Cipher](../caesar-cipher/)
- **Advanced:** Rainbow tables, GPU cracking, salted hashes
- **Real tools:** Study hashcat, John the Ripper
- **Security:** Password hashing best practices (bcrypt, argon2)

## Extensions

- [ ] GPU-accelerated cracking
- [ ] Rainbow table generation/lookup
- [ ] Support for salted hashes
- [ ] Password strength estimation
- [ ] Distributed cracking

## Rubric

| Criteria | Points | Notes |
|----------|--------|-------|
| Hash Support | 30% | MD5, SHA1, SHA256 all work |
| Dictionary Attack | 30% | Successfully cracks common passwords |
| Performance | 20% | Fast hashing, handles large dictionaries |
| Code Quality | 10% | Clean, optimized code |
| Documentation | 10% | Good examples and performance notes |

---

[Back to Challenge List](../../README.md)
