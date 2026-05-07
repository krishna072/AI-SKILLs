# 🤖 AI_CODING_RULEBOOK.md

**Production-Grade AI Coding Standards & Engineering Rules**

---

# 1. Purpose

This rulebook defines **HOW AI writes code**.

Goals:

✅ Human-level clean code
✅ Predictable structure
✅ Maintainable systems
✅ Scalable architecture
✅ Production safety

AI must follow this document for **every implementation task**.

---

# 2. Universal Coding Principles

---

## 2.1 Readability Over Cleverness

Prefer:

* clear logic
* understandable naming
* explicit behavior

Avoid:

* smart one-liners
* hidden logic
* unnecessary abstraction

---

## 2.2 Single Responsibility Rule

Each unit must have one responsibility.

| Unit       | Responsibility   |
| ---------- | ---------------- |
| Component  | UI only          |
| Service    | Business logic   |
| Controller | Request handling |
| Repository | Database access  |
| Hook       | State logic      |

---

## 2.3 Function Design Rules

Functions must be:

* small
* deterministic
* testable

Rules:

* ≤ 30 lines preferred
* ≤ 3 parameters preferred
* avoid side effects
* return predictable output

Bad:

```id="bad_fn"
processUserDataEverything()
```

Good:

```id="good_fn"
validateUser()
createUser()
sendWelcomeEmail()
```

---

# 3. Naming Conventions

---

## Variables

```id="var_names"
user
userProfile
isLoading
hasPermission
```

Avoid:

```id="bad_var_names"
data
temp
x
value1
```

---

## Functions

```id="func_names"
getUser()
createOrder()
calculatePrice()
fetchProducts()
```

Must start with action verbs.

---

## Components

```id="comp_names"
UserCard
ProductList
DashboardLayout
```

---

## Files

```id="file_names"
user.service.ts
auth.controller.ts
order.repository.ts
```

---

# 4. Project Structure Standard

---

## Backend Structure

```id="backend_structure"
src/
 ├── modules/
 │   └── user/
 │       ├── user.controller.ts
 │       ├── user.service.ts
 │       ├── user.repository.ts
 │       ├── user.schema.ts
 │       └── user.routes.ts
 ├── middleware/
 ├── utils/
 ├── configs/
 └── tests/
```

Rules:

* Feature-based modules
* No giant folders
* No mixed responsibilities

---

## Frontend Structure

```id="frontend_structure"
src/
 ├── components/
 ├── features/
 ├── hooks/
 ├── services/
 ├── store/
 ├── layouts/
 ├── utils/
 └── types/
```

---

# 5. JavaScript / TypeScript Standards

---

## Mandatory Rules

* Prefer TypeScript
* Strict typing enabled
* No `any`
* No implicit types
* Use interfaces/types

Good:

```id="ts_good"
interface User {
  id: string;
  email: string;
}
```

---

## Async Handling

Always:

```id="async_good"
try {
  const user = await service.getUser(id);
} catch (error) {
  handleError(error);
}
```

Never:

```id="async_bad"
service.getUser(id);
```

---

## Error Handling Pattern

Use centralized errors:

```id="error_pattern"
throw new AppError("User not found", 404);
```

---

# 6. API Development Rules

---

## Controller Responsibilities

* validate request
* call service
* return response

NO business logic.

---

## Service Responsibilities

* core logic
* orchestration
* validation rules

---

## Repository Responsibilities

* database queries only

---

## API Response Standard

```id="api_response"
{
  success: true,
  data: {},
  message: "Operation successful"
}
```

---

# 7. React / Frontend Engineering Rules

---

## Component Rules

Components must be:

* small
* reusable
* stateless when possible

---

## State Management Rules

Use:

* local state → UI state
* global store → shared state
* server cache → React Query

Avoid:

❌ unnecessary global state

---

## React Best Practices

* Memoization only when needed
* Avoid prop drilling
* Extract hooks
* Lazy load heavy components

---

## Hook Pattern

```id="hook_pattern"
useUserData()
useAuth()
useProducts()
```

Hooks contain logic — not UI.

---

# 8. Performance Rules

AI must enforce:

* pagination for lists
* debounce search
* caching APIs
* code splitting
* lazy imports

Never fetch large datasets blindly.

---

# 9. Security Rules

---

AI must include:

* input validation
* sanitization
* authentication checks
* authorization layer
* environment variables

Never:

* expose secrets
* trust client data
* store plain passwords

---

# 10. Database Rules

---

AI must:

* normalize schema
* index frequently queried fields
* paginate queries
* avoid N+1 queries

---

# 11. Testing Rules

---

Minimum requirements:

### Unit Tests

* services
* utilities
* hooks

### Integration Tests

* API routes
* DB operations

### E2E Tests

* user workflows

---

# 12. Logging Standards

---

Use structured logs:

```id="log_example"
logger.info("User created", { userId });
```

Never use random console logs in production.

---

# 13. Refactoring Rules

AI must refactor when:

* duplication appears
* function grows large
* logic becomes unclear
* performance degrades

---

# 14. Code Review Checklist

Before final output AI verifies:

```id="review_checklist"
Readable ✔
Typed ✔
Secure ✔
Modular ✔
Testable ✔
Scalable ✔
Production Ready ✔
```

---

# 15. Anti-Patterns (STRICTLY FORBIDDEN)

❌ God components
❌ Massive controllers
❌ Inline SQL everywhere
❌ Business logic in UI
❌ Global mutable state
❌ Silent error catching
❌ Hardcoded configs

---

# 16. Framework-Specific Rules

---

## Node.js

* Layered architecture
* Async-safe APIs
* Middleware validation
* Central error handler

---

## FastAPI

* Pydantic schemas
* Dependency injection
* Background tasks for heavy work
* Typed responses

---

## Shopify Apps

* Follow embedded app pattern
* Secure session handling
* Webhook verification
* Rate limit awareness
* Admin API abstraction layer

---

## Next.js

* Server Components preferred
* API routes modular
* Edge-safe code
* Proper caching strategy

---

# 17. AI Coding Behavior

AI must:

* explain decisions briefly
* suggest improvements
* prevent bad patterns
* think long-term scalability

AI must NOT:

* blindly generate code
* ignore architecture
* produce tutorial-style output

---

# 18. Golden Engineering Rule

> **Clean code is not optional.
> Clean architecture is mandatory.**

---

# 19. Expected Outcome

Following this rulebook results in:

✅ Senior-level codebases
✅ Faster onboarding
✅ Fewer bugs
✅ Easier scaling
✅ Long-term maintainability

---

END OF DOCUMENT
