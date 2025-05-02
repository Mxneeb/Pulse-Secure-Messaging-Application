# Pulse - Secure Messaging Application

## Overview

Pulse is a privacy-focused messaging application that offers end-to-end encryption for secure conversations. It prioritizes user confidentiality, eliminating data exploitation and unauthorized surveillance. With Pulse, users have complete control over their data with transparent practices and minimal data retention.

The application is built using C# and Windows Forms, providing a user-friendly interface for real-time messaging, file sharing, and group chats.

## Key Features

- **End-to-End Encryption**: All messages are encrypted using AES encryption for maximum security
- **Secure Authentication**: User credentials are stored with encryption
- **Real-Time Messaging**: Instant communication between users
- **User Profiles**: Customizable user profiles with profile pictures
- **Status Updates**: Share your availability and current activities
- **Chat Rooms**: Support for multiple users in group conversations
- **File Sharing**: Ability to share images and files
- **Minimal Data Retention**: Only essential data is stored

## Project Structure

```
Pulse/
├── src/                    # Source code
│   ├── Login/              # Main project
│   │   ├── Forms/          # Windows Forms
│   │   ├── Models/         # Data models
│   │   ├── Utils/          # Utility classes
│   │   └── Resources/      # Resources files
├── docs/                   # Documentation
│   ├── images/             # Documentation images
│   └── project_report.md   # Project report
├── assets/                 # Assets for the project
│   └── pulse-logo.png      # Project logo
└── tests/                  # Test files
```

## Getting Started

### Prerequisites

- Visual Studio 2019 or later
- .NET Framework 4.7.2 or later
- Windows 7 or later

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Mxneeb/Pulse-Secure-Messaging-Application
```

2. Open the solution file (`Login.sln`) in Visual Studio.

3. Build the solution by pressing F6 or selecting Build > Build Solution from the menu.

4. Run the application by pressing F5 or selecting Debug > Start Debugging from the menu.

### Usage

1. **Sign Up**: Create a new account with a unique username and secure password.
2. **Log In**: Log in using your credentials.
3. **Chat**: Start chatting with other users in real-time.
4. **Profile**: Customize your profile and upload a profile picture.
5. **Status**: Update your status to let others know about your availability.

## Security Features

Pulse implements several security measures to protect user data:

- **AES Encryption**: All messages are encrypted using AES encryption with unique keys.
- **Password Hashing**: User passwords are encrypted before storage.
- **Secure File Storage**: Profile information is stored securely.
- **Encrypted User Data**: User credentials are stored in an encrypted format.

## Development Roadmap

Pulse was developed in three sprints:

1. **Sprint 1**: UI/UX design and prototyping
2. **Sprint 2**: Core functionality implementation
3. **Sprint 3**: Network integration, multi-user support, and final testing


