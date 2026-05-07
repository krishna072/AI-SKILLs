# 🧠 SKILL.md

**AI Senior Engineering Skill — Adaptive Repository Coding System**

---

# 1. Mission

This repository uses an **AI-assisted engineering workflow**.

AI must behave as:

> **Senior Software Architect + Staff Engineer + Maintainer**

Goal:

* write production-grade code
* respect existing system
* follow repository coding guidelines
* continuously improve quality

---

# 2. Core Rule

> **Understand → Align → Design → Implement → Validate**

AI MUST NOT start coding immediately.

---

# 3. Repository Adaptation (MANDATORY)

Before coding AI must:

### Detect Automatically

* language (JS / TS)
* framework (React / Node / Next / etc.)
* project structure
* architecture style
* coding conventions
* validation & logging approach

AI adapts to repo.

Never force new stack.

---

# 4. Coding Philosophy (From Project Guideline)

AI must produce code that is:

✅ readable
✅ modular
✅ reusable
✅ testable
✅ predictable
✅ scalable

Code must look human-written by a senior engineer.

---

# 5. JavaScript / TypeScript Engineering Rules

---

## Function Design

Functions must:

* do ONE thing
* be small
* predictable
* reusable
* easily testable

Avoid:

* large functions
* nested logic
* hidden side effects

---

## Naming Rules

Use clear semantic naming.

### Variables

```id="v1"
userData
isLoading
hasPermission
orderTotal
```

### Functions

```id="v2"
fetchUsers()
createInvoice()
validateInput()
```

### Components

```id="v3"
UserList
PaymentForm
DashboardLayout
```

---

# 6. Project Structure Discipline

AI must follow existing structure.

Typical pattern:

```id="v4"
feature/
 ├── controller
 ├── service
 ├── repository
 ├── types
 ├── utils
 └── tests
```

Rules:

* No logic dumping
* Keep concerns separated
* Extend existing modules

---

# 7. Logic Placement Rules

| Location     | Responsibility      |
| ------------ | ------------------- |
| UI           | rendering only      |
| hooks        | state & interaction |
| services     | business logic      |
| repositories | data access         |
| utils        | reusable helpers    |

Never mix responsibilities.

---

# 8. Validation Rules

AI must always implement:

* input validation
* schema validation if present
* defensive programming

Assume invalid input exists.

---

# 9. Error Handling Standard

Required:

* centralized error handling
* meaningful messages
* safe user responses
* internal logging

Never ignore errors.

---

# 10. Logging Rules

AI must reuse project logging style.

Logs must include:

* error logs
* debug logs
* execution context

No console spam in production.

---

# 11. Dependency Rules

Before adding library AI must:

1. Check existing utilities
2. Check installed dependencies
3. Justify need

Avoid duplicate packages.

---

# 12. Performance Rules

AI automatically considers:

* unnecessary rerenders
* async operations
* API efficiency
* pagination
* caching opportunities

Performance is default responsibility.

---

# 13. Security Rules

Always enforce:

* input sanitization
* authentication validation
* authorization checks
* environment variable usage

Never expose secrets.

---

# 14. Legacy Code Policy

When existing code is messy:

* understand intent
* preserve behavior
* improve locally
* avoid full rewrite

Evolution > Replacement.

---

# 15. Testing Alignment

AI must follow existing testing setup.

Add:

* unit test strategy
* edge cases
* failure scenarios

Do NOT introduce new testing framework.

---

# 16. Implementation Workflow

AI follows:

```id="v5"
Understand Feature
→ Study Existing Code
→ Follow Current Pattern
→ Implement Minimal Change
→ Validate Impact
→ Self Review
```

---

# 17. AI Self-Review Checklist

Before finishing:

```id="v6"
Matches repository style ✔
Architecture preserved ✔
Readable ✔
Typed (if TS) ✔
Validated ✔
Secure ✔
Performant ✔
Production Ready ✔
```

---

# 18. Improvement Responsibility

AI should gradually improve:

* naming clarity
* modularity
* error safety
* typing quality
* performance

No aggressive refactors.

---

# 19. Communication Style

AI responses must be:

* concise
* engineering-focused
* decision-driven

Avoid tutorials or generic explanations.

---

# 20. Golden Rule

> **The best AI contribution feels native to the repository.**

---

# 21. Expected Outcome

Using this SKILL system:

✅ AI adapts to any JS/TS repository
✅ Code quality continuously improves
✅ Architecture remains stable
✅ Technical debt decreases
✅ Output matches senior engineer level

---

END OF FILE
