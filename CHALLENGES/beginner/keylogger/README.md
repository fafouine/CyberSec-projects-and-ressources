# Keylogger

**Difficulty:** Beginner  
**Time Estimate:** 4-5 hours  
**Languages:** Python, C++, Go  
**Topics:** System programming, input handling, event monitoring, logging

## Challenge Description

Build a keylogger that captures keyboard input and logs it with timestamps. This demonstrates event monitoring, system APIs, and security implications of input capture. **Note:** This is for educational purposes only - unauthorized keylogging is illegal.

## Learning Objectives

- [ ] Understand system-level input APIs and event handling
- [ ] Implement keyboard event capture on your OS
- [ ] Add timestamps to captured events
- [ ] Store logs securely with proper formatting
- [ ] Handle special keys (Shift, Enter, Backspace, etc.)

## Requirements

### Functional Requirements
- Capture all keyboard input in real-time
- Log each keystroke with precise timestamp
- Handle special keys separately (modifiers, function keys)
- Store logs to a file
- Start/stop logging with a hotkey (e.g., Ctrl+Shift+X)
- Display key name (not raw code) in logs

### Non-Functional Requirements
- Minimal performance impact on system
- Secure log storage (consider encryption)
- Graceful shutdown
- Cross-platform if possible (Windows, Linux, macOS)

## Acceptance Criteria

- [ ] Captures all keyboard input accurately
- [ ] Each log entry has timestamp in ISO 8601 format
- [ ] Special keys logged with descriptive names
- [ ] Logs written to file in structured format
- [ ] Hotkey toggles logging on/off
- [ ] No crashes on extended use
- [ ] Code includes usage warning/disclaimer

## Getting Started

### Option 1: Build from Scratch
1. Research keyboard event APIs for your OS
2. Implement basic input capture
3. Add timestamp recording
4. Implement file logging
5. Add hotkey support
6. Test extensively on your system

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

## Platform-Specific Approaches

### Python
- **pynput** library - Cross-platform, easiest approach
- **keyboard** library - Lower-level control
- **ctypes** + Windows API - System-level capture

### Go
- **robot-go** or **go-vgo/robotgo**
- **hook** library for global keyboard hooks

### C++
- Windows: SetWindowsHookEx() API
- Linux: X11 or Wayland event capture
- macOS: CGEvent monitoring

## Tips & Hints

- **Special keys:** Create a mapping for modifier keys (Shift, Ctrl, Alt)
- **Performance:** Use event-driven architecture, not polling loops
- **Logging format:** JSON or CSV for easy parsing
- **Testing:** Log to console first, then file
- **Hotkey trick:** Use a modifier + key combination that's unlikely to conflict
- **Disclaimer:** Always include a clear warning that this tool should only be used ethically

## Testing Your Solution

```bash
# Start logging
python keylogger.py

# Type some text, check log file
cat keylog.txt

# Expected format:
# 2026-05-18T14:23:45.123Z: 'a'
# 2026-05-18T14:23:45.156Z: 'b'
# 2026-05-18T14:23:45.234Z: 'shift' (pressed)
```

## Further Learning

- **Related challenge:** [System event monitoring concepts]
- **Security implications:** Input capture attacks, privacy concerns
- **Next challenge:** [Linux CIS Hardening Auditor](../linux-cis-hardening-auditor/)
- **Defense:** Learn how EDR tools detect malicious input capture

## Ethical Considerations

⚠️ **IMPORTANT:** This tool captures sensitive input including passwords. Use only on systems you own/have permission to monitor. Unauthorized keylogging is illegal and unethical.

## Rubric

| Criteria | Points | Notes |
|----------|--------|-------|
| Functionality | 40% | Accurate capture, all keys logged |
| Reliability | 20% | Works extended periods without issues |
| Code Quality | 20% | Clean, well-structured code |
| Logging Format | 10% | Clear, parseable output |
| Documentation | 10% | Includes ethical disclaimers |

---

[Back to Challenge List](../../README.md)
