# Caesar Cipher

**Difficulty:** Beginner  
**Time Estimate:** 2-4 hours  
**Languages:** Python, Go, C++, JavaScript  
**Topics:** Cryptography fundamentals, string manipulation, encryption/decryption

## Challenge Description

Implement a Caesar cipher - one of the oldest and simplest encryption methods. Build a CLI tool that can encrypt and decrypt text using a configurable shift value. This introduces cryptographic concepts and is a foundational exercise in security.

## Learning Objectives

- [ ] Understand basic substitution cipher mechanics
- [ ] Implement encryption and decryption algorithms
- [ ] Handle edge cases (non-alphabetic characters, case preservation)
- [ ] Create a user-friendly CLI interface
- [ ] Understand frequency analysis and cipher breaking

## Requirements

### Functional Requirements
- Encrypt text with a given shift (0-25)
- Decrypt text with a given shift
- Preserve case (A stays uppercase, a stays lowercase)
- Handle non-alphabetic characters (numbers, punctuation) unchanged
- Accept input from command-line arguments or file
- Output to stdout or file
- Brute-force decryption (try all 26 shifts)

### Non-Functional Requirements
- Performance: Handle files up to 1MB
- Usability: Clear command-line help
- Code quality: Well-documented, no magic numbers

## Acceptance Criteria

- [ ] Encrypts text correctly with specified shift
- [ ] Decrypts text correctly with specified shift
- [ ] Preserves case sensitivity
- [ ] Leaves non-alphabetic characters unchanged
- [ ] Accepts CLI arguments (mode, shift, input)
- [ ] Brute-force mode tries all 26 shifts
- [ ] Clear error messages for invalid input
- [ ] Code is well-documented

## Getting Started

### Option 1: Build from Scratch
1. Understand ASCII values for letters
2. Implement character shifting logic
3. Handle case preservation
4. Build encryption function
5. Build decryption function
6. Add CLI argument parsing
7. Implement brute-force mode

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

## Algorithm Explanation

**Caesar Cipher Formula:**
```
Encrypted = (Plaintext + Shift) mod 26
Decrypted = (Encrypted - Shift) mod 26
```

**Example:** Shift = 3 (ROT3)
```
A -> D
B -> E
Z -> C
```

## Tips & Hints

- **ASCII values:** A-Z: 65-90, a-z: 97-122
- **Modulo arithmetic:** Use mod 26 to wrap around the alphabet
- **Case handling:** Check if character is uppercase/lowercase before shifting
- **Non-letters:** Check character type before processing
- **Brute-force trick:** Print all 26 possibilities and let user find plaintext
- **Frequency analysis:** Teach how to break Caesar cipher with English letter frequencies

## Testing Your Solution

```bash
# Encrypt with shift 3
python cipher.py encrypt -s 3 -i "Hello, World!"
# Output: Khoor, Zruog!

# Decrypt with shift 3
python cipher.py decrypt -s 3 -i "Khoor, Zruog!"
# Output: Hello, World!

# Brute force (try all shifts)
python cipher.py bruteforce -i "Khoor, Zruog!"
# Output all 26 possibilities

# From file
python cipher.py encrypt -s 3 -f input.txt -o output.txt
```

## Further Learning

- **Cryptanalysis:** Learn frequency analysis to break Caesar cipher
- **Vigenère Cipher:** Next step - polyalphabetic substitution
- **Related challenge:** [Base64 Encoder/Decoder](../base64-encoder-decoder/)
- **Security note:** Caesar cipher provides NO real security - use modern crypto!

## Extensions

- [ ] Support Vigenère cipher (key-based shifts)
- [ ] Implement frequency analysis attack
- [ ] Add ROT13 mode (special case: shift 13)
- [ ] Support multiple languages
- [ ] GUI interface

## Rubric

| Criteria | Points | Notes |
|----------|--------|-------|
| Core Functionality | 40% | Encrypt/decrypt work correctly |
| Edge Cases | 20% | Handles case, non-letters, special chars |
| CLI Interface | 20% | Clear arguments, helpful output |
| Code Quality | 10% | Clean, readable, commented |
| Documentation | 10% | Good examples and explanations |

---

[Back to Challenge List](../../README.md)
