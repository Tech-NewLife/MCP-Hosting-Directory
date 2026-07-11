# Contabo MCP

> An MCP (Model Context Protocol) server specification for integrating AI assistants with Contabo hosting services.

**Status:** 🚧 Planned

---

# Overview

Contabo MCP aims to provide a secure interface between AI assistants and the Contabo platform, allowing users to manage cloud infrastructure and hosting services using natural language.

Instead of manually using the customer control panel, users can simply ask an AI assistant to perform common tasks such as restarting a VPS, viewing server details, reinstalling an operating system, or checking resource usage.

---

# Why Contabo MCP?

Contabo provides affordable cloud infrastructure and hosting services including:

- VPS
- VDS
- Dedicated Servers
- Object Storage
- Networking

An MCP server would make these services accessible through AI assistants while maintaining secure authentication and permission controls.

---

# Goals

The Contabo MCP project aims to:

- Simplify cloud infrastructure management
- Reduce repetitive administrative tasks
- Enable AI-powered server operations
- Standardize hosting automation using MCP

---

# Planned Features

## VPS Management

### Information

- List VPS
- VPS Details
- Resource Usage
- Operating System
- Assigned IP Addresses
- Hostname

### Power Operations

- Restart VPS
- Shutdown VPS
- Power On VPS
- Force Reboot

### Administration

- Reset Root Password
- Reinstall Operating System
- Change Hostname

---

## Dedicated Servers

### Information

- List Servers
- Hardware Information
- Public IP Addresses

### Power

- Reboot Server
- Shutdown Server
- Power Cycle

---

## Object Storage

- List Buckets
- Create Bucket
- Delete Bucket

---

# Authentication

Contabo MCP should support secure authentication using:

- API Token
- Access Token

---

# Security

The MCP server should:

- Require authentication
- Use HTTPS
- Respect user permissions
- Log administrative actions
- Support read-only mode

---

# Example Prompts

## VPS

```
Restart my VPS.
```

```
Show my VPS details.
```

```
Reinstall Ubuntu 24.04.
```

---

# Example Workflow

```
User

↓

Restart my VPS

↓

MCP Client

↓

Contabo MCP

↓

Authenticate

↓

Contabo API

↓

Restart VPS

↓

Success Response

↓

AI Assistant

↓

Your VPS has been restarted successfully.
```

---

# Proposed MCP Tools

## VPS

| Tool | Description |
|------|-------------|
| list_vps | List VPS instances |
| get_vps | Show VPS details |
| restart_vps | Restart VPS |
| shutdown_vps | Shutdown VPS |
| reinstall_vps | Reinstall operating system |

---

## Dedicated Servers

| Tool | Description |
|------|-------------|
| list_servers | List dedicated servers |
| reboot_server | Reboot server |
| shutdown_server | Shutdown server |

---

# Suggested Directory Structure

```text
providers/contabo/

README.md
api.md
authentication.md
examples.md
roadmap.md
```

---

# Development Roadmap

## Phase 1

- Research APIs
- Authentication
- Documentation

## Phase 2

- VPS Management
- Dedicated Servers

## Phase 3

- Object Storage
- Networking

---

# Contributing

Contributions are welcome.

Please submit a Pull Request or open an Issue.

---

# Disclaimer

This project is an independent community effort intended to explore MCP integrations for hosting platforms.

Contabo is a trademark of its respective owner. This project is not affiliated with, endorsed by, or maintained by Contabo unless explicitly stated.
