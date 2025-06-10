# 📋 API Security Testing Checklist

A structured approach to testing APIs for security vulnerabilities.  
**Note:** Always obtain proper authorization before testing.

---

## 🔍 **1. Information Gathering**
- [ ] Identify API endpoints (e.g., `/api/v1/users`, `/graphql`).
- [ ] Review API documentation (Swagger/OpenAPI, Postman collections).
- [ ] Check for exposed debug endpoints (e.g., `/debug`, `/test`).
- [ ] Enumerate HTTP methods (`GET`, `POST`, `PUT`, `DELETE`, `PATCH`).
- [ ] Identify authentication mechanisms (JWT, OAuth, API keys).

---

## 🛡️ **2. Authentication & Authorization**
- [ ] Test for **broken authentication**:
  - [ ] Weak API keys or default credentials.
  - [ ] JWT issues (expired/algo=none/weak secrets).
  - [ ] OAuth misconfigurations (token leakage, insecure redirects).
- [ ] Test for **broken object-level authorization (BOLA/IDOR)**:
  - [ ] Manipulate IDs in requests (e.g., `/api/user/123` → `/api/user/456`).
  - [ ] Check if UUIDs/IDs are predictable.
- [ ] Test for **excessive data exposure** (e.g., API returns hidden fields like `"isAdmin":true`).

---

## 🕳️ **3. Input Validation & Injection**
- [ ] **SQLi** (e.g., `user_id=1' SLEEP(5)--`).
- [ ] **NoSQLi** (e.g., `{"username":{"$ne":"foo"}}`).
- [ ] **Command Injection** (e.g., `; ls -la` in input fields).
- [ ] **SSRF** (e.g., `url=http://internal-server`).
- [ ] **XXE** (if XML is accepted).
- [ ] Test for **mass assignment** (e.g., adding `"role":"admin"` in JSON).

---

## 🔗 **4. Business Logic Flaws**
- [ ] Test for **rate limiting bypass** (e.g., brute-forcing logins).
- [ ] Check if **price manipulation** is possible (e.g., `"price":0.01`).
- [ ] Test for **replay attacks** (reusing tokens/requests).
- [ ] Verify **workflow bypasses** (e.g., skipping payment steps).

---

## 🗃️ **5. Data Exposure & Misconfigurations**
- [ ] Check for **sensitive data leaks** (PII, tokens in headers/logs).
- [ ] Test for **CORS misconfigurations**:
  - [ ] `Access-Control-Allow-Origin: *` with credentials.
- [ ] Review **HTTP headers** (missing `HSTS`, `X-Content-Type-Options`).
- [ ] Test for **verbose error messages** (leaking stack traces).

---

## ⚙️ **6. Other Tests**
- [ ] Test **WebSockets** (if used) for auth/data leaks.
- [ ] Check **GraphQL** for introspection queries or batch attacks.
- [ ] Verify **file uploads** (malicious files, directory traversal).
- [ ] Test **cache poisoning** (e.g., manipulating `X-Forwarded-Host`).

---



---

🔐 **References:**  
- [OWASP API Security Top 10](https://owasp.org/www-project-api-security/)  
- [PortSwigger API Testing Guide](https://portswigger.net/web-security/api-security)

 ---

> ⚠️ **Disclaimer:** Use this checklist only on applications you have permission to test.
