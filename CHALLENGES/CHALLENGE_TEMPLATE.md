# Challenge Template

Use this template when creating new challenges for the repository.

## Directory Structure

```
CHALLENGES/[difficulty]/[challenge-name]/
├── README.md                 # Challenge description
├── REQUIREMENTS.md          # Detailed requirements & acceptance criteria
├── starter_code/            # Optional: starter template/skeleton
│   └── [language files]
├── solution/                # Reference solution (optional)
│   └── [language files]
└── .gitignore              # Ignore solution files & progress
```

## README.md Template

```markdown
# [Challenge Name]

**Difficulty:** [Beginner/Intermediate/Advanced]  
**Time Estimate:** [X-Y hours/days]  
**Languages:** [Python, Go, C++, etc.]  
**Topics:** [Security concept 1], [Security concept 2]

## Challenge Description

Brief, engaging description of what the learner will build.

## Learning Objectives

- [ ] Objective 1
- [ ] Objective 2
- [ ] Objective 3

## Requirements

### Functional Requirements
- Must do X
- Must implement Y
- Must handle Z

### Non-Functional Requirements
- Performance: [if applicable]
- Security: [if applicable]
- Code quality: [if applicable]

## Acceptance Criteria

- [ ] All functional requirements met
- [ ] Code is well-documented
- [ ] Solution follows best practices
- [ ] [Specific test case 1]
- [ ] [Specific test case 2]

## Getting Started

### Option 1: Build from Scratch
Start from scratch using the concepts outlined above.

### Option 2: Use Starter Code
```bash
cd starter_code
# Follow instructions in starter_code/README.md
```

### Option 3: Learn from Solution
```bash
cd solution
# Review the reference implementation
```

## Tips & Hints

- Hint 1
- Hint 2
- Common pitfalls to avoid

## Testing Your Solution

```bash
# Example test commands
python test.py
./test.sh
```

## Further Learning

- Related project: [Link]
- Useful resource: [Link]
- Next challenge: [Link]

## Rubric

| Criteria | Points | Notes |
|----------|--------|-------|
| Functionality | 40% | All requirements met |
| Code Quality | 30% | Clean, documented, efficient |
| Security | 20% | Handles edge cases, secure practices |
| Documentation | 10% | Clear comments and README |

---

[Back to Challenge List](../../README.md)
```

## File Structure Best Practices

```
CHALLENGES/
├── README.md                          # Main challenges index
├── CHALLENGE_TEMPLATE.md              # This file
├── beginner/
│   ├── port-scanner/
│   │   ├── README.md
│   │   ├── REQUIREMENTS.md
│   │   ├── starter_code/
│   │   │   ├── README.md
│   │   │   └── main.py
│   │   ├── solution/
│   │   │   ├── README.md
│   │   │   └── main.py
│   │   └── .gitignore
│   └── [more beginner challenges]/
├── intermediate/
│   └── [intermediate challenges]/
└── advanced/
    └── [advanced challenges]/
```

## Creating a New Challenge

1. **Create the directory structure:**
   ```bash
   mkdir -p CHALLENGES/[difficulty]/[challenge-name]/{starter_code,solution}
   ```

2. **Copy and customize this template:**
   ```bash
   cp CHALLENGE_TEMPLATE.md CHALLENGES/[difficulty]/[challenge-name]/README.md
   ```

3. **Fill in all sections** with specific challenge details

4. **Create starter code** (optional but recommended)
   - Remove solutions/answers
   - Include helpful comments and structure
   - Add a README.md with setup instructions

5. **Create solution** (optional reference implementation)
   - Well-documented code
   - Best practices and secure patterns
   - Comments explaining security concepts

6. **Create .gitignore:**
   ```
   # Compiled files
   *.pyc
   *.pyo
   __pycache__/
   *.o
   *.a
   *.so
   
   # IDE
   .vscode/
   .idea/
   *.swp
   
   # Testing
   .coverage
   htmlcov/
   
   # Solution (optional - remove this if you want to track solutions)
   # solution/
   ```

7. **Update main README** with link to new challenge

## Naming Conventions

- **Folder names:** Use kebab-case (e.g., `port-scanner`, `api-security-scanner`)
- **Files:** Use snake_case for Python (e.g., `port_scanner.py`)
- **Commits:** "Add challenge: [Challenge Name]"

## Content Guidelines

### Challenge Description
- Start with the "why" - what real-world problem does this solve?
- Make it engaging and relevant
- Keep it 2-3 sentences max

### Learning Objectives
- 3-5 clear, measurable objectives
- Use action verbs (implement, analyze, detect, etc.)
- Should be achievable within the time estimate

### Requirements
- Be specific and testable
- Cover both happy path and edge cases
- Include any security considerations

### Tips & Hints
- Suggest tools or libraries
- Point out common mistakes
- Give subtle guidance without spoiling

## Difficulty Levels

### Beginner
- Time: 2-6 hours
- Concepts: Single security topic
- Skills: Basic programming, 1-2 libraries
- Example: Port scanner, Caesar cipher

### Intermediate
- Time: 1-5 days
- Concepts: Multiple security topics combined
- Skills: Intermediate programming, multiple libraries, design patterns
- Example: SIEM dashboard, API security scanner

### Advanced
- Time: 1-4 weeks
- Concepts: Complex security architecture
- Skills: Advanced programming, system design, performance optimization
- Example: Exploit framework, APT simulator

---

**Created:** 2026-05-18  
**Last Updated:** 2026-05-18
