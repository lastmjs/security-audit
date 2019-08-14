# Security Audit

Web application security audit to be performed once per quarter.

- [ ] Review latest OWASP Top 10
- [ ] Run automatic security checks
  - [ ] Mozilla Observatory: https://observatory.mozilla.org
  - [ ] Google CSP Evaluator: https://csp-evaluator.withgoogle.com/
  - [ ] Security header scanner: https://securityheaders.com/
  - [ ] Lighthouse (Chrome dev tools)
- [ ] Ensure encryption of data in transit (force SSL connections everywhere possible)
- [ ] Ensure encryption of data at rest (databases, harddrives, passwords, etc should be encrypted)
- [ ] Update all dependencies
  - [ ] Use LTS versions (Node.js, Ubuntu, etc)
- [ ] No vulnerabilities found in dependencies (GitHub and npm security reports, etc)
- [ ] Lock down ports (tcp, udp, etc)
  - [ ] Only open ports that are absolutely necessary
  - [ ] Only open the smallest subset of absolutely necessary IP addresses on each port
- [ ] Ensure strong authentication system
  - [ ] Study up on the latest authentication best practices
  - [ ] up-to-date and secure
  - [ ] Cookies, JWTs, private and public keys, web storage, etc all used correctly
- [ ] Ensure strong authorization system
  - [ ] Study up on the latest authorization best practices
  - [ ] Automated tests to ensure data integrity
  - [ ] Physical/logistical access controls should be in place (locking screens, not sharing passwords, etc)
- [ ] Analyze all endpoints and ensure proper authentication and authorization 
  - [ ] All processes that are accessible through tcp/ip ports should be audited to ensure each endpoint has proper           - [ ] Analyze the types of operations, reads or writes, that are permitted
- [ ] Rotate all keys
  - [ ] public and private keys
  - [ ] secrets
  - [ ] passwords (minimum of 10 characters in length)
- [ ] All cryptographic algorithms up-to-date (i.e. do not use sha1)
  - [ ] For example, use a good hashing algorithm
  - [ ] For example, choose a proper ECDSA curve
- [ ] Ensure physical integrity of all keys
  - [ ] You must be able to physically access all keys
  - [ ] Consider having multiple physical locations for each key (these cannot be lost)
  - [ ] Know where all keys are stored (laptop, USB drive, environment variables, cloud storage, safes, etc)

- [ ] Review organizational access control policies (Review organizational access control policies such as who has access to what data, password length, password lifetimes, access to secret keys, password sharing, screen locking, proper data sharing channels (Gmail, Slack, Excel) etc)
- [ ] Sanitize data (Health data, credit card data, and other types of sensitive data with compliance requirements should never be stored in our systems anywhere, unless we can store them compliantly. If we are storing that data, we should track it down and delete it. We should also build the functionality to stop storing the data. Personal data should be deleted over time as it becomes unneeded.)
- [ ]  Revoke access to terminated employees (Review all user accounts. Anyone who is not currently an employee should be completely removed from our system so that they no longer have access to any sensitive data or functionality. Check our database, GitLab, Gmail, Twilio, Stripe, Slack, etc)
- [ ] Review compliance with regulations (Make sure we are compliant with HIPAA, PCI, GDPR, etc)
- [ ] Audit the audit (Take some time to study the latest security best practices. Ensure that our audit process is up-to-date and will lead to sufficient security. Clean up the issue, change wording, add audits, etc.)
- [ ] New audit to add: Ensure proper logging and monitoring. We don't really have a good way of knowing what attacks are taking place on our system, no alarms or anything to notify us of breaches
