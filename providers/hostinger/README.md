# Hostinger MCP

> An MCP (Model Context Protocol) server specification for integrating AI assistants with Hostinger hosting services.

**Status:** 🚧 Planned

---

# Overview

Hostinger MCP aims to provide a secure interface between AI assistants and the Hostinger platform, allowing users to manage hosting services using natural language.

Instead of manually navigating hPanel, users can simply ask an AI assistant to perform common hosting tasks such as managing websites, domains, email accounts, DNS records, and hosting settings.

---

# Why Hostinger MCP?

Hostinger provides a wide range of hosting services including:

- hPanel
- Shared Hosting
- Cloud Hosting
- VPS
- WordPress Hosting
- Domains
- Email Hosting
- DNS Management

An MCP server makes these services accessible through AI assistants while maintaining secure authentication and permission controls.

---

# Goals

The Hostinger MCP project aims to:

- Simplify hosting management
- Automate repetitive administrative tasks
- Provide AI-powered website management
- Standardize hosting automation using MCP

---

# Planned Features

## Hosting Management

### Information

- List Hosting Accounts
- Disk Usage
- Bandwidth Usage
- PHP Version
- SSL Status

### Management

- Reset Hosting Password
- Change PHP Version
- Enable SSL
- View Website Information

---

## Domain Management

- List Domains
- Register Domain
- Renew Domain
- Transfer Domain
- WHOIS Information

---

## DNS Management

Supported record types:

- A
- AAAA
- CNAME
- MX
- TXT
- CAA
- SRV

Supported actions:

- List Records
- Create Record
- Edit Record
- Delete Record

---

## Email Management

- List Mailboxes
- Create Mailbox
- Delete Mailbox
- Reset Password
- Configure Forwarders

---

# Authentication

Hostinger MCP should support secure authentication using:

- API Token
- OAuth (if available)
- Session Authentication

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

## Hosting

```
Show my hosting accounts.
```

```
Check my website disk usage.
```

```
Enable SSL for my website.
```

---

## Domains

```
List my domains.
```

```
Renew my domain.
```

---

## Email

```
Create a new mailbox.
```

```
Reset my email password.
```

---

# Example Workflow

```
User

↓

Create a new email account

↓

MCP Client

↓

Hostinger MCP

↓

Authenticate

↓

Hostinger API

↓

Create Mailbox

↓

Success Response

↓

AI Assistant

↓

Your email account has been created successfully.
```

---

# Proposed MCP Tools

## Hosting

| Tool | Description |
|------|-------------|
| list_hosting | List hosting accounts |
| get_hosting | Show hosting details |
| enable_ssl | Enable SSL |
| reset_hosting_password | Reset hosting password |

---

## Domains

| Tool | Description |
|------|-------------|
| list_domains | List domains |
| renew_domain | Renew domain |
| transfer_domain | Transfer domain |

---

## DNS

| Tool | Description |
|------|-------------|
| list_dns | List DNS records |
| add_dns_record | Create DNS record |
| update_dns_record | Update DNS record |
| delete_dns_record | Delete DNS record |

---

## Email

| Tool | Description |
|------|-------------|
| list_mailboxes | List mailboxes |
| create_mailbox | Create mailbox |
| reset_email_password | Reset email password |

---

# Suggested Directory Structure

```text
providers/hostinger/

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

- Hosting Management
- Domains
- Email

## Phase 3

- DNS Management
- VPS Support
- Advanced Automation

---

# Contributing

Contributions are welcome.

Please submit a Pull Request or open an Issue.

---

# Disclaimer

This project is an independent community effort intended to explore MCP integrations for hosting platforms.

Hostinger is a trademark of its respective owner. This project is not affiliated with, endorsed by, or maintained by Hostinger unless explicitly stated.
