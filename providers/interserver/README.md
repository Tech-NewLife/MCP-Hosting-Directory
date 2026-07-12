# InterServer MCP

> Community-maintained documentation and proposed tool mappings for the available InterServer MCP Server and Management API.

**Official InterServer MCP status:** ✅ Available  
**This repository:** 📖 Community documentation and proposed mappings

> [!IMPORTANT]
> InterServer provides an MCP Server and Management API.
> This repository is an independent community reference and is not affiliated with, endorsed by, or maintained by InterServer.

------------------------------------------------------------------------

# Overview

InterServer MCP aims to provide a secure interface between AI assistants
and the InterServer platform, allowing users to manage hosting services,
cloud resources, and Marketplace applications using natural language.

Instead of manually navigating the control panel, users can simply ask
an AI assistant to perform common hosting tasks such as restarting a
VPS, managing DNS records, checking invoices, deploying Marketplace
applications, or opening support tickets.

------------------------------------------------------------------------

# Why InterServer MCP?

InterServer provides a broad range of hosting and infrastructure
services that are well suited for AI-driven automation, including:

-   Linux VPS
-   Windows VPS
-   Dedicated Servers
-   Shared Hosting
-   Domains
-   DNS Management
-   Email Hosting
-   Billing
-   Technical Support
-   Cloud Marketplace Applications

One of InterServer's standout features is the **Cloud Marketplace**,
which allows users to deploy popular applications with minimal setup. An
MCP server can extend this capability by allowing AI assistants to
deploy and manage Marketplace applications through natural language.

------------------------------------------------------------------------

# Goals

The InterServer MCP project aims to:

-   Simplify hosting and infrastructure management
-   Automate repetitive administrative tasks
-   Provide AI-powered server operations
-   Standardize hosting automation using MCP
-   Demonstrate practical MCP integrations for hosting providers

------------------------------------------------------------------------

# Available and Proposed Capabilities

# InterServer Cloud Marketplace

## Application Discovery

-   List Marketplace Applications
-   Search Applications
-   View Application Details
-   Browse by Category

### Example Marketplace Applications

#### Content Management

-   Nextcloud
-   MediaWiki
-   MicroWeber Website Builder

#### Development

-   Node.js
-   MongoDB Community Edition

#### Networking & Infrastructure

-   NetBird Server
-   MooseFS
-   NirvaShare
-   Octelium

#### Game Servers

-   Minecraft (Vanilla)
-   Minecraft (Forge)
-   Minecraft (PaperSpigot)

### Deployment

-   Deploy Application
-   Restart Application
-   Stop Application
-   Remove Deployment
-   View Deployment Status
-   View Deployment Logs
-   View Resource Usage

------------------------------------------------------------------------

# VPS Management

## Information

-   List VPS
-   VPS Details
-   Resource Usage
-   Operating System
-   Assigned IP Addresses
-   Hostname
-   Bandwidth Usage

## Power Operations

-   Restart VPS
-   Shutdown VPS
-   Power On VPS
-   Force Reboot

## Administration

-   Reset Root Password
-   Change Hostname
-   Reinstall Operating System
-   View Console Information

------------------------------------------------------------------------

# Dedicated Servers

## Information

-   List Servers
-   Hardware Specifications
-   Public IP Addresses
-   Bandwidth Usage

## Power

-   Reboot Server
-   Power Cycle
-   Shutdown

------------------------------------------------------------------------

# Shared Hosting

## Account

-   List Hosting Accounts
-   Disk Usage
-   Bandwidth Usage
-   PHP Version
-   SSL Status

## Management

-   Suspend Account
-   Unsuspend Account
-   Reset Password
-   View Account Information

------------------------------------------------------------------------

# Domain Management

-   List Domains
-   Register Domain
-   Renew Domain
-   Transfer Domain
-   Domain Lock
-   WHOIS Information
-   Expiry Date

------------------------------------------------------------------------

# DNS Management

Supported Record Types:

-   A
-   AAAA
-   CNAME
-   MX
-   TXT
-   CAA
-   SRV
-   PTR

Supported Actions:

