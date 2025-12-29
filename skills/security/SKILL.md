---
name: cyber-security
description: Secure systems against threats, implement encryption, protect against common attacks, and maintain compliance. Use when working on security, authentication, penetration testing, or compliance.
sasmp_version: "1.3.0"
bonded_agent: ai-ml-agent
bond_type: PRIMARY_BOND
---

# Cyber Security & Information Security

## Quick Start

Security is a critical aspect of modern systems. Start with fundamentals:

### Security Principles

```
Confidentiality: Data is accessible only to authorized users
Integrity: Data cannot be modified without authorization
Availability: Systems are accessible when needed (No DoS)

Identification: Who are you?
Authentication: Prove who you are
Authorization: What can you do?
Accounting: Track what you did
```

### Authentication Methods

```bash
# Password security
- Use strong passwords (12+ characters, mixed case, symbols)
- Hash passwords with bcrypt/scrypt, never store plaintext
- Implement rate limiting against brute force

# Multi-Factor Authentication (MFA)
- Something you know: password
- Something you have: phone, security key
- Something you are: fingerprint, face

# Recommended: SSH keys for servers
ssh-keygen -t rsa -b 4096
```

### HTTPS/TLS

```
HTTPS ensures:
- Encryption: Data cannot be read in transit
- Authentication: Server identity is verified
- Integrity: Data cannot be tampered with

Steps:
1. Client initiates secure connection
2. Server provides SSL certificate
3. Parties establish encryption keys
4. Encrypted communication begins
```

### Common Vulnerabilities (OWASP Top 10)

```python
# 1. SQL Injection - VULNERABLE
query = "SELECT * FROM users WHERE id = " + user_input

# SECURE - Use parameterized queries
cursor.execute("SELECT * FROM users WHERE id = %s", (user_id,))

# 2. XSS (Cross-Site Scripting) - VULNERABLE
html = f"<h1>{user_input}</h1>"

# SECURE - Escape HTML
from html import escape
html = f"<h1>{escape(user_input)}</h1>"

# 3. CSRF (Cross-Site Request Forgery)
# Include CSRF tokens in forms
<form method="POST">
    <input type="hidden" name="csrf_token" value="{{ csrf_token }}">
</form>
```

### Encryption

```python
# Symmetric encryption (same key for encrypt/decrypt)
from cryptography.fernet import Fernet
key = Fernet.generate_key()
cipher = Fernet(key)
encrypted = cipher.encrypt(b"secret data")
decrypted = cipher.decrypt(encrypted)

# Asymmetric encryption (public/private key pair)
# Use for: Secure communication, digital signatures
from cryptography.hazmat.primitives.asymmetric import rsa
private_key = rsa.generate_private_key(public_exponent=65537, key_size=2048)
public_key = private_key.public_key()
```

### Secure Coding Practices

```python
# 1. Input Validation
def validate_email(email):
    if "@" not in email or len(email) < 5:
        raise ValueError("Invalid email")
    return email

# 2. Error Handling (don't expose internals)
try:
    result = risky_operation()
except Exception:
    return "An error occurred"  # Generic, don't expose stack trace

# 3. Logging security events
import logging
logging.warning(f"Failed login attempt for user: {username}")

# 4. Use environment variables for secrets
import os
db_password = os.getenv("DB_PASSWORD")  # Never hardcode
```

## Key Concepts

- **Threat Modeling**: Identify potential attacks
- **Vulnerability Assessment**: Find weaknesses
- **Penetration Testing**: Simulate attacks (authorized only)
- **Security Monitoring**: Detect suspicious activity
- **Incident Response**: Handle security breaches
- **Compliance**: Meet standards (GDPR, HIPAA, PCI-DSS)

## Learning Path

1. Learn security fundamentals and principles
2. Master authentication and authorization
3. Study common vulnerabilities and defenses
4. Learn cryptography basics
5. Understand network security
6. Practice ethical hacking (authorized)
7. Learn compliance and standards

## Tools

- **Burp Suite**: Web application testing
- **Wireshark**: Network traffic analysis
- **Kali Linux**: Penetration testing platform
- **OWASP ZAP**: Open-source vulnerability scanner
- **Metasploit**: Penetration testing framework

## Important Note

Only perform security testing on systems you own or have explicit written authorization. Unauthorized access is illegal.

## Resources

- **OWASP**: owasp.org
- **PortSwigger**: Web security academy
- **Cybrary**: Free security courses
- **TryHackMe**: Hands-on hacking practice
