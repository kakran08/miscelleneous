# HTTP Status Codes Cheatsheet

HTTP status codes are categorized into **5 classes** based on the first digit of the code:

| Class          | Description                                      |
|----------------|--------------------------------------------------|
| **1xx**        | Informational: Request received, processing continues. |
| **2xx**        | Success: Request successfully received, understood, and accepted. |
| **3xx**        | Redirection: Additional action required to complete request. |
| **4xx**        | Client Error: Request contains bad syntax or cannot be fulfilled. |
| **5xx**        | Server Error: Server failed to fulfill a valid request. |

---

## 1xx: Informational Responses
| Code | Meaning                   | Description |
|------|---------------------------|-------------|
| 100  | **Continue**              | Request headers received, proceed to send body. |
| 101  | **Switching Protocols**   | Switching to a new protocol as requested. |
| 102  | **Processing**            | Request is being processed but no response yet. |
| 103  | **Early Hints**           | Preloads some headers before the final response. |

---

## 2xx: Successful Responses
| Code | Meaning                   | Description |
|------|---------------------------|-------------|
| 200  | **OK**                    | Standard success response. |
| 201  | **Created**               | Resource created successfully. |
| 202  | **Accepted**              | Request accepted but not processed yet. |
| 204  | **No Content**            | Request processed, no content to return. |
| 206  | **Partial Content**       | Partial resource delivered (e.g., for range requests). |

---

## 3xx: Redirection
| Code | Meaning                   | Description |
|------|---------------------------|-------------|
| 301  | **Moved Permanently**     | Resource permanently moved to a new URI. |
| 302  | **Found**                 | Temporary redirection to another URI. |
| 303  | **See Other**             | Resource found under another URI via GET. |
| 307  | **Temporary Redirect**    | Temporary redirect, same request method. |
| 308  | **Permanent Redirect**    | Permanent redirect, same request method. |

---

## 4xx: Client Errors
| Code | Meaning                   | Description |
|------|---------------------------|-------------|
| 400  | **Bad Request**           | Malformed request. |
| 401  | **Unauthorized**          | Authentication required or failed. |
| 403  | **Forbidden**             | Valid request, but action not allowed. |
| 404  | **Not Found**             | Resource not found. |
| 429  | **Too Many Requests**     | Client has sent too many requests. |

---

## 5xx: Server Errors
| Code | Meaning                   | Description |
|------|---------------------------|-------------|
| 500  | **Internal Server Error** | Generic server error. |
| 502  | **Bad Gateway**           | Invalid response from upstream server. |
| 503  | **Service Unavailable**   | Server overloaded or down for maintenance. |
| 504  | **Gateway Timeout**       | Upstream server failed to respond in time. |
| 511  | **Network Authentication Required** | Network access requires authentication. |

---

### Notes:
- **Unofficial Codes**: Some codes (e.g., `418 I'm a teapot`) are experimental or humorous.
- **Deprecated Codes**: Some codes (e.g., `102 Processing`) are no longer recommended for use.
- **WebDAV Specific**: Codes like `207 Multi-Status` and `423 Locked` are for WebDAV applications.

