---
name: system-design
description: Design large-scale distributed systems, handle millions of users, and build reliable architectures. Use when working on system architecture, scalability, database design, or designing for scale.
sasmp_version: "1.3.0"
bonded_agent: ai-ml-agent
bond_type: PRIMARY_BOND
---

# System Design & Architecture

## Quick Start

System design involves making high-level decisions about how systems are structured:

### Design Process

```
1. Understand Requirements
   - Functional: What the system does
   - Non-functional: Scale, latency, availability

2. Back-of-Envelope Calculation
   - Estimate users, requests per second, storage

3. High-Level Design
   - Identify major components
   - Draw architecture diagram

4. Deep Dive
   - Database selection
   - Caching strategy
   - API design
```

### Database Selection

```
Relational (SQL):
- PostgreSQL, MySQL: ACID transactions, complex queries
- Use for: Financial data, complex relationships

NoSQL:
- MongoDB: Flexible schema, document storage
- Redis: In-memory, caching, sessions
- Cassandra: Distributed, high write throughput
- Elasticsearch: Full-text search, analytics

Choice depends on:
- Data structure (structured vs flexible)
- Query patterns (complex joins vs simple lookups)
- Scale requirements (single node vs distributed)
```

### Caching Strategy

```python
# Cache layers
Browser Cache (Static assets)
    ↓
CDN Cache (Global distribution)
    ↓
Server Cache (Redis, Memcached)
    ↓
Database Cache (Query results)
    ↓
Database

# Cache invalidation patterns
- TTL (Time-To-Live): Auto expire after time
- LRU (Least Recently Used): Remove oldest
- Explicit: Invalidate when data changes
```

### Load Balancing

```
┌─────────────┐
│   Client    │
└──────┬──────┘
       │
┌──────▼──────────┐
│  Load Balancer  │
└──────┬──────────┘
       │
   ┌───┴───┬───────┐
   │       │       │
┌──▼─┐ ┌──▼─┐ ┌──▼─┐
│ S1 │ │ S2 │ │ S3 │  (Server replicas)
└────┘ └────┘ └────┘
```

### Microservices Pattern

```
User Service    Product Service    Order Service
     │                 │                  │
     └─────────────────┼──────────────────┘
                       │
                  API Gateway
                       │
                    Client
```

## Scalability Patterns

```
Vertical Scaling: Add more power to single server
- CPU, RAM upgrades
- Simple but has limits

Horizontal Scaling: Add more servers
- Requires load balancing
- Better for distributed systems
- Preferred approach
```

## Consistency Models

```
Strong Consistency:
- All users see same data immediately
- Example: Banking systems

Eventual Consistency:
- Data eventually becomes consistent
- Better performance, higher availability
- Example: Social media likes
```

## Key Metrics

- **Latency**: Response time (should be < 100ms)
- **Throughput**: Requests per second
- **Availability**: Uptime percentage (99.99%)
- **Durability**: Data not lost

## Learning Path

1. Master design fundamentals
2. Learn database and caching design
3. Study load balancing and scaling
4. Understand microservices
5. Design real-world systems
6. Learn fault tolerance patterns

## Common Interview Patterns

- Design Twitter/Instagram feed
- Design URL shortener
- Design file storage system (Google Drive)
- Design video streaming (Netflix)
- Design payment system

## Resources

- **System Design Interview** book
- **Alex Xu** system design resources
- **Grokking** system design course
- **High Scalability** blog
