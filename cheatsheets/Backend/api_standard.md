# API Standards & Security

## HTTP Response Codes
- **200 OK**: Success.
- **201 Created**: Successful creation (POST).
- **204 No Content**: Success but no body (DELETE).
- **400 Bad Request**: Client-side error.
- **401 Unauthorized**: Missing or invalid authentication.
- **403 Forbidden**: Authenticated but lacks permissions.
- **404 Not Found**: Resource doesn't exist.
- **500 Internal Server Error**: Server-side crash.

## Authentication (JWT)
- **Header**: Algorithm & token type.
- **Payload**: Data (user ID, expiration).
- **Signature**: Verify sender & ensure no changes.

## Security Checklist
- [ ] Use HTTPS everywhere.
- [ ] Sanitize and validate all inputs (prevent XSS/SQLi).
- [ ] Use `helmet` for secure HTTP headers.
- [ ] Implement rate limiting.
- [ ] Never store secrets in code; use `.env` files.
- [ ] Implement CORS correctly.
- [ ] Keep dependencies updated.

## RESTful Best Practices
- Use nouns, not verbs: `/users` instead of `/getUsers`.
- Use plural: `/items/123`.
- Nested resources: `/users/1/posts`.
- Use appropriate methods (GET, POST, PUT, DELETE).
- Version your API: `/v1/users`.