-   List Records
-   Create Record
-   Edit Record
-   Delete Record

------------------------------------------------------------------------

# Billing

-   List Services
-   List Invoices
-   Outstanding Balance
-   Payment History
-   Renew Services
-   Upgrade Services

------------------------------------------------------------------------

# Support

-   Create Ticket
-   View Tickets
-   Reply to Ticket
-   Close Ticket
-   Search Knowledgebase

------------------------------------------------------------------------

# Email

-   List Mailboxes
-   Create Mailbox
-   Delete Mailbox
-   Reset Password
-   Manage Forwarders

------------------------------------------------------------------------

## Authentication

Verified InterServer Management API authentication methods:

- API key using the `X-API-KEY` header
- Session-based authentication

Additional authentication methods should only be listed when verified in current official InterServer documentation.

------------------------------------------------------------------------

# Security

-   Require authentication
-   Use HTTPS
-   Respect account permissions
-   Log administrative actions
-   Support read-only and administrative modes
-   Never expose sensitive credentials

------------------------------------------------------------------------

# Example Prompts

## Marketplace

    Show Marketplace applications.

    Deploy Nextcloud.

    Deploy MongoDB Community Edition.

    Restart my Marketplace deployment.

## VPS

    Restart my VPS.

    Show my VPS list.

## DNS

    Show DNS records for example.com.

    Create an A record.

## Billing

    Show unpaid invoices.

## Support

    Create a support ticket.

------------------------------------------------------------------------

# Example Workflow

    User

    ↓

    Deploy Nextcloud

    ↓

    MCP Client

    ↓

    InterServer MCP

    ↓

    Authenticate

    ↓

    InterServer API

    ↓

    Marketplace

    ↓

    Deploy Application

    ↓

    Success Response

    ↓

    AI Assistant

    ↓

    Nextcloud has been deployed successfully.

------------------------------------------------------------------------

# Proposed MCP Tools

## Marketplace

| Tool | Description |
|------|-------------|
| list_marketplace_apps | List Marketplace applications |
| deploy_marketplace_app | Deploy application |
| list_deployments | List deployments |
| restart_application | Restart deployment |
| remove_application | Delete deployment |
| application_logs | View logs |

---

## VPS

| Tool | Description |
|------|-------------|
| list_vps | List VPS |
| get_vps | VPS details |
| restart_vps | Restart VPS |
| shutdown_vps | Shutdown VPS |
| poweron_vps | Power on VPS |
| reinstall_vps | Reinstall OS |
| reset_password | Reset password |

---

## DNS

| Tool | Description |
|------|-------------|
| list_dns | List DNS records |
| add_dns_record | Create record |
| update_dns_record | Update record |
| delete_dns_record | Delete record |

---

## Billing

| Tool | Description |
|------|-------------|
| list_services | List services |
| list_invoices | List invoices |
| renew_service | Renew service |

---

## Support

| Tool | Description |
|------|-------------|
| list_tickets | View tickets |
| create_ticket | Create ticket |
| reply_ticket | Reply to ticket |

------------------------------------------------------------------------

# Suggested Directory Structure

``` text
providers/interserver/

README.md
api.md
installation.md
authentication.md
examples.md
roadmap.md
```

------------------------------------------------------------------------

# Development Roadmap

## Phase 1

-   Research APIs
-   Define MCP tools
-   Authentication model
-   Documentation

## Phase 2

-   Marketplace
-   VPS
-   Billing
-   Support

## Phase 3

-   DNS
-   Domains
-   Shared Hosting

## Phase 4

-   Dedicated Servers
-   Email Management
-   Advanced Automation

------------------------------------------------------------------------

# Contributing

Contributions are welcome.

You can help by:

-   Improving documentation
-   Adding API endpoints
-   Creating MCP tool definitions
-   Writing installation guides
-   Sharing prompt examples

Please open an Issue or submit a Pull Request.

------------------------------------------------------------------------

# Disclaimer

This project is an independent community effort intended to explore MCP
integrations for hosting platforms.

InterServer is a trademark of its respective owner. This project is not
affiliated with, endorsed by, or maintained by InterServer unless
explicitly stated.