### Helpful Links:
- [RFC 7231: HTTP/1.1 Semantics](https://tools.ietf.org/html/rfc7231)
- [IANA HTTP Status Code Registry](https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml)


# Non-Standard HTTP Status Codes Cheat Sheet

## General Information
Non-standard HTTP status codes are used by specific systems or frameworks. They are not part of the official HTTP specification but can convey unique information.

---

## Non-Standard HTTP Status Codes

| **Code** | **Description** | **Usage**                                                                                     |
|----------|-----------------|-----------------------------------------------------------------------------------------------|
| 218      | This is fine    | Used by Apache servers for generic error conditions.                                          |
| 419      | Page Expired    | Laravel Framework - CSRF token missing or expired.                                            |
| 420      | Method Failure  | Spring Framework - Deprecated WebDAV status for failed methods.                               |
| 420      | Enhance Your Calm | Twitter API v1 - Client rate-limited.                                                       |
| 430      | Request Header Fields Too Large | Shopify - Deprecated, replaced by 429 Too Many Requests.                     |
| 430      | Security Rejection | Shopify - Signals a malicious request.                                                    |
| 450      | Blocked by Windows Parental Controls | Microsoft - Access blocked due to parental controls.                   |
| 498      | Invalid Token   | ArcGIS - Expired or invalid token.                                                            |
| 499      | Token Required  | ArcGIS - Token required but not provided.                                                     |
| 509      | Bandwidth Limit Exceeded | Apache/cPanel - Exceeded bandwidth limit.                                            |
| 529      | Site Overloaded | Qualys SSL Labs - Server cannot process the request.                                          |
| 530      | Site Frozen     | Pantheon - Inactive site.                                                                     |
| 530      | Origin DNS Error | Shopify - Cloudflare cannot resolve DNS record.                                              |
| 540      | Temporarily Disabled | Shopify - Endpoint temporarily disabled.                                                |
| 598      | Network Read Timeout | HTTP proxies - Network read timeout behind the proxy.                                     |
| 599      | Network Connect Timeout | HTTP proxies - Network connect timeout behind the proxy.                              |
| 783      | Unexpected Token | Shopify - JSON syntax error in request.                                                     |
| 999      | Non-standard    | LinkedIn - Access blocked or requires login.                                                 |

---

## Microsoft IIS Extensions

| **Code** | **Description**          | **Details**                                                                         |
|----------|--------------------------|-------------------------------------------------------------------------------------|
| 440      | Login Time-out           | Client session expired.                                                            |
| 449      | Retry With               | Missing required information from the client.                                       |
| 451      | Redirect                 | Exchange ActiveSync - Redirect to a more appropriate server.                        |

---

## Nginx Extensions

| **Code** | **Description**                 | **Details**                                                                        |
|----------|---------------------------------|------------------------------------------------------------------------------------|
| 444      | No Response                     | Server closes connection without a response.                                       |
| 494      | Request Header Too Large        | Header or request size exceeds limits.                                             |
| 495      | SSL Certificate Error           | Invalid client certificate provided.                                               |
| 496      | SSL Certificate Required        | Client certificate missing.                                                        |
| 497      | HTTP Request Sent to HTTPS Port | HTTP request sent to an HTTPS port.                                                |
| 499      | Client Closed Request           | Client closed the connection before the server responded.                          |

---

## Cloudflare Extensions

| **Code** | **Description**           | **Details**                                                                        |
|----------|---------------------------|------------------------------------------------------------------------------------|
| 520      | Web Server Unknown Error  | Unexpected response from the origin server.                                        |
| 521      | Web Server Is Down        | Cloudflare refused by the origin server.                                           |
| 522      | Connection Timed Out      | Timeout contacting the origin server.                                              |
| 523      | Origin Is Unreachable     | DNS records missing or incorrect.                                                  |
| 524      | A Timeout Occurred        | TCP connection made, but no timely HTTP response.                                  |
| 525      | SSL Handshake Failed      | SSL/TLS handshake failure.                                                         |
| 526      | Invalid SSL Certificate   | SSL certificate validation failed.                                                 |
| 527      | Railgun Error (obsolete)  | Deprecated - connection issue with Railgun server.                                 |

---

## AWS Elastic Load Balancing Codes

| **Code** | **Description**           | **Details**                                                                        |
|----------|---------------------------|------------------------------------------------------------------------------------|
| 000      | GOAWAY frame              | Header length exceeds limit or excessive requests.                                 |
| 460      | Client Closed Connection  | Client closed connection before idle timeout.                                      |
| 463      | Excessive IP Addresses    | X-Forwarded-For header contains >30 IPs.                                          |
| 464      | Protocol Version Mismatch | Incompatible versions between client and origin.                                   |
| 561      | Unauthorized              | Authentication failure with an identity provider (IdP).                           |

---

## Obsolete Caching Warning Codes

| **Code** | **Description**           | **Details**                                                                        |
|----------|---------------------------|------------------------------------------------------------------------------------|
| 110      | Response is Stale         | Cache content exceeds max age.                                                    |
| 111      | Revalidation Failed       | Cache unable to validate response with the origin server.                          |
| 112      | Disconnected Operation    | Cache operating without network connectivity.                                      |
| 113      | Heuristic Expiration      | Cache content older than 24 hours.                                                |
| 199      | Miscellaneous Warning     | Arbitrary warning text.                                                            |
| 214      | Transformation Applied    | Proxy applied transformations to the response.                                     |
| 299      | Persistent Warning        | Similar to 199 but persists.                                                       |

---

**See Also:**  
- Custom Error Pages  
- List of HTTP Header Fields  
- Common Log Format  
