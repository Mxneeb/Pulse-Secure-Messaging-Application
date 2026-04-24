# Project Structure

This document outlines the structure of the Pulse Secure Messaging application codebase.

## Repository Structure

```
pulse-secure-messaging/
├── src/
│   └── Login/                  # Main WinForms project
│       ├── Form1.cs
│       ├── Page1.cs
│       ├── Page2.cs
│       ├── Page3.cs
│       ├── Signup.cs
│       ├── clsLogin.cs
│       ├── Properties/
│       ├── App.config
│       └── Login.csproj
├── docs/
│   ├── images/                 # Architecture and UI assets
│   ├── project-artifacts/      # Original design image bundle folder
│   ├── projectStructure.md
│   └── security.md
├── assets/
│   └── icons/
├── Login.sln
└── README.md
```

## Core Components

### Authentication System

- **Form1.cs**: Login interface
- **Signup.cs**: User registration
- Uses encryption for secure storage of credentials

### Messaging System

- **Page1.cs**: Main chat interface
- Implements TCP client-server architecture
- Uses AES encryption for secure message transmission

### Profile Management

- **Page2.cs**: User profile settings
- Allows customization of user information and profile pictures

### Media Sharing

- **Page3.cs**: File sharing functionality
- Supports image uploading and sharing

### Encryption Utilities

- AES encryption for message content
- Secure credential storage
- End-to-end encryption implementation

## Data Flow

1. **User Authentication**:
   - User credentials are validated against encrypted storage
   - Successful login leads to the chat interface

2. **Message Transmission**:
   - Messages are encrypted on the sender's device
   - Transmitted over TCP
   - Decrypted on the recipient's device

3. **Profile Management**:
   - Profile changes are saved locally
   - Profile pictures are stored in a designated directory

4. **File Sharing**:
   - Files are uploaded to a shared storage
   - Recipients can access shared files through the interface
