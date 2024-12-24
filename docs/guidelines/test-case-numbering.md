# Test Case Numbering Guidelines

## Format
Test cases should follow this numbering format:
```
[Module]-[SubModule]-[Type]-[Number]
```

Example: `AUTH-LOG-FUN-001`

### Components:

1. **Module Code (2-4 chars)**
   - AUTH: Authentication
   - USR: User Management
   - GIFT: Gift Management
   - ORD: Order Management
   etc.

2. **SubModule Code (2-3 chars)**
   - LOG: Login
   - REG: Registration
   - PROF: Profile
   etc.

3. **Type Code (2-3 chars)**
   - FUN: Functional
   - SEC: Security
   - PERF: Performance
   - UI: User Interface
   - API: API Testing

4. **Number (3 digits)**
   - Sequential number starting from 001

## Examples:
- `AUTH-LOG-FUN-001`: Authentication - Login - Functional Test #1
- `GIFT-PDP-UI-001`: Gift - Product Detail Page - UI Test #1
- `USR-PROF-API-001`: User - Profile - API Test #1

## Best Practices:
1. Always use uppercase for module, submodule, and type codes
2. Always use 3 digits for the number portion
3. Keep a central registry of module and submodule codes
4. When adding a new test case, use the next available number in its category
5. Never reuse numbers, even if old test cases are deleted
