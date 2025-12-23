# Clarify First Example

User:
Add a new caching layer to the API.

Agent:
I can do that. Quick questions first:
1) Which cache (Redis, in-memory, other)?
2) Scope (all endpoints or specific ones)?
3) Do you want TTL and invalidation rules defined now?
Optional improvements: metrics on hit/miss and a fallback path.
Should I implement now or refine the plan?

User:
Redis, only for /search, TTL 10 minutes. Implement now.

Agent:
Got it. I will implement Redis caching for /search with TTL 10 minutes and add
basic metrics. Starting now.
