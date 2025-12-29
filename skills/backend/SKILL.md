---
name: backend-development
description: Master backend technologies including programming languages, databases, REST APIs, authentication systems, and building scalable server-side applications. Use when working with backend systems, APIs, databases, or server-side architecture.
sasmp_version: "1.3.0"
bonded_agent: ai-ml-agent
bond_type: PRIMARY_BOND
---

# Backend Development

## Quick Start

Backend development involves building server-side applications that power websites and mobile apps. Start with a programming language:

### Choose Your Language

```python
# Python: Popular for backend, data science, automation
# Install Python 3.10+
python --version

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Basic Hello World
print("Hello, Backend!")
```

```javascript
// Node.js: JavaScript on server, great for full-stack
// Install Node.js 16+
node --version

// Basic Hello World
console.log("Hello, Backend!");
```

## Core Concepts

### 1. Request-Response Cycle

```python
# Flask example
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello():
    return {'message': 'Hello, World!'}

if __name__ == '__main__':
    app.run(debug=True)
```

### 2. Database Operations

```python
# PostgreSQL with Python (psycopg2)
import psycopg2

conn = psycopg2.connect(
    "dbname=mydb user=postgres password=secret"
)
cursor = conn.cursor()

# Create table
cursor.execute('''
    CREATE TABLE users (
        id SERIAL PRIMARY KEY,
        email VARCHAR(255),
        created_at TIMESTAMP DEFAULT NOW()
    )
''')
conn.commit()
```

### 3. REST API Design

```python
# RESTful endpoints pattern
GET    /api/users      # List all users
GET    /api/users/123  # Get user with id 123
POST   /api/users      # Create new user
PUT    /api/users/123  # Update user 123
DELETE /api/users/123  # Delete user 123
```

## Learning Resources

- **Official Docs**: Python (python.org), Node.js (nodejs.org), Java (oracle.com)
- **Practice**: Build a simple TODO API
- **Database**: PostgreSQL fundamentals, SQL basics
- **API Tools**: Postman or Thunder Client for testing

## Next Steps

1. Choose a programming language
2. Learn database fundamentals
3. Build a simple REST API
4. Learn about authentication
5. Study system design and scalability
