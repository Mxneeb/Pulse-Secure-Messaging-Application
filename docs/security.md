# Security Policy

## Supported Versions

Currently, these versions of Pulse are being supported with security updates:

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |

## Encryption Implementation

Pulse uses industry-standard encryption methods to protect user data:

### Message Encryption

All messages in Pulse are encrypted using AES (Advanced Encryption Standard):

- Each message is encrypted with a unique AES key
- The key and initialization vector (IV) are generated for each message
- Both the key and IV are sent along with the encrypted message, but only to authorized recipients

### User Authentication

User passwords are securely handled using the following methods:

- Passwords are encrypted before storage
- A fixed key is used for password encryption (note: in future versions, this will be improved with salted hashing)
- User credentials are stored in an encrypted file (`users.enc`)

### Data Storage

- Chat messages are stored in an encrypted format
- Profile information is stored with proper access controls

## Security Features

1. **End-to-End Encryption**: All messages are encrypted from sender to recipient
2. **Secure Authentication**: Login credentials are validated against encrypted storage
3. **Encrypted Storage**: User data is stored in encrypted format
4. **Network Security**: Communication happens over encrypted channels

## Current Limitations

1. The fixed encryption key for password storage should be replaced with a more secure approach like salted hashing
2. The application currently sends encryption keys along with messages, which could be improved
3. The application stores messages locally, which could be secured with additional encryption

## Reporting a Vulnerability

If you discover a security vulnerability within Pulse, please send an email to security@pulse-messaging.com. All security vulnerabilities will be promptly addressed.

Please include the following information in your report:

- Type of vulnerability
- Steps to reproduce the issue
- Affected versions
- Potential impact

## Security Roadmap

Future security improvements planned for Pulse:

1. Implement salted password hashing instead of symmetric encryption
2. Add two-factor authentication
3. Implement perfect forward secrecy for message encryption
4. Add secure message deletion with guaranteed data removal
5. Implement certificate pinning for enhanced security
