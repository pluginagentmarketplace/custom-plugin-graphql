---
name: learn
description: Interactive GraphQL Learning Path
allowed-tools: Read
---

# /learn - Interactive GraphQL Learning Path

Interactive command to start learning GraphQL with guided roadmaps. Choose your learning path and get personalized guidance.

## Usage

```
/learn [topic]
```

## What This Command Does

1. **Topic Selection**: Choose from 7 GraphQL learning paths:
   - GraphQL Fundamentals
   - Schema Design
   - Resolvers & DataLoader
   - Apollo Server
   - Apollo Client
   - Security
   - Code Generation

2. **Level Assessment**: Determine your current level:
   - Beginner: New to GraphQL
   - Intermediate: Built basic GraphQL APIs
   - Advanced: Production experience needed

3. **Learning Path**: Get customized roadmap with:
   - Core concepts and patterns
   - Code examples and best practices
   - Hands-on exercises
   - Real-world project ideas
   - Related skills and agents

4. **Progress Tracking**:
   - Mark topics as completed
   - Track learning progress
   - Unlock advanced topics

## Example Flow

```
> /learn

Welcome to GraphQL Learning Path!

Select your topic:
1. GraphQL Fundamentals (Types, Queries, Mutations)
2. Schema Design (Patterns, Pagination, Errors)
3. Resolvers & DataLoader (N+1, Batching)
4. Apollo Server (Plugins, Federation, Caching)
5. Apollo Client (Hooks, Cache, Subscriptions)
6. Security (Auth, Rate Limiting, Validation)
7. Code Generation (TypeScript, React Hooks)

Your choice: 1

Select your level:
1. Beginner (New to GraphQL)
2. Intermediate (Basic APIs built)
3. Advanced (Production optimization)

Your choice: 1

✅ GraphQL Fundamentals - Beginner Path
Estimated: 2-4 hours

📚 Phase 1: Core Concepts
- Scalar types (String, Int, Float, Boolean, ID)
- Object types and fields
- Non-null (!) and list ([]) modifiers
- Enums and input types

📚 Phase 2: Operations
- Writing queries
- Variables and aliases
- Fragments for reusability
- Mutations for data changes

📚 Phase 3: Subscriptions
- Real-time data with subscriptions
- WebSocket connections
- Filtering subscription events

Would you like to start with Phase 1? (yes/no)
```

## Learning Paths Overview

| Path | Duration | Prerequisites |
|------|----------|---------------|
| Fundamentals | 2-4 hours | None |
| Schema Design | 3-5 hours | Fundamentals |
| Resolvers | 4-6 hours | Fundamentals, Schema |
| Apollo Server | 4-6 hours | Resolvers |
| Apollo Client | 4-6 hours | Fundamentals |
| Security | 3-5 hours | Server basics |
| Code Generation | 2-4 hours | TypeScript basics |

## Tips

- Start with Fundamentals if you're new to GraphQL
- Complete prerequisites before advanced topics
- Practice with the code examples in each skill
- Use related agents for deeper guidance
- Build a real project combining multiple topics

## Related Commands

- `/assess` - Test your GraphQL knowledge
- `/browse-agent` - Explore GraphQL agents
- `/roadmap` - View complete learning roadmaps
