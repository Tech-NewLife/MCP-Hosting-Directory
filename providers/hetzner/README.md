# Hetzner MCP

> An MCP (Model Context Protocol) server specification for integrating AI assistants with Hetzner Cloud and Dedicated Infrastructure.

**Status:** 🚧 Planned

---

# Overview

Hetzner MCP aims to provide a secure interface between AI assistants and the Hetzner platform, allowing users to manage cloud infrastructure and dedicated servers using natural language.

Instead of manually using the Hetzner Cloud Console or Robot interface, users can simply ask an AI assistant to deploy, manage, and monitor infrastructure resources.

---

# Why Hetzner MCP?

Hetzner provides reliable cloud and dedicated infrastructure services including:

- Cloud Servers
- Dedicated Servers
- Storage Boxes
- Object Storage
- Volumes
- Load Balancers
- Private Networks
- Firewalls
- Floating IPs
- DNS

An MCP server makes these services accessible through AI assistants while maintaining secure authentication and permission controls.

---

# Goals

The Hetzner MCP project aims to:

- Simplify infrastructure management
- Reduce repetitive administrative tasks
- Enable AI-powered cloud automation
- Standardize cloud operations using MCP

---

# Planned Features

## Cloud Servers

### Information

- List Servers
- Server Details
- CPU Usage
- Memory Usage
- Disk Usage
- Public & Private IP Addresses

### Management

- Create Server
- Restart Server
- Shutdown Server
- Power On Server
- Rebuild Server
- Delete Server
- Resize Server

---

## Dedicated Servers

- List Servers
- Hardware Information
- Reboot Server
- Rescue Mode
- Reset Server

---

## Networking

- Floating IPs
- Firewalls
- Private Networks
- Load Balancers

---

## Storage

- Volumes
- Storage Boxes
- Object Storage

---

## DNS

- List Zones
- Create Records
- Update Records
- Delete Records

---

# Authentication

Hetzner MCP should support secure authentication using:

- API Token
- Access Token

---

# Security

The MCP server should:

- Require authentication
- Use HTTPS
- Respect account permissions
- Log administrative actions
- Support read-only mode

---

# Example Prompts

## Cloud

```
Show my cloud servers.
```

```
Create a new Ubuntu server.
```

```
Restart my server.
```

---

## Networking

```
Create a firewall.
```

```
Assign a Floating IP.
```

---

## Storage

```
Create a new volume.
```

---

# Example Workflow

```
User

↓

Create a new cloud server

↓

MCP Client

↓

Hetzner MCP

↓

Authenticate

↓

Hetzner API

↓

Deploy Server

↓

Success Response

↓

AI Assistant

↓

Your cloud server has been created successfully.
```

---

# Proposed MCP Tools

## Cloud

| Tool | Description |
|------|-------------|
| list_servers | List cloud servers |
| get_server | Show server details |
| create_server | Create server |
| restart_server | Restart server |
| shutdown_server | Shutdown server |
| delete_server | Delete server |

---

## Networking

| Tool | Description |
|------|-------------|
| list_firewalls | List firewalls |
| create_firewall | Create firewall |
| list_networks | List private networks |
| assign_floating_ip | Assign floating IP |

---

## DNS

| Tool | Description |
|------|-------------|
| list_dns_zones | List DNS zones |
| list_dns_records | List DNS records |
| add_dns_record | Create DNS record |
| update_dns_record | Update DNS record |
| delete_dns_record | Delete DNS record |

---

# Suggested Directory Structure

```text
providers/hetzner/

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

- Cloud Servers
- Dedicated Servers
- Networking

## Phase 3

- Storage
- DNS
- Advanced Automation

---

# Contributing

Contributions are welcome.

Please submit a Pull Request or open an Issue.

---

# Disclaimer

This project is an independent community effort intended to explore MCP integrations for hosting platforms.

Hetzner is a trademark of its respective owner. This project is not affiliated with, endorsed by, or maintained by Hetzner unless explicitly stated.
