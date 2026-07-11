# OVHcloud MCP

> An MCP (Model Context Protocol) server specification for integrating AI assistants with OVHcloud cloud and dedicated infrastructure.

**Status:** 🚧 Planned

---

# Overview

OVHcloud MCP aims to provide a secure interface between AI assistants and the OVHcloud platform, allowing users to manage cloud infrastructure, dedicated servers, networking, and hosted services using natural language.

Instead of manually navigating the OVHcloud Control Panel, users can simply ask an AI assistant to provision resources, manage servers, configure networking, or monitor infrastructure.

---

# Why OVHcloud MCP?

OVHcloud provides a broad range of cloud and infrastructure services including:

- Public Cloud
- VPS
- Dedicated Servers
- Bare Metal Cloud
- Managed Kubernetes
- Object Storage
- Block Storage
- Load Balancers
- Networking
- Domains
- DNS
- Email Hosting

An MCP server makes these services accessible through AI assistants while maintaining secure authentication and permission controls.

---

# Goals

The OVHcloud MCP project aims to:

- Simplify cloud infrastructure management
- Reduce repetitive administrative tasks
- Enable AI-powered infrastructure automation
- Standardize cloud operations using MCP

---

# Planned Features

## Cloud Infrastructure

### Information

- List Cloud Instances
- Instance Details
- CPU Usage
- Memory Usage
- Storage Usage
- Public IP Addresses

### Management

- Create Instance
- Restart Instance
- Shutdown Instance
- Delete Instance
- Resize Instance

---

## Dedicated Servers

- List Servers
- Hardware Information
- Reboot Server
- Power Cycle
- Rescue Mode

---

## Networking

- Floating IPs
- Load Balancers
- Private Networks
- Firewalls

---

## Storage

- Object Storage
- Block Storage
- Snapshots

---

## Domains & DNS

- List Domains
- DNS Zones
- Create DNS Records
- Update DNS Records
- Delete DNS Records

---

# Authentication

OVHcloud MCP should support secure authentication using:

- API Keys
- Access Tokens
- OAuth (if available)

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
Show my cloud instances.
```

```
Deploy a new Ubuntu server.
```

```
Restart my VPS.
```

---

## Networking

```
Assign a Floating IP.
```

```
Create a firewall.
```

---

## Domains

```
Show my DNS records.
```

```
Create an MX record.
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

OVHcloud MCP

↓

Authenticate

↓

OVHcloud API

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

## Cloud

| Tool | Description |
|------|-------------|
| list_instances | List cloud instances |
| get_instance | Show instance details |
| create_instance | Create cloud instance |
| restart_instance | Restart instance |
| shutdown_instance | Shutdown instance |
| delete_instance | Delete instance |

---

## Dedicated Servers

| Tool | Description |
|------|-------------|
| list_servers | List dedicated servers |
| reboot_server | Reboot server |
| rescue_server | Enable rescue mode |

---

## DNS

| Tool | Description |
|------|-------------|
| list_dns | List DNS zones |
| add_dns_record | Create DNS record |
| update_dns_record | Update DNS record |
| delete_dns_record | Delete DNS record |

---

# Suggested Directory Structure

```text
providers/ovhcloud/

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

- Cloud Infrastructure
- Dedicated Servers
- Networking

## Phase 3

- Storage
- Domains
- DNS
- Advanced Automation

---

# Contributing

Contributions are welcome.

Please submit a Pull Request or open an Issue.

---

# Disclaimer

This project is an independent community effort intended to explore MCP integrations for hosting platforms.

OVHcloud is a trademark of its respective owner. This project is not affiliated with, endorsed by, or maintained by OVHcloud unless explicitly stated.
