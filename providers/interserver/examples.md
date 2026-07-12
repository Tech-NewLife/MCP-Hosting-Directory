# Examples

This page provides practical examples of how to authenticate and interact with the InterServer API. These examples are intended as a starting point for developers building MCP servers, automation scripts, and custom integrations.

---

# Prerequisites

Before using the API, ensure you have:

- An active InterServer account
- A valid API Key
- HTTPS access to the InterServer API
- Basic knowledge of REST APIs

Base API URL:

```
https://my.interserver.net/apiv2
```

---

# Public Endpoint Example (No Authentication Required)

Some API endpoints are publicly accessible and do not require authentication.

### Test API Availability

```bash
curl https://my.interserver.net/apiv2/info
```

This endpoint can be used to verify API connectivity before generating an API key.

---

# API Key Authentication

Authenticate by including your API key in the request header.

### Header

```http
X-API-KEY: YOUR_API_KEY
```

---

# Example 1 – Get Account Information

```bash
curl \
  -H "X-API-KEY: YOUR_API_KEY" \
  https://my.interserver.net/apiv2/account
```

---

# Example 2 – Using Environment Variables

Store your API key securely.

```bash
export INTERSERVER_API_KEY="YOUR_API_KEY"
```

Use it in requests:

```bash
curl \
  -H "X-API-KEY: $INTERSERVER_API_KEY" \
  https://my.interserver.net/apiv2/account
```

---

# Example 3 – Python

```python
import os
import requests

API_KEY = os.getenv("INTERSERVER_API_KEY")

headers = {
    "X-API-KEY": API_KEY,
    "Accept": "application/json"
}

response = requests.get(
    "https://my.interserver.net/apiv2/account",
    headers=headers
)

print(response.status_code)
print(response.json())
```

---

# Example 4 – JavaScript (Node.js)

```javascript
const axios = require("axios");

const apiKey = process.env.INTERSERVER_API_KEY;

axios.get("https://my.interserver.net/apiv2/account", {
    headers: {
        "X-API-KEY": apiKey,
        "Accept": "application/json"
    }
})
.then(response => {
    console.log(response.data);
})
.catch(error => {
    console.error(error.response?.data || error.message);
});
```

---

# Example 5 – PHP

```php
<?php

$apiKey = getenv("INTERSERVER_API_KEY");

$curl = curl_init();

curl_setopt_array($curl, [
    CURLOPT_URL => "https://my.interserver.net/apiv2/account",
    CURLOPT_RETURNTRANSFER => true,
    CURLOPT_HTTPHEADER => [
        "Accept: application/json",
        "X-API-KEY: $apiKey"
    ]
]);

$response = curl_exec($curl);

curl_close($curl);

echo $response;
```

---

# Example 6 – PowerShell

```powershell
$headers = @{
    "Accept" = "application/json"
    "X-API-KEY" = $env:INTERSERVER_API_KEY
}

Invoke-RestMethod `
    -Uri "https://my.interserver.net/apiv2/account" `
    -Headers $headers `
    -Method Get
```

---

# Example 7 – Session Authentication

InterServer also supports session-based authentication.

```http
sessionid: YOUR_SESSION_ID
```

This authentication method is generally intended for interactive applications.

---

# Example Response

```json
{
  "success": true,
  "text": "Ok"
}
```

---

# Common Headers

```http
Accept: application/json
X-API-KEY: YOUR_API_KEY
```

---

# Common HTTP Status Codes

| Code | Meaning |
|------|---------|
| 200 | Success |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Resource Not Found |
| 422 | Validation Failed |
| 429 | Too Many Requests |
| 500 | Internal Server Error |

---

# API Service Categories

The InterServer API provides access to a wide range of services, including:

- Account Management
- Backups
- Billing
- DNS
- Domains
- Floating IPs
- Licenses
- Mail
- QuickServers
- SSL Certificates
- Support Tickets
- VPS
- Web Hosting
- Dedicated Servers

---

# API Key Rotation

InterServer provides an endpoint for rotating (regenerating) your API key.

> **Important**
>
> Rotating an API key immediately invalidates the previous key. Update all applications, scripts, and MCP servers before using the new key.

---

# Two-Factor Authentication (2FA)

The API includes endpoints for enrolling and managing Time-based One-Time Password (TOTP) authenticators, such as Google Authenticator, to improve account security.

---

# Security Best Practices

- Always use HTTPS.
- Store API keys in environment variables.
- Never commit credentials to Git repositories.
- Rotate API keys periodically.
- Grant only the minimum permissions required.
- Never expose API keys in client-side code.
- Avoid logging sensitive authentication information.
- Handle API errors gracefully.

---

# MCP Integration Example

A typical MCP server workflow is:

1. Read the API key from an environment variable.
2. Authenticate using the `X-API-KEY` header.
3. Send requests to the InterServer API.
4. Parse the JSON response.
5. Handle authentication failures and rate limits.
6. Log errors without exposing credentials.

---

# Interactive API Documentation

Explore and test API endpoints using the official interactive documentation:

- Swagger UI
- Scalar
- ReDoc
- Stoplight Elements

Documentation:

https://my.interserver.net/api-docs/

---

# Related Documentation

- [Authentication](authentication.md)
- https://my.interserver.net/api-docs/
- https://my.interserver.net/login.php
- https://www.interserver.net/tips/
- https://my.interserver.net/faq.php

---

# References

This document is based on the official InterServer API documentation and authentication guidance. Authentication methods, available endpoints, and features may evolve over time. Always refer to the official InterServer documentation for the latest information and implementation details.
