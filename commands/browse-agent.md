---
name: browse-agent
description: Explore GraphQL Specialized Agents
allowed-tools: Read
---

# /browse-agent - Explore GraphQL Agents

Discover and explore the 7 specialized GraphQL agents available in this plugin.

## Usage

```
/browse-agent [agent-name]
```

## Agents Overview

### 1. GraphQL Fundamentals Agent
> Master core GraphQL concepts and type system

**Expertise**:
- Type system (scalars, objects, enums, interfaces, unions)
- Queries, mutations, subscriptions
- Variables, aliases, fragments
- Nullability and list modifiers

**Best For**: Learning GraphQL basics, understanding type system, writing operations

**Invoke**: `Task(subagent_type="graphql:01-graphql-fundamentals")`

---

### 2. GraphQL Schema Agent
> Design production-grade GraphQL schemas

**Expertise**:
- Naming conventions and best practices
- Relay-style connection pagination
- Error handling patterns (Payload, Union)
- Node interface for global object identification
- Schema organization and modularization

**Best For**: Designing APIs, pagination patterns, error handling strategy

**Invoke**: `Task(subagent_type="graphql:02-graphql-schema")`

---

### 3. GraphQL Resolvers Agent
> Build performant data fetching with DataLoader

**Expertise**:
- Resolver signature and patterns
- DataLoader for N+1 prevention
- Batching and caching strategies
- Context design and setup
- Subscription resolvers with PubSub

**Best For**: Performance optimization, N+1 issues, resolver implementation

**Invoke**: `Task(subagent_type="graphql:03-graphql-resolvers")`

---

### 4. Apollo Server Agent
> Production-ready GraphQL server configuration

**Expertise**:
- Apollo Server v4 setup and configuration
- Plugin system and lifecycle hooks
- Apollo Federation for microservices
- Server-side caching (Redis, CDN)
- Error formatting and logging

**Best For**: Server setup, federation architecture, production deployment

**Invoke**: `Task(subagent_type="graphql:04-graphql-apollo-server")`

---

### 5. Apollo Client Agent
> React integration with Apollo Client 3.x

**Expertise**:
- React hooks (useQuery, useMutation, useSubscription)
- Cache management and normalization
- Optimistic UI updates
- Local state with reactive variables
- Error handling and loading states

**Best For**: React apps, cache strategies, real-time updates

**Invoke**: `Task(subagent_type="graphql:05-graphql-apollo-client")`

---

### 6. GraphQL Security Agent
> Secure GraphQL APIs against vulnerabilities

**Expertise**:
- JWT authentication with refresh tokens
- Authorization with graphql-shield
- Rate limiting (per-user, per-operation)
- Query complexity and depth limiting
- Input validation and sanitization
- CORS and security headers

**Best For**: Auth implementation, security hardening, vulnerability prevention

**Invoke**: `Task(subagent_type="graphql:06-graphql-security")`

---

### 7. GraphQL Codegen Agent
> TypeScript type generation from schemas

**Expertise**:
- GraphQL Code Generator configuration
- TypeScript types from schema
- React Apollo hooks generation
- Near-operation-file preset
- Fragment handling and colocation
- Client preset (modern approach)

**Best For**: Type safety, React hooks generation, TypeScript integration

**Invoke**: `Task(subagent_type="graphql:07-graphql-codegen")`

---

## Agent Capabilities Matrix

| Agent | Schema | Server | Client | Security | Types |
|-------|--------|--------|--------|----------|-------|
| Fundamentals | ✅ | - | - | - | - |
| Schema | ✅✅ | - | - | - | - |
| Resolvers | ✅ | ✅ | - | - | - |
| Apollo Server | - | ✅✅ | - | ✅ | - |
| Apollo Client | - | - | ✅✅ | - | ✅ |
| Security | - | ✅ | - | ✅✅ | - |
| Codegen | ✅ | - | ✅ | - | ✅✅ |

## How to Use Agents

1. **Browse agents** to find the right expertise
2. **Invoke agent** using Task tool with subagent_type
3. **Ask specific questions** within their domain
4. **Combine agents** for complex tasks

## Example Interactions

```
# Learn about DataLoader
Task(subagent_type="graphql:03-graphql-resolvers")
"How do I implement DataLoader for a hasMany relationship?"

# Set up authentication
Task(subagent_type="graphql:06-graphql-security")
"Implement JWT authentication with refresh tokens"

# Generate TypeScript types
Task(subagent_type="graphql:07-graphql-codegen")
"Configure codegen for React Apollo hooks"
```

## Related Commands

- `/learn` - Start guided learning path
- `/assess` - Evaluate your knowledge
- `/roadmap` - View complete roadmaps
