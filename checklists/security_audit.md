# 🛡️ Rapid Security Audit Checklist

## 🔑 Authentication & Authorization
- [ ] Are passwords hashed using a strong algorithm (e.g., bcrypt)?
- [ ] Is JWT secret stored in an environment variable?
- [ ] Does every protected route have an authorization check?
- [ ] Are session tokens revoked on logout?

## 📥 Input Validation
- [ ] Are all inputs validated (Zod/Joi)?
- [ ] Is the application protected against SQL Injection (ORM or param queries)?
- [ ] Are inputs sanitized to prevent XSS?

## 🌐 Headers & CORS
- [ ] Is `helmet` used to set secure HTTP headers?
- [ ] Is CORS configured to allow only specific origins?
- [ ] Are `HttpOnly` and `Secure` flags set on cookies?

## 📦 Dependencies
- [ ] Have you run `npm audit` recently?
- [ ] Are there any unmaintained or known-vulnerable packages?

## 🚀 Environment
- [ ] Is `NODE_ENV` set to `production`?
- [ ] Are debug modes disabled in production?
