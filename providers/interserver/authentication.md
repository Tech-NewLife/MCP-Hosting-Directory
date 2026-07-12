# Authentication

This document describes how clients authenticate when communicating with the InterServer API and provides guidance for MCP server integrations.

## Overview

Authentication ensures that only authorized users and applications can securely access InterServer resources and perform account operations.

InterServer currently supports two authentication methods:

- **API Key (Recommended)**
- **Session-based Authentication**

For MCP servers and other automated integrations, **API Key authentication is the recommended approach**.

---

## API Key Authentication (Recommended)

Authenticate by including your API key in the request header.

### Header

```http
X-API-KEY: YOUR_API_KEY
```

### Example Request

```bash
curl \
  -H "X-API-KEY: YOUR_API_KEY" \
  https://my.interserver.net/apiv2/account
```

### Advantages

- Recommended for automation and MCP servers
- No repeated login requests
- Easy to integrate
- Suitable for long-running applications

---

## Session Authentication

InterServer also supports session-based authentication.

Typical workflow:

1. Authenticate using the login endpoint.
2. Receive a session ID.
3. Include the session ID in subsequent requests.

Example:

```http
sessionid: YOUR_SESSION_ID
```

Session authentication is generally better suited for interactive applications rather than automated services.

---

## Obtaining an API Key

1. Log in to **My InterServer**.
2. Navigate to **Account Security**.
3. Generate a new API Key.
4. Store the key securely.
5. Never expose your API key in public repositories or client-side applications.

### Environment Variable Example

```bash
export INTERSERVER_API_KEY="your_api_key"
```

or

```env
INTERSERVER_API_KEY=your_api_key
```

---

## Base API Endpoint

```
https://my.interserver.net/apiv2
```

---

## Example HTTP Request

```http
GET /account HTTP/1.1
Host: my.interserver.net
X-API-KEY: YOUR_API_KEY
Accept: application/json
```

---

## Authentication Errors

| Status Code | Description |
|-------------|-------------|
| **401 Unauthorized** | Missing or invalid API key or session. |
| **403 Forbidden** | Authentication succeeded, but permission is denied. |
| **429 Too Many Requests** | API rate limit exceeded. |

---

## Security Best Practices

- Always use HTTPS.
- Never commit API keys to source control.
- Store credentials in environment variables or a secure secrets manager.
- Rotate API keys periodically.
- Grant only the minimum permissions required.
- Revoke compromised credentials immediately.
- Avoid embedding credentials directly in application code.
- Never log API keys or session IDs.

---

## MCP Integration Recommendations

For MCP server implementations:

- Prefer **API Key authentication** over session authentication.
- Read the API key from an environment variable.
- Handle authentication failures gracefully.
- Retry transient API failures using exponential backoff.
- Keep credentials outside of source code.
- Follow the principle of least privilege when granting API access.

---

## Official Resources

- **My InterServer Login Portal**  
  https://my.interserver.net/login.php

- **How to Login or Access my.interserver.net**  
  https://www.interserver.net/tips/kb/login-access-interserver-net/

- **InterServer API Documentation**  
  https://my.interserver.net/api-docs/

- **InterServer Knowledge Base**  
  https://www.interserver.net/tips/

- **InterServer FAQ**  
  https://my.interserver.net/faq.php

---

## References

This document is based on the official InterServer API documentation and authentication guidance. Authentication methods, endpoints, and features may change over time. Always refer to the official documentation for the most up-to-date information.
