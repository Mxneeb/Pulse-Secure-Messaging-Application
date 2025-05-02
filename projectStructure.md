# Project Structure

This document outlines the structure of the Pulse Secure Messaging application codebase.

## Repository Structure

```
pulse-secure-messaging/
├── .github/
│   └── workflows/              # GitHub Actions workflows
│       └── build.yml           # CI/CD workflow
├── assets/
│   └── pulse-logo.png          # Project logo
├── docs/
│   ├── images/                 # Documentation images
│   ├── user_stories.md         # User stories documentation
│   └── project_report.md       # Full project report
├── src/
│   └── Login/                  # Main project folder
│       ├── Forms/              # Windows Forms classes
│       │   ├── Form1.cs        # Login form
│       │   ├── Page1.cs        # Main chat interface
│       │   ├── Page2.cs        # Profile settings
│       │   ├── Page3.cs        # Media sharing
│       │   └── Signup.cs       # Registration form
│       ├── Models/             # Data models
│       │   └── ClientInfo.cs   # Client information model
│       ├── Utils/              # Utility classes
│       │   ├── Encryption.cs   # Encryption utilities
│       │   └── NetworkManager.cs # Network communication
│       ├── Resources/          # Application resources
│       ├── App.config          # Application configuration
│       ├── Login.csproj        # Project file
│       └── Program.cs          # Entry point
├── tests/                      # Test projects
│   └── Login.Tests/            # Unit tests for the Login project
├── .gitignore                  # Git ignore file
├── LICENSE                     # License file
├── Login.sln                   # Solution file
└── README.md                   # Project overview
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
