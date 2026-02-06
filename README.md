# Task 13 – Secure API Testing & Authorization Validation

## Objective
The objective of this task is to understand REST API security, test authentication and authorization mechanisms, identify common API security weaknesses, and map findings to OWASP API security risks.

---

## Tools Used
- Postman
- cURL
- Insomnia

---

## Understanding REST APIs
REST APIs allow applications to communicate using HTTP methods such as:

| Method | Purpose |
|---|---|
| GET | Retrieve data |
| POST | Create data |
| PUT | Update data |
| DELETE | Remove data |

APIs are widely used in mobile apps, web apps, and cloud services.

---

## API Security Testing Methodology

### 1. API Configuration
Configured API requests using:
- Endpoint URL
- Headers (Authorization tokens)
- Request body
- Query parameters

---

### 2. Authentication Testing
Tested API behavior using:
- Valid credentials
- Invalid credentials
- Missing authentication headers

Goal: Verify if unauthorized access is blocked.

---

### 3. Authorization Testing
Modified resource identifiers to check if users can access:
- Other users’ data
- Restricted resources

Goal: Detect broken authorization issues.

---

### 4. Input Validation Testing
Sent:
- Unexpected values
- Large payloads
- Invalid formats

Goal: Check input validation and error handling.

---

### 5. Rate Limiting Testing
Sent multiple rapid requests to verify if:
- API limits repeated requests
- Abuse protection exists

---

### 6. Response Analysis
Checked:
- HTTP response codes
- Error messages
- Data exposure in responses

---

## Observed Security Risks

| Issue | Risk |
|---|---|
| Weak authentication | Unauthorized access |
| Broken authorization | Data exposure |
| Poor input validation | Injection attacks |
| No rate limiting | API abuse |
| Verbose error messages | Information leakage |

---

## OWASP API Risk Mapping

| Finding | OWASP API Risk |
|---|---|
| Missing authentication | API2: Broken Authentication |
| Broken authorization | API1: Broken Object Level Authorization |
| No rate limiting | API4: Lack of Resources & Rate Limiting |
| Input validation issues | API8: Injection |
| Excessive data exposure | API3: Excessive Data Exposure |

---

## Security Recommendations

- Implement strong authentication (JWT, OAuth2)
- Enforce authorization checks
- Validate all inputs
- Enable rate limiting
- Use proper error handling
- Encrypt sensitive data

---

## Ethical Considerations
All API testing performed:
- On authorized or test APIs
- For educational purposes only
- Without targeting production systems

---

## Summary
This task improved understanding of:
- API authentication and authorization
- Secure API design principles
- OWASP API security risks
- API security testing methodology

---

## Final Outcome
Developed the ability to test APIs for common security misconfigurations and authorization flaws.

---

## Sources & References

1. OWASP API Security Top 10  
https://owasp.org/www-project-api-security/

2. OWASP API Security Risks Documentation  
https://owasp.org/API-Security/

3. Postman Learning Center  
https://learning.postman.com/docs/getting-started/introduction/

4. REST API Security Best Practices  
https://www.cloudflare.com/learning/security/api/what-is-api-security/

5. PortSwigger API Testing Guide  
https://portswigger.net/web-security/api-testing
