---
name: assess
description: GraphQL Knowledge Assessment & Skill Gap Analysis
allowed-tools: Read
---

# /assess - GraphQL Knowledge Assessment

Evaluate your GraphQL knowledge level and identify skill gaps across different areas.

## Usage

```
/assess [topic]
```

## Assessment Areas

### 1. GraphQL Fundamentals
- Type system (scalars, objects, enums)
- Queries, mutations, subscriptions
- Variables and fragments
- Nullability and lists

### 2. Schema Design
- Naming conventions
- Relay-style pagination
- Error handling patterns
- Interface and union types

### 3. Resolvers & Performance
- Resolver signature (parent, args, context, info)
- DataLoader pattern
- N+1 query prevention
- Context design

### 4. Apollo Server
- Server configuration
- Plugins and middleware
- Federation architecture
- Caching strategies

### 5. Apollo Client
- React hooks (useQuery, useMutation)
- Cache management
- Optimistic updates
- Subscriptions

### 6. Security
- Authentication (JWT)
- Authorization (graphql-shield)
- Rate limiting
- Input validation

### 7. Code Generation
- TypeScript type generation
- React hooks generation
- Configuration options
- Fragment handling

## Example Assessment

```
> /assess

GraphQL Knowledge Assessment

Choose assessment type:
1. Quick Self-Assessment (5 min)
2. Topic-Specific Assessment
3. Full Diagnostic (All areas)

Your choice: 3

📊 Full GraphQL Assessment

Rate your knowledge (1-5):

Fundamentals:
  Type System: 4 (Advanced)
  Operations: 4 (Advanced)
  Subscriptions: 2 (Foundational)

Schema Design:
  Naming Conventions: 3 (Intermediate)
  Pagination: 2 (Foundational)
  Error Handling: 2 (Foundational)

Resolvers:
  Basic Resolvers: 4 (Advanced)
  DataLoader: 1 (Beginner)
  Context Design: 2 (Foundational)

Apollo Server:
  Basic Setup: 3 (Intermediate)
  Plugins: 1 (Beginner)
  Federation: 1 (Beginner)

Apollo Client:
  React Hooks: 3 (Intermediate)
  Cache Management: 2 (Foundational)
  Subscriptions: 1 (Beginner)

Security:
  Authentication: 3 (Intermediate)
  Authorization: 2 (Foundational)
  Rate Limiting: 1 (Beginner)

Code Generation:
  Basic Setup: 2 (Foundational)
  Advanced Config: 1 (Beginner)

📈 Results Summary

Overall Level: Intermediate GraphQL Developer

Strengths (70%+):
✅ Type system fundamentals
✅ Basic queries and mutations
✅ Basic resolver implementation

Areas to Improve (40-70%):
⚠️ Schema design patterns
⚠️ Apollo Client hooks
⚠️ Authentication

Priority Learning (< 40%):
❌ DataLoader & N+1 prevention
❌ Apollo federation
❌ Rate limiting & security
❌ Advanced code generation

Recommended Learning Path:
1. Master DataLoader pattern (prevents N+1)
2. Learn connection pagination
3. Implement graphql-shield authorization
4. Set up code generation workflow

Use: /learn resolvers to start
```

## Skill Levels

| Level | Description | Typical Experience |
|-------|-------------|-------------------|
| Beginner | Just starting | 0-1 month |
| Foundational | Basic understanding | 1-3 months |
| Intermediate | Can build APIs | 3-6 months |
| Advanced | Production experience | 6-12 months |
| Expert | Architectural decisions | 12+ months |

## Assessment Benefits

- Identify knowledge gaps quickly
- Get prioritized learning recommendations
- Track progress over time
- Find optimal learning sequence
- Validate skill improvements

## Related Commands

- `/learn` - Start learning identified gaps
- `/browse-agent` - Get help from specialized agents
- `/roadmap` - View complete learning paths
