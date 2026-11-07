
# Removal Test

The following rules are important because removing them
could cause the AI agent to make specific security mistakes.

### 1. Never read or expose .env files.
Without this rule, the AI agent might access environment
files and expose sensitive configuration information.

### 2. Never print API keys, passwords, or access tokens.
Without this rule, the AI agent might accidentally include
credentials in its responses or generated code.

### 3. Never use real personal data in examples or tests.
Without this rule, the AI agent might use real user information
in educational examples or testing scenarios.

### 4. Never perform attacks or scans against real targets.
Without this rule, the AI agent might perform unauthorized
security testing outside approved lab environments.

### 5. Validate all user inputs on the server.
Without this rule, the AI agent might rely only on client-side
validation, allowing invalid or malicious input to reach the server.

### 6. Never store passwords in plain text.
Without this rule, the AI agent might store passwords without
proper hashing, exposing user credentials.

### 7. Use parameterized queries for database operations.
Without this rule, the AI agent might construct unsafe SQL
queries that could lead to SQL injection vulnerabilities.

### 8. Analyze only output explicitly provided by the user.
Without this rule, the AI agent might attempt to perform
live scans instead of analyzing user-provided results.
